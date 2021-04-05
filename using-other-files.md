# Using other files for functions
Assume two files. One is the `main.rs` file with the `main()` method. Other is a file named `utils.rs`.  
<b>Make sure both `main.rs` and `utils.rs` are under the same directory</b>
Contents are as below:  
### `utils.rs`
```
pub fn print_msg(msg: String){
    println!("{}", msg);
}
```
### Usage in `main.rs`
```
mod utils;      // Import the file

fn main() {
    // create a String
    let ship = "Starship";
    let msg = format!("The space ship {} is {} meters tall.", ship, 50);

    // pass the String
    utils::print_msg(msg);
}
```
> The space ship Starship is 50 meters tall.

