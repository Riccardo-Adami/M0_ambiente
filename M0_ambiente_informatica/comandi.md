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


# Esercizio 4 — Configurazione dell'identità in Git

## Comando usao
```cmd
git config --global user.name "Riccardo Adami"
@Riccardo-Adami ➜ /workspaces/M0_ambiente (main) $ git config --global user.email "riccardo.adami@marconirovereto.it"
@Riccardo-Adami ➜ /workspaces/M0_ambiente (main) $ git config --global init.defaultBranch main
git config --global core.editor "code --wait"
```

## Output del comando di verifica
```bash
@Riccardo-Adami ➜ /workspaces/M0_ambiente (main) $ git config --list --show-origin
file:/etc/gitconfig     user.name=Riccardo-Adami
file:/etc/gitconfig     user.email=158182544+Riccardo-Adami@users.noreply.github.com
file:/etc/gitconfig     gpg.program=/.codespaces/bin/gh-gpgsign
file:/etc/gitconfig     init.defaultbranch=main
file:/etc/gitconfig     credential.helper=/.codespaces/bin/gitcredential_github.sh
file:/home/codespace/.gitconfig filter.lfs.clean=git-lfs clean -- %f
file:/home/codespace/.gitconfig filter.lfs.smudge=git-lfs smudge -- %f
file:/home/codespace/.gitconfig filter.lfs.process=git-lfs filter-process
file:/home/codespace/.gitconfig filter.lfs.required=true
file:/home/codespace/.gitconfig user.name=Riccardo Adami
file:/home/codespace/.gitconfig user.email=riccardo.adami@marconirovereto.it
file:/home/codespace/.gitconfig init.defaultbranch=main
file:/home/codespace/.gitconfig core.editor=code --wait
```


# Esercizio 5 — Creazione del repository personale e primo commit

## Verifica dello stato del repository locale
```cmd
PS Z:\lab-info-4bi-adami> git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

