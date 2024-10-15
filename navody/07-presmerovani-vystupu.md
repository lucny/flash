# Návod na přesměrování výstupů do textového souboru v příkazovém řádku Windows

V příkazovém řádku Windows můžete snadno přesměrovat výstup jakéhokoli příkazu do textového souboru. To je užitečné například pro ukládání výpisů složek, výsledků příkazů nebo chybových hlášení do souboru pro další analýzu.

Existují dva základní operátory pro přesměrování výstupu:
- **`>`** – Přesměruje výstup do souboru. Pokud soubor již existuje, bude přepsán.
- **`>>`** – Přesměruje výstup do souboru, ale pokud soubor již existuje, výstup se k němu pouze připojí (nebude přepsán).

---

### 1. Přesměrování výstupu do nového souboru

Chcete-li výstup nějakého příkazu přesměrovat do nového textového souboru, použijte operátor **`>`**.

#### Příklad: Uložení výpisu obsahu složky do souboru

```cmd
dir C:\Cesta\k\slozce > C:\Cesta\k\souboru\vystup.txt
```

Tento příkaz uloží výpis obsahu složky `C:\Cesta\k\slozce` do souboru `vystup.txt`. Pokud soubor již existuje, bude přepsán.

---

### 2. Připojení výstupu k existujícímu souboru

Pokud chcete přidat výstup do již existujícího souboru (namísto jeho přepsání), použijte operátor **`>>`**.

#### Příklad: Přidání výpisu do existujícího souboru

```cmd
dir C:\Cesta\k\dalsi_slozce >> C:\Cesta\k\souboru\vystup.txt
```

Tento příkaz přidá výpis obsahu složky `C:\Cesta\k\dalsi_slozce` na konec souboru `vystup.txt`.

---

### 3. Přesměrování chybových hlášení do souboru

Pokud chcete přesměrovat pouze chybové hlášení (chybový výstup), použijte operátor **`2>`** pro přesměrování chybového výstupu.

#### Příklad: Přesměrování chyb do souboru

```cmd
dir C:\neexistujici_slozka 2> C:\Cesta\k\souboru\chyby.txt
```

Tento příkaz se pokusí vypsat obsah neexistující složky, což způsobí chybu. Chybové hlášení bude uloženo do souboru `chyby.txt`.

---

### 4. Přesměrování výstupu i chyb do jednoho souboru

Pokud chcete přesměrovat jak standardní výstup, tak chybové hlášení do jednoho souboru, použijte kombinaci **`>`** pro výstup a **`2>&1`** pro chyby.

#### Příklad: Uložení výstupu a chyb do jednoho souboru

```cmd
dir C:\Cesta\k\slozce > C:\Cesta\k\souboru\vystup_a_chyby.txt 2>&1
```

Tento příkaz uloží jak výpis obsahu složky, tak případné chybové hlášení do souboru `vystup_a_chyby.txt`.

---

### 5. Přesměrování pouze chyb

Pokud chcete uložit pouze chybové hlášení a ignorovat výstup, použijte následující příkaz:

```cmd
dir C:\neexistujici_slozka 2> C:\Cesta\k\souboru\chyby.txt
```

---

### 6. Příklady použití

1. **Uložení výpisu souborů s příponou `.txt` ve složce `Dokumenty` do souboru**:

```cmd
dir C:\Users\Jmeno\Dokumenty\*.txt > C:\Users\Jmeno\Dokumenty\seznam_txt_souboru.txt
```

2. **Přidání výpisu souborů do existujícího souboru bez přepsání**:

```cmd
dir C:\Users\Jmeno\Dokumenty >> C:\Users\Jmeno\Dokumenty\kompletni_vystup.txt
```

3. **Zachycení chybového hlášení při pokusu o přístup k neexistující složce**:

```cmd
dir C:\neexistujici_slozka 2> C:\Users\Jmeno\chyby.txt
```

4. **Uložení standardního výstupu i chybových hlášení do jednoho souboru**:

```cmd
dir C:\Users\Jmeno > C:\Users\Jmeno\zaznam.txt 2>&1
```

---

### Důležité poznámky:
- Přesměrování výstupu do souboru vám umožní uchovávat výsledky operací pro pozdější analýzu nebo archivaci.
- Pokud chcete přesměrovat chybové hlášení, použijte operátor `2>`.
- Pro kombinaci výstupu i chyb použijte `2>&1`.

Tento návod vám ukázal, jak efektivně přesměrovat výstupy z příkazového řádku Windows do textových souborů.