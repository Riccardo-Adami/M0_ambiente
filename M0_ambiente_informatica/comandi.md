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


# Esercizio 7 — File .gitignore e verifica delle regole

## Output dei comandi (`git status` e `git check-ignore`)
```bash
@Riccardo-Adami ➜ /workspaces/M0_ambiente (main) $ git status
git check-ignore -v M0_ambiente/.venv/pyvenv.cfg
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
.gitignore:7:.venv/     M0_ambiente/.venv/pyvenv.cfg
```

# Es 8
non abbiamo applicazione ssh installata


# Esercizio 9 — Lettura e interpretazione della cronologia

## Output del comando `git log --oneline --graph --decorate`
```text
* 4835624 (HEAD -> main, origin/main, origin/HEAD) feat aggiunta gitignore
* cbcded4 feat esercizio 5, inizializzazione repo privata in locale
* 3f4bac9 feat, esercizio 4 con configurazione profilo git
* 00a239a Aggiungi file comandi.md con dettagli sulle versioni della postazione e istruzioni
*   40ce59a Merge branch 'main' of https://github.com/Riccardo-Adami/M0_ambiente
|\  
| * 142aa83 Create t
* | d10ee12 Aggiorna comandi.md con dettagli sulle verifiche e rimuove output non necessari
|/  
* b6d2ece Aggiungi file comandi.md con istruzioni e versioni degli strumenti
* 5dc2008 Add initial README with project title
```

## Output del comando `git log -5 --pretty=format:"%h %ad %an %s" --date=short`
```text
4835624 2026-09-18 Riccardo Adami feat aggiunta gitignore
cbcded4 2026-09-18 Riccardo Adami feat esercizio 5, inizializzazione repo privata in locale
3f4bac9 2026-09-18 Riccardo Adami feat, esercizio 4 con configurazione profilo git
00a239a 2026-09-18 Riccardo-Adami Aggiungi file comandi.md con dettagli sulle versioni della postazione e istruzioni
40ce59a 2026-09-18 Riccardo-Adami Merge branch 'main' of https://github.com/Riccardo-Adami/M0_ambiente
```


# Esercizio 10

Guardare README.md


# Esercizio 11

## Sequenza dei comandi

```bash

mkdir temporanei
touch temporanei/nota.txt temporanei/dati.tmp

git add temporanei
git commit -m "feat: aggiunge cartella temporanei per errore"

echo "temporanei/" >> .gitignore

git rm -r --cached temporanei

git add .gitignore
git commit -m "fix: rimuove temporanei dal tracciamento Git"

git ls-files temporanei
git check-ignore -v temporanei/nota.txt


# Esercizio 12
Comandi
```bash
git add versioni.md
git commit -m "Aggiorna la scheda delle versioni della postazione"
git push```

Errore (output) esercizio 12:
```bash
[main 7a60b3e] Aggiorna la scheda delle versioni della postazione
 1 file changed, 1 insertion(+)
 create mode 100644 M0_ambiente_informatica/versioni.md
To https://github.com/Riccardo-Adami/M0_ambiente
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/Riccardo-Adami/M0_ambiente'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
@Riccardo-Adami ➜ /workspaces/M0_ambiente/M0_ambiente_informatica (main) $ 
```

Per risolvere il blocco ho pulito l'area di lavoro efatto il rebase:
```bash
git stash
git rebase origin/main
git push origin main

# Ripristina i file messi temporaneamente da parte
git stash pop
git log --oneline --graph --decorate
```