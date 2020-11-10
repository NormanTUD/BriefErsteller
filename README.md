### BriefErsteller

BriefErsteller hilft dabei, LaTeX-Briefe zu erzeugen und speichert einmal eingegebene Kontaktdaten 
in ~/briefkoepfe.pl, damit man später auf sie zugreifen kann. D.h. man muss nur ein einziges Mal einen
Namen, eine Adresse, eine Anrede usw. eingeben, dann nie wieder.

Ich würde empfehlen, das Programm nach

/bin/brief

zu packen, um es überall aufrufen zu können. Weil es sich um ein Perlskript handelt, erfolgt der Aufruf mit:
```console
me@mymachine:~$ perl brief
```
Die .tex-Datei wird immer im aktuellen PWD geschrieben.


# Abhängigkeiten

```console
sudo apt-get install whiptail latexmk xdg-utils
sudo cpan -i Term::ANSIColor
sudo cpan -i UI::Dialog
```

Für LaTeX wird das Paket g-brief benötigt (https://ctan.org/pkg/g-brief?lang=de).

# Skript überall lauffähig machen

```console
sudo cp brief /usr/local/bin
brief
```

Um das Skript über die GUI aufzurufen, kann man die `BriefErsteller.desktop` nehmen und sie z.\,B. ins KDE-Menü einfügen.
Dazu reicht es,

```console
sudo cp BriefErsteller.desktop /usr/share/applications
```

zu kopieren.

# Video

https://www.youtube.com/watch?v=kP5sorq1hFU&feature=youtu.be
