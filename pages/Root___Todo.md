- #+BEGIN_QUERY
  {:title [:h2 "Test query"]
   :query [:find (pull ?b [*])
           :where
           [?b :block/properties ?p]
           [(get ?b "type") ?t]
           [(= "Video" ?t)]]
   }
  #+END_QUERY
-
-
# Tâches en cours
	- {{query (todo todo now later doing)}}
	  query-table:: true