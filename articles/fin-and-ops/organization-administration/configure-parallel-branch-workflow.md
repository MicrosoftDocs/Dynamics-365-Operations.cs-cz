---
title: Konfigurace paralelních větví ve workflow
description: Pokud chcete nakonfigurovat paralelní větev, postupujte následovně v editoru workflowu.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 73626ad21dfe2be7400f321a3eee272c896276f3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "367333"
---
# <a name="configure-parallel-branches-in-a-workflow"></a><span data-ttu-id="f32c8-103">Konfigurace paralelních větví ve workflow</span><span class="sxs-lookup"><span data-stu-id="f32c8-103">Configure parallel branches in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f32c8-104">Pokud chcete nakonfigurovat paralelní větev, postupujte následovně v editoru workflowu.</span><span class="sxs-lookup"><span data-stu-id="f32c8-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="f32c8-105">Paralelní větev je v podstatě workflow, který je spuštěn v kontextu nadřazeného workflowu.</span><span class="sxs-lookup"><span data-stu-id="f32c8-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="f32c8-106">Pojmenujte větev</span><span class="sxs-lookup"><span data-stu-id="f32c8-106">Name a branch</span></span>

<span data-ttu-id="f32c8-107">Pomocí následujících kroků zadejte název paralelní větve.</span><span class="sxs-lookup"><span data-stu-id="f32c8-107">Follow these steps to enter a name for a parallel branch.</span></span>

1. <span data-ttu-id="f32c8-108">Klikněte pravým tlačítkem na paralelní větev a poté na položku **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="f32c8-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="f32c8-109">Zobrazí se formulář **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="f32c8-109">The **Properties** form is displayed.</span></span>
2. <span data-ttu-id="f32c8-110">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="f32c8-110">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="f32c8-111">V poli **Název** zadejte jedinečný název paralelní větve.</span><span class="sxs-lookup"><span data-stu-id="f32c8-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4. <span data-ttu-id="f32c8-112">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="f32c8-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="f32c8-113">Navrhněte a konfigurujte prvky větve</span><span class="sxs-lookup"><span data-stu-id="f32c8-113">Design and configure the elements of a branch</span></span>

<span data-ttu-id="f32c8-114">Pomocí následujících kroků navrhněte a nakonfigurujte prvky této paralelní větve.</span><span class="sxs-lookup"><span data-stu-id="f32c8-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>

1. <span data-ttu-id="f32c8-115">Dvakrát klikněte na paralelní větev.</span><span class="sxs-lookup"><span data-stu-id="f32c8-115">Double-click the parallel branch.</span></span>
2. <span data-ttu-id="f32c8-116">Přetáhněte prvky workflowu na plátno a nakonfigurujte prvky, jako byste chtěli vytvořit jakýkoliv jiný workflow.</span><span class="sxs-lookup"><span data-stu-id="f32c8-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="f32c8-117">Další informace naleznete v tématu [Vytvoření workflowu](create-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="f32c8-117">For more information, see [Create a workflow](create-workflow.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f32c8-118">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="f32c8-118">Additional resources</span></span>

[<span data-ttu-id="f32c8-119">Vytvoření workflow</span><span class="sxs-lookup"><span data-stu-id="f32c8-119">Create a workflow</span></span>](create-workflow.md)
