---
title: "Odebrat prostředí Talent"
description: "Toto téma vás provede procesem odstranění testovacího produkčního prostředí pro aplikaci Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d1870c84d4d5e7402bae44d192ce7587c2f67fe7
ms.openlocfilehash: 0e7748b079b1cd5c069917d46e05cd281ea6aa01
ms.contentlocale: cs-cz
ms.lasthandoff: 04/05/2018

---
# <a name="remove-a-talent-environment"></a><span data-ttu-id="5fdf6-103">Odebrat prostředí Talent</span><span class="sxs-lookup"><span data-stu-id="5fdf6-103">Remove a Talent environment</span></span>

<span data-ttu-id="5fdf6-104">Toto téma vás provede procesem odstranění testovacího produkčního prostředí pro aplikaci Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 for Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="5fdf6-105">Odstranění testovacího prostředí</span><span class="sxs-lookup"><span data-stu-id="5fdf6-105">Removing a test drive environment</span></span>

<span data-ttu-id="5fdf6-106">Testovací jednotky Talent jsou zřizovány s 60denním vypršením platnosti.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="5fdf6-107">Vlastníci prostředí testovací jednotky však mají možnost ukončit své zkušební verze dříve podle následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="5fdf6-108">Přejděte na [Centrum správy PowerApps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="5fdf6-108">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="5fdf6-109">Vyberte **Prostředí**.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-109">Select **Environments**.</span></span>
3. <span data-ttu-id="5fdf6-110">Vyberte testovací prostředí, které má podobný vzorec pojmenování jako tento: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="5fdf6-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="5fdf6-111">Vyberte **Odstranit** a potvrďte rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="5fdf6-112">Existující testovací prostředí bude odstraněno.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="5fdf6-113">Po odebrání se můžete přihlásit k novému testovacímu prostředí.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="5fdf6-114">Odstranění produkčního prostředí</span><span class="sxs-lookup"><span data-stu-id="5fdf6-114">Removing a production environment</span></span>

<span data-ttu-id="5fdf6-115">Toto téma předpokládá, že jste si zakoupili aplikaci Talent prostřednictvím poskytovatele cloudového řešení (CSP) nebo smlouvy o podnikové architektuře (EA).</span><span class="sxs-lookup"><span data-stu-id="5fdf6-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="5fdf6-116">Vzhledem k tomu, že jedno prostředí Talent je obsaženo v jednom prostředí PowerApps, existují dvě možnosti ke zvážení.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-116">Since a single Talent environment is “contained” within a single PowerApps environment, there are two options to consider.</span></span> <span data-ttu-id="5fdf6-117">První možnost zahrnuje odebrání celého prostředí PowerApps; druhá možnost vyžaduje odebrání pouze aplikace Talent.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-117">The first option involves removing the entire PowerApps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="5fdf6-118">První volba je upřednostňována při vytvoření prostředí PowerApps výslovně za účelem zřízení aplikace Talent a při začátku implementace, nebo když nemáte žádné ustavené integrace.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-118">The first option is preferred when you have created a PowerApps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="5fdf6-119">Druhá možnost je vhodná, pokud máte zřízené prostředí PowerApps naplněné mnoha daty, která jsou využita v PowerApps a tocích.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-119">The second option is appropriate when you have an established PowerApps environment populated with rich data that's leveraged in PowerApps and Flows.</span></span>

> [!Important]
> <span data-ttu-id="5fdf6-120">Před odstraněním prostředí PowerApps ověřte, že se již nepoužívá pro bohaté datové integrace mimo aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-120">Before removing the PowerApps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="5fdf6-121">Povšimněte si též, že výchozí prostředí PowerApps nelze odstranit.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-121">Also note that the default PowerApps environments cannot be removed.</span></span> 

<span data-ttu-id="5fdf6-122">Chcete-li odebrat celé prostředí PowerApps, včetně prostředí Talent a přidružených aplikací a toků:</span><span class="sxs-lookup"><span data-stu-id="5fdf6-122">To remove the entire PowerApps environment, including Talent and the associated Apps and Flows:</span></span>

1. <span data-ttu-id="5fdf6-123">Přejděte na [Centrum správy PowerApps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="5fdf6-123">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="5fdf6-124">Vyberte **Prostředí**.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-124">Select **Environments**.</span></span>
3. <span data-ttu-id="5fdf6-125">Vyberte prostředí, které má být odstraněno.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="5fdf6-126">Vyberte **Odstranit** a potvrďte rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="5fdf6-127">Počkejte, dokud není dokončeno odstranění.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="5fdf6-128">Přihlaste se do [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) pomocí účtu, který jste použili pro přihlášení se k odběru aplikace Talent.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="5fdf6-129">Vyberte projekt Talent obsahující prostředí.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="5fdf6-130">Ve svém LCS projektu vyberte dlaždici **Správa aplikace Talent**.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="5fdf6-131">Vyberte instanci, kterou chcete odebrat.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="5fdf6-132">Vyberte **Odebrat instanci** a potvrďte vaše rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="5fdf6-133">Chcete-li odebrat prostředí Talent z existujícího prostředí PowerApps, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-133">To remove a Talent environment from an existing PowerApps environment, complete the following steps.</span></span> <span data-ttu-id="5fdf6-134">Všimněte si, že nutnost zahrnout podporu a kontaktovat tým Talent DevOps je dočasná, dokud tato funkce nebude povolena přímo v LCS.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="5fdf6-135">Požádejte podporu o zahájení požadavku na odebrání.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="5fdf6-136">Tým podpory iniciuje požadavek na odebrání s týmem Talent DevOps.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="5fdf6-137">Pokračujte po zobrazení informace, že bylo prostředí odebráno.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="5fdf6-138">Přihlaste se do LCS pomocí účtu, který jste použili pro přihlášení se k odběru aplikace Talent.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="5fdf6-139">Vyberte projekt Talent obsahující prostředí.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="5fdf6-140">Ve svém LCS projektu vyberte dlaždici **Správa aplikace Talent**.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="5fdf6-141">Vyberte instanci, kterou chcete odebrat. Ta by měla být označena stavem nasazení **Neúspěšný**.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="5fdf6-142">Vyberte **Odebrat instanci** a potvrďte vaše rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="5fdf6-142">Select **Remove instance** and confirm your decision.</span></span> 


