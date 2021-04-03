---
title: Konfigurace paralelních aktivit ve workflow
description: Pokud chcete nakonfigurovat paralelní aktivitu, postupujte následovně v editoru workflowu.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 450420d44ad4aab233afc5a116369e993aa7a15b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570607"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="9f5ff-103">Konfigurace paralelních aktivit ve workflow</span><span class="sxs-lookup"><span data-stu-id="9f5ff-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f5ff-104">Pokud chcete nakonfigurovat paralelní aktivitu, postupujte následovně v editoru workflowu.</span><span class="sxs-lookup"><span data-stu-id="9f5ff-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="9f5ff-105">Paralelní aktivita je tvořena větvemi workflowu, které běží ve stejnou dobu.</span><span class="sxs-lookup"><span data-stu-id="9f5ff-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="9f5ff-106">Pojmenování paralelní aktivity</span><span class="sxs-lookup"><span data-stu-id="9f5ff-106">Name a parallel activity</span></span>

<span data-ttu-id="9f5ff-107">Pomocí následujících kroků zadejte název paralelní aktivity.</span><span class="sxs-lookup"><span data-stu-id="9f5ff-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="9f5ff-108">Klikněte pravým tlačítkem na paralelní aktivitu a poté klikněte na tlačítko **Vlastnosti** k otevření formuláře **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="9f5ff-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="9f5ff-109">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="9f5ff-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="9f5ff-110">V poli **Název** zadejte jedinečný název paralelní aktivity.</span><span class="sxs-lookup"><span data-stu-id="9f5ff-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="9f5ff-111">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="9f5ff-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="9f5ff-112">Konfigurace větví paralelní aktivity</span><span class="sxs-lookup"><span data-stu-id="9f5ff-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="9f5ff-113">Pomocí následujících kroků přidejte a nakonfigurujte větve této paralelní aktivity.</span><span class="sxs-lookup"><span data-stu-id="9f5ff-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="9f5ff-114">Poklikejte na paralelní aktivitu, aby se zobrazily její větve.</span><span class="sxs-lookup"><span data-stu-id="9f5ff-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="9f5ff-115">Pokud chcete přidat pobočku, přetáhněte prvek **Větev** z oblasti **Prvky workflowu** do oblasti vložení na plátně.</span><span class="sxs-lookup"><span data-stu-id="9f5ff-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="9f5ff-116">Následující obrázek znázorňuje oblast vložení.</span><span class="sxs-lookup"><span data-stu-id="9f5ff-116">The following figure shows an insertion point.</span></span>

    ![Oblast vložení](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="9f5ff-118">Pořadí větví není důležité, protože všechny větve paralelní aktivity běží současně.</span><span class="sxs-lookup"><span data-stu-id="9f5ff-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="9f5ff-119">Informace o konfiguraci jednotlivých větví uvádí téma [Konfigurace paralelních větví ve workflow](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="9f5ff-119">To configure each branch, see [Configure parallel branches in a workflow](configure-parallel-branch-workflow.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]