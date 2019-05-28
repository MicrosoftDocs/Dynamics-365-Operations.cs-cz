---
title: Nelze vytvořit prostředí v centru pro správu PowerApps
description: Toto téma vysvětluje, jak postupovat, když správce nemůže vytvořit prostředí v centru pro správu Microsoft PowerApps.
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
ms.openlocfilehash: 97d44dc034cb8097fc0ecf9ac4e485425f097102
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517481"
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
