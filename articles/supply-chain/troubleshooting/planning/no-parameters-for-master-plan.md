---
title: Parametry pro hlavní plán neexistují
description: Při pokusu o potvrzení plánované objednávky se zobrazí chybová zpráva s oznámením, že pro hlavní plán neexistují žádné parametry.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d039b79684f87e7791fb9dae7cbdc6ced220bc092d9a0ab624616c1c345986da
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756768"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a>Parametry pro hlavní plán neexistují

Kód chyby: SYS25368

## <a name="symptoms"></a>Příznaky

Když se pokusíte potvrdit objednávku, zobrazí se následující chybová zpráva:

> Parametry hlavního plánu %1 neexistují.

## <a name="cause"></a>Příčina

Z důvodu problémů s konfigurací systém nemůže najít nastavení pro zadaný plán.

## <a name="resolution"></a>Řešení

- Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány** a ujistěte se, že plán, který má zadaný název, existuje.
