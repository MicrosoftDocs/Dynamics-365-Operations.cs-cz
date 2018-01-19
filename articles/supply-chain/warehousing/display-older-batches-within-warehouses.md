---
title: "Konfigurace možnosti Zobrazení starších dávek v rámci skladu na mobilním zařízení"
description: "Toto téma popisuje, jak nastavit mobilní zařízení k zobrazení seznamu skladových míst s dávkami, které jsou starší než aktuální umístění řádku práce."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cd0a9c2e9fbfea987b045e301fb73a505a0f2a4e
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a>Konfigurace možnosti Zobrazení starších dávek v rámci skladu na mobilním zařízení

[!include[banner](../includes/banner.md)]

Konfigurace **Zobrazení starších dávek v rámci skladu** umožňuje zobrazit seznam skladových míst s dávkami, které jsou starší než aktuální umístění řádku práce. Seznam skladových míst, která se zobrazují, obsahuje informace o starších dávkách ve skladovém místě s datem vypršení platnosti a fyzickými zásobami pro každou dávku. Můžete se rozhodnout pro vyskladnění z nového skladového místa nebo můžete pokračovat ve vyskladnění z aktuálního skladového místa. 
- Vyskladnění z nového umístění – pokud vyberete nové místo k vyskladnění, aktuální řádek práce bude aktualizován na nové skladové místo použití a práce bude v novém místě pokračovat obvyklým způsobem. Aby bylo nové skladové místo platné, musí mít dostatek disponibilního množství pro celý řádek práce. Pokud není požadované množství k dispozici, nebude řádek práce aktualizován a zobrazí se seznam. 
- Pokračovat ve vyskladnění z aktuálního místa – pokud budete pokračovat v aktuálním umístění řádku práce, bude množství pro řádek práce dále vyskladňováno z původního umístění.

## <a name="where-it-applies"></a>Kdy se to používá
Možnost Zobrazit starší dávky ve skladu je nakonfigurována pro položky nabídky mobilního zařízení a má vliv na vyskladnění dávky pod položkami.

## <a name="set-up-display-older-batches-within-warehouse"></a>Nastavení zobrazení starších dávek v rámci skladu
Konfigurace **Zobrazení starších dávke v rámci skladu** je k dispozici v položkách nabídky mobilního zařízení, pokud je možnost **Vyskladnit nejstarší dávku** nastavena na **Upozornit**.

- V části **Správa skladu** > **Nastavení** > **Mobilní zařízení** > **Položky nabídky mobilního zařízení** nastavte možnost **Použít existující práci** na **Ano** u položek nabídky a vyberte možnost **Upozornit** v poli **Vyskladnění nejstarší dávky**. 


