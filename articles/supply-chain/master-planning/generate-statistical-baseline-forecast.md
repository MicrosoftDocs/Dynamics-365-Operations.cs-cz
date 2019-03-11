---
title: Generování statistické základní prognózy
description: Tento článek obsahuje informace o parametrech a filtrech, které se používají při výpočtu prognózy poptávky.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30f2ccb8c0b4d7c4755e0b8dc66539e165265090
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "326416"
---
# <a name="generate-a-statistical-baseline-forecast"></a>Generování statistické základní prognózy

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o parametrech a filtrech, které se používají při výpočtu prognózy poptávky. 

Při vytváření základní prognózy musíte nejprve zadat parametry a filtry, které jsou použity ve výpočtu. Můžete například vytvořit základní prognózu poptávky odhadující poptávku v závislosti na datech transakcí z minulého roku pro konkrétní společnost, příští měsíc a pro vybranou skupinu položek. 

Pro generování prognózy poptávky přejděte na **Hlavní plánování &gt; Prognózování &gt; Prognóza poptávky &gt; Generovat statistickou základní prognózu**. 

Během generování předpovědi lze vybrat interval prognózy. Dostupné hodnoty jsou Den, Týden a Měsíc. 

Počet intervalů prognóz pro generování prognózy je nastaven v poli **Horizont prognózy**. 

Pokud je strategie prognózy nastavena na **Kopírování mezi historickými poptávkami**, konec historického horizontu je ignorován. Systém zkopíruje počet intervalů uvedených v poli **Horizont prognózy** do prognózy poptávky, začínaje datem v poli **Od data** v nabídce **Historický horizont**. Díky zkopírování historické poptávky z určitého data dopředu může plánovač výroby vytvořit plán pro další čtvrtletí, a to dvěma způsoby:

-   Zkopírováním poptávky ze stejného čtvrtletí z minulého roku.
-   Zkopírováním poptávky z předchozího čtvrtletí.

Aby se zabránilo nejasnostem v plánování výroby, může být určitý počet intervalů prognóz zamrazen. Tento počet je nastaven v poli **Ochranná doba zablokování**. Na stránce **Upravená prognóza poptávky** jsou buňky pro zmrazené období zakázány a poskytují tak vizuální označení, že by tyto hodnoty neměly být změněny. 

Datum zahájení pro základní prognózu poptávky nemusí být aktuální datum ani datum v budoucnosti. Pro nastavení jiného počátečního data lze používat pole **Datum zahájení základní prognózy – počáteční datum**. Například v červnu mohou uživatelé generovat prognózu pro příští rok. Vzhledem k tomu, že intervaly prognóz mezi koncem historické poptávky a zahájením základní poptávky chybí, nemusí být předpovědi přesné. Pokud používáte službu prognózy poptávky aplikace Microsoft Dynamics 365 for Finance and Operations, máte k dispozici čtyři způsoby, jak vyplnit chybějící mezery. Můžete zvolit požadovanou metodu nastavením parametru MISSING\_VALUE\_SUBSTITUTION na stránce **Parametry tvorby prognóz poptávky**. 

Pole **Datum zahájení základní prognózy** - **počáteční datum** musí být nastaveno na začátek intervalu prognózy, například v USA na neděli, pokud je interval prognózy nastaven na týden. Systém automaticky nastaví pole **Datum zahájení základní prognózy** - **počáteční datum** tak, aby odpovídalo začátku intervalu prognózy. 

Pole **Datum zahájení základní prognózy** - **počáteční datum** lze nastavit na datum v minulosti. Jinak řečeno lze generovat prognózu poptávky v minulosti. To je užitečné, protože to umožňuje ladit parametry služby prognózy tak, aby statistická prognóza generovaná v minulosti odpovídala skutečné historické poptávce. Uživatelé pak mohou pokračovat v používání těchto parametru pro vygenerování statistické základní prognózy do budoucna. 

Ruční úpravy provedené v předchozích iteracích prognózy poptávky lze automaticky použít v nové základní prognóze, označíte- li pole **Přeneste ruční úpravy do prognózy poptávky**. Pokud je zaškrtnutí políčka zrušeno, ruční úpravy nebudou do základní prognózy přidány, ale nejsou odstraněny. Ruční úpravy provedené v prognóze lze odstranit pouze v okamžiku importu prognózy, a to zrušením označení pole **Uložit ruční úpravy provedené v základní prognóze poptávky**. Ruční úpravy jsou uloženy v době autorizace. Z toho vyplývá, že pokud uživatel provede ruční úpravy prognózy, ale neprovede zpětnou autorizaci prognózy v aplikaci Finance and Operations, změny budou ztraceny. Další informace o ručních úpravách a jejich průběhu naleznete v tématu [Autorizace upravené prognózy](authorize-adjusted-forecast.md). 

Generování prognózy poptávky může mít název a komentáře, které usnadní uživatelům identifikovat prognózu, která byla vygenerována. Tyto hodnoty jsou zobrazeny v historii generování předpovědi na stránce **Historie generování statistické základní prognózy**. 

Vnitropodniková plánovací skupina, alokační klíče položky a dalších filtry lze použít v době generování předpovědi. Tyto pomáhají zvýšit výkon nebo rozdělit data do spravovatelných segmentů. Mějte však na paměti, že prognóza poptávky se nevygeneruje pro členy alokačního klíče položky, který není spojen se skupinou mezipodnikového plánování, ani když je alokační klíč položky vybrán v dotazu. 

**Tip**: v některých případech mohou uživatelé obdržet chyby při generování prognózy poptávky, nebo se generování předpovědi dokončí bez relačního protokolu. K tomu může dojít z důvodu přebývajících dat v dotazu, která byla dříve použita pro generování předpovědi. Chcete-li tento problém vyřešit, klepněte na tlačítko **Vybrat** a otevřete tak stránku **Dotaz**, klepněte na **Vynulovat** a potom znovu vytvořte základní prognózu. 

Pokud se prognóza nevygeneruje pro velkou sadu položek, ale například vždy jen pro jednu položku nebo jeden alokační klíč položky, bude pro dosažení lepšího výkonu nutné označit pole **Použít režim odpovědi na požadavek** na kartě **Hlavní plánování – nastavení – prognóza poptávky** - **Parametry tvorby prognóz poptávky - Azure Machine Learning**.

<a name="additional-resources"></a>Další zdroje
--------

[Nastavení prognózy poptávky](demand-forecasting-setup.md)

[Ruční úpravy základní prognózy](manual-adjustments-baseline-forecast.md)

[Autorizování upravené prognózy](authorize-adjusted-forecast.md)



