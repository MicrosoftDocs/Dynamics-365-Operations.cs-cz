---
title: Řešení potíží u analytických sestav
description: Tento článek vysvětluje, jak postupovat, když e nezobrazují změny dat odběratele v žádném z pracovních prostorů odběratele.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8dab12213e9730e72aede70c5b5d1368ef77664e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053532"
---
# <a name="troubleshoot-analytic-reports"></a>Řešení potíží u analytických sestav

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

![Dávkové úlohy](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]