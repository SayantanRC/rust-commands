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
println!("Trait: {0:?}. Hex of {3} is {3:x}. Second arg is {2}. Binary of {1} is {1:b}.", (12, true), 24, "aaa", 10);
```
