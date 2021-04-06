# Strings
Strings can be made using two ways.
1. `let a = "aaaaa";` - The type of `a` is `&str`
2. `let a = Strings::from("aaaaa");` - The type of `a` is `String`

### Pushing in a string.
<b>The String variable must be mutable type.</b>
```
let mut a = String::from("aaaaa");
```
1. Push a character
   ```
   a.push('!');
   println!("{}", a);
   ```
   > aaaaa!
2. Push another string
   ```
   a.push_str("bbbbb");
   println!("{}", a);
   ```
   > aaaaa!bbbbb

### Length and capacity
- To find length - `<string_name>.len()`  
- To find capacity - `<string_name>.capacity()`  
When a String is made, it is made with some capacity. It is the space allocated to the String in bytes. 
The actual length of the String can be smaller than the capacity. Capacity is not a hard limit. 
As more characters are added, i.e. as the length increases, the capacity also increases. 
Often times the capacity becomes double of previous capacity when the length exceeds the capacity.  

#### Examples on capacity
```
let mut a_string = String::from("Starship is a next gen spaceship.");
println!("{}. Capacity: {}. Length: {}", a_string, a_string.capacity(), a_string.len());
```
> Starship is a next gen spaceship.. Capacity: 33. Length: 33
```
a_string.push_str(" It is made by SpaceX.");
println!("{}. Capacity: {}. Length: {}", a_string, a_string.capacity(), a_string.len());
```
> Starship is a next gen spaceship. It is made by SpaceX.. Capacity: 66. Length: 55

<i>Note how the capacity increases to double of previous.</i>
```
a_string.push_str(" It will be used to make humans interplanetary.");
println!("{}. Capacity: {}. Length: {}", a_string, a_string.capacity(), a_string.len());
```
> Starship is a next gen spaceship. It is made by SpaceX. It will be used to make humans interplanetary.. Capacity: 132. Length: 102

### Defining a String by capacity
```
let mut another_str = String::with_capacity(5);
  // Designed for 5 bytes
another_str.push_str("Stars");
  // pushed 5 bytes. Length and capacity should be 5 now.
```
> Stars. Capacity: 5. Length: 5
```
another_str.push_str("hip");
  // adding more characters.
println!("{}. Capacity: {}. Length: {}", another_str, another_str.capacity(), another_str.len());
  // capacity will now be increased for the extra characters.
```
> Starship. Capacity: 10. Length: 8

### Checking if a String contains something
```
let mut a_string = String::from("Starship is a next gen spaceship.");
// check if "Star" is present in the String
println!("{}", a_string.contains("Star"));
```
> true
```
// case sensitive. "star" does not work.
println!("{}", a_string.contains("star"));
```
> false

### Replace in a String
```
let mut a_string = String::from("Starship is a next gen spaceship.");
println!("{}", a_string.replace("next gen", "huge"));
  // the above replace does not change the original String
println!("{}", a_string);
```
> Starship is a huge spaceship.  
> Starship is a next gen spaceship.  

<b>NOTE: The original string remains unaffected even if it is mutable.</b>

#### Replace with another String variable
The same replace can be done by -
```
let mut a_string = String::from("Starship is a next gen spaceship.");
let word = String::from("huge");
println!("{}", a_string.replace("next gen", &word));
```

### Looping over words in a String
```
let mut a_string = String::from("Starship is a next gen spaceship.");
for word in a_string.split_whitespace() {
  println!("Found word: {}", word)
}
```
> Found word: Starship  
> Found word: is  
> Found word: a  
> Found word: next  
> Found word: gen  
> Found word: spaceship.  

### Change case
- Lower case: `<string-name>.to_lowercase()`  
- Upper case: `<string-name>.to_uppercase()`  
These two menthods change some special characters as well. Example, `to_lowercase()` converts 'Σ' to 'σ'.  
To avoid processing special characters and only consider english alphabets, use `to_ascii_lowercase()` and `to_ascii_uppercase()` methods.
