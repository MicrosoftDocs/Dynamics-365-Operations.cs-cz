---
title: Schválit plánované objednávky
description: Tohle téma popisuje schválení plánovaných objednávek, které jsou podporovány optimalizací plánování.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b7975088be898ccecceb1f7be009cecff107f6e6
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759681"
---
# <a name="approve-planned-orders"></a>Schválit plánované objednávky

[!include [banner](../../includes/banner.md)]

Tohle téma poskytuje informace, jak aktualizovat stav plánovaných objednávek v optimalizaci plánování.

Schválení plánovaných objednávek je volitelným krokem na cestě k vytvoření potvrzené objednávky z plánované objednávky. Doporučujeme schválit změněné plánované objednávky, jinak budou úpravy ignorovány a přepsány při dalším běhu plánování.

![Tok plánované objednávky](media/approved-planned-orders-1.png)

Pole **Stav** vám pomůže zvládnout váš postup využitím následujících hodnot:

- **Nezpracováno:** Když hlavní plánování vytvoří naplánované objednávky, mají stav *Nezpracováno*. Plánované objednávky s tímto stavem budou odstraněny během dalšího běhu plánování.
- **Dokončeno:** Pokud se rozhodnete nepotvrdit plánovanou objednávku, můžete změnit stav na *Dokončeno* k označení, že jste dokončili vyhodnocení této plánované objednávky. Mějte na paměti, že se stavy *Nezpracováno* a *Dokončeno* systém zachází stejně.
- **Schváleno:** Chcete-li zachovat úpravy nebo plánujete potvrdit plánovanou objednávku, změňte stav na *Schváleno* . Plánované objednávky se stavem *Schváleno* jsou hlavním plánováním považovány za fixní a očekávané dodávky, takže nebudou během pozdějších běhů hlavního plánování změněny ani odstraněny. Pro dosažení tohoto cíle logika plánování zkopíruje *schválené* plánované objednávky z původní verze plánu do nové verze plánu během hlavního plánování. Pamatujte si, že plánované objednávky ve stavu *Schváleno* jsou považovány za dodávky v rámci konkrétního hlavního plánu.

Naplánované objednávky lze spravovat v pracovním prostoru **Hlavní plánování**, na seznamu **Plánovaná objednávka** nebo na seznamech **Plánované výrobní zakázky**, **Plánované nákupní objednávky** a **Plánovaný převod**.
