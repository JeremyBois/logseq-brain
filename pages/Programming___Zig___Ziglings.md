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
- `const` permet d'indiquer qu'une expression est évaluée à la compilation
	- `const std = @import("std");`
-