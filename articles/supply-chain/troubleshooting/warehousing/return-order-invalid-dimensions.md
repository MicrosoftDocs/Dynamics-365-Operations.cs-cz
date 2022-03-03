---
title: Nelze vytvořit řádek vytížení z důvodu neplatných dimenzí zásob
description: Při pokusu o vydání zpětné prodejní objednávky do skladu se může zobrazit chyba ohledně neplatných dimenzí zásob. Odstraňte je z řádku objednávky.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b02408b61b07b272a7e7d52004dc2492d60ef28c
ms.sourcegitcommit: 0d14c4a1e6cf533dd20463f1a84eae8f6d88f71b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/14/2022
ms.locfileid: "8119205"
---
# <a name="cant-create-load-line-for-return-sales-order-due-to-invalid-inventory-dimensions"></a>Nelze vytvořit řádek vytížení pro vratku prodejní objednávky z důvodu neplatných dimenzí zásob

## <a name="symptoms"></a>Příznaky

Při pokusu o uvolnění objednávky prodejní vratky do skladu se může zobrazit následující chybová zpráva:

> Nelze vytvořit řádek nákladu pro tento řádek objednávky, protože obsahuje neplatné dimenze inventáře. V hierarchii rezervací nemůžete odkazovat na dimenze zásob, které se nacházejí pod dimenzí umístění. Odeberte neplatné rozměry z řádku objednávky.

## <a name="resolution"></a>Řešení

Produkt bohužel nepodporuje zpracování nákladu pro proces vrácení prodeje. Proto nemůžete uvolnit objednávku prodejní vratky do skladu.

V transakcích prodejní objednávky nemůžete odkazovat na dimenze zásob, které se nacházejí pod dimenzí **umístění** v hierarchii rezervací. Řešením je odebrání neplatných rozměrů z řádku objednávky.
