---
title: Zrušení plánovací úlohy
description: Toto téma vysvětluje způsob zrušení aktivní plánovací úlohy, která používá funkci optimalizace plánování.
author: ChristianRytt
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: e9cf4902251c3c2b93af12a8ad9bd571930ef769
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833322"
---
# <a name="cancel-a-planning-job"></a>Zrušení plánovací úlohy

[!include [banner](../../includes/banner.md)]

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]