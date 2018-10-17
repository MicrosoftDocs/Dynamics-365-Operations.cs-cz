---
title: "Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (1. října 2018)"
description: "Toto téma popisuje funkce, které jsou v aktuální verzi aplikace Microsoft Dynamics 365 for Talent Core HR."
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
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
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: 97820cd25ece48dc0b8045d9ba509d0971ca5aad
ms.contentlocale: cs-cz
ms.lasthandoff: 10/01/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-1-2018"></a><span data-ttu-id="fb28c-103">Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (1. října 2018)</span><span class="sxs-lookup"><span data-stu-id="fb28c-103">What's new or changed in Dynamics 365 for Talent Core HR (October 1, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fb28c-104">**Sestavení 8.1.1035.0**</span><span class="sxs-lookup"><span data-stu-id="fb28c-104">**Build 8.1.1035.0**</span></span>

<span data-ttu-id="fb28c-105">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.</span><span class="sxs-lookup"><span data-stu-id="fb28c-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="turn-off-electronic-payment-validation"></a><span data-ttu-id="fb28c-106">Vypnutí ověření elektronické platby</span><span class="sxs-lookup"><span data-stu-id="fb28c-106">Turn off electronic payment validation</span></span>

<span data-ttu-id="fb28c-107">K ověření informací o elektronické platbě dochází, pokud nastavíte úhrady pro přímý vklad buď prostřednictvím pracovního prostoru **Samoobsluha pro zaměstnance** nebo přímo na formuláři zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="fb28c-107">Electronic payment information validation occurs if you set up disbursements for direct deposit either through **Employee self-service** workspace (ESS) or directly on the employee form.</span></span> <span data-ttu-id="fb28c-108">Tato volba poskytuje možnost odebrat takové ověření, pokud nevyžadujete kontroly ověření pro částky a hodnoty zůstatku.</span><span class="sxs-lookup"><span data-stu-id="fb28c-108">This option gives you the flexibility to remove that validation if you do not require the validation checks for amounts and remainder values.</span></span> <span data-ttu-id="fb28c-109">Tato funkce je užitečná v případě, kdy provádíte integraci s externím mzdovým systémem, který má jiné požadavky.</span><span class="sxs-lookup"><span data-stu-id="fb28c-109">This feature is helpful if you're integrating with an external payroll system that has different requirements.</span></span>

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a><span data-ttu-id="fb28c-110">Samoobsluha pro manažery - Přidání cílů pro členy týmu prostřednictvím dlaždice Cíle výkonnosti týmu</span><span class="sxs-lookup"><span data-stu-id="fb28c-110">Manager self-service - Add goals for team members through the Team performance goals tile</span></span>

<span data-ttu-id="fb28c-111">Před touto verzí manažeři mohou přidat cíle svým zaměstnancům jednotlivě prostřednictvím cílů výkonnosti přidružených ke každému zaměstnanci.</span><span class="sxs-lookup"><span data-stu-id="fb28c-111">Prior to this release, managers can add goals to their employees individually through the performance goals associated to each employee.</span></span> <span data-ttu-id="fb28c-112">Od této aktualizace mají manažeři přístup k dlaždici **Cíle výkonnosti týmu** a mohou vytvořit nové cíle volbou jakéhokoliv ze svých přímých podřízených.</span><span class="sxs-lookup"><span data-stu-id="fb28c-112">With this update, managers can access the **Team performance goals** tile and create new goals by selecting any of their direct reports.</span></span>

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a><span data-ttu-id="fb28c-113">Samoobsluha pro manažery - Přidání kontrol pro členy týmu prostřednictvím dlaždice Kontroly výkonnosti týmu</span><span class="sxs-lookup"><span data-stu-id="fb28c-113">Manager self-service - Add reviews for team members through the Team performance reviews tile</span></span>

