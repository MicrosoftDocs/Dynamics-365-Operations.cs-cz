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
ms.openlocfilehash: 6a683ffce487dc4388711ad160c2e8dc55a690dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410713"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a>Možnosti zabránění slevám pro maloobchodní produkty

[!include [banner](includes/banner.md)]

Existují různé důvody, proč maloobchodní prodejci mohou chtít, aby na některé produkty neplatila sleva, buď v rámci promoakce nebo během prodeje v POS.

Následující možnosti, které se nachází na kartě **Velkoobchod** vydaných produktů, umožní nakonfigurování výrobku tak, aby se na něj nevztahovaly všechny nebo pouze manuální slevy. Nastavení lze také určit na úrovni kategorie z hierarchie kategorií.

- **Zabránit všem selvám** - Výběrem této volby můžete zabránit, aby se na tento produkt aplikoval jakýkoliv typ slevy. To zahrnuje promoakce, jako například kombinační slevy, množstevní a mezní slevy, jakož i manuální slevy řádku a transakce použité při prodeji uživatelem POS.
- **Zabránit ručním slevám** - Tuto možnost vyberte pouze pro zabránění slev řádku nebo transakce použitým při prodeji uživatelem POS. Produkty s touto zvolenou možností mají stále nárok na promoakce, jako jsou například kombinační, množstevní a mezní slevy.

> [!NOTE]
> Tato nastavení neomezují operaci přepisu ceny, protože se nastaví základní cena, se kterou se nenakládá jako se slevou.

[![Pole zabránění slev](./media/prevent-discounts.png)](./media/prevent-discounts.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]