---
title: Prognóza cashflow (Preview)
description: Toto téma popisuje funkci prognózování cashflow.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
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
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f97b8fc0896f0f7b95bf5609f94367b3a8230ca7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645241"
---
# <a name="cash-flow-forecast-preview"></a>Prognóza cashflow (Preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Cashflow je pro každé podnikání zásadní. Dokonce i ziskové společnosti mohou čelit platební neschopnosti, pokud neudržují cashflow, aby uspokojily okamžité potřeby. Funkce prognózování cashflow v přehledech Finance může společnostem pomoci efektivně sledovat a spravovat své hotovostní zůstatky. Tato funkce využívá strojové učení, aby pomohla podnikům předpovídat cashflow přesněji než dříve. Může také pomoci manažerům činit rozhodnutí, která optimalizují příležitosti v kontextu jejich aktuální pozice hotovosti. 

Pro většinu společností je správa cashflow a jejich prognózování zdlouhavým, opakujícím se a ručním procesem. Většina společností se spoléhá na řešení Microsoft Excel, která mají různé stupně složitosti. Mezi výzvy týkající se přesné předpovědi cashflow patří následující:

- Data nejsou k dispozici osobám s rozhodovací pravomocí, protože jsou rozptýlena na více místech, včetně: 
  - Účetní systém nebo systém plánování podnikových zdrojů
  - Software pro finanční plánování
  - Aplikace Excel
  - Další softwarové aplikace 
- Prognózy jsou založeny na interních znalostních bázích, které se nacházejí v „silech“ v každé doméně nebo oddělení.
- Měření přesnosti prognózování cashflow po uplatnění financí je nejisté a obtížné.
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a>Podrobnosti o funkci prognózování cashflow
Funkce prognózování cashflow zahrnuje následující funkce. 

- Usnadňuje integraci dat cashflow z externích systémů do Dynamics 365 Finance. Prognózy cashflow mohou také využívat rámec importu a exportu dat. Tento rámec usnadňuje integraci s Excel OData. Můžete také kombinovat data z více zdrojů a vytvořit komplexní řešení cashflow. 

- Představuje inteligentní pozici hotovosti. Pozice hotovosti se vytváří na základě chování platby zákazníka, aby bylo možné predikovat, kdy může společnost očekávat, že na její účty dorazí hotovost. Analyzuje také historické vzorce platících dodavatelů, aby predikoval, kdy je pravděpodobné, že budou uhrazeny budoucí faktury a objednávky. 

- Představuje inteligentní prognózování cashflow pro dlouhodobé prognózování pomocí časových řad prostřednictvím automatizované integrace s AI Builder.

- Poskytuje možnost ukládat konkrétní pozice cashflow nebo prognózy, upravovat je a poté snadno porovnávat a měřit výkon prognózy se skutečnými finančními údaji.

- Umožňuje pravděpodobnostní analýzu prostřednictvím porovnání snímků. Můžete například vytvořit několik snímků, které představují optimistické, pesimistické a nejrealističtější zobrazení cashflow a poté porovnat a zobrazit rozdíly.

- Poskytuje možnost zobrazit prognózu cashflow ve více měnách, napříč právnickými osobami a filtrovat a zobrazit cashflow související s bankovním účtem. 

- Umožňuje filtrovat a zobrazit bankovní účty, které souvisejí s finančními dimenzemi.

Funkce prognózování cashflow v Dynamics 365 Finance umožní vaší organizaci transformovat zdlouhavé, složité a přitom opakující se projekce cashflow na jednoduchý automatizovaný proces. Automatizace nejzdlouhavějších aspektů prognózování cashflow vám umožní soustředit se na kritické rozhodování a dosáhnout požadovaných obchodních výsledků.

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Nastavení dimenzí pro prognózu cashflow
Nová karta na stránce **Nastavení prognózy cashflow** umožňuje řídit, jaké finanční dimenze se mají použít pro filtrování v pracovním prostoru **Prognóza cashflow**. Tato karta se zobrazí, pouze pokud je povolena funkce prognózy cashflow. 

Na kartě **Dimenze** vyberte ze seznamu dimenze, které se mají použít pro filtrování, a pomocí kláves se šipkami je přesuňte do pravého sloupce. Pro filtrování dat prognózy cashflow lze vybrat pouze dvě dimenze. 

#### <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů
Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb (SLA) pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.
