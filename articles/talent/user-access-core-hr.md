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
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006303"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a><span data-ttu-id="7d3e7-103">Uživatel má přístup k Human Resources, ale nikoliv k aplikacím Onboard nebo Attract</span><span class="sxs-lookup"><span data-stu-id="7d3e7-103">User can access Human Resources but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7d3e7-104">**Podrobnosti o prostředí**</span><span class="sxs-lookup"><span data-stu-id="7d3e7-104">**Environment details**</span></span>

- <span data-ttu-id="7d3e7-105">Nasazení služeb Microsoft Dynamics Lifecycle Services bylo provedeno uživatelem A.</span><span class="sxs-lookup"><span data-stu-id="7d3e7-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="7d3e7-106">Uživatel A přidal uživatele B jako uživatele do aplikace Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7d3e7-106">User A added user B as a user to Microsoft Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="7d3e7-107">**Vydání**</span><span class="sxs-lookup"><span data-stu-id="7d3e7-107">**Issue**</span></span>

<span data-ttu-id="7d3e7-108">Uživatel B má přístup do Human Resources, ale nedostane se do aplikací Talent: Attract nebo Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="7d3e7-108">User B can access Human Resources, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="7d3e7-109">Pokud se uživatel pokusí přejít na **Vyzkoušení aplikací**, je zaveden místo toho do zkušebního prostředí.</span><span class="sxs-lookup"><span data-stu-id="7d3e7-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="7d3e7-110">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="7d3e7-110">**Solution**</span></span>

<span data-ttu-id="7d3e7-111">Uživatel B musí být přiřazena oprávnění k zobrazení prostředí Microsoft Power Apps, které vytvořil uživatel A během procesu zřizování.</span><span class="sxs-lookup"><span data-stu-id="7d3e7-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="7d3e7-112">Informace naleznete v části Zřízení přístupu k prostředí v tématu [Zřízení aplikace Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="7d3e7-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="7d3e7-113">**Dlouhodobé řešení**</span><span class="sxs-lookup"><span data-stu-id="7d3e7-113">**Long-term solution**</span></span>

<span data-ttu-id="7d3e7-114">Společnost Microsoft zvažuje automatické přiřazení příslušných práv k aplikacím Onboard a Attract, když je uživatel přidán do Human Resources.</span><span class="sxs-lookup"><span data-stu-id="7d3e7-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Human Resources.</span></span>
