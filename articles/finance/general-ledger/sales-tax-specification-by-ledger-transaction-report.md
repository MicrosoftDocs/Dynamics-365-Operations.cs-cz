---
title: Specifikace DPH podle sestavy transakce hlavní knihy
description: V tomto tématu je vysvětleno použití specifikace DPH podle sestavy transakce hlavní knihy k zobrazení a tisku informací o transakcích hlavní knihy, pro které se počítá DPH.
author: ericwang
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 75913edcbac0151d5d27d866ff5430b194c62738
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815253"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a>Specifikace DPH podle sestavy transakce hlavní knihy
[!include [banner](../includes/banner.md)]

V tomto tématu je vysvětleno použití **specifikace DPH podle sestavy transakce hlavní knihy** k zobrazení a tisku informací o transakcích hlavní knihy, pro které se počítá DPH.

## <a name="tax-accounts-vs-non-tax-accounts"></a>Daňové účty vs. nedaňové účty

Sestava **Specifikace DPH podle transakce hlavní knihy** zobrazuje daňové transakce pro daňové účty i pro nedaňové účty. Tyto účty jsou rozděleny do kategorií následujícím způsobem:

- **Daňový účet** – účet je považován za daňový účet při zaúčtování daňové transakce a hlavní účet na řádku deníku **DPH** je daňový účet, jako je například účet závazků DPH nebo účet pohledávek DPH.
- **Nedaňový účet** – účet je považován za nedaňový účet při zaúčtování daňové transakce a hlavní účet v původní transakci je nedaňový účet, jako je například účet výnosů nebo účet výdajů.

U daňových účtů je **původní zdroj** **pohledávky DPH** a sloupce **Splatná DPH** v sestavě zobrazují hodnotu **0** (nula). U nedaňových účtů jsou v těchto sloupcích zobrazeny částky.

## <a name="filtering-the-data-on-the-report"></a>Filtrování dat v sestavě

Při generování sestavy jsou k dispozici následující výchozí pole. Tato pole slouží k filtrování dat, která se zobrazí v sestavě.

| Pole                      | Popis |
|----------------------------|-------------|
| Datum                       | Pomocí polí v sekcích **Od** a **Do** definujte rozsah daňových transakcí. |
| Hlavní účet               | Pomocí polí v sekcích **Od** a **Do** definujte rozsah hlavních účtů. |
| Kód DPH             | Pomocí polí v sekcích **Od** a **Do** definujte rozsah kódů DPH. |
| Seskupení                   | Vyberte, zda má být sestava seskupena podle účtu hlavní knihy nebo kódu DPH. |
| Mezisoučet podle kódu DPH/DPH | Chcete-li zobrazit mezisoučty podle kódu DPH, nastavte tuto možnost na hodnotu **Ano**. |
| Pouze součty                | Chcete-li zobrazit pouze součty, nastavte tuto možnost na hodnotu **Ano**. |
| Pouze hlavní účty         | Chcete-li do sestavy zahrnout pouze hlavní účty, nastavte tuto možnost na hodnotu **Ano**. |

## <a name="showing-only-non-tax-accounts-on-the-report"></a>Zobrazení pouze nedaňových účtů v sestavě

Chcete-li v sestavě zobrazit pouze nedaňové účty, nastavte podmínku filtru, například hvězdičku (\*), jak je znázorněno na následujícím obrázku.

![Sestava zobrazující nedaňové účty](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]