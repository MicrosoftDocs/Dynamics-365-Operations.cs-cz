---
title: Automatická aktualizace čítačů majetku
description: Toto téma popisuje automatickou aktualizaci čítačů majetku ve správě majetku.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d3e8619439545cf3ea42f84a6dd7ee6ffdf1026e
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021923"
---
# <a name="automatic-update-of-asset-counters"></a>Automatická aktualizace čítačů majetku

[!include [banner](../../includes/banner.md)]

Informace o ruční registraci čítačů majetku naleznete v tématu [Ruční aktualizace čítačů majetku](../work-orders/manual-update-of-asset-counters.md). Další informace o nastavení čítačů majetku naleznete v tématu [Čítače](../setup-for-objects/counters.md).

Hodnoty čítačů lze také automaticky aktualizovat z registrací výroby na základě výrobních hodin nebo výrobního množství (tj. vyrovené množství). Tato aktualizace je prováděna na stránce **Aktualizovat čítače majetku**. Jeden nebo více majetků lze aktualizovat nastavením jednoho parametru, **Od data**. Tento parametr určuje počáteční datum registrací výroby (výrobní hodiny nebo výrobní množství). Jinými slovy, určuje datum, od kterého se mají aktualizovat hodnoty čítačů.

Všechny majetky, které souvisejí se zdrojem *a* mají čítače majetku, které jsou nastaveny pro aktualizaci na základě vyrobeného množství nebo výrobního množství, budou zahrnuty do automatické aktualizace a budou vytvořeny nové hodnoty čítačů. Budou vytvořeny nové hodnoty čítačů.

U čítačů, které jsou založeny na množství výroby, zahrnuje množství zboží i zaregistrované chybné množství. Pokud se jednotka použitá pro registraci výrobního množství odlišuje od jednotky použité pro čítač, bude množství převedeno tak, aby odpovídalo jednotce čítače.

Jak bylo uvedeno výše, automatické čítače lze aktualizovat z registrací výroby. Majetek, pro který chcete automaticky aktualizovat čítače, musí tedy souviset se zdrojem (stroj). Po zaregistrování vyrobeného množství nebo výrobních hodin u zdroje můžete aktualizovat související čítače majetku.

1. Vyberte **Správa majetku** > **Periodická** > **Majetek** > **Aktualizovat čítače majetku**.

2. V poli **Od data** vyberte počáteční datum automatické aktualizace.

    >[!NOTE]
    >Datum v tomto poli je datem nedokončené výroby z **Transakce postupu** (**Řízení výroby** > **Dotazy a sestavy** > **Výroba** > **Transakce postupu** > **Fyzické datum**).

3. Na pevné záložce **Záznamy, které mají být zahrnuty** můžete vybrat konkrétní majetek, typy majetku nebo zdroje pro automatickou aktualizaci. Výběrem možnosti **Filtr** proveďte příslušné výběry.

4. Na záložce s náhledem **Spustit na pozadí** můžete dle potřeby nastavit automatickou aktualizaci jako dávkovou úlohu.

    Následující ilustrace znázorňuje příklad dialogu **Aktualizovat čítače majetku**.

    ![Obrázek č. 1](media/12-work-orders.png)

5. Vyberte **OK**. 

Po dokončení aktualizace automatického čítače majetku můžete zobrazit registrace čítačů, které souvisejí s majetkem na stránce **Čítače majetku**. Vyberte **Správa majetku** > **Společné** > **Majetek** > **Všechen majetek**, vyberte majetek a pak v podokně akcí na kartě **Majetek** ve skupině **Preventivní** vyberte **Čítače**.

Na stránce **Souhrnná hodnota majetku** lze získat přehled o poslední registraci provedené na všech typech čítačů na veškerém majetku. Vyberte **Správa majetku** > **Dotazy** > **Majetek** > **Agregovaná hodnota majetku**. Tato stránka se podobá stránce **Čítače majetku**, ale nelze přidávat ani upravovat registrace. Zobrazení je určeno pouze pro přehled.

Následující ilustrace znázorňuje příklad stránky **Agregovaná hodnota majetku**.

![Obrázek č. 2](media/13-work-orders.png)

Mějte na paměti následující body:

- Je stále možné vytvořit ruční registrace hodnot čítačů pro typy čítačů, které jsou automaticky aktualizovány. Další informace naleznete v části [Ruční aktualizace čítačů majetku](../work-orders/manual-update-of-asset-counters.md).

- Můžete nastavit čítače, které souvisejí s jiným čítačem. V takovém případě jsou při aktualizaci čítače automaticky aktualizovány související čítače. Další informace o nastavení souvisejících čítačů naleznete v tématu [Čítače](../setup-for-objects/counters.md).

