---
title: Intrastat - Polsko
description: Tento článek obsahuje informace o sestavě Intrastat v Polsku.
author: andosip
ms.date: 11/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.openlocfilehash: 45bd1d3c90d0a8a8ad5db6d0b80c5eed0aa489e8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871094"
---
# <a name="polish-intrastat"></a>Intrastat - Polsko

[!include[banner](../includes/banner.md)]

Stránka **Intrastat** se použije pro vygenerování a nahlášení informací o obchodu mezi zeměmi Evropské unie (EU). Polské prohlášení Intrastat obsahuje informace o obchodu se zbožím pro vykazování.

V polské deklaraci Intrastat jsou zahrnuta následující pole. Všechna pole jsou zahrnuta v příjezdech a odesláních kromě **RodzajTransportu** (způsob dopravy) a **KrajPochodzenia** (země nebo region původu), které nejsou uvedeny v zásilkách, a **IdKontrahenta** (zahraniční DIČ zákazníka), které není zahrnuto při příjezdu.

| Název pole | Popis |
|-------------------------|-------------------------|
| Deklaracja Data | Datum vytvoření dokumentu. |
| Miesiac | Referenční měsíc prohlášení. |
| Rok | Referenční rok prohlášení. |
| Numer | Číslo prohlášení v referenčním období. |
| Wersja | Číslo verze prohlášení. |
| NrWlasny | Identifikátor prohlášení. Tato hodnota je generována automaticky. |
| Typ | Směr sestavy.</br><li>U příchozích je vytištěno „P“.</li><li>U odchozích položek se tiskne "W".</li> |
| Rodzaj | Typ prohlášení. Hodnota udává, zda je sestava původním prohlášením nebo opravným prohlášením. |
| UC | Kód jednotky, na kterou je určen Výkaz pro Intrastat. Hodnota je uvedena v poli **DIČ** v sekci **Prodejní daň** na kartě **Agwnt** na stránce **Parametry zahraničního obchodu**. |
| Nazwa | Název společnosti. |
| Miejscowosc, UlicaNumer, KodPocztowy | Úplná adresa právnické osoby. |
| Nip | Polské daňové identifikační číslo (ID daně z přidané hodnoty [DPH]). |
| Regon | Polské statistické identifikační číslo (číslo podniku). |
| LacznaWartoscFaktur | Součet hodnot faktury. |
| LacznaWartoscStatystyczna | Součet statistických hodnot. |
| LacznaLiczbaPozycji | Celkový počet položek zboží. |
| PozId | Pořadové číslo dané položky zboží. |
| OpisTowaru | Obchodní název komodity. |
| KrajPochodzeniaWysylki | Kód země nebo oblasti protistrany používaný Mezinárodní organizací pro normalizaci (ISO) |
| WarunkiDostawy | Kód Intrastat pro dodací podmínky. |
| RodzajTransakcji | Kód, který označuje povahu transakce. Společnosti v Polsku používají dvoumístné transakční kódy. |
| KodTowarowy | Osmimístný kód zboží podle kombinované nomenklatury. |
| RodzajTransportu | Kód Intrastat pro zplsob dopravy. |
| KrajPochodzenia | ISO kód země nebo regionu, kde byly komodity vyrobeny. |
| MasaNetto | Čistá hmotnost v celých kilogramech. |
| IloscUzupelniajacaJm | Množství v doplňkové měrné jednotce v celých číslech. |
| WartoscFaktury | Fakturovaná hodnota všech transakcí, které jsou pokryty jednou položkou. |
| WartoscStatystyczna | Statistická hodnota. |
| Wypelniajacy: NazwiskoImie, Telefon, Faks, Email | Jméno a příjmení, telefonní číslo, faxové číslo a e-mailová adresa osoby, která prohlášení podává. |
| IdKontrahenta | Zahraniční DIČ zákazníka v členském státě EU. |


## <a name="set-up-intrastat"></a>Vytvořit Intrastat

Z globálního úložiště importujte poslední verzi následujících konfigurací elektronického výkaznictví (ER):

   - Modul Intrastat
   - Sestava Intrastat
   - Intrastat (PL)

