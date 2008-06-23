## action\_name

Per conoscere da quale action è stata chiamata la vostra view, ora potete semplicemente usare il metodo  **action\_name** :

	<%= action_name %>

Il valore restituito sarà lo stesso restituito da  **params[:action]**, ma il codice risulterà più elegante.
