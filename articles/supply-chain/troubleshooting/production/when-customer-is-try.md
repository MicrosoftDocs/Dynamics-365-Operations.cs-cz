---
title: Číslo dávky se vymaže, když je vybráno nové ID dávky
description: Při kontrole řádku deníku výběrových seznamů se hodnota v poli Číslo dávky vymaže, pokud v poli ID dávky vyberete novou hodnotu.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026322"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>Číslo dávky se vymaže, když je vybráno nové ID dávky

Číslo článku znalostní báze: 4613107

## <a name="symptoms"></a>Příznaky

Při kontrole řádku deníku výběrových seznamů se hodnota v poli **Číslo dávky** vymaže, pokud v poli **ID dávky** vyberete novou hodnotu.

## <a name="resolution"></a>Rozlišení

Systém se chová tak, jak byl navržen. Pokud změníte ID dávky, změníte kontext položky. Proto je číslo dávky resetováno.

Chcete-li přidružit číslo dávky k ID dávky, musíte nejprve nastavit ID dávky.
