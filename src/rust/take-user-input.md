[
  id: rust-take-user-input
  tags:
  locations:
]: #

# Take user input

Import:

````rust
use std::io;
````

Add where you want the functionality:

````rust
println!("Enter name: ");

let mut input = String::new();
let stdin = io::stdin();

stdin.read_line(&mut input).unwrap();

println!("\nHello, {} ", input);
````
