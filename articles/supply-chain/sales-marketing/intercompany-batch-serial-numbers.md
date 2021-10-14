---
title: Mezipodniková čísla šarže a sériová čísla
description: Toto téma vysvětluje, co se stane, když zaregistrujete čísla šarže a sériová čísla pro mezipodnikové objednávky
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
ms.openlocfilehash: 4da936263bb57c24eeb7021ac61b3945bb2777fb
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548159"
---
# <a name="intercompany-batch-and-serial-numbers"></a>Mezipodniková čísla šarže a sériová čísla

[!include [banner](../../includes/banner.md)]

Společnosti používající sériová čísla anebo čísla šarže pro sledování vlastních položek rovněž musejí sledovat sériová čísla a čísla šarže vyzvednutých položek. Mezipodnikové funkce automatizují převádění sériových čísel/čísel šarže z jedné společnosti na jinou. Když zaregistrujete sériová čísla a čísla šarží u položek v mezipodnikové prodejní objednávce, můžete nastavit program tak, aby převedl tato čísla automaticky do mezipodnikové nákupní objednávky a originální prodejní objednávky. Příslušné parametry se nastavují ve stránce **Mezipodnikové** pro prodejní objednávku:

- Pokud vyberete pole **Číslo šarže** na stránce **Zásady prodejních objednávek**, číslo šarže se sesynchronizuje se skladovými transakcemi v řádcích mezipodnikové nákupní objednávky při zaúčtování dodacího listu mezipodnikové nákupní objednávky.
- Pokud vyberete pole **Sériové číslo**, sériová čísla jsou sesynchronizována se skladovými transakcemi v řádcích mezipodnikové nákupní objednávky při zaúčtování dodacího listu mezipodnikové nákupní objednávky.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
