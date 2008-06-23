## Specificare il file per le routes

In Rails 2.1 potete definire dove si trova la configurazione delle route, includendo la seguente line di codice nel vostro *enviroment.rb*:

	config.routes_configuration_file

Questo può essere utile quando avete due front-end separati che condividono gli stessi moduli, librerie e plugin.

Ad esempio, getsatisfaction.com e api.getsatisfaction.com condividono gli stessi modelli, ma non i controller, gli helper e le view.
getsatisfaction.com ha il suo file delle route ottimizzate per i motori di ricerca (SEO), mentre il file delle route delle API non ha bisogno di tali ottimizzazioni.
