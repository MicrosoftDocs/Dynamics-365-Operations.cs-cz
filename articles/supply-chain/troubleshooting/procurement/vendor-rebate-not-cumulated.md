---
title: Rabat dodavatele se nesčítá na základě faktur
description: Rabat dodavatele se nesčítá na základě faktur
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 9d4596a7351969bf181982a24ea1dcc6f5732831
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475839"
---
# <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>Rabat dodavatele se nesčítá na základě faktur

## <a name="symptoms"></a>Příznaky

Pokud zaúčtované faktury mají různá data splatnosti, tyto faktury se neprojeví v rabatech dodavatelů, které se z nich generují.

## <a name="resolution"></a>Řešení

Datum splatnosti se při výpočtu rabatu dodavatele nezohledňuje. Zvažte přizpůsobení systému tak, aby datum splatnosti a vztah k faktuře byly zjevnější s ohledem na skutečný rabat dodavatele.
