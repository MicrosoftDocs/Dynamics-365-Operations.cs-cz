---
title: Typy požadavků na údržbu
description: Toto téma vysvětluje, jak nastavit stavy životního cyklu požadavků na údržbu v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19d529df6c8aab036de59502b4f14101e1a07707
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790473"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="22326-103">Typy požadavků na údržbu</span><span class="sxs-lookup"><span data-stu-id="22326-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="22326-104">Typy požadavků údržby slouží ke kategorizaci požadavků na údržbu.</span><span class="sxs-lookup"><span data-stu-id="22326-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="22326-105">Můžete mít například typy požadavků na údržbu, které souvisejí s preventivní údržbou a opravnou údržbou.</span><span class="sxs-lookup"><span data-stu-id="22326-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="22326-106">Nebo můžete mít speciální typ požadavku na údržbu, který se používá ke správě opravy majetku (oprava skladu).</span><span class="sxs-lookup"><span data-stu-id="22326-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="22326-107">Typ požadavku údržby definuje příslušnost ke skupině stavů životního cyklu požadavků na údržbu (model životního cyklu údržby).</span><span class="sxs-lookup"><span data-stu-id="22326-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="22326-108">Modely životního cyklu požadavků údržby definují stavy životního cyklu, které lze nastavit pro požadavek údržby.</span><span class="sxs-lookup"><span data-stu-id="22326-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="22326-109">(Příklady stavů životního cyklu požadavků na údržbu zahrnují **Vytvořené** **Aktivní** a **Ukončené**.)</span><span class="sxs-lookup"><span data-stu-id="22326-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="22326-110">Vyberte **Správa majetku** \> **Nastavení** \> **Požadavky na údržbu** \> **Typy požadavků na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="22326-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="22326-111">Zvolte **Nový** pro vytvoření typu životního cyklu požadavku na údržbu.</span><span class="sxs-lookup"><span data-stu-id="22326-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="22326-112">V poli **Typy požadavků na údržbu** zadejte ID pro typ požadavku údržby.</span><span class="sxs-lookup"><span data-stu-id="22326-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="22326-113">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="22326-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="22326-114">Na kartě **Obecné** v poli **Model životního cyklu požadavků údržby** vyberte model životního cyklu požadavků údržby.</span><span class="sxs-lookup"><span data-stu-id="22326-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="22326-115">V poli **Typ pracovního příkazu** vyberte typ pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="22326-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="22326-116">Když je požadavek na údržbu převeden na pracovní příkaz, pracovní příkaz automaticky získá typ pracovního příkazu, který souvisí s typem požadavku údržby.</span><span class="sxs-lookup"><span data-stu-id="22326-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="22326-117">Následující ilustrace znázorňuje příklad stránky **Typy požadavků na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="22326-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![Obrázek č. 1](media/07-setup-for-requests.png)
