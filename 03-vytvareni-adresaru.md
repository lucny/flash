# Návod na vytvoření, přejmenování a smazání složek v příkazovém řádku Windows

Tento návod vás naučí, jak vytvořit vlastní strukturu adresářů a podsložek v příkazovém řádku, jak složky přejmenovat a jak je případně smazat.

---

### 1. Vytvoření nové složky

Pro vytvoření nové složky použijte příkaz `mkdir` (make directory). Můžete vytvořit jak jednu složku, tak i celou strukturu adresářů.

- **Vytvoření jedné složky**:

```cmd
mkdir nazev_slozky
```

Tento příkaz vytvoří složku s názvem `nazev_slozky` v aktuální složce.

- **Vytvoření složky v jiné cestě**:

Pokud chcete vytvořit složku v jiné než aktuální cestě, můžete zadat celou cestu:

```cmd
mkdir C:\Cesta\k\slozce\nova_slozka
```

- **Vytvoření celé struktury složek**:

Pokud chcete vytvořit několik složek najednou (např. složku a její podsložky), můžete to udělat v jednom příkazu:

```cmd
mkdir C:\Cesta\k\slozce\hlavni_slozka\podslozka1\podslozka2
```

Tento příkaz vytvoří strukturu `hlavni_slozka` -> `podslozka1` -> `podslozka2` najednou.

---

### 2. Přejmenování složky

Pro přejmenování složky použijte příkaz `ren` (rename):

- **Přejmenování složky v aktuální složce**:

```cmd
ren stara_slozka nova_slozka
```

Tento příkaz přejmenuje složku `stara_slozka` na `nova_slozka` v aktuální složce.

- **Přejmenování složky v jiné cestě**:

Pokud chcete přejmenovat složku na jiném místě než v aktuální složce, použijte celou cestu:

```cmd
ren C:\Cesta\k\slozce\stara_slozka nova_slozka
```

---

### 3. Smazání složky

Pro smazání složky můžete použít příkaz `rmdir` (remove directory). Tento příkaz odstraní složku, a pokud chcete odstranit i její obsah, musíte použít příslušné přepínače.

- **Smazání prázdné složky**:

```cmd
rmdir nazev_slozky
```

Tento příkaz smaže prázdnou složku `nazev_slozky` v aktuální složce.

- **Smazání složky v jiné cestě**:

Pokud se složka nachází v jiné než aktuální složce, použijte celou cestu:

```cmd
rmdir C:\Cesta\k\slozce\nazev_slozky
```

- **Smazání složky a jejího obsahu**:

Pokud chcete smazat složku i s jejím obsahem (včetně podsložek), použijte přepínač `/S`:

```cmd
rmdir /S nazev_slozky
```

Tento příkaz smaže složku `nazev_slozky` a všechny soubory a podsložky uvnitř ní. Budete požádáni o potvrzení.

- **Smazání složky a jejího obsahu bez potvrzení**:

Pokud nechcete být dotázáni na potvrzení, použijte přepínač `/Q` (quiet):

```cmd
rmdir /S /Q nazev_slozky
```

---

### Příklady

1. **Vytvoření složky `Projekt` a v ní dvou podsložek `Kód` a `Dokumentace`**:

```cmd
mkdir Projekt\Kód Projekt\Dokumentace
```

2. **Přejmenování složky `Dokumentace` na `Docs`**:

```cmd
ren Projekt\Dokumentace Docs
```

3. **Smazání celé složky `Projekt` a jejího obsahu**:

```cmd
rmdir /S Projekt
```

---

### Důležité poznámky:
- Pokud se pokusíte smazat složku, která obsahuje soubory, příkaz `rmdir` bez přepínače `/S` nebude fungovat. Pro smazání složek s obsahem vždy použijte přepínač `/S`.
- Buďte opatrní při použití přepínače `/Q`, protože odstraní složku bez potvrzení.

Tento návod vás naučil, jak efektivně vytvářet, přejmenovávat a mazat složky v příkazovém řádku Windows.