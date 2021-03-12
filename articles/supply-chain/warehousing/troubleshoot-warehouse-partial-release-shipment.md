---
title: Odstraňování potíží s částečným uvolněním a částečnou dodávkou
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s příchozími s částečným uvolněním a částečnými dodávkami v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 33323a8aed44cf19db6c2c937abcb09f7e05b6c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993932"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a>Odstraňování potíží s částečným uvolněním a částečnou dodávkou

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při práci s příchozími s částečným uvolněním a částečnými dodávkami v Microsoft Dynamics 365 Supply Chain Management.

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Stav uvolnění prodejní objednávky zůstává Částečně uvolněn i po fakturaci prodejní objednávky.

### <a name="issue-description"></a>Popis problému

Prodejní objednávka je objednávka dodání, ale jedna nebo více položek v ní má jiný způsob dodání. Po fakturaci objednávky má stále stav uvolnění *Částečně uvolněn*.

Například prodejní objednávka má dvě položky: jednu pro doručení a druhou pro vyzvednutí. Dodání i vyzvednutí byly provedeny. Proto byly oba řádky fakturovány. Stav uvolnění se však stále zobrazuje jako *Částečně uvolněno*, což je zavádějící.

### <a name="issue-resolution"></a>Řešení problému

Stav uvolnění se vztahuje pouze na řádky objednávky, kde jsou položky povoleny pro správu skladu. Stav uvolnění proto zůstává *Částečně uvolněno* v tomto scénáři. Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí. Jako součást procesu dodacího listu a procesu fakturace bylo možné přidat rozšíření pro aktualizaci stavu uvolnění.
