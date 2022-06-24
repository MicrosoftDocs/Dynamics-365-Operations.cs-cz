---
title: Mezipodnikové převody měn
description: Tento článek vysvětluje převody měn u mezipodnikových transakcí
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 41bfafc0dcb3bd356931b67dc63b717c0d098116
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851471"
---
# <a name="intercompany-currency-conversions"></a>Mezipodnikové převody měn

[!include [banner](../../includes/banner.md)]

Pokud se kód měny v původní prodejní objednávce a mezipodnikové nákupní objednávce liší, jsou v následujících polích převedeny měny, pokud je povolena synchronizace:

- **Jedn. cena**
- **Prodejní poplatky** nebo **Nákupní poplatky**
- **Sleva**
- **Víceřádková sleva**

Tato pole jsou poté synchronizována s řádkem mezipodnikové prodejní objednávky.

Vzhledem k tomu, že měna v mezipodnikové nákupní objednávce a v mezipodnikové prodejní objednávce je vždy synchronizována, následující pole jsou synchronizovány bez použití převodu měny:

- **Jedn. cena**
- **Prodejní poplatky** nebo **Nákupní poplatky**
- **Sleva**
- **Procento slevy**
- **Víceřádková sleva**
- **Procenta víceřádkové slevy**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
