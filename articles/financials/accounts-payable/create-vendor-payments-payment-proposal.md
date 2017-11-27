---
title: "Vytvoření plateb dodavatele pomocí návrhu platby"
description: "Toto téma obsahuje přehled možností návrhu platby a nabízí příklady zobrazující, jak návrh plateb funguje. Návrhy plateb jsou často používány k vytvoření platby dodavatele, protože dotaz umožňuje rychle vybrat faktury dodavatele pro platbu na základě kritérií, jako jsou data splatnosti a platební slevy."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14312
ms.assetid: 585d5b0b-1b79-4a03-ab18-528918070377
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 454a370e73e6e0d33f0aeb1ca2b3f9d6d9f8cb98
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="create-vendor-payments-by-using-a-payment-proposal"></a>Vytvoření plateb dodavatele pomocí návrhu platby

[!include[banner](../includes/banner.md)]


Toto téma obsahuje přehled možností návrhu platby a nabízí příklady zobrazující, jak návrh plateb funguje. Návrhy plateb jsou často používány k vytvoření platby dodavatele, protože dotaz umožňuje rychle vybrat faktury dodavatele pro platbu na základě kritérií, jako jsou data splatnosti a platební slevy. 

Organizace často používá návrhy plateb k vytvoření platby dodavatele, protože dotaz na platební návrh umožňuje rychle vybrat faktury dodavatele pro platbu na základě data splatnosti, platební slevy a dalších kritérií. 

Dotaz na návrh platby obsahuje různé karty, z nichž každá má různé možnosti výběru faktur k platbě. Karta **Parametr** obsahuje možnosti, které používá většina organizací. Na pevné záložce **Záznamy, které chcete zahrnout** můžete určit, které faktury nebo dodavatele chcete zahrnout do platby definováním rozsahů různých vlastností. Například pokud chcete zaplatit pouze pro určitý rozsah dodavatelů, můžete definovat filtr pro rozsah dodavatelů. Tato funkce se často používá k výběru faktur pro konkrétní platební metodu. Například můžete definovat filtr, kde **Způsob platby** = **Kontrola** a pouze faktury, které mají tento způsob platby, budou vybrány pro platbu, za předpokladu, že splňují také jiná kritéria zadaná v dotazu. karta **Rozšířené parametry** obsahuje další možnosti, které nemusí být vztahující se k vaší organizaci. Na této kartě například naleznete možnosti pro úhradu faktur pro centralizované platby.

## <a name="parameters"></a>Parametry
-   **Výběr faktur podle** – faktury v rozsahu dat, který je určen v poli **Od data** a **Do data** lze vybrat podle data splatnosti, data platební slevy nebo obojího. Používáte-li datum platební slevy, systém nejprve vyhledá faktury, které mají datum platební slevy mezi počátečním datem a koncovým datem. Systém pak určuje, zda má faktura nárok na platební slevu použitím data relace pro ujištění se, že datum platební slevy již neuplynulo.
-   **Od data** a **Do data** – faktury, které mají datum splatnosti nebo datum platební slevy v tomto časovém intervalu, jsou vybrány pro platbu.
-   **Datum platby** – Používá se pouze v případě, kdy je pole **Období** u způsobu platby nastaveno na hodnotu **Celkem**. Pokud je definováno datum, jsou vytvořeny všechny platby k tomuto datu. Pole **Minimální datum platby** je ignorováno.
-   **Minimální datum platby** – zadejte minimální datum platby. Například pole **Od data** a **Do data** uvádí rozsah od 1. září do 10. září a minimální datum platby je 5. září. V takovém případě všechny faktury, které mají datum splatnosti od 1. září do 5. září, mají datum platby 5. září. Všechny faktury, které mají datum splatnosti od 5. září do 10. září však mají datum platby, které odpovídá datu splatnosti jednotlivých faktur.
-   **Limit částky** – zadejte maximální celkovou částku u všech plateb.
-   **Vytvořit platby bez náhledu faktury** – je-li tato možnost nastavena na **Ano**, platby budou vytvořeny okamžitě na stránce **Platby dodavatele**. Stránka **Návrh platby** bude přeskočena. Z toho vyplývá, že platby se vytvoří rychleji. Platby lze měnit i nadále ze stránky **Platby dodavatele**. Alternativně se můžete vrátit na stránku **Návrh platby** pomocí tlačítka **Upravit faktury k vybrané platbě**.

