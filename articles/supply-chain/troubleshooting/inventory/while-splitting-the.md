---
title: Pokud je množství hmotnosti úlovku rozděleno, použije se místo nominálního množství minimální množství
description: Když je množství hmotnosti úlovku rozděleno do dávek, používá pole Vyskladněné množství minimální množství, které je pro položku nastaveno, nikoli nominální množství.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026346"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a>Pokud je množství hmotnosti úlovku rozděleno, použije se místo nominálního množství minimální množství

Číslo článku znalostní báze: 4612073

## <a name="symptoms"></a>Příznaky

Když je množství hmotnosti úlovku rozděleno do dávek, používá pole **Vyskladněné množství** minimální množství, které je pro položku nastaveno, nikoli nominální množství.

## <a name="resolution"></a>Rozlišení

Systém se chová tak, jak byl navržen. Systém používá k vychystávání nastavení minimálního množství každé položky.
