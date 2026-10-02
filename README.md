# clamp-gt-fly

Clamp in steady-state dello stato metabolico su archi del connettoma di *Drosophila* (FlyWire). Il precedente è Shiu et al. 2024: un LIF sul grafo FAFB predice un riflesso. Qui lo stimolo resta quello, e si aggiunge lo stato che a loro manca.

Account: `scappellidoc-sudo`. Metodi: bozza v0.3 (2 ottobre 2026).

## Disegno, non ancora eseguito per intero

- Trial di 1 s. Da 0 a 200 ms solo la condizione metabolica. A 200 ms lo stimolo dell'arco. La latenza si misura dall'onset dello stimolo.
- Clamp: un metabolita alla volta, gli altri fermi. G fino a 40 mM, T fino a 80 mM, F fino a 20 mM (punti alti = sovrafisiologico, diabete in silico). DILP non è un mM: proxy = ipotesi IPC solo-rete contro IPC che sentono G.
- Ingresso sweepato a 0, 10, 25, 50, 100, 200 Hz, per vedere se l'effetto dello stato regge anche a stimolo forte.
- Strati accesi in ordine: A grafo LIF; B sensori; C IPC A oppure B, mai la media; D trealosio-glia spento di default.
- n >= 10 semi per condizione. Uno spike di effettore non è un comportamento.

## Cosa c'è nel repo

- `ids/fafb783_core_high.csv` — root ID FAFB v783. CB0701 = MN9; DNp01 = Giant Fiber.
- `notebooks/01_per_control_v783.ipynb` — PER senza overlay, 3 trial, GRN zucchero 100 Hz. Controllo di cablaggio.
- `notebooks/02_per_overlay_sensori_v783.ipynb` — overlay sensori, n = 1, T = 30 mM, scalare off. Non è la curva.
- `notebooks/GFS.ipynb` — 200 ms di solo overlay, poi looming. È l'unico notebook già in fase col pre-stimolo. n = 1, GF saturo a 100 Hz.

`example.ipynb` (Colab dell'esempio Shiu, stimolo da t = 0, niente clamp) è stato rimosso: non è questo disegno.

## Cosa non va nel git

Connettoma, mesh, output LIF. Stanno in `data/` locale (`.gitignore`).

## Dataset

- Run fatti: FAFB / FlyWire v783.
- BANC v888 quando l'uscita è un motoneurone della corda. ID non mescolati.
