# Návod na práci s atributy souborů v příkazovém řádku Windows

V příkazovém řádku Windows můžete nastavit a zobrazit různé atributy souborů a složek pomocí příkazu `attrib`. Atributy souborů a složek určují jejich chování a ochranu v systému. Mezi nejčastější atributy patří **Read-Only** (jen pro čtení), **Hidden** (skrytý), **System** (systémový soubor), a **Archive** (archivní).

### 1. Zobrazení atributů souborů a složek

Pro zobrazení atributů souborů nebo složek použijte příkaz `attrib`:

```cmd
attrib C:\Cesta\k\souboru.txt
```

Tento příkaz zobrazí atributy pro soubor `soubor.txt`. Výstup může vypadat například takto:

```
 A  R    C:\Cesta\k\souboru.txt
```

- **R** znamená, že soubor je "jen pro čtení" (Read-Only).
- **A** označuje, že soubor má nastavený atribut "archivní" (Archive).

Pokud chcete zobrazit atributy všech souborů ve složce, použijte příkaz bez uvedení konkrétního souboru:

```cmd
attrib C:\Cesta\k\slozce\*
```

---

### 2. Nastavení atributů souborů

Pomocí příkazu `attrib` můžete také nastavit nebo odstranit atributy souborů a složek. Pro přidání atributu použijte symbol **+**, pro odstranění atributu použijte **-**.

#### Atributy, které můžete použít:

- **R** – Read-Only (soubor nelze upravovat).
- **H** – Hidden (skrytý soubor nebo složka).
- **A** – Archive (označuje, že soubor byl upraven a měl by být zálohován).
- **S** – System (označuje systémový soubor).

---

### 3. Přidání atributů souboru

Pokud chcete přidat atribut souboru, například nastavit soubor jako jen pro čtení, použijte následující příkaz:

```cmd
attrib +R C:\Cesta\k\souboru.txt
```

Tím nastavíte souboru `soubor.txt` atribut Read-Only.

Další příklady:
- **Skrytí souboru**:

```cmd
attrib +H C:\Cesta\k\souboru.txt
```

- **Nastavení souboru jako systémový soubor**:

```cmd
attrib +S C:\Cesta\k\souboru.txt
```

---

### 4. Odebrání atributů souboru

Pokud chcete odstranit určitý atribut, například atribut "jen pro čtení", použijte následující příkaz:

```cmd
attrib -R C:\Cesta\k\souboru.txt
```

Další příklady:
- **Odstranění atributu "Skrytý"**:

```cmd
attrib -H C:\Cesta\k\souboru.txt
```

- **Odstranění atributu "Systémový"**:

```cmd
attrib -S C:\Cesta\k\souboru.txt
```

---

### 5. Změna atributů složek

Atributy můžete nastavovat nejen na soubory, ale i na složky. Pokud chcete například označit složku jako skrytou, použijte následující příkaz:

```cmd
attrib +H C:\Cesta\k\slozce
```

---

### 6. Aplikace změn na všechny soubory ve složce

Pokud chcete aplikovat atributy na všechny soubory ve složce a podsložkách, použijte přepínač `/S` pro rekurzivní aplikaci atributů. Můžete přidat i přepínač `/D`, pokud chcete aplikovat atributy i na složky.

#### Příklad nastavení atributu "Skrytý" na všechny soubory ve složce a jejích podsložkách:

```cmd
attrib +H C:\Cesta\k\slozce\* /S
```

Tento příkaz nastaví atribut **Hidden** na všechny soubory v dané složce a jejích podsložkách.

---

### 7. Příklady práce s atributy:

1. **Zobrazení atributů všech souborů ve složce `Dokumenty`**:

```cmd
attrib C:\Users\Jmeno\Dokumenty\*
```

2. **Nastavení atributu "jen pro čtení" pro soubor `soubor.txt`**:

```cmd
attrib +R C:\Users\Jmeno\Dokumenty\soubor.txt
```

3. **Odstranění atributu "Skrytý" ze složky `Data`**:

```cmd
attrib -H C:\Data
```

4. **Skrytí všech souborů ve složce `Projekty` a jejích podsložkách**:

```cmd
attrib +H C:\Projekty\* /S
```

---

### Důležité poznámky:

- **Read-Only** (jen pro čtení) chrání soubor před úpravou, ale nebrání smazání.
- **Hidden** (skrytý) soubor se v Průzkumníku Windows nezobrazí, pokud není nastaveno zobrazení skrytých souborů.
- **System** (systémový soubor) soubor chrání, aby nebyl omylem smazán nebo upraven běžným uživatelem.
- **Archive** (archivní) označuje, že soubor byl upraven a měl by být zálohován.

Tento návod vás naučil, jak zobrazit, přidat nebo odstranit atributy souborů a složek v příkazovém řádku Windows.