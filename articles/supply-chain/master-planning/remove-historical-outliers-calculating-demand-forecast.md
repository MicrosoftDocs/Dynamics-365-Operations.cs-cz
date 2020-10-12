---
title: Odebrání odlehlých hodnot z historických dat transakcí při výpočtu prognózy poptávky
description: Tento článek popisuje, jak vyloučit odlehlé hodnoty z historických dat, která se používají k výpočtu prognózy poptávky. Vyloučením odlehlých hodnot můžete zlepšit přesnost prognózy.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup, ReqDemPlanOutlierQueryPreview
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a44be713a1049e90618392d028c81e974841b348
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2020
ms.locfileid: "3886816"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>Odebrání odlehlých hodnot z historických dat transakcí při výpočtu prognózy poptávky

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak vyloučit odlehlé hodnoty z historických dat, která se používají k výpočtu prognózy poptávky. Vyloučením odlehlých hodnot můžete zlepšit přesnost prognózy.

Přesnost prognózy můžete zlepšit vyloučením odlehlých hodnot. Tato úloha je volitelná. Přehled procesu:

1.  Klikněte na **Hlavní plánování** &gt; **Nastavení** &gt; **Prognóza poptávky** &gt; **Odebrání odlehlé hodnoty**. Otevře se stránka **Odebrání odlehlé hodnoty**, na které můžete pomocí dotazu vybrat transakce k vyloučení.
2.  Vyberte společnost, pro kterou se použije dotaz, a pak zadejte název a popis. Pole **Datum dotazu** je automaticky nastaveno na aktuální datum.
3.  Zaškrtněte políčko **Aktivní**, chcete-li vyloučit transakce, které byly nalezeny dotazem, z historických dat. Toto nastavení se projeví při vytváření základní prognózy.
4.  Na stránce **Dotaz na odebrání odlehlé hodnoty** lze přidat, odebrat a vybrat kritéria, která definují transakce, které budou vyloučeny při výpočtu základní prognózy. Například vyberte konkrétní položku nebo transakci zakázky, kterou chcete vyloučit.
5.  Klikněte na možnost **Zobrazit transakce**. Stránka **Transakce odlehlé hodnoty** uvádí seznam transakcí, které splňují kritéria, která jste definovali v dotazu, a které budou vyloučeny z historických dat při výpočtu prognózy poptávky.

**Poznámka:** Můžete také vytvořit dotaz, který vychází z existujícího dotazu. Vyberte dotaz, který se má kopírovat, a klikněte na možnost **Duplikovat**. Pole **Datum dotazu** určuje verzi. Můžete vybrat dotaz, jak je, nebo můžete kliknout na možnost **Upravit dotaz**, chcete-li změnit kritéria. Volitelně můžete upravit název a popis nového dotazu.

<a name="additional-resources"></a>Další zdroje
--------

[Přehled prognózy poptávky](introduction-demand-forecasting.md)

[Monitorování přesnosti prognózy](monitor-forecast-accuracy.md)



