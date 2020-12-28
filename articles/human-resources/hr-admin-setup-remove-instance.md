---
title: Odebrání instance
description: Tento článek vás provede procesem odebrání zkušební jednotky nebo výrobního prostředí pro aplikaci Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0a8eac74f0d840251ab56445dd5af4d19d3c0490
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417667"
---
# <a name="remove-an-instance"></a><span data-ttu-id="030d5-103">Odebrání instance</span><span class="sxs-lookup"><span data-stu-id="030d5-103">Remove an instance</span></span>

<span data-ttu-id="030d5-104">Tento článek vás provede procesem odebrání zkušební jednotky nebo výrobního prostředí pro aplikaci Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="030d5-104">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="030d5-105">Odebrání testovacího prostředí</span><span class="sxs-lookup"><span data-stu-id="030d5-105">Remove a test drive environment</span></span>

<span data-ttu-id="030d5-106">Testovací jednotky aplikace Human Resources jsou zřizovány s 60denním vypršením platnosti.</span><span class="sxs-lookup"><span data-stu-id="030d5-106">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="030d5-107">Vlastníci prostředí testovací jednotky však mají možnost ukončit své zkušební verze dříve podle následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="030d5-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="030d5-108">Přejděte do [Centra pro správu Power Apps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="030d5-108">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="030d5-109">Vyberte **Prostředí**.</span><span class="sxs-lookup"><span data-stu-id="030d5-109">Select **Environments**.</span></span>
3. <span data-ttu-id="030d5-110">Vyberte testovací prostředí, které má podobný vzorec pojmenování jako tento: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="030d5-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="030d5-111">Vyberte **Odstranit** a potvrďte rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="030d5-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="030d5-112">Existující testovací prostředí bude odstraněno.</span><span class="sxs-lookup"><span data-stu-id="030d5-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="030d5-113">Po odebrání se můžete přihlásit k novému testovacímu prostředí.</span><span class="sxs-lookup"><span data-stu-id="030d5-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="030d5-114">Odebrání produkčního prostředí</span><span class="sxs-lookup"><span data-stu-id="030d5-114">Remove a production environment</span></span>

