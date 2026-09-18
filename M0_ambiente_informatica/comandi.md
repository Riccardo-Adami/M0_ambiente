# Esercizio 1 — Scheda delle versioni della postazione
**Postazione laboratorio:** 17

## Verifica Python
```cmd
z:\>py --version
Python 3.13.0
```

## Verifica Visual Studio Code
```cmd
z:\>code --version
1.111.0
ce099c1ed25d9eb3076c11e4a280f3eb52b4fbeb
x64
```

## Verifica Git
```cmd
z:\>git --version
git version 2.47.0.windows.1
```



# Esercizio 2 — Navigazione e percorsi nel terminale

## Sequenza dei comandi eseguiti
```cmd
z:\>cd M0_ambiente
z:\M0_ambiente>cd ../Documenti
z:\Documenti>mkdir esercizio-percorsi
z:\Documenti>cd esercizio-percorsi && mkdir dati && mkdir risultati && cd dati && cd ../risultati
```

## Output di Get-Location da PowerShell
```powershell
PS Z:\Documenti\esercizio-percorsi\risultati> Get-Location

Path
----
Z:\Documenti\esercizio-percorsi\risultati
```



# Esercizio 3 — Esecuzione di un programma dal terminale

## Comando usato
```cmd
py orario.py
```

## Output ottenuto
```cmd
Postazione 17 pronta per Riccardo Aami
```
