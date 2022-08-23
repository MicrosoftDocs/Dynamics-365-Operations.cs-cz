---
title: Integrovaná hlavní kniha
description: Tento článek popisuje integraci dat hlavní knihy mezi finančními a provozními aplikacemi a ostatními aplikacemi Dynamics 365 používajícími Dataverse.
author: RamaKrishnamoorthy
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 728c131c260586e7f1f787f22ccf02ed81c94c01
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289141"
---
# <a name="integrated-ledger"></a>Integrovaná hlavní kniha

[!include [banner](../../includes/banner.md)]



V obchodní aplikaci definují data hlavní knihy základní nastavení pro to, jak společnost podniká. Data hlavní knihy například popisují fiskální rok, podle kterého se společnost řídí, měny, ve kterých provádí transakce, a účty, které používá. Tento článek popisuje integraci těchto základních finančních dat.

## <a name="templates"></a>Šablony

Data hlavní knihy zahrnují mapy kolekce tabulek základních financí, které pracují společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.

Finanční a provozní aplikace | Aplikace Customer Engagement     | popis
---------------------------------|----------------------------------|------------
[Směnné kurzy CDS](mapping-reference.md#123) | msdyn_currencyexchangerates |
[Účtová osnova](mapping-reference.md#121) | msdyn_chartofaccountses |
[Měny](mapping-reference.md#218) | transactioncurrencies |
[Pár měny směnného kurzu](mapping-reference.md#122) | msdyn_currencyexchangeratepairs |
[Typ směnného kurzu](mapping-reference.md#129) | msdyn_exchangeratetypes |
[Formát finanční dimenze](mapping-reference.md#130) | msdyn_financialdimensionformats |
[Finanční dimenze](mapping-reference.md#128) | msdyn_dimensionattributes |
[Entita integrace fiskálního kalendáře](mapping-reference.md#132) | msdyn_fiscalcalendars |
[Fiskální kalendářní období](mapping-reference.md#131) | msdyn_fiscalcalendarperiods |
[Entita integrace roku fiskálního kalendáře](mapping-reference.md#133) | msdyn_fiscalcalendaryears |
[Ledger](mapping-reference.md#148) | msdyn_ledgers |
[Hlavní účet](mapping-reference.md#152) | msdyn_mainaccounts |
[Kategorie hlavního účtu](mapping-reference.md#151) | msdyn_mainaccountcategories |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

