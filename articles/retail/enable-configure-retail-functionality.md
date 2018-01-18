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
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7388324fe8a9abc8fc3d723b7c8df2c73d76a2ae
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

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





