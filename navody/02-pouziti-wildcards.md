# Návod na používání "wildcards" v příkazovém řádku Windows

Wildcards (zástupné znaky) umožňují vyhledávat soubory nebo adresáře v příkazovém řádku podle určitých vzorců. Jsou velmi užitečné, když chcete filtrovat obsah složek a pracovat s více soubory najednou.

Existují dva základní zástupné znaky:
- **\*** (hvězdička) – Nahrazuje libovolný počet znaků.
- **?** (otazník) – Nahrazuje jeden libovolný znak.

---

### 1. Zobrazení všech souborů určitého typu

Chcete-li zobrazit všechny soubory určitého typu (např. všechny `.txt` soubory), použijte zástupný znak `*`:

```cmd
dir *.txt
```

Tento příkaz zobrazí všechny soubory s příponou `.txt` v aktuální složce.

---

### 2. Zobrazení souborů začínajících na určitou sadu znaků

Chcete-li zobrazit všechny soubory, jejichž názvy začínají na určitou sadu znaků, použijte následující zápis:

```cmd
dir test*.*
```

Tento příkaz zobrazí všechny soubory, které začínají na `test`, bez ohledu na příponu. Například soubory `test1.txt`, `test2.docx`, `testing.pdf`.

---

### 3. Filtrování souborů podle přípony

Pokud chcete zobrazit soubory s konkrétní příponou, můžete využít zástupné znaky pro část názvu:

```cmd
dir *.doc
```

Tento příkaz zobrazí všechny soubory s příponou `.doc`.

---

### 4. Použití zástupného znaku **?** pro jeden znak

Znak `?` nahrazuje přesně jeden znak. Můžete jej použít k vyhledávání souborů, kde neznáte konkrétní znaky v názvu.

Například:

```cmd
dir file?.txt
```

Tento příkaz zobrazí soubory s názvy jako `file1.txt`, `file2.txt`, ale nikoliv soubory s názvy jako `file12.txt` nebo `file123.txt` (protože `?` nahrazuje pouze jeden znak).

---

### 5. Vyhledávání podle části názvu i přípony

Pokud chcete vyhledávat soubory, kde neznáte přesný název ani příponu, můžete zkombinovat více zástupných znaků:

```cmd
dir *.???
```

Tento příkaz zobrazí všechny soubory, které mají přesně tři znaky v příponě, jako například `file.txt`, `doc.doc`, ale ne `data.csv`.

---

### 6. Filtrování složek a podsložek

Prohledávání složek i podsložek lze provést kombinací přepínače `/S` a zástupných znaků. Chcete-li například zobrazit všechny `.txt` soubory ve složce a jejích podsložkách, použijte:

```cmd
dir *.txt /S
```

---

### 7. Filtrování podle části názvu složky

Můžete také filtrovat složky pomocí wildcards. Pokud chcete například najít všechny složky, které začínají písmeny `doc`, použijte:

```cmd
dir doc* /AD
```

- `/AD` znamená, že chcete zobrazit pouze adresáře.

---

### Shrnutí

- **\*** – Nahrazuje libovolný počet znaků.
- **?** – Nahrazuje jeden znak.
- Používání zástupných znaků umožňuje efektivně filtrovat výpisy souborů a složek v příkazovém řádku.
- Zástupné znaky můžete použít společně s příkazem `dir` pro snadné procházení složek a filtraci souborů.

Díky těmto základním příkazům a wildcards můžete rychle najít požadované soubory nebo složky bez nutnosti procházet celý obsah ručně.