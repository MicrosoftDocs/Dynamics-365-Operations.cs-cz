---
title: Po konfiguraci profilu nebylo pro cluster nalezeno dost práce
description: Pokud konfigurujete profil clusteru, může se zobrazit chybová zpráva, že není možné najít dostatek práce. Upravte profil a nastavte Aktivovat pozice na Ne.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 139fd72e571c8ef83af2fd0e497cf334b6ef0ea4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475762"
---
# <a name="not-enough-work-found-for-cluster-when-using-system-directed-cluster-picking"></a>Při používání vyzvedávání seskupení řízeného systémem nebyl pro seskupení nalezen dostatek práce

## <a name="symptoms"></a>Příznaky

Když používáte proces *Systémově řízený výdej seskupení*, pokud nakonfigurujete profil seskupení, kde lze vybrat například 10 pozic, proces funguje podle plánu, když je dostatek práce k výdeji do 10 pozic. Pokud je však k výběru pouze osm pozic, zobrazí se následující chybová zpráva:

> Pro seskupení nelze nalézt dostatek práce.

## <a name="resolution"></a>Řešení

Chcete-li tento problém vyřešit, upravte profil seskupení a nastavte možnost **Aktivovat pozice** na *Ne*.
