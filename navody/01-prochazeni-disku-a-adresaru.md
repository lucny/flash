# Návod pro práci s disky a složkami v příkazovém řádku Windows

Tento návod vám ukáže, jak pomocí příkazového řádku procházet diskové jednotky a složky, zjišťovat jejich obsah a strukturu.

---

### 1. Spuštění příkazového řádku

- Stiskněte **Windows + R**, napište `cmd` a stiskněte **Enter**.
- Nebo vyhledejte "Příkazový řádek" ve Start menu.

---

### 2. Změna aktuálního disku

Chcete-li přejít na jiný disk (například z `C:` na `D:`), napište do příkazového řádku písmeno disku, dvojtečku a stiskněte **Enter**:

```cmd
D:
```

---

### 3. Zobrazení obsahu složky

Pro zobrazení obsahu aktuální složky použijte příkaz:

```cmd
dir
```

Tento příkaz vypíše všechny soubory a složky v aktuální složce.

#### Užitečné přepínače příkazu `dir`:

- `/P` – Výpis po stránkách (užitečné, pokud je mnoho souborů).
- `/O:N` – Řazení podle názvu (abecedně).
- `/O:S` – Řazení podle velikosti souborů.
- `/S` – Zobrazení obsahu i v podsložkách.

Příklad:

```cmd
dir /P /O:N
```

---

### 4. Změna složky

Chcete-li přejít do jiné složky, použijte příkaz `cd` (change directory):

- **Přejít do podsložky**:

```cmd
cd nazev_slozky
```

Tím se přesunete do složky `nazev_slozky`, která je v aktuální složce.

- **Přejít o jednu úroveň výše** (do nadřazené složky):

```cmd
cd ..
```

Dvojité tečky `..` znamenají přechod do nadřazené složky.

- **Přejít na konkrétní cestu**:

Pokud chcete přejít do složky na konkrétním místě, můžete zadat celou cestu:

```cmd
cd C:\Users\Jmeno\Dokumenty
```

---

### 5. Návrat do kořenové složky disku

Chcete-li se vrátit do kořenové (hlavní) složky aktuálního disku, použijte příkaz:

```cmd
cd \
```

Tím se vrátíte do hlavní složky disku, například `C:\`.

---

### 6. Zobrazení struktury složek

Pro zobrazení stromové struktury složek použijte příkaz:

```cmd
tree
```

Tento příkaz zobrazí hierarchickou strukturu aktuální složky a jejích podsložek.

Pokud chcete zobrazit pouze strukturu složek bez souborů, použijte:

```cmd
tree /F
```

---

### 7. Zjištění aktuální cesty

Pokud chcete zjistit, v jaké složce se právě nacházíte, použijte příkaz:

```cmd
cd
```

Tento příkaz zobrazí aktuální cestu (adresář), ve které se nacházíte.

---

### 8. Vyčištění obrazovky

Pokud chcete vyčistit obrazovku příkazového řádku, použijte příkaz:

```cmd
cls
```

Tento příkaz smaže všechny předchozí výpisy a nastaví čistou obrazovku.

---

Nyní je návod zobrazen bez formátování Markdown a jednotně, jak jste si přál.