---
title: Hlavní plánování generuje plánované objednávky pro demonstrační produkty
description: Plánované objednávky se generují po spuštění hlavního plánování.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f3170bcb723e2d7483258bb0ecf786e62f2aa3d196745074c2ac554bc212ec55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741997"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>Hlavní plánování generuje plánované objednávky pro demonstrační produkty

Číslo článku znalostní báze: 4614729

## <a name="symptoms"></a>Příznaky

Plánované objednávky se generují po spuštění hlavního plánování.

## <a name="resolution"></a>Rozlišení

Nastavení možnosti **Demonstrační** pro vydané produkty určuje výchozí typ řádku na kusovníku (BOM). Když je možnost **Demonstrační** je nastavena na *Ano*, systém bude i nadále vytvářet plánované objednávky pro položku, ale možnost **Přímo odvozený požadavek** pro každou plánovanou objednávku bude nastavena na *Ano*. Proto nelze plánovanou výrobní zakázku zpracovat samostatně. Místo toho bude vždy automaticky zahrnut, když je nadřazená výrobní zakázka spuštěna. Řádky kusovníku plánované demonstrační objednávky budou navíc zahrnuty do kusovníku nadřazené výrobní zakázky.
