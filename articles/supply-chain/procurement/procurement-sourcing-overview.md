---
title: Přehled zásobování a zdrojů
description: Tento článek poskytuje přehled funkci, které jsou k dispozici v modulu Zásobování a zdroje.
author: mkirknel
manager: tfehr
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogListPage, CatVendorCatalogListPage, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 58021
ms.assetid: eea24e23-a803-4de0-a218-6485757cde1b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f46bbaca86f9113a3e4705e4f2c0f76590e62ec1
ms.sourcegitcommit: 86052c58e3c365c443bd6f37ad1054bea395e21b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/06/2020
ms.locfileid: "3338326"
---
# <a name="procurement-and-sourcing-overview"></a>Přehled zásobování a zdrojů

[!include [banner](../includes/banner.md)]

Tento článek poskytuje přehled funkci, které jsou k dispozici v modulu Zásobování a zdroje.

Zásobování a zdroje zahrnují všechny kroky od identifikace potřeby produktů a služeb, přes obstarání produktu, příjem, fakturaci a zpracování plateb s dodavateli. Procesy zásobování lze definováním zásad nákupu a workflow nakonfigurovat k dosažení specifických potřeb.

## <a name="identifying-a-need-for-product-and-services"></a>Identifikace potřeby produktů a služeb

Potřeba produktů nebo služeb může vzniknout ze *žádanek*, například když zaměstnanec vyžaduje produkt. *Katalogy produktů* mohou být nastaveny na průvodce výběrem dostupných produktů, ze kterých lze vybírat nebo požadavky lze vytvořit pro produkty, které nebyly dosud dostupné v katalogu, umožňující nákupnímu oddělení zvážit, jak může být produkt dodán.  

*Omezení útrat* lze použít k omezení útrat žádanek a *nákupnímu workflow* přidá možnost požadovat schválení před objednáváním. V případě potřeby je také možné zadat přidělení finančních prostředků rozpočtu.  

Oddělení zásobování identifikuje dodavatelé pro požadované produkty a služby, a tento výpočet může zahrnovat *požadavek na nabídku* odesílaný několika potenciálním dodavatelům. Je možné sdílet specifikace produktu, které jsou požadovány a potenciální dodavatelé mohou zobrazit, zda mohou dodat produkt, který je v souladu s jejich požadavky. Dodavatelé vracejí své nabídky, které jsou pak kontrolovány oddělením zásobování, předtím, než vyberou dodavatele, kteří je budou zásobovat.  

Nákupní objednávky zahrnují možnost odesílat *nákupní žádanku* dodavateli jako alternativu ke komplexnějšímu zpracování požadavku na nabídku. Nákupní žádanku lze použít při vytváření podmínek, jako jsou ceny, slevy a datum dodání objednávky. Pokud jsou dodavatelé nastaveni k používání **Portálu pro dodavatele**, funkce nákupní žádanky je zakázána. Namísto toho je objednávka sdílena v**dodavatelském portálu**, a když je *potvrzení požadavku* odesláno dodavateli, lze přímo objednávku potvrdit.  

*Katalogy dodavatelů* slouží ke shromažďování informací o sortimentu produktů, které dodavatelé mohou dodávat. Dodavatele mohou publikovat vlastní katalog, a tak je možné katalog udržovat lépe aktuální. K produktu je možné připojit *seznam schválených dodavatelů*, a díky tomu je možné dodavateli pomoci s výběrem, když jsou otevřené nové nákupní objednávky a zabránit použití nežádoucích dodavatelů.

## <a name="procurement"></a>Zásobování

*Nákupní objednávky* lze vytvořit v různém množství různými způsoby včetně:

- Jako výsledek hlavního plánování, které stanovilo požadavek vyžadující nákup. Tento proces generuje plánované nákupní objednávky a po jejich uvolnění jsou generovány nákupní objednávky.
- Prostřednictvím zpracování nákupních žádanek, jejichž výsledkem je zásobování.
- Prostřednictvím zpracování nákupní smlouvy, kde nákupní objednávky jsou vytvořeny jako výdejky z dohod. Používá se běžně při nákupních smlouvách, které se používají k vyjádření paušální objednávky.
- Ručně, když nákupní objednávka není vytvořena na základě jiného dokumentu.

Nákupní objednávky, které jsou konfigurovány s *nákupním workflowů pro schvalování* vyžadují schválení předtím, než budou uloženy jako schválené a tento krok je nutný dříve, než objednávky budou zpracovány dále.

*Potvrzení* nákupních objednávek představuje zjištěnou smlouvu s dodavatelem. Nákupní objednávka bude poté postupně průběhu v odlišných stavech, dokud nebude finálně vyfakturovaná nebo zrušená.  

Při vytvoření nákupní objednávky jsou v řadě polí předem naplněny hodnoty odvozené z uložených informací o dodavateli na stránce **Dodavatelé**. To znamená, že je omezený počet polí, která je nutné v nákupní objednávce vyplnit, ačkoliv je možné přepsat výchozí hodnoty.

