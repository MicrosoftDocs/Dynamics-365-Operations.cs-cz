---
title: Analytické sestavy nejsou aktualizovány
description: Toto téma vysvětluje, jak postupovat, když e nezobrazují změny dat odběratele v žádném z pracovních prostorů odběratele.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "303543"
---
# <a name="analytic-reports-are-not-updated"></a>Analytické sestavy nejsou aktualizovány

[!include [banner](includes/banner.md)]

**Problém**

Změny dat odběratele nejsou zobrazeny na kartách **Analytika** v žádném z pracovních prostorů odběratele.

**Příčina**

Ve výchozím nastavení se sestavy Microsoft Power BI aktualizují každé čtyři hodiny, podle plánu dávkové úlohy Nasadit měrný systém.

**Rozlišení**

Tento problém může být pouze záležitostí časování. Tento postup slouží ke spuštění dávkové úlohy a aktualizaci pracovní prostorů analytiky.

1. Otevřete stránku **Dávkové úlohy** v možnostech **Správa systému \> Odkazy \> Dávkové úlohy \> Dávkové úlohy**. Nebo použijte vyhledávání a zadejte **Dávkové úlohy**.
1. Vyhledejte úlohu **Nasadit měrný systém** v seznamu.
1. Vyberte **Upravit** v horní části stránky a nastavte naplánované počáteční datum a čas na hodnotu, která bude aktualizovat analytiku blíže aktuálnímu času.

![Dávkové úlohy](media/batch-jobs.png)
