---
title: Převedení asynchronních zákazníků na synchronní zákazníky
description: Tento článek vysvětluje, jak převést asynchronní zákazníky na synchronní zákazníky v Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 0ce4906816deab8824b1079a34489e55651c0e03
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884384"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>Převedení asynchronních zákazníků na synchronní zákazníky

[!include [banner](includes/banner.md)]

Tento článek vysvětluje, jak převést asynchronní zákazníky na synchronní zákazníky v Microsoft Dynamics 365 Commerce.

Chcete-li převést asynchronní zákazníky na synchronní zákazníky, postupujte následovně.

1. V ústředí Commerce spusťte **P-úlohu** poslat asynchronní zákazníky do ústředí Commerce.
1. Spusťte úlohu **Synchronizovat zákazníky a obchodní partnery z asynchronního režimu** k vytvoření ID zákaznického účtu. (Tato úloha se dříve jmenovala **Synchronizovat zákazníky a obchodní partnery z asynchronního režimu**.)
1. Spusťte úlohu **1010** k synchronizaci nových ID zákaznických účtů s kanály.

Pokud objednávka odkazuje na asynchronního zákazníka nebo adresu, která ještě nebyla synchronizována s centrálou Commerce, bude zákazník nebo adresa synchronizována jako součást dávkové úlohy **Synchronizovat objednávky**. Pokud transakce typu cash-and-carry odkazuje na asynchronního zákazníka nebo adresu, bude zákazník nebo adresa synchronizována před odesláním na konci dne (EOD).

## <a name="additional-resources"></a>Další prostředky

[Správa zákazníků v obchodech](customer-mgmt-stores.md)

[Asynchronní režim vytváření zákazníka](async-customer-mode.md)

[Atributy odběratele](dev-itpro/customer-attributes.md)

[Vyloučení dat offline](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
