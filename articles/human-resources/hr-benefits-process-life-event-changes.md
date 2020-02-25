---
title: Zpracování změn životních událostí
description: Zpracování změn životní události v Microsoft Dynamics 365 Human Resources pro změny životní události.
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
ms.openlocfilehash: f9bce9394a361bbecfcc0531c5d7ebe9302c8f11
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008367"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="76545-103">Zpracování změn životních událostí</span><span class="sxs-lookup"><span data-stu-id="76545-103">Process life event changes</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="76545-104">Zpracování změn životní události v Microsoft Dynamics 365 Human Resources pro dvě změny životní události:</span><span class="sxs-lookup"><span data-stu-id="76545-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="76545-105">Změny narozenin</span><span class="sxs-lookup"><span data-stu-id="76545-105">Birthday changes</span></span>
- <span data-ttu-id="76545-106">Změny platnosti přepisu pravidla nároku</span><span class="sxs-lookup"><span data-stu-id="76545-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="76545-107">V pracovním prostoru **Správa výhod** vyberte v části **Zpracování** možnost **Zpracování změny životní události**.</span><span class="sxs-lookup"><span data-stu-id="76545-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="76545-108">V dialogovém okně **Spustit proces změny životní události** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="76545-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="76545-109">Pole</span><span class="sxs-lookup"><span data-stu-id="76545-109">Field</span></span> | <span data-ttu-id="76545-110">Popis</span><span class="sxs-lookup"><span data-stu-id="76545-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="76545-111">Období registrace</span><span class="sxs-lookup"><span data-stu-id="76545-111">Enrollment period</span></span> | <span data-ttu-id="76545-112">Období registrace pro zpracování změn životní události.</span><span class="sxs-lookup"><span data-stu-id="76545-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="76545-113">Právnická osoba</span><span class="sxs-lookup"><span data-stu-id="76545-113">Legal entity</span></span> | <span data-ttu-id="76545-114">Právnická osoba pro zpracování změn životní události.</span><span class="sxs-lookup"><span data-stu-id="76545-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="76545-115">Chcete-li spustit proces na pozadí, vyberte možnost **Spustit na pozadí** a proveďte následující úkony:</span><span class="sxs-lookup"><span data-stu-id="76545-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="76545-116">Zadejte informace pro proces.</span><span class="sxs-lookup"><span data-stu-id="76545-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="76545-117">Chcete-li nastavit opakovanou úlohu, vyberte možnost **opakování**, zadejte informace o opakování a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="76545-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="76545-118">Chcete-li nastavit výstrahu úlohy,vyberte **výstrahy**, vyberte výstrahy, které chcete přijmout, a pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="76545-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="76545-119">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="76545-119">Select **OK**.</span></span> <span data-ttu-id="76545-120">Proces bude spuštěn s nastavenými parametry.</span><span class="sxs-lookup"><span data-stu-id="76545-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="76545-121">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="76545-121">Select **OK**.</span></span>
