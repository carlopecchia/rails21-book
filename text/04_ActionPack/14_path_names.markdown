## Path Names

I lettori del mio blog (http://www.nomedojogo.com) conosceranno il mio plugin **Custom Resource Name**. Penso che morirà presto... :( 

In rails era possibile includere l'opzione **:as** nelle route (cosa che ho implemetato nel mio plugin per mantenere la compatibilità), ed ora è possibile specificare l'opzione **:path\_names** per personalizzare il nome delle **action**.
	
	map.resource :schools, :as => 'escolas', :path_names => { :new => 'nova' }

Comunque, il mio plugin continuerà ad essere utile a coloro che utilizzano una versione precedente di Rails.
