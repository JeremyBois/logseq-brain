file:: [Effective-Haskell_P1.0_1691935393283_0.pdf](../assets/Effective-Haskell_P1.0_1691935393283_0.pdf)
file-path:: ../assets/Effective-Haskell_P1.0_1691935393283_0.pdf
[[Aug 13th, 2023]] 
***

- ![Viewer](../assets/Effective-Haskell_P1.0_1691935393283_0.pdf) | [PDF](../assets/Effective-Haskell_P1.0_1691935393283_0.pdf)
  ***
- Minimal style for some queries  #minimal-query
  query-sort-by:: block
  query-table:: true
  query-sort-desc:: false
  #+BEGIN_QUERY
  {
  :query [:find (pull ?b [*])
  :where
  (task ?b #{"TODO" "DOING"})
  
  [?b :block/page ?p]
  (page-property ?p :type "Book")
  ]
  
  :collapsed? false
  :breadcrumb-show? true
  }
  #+END_QUERY