# clamp-gt-fly

Esperimento in silico: clamp in steady-state di glucosio (G) e trealosio (T) extracellulari su circuiti del connettoma di *Drosophila* (FlyWire FAFB + BANC).

Account GitHub: `scappellidoc-sudo`.

## Cosa c'e' ora

- `ids/fafb783_inventory_starter.csv` — inventario root ID FlyWire v783 (annotazioni pubbliche + lista GRN zucchero di Shiu).
- I metodi Word restano nel progetto Grok (`Metodi_clamp_glucosio_trealosio_connettoma.docx`, v0.2) finche' non li copiamo qui.

## Cosa non va nel git

Connettoma (parquet/feather Codex o GCS), mesh, output dei run LIF. Vanno in `data/` locale (vedi `.gitignore`).

## Prossimo passo

1. Confermare su Codex FAFB i tipi *high* (CB0701 = MN9, DNp01, DH44, IPC, ISN, BiT).
2. Controllo PER: repo Shiu (`philshiu/Drosophila_brain_model`) sulle GRN `GRN_sugar_Shiu_example` → readout CB0701.
3. Overlay Hill G/T solo sui sensori; scalare carburante off di default.

## Dataset

- Inventario attuale: FAFB / FlyWire **v783**.
- BANC v888: colonna `banc_root_id` ancora vuota. Non mescolare gli ID.
