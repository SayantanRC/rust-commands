# Print commands
### Simple println
```
println!("a string");
```
> a string
### Print with variables
```
let ship = "Starship";
println!("The space ship {} made by {}, is {} meters tall", ship, "SpaceX", 50);
```
> The space ship Starship made by SpaceX, is 50 meters tall
### Print with position
Useful for re-using an argument multiple times.
```
let ship = "Starship";
println!("The space ship {0} made by {1}, is {2} meters tall. {0} is a very good ship.", ship, "SpaceX", 50);
```
> The space ship Starship made by SpaceX, is 50 meters tall. Starship is a very good ship.
### Print with name
```
println!("The space ship {ship} is {height} meters tall.", ship = "Starship", height = 50);
```
> The space ship Starship is 50 meters tall.
### Equivalent expression
```
println!("10 + 10 is {}", 10 + 10);
println!("Is it 20? {}", 10 + 10 == 20);
```
> 10 + 10 is 20
> Is it 20? true
### Print debug trait
Print multiple things at once.
```
let a_variable = true;
println!("{:?}", (122, "text", a_variable));
```
> (122, "text", true)
### Print binary, hexa-decimal, octal values
```
println!("{:x} {:b} {:o}", 12, 332, 20);
```
> c 101001100 24

x - hexadecimal  
b - binary  
o - octal  
```
let a_number = 24;
println!("Trait: {0:?}. Hex of {3} is {3:x}. Second arg is {2}. Binary of {1} is {1:b}.", (12, true), a_number, "aaa", 10);
```
> Trait: (12, true). Hex of 10 is a. Second arg is aaa. Binary of 24 is 11000.
