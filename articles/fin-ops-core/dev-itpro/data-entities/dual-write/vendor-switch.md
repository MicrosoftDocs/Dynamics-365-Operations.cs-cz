---
title: Přepínání mezi návrhy dodavatele
description: Tohle téma popisuje způsob přepínání integrace dat dodavatele mezi aplikacemi Finance and Operations a Dataverse.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5a18fed2eac4c120dca20a1d7797d047639275b9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750587"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="0c3a1-103">Přepínání mezi návrhy dodavatele</span><span class="sxs-lookup"><span data-stu-id="0c3a1-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="0c3a1-104">Tok dat dodavatele</span><span class="sxs-lookup"><span data-stu-id="0c3a1-104">Vendor data flow</span></span> 

<span data-ttu-id="0c3a1-105">Pokud se rozhodnete použít tabulku **Účet** k ukládání dodavatelů typu **Organizace** a tabulku **Kontakt** k ukládání dodavatelů typu **Osoba**, nakonfigurujte následující workflowy.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-105">If you choose to use the **Account** table to store vendors of the **Organization** type and the **Contact** table to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="0c3a1-106">V opačném případě není tato konfigurace nutná.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="0c3a1-107">Použití rozšířeného návrhu dodavatele pro dodavatele typu Organizace</span><span class="sxs-lookup"><span data-stu-id="0c3a1-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="0c3a1-108">Balíček řešení **Dynamics365FinanceExtended** obsahuje následující šablony procesu workflowu.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="0c3a1-109">Pro každou šablonu vytvoříte workflow.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="0c3a1-110">Vytvoření dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="0c3a1-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="0c3a1-111">Vytvoření dodavatelů v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="0c3a1-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="0c3a1-112">Aktualizace dodavatelů v tabulce Účty</span><span class="sxs-lookup"><span data-stu-id="0c3a1-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="0c3a1-113">Aktualizace dodavatelů v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="0c3a1-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="0c3a1-114">Pro vytvoření nových procesů workflowu pomocí šablon procesů workflowu postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="0c3a1-115">Vytvořte proces pracovního postupu pro tabulku **Dodavatel** a vyberte šablonu procesu pracovního postupu **Vytvoření dodavatelů v tabulce Účty**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-115">Create a workflow process for the **Vendor** table, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="0c3a1-116">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-116">Then select **OK**.</span></span> <span data-ttu-id="0c3a1-117">Tento workflow zpracovává scénář vytvoření dodavatele pro tabulku **Účet**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-117">This workflow handles the vendor creation scenario for the **Account** table.</span></span>

    ![Proces pracovního postupu Vytvoření dodavatelů v tabulce Účty](media/create_process.png)

2. <span data-ttu-id="0c3a1-119">Vytvořte proces pracovního postupu pro tabulku **Dodavatel** a vyberte šablonu procesu pracovního postupu **Aktualizace dodavatelů v tabulce Účty**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-119">Create a workflow process for the **Vendor** table, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="0c3a1-120">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-120">Then select **OK**.</span></span> <span data-ttu-id="0c3a1-121">Tento workflow zpracovává scénář aktualizace dodavatele pro tabulku **Účet**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-121">This workflow handles the vendor update scenario for the **Account** table.</span></span>
3. <span data-ttu-id="0c3a1-122">Vytvořte proces pracovního postupu pro tabulku **Účet** a vyberte šablonu procesu pracovního postupu **Vytvoření dodavatelů v tabulce Dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-122">Create a workflow process for the **Account** table, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="0c3a1-123">Vytvořte proces pracovního postupu pro tabulku **Účet** a vyberte šablonu procesu pracovního postupu **Aktualizace dodavatelů v tabulce Dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-123">Create a workflow process for the **Account** table, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="0c3a1-124">Pracovní postupy můžete konfigurovat buď jako workflowy v reálném čase nebo na pozadí v závislosti na vašich požadavcích.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="0c3a1-125">Chcete-li nakonfigurovat workflow jako workflow na pozadí, vyberte možnost **Převést na workflow na pozadí**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![Tlačítko Převést na workflow na pozadí](media/background_workflow.png)

6. <span data-ttu-id="0c3a1-127">Aktivujte pracovní postupy, které jste vytvořili pro tabulky **Účet** a **Dodavatel**, abyste mohli začít používat tabulku **Účet** k ukládání informací pro dodavatele typu **Organizace**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** table to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="0c3a1-128">Použití rozšířeného návrhu dodavatele pro dodavatele typu Osoba</span><span class="sxs-lookup"><span data-stu-id="0c3a1-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="0c3a1-129">Balíček řešení **Dynamics365FinanceExtended** obsahuje následující šablony procesu workflowu.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="0c3a1-130">Pro každou šablonu vytvoříte workflow.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="0c3a1-131">Vytvoření dodavatelů typu Osoba v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="0c3a1-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="0c3a1-132">Vytvoření dodavatelů typu Osoba v tabulce Kontakty</span><span class="sxs-lookup"><span data-stu-id="0c3a1-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="0c3a1-133">Aktualizace dodavatelů typu Osoba v tabulce Kontakty</span><span class="sxs-lookup"><span data-stu-id="0c3a1-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="0c3a1-134">Aktualizace dodavatelů typu Osoba v tabulce Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="0c3a1-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="0c3a1-135">Pro vytvoření nových procesů workflowu pomocí šablon procesů workflowu postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="0c3a1-136">Vytvořte proces pracovního postupu pro tabulku **Dodavatel** a vyberte šablonu procesu pracovního postupu **Vytvoření dodavatelů typu Osoba v tabulce Kontakty**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-136">Create a workflow process for the **Vendor** table, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="0c3a1-137">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-137">Then select **OK**.</span></span> <span data-ttu-id="0c3a1-138">Tento workflow zpracovává scénář vytvoření dodavatele pro tabulku **Kontakt**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-138">This workflow handles the vendor creation scenario for the **Contact** table.</span></span>
2. <span data-ttu-id="0c3a1-139">Vytvořte proces pracovního postupu pro tabulku **Dodavatel** a vyberte šablonu procesu pracovního postupu **Aktualizace dodavatelů typu Osoba v tabulce Kontakty**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-139">Create a workflow process for the **Vendor** table, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="0c3a1-140">Pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-140">Then select **OK**.</span></span> <span data-ttu-id="0c3a1-141">Tento workflow zpracovává scénář aktualizace dodavatele pro tabulku **Kontakt**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-141">This workflow handles the vendor update scenario for the **Contact** table.</span></span>
3. <span data-ttu-id="0c3a1-142">Vytvořte proces pracovního postupu pro tabulku **Kontakt** a vyberte šablonu **Vytvoření dodavatelů typu Osoba v tabulce Dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-142">Create a workflow process for the **Contact** table, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="0c3a1-143">Vytvořte proces pracovního postupu pro tabulku **Kontakt** a vyberte šablonu **Aktualizace dodavatelů typu Osoba v tabulce Dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-143">Create a workflow process for the **Contact** table, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="0c3a1-144">Pracovní postupy můžete konfigurovat buď jako workflowy v reálném čase nebo na pozadí v závislosti na vašich požadavcích.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="0c3a1-145">Chcete-li nakonfigurovat workflow jako workflow na pozadí, vyberte možnost **Převést na workflow na pozadí**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="0c3a1-146">Aktivujte pracovní postupy, které jste vytvořili pro tabulky **Kontakt** a **Dodavatel**, abyste mohli začít používat tabulku **Kontakt** k ukládání informací pro dodavatele typu **Osoba**.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** table to store information for vendors of the **Person** type.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]