---
title: Vyloučení produktů s konkrétními stavy životního cyklu produktu
description: Toto téma vysvětluje, jak vyloučit produkty na základě jejich stavu životního cyklu při použití funkce Optimalizace plánování.
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 02c31aa3862df8dabc2b8c065dc3a94877d237f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992413"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a>Vyloučení produktů s konkrétními stavy životního cyklu produktu

[!include [banner](../../includes/banner.md)]

Uvolněné produkty a uvolněné verze produktů obsahují pole **Stav životního cyklu produktu**. Toto pole umožňuje mimo jiné řídit, které produkty jsou zahrnuty během hlavního plánování. Stavy životního cyklu můžete podle potřeby přidávat, odebírat a upravovat přechodem na **Správa informací o produktu \> Nastavit \> Stav životního cyklu produktu**. Pro každý stav životního cyklu produktu nastavte možnost **Je aktivní pro plánování** na *Ano*, pokud by během hlavního plánování měly být zahrnuty produkty, které mají tento stav. Když je možnost nastavena na *Ne*, přidružené produkty a varianty budou vyloučeny ze všech hlavních plánování a všech výpočtů na úrovni kusovníku (BOM).

S vydanými produkty a variantami, kde pole **Stav životního cyklu produktu** je ponecháno prázdné, se zachází způsobem, jako by měly stav životního cyklu produktu, kde možnost **Je aktivní pro plánování** je nastavena na *Ano*. Jinými slovy budou zahrnuty během hlavního plánování.

> [!NOTE]
> Abychom se vyhnuli zbytečným návrhům dodávek, důrazně doporučujeme, abyste všechny zastaralé uvolněné produkty a varianty přidružili ke stavu životního cyklu produktu, kde je možnost **Je aktivní pro plánování** nastavena na *Ne*. Tento přístup je obzvláště důležitý, když pracujete s variantami konfigurace produktu, které nelze opakovaně použít, protože to pomůže zabránit plýtvání.

## <a name="related-resources"></a>Související prostředky

Další informace o stavech životního cyklu produktu najdete v části [Přehled stavu životního cyklu produktu](../../pim/product-lifecycle.md).

Podrobné informace, které zahrnují kroky pro použití stavů životního cyklu produktu k vyloučení produktů z hlavního plánování a výpočtů na úrovni kusovníku, najdete v části [Vytvoření stavu životního cyklu produktu k vyloučení produktů z hlavního plánování](../../pim/tasks/exclude-products-master-planning.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]