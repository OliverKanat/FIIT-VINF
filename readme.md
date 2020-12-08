# Disambiguation pages - zoznam z SQL dump-u a potom tieto stránky vyparsovat title, anchor a popis (Python)

## Opis problemu
Z SQL dumpu je potrebne vyparsovat vsetky stranky, ktore patria medzi tzv. rozlisovacie stranky. Pre kazdu najdenu stranku z XML suboru vyparsujeme jej nadpis, link ukazujuci na danu stranku a popis stranky. Nasledne je potrebne indexovat export SQL dumpu. Motivaciou pre tuto ulohu je zistenie vsetkych slov a slovnych spojeni, ktore moze nadobudat viacero vyznamov v nasom jazyku.

Kedze data s ktorymi pracujeme su velkeho rozsahu, bude ich potrebne spracovat sekvencne a po castiach. Pre urychlenie parsovania je mozne pouzit paralelne spracovanie.

## Spustenie programu
Program je implementovany v jazyku Python. Na parsovanie SQL dumpu nie su potrebne ziadne dalsie kniznice. Pre nasledne indexovanie vyparsovaneho csv exportu je potrebna kniznica `whoosh`. Kod je potom mozne spustit v prostredi Jupyter Notebooku. 