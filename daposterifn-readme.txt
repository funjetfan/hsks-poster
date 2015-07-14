---------
Hinweise:
---------

- Das Erscheinungsbild des Posters kann mit den Optionen 
   - tnt, hf, tk, mns (f�r die einzelnen Lehrst�hle des Instituts),
   - diplom, master   (f�r Diplom- oder Masterarbeit),
   - extern           (im Falle einer extern angefertigten Arbeit - erlaubt zus�tzlichen externen Betreuer + Firma)
  angepasst werden.

- Die Parameter f�r den Posterkopf werden mit den Befehlen
   - \setDAParameter
   - \setStudentPassbild
   - \setStudentWerdegang
  �bergeben.

  Zur Benutzung der Befehle (Beispiele siehe beiliegende LaTeX-Datei):

  - \setDAParameter[Param1]{Param2}{Param3}
    -> Param2 ist eines der Schl�sselw�rter
        'Thema',
        'Student',
        'BetreuerTUD',
        'BetreuerExternName',  (nur mit Option 'extern')
        'BetreuerExternFirma', (nur mit Option 'extern')
        'Hochschullehrer',
        'VerteidigungDatum'. 
    -> Param3 ist der jeweils an den Posterkopf zu �bergebende Inhalt.
    -> Param1 ist optional und erlaubt die �nderung der Gr��e des Postertitels (nur mit Param2 = 'Thema') durch
        '\LARGE',
        '\Large',
        '\large'.

  - \setStudentPassbild[Param1]{Param2}
    -> Param2 ist der Pfad des Passbildes.
    -> Param1 ist optional und erlaubt die �nderung der Breite des Passbildes.

  - \setStudentWerdegang[Param1][Param2]{Param3}
    -> Param3 ist der an den Posterkopf zu �bergebende Inhalt, d.h. der Werdegang des Autors - in getrennten Abs�tzen und mit Zeilenumbruch nach dem Datum.
    -> Param1 ist optional und erlaubt die �nderung der Schriftgr��e f�r diesen Bereich durch
        '\normalsize',
        '\small',
        '\footnotesize',
        '\scriptsize'.
    -> Param2 ist optional und erlaubt die �nderung des Abstandes der Abs�tze f�r diesen Bereich.

- �berschriften bitte nicht nummerieren (\section* statt \section) und m�glichst nur zwei Ebenen (\section* und \subsection*) verwenden.

- Das fertige Poster (vorm Druck) bitte als PDF an den Betreuer senden, damit der noch einen pr�fenden Blick drauf werfen kann.


---------------------------------------------
Nutzungshinweise f�r die vorliegende Version:
---------------------------------------------

- Die derzeitige Version der Vorlage verwendet die Schriftart Computer Modern Sans Serif.
  Die TU-Schriftart wird noch nicht unterst�tzt.

- Bitte �berpr�fen, ob alle Textelemente korrekt in serifenloser Schrift auftauchen.
  Da kann es bei "exotischeren" Umgebungen und Paketen noch Probleme geben.

- Probleme mit der Vorlage - am besten mit L�sung! ;-) - an: Anne Wolf <anne.wolf@tu-dresden.de>


---------------------------------------------
bekannte (noch ungel�ste) Probleme:
---------------------------------------------

- Bei Verwendung des Mathe-Fonts von Computer Modern werden eigentlich skalierbare Mathesymbole (Summenzeichen u.�.) in Relation zum Rest der Gleichung zu klein dargestellt.
-> Werden Schriften mit einem anderen Mathe-Font verwendet, scheint das Problem nicht aufzutreten:
   z.B. Libertine: \usepackage{libertine} oder   
        txfonts:   \usepackage{txfonts}