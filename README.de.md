# FreeCAD Makro: Schnittansichten (Cutviews) für Baugruppen und Teile

Dieses FreeCAD-Makro automatisiert das Erstellen, Verwalten und Löschen von Schnittansichten ("Cutviews") für Baugruppen und Einzelteile.  
Es richtet sich an fortgeschrittene Anwender und unterstützt sowohl Einzelteile als auch komplexe Baugruppen mit Links und verschachtelten Strukturen.  
**Kompatibel mit der Part- und PartDesign-Workbench.**

---

> 🇬🇧 [English description here (Englische Version)](README.md)

---

## Funktionen

- **Automatisches Erstellen von Schnittansichten** für einzelne Körper oder ganze Baugruppen
- **Qt-basierter Benutzerdialog** für einfache Bedienung (Schnitt-Buchstabe und Rechteckgröße wählbar)
- **Löschen bestehender Cutview-Gruppen** über einen eigenen Dialog
- Funktioniert sowohl mit einfachen Teilen als auch mit verschachtelten Assemblies (inkl. Links)
- Unterstützt **Part**- und **PartDesign**-Objekte

---

## Anwendung

### 1. Vorbereitung

- Öffne das gewünschte FreeCAD-Dokument.
- Wähle entweder:
  - einen Körper oder eine Baugruppe **und** eine Schnittebene, um eine neue Schnittansicht zu erstellen, oder
  - eine bestehende Cutview-Gruppe, um sie zu löschen.

> **MARKER_BILD1**  
> *(Hier Screenshot vom Auswahlzustand einfügen)*

---

### 2. Neue Schnittansicht erstellen

1. **Objekt und Ebene auswählen:**  
   Wähle im Baum einen Körper/Baugruppe und eine vorhandene Ebene (DatumPlane/Plane) aus.
2. **Makro ausführen:**  
   Ein Dialog erscheint. Wähle den Buchstaben für die Beschriftung und die Rechteckgröße (für den Schnittwürfel).
3. **Bestätigen:**  
   Das Makro erstellt automatisch Unter-Links und die zugehörigen Schnittwürfel und führt den Schnitt aus.

> **MARKER_BILD2**  
> *(Hier Screenshot des Dialogs einfügen)*

---

### 3. Bestehende Cutview löschen

- Wähle im Baum eine Gruppe aus, deren Name mit `Cut_` beginnt (z.B. `Cut_A`).
- Führe das Makro erneut aus.  
  Ein Dialog öffnet sich, in dem das Löschen der gesamten Gruppe möglich ist.

> **MARKER_BILD3**  
> *(Hier Screenshot des Lösch-Dialogs einfügen)*

---

## Hinweise & Tipps

- Koplanare Flächen an der Schnittstelle werden **dunkelrot hervorgehoben** für bessere Sichtbarkeit.
- Die Gruppierung der Objekte erfolgt automatisch in Haupt- und Untergruppen.
- Funktioniert mit Einzelteilen und komplexen Baugruppen mit verschachtelten Strukturen und Links.

> **MARKER_BILD4**  
> *(Hier Screenshot einer fertig erzeugten Schnittansicht einfügen)*

---

## Installation

1. Die Datei `ZZZZ_Create_Cutviews_ASM.FCMacro` in den Makro-Ordner von FreeCAD kopieren.
2. FreeCAD starten und das Makro über die Makro-Verwaltung ausführen.

---

## Voraussetzungen

- FreeCAD (aktuelle Version empfohlen)
- Part- und/oder PartDesign-Workbench aktiviert
- Für Baugruppen ggf. eine Assembly-Workbench (A2plus, Assembly3, etc.)

---

## Lizenz

Dieses Makro steht unter der MIT-Lizenz.

---

## Support / Fragen

Bei Problemen oder Verbesserungsvorschlägen bitte ein Issue im [GitHub-Repository](https://github.com/PuLs4r1203/FreeCAD_Cut_view) eröffnen.
