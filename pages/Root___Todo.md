- #+BEGIN_QUERY
  {:title [:h2 "Test query"]
   :query [:find (pull ?b [*])
           :where
           [?b :block/properties ?p]
           [(get ?p "type") ?t]
           [(= "Video" ?t)]]
   :view (fn [result]
           (when (seq result)
             (let [blocks (flatten result)]
               [:div.table-wrapper
                [:table.table-auto
                 [:thead
                  [:tr
                   [:th {:width "20%"} "Name"]
                   [:th {:width "20%"} "Creator"]
                   [:th {:width "60%"} "Description"]]]
                 [:tbody
                  (for [{:block/keys [title properties]} blocks]
                    [:tr
                     [:td (second (:url (second (first title))))]
                     [:td (get properties "type")]
                     [:td (get properties "type")]])]]])))
   }
  #+END_QUERY
-
-
# Tâches en cours
	- {{query (todo todo now later doing)}}
	  query-table:: true
	  query-properties:: [:page :link :tags :block]