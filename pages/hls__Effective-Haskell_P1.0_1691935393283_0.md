file:: [Effective-Haskell_P1.0_1691935393283_0.pdf](../assets/Effective-Haskell_P1.0_1691935393283_0.pdf)
file-path:: ../assets/Effective-Haskell_P1.0_1691935393283_0.pdf
[[Aug 13th, 2023]] 
***

- ![Viewer](../assets/Effective-Haskell_P1.0_1691935393283_0.pdf) | [PDF](../assets/Effective-Haskell_P1.0_1691935393283_0.pdf)
  ***
- #+BEGIN_QUERY
 :title [:h2 "Title"]
 :query [
         :find (pull ?b [*])
         :where

          [?b :block/properties ?properties]

          [(get ?properties :type) ?type]


          (or
             [(= ?type "book")]
             [(contains? ?type "book")]
            )
         ]
#+END_QUERY
