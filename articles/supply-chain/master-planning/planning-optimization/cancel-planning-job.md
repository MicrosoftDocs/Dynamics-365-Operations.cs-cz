---
title: Zrušení plánovací úlohy
description: Tento článek vysvětluje způsob zrušení aktivní plánovací úlohy, která používá funkci optimalizace plánování.
author: t-benebo
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
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: f5f1f2c8e3e43e36d837ebf989422b0dca7819d6
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741169"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]