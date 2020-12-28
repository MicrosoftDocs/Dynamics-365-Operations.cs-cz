---
title: Zpracování změn sazby
description: Zpracování změn sazby zaměstnaneckých výhod v Microsoft Dynamics 365 Human Resources, když má nový nebo existující plán zaměstnaneckých výhod změnu v nastavení pravidla způsobilosti.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: da42ef6ea91b95903316e35b551b222b8ff3b946
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417606"
---
# <a name="process-rate-changes"></a><span data-ttu-id="d74a7-103">Zpracování změn sazby</span><span class="sxs-lookup"><span data-stu-id="d74a7-103">Process rate changes</span></span>

<span data-ttu-id="d74a7-104">Zpracování změn sazby zaměstnaneckých výhod v Microsoft Dynamics 365 Human Resources, když má nový nebo existující plán zaměstnaneckých výhod změnu v nastavení pravidla způsobilosti.</span><span class="sxs-lookup"><span data-stu-id="d74a7-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="d74a7-105">Pokud je vytvořeno nové pravidlo způsobilosti a je přiřazeno k plánu, zobrazí se výzva systému pro opětovné spuštění nároku pracovníka ke kontrole, zda mohou mít zaměstnanci nárok na plán na základě nových možností nároku.</span><span class="sxs-lookup"><span data-stu-id="d74a7-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to rerun worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="d74a7-106">V pracovním prostoru **Správa výhod** vyberte v části **Zpracování** možnost **Zpracování aktualizace změny sazby**.</span><span class="sxs-lookup"><span data-stu-id="d74a7-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="d74a7-107">V dialogovém okně **Spustit proces aktualizace sazby zaměstnanecké výhody** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="d74a7-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="d74a7-108">Pole</span><span class="sxs-lookup"><span data-stu-id="d74a7-108">Field</span></span> | <span data-ttu-id="d74a7-109">Popis</span><span class="sxs-lookup"><span data-stu-id="d74a7-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d74a7-110">**Období registrace**</span><span class="sxs-lookup"><span data-stu-id="d74a7-110">**Enrollment period**</span></span> | <span data-ttu-id="d74a7-111">Období registrace, pro které mají být zpracovány změny sazeb.</span><span class="sxs-lookup"><span data-stu-id="d74a7-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="d74a7-112">Chcete-li spustit proces na pozadí, vyberte možnost **Spustit na pozadí** a proveďte následující úkony:</span><span class="sxs-lookup"><span data-stu-id="d74a7-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="d74a7-113">Zadejte informace pro proces.</span><span class="sxs-lookup"><span data-stu-id="d74a7-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="d74a7-114">Chcete-li nastavit opakovanou úlohu, vyberte možnost **opakování**, zadejte informace o opakování a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d74a7-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="d74a7-115">Chcete-li nastavit výstrahu úlohy,vyberte **výstrahy**, vyberte výstrahy, které chcete přijmout, a pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d74a7-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="d74a7-116">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d74a7-116">Select **OK**.</span></span> <span data-ttu-id="d74a7-117">Proces bude spuštěn s nastavenými parametry.</span><span class="sxs-lookup"><span data-stu-id="d74a7-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="d74a7-118">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d74a7-118">Select **OK**.</span></span>
