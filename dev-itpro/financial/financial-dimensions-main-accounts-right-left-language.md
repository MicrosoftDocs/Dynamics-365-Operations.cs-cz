---
title: "Finanční dimenze a hlavní účty v jazyce zprava doleva."
description: "Toto téma popisuje některá rozhodnutí implementací, která byste měli zvážit, pokud používáte jazyk zprava doleva v aplikaci Microsoft Dynamics 365 for Operations, a která musíte nastavit ve finančních dimenzích a hlavních účtech."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b1f196d2a13bba49647dd4f008cd39b7417940f1
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="financial-dimensions-and-main-accounts-in-a-right-to-left-language"></a>Finanční dimenze a hlavní účty v jazyce zprava doleva.

[!include[banner](../includes/banner.md)]


Toto téma popisuje některá rozhodnutí implementací, která byste měli zvážit, pokud používáte jazyk zprava doleva v aplikaci Microsoft Dynamics 365 for Operations, a která musíte nastavit ve finančních dimenzích a hlavních účtech.

Finanční dimenze a hlavní účty jsou klíčové součásti fázi plánování pro implementaci. Po vytvoření se finanční dimenze a hlavní účty v systému používají na stránkách **Konfigurování účetní struktury**, **Rozšířené struktury pravidel** a **konfigurace finanční dimenze pro integraci aplikací**. Pořadí, které je definováno na těchto stránkách, slouží v systému k zadávání dat a spotřeby. V některých místech v systému se finanční dimenze a hlavní účty zobrazují v samostatných polích. Avšak na dalších místech, jako jsou například deníky, finanční dimenze a hlavní účty, se zobrazí jako jeden řetězec.

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Doporučené postupy při nastavování finančních dimenzí a hlavních účtů v systému zprava doleva

-   Vyberete-li oddělovač účtové osnovy, vyberte jednu z možností dvojího oddělovače: dvojitá pomlčka (-–), dvě čáry (||), dvě tečky (..) nebo dvojnásobné podtržení (\_\_).
-   Když vytvoříte finanční dimenzi a hodnoty hlavního účtu, použijte pouze číslice a znaky zprava doleva.
-   Nepoužívejte vybrané oddělovače účtové osnovy ve finanční dimenzi a hodnotách hlavního účtu.

Podle těchto doporučených postupů můžete zajistit konzistentní reprezentaci uživatelem definované objednávky v celém systému.




