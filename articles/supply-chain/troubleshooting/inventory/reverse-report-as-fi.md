---
title: Obrácení hlášení po dokončení vytvoří neočekávanou otevřenou transakci
description: Převrácení hlášení jako dokončeného, které má označení, vytvoří otevřenou transakci, kde má převrácené množství stejné rozměry zásob jako převrácené transakce.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026349"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>Obrácení hlášení po dokončení vytvoří neočekávanou otevřenou transakci

Číslo článku znalostní báze: 4612469

## <a name="symptoms"></a>Příznaky

Pokud převrátíte hlášení jako dokončené, které má označení, systém vytvoří otevřenou transakci, kde má převrácené množství stejné rozměry zásob jako převrácená transakce, která byla stornována.

## <a name="resolution"></a>Rozlišení

Když obrátíte operaci sestavy jako hotovou, dimenze zásob se inicializuje z výrobního deníku. Proto je číslo dávky získáno. Kvůli označení zdědí transakce prodejní objednávky číslo dávky.

Dimenzi lze resetovat, když se zaúčtuje hlášení po dokončení.
