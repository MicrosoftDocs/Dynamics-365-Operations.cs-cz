---
title: Sady finančních dimenzí
description: Toto téma popisuje sady finančních dimenzí a poskytuje několik tipů pro optimalizaci jejich použití.
author: yukonpeegs
ms.date: 03/07/2022
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
ms.openlocfilehash: 9274e7f85005ab27d9f2b35fbb0be42e216941c9
ms.sourcegitcommit: 411874545d7c326fc4aa877948a059371f0ccb3c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/07/2022
ms.locfileid: "8392929"
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

## <a name="delete-a-dimension-set"></a>Odstranění sady dimenzí

Nepokoušejte se **smazat a znovu vytvořit** sady dimenzí jako jakékoli náhradní řešení k vyřešení potenciálních problémů s daty zůstatků pro konkrétní sadu dimenzí. Znovuvytvoření sady dimenzí je nákladné. Další pomoc s problémy vám poskytnou pracovníci zákaznické podpory. 


Další informace naleznete v tématu [Finanční dimenze](financial-dimensions.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
