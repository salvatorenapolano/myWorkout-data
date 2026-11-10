# myWorkout-data

I dati che l'app **myWorkout** scarica da internet: scheda, dieta, lista della spesa e immagini.
Nell'app: cerchio del profilo in alto a destra → **Scarica gli ultimi dati**.

```
assets/data/workout_plan.json     la scheda (giorni, esercizi, serie, recuperi)
assets/data/exercises.json        la libreria esercizi (descrizioni, consigli, video)
assets/data/diet.json             la dieta settimanale
assets/data/shopping.json         la lista della spesa
assets/images/exercises/<id>.svg  anteprima di ogni esercizio
assets/images/muscles/<nome>.webp illustrazioni dei muscoli
```

## Come si aggiorna

- **Dal sito di GitHub**: apri un file, matita ✏️, modifica, *Commit changes*. Il messaggio del commit
  compare nell'app ("versione di … : messaggio").
- **Dal PC**: nel progetto dell'app `python tool/sync_data_repo.py`, poi qui
  `git add -A`, `git commit -m "…"`, `git push`.

L'app scarica solo i file cambiati e, prima di usarli, controlla che si leggano: se un JSON è rotto
o manca un'immagine, tiene i dati di prima e mostra l'errore.

⚠️ Il repo è **pubblico**: qui non vanno pesi, pesate o altri dati personali (quelli restano sul telefono).
