---
title: Přístup k soukromým adresám podle role zabezpečení
description: Tento článek vysvětluje, jak vyřešit problém, pokud zákazník nemá přístup k soukromým adresám.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
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
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: facfd17f007b2c9e6f068d0ec4c5ce45b85a1b78
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008378"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="45a0e-103">Přístup k soukromým adresám podle role zabezpečení</span><span class="sxs-lookup"><span data-stu-id="45a0e-103">Access to private addresses by security role</span></span>

<span data-ttu-id="45a0e-104">**Problém**</span><span class="sxs-lookup"><span data-stu-id="45a0e-104">**Issue**</span></span>

<span data-ttu-id="45a0e-105">Poté, co zákazník duplikuje roli zabezpečení a přihlásí se s touto novou rolí, nemůže vidět adresy označené jako soukromé.</span><span class="sxs-lookup"><span data-stu-id="45a0e-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="45a0e-106">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="45a0e-106">**Resolution**</span></span>

<span data-ttu-id="45a0e-107">Chcete-li vyřešit tento problém, zákazník musí postupovat podle těchto kroku pro duplikovanou roli zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="45a0e-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="45a0e-108">Přejděte do nabídky **Správa organizace \> Globální adresář \> Parametry globálního adresáře**.</span><span class="sxs-lookup"><span data-stu-id="45a0e-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="45a0e-109">Na kartě **Zabezpečení soukromého umístění** přesuňte novou roli zabezpečení ze seznamu **Dostupné role** do seznamu **Vybrané role**.</span><span class="sxs-lookup"><span data-stu-id="45a0e-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="45a0e-110">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="45a0e-110">Select **Save**.</span></span>

![Stránka parametrů globálního adresáře](media/GAD-parameters.png)
