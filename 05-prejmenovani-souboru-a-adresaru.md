# Návod pro přejmenování souborů a složek v příkazovém řádku Windows

Příkazový řádek Windows poskytuje jednoduchý způsob, jak přejmenovat soubory a složky pomocí příkazu `ren` (rename). Tento návod vás provede postupem pro přejmenování jednotlivých souborů a složek, včetně hromadného přejmenování pomocí zástupných znaků.

---

### 1. Přejmenování jednotlivého souboru

Pro přejmenování jednoho konkrétního souboru použijte příkaz `ren`, který přijímá dva argumenty – starý název a nový název.

#### Příklad:

```cmd
ren C:\Cesta\k\souboru\stary_nazev.txt novy_nazev.txt
```

Tento příkaz přejmenuje soubor `stary_nazev.txt` na `novy_nazev.txt` ve složce `C:\Cesta\k\souboru`.

---

### 2. Přejmenování složky

Stejným způsobem lze přejmenovat i složku. Stačí zadat cestu ke složce a nový název.

#### Příklad:

```cmd
ren C:\Cesta\k\slozce\stara_slozka nova_slozka
```

Tento příkaz přejmenuje složku `stara_slozka` na `nova_slozka` v dané cestě.

---

### 3. Hromadné přejmenování souborů

Pokud potřebujete přejmenovat více souborů najednou, můžete využít zástupné znaky (wildcards) – hvězdičku `*` a otazník `?`.

#### Přejmenování všech souborů s určitou příponou:

Například chcete přejmenovat všechny `.txt` soubory na `.bak`:

```cmd
ren *.txt *.bak
```

Tento příkaz přejmenuje všechny soubory s příponou `.txt` v aktuální složce na příponu `.bak`.

#### Přejmenování souborů, které mají společnou část názvu:

Pokud máte soubory s názvy jako `report1.txt`, `report2.txt`, `report3.txt` a chcete je přejmenovat na `zprava1.txt`, `zprava2.txt`, `zprava3.txt`, použijte tento příkaz:

```cmd
ren report*.txt zprava*.txt
```

Tento příkaz přejmenuje všechny soubory, jejichž název začíná `report`, na soubory začínající `zprava`.

---

### 4. Hromadné přejmenování pomocí zástupného znaku `?`

Zástupný znak `?` nahrazuje přesně jeden znak. Můžete jej použít pro přejmenování souborů s fixní délkou názvu.

#### Příklad:

```cmd
ren file?.txt file?.bak
```

Tento příkaz přejmenuje soubory jako `file1.txt`, `file2.txt`, ale ne přejmenuje soubory jako `file10.txt`, protože `?` nahrazuje pouze jeden znak.

---

### 5. Přejmenování souborů ve specifické složce

Pokud chcete přejmenovat všechny soubory v konkrétní složce, můžete specifikovat celou cestu k těmto souborům:

```cmd
ren C:\Cesta\k\slozce\*.log *.txt
```

Tento příkaz přejmenuje všechny soubory s příponou `.log` na `.txt` ve složce `C:\Cesta\k\slozce`.

---

### 6. Přejmenování souborů s rozlišením na velká a malá písmena

V systému Windows není rozlišování mezi velkými a malými písmeny u názvů souborů a složek. Pokud však chcete přejmenovat soubor a změnit pouze velikost písmen, musíte použít přechodný název.

#### Příklad:

```cmd
ren soubor.txt docasny_nazev.txt
ren docasny_nazev.txt SOUBOR.txt
```

Tento postup použije přechodný název, aby systém Windows správně změnil velikost písmen.

---

### 7. Přejmenování složek ve specifické cestě

Pro přejmenování více složek v určité cestě použijte stejný přístup jako u souborů. Pokud chcete například přejmenovat všechny složky, které začínají písmenem "A", na "B", použijte následující příkaz:

```cmd
ren C:\Cesta\k\slozce\A* B*
```

Tento příkaz přejmenuje všechny složky začínající písmenem "A" na složky začínající písmenem "B" ve složce `C:\Cesta\k\slozce`.

---

### 8. Přejmenování souborů nebo složek se skrytými nebo systémovými atributy

Pokud chcete přejmenovat soubory nebo složky, které jsou skryté nebo označené jako systémové, musíte nejprve odstranit tyto atributy pomocí příkazu `attrib`.

#### Příklad:

1. **Odstranění atributu Skrytý**:

```cmd
attrib -H C:\Cesta\k\slozce\skryta_slozka
```

2. **Přejmenování složky**:

```cmd
ren C:\Cesta\k\slozce\skryta_slozka nova_slozka
```

---

### Příklady použití:

1. **Přejmenování souboru `document.txt` na `dokument.txt`**:

```cmd
ren document.txt dokument.txt
```

2. **Přejmenování všech souborů `.txt` na `.bak`**:

```cmd
ren *.txt *.bak
```

3. **Přejmenování složky `Data` na `Archiv`**:

```cmd
ren Data Archiv
```

4. **Přejmenování souboru s přechodným názvem pro změnu velikosti písmen**:

```cmd
ren report.txt temp.txt
ren temp.txt REPORT.txt
```

---

### Důležité poznámky:
- **Příkaz `ren` nelze použít k přejmenování souborů nebo složek, které jsou v daném okamžiku používány jinými procesy.** Před přejmenováním se ujistěte, že soubor nebo složka nejsou otevřeny.
- **Wildcards** (`*` a `?`) jsou užitečné pro hromadné přejmenování více souborů najednou.
- **Při přejmenování souborů nebo složek pomocí zástupných znaků** buďte opatrní, protože příkaz přejmenuje všechny odpovídající soubory.

Tento návod vás naučil, jak efektivně přejmenovat jednotlivé soubory i složky, a jak provádět hromadné přejmenování pomocí příkazového řádku Windows.