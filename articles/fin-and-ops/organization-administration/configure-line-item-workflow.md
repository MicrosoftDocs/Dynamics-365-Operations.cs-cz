---
title: "Konfigurace workflowu položky řádku"
description: "Toto téma vysvětluje, jak nakonfigurovat prvek workflowu položky řádku."
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1d36ec599250f62c523e8d538a37cada9b223007
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="configure-a-line-item-workflow"></a><span data-ttu-id="841f4-103">Konfigurace workflowu položky řádku</span><span class="sxs-lookup"><span data-stu-id="841f4-103">Configure a line-item workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="841f4-104">Toto téma vysvětluje, jak nakonfigurovat prvek workflowu položky řádku.</span><span class="sxs-lookup"><span data-stu-id="841f4-104">This topic explains how to configure a line-item workflow element.</span></span>

<span data-ttu-id="841f4-105">Pokud budete chtít nakonfigurovat prvek workflow položky řádku v editoru workflowu, klikněte pravým tlačítkem myši na ruční rozhodnutí a kliknutím na tlačítko **Vlastnosti** otevřete stránku **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="841f4-105">To configure a line-item workflow element, in the workflow editor, right-click the element, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="841f4-106">Pro konfiguraci vlastností prvku workflowu položky řádky můžete použít následující kroky.</span><span class="sxs-lookup"><span data-stu-id="841f4-106">Then use the following procedures to configure the properties of the line-item workflow element.</span></span>

## <a name="name-the-line-item-workflow-element"></a><span data-ttu-id="841f4-107">Pojmenování prvku workflowu položky řádku</span><span class="sxs-lookup"><span data-stu-id="841f4-107">Name the line-item workflow element</span></span>
<span data-ttu-id="841f4-108">Pomocí následujících kroků zadejte název prvku workflowu položky řádky.</span><span class="sxs-lookup"><span data-stu-id="841f4-108">Follow these steps to enter a name for the line-item workflow element.</span></span>

1.  <span data-ttu-id="841f4-109">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="841f4-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="841f4-110">V poli **Název** zadejte jedinečný název prvku workflowu položky řádky.</span><span class="sxs-lookup"><span data-stu-id="841f4-110">In the **Name** field, enter a unique name for the line-item workflow element.</span></span>

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a><span data-ttu-id="841f4-111">Určení, zda se jeden workflow používá ke zpracování všech položek řádku</span><span class="sxs-lookup"><span data-stu-id="841f4-111">Specify whether the same workflow is used to process all line items</span></span>
<span data-ttu-id="841f4-112">Tento postup slouží k určení, zda stejný workflow slouží ke zpracování všech položek řádku v dokumentu.</span><span class="sxs-lookup"><span data-stu-id="841f4-112">Follow these steps to specify whether the same workflow is used to process all the line items on a document.</span></span>

1.  <span data-ttu-id="841f4-113">V levém podokně klepněte na tlačítko **Základní nastavení**.</span><span class="sxs-lookup"><span data-stu-id="841f4-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="841f4-114">Pokud by měl stejný workflow zpracovávat všechny položky řádku v dokumentu, klepněte na tlačítko **Vyvolat jediný workflow pro všechny položky řádku**.</span><span class="sxs-lookup"><span data-stu-id="841f4-114">If the same workflow should process all the line items on a document, click **Invoke a single workflow for all line-items**.</span></span> <span data-ttu-id="841f4-115">Potom vyberte workflow, který slouží ke zpracování položek řádku.</span><span class="sxs-lookup"><span data-stu-id="841f4-115">Then select the workflow to use to process the line items.</span></span>
3.  <span data-ttu-id="841f4-116">Pokud má konkrétní workflow zpracovávat položky řádku, které splňují konkrétní sadu podmínek, klepněte na **Vyvolat workflow pro každou položku řádku**.</span><span class="sxs-lookup"><span data-stu-id="841f4-116">If a specific workflow should process line items that meet a specific set of conditions, click **Invoke a workflow for each line-item**.</span></span> <span data-ttu-id="841f4-117">Podle následujícího postupu určete sadu podmínek:</span><span class="sxs-lookup"><span data-stu-id="841f4-117">Then follow these steps to define the set of conditions:</span></span>
    1.  <span data-ttu-id="841f4-118">Klepněte na možnost **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="841f4-118">Click **Add**.</span></span>
    2.  <span data-ttu-id="841f4-119">V tabulce vyberte podmínku.</span><span class="sxs-lookup"><span data-stu-id="841f4-119">Select the condition in the table.</span></span>
    3.  <span data-ttu-id="841f4-120">Na kartě **Název podmínky** zadejte název sady podmínek, které definujete.</span><span class="sxs-lookup"><span data-stu-id="841f4-120">On the **Condition name** tab, enter a name for the set of conditions that you're defining.</span></span>
    4.  <span data-ttu-id="841f4-121">Klepněte na volbu **Přidat podmínku** a zadejte podmínku.</span><span class="sxs-lookup"><span data-stu-id="841f4-121">Click **Add condition** to enter a condition.</span></span>
    5.  <span data-ttu-id="841f4-122">Zadejte všechny další podmínky, které jsou požadovány.</span><span class="sxs-lookup"><span data-stu-id="841f4-122">Enter any additional conditions that are required.</span></span>
    6.  <span data-ttu-id="841f4-123">Chcete-li ověřit, zda je zadaná sada podmínek nakonfigurována správně, klepněte na možnost **Testovací podmínka**.</span><span class="sxs-lookup"><span data-stu-id="841f4-123">To verify that the set of conditions that you entered is configured correctly, click **Test**.</span></span> <span data-ttu-id="841f4-124">Na stránce **Podmínka testovacího workflowu** v oblasti **Ověřit podmínku** vyberte záznam a klikněte na **Test**.</span><span class="sxs-lookup"><span data-stu-id="841f4-124">On the **Test workflow condition** page, in the **Validate condition** area, select a record, and then click **Test**.</span></span> <span data-ttu-id="841f4-125">Systém záznam vyhodnotí a určí, zda odpovídá zadaným podmínkám.</span><span class="sxs-lookup"><span data-stu-id="841f4-125">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span> <span data-ttu-id="841f4-126">Klikněte na tlačítko **OK** nebo klepnutím na tlačítko **Storno** se vraťte na stránku **Vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="841f4-126">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

    <span data-ttu-id="841f4-127">Na kartě **Workflow** vyberte workflow, který slouží ke zpracování položek řádků, které vyhovují sadě podmínek, které jste definovali.</span><span class="sxs-lookup"><span data-stu-id="841f4-127">On the **Workflow** tab, select the workflow select the workflow to use to process line items that meet the set of conditions that you defined.</span></span>





