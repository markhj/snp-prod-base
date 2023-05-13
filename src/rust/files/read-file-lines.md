[
  id: rust-files-read-lines
  tags:
  locations:
]: #

# Read lines from a file

````rust
let file = File::open("/path/to/file").expect("Failed to load file");
let reader = BufReader::new(file);
for line in reader.lines() {
    // ...
}
````
