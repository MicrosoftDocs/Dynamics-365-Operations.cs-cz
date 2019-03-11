---
title: Přehledy plateb zákazníka (preview)
description: Toto téma popisuje, jak přehledy plateb zákazníka mohou pomoci předpovídat, kdy bude faktura zaplacena, a rovněž pomoci organizacím vytvořit strategie optimalizace, které zlepší pravděpodobnost včasného zaplacení.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "344655"
---
# <a name="customer-payment-insights-preview"></a>Přehledy plateb zákazníka (preview)

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> Tato funkce je součástí cíleného vydání a je k dispozici pouze pro uživatele, kteří se rozhodli pro soukromé verze Preview. Tato funkce bude zahrnuta v nadcházejícím vydání všeobecné dostupnosti.

# <a name="overview"></a>Přehled

Organizace často považují za náročné předvídat, kdy zákazník zaplatí faktury. Tento nedostatek přehledu může vést k nepřesným prognózám cashflow, neefektivním procesům výběru a možnosti uvolnění objednávek zákazníkům, kteří mohou představovat úvěrové riziko. Přehledy plateb zákazníka (preview) používají strojové učení pro předpovídání zaplacení faktury. Poskytuje také optimalizační strategie, které mohou být přizpůsobeny tak, aby maximalizovaly pravděpodobnost, že zákazníci budou platit včas.

## <a name="predictions"></a>Předpovědi

Předpovědi plateb umožňují organizacím zlepšit své obchodní procesy tím, že pomáhají:

-   Snadno identifikovat faktury, u kterých se dá očekávat opožděné zaplacení.
-   Provést příslušná opatření ke zlepšení šancí získat platbu včas.

Přehledy plateb zákazníka (preview) používají strojové učení pro předpovídání zaplacení faktury. Využívá historických faktur, plateb a údajů o zákaznících k vytvoření modelu strojového učení, který slouží k předvídání, kdy bude zaplacena faktura.

Pro každou otevřenou fakturu předpovídají Přehledy plateb zákazníka (preview) tři pravděpodobnosti platby:

-  Pravděpodobnost včasné platby (v rámci data splatnosti faktury).
-  Pravděpodobnost platby do 30 dnů v rámci data splatnosti faktury.
-  Pravděpodobnost platby po 30 dnech po datu splatnosti faktury.

Pravděpodobnost platby můžete zobrazit v oddílu předpovědi.

[![Předpovědi platby](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)

Každé faktuře je rovněž přiřazena vítězná pravděpodobnost platby pomocí jednoho ze tří scénářů pravděpodobností plateb definovaných výše. Scénář s nejvyšší pravděpodobnost platby je vítězný scénář.


Předpokládejme například, že předpověď pro fakturu ukazuje 71% pravděpodobnost, že faktura bude zaplacena včas, 13% pravděpodobnost, že faktura bude zaplacena do 30 dnů od data splatnosti a 16% pravděpodobnost, že faktura bude zaplacena po 30 dnech splatnosti. Nejvyšší pravděpodobnost ukazuje, že faktura bude ve včasném scénáři, takže faktura bude označena pravděpodobností, že bude zaplacena včas

[![Předpovědi platby](./media/payment-predict.png)](./media/payment-predict.png)

## <a name="optimization-strategies"></a>Strategie optimalizace

Kromě předpovědí plateb mohou Přehledy plateb zákazníka (preview) využívat optimalizační strategie ke zlepšení šancí na včasné zaplacení. To umožňuje organizacím provádět analýzu „Co když“ tím, že umožňuje uživatelům přizpůsobit fakturu a parametry zákazníků, a pak porovnat odpovídající vliv na pravděpodobnost, že bude platba faktur přijata včas.

Například organizace může chtít vyhodnotit účinek aktualizace hotovostní slevy na faktury na pravděpodobnost, že bude platba přijata včas. Když jsou faktury optimalizovány pro použití nové slevy, uživatelé mohou posoudit účinek uplatnění slevy na pravděpodobnost, že budou tyto faktury zaplaceny včas. Pokud jsou náklady na uplatnění slevy minimální ve srovnání s výhodou včasného získání platby, organizace se může rozhodnout použít vybranou slevu na všechny budoucí otevřené objednávky.

> [!NOTE] 
> V současné době je k dispozici pouze sleva jako optimalizační strategie pro Přehledy plateb zákazníka (preview).

[![Optimalizované předpovědi](./media/optimized-pay.png)](./media/optimized-pay.png)

## <a name="how-to-get-customer-payment-insights-preview"></a>Jak získat Přehledy plateb zákazníka (preview)

Pokud chcete vyzkoušet Přehledy plateb zákazníka (preview), pošlete e-mail týmu [Finanční přehledy - Preview](mailto:fiap@microsoft.com). 

## <a name="privacy-statement"></a>Prohlášení o ochraně osobních údajů

Verze Preview ukládají údaje o zákaznících ve Spojených státech. Kromě toho verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 for Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.
