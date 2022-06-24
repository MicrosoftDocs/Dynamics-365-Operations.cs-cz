---
title: Životní cyklus správy modelů
description: Tento článek popisuje způsoby, jak udržovat modely strojového učení vaší organizace pro optimalizaci předpovědí, které generují.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 526916929e4bc079f9cea82d8ea9f80813e89b83
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880867"
---
# <a name="model-management-lifecycle"></a>Životní cyklus správy modelů

[!include [banner](../includes/banner.md)]

Tento článek popisuje způsoby, jak udržovat modely strojového učení vaší organizace pro optimalizaci předpovědí, které generují.

Doporučujeme vám trénovat model AI v prostředí izolovaného prostoru a poté ho pomocí spravovaných řešení nasadit do produkčního prostředí. Tento přístup pomáhá zajistit, aby byly k dispozici správné ovládací prvky pro správu životního cyklu modelu.

Protože model AI je založen na dostupných datech faktur a zákazníků, je důležité, aby izolované prostředí mělo nedávnou kopii produkčních dat. Model můžete začít trénovat podle pokynů v části [Použití předpovědí plateb zákazníka](use-customer-payment-predictions.md). Po přetrénování modelu vyhodnoťte výsledky podle popisu v části [Vyhodnocení úvodního modelu predikce plateb zákazníka](evaluate-payment-prediction.md). Použijte informace v části [Vylepšení predikčního modelu](improve-model.md) k experimentování s kombinacemi funkcí a filtrů, které mohou pomoci vylepšit model.

Pokud jste s výsledky trénování spokojeni, postupujte podle pokynů v části [Distribuujte svůj model AI](/ai-builder/distribute-model) k převodu modelu do produkčního prostředí.
