---
title: Nelze vytvořit prostředí v centru pro správu Power Apps
description: Tento článek vysvětluje, jak postupovat, když správce nemůže vytvořit prostředí v centru pro správu Microsoft Power Apps.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f4c75706183a3d6c961852395e464d46ba3ec1f2
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008322"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Nelze vytvořit prostředí v centru pro správu Power Apps

**Vydání**

- Správce klienta/prostředí nemůže vytvořit prostředí v centru pro správu Microsoft Power Apps.
- Licence, která uživateli poskytuje právo provádět krok vytváření prostředí, nebyla přiřazena přímo uživateli, který provádí tento krok.

**Řešení**

Ujistěte se, že správce klienta přidělil platnou licenci Power Apps P2 přímo uživateli, který provede krok vytvoření prostředí. Zde jsou servisní plány Microsoft Dynamics, které poskytují toto právo.

| Celkové skladová jednotka zásob produktu (SKU)       | Servisní plán Power Apps P2  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps for Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | Power Apps for Dynamics 365 |

Všimněte si, že různé skladové jednotky aplikace Microsoft Office také poskytují toto právo, společně se samostatnými SKU Power Apps plánu 2. Důležité je, že jedna z těchto skladových jednotek zásob musí být přítomná.

1. Přejděte na [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Vytvořte prostředí podle pokynů v části [Zřízení Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).