<span data-ttu-id="030d5-115">Tento článek předpokládá, že jste si zakoupili aplikaci Human Resources prostřednictvím poskytovatele cloudového řešení (CSP) nebo smlouvy o podnikové architektuře (EA).</span><span class="sxs-lookup"><span data-stu-id="030d5-115">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="030d5-116">Vzhledem k tomu, že jedno prostředí aplikace Human Resources je obsaženo v jednom prostředí Power Apps, existují dvě možnosti ke zvážení.</span><span class="sxs-lookup"><span data-stu-id="030d5-116">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="030d5-117">První možnost zahrnuje odebrání celého prostředí Power Apps; druhá možnost vyžaduje odebrání pouze aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="030d5-117">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="030d5-118">První volba je upřednostňována při vytvoření prostředí Power Apps výslovně za účelem zřízení aplikace Human Resources a při začátku implementace, nebo když nemáte žádné ustavené integrace.</span><span class="sxs-lookup"><span data-stu-id="030d5-118">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="030d5-119">Druhá možnost je vhodná, pokud máte zřízené prostředí Power Apps naplněné mnoha daty, která jsou využita v Power Apps a Power Automate.</span><span class="sxs-lookup"><span data-stu-id="030d5-119">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="030d5-120">Před odstraněním prostředí Power Apps ověřte, že se již nepoužívá pro bohaté datové integrace mimo aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="030d5-120">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="030d5-121">Povšimněte si též, že výchozí prostředí Power Apps nelze odstranit.</span><span class="sxs-lookup"><span data-stu-id="030d5-121">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="030d5-122">Chcete-li odebrat celé prostředí Power Apps, včetně prostředí Human Resources a přidružených aplikací a toků:</span><span class="sxs-lookup"><span data-stu-id="030d5-122">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="030d5-123">Přejděte do [Centra pro správu Power Apps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="030d5-123">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="030d5-124">Vyberte **Prostředí**.</span><span class="sxs-lookup"><span data-stu-id="030d5-124">Select **Environments**.</span></span>
3. <span data-ttu-id="030d5-125">Vyberte prostředí, které má být odstraněno.</span><span class="sxs-lookup"><span data-stu-id="030d5-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="030d5-126">Vyberte **Odstranit** a potvrďte rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="030d5-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="030d5-127">Počkejte, dokud není dokončeno odstranění.</span><span class="sxs-lookup"><span data-stu-id="030d5-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="030d5-128">Přihlaste se do [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) pomocí účtu, který jste použili pro přihlášení se k odběru aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="030d5-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="030d5-129">Vyberte projekt Human Resources obsahující prostředí.</span><span class="sxs-lookup"><span data-stu-id="030d5-129">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="030d5-130">Ve svém LCS projektu vyberte dlaždici **Správa aplikace Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="030d5-130">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="030d5-131">Vyberte instanci, kterou chcete odebrat.</span><span class="sxs-lookup"><span data-stu-id="030d5-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="030d5-132">Vyberte **Odebrat instanci** a potvrďte vaše rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="030d5-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="030d5-133">Chcete-li odebrat prostředí Human Resources z existujícího prostředí Power Apps, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="030d5-133">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="030d5-134">Všimněte si, že nutnost zahrnout podporu a kontaktovat tým Human Resources DevOps je dočasná, dokud tato funkce nebude povolena přímo v LCS.</span><span class="sxs-lookup"><span data-stu-id="030d5-134">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="030d5-135">Požádejte podporu o zahájení požadavku na odebrání.</span><span class="sxs-lookup"><span data-stu-id="030d5-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="030d5-136">Tým podpory iniciuje požadavek na odebrání s týmem Human Resources DevOps.</span><span class="sxs-lookup"><span data-stu-id="030d5-136">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="030d5-137">Pokračujte po zobrazení informace, že bylo prostředí odebráno.</span><span class="sxs-lookup"><span data-stu-id="030d5-137">Continue after you receive word that the environment has been removed.</span></span>
4. <span data-ttu-id="030d5-138">Přihlaste se do LCS pomocí účtu, který jste použili pro přihlášení k odběru aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="030d5-138">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="030d5-139">Vyberte projekt Human Resources obsahující prostředí.</span><span class="sxs-lookup"><span data-stu-id="030d5-139">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="030d5-140">Ve svém LCS projektu vyberte dlaždici **Správa aplikace Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="030d5-140">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="030d5-141">Vyberte instanci, kterou chcete odebrat. Ta by měla být označena stavem nasazení **Odstraněný**.</span><span class="sxs-lookup"><span data-stu-id="030d5-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Deleted**.</span></span>
8. <span data-ttu-id="030d5-142">Vyberte **Odebrat instanci** a potvrďte vaše rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="030d5-142">Select **Remove instance** and confirm your decision.</span></span> 

## <a name="recover-a-soft-deleted-environment"></a><span data-ttu-id="030d5-143">Obnovte prostředí s logickým odstraněním</span><span class="sxs-lookup"><span data-stu-id="030d5-143">Recover a soft-deleted environment</span></span>

<span data-ttu-id="030d5-144">Pokud odstraníte prostředí Power Apps, ke kterému je vaše prostředí Human Resources připojeno, bude stav prostředí Human Resources ve službě Lifecycle Services **Logicky odstraněno**.</span><span class="sxs-lookup"><span data-stu-id="030d5-144">If you delete the Power Apps environment that your Human Resources environment is connected to, the status of the Human Resources environment in Lifecycle Services will be **Soft deleted**.</span></span> <span data-ttu-id="030d5-145">V tomto případě se uživatelé nemohou připojit k Human Resources.</span><span class="sxs-lookup"><span data-stu-id="030d5-145">In this case, users can't connect to Human Resources.</span></span>

<span data-ttu-id="030d5-146">Postup obnovení prostředí:</span><span class="sxs-lookup"><span data-stu-id="030d5-146">To restore the environment:</span></span>

1. <span data-ttu-id="030d5-147">Postupujte podle pokynů v [Obnovení prostředí Power Apps](/power-platform/admin/recover-environment.md).</span><span class="sxs-lookup"><span data-stu-id="030d5-147">Follow the instructions in [Recover the Power Apps environment](/power-platform/admin/recover-environment.md).</span></span>

2. <span data-ttu-id="030d5-148">Chcete-li obnovit prostředí Human Resources, kontaktujte podporu.</span><span class="sxs-lookup"><span data-stu-id="030d5-148">Contact Support to restore the Human Resources environment.</span></span> <span data-ttu-id="030d5-149">Pro další informace si přečtěte [Získání podpory](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="030d5-149">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

> [!Warning]
> <span data-ttu-id="030d5-150">Prostředí Power Apps jsou uložena pouze po dobu sedmi dnů po odstranění.</span><span class="sxs-lookup"><span data-stu-id="030d5-150">Power Apps environments are only saved for seven days after deletion.</span></span> <span data-ttu-id="030d5-151">Prostředí musíte obnovit do sedmi dnů.</span><span class="sxs-lookup"><span data-stu-id="030d5-151">You must recover the environment within the seven day period.</span></span>
