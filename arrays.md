# Arrays
### Defining an array
```
let arr = ['a', 'c', 's', 'q', 'y', 'c'];
```
Or, we can also specify the size of th array while creation
```
let arr: [char;6];
arr = ['a', 'c', 's', 'q', 'y', 'c'];
  // Or simply: let arr: [char;6] = ['a', 'c', 's', 'q', 'y', 'c'];
```
The size and number of elements must be same.

### Print all elements
```
println!("{:?}", arr);
```
> ['a', 'c', 's', 'q', 'y', 'c']

### Length of array
```
println!("Length of the array is: {}", arr.len());
```
> Length of the array is: 6

### Accessing specific elements of array
```
println!("The third element of the array is: {}", arr[2]);
```
> The third element of the array is: s

### Looping over array elements
Syntax is `for <element-name> in &<array-name>`.
```
arr = ['a', 'c', 's', 'q', 'y', 'c'];
let mut word = String::from("");
for e in &arr {
  word.push(*e);
}
println!("word formed: {}", word);
```
> word formed: acsqyc

### Slicing arrays
Syntax is `&<array-name>[<start_index>..<end_index>]`
```
let slice = &arr[2..5];
println!("slice is: {:?}", slice);
println!("slice length: {}", slice.len());
```
> slice is: ['s', 'q', 'y']  
> slice length: 3  

### Size of array in bytes
```
println!("Size in bytes: {}", std::mem::size_of_val(&arr));
```
> Size in bytes: 24
