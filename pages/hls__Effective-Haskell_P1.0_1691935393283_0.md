file:: [Effective-Haskell_P1.0_1691935393283_0.pdf](../assets/Effective-Haskell_P1.0_1691935393283_0.pdf)
file-path:: ../assets/Effective-Haskell_P1.0_1691935393283_0.pdf
[[Aug 13th, 2023]] 
***

- ![Viewer](../assets/Effective-Haskell_P1.0_1691935393283_0.pdf) | [PDF](../assets/Effective-Haskell_P1.0_1691935393283_0.pdf)
  ***
- Minimal style for some queries #minimal-query
  #+BEGIN_QUERY
  {
  :query [:find (pull ?p [*])
  :where
  [?b :block/page ?p]
  (page-property ?p :type "Book")
  ]
  :breadcrumb-show? false
  :result-transform (fn [r] r)}
  }
  #+END_QUERY
