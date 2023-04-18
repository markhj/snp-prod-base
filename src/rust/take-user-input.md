[
  id: rust-take-user-input
  tags:
  locations:
]: #

# Take user input

````rust
use std::io::{self, Write};

fn main() {
    print!("Enter name: ");
    io::stdout().flush().unwrap();

    let mut input = String::new();
    let stdin = io::stdin();

    stdin.read_line(&mut input).unwrap();

    println!("Hello, {} ", input);
}
````