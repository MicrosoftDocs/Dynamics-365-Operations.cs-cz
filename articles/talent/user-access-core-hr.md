---
title: Uživatel má přístup k Human Resources, ale nikoliv k aplikacím Onboard nebo Attract
description: Toto téma vysvětluje, jak vyřešit problém, kdy má uživatel přístup k aplikaci Microsoft Dynamics 365 Talent - Human Resources, nikoliv však k aplikacím Attract nebo Onboard.
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460550"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a><span data-ttu-id="5c802-103">Uživatel má přístup k Human Resources, ale nikoliv k aplikacím Onboard nebo Attract</span><span class="sxs-lookup"><span data-stu-id="5c802-103">User can access Human Resources but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5c802-104">**Podrobnosti o prostředí**</span><span class="sxs-lookup"><span data-stu-id="5c802-104">**Environment details**</span></span>

- <span data-ttu-id="5c802-105">Nasazení služeb Microsoft Dynamics Lifecycle Services bylo provedeno uživatelem A.</span><span class="sxs-lookup"><span data-stu-id="5c802-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="5c802-106">Uživatel A přidal uživatele B jako uživatele do aplikace Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5c802-106">User A added user B as a user to Microsoft Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="5c802-107">**Vydání**</span><span class="sxs-lookup"><span data-stu-id="5c802-107">**Issue**</span></span>

<span data-ttu-id="5c802-108">Uživatel B má přístup do Human Resources, ale nedostane se do aplikací Talent: Attract nebo Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="5c802-108">User B can access Human Resources, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="5c802-109">Pokud se uživatel pokusí přejít na **Vyzkoušení aplikací**, je zaveden místo toho do zkušebního prostředí.</span><span class="sxs-lookup"><span data-stu-id="5c802-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="5c802-110">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="5c802-110">**Solution**</span></span>

<span data-ttu-id="5c802-111">Uživatel B musí být přiřazena oprávnění k zobrazení prostředí Microsoft Power Apps, které vytvořil uživatel A během procesu zřizování.</span><span class="sxs-lookup"><span data-stu-id="5c802-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="5c802-112">Informace naleznete v části Zřízení přístupu k prostředí v tématu [Zřízení aplikace Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="5c802-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="5c802-113">**Dlouhodobé řešení**</span><span class="sxs-lookup"><span data-stu-id="5c802-113">**Long-term solution**</span></span>

<span data-ttu-id="5c802-114">Společnost Microsoft zvažuje automatické přiřazení příslušných práv k aplikacím Onboard a Attract, když je uživatel přidán do Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5c802-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Human Resources.</span></span>
