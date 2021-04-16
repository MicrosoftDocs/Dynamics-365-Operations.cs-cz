---
title: Zpracování životních událostí
description: Během životního cyklu zaměstnance v aplikaci Microsoft Dynamics 365 Human Resources se může každý zaměstnanec setkat s různými změnami životních událostí.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 461f90c3da8fa5b2db14b6dd67a0c19f7eabe867
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793794"
---
# <a name="process-life-events"></a><span data-ttu-id="41138-103">Zpracování životních událostí</span><span class="sxs-lookup"><span data-stu-id="41138-103">Process life events</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="41138-104">Během životního cyklu zaměstnance v aplikaci Microsoft Dynamics 365 Human Resources se může každý zaměstnanec setkat s různými změnami životních událostí.</span><span class="sxs-lookup"><span data-stu-id="41138-104">During the employee lifecycle in Microsoft Dynamics 365 Human Resources, each employee may encounter various life event changes.</span></span> <span data-ttu-id="41138-105">Například sňatek, změna zaměstnání nebo změna závislé osoby / příjemce.</span><span class="sxs-lookup"><span data-stu-id="41138-105">For example, marriage, change in employment, or dependent/beneficiary change.</span></span> <span data-ttu-id="41138-106">Chcete-li používat životní události, je nutné povolit životní události ve formuláři Parametry zaměstnaneckých výhod, nastavit typy životních událostí a nastavit možnosti životních událostí pro typy plánu.</span><span class="sxs-lookup"><span data-stu-id="41138-106">To use life events, you must enable life events in the benefits parameters form, set up life event types, and set up life event options for plan types.</span></span>

<span data-ttu-id="41138-107">Než bude možné zpracovat životní události, musí být v průběhu doby náboru již alespoň jednou spuštěna možnost otevřít registraci.</span><span class="sxs-lookup"><span data-stu-id="41138-107">Before you can process life events, you must have already run open enrollment at least once during a hiring time frame.</span></span> <span data-ttu-id="41138-108">V USA je otevření registrace obvykle jednou za rok.</span><span class="sxs-lookup"><span data-stu-id="41138-108">In the United States, open enrollment is typically once per year.</span></span> <span data-ttu-id="41138-109">Mimo USA může být otevření registrace spuštěno v době nástupu do zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="41138-109">Outside the United States, open enrollment may be run at the time of hire.</span></span> <span data-ttu-id="41138-110">Pracovník nemusí vybírat plán zaměstnaneckých výhod, aby mohl zpracovat životní události, ale musí být zahrnuty v procesu otevřené registrace.</span><span class="sxs-lookup"><span data-stu-id="41138-110">A worker does not need to select a benefit plan in order for life events to be processed, but they need to have been included in open enrollment processing.</span></span> 

<span data-ttu-id="41138-111">Zpracování životní události použijte, když máte pracovníky s životními událostmi, které se uskuteční v budoucnu.</span><span class="sxs-lookup"><span data-stu-id="41138-111">Use life event processing when you have workers who have life events that take place on a future date.</span></span> <span data-ttu-id="41138-112">Tato událost zpracuje všechny životní události, které nebyly zpracovány (jako budoucí životní události nebo životní události, které byly přidány a nejsou specifické pro žádného jiného pracovníka – jedním z příkladů je nová zaměstnanecká výhoda).</span><span class="sxs-lookup"><span data-stu-id="41138-112">This event will process all life events that have not been processed (like future life events, or life events that have been added that are not specific to any one worker – one example is a new benefit).</span></span> <span data-ttu-id="41138-113">Životní události z reálného života jsou skryté.</span><span class="sxs-lookup"><span data-stu-id="41138-113">Real-time life events are hidden.</span></span>

<span data-ttu-id="41138-114">Pokud je například dnes 1. února a na 14. února je naplánována změna právnických osob pro Jana Nováka, pak pokud spustíte zpracování životní události na 15. února, systém zpracuje všechny události do 15. února.</span><span class="sxs-lookup"><span data-stu-id="41138-114">For example, if today is February 1, and on February 14 worker Joe Smith is scheduled to change legal entities, if you run life event processing for February 15, the system processes all events up until February 15.</span></span> 

1. <span data-ttu-id="41138-115">V pracovním prostoru **Správa výhod** vyberte v části **Zpracování** možnost **Zpracování životní události**.</span><span class="sxs-lookup"><span data-stu-id="41138-115">In the **Benefits management** workspace, under **Processing**, select **Life event processing**.</span></span>

2. <span data-ttu-id="41138-116">V dialogovém okně **Spustit zpracování životní události** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="41138-116">In the **Run life event process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="41138-117">Pole</span><span class="sxs-lookup"><span data-stu-id="41138-117">Field</span></span> | <span data-ttu-id="41138-118">Popis</span><span class="sxs-lookup"><span data-stu-id="41138-118">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="41138-119">**Období registrace**</span><span class="sxs-lookup"><span data-stu-id="41138-119">**Enrollment period**</span></span> | <span data-ttu-id="41138-120">Období registrace pro zpracování životních událostí pro.</span><span class="sxs-lookup"><span data-stu-id="41138-120">The enrollment period to process life events for.</span></span> |
   | <span data-ttu-id="41138-121">**Právnická osoba**</span><span class="sxs-lookup"><span data-stu-id="41138-121">**Legal entity**</span></span> | <span data-ttu-id="41138-122">Právnická osoba pro zpracování životních událostí.</span><span class="sxs-lookup"><span data-stu-id="41138-122">The legal entity to process life events for.</span></span> |
   | <span data-ttu-id="41138-123">**Datum životní události**</span><span class="sxs-lookup"><span data-stu-id="41138-123">**Life event date**</span></span> | <span data-ttu-id="41138-124">Systém zpracuje všechny události během období registrace, ke kterému dojde do tohoto data.</span><span class="sxs-lookup"><span data-stu-id="41138-124">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="41138-125">**Pracovní podproces**</span><span class="sxs-lookup"><span data-stu-id="41138-125">**Worker**</span></span> | <span data-ttu-id="41138-126">Pracovník, pro něhož mají být zpracovány životní události.</span><span class="sxs-lookup"><span data-stu-id="41138-126">The worker to process life events for.</span></span> <span data-ttu-id="41138-127">Pokud toto pole ponecháte prázdné, budou životní události zpracovány pro všechny pracovníky.</span><span class="sxs-lookup"><span data-stu-id="41138-127">If you leave this field blank, life events will be processed for all workers.</span></span> |

3. <span data-ttu-id="41138-128">Chcete-li spustit proces na pozadí, vyberte možnost **Spustit na pozadí** a proveďte následující úkony:</span><span class="sxs-lookup"><span data-stu-id="41138-128">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="41138-129">Zadejte informace pro proces.</span><span class="sxs-lookup"><span data-stu-id="41138-129">Enter information for the process.</span></span>

   2. <span data-ttu-id="41138-130">Chcete-li nastavit opakovanou úlohu, vyberte možnost **opakování**, zadejte informace o opakování a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="41138-130">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="41138-131">Chcete-li nastavit výstrahu úlohy,vyberte **výstrahy**, vyberte výstrahy, které chcete přijmout, a pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="41138-131">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="41138-132">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="41138-132">Select **OK**.</span></span> <span data-ttu-id="41138-133">Proces bude spuštěn s nastavenými parametry.</span><span class="sxs-lookup"><span data-stu-id="41138-133">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="41138-134">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="41138-134">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]