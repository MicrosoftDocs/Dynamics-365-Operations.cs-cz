---
title: Přehledy plateb odběratele (Preview)
description: V tomto tématu je popsána funkce platebních přehledů, která pomáhá zlepšit pochopení typických způsobů plateb jednotlivých odběratelů a může identifikovat okolnosti, které opravňují ke spouštění procesů inkasa dříve, než jste provedli jiné operace.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f9f1e4ae4270380c88069723e768fd44ecf8c113
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773914"
---
# <a name="customer-payment-insights-preview"></a>Přehledy plateb odběratele (Preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

V tomto tématu je popsána funkce platebních přehledů, která pomáhá zlepšit pochopení typických způsobů plateb jednotlivých odběratelů a může identifikovat okolnosti, které opravňují ke spouštění procesů inkasa dříve, než je možné provést jiné operace. 

## <a name="overview"></a>Přehled

Organizace často považují za náročné předvídat, kdy zákazník zaplatí faktury. Tento nedostatek přehledu vede k méně přesným prognózám toku hotovosti, procesům inkasa, které začínají příliš pozdě, a objednávek, které jsou vydány odběratelům, kteří mohou mít pro platbu výchozí nastavení. Toto téma popisuje, jak přehledy plateb (Preview) pomáhají organizacím předpovídat, kdy bude faktura zákazníka zaplacena, což pomáhá organizacím vytvořit strategie optimalizace, které zlepší pravděpodobnost včasného zaplacení. 

## <a name="predictions"></a>Předpovědi

Předpovědi plateb umožní organizacím zlepšovat své obchodní procesy tím, že jim usnadní snadnou identifikaci faktur, které by mohly být placeny pozdě, a přijme vhodná opatření, která zlepšují jejich šanci zaplacení včas.

Pomocí modelu strojového učení, který vyplní historické faktury, platby a data odběratele, aplikace Přehledy plateb odběratelů (Preview) přesnější předpovídá, kdy odběratel zaplatí nevyřízenou fakturu.

Pro každou otevřenou fakturu předpovídají Přehledy plateb zákazníka (Preview) tři pravděpodobnosti platby:

-   Pravděpodobnost platby včas 
-   Pravděpodobnost platby se zpožděním
-   Pravděpodobnost platby s velkým zpožděním

Chcete-li pomoci organizacím pochopit celkovou částku platby, kterou mohou očekávat od zákazníka v jednom ze tří intervalů, včas, se zpožděním a s velkým zpožděním, poskytuje aplikace Přehledy plateb odběratelů (Preview) také agregované zobrazení očekávaných plateb.

[![Agregované zobrazení předpovědí platby](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Každá faktura má také přiřazenou pravděpodobnost platby včas. Je-li pravděpodobnost platby v čase nižší než 50 %, budou faktury označeny červeným kroužkem, což znamená, že tyto faktury mohou vyžadovat pozornost inkasa. 

[![Seznam pravděpodobností platby](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Aplikace Customer Payment Insights (Preview) také poskytuje kontextové informace vysvětlující předpověď, jako jsou například nejvyšší faktory ovlivňující předpovědi, aktuální stav obchodu se zákazníkem a podrobnosti historickém chování platby odběratele. V mnoha společnostech byl proces inkasa reaktivní aktivitou; což znamená, že nebyl zahájen, dokud nebyly faktury splatné. 

S nástupem aplikace Přehledy plateb zákazníka (Preview) mohou být organizace aktivnější v oblasti inkas. Již nemusí čekat na to, aby transakce byly splatné, aby mohl být zahájen proces inkasa. Namísto toho mohou pomocí možnosti předpovědi plateb určit, zda provedená aktivní inkasa zvýší pravděpodobnost platby včas. Předpověď platby také poskytuje podnikům informace potřebné k tomu, aby byl proces inkasa zahájen včas.

## <a name="methodology"></a>Metodologie

Vývoj a nasazení řešení AI je tvrdý. Vyžaduje tým datových vědců, odborníků na dané záležitosti a techniků, kteří pracují dlouhou dobu na formulování, vývoji, nasazení a udržování použitelného řešení AI. Usnadňujeme nasazení a používání řešení AI v modulu Finance. V modulu Finance připravujeme řešení vybudovaná na aplikaci Microsoft AI Builder. Koncový uživatel jediným kliknutím na tlačítko může nasadit řešení AI a začít využívat výhod inteligentních předpovědi. Není-li organizace spokojená s přesností předpovědi, může uživatel power user znovu jedním kliknutím spustit prostředí rozšíření aplikace AI builder a poté vybrat nebo zrušit výběr polí používaných k vygenerování předpovědi. Jakmile je to možné, mohou tyto změny vyzkoušet a publikovat a nově osvojený model bude automaticky vybrán pro předpovědi v modulu Finance.

## <a name="how-to-get-customer-payment-insights-preview"></a>Jak získat Přehledy plateb zákazníka (Preview)

Pokud chcete vyzkoušet Přehledy plateb zákazníka (Preview), pošlete e-mail týmu [Přehledy plateb zákazníka (Preview)](mailto:fiap@microsoft.com).

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů

Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.


