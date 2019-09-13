---
title: Automatická aktualizace čítačů majetku
description: Toto téma popisuje automatickou aktualizaci čítačů majetku ve správě majetku.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875553"
---
# <a name="automatic-update-of-asset-counters"></a>Automatická aktualizace čítačů majetku

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

V předchozí části je popsána ruční registrace čítačů majetku. Nastavení čítačů majetku je popsáno v části [Čítače](../setup-for-objects/counters.md).

Hodnoty čítačů lze také automaticky aktualizovat z registrací výroby na základě výrobních hodin nebo výrobního množství. To se provádí v možnosti **Aktualizace čítačů majetku**. Jeden nebo více majetků lze aktualizovat vložením jednoho parametru, **Od data**. Tento parametr určuje počáteční datum registrací výroby (hodiny nebo vyrobené množství), což znamená počáteční datum, od kterého se mají aktualizovat hodnoty čítačů.

Všechny majetky, které souvisejí se zdrojem *a* mají čítače majetku, které jsou nastaveny pro aktualizaci na základě vyrobeného množství nebo výrobních hodin , budou zahrnuty do automatické aktualizace a budou vytvořeny nové hodnoty čítačů.

V počtu jsou zahrnuty čítače založené na množství výroby, množství zboží a zaregistrovaném chybném množství. Pokud se jednotka použitá pro registraci vyrobeného množství liší od jednotky použité v čítači, bude množství převedeno tak, aby odpovídalo jednotce čítače.

Jak bylo uvedeno výše, automatické čítače lze aktualizovat z registrací výroby. Majetek, pro který chcete automaticky aktualizovat čítače, musí tedy souviset se zdrojem (stroj). Následující popisy poskytují přehled nastavení a zpracování výrobních zakázek (v modulu **Řízení výroby**), který slouží jako základ pro automatickou aktualizaci čítačů majetku v modulu **Správa majetku**.

Po zaregistrování vyrobeného množství nebo výrobních hodin u zdroje můžete aktualizovat související čítače majetku.

1. Klikněte na **Správa majetku** > **Periodická** > **Majetek** > **Aktualizovat čítače majetku**.

2. V poli **Od data** vyberte počáteční datum automatické aktualizace.

>[!NOTE]
>Datum v tomto poli je datem nedokončené výroby z **Transakce postupu** (**Řízení výroby** > **Dotazy a sestavy** > **Výroba** > **Transakce postupu** > **Fyzické datum**).

3. Chcete-li zvolit konkrétní majetek, typy majetku nebo zdroje pro automatickou aktualizaci, klikněte na **Filtr** na záložce s náhledem **Záznamy k zahrnutí** a proveďte příslušný výběr.

4. Pokud je to nutné, na záložce s náhledem **Spustit na pozadí** můžete dle potřeby nastavit automatickou aktualizaci jako dávkovou úlohu.

![Obrázek č. 1](media/12-work-orders.png)

5. Klikněte na tlačítko **OK**. Po dokončení automatické aktualizace čítače majetku můžete zobrazit registrace čítačů související s majetkem v možnostech **Čítače majetku** (**Správa majetku** > **Společné** > **Majetek** > **Všechen majetek** > zvolte majatek > tlačítko **Čítače**).

V **součtech čítače majetku** lze získat přehled o poslední registraci provedené na všech typech čítačů na veškerém majetku. Klikněte na **Správa majetku** > **Dotazy** > **Majetek** > **Agregovaná hodnota majetku**. Zobrazení je velmi podobné **čítačům majetku**, ale nelze přidávat ani upravovat registrace v možnosti **Agregovaná hodnota majetku**. Zobrazení je určeno pouze pro přehled.

![Obrázek č. 2](media/13-work-orders.png)


- Je stále možné vytvořit ruční registrace hodnot čítačů pro typy čítačů, které jsou automaticky aktualizovány. Další informace naleznete v části Ruční aktualizace čítačů majetku.
- Můžete nastavit čítače související s jiným čítačem, což znamená, že při aktualizaci čítače budou související čítače automaticky aktualizovány ve stejnou dobu. Informace o nastavení souvisejícch čítačů naleznete v tématu [Čítače](../setup-for-objects/counters.md).
