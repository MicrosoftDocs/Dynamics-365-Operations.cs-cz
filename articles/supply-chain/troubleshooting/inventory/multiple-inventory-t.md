---
title: Více skladových transakcí pro čísla šarží, když je zakázána fyzická aktualizace
description: Po úpravě řádku nákupní objednávky u položek, kde je možnost Při fyzické aktualizaci skupiny čísel dávek nastavena na Ne, se vytvoří více transakcí zásob.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026351"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a>Více skladových transakcí pro čísla šarží, když je zakázána fyzická aktualizace

Číslo článku znalostní báze: 4613390

## <a name="symptoms"></a>Příznaky

Po úpravě řádku nákupní objednávky u položek, kde je možnost **Při fyzické aktualizaci** skupiny čísel dávek nastavena na *Ne*, se vytvoří více transakcí zásob.

Když vytvoříte položku, kde je volba **Při fyzické aktualizaci** skupiny čísel šarží nastavena na *Ne*, systém automaticky vytvoří nové číslo šarže, pokud upravíte množství řádku nákupu a uložíte stránku nákupní objednávky.

## <a name="resolution"></a>Rozlišení

Nastavení **Při fyzické aktualizaci** pro skupiny čísel šarží funguje následujícím způsobem:

- Když je tato volba nastavena na *Ano*, nová čísla šarží se vytvoří až po fyzické aktualizaci (například při odeslání nebo přijetí zboží).
- Když je tato volba nastavena na *Ne*, nové číslo šarže se vytvoří pokaždé, když dojde k příslušné aktualizaci (například při přidání nového množství k nákupní objednávce).
