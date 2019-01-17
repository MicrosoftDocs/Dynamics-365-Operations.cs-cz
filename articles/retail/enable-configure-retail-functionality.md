---
title: "Inicializace počátečních dat v nových prostředích Retail"
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
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 52f0c52748958f0bebb6c40df01cfac10c0ed427
ms.contentlocale: cs-cz
ms.lasthandoff: 01/04/2019

---

# <a name="initialize-seed-data-in-new-retail-environments"></a>Inicializace počátečních dat v nových prostředích Retail

[!include [banner](includes/banner.md)]

Tento článek popisuje data, která se vytváří v rámci inicializačního procesu pro aplikaci Microsoft Dynamics 365 for Retail.

Po zavedení maloobchodního řešení pomocí aplikace Microsoft Dynamics Lifecycle Services (LCS), musíte k vytvoření základních dat konfigurace inicializovat maloobchodní konfiguraci.

> [!IMPORTANT]
> Před inicializací konfigurace maloobchodu se ujistěte, že jste zadali jazyk a poštovní adresu pro každou právnickou osobu všude, kde maloobchody nastavíte. Tento krok je nutné provést pro každou právnickou osobu, kterou používáte pro maloobchod.

Pro inicializaci konfigurace maloobchodu, postupujte takto.

1. Spusťte klienta aplikace Dynamics 365 for Retail.
2. Klikněte na možnost **Maloobchod** &gt; **Nastavení centrály** &gt; **Parametery** &gt; **Parametry maloobchodu**.
3. Klepněte na tlačítko **Inicializovat**.

Inicializace vytvoří následující výchozí data konfigurace:

- Úlohy a dílčí úlohy Maloobchodního plánovače
- Schéma maloobchodní sítě
- Plány maloobchodní distribuce
- Výchozí rozložení obrazovky, které zahrnuje mřížky tlačítek, obrázky a motivy
- Informace o časovém pásmu
- Operace pokladních míst (POS)
- Oprávnění POS
- Sestavy kanálu
- Metadata atributu
- Šablony ověření entity
- Dávková úloha pro vymazání historie relace Commerce Data Exchange

U databáze aplikace Dynamics 365 for Retail je také povoleno protokolování, které se vztahuje k odvětví platebních karet (PCI).

> [!NOTE]
> Je možné Maloobchodní plánovač konfigurovat samostatně. Tato možnost umožňuje obnovíte konfiguraci maloobchodního plánovače na výchozí nastavení.

Po dokončení inicializace je nutné nakonfigurovat další data pro maloobchod. Několik příkladů:

- Parametry maloobchodu
- Parametry programu Maloobchodní plánovač
- Maloobchodní sítě
- Registry a zařízení
- Sortimenty

