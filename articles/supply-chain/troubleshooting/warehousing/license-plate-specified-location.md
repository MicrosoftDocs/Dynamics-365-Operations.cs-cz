---
title: Pro toto skladové místo musí být zadána registrační značka
description: Pokud se vám tato chyba zobrazí po vytvoření objednávky přenosu pro sklad s povolením WMS, pole Výchozí umístění příjmu pro přechodový sklad je prázdné.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2e562ad2b41dd149f215adc83bd2d54e55dccc05
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475763"
---
# <a name="license-plate-specification-error-when-confirming-shipment-for-a-transfer-order"></a>Chyba specifikace registrační značky při potvrzování zásilky pro převodní příkaz

## <a name="symptoms"></a>Příznaky

Pokud vytvoříte převodní příkaz pomocí skladu, který je povolen pro pokročilou správu skladu (WMS), a po dokončení práce se pokusíte potvrdit zásilku, může se zobrazit následující chybová zpráva.

> Pro toto skladové místo musí být zadána registrační značka.

## <a name="cause"></a>Příčina

K této chybě dochází, protože je pole **Výchozí skladové místo příjmu** prázdné pro tranzitní sklad ze skladu.

## <a name="resolution"></a>Řešení

Chcete-li tento problém vyřešit, zadejte výchozí skladové místo příjmu v tranzitním skladu. Ujistěte se, že toto umístění je řízeno registrační značkou.
