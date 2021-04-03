---
title: Zpracování změn životních událostí
description: Zpracování změn životní události v Microsoft Dynamics 365 Human Resources pro změny životní události.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 2726dcb3c847c9af2a431358de04a27341b9e66c
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464243"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="d8cfd-103">Zpracování změn životních událostí</span><span class="sxs-lookup"><span data-stu-id="d8cfd-103">Process life event changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d8cfd-104">Zpracování změn životní události v Microsoft Dynamics 365 Human Resources pro dvě změny životní události:</span><span class="sxs-lookup"><span data-stu-id="d8cfd-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="d8cfd-105">Změny narozenin</span><span class="sxs-lookup"><span data-stu-id="d8cfd-105">Birthday changes</span></span>
- <span data-ttu-id="d8cfd-106">Změny platnosti přepisu pravidla nároku</span><span class="sxs-lookup"><span data-stu-id="d8cfd-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="d8cfd-107">V pracovním prostoru **Správa výhod** vyberte v části **Zpracování** možnost **Zpracování změny životní události**.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="d8cfd-108">V dialogovém okně **Spustit proces změny životní události** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="d8cfd-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="d8cfd-109">Pole</span><span class="sxs-lookup"><span data-stu-id="d8cfd-109">Field</span></span> | <span data-ttu-id="d8cfd-110">Popis</span><span class="sxs-lookup"><span data-stu-id="d8cfd-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d8cfd-111">Období registrace</span><span class="sxs-lookup"><span data-stu-id="d8cfd-111">Enrollment period</span></span> | <span data-ttu-id="d8cfd-112">Období registrace pro zpracování změn životní události.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="d8cfd-113">Právnická osoba</span><span class="sxs-lookup"><span data-stu-id="d8cfd-113">Legal entity</span></span> | <span data-ttu-id="d8cfd-114">Právnická osoba pro zpracování změn životní události.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="d8cfd-115">Chcete-li spustit proces na pozadí, vyberte možnost **Spustit na pozadí** a proveďte následující úkony:</span><span class="sxs-lookup"><span data-stu-id="d8cfd-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="d8cfd-116">Zadejte informace pro proces.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="d8cfd-117">Chcete-li nastavit opakovanou úlohu, vyberte možnost **opakování**, zadejte informace o opakování a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="d8cfd-118">Chcete-li nastavit výstrahu úlohy,vyberte **výstrahy**, vyberte výstrahy, které chcete přijmout, a pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="d8cfd-119">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-119">Select **OK**.</span></span> <span data-ttu-id="d8cfd-120">Proces bude spuštěn s nastavenými parametry.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="d8cfd-121">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d8cfd-121">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]