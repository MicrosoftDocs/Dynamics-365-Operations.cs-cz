---
title: Přepínání mezi návrhy dodavatele
description: Tohle téma popisuje způsob přepínání integrace dat dodavatele mezi aplikacemi Finance and Operations a Common Data Service.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 0ecc401706911f8b92146b95bb6415185df8b451
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997545"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="a2657-103">Přepínání mezi návrhy dodavatele</span><span class="sxs-lookup"><span data-stu-id="a2657-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="a2657-104">Tok dat dodavatele</span><span class="sxs-lookup"><span data-stu-id="a2657-104">Vendor data flow</span></span> 

<span data-ttu-id="a2657-105">Pokud se rozhodnete použít entitu **Účet** k ukládání dodavatelů typu **Organizace** a entitu **Kontakt** k ukládání dodavatelů typu **Osoba** , nakonfigurujte následující workflowy.</span><span class="sxs-lookup"><span data-stu-id="a2657-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="a2657-106">V opačném případě není tato konfigurace nutná.</span><span class="sxs-lookup"><span data-stu-id="a2657-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="a2657-107">Použití rozšířeného návrhu dodavatele pro dodavatele typu Organizace</span><span class="sxs-lookup"><span data-stu-id="a2657-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="a2657-108">Balíček řešení **Dynamics365FinanceExtended** obsahuje následující šablony procesu workflowu.</span><span class="sxs-lookup"><span data-stu-id="a2657-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="a2657-109">Pro každou šablonu vytvoříte workflow.</span><span class="sxs-lookup"><span data-stu-id="a2657-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="a2657-110">Vytvořte dodavatele v entitě Účty.</span><span class="sxs-lookup"><span data-stu-id="a2657-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="a2657-111">Vytvořte dodavatele v entitě Dodavatelé.</span><span class="sxs-lookup"><span data-stu-id="a2657-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="a2657-112">Aktualizujte dodavatele v entitě Účty.</span><span class="sxs-lookup"><span data-stu-id="a2657-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="a2657-113">Aktualizujte dodavatele v entitě Dodavatelé.</span><span class="sxs-lookup"><span data-stu-id="a2657-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="a2657-114">Pro vytvoření nových procesů workflowu pomocí šablon procesů workflowu postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="a2657-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="a2657-115">Vytvořte proces workflowu pro entitu **Dodavatel** a vyberte šablonu procesu workflowu **Vytvoření dodavatelů v entitě Účty**.</span><span class="sxs-lookup"><span data-stu-id="a2657-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="a2657-116">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2657-116">Then select **OK**.</span></span> <span data-ttu-id="a2657-117">Tento workflow zpracovává scénář vytvoření dodavatele pro entitu **Účet**.</span><span class="sxs-lookup"><span data-stu-id="a2657-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![Proces workflowu Vytvoření dodavatelů v entitě Účty](media/create_process.png)

2. <span data-ttu-id="a2657-119">Vytvořte proces workflowu pro entitu **Dodavatel** a vyberte šablonu procesu workflowu **Aktualizace dodavatelů v entitě Účty**.</span><span class="sxs-lookup"><span data-stu-id="a2657-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="a2657-120">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2657-120">Then select **OK**.</span></span> <span data-ttu-id="a2657-121">Tento workflow zpracovává scénář aktualizace dodavatele pro entitu **Účet**.</span><span class="sxs-lookup"><span data-stu-id="a2657-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="a2657-122">Vytvořte proces workflowu pro entitu **Účet** a vyberte šablonu procesu workflowu **Vytvoření dodavatelů v entitě Dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="a2657-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="a2657-123">Vytvořte proces workflowu pro entitu **Účet** a vyberte šablonu procesu workflowu **Aktualizace dodavatelů v entitě Dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="a2657-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="a2657-124">Pracovní postupy můžete konfigurovat buď jako workflowy v reálném čase nebo na pozadí v závislosti na vašich požadavcích.</span><span class="sxs-lookup"><span data-stu-id="a2657-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="a2657-125">Chcete-li nakonfigurovat workflow jako workflow na pozadí, vyberte možnost **Převést na workflow na pozadí**.</span><span class="sxs-lookup"><span data-stu-id="a2657-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Tlačítko Převést na workflow na pozadí](media/background_workflow.png)

