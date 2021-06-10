---
title: Zpracování změn sazby
description: Zpracování změn sazby zaměstnaneckých výhod v Microsoft Dynamics 365 Human Resources, když má nový nebo existující plán zaměstnaneckých výhod změnu v nastavení pravidla způsobilosti.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5cfecc4da90b4fb39bdece38095f3b25023e4cae
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055693"
---
# <a name="process-rate-changes"></a><span data-ttu-id="bc49b-103">Zpracování změn sazby</span><span class="sxs-lookup"><span data-stu-id="bc49b-103">Process rate changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bc49b-104">Zpracování změn sazby zaměstnaneckých výhod v Microsoft Dynamics 365 Human Resources, když má nový nebo existující plán zaměstnaneckých výhod změnu v nastavení pravidla způsobilosti.</span><span class="sxs-lookup"><span data-stu-id="bc49b-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="bc49b-105">Pokud je vytvořeno nové pravidlo způsobilosti a je přiřazeno k plánu, zobrazí se výzva systému pro opětovné spuštění nároku pracovníka ke kontrole, zda mohou mít zaměstnanci nárok na plán na základě nových možností nároku.</span><span class="sxs-lookup"><span data-stu-id="bc49b-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to rerun worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="bc49b-106">V pracovním prostoru **Správa výhod** vyberte v části **Zpracování** možnost **Zpracování aktualizace změny sazby**.</span><span class="sxs-lookup"><span data-stu-id="bc49b-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="bc49b-107">V dialogovém okně **Spustit proces aktualizace sazby zaměstnanecké výhody** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="bc49b-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="bc49b-108">Pole</span><span class="sxs-lookup"><span data-stu-id="bc49b-108">Field</span></span> | <span data-ttu-id="bc49b-109">Popis</span><span class="sxs-lookup"><span data-stu-id="bc49b-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bc49b-110">**Období registrace**</span><span class="sxs-lookup"><span data-stu-id="bc49b-110">**Enrollment period**</span></span> | <span data-ttu-id="bc49b-111">Období registrace, pro které mají být zpracovány změny sazeb.</span><span class="sxs-lookup"><span data-stu-id="bc49b-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="bc49b-112">Chcete-li spustit proces na pozadí, vyberte možnost **Spustit na pozadí** a proveďte následující úkony:</span><span class="sxs-lookup"><span data-stu-id="bc49b-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="bc49b-113">Zadejte informace pro proces.</span><span class="sxs-lookup"><span data-stu-id="bc49b-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="bc49b-114">Chcete-li nastavit opakovanou úlohu, vyberte možnost **opakování**, zadejte informace o opakování a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="bc49b-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="bc49b-115">Chcete-li nastavit výstrahu úlohy,vyberte **výstrahy**, vyberte výstrahy, které chcete přijmout, a pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="bc49b-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="bc49b-116">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="bc49b-116">Select **OK**.</span></span> <span data-ttu-id="bc49b-117">Proces bude spuštěn s nastavenými parametry.</span><span class="sxs-lookup"><span data-stu-id="bc49b-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="bc49b-118">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="bc49b-118">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]