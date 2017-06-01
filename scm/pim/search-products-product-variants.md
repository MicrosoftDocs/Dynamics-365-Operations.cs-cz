---
title: "Vyhledávání produktů a variant produktu během zadání objednávky"
description: "Použijte pole <strong>Číslo položky </strong>k vyhledání produktů a variant produktů, až budete ručně vytvářet řádek prodejní objednávky nebo řádek nákupní objednávky.  Tímto způsobem můžete rychle vyhledat varianty produktu, pokud máte k dispozici pouze konfigurační řetězec nebo jednu z dimenzí produktu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: MCRFullTextIndexField, MCRFullTextParameters, PurchTable, SalesTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 248534
ms.assetid: 99dd5ce1-0029-4f06-90e7-865e6d46d86e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3960cc3eb9b8d488973d258db45aa0ab9f1dd988
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="search-for-products-and-product-variants-during-order-entry"></a>Vyhledávání produktů a variant produktu během zadání objednávky

[!include[banner](../includes/banner.md)]


Použijte pole <strong>Číslo položky </strong>k vyhledání produktů a variant produktů, až budete ručně vytvářet řádek prodejní objednávky nebo řádek nákupní objednávky.  Tímto způsobem můžete rychle vyhledat varianty produktu, pokud máte k dispozici pouze konfigurační řetězec nebo jednu z dimenzí produktu.

V některých případech mít příliš moc něčeho není tou nejlepší situací, zejména pokud prodáváte více produktů, které jsou si podobné a vy se snažíte zapamatovat si čísla položek nebo vyhledávací názvy produktů, abyste našli správný produkt do prodejní objednávky. Jako vyhledávací pole lze použít pole **číslo položky** na řádku prodejní objednávky nebo řádku nákupní objednávky. Můžete zadat libovolnou část názvu produktu, čísla nebo dimenze a získat vyhledání, které zobrazuje všechny položky, které odpovídají hledanému slovu.

## <a name="how-search-works"></a>Jak funguje hledání
Při hledání produktu nebo varianty produktu, je třeba pochopit, jak funkce hledá produkty, které odpovídají zadanému textu. Klíčová pravidla hledání přinášející výsledky hledání jsou:

-   Výsledky hledání nepřinesou odpovídající záznam bez ohledu na pole, v němž je zadán text pro hledání.
-   Hledaný text musí být přítomen v příslušném záznamu v úplné délce.
-   Ke spárování dojde i v případě, že je hledaný text uprostřed textového řetězce odpovídajícího záznamu. Nemusí se nutně zobrazovat na začátku řetězce.
-   Hledaný text je zpracován jako jednoduchý textový řetězec, a to i v případě, že obsahuje prázdné znaky.

### <a name="examples"></a>Příklad

Následující příklady využívají produkty a varianty produktů, aby ilustrovaly způsob, jak hledání probíhá v různých situacích. **Předpoklad:** V části **Prodej a marketing &gt; Nastavení &gt; Hledat &gt; Parametry vyhledávání** &gt; **Typ vyhledávání** vyberte možnost **Úplná shoda**.

| Typ produktu     | Název produktu    | Zobrazit číslo produktu | Č. položky | Konfigurace |
|------------------|-----------------|------------------------|-------------|---------------|
| Jedinečný produkt | SpeakerMidRange | D0001                  | D0001       | Není k dispozici            |
| Varianta produktu  | Aktivní reproduktor  | D0010:::Černá:         | D0010       | 000005        |
| Varianta produktu  | Aktivní reproduktor  | D0010:::Bílá:         | D0010       | Bílá         |

Pokud zadáte 'hovořit' do pole **Číslo položky**, obdržíte všechny výše uvedené produkty v jako výsledek vyhledávání. Pokud napíšete 'černá' do pole **Číslo položky**, zobrazí se druhý produkt, protože má text "černá" v zobrazení čísla produktu. Tyto dva příklady ilustrují, že se nevyhledává jen od začátku tohoto pole. Ke shodě dojde i v případě, že hledaný text se nachází uprostřed textového řetězce v odpovídajícím záznamu.  

Pokud zadáte "05" obdržíte pouze druhou variantu produktu, protože má v konfiguraci: '05'. To dokazuje, že hledání je probíhá napříč povolenými poli na stránce **Kritéria vyhledávání**.  

Pokud zadáte 'hovořit 05', nezískáte žádné výsledky. Důvodem je skutečnost, že vyhledávání hledá úplný text, který je zadán. Vyhledávání se nebude snažit vyhledání "hovořit" a pak zúžit výsledky na ty obsahující '05'.  

