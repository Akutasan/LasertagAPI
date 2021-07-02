# LasertagAPI

## Beispiel:

### Lesen:

Zum Bekommen eines Namens nach der Weapon-ID:
```python
from sql import rmy # Importiert die Klasse

SQL = rmy("miro", "") # Verbindet sich mit der Datenbank

printing = SQL.get("name", "wid", 1) # Erstellt Variable 'printing' mit Auswahl von Name wo die Weapon-ID 1 ist
print(printing)  # Druckt printing

rmy.close(SQL) # Schließt die Datenbank 
```

Zum Bekommen eines Kill-Counters nach dem Barcode:
```python
from sql import rmy # Importiert die Klasse

SQL = rmy("miro", "") # Verbindet sich mit der Datenbank

printing = SQL.get("kills", "barcode", 3000000035856) # Erstellt Variable 'printing' mit Auswahl von kills wo Barcode 300...56 ist
print(printing) # Druckt printing

rmy.close(SQL) # Schließt die Datenbank 
```

### Schreiben:

Zum Schreiben eines Kill-Counters nach der Vest-Id:
```python
from sql import rmy # Importiert die Klasse

SQL = rmy("schreibuser", "safespasswort") # Verbindet sich mit der Datenbank

printing = SQL.set(""kills", 6, "vid", 2) # Erstellt Variable 'printing' mit Bearbeitung von Kills zu 6 wo Vest-ID 2 ist
print(printing)  # Druckt printing

rmy.close(SQL) # Schließt die Datenbank 
```

### **WICHITIG**: 
```python 
from sql import rmy
SQL = rmy("miro", "") 
rmy.close(SQL)
```
sind **IMMER** Pflicht!

## User-Daten:
Falls Ihr Schreib-Rechte benötigt, sagt mir im Vorraus Bescheid.
