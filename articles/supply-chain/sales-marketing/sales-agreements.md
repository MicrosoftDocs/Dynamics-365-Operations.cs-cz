---
title: Přehled prodejních smluv
description: V tomto článku jsou informace o prodejních smlouvách. Prodejní smlouva je smlouva, která zaváže odběratele k nákupu produktů v určitém množství nebo stanovené částce za určitý čas výměnou za zvláštní ceny nebo slevy.
author: Henrikan
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesAgreementListPage, SalesAgreementInvoiceJournal, SalesAgreementInvoicePart
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "9554"
- intro-internal
ms.assetid: c5d55c8d-99f2-44f9-a897-5b0dee85fc81
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e84b8be597870deea3beaf1bdc4a98021b7f135
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903833"
---
# <a name="sales-agreements-overview"></a>Přehled prodejních smluv

[!include [banner](../includes/banner.md)]

V tomto článku jsou informace o prodejních smlouvách. Prodejní smlouva je smlouva, která zaváže odběratele k nákupu produktů v určitém množství nebo stanovené částce za určitý čas výměnou za zvláštní ceny nebo slevy.

Prodejní smlouva je smlouva, která umožní odběrateli zakoupit produkty v určitém množství nebo za specifickou částku za určitý čas, výměnou za zvláštní ceny, speciální slevy a další speciální podmínky, například platby a dodací podmínky. Ceny a slevy prodejní smlouvy přepíší všechny ceny a slevy, uvedené ve všech obchodních smlouvách, které existují.  

Období platnosti řádku prodejní smlouvy je definováno v poli **Datum platnosti** a **Datum vypršení platnosti** ve smlouvě. Prodejní objednávky odběratele opravňují používat dohody podmínky, pokud požadované datum expedice objednávky je v rámci doby platnosti. Všechny řádky prodejní objednávky, které jsou spojeny s prodejní smlouvou, přispívají k plnění prodejní smlouvy.  

