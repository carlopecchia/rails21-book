## Stringhe formattate come titolo

Il metodo **String#titleize** conteneva un bug quando lo si applicava a stringhe contenenti 's. Questo bug faceva si che il metodo ritornasse 's maiuscolo. Vediamo l'esempio:

	>> "brando’s blog".titleize
	=> "Brando’S Blog"

Vediamo lo stesso esempio, dopo la correzione del bug:

	>> "brando’s blog".titleize
	=> "Brando’s Blog"
