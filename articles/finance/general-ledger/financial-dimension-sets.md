---
title: Sady finančních dimenzí
description: Toto téma popisuje sady finančních dimenzí a poskytuje několik tipů pro optimalizaci jejich použití.
author: yukonpeegs
manager: AnnBe
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b719d8eb868cb1722b470be4443d01181078ce21
ms.sourcegitcommit: 97ada5d52ed1829dcf030dad254096cd8df25da8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/06/2021
ms.locfileid: "5864405"
---
# <a name="financial-dimension-sets"></a>Sady finančních dimenzí

[!include [banner](../includes/banner.md)]

Toto téma popisuje sady finančních dimenzí a poskytuje několik tipů pro optimalizaci jejich použití.

Sada dimenzí je seřazený seznam finančních dimenzí, které lze použít k shrnutí dat hlavní knihy uživatelem definovaným způsobem. Primárním použitím sady dimenzí je definování předvahy.

Jedinou standardní sadou dimenzí je sada dimenzí, která obsahuje pouze hlavní účet.

Stránku **Sady finanční dimenze** používáte pro vytváření a správu sad finančních dimenzí.

## <a name="dimension-set-balances"></a>Zůstatky sad dimenzí

Sada dimenzí může mít zůstatky, které jsou založeny na jejích finančních dimenzích. Zůstatky existují v hlavní knize a jsou založeny na definici sady dimenzí. Zůstatky jsou shrnuty z údajů hlavní knihy, aby pomohly zlepšit výkon při jejich načtení (například při generování předvahy).

## <a name="create-balances"></a>Vytvořit zůstatky

Použijte tlačítko **Vytvořit zůstatky** k inicializaci zůstatků pro sadu dimenzí, která aktuálně nemá zůstatky.

> [!NOTE]
> Doporučujeme omezit počet sad dimenzí, které mají zůstatky, protože aktualizace zůstatků ovlivňují všechny aktivity účtování hlavní knihy.

## <a name="update-balances"></a>Aktualizovat zůstatky

Použijte tlačítko **Aktualizovat zůstatky** k zahrnutí nejnovější aktivity účtování hlavní knihy do zůstatků. Aktualizace zůstatku jsou lehké operace. Musí zpracovat pouze aktivitu účtování hlavní knihy, ke které došlo od poslední aktualizace.

> [!NOTE]
> Zobrazení zkušebního zůstatku vynutí aktualizaci, aby se zajistilo, že zobrazené zůstatky jsou aktuální. Zvažte použití opakované dávkové úlohy, aby aktualizace vašich nejčastěji používaných sad dimenzí byly rychlé. Tímto způsobem pomáháte minimalizovat dobu, po kterou musí uživatelé zůstatku na předvahu čekat.

## <a name="rebuild-balances"></a>Znovu sestavit zůstatky

Tlačítko **Znovu sestavit zůstatky** použijte pro opětovné vytvoření zůstatků od nuly. Tímto způsobem pomůžete zajistit, aby odpovídaly údajům v hlavní knize. Opětovné sestavení zůstatků vyžaduje spoustu zpracování a nemělo by se obvykle vyžadovat.

> [!NOTE]
> Pokud máte scénář, který pravidelně vyžaduje opětovné sestavení zůstatků, doporučujeme vám kontaktovat zákaznickou podporu. Zákaznická podpora vám pomůže určit, proč zůstatky neodpovídají údajům v hlavní knize.

## <a name="clear-balances"></a>Vymazat zůstatky

Tlačítko **Vymazat zůstatky** použijte k odstranění zůstatků a zastavení dalších aktualizací. Sada dimenzí již nebude mít dopad na aktivity účtování hlavní knihy.

Další informace naleznete v tématu [Finanční dimenze](financial-dimensions.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
