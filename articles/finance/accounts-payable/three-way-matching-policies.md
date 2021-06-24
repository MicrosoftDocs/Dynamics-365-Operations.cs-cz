---
title: Zásady třícestného párování
description: Toto téma obsahuje příklady třícestného párování.
author: abruer
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: roschlom
ms.custom: 2761
ms.assetid: 70f3cb1a-18b7-4474-95ec-28b2410dd8f8
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87ab65469ec4a8154267b88fe45481b65ade5e7a
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189171"
---
# <a name="three-way-matching-policies"></a>Zásady třícestného párování

[!include [banner](../includes/banner.md)]

Toto téma obsahuje příklady třícestného párování.

## <a name="example-three-way-matching-for-items"></a>Příklad: Třícestné párování pro položky

**Souhrn:** Ken bude kontrolor v sídle společnosti právnické osoby Fabrikam. Ken se rozhodne, že všechny faktury dodavatele, které jsou založeny na nákupních objednávkách, budou párovány s řádky nákupní objednávky (dvoucestné párování). Pro nákupy položek, které budou použity jako dlouhodobý majetek, by faktury měly být spárovány s řádky nákupní objednávky i řádky příjemky produktu (třícestné párování).

Společnost Fabrikam pracuje s více právnickými osobami a zaměstnanci ve všech částech světa. Jak se zvyšuje objem transakcí, zvyšují se také nesrovnalosti příjemek a faktur. Výsledkem jsou odpisy majetku. Faktury od dodavatelů jsou placeny, ale proces nezahrnuje identifikaci nesrovnalostí při příjmu méně položek, než bylo původně objednáno, nebo pokud položky nebyly přijaty vůbec. Výdaje se také zvyšují vzhledem k tomu, že zaměstnanci stále potřebují nástroje a další materiál pro vykonávání své práce. Ken se chce ujistit, že dodavatelé dodávají produkty, které jsou objednány, a zaměstnanci Fabrikam přijímají zboží. Ken proto vyžaduje dvoucestné a třícestné párování pro všechny právnické osoby v rámci organizace. Párování faktur napomáhá k ujištění, potíže s položkami, které byly ztraceny nebo nebyly přijaty můžete sledovat a řešit. 

Zásady párování faktur v tomto příkladu pomáhají osobám v následujících rolích splnit tyto cíle:

-   Ken bude kontrolor pro společnost Fabrikam. Pomáhá osobám v organizaci při identifikaci a nápravě problémů s objednáváním, příjem a placením položek (zboží a služby) od dodavatelů.
-   Phyllis a April jsou účetní vedoucí v oddělení závazků pro USA divizi společnosti Fabrikam. Mohou vynutit zásady společnosti a ujistit se, že faktury jsou zaplaceny až poté, co jsou faktury porovnávány s nákupní objednávkou a příjmem zboží a služeb (kde je to vhodné).
-   Tony je vedoucí výroby pro USA divizi společnosti Fabrikam. Spolu s ostatními výrobními pracovníky může zajistit, aby byly položky přijímány tak, jak jsou objednávány od dodavatelů, a jsou tvořeny tak, aby pracovníci měli vše potřebné ke své práci.

### <a name="prerequisites"></a>Předpoklady

-   Ken nastaví zásady párování na úrovni právnické osoby pro třícestné párování.
-   Ken nastaví Automaticky aktualizovat stav párování záhlaví u právnické osoby na hodnotu Ano.
-   Ken nastaví pole Párování celkových cen u právnické osoby na Procento a zadá 15 % jako procentuální hodnotu tolerance.
-   Ken nastaví zásady párování na úrovni položky pro položku 1500 – zařízení CNC Milicron na třícestné párování. Tato položka je položkou majetku použitou pro výrobu ve společnosti Fabrikam. Faktury pro tuto položku jsou pak spárovány s řádky nákupní objednávky s ohledem na ceny a příjemky produktů na množství.
-   Tony zadá požadavek pro pět zařízení CNC Milicron. Alicia, úředník pro nákupní objednávky ve společnosti Fabrikam, vystaví nákupní objednávku právnické osobě s názvem Contoso s cílem zadat položky.

    | Č. položky                 | Množství | Jedn. cena | Čistá částka | Kód nákladů        | Hodnota nákladů |
    |-----------------------------|----------|------------|------------|---------------------|---------------|
    | 1500 – zařízení CNC Milicron | 5        | 8 000,00   | 40 000,00  | Expedice a zpracování | 3,000.00      |

-   Arnie, úředník pohledávek ve společnosti Contoso, prověří dodávky pro daný týden. Arnie vybere transakce dodávky pro fakturaci společnosti Fabrikam v rámci dodání zařízení CNC Milicron. Arnie zahrne náklady na expedici a zpracování. Společnost Fabrikam zváží přidání poplatků jako součást nákladů na majetek.

