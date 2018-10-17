---
title: "Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (24. září 2018)"
description: "Toto téma popisuje funkce, které jsou v aktuální verzi aplikace Microsoft Dynamics 365 for Talent Core HR."
author: Darinkramer
manager: AnnBe
ms.date: 09/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 94950fbe5c1aad3dfbd3de59d1bcb47337ff68ea
ms.openlocfilehash: aeb75fe4c775b9003c6429de536498f495224098
ms.contentlocale: cs-cz
ms.lasthandoff: 09/24/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-24-2018"></a><span data-ttu-id="e4dee-103">Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (24. září 2018)</span><span class="sxs-lookup"><span data-stu-id="e4dee-103">What's new or changed in Dynamics 365 for Talent Core HR (September 24, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e4dee-104">**Sestavení 8.1.1015.0**</span><span class="sxs-lookup"><span data-stu-id="e4dee-104">**Build 8.1.1015.0**</span></span>

<span data-ttu-id="e4dee-105">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.</span><span class="sxs-lookup"><span data-stu-id="e4dee-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="currency-added-to-benefits"></a><span data-ttu-id="e4dee-106">Měna přidána do zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="e4dee-106">Currency added to Benefits</span></span>

<span data-ttu-id="e4dee-107">Byly aktualizovány plány zaměstnaneckých výhod, aby zahrnovaly měnu výhody.</span><span class="sxs-lookup"><span data-stu-id="e4dee-107">Benefit plans have been updated to include the currency of the benefit.</span></span> <span data-ttu-id="e4dee-108">Toto nové pole je také k dispozici na registrovaných zaměstnaneckých výhodách pracovníka.</span><span class="sxs-lookup"><span data-stu-id="e4dee-108">This new field is also available on worker enrolled benefits.</span></span> <span data-ttu-id="e4dee-109">Toto nové pole je součástí oprávnění zabezpečení Udržovat zaměstnanecké výhody a Zobrazit seznam zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="e4dee-109">This new field is part of the Maintain benefits and View a list of benefits security privilege.</span></span>

## <a name="update-proration-process--leave-and-absence"></a><span data-ttu-id="e4dee-110">Aktualizace poměrného procesu - Pracovní volno a absence</span><span class="sxs-lookup"><span data-stu-id="e4dee-110">Update proration process – Leave and Absence</span></span>

<span data-ttu-id="e4dee-111">Organizace přidělují volno odlišným způsobem na základě toho, kdy zaměstnanci nastoupili do společnosti a kdy ji opouštějí.</span><span class="sxs-lookup"><span data-stu-id="e4dee-111">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="e4dee-112">U zaměstnanců, kteří opouštějí organizaci, mohou někteří potřebovat ukončit odměny v den ukončení, zatímco jiní se spoléhají na poslední den práce, aby zastavili proces časového rozlišení.</span><span class="sxs-lookup"><span data-stu-id="e4dee-112">For employees leaving the organization, some may need to end the award on the termination date, while others rely on the last day worked to stop the accrual process.</span></span> <span data-ttu-id="e4dee-113">Tyto změny umožňují organizacím zvolit, kdy má být ukončena registrace během ukončovacího procesu.</span><span class="sxs-lookup"><span data-stu-id="e4dee-113">These changes provide organizations the ability to choose when to end enrollment during the termination process.</span></span> <span data-ttu-id="e4dee-114">Tyto nové možnosti jsou součástí oprávnění pro Ukončit poměr pracovníka a Ukončit poměr pracovníka ze samoobsluhy pro manažery.</span><span class="sxs-lookup"><span data-stu-id="e4dee-114">These new options are part of the privileges for Terminate a worker and Terminate a worker from manager self service.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="e4dee-115">Další změny</span><span class="sxs-lookup"><span data-stu-id="e4dee-115">Other changes</span></span>

<span data-ttu-id="e4dee-116">Toto vydání obsahuje několik dalších oprav chyb.</span><span class="sxs-lookup"><span data-stu-id="e4dee-116">This release includes several additional bug fixes.</span></span>

## <a name="known-issue"></a><span data-ttu-id="e4dee-117">Známý problém</span><span class="sxs-lookup"><span data-stu-id="e4dee-117">Known Issue</span></span>

-   <span data-ttu-id="e4dee-118">**Problém:** Při přidání nové přílohy k pracovníkovi jsou zašedlá tlačítka **Nová** a **Upravit**. **Řešení:** Než otevřete stránku přílohy, ujistěte se, že jsou zavřena okna s fakty na stránce **Pracovník**.</span><span class="sxs-lookup"><span data-stu-id="e4dee-118">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the fact boxes on the **Worker** page are closed.</span></span> <span data-ttu-id="e4dee-119">Jsou-li okna s fakty uzavřena při načítání stránky **Pracovník**, budou tlačítka příloh k dispozici.</span><span class="sxs-lookup"><span data-stu-id="e4dee-119">If the fact boxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="e4dee-120">(Tento problém bude opraven v další aktualizaci Platform Update.)</span><span class="sxs-lookup"><span data-stu-id="e4dee-120">(This issue will be fixed in the next platform update.)</span></span>