6. <span data-ttu-id="a2657-127">Aktivujte workflowy, které jste vytvořili pro entity **Účet** a **Dodavatel** , abyste mohli začít používat entitu **Účet** k ukládání informací pro dodavatele typu **Organizace**.</span><span class="sxs-lookup"><span data-stu-id="a2657-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="a2657-128">Použití rozšířeného návrhu dodavatele pro dodavatele typu Osoba</span><span class="sxs-lookup"><span data-stu-id="a2657-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="a2657-129">Balíček řešení **Dynamics365FinanceExtended** obsahuje následující šablony procesu workflowu.</span><span class="sxs-lookup"><span data-stu-id="a2657-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="a2657-130">Pro každou šablonu vytvoříte workflow.</span><span class="sxs-lookup"><span data-stu-id="a2657-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="a2657-131">V entitě Dodavatelé vytvořte dodavatele typu Osoba.</span><span class="sxs-lookup"><span data-stu-id="a2657-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="a2657-132">V entitě Kontakty vytvořte dodavatele typu Osoba.</span><span class="sxs-lookup"><span data-stu-id="a2657-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="a2657-133">V entitě Kontakty aktualizujte dodavatele typu Osoba.</span><span class="sxs-lookup"><span data-stu-id="a2657-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="a2657-134">V entitě Dodavatelé aktualizujte dodavatele typu Osoba.</span><span class="sxs-lookup"><span data-stu-id="a2657-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="a2657-135">Pro vytvoření nových procesů workflowu pomocí šablon procesů workflowu postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="a2657-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="a2657-136">Vytvořte proces workflowu pro entitu **Dodavatel** a vyberte šablonu procesu workflowu **Vytvoření dodavatelů typu Osoba v entitě Kontakty**.</span><span class="sxs-lookup"><span data-stu-id="a2657-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="a2657-137">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2657-137">Then select **OK**.</span></span> <span data-ttu-id="a2657-138">Tento workflow zpracovává scénář vytvoření dodavatele pro entitu **Kontakt**.</span><span class="sxs-lookup"><span data-stu-id="a2657-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="a2657-139">Vytvořte proces workflowu pro entitu **Dodavatel** a vyberte šablonu procesu workflowu **Aktualizace dodavatelů typu Osoba v entitě Kontakty**.</span><span class="sxs-lookup"><span data-stu-id="a2657-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="a2657-140">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2657-140">Then select **OK**.</span></span> <span data-ttu-id="a2657-141">Tento workflow zpracovává scénář aktualizace dodavatele pro entitu **Kontakt**.</span><span class="sxs-lookup"><span data-stu-id="a2657-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="a2657-142">Vytvořte proces workflowu pro entitu **Kontakt** a vyberte šablonu **Vytvoření dodavatelů typu Osoba v entitě Dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="a2657-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="a2657-143">Vytvořte proces workflowu pro entitu **Kontakt** a vyberte šablonu **Aktualizace dodavatelů typu Osoba v entitě Dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="a2657-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="a2657-144">Pracovní postupy můžete konfigurovat buď jako workflowy v reálném čase nebo na pozadí v závislosti na vašich požadavcích.</span><span class="sxs-lookup"><span data-stu-id="a2657-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="a2657-145">Chcete-li nakonfigurovat workflow jako workflow na pozadí, vyberte možnost **Převést na workflow na pozadí**.</span><span class="sxs-lookup"><span data-stu-id="a2657-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="a2657-146">Aktivujte workflowy, které jste vytvořili v entitách **Kontakt** a **Dodavatel** , abyste mohli začít používat entitu **Kontakt** k ukládání informací pro dodavatele typu **Osoba**.</span><span class="sxs-lookup"><span data-stu-id="a2657-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
