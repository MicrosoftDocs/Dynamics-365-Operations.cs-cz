---
title: Možnosti zabránění slevám pro maloobchodní produkty
description: Existují různé důvody, proč maloobchodní prodejci mohou chtít, aby na některé produkty neplatila sleva, buď v rámci promoakce nebo během prodeje v POS.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 64f54c1a63706ccd9225d47df96ffc3f88cf3332
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606911"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a>Možnosti zabránění slevám pro maloobchodní produkty

[!include [banner](includes/banner.md)]

Existují různé důvody, proč maloobchodní prodejci mohou chtít, aby na některé produkty neplatila sleva, buď v rámci promoakce nebo během prodeje v POS.

Následující možnosti, které se nachází na kartě **Maloobchod** vydaných produktů, umožní nakonfigurování výrobku tak, aby se na něj nevztahovaly všechny nebo pouze manuální slevy. Nastavení lze také určit na úrovni kategorie z hierarchie kategorií maloobchodu.

- **Zabránit všem selvám** - Výběrem této volby můžete zabránit, aby se na tento produkt aplikoval jakýkoliv typ slevy. To zahrnuje promoakce, jako například kombinační slevy, množstevní a mezní slevy, jakož i manuální slevy řádku a transakce použité při prodeji uživatelem POS.
- **Zabránit ručním slevám** - Tuto možnost vyberte pouze pro zabránění slev řádku nebo transakce použitým při prodeji uživatelem POS. Produkty s touto zvolenou možností mají stále nárok na promoakce, jako jsou například kombinační, množstevní a mezní slevy.

> [!NOTE]
> Tato nastavení neomezují operaci přepisu ceny, protože se nastaví základní cena, se kterou se nenakládá jako se slevou.

[![Pole zabránění slev](./media/prevent-discounts.png)](./media/prevent-discounts.png)
