---
title: Nelze vytvořit řádek vytížení z důvodu neplatných dimenzí zásob
description: Při pokusu o vydání zpětné prodejní objednávky do skladu se může zobrazit chyba ohledně neplatných dimenzí zásob. Odstraňte je z řádku objednávky.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac58
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3cb728f6a989cdac63c91d49baaea094bace59e4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475812"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>Nelze vytvořit řádek vytížení pro vratku prodejní objednávky z důvodu neplatných dimenzí zásob

## <a name="symptoms"></a>Příznaky

Při pokusu o uvolnění objednávky prodejní vratky do skladu se může zobrazit následující chybová zpráva:

> Nelze vytvořit řádek nákladu pro tento řádek objednávky, protože obsahuje neplatné dimenze inventáře. V hierarchii rezervací nemůžete odkazovat na dimenze zásob, které se nacházejí pod dimenzí umístění. Odeberte neplatné rozměry z řádku objednávky.

## <a name="resolution"></a>Řešení

Produkt bohužel nepodporuje zpracování nákladu pro proces vrácení prodeje. Proto nemůžete uvolnit objednávku prodejní vratky do skladu.

V transakcích prodejní objednávky nemůžete odkazovat na dimenze zásob, které se nacházejí pod dimenzí **umístění** v hierarchii rezervací. Řešením je odebrání neplatných rozměrů z řádku objednávky.