## <a name="advanced-options"></a>Rozšířené možnosti
-   **Kontrola zůstatku dodavatele** – je-li tato možnost je nastavena na **Ano**, systém potvrdí, že dodavatel nemá záporný zůstatek před zaplacením jakékoli faktury. Pokud dodavatel má záporný zůstatek, nebude vytvořena žádná platba. Dodavatel může mít například dobropisy nebo platby, které byly zaúčtovány, ale dosud nebyly vyrovnány. V takovém případě by neměla být platba dodavateli odeslána. Místo toho by měly být dobropisy nebo platby vyrovnány s ohledem na nevyřízené faktury.
-   **Odstranit záporné platby** – tuto možnost lze použít různě, v závislosti na tom, zda jsou platby vytvořeny pro jednotlivé faktury nebo součet faktur, které splňují kritéria platby. Toto chování je definováno pro metodu platby.
-   **Platba pro každou fakturu** – pokud možnost **Odstranit záporné platby** je nastavena na **Ano** a nevyrovnané faktury a platby existují u dodavatele, jsou k platbě vybrány pouze faktury. Stávající platba je poté vyrovnána podle faktury. Pokud možnost **Odstranit záporné platby** je nastavena na **Ne**, a faktura a platba není vyrovnána, faktura i platba jsou vybrány pro platbu. Vytvoří se platba pro platbu a vytvoří se vrácení (záporná platba) pro platbu.
-   **Platby pro součet faktur** – pokud je možnost **Odstranit záporné platby** nastavena na **Ano**, a nevyrovnané faktury a platby existují pro dodavatele, nevyrovnané faktury i platby jsou vybrány pro platbu, a částky budou přidány společně k vytvoření celkové placené částky. Jediná výjimka nastane, pokud částka vyústí v refundaci. V takovém případě nebude vybrána faktura ani platba. Pokud je možnost **Odstranit záporné platby** nastavena na **Ne**, a faktura ani platba není vyrovnána, faktury i platby jsou vybrány pro platbu, a částky budou přidány společně k vytvoření celkové placené částky.
-   **Pouze tisk sestavy** – nastavte tuto možnost **Ano**, pokud chcete vidět výsledky návrhu platby v sestavě, ale nechcete vytvářet žádné platby.
-   **Zahrnout faktury dodavatelů od ostatních právnických osob** - Pokud má vaše organizace centralizované zpracování plateb a návrh platby by měl mít zahrnuté faktury od ostatních právnických osob, které jsou zahrnuty do kritérií hledání, nastavte tuto možnost na **Ano**.
-   **Navrhnout samostatnou platbu dodavatele za každou právnickou osobu** – je-li tato možnost nastavena na **Ano**, pro každou právnickou osobu u každého dodavatele je vytvořena samostatná platba. Dodavatele u platby je dodavatelem z faktury od každé právnické osoby. Pokud je tato možnost nastavena na **Ne** a stejný dodavatel má faktury z více právnických osob, bude vytvořena jediná platba na celkovou částku vybraných faktur. Dodavatel pro platbu je dodavatel od aktuální právnické osoby. Pokud účet dodavatele u aktuální právnické osoby neexistuje, bude použit účet dodavatele pro první splatnou fakturu.
-   **Měna platby** – toto pole specifikuje měnu, ve které jsou vytvořeny všechny platby. Pokud není měna definována, každý faktura je zaplacena v měně faktury.
-   **Den v týdnu pro platbu** – zadejte den v týdnu, kdy bude provedena platba. Toto pole se používá pouze v případě, že je metoda nastavena na celkové faktury k platbě pro určitý den v týdnu.
-   **Typ protiúčtu** a **Protiúčet** – tato pole nastavte, pokud chcete definovat určitý typ účtu (například **Hlavní kniha** nebo **Banka**) a protiúčet (například konkrétní bankovní účet). Metoda platby pro fakturu definuje výchozí typ protiúčtu a protiúčet, ale můžete přepsat výchozí hodnoty těchto polí.
-   **Další filtry** – Na pevné záložce **Záznamy**, které chcete zahrnout můžete definovat další rozsahy kritérií. Například pokud chcete zaplatit pouze pro určitý rozsah dodavatelů, můžete definovat filtr pro rozsah dodavatelů. Tato funkce se často používá k výběru faktur pro konkrétní platební metodu. Například můžete definovat filtr, kde **Způsob platby** = **Kontrola** a pouze faktury, které mají tento způsob platby, budou vybrány pro platbu, za předpokladu, že splňují také jiná kritéria zadaná v dotazu.

## <a name="scenarios"></a>Scénáře
| Dodavatel | Faktura | Datum fakturace | Fakturovaná částka | Datum splatnosti | Datum platební slevy | Částka platební slevy |
|--------|---------|--------------|----------------|----------|--------------------|----------------------|
| 3050   | 1 001    | 15. června      | 500,00         | 15. červenec  | 29. června            | 10,00                |
| 3050   | 1 002    | 20. června      | 600,00         | 20. červenec  | 4. červenec             | 12,00                |
| 3075   | 1003    | 15. června      | 250,00         | 29. června  |                    | 0,00                 |
| 3100   | 1004    | 17. června      | 100,00         | 17. červenec  | 1. červenec             | 1,00                 |

