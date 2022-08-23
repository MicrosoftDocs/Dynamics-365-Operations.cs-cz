---
title: Kontrola kvality zboží
description: Tento článek popisuje, jak zpracovat objednávky kvality.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b881f9c6f872061864d4254ce880d981ca71c479
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219027"
---
# <a name="inspect-the-quality-of-goods"></a>Kontrola kvality zboží

[!include [banner](../../includes/banner.md)]

Tento článek popisuje, jak zpracovat objednávky kvality. Kontroly kvality obvykle provádějí pracovníci pro kontrolu kvality.

Pokud jsou nainstalována standardní [ukázková data](../../../fin-ops-core/fin-ops/get-started/demo-data.md), můžete je použít k provedení postupů v tomto článku. K použití ukázkových dat vyberte právnickou osobu *USMF*. Poté musíte potvrdit nákupní objednávku *000016* a zaúčtovat příjemku produktu. Objednávka kvality je generována automaticky.

## <a name="step-1-select-a-quality-order"></a>Krok 1: Vyberte objednávku kvality

Pokud chcete vybrat objednávku kvality, postupujte takto.

1. Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Objednávky kvality**.
1. Vyberte objednávku kvality, která byla vygenerována před zahájením tohoto postupu.

## <a name="step-2-record-test-results"></a>Krok 2: Záznam výsledků testu

Chcete-li zaznamenat výsledky testu, postupujte takto.

1. Vyberte **Výsledky**
1. Vyberte možnost **Upravit**.
1. V poli **Výsledné množství** zadejte číslo.
1. V poli **Výsledek** zvolte požadovaný záznam. V tomto příkladu vychází výsledek z předem definovaného výsledku. Obvykle vytvoříte záznam s mnohem přesnějšími výsledky, jako například s velikostí nebo jinou dimenzí.
1. Zvolte **Uložit**.
1. Zavřete stránku.

## <a name="step-3-validate-the-quality-order"></a>Krok 3: Ověřit objednávku kvality

Pokud chcete objednávku kvality ověřit, postupujte takto.

1. Vyberte **Ověřit**.
1. V poli **Potvrdil(a)** vyberte uživatele, který provádí kontrolu.
1. Zvolte **Zvolit**.
1. Vyberte **OK**.
1. Zavřete stránku.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
