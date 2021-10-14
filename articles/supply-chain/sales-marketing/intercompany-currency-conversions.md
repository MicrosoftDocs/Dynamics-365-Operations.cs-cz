---
title: Mezipodnikové převody měn
description: Toto téma vysvětluje převody měn u mezipodnikových transakcí
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 540849003d532ef2f0905c18332d9cb82a04cf7c
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548157"
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
