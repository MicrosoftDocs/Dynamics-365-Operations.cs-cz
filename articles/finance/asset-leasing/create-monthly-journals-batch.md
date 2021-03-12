---
title: Vytvoření měsíčních položek deníku v dávce
description: Toto téma vysvětluje, jak vytvořit položky deníku v dávce, což pomůže zvýšit efektivitu při zaznamenávání měsíčních výdajů na leasing.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7f46f289c58c32c535dd20fb510cf2812625c49c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971321"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a>Vytvoření měsíčních položek deníku v dávce

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit položky deníku v dávce, což pomůže zvýšit efektivitu při zaznamenávání měsíčních výdajů na leasing. Dávkové zpracování lze použít k vytvoření položek deníku z více plánů. Mezi tyto položky deníku mohou patřit leasingové splátky, amortizace závazků, amortizace používaného majetku a výdaje na zachraňovací náklady. Dávkové zpracování můžete také použít k počátečnímu uznání více leasingů najednou nebo k vytvoření přechodových úprav pro více leasingů najednou.

Chcete-li vytvořit dávkovou úlohu nebo zpracovat platební faktury, odpisy nebo úroky pro více leasingů, přejděte na **Leasing majetku \> Periodicky \> Dávkové vytvoření deníku**. V dialogovém okně, které se zobrazí, můžete vybrat plán, ze kterého mají být vytvořeny položky deníku. Můžete také určit, zda má být dávkový proces spuštěn pro konkrétní entity, skupiny leasingu nebo leasingové knihy.

> [!NOTE]
> Následné transakce, jako jsou plány amortizace závazků, platby, odpisy a výdaje, budou zaúčtovány až po zaúčtování počátečního uznání u příslušných leasingů.
>
> Položky deníku jsou vytvořeny, ale nebudou zaúčtovány, dokud nevyberete příkaz **Spustit**.
