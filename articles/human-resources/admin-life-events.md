---
title: Nastavení administrátorských práv pro životní události
description: Tento článek vysvětluje, jak konfigurovat administrátorská práva pro životní události v Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9deed240977394667cee8b107397267b182d960b
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229890"
---
# <a name="set-administrator-rights-for-life-events"></a>Nastavení administrátorských práv pro životní události

[!include [banner](../includes/preview-banner.md)]

Správci mohou aktualizovat možnosti životních události v závislosti na nastavení konfigurace. Na stránce **Parametry lidských zdrojů** můžete nakonfigurovat parametry, které správcům umožní provádět změny ve výběrech plánu. Můžete také plně omezit administrátory v provádění změn.

Na stránce **Parametry lidských zdrojů** můžete nastavit omezení změny plánu pro potvrzené plány a možnosti životních událostí.

Pokud je vybrána možnost **Potvrzené plány**, lze změny provádět pouze v případě, že je aktivní období zápisu. (Příklady období zápisu zahrnují období otevřených zápisů, období zápisu nových zaměstnanců a období zápisu životních událostí.) Pokud tato možnost není vybrána, lze kdykoli provést změny.

Pokud je vybrána možnost **Možnosti životní události**, jsou změny plánu během životní události omezeny možnostmi životní události, které jsou definovány pro typ plánu. Pokud tato možnost není vybrána, výběr plánu lze změnit během životní události.

## <a name="set-plan-change-restrictions"></a>Nastavení omezení změny plánu

Na stránce **Parametry lidských zdrojů** na kartě **Správa zaměstnaneckých výhod** jsou k dispozici následující pole.

| Pole | Popis |
|-------|-------------|
| Potvrzené plány | Tuto možnost vyberte, pokud jsou změny plánu povoleny pouze v případě, že je aktivní období registrace. Pokud tato možnost není vybrána, změny lze provést kdykoli. |
| Možnosti životní události | Vyberte tuto možnost, pokud jsou změny plánu během životní události omezeny možnostmi životní události, které jsou definovány pro typ plánu. Pokud tato možnost není vybrána, výběr plánu lze změnit během životní události. |