### <a name="scenario"></a>Scénář

1.  Sammy, pracovník v oddělení příjmu ve společnosti Fabrikam, obdrží celkové množství strojů dodaných od společnosti Contoso. Zadá na příjemce produktu počet 5. Protože nákupní objednávka byla plně přijata, stav nákupní objednávky se změní na Přijato.
2.  April, koordinátor závazků ve společnosti Fabrikam, zadá a ověří fakturu odeslanou společností Contoso. Ověří následující informace:
    -   U položek, které vyžadují třícestné párování, ověří zda množství na řádku faktury odpovídá množství, které bylo přijato. Přijaté množství je uvedeno na příjemce produktu, které je párováno s fakturou.
    -   Pro položky, které vyžadují dvoucestné nebo třícestné párování, jsou ceny na řádku faktury v rámci tolerance definované v aplikaci Microsoft Dynamics 365 Finance. Jedná se o následující typy párování ceny:
        -   Párování čisté jednotkové ceny – čistá jednotková cena na řádku faktury odpovídá čisté jednotkové ceně na řádku nákupní objednávky v rámci procenta odchylky. V tomto příkladu je tolerance pro čistou jednotkovou cenu +8 %.
        -   Párování celkových cen – čistá částka na řádku faktury odpovídá čisté částce na řádku nákupní objednávky v rámci procenta, částky nebo procenta a částky odchylky. V tomto příkladu je tolerance celkové párované ceny +15 %.

Papírová faktura ze společnosti Contoso obsahuje následující informace.

| Zboží                        | Množství | Jedn. cena | Čistá částka |
|-----------------------------|----------|------------|------------|
| 1500 – zařízení CNC Milicron | 5        | 8 100,00   | 40,500.00  |
| Expedice a zpracování       |          |            | 4,000.00   |
| Daň                         |          |            | 0,00       |
| Součet                       |          |            | 44,500.00  |

Řádek faktury obsahuje následující informace:

| Č. položky                 | Množství | Jednotková cena | Čistá částka řádku | Zásady párování    | Spárování množství v příjemce produktu | Shoda ceny | Párování celkových cen |
|-----------------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| 1500 – zařízení CNC Milicron | 5        | 8 100,00   | 40 500,00       | Třícestné párování | Úspěšné                         | Úspěšné      | Úspěšné            |

Vzhledem k tomu, že tento řádek splňuje požadavky procesu párování faktur, fakturu je možné zaúčtovat.

## <a name="example-three-way-matching-for-item-and-vendor-combinations"></a> Příklad: Třícestné párování pro kombinaci položky a dodavatele
Souhrn: Ken bude kontrolor v sídle společnosti právnické osoby Fabrikam. Ken se rozhodne, že všechny faktury, které jsou založeny na nákupních objednávkách, budou párovány s řádky nákupní objednávky (dvoucestné párování). Cassie je účetní v divizi pro Malajsii společnosti Fabrikam. Určuje, že vybrané položky, které jsou objednány od určitých dodavatelů v Malajsii. je třeba spárovat s řádky nákupní objednávky i řádky příjemky produktu (třícestné párování). Rovněž může přepsat zásady párování na vyšší úroveň párování pro specifické nákupní objednávky. 

Množství a částky jsou malé a mohlo dojít k potížím s dodávkou od některých dodavatelů v Malajsii. Z tohoto důvodu Cassie určí úroveň řízení pro určité kombinace položek a dodavatelů pocházející z Malajsie na třícestné párování. 

Zásady párování faktur v tomto příkladu pomáhají osobám v následujících rolích splnit tyto cíle:
-   Ken bude kontrolor pro společnost Fabrikam. Pomáhá osobám v organizaci při identifikaci a nápravě problémů s objednáváním, příjem a placením položek (zboží a služby) od dodavatelů.
-   Cassie je účetní v divizi pro Malajsii společnosti Fabrikam. Může vynutit zásady společnosti a ujistit se, že faktury jsou zaplaceny až poté, co jsou porovnávány s řádky nákupní objednávky a příjemkami produktu, které představují příjmem zboží a služeb. Může také zvýšit úroveň řízení na třícestné párování pro specifické položky a řídit tak provozní náklady.

### <a name="prerequisites"></a>Předpoklady