<span data-ttu-id="fb28c-114">Před touto verzí manažeři mohou přidat kontroly svým zaměstnancům jednotlivě prostřednictvím kontrol výkonnosti přidružených ke každému zaměstnanci.</span><span class="sxs-lookup"><span data-stu-id="fb28c-114">Prior to this release, managers can add reviews to their employees individually through the reviews associated to each employee.</span></span> <span data-ttu-id="fb28c-115">Od této aktualizace mají manažeři přístup k dlaždici **Kontroly výkonnosti týmu** a mohou vytvořit nové kontroly volbou jakéhokoliv ze svých přímých podřízených.</span><span class="sxs-lookup"><span data-stu-id="fb28c-115">With this update, managers can access the **Team performance reviews** tile and create new reviews by selecting any of their direct reports.</span></span>

## <a name="configure-proration-options-by-leave-plan"></a><span data-ttu-id="fb28c-116">Konfigurace poměrných možností podle plánu pracovního volna</span><span class="sxs-lookup"><span data-stu-id="fb28c-116">Configure proration options by leave plan</span></span>

<span data-ttu-id="fb28c-117">Organizace přidělují volno odlišným způsobem na základě toho, kdy zaměstnanci nastoupili do společnosti a kdy ji opouštějí.</span><span class="sxs-lookup"><span data-stu-id="fb28c-117">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="fb28c-118">U některých organizací dostanou zaměstnanci v datum svého nástupu své úplné přidělení, zatímco jiné organizace přidělí pouze poměrnou část.</span><span class="sxs-lookup"><span data-stu-id="fb28c-118">For some organizations, employees are awarded their full allocation on their start date while others prorate the award.</span></span> <span data-ttu-id="fb28c-119">Nové možnosti jsou k dispozici v této verzi k výběru způsobu poměrného rozdělení volna a časovému rozlišení pro nastupující a odcházející zaměstnance v organizaci.</span><span class="sxs-lookup"><span data-stu-id="fb28c-119">New options are provided in this release to choose how to prorate the awards and accruals for joiners and leavers in an organization.</span></span> <span data-ttu-id="fb28c-120">Možnosti zahrnují: Poměrné, Úplné časové rozlišení a Bez časového rozlišení.</span><span class="sxs-lookup"><span data-stu-id="fb28c-120">Options include: Prorated, Full accrual, and No accrual.</span></span>

## <a name="other-changes"></a><span data-ttu-id="fb28c-121">Další změny</span><span class="sxs-lookup"><span data-stu-id="fb28c-121">Other changes</span></span>

-   <span data-ttu-id="fb28c-122">Entita zaměstnance byla aktualizována - Dlaždici **Osobní** lze nyní aktualizovat pomocí doplňku aplikace Excel / správy dat.</span><span class="sxs-lookup"><span data-stu-id="fb28c-122">Employee entity updated - The **Personal** title can now be updated using the Excel add-in/data management.</span></span>

-   <span data-ttu-id="fb28c-123">Změna zabezpečení pro povolení odstranění tlačítek **Odstranit** a **Deaktivovat** v samoobsluze zaměstnance pro informace o platbě.</span><span class="sxs-lookup"><span data-stu-id="fb28c-123">Security change to allow removal of the **Delete** and **Deactivate** buttons in employee self-service for payment information.</span></span>

## <a name="known-issue"></a><span data-ttu-id="fb28c-124">Známý problém</span><span class="sxs-lookup"><span data-stu-id="fb28c-124">Known issue</span></span>

-   <span data-ttu-id="fb28c-125">**Problém:** Při přidání nové přílohy k pracovníkovi jsou zašedlá tlačítka **Nová** a **Upravit**. **Řešení:** Než otevřete stránku přílohy, ujistěte se, že jsou zavřena okna s fakty na stránce **Pracovník**.</span><span class="sxs-lookup"><span data-stu-id="fb28c-125">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="fb28c-126">Jsou-li okna s fakty uzavřena při načítání stránky **Pracovník**, budou tlačítka **Přílohy** k dispozici.</span><span class="sxs-lookup"><span data-stu-id="fb28c-126">If the FactBoxes are closed when the **Worker** page is loaded, the **Attachments** buttons will be enabled.</span></span> <span data-ttu-id="fb28c-127">(Tento problém bude opraven v další aktualizaci Platform Update.)</span><span class="sxs-lookup"><span data-stu-id="fb28c-127">(This issue will be fixed in the next platform update.)</span></span>

