---
title: "Informační kódy"
description: "Tento článek podává přehled o informačních kódech, skupinách informačních kódů a jejich použití."
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailInfocodeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3339b8cb955fcf290e18e73180968fab128cc849
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="info-codes"></a>Informační kódy

[!INCLUDE [banner](includes/banner.md)]

Tento článek podává přehled o informačních kódech, skupinách informačních kódů a jejich použití.

Informační kódy poskytují způsob zaznamenání dat na registrační pokladně pokladních míst (POS). Informační kódy můžete použít k upozornění pokladního k zadání informací během jednotlivých akce v POS, například zboží ve slevě, vrácení zboží nebo výběr odběratele. Pokladní mohou vybrat vstupní hodnoty ze seznamu nebo je zadat jako kód, číslo, datum nebo text. Informační kódy mohou být přiřazeny k předdefinovaným akcím obchodu, maloobchodním položkám, způsobům platby, zákazníkům nebo určitým aktivitám na pokladním místě. Informační kódy lze použít k provedení následujících akcí:
-   Získávání dalších informací v okamžiku transakce, jako je například číslo letu nebo důvodu vrácení.
-   Vyzvat pokladního k výběru ze seznamu cen pro konkrétní produkty.
-   Spojit subkód s informačním kódem, které vyzvou pokladního k zadání údajů při provádění určitých aktivit. Například když odběratel vrací produkt, lze pokladního vyzvat, aby se zeptal na důvod vrácení produktu. Poté můžete použít subkódy k zobrazení seznamu důvodů, ze kterých si pokladní může vybírat.
-   Prodej produktu jako běžný prodej, zlevněný prodej nebo produkt zdarma.
-   Vyzvat pokladního k zadání hodnoty nebo výběru ze seznamu subkódů při otevření zásuvky pokladny bez provedení prodejní operace.

## <a name="info-codes-group"></a>Skupina informačních kódů
V aplikaci Dynamics 365 for Retail můžete vytvářet skupiny informačních kódů. Skupiny informačních kódů přidávají flexibilitu tím, že umožňují definovat méně informačních kódů a poté je používat univerzálněji. Skupiny informačních kódů lze použít následujícími způsoby:
-   Definovat méně informačních kódů a snadno ke znovu použít. Informační kódy, které jsou součástí skupiny informačních kódů, nemají žádné předdefinované závislosti na jiných informačních kódech. Stejný informační kód lze zahrnout do více skupin informačních kódů a poté podle priorit ukazovat stejné informační kódy v pořadí, které dává v konkrétní situaci smysl.
-   Spojit informační kódy s jinými informačními kódy nebo skupinami informačních kódů ke shromažďování informací o produktu nebo transakci, aniž by bylo nutné definovat samostatný informační kód nebo propojený informační kód pro každý scénář.

## <a name="info-code-examples"></a>Příklady informačních kódů
**Příklad 1: Opakované použití informačního kódu** Můžete propojit informační kódy tak, aby při spuštění jednoho informačního kódu byl jiný informační kód spuštěn bezprostředně po něm. Například při prodeji některých produktů můžete vyzvat pokladního, aby se zeptal odběratele, zda chce koupit baterie a záruku produktu. U jiných produktů můžete vyzvat pokladního, aby se zeptal odběratele, zda chce koupit baterie, a aby získal PSČ. Pokud vytvoříte propojené informační kódy pro tyto situace, musíte nastavit každou variantu informačního kódu, aby tak byl pokladní vyzván k dotázání se na správné informace. Při použití skupin informačních kódů lze běžné informační kódy, jako je například dotaz na baterii, nastavit jednou a pak znovu použít ve více skupinách informačních kódů. Také můžete prioritizovat ve skupinách informačních kódů pro určeení pořadí, v němž se pokyny zobrazují.


**Příklad 2: Propojení informačních kódů se skupinami informačních kódů** Při prodeji některých produktů, např. mobilních zařízení, chcete vždy shromáždit sadu určitých informací, například telefonní číslo, identifikátor mobilního zařízení (MEID) a sériové číslo. Také však chcete získat jiné informace pro tablet a pro mobilní telefon. Lze nastavit skupinu informačních kódů, která zahrnuje výzvy na telefonní číslo, MEID a sériové číslo, a poté propojit skupinu informačních kódů s jednotlivým informačním kódem. Při spuštění informačního kódu specifického pro produkt lze skupinu informačních kódů spustit následně, abyste mohli shromažďovat společná data, aniž by bylo nutné definovat více sad propojených informačních kódů pro každé zařízení.





