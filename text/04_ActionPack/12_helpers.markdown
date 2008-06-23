## Utilizzare gli helper fuori dalle view

Quante volte avreste voluto utilizzare un **helper** anche all'interno del vostro controller? Per far ciò dovevamo includere il modulo **helper** all'interno del **controller**, ma questo sporcava il codice.

Per Rails 2.1 è stato sviluppato un proxy per permettere di accedere agli helper fuori dalle view. Il suo funzionamento è molto semplice:

 	# Per accedere, ad esempio, al metodo simple_format method
	ApplicationController.helpers.simple_format(text)

Facile e pulito!