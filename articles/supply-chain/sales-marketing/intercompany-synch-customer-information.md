---
title: Synchronizace mezipodnikových informací o odběratelích
description: Toto téma vysvětluje synchronizaci informací o odběratelích u mezipodnikových objednávek
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
ms.openlocfilehash: c82216c8391f6c447bec74f25cd16b9db18d468d
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548152"
---
# <a name="synchronize-intercompany-customer-information"></a>Synchronizace mezipodnikových informací o odběratelích

[!include [banner](../../includes/banner.md)]

K synchronizaci informací o odběrateli dojde v případě, že je při vytvoření prodejní objednávky nebo při změně odběratele, odkazu dodavatele, případně čísla požadavku odběratele povoleno pole **Informace o odběrateli**.

Hodnotu v těchto synchronizačních polích můžete kdykoli změnit. Výběrem tohoto parametru však můžete určit pouze to, zda je tato hodnota zkopírována do ostatních mezipodnikových objednávek. Pokud jste povolili pole **Informace o odběrateli**, bude každá změna mezipodnikové prodejní objednávky synchronizována s mezipodnikovou nákupní objednávkou. Pokud bylo pole **Informace o odběrateli** povoleno také na mezipodnikové nákupní objednávce, bude synchronizace provedena i na původní prodejní objednávce.

> [!NOTE]
> V případě, že jste pole **Informace o odběrateli** povolili na mezipodnikové nákupní i prodejní objednávce, budou aktualizace provedené určitou osobou ve společnosti přepsány aktualizacemi provedenými jinou osobou v jiné společnosti na stejné objednávce.

Nejlepší praxí je povolit pole **Informace o odběrateli** v mezipodnikové nákupní objednávce. To umožňuje synchronizaci mezi původní prodejní objednávkou a mezipodnikovou nákupní objednávkou a z mezipodnikové nákupní objednávky do mezipodnikové prodejní objednávky.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
