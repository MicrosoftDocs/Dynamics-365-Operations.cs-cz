---
title: Nákupní objednávky neodrážejí jazyková nastavení právnické osoby
description: Název produktu na nákupní objednávce se zobrazuje v jazyce systému místo v jazyce nastaveném pro právnickou osobu, kde byla vytvořena nákupní objednávka.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4deec493b5480dc570ac82876243bc31a2ae87aa
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475785"
---
# <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Nákupní objednávky neodrážejí jazyková nastavení právnické osoby


## <a name="symptoms"></a>Příznaky

Název produktu na nákupní objednávce se zobrazuje v jazyce systému místo v jazyce nastaveném pro právnickou osobu, kde byla vytvořena nákupní objednávka.

## <a name="reproduce-the-issue"></a>Reprodukování problému

Následující postup ukazuje jeden způsob, jak reprodukovat problém.

1. Nastavte jazyk systému na *EN-US* (americká angličtina).
1. Ujistěte se, že existuje produkt, kde jsou udržovány jazyky *EN-US* a *DE* (němčina) pro překlady názvu produktu.
1. Změňte jazyk právnické osoby na *DE*.
1. V právnické osobě, kde je jako jazyk nastaveno *DE*, vytvořte nákupní objednávku, která zahrnuje produkt.
1. Všimněte si, že název produktu je stále zobrazen v americké angličtině (systémový jazyk).

## <a name="resolution"></a>Řešení

Toto chování je záměrné. Na nákupních objednávkách je produkt vždy zobrazen v systémovém jazyce. Při vytvoření deníku potvrzení se použije jazyk nákupní objednávky.
