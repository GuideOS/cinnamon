Du möchtest den Quellcode von **Cinnamon 5.6.8** bearbeiten. Hier sind die Schritte:

### 1. **Abhängigkeiten installieren**
Bevor du loslegst, installiere die notwendigen Werkzeuge:

```bash
sudo apt update
sudo apt install devscripts build-essential
```

Falls du die Abhängigkeiten für Cinnamon selbst benötigst:

```bash
sudo apt build-dep cinnamon
```

### 2. **Paket entpacken**
Entpacke das Debian-Quellpaket mit:

```bash
dpkg-source -x cinnamon_5.6.8-1.dsc
```

Dadurch wird ein Ordner **cinnamon-5.6.8** erstellt, in dem sich der Quellcode befindet.

### 3. **Code bearbeiten**
Navigiere in das Verzeichnis:

```bash
cd cinnamon-5.6.8
```

Bearbeite den Code nach deinen Wünschen.

### 4. **Paket neu bauen**
Nach deinen Änderungen kannst du das Paket neu erstellen:

```bash
debuild -us -uc
```

Falls du zusätzliche Abhängigkeiten benötigst, überprüfe sie mit:

```bash
mk-build-deps -i
```

### 5. **Neues Paket installieren**
Nach erfolgreichem Build findest du das neue `.deb`-Paket eine Ebene höher:

```bash
cd ..
sudo dpkg -i cinnamon_5.6.8-1_amd64.deb
```

Falls Abhängigkeiten fehlen:

```bash
sudo apt -f install
```

Falls du spezifische Änderungen hast, die du besprechen möchtest, lass es mich wissen! 😊