### <a name="prices-and-discounts"></a>Ceny a slevy

Ceny a slevy obsahují informace o cenách, slevách a podmínkách rabatu, který nabízejí. Ceny a slevy lze znázornit jako *obchodní smlouvy*. Obchodní smlouvy představují ceníky dodavatele s cenami nebo slevami a obsahují specifickou sadu dat, pro které je dohoda platí. Ceny a slevy lze dojednat a představit prostřednictvím *nákupní smlouvy* s podmínkami, jako závazky nákupu určitého množství nebo peněžní částky, jako předběžná podmínka vyjednaných podmínek. *Smlouvy o rabatu* lze vytvořit s dodavateli, kde získání určitého produktu nebo skupiny produktů může být důvodem rabatu od dodavatele v závislosti na nákupním množství nebo objemu.

### <a name="delivery-options"></a>Možnosti dodání

K dispozici jsou různé možnosti pro proces dodání přidružený k nákupní objednávce. Objednané produkty, lze rozdělit na *plány dodání*, kde části objednaného množství lze plánovat k dodání různého data. Dodávky mohou rovněž zahrnovat *přímou dodávku* zahájenou z prodejní objednávky, která zautomatizuje generování dodacího listu na prodejní objednávce v okamžiku zjištění příjmu produktu na nákupní objednávce. Nákupní objednávky mohou být součástí *dodavatelsko-odběratelského řetězce*, někdy označovaného také jako mezipodnikové nákupní objednávky, kde jsou objednány produkty z odpovídající mezipodnikové prodejní objednávky. V takovém případě jsou některé kroky mezi dvěma souvisejícími mezipodnikovými objednávkami automatické.

### <a name="supplementary-items"></a>Doplňkové položky

Produkty lze nastavit tak, aby zahrnovaly *doplňkové položky*. Ty navrhují produkty, které se vztahují k produktu, které jsou objednávány. Další produkty mohou být vyžadovány, nebo mohou být volitelné. V některých případech mohou být doplňkové položky přidány jako bezplatné produkty, které jsou součástí nákupu dalších produktů.

### <a name="purchase-order-charges"></a>Náklady nákupní objednávky

Náklady mohou být přiřazeny k nákupní objednávce. K tomu dochází automaticky pomocí nastavení automatických nákladů, nebo ručním přidáním nákladů. Náklady lze přiřadit k objednávce na úrovni záhlaví, nebo na úrovni řádku objednávky. Účtování nákladů můžete nastavit různými způsoby. Náklady lze například nastavit k zaúčtování jako náklady produktu. Pokud to provedete, náklady musí být přiřazeny do úrovně řádku objednávky ještě před potvrzením. Je k dispozici možnost umožňující přidělit náklady ze záhlaví objednávky do řádků.

## <a name="product-receipt-and-invoicing"></a>Příjem produktu a fakturace

Nákupní objednávky, které obsahují fyzické produkty běžně vyžadují *registrace doručení*, ke které má dojít v rámci skladu, a poté je registrována pro objednávku *příjemka produktu*. Nákupní objednávky s produkty, které splňují požadavky mohou být nakonfigurovány tak, aby zaměstnanci, kteří vyžadují produkty rovněž museli poskytnout *potvrzení o přijetí*.  

Některé nákupní objednávky zahrnují produkty, které obsahují služby a jiné nefyzické produkty, jejichž příjem ve skladu není nutné. Produkty, které mohou být vytvořeny jako služby nebo *kategorie zásobování* lze přímo použít v nákupní objednávce pro takové objednávky. S těmito objednávkami je někdy vynecháno účtování příjemky produktu a objednávka je fakturována přímo, nebo také se provádí registrace příjemky produktu na nákupní objednávce bez jakékoli předchozí registrace doručení.  

Příjem produktů může být automatickou spotřebu pro určitý účel. Jedná se o předpokládanou spotřebu s přímou dodávkou, spotřebu na projektu nebo účetnictví produktu jako dlouhodobého majetku.  

Při doručení *dodavatelských faktur* od dodavatelů, mohou být faktury nejprve zaznamenány v *registru faktur* nezávisle na nákupní objednávce, a později schválen jako záznam na nákupní objednávce. Záznam faktury dodavatele s nákupní objednávkou zahrnuje párování příjemky produktu k faktuře.  

*Rozúčtování* lze zadat na nákupní objednávce, chcete-li popsat způsob, jakým má být provedena fakturace v hlavní knize a můžete také definovat způsob získávání přidělení finančních prostředků rozpočtu, pokud to je zahrnuto ve vaší konfiguraci.  

Fakturované nákupní objednávky zaznamená pasiva na účet dodavatele v rámci závazků, ze kterého mohou být zpracovány *platby dodavatele*.

## <a name="vendor-performance"></a>Výkonnost dodavatele

Přehled nákupu a výkon je podporován prostřednictvím *zásobování a sestav závazků*, zahrnující analýzy výdajů a analýzy výkonnosti dodavatelů.