Počet výsledků vyhledávání můžete omezit pomocí pole **Počet výsledků** na stránce **Prodej a marketing &gt; Nastavení &gt; Vyhledávání &gt; Parametry hledání**. Pokud toto pole nastavíte na hodnotu 0, budou všechny výsledky vyhledávání odmítnuty. Pokud nastavíte například 10, získáte jako maximální počet výsledků hledání 10.

## <a name="configure-the-product-search"></a>Nakonfigurujte vyhledávání produktu
Před použitím funkce vyhledávání produktu a varianty produktu, postupujte podle následujících kroků při konfigurování vyhledávání produktu. [![3 kroky ke konfiguraci vyhledávání produktu\_AXAppFall](./media/3-steps-to-configure-product-search_axappfall.png)](./media/3-steps-to-configure-product-search_axappfall.png)

### <a name="step-1-include-all-the-relevant-product-and-product-variant-identifiers-and-dimensions-in-the-search-criteria"></a>Krok 1: Zahrňte všechny relevantní identifikátory produktu a variant produktu i dimenzí do kritérií vyhledávání

Příklady identifikátorů produktu a variant produktu i dimenzí, podle nichž můžete vyhledávat, jsou **Název produktu, číslo položky**, **Zobrazit číslo produktu, Konfigurace, Barva, Velikost, Styl, Název pro vyhledávání apod**.  

Přejděte na stránku **Prodej a marketing &gt; Nastavení &gt; Vyhledávání &gt; Kritéria vyhledávání**. Stránka **Kritéria vyhledávání** vám umožňuje definovat kritéria pro odběratele, potenciální zákazníky a vyhledávání produktu. Ověřte, že stránku filtrujete pomocí kritérií vyhledávání produktu. To můžete provést přepnutím do **Produkt** v nabídce na stránce.  

Pokud chcete do kritérií vyhledávání přidat číslo zobrazeného produktu, klikněte na **Nový** v nabídce stránky. To přidá nový záznam do mřížky **Kritéria hledání**. Otevřete sloupec vyhledávání **Název pole** a vyberte **DisplayProductNumber**. Chcete-li přidat konfiguraci produktu ke kritériím hledání, vytvořte nový záznam v tabulce **Kritéria vyhledávání** a vyberte **configId** ve sloupci **Název pole**. Stejným způsobem vytvořte záznam s **Název_pole** **InventColorId** pro dimenzi barvy, **InventSizeId** pro dimenzi velikosti a **InventStyleId** pro dimenzi stylu.

### <a name="step-2-populate-the-database-table-that-is-used-for-product-search"></a>Krok 2: Vyplňte tabulku databáze, která se používá pro hledání produktu

Na stránce **Kritéria vyhledávání** klepněte na tlačítko **Aktualizace data vyhledávání**. V dialogovém okně **Aktualizace data vyhledávání** se ujistěte, že **Zdroj** je nastaven na **Produkt** a klepněte na tlačítko **OK**. Systém bude v jedné tabulce agregovat všechna vybraná vyhledávací kritéria zadaná v kroku 1. Pokud máte velké množství produktů a variant produktů, operace mohou být dlouhodobé a mohou se zobrazit upozornění. Doporučujeme naplánovat vyplnění tabulky vyhledávání na dávkovém serveru v okamžiku, kdy server není příliš zaneprázdněn.  

Dokud nebude tabulka vyplněna, vyhledávání produktu neposkytne správné výsledky. Pokud se vám nezobrazí žádné výsledky vyhledávání, ujistěte se, že je tato tabulka vyplněná.  

Tabulka musí být také vyplněná po úpravě kritérií hledání. Nově představené produkty a varianty produktů se automaticky přidávají do tabulky. Zrušené produkty a varianty produktů se automaticky mažou z tabulky.

### <a name="step-3-enable-the-lookup-for-product-search-on-sales-and-purchase-order-lines"></a>krok 3: Povolte hledání pro vyhledávání produktu v prodejních a nákupních objednávkách

Tuto funkci můžete povolit v části **Prodej a marketing &gt; Nastavení &gt; Vyhledávání &gt; Parametry vyhledávání** a nastavením možnosti **Povolit hledání pro vyhledávání** na **Ano** na kartě **Obecné**.  

Pro položku řádku prodejní objednávky je standardní postup takový, že otevřete stránku **Vyhledávání produktu**, kam začnete vyplňovat **Číslo položky** a pak stisknete klávesu **Tab**. Stránka **Vyhledávání produktu** mění kontext během tvoření řádku objednávky a lze ji považovat za zbytečně rušivou. Pokud dáváte přednost výsledkům hledání v hledání a nechcete ztratit kontext při zadávání řádku objednávky, můžete použít místo toho vyhledávání v hledání. Hledáte-li produkt nebo variantu produktu, ale nevyberete nic v hledání a stiskněte klávesu **Tab**, objeví se stránka **Vyhledávání produktu**.




