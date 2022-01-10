---
title: Systém nemůže najít plánovanou objednávku během operací s více zakázkami
description: K chybě „Plánovaná objednávka neexistuje“ dochází, když provádíte operace s více plánovanými objednávkami a alespoň dvě objednávky patří ke stejnému ID položky.
author: t-benebo
ms.date: 12/07/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo_ReqTransPoMarkChangeType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-12-07
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0ece4a331b63b86e896c5b337a58185ed3ea1049
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920793"
---
# <a name="the-system-cant-find-a-planned-order-during-operations-on-multiple-orders"></a>Systém nemůže najít plánovanou objednávku během operací s více zakázkami

Kód chyby: SYS24774

## <a name="symptoms"></a>Příznaky

Následující chybová zpráva se zobrazí, když se pokusíte provést operaci na více plánovaných objednávkách současně a alespoň dvě z objednávek patří ke stejnému ID položky. K chybě může například dojít, když jsou objednávky potvrzeny nebo se změní jejich typ.

> Plánovaná objednávka %1 neexistuje.

## <a name="cause"></a>Příčina

Když systém potvrdí nebo změní typ objednávky, musí přehodnotit existující plánované objednávky pro danou položku, aby se ujistil, že plánovaná nabídka odpovídá poptávce a existující nabídce. V rámci tohoto procesu systém znovu vytvoří plánované objednávky pro položku. Druhá plánovaná objednávka, jejíž zpracování systém předpokládá, proto již neexistuje.

## <a name="workaround"></a>Alternativní řešení

Schvalujte objednávky před jejich zpracováním. Tímto způsobem nebudou objednávky odstraněny, když systém zpracuje první objednávku položky.
