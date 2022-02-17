---
title: Řešení potíží u analytických sestav
description: Toto téma vysvětluje, jak řešit a diagnostikovat problémy, když se nezobrazují změny dat odběratele v žádném z pracovních prostorů odběratele.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6ea04c06858cc98b0e233b9133d9dfbebfe59fd6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067722"
---
# <a name="troubleshoot-analytic-reports"></a>Řešení potíží u analytických sestav


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Vydání**

Změny dat odběratele nejsou zobrazeny na kartách **Analytika** v žádném z pracovních prostorů odběratele.

**Příčina**

Ve výchozím nastavení se sestavy Microsoft Power BI aktualizují každé čtyři hodiny, podle plánu dávkové úlohy Nasadit měrný systém.

**Rozlišení**

Tento problém může být pouze záležitostí časování. Tento postup slouží ke spuštění dávkové úlohy a aktualizaci pracovní prostorů analytiky.

1. Otevřete stránku **Dávkové úlohy** v možnostech **Správa systému \> Odkazy \> Dávkové úlohy \> Dávkové úlohy**. Nebo použijte vyhledávání a zadejte **Dávkové úlohy**.
1. Vyhledejte úlohu **Nasadit měrný systém** v seznamu.
1. Vyberte **Upravit** v horní části stránky a nastavte naplánované počáteční datum a čas na hodnotu, která bude aktualizovat analytiku blíže aktuálnímu času.

![Dávkové úlohy.](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
