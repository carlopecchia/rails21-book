## session(:on)

Probabilmente non ne siete a conoscenza, ma in Rails è possibile disattivare le sessioni:

	class ApplicationController < ActionController::Base
	  session :off
	end

Da notare che nell'esempio sono state disattivate le sessioni per tutti i controller (**ApplicationController**), possiamo fare la stessa cosa per un singolo controller.

Ma se volessi abilitare le sessioni per un solo controller? In Rails 2.1 il metodo accetta l'opzione **:on**:

	class UsersController < ApplicationController
	  session :on
	end
