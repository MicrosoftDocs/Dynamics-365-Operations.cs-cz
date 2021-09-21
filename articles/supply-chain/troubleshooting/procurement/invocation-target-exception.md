---
title: Během účtování faktury dodavatele dochází k výjimce
description: Během účtování dodavatele faktury dochází k výjimce „Výjimka byla vyvolána cílem vyvolání“.
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
ms.openlocfilehash: ecc63cb7d0d2392105d8e4290f8e837945ae0781
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475792"
---
# <a name="an-exception-occurs-during-vendor-invoice-posting"></a>Během účtování faktury dodavatele dochází k výjimce


## <a name="symptoms"></a>Příznaky

Při zaúčtování faktury dodavatele obdržíte následující výjimku:

> Cíl vyvolání vyvolal výjimku

## <a name="cause"></a>Příčina

K tomuto problému může dojít z důvodu nekonzistence v distribucích nákupních objednávek.

## <a name="resolution"></a>Řešení

Chcete-li tento problém odblokovat a resetovat nákupní objednávku do stavu *Koncept*, přejděte na **Zásobování a zdroje \> Pravidelné úkoly \> Vyčistit \> Reset distribuce nákupní objednávky**. Další informace najdete v následujícím příspěvku na blogu: [Řešení chyb distribuce nákupní objednávky v Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).
