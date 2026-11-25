Was möchte ich herausfinden?

Welche Attribute korrellieren besonders stark mit der Menge an Unfällen:
     - Hinweis in df.describe(include = ""all) -> Wenn Menge der häufigsten Ausprägung deutlich höher als Menge der Unfälle/Menge der eindeutigen Ausprägungen
     - Bestätigen über Gruppierung nach dem Attribut -> gucken, welche Ausprägungen häufig vorkommen und welche nicht
     - Gibt es eine Möglichkeit, herauszufinden, ob bestimmte Kombinationen aus Faktoren ausschlaggebend sind
     - Gibt es einen Koeffizienten/eine Kennzahl, mit der das Ganze gezeigt werden kann? 

Wie stark korellieren die einzelnen Faktoren mit der Schwere des Unfalls?
    - Korellationskoeffizienten zwischen Faktoren und der Schwere des Unfalls berechnen
    - Gibt es eine Möglichkeit, die Korellation zwischen einer Kombination aus Faktoren und der Schwere des Unfalls zu erkennen/untersuchen?


Hypothesen(Aufgabe 3.2):

- Die Spalten "Accident_Date", "Month", "Day_of_Week", und "Year" sollten in ihren Ausprägungen übereinstimmen (z.B. "Month" ist der tatsächliche Monat aus "Accident_Date", "Day_of_Week" ist der passende Wochentag etc.)
    - Direkt überprüfen (Schon im Code)

- Wetterbedingungen und Zustand der Straßenoberfläche hängen zusammen (z.B. nasse Straße bei Regen)
    - Cramers-V: 0.49, starker Zusammenhang, Kontingenztabelle ✅

- Straßentyp und Speed-Limit hängen zusammen
    - Eta-Quadrat 0.16/ 16% Auswertung nach Cohen(1988), Kontingenztabelle ✅

- Zeit, Monat und Lichtbedingungen hängen zusammen
    - (Verschiedene Methoden im Code probiert)

- "Junction_Control" und "Junction_Type" korelliere
    - Cramers-V: 0.49, Kontingenztabelle ✅

- Spalten und Ausprägungen, die sich auf die Häufigkeit der Unfälle auswirken:
    - Wetter-, Straßen- und Lichtbedingungen:
        - Mehr Unfälle bei schlechten Lichtbedingungen, Regen/Nebel, nassen/gefrorenen Straßen

    - Road_Type:
        - Mehr Unfälle auf Straßen mit gegenfahrbahn und Kreiseln als auf anderen (evtl. nur auf offener Straße und nicht an Kreuzungen)

    - Urban/Rural:
        - Mehr in urban

    - Junction-Control: 
        - Mehr Unfälle an Kreuzungen die nicht oder nur durch ein Schild geregelt werden, im Vergleich zu Ampeln, Autorisierten Personen und offener 

    - Wochentag:
        - Mehr Unfälle an Wochentagen, da mehr Stress
        - Evtl im Zusammenhang damit, ob städtisch oder nicht

    - Tageszeit:
        - Mehr Unfälle zu Rush-Hours (z.B. 7-9 Uhr, 16-18 Uhr)

    - Unfälle treten häufiger auf, wenn Hindernis im Weg   
        - nicht richtig überprüfbar


- Spalten und Ausprägungen, die sich auf die Schwere des Unfalls auswieken:
    - Number of Vehicles:
        - Unfälle, in denen nur ein Fahrzeug verwickelt ist sind häufiger schwer oder tödlich

    - Vehicle Type:
        - Unfälle, in die offene Fahrzeuge (z.B. Pferd/Motorrad) verwickelt sind, fallen schwerer aus als Unfälle mit geschlossenen Fahrzeugen (Auto/LKW)

    - Straßenoberfläche, Wetter und Licht:
        - Faktoren, die rechtzeitiges/effektives Bremsen erschweren erhöhen die Unfallschwere