1. července April zaplatí dodavatelům. Použije návrh platby k dokončení tohoto úkolu efektivněji.

### <a name="option-1-by-cash-discount"></a>Možnost 1: Dle platební slevy

April vybere **Platební sleva** jako typ návrhu. Zadá rozsah dat od 26. června do 10. července. Tyto faktury jsou zahrnuty v návrhu:

-   1002, protože datum slevy pro 4. července je v rozsahu dat pro platbu.
-   1004, protože datum slevy pro 1. července je v rozsahu dat pro platbu.

Následující faktury nejsou zahrnuty v návrhu:

-   1001, protože datum slevy pro 29. června již vypršelo a faktura proto již nemá nárok na platební slevu.
-   1003, protože tato faktura neobsahuje datum slevy.

### <a name="option-2-by-due-date"></a>Možnost 2: Podle dne splatnosti

April vybere **Dle data splatnosti** jako typ návrhu. Zadá rozsah dat od 26. června do 10. července. Tyto faktury jsou zahrnuty v návrhu:

-   1003, protože datum splatnosti pro 29. června je v rozsahu dat pro platbu.

Následující faktury nejsou zahrnuty v návrhu:

-   1001, protože datum splatnosti pro 15. července je mimo rozsah dat pro platbu.
-   1002, protože datum splatnosti pro 20. července je mimo rozsah dat pro platbu.
-   1004, protože datum splatnosti pro 17. července je mimo rozsah dat pro platbu.

### <a name="option-3-by-due-date-and-cash-discount"></a>Možnost 3: Podle data splatnosti a platební slevy

April vybere **Datum splatnosti a platební sleva** jako typ návrhu. Zadá rozsah dat od 26. června do 10. července. Tyto faktury jsou zahrnuty v návrhu:

-   1003, protože datum splatnosti pro 29. června je v rozsahu dat pro platbu.
-   1002, protože datum slevy pro 4. července je v rozsahu dat pro platbu.
-   1004, protože datum slevy pro 1. července je v rozsahu dat pro platbu.

Následující faktury nejsou zahrnuty v návrhu:

-   1001, protože datum slevy pro 29. června již vypršelo, takže tato faktura již nemá nárok na platební slevu, a datum splatnosti 15. července je také mimo rozsah dat.

## <a name="country-specific-considerations"></a>Informace k volbě Závislé na zemi/oblasti
### <a name="norway"></a>Norsko

#### <a name="dimension-control"></a>Kontrola dimenze

Kontrola dimenzí umožňuje kontrolovat seskupení generovaných řádků podle návrhu platby a nastavit výchozí dimenze na základě finančních dimenzí používaných pro aplikovanou fakturu. V kontextu Norska pro každý způsob platby je finanční dimenze karta, na které lze aktivovat kontrolu dimenzí a také povolit seskupení pro každou dimenzi. K dispozici jsou tyto možnosti:

-   Pole **Kontrola dimenzí** je zakázáno. Návrh platby se chová jako ve kterékoli jiné zemi.
-   Pole **Kontrola dimenzí** je aktivováno bez dalšího definování dimenzí Návrh platby bude vytvořen bez ohledu na dimenzi. Vytvořená transakce nedědí žádné dimenze z aplikované položky.
-   Pole **Kontrola dimenzí** je aktivováno a jsou povoleny další dimenze. Nyní můžete definovat, jak dimenze budou zkopírovány do deníku. Například: • vyberte zaškrtávací políčko **BusinessUnit**, chcete-li vytvořit návrh platby podle organizační jednotky pro metodu platby • vyberte zaškrtávací políčko **CostCenter**, chcete-li vytvořit návrh platby podle nákladového střediska pro metodu platby.

**Poznámka:** Pokud ve třetí možnosti vyberete více dimenzí, dojde k vytvoření návrhu platby pro danou kombinaci dimenzí.

#### <a name="bank-account-selection"></a>Výběr účtu

Můžete definovat standardní debetní účet plateb podle metody platby bez ohledu na kontext země. To bude nastaveno na řádcích platby generovaných návrhem. S funkcí bankovního účtu lze definovat více debetní bankovních účtů spravovaných dimenzí a měnou nebo jejich kombinací k použití různých debetní bankovních účtů, v závislosti na jednotlivých kombinacích. Tyto kombinace můžete nastavit na stránce **Metody platby** pomocí tlačítka **Bankovní účty** dostupného pro každou metodu platby pomocí položky **Typ účtu pro zaúčtování** = **Banka**.




