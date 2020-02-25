---
title: Řešení potíží u analytických sestav
description: Tento článek vysvětluje, jak postupovat, když e nezobrazují změny dat odběratele v žádném z pracovních prostorů odběratele.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 99d9eb3a16e6470820a2eb0a19c1d50e89bd3d36
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008303"
---
# <a name="troubleshoot-analytic-reports"></a>Řešení potíží u analytických sestav

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
