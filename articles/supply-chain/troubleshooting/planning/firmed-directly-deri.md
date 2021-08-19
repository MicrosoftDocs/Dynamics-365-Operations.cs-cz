---
title: Přímo odvozené potvrzené objednávky jsou zpracovávány v rámci workflow kontroly
description: Přímo odvozené potvrzené objednávky jsou zpracovávány workflow, který má stav Probíhá kontrola.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d20f1c1d6e8fc83dd996b04bf0321a41f7b39290f306d1ac9f4fcd17514832e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721168"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>Přímo odvozené potvrzené objednávky jsou zpracovávány v rámci workflow kontroly

Číslo článku znalostní báze: 4612450

## <a name="symptoms"></a>Příznaky

Přímo odvozené potvrzené objednávky jsou zpracovávány workflow, který má stav *Probíhá kontrola*.

## <a name="resolution"></a>Rozlišení

Když je povoleno sledování změn, bude potvrzeným odvozeným objednávkám (dílčí nákupní objednávky) přidělen stav *Probíhá kontrola*. Pokud je tedy nákupní objednávka odvozena (nákupní objednávka na subdodávku), odešle se pouze do pracovního postupu. Pokud je nákupní objednávka pevně plánovanou nákupní objednávkou, je automaticky schválena, aby bylo zajištěno, že plánovací modul nevytvoří nové plánované objednávky, dokud je nákupní objednávka stále ve stavu *Koncept*.
