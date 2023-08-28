tags:: Zig, Formation
alias:: Ziglings
link:: https://github.com/ratfactor/ziglings
[[Aug 28th, 2023]]
***

- ↳ [[Programming/Zig]] 
  {{namespace Programming/Zig/Ziglings}}
  ***
- Fonctions
	- Privée --> Défaut
		- ```zig
		  fn main() void {
		      std.debug.print("Hello world!\n", .{});
		  }
		  ```
	- Publique --> Prefixe `pub`
		- ```zig
		  pub fn main() void {
		      std.debug.print("Hello world!\n", .{});
		  }
		  ```
- #comptime indique que l'évaluation est réalisée à la compilation
- `const` permet d'indiquer qu'une expression est évaluée à #comptime
	- `const std = @import("std");`
	- `const foo: u8 = 20;`
- `var` permet d'indiquer qu'une expression est une variable mutable
	- `var bar: u8 = 20;`
- Le type est déclaré en utilisant `:`
	- `var n: u8 = 50;`
	- `const pi: u32 = 314159;`
- Tableaux
	- Type explicite
		- `var foo: [3]u32 = [3]u32{ 42, 108, 5423 };`
	- Type déduit par le compilateur
		- `var foo = [_]u32{ 42, 108, 5423 };`
	- Addition de tableaux --> `++` #comptime
	- Multiplication de tableaux --> `**` #comptime
		- `const d = [_]u8{ 1,2,3 } ** 2; // equals 1 2 3 1 2 3`
	-