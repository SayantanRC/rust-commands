# Variables and Types

## Declaring mutable types
All above declarations are for immutable variables, i.e they cannot be changed.  
To create a mutable variable, specify `mut`
```
let mut a = 5;
a = 10;
```

## Following types are valid:  
- <b>u8, u16, u32, u64</b> - unsigned integer of 8 bit, 16 bit, 32 bit, 64 bit respectively
- <b>i8, i16, i32, i64</b> - signed integer
- <b>f32, f64</b> - floating point numbers (fractional numbers)
- <b>bool</b> - Boolean type, only `true` or `false`
- <b>char</b> - a single character (alphabet, number, unicode etc)

### Find type of a variable
The following function needs to be defined.
```
fn get_type_of<T>(_: &T) -> String {
    return format!("{}", std::any::type_name::<T>());
}
```
This can then be used as:
```
let i = 333;
let f = 33.3;
let type_i = get_type_of(&i);
let type_f = get_type_of(&f);
println!("Type of {} is {}", i, type_i);
println!("Type of {} is {}", f, type_f);
```
> Type of 333 is i32  
> Type of 33.3 is f64  

### Default for numbers
As is evident from the above example,
- Non fractional numbers : `i32`
- Fractional numbers : `f64`

### Explicit declaring of variables
```
let i: i64 = 333;
println!("Type is {}", i, type_i);
```
> Type is i64

### Max size of a type
```
println!("max size of i32 is {}", std::i32::MAX);
println!("max size of i64 is {}", std::i64::MAX);
println!("max size of f32 is {}", std::f32::MAX);
println!("max size of f64 is {}", std::f64::MAX);
```
> max size of i32 is 2147483647  
> max size of i64 is 9223372036854775807  
> max size of f32 is 340282350000000000000000000000000000000  
> max size of f64 is 179769313486231570000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000  

### Example
```
let i = 333;
let f = 33.3;
let b = true;
let c = 'q';
let emoji: char = '\u{1F600}';
let str = "a string";
println!("{:?}", (i, f, b, c, emoji, str));
```
> (333, 33.3, true, 'q', '😀', "a string")
