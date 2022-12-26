---
title: Francouzský Intrastat
description: Tento článek obsahuje informace o deklaraci Intrastat ve Francii.
author: anasyash
ms.date: 11/30/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 2076649c7fff9f47b9c1fda62a103168b19bb973
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831798"
---
# <a name="french-intrastat"></a>Francouzský Intrastat

[!include[banner](../includes/banner.md)]

Společnosti ve Francii, které jsou registrované pro daň z přidané hodnoty (DPH) a které obchodují s ostatními zeměmi Evropské unie (EU), musí deklarovat směnu zboží a služeb do a z Francie. Deklarace d'exchanges de biens (Deklarace obchodu se zbožím nebo DEB) je kombinací seznamu prodejů EU a sestavy Intrastat. Tuto zprávu musíte odeslat měsíčně u veškerého prodeje zboží v rámci Společenství.

Sestavu DEB můžete generovat v jednom ze dvou formátů elektronických textových souborů: SAISUNIC 330 nebo INTRACOM.

V následující tabulce jsou uvedena pole, která jsou obsažena ve francouzské deklaraci Intrastat ve formátu SAISUNIC 330. Tabulka také uvádí úroveň sestavy každého pole. Pole může mít následující úrovně sestavy:

- **4** – Daňové přiznání.
- **1** – Statistická odpověď.
- **5** – Statistická odpověď na dodávku, daňové přiznání a společné vyplnění.

| Pole                       | Úrovně sestavy |
|-----------------------------|---------------|
| Referenční období         | 4, 1, 5       |
| Číslo prohlášení       | 4, 1, 5       |
| Číslo řádku                 | 4, 1, 5       |
| Kód ISO země (FR)       | 4, 1, 5       |
| Doplňkový kód          | 4, 1, 5       |
| Číslo Siren                | 4, 1, 5       |
| Kód DPH odběratele        | 4, 1, 5       |
| Kód směru              | 4, 1, 5       |
| Typ transakce            | 4, 1, 5       |
| Úroveň povinnosti            | 4, 1, 5       |
| Kód zboží              | 1, 5          |
| Národní NGP                | 1, 5          |
| Okres (oddělení)         | 1, 5          |
| Povaha transakce       | 1, 5          |
| Země původu      | 1, 5          |
| Země původu - Import | 1, 5          |
| Konečný cíl - Export | 1, 5          |
| Hodnota faktury               | 4, 1, 5       |
| Statistická hodnota           | 1, 5          |
| Čistá hmotnost                  | 1, 5          |
| Dodatečné jednotky            | 1, 5          |
| Kód přenosu              | 1, 5          |

V následující tabulce jsou uvedena pole, která jsou obsažena ve francouzské deklaraci Intrastat ve formátu INTRACOM. Tabulka také uvádí úroveň sestavy každého pole. Pole může mít následující úrovně sestavy:

- **4** – Daňové přiznání.
- **1** – Statistická odpověď.
- **5** – Statistická odpověď na dodávku, daňové přiznání a společné vyplnění.

| Pole                       | Úrovně sestavy |
|-----------------------------|---------------|
| Kód směru              | 4, 1, 5       |
| Číslo prohlášení       | 4, 1, 5       |
| Číslo řádku              | 4, 1, 5       |
| Siren                       | 4, 1, 5       |
| Okres (oddělení)         | 1, 5          |
| Kód přenosu              | 1, 5          |
| Země původu           | 1, 5          |
| Povaha transakce       | 1, 5          |
| Hodnota faktury               | 4, 1, 5       |
| Způsoby dodání           | 1, 5          |
| Typ transakce            | 4, 1, 5       |
| Úroveň povinnosti            | 4, 1, 5       |
| Kód zboží              | 1, 5          |
| Národní NGP                | 1, 5          |
| Čistá hmotnost                  | 1, 5          |
| Statistická hodnota           | 1, 5          |
| Dodatečné jednotky            | 1, 5          |
| Země původu - Import | 1, 5          |
| Konečný cíl - Export | 1, 5          |
| Kód DPH odběratele        | 4, 1, 5       |
| Doplňkový kód          | 4, 1, 5       |
| Referenční období         | 4, 1, 5       |

