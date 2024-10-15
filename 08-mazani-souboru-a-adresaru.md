# Návod pro mazání souborů a složek v příkazovém řádku Windows

Tento návod vás provede mazáním souborů a složek v příkazovém řádku Windows. Příkazový řádek poskytuje několik příkazů, které umožňují mazání jednotlivých souborů, složek, a také celé struktury složek a podsložek.

---

### 1. Mazání jednotlivého souboru

Pro smazání jednoho konkrétního souboru použijte příkaz `del` (delete).

#### Příklad:

```cmd
del C:\Cesta\k\souboru\soubor.txt
```

Tento příkaz smaže soubor `soubor.txt` ve složce `C:\Cesta\k\souboru`.

---

### 2. Mazání více souborů najednou

Pokud chcete smazat více souborů najednou, můžete použít zástupné znaky (wildcards).

#### Příklad: Mazání všech souborů s příponou `.txt` ve složce:

```cmd
del C:\Cesta\k\souboru\*.txt
```

Tento příkaz smaže všechny soubory s příponou `.txt` ve složce `C:\Cesta\k\souboru`.

---

### 3. Mazání souborů z různých složek

Pokud chcete mazat soubory včetně těch, které se nacházejí v podsložkách, použijte přepínač `/S`:

#### Příklad: Mazání všech souborů s příponou `.log` ve složce a všech jejích podsložkách:

```cmd
del C:\Cesta\k\slozce\*.log /S
```

Tento příkaz smaže všechny `.log` soubory ve složce `C:\Cesta\k\slozce` a všech jejích podsložkách.

---

### 4. Mazání složky

Pro smazání složky použijte příkaz `rmdir` (remove directory). Tento příkaz smaže pouze prázdnou složku. Pokud je ve složce obsah, musíte použít přepínač `/S` (viz další krok).

#### Příklad: Smazání prázdné složky:

```cmd
rmdir C:\Cesta\k\slozce\nazev_slozky
```

Tento příkaz smaže prázdnou složku `nazev_slozky`.

---

### 5. Mazání složky a jejího obsahu

Pokud chcete smazat složku včetně všech jejích souborů a podsložek, použijte přepínač `/S`. Přepínač `/S` zajistí, že se složka smaže včetně obsahu.

#### Příklad: Smazání složky a všech jejích podsložek a souborů:

```cmd
rmdir /S C:\Cesta\k\slozce\nazev_slozky
```

Tento příkaz smaže složku `nazev_slozky` včetně všech souborů a podsložek uvnitř.

---

### 6. Mazání složky bez potvrzení

Pokud nechcete být dotázáni na potvrzení před smazáním, přidejte přepínač `/Q` (quiet):

#### Příklad: Smazání složky a jejího obsahu bez potvrzení:

```cmd
rmdir /S /Q C:\Cesta\k\slozce\nazev_slozky
```

Tento příkaz smaže složku `nazev_slozky` a vše uvnitř bez zobrazení potvrzovacího dotazu.

---

### 7. Mazání skrytých nebo systémových souborů

Pokud chcete smazat soubory nebo složky, které jsou skryté nebo mají atribut systému, musíte nejprve odstranit tyto atributy pomocí příkazu `attrib`.

#### Příklad:

1. **Odstranění atributu Skrytý**:

```cmd
attrib -H C:\Cesta\k\souboru\skryty_soubor.txt
```

2. **Smazání skrytého souboru**:

```cmd
del C:\Cesta\k\souboru\skryty_soubor.txt
```

---

### 8. Příklady použití

1. **Smazání jednoho souboru `dokument.txt`**:

```cmd
del C:\Dokumenty\dokument.txt
```

2. **Smazání všech `.bak` souborů ve složce `Zalohy`**:

```cmd
del C:\Zalohy\*.bak
```

3. **Smazání celé složky `StaréProjekty` a všech jejích podsložek**:

```cmd
rmdir /S C:\Projekty\StareProjekty
```

4. **Smazání složky a obsahu bez potvrzení**:

```cmd
rmdir /S /Q C:\Projekty\DocasnaSlozka
```

---

### Důležité poznámky:

- **Příkaz `del`** maže soubory, nikoliv složky. Pokud chcete mazat složky, použijte **`rmdir`**.
- **Příkaz `rmdir`** smaže prázdnou složku, ale pokud má složka obsah, musíte použít přepínač `/S` pro mazání včetně souborů a podsložek.
- **Buďte opatrní při používání přepínače `/Q`**, protože smaže složky a jejich obsah bez potvrzení.

Tento návod vás naučil, jak efektivně mazat soubory a složky v příkazovém řádku Windows, včetně hromadného mazání, mazání složek a mazání skrytých souborů.