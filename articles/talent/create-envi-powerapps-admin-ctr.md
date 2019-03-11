---
title: Nelze vytvořit prostředí v centru pro správu PowerApps
description: Toto téma vysvětluje, jak postupovat, když správce nemůže vytvořit prostředí v centru pro správu Microsoft PowerApps.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "303633"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a>Nelze vytvořit prostředí v centru pro správu PowerApps

[!include [banner](includes/banner.md)]

**Problém**

- Správce klienta/prostředí nemůže vytvořit prostředí v centru pro správu Microsoft PowerApps.
- Licence, která uživateli poskytuje právo provádět krok vytváření prostředí, nebyla přiřazena přímo uživateli, který provádí tento krok.

**Řešení**

Ujistěte se, že správce klienta přidělil platnou licenci PowerApps P2 přímo uživateli, který provede krok vytvoření prostředí. Zde jsou servisní plány Microsoft Dynamics, které poskytují toto právo.

| Celkové skladová jednotka zásob produktu (SKU)       | Servisní plán PowerApps P2  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | PowerApps pro Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | PowerApps pro Dynamics 365 |

Všimněte si, že různé skladové jednotky aplikace Microsoft Office také poskytují toto právo, společně se samostatnými SKU PowerApps Plan 2 Důležité je, že jedna z těchto skladových jednotek zásob musí být přítomná.

1. Přejděte na [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Vytvořte prostředí podle pokynů v části [Zřízení aplikace Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).
