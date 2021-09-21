---
title: Úkol Aktualizovat příjmy produktů potvrzuje nepotvrzené objednávky
description: Po spuštění Aktualizovat účtenky produktů systém potvrdí nepotvrzené objednávky, které mají stav Registrováno. Další informace o funkci, která tento problém řeší.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 171a978efc6b55b92f429381e72036cb1b3296c6
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475761"
---
# <a name="unconfirmed-purchase-orders-are-confirmed-after-running-update-product-receipts"></a>Nepotvrzené nákupní objednávky jsou potvrzeny po spuštění aktualizace příjemek produktů

## <a name="symptoms"></a>Příznaky

Po spuštění periodického úkolu *Aktualizovat příjemky produktů* systém automaticky potvrzuje nepotvrzené nákupní objednávky, které mají stav transakce zásob *Registrovaný*.

## <a name="resolution"></a>Řešení

Nová funkce zpracování příchozího nákladu *Příjem většího množství nákladu* opravuje tento problém. Chcete-li tuto funkci zapnout, přejděte k pracovnímu prostoru [Správa funkcí](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) a zapněte následující funkce (v pořadí, v jakém jsou uvedeny):

1. Přiřadit transakce zásob nákupní objednávky k vytížení
2. Nadměrné přijetí množství vytížení

Další informace viz [Zaúčtujte registrované množství produktu oproti nákupním objednávkám](/dynamics365/supply-chain/warehousing/inbound-load-handling).
