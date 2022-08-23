---
title: Převedení asynchronních zákazníků na synchronní zákazníky
description: Tento článek vysvětluje, jak převést asynchronní zákazníky na synchronní zákazníky v Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: b442bfc0685706359771e4d9e2729565d3652a60
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278185"
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
