tags:: Zig, Formation
alias:: Ziglings, Programmation/Zig/Ziglings
link:: https://github.com/ratfactor/ziglings
[[Aug 28th, 2023]]
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
		- `const c = a ++ b ++ [_]u8{ 5 };`
	- Multiplication de tableaux --> `**` #comptime
		- `const d = [_]u8{ 1,2,3 } ** 2; // equals 1 2 3 1 2 3`
	- `usize` est le type idiomatique pour les indices
		- `const x: usize = 1;`
		- Sa taille dépend de l'architecture [[Électronique/CPU]]
	- `undefined` permet l'initialisation sans ajouter de valeurs
		- `var lang: [3]u8 = undefined;`
- Boucles
	- `for (<item array>) |item| { <do something with item> }`
	- `for (leet) |n| {std.debug.print("{}", .{n});}`
	- Boucle `while` avec expression de continuation
		- `while (expression) : (continuation) { corps de la fonction}`
		- `while (n <= 20) : (n += 1) {}`
- Strings
	- Possible de construire des string multi lignes avec `\\`
		- ```zig
		  const lyrics =
		      \\Ziggy played guitar
		      \\Jamming good with Andrew Kelley	
		      \\And the Spiders from Mars
		  ;
		  ```
- `if` / `else`
	- Utilise uniquement des booléens pour les tests
		- Pas de types ni de coercions
		- ```zig
		  if (foo) {
		          // We want our program to print this message!
		          std.debug.print("Foo is 1!\n", .{});
		      } else {
		          std.debug.print("Foo is not 1!\n", .{});
		      }
		  ```
- Erreurs
	- Une erreur est une enumération du type `error`
		- `const MyNumberError = error{TooSmall};`
	- Utilise des unions de types pour retourner soit la valeur soit l'erreur
		- `var my_number: MyNumberError!u8 = 5;`
			- Omission du type possible si il peut être déduit automatiquement
			- ```zig
			  fn addTwenty(n: u32) !u32 {
			      if (n < 5) {
			          return MyNumberError.TooSmall;
			      } else {
			          return n + 20;
			      }
			  }
			  ```
		- Similaire au `Either` en [[Haskell]]
	- Une erreur peut être interompue avec `catch` `try`
		- `canFail() catch |err| return err;`
		- `try canFail();`

