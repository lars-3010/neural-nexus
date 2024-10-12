

- Algorithmen
    
    - lösen Probleme automatisiert
    - muss allgemein, ausführbar, eindeutig, endlich sein
    - Elementaranweisungen: Basisaktionen des Prozessors
    - Kontrollanweisungen: Aufgabe, die Ablauflogik festzulegen z.B.: Beschreibung von Wiederholungen, Fallunterscheidungen und zur Sequenzbildung
- Transportproblem
    
    - Roboter soll Stapel von Steinen wegtragen
    - gehe zu den Steinen, trage diese 2 Felder Richtung Süden, gehe zurück
        - zu ungenau
    - Kurzbefehle für drehen, gehen und tragen, sodass man ihm genau sagt, was er tun soll
    - geht zum Turm, holt einen Stein und wiederholt das solange, bis keine Steine mehr da sind, geht zurück
        - das ganze mit wenn, sonst
    - Roboter soll einzelne Steine stapeln
        - gehen, wenn Ziegel, einsammeln, zurückbringen, sonst weiter
- Datentypen
    
    - Integer: ganze Zahlen
    - String: Zeichenkette, wird durch umfassende Hochkommata gekennzeichnet
- Funktion
    
    Unterprogramme, die die Aufgaben haben öfter wiederholende Programme als Baustein zusammenzufassen → Baustein erhält einen eindeutigen Namen (kann aufgerufen und ausgeführt werden)
    
- Geldwechselproblem
    
    313*+6_8=87 513_+5*8=105
    
    Ganzzahldivision:
    
    267 DIV 5 = 53 90 DIV 11 = 8
    
    Restklassen:
    
    267 MOD 5 = 2 90 MOD 11 = 2 24 MOD 7 = 3
    
    solange Rest =/ 0 tue Zahl(87) DIV 13 = 6 Zahl(87) MOD 13 = 9 Rest(9) MOD 8 = 1
    
    ---
    
    wenn 1 = 0 dann ... sonst ... 6 - 1 = 5 *solange
    
    while-do -Schleife (mit Eintrittsbedingung)
    
    - Syntax
        
        while <Bedingung> do begin <Anweisungsblock> end;
        
    - mehrere Anweisungen im Anweisungsblock → umfasst mit “begin ; end”
        
    
    -Struktogramm: solange Bedingung erfüllt ist, führe aus: -Anweisungen
    
    - wird nicht unbedingt durchlaufen; Anzahl der Schleifendurchläufe hängt von der Eintrittsbedingung ab
- Beispiele
    
    procedure TForm1.eEingabeChange(Sender: TObject); var Zahl, Rest: Integer; begin end; procedure TForm1.Label1Click(Sender: TObject); begin end; procedure TForm1.PBerechnungClick(Sender: TObject); begin end;
    
    procedure TForm1.BStartClick(Sender: TObject); var iZahl, iRest, iFaktor, iRubel8, iRubel13: Integer; begin iZahl :=StrToInt (eEingabe.Text); iRest :=iZahl mod 13; iFaktor :=iZahl div 13; while iRest mod 8<>0 do begin iFaktor :=iFaktor-1; iRest :=iRest+13; end; iRubel13 :=iFaktor; iRubel8 :=iRest div 8; PBerechnung.Caption:=IntToStr(iZahl) +'=' +IntToStr(iFaktor) +'*13+' +IntToStr(iRubel8) +'*8'; end; end.
    
    Musterlösung:
    
    Nr.1: a) Ausführbarkeit - Allgemeinheit - Eindeutigkeit - Endlichkeit b) Elementaranweisungen - Kontrollanweisungen c) Flussdiagramm
    
    Nr.2: Integer; b:=5; String;
    
    Nr.3: a) Fehler: inkompatible Typen ( String - Integer) b) auf dem Panel 3+4 c) .Caption fehlt
    
    Nr.4: a) Label Bezeichner keine Umlaute b) eEdit1.SetFocus c) Bei ActivControl einstellen
    
    Nr.5: a) Ausgabe 18 b) Quersumme einer Zahl c)
    
    Nr.6: a) Schreibtischtest halt -> 18 b) Quersumme c) var n, s: integer; begin n:=StrToInt(EEingabe.Text); s:=0; while n<>0 do begin s:= s + n mod 10; n:= n div 10; end; PAusgabe.Caption:=IntToStr(s); end;
    
    ggT berechnen:
    
    1. T274= {1;2;274} T158= {1;2;158}
        
    2. 274=2_137 158=2_79 Primfaktorzerlegung
        
        gg (274;158)=2
        
    3. 274=*158+116 158=_116+42 116=42+32 42=_32+10 32=30_+2 10=5_2+0 ggT(274;158)=2