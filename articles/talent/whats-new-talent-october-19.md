---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent – Core HR (16. října 2018)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0d7c6562ca8b5e7cfa0071ec408955e13a46cb6e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551696"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-16-2018"></a><span data-ttu-id="ff831-103">Co je nového nebo upraveného v aplikaci Dynamics 365 Talent – Core HR (16. října 2018)</span><span class="sxs-lookup"><span data-stu-id="ff831-103">What's new or changed in Dynamics 365 Talent - Core HR (October 16, 2018)</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="ff831-104">**Sestavení 8.1.1067**</span><span class="sxs-lookup"><span data-stu-id="ff831-104">**Build 8.1.1067**</span></span>

<span data-ttu-id="ff831-105">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.</span><span class="sxs-lookup"><span data-stu-id="ff831-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-managers-to-update-time-off-requests"></a><span data-ttu-id="ff831-106">Povolení manažerům aktualizovat požadavky na volno</span><span class="sxs-lookup"><span data-stu-id="ff831-106">Allow managers to update time off requests</span></span>

<span data-ttu-id="ff831-107">Požadavky na volno zaměstnance je třeba někdy aktualizovat po jejich schválení prostřednictvím workflow.</span><span class="sxs-lookup"><span data-stu-id="ff831-107">Employee time off requests may need to be updated after they are approved through the workflow.</span></span> <span data-ttu-id="ff831-108">V mnoha případech provádí manažeři tyto aktualizace jménem zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="ff831-108">In many cases, the manager makes these updates on the employee’s behalf.</span></span> <span data-ttu-id="ff831-109">Tato nová funkce umožňuje manažerům aktualizovat požadavky na volno nebo zrušení volna jménem zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="ff831-109">This new feature provides the ability for managers to update time off or cancel time off requests on behalf of their employees.</span></span> <span data-ttu-id="ff831-110">Tato funkce je řízena parametrem **Práce jménem**, který lze nastavit na stránce **Parametry lidských zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="ff831-110">This capability is controlled by the **Work on behalf** parameter that can be set on the **Human Resource Parameters** page.</span></span> 
 
## <a name="allow-hr-to-update-time-off-requests"></a><span data-ttu-id="ff831-111">Povolení pro oddělení lidských zdrojů aktualizovat požadavky na volno</span><span class="sxs-lookup"><span data-stu-id="ff831-111">Allow HR to update time off requests</span></span>

<span data-ttu-id="ff831-112">Podobně jako u výše uvedené funkce může být třeba, aby požadavky na volno aktualizovalo oddělení lidských zdrojů, poté, co byly schváleny prostřednictvím workflow.</span><span class="sxs-lookup"><span data-stu-id="ff831-112">Similar to the feature above, employee time off requests may need to be updated by HR after they have been previously approved through the workflow.</span></span> <span data-ttu-id="ff831-113">Tato funkce umožňuje uživatelům HR aktualizovat požadavky na volno.</span><span class="sxs-lookup"><span data-stu-id="ff831-113">This feature provides the ability for HR users to update time off requests.</span></span> <span data-ttu-id="ff831-114">Možnost se povoluje v pracovním prostoru **Lidé** na stránce **Pracovník** pomocí nové možnosti s názvem **Zobrazení volna**.</span><span class="sxs-lookup"><span data-stu-id="ff831-114">The capability is enabled in the **People** workspace and on the **Worker** page, using a new option called **View time off**.</span></span> <span data-ttu-id="ff831-115">Na těchto stránkách mohou HR uživatelé zobrazit žádosti a aktualizovat transakce volna podobným způsobem, jako mohou tyo akce provádět manažeři.</span><span class="sxs-lookup"><span data-stu-id="ff831-115">On those pages, HR users can view requests and update time off transactions, similar to how managers can perform these actions.</span></span>

<span data-ttu-id="ff831-116">Funkční oprávnění zabezpečení, které řídí přístup k této funkci je:</span><span class="sxs-lookup"><span data-stu-id="ff831-116">The security duty that controls access to this functionality is:</span></span>
- <span data-ttu-id="ff831-117">Funkční oprávnění: Udržovat procesy pracovního volna a absence specifické pro pracovníka.</span><span class="sxs-lookup"><span data-stu-id="ff831-117">Duty: Maintain worker-specific leave and absence processes.</span></span>
- <span data-ttu-id="ff831-118">Oprávnění: Udržovat požadavky na pracovní volno a absenci pro všechny pracovníky.</span><span class="sxs-lookup"><span data-stu-id="ff831-118">Privilege: Maintain leave and absence requests for all workers.</span></span>

## <a name="other-changes"></a><span data-ttu-id="ff831-119">Další změny</span><span class="sxs-lookup"><span data-stu-id="ff831-119">Other changes</span></span>
<span data-ttu-id="ff831-120">V této verzi byly provedeny následující aktualizace:</span><span class="sxs-lookup"><span data-stu-id="ff831-120">The following updates have been made in this release:</span></span>
- <span data-ttu-id="ff831-121">Změny akcí náboru pracovníka, aby již nezůstávaly zadržení ve stavu **Workflow dokončen**.</span><span class="sxs-lookup"><span data-stu-id="ff831-121">Changes to worker hire actions so that they are no longer "stuck" in **Workflow complete** state.</span></span>
- <span data-ttu-id="ff831-122">Záznam zaměstnání lze nyní vytvořit bez počátečního data zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="ff831-122">Employment record can now be created without an employment start date.</span></span>
- <span data-ttu-id="ff831-123">Datum registrace Dynamics 365 Talent pro kurz zobrazený v samoobsluze pro zaměstnance nyní uplatňuje časový posun pro datum.</span><span class="sxs-lookup"><span data-stu-id="ff831-123">The Dynamics 365 Talent registration date for a course shown in Employee self-service now applies the time zone offset to the date.</span></span>
- <span data-ttu-id="ff831-124">Soubory aplikace Excel lze importovat vícekrát bez chyb pomocí **Entity zaměstnance**.</span><span class="sxs-lookup"><span data-stu-id="ff831-124">Excel files can be imported multiple times without any errors using **Employee Entity**.</span></span>

## <a name="known-issue"></a><span data-ttu-id="ff831-125">Známý problém</span><span class="sxs-lookup"><span data-stu-id="ff831-125">Known issue</span></span>

- <span data-ttu-id="ff831-126">**Problém**: Při přidání nové přílohy k pracovníkovi jsou tlačítka **Nová** a **Upravit** zobrazena šedě.</span><span class="sxs-lookup"><span data-stu-id="ff831-126">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="ff831-127">**Řešení:** Než otevřete stránku přílohy, ujistěte se, že jsou zavřena okna s fakty na stránce **Pracovník**.</span><span class="sxs-lookup"><span data-stu-id="ff831-127">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="ff831-128">Jsou-li okna s fakty uzavřena při načítání stránky **Pracovník**, budou tlačítka přílohy k dispozici.</span><span class="sxs-lookup"><span data-stu-id="ff831-128">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="ff831-129">(Tento problém bude opraven v další aktualizaci Platform Update.)</span><span class="sxs-lookup"><span data-stu-id="ff831-129">(This issue will be fixed in the next platform update.)</span></span>
