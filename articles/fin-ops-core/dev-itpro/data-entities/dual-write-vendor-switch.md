---
title: Přepínání mezi návrhy dodavatele
description: ''
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772357"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="86b03-102">Přepínání mezi návrhy dodavatele</span><span class="sxs-lookup"><span data-stu-id="86b03-102">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="86b03-103">Tok dat dodavatele</span><span class="sxs-lookup"><span data-stu-id="86b03-103">Vendor data flow</span></span> 

<span data-ttu-id="86b03-104">Pokud chcete použít další aplikace Dynamics 365 pro hlavní řízení dodavatele a chcete izolovat informace o dodavateli od zákazníků, použijte tento základní návrh dodavatele.</span><span class="sxs-lookup"><span data-stu-id="86b03-104">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Základní tok dodavatele](media/dual-write-switch-1.png)
 
<span data-ttu-id="86b03-106">Pokud chcete použít další aplikace Dynamics 365 pro hlavní řízení dodavatele a chcete pokračovat v používání entity **Účet** pro ukládání informací o dodavateli, můžete použít tento rozšířený návrh dodavatele.</span><span class="sxs-lookup"><span data-stu-id="86b03-106">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="86b03-107">V tomto návrhu jsou rozšířené informace o dodavateli, jako je například stav blokovaných dodavatelů a profil dodavatele, uloženy v entitě **dodavatelé** v Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="86b03-107">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Rozšířený tok dodavatele](media/dual-write-switch-2.png)
 
<span data-ttu-id="86b03-109">Chcete-li použít rozšířený návrh dodavatele, postupujte podle následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="86b03-109">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="86b03-110">Balíček řešení **SupplyChainCommon** obsahuje šablony procesu workflow, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="86b03-110">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="86b03-111">![Šablony procesu workflow](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="86b03-111">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="86b03-112">Vytvoření nových procesů workflowu pomocí šablon procesů workflowu:</span><span class="sxs-lookup"><span data-stu-id="86b03-112">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="86b03-113">Vytvořte nový proces workflowu pro entitu **Dodavatel** pomocí šablony procesu workflowu **Vytvořit dodavatele v entitě účtu** a klikněte na **OK**.</span><span class="sxs-lookup"><span data-stu-id="86b03-113">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="86b03-114">Tento workflow zpracovává scénář vytvoření dodavatele pro entitu **Účet**.</span><span class="sxs-lookup"><span data-stu-id="86b03-114">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="86b03-115">![Vytvořit dodavatele v entitě účet](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="86b03-115">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="86b03-116">Vytvořte nový proces workflowu pro entitu **Dodavatel** pomocí šablony procesu workflowu **Aktualizovat entitu účtu** a klikněte na **OK**.</span><span class="sxs-lookup"><span data-stu-id="86b03-116">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="86b03-117">Tento workflow zpracovává scénář aktualizace dodavatele pro entitu **Účet**.</span><span class="sxs-lookup"><span data-stu-id="86b03-117">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="86b03-118">![Aktualizovat entitu Účty](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="86b03-118">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="86b03-119">Vytvoření nových procesů workflowu ze šablon vytvořených v entitě **Účty**.</span><span class="sxs-lookup"><span data-stu-id="86b03-119">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="86b03-120">![Vytvoření dodavatelů v entitě dodavatelů](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="86b03-120">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="86b03-121">![Aktualizovat entitu dodavatelů](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="86b03-121">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="86b03-122">Pracovní postupy můžete konfigurovat jako pracovní postupy v reálném čase nebo na pozadí na základě vašich požadavků.</span><span class="sxs-lookup"><span data-stu-id="86b03-122">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="86b03-123">![Převod do workflowu na pozadí](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="86b03-123">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="86b03-124">Aktivujte workflowy, které jste vytvořili v entitách **Účet** a **Dodavatel**, abyste mohli začít používat entitu **Účet** Customer Engagement k ukládání informací o dodavateli.</span><span class="sxs-lookup"><span data-stu-id="86b03-124">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the Customer Engagement **Account** entity for storing vendor information.</span></span> 
 
