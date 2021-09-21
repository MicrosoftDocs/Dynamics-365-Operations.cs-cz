---
title: Umístění dimenze nemůže být prázdné, pokud je nastaveno sériové číslo
description: Pokud se vám tato chyba zobrazí při potvrzování zásilky po vytvoření objednávky přenosu pro sériovou položku, pole Výchozí umístění příjmu je prázdné.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6f58c72438d5d1d93e59e46525debd65d44d9a76
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475832"
---
# <a name="error-when-confirming-shipment-after-creating-a-transfer-order-for-a-serial-item"></a>Chyba při potvrzování dodávky po vytvoření převodního příkazu pro sériové zboží

## <a name="symptoms"></a>Příznaky

Pokud vytvoříte převodní příkaz pro sériovou položku pomocí skladu, který je povolen pro pokročilou správu skladu (WMS), a po dokončení práce se pokusíte potvrdit zásilku, zobrazí se následující chybová zpráva:

> Umístění dimenze nemůže být prázdné, pokud je nastaveno sériové číslo dimenze.

## <a name="cause"></a>Příčina

K této chybě dochází, protože je pole **Výchozí skladové místo příjmu** prázdné pro tranzitní sklad ze skladu.

## <a name="resolution"></a>Řešení

Chcete-li tento problém vyřešit, zadejte výchozí skladové místo příjmu v tranzitním skladu. Ujistěte se, že toto umístění je řízeno registrační značkou.
