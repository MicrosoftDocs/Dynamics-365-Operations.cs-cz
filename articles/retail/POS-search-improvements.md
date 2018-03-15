---
title: "Vyhledávání produktu a vyhledávání zákazníka v POS"
description: "Toto téma poskytuje přehled vylepšení, která byla provedena v aplikaci Dynamics 365 for Retail ohledně funkce vyhledávání produktu a vyhledávání zákazníka."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 08/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 2af45de0d63b01e71b5009e2f62cfdff6844da7d
ms.contentlocale: cs-cz
ms.lasthandoff: 02/07/2018

---

# <a name="overview-of-product-and-customer-search-in-point-of-sale"></a>Přehled vyhledávání produktu a zákazníka v pokladním místě

[!include[banner](includes/banner.md)]

Moderní pokladní místo (MPOS) a cloudové pokladní místo (CPOS) poskytují snadno použitelnou funkci vyhledávání, která umožní zaměstnancům rychlé vyhledávání produktů a zákazníků. Panel vyhledávání je vždy k dispozici v horní části MPOS a CPOS, aby zaměstnanci mohli rychle vyhledat produkty a zákazníky.

Zaměstnanci mohou hledat produkty v sortimentech a katalozích, které jsou přiřazeny k aktuálnímu obchodu, a v sortimentech a katalozích, které jsou spojeny s jiným obchodem ve společnosti. Proto pokladníci mohou prodávat a vracet produkty mimo sortiment obchodu. Stejně tak mohou zaměstnanci vyhledávat zákazníky, kteří jsou ve společnosti spojeni s běžným obchodem nebo jiným obchodem. Kromě toho mohou zaměstnanci vyhledávat zákazníky, kteří jsou spojeni s jinou společností v nadřazené organizaci.

## <a name="product-search"></a>Hledání produktu 

Ve výchozím nastavení se vyhledávání produktů provádí v sortimentu obchodu. Tento typ vyhledávání se nazývá *vyhledávání místních produktů*. Zaměstnanci však mohou snadno přepnout do libovolného katalogu, který je přidružen k aktuálnímu obchodu, nebo mohou vyhledávat v jiném obchodě. Tento typ vyhledávání se nazývá *vyhledávání vzdálených produktů*. Chcete-li změnit katalog, zvolte tlačítko **Kategorie** v levé části stránky. V horní části zobrazeného podokna vyberte tlačítko **Změnit katalog** a vyberte jeden z dostupných katalogů pro jeho prohlížení. Systém bude prohledávat vybraný katalog produktů.

Na stránce **Změnit katalog** mohou zaměstnanci snadno vybrat libovolný obchod, nebo mohou vyhledávat produkty ve všech obchodech.

![Změna katalogu](./media/Changecatalog.png "Změna katalogu")
 
Vyhledávání místních produktů vyhledává v rámci následujících vlastností produktu:

- Číslo produktu
- Název produktu
- popis
- Dimenze
- Čárový kód
- Vyhledávací název

### <a name="enhancements-to-local-product-searches"></a>Vylepšení vyhledávání místních produktů

Zkušenosti při hledání místních produktů byly provedeny tak, aby byly více uživatelsky přívětivější. Byla provedena následující vylepšení:

- Rozbalovací nabídky produktu a zákazníka byly přidány do vyhledávacího panelu, takže zaměstnanci mohou před vyhledáváním vybrat buď **Produkt** nebo **Zákazník**. Ve výchozím nastavení je vybrán **Produkt**, jak je uvedeno na následujícím obrázku.
- U vyhledávání s více klíčovými slovy (to znamená u vyhledávání, které používají hledané termíny) mohou prodejci nakonfigurovat, zda výsledky vyhledávání mají obsahovat výsledky, které odpovídají libovolnému hledanému termínu, nebo pouze výsledky, které odpovídají všem hledaným termínům. Toto nastavení je k dispozici v profilu funkce POS pod novou skupinu s názvem **Vyhledávání produktu**. Ve výchozím nastavení je **Spárovat jakékoli hledané termíny**. Toto nastavení je rovněž doporučené nastavení. Při použití nastavení **Spárovat jakékoli hledané termíny** se vrátí jako výsledky všechny produkty, které zcela nebo částečně odpovídají jednomu nebo více hledaným termínům, a výsledky jsou roztříděny automaticky podle produktů, které mají největší shodu s klíčovým slovem (úplnou nebo částečnou).

    Nastavení **Spárovat všechny hledané termíny** vrátí pouze produkty odpovídající všem hledaným termínům (úplné nebo částečné). Toto nastavení je užitečné, když jsou názvy produktu dlouhé a zaměstnanci potřebují zobrazit pouze omezené produkty ve výsledcích vyhledávání. Tento typ vyhledávání však má dvě omezení:

    - Hledání se provádí na základě jednotlivých vlastností produktu. Jsou například vráceny pouze produkty, které mají všechna vyhledaná klíčová slova v alespoň jedné vlastnosti produktu.
    - Neprohledávají se dimenze.

