---
title: Jednotkové ceny u nákupních objednávek se nevypočítávají na základě převodu jednotek
description: Jednotkové ceny u nákupních objednávek se nevypočítávají na základě převodu jednotek
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 4695f4661c3abb8ab38e3ca74b513e8529e37d20
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475791"
---
# <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>Jednotkové ceny u nákupních objednávek se nevypočítávají na základě převodu jednotek

## <a name="symptoms"></a>Příznaky

Když se na nákupní objednávce změní jednotka, ceny obchodních smluv se nepřepočítají podle definic převodu jednotek.

## <a name="cause"></a>Příčina

Ceny se vždy získávají z obchodních smluv (nebo jiného nastavení cen v systému, jako jsou prodejní smlouvy nebo ceny zboží), a jsou stanoveny pro jednotku.

Pokud je jednotka změněna na řádku objednávky, systém vyhledá cenu pro novou jednotku a použije tuto cenu. Pokud pro jednotku není nalezena žádná cena, systém cenu nepoužije. Převod jednotky nelze použít k přepočtu ceny na jinou jednotku. Teoreticky se cena za jednu krabici z deseti nemusí rovnat desetinásobku ceny jedné krabice.

## <a name="workaround"></a>Alternativní řešení

Jedním ze způsobů, jak tento problém vyřešit, je zajistit, aby existovaly obchodní smlouvy pro jednotky, u kterých očekáváte, že budou použity na řádcích objednávek pro položku.
