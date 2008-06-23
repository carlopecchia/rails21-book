## JSON

Ora Rails accetta le richieste POST con contenuto JSON. Ad esempio, potete inviare una richiesta POST in questo modo:

	POST /posts
	{"post": {"title": "Breaking News"}}

Tutto verrà salvato nella variabile **params**. Ad esempio:

	def create
	  @post = Post.create params[:post]
	  # …
	end

Per chi non lo sapesse JSON è un "concorrente" di XML, ed è molto usato per lo scambio dati in JavaScript, dato che viene rappresentato in questo linguaggio. Prende il suo nome da: **JavaScript Object Notation**.
