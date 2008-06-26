##Ottenere informazioni su un plugin

Questa è una delle novità di Rails 2.1 che probabilmente non avete mai utilizzato. Dico "probabilmente" perché in alcuni casi molto specifici può essere utile, ad esempio, conoscere la versione di un plugin.

Per testarlo, occorre creare un nuovo file chiamato *about.yml* nella directory plgin, contenente qualcosa del genere:

	author: Carlos Brando
	version: 1.2.0
	description: A description about the plugin
	url: http://www.nomedojogo.com

Possiamo accedere a queste informazioni così:

	plugin = Rails::Plugin.new(plugin_directory)
	plugin.about["author"] # => “Carlos Brando”
	plugin.about["url"] # => “http://www.nomedojogo.com”

Se trovate qualche uso utile di questa feature e vorreste condividerla con noi, forse cambieremmo la nostra opinione sulla sua utilità.
