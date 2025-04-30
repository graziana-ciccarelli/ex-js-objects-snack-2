## Code question 1

Nel codice le variabili Hamburger e  secondHamburger fanno riferimento allo stesso oggetto e se modifichiamo le proprietà di secondHamburger, viene modificato lo stesso oggetto a cui punta anche hamburger. Quindi, quando stampiamo hamburger.name e secondHamburger.name, entrambe ci restituiranno in console "Double Cheese Burger". Questo perché si tratta di una copia di riferimento, ovvero non viene crerata una copia dell'oggetto, ma ci sarà solo un oggetto in memoria che ha cambiato le sue proprietà.

## Code question 2

In questo caso quando cerchiamo di fare una copia dell'oggetto, si tratta una copia superficiale perché le proprietà come il peso e il nome vengono veramente copiate con l'utilizzo dell' operatore spread, ma la lista di array con gli ingredienti non viene copiata. Questo perché viene copiato solamente il collegamento a quella lista. In poche parole, sia l'originale che la copia condividono la stessa lista che è in memoria, che se viene modificata nella copia , verrà modificata anche nell'originale. Quindi avremo due oggetti distinti in memoria, che condividono lo stesso array di ingredienti e di conseguenza entrambi stamperanno "Salad" in console.

## Code question 3

In questo codice vengono creati 3 oggetti. Si tratta  di una copia profonda perché viene fatta una copia completa dell'oggetto e tutti gli oggetti annidati dentro, grazie allo structuredClone che ci permette di gestire oggetti complessi. Questa volta ogni oggetto è completamente indipendente da hamburger e non condividono nessun riferimento a dati interni.

