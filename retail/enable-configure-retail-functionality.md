---
title: "Inicializace zdrojových dat v novém prostředí maloobchodu"
description: "Tento článek popisuje data, která se vytváří v rámci inicializačního procesu pro aplikaci Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 0ee002d733882734c9f5a21e0467cacd1b3ff318
ms.contentlocale: cs-cz
ms.lasthandoff: 06/20/2017



---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Inicializace zdrojových dat v novém prostředí maloobchodu

[!include[banner](includes/banner.md)]


Tento článek popisuje data, která se vytváří v rámci inicializačního procesu pro aplikaci Microsoft Dynamics 365 for Retail.

Po zavedení maloobchodního řešení pomocí aplikace Microsoft Dynamics Lifecycle Services (LCS), musíte k vytvoření základních dat konfigurace inicializovat maloobchodní konfiguraci. **Upozornění:** Před inicializací konfigurace maloobchodu se ujistěte, že jste zadali jazyk a poštovní adresu pro každou právnickou osobu všude, kde maloobchody nastavíte. Tento krok je nutné provést pro každou právnickou osobu, kterou používáte pro maloobchod. Pro inicializaci konfigurace maloobchodu, postupujte takto.

1.  Spusťte klienta aplikace Dynamics 365 for Retail.
2.  Klikněte na možnost **Maloobchod** &gt; **Nastavení centrály** &gt; **Parametery** &gt; **Parametry maloobchodu**.
3.  Klepněte na tlačítko **Inicializovat**.

Inicializace vytvoří následující výchozí data konfigurace:

-   Úlohy a dílčí úlohy Maloobchodního plánovače
-   Schéma maloobchodní sítě
-   Plány maloobchodní distribuce
-   Výchozí rozložení obrazovky, které zahrnuje mřížky tlačítek, obrázky a motivy
-   Informace o časovém pásmu
-   Operace pokladních míst (POS)
-   Oprávnění POS
-   Sestavy kanálu
-   Metadata atributu
-   Šablony ověření entity
-   Dávková úloha pro vymazání historie relace Commerce Data Exchange

U databáze aplikace Dynamics 365 for Retail je také povoleno protokolování, které se vztahuje k odvětví platebních karet (PCI). **Poznámka:** Je možné Maloobchodní plánovač konfigurovat samostatně. Tato možnost umožňuje obnovíte konfiguraci maloobchodního plánovače na výchozí nastavení. Po dokončení inicializace je nutné nakonfigurovat další data pro maloobchod. Několik příkladů:

-   Parametry maloobchodu
-   Parametry programu Maloobchodní plánovač
-   Maloobchodní sítě
-   Registry a zařízení
-   Sortimenty





