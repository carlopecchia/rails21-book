## flash.now anche nei test

Chi di noi non ha avuto dei malditesta a causa di questo? Il problema era che durante i test non potevamo confermare se un messaggio venisse salvato in flash, questo perché flash veniva pulito da Rails prima di lanciare il vostro script di test.

In rails 2.1 questo problema è stato risolto. Ora potete scrivere linee di codice come questa nei vostri test:

	assert_equal '>value_now<', flash['test_now']
