## Metodo caches\_page condizionale

Ora il metodo **caches\_page** accetta l'opzione condizionale (**:if**). Ad esempio:

	# In Rails 2.0
	caches_page :index

	# In Rails 2.1 potete usare l'opzione :if
	caches_page :index, :if => Proc.new { |c| !c.request.format.json? }
