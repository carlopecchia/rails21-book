## caches\_action condizionale

Ora il metodo **caches\_action** accetta l'opzione **:if**, consentendo l'utilizzo di espressioni condizionali per specificare quando una **action** potrà essere salvata in **cache**. Ad esempio:

	caches_action :index, :if => Proc.new { |c| !c.request.format.json? }

Nell'esempio, il metodo **action index** sarà salvato in **cache** solo se non verrà chiamato da una richiesta JSON.
