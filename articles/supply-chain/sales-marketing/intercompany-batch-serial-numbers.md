---
title: Mezipodniková čísla šarže a sériová čísla
description: Toto téma vysvětluje, co se stane, když zaregistrujete čísla šarže a sériová čísla pro mezipodnikové objednávky
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
ms.openlocfilehash: 9d5e6ddd0bf9ab9dd032e3ab8d1e11d53fba639e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672927"
---
# <a name="intercompany-batch-and-serial-numbers"></a>Mezipodniková čísla šarže a sériová čísla

[!include [banner](../../includes/banner.md)]

Společnosti používající sériová čísla anebo čísla šarže pro sledování vlastních položek rovněž musejí sledovat sériová čísla a čísla šarže vyzvednutých položek. Mezipodnikové funkce automatizují převádění sériových čísel/čísel šarže z jedné společnosti na jinou. Když zaregistrujete sériová čísla a čísla šarží u položek v mezipodnikové prodejní objednávce, můžete nastavit program tak, aby převedl tato čísla automaticky do mezipodnikové nákupní objednávky a originální prodejní objednávky. Příslušné parametry se nastavují ve stránce **Mezipodnikové** pro prodejní objednávku:

- Pokud vyberete pole **Číslo šarže** na stránce **Zásady prodejních objednávek**, číslo šarže se sesynchronizuje se skladovými transakcemi v řádcích mezipodnikové nákupní objednávky při zaúčtování dodacího listu mezipodnikové nákupní objednávky.
- Pokud vyberete pole **Sériové číslo**, sériová čísla jsou sesynchronizována se skladovými transakcemi v řádcích mezipodnikové nákupní objednávky při zaúčtování dodacího listu mezipodnikové nákupní objednávky.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
