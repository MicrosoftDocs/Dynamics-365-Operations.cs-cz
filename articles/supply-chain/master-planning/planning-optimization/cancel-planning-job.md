---
title: Zrušení plánovací úlohy
description: Toto téma vysvětluje způsob zrušení aktivní plánovací úlohy, která používá funkci optimalizace plánování.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: b731aa4573b438e594ede702e6556c1be2daa549
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213463"
---
# <a name="cancel-a-planning-job"></a>Zrušení plánovací úlohy

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

V aplikaci Microsoft Dynamics 365 Supply Chain Management můžete zrušit aktivní plánovací úlohy, která používá funkci optimalizace plánování. Pokud v dialogovém okně vyberete možnost **Zrušit**, když je úloha optimalizace plánování spuštěna přímo z uživatelského rozhraní (ne na pozadí), nebude úloha optimalizace plánování stornována. I v případě, že se zobrazí upozornění typu "Operace byla zrušena", budete přesto potřebovat následující postup pro zrušení úlohy plánování s optimalizací plánování.


Chcete-li zrušit aktivní plánovací úlohu, postupujte podle následujících kroků. 

> [!NOTE]
> Lze zrušit pouze aktivní úlohy.

1. Přejděte na **Hlavní plánování \> Nastavení \> Plány**.
2. Vyberte příslušný plán pro spuštění plánování.
3. Zvolte možnost **Historie**.
4. Vybrat plánovací úlohu ke zrušení.
5. Vyberte možnost **Zrušit**.

Stav úlohy bude **Probíhá zrušení**, dokud služba optimalizace plánování nepotvrdí, že úloha byla zrušena. Stav se změní na **Zrušeno**.

> [!NOTE]
> Chcete-li zobrazit změny stavu, je nutné aktualizovat stránku výběrem tlačítka **Aktualizovat**.

## <a name="additional-resources"></a>Další zdroje

[Přehled optimalizace plánování](planning-optimization-overview.md)

[Začínáme s optimalizací plánování](get-started.md)

[Analýza přizpůsobení pro optimalizaci plánování](planning-optimization-fit-analysis.md)

[Zobrazení historie plánu a protokolů plánování](plan-history-logs.md)

[Použití filtrů v plánu](plan-filters.md)
