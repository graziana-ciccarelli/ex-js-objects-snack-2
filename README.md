## Code question 1 (snack-1). Senza lanciare il codice, riesci a prevedere cosa viene stampato in console?; Quanti oggetti sono stati creati in memoria durante l'esecuzione di questo codice?

Nel codice le variabili Hamburger e  secondHamburger fanno riferimento allo stesso oggetto e se modifichiamo le proprietà di secondHamburger, viene modificato lo stesso oggetto a cui punta anche hamburger. Quindi, quando stampiamo hamburger.name e secondHamburger.name, entrambe ci restituiranno in console "Double Cheese Burger". Questo perché si tratta di una copia di riferimento, ovvero non viene crerata una copia dell'oggetto, ma ci sarà solo un oggetto in memoria che ha cambiato le sue proprietà.

## Code question 2 (snack-2). Senza lanciare il codice, riesci a prevedere cosa viene stampato in console?; Quanti oggetti sono stati creati in memoria durante l'esecuzione di questo codice?

In questo caso quando cerchiamo di fare una copia dell'oggetto, si tratta una copia superficiale perché le proprietà come il peso e il nome vengono veramente copiate con l'utilizzo dell' operatore spread, ma la lista di array con gli ingredienti non viene copiata. Questo perché viene copiato solamente il collegamento a quella lista. In poche parole, sia l'originale che la copia condividono la stessa lista che è in memoria, che se viene modificata nella copia , verrà modificata anche nell'originale. Quindi avremo due oggetti distinti in memoria, che condividono lo stesso array di ingredienti e di conseguenza entrambi stamperanno "Salad" in console.

## Code question 3 (snack-3). Quanti oggetti sono stati creati in memoria durante l'esecuzione di questo codice?

In questo codice vengono creati 3 oggetti. Si tratta  di una copia profonda perché viene fatta una copia completa dell'oggetto e tutti gli oggetti annidati dentro, grazie allo structuredClone che ci permette di gestire oggetti complessi. Questa volta ogni oggetto è completamente indipendente da hamburger e non condividono nessun riferimento a dati interni.

## Code question 4 (snack-4). Qual è il metodo migliore per clonare l’oggetto chef, e perché? Qual è il metodo migliore per clonare l’oggetto restaurant, e perché?

Nel caso dell'oggetto chef non possiamo utilizzare né il metodo structuredClone né il metodo JSON.parse(JSON.stringify ()), questo perché entrambi non sono in grado di copiare le funzioni (in questo caso la funzione  makeBurger verrebbe persa). Quindi l'unica cosa che potremmo fare per clonare l'oggetto è quella di farlo manualmente. Per quanto riguarda l'oggetto restaurant il metodo più adatto per clonarlo è quello di utilizzare il metodo structuredClone perché è in grado di gestire oggetti annidati, date (perché vengono clonate come oggetto Date e non come stringa), valori booleani , stringhe e numeri.