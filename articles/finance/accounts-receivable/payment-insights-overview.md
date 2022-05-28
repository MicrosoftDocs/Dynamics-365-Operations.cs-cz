---
title: Přehledy plateb odběratele (Preview)
description: Toto téma popisuje funkci přehledů plateb, která pomáhá lépe porozumět typickým platebním praktikám jednotlivých zákazníků. Tato funkce vám pomůže identifikovat okolnosti, které ospravedlňují zahájení procesu inkasa dříve, než byste to udělali v ostatních případech.
author: ShivamPandey-msft
ms.date: 11/06/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 59613e41eed95c248595be006f13fb2f32854728
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713211"
---
# <a name="customer-payment-insights-preview"></a>Přehledy plateb odběratele (Preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Toto téma popisuje funkci přehledů plateb, která pomáhá lépe porozumět typickým platebním praktikám jednotlivých zákazníků. Tato funkce vám pomůže identifikovat okolnosti, které ospravedlňují zahájení procesu inkasa dříve, než byste to udělali v ostatních případech. 

## <a name="overview"></a>Přehled

Předvídat, kdy zákazník zaplatí faktury, může být náročné. Tento nedostatek přehledu vede k méně přesným prognózám toku hotovosti, procesům inkasa, které začínají příliš pozdě, a objednávek, které jsou vydány odběratelům, kteří mohou mít pro platbu výchozí nastavení. Přehledy plateb zákazníka (preview) pomáhá organizacím předpovědět, kdy dojde k zaplacení faktury zákazníkem. Tyto informace mohou organizacím pomoci vytvořit strategie inkasa, které zvyšují pravděpodobnost včasného zaplacení. 

## <a name="predictions"></a>Předpovědi

Předpovědi plateb umožní organizacím zlepšovat své obchodní procesy tím, že jim usnadní snadnou identifikaci faktur, které by mohly být placeny pozdě, a přijme vhodná opatření, která zlepšují jejich šanci zaplacení včas.

Pomocí modelu strojového učení, který vyplní historické faktury, platby a data odběratele, aplikace Přehledy plateb odběratelů (Preview) přesnější předpovídá, kdy odběratel zaplatí nevyřízenou fakturu.

Pro každou otevřenou fakturu mohou Přehledy plateb zákazníka (Preview) předpovědět tři pravděpodobnosti platby:

-   Pravděpodobnost platby včas 
-   Pravděpodobnost platby se zpožděním
-   Pravděpodobnost platby s velkým zpožděním

Aplikace Přehledy plateb odběratelů (Preview) také poskytuje agregované zobrazení očekávaných plateb, což může pomoci organizacím pochopit celkovou částku platby, kterou mohou očekávat od zákazníka v jednom ze tří intervalů, včas, se zpožděním a s velkým zpožděním.

[![Agregované zobrazení předpovědí platby.](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Každá faktura má také přiřazenou pravděpodobnost platby včas. Je-li pravděpodobnost platby v čase nižší než 50 %, budou faktury označeny červeným kroužkem, což znamená, že tyto faktury mohou vyžadovat pozornost inkasa. 

[![Seznam pravděpodobností platby.](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Aplikace Customer Payment Insights (Preview) také poskytuje kontextové informace vysvětlující předpověď, jako jsou například nejvyšší faktory ovlivňující předpovědi, aktuální stav obchodu se zákazníkem a podrobnosti historickém chování platby odběratele. V mnoha společnostech byl proces inkasa reaktivní aktivitou; což znamená, že nebyl zahájen, dokud nebyly faktury splatné. 

S nástupem aplikace Přehledy plateb zákazníka (Preview) mohou být organizace aktivnější v oblasti inkas. Již nemusí čekat na to, aby transakce byly splatné, aby mohl být zahájen proces inkasa. Namísto toho mohou pomocí možnosti předpovědi plateb určit, zda provedená aktivní inkasa zvýší pravděpodobnost platby včas. Předpověď platby také poskytuje podnikům informace potřebné k tomu, aby byl proces inkasa zahájen včas.

## <a name="methodology"></a>Metodologie

Vývoj a nasazení řešení AI je tvrdý. Vyžaduje tým datových vědců, odborníků na dané záležitosti a techniků, kteří pracují dlouhou dobu na formulování, vývoji, nasazení a udržování použitelného řešení AI. Usnadňujeme nasazení a používání řešení AI v modulu Finance. V modulu Finance připravujeme řešení vybudovaná na aplikaci Microsoft AI Builder. Koncový uživatel jediným kliknutím na tlačítko může nasadit řešení AI a začít využívat výhod inteligentních předpovědi. Není-li organizace spokojená s přesností předpovědi, může uživatel power user znovu jedním kliknutím spustit prostředí rozšíření aplikace AI builder a poté vybrat nebo zrušit výběr polí používaných k vygenerování předpovědi. Jakmile je to možné, mohou tyto změny vyzkoušet a publikovat a nově osvojený model bude automaticky vybrán pro předpovědi v modulu Finance.

## <a name="how-to-get-customer-payment-insights-preview"></a>Jak získat Přehledy plateb zákazníka (Preview)

Pokud chcete vyzkoušet Přehledy plateb zákazníka (Preview), pošlete e-mail týmu [Přehledy plateb zákazníka (Preview)](mailto:fiap@microsoft.com).

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů

Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations (2) nejsou zahrnuty v dohodě o úrovni služeb pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
