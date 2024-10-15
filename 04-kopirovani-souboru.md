# Návod na kopírování, přejmenování a mazání souborů v příkazovém řádku Windows

Tento návod vám ukáže, jak kopírovat soubory, včetně těch se shodnou částí názvu z různých podsložek, jak soubory přejmenovat a jak je případně smazat.

---

### 1. Kopírování souborů

Pro kopírování souborů se používá příkaz `copy` nebo `xcopy`, pokud chcete kopírovat soubory z různých složek a podsložek.

#### **Kopírování jednotlivého souboru**:

Chcete-li zkopírovat konkrétní soubor do jiné složky, použijte následující příkaz:

```cmd
copy C:\Cesta\k\souboru.txt D:\Cilova\slozka\
```

Tento příkaz zkopíruje soubor `soubor.txt` do složky `D:\Cilova\slozka\`.

#### **Kopírování více souborů**:

Pokud chcete kopírovat více souborů najednou, můžete využít zástupné znaky (wildcards). Například pro zkopírování všech souborů s příponou `.txt`:

```cmd
copy C:\Cesta\k\adresari\*.txt D:\Cilova\slozka\
```

Tento příkaz zkopíruje všechny `.txt` soubory ze složky `C:\Cesta\k\adresari` do složky `D:\Cilova\slozka`.

---

### 2. Kopírování souborů z různých podsložek

Pokud chcete kopírovat soubory z různých podsložek, použijte příkaz `xcopy` s přepínačem `/S`, který umožní kopírovat i soubory z podsložek.

#### **Kopírování souborů se stejnou částí názvu z podsložek**:

Například chcete zkopírovat všechny soubory s názvem `report.txt`, které se nacházejí v různých podsložkách:

```cmd
xcopy C:\HlavniSlozka\report.txt D:\CilovaSlozka\ /S
```

Tento příkaz zkopíruje všechny soubory s názvem `report.txt` ze složky `C:\HlavniSlozka` a všech jejích podsložek do složky `D:\CilovaSlozka`.

---

### 3. Kopírování celé složky a jejích souborů

Pro zkopírování celé složky i s jejími soubory a podsložkami použijte příkaz `xcopy` s přepínači `/E` a `/I`:

```cmd
xcopy C:\ZdrojovaSlozka D:\CilovaSlozka /E /I
```

- `/E` – Zkopíruje všechny podsložky, i prázdné.
- `/I` – Pokud cílová složka neexistuje, vytvoří ji.

Tento příkaz zkopíruje všechny soubory a složky ze složky `C:\ZdrojovaSlozka` do složky `D:\CilovaSlozka`.

---

### 4. Přejmenování souborů

Pro přejmenování souboru se používá příkaz `ren` (rename).

#### **Přejmenování jednoho souboru**:

```cmd
ren C:\Cesta\k\adresari\stary_nazev.txt novy_nazev.txt
```

Tento příkaz přejmenuje soubor `stary_nazev.txt` na `novy_nazev.txt` ve složce `C:\Cesta\k\adresari`.

#### **Přejmenování více souborů**:

Pomocí zástupných znaků můžete přejmenovat více souborů. Například přejmenujte všechny soubory `.txt` na `.bak`:

```cmd
ren *.txt *.bak
```

Tento příkaz přejmenuje všechny soubory s příponou `.txt` na soubory s příponou `.bak` v aktuální složce.

---

### 5. Mazání souborů

Pro smazání souborů se používá příkaz `del` (delete).

#### **Smazání jednoho souboru**:

```cmd
del C:\Cesta\k\adresari\soubor.txt
```

Tento příkaz smaže soubor `soubor.txt` ve složce `C:\Cesta\k\adresari`.

#### **Smazání více souborů najednou**:

Pokud chcete smazat více souborů najednou, můžete využít zástupné znaky. Například pro smazání všech `.txt` souborů:

```cmd
del *.txt
```

Tento příkaz smaže všechny `.txt` soubory v aktuální složce.

---

### 6. Smazání souborů z různých složek

Pokud chcete smazat všechny soubory s určitým názvem v různých složkách, použijte přepínač `/S` s příkazem `del`:

```cmd
del C:\Cesta\k\adresari\report.txt /S
```

Tento příkaz smaže všechny soubory s názvem `report.txt` ve složce `C:\Cesta\k\adresari` a všech jejích podsložkách.

---

### Příklady:

1. **Zkopírování všech souborů `.jpg` ze složky `Fotky` do složky `Archiv`**:

```cmd
copy C:\Fotky\*.jpg D:\Archiv\
```

2. **Přejmenování souboru `final.txt` na `zaloha.txt`**:

```cmd
ren C:\Dokumenty\final.txt zaloha.txt
```

3. **Smazání všech souborů `.log` ve složce a jejích podsložkách**:

```cmd
del C:\Soubory\*.log /S
```

---

### Důležité poznámky:
- **Příkaz `del`** je nevratný, takže buďte opatrní při mazání souborů, zejména pokud používáte zástupné znaky.
- **Příkaz `copy`** funguje pouze pro kopírování souborů, pokud potřebujete kopírovat i složky, použijte **`xcopy`**.

Tento návod vás naučil, jak efektivně kopírovat, přejmenovávat a mazat soubory v příkazovém řádku Windows.