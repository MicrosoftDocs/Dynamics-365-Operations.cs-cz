---
title: Nelze vytvořit prostředí v centru pro správu Power Apps
description: Toto téma vysvětluje, jak postupovat, když správce nemůže vytvořit prostředí v centru pro správu Microsoft Power Apps.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5923c59ab5dde13fed0483972e76634031404fd8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773212"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Nelze vytvořit prostředí v centru pro správu Power Apps

[!include [banner](includes/banner.md)]

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
2. Vytvořte prostředí podle pokynů v části [Zřízení aplikace Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).