-   Ken nastaví zásady párování na úrovni právnické osoby pro dvoucestné párování.
-   Ken nastaví pole Párování celkových cen u právnické osoby na Procento a zadá 10 % jako procentuální hodnotu tolerance.
-   Ken nastaví toleranci ceny pro všechny položky na 2 %.
-   Cassie nastaví zásady párování na úrovni kombinace položek a dodavatelů "PH2500 – počítač" a "dodavatel Contoso" na třícestné párování.
-   Alicia, účetní nákupní objednávky v divizi pro Malajsii společnosti Fabrikam, vystaví nákupní objednávky pro společnost Contoso s cílem dodat tři položky způsobem znázorněným v následující tabulce. Když vytvoří nákupní objednávku, přepíše odpovídající zásady párování pro bezdrátovou myš na třícestné párování namísto dvoucestného párování.

    | Číslo zboží           | Množství | Jednotková cena | Čistá částka | Zásady párování (výchozí hodnota) | Zásady párování (na řádku nákupní objednávky) |
    |-----------------------|----------|------------|------------|---------------------------------|----------------------------------------------|
    | PH2500 – Počítač     | 2        | 2 500,00   | 5 000,00   | Třícestné párování              | Třícestné párování                           |
    | MM01 – bezdrátová myš | 2        | 40,00      | 80,00      | Dvoucestné párování                | Třícestné párování                           |
    | Jednotka USB             | 200      | 10,00      | 2 000,00   | Dvoucestné párování                | Dvoucestné párování                             |

### <a name="scenario"></a>Scénář

1.  Položky dorazí. Sammy, pracovník v oddělení příjmu v divizi pro Malajsii společnosti Fabrikam, bude přerušen a nezaúčtuje příjemku produktu okamžitě.
2.  April, koordinátor závazků ve společnosti Fabrikam, zadá a ověří fakturu odeslanou společností Contoso. Ověří následující informace:
    -   U položek, které vyžadují třícestné párování, ověří zda množství na řádku faktury odpovídá množství, které bylo přijato. Přijaté množství je uvedeno na příjemce produktu, které je párováno s fakturou.
    -   Pro položky, které vyžadují dvoucestné nebo třícestné párování, jsou ceny na řádku faktury v rámci tolerance definované v aplikaci. Jedná se o následující typy párování ceny:
        -   Párování čisté jednotkové ceny – čistá jednotková cena na řádku faktury odpovídá čisté jednotkové ceně na řádku nákupní objednávky v rámci procenta odchylky. V tomto příkladu je tolerance pro čistou jednotkovou cenu +2 %.
        -   Párování celkových cen – čistá částka na řádku faktury odpovídá čisté částce na řádku nákupní objednávky v rámci procenta, částky nebo procenta a částky odchylky. V tomto příkladu je tolerance celkové párované ceny +10 %.

Papírová faktura ze společnosti Contoso obsahuje následující informace.

| Zboží                  | Množství | Jedn. cena | Čistá částka |
|-----------------------|----------|------------|------------|
| PH2500 – Počítač     | 2        | 2 500,00   | 5 000,00   |
| MM01 – bezdrátová myš | 2        | 41.00      | 82.00      |
| Jednotka USB             | 200      | 10.05      | 2,010.00   |
| Celková faktura         |          |            | 7,092.00   |

Řádek faktury obsahuje následující informace:

| Č. položky           | Množství | Jednotková cena | Čistá částka řádku | Zásady párování    | Spárování množství v příjemce produktu | Shoda ceny | Párování celkových cen |
|-----------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| PH2500 – Počítač     | 2        | 2 500,00   | 5 000,00        | Třícestné párování | Nezdařilo se                         | Úspěšné      | Úspěšné            |
| MM01 – bezdrátová myš | 2        | 41,00      | 82,00           | Třícestné párování | Nezdařilo se                         | Nezdařilo se      | Úspěšné            |
| Jednotka USB             | 200      | 10,05      | 2010,00         | Dvoucestné párování   |                                | Úspěšné      | Úspěšné            |

Mějte na paměti následující body:
-   Pro řádek PH2500 – počítač má sloupec Spárování množství v příjemce produktu uvedenou varovnou ikonu, protože řádek faktury neodpovídá příjemce produktu.
-   Pro řádek MM01 – bezdrátová myš má sloupec Spárování množství v příjemce produktu uvedenou varovnou ikonu, protože řádek faktury neodpovídá příjemce produktu. Sloupec Párování jednotkové ceny má zobrazenou varovnou ikonu, protože dojde k překročení tolerance 2 % u čisté jednotkové ceny.
-   Pro řádek Jednotka USB je sloupec Množství v příjemce produktu nevyplněný, protože dvoucestné párování neodpovídá množství na řádku faktury a řádku příjemky produktu.

Pokud je schválení vyžadováno u faktur, které mají být zaúčtovány s odlišnostmi v párování faktur, je nutné vybrat možnost Schválit zaúčtování s odpovídajícími odlišnostmi na stránce Podrobnosti o párování faktur dříve, než bude možné zaúčtovat fakturu s chybou v párování ceny nebo párování množství. Pokud schválení není vyžadováno, zpracování faktury může pokračovat, pokud neexistují žádné chyby v zaúčtování.


Další informace naleznete v tématu [Přehled párování faktur závazků](accounts-payable-invoice-matching.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]