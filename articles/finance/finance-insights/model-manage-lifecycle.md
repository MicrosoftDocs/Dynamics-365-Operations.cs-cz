---
title: Životní cyklus správy modelů (Preview)
description: Toto téma popisuje způsoby, jak udržovat modely strojového učení vaší organizace pro optimalizaci předpovědí, které generují.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 3daec03b7ba349d8f72863317e2d601a83417d58
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638385"
---
# <a name="model-management-lifecycle-preview"></a>Životní cyklus správy modelů (Preview)

[!include [banner](../includes/banner.md)]

Toto téma popisuje způsoby, jak udržovat modely strojového učení vaší organizace pro optimalizaci předpovědí, které generují.

Doporučujeme vám trénovat model AI v prostředí izolovaného prostoru a poté ho pomocí spravovaných řešení nasadit do produkčního prostředí. Tento přístup pomáhá zajistit, aby byly k dispozici správné ovládací prvky pro správu životního cyklu modelu.

Protože model AI je založen na dostupných datech faktur a zákazníků, je důležité, aby izolované prostředí mělo nedávnou kopii produkčních dat. Model můžete začít trénovat podle pokynů v části [Použití předpovědí plateb zákazníka](use-customer-payment-predictions.md). Po přetrénování modelu vyhodnoťte výsledky podle popisu v části [Vyhodnocení úvodního modelu predikce plateb zákazníka](evaluate-payment-prediction.md). Použijte informace v části [Vylepšení predikčního modelu](improve-model.md) k experimentování s kombinacemi funkcí a filtrů, které mohou pomoci vylepšit model.

Pokud jste s výsledky trénování spokojeni, postupujte podle pokynů v části [Distribuujte svůj model AI](https://docs.microsoft.com/ai-builder/distribute-model) k převodu modelu do produkčního prostředí.
