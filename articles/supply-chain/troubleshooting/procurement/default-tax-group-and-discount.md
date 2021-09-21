---
title: Výchozí daňová skupina a platební sleva se z účtu faktury nevyplňují
description: Z účtu faktury není vyplněna výchozí daňová skupina a výchozí platební sleva
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
ms.openlocfilehash: bb984eb17209dc92e336df5ad475bb0f70c6e35c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475789"
---
# <a name="default-tax-group-and-cash-discount-arent-filled-in-from-the-invoice-account"></a>Výchozí daňová skupina a platební sleva se z účtu faktury nevyplňují

## <a name="symptoms"></a>Příznaky

Pokud používáte účet faktury, který se liší od účtu zákazníka, nevyplní se při vytvoření nákupní objednávky výchozí daňová skupina a výchozí platební sleva z účtu faktury.

## <a name="resolution"></a>Řešení

Toto chování je záměrné. Výchozí hodnoty pro daňovou skupinu, platební slevy a další informace o cenách jsou založeny na účtu zákazníka, nikoli na účtu faktury.
