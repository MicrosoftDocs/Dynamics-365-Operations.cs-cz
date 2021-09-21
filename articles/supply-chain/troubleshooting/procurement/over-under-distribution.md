---
title: Rozúčtování jsou buď nadměrně nebo nedostatečně distribuovaná
description: Jedno nebo více rozúčtování je nadměrně distribuováno nebo nedostatečně distribuováno.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 7ff0172469df50da9e4272b3fa3f75001a4eb7eb
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475794"
---
# <a name="accounting-distributions-are-either-over--or-under-distributed"></a>Rozúčtování jsou buď nadměrně nebo nedostatečně distribuovaná


## <a name="symptoms"></a>Příznaky

Zobrazí se následující chyba:

> Jedno nebo více rozúčtování je nadměrně distribuováno nebo nedostatečně distribuováno

## <a name="cause"></a>Příčina

K tomuto problému může dojít z důvodu nekonzistence v distribucích nákupních objednávek.

## <a name="resolution"></a>Řešení

Chcete-li tento problém odblokovat a resetovat nákupní objednávku do stavu *Koncept*, přejděte na **Zásobování a zdroje \> Pravidelné úkoly \> Vyčistit \> Reset distribuce nákupní objednávky**. Další informace najdete v následujícím příspěvku na blogu: [Řešení chyb distribuce nákupní objednávky v Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).
