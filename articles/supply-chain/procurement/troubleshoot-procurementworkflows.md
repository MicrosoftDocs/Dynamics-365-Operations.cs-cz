---
title: Řešení problémů s pracovními postupy zásobování a zdrojů
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s pracovními postupy zásobování a zdrojů.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: e8274890c581fffc7330538430c9b2ba060041bc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999096"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a><span data-ttu-id="50190-103">Řešení problémů s pracovními postupy zásobování a zdrojů</span><span class="sxs-lookup"><span data-stu-id="50190-103">Troubleshoot procurement and sourcing workflows</span></span>

<span data-ttu-id="50190-104">Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s pracovními postupy zásobování a zdrojů.</span><span class="sxs-lookup"><span data-stu-id="50190-104">This topic describes how to fix issues that you might encounter while you work with procurement and sourcing workflows.</span></span>

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a><span data-ttu-id="50190-105">Chyba při opětovném odeslání nákupní objednávky do pracovního postupu po změně: „Změny nákupní objednávky X jsou povoleny pouze ve stavu konceptu, když je aktivována správa změn“</span><span class="sxs-lookup"><span data-stu-id="50190-105">Error when re-submitting a purchase order to the workflow after a change: "Changes to purchase order X are allowed only in a Draft state when change management is activated"</span></span>

<span data-ttu-id="50190-106">K tomuto problému dochází, pouze pokud byla nákupní objednávka ve stavu *Potvrzeno* před požadováním změn.</span><span class="sxs-lookup"><span data-stu-id="50190-106">This issue occurs only if the purchase order was in a *Confirmed* state before you requested changes.</span></span> <span data-ttu-id="50190-107">Pokud požadujete změny, když je objednávka ve stavu *Schváleno*, lze pracovní postup úspěšně zpracovat.</span><span class="sxs-lookup"><span data-stu-id="50190-107">If you request changes while the purchase order is in an *Approved* state, the workflow can be processed successfully.</span></span>

### <a name="error-description"></a><span data-ttu-id="50190-108">Popis chyby</span><span class="sxs-lookup"><span data-stu-id="50190-108">Error description</span></span>

<span data-ttu-id="50190-109">Při opakovaném odeslání nákupní objednávky po změně dojde v pracovním postupu k následující chybě:</span><span class="sxs-lookup"><span data-stu-id="50190-109">The following error occurs in the workflow when a purchase order is resubmitted after a change:</span></span>

> <span data-ttu-id="50190-110">Zastaveno (chyba): Výjimka X++: Změny nákupní objednávky PO0000569 jsou povoleny pouze ve stavu Koncept, když je aktivována správa změn na</span><span class="sxs-lookup"><span data-stu-id="50190-110">Stopped (error): X++ Exception: Changes to purchase order PO0000569 are only allowed in state Draft when change management is activated at</span></span><br>
<span data-ttu-id="50190-111">SysWorkflowParticipantProvider-resolve</span><span class="sxs-lookup"><span data-stu-id="50190-111">SysWorkflowParticipantProvider-resolve</span></span><br>
<span data-ttu-id="50190-112">SysWorkflowParticipantProvider-resolveParticipants</span><span class="sxs-lookup"><span data-stu-id="50190-112">SysWorkflowParticipantProvider-resolveParticipants</span></span><br>
<span data-ttu-id="50190-113">SysWorkflowServiceProvider-resolveParticipant</span><span class="sxs-lookup"><span data-stu-id="50190-113">SysWorkflowServiceProvider-resolveParticipant</span></span><br>
<span data-ttu-id="50190-114">SysWorkflowQueue-resume</span><span class="sxs-lookup"><span data-stu-id="50190-114">SysWorkflowQueue-resume</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="50190-115">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="50190-115">Issue resolution</span></span>

