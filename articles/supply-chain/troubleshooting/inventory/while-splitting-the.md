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
ms.openlocfilehash: 424ad46281612f6a3e8cb4c90478a39f757d5416c3ce1d77ed6ff6dba7b20dcb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723448"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a>Pokud je množství hmotnosti úlovku rozděleno, použije se místo nominálního množství minimální množství

Číslo článku znalostní báze: 4612073

## <a name="symptoms"></a>Příznaky

Když je množství hmotnosti úlovku rozděleno do dávek, používá pole **Vyskladněné množství** minimální množství, které je pro položku nastaveno, nikoli nominální množství.

## <a name="resolution"></a>Rozlišení

Systém se chová tak, jak byl navržen. Systém používá k vychystávání nastavení minimálního množství každé položky.
