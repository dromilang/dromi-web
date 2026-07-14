# Usare WDromi

## Importarlo

Crea un file `main.js` e importiamo WDromi, aggiungendo questa riga:

```javascript
import { runDromi } from "https://dromilang.github.io/WDromi/dromi-v1.1/wdromi.js";
```

Se vorresti usare un'altro link, vedi [Supporto alle versioni](/dromi-web/support).

---

## Funzioni

La funzione principal è `runDromi`. Essa ha due paramentri:

- `line` - Il codice che vogliamo eseguire
- `out` - dove deve essere eseguito (di defalut nella console)

Scrivi questo:

```javascript
runDromi("print('WDromi')");
```

Salva il file e crea `index.html` con questo:

```html
<!DOCTYPE html>
<script src="main.js" type="module"></script>
</html>
```

> Non dimenticarti di inserire `type="module"` nel tag dello script. Se non ce l'hai, WDromi non si importerebbe.
> Inoltre per far funzionare questo dovrai usare un webserver.

Ora aprilo in un browser e premi `F12` e clicca "Console". Dovresti vedere `WDromi` nella console.

---

## Usare un `out` personalizzato

Di defalut esegue nella console, ma vorresti vederlo a schermo. Puoi modificare il paramentro `out` per far andare l'output dove vuoi. Ad esempio:

```javascript
let doOut = document.getElementById("output");

runDromi("print('WDromi')", doOut);
```