<span data-ttu-id="50190-116">K tomuto problému může dojít z důvodu nekonzistence v distribucích nákupních objednávek.</span><span class="sxs-lookup"><span data-stu-id="50190-116">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="50190-117">Chcete-li tento problém odblokovat a resetovat nákupní objednávku do stavu *Koncept*, přejděte na **Zásobování a zdroje \> Pravidelné úkoly \> Vyčistit \> Reset distribuce nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="50190-117">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="50190-118">Další informace najdete v následujícím příspěvku na blogu: [Řešení chyb distribuce nákupní objednávky v Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="50190-118">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

<span data-ttu-id="50190-119">Problém bude vyřešen prostřednictvím [tohoto článku znalostní báze Microsoft](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span><span class="sxs-lookup"><span data-stu-id="50190-119">The issue will be fixed through [this Microsoft Knowledge Base (KB) article](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="50190-120">Jedno nebo více rozúčtování je nadměrně distribuováno nebo nedostatečně distribuováno.</span><span class="sxs-lookup"><span data-stu-id="50190-120">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

<span data-ttu-id="50190-121">K tomuto problému může dojít z důvodu nekonzistence v distribucích nákupních objednávek.</span><span class="sxs-lookup"><span data-stu-id="50190-121">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="50190-122">Chcete-li tento problém odblokovat a resetovat nákupní objednávku do stavu *Koncept*, přejděte na **Zásobování a zdroje \> Pravidelné úkoly \> Vyčistit \> Reset distribuce nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="50190-122">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="50190-123">Další informace najdete v následujícím příspěvku na blogu: [Řešení chyb distribuce nákupní objednávky v Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="50190-123">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a><span data-ttu-id="50190-124">Pokud je zbytek dodávky zrušen u nákupní objednávky, kde je zapnuta správa změn, přejde nákupní objednávka do stavu Potvrzeno.</span><span class="sxs-lookup"><span data-stu-id="50190-124">If a delivery remainder is canceled on a purchase order where change management is turned on, the purchase order goes to a Confirmed state.</span></span>

### <a name="issue-description"></a><span data-ttu-id="50190-125">Popis problému</span><span class="sxs-lookup"><span data-stu-id="50190-125">Issue description</span></span>

<span data-ttu-id="50190-126">Pokud je u nákupní objednávky, která podléhá správě změn, jedinou požadovanou změnou zrušení zbytku dodávky na jednom nebo více řádcích, přejde nákupní objednávka přímo do stavu *Potvrzeno*, když je schválena, a nebude vytvořen žádný deník.</span><span class="sxs-lookup"><span data-stu-id="50190-126">For a purchase order that is subject to change management, if the only change that is requested is the cancellation of a delivery remainder on one or more of the lines, the purchase order will go directly to a *Confirmed* state when it's approved, and no journal will be created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="50190-127">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="50190-127">Issue resolution</span></span>

<span data-ttu-id="50190-128">Zrušení zbytku dodávky nemá vliv na obsah deníku potvrzení.</span><span class="sxs-lookup"><span data-stu-id="50190-128">Cancellation of a delivery remainder doesn't affect the contents of the confirmation journal.</span></span> <span data-ttu-id="50190-129">Tato funkce by měla být použita, když byl řádek částečně přijat, a zbývající kvalita by měla být zrušena v kroku procesu po potvrzení nákupní objednávky u dodavatele.</span><span class="sxs-lookup"><span data-stu-id="50190-129">This functionality should be used when the line has been partially received, and the remainder quality should be canceled in the process step after the purchase order has been confirmed with the vendor.</span></span>

<span data-ttu-id="50190-130">Pokud by se to mělo projevit v potvrzení nákupní objednávky, mělo by být množství upraveno na řádku nákupní objednávky tak, aby bylo vyžadováno potvrzení.</span><span class="sxs-lookup"><span data-stu-id="50190-130">If this should be reflected on the purchase order confirmation, the quantity should be adjusted on the purchase order line so that the confirmation will be required.</span></span> <span data-ttu-id="50190-131">Popřípadě pokud na řádku nic nebylo přijato, lze množství odebrat.</span><span class="sxs-lookup"><span data-stu-id="50190-131">Alternatively, if nothing has been received on the line, the quantity can be removed.</span></span> <span data-ttu-id="50190-132">V takovém případě bude vyžadováno opětovné potvrzení.</span><span class="sxs-lookup"><span data-stu-id="50190-132">In this case, reconfirmation will be required.</span></span>

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a><span data-ttu-id="50190-133">Zrušené nákupní objednávky se zobrazí v seznamu konceptů v pracovním prostoru Příprava nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="50190-133">Canceled purchase orders appear in the draft list in the Purchase order preparation workspace.</span></span>

### <a name="issue-description"></a><span data-ttu-id="50190-134">Popis problému</span><span class="sxs-lookup"><span data-stu-id="50190-134">Issue description</span></span>

<span data-ttu-id="50190-135">Po zrušení nákupních objednávek, které byly ve stavu *Potvrzeno* se zrušené nákupní objednávky stále zobrazují v seznamu konceptů nákupních objednávek v pracovním prostoru **Příprava nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="50190-135">After you cancel purchase orders that were in a *Confirmed* state, the canceled purchase orders still appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="50190-136">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="50190-136">Issue resolution</span></span>

<span data-ttu-id="50190-137">K tomuto problému dochází pouze u nákupních objednávek, které podléhají správě změn.</span><span class="sxs-lookup"><span data-stu-id="50190-137">This issue occurs only for purchase orders that are subject to change management.</span></span> <span data-ttu-id="50190-138">Dochází k tomu, protože zrušení je považováno za změnu, kterou je nutné schválit.</span><span class="sxs-lookup"><span data-stu-id="50190-138">It occurs because the cancellation is considered a change that must be approved.</span></span> <span data-ttu-id="50190-139">Schválení může být provedeno automaticky systémem.</span><span class="sxs-lookup"><span data-stu-id="50190-139">The approval can be done automatically by the system.</span></span> <span data-ttu-id="50190-140">Proto je procesem odeslání zrušené nákupní objednávky do pracovního postupu schválení, aby mohla přejít do stavu *Schváleno*.</span><span class="sxs-lookup"><span data-stu-id="50190-140">Therefore, the process is to submit the canceled purchase order to the approval workflow so that it can go to an *Approved* state.</span></span> <span data-ttu-id="50190-141">V tomto okamžiku se nákupní objednávka již nebude zobrazovat v seznamu konceptů nákupních objednávek v pracovním prostoru **Příprava nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="50190-141">At that point, the purchase order will no longer appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

