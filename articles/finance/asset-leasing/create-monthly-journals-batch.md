---
title: Vytvoření měsíčních položek deníku v dávce
description: Toto téma vysvětluje, jak vytvořit položky deníku v dávce, což pomůže zvýšit efektivitu při zaznamenávání měsíčních výdajů na leasing.
author: moaamer
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 22e2892a6866123ecf0e72511bdce19fe12895df
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344846"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a>Vytvoření měsíčních položek deníku v dávce

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Toto téma vysvětluje, jak vytvořit položky deníku v dávce, což pomůže zvýšit efektivitu při zaznamenávání měsíčních výdajů na leasing. Dávkové zpracování lze použít k vytvoření položek deníku z více plánů. Mezi tyto položky deníku mohou patřit leasingové splátky, amortizace závazků, amortizace používaného majetku a výdaje na zachraňovací náklady. Dávkové zpracování můžete také použít k počátečnímu uznání více leasingů najednou nebo k vytvoření přechodových úprav pro více leasingů najednou.

Chcete-li vytvořit dávkovou úlohu nebo zpracovat platební faktury, odpisy nebo úroky pro více leasingů, přejděte na **Leasing majetku \> Periodicky \> Dávkové vytvoření deníku**. V dialogovém okně, které se zobrazí, můžete vybrat plán, ze kterého mají být vytvořeny položky deníku. Můžete také určit, zda má být dávkový proces spuštěn pro konkrétní entity, skupiny leasingu nebo leasingové knihy.

> [!NOTE]
> Následné transakce, jako jsou plány amortizace závazků, platby, odpisy a výdaje, budou zaúčtovány až po zaúčtování počátečního uznání u příslušných leasingů.
>
> Položky deníku jsou vytvořeny, ale nebudou zaúčtovány, dokud nevyberete příkaz **Spustit**.

Chcete-li zaúčtovat počáteční deník uznání k jinému datu, než je datum zahájení leasingu, vyberte **Přiřazení počátečního data zaúčtování uznání**. Zobrazí se pole **Datum**, které vám umožní určit správné datum zaúčtování.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
