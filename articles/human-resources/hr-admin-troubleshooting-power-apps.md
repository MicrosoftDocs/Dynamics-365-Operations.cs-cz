---
title: Nelze vytvořit prostředí v centru pro správu Power Apps
description: Tento článek vysvětluje, jak postupovat, když správce nemůže vytvořit prostředí v centru pro správu Microsoft Power Apps.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cc62d3c8fe560d4f7d2e754a79de6fec3ef6041b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882917"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Nelze vytvořit prostředí v centru pro správu Power Apps


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Vydání**

- Správce klienta/prostředí nemůže vytvořit prostředí v centru pro správu Microsoft Power Apps.
- Uživatel nemá licenci, která dává právo vytvářet prostředí.

**Řešení**

Ujistěte se, že správce tenanta přidělil platnou licenci Power Apps P2 pro uživatele vytvářejícího prostředí. Následující plány služeb Microsoft Dynamics poskytují oprávnění k vytváření prostředí:

| Celkové skladová jednotka zásob produktu (SKU)       | Servisní plán Power Apps P2  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps for Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | Power Apps for Dynamics 365 |

Všimněte si, že různé skladové jednotky aplikace Microsoft Office také poskytují toto právo, společně se samostatnými SKU Power Apps plánu 2. Důležité je, že jedna z těchto skladových jednotek zásob musí být přítomná.

1. Přejděte na [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Vytvořte prostředí podle pokynů v části [Zřízení Human Resources](/dynamics365/unified-operations/talent/provisioning-talent).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
