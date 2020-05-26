---
title: Poradce při potížích souvisejících s připraveností řešení
description: Toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s připraveností řešení.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 013e37269ec3df2bede15b28cffcc175967de9a3
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172614"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="dc861-103">Poradce při potížích souvisejících s připraveností řešení</span><span class="sxs-lookup"><span data-stu-id="dc861-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="dc861-104">Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="dc861-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="dc861-105">Konkrétně obsahuje informace, které vám pomohou vyřešit problémy s připraveností řešení.</span><span class="sxs-lookup"><span data-stu-id="dc861-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dc861-106">Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="dc861-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="dc861-107">Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.</span><span class="sxs-lookup"><span data-stu-id="dc861-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="dc861-108">Chyba na stránce dvojího zápisu</span><span class="sxs-lookup"><span data-stu-id="dc861-108">Error on the Dual-write page</span></span>

<span data-ttu-id="dc861-109">Na stránce **Dvojího zápisu** se může zobrazit chybová zpráva podobná následujícímu příkladu:</span><span class="sxs-lookup"><span data-stu-id="dc861-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="dc861-110">*Entita s názvem 'msdyn\_dualwriteentitymap' s namemapping = 'logický' nebyla nalezena v MetadataCache.*</span><span class="sxs-lookup"><span data-stu-id="dc861-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="dc861-111">Chcete-li tento problém vyřešit, zkontrolujte, zda je v aplikaci Common Data Service nainstalováno základní řešení dvojího zápisu.</span><span class="sxs-lookup"><span data-stu-id="dc861-111">To fix the issue, make sure that the dual-write core solution is installed in Common Data Service.</span></span> <span data-ttu-id="dc861-112">Základní řešení duálního zapisování je předpokladem pro sledování řešení.</span><span class="sxs-lookup"><span data-stu-id="dc861-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>