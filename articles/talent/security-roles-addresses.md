---
title: "Přístup k soukromým adresám podle role zabezpečení"
description: "Toto téma vysvětluje, jak vyřešit problém, pokud zákazník nemá přístup k soukromým adresám."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: c1c1c3ce1233408e73d177f9e04f1137f3171a49
ms.contentlocale: cs-cz
ms.lasthandoff: 12/04/2018

---

# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="da13c-103">Přístup k soukromým adresám podle role zabezpečení</span><span class="sxs-lookup"><span data-stu-id="da13c-103">Access to private addresses by security role</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="da13c-104">**Problém**</span><span class="sxs-lookup"><span data-stu-id="da13c-104">**Issue**</span></span>

<span data-ttu-id="da13c-105">Poté, co zákazník duplikuje roli zabezpečení a přihlásí se s touto novou rolí, nemůže vidět adresy označené jako soukromé.</span><span class="sxs-lookup"><span data-stu-id="da13c-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="da13c-106">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="da13c-106">**Resolution**</span></span>

<span data-ttu-id="da13c-107">Chcete-li vyřešit tento problém, zákazník musí postupovat podle těchto kroku pro duplikovanou roli zabezpečení.</span><span class="sxs-lookup"><span data-stu-id="da13c-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="da13c-108">Přejděte do nabídky **Správa organizace \> Globální adresář \> Parametry globálního adresáře**.</span><span class="sxs-lookup"><span data-stu-id="da13c-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="da13c-109">Na kartě **Zabezpečení soukromého umístění** přesuňte novou roli zabezpečení ze seznamu **Dostupné role** do seznamu **Vybrané role**.</span><span class="sxs-lookup"><span data-stu-id="da13c-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="da13c-110">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="da13c-110">Select **Save**.</span></span>

![Stránka parametrů globálního adresáře](media/GAD-parameters.png)

