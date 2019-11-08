---
title: Projektové prodejní objednávky pro projekty určené časem a materiálem
description: Toto téma vysvětluje, jak vytvářet prodejní objednávky na základě projektů určených časem a materiálem.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 2f27e3e0a2d6aadc4c5224b55f8a416cbe4e83aa
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551195"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projektové prodejní objednávky pro projekty určené časem a materiálem

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Toto téma popisuje způsob vytvoření prodejní objednávky pro projekt. Prodejní objednávky lze vytvořit pouze pro projekty typu **čas a materiál**.

Pokud má projekt určený časem a materiálem na projektové smlouvě více zdrojů financování, musíte povolit parametr **Povolit prodejní objednávky pro projekty s více zdroji financování** na stránce **Parametry modulu Řízení a účetnictví projektu**. 

> [!NOTE]
> - Podpora prodejních objednávek projektu s více zdroji financování je k dispozici od vydání aplikace 10.0.2 a vyššího.
> - Parametr umožňující podporu pro prodejní objednávky projektu s více zdroji financování bude odstraněn ve vlně vydání z dubna 2020, po které bude funkce vždy povolena.

Prodejní objednávky na základě projektu lze vytvořit dvěma způsoby:

- Přejděte na samotný projekt. V podokně akcí zvolte **Spravovat > Úlohy položky > Prodejní objednávka**. Informace o projektu se nastaví na výchozí prodejní objednávky z projektu. Pokud má projektová smlouva více než jeden zdroj financování, budete muset vybrat zdroj financování pro nastavení zákazníka pro prodejní objednávku. Pokud pro projekt existuje pouze jeden zdroj financování, bude zákazník automaticky nastaven.
- Přejděte na stránku se seznamem **Všechny prodejní objednávky** a vytvořte novou prodejní objednávku. Musíte vybrat projekt pro prodejní objednávku. Po výběru projektu bude zákazník nastaven ze zdroje financování nebo bude nutné vybrat zdroj financování, pokud má projektová smlouva více zdrojů financování.

