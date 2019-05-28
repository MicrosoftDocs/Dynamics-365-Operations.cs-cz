---
title: Sledování výsledků vygenerovaných sestav a jejich porovnání se základními hodnotami
description: Toto téma obsahuje informace o porovnání výsledků generovaných sestav ER se základními hodnotami sestavy.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 7f7877ccaa0c45ab5f0032d6808280e3c47a43ca
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554108"
---
# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Sledování výsledků vygenerovaných sestav a jejich porovnání se základními hodnotami

[!include[banner](../includes/banner.md)]

Můžete sledovat výsledky formátů ER, které generují odchozí elektronické dokumenty. Když je zapnuté generování trasování (parametr uživatele ER **Spustit v režimu ladění**), nový záznam sledování je generován v protokolu spuštění formátu pokaždé, když je spuštěna sestava ER. Následující údaje jsou uloženy v každém trasování, které je generováno:

- Všechny výstrahy, které byly vytvořeny pravidly ověření
- Všechny chyby, které byly vytvořeny pravidly ověření
- Všechny vytvořené soubory, které jsou uloženy jako přílohy záznamu sledování

Jednotlivé základní soubory aplikací můžete uložit pro libovolný formát ER. Soubory jsou považovány za základní, když popisují očekávané výsledky sestavy, které jsou spuštěny. Pokud je k dispozici základní soubor pro formát ER, který byl spuštěný při zapnutí generování sledování, sledování kromě dříve zmíněných detailů uloží výsledky porovnání generovaného elektronického dokumentu do základního souboru. Stačí jediné kliknutí a můžete získat také generovaný elektronický dokument a jeho základní soubor v jednom souboru ZIP. Pak můžete provést detailní srovnání pomocí externího nástroje, například Windiff.

Můžete vyhodnotit sledování k analýze, zda elektronické dokumenty, které jsou generovány, obsahují očekávaný obsah. Toto hodnocení můžete provést v prostředí testování přijetí uživatelem (UAT), když byl změněn základní kód (například při migraci na novou instanci aplikace, nainstalované balíčky oprav hotfix nebo změn nasazeného kódu). Tímto způsobem zajistíte, že hodnocení neovlivní provádění sestav ER sestavy, které se používají. U spousty sestav ER může probíhat hodnocení probíhat v bezobslužném režimu.

Další informace o této funkci získáte přehráním průvodců záznamů úloh **Generování sestav ER a porovnání jejich výsledků (část 1)** a **Generování sestav ER a porovnání výsledků (část 2)**, které jsou součástí obchodního procesu **7.5.4.3 Test IT services/solutions (10679)** a které se dají stáhnout ve [službě stažení softwaru Microsoft](https://go.microsoft.com/fwlink/?linkid=874684). Tito průvodci záznamů úloh vás provedou procesem konfigurace rozhraní ER na používání základních souborů pro posouzení generovaných elektronických dokumentů.
