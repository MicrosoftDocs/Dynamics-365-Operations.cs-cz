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
ms.openlocfilehash: fbe0e8acc1b879e4d7982b33413236432f25f630
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431031"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="2f8ae-103">Přístup k soukromým adresám podle role zabezpečení</span><span class="sxs-lookup"><span data-stu-id="2f8ae-103">Access to private addresses by security role</span></span>

<span data-ttu-id="2f8ae-104">**Problém**</span><span class="sxs-lookup"><span data-stu-id="2f8ae-104">**Issue**</span></span>

<span data-ttu-id="2f8ae-105">Poté, co zákazník duplikuje roli zabezpečení a přihlásí se s touto novou rolí, nemůže vidět adresy označené jako soukromé.</span><span class="sxs-lookup"><span data-stu-id="2f8ae-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="2f8ae-106">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="2f8ae-106">**Resolution**</span></span>

<span data-ttu-id="2f8ae-107">Chcete-li vyřešit tento problém, zákazník musí postupovat podle těchto kroku pro duplikovanou roli zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="2f8ae-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="2f8ae-108">Přejděte do nabídky **Správa organizace \> Globální adresář \> Parametry globálního adresáře**.</span><span class="sxs-lookup"><span data-stu-id="2f8ae-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="2f8ae-109">Na kartě **Zabezpečení soukromého umístění** přesuňte novou roli zabezpečení ze seznamu **Dostupné role** do seznamu **Vybrané role**.</span><span class="sxs-lookup"><span data-stu-id="2f8ae-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="2f8ae-110">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="2f8ae-110">Select **Save**.</span></span>

![Stránka parametrů globálního adresáře](media/GAD-parameters.png)
