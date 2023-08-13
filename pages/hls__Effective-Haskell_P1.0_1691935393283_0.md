file:: [Effective-Haskell_P1.0_1691935393283_0.pdf](../assets/Effective-Haskell_P1.0_1691935393283_0.pdf)
file-path:: ../assets/Effective-Haskell_P1.0_1691935393283_0.pdf
[[Aug 13th, 2023]] 
***

- ![Viewer](../assets/Effective-Haskell_P1.0_1691935393283_0.pdf) | [PDF](../assets/Effective-Haskell_P1.0_1691935393283_0.pdf)
  ***
- #+BEGIN_QUERY
{
:title [:h2 "My books"]
:query [:find (pull ?b [*])
:where
[?b :block/page ?p]
(page-property ?p :parent "Haskell")
]
:collapsed? false
:breadcrumb-show? false
}
#+END_QUERY
