# Configurazione Postazione Windows

1. **Verifica Git**
   ```powershell
   git --version
   ```

2. **Identità Globale**
   ```powershell
   git config --global user.name "Riccardo Adami"
   git config --global user.email "la-tua-email@esempio.com"
   git config --global --list
   ```

3. **Terminatori di linea**
   ```powershell
   git config --global core.autocrlf true
   git config core.autocrlf
   ```


4. **Inizializzazione Repository**
   ```powershell
   cd $HOME
   mkdir -p workspace/M0_ambiente_informatica
   cd workspace/M0_ambiente_informatica
   git init
   Test-Path .git
   ```


5. **Collegamento Remoto**
   ```powershell
   git remote add origin https://github.com
   git remote -v
   ```