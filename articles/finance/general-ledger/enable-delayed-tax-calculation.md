---
title: Povolit výpočet opožděné daně v deníku
description: Toto téma vysvětluje, jak pomocí funkce **Povolit výpočet opožděné daně v deníku** zvýšit výkonnost výpočtu daně, pokud je objem řádků deníku velmi velký.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176749"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a><span data-ttu-id="f820f-103">Povolit výpočet opožděné daně v deníku</span><span class="sxs-lookup"><span data-stu-id="f820f-103">Enable delayed tax calculation on journal</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f820f-104">Toto téma vysvětluje, jak pomocí funkce **Povolit výpočet opožděné daně v deníku** zvýšit výkonnost výpočtu daně, pokud je objem řádků deníku velmi velký.</span><span class="sxs-lookup"><span data-stu-id="f820f-104">This topic explains how to use the **Enable delayed tax calculation on journal** feature to improve tax calculation performance when the volume of journal lines is huge.</span></span>

<span data-ttu-id="f820f-105">Aktuální chování při výpočtu DPH v deníku je v reálném čase spuštěno při aktualizaci polí daně, např. skupiny DPH nebo skupiny DPH položky.</span><span class="sxs-lookup"><span data-stu-id="f820f-105">Current sales tax calculation behavior on journal is real-time triggered when user updates tax related fields, e.g. sales tax group/item sales tax group.</span></span> <span data-ttu-id="f820f-106">Každá aktualizace na úrovni řádku deníku znovu vypočítá částku daně na všech řádcích deníku.</span><span class="sxs-lookup"><span data-stu-id="f820f-106">Any update at journal line level will re-calculate tax amount on all journal lines.</span></span> <span data-ttu-id="f820f-107">Pomáhá uživateli zobrazit vypočítanou částku daně v reálném čase, ale může také vést k potížím s výkonem v případě, že objem řádků deníku je velmi velký.</span><span class="sxs-lookup"><span data-stu-id="f820f-107">It helps user to see real-time calculated tax amount but it could also bring performance issue if  the volume of journal lines is huge.</span></span>

<span data-ttu-id="f820f-108">Tato funkce poskytuje možnost odložit výpočet daně za účelem vyřešení problému s výkonem.</span><span class="sxs-lookup"><span data-stu-id="f820f-108">This feature provides an option to delay tax calculation to solve performance issue.</span></span> <span data-ttu-id="f820f-109">Je-li tato funkce zapnuta, bude částka daně vypočtena pouze v případě, že uživatel klikne na příkaz „DPH“ nebo zaúčtuje deník.</span><span class="sxs-lookup"><span data-stu-id="f820f-109">If this feature is turned on, tax amount will only be calculated when user clicks "Sales Tax" command or posts the journal.</span></span>

<span data-ttu-id="f820f-110">Uživatel může parametr zapnout nebo vypnout ve třech úrovních:</span><span class="sxs-lookup"><span data-stu-id="f820f-110">User can turn on/off the parameter at three levels:</span></span>
- <span data-ttu-id="f820f-111">Podle právnické osoby</span><span class="sxs-lookup"><span data-stu-id="f820f-111">By legal entity</span></span>
- <span data-ttu-id="f820f-112">Dle názvu deníku</span><span class="sxs-lookup"><span data-stu-id="f820f-112">By journal name</span></span>
- <span data-ttu-id="f820f-113">Dle záhlaví deníku</span><span class="sxs-lookup"><span data-stu-id="f820f-113">By journal header</span></span>

<span data-ttu-id="f820f-114">Systém převezme hodnotu parametru v záhlaví deníku jako konečný.</span><span class="sxs-lookup"><span data-stu-id="f820f-114">System will take the parameter value on journal header as final.</span></span> <span data-ttu-id="f820f-115">Hodnota parametru v záhlaví deníku bude převzata z názvu deníku.</span><span class="sxs-lookup"><span data-stu-id="f820f-115">Parameter value on journal header will be defaulted from journal name.</span></span> <span data-ttu-id="f820f-116">Hodnota parametru v názvu deníku bude při vytvoření názvu deníku přepsána z parametru hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="f820f-116">Parameter value on journal name will be defaulted from general ledger parameter when the journal name is created.</span></span>