Můžete vytvořit prodejní objednávku přímo z prodejní smlouvy pomocí akce **Uvolnit zakázku**. Případně můžete vybrat platnou prodejní smlouvu při podávání objednávek (viz "Použití prodejní smlouvy v procesu objednávky“ v tomto článku).  

> [!NOTE] 
> V předchozích verzích byly prodejní smlouvy označovány jako paušální prodejní objednávky.

## <a name="commitment-types"></a>Typy závazků
Každý řádek prodejní smlouvy vyjadřuje závazek prodat. Obecně existují dvě kategorie závazku:

-   **Závazek ohledně hodnoty**– odběratel souhlasí se zakoupením produktů za určitou částku.
-   **Závazek ohledně množství**– odběratel souhlasí se zakoupením určitého množství produktu.

Smlouva kromě toho můžete umožnit odběrateli zakoupit určitý produkt nebo produkty v kategorii produktu. Kombinováním těchto dvou faktorů (hodnota a množství a specifických produktů a kategorií produktu) získáme čtyři typy závazků:

-   **Závazek ohledně množství produktu** – odběratel souhlasí se zakoupením určitého množství produktu. Řádky, které používají tento typ závazku, jsou definovány podle čísla položky a množství a jednotky, která byla schválena. Pole **Částka** není k dispozici.
-   **Závazek ohledně hodnoty produktu** – odběratel souhlasí se zakoupením konkrétních produktů za určitou částku. Řádky, které používají tento typ závazku, jsou definovány podle čísla položky a množství, která byla schválena. Pole **Množství** a **Jednotka** nejsou k dispozici.
-   **Závazek ohledně hodnoty kategorie produktu** – odběratel souhlasí se zakoupením produktů z určité prodejní kategorie za určitou částku. Řádky používající tento typ závazku jsou definovány kategorií prodeje v hierarchii kategorií prodeje a částky. Pole **Množství** a **Jednotka** nejsou k dispozici.
-   **Závazek ohledně hodnoty** – odběratel souhlasí se zakoupením jakýchkoli produktů nebo produktu z libovolné kategorie zásobování za určitou částku. Pole **Množství** a **Jednotka** nejsou k dispozici.

Řádky ve stejné prodejní smlouvě mají různé typy závazků.

## <a name="pricing-terms-for-sales-agreements"></a>Cenové podmínky pro prodejní smlouvy
Cenové podmínky se mohou lišit v závislosti na typu závazku. U prodejní objednávky, která je spojena s prodejní smlouvou, přepisují podmínky cen z této prodejní smlouvy jakékoli jiné cenové podmínky použité na základě obchodních smluv. V následující tabulce jsou popsána pole související s cenami, kterých se jednotlivé typy závazku dotýkají. „Ano“ značí, že pole mohou být aktualizována na řádku objednávky.

| Typ závazku                   | Jednotková cena | Cenová jednotka | Procento slevy | Částka platební slevy |
|-----------------------------------|------------|------------|------------------|----------------------|
| Závazek – množství produktu       | Ano        | Ano        | Ano              | Ano                  |
| Závazek – hodnota produktu          |            |            | Ano              |                      |
| Závazek – hodnota kategorie produktu |            |            | Ano              |                      |
| Závazek ohledně hodnoty                  |            |            | Ano              |                      |

## <a name="policies-for-sales-agreements"></a>Zásady pro prodejní smlouvy
Následující zásady mají vliv na způsob propojení mezi závazkem prodejní smlouvy a příslušnými řádky prodejní objednávky:

-   **Max je vynuceno** – Celkové množství nebo částka za všechny řádky objednávky nemůže překročit množství nebo částku, která je specifikována v souvisejícím závazku.
-   **Cena a sleva je pevná** – Cena na řádku objednávky a cena v souvisejícím závazku se nesmí lišit. Pokud dojde ke změně ceny na řádku objednávky, dojde k přerušení propojení závazku. Pokud je propojení přerušeno, řádek objednávky nebude přispívat k plnění závazku.
-   **Minimální uvolněná částka** a **Maximální uvolněná částka** – Je-li částka zadána, zobrazí se zpráva, pokud provedete jakékoli změny na řádku objednávky, které způsobí, že řádek objednávky se bude lišit od souvisejícího závazku.

## <a name="fulfillment-calculations-for-sales-agreements"></a>Výpočty plnění prodejní smlouvy
Karta **Plnění** na pevné záložce **Podrobnosti řádku** na stránce **Prodejní smlouvy** popisuje množství a částky plnění.  

V oblasti **Plnění** lze zobrazit celkové množství a částky pro všechny řádky objednávky propojené s určitými prodejními smlouvami. Můžete také zobrazit zbývající částku nebo množství, které je nutné ke splnění závazku.  

V oblasti **Smlouva** lze zobrazit množství a částky z vybrané prodejní smlouvy. Tato množství a částky jsou celková množství a částky, ke kterým jste se zavázali.

## <a name="confirmations-and-version-history-for-sales-agreements"></a>Potvrzení a historie verzí prodejních smluv
Při potvrzení prodejní smlouvy bude aktuální verze prodejní smlouvy uložena v tabulce historie. Změníte-li prodejní smlouvu, můžete ji znovu potvrdit a uložit jinou verzi prodejní smlouvy do historie.  

Pokud není prodejní smlouva potvrzena, je možné ji stále používat k vytvoření prodejních objednávek. Informace o historii prodejní smlouvy však nebudou uloženy.  

Můžete zobrazit náhled všech revizí potvrzení nebo je vytisknout. Poté můžete sdílet revize s odběratelem a získat schválení.

## <a name="applying-sales-agreements-during-the-ordering-process"></a>Použití prodejních smluv v procesu objednávky
Pokud nevydáváte prodejní objednávky přímo pro prodejní smlouvu, stále během procesu zadávání objednávek můžete propojovat prodejní smlouvy k objednávce. Při vytváření nové prodejní objednávky a výběru prodejní smlouvy jsou dohody, jako jsou například platební podmínky, dodací podmínky a adresa dodání, použity v záhlaví objednávky, a vytvoří se propojení mezi dohodou a objednávkou. Poté, když na řádcích objednávky můžete vybrat produkty a kategorie, které jsou zadané v prodejní smlouvě, se ceny a slevy zkopírují z dané smlouvy. Stejná prodejní objednávka může zahrnovat řádky, které nesouvisí s prodejní smlouvou, i řádky, které mají závazek plnění prodejní smlouvy.

## <a name="modifying-sales-orders-that-are-linked-to-sales-agreements"></a>Úprava prodejních objednávek, které jsou propojeny s prodejní smlouvou
Pokud jste vytvořili (vydali) prodejní objednávku proti prodejní smlouvě, některá pole na řádcích prodejní objednávky bude možné změnit pouze v případě, že odeberete odkaz na přiřazené řádky prodejní smlouvy. V následující tabulce jsou uvedeny některá z těchto polí.

| Pole                                                             | Popis                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Požadované datum expedice                                               | Pokud změníte požadované datum expedice na datum starší než je hodnota **Datum začátku platnosti** na řádku prodejní smlouvy, je třeba nejprve odebrat odkaz na řádek prodejní smlouvy, než bude možné uložit změny data expedice. Pokud změníte požadované datum expedice na datum novější než je hodnota **Datum vypršení platnosti** na řádku prodejní smlouvy, je třeba nejprve odebrat odkaz na řádek prodejní smlouvy, než bude možné uložit změny data expedice. |
| Hodnota CurrencyDiscount, percentDiscountUnit, pricePrice, unitNet | Jestliže změníte hodnotu v některém z těchto polí a označíte pole **Cena a sleva je pevná** u řádku související prodejní smlouvy, zobrazí se zpráva s dotazem, zda chcete uložit změny. Klepněte na tlačítko **Ano** pro odebrání odkazu na řádek prodejní smlouvy a přepočítání ceny. Klepněte na tlačítko **Ne** pro odebrání odkazu na řádek prodejní smlouvy bez přepočítání ceny.                                                                   |
| Čistá částka                                                        | Pokud zadáte částku přesahující částku, která je specifikována na řádku prodejní smlouvy, kde je označeno pole **Max je vynuceno**, zobrazí se zpráva s dotazem, zda chcete uložit upravené množství. Klepněte na tlačítko **Ano** pro odebrání odkazu na řádek prodejní smlouvy a přepočítání ceny. Klepněte na tlačítko **Ne** pro odebrání odkazu na řádek prodejní smlouvy bez přepočítání ceny.                                                                 |
| Množství                                                          | Pokud zadáte množství přesahující množství, které je specifikováno na řádku prodejní smlouvy, kde je označeno pole **Max je vynuceno**, zobrazí se zpráva s dotazem, zda chcete uložit upravené množství. Klepněte na tlačítko **Ano** pro odebrání odkazu na řádek prodejní smlouvy a přepočítání ceny. Klepněte na tlačítko **Ne** pro odebrání odkazu na řádek prodejní smlouvy bez přepočítání ceny.                                                            |

## <a name="returning-an-item-that-was-ordered-from-a-sales-agreement"></a>Vrácení zboží objednaného z prodejní smlouvy
Když odběratel vrací produkt, který byl objednán z prodejní smlouvy, aplikace Supply Chain Management může vyhledat a automaticky aktualizovat závazek prodejní smlouvy tak, aby odrážel změny v množství nebo částce. Vytvořením vratky na základě původní prodejní objednávky, která je propojena s prodejní smlouvou, vytvoříte vztah mezi závazkem prodejní smlouvy, řádkem prodejní objednávky a fakturou vratky.  

Pokud nechcete odečíst množství vrácených položek ze závazku prodejní smlouvy, můžete použít ovládací prvek **Odebrat odkaz** na stránce **Vratka** k odebrání propojení mezi vratkou a závazkem prodejní smlouvy. Pokud budete muset obnovit propojení později, klepněte na tlačítko **Vytvořit odkaz**.  

**Poznámka:** Vratku lze propojit pouze s jednou prodejní smlouvou. Pokud odběratel vrací více než jeden produkt, který byl objednán z více než jedné prodejní smlouvy, musíte vytvořit novou vratku pro každý produkt a vytvořit odkaz na odpovídající prodejní smlouvy.

## <a name="automatic-search-for-sales-agreements"></a>Automatické hledání prodejní smlouvy
V některých situacích, kdy vytváření prodejních objednávek proběhlo nepřímo, například když vytvoříte dobropis nebo mezipodnikové prodejní objednávky, můžete určit, zda systém automaticky vyhledá použitelné prodejní smlouvy.

## <a name="financial-dimensions-on-sales-agreements"></a>Finanční dimenze pro prodejní smlouvy
Můžete kopírovat finanční dimenze, záhlaví dokladů nebo jednotlivé řádky prodejní smlouvy. Dimenze pro záhlaví smlouvy nebo řádku smlouvy lze změnit kdykoliv. V takovém případě dimenze jsou automaticky zkopírovány do záhlaví vydání nebo řádku vydání u vydané objednávky.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]