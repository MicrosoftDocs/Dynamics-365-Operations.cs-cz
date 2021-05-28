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
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026344"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a>Hlavní plánování generuje plánované objednávky pro demonstrační produkty

Číslo článku znalostní báze: 4614729

## <a name="symptoms"></a>Příznaky

Plánované objednávky se generují po spuštění hlavního plánování.

## <a name="resolution"></a>Rozlišení

Nastavení možnosti **Demonstrační** pro vydané produkty určuje výchozí typ řádku na kusovníku (BOM). Když je možnost **Demonstrační** je nastavena na *Ano*, systém bude i nadále vytvářet plánované objednávky pro položku, ale možnost **Přímo odvozený požadavek** pro každou plánovanou objednávku bude nastavena na *Ano*. Proto nelze plánovanou výrobní zakázku zpracovat samostatně. Místo toho bude vždy automaticky zahrnut, když je nadřazená výrobní zakázka spuštěna. Řádky kusovníku plánované demonstrační objednávky budou navíc zahrnuty do kusovníku nadřazené výrobní zakázky.
