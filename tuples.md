# Tuples
### Creating tuple
```
let tuple = ("aaa", 56, true);
```
OR
```
let tuple: (&str, i32, bool) = ("aaa", 56, true);
```

### Printing all elements of tuple by debug trait
```
println!("{:?}", tuple);
```
> ("aaa", 56, true)

### Accessing specific elements of tuple
```
println!("0: {}, 1: {}, 2: {}", tuple.0, tuple.1, tuple.2);
```
> 0: aaa, 1: 56, 2: true

### Looping on tuple elements
Not possible

### Length of a tuple
Not possible
