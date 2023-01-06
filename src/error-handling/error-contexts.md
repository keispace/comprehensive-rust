# Adding Context to Errors

[anyhow](https://docs.rs/anyhow/) 크레이트는 오류에 대한 상황정보를 추가하기 위해 널리 사용되며 사용자 정의 오류 유형을 줄일 수 있습니다: 
> The widely used [anyhow](https://docs.rs/anyhow/) crate can help you add
> contextual information to your errors and allows you to have fewer
> custom error types:

```rust,editable,compile_fail
use std::{fs, io};
use std::io::Read;
use thiserror::Error;
use anyhow::{Context, Result};

#[derive(Error, Debug)]
enum ReadUsernameError {
    #[error("Found no username in {0}")]
    EmptyUsername(String),
}

fn read_username(path: &str) -> Result<String> {
    let mut username = String::with_capacity(100);
    fs::File::open(path)
        .context(format!("Failed to open {path}"))?
        .read_to_string(&mut username)
        .context("Failed to read")?;
    if username.is_empty() {
        return Err(ReadUsernameError::EmptyUsername(String::from(path)))?;
    }
    Ok(username)
}

fn main() {
    //fs::write("config.dat", "").unwrap();
    match read_username("config.dat") {
        Ok(username) => println!("Username: {username}"),
        Err(err)     => println!("Error: {err:?}"),
    }
}
```