## <a name="set-up-intrastat"></a>Vytvořit Intrastat

- V [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/Logon/Index) v knihovně sdíleného majetku si stáhněte nejnovější verze následujících konfigurací elektronického výkaznictví (ER) pro přiznání Intrasat:

    - Modul Intrastat
    - Sestava Intrastat
    - Intrastat INTRACOM (FR)
    - Intrastat SAISUNIC (FR)

    Další informace viz [Stažení konfigurace elektronického vykazování ze služby Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

### <a name="set-up-vat-ids"></a>Nastavení DIČ

#### <a name="set-up-vat-codes-for-your-company"></a>Nastavení DPH pro vaši společnost

1. Přejděte na **Daň** \> **Nastavení** \> **Prodejní daň** \> **Čísla DIČ**.
2. V podokně akcí zvolte **Nový**.
3. V poli **Země/region** vyberte **FRA**.
4. V poli **DIČ** zadejte DIČ vaší společnosti.
5. Přejděte na **Správa organizace** \> **Organizace** \> **Právnické osoby** a vyberte svou společnost.
6. Na pevné záložce **Zahraniční obchod a logistika** v sekci **Intrastat** nastavte pole **Export čísla osvobozeného od DPH** a **Import čísla osvobozeného od DPH** na kód vytvořený v kroku 4.
7. Na pevné záložce **Daňová registrace** v poli **Daňové registrační číslo** zadejte daňové identifikační číslo (DIČ) vaší společnosti.

#### <a name="set-up-the-vat-ids-for-trading-partners"></a>Nastavení čísel DIČ pro obchodní partnery

##### <a name="create-a-registration-type-for-the-company-code"></a>Vytvoření typu registrace pro kód společnosti

Pro všechny země nebo oblasti, se kterými vaše společnost obchoduje, musíte vytvořit typy registrací DIČ.

1. Přejděte na položky **Správa organizace** \> **Globální adresář** \> **Typy registrace** \> **Typy registrace**.
2. V podokně Akce vyberte možnost **Nová**, vytvoří se typ registrace pro DIČ.
3. V dialogovém okně **Vložit podrobnosti typu registrace** zadejte v poli **Název** název typu registrace. Například zadejte **DIČ**.
4. V poli **Země/oblast** vyberte zemi nebo oblast obchodního partnera.
5. Vyberte **Vytvořit**.

##### <a name="match-the-registration-type-with-a-registration-category"></a>Spárování typu registrace s kategorií registrace

1. Přejděte na položky **Správa organizace** \> **Globální adresář** \> **Typy registrace** \> **Kategorie registrace**.
2. V podokně akcí vyberte **Nový** pro vytvoření propojení mezi typem registrace a kategorií registrace.
3. Pro typ registrace pro DIČ vyberte **DIČ** kategorie registrace.
4. Opakujte kroky 2 a 3 pro další typy registrace, které jste vytvořili pro země nebo oblasti, se kterými vaše společnost obchoduje.

##### <a name="set-up-the-vat-number-of-a-trading-partner"></a>Nastavení DIČ obchodního partnera

1. Přejděte na **Pohledávky** \> **Odběratelé** \> **Všichni odběratelé**.
2. V mřížce vyberte zákazníka.
3. V podokně Akce na kartě **Zákazník** ve skupině **Registrace** zvolte **ID registrace**.
4. Na pevné záložce **ID registrace** vyberte **Přidat** pro vytvoření ID registrace.
5. V poli **Typ registrace** vyberte typ registrace, který jste vytvořili pro kód společnosti.
6. Do pole **Registrační číslo** zadejte DPH společnosti.
7. V podokně akcí zvolte **Uložit** a poté zavřete stránku.

Další informace naleznete v tématu [ID registrace](emea-registration-ids.md).

### <a name="set-up-foreign-trade-parameters"></a>Nastavit parametry zahraničního obchodu

1. Přejděte na **Daň** \> **Nastavení** \> **Zahraniční obchod** \> **Parametry zahraničního obchodu**.
2. Na kartě **Intrastat** na pevné záložce **Elektronické hlášení** v poli **Mapování formátu souboru** vyberte **Intrastat INTRACOM (FR)** nebo **Intrastat SAISUNIC (FR)**.
3. V poli **Mapování formátu sestavy** vyberte **Sestava Intrastat**.
4. Na pevné záložce **Hierarchie komoditních kódů** v poli **Hierarchie kategorií** vyberte **Intrastat**.
5. Na pevné záložce **Všeobecné** v poli **Kód transakce** vyberte kód, který se používá pro převody zboží.
6. V poli **Dobropis** vyberte kód, který se použije pro vrácení zboží.
7. V poli **Pracovník** vyberte jméno kontaktní osoby.
8. Na kartě **Kontakt** přidejte informace o kontaktní osobě:

    - Do pole **Telefon** zadejte telefonní číslo kontaktní osoby.
    - Do pole **Fax** zadejte číslo faxu kontaktní osoby.

9. Na kartě **Vlastnosti země/oblasti** v poli **Země/oblast** jsou uvedeny všechny země nebo oblasti, se kterými vaše společnost obchoduje. Pro každou zemi, která je součástí EU, v poli **Typ země/oblasti** vyberte **EU**, aby se země objevila ve vaší sestavě Intrastat. Pro Francii v poli **Typ země/oblasti** vyberte **Domácí**.

### <a name="set-up-compression-of-intrastat"></a>Nastavit kompresi pro systém Intrastat

- Přejděte na **Daň** \> **Nastavení** \> **Zahraniční obchod** \> **Komprese Intrastatu** a vyberte pole, která mají být porovnána, když jsou shrnuty informace Intrastat. Pro francouzský Intrastat vyberte následující pole:
 
    - Statistická procedura
    - Země/oblast původu
    - Přeprava
    - Oprava
    - Země / oblast
    - Okres místa původu či určení
    - Směr
    - Země/oblast odesílatele
    - Kód transakce
    - Zboží

### <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>Nastavte parametry produktu pro prohlášení Intrastat

1. Přejděte na **Řízení informací o produktech** \> **Produkty** \> **Uvolněné produkty**.
2. V mřížce vyberte produkt.
3. Na pevné záložce **Zahraniční obchod** v sekci **Intrastat** v poli **Komodita** vyberte příslušný kód komodity. Název komodity bude vytištěn v poli **Popis zboží** ve výkazu Intrastat.
4. V sekci **Původ** v poli **Země/oblast** vyberte zemi nebo oblast původu produktu.
5. Na záložce s náhledem **Správa zásob** v poli **Čistá hmotnost** zadejte hmotnost produktů v kilogramech.

### <a name="ngp-codes"></a>Kódy NGP

Ve zprávě DEB se kodifikace produktů skládá z následujících prvků:

- Osmimístný kód CN8, který představuje celní a statistickou nomenklaturu EU.
- Je-li to relevantní, jednociferný národní kód položky Nomenklatura Générale des Produits (NGP).

V roce 2022 se NGP vztahuje pouze na tři typy produktů:

- Některé produkty krav, ovcí a koz
- Vojenské vybavení
- Francouzská vína

Musíte nastavit kódy NGP a přiřadit je k souvisejícím produktům. Pole **NGP** se poté automaticky nastaví na stranu **Deník Intrastat**.

#### <a name="set-up-an-ngp-code"></a>Nastavení kódu NGP

1. Přejděte na **Daň** \> **Nastavení** \> **Zahraniční obchod** \> **Kódy transakcí**.
2. V podokně akcí zvolte **Nový**.
3. V poli **NGP** zadejte jednociferný kód.
4. Do pole **Popis** zadejte popis kódu.

#### <a name="assign-an-ngp-code-to-a-product"></a>Přiřazení kódu NGP k produktu

1. Přejděte na **Řízení informací o produktech** \> **Produkty** \> **Uvolněné produkty**.
2. V mřížce vyberte produkt.
3. Na pevné záložce **Zahraniční obchod** v sekci **Intrastat** v poli **NGP** vyberte příslušný kód NGP.

### <a name="set-up-warehouse-parameters-for-the-intrastat-declaration"></a>Nastavení parametrů skladu pro přiznání Intrastat

1. Přejděte na **Řízení skladu** \> **Nastavení** \> **Sklad** \> **Sklady**.
2. Vyberte sklad a poté na pevné záložce **Adresy** vyberte **Přidat** nebo **Upravit**.
3. V dialogovém okně, v poli **Město** vyberte město skladu. Stát nebo provincie města bude pro vaši zprávu DEB použita jako kraj.

### <a name="set-up-the-transport-method"></a>Nastavení metody dopravy

1. Přejděte na **Daň** \> **Nastavení** \> **Zahraniční obchod** \> **Metoda dopravy**.
2. V podokně akcí zvolte **Nový**.
3. V poli **Přeprava** zadejte jedinečný. Společnosti ve Francii používají jednomístné kódy dopravy.

### <a name="intrastat-journal"></a>Deník Intrastat

Přejděte na **Daň** \> **Přiznání** \> **Zahraniční obchod** \> **Intrastat** ke správě vašich transakcí, které se vztahují na zahraniční obchod se zeměmi EU. Další informace naleznete v [Přehledu Intrastat](emea-intrastat.md).

Sloupec **NGP** je specifický pro Francii a zobrazuje kód NGP pro produkt. Pokud se NGP na produkt nevztahuje, zobrazí se **0** (nula). Pro úpravu kódu NGP vyberte transakci a poté na kartě **Obecné** v sekci **Kódy** v poli **NGP** vyberte požadovaný kód NGP.

#### <a name="intrastat-transfer"></a>Přenos Intrastat

Na stránce **Intrastat** v podokně akcí můžete vybrat **Přenos** k automatickému přenosu informací o obchodu uvnitř Společenství z vašich prodejních objednávek, faktury s volným textem, nákupní objednávky, faktury dodavatele, účtenky produktů dodavatele, faktury projektu a objednávky přenosu. Budou přeneseny pouze dokumenty, které mají jako zemi nebo region určení (pro odeslání) nebo zásilku (pro přijetí) zemi EU.

Protože sestava DEB je kombinací EU Sales List a Intrastat report, obsahuje také *trojúhelníkové* transakce, kdy je přímé dodání provedeno z jedné země EU (strana A) do jiné země EU (strana C) a francouzský právní subjekt (strana B) je uprostřed trojúhelníkového obchodu.

#### <a name="generate-a-deb-intrastat-report"></a>Vygenerovat sestavu DEB (Intrastat)

1. Přejděte na **Daň** \> **Deklarace** \> **Zahraniční obchod** \> **Intrastat**.
2. V podokně akcí vyberte **Výstup** \> **Sestava**.
3. V dialogovém okně **Sestava Intrastat** nastavte následující pole.

    | Pole            | popis                                                                                                                         |
    |------------------|-------------------------------------------------------------------------------------------------------------------------------------|
    | Od data        | Vyberte počáteční datum sestavy.                                                                                               |
    | Do data          | Vyberte koncové datum sestavy.                                                                                                 |
    | Generovat soubor    | Tuto možnost nastavte na **Ano**, chcete-li generovat soubor .txt.                                                                                 |
    | Název souboru        | Zadejte název souboru .txt pro sestavu Intrastat.                                                                          |
    | Generovat sestavu  | Tuto možnost nastavte na **Ano**, chcete-li generovat soubor .xml.                                                                                |
    | Název souboru sestavy | Zadejte požadovaný název.                                                                                                            |
    | Pouze oprava | Chcete-li hlásit pouze opravy, nastavte tuto možnost na hodnotu **Ano**. Nastavte ji na **Ne**, chcete-li vykazovat běžné transakce i opravy.         |
    | Směr        | Vyberte **Příjezdy** pro zprávu o příchozích do společenství. Vyberte **Odeslání** pro zprávu o odeslání v rámci komunity. |

4. Zvolte **OK** a zavřete dialogové okno **Sestava Intrastat**.
5. V dialogovém okně **Parametry elektronického výkaznictví** na pevné záložce **Parametry** v poli **Úroveň sestavy** vyberte úroveň sestavy. Úroveň sestavy může být **1 – statistická odpověď**, **4 – daňové přiznání** nebo **5 - statistická odpověď na zásilku a daňové přiznání**.

## <a name="example"></a>Příklad

Následující příklad ukazuje, jak nastavit Francouzský Intrastat a vytvořit zprávu DEB. Použije právnickou osobu **DEMF**.

### <a name="preliminary-setup"></a>Předběžné nastavení

1. V [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/Logon/Index) v knihovně Sdílený majetek si stáhněte nejnovější verze následujících konfigurací ER pro formát přiznání Intrasat:

    - Modul Intrastat
    - Sestava Intrastat
    - Intrastat INTRACOM (FR)

2. Nastavte hierarchii produktů:

    1. Přejděte do nabídky **Řízení informací o produktech** \> **Nastavení** \> **Kategorie a atributy** \> **Hierarchie kategorií**.
    2. V mřížce vyberte **Intrastat**.
    3. V podokně akcí na kartě **Hierarchie kategorií** ve skupině **Spravovat** zvolte **Upravit**.
    4. V podokně akcí vyberte možnost **Nový uzel kategorií**.
    5. Do pole **Název** zadejte **Autres Libournais**.
    6. Do pole **Kód** zadejte **2204 21 42**.
    7. V podokně akcí vyberte **Uložit**.

### <a name="set-up-vat-ids"></a>Nastavení DIČ

#### <a name="set-up-vat-codes-for-your-company"></a>Nastavení DPH pro vaši společnost

1. Přejděte na **Daň** \> **Nastavení** \> **Prodejní daň** \> **Čísla DIČ**.
2. V podokně akcí zvolte **Nový**.
3. V poli **Země/region** vyberte **FRA**.
4. Do pole **DIČ** zadejte **MS123456**.
5. Přejděte na **Správa organizace** \> **Organizace** \> **Právnické osoby** a vyberte **DEMF**.
6. Na pevné záložce **Zahraniční obchod a logistika** v sekci **Intrastat** nastavte pole **Export čísla osvobozeného od DPH** a **Import čísla osvobozeného od DPH** na kód vytvořený v kroku 4.
7. Na pevné záložce **Daňová registrace** do pole **Daňové registrační číslo** zadejte **123456789**.

#### <a name="set-up-the-vat-ids-for-trading-partners"></a>Nastavení čísel DIČ pro obchodní partnery

##### <a name="create-a-registration-type-for-the-company-code"></a>Vytvoření typu registrace pro kód společnosti

1. Přejděte na položky **Správa organizace** \> **Globální adresář** \> **Typy registrace** \> **Typy registrace**.
2. V podokně Akce vyberte možnost **Nová**, vytvoří se typ registrace pro DIČ.
3. V dialogovém okně **Vložit podrobnosti typu registrace** do pole **Název** zadejte **DIČ**.
4. V poli **Země/region** vyberte **DEU**.
5. Vyberte **Vytvořit**.

##### <a name="match-the-registration-type-with-a-registration-category"></a>Spárování typu registrace s kategorií registrace

1. Přejděte na položky **Správa organizace** \> **Globální adresář** \> **Typy registrace** \> **Kategorie registrace**.
2. V podokně akcí vyberte **Nový** pro vytvoření propojení mezi typem registrace a kategorií registrace.
3. Pro typ registrace **DIČ** země **DEU** vyberte kategorii registrace **DIČ**.

##### <a name="set-up-the-customers-vat-registration-number"></a>Nastavení daňového identifikačního čísla zákazníka

1. Přejděte na **Pohledávky** \> **Odběratelé** \> **Všichni odběratelé**.
2. V mřížce vyberte **DE-016**.
3. V podokně Akce na kartě **Zákazník** ve skupině **Registrace** zvolte **ID registrace**.
4. Na pevné záložce **ID registrace** vyberte **Přidat** pro vytvoření ID registrace.
5. V poli **Typ registrace** vyberte **DIČ**.
6. Do pole **Registrační číslo** zadejte **DE9012**.
7. V podokně akcí zvolte **Uložit** a poté zavřete stránku.
8. Na pevné záložce **Faktura a dodávky** v sekci **DPH** v poli **Číslo osvobození od daně** vyberte **DE9012**.

### <a name="set-up-foreign-trade-parameters"></a>Nastavit parametry zahraničního obchodu

1. Přejděte na **Daň** \> **Nastavení** \> **Zahraniční obchod** \> **Parametry zahraničního obchodu**.
2. Na kartě **Intrastat** na pevné záložce **Všeobecné** v poli **Kód transakce** vyberte **11**.
3. Na pevné záložce **Elektronické hlášení** v poli **Mapování formátu souboru** vyberte **Intrastat INTRACOM (FR)**.
4. V poli **Mapování formátu sestavy** vyberte **Sestava Intrastat**.
5. Na pevné záložce **Hierarchie komoditních kódů** v poli **Hierarchie kategorií** vyberte **Intrastat**.
6. V poli **Pracovník** vyberte záznam.
7. Na kartě **Kontakt** zadejte do pole **Telefon** telefonní číslo kontaktní osoby.
8. Do pole **Fax** zadejte číslo faxu kontaktní osoby.

### <a name="create-ngp-code"></a>Vytvoření kódu NGP

1. Přejděte na **Daň** \> **Nastavení** \> **Zahraniční obchod** \> **Kódy transakcí**.
2. V podokně akcí zvolte **Nový**.
3. Do pole **NGP** zadejte **8**.
4. Do pole **Název popisu** zadejte **NGP 8**.
5. V podokně akcí vyberte **Uložit**.

### <a name="set-up-product-information"></a>Nastavení Informací o produktu

1. Přejděte na **Řízení informací o produktech** \> **Produkty** \> **Uvolněné produkty**.
2. V mřížce vyberte **D0001**.
3. Na záložce s náhledem **Zahraniční obchod** v sekci **Intrastat** v poli **NGP** vyberte **8**.
4. V poli **Zboží** vyberte **2204 21 42**.
5. V sekci **Původ** v poli **Země/oblast** vyberte **FRA**.
6. Na záložce s náhledem **Správa zásob** v sekci **Měření hmotnosti** v poli **Čistá hmotnost** zadejte **2**.
7. V podokně akcí zvolte **Uložit** a poté zavřete stránku.
8. V mřížce vyberte **D0003**.
9. Na záložce s náhledem **Zahraniční obchod** v sekci **Intrastat** v poli **Komodita** vyberte **100 200 30**.
10. V sekci **Původ** v poli **Země/oblast** vyberte **DEU**.
11. Na záložce s náhledem **Správa zásob** v sekci **Měření hmotnosti** v poli **Čistá hmotnost** zadejte **5**.
12. V podokně akcí vyberte **Uložit**.

### <a name="set-up-regime-codes"></a>Nastavení kódů režimu

1. Přejděte na **Daň** \> **Nastavení** \> **Zahraniční obchod** \> **Statistická procedura**.
2. V podokně akcí zvolte **Nový**.
3. Do pole **Statistická procedura** zadejte **21**.
4. Do pole **Text 1** zadejte **Kód režimu 21**.

### <a name="change-the-site-address"></a>Změňte adresu webu

1. Přejděte do nabídky **Řízení skladu** \> **Nastavení** \> **Sklad** \> **Pracoviště**.
2. V mřížce vyberte **1**.
3. Na záložce s náhledem **Adresy** vyberte **Upravit**.
4. V dialogovém okně **Upravit adresu** v poli **Země/oblast** vyberte **FRA**.
5. Vyberte **OK**.
6. Přejděte na **Správu skladu** \> **Založit** \> **Sklad** \> **Sklady** a vyberte sklad.
7. Na záložce s náhledem **Adresy** vyberte **Přidat**.
8. V dialogovém okně **Nová adresa** v poli **Země/oblast** vyberte **FRA**.
9. V poli **Město** vyberte **Bordeaux**.
10. Zvolte **OK** a zavřete dialogové okno.

### <a name="set-up-a-transport-method"></a>Nastavení metody dopravy

1. Přejděte na **Daň** \> **Nastavení** \> **Zahraniční obchod** \> **Metoda dopravy**.
2. V podokně akcí zvolte **Nový**.
3. Do pole **Doprava** zadejte **3**.
4. V poli **Popis** zadejte hodnotu **Silniční doprava**.

### <a name="assign-a-transport-mode-to-a-mode-of-delivery"></a>Přiřazení způsobu dopravy ke způsobu doručení

1. Přejděte na **Zásobování a zdroje** \> **Nastavení** \> **Distribuce** \> **Způsoby doručení**.
2. V mřížce vyberte **50**.
3. Na pevné záložce **Zahraniční obchod** v poli **Přeprava** vyberte **3**.

### <a name="create-a-sales-order-with-an-eu-customer-that-includes-the-new-product"></a>Vytvoření prodejní objednávky se zákazníkem z EU, která obsahuje nový produkt

1. Přejděte na **Pohledávky** \> **Objednávky** \> **Všechny prodejní objednávky**.
2. V podokně akcí zvolte **Nový**.
3. V dialogovém okně **Vytvoření prodejní objednávky** v sekci **Zákazní** vyberte v poli **Účet zákazníka** hodnotu **DE-016**.
4. V sekci **Adresa** v poli **Doručovací adresa** vyberte znaménko plus (**+**) k vytvoření adresy.
5. V dialogovém okně **Nová adresa** v poli **Název popisu** zadejte **Německo**.
6. V poli **Země/region** vyberte **DEU**.
7. Vyberte **OK**.
8. Vyberte **OK** v dialogovém okně **Vytvoření prodejní objednávky**.
9. Na pevné záložce **Řádky prodejní objednávky** v poli **Číslo položky** vyberte **0001**.
10. Na pevné záložce **Podrobnosti řádků** na kartě **Zahraniční obchod** v poli **Statistická procedura** vyberte **21**.
11. V poli **Stát původu** vyberte **AL**.
12. V podokně akcí vyberte **Uložit**.
13. Na kartě **Záhlaví** na pevné záložce **Doručení** v poli **Způsob doručení** se ujistěte, že je vybrána hodnota **50**.
14. V podokně akcí na kartě **Faktura** ve skupině **Generovat** zvolte **Faktura**.
15. V dialogovém okně **Účtování faktury** na pevné záložce **Parametry** v sekci **Parametr**, v poli **Množství** vyberte **Všechny**. Poté vyberte **OK** pro zaúčtování faktury.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Přeneste transakci do deníku Intrastat a zkontrolujte výsledek

1. Přejděte na **Daň** \> **Deklarace** \> **Zahraniční obchod** \> **Intrastat**.
2. V podokně akcí zvolte **Převod**.
3. V dialogovém okně **Intrastat (přenos)** v sekci **Parametry** nastavte možnost **Zákaznická faktura** na **Ano**. Pak vyberte **OK**.
4. Seřaďte transakce podle pole **Datum**. Horní transakce je výsledná transakce.

    ![Řádek, který představuje prodejní objednávku na stránce Intrastat.](media/intrastat_fr_1.png)

5. Vyberte řádek transakce a poté vyberte kartu **Obecné**, čímž zobrazíte další podrobnosti.

    ![Podrobnosti o prodejní objednávce na kartě Obecné na stránce Intrastat.](media/intrastat_fr_2.png)

6. V podokně akcí vyberte **Výstup** \> **Sestava**.
7. V dialogovém okně **Sestava Intrastat** na pevné záložce **Parametry** v sekci **Datum** vyberte měsíc prodejní objednávky, kterou jste vytvořili.
8. V sekci **Možnosti exportu** nastavte možnost **Generovat soubor** na **Ano**.
9. Do pole **Název souboru** zadejte požadovaný název.
10. Zvolte **OK** a zavřete dialogové okno **Sestava Intrastat**.
11. V dialogovém okně **Parametry elektronického výkaznictví** na pevné záložce **Parametry** na kartě **Úroveň sestavy** vyberte **5 – statistická odpověď na zásilku a daňové přiznání** a sestavu si prohlédněte.

    ![Sestava Intracom pro odchozí položky.](media/intrastat_fr_3.png)

12. Prohlédněte si generovanou sestavu Excel.

    ![Sestava Intrastat pro odchozí položky.](media/intrastat_fr_4.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
