---
title: "Uživatel má přístup k aplikaci Core HR, ale nikoliv k aplikacím Onboard nebo Attract"
description: "Toto téma vysvětluje, jak vyřešit problém, kdy má uživatel přístup k aplikaci Microsoft Dynamics 365 for Talent Core HR, nikoliv však k aplikacím Attract nebo Onboard."
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
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.contentlocale: cs-cz
ms.lasthandoff: 12/04/2018

---

# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="a84ec-103">Uživatel má přístup k aplikaci Core HR, ale nikoliv k aplikacím Onboard nebo Attract</span><span class="sxs-lookup"><span data-stu-id="a84ec-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a84ec-104">**Podrobnosti o prostředí**</span><span class="sxs-lookup"><span data-stu-id="a84ec-104">**Environment details**</span></span>

- <span data-ttu-id="a84ec-105">Nasazení služeb Microsoft Dynamics Lifecycle Services bylo provedeno uživatelem A.</span><span class="sxs-lookup"><span data-stu-id="a84ec-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="a84ec-106">Uživatel A přidal uživatele B jako uživatele do aplikace Microsoft Dynamics 365 for Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="a84ec-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="a84ec-107">**Problém**</span><span class="sxs-lookup"><span data-stu-id="a84ec-107">**Issue**</span></span>

<span data-ttu-id="a84ec-108">Uživatel B má přístup do Core HR, ale nedostane se do aplikací Talent: Attract nebo Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="a84ec-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="a84ec-109">Pokud se uživatel pokusí přejít na **Vyzkoušení aplikací**, je zaveden místo toho do zkušebního prostředí.</span><span class="sxs-lookup"><span data-stu-id="a84ec-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="a84ec-110">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="a84ec-110">**Solution**</span></span>

<span data-ttu-id="a84ec-111">Uživatel B musí být přiřazena oprávnění k zobrazení prostředí Microsoft PowerApps, které vytvořil uživatel A během procesu zřizování.</span><span class="sxs-lookup"><span data-stu-id="a84ec-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="a84ec-112">Informace naleznete v části Zřízení přístupu k prostředí v tématu [Zřízení aplikace Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="a84ec-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="a84ec-113">**Dlouhodobé řešení**</span><span class="sxs-lookup"><span data-stu-id="a84ec-113">**Long-term solution**</span></span>

<span data-ttu-id="a84ec-114">Společnost Microsoft zvažuje automatické přiřazení příslušných práv k aplikacím Onboard a Attract, když je uživatel přidán do Core HR.</span><span class="sxs-lookup"><span data-stu-id="a84ec-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>

