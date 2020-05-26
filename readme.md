## what is dynamic route in Vue?

[Getting Started | Vue Router](https://router.vuejs.org/guide/#html)

你可以在router obj中的routes陣列中，去定義每個route的obj
裡面吃的屬性包括path, 要連到的component等等
如果path裡面有像是:var, 這個var就是可以動態調整

像是`path: '/user/:username/post/:post_id',`
你的router link tag就可以用to="/user/Erin/post/2"
或是用 to="/user/Ben/post/23"，都可以，所以說是動態

另外，你也可以透過$route.params.username和
$route.params.post_id在vue實例內拿到數值

另一種在tag內的寫法是`:to="{ name: 'home-tag', params: { tag } }`
這樣你還可以把參數傳進去
