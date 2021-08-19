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
ms.openlocfilehash: 73ebc45ee83516f573c3f73ef8106da9ae44c590c05d8dbd08520bc5ef19e49a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714203"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a>Obrácení hlášení po dokončení vytvoří neočekávanou otevřenou transakci

Číslo článku znalostní báze: 4612469

## <a name="symptoms"></a>Příznaky

Pokud převrátíte hlášení jako dokončené, které má označení, systém vytvoří otevřenou transakci, kde má převrácené množství stejné rozměry zásob jako převrácená transakce, která byla stornována.

## <a name="resolution"></a>Rozlišení

Když obrátíte operaci sestavy jako hotovou, dimenze zásob se inicializuje z výrobního deníku. Proto je číslo dávky získáno. Kvůli označení zdědí transakce prodejní objednávky číslo dávky.

Dimenzi lze resetovat, když se zaúčtuje hlášení po dokončení.
