tags:: #DSL #Logseq 
link:: [Github](https://github.com/weavejester/hiccup)
[[Mar 8th, 2023]]

- # Introduction
	- Bibliothèque [[Closure]] pour générer simplement du [[HTML]]
		- [Utilisable dans Logseq](https://docs.logseq.com/#/page/hiccup)
- # Cours
- ## Hiccup Lightning Tutorial
	- type:: Article
	  author:: #[[Iwo Herka]]
	  link:: https://medium.com/makimo-tech-blog/hiccup-lightning-tutorial-6494e477f3a5)
	- ```closure
	  [:div
	    [:button#counter-btn
	      {:class "btn active"
	       :style {:padding 5}
	       :on-click (fn [e] (swap! counter inc))}
	      "Click me!"]]
	  ```
	- ```html
	  <div>
	      <button class="btn active"
	              id="counter-btn"
	              style="padding: 5px;">
	          Click me!
	      </button>
	  </div>
	  
	  <!-- add also JavaScript code for
	       the event listener -->
	  ```
-