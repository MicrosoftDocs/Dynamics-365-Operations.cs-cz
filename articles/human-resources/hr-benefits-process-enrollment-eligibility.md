---
title: Zpracování způsobilosti k registraci
description: Tento článek vysvětluje, jak spustit proces nároku na přihlášení.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0344c48460a7d1540481e09ba106526e119de72b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008301"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="790a5-103">Zpracování způsobilosti k registraci</span><span class="sxs-lookup"><span data-stu-id="790a5-103">Process enrollment eligibility</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="790a5-104">Tento článek vysvětluje, jak spustit proces nároku na přihlášení.</span><span class="sxs-lookup"><span data-stu-id="790a5-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="790a5-105">V pracovním prostoru **Správa výhod** vyberte v části **Zpracování** možnost **Zpracování nároku na registraci**.</span><span class="sxs-lookup"><span data-stu-id="790a5-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="790a5-106">V dialogovém okně **Spustit proces nároku na registraci zaměstnanecké výhody** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="790a5-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="790a5-107">Pole</span><span class="sxs-lookup"><span data-stu-id="790a5-107">Field</span></span> | <span data-ttu-id="790a5-108">Popis</span><span class="sxs-lookup"><span data-stu-id="790a5-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="790a5-109">Období registrace</span><span class="sxs-lookup"><span data-stu-id="790a5-109">Enrollment period</span></span> | <span data-ttu-id="790a5-110">Období pro přihlášení pro zpracování nároku na zaměstnanecké výhody.</span><span class="sxs-lookup"><span data-stu-id="790a5-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="790a5-111">Právnická osoba</span><span class="sxs-lookup"><span data-stu-id="790a5-111">Legal entity</span></span> | <span data-ttu-id="790a5-112">Právnická osoba pro zpracování nároku na registraci.</span><span class="sxs-lookup"><span data-stu-id="790a5-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="790a5-113">Pracovní podproces</span><span class="sxs-lookup"><span data-stu-id="790a5-113">Worker</span></span> | <span data-ttu-id="790a5-114">Pracovník pro zpracování nároku na registraci.</span><span class="sxs-lookup"><span data-stu-id="790a5-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="790a5-115">Pokud toto pole ponecháte prázdné, bude nárok na registraci zpracován pro všechny pracovníky.</span><span class="sxs-lookup"><span data-stu-id="790a5-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="790a5-116">Plán zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="790a5-116">Benefit plan</span></span> | <span data-ttu-id="790a5-117">Plán zaměstnaneckých výhod pro zpracování nároku na registraci.</span><span class="sxs-lookup"><span data-stu-id="790a5-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="790a5-118">Chcete-li spustit proces na pozadí, vyberte možnost **Spustit na pozadí** a proveďte následující úkony:</span><span class="sxs-lookup"><span data-stu-id="790a5-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="790a5-119">Zadejte informace pro proces.</span><span class="sxs-lookup"><span data-stu-id="790a5-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="790a5-120">Chcete-li nastavit opakovanou úlohu, vyberte možnost **opakování**, zadejte informace o opakování a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="790a5-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="790a5-121">Chcete-li nastavit výstrahu úlohy,vyberte **výstrahy**, vyberte výstrahy, které chcete přijmout, a pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="790a5-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="790a5-122">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="790a5-122">Select **OK**.</span></span> <span data-ttu-id="790a5-123">Proces bude spuštěn s nastavenými parametry.</span><span class="sxs-lookup"><span data-stu-id="790a5-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="790a5-124">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="790a5-124">Select **OK**.</span></span>
