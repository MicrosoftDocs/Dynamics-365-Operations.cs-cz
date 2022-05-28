---
title: Synchronizace mezipodnikových nákladů
description: Toto téma vysvětluje synchronizaci mezipodnikových nákladů
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
ms.openlocfilehash: 2c7f60786743cf750b2bb17ccc0dadf71d859766
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678568"
---
# <a name="synchronize-intercompany-charges"></a>Synchronizace mezipodnikových nákladů

[!include [banner](../../includes/banner.md)]

Náklady jsou synchronizovány pouze mezi mezipodnikovou prodejní objednávkou a mezipodnikovou nákupní objednávkou a k této synchronizaci dochází vždy.

Je-li v mezipodnikové prodejní objednávce nebo v mezipodnikové nákupní objednávce vybráno pole **Povolit úpravu ceny**, můžete náklady přidat do mezipodnikové prodejní objednávky nebo do mezipodnikové nákupní objednávky ručně. V opačném případě tak učinit nemůžete.

Pokud pole **Povolit úpravu ceny** v mezipodnikové prodejní objednávce vybráno není, nemůžete náklady ručně přidat do mezipodnikové prodejní objednávky.

Pokud pole **Povolit úpravu ceny** v mezipodnikové nákupní objednávce vybráno není, nemůžete náklady ručně přidat do mezipodnikové nákupní objednávky.

Pokud je pole **Povolit úpravu ceny** povoleno v mezipodnikové nákupní i prodejní objednávce, můžete náklady ručně přidat do obou objednávek. To však může mít za následek nesprávné přidání mnoha nákladů.

Chcete-li předejít tomuto typu konfliktů, je doporučeno povolit přidání nákladů buď do mezipodnikové prodejní objednávky, nebo do mezipodnikové nákupní objednávky, ale ne do obou.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
