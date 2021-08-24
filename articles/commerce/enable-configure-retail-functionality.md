---
title: Inicializace počátečních dat v nových prostředích Commerce
description: Tento článek popisuje data, která se vytváří v rámci inicializačního procesu pro aplikaci Dynamics 365 Commerce.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 14d56636b48d8f8ff15863bb04c762e398f8c370664fbd52f80ed5f05f0e4895
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718724"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a>Inicializace počátečních dat v nových prostředích Commerce

[!include [banner](includes/banner.md)]

Tento článek popisuje data, která se vytváří v rámci inicializačního procesu pro aplikaci Dynamics 365 Commerce.

Po zavedení řešení Commerce pomocí aplikace Microsoft Dynamics Lifecycle Services (LCS), musíte k vytvoření základních dat konfigurace inicializovat konfiguraci Commerce.

> [!IMPORTANT]
> Před inicializací konfigurace Commerce se ujistěte, že jste zadali jazyk a poštovní adresu pro každou právnickou osobu všude, kde obchody nastavíte. Tento krok je nutné provést pro každou právnickou osobu, kterou používáte pro Commerce.

Pro inicializaci konfigurace postupujte takto.

1. Spusťte klienta aplikace Commerce.
2. Click **Retail a Commerce** &gt; **Nastavení centrály** &gt; **Parametry** &gt; **Parametry Commerce**.
3. Klepněte na tlačítko **Inicializovat**.

Inicializace vytvoří následující výchozí data konfigurace:

- Úlohy a dílčí úlohy plánovače Commerce
- Schéma obchodního kanálu
- Plány distribuce Commerce
- Výchozí rozložení obrazovky, které zahrnuje mřížky tlačítek, obrázky a motivy
- Informace o časovém pásmu
- Operace pokladních míst (POS)
- Oprávnění POS
- Sestavy kanálu
- Metadata atributu
- Šablony ověření entity
- Dávková úloha pro vymazání historie relace Commerce Data Exchange

Dále protokolování, které se vztahuje k odvětví platební karty (PCI) je povoleni pro databázi aplikace Commerce.

> [!NOTE]
> Je možné konfigurovat plánovač Commerce samostatně. Tato možnost umožňuje obnovíte konfiguraci plánovače Commerce na výchozí nastavení.

Po dokončení inicializace je nutné nakonfigurovat další obchodní data. Několik příkladů:

- Parametry obchodu
- Parametry plánovače obchodu
- Kanály Commerce
- Registry a zařízení
- Sortimenty


[!INCLUDE[footer-include](../includes/footer-banner.md)]