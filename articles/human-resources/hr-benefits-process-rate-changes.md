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
ms.openlocfilehash: 850709480326f6a0871f19ea1bb287631cd58b42
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229926"
---
# <a name="process-rate-changes"></a><span data-ttu-id="730f0-103">Zpracování změn sazby</span><span class="sxs-lookup"><span data-stu-id="730f0-103">Process rate changes</span></span>

<span data-ttu-id="730f0-104">Zpracování změn sazby zaměstnaneckých výhod v Microsoft Dynamics 365 Human Resources, když má nový nebo existující plán zaměstnaneckých výhod změnu v nastavení pravidla způsobilosti.</span><span class="sxs-lookup"><span data-stu-id="730f0-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="730f0-105">Pokud je vytvořeno nové pravidlo způsobilosti a je přiřazeno k plánu, zobrazí se výzva systému pro opětovné spuštění nároku pracovníka ke kontrole, zda mohou mít zaměstnanci nárok na plán na základě nových možností nároku.</span><span class="sxs-lookup"><span data-stu-id="730f0-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to rerun worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="730f0-106">V pracovním prostoru **Správa výhod** vyberte v části **Zpracování** možnost **Zpracování aktualizace změny sazby**.</span><span class="sxs-lookup"><span data-stu-id="730f0-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="730f0-107">V dialogovém okně **Spustit proces aktualizace sazby zaměstnanecké výhody** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="730f0-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="730f0-108">Pole</span><span class="sxs-lookup"><span data-stu-id="730f0-108">Field</span></span> | <span data-ttu-id="730f0-109">Popis</span><span class="sxs-lookup"><span data-stu-id="730f0-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="730f0-110">**Období registrace**</span><span class="sxs-lookup"><span data-stu-id="730f0-110">**Enrollment period**</span></span> | <span data-ttu-id="730f0-111">Období registrace, pro které mají být zpracovány změny sazeb.</span><span class="sxs-lookup"><span data-stu-id="730f0-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="730f0-112">Chcete-li spustit proces na pozadí, vyberte možnost **Spustit na pozadí** a proveďte následující úkony:</span><span class="sxs-lookup"><span data-stu-id="730f0-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="730f0-113">Zadejte informace pro proces.</span><span class="sxs-lookup"><span data-stu-id="730f0-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="730f0-114">Chcete-li nastavit opakovanou úlohu, vyberte možnost **opakování**, zadejte informace o opakování a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="730f0-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="730f0-115">Chcete-li nastavit výstrahu úlohy,vyberte **výstrahy**, vyberte výstrahy, které chcete přijmout, a pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="730f0-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="730f0-116">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="730f0-116">Select **OK**.</span></span> <span data-ttu-id="730f0-117">Proces bude spuštěn s nastavenými parametry.</span><span class="sxs-lookup"><span data-stu-id="730f0-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="730f0-118">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="730f0-118">Select **OK**.</span></span>
