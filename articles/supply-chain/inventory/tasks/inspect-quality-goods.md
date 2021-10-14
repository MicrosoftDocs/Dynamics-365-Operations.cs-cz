---
title: Kontrola kvality zboží
description: Toto téma popisuje, jak zpracovat objednávky kvality.
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
ms.openlocfilehash: cc2fbbedb608b38c6855fbd48ff0c3e26ee3e0bc
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575841"
---
# <a name="inspect-the-quality-of-goods"></a>Kontrola kvality zboží

[!include [banner](../../includes/banner.md)]

Toto téma popisuje, jak zpracovat objednávky kvality. Kontroly kvality obvykle provádějí pracovníci pro kontrolu kvality.

Pokud jsou nainstalována standardní ukázková data, můžete je použít k provedení postupů v tomto tématu. K použití ukázkových dat vyberte právnickou osobu *USMF*. Poté musíte potvrdit nákupní objednávku *000016* a zaúčtovat příjemku produktu. Objednávka kvality je generována automaticky.

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
