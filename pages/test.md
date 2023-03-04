- [[Clojure]]
  type:: programming_lang
  creator:: [[Rich Hickey]]
  description:: Clojure is a dialect of Lisp, and shares with Lisp the code-as-data philosophy and a powerful macro system.
- [[Erlang]]
  type:: programming_lang
  creator:: [[Joe Armstrong]]
  description:: Erlang is a programming language used to build massively scalable soft real-time systems with requirements on high availability.
- #+BEGIN_QUERY
  {:title [:h2 "Programming languages list"]
   :query [:find (pull ?b [*])
           :where
           [?b :block/properties ?p]
           [(get ?p "type") ?t]
           [(= "programming_lang" ?t)]]
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
                     [:td (get properties "creator")]
                     [:td (get properties "description")]])]]])))
   }
  #+END_QUERY
-