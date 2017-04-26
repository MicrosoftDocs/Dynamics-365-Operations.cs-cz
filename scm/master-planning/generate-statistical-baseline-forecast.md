---
title: "Generovat statistické základní prognózy"
description: "Tento článek obsahuje informace o parametrech a filtrech, které se používají při výpočtu prognózy poptávky."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c0c918b94fe96d123bb6c25c42fe168a026cd8a9
ms.lasthandoff: 03/31/2017


---

# <a name="generate-a-statistical-baseline-forecast"></a>Generovat statistické základní prognózy

[!include[banner](../includes/banner.md)]


Tento článek obsahuje informace o parametrech a filtrech, které se používají při výpočtu prognózy poptávky. 

Při vytváření základní prognózy musíte nejprve zadat parametry a filtry, které jsou použity ve výpočtu. Můžete například vytvořit základní prognózu poptávky odhadující poptávku v závislosti na datech transakcí z minulého roku pro konkrétní společnost, příští měsíc a pro vybranou skupinu položek. 

Chcete-li generovat prognózy poptávky, přejděte na **Master planning &gt;Prognóza &gt;prognózy poptávky &gt;generovat statistické základní prognózy**. 

Během generování předpovědi lze vybrat interval prognózy. Dostupné hodnoty jsou Den, Týden a Měsíc. 

Počet intervalů prognóz pro generování prognózy je nastaven v poli** Horizont prognózy**. 

Pokud je strategie prognózy nastavena na **Kopírování mezi historickými poptávkami**, konec historického horizontu je ignorován. Systém zkopíruje počet bloků podle **horizontu prognózy** prognózy poptávky, počínaje datem v poli **ode** pod řádkem **historického obzoru**. Díky zkopírování historické poptávky z určitého data dopředu může plánovač výroby vytvořit plán pro další čtvrtletí, a to dvěma způsoby:

-   Zkopírováním poptávky ze stejného čtvrtletí z minulého roku.
-   Zkopírováním poptávky z předchozího čtvrtletí.

Aby se zabránilo nejasnostem v plánování výroby, může být určitý počet intervalů prognóz zamrazen. Tento počet je nastaven v poli **Ochranná doba zablokování**. Na stránce **Upravená prognóza poptávky **jsou buňky pro zmrazené období zakázány a poskytují tak vizuální označení, že by tyto hodnoty neměly být změněny. 

Datum zahájení pro základní prognózu poptávky nemusí být aktuální datum ani datum v budoucnosti. Pro nastavení jiného počátečního data lze používat pole **Datum zahájení základní prognózy – počáteční datum**. Například v červnu mohou uživatelé generovat prognózu pro příští rok. Vzhledem k tomu, že intervaly prognóz mezi koncem historické poptávky a zahájením základní poptávky chybí, nemusí být předpovědi přesné. Pokud používáte služeb Microsoft Dynamics 365 operace poptávky prognózy služby, jsou čtyři způsoby, ve kterých můžete vyplnit chybějící mezery. Můžete zvolit způsob, který má nastavení chybějící\_hodnoty\_nahrazení parametru **parametry prognózy poptávky** stránky. 

**Počáteční datum prognózy základní** - **ode** pole má být nastavena na začátku prognózy plechovka, například ve Spojených státech, neděle Pokud prognózy blok je v týdnu. Systém automaticky upraví **počáteční datum prognózy podle směrného plánu** - **ode** pole odpovídající začátku prognózy plechovka. 

**Počáteční datum prognózy podle směrného plánu** - **ode** nastaveno na datum v minulosti. Jinak řečeno lze generovat prognózu poptávky v minulosti. To je užitečné, protože to umožňuje ladit parametry služby prognózy tak, aby statistická prognóza generovaná v minulosti odpovídala skutečné historické poptávce. Uživatelé pak mohou pokračovat v používání těchto parametru pro vygenerování statistické základní prognózy do budoucna. 

Ruční úpravy provedené v předchozích iteracích prognózy poptávky lze automaticky použít v nové základní prognóze, označíte- li pole **Přeneste ruční úpravy do prognózy poptávky**. Pokud je zaškrtnutí políčka zrušeno, ruční úpravy nebudou do základní prognózy přidány, ale nejsou odstraněny. Ruční úpravy provedené v prognóze lze odstranit pouze v okamžiku importu prognózy, a to zrušením označení pole **Uložit ruční úpravy provedené v základní prognóze poptávky**. Ruční úpravy jsou uloženy v době autorizace. Proto pokud uživatel provádí ruční úpravy Prognóza, ale není povolit zpět do 365 Dynamics pro operace prognózy, změny budou ztraceny. Další informace o ruční úpravy a jejich funkce, viz [autorizace upravené prognóze](authorize-adjusted-forecast.md). 

Generování prognózy poptávky může mít název a komentáře, které usnadní uživatelům identifikovat prognózu, která byla vygenerována. Tyto hodnoty jsou zobrazeny v historii generování předpovědi na stránce **Historie generování statistické základní prognózy**. 

Vnitropodniková plánovací skupina, alokační klíče položky a dalších filtry lze použít v době generování předpovědi. Tyto pomáhají zvýšit výkon nebo rozdělit data do spravovatelných segmentů. Mějte však na paměti, že prognóza poptávky se nevygeneruje pro členy alokačního klíče položky, který není spojen se skupinou mezipodnikového plánování, ani když je alokační klíč položky vybrán v dotazu. 

**Tip**: v některých případech mohou uživatelé obdržet chyby při generování prognózy poptávky, nebo se generování předpovědi dokončí bez relačního protokolu. K tomu může dojít z důvodu přebývajících dat v dotazu, která byla dříve použita pro generování předpovědi. Chcete-li tento problém vyřešit, klepněte na tlačítko **Vybrat** a otevřete tak stránku **Dotaz**, klepněte na **Vynulovat** a potom znovu vytvořte základní prognózu. 

Pokud prognózy nejsou generovány pro velkou sadu položek, ale, například pro jednu položku nebo jednu položku Alokační klíč najednou, pak chcete-li získat lepší výkon, můžete vybrat **použití požadavek odpověď režim** políčko na **hlavního plánování prognózy poptávky - Setup -** - **poptávky prognózy parametry - Azure Machine Learning** kartu.

<a name="see-also"></a>Viz také
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)