Další informace viz [Stáhněte si konfigurace elektronického výkaznictví z Globálního úložiště konfigurační služby](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Nastavte DIČ a číslo firmy pro vaši společnost

### <a name="create-registration-types-for-company-codes"></a>Vytvořte typy registrace pro kódy společností

Musíte vytvořit dva typy registrace pro kódy společnosti: jeden pro DIČ (kód NIP) a jeden pro číslo podniku (kód regionu).

1. Přejděte na položky **Správa organizace** > **Globální adresář** > **Typy registrace** > **Typy registrace**.
2. V podokně Akce vyberte možnost **Nová**, vytvoří se typ registrace pro DIČ.
3. V dialogovém okně **Vložit podrobnosti typu registrace** zadejte v poli **Název** název typu registrace. Například zadejte **NIP**.
4. V poli **Země/region** vyberte **POL**.
5. Vyberte **Vytvořit**.
6. V podokně Akce vyberte možnost **Nová**, vytvoří se typ registrace pro číslo podniku.
7. V dialogovém okně **Vložit podrobnosti typu registrace** zadejte v poli **Název** název typu registrace. Například zadejte **Regon**.
8. V poli **Země/region** vyberte **POL**.
9. Vyberte **Vytvořit**.

### <a name="match-the-registration-types-with-registration-categories"></a>Spojte typy registrace s kategoriemi registrace

1. Přejděte na položky **Správa organizace** > **Globální adresář** > **Typy registrace** > **Kategorie registrace**.
2. V podokně akcí vyberte **Nový** pro vytvoření propojení mezi každým typem registrace, který jste vytvořili, a kategorií registrace.

    - Pro typ registrace pro DIČ (kód NIP) vyberte **DIČ** kategorie registrace.
    - Pro typ registrace pro číslo podniku (kód Regon) vyberte **ID podniku (COID)** kategorie registrace.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Nastavte DIČ a číslo firmy pro vaši společnost

1. Přejděte do části na **Správa organizace** > **Organizace** > **Právnické osoby**.
2. V mřížce vyberte svoji společnost.
3. V podokně Akce vyberte možnost **ID registrace**.
4. Na pevné záložce **ID registrace** vyberte **Přidat**.
5. V poli **Typ registrace** vyberte jeden z typů registrace, které jste vytvořili dříve.
6. Zadejte DIČ vaší společnosti (kód NIP) nebo podnikové číslo (kód Regon) v závislosti na typu registrace, který jste vybrali v předchozím kroku.
7. Opakujte kroky 4 až 6 pro jiný typ registrace, který jste vytvořili dříve.

## <a name="set-up-a-company-address"></a>Nastavení adresy společnosti

1. Přejděte do části na **Správa organizace** > **Organizace** > **Právnické osoby**.
2. V mřížce vyberte svoji společnost.
3. Na kartě **Adresy** vyberte **Upravit**.
4. V dialogovém okně **Upravit adresu** v poli **PSČ** vyberte PSČ vaší společnosti.
5. Do pole **Ulice** zadejte svou adresu.
6. V poli **Město** vyberte své město.

## <a name="set-up-foreign-trade-parameters"></a>Nastavit parametry zahraničního obchodu

1. Přejděte na **Daň** > **Nastavení** > **Parametry zahraničního obchodu**.
2. Na kartě **Intrastat** na záložce s náhledem **Elektronické hlášení** v poli **Mapování formátu souboru** vyberte **Intrastat (PL)**.
3. V poli **Mapování formátu sestavy** vyberte **Sestava Intrastat**.
4. Na pevné záložce **Hierarchie komoditních kódů** v poli **Hierarchie kategorií** vyberte **Intrastat**.
5. V poli **Kód transakce** vyberte kód transakce pro převody majetku. Tento kód použijete pro transakce, které provádí skutečné nebo plánované převody majetku v souvislosti s kompenzací (finanční nebo jinou). Použijete jej také pro opravy. Společnosti v Polsku používají dvoumístné transakční kódy.
6. V poli **Dobropis** vyberte kód transakce pro vrácení zboží.
7. Na kartě **Vlastnosti země/oblasti** v poli **Země/oblast** jsou uvedeny všechny země nebo oblasti, se kterými vaše společnost obchoduje. Pro každou zemi, která je součástí EU, v poli **Typ země/oblasti** vyberte **EU**, aby se země objevila ve vaší sestavě Intrastat. Pro Polsko v poli **Typ země/oblasti** vyberte **Domácí**.
8. Na kartě **Agent** na záložce s náhledem **Agent** v sekci **DPH** v poli **DIČ** zadejte **420000** k uvedení kódu jednotky, které je Výkaz určen pro Intrastat.
9. Na kartě **Kontakt** zadejte jméno, telefonní číslo, faxové číslo a e-mailovou adresu osoby, která prohlášení podává.
10. Na kartě **Číselné řady** v poli **Kód číselné řady** pro odkaz **Číslo souboru XML** zadejte nesouvislou číselnou řadu, která má maximálně devět znaků. Toto pole se používá k automatickému vygenerování hodnoty pro pole **Identifikátor prohlášení** ve výkazu Intrastat.

## <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>Nastavte parametry produktu pro prohlášení Intrastat

1. Přejděte na **Řízení informací o produktech** > **Produkty** > **Uvolněné produkty**.
2. V mřížce vyberte produkt.
3. Na pevné záložce **Zahraniční obchod** v sekci **Intrastat** v poli **Komodita** vyberte příslušný kód komodity. Název komodity bude vytištěn v poli **Popis zboží** ve výkazu Intrastat.
4. V sekci **Původ** v poli **Země/oblast** vyberte zemi nebo oblast původu produktu.
5. Na záložce s náhledem **Správa zásob** v poli **Čistá hmotnost** zadejte hmotnost produktů v kilogramech.

## <a name="set-up-compression-of-intrastat"></a>Nastavit kompresi pro systém Intrastat

-   Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Komprese Intrastatu** a vyberte pole, která mají být porovnána po shrnutí informací Intrastat. Pro polský Intrastat vyberte následující pole:

    - Zboží
    - Kód transakce
    - Země/oblast původu
    - Přeprava
    - Dodací podmínky
    - Země/oblast odesílatele
    - Země/oblast
    - Oprava
    - DIČ
    - Směr
    - Faktura

## <a name="set-up-the-transport-method-and-delivery-terms"></a>Nastavte způsob dopravy a dodací podmínky

1.  Nastavte kódy dopravy.

    1. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Metoda dopravy**.
    2. V podokně akcí zvolte **Nový**.
    3. V poli **Přeprava** zadejte jedinečný. Společnosti v Polsku používají jednomístné kódy dopravy.

2.  Nastavte kódy Intrastat pro způsob doručení.

    1. Přejděte na **Zásobování a zdroje** > **Nastavení** > **Distribuce** > **Podmínky doručení**.
    2. V mřížce vyberte sadu dodacích podmínek.
    3. Na záložce s náhledem **Obecné** v poli **Kód Intrastat** zadejte jedinečný kód.

## <a name="intrastat-transfer"></a>Přenos Intrastat

Na stránce **Intrastat** v podokně akcí můžete vybrat **Přenos** k automatickému přenosu informací o obchodu uvnitř Společenství z vašich prodejních objednávek, faktury s volným textem, nákupní objednávky, faktury dodavatele, účtenky produktů dodavatele, faktury projektu a objednávky přenosu. Budou přeneseny pouze dokumenty, které mají jako zemi nebo region určení nebo zásilku zemi EU.

Také můžete ručně zadat transakce výběrem **Nový** v podokně akcí.

### <a name="generate-an-intrastat-report"></a>Vygenerovat sestavu Intrastat

1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**.
2. V podokně akcí vyberte **Výstup** &gt; **Sestava**.
3. V dialogovém okně **Sestava Intrastat** nastavte následující pole.

    | Pole | Popis |
    |-------------------------|-------------------------|
    | Od data | Vyberte počáteční datum sestavy. |
    | Generovat soubor | Tuto možnost nastavte na **Ano**, chcete-li generovat soubor .xml pro vaši sestavu Intrastat. |
    | Název souboru | Zadejte název souboru .xml. |
    | Generovat sestavu | Tuto možnost nastavte na **Ano**, chcete-li generovat soubor .xlxs pro vaši sestavu Intrasat. |
    | Název souboru sestavy | Zadejte název souboru .xlxs. |
    | Směr | Vyberte **Příjezdy** pro zprávu o příchozích do společenství.</br>Vyberte **Odeslání** pro zprávu o odeslání v rámci komunity. |
    | Identifikátor prohlášení | ID dokumentu se generuje automaticky a lze jej aktualizovat. |
    | Typ prohlášení | Vyberte **Prohlášení** pro původní prohlášení.</br>Vyberte **Oprava prohlášení – výměna** pro opravné prohlášení, které má plně nahradit stávající, dříve podaný originál nebo opravné prohlášení. |
    | Město vytvoření dokladu | Zadejte hodnotu, která má být vytištěna v poli **Miejscowosc** ve Výkazu pro Intrastat. |
    | Datum vytvoření dokladu | Zadejte hodnotu, která má být vytištěna v poli **Deklaracja Data** ve Výkazu pro Intrastat. |
    | Číslo dokladu | Zadejte hodnotu, která má být vytištěna v poli **Numer** ve Výkazu pro Intrastat. |
    | Verze dokumentu | Zadejte hodnotu, která má být vytištěna v poli **Wersja** ve Výkazu pro Intrastat. |

4. Vyberte **OK** a zkontrolujte vygenerové sestavy.

## <a name="example"></a>Příklad

Tento příklad ukazuje, jak zaúčtovat příchozí a odchozí zásilky pro Intrastat pomocí právnické osoby **DEMF**.

### <a name="preliminary-setup"></a>Předběžné nastavení

Importujte nejnovější verzi následujících konfigurací ER:

   - Modul Intrastat
   - Sestava Intrastat
   - Intrastat (PL)

### <a name="set-up-a-company-address"></a>Nastavení adresy společnosti

1. Přejděte do nabídky **Správa organizace** > **Globální adresář** > **Globální adresář** > **Nastavení adresy**.
2. Na kartě **Město** vyberte možnost **Nová**.
3. V poli **Země/region** vyberte **POL**.
4. Do pole **Mněsto** zadejte **Varšava**.
5. Na kartě **PSČ** vyberte možnost **Nová**.
6. V poli **Země/region** vyberte **POL**.
7. V poli **Město** vyberte **Varšava**.
8. V poli **PSČ** zadejte **00-844**.
9. Přejděte na **Správa organizace** > **Organizace** > **Právnické osoby** a vyberte právnickou osobu **DEMF**.
10. Na záložce s náhledem **Adresy** vyberte **Upravit**.
11. V poli **Země/region** vyberte **POL**.
12. V poli **PSČ** vyberte **31-111**.
13. Do pole **Ulice** zadejte **Statystyczna 22/1**.
14. V poli **Město** vyberte **Varšava**.
15. Vyberte **OK**.

## <a name="set-up-a-vat-id-and-an-enterprise-number-code-for-your-company"></a>Nastavte DIČ a kód čísla firmy pro vaši společnost

### <a name="create-registration-types-for-company-codes"></a>Vytvořte typy registrace pro kódy společností

1. Přejděte na položky **Správa organizace** > **Globální adresář** > **Typy registrace** > **Typy registrace**.
2. V podokně Akce vyberte možnost **Nová**, vytvoří se typ registrace pro DIČ (kód NIP).
3. V dialogovém okně **Vložit podrobnosti typu registrace** do pole **Název** zadejte **NIP**.
4. V poli **Země/region** vyberte **POL**.
5. Vyberte **Vytvořit**.
6. V podokně Akce vyberte možnost **Nová**, vytvoří se typ registrace pro číslo podniku (kód Regon).
7. V dialogovém okně **Vložit podrobnosti typu registrace** do pole **Název** zadejte **Regon**.
8. V poli **Země/region** vyberte **POL**.
9. Vyberte **Vytvořit**.

### <a name="match-the-registration-types-with-registration-categories"></a>Spojte typy registrace s kategoriemi registrace

1. Přejděte na položky **Správa organizace** > **Globální adresář** > **Typy registrace** > **Kategorie registrace**.
2. V podokně akcí vyberte **Nový** pro vytvoření propojení mezi každým typem registrace, který jste vytvořili, a kategorií registrace.

    - Pro typ registrace pro **NIP** vyberte **DIČ** kategorie registrace.
    - Pro typ registrace **Regon** vyberte **ID podniku (COID)** kategorie registrace.

### <a name="set-up-a-vat-id-and-an-enterprise-number-for-your-company"></a>Nastavte DIČ a číslo firmy pro vaši společnost

1. Přejděte do části na **Správa organizace** > **Organizace** > **Právnické osoby**.
2. V mřížce vyberte **DEMF**.
3. V podokně Akce vyberte možnost **ID registrace**.
4. Na pevné záložce **ID registrace** vyberte **Přidat**.
5. V poli **Typ registrace** vyberte **NIP**.
6. Do pole **Registrační číslo** zadejte **1234567890**.
7. Vyberte **přidat**.
8. V poli **Typ registrace** vyberte **Regon**.
9. Do pole **Registrační číslo** zadejte **12345678901234**.

### <a name="set-up-a-number-sequence-code"></a>Nastavte kód číselné řady

1. Přejděte na **Správa organizace** > **Číselné řady** > **Číselné řady**.
2. V podokně akcí na kartě **Číselná řada** ve skupině **Nový** vyberte **Číselná řada**.
3. V záložce s náhledem **Identifikace** v poli **Kód číselné řady** zadejte **XML\_soubor**.
4. Na záložce s náhledem **Parametry rozsahu** v poli **Rozsah** vyberte **Společnost**.
5. V poli **Společnost** vyberte **DEMF**.
6. V záložce s náhledem **Segmenty** v poli **Délka** pro **Alfanumerický** segment zadejte **4**.
7. Na záložce s náhledem **Obecné** v části **Nastavení** nastavte možnost **Souvislé** na **Ne**.
8. V sekci **Přidělení čísel** v poli **Největší** zadejte **9999**.

### <a name="set-up-foreign-trade-parameters"></a>Nastavit parametry zahraničního obchodu

1. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Parametry zahraničního obchodu**.
2. Na kartě **Intrastat** na záložce s náhledem **Obecné** v poli **Kód** **transakce** vyberte **11**.
3. Na záložce s náhledem **Elektronické výkaznictví** v poli **Mapování formátu souboru** vyberte **Intrastat (PL)**.
4. V poli **Mapování formátu sestavy** vyberte **Sestava Intrastat**.
5. Na záložce s náhledem **Hierarchie komoditních kódů** ověřte, že je pole **Hierarchie kategorií** nastaveno na **Intrastat**.
6. Na kartě **Vlastností země/oblasti** vyberte **Nová**.
7. V poli **Země/oblast strany** vyberte **POL**. Pak v poli **Typ země/oblasti** vyberte **Domácí**.
8. V poli **Země/oblast strany** vyberte **DEU**. Pak v poli **Typ země/oblasti** vyberte **EU**.
9. Na kartě **Agent** na záložce s náhledem **Agent** v sekci **DPH** v poli **DIČ** zadejte **420000**.
10. Na kartě **Kontakt** v poli **Název** zadejte **Manish Chopra**.
11. V poli **Telefon** zadejte hodnotu **425-555-5068**.
12. Do pole **Faxové číslo** zadejte hodnotu **425-555-5049**.
13. V poli **E-mail** zadejte **manishc@contoso.com**.
14. Na kartě **Číselné řady** v poli **Kód číselné řady** pro odkaz **číslo souboru XML** vyberte **XML\_file**.

### <a name="set-up-product-information"></a>Nastavení Informací o produktu

1. Přejděte na možnosti **Řízení informací o produktech** > **Produkty** > **Uvolněné** **produkty**.
2. V mřížce vyberte **D0001**.
3. Na záložce s náhledem **Zahraniční obchod** v sekci **Intrastat** v poli **Komodita** vyberte **100 200 30**.
4. Na záložce s náhledem **Správa zásob** v sekci **Měření hmotnosti** v poli **Čistá hmotnost** zadejte **2**.
5. V podokně akcí vyberte **Uložit**.
6. V mřížce vyberte **D0003**.
7. Na záložce s náhledem **Zahraniční obchod** v sekci **Intrastat** v poli **Komodita** vyberte **100 200 30**.
8. V sekci **Původ** v poli **Země/oblast** vyberte **DEU**.
9. Na záložce s náhledem **Správa zásob** v sekci **Měření hmotnosti** v poli **Čistá hmotnost** zadejte **5**.
10. V podokně akcí vyberte **Uložit**.

### <a name="change-the-site-address"></a>Změňte adresu webu

1. Přejděte do nabídky **Warehouse Management** > **Nastavení** > **Sklad** > **Pracoviště**.
2. V mřížce vyberte **1**.
3. Na záložce s náhledem **Adresy** vyberte **Upravit**.
4. V dialogovém okně **Upravit adresu** v poli **Země/oblast** vyberte **POL**.
5. Vyberte **OK**.

### <a name="set-up-a-transport-method"></a>Nastavení metody dopravy

1. Vytvoření metody přepravy.

    1. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Metoda dopravy**.
    2. V podokně akcí zvolte **Nový**.
    3. Do pole **Doprava** zadejte **3**.
    4. V poli **Popis** zadejte hodnotu **Silniční doprava**.

2. Přiřazení nové metody přepravy ke způsobu dodání. Tímto způsobem nastavíte výchozí hodnoty, které se použijí pro způsob dopravy při výběru odpovídajícího způsobu doručení.

    1. Přejděte na **Zásobování a zdroje** > **Nastavení** > **Distribuce** > **Způsoby doručení**.
    2. V mřížce vyberte **10**.
    3. Na pevné záložce **Zahraniční obchod** v poli **Přeprava** vyberte **3**.

3. Vyberte výchozí způsob doručení pro zákazníka.

    1. Přejděte na **Pohledávky** > **Odběratelé** > **Všichni odběratelé**.
    2. V mřížce vyberte **DE-016**.
    3. Na záložce s náhledem **Faktura a doručení** v poli **Režim doručení** vyberte **10**.

4. Vyberte výchozí způsob doručení pro dodavatele.

    1. Přejděte do části **Závazky** > **Dodavatelé** > **Všichni dodavatelé**.
    2. V mřížce vyberte **DE-001**.
    3. Na záložce s náhledem **Faktura a doručení** v poli **Režim doručení** vyberte **10**.

### <a name="set-up-codes-for-terms-of-delivery"></a>Nastavit kódy pro podmínky dodání.

1. Nastavte kód Intrastat pro dodací podmínky.

    1. Přejděte na **Zásobování a zdroje** > **Nastavení** > **Distribuce** > **Podmínky doručení**.
    2. V mřížce vyberte **CIF**.
    3. Na záložce s náhledem **Obecné** v poli **Kód Intrastat** zadejte **CIF**.

2. Vyberte výchozí podmínky doručení pro zákazníka.

    1. Přejděte na **Pohledávky** > **Odběratelé** > **Všichni odběratelé**.
    2. V mřížce vyberte **DE-016**.
    3. Na záložce s náhledem **Faktura a doručení** v poli **Podmínky doručení** vyberte **CIF**.

3. Vyberte výchozí podmínky doručení pro dodavatele.

    1. Přejděte do části **Závazky** > **Dodavatelé** > **Všichni dodavatelé**.
    2. V mřížce vyberte **DE-001**.
    3. Na záložce s náhledem **Faktura a doručení** v poli **Podmínky doručení** vyberte **CIF**.

### <a name="verify-an-eu-customers-tax-exempt-number-code"></a>Ověřte kód DIČ odběratele z EU

1. Přejděte na **Pohledávky** > **Odběratelé** > **Všichni odběratelé**.
2. V mřížce vyberte **DE-016**.
3. Na záložce s náhledem **Faktura a dodávky** v sekci **DPH** ověřte, že je pole **DIČ** nastaveno na **DE9012**.

### <a name="create-a-sales-order-with-an-eu-customer"></a>Vytvořte prodejní objednávku se zákazníkem z EU

1. Přejděte na **Pohledávky** > **Objednávky** > **Všechny prodejní objednávky**.
2. V podokně akcí zvolte **Nový**.
3. V dialogovém okně **Vytvořit prodejní objednávku** na záložce s náhledem **Zákazník** v sekci **Zákazník** vyberte v poli **Účet zákazníka** hodnotu **DE-016**.
4. Na záložce s náhledem **Obecné** v sekci **Dimenze úložiště** v poli **Lokalita** vyberte **1**.
5. V poli **Sklad** zvolte **11**.
6. Na kartě **Adresa** ověřte, že je pole **Adresa** nastaveno na **Teichgasse 12, Kiel, 24103, DEU**, protože zákazník je z Německa.
7. Vyberte **OK**.
8. Na kartě **Záhlaví** na záložce s náhledem **Doručení** ověřte, že je pole **Podmínky doručení** nastaveno na **CIF** a pole **Způsob doručení** je nastaveno na **10**.
9. Na kartě **Řádky** na záložce s náhledem **Řádky prodejní objednávky** v poli **Číslo položky** vyberte **D0001**. Poté do pole **Množství** zadejte **8**.
10. Na záložce s náhledem **Podrobnosti řádku** na kartě **Zahraniční obchod** ověřte, že je pole **Kód transakce** nastaveno na **11**, pole **Komodita** je nastaveno na **100 200 30** a pole **Země/oblast původu** je nastaveno na **POL**.
11. V podokně akcí vyberte **Uložit**.
12. V podokně akcí na kartě **Faktura** ve skupině **Generovat** zvolte **Faktura**.
13. V dialogovém okně **Účtování faktury** na pevné záložce **Parametry** v sekci **Parametr**, v poli **Množství** vyberte **Všechny**.
14. Na záložce s náhledem **Nastavení** v poli **Datum prodeje** vyberte **10/18/2021** (18. října 2021).
15. Výběrem tlačítka **OK** zaúčtujte fakturu.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Přeneste transakci do deníku Intrastat a zkontrolujte výsledek

1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**.
2. V podokně akcí zvolte **Převod**.
3. V dialogovém okně **Intrastat (přenos)** v sekci **Parametry** nastavte možnost **Zákaznická faktura** na **Ano**.
4. Vyberte **Filtr**.
5. V dialogovém okně **Filtr Intrastat** na kartě **Rozsah** vyberte první řádek a ujistěte se, že pole **Pole** je nastaveno na **Datum**.
6. V poli **Kritéria** vyberte aktuální datum.
7. Zvolte **OK** a zavřete dialogové okno **Filtr Intrastat**.
8. Vyberte **OK** pro zavření dialogového okna **Intrastat (převod)** a zkontrolujte výsledek. Řádek představuje prodejní objednávku, kterou jste vytvořili dříve.

    ![Řádek, který představuje prodejní objednávku na stránce Intrastat](media/intrastat_pl_1.png)

9. Vyberte řádek transakce a poté vyberte kartu **Obecné**, čímž zobrazíte další podrobnosti.

    ![Podrobnosti o prodejní objednávce na kartě Obecné na stránce Intrastat](media/intrastat_pl_2.png)

10. V podokně akcí vyberte **Výstup** > **Sestava**.
11. V dialogovém okně **Sestava Intrastat** na záložce s náhledem **Parametry** v sekci **Datum** v poli **Od data** vyberte první den aktuálního měsíce.
12. V sekci **Možnosti** **exportu** nastavte možnost **Generovat soubor** na **Ano**. Potom do pole **Název souboru** zadejte požadovaný název.
13. Nastavte možnost **Generovat sestavu** na **Ano**. Potom do pole **Název souboru sestavy** zadejte požadovaný název.
14. V poli **Směr** vyberte hodnotu **Expedice**.
15. V sekci **Mapování formátu souboru** ověřte, že je poel **Typ prohlášení** nastaveno na **Prohlášení**.
16. V poli **Město tvorby dokumentů** zadejte **Krakov**.
17. V poli **Datum vytvoření dokumentu** vyberte **10/19/2021** (19. října 2021).
18. Do pole **Číslo dokumentu** zadejte **11**.
19. Do pole **Verze dokumentu** zadejte **22**.
20. Vyberte **OK** a zkontrolujte vygenerovanou sestavu ve formátu XML. Následující tabulka zobrazuje hodnoty v ukázkové sestavě.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Název pole</strong></p>
    </td>
    <td>
    <p><strong>Popis pole</strong></p>
    </td>
    <td>
    <p><strong>Hodnota</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Informace o dokumentu.</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja Data</p>
    </td>
    <td>
    <p>Datum vytvoření dokumentu.</p>
    </td>
    <td>
    <p>2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>Město vytvoření dokumentu.</p>
    </td>
    <td>
    <p>Krakov</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>Celkový počet položek.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>Celková statistická hodnota.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>Celková fakturovaná hodnota.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>Kód jednotky.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Typ prohlášení.</p>
    </td>
    <td>
    <p>D</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>Verze dokumentu.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Numer</p>
    </td>
    <td>
    <p>Číslo dokumentu.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="330">
    <p>Měsíc odkazu.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="330">
    <p>Rok odkazu.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Typ</p>
    </td>
    <td width="330">
    <p>Směr sestavy.</p>
    </td>
    <td>
    <p>W</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>NrWlasny</p>
    </td>
    <td width="330">
    <p>Identifikátor prohlášení.</p>
    </td>
    <td>
    <p>21ISTDEMF-0001</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Informace o společnosti.</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscowosc</p>
    </td>
    <td width="330">
    <p>Město, ve kterém se společnost nachází.</p>
    </td>
    <td>
    <p>Varšava</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regon</p>
    </td>
    <td width="330">
    <p>Kód Regon společnosti.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>Kód NIP společnosti.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztowy</p>
    </td>
    <td>
    <p>Kód PSČ společnosti.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>Ulice, ve které se společnost nachází.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>Název společnosti.</p>
    </td>
    <td>
    <p>Contoso Entertainment System Germany</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Informace o zboží</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>Statistická hodnota.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscFaktury</p>
    </td>
    <td>
    <p>Hodnota faktury.</p>
    </td>
    <td>
    <p>2632</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>Čistá hmotnost.</p>
    </td>
    <td>
    <p>16</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>IdKontrahenta</p>
    </td>
    <td>
    <p>DIČ zákazníka.</p>
    </td>
    <td>
    <p>DE9012</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarowy</p>
    </td>
    <td>
    <p>Kód komodity.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Kód transakce.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WarunkiDostawy</p>
    </td>
    <td>
    <p>Režim podmínek dodání.</p>
    </td>
    <td>
    <p>CIF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzeniaWysylki</p>
    </td>
    <td>
    <p>Kód země nebo oblasti odeslání/místa určení.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>Popis komodit.</p>
    </td>
    <td>
    <p>Hardware</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId</p>
    </td>
    <td>
    <p>Číslo položky.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p><strong>Kontaktní informace</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>E-mail</p>
    </td>
    <td>
    <p>E-mailová adresa podávající osoby.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>Číslo faxu podávající osoby.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefon</p>
    </td>
    <td>
    <p>Číslo telefonu podávající osoby.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>Jméno podávající osoby.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

21. Zkontrolujte vygenerovaný soubor ve fromátu Excel.

    ![Sestava Intrastat pro odchozí položky](media/intrastat_pl_3.png)

### <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky

1. Přejděte na **Závazky** > **Nákupní objednávky** > **Všechny nákupní objednávky**.
2. V podokně akcí zvolte **Nový**.
3. V dialogovém okně **Vytvoření nákupní objednávky** v poli **Účet dodavatele** vyberte **DE-001**.
4. V poli **Pracoviště** zvolte **1**.
5. V poli **Sklad** zvolte **11**.
6. Vyberte **OK**.
7. Na kartě **Záhlaví** na záložce s náhledem **Doručení** ověřte, že je pole **Podmínky doručení** nastaveno na **CIF** a pole **Způsob doručení** je nastaveno na **10**.
8. Na kartě **Řádky** na záložce s náhledem **Řádky nákupní objednávky** v poli **Číslo položky** vyberte **D0003**. Poté do pole **Množství** zadejte **6**.
9. Na záložce s náhledem **Podrobnosti řádku** na kartě **Zahraniční obchod** ověřte, že je pole **Kód transakce** nastaveno na **11**, pole **Přeprava** je nastaveno na **3**, pole **Komodita** je nastaveno na **100 200 30** a pole **Země/oblast původu** je nastaveno na **DEU**.
10. V podokně akcí na kartě **Nákup** ve skupině **Akce** zvolte **Potvrdit**.
11. V podokně akcí na kartě **Faktura** ve skupině **Generovat** zvolte **Faktura**.
12. V podokně Akce vyberte **Výchozí od** a pak v poli **Výchozí množství pro řádky** vyberte **Objednané množství**. Pak vyberte **OK**.
13. Na záložce s náhledem **Záhlaví faktury dodavatele** v sekci **Identifikace faktury** v poli **Číslo** zadejte **00010**.
14. V sekci **Data faktur** v poli **Datum faktury** vyberte aktuální datum. Toto datum bude použito pro převod Intrastat.
15. V poli **Datum obdržení dokumentu** vyberte **10/18/2021** (18. října 2021).
16. Chcete-li zaúčtovat fakturu, vyberte **Zaúčtovat** z akčního podokna.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Vytvořte prohlášení Intrastat pro příchozí položky

1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**.
2. V podokně akcí zvolte **Převod**.
3. V dialogovém okně **Intrastat (přenos)** nastavte možnost **Faktura dodavatele** na **Ano**.
4. Vyberte **OK** pro přenesení transakcí a pak zkontrolujte deník Intrastat.

    ![Řádek, který představuje nákupní objednávku na stránce Intrastat](media/intrastat_pl_4.png)

5. Zkontrolujte informace na kartě **Všeobecné** pro nákupní objednávku.

    ![Podrobnosti o nákupní objednávce na kartě Obecné na stránce Intrastat](media/intrastat_pl_5.png)

6. V podokně akcí vyberte **Výstup** > **Sestava**.
7. V dialogovém okně **Sestava Intrastat** na záložce s náhledem **Parametry** v sekci **Datum** v poli **Od data** vyberte první den aktuálního měsíce.
8. V sekci **Možnosti** **exportu** nastavte možnost **Generovat soubor** na **Ano**. Potom do pole **Název souboru** zadejte požadovaný název.
9. Nastavte možnost **Generovat sestavu** na **Ano**. Potom do pole **Název souboru sestavy** zadejte požadovaný název.
10. V poli **Směr** vyberte hodnotu **Příchozí**.
11. V sekci **Mapování formátu souboru** ověřte, že je poel **Typ prohlášení** nastaveno na **Prohlášení**.
12. V poli **Město tvorby dokumentů** zadejte **Krakov**.
13. V poli **Datum vytvoření dokumentu** vyberte **10/19/2021** (19. října 2021).
14. Do pole **Číslo dokumentu** zadejte **11**.
15. Do pole **Verze dokumentu** zadejte **22**.
16. Vyberte **OK** a zkontrolujte vygenerovanou sestavu ve formátu XML. Následující tabulka zobrazuje hodnoty v ukázkové sestavě.

    <table>
    <tbody>
    <tr>
    <td>
    <p><strong>Název pole</strong></p>
    </td>
    <td>
    <p><strong>Popis pole</strong></p>
    </td>
    <td>
    <p><strong>Hodnota</strong></p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Informace o dokumentu.</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Deklaracja Data</p>
    </td>
    <td>
    <p>Datum vytvoření dokumentu.</p>
    </td>
    <td>
    <p>2021-10-19</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Miejscowosc</p>
    </td>
    <td>
    <p>Město vytvoření dokumentu.</p>
    </td>
    <td>
    <p>Krakov</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaLiczbaPozycji</p>
    </td>
    <td>
    <p>Celkový počet položek.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscStatystyczna</p>
    </td>
    <td>
    <p>Celková statistická hodnota.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>LacznaWartoscFaktur</p>
    </td>
    <td>
    <p>Celková fakturovaná hodnota.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UC</p>
    </td>
    <td>
    <p>Kód jednotky.</p>
    </td>
    <td>
    <p>420000</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Rodzaj</p>
    </td>
    <td>
    <p>Typ prohlášení.</p>
    </td>
    <td>
    <p>D</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Wersja</p>
    </td>
    <td>
    <p>Verze dokumentu.</p>
    </td>
    <td>
    <p>22</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Numer</p>
    </td>
    <td>
    <p>Číslo dokumentu.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miesiac</p>
    </td>
    <td width="332">
    <p>Měsíc odkazu.</p>
    </td>
    <td>
    <p>10</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Rok</p>
    </td>
    <td width="332">
    <p>Rok odkazu.</p>
    </td>
    <td>
    <p>2021</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Typ</p>
    </td>
    <td width="332">
    <p>Směr sestavy.</p>
    </td>
    <td>
    <p>P</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>NrWlasny</p>
    </td>
    <td width="332">
    <p>Identifikátor prohlášení.</p>
    </td>
    <td>
    <p>21ISTDEMF-0002</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Informace o společnosti.</strong></p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Miejscowosc</p>
    </td>
    <td width="332">
    <p>Město, ve kterém se společnost nachází.</p>
    </td>
    <td>
    <p>Varšava</p>
    </td>
    </tr>
    <tr>
    <td width="191">
    <p>Regon</p>
    </td>
    <td width="332">
    <p>Kód Regon společnosti.</p>
    </td>
    <td>
    <p>12345678901234</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nip</p>
    </td>
    <td>
    <p>Kód NIP společnosti.</p>
    </td>
    <td>
    <p>1234567890</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodPocztowy</p>
    </td>
    <td>
    <p>Kód PSČ společnosti.</p>
    </td>
    <td>
    <p>31-111</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>UlicaNumer</p>
    </td>
    <td>
    <p>Ulice, ve které se společnost nachází.</p>
    </td>
    <td>
    <p>Statystyczna 22/1</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Nazwa</p>
    </td>
    <td>
    <p>Název společnosti.</p>
    </td>
    <td>
    <p>Contoso Entertainment System Germany</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Informace o zboží</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscStatystyczna</p>
    </td>
    <td>
    <p>Statistická hodnota.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WartoscFaktury</p>
    </td>
    <td>
    <p>Hodnota faktury.</p>
    </td>
    <td>
    <p>965</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>MasaNetto</p>
    </td>
    <td>
    <p>Čistá hmotnost.</p>
    </td>
    <td>
    <p>30</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzenia</p>
    </td>
    <td>
    <p>Kód země nebo oblasti původu.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransportu</p>
    </td>
    <td>
    <p>Kód způsobu dopravy.</p>
    </td>
    <td>
    <p>3</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KodTowarowy</p>
    </td>
    <td>
    <p>Kód komodity.</p>
    </td>
    <td>
    <p>10020030</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>RodzajTransakcji</p>
    </td>
    <td>
    <p>Kód transakce.</p>
    </td>
    <td>
    <p>11</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>WarunkiDostawy</p>
    </td>
    <td>
    <p>Režim podmínek dodání.</p>
    </td>
    <td>
    <p>CIF</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>KrajPochodzeniaWysylki</p>
    </td>
    <td>
    <p>Kód země nebo oblasti odeslání/místa určení.</p>
    </td>
    <td>
    <p>DE</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>OpisTowaru</p>
    </td>
    <td>
    <p>Popis komodit.</p>
    </td>
    <td>
    <p>Hardware</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>PozId</p>
    </td>
    <td>
    <p>Číslo položky.</p>
    </td>
    <td>
    <p>1</p>
    </td>
    </tr>
    <tr>
    <td colspan="3">
    <p align=center><strong>Kontaktní informace</strong></p>
    </td>
    </tr>
    <tr>
    <td>
    <p>E-mail</p>
    </td>
    <td>
    <p>E-mailová adresa podávající osoby.</p>
    </td>
    <td>
    <p>manishc@contoso.com</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Faks</p>
    </td>
    <td>
    <p>Číslo faxu podávající osoby.</p>
    </td>
    <td>
    <p>425-555-5049</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Telefon</p>
    </td>
    <td>
    <p>Číslo telefonu podávající osoby.</p>
    </td>
    <td>
    <p>425-555-5068</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>NazwiskoImie</p>
    </td>
    <td>
    <p>Jméno podávající osoby.</p>
    </td>
    <td>
    <p>Manish Chopra</p>
    </td>
    </tr>
    </tbody>
    </table>

17. Zkontrolujte vygenerovaný soubor ve fromátu Excel.

    ![Sestava příchozích položek Intrastat.](media/intrastat_pl_6.png)