<span data-ttu-id="f820f-117">Je-li tento parametr zapnutý, skryje se pole ‚Skutečná částka DPH‘ a ‚Vypočítaná částka DPH‘ v deníku.</span><span class="sxs-lookup"><span data-stu-id="f820f-117">"Actual sales tax amount" and "Calculated sales tax amount" fields on journal will be hided if this parameter is turned on.</span></span> <span data-ttu-id="f820f-118">Účelem je , aby nedošlo ke zmatení uživatele, protože hodnota těchto dvou polí vždy zobrazí 0 před spuštěním výpočtu daně uživatelem.</span><span class="sxs-lookup"><span data-stu-id="f820f-118">The purpose is not to confuse user because the value of these two fields will always show 0 before user trigger the tax calculation.</span></span>

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a><span data-ttu-id="f820f-119">Povolit výpočet zpožděné daně podle právnické osoby</span><span class="sxs-lookup"><span data-stu-id="f820f-119">Enable delayed tax calculation by legal entity</span></span>

1. <span data-ttu-id="f820f-120">Přejděte do **Hlavní knihy > Nastavení hlavní knihy > Parametry hlavní knihy**</span><span class="sxs-lookup"><span data-stu-id="f820f-120">Go to **General ledger > Ledger setup > General ledger parameters**</span></span>
2. <span data-ttu-id="f820f-121">Klikněte na kartu **DPH**</span><span class="sxs-lookup"><span data-stu-id="f820f-121">Click **Sales tax** tab</span></span>
3. <span data-ttu-id="f820f-122">Na pevné kartě **Obecné** vyhledejte parametr **Výpočet opožděné daně** a zapněte jej nebo vypněte.</span><span class="sxs-lookup"><span data-stu-id="f820f-122">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a><span data-ttu-id="f820f-123">Povolit výpočet opožděné daně dle názvu deníku</span><span class="sxs-lookup"><span data-stu-id="f820f-123">Enable delayed tax calculation by journal name</span></span>

1. <span data-ttu-id="f820f-124">Přejděte do **Hlavní knihy > Nastavení deníku > Názvy deníků**</span><span class="sxs-lookup"><span data-stu-id="f820f-124">Go to **General ledger > Journal setup > Journal names**</span></span>
2. <span data-ttu-id="f820f-125">Na pevné kartě **Obecné** vyhledejte parametr **Výpočet opožděné daně** a zapněte jej nebo vypněte.</span><span class="sxs-lookup"><span data-stu-id="f820f-125">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a><span data-ttu-id="f820f-126">Povolit výpočet opožděné daně dle deníku</span><span class="sxs-lookup"><span data-stu-id="f820f-126">Enable delayed tax calculation by journal</span></span>

1. <span data-ttu-id="f820f-127">Přejděte do nabídky **Hlavní kniha > Položky deníku > Hlavní deníky**</span><span class="sxs-lookup"><span data-stu-id="f820f-127">Go to **General ledger > Journal entries > General journals**</span></span>
2. <span data-ttu-id="f820f-128">Klepněte na možnost **Nový**</span><span class="sxs-lookup"><span data-stu-id="f820f-128">Click **New**</span></span>
3. <span data-ttu-id="f820f-129">Vyberte název deníku.</span><span class="sxs-lookup"><span data-stu-id="f820f-129">Select a journal name</span></span>
4. <span data-ttu-id="f820f-130">Klikněte na možnost **Nastavení**</span><span class="sxs-lookup"><span data-stu-id="f820f-130">Click **Setup**</span></span>
5. <span data-ttu-id="f820f-131">Vyhledej parametr **Výpočet opožděné daně** a zapněte jej nebo vypněte.</span><span class="sxs-lookup"><span data-stu-id="f820f-131">Find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-header.png)
