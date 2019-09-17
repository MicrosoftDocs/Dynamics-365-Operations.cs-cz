---
title: Uživatel má přístup k aplikaci Core HR, ale nikoliv k aplikacím Onboard nebo Attract
description: Toto téma vysvětluje, jak vyřešit problém, kdy má uživatel přístup k aplikaci Dynamics 365 for Talent Core HR, nikoliv však k aplikacím Attract nebo Onboard.
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
ms.openlocfilehash: 6fc27a4c137fef2f8d204d90366c316389da08e6
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741703"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="b45ec-103">Uživatel má přístup k Core HR, ale nikoliv k aplikacím Onboard nebo Attract</span><span class="sxs-lookup"><span data-stu-id="b45ec-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b45ec-104">**Podrobnosti o prostředí**</span><span class="sxs-lookup"><span data-stu-id="b45ec-104">**Environment details**</span></span>

- <span data-ttu-id="b45ec-105">Nasazení služeb Microsoft Dynamics Lifecycle Services bylo provedeno uživatelem A.</span><span class="sxs-lookup"><span data-stu-id="b45ec-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="b45ec-106">Uživatel A přidal uživatele B jako uživatele do aplikace Microsoft Dynamics 365 for Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="b45ec-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="b45ec-107">**Výdej**</span><span class="sxs-lookup"><span data-stu-id="b45ec-107">**Issue**</span></span>

<span data-ttu-id="b45ec-108">Uživatel B má přístup do Core HR, ale nedostane se do aplikací Talent: Attract nebo Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="b45ec-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="b45ec-109">Pokud se uživatel pokusí přejít na **Vyzkoušení aplikací**, je zaveden místo toho do zkušebního prostředí.</span><span class="sxs-lookup"><span data-stu-id="b45ec-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="b45ec-110">**Řešení**</span><span class="sxs-lookup"><span data-stu-id="b45ec-110">**Solution**</span></span>

<span data-ttu-id="b45ec-111">Uživatel B musí být přiřazena oprávnění k zobrazení prostředí Microsoft PowerApps, které vytvořil uživatel A během procesu zřizování.</span><span class="sxs-lookup"><span data-stu-id="b45ec-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="b45ec-112">Informace naleznete v části Zřízení přístupu k prostředí v tématu [Zřízení aplikace Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span><span class="sxs-lookup"><span data-stu-id="b45ec-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="b45ec-113">**Dlouhodobé řešení**</span><span class="sxs-lookup"><span data-stu-id="b45ec-113">**Long-term solution**</span></span>

<span data-ttu-id="b45ec-114">Společnost Microsoft zvažuje automatické přiřazení příslušných práv k aplikacím Onboard a Attract, když je uživatel přidán do Core HR.</span><span class="sxs-lookup"><span data-stu-id="b45ec-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
