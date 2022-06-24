---
title: Synchronizace mezipodnikových informací o odběratelích
description: Tento článek vysvětluje synchronizaci informací o odběratelích u mezipodnikových objednávek
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
ms.openlocfilehash: a3a67c9bcf93f88375d2d4d78d87175200626d50
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897509"
---
# <a name="synchronize-intercompany-customer-information"></a>Synchronizace mezipodnikových informací o odběratelích

[!include [banner](../../includes/banner.md)]

K synchronizaci informací o odběrateli dojde v případě, že je při vytvoření prodejní objednávky nebo při změně odběratele, odkazu dodavatele, případně čísla požadavku odběratele povoleno pole **Informace o odběrateli**.

Hodnotu v těchto synchronizačních polích můžete kdykoli změnit. Výběrem tohoto parametru však můžete určit pouze to, zda je tato hodnota zkopírována do ostatních mezipodnikových objednávek. Pokud jste povolili pole **Informace o odběrateli**, bude každá změna mezipodnikové prodejní objednávky synchronizována s mezipodnikovou nákupní objednávkou. Pokud bylo pole **Informace o odběrateli** povoleno také na mezipodnikové nákupní objednávce, bude synchronizace provedena i na původní prodejní objednávce.

> [!NOTE]
> V případě, že jste pole **Informace o odběrateli** povolili na mezipodnikové nákupní i prodejní objednávce, budou aktualizace provedené určitou osobou ve společnosti přepsány aktualizacemi provedenými jinou osobou v jiné společnosti na stejné objednávce.

Nejlepší praxí je povolit pole **Informace o odběrateli** v mezipodnikové nákupní objednávce. To umožňuje synchronizaci mezi původní prodejní objednávkou a mezipodnikovou nákupní objednávkou a z mezipodnikové nákupní objednávky do mezipodnikové prodejní objednávky.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
