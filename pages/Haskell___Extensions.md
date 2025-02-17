tags:: Haskell
link:: [Languages extensions](https://ghc.gitlab.haskell.org/ghc/doc/users_guide/exts/intro.html)
[[Jul 24th, 2023]]
***

- Permet d'étendre et/ou modifier le comportement du compilateur ou la syntaxe
- [The implicit Prelude import](https://ghc.gitlab.haskell.org/ghc/doc/users_guide/exts/rebindable_syntax.html)
	- `NoImplicitPrelude` permet de ne pas charger de bibliothèque par défaut
- [Duplicate record fields](https://downloads.haskell.org/~ghc/9.2.1/docs/html/users_guide/exts/duplicate_record_fields.html)
	- Permet aux *records* de partager un même nom pour un attribut
		- Évite un conflit dans l'espace de nom global
	- ```haskell
	  {-# LANGUAGE DuplicateRecordFields #-}
	  
	  data Person = Person { name :: String }
	  data Company = Company { name :: String, owner :: Person }
	  ```
- [Overloaded record dot](https://downloads.haskell.org/~ghc/9.2.1/docs/html/users_guide/exts/overloaded_record_dot.html)
  id:: 64be48d5-126b-4c7b-9811-10dc9f228444
	- Permet d'utiliser la notation `instance.attribut` pour accéder à un attribut de l'instance
		- Expérience similaire à une notation OOP
	- ```haskell
	  {-# LANGUAGE OverloadedRecordDot #-}
	  {-# LANGUAGE DuplicateRecordFields #-}
	  
	  data Person = Person { name :: String }
	  data Company = Company { name :: String, owner :: Person }
	  
	  main = do
	    let c = Company { name = "Acme Corp."
	                    , owner = Person { name = "Wile E. Coyote" } }
	    print $ c.name ++ " is run by " ++ c.owner.name
	  ```
- [No Field selectors](https://ghc.gitlab.haskell.org/ghc/doc/users_guide/exts/field_selectors.html#extension-FieldSelectors)
	- Supprime les méthodes auto-générées permettant d'accéder aux attributs
		- Utile pour ne pas polluer l'espace global
		- Utile en combinaison avec ((64be48d5-126b-4c7b-9811-10dc9f228444))
	- ```haskell
	  data Foo = MkFoo { bar :: Int }
	  ```
		- `bar :: Foo -> Int` accessible
	- ```haskell
	  {-# LANGUAGE NoFieldSelectors #-}
	  
	  data Foo = MkFoo { bar :: Int }
	  ```
		- `bar :: Foo -> Int` **non** accessible
-