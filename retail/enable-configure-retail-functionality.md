---
title: "Inicializace zdrojových dat v novém prostředí maloobchodu"
description: "Tento článek popisuje data, která jsou vytvořena v rámci inicializačního procesu pro aplikaci Microsoft Dynamics 365 for Operations - Retail."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 534c9ab0f4d95f42d09f35d3197a2258c8d39526
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Inicializace zdrojových dat v novém prostředí maloobchodu

[!include[banner](includes/banner.md)]


Tento článek popisuje data, která jsou vytvořena v rámci inicializačního procesu pro aplikaci Microsoft Dynamics 365 for Operations - Retail.

Po zavedení maloobchodního řešení pomocí aplikace Microsoft Dynamics Lifecycle Services (LCS), musíte k vytvoření základních dat konfigurace inicializovat maloobchodní konfiguraci. **Upozornění:** Před inicializací konfigurace maloobchodu se ujistěte, že jste zadali jazyk a poštovní adresu pro každou právnickou osobu všude, kde maloobchody nastavíte. Tento krok je nutné provést pro každou právnickou osobu, kterou používáte pro maloobchod. Pro inicializaci konfigurace maloobchodu, postupujte takto.

1.  Spusťte klient Dynamics 365 for Operations.
2.  Klikněte na nabídku **Maloobchodní a velkoobchodní prodej** &gt; **Nastavení centrál** &gt; **Parametery** &gt; **Parametry maloobchodu**.
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

Dále protokolování, které se vztahuje k odvětví platební karty (PCI) je povoleni pro databázi aplikace Dynamics 365 for Operations. **Poznámka:** Je možné Maloobchodní plánovač konfigurovat samostatně. Tato možnost umožňuje obnovíte konfiguraci maloobchodního plánovače na výchozí nastavení. Po dokončení inicializace je nutné nakonfigurovat další data pro maloobchod. Několik příkladů:

-   Parametry maloobchodu
-   Parametry programu Maloobchodní plánovač
-   Maloobchodní sítě
-   Registry a zařízení
-   Sortimenty





