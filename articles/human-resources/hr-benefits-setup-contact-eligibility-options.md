---
title: Konfigurace možností způsobilosti osobních kontaktů
description: Nakonfigurujte možnosti způsobilosti osobních kontaktů v Microsoft Dynamics 365 Human Resources. Osobními kontakty mohou být osoby, které jsou příjemci nebo závislé osoby.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2f300ac917ac21db9fffbffcc6eb8589357c0a3e
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466199"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="df3fb-104">Konfigurace možností způsobilosti osobních kontaktů</span><span class="sxs-lookup"><span data-stu-id="df3fb-104">Configure personal contact eligibility options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="df3fb-105">Tento článek vysvětluje, jak konfigurovat typy osobních kontaktů, které mají být použity ve výhodách v aplikaci Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="df3fb-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="df3fb-106">Osobními kontakty mohou být osoby, které jsou příjemci nebo závislé osoby.</span><span class="sxs-lookup"><span data-stu-id="df3fb-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="df3fb-107">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Možnosti nároků na osobní kontakty**.</span><span class="sxs-lookup"><span data-stu-id="df3fb-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="df3fb-108">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="df3fb-108">Select **New**.</span></span>

3. <span data-ttu-id="df3fb-109">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="df3fb-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="df3fb-110">Pole</span><span class="sxs-lookup"><span data-stu-id="df3fb-110">Field</span></span> | <span data-ttu-id="df3fb-111">Popis</span><span class="sxs-lookup"><span data-stu-id="df3fb-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="df3fb-112">**Možnost způsobilosti**</span><span class="sxs-lookup"><span data-stu-id="df3fb-112">**Eligibility option**</span></span> | <span data-ttu-id="df3fb-113">Jedinečný název nebo kód možnosti nároku pro identifikaci možnosti nároku.</span><span class="sxs-lookup"><span data-stu-id="df3fb-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="df3fb-114">**Popis**</span><span class="sxs-lookup"><span data-stu-id="df3fb-114">**Description**</span></span> | <span data-ttu-id="df3fb-115">Stručný popis možnosti nároku.</span><span class="sxs-lookup"><span data-stu-id="df3fb-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="df3fb-116">**Kód způsobilosti kontaktu**</span><span class="sxs-lookup"><span data-stu-id="df3fb-116">**Contact eligibility code**</span></span> | <span data-ttu-id="df3fb-117">Systémový kód, který nejlépe popisuje možnost osobní způsobilosti.</span><span class="sxs-lookup"><span data-stu-id="df3fb-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="df3fb-118">Lze vybrat následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="df3fb-118">You can choose from:</span></span> <ul><li><span data-ttu-id="df3fb-119">Vztah</span><span class="sxs-lookup"><span data-stu-id="df3fb-119">Relationship</span></span></li><li><span data-ttu-id="df3fb-120">Student</span><span class="sxs-lookup"><span data-stu-id="df3fb-120">Student</span></span></li><li><span data-ttu-id="df3fb-121">Rodinný příslušník nad věkovým limitem</span><span class="sxs-lookup"><span data-stu-id="df3fb-121">Overage dependent</span></span></li><li><span data-ttu-id="df3fb-122">Rodinný příslušník s postižením nad věkovým limitem</span><span class="sxs-lookup"><span data-stu-id="df3fb-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="df3fb-123">**Stav**</span><span class="sxs-lookup"><span data-stu-id="df3fb-123">**Status**</span></span> | <span data-ttu-id="df3fb-124">Stav možnosti nároku.</span><span class="sxs-lookup"><span data-stu-id="df3fb-124">The status of the eligibility option.</span></span> <span data-ttu-id="df3fb-125">Pokud je stav možnosti nároku nastaven na neaktivní, nemůžete vybrat možnost nároku na osobní kontakt pro osobní kontakty.</span><span class="sxs-lookup"><span data-stu-id="df3fb-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="df3fb-126">**Vztah**</span><span class="sxs-lookup"><span data-stu-id="df3fb-126">**Relationship**</span></span> | <span data-ttu-id="df3fb-127">Určuje vztah mezi osobním kontaktem a zaměstnancem.</span><span class="sxs-lookup"><span data-stu-id="df3fb-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="df3fb-128">Toto pole je aktivní pouze v případě, že je kód nároku na kontakt nastavený na vztah.</span><span class="sxs-lookup"><span data-stu-id="df3fb-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="df3fb-129">**Věk**</span><span class="sxs-lookup"><span data-stu-id="df3fb-129">**Age**</span></span> | <span data-ttu-id="df3fb-130">Maximální stáří vhodného osobního kontaktu pro plán zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="df3fb-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="df3fb-131">Toto pole je aktivní pouze v případě, že vyberete vztah.</span><span class="sxs-lookup"><span data-stu-id="df3fb-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="df3fb-132">Tento věk se porovnává s vypočítaným stářím osobního kontaktu.</span><span class="sxs-lookup"><span data-stu-id="df3fb-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="df3fb-133">Vypočítaný věk je: (datum disponibility – datum narození osobního kontaktu / 365).</span><span class="sxs-lookup"><span data-stu-id="df3fb-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="df3fb-134">Toto číslo je vždy celé číslo.</span><span class="sxs-lookup"><span data-stu-id="df3fb-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="df3fb-135">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="df3fb-135">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]