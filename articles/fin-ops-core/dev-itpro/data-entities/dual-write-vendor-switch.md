---
title: Přepínání mezi návrhy dodavatele
description: Toto téma popisuje způsob přepínání mezi integrací dat dodavatele mezi aplikacemi Finance and Operations a Common Data Service.
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
ms.openlocfilehash: 204d788e72e79e7acf744d24cbeacb0f9b47da7d
ms.sourcegitcommit: 3306e451f04df01c51d8d332306b135d8ae1e254
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/09/2019
ms.locfileid: "2902718"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="12162-103">Přepínání mezi návrhy dodavatele</span><span class="sxs-lookup"><span data-stu-id="12162-103">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="12162-104">Tok dat dodavatele</span><span class="sxs-lookup"><span data-stu-id="12162-104">Vendor data flow</span></span> 

<span data-ttu-id="12162-105">Pokud chcete použít další aplikace Dynamics 365 pro hlavní řízení dodavatele a chcete izolovat informace o dodavateli od zákazníků, použijte tento základní návrh dodavatele.</span><span class="sxs-lookup"><span data-stu-id="12162-105">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Základní tok dodavatele](media/dual-write-vendor-data-flow.png)
 
<span data-ttu-id="12162-107">Pokud chcete použít další aplikace Dynamics 365 pro hlavní řízení dodavatele a chcete pokračovat v používání entity **Účet** pro ukládání informací o dodavateli, můžete použít tento rozšířený návrh dodavatele.</span><span class="sxs-lookup"><span data-stu-id="12162-107">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="12162-108">V tomto návrhu jsou rozšířené informace o dodavateli, jako je například stav blokovaných dodavatelů a profil dodavatele, uloženy v entitě **dodavatelé** v Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="12162-108">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Rozšířený tok dodavatele](media/dual-write-vendor-detail.jpg)
 
<span data-ttu-id="12162-110">Chcete-li použít rozšířený návrh dodavatele, postupujte podle následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="12162-110">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="12162-111">Balíček řešení **SupplyChainCommon** obsahuje šablony procesu workflow, jak je znázorněno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="12162-111">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="12162-112">![Šablony procesu workflow](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="12162-112">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="12162-113">Vytvoření nových procesů workflowu pomocí šablon procesů workflowu:</span><span class="sxs-lookup"><span data-stu-id="12162-113">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="12162-114">Vytvořte nový proces workflowu pro entitu **Dodavatel** pomocí šablony procesu workflowu **Vytvořit dodavatele v entitě účtu** a klikněte na **OK**.</span><span class="sxs-lookup"><span data-stu-id="12162-114">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="12162-115">Tento workflow zpracovává scénář vytvoření dodavatele pro entitu **Účet**.</span><span class="sxs-lookup"><span data-stu-id="12162-115">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="12162-116">![Vytvořit dodavatele v entitě účet](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="12162-116">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="12162-117">Vytvořte nový proces workflowu pro entitu **Dodavatel** pomocí šablony procesu workflowu **Aktualizovat entitu účtu** a klikněte na **OK**.</span><span class="sxs-lookup"><span data-stu-id="12162-117">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="12162-118">Tento workflow zpracovává scénář aktualizace dodavatele pro entitu **Účet**.</span><span class="sxs-lookup"><span data-stu-id="12162-118">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="12162-119">![Aktualizovat entitu Účty](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="12162-119">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="12162-120">Vytvoření nových procesů workflowu ze šablon vytvořených v entitě **Účty**.</span><span class="sxs-lookup"><span data-stu-id="12162-120">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="12162-121">![Vytvoření dodavatelů v entitě dodavatelů](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="12162-121">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="12162-122">![Aktualizovat entitu dodavatelů](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="12162-122">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="12162-123">Pracovní postupy můžete konfigurovat jako pracovní postupy v reálném čase nebo na pozadí na základě vašich požadavků.</span><span class="sxs-lookup"><span data-stu-id="12162-123">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="12162-124">![Převod do workflowu na pozadí](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="12162-124">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="12162-125">Aktivujte workflowy, které jste vytvořili v entitách **Účet** a **Dodavatel**, abyste mohli začít používat entitu **Účet** k ukládání informací o dodavateli.</span><span class="sxs-lookup"><span data-stu-id="12162-125">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the **Account** entity for storing vendor information.</span></span> 
 