- Maloobchodníci mohou nyní nakonfigurovat vyhledávání produktů pro zobrazení návrhů vyhledávání, když uživatelé zadávají názvy produktů. Nové nastavení této funkce je k dispozici v profilu funkce POS pod skupinu s názvem **Vyhledávání produktu**. Toto nastavení se nazývá **Zobrazit návrhy vyhledávání při zadávání**. Tato funkce pomůže zaměstnancům rychle najít produkt, který hledají, protože nemusí ručně zadávat celé jméno.
- Algoritmus vyhledávání produktu nyní hledá vyhledávané termíny ve vlastnosti produktu **Vyhledávání jména**.

![Návrhy produktu](./media/Productsuggestions.png "Návrhy produktu")

## <a name="customer-search"></a>Hledat zákazníka

Vyhledávání zákazníka slouží k vyhledání zákazníků pro různé účely. Pokladníci například mohou chtít zobrazit seznam přání zákazníka nebo historii nákupů, nebo přidat zákazníka do transakce. V případě vyhledání více klíčových slov vrací algoritmus vyhledávání zákazníků všechny zákazníky, kteří odpovídají některému z hledaných klíčových slov. V horní části výsledků se však objevují zákazníci, kteří odpovídají většině klíčových slov. Toto chování je podobné způsobu, kterým zobrazují výsledky jiné vyhledávače. Zobrazují nejprve výsledky, které odpovídají nejvíce vyhledávaným termínům, a poté zobrazují výsledky, které částečně odpovídají vyhledávaným klíčovým slovům. Toto chování pomáhá pokladníkům v situacích, kdy pro své vyhledávání použijí více klíčových slov, ale jedno z klíčových slov má pravopisnou chybu.

Ve výchozím nastavení se vyhledávání zákazníků provádí na adresářích zákazníků, které jsou přiřazeny k obchodu. Tento typ vyhledávání se nazývá *vyhledávání místních zákazníků*. Zaměstnanci však mohou také vyhledávat zákazníky globálně. Jinými slovy, mohou vyhledávat ve všech obchodech společnosti a ve všech ostatních právnických osobách. Tento typ vyhledávání se nazývá *vyhledávání vzdálených zákazníků*.

Pokud chtějí vyhledávat globálně, mohou zaměstnanci vybrat tlačítko **Filtrovat výsledky** v dolní části stránky a potom vybrat možnost **Prohledat všechny obchody**, jak je znázorněno na následujícím obrázku. V takovém případě nejsou vráceni jen zákazníci. Všechny typy stran, které jsou součástí jakéhokoli adresáře v ústředí jsou vráceny též. Tyto strany zahrnují pracovníky, dodavatele, kontakty a konkurenty.

> [!NOTE]
> Aby bylo možné získat výsledky vyhledávání pro vzdáleného zákazníka, je třeba zadat minimálně čtyři znaky.

V případě vyhledávání vzdáleného zákazníka se ID zákazníka nezobrazuje pro zákazníky z jiných právnických osob, protože pro tyto strany v současné společnosti nebylo vytvořeno žádné ID zákazníka. Pokud však zaměstnanec otevře stránku s podrobnostmi o zákazníkovi, systém automaticky vygeneruje ID zákazníka pro danou stranu a zároveň propojí adresáře zákazníka obchodu se zákazníkem. Proto bude zákazník viditelný v prohledáváních místního obchodu, která budou provedena později.

![Vyhledávání globálních zákazníků](./media/Globalcustomersearch.png "Vyhledávání globálních zákazníků")

### <a name="enhancements-to-local-customer-searches"></a>Vylepšení vyhledávání místních zákazníků

Vyhledávání místních zákazníků pomáhá zaměstnancům rychle nalézt zákazníka podle telefonního čísla. Zaměstnanci nemusí zadávat žádné speciální znaky, které byly přidány do telefonní číslo zákazníka, například mezery, závorky nebo pomlčky. Ačkoli pokladníci mohou ukládat telefonní čísla v libovolném formátu (například mohou obsahovat závorky, pomlčky, symboly atd.), mohou hledat zákazníky zadáním částečného telefonního čísla. Pokud pokladník zahrnul speciální znaky, když zadal telefonní číslo, jiní pokladníci najdou zákazníka zadáním čísel, které se objeví za speciálními znaky. Pokud telefonní číslo zákazníka byl zadáno například jako **123-456-7890**, pokladník můžete hledat zákazníka zadáním **123**, **456**, **7890**, nebo **1234567890**, nebo částečně zadáním několika počátečních čísel telefonního čísla.

