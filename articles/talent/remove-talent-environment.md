---
title: Odstranění prostředí Talent
description: Toto téma vás povede procesem odebrání zkušební jednotky nebo výrobního prostředí pro aplikaci Dynamics 365 for Talent.
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: e0422a5b7ac227ad03ccafb4e34e614dc770a363
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "303659"
---
# <a name="remove-talent-environments"></a><span data-ttu-id="8c012-103">Odstranění prostředí Talent</span><span class="sxs-lookup"><span data-stu-id="8c012-103">Remove Talent environments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8c012-104">Toto téma vás povede procesem odebrání zkušební jednotky nebo výrobního prostředí pro aplikaci Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="8c012-104">This topic walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 for Talent.</span></span>

## <a name="removing-a-test-drive-environment"></a><span data-ttu-id="8c012-105">Odstranění testovacího prostředí</span><span class="sxs-lookup"><span data-stu-id="8c012-105">Removing a test drive environment</span></span>

<span data-ttu-id="8c012-106">Testovací jednotky Talent jsou zřizovány s 60denním vypršením platnosti.</span><span class="sxs-lookup"><span data-stu-id="8c012-106">Talent test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="8c012-107">Vlastníci prostředí testovací jednotky však mají možnost ukončit své zkušební verze dříve podle následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="8c012-107">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="8c012-108">Přejděte na [Centrum správy PowerApps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="8c012-108">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="8c012-109">Vyberte **Prostředí**.</span><span class="sxs-lookup"><span data-stu-id="8c012-109">Select **Environments**.</span></span>
3. <span data-ttu-id="8c012-110">Vyberte testovací prostředí, které má podobný vzorec pojmenování jako tento: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="8c012-110">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="8c012-111">Vyberte **Odstranit** a potvrďte rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="8c012-111">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="8c012-112">Existující testovací prostředí bude odstraněno.</span><span class="sxs-lookup"><span data-stu-id="8c012-112">The existing test drive environment will be removed.</span></span> <span data-ttu-id="8c012-113">Po odebrání se můžete přihlásit k novému testovacímu prostředí.</span><span class="sxs-lookup"><span data-stu-id="8c012-113">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="removing-a-production-environment"></a><span data-ttu-id="8c012-114">Odstranění produkčního prostředí</span><span class="sxs-lookup"><span data-stu-id="8c012-114">Removing a production environment</span></span>

<span data-ttu-id="8c012-115">Toto téma předpokládá, že jste si zakoupili aplikaci Talent prostřednictvím poskytovatele cloudového řešení (CSP) nebo smlouvy o podnikové architektuře (EA).</span><span class="sxs-lookup"><span data-stu-id="8c012-115">This topic assumes that you've purchased Talent through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="8c012-116">Vzhledem k tomu, že jedno prostředí Talent je obsaženo v jednom prostředí PowerApps, existují dvě možnosti ke zvážení.</span><span class="sxs-lookup"><span data-stu-id="8c012-116">Since a single Talent environment is “contained” within a single PowerApps environment, there are two options to consider.</span></span> <span data-ttu-id="8c012-117">První možnost zahrnuje odebrání celého prostředí PowerApps; druhá možnost vyžaduje odebrání pouze aplikace Talent.</span><span class="sxs-lookup"><span data-stu-id="8c012-117">The first option involves removing the entire PowerApps environment; the second option involves removing only Talent.</span></span> <span data-ttu-id="8c012-118">První volba je upřednostňována při vytvoření prostředí PowerApps výslovně za účelem zřízení aplikace Talent a při začátku implementace, nebo když nemáte žádné ustavené integrace.</span><span class="sxs-lookup"><span data-stu-id="8c012-118">The first option is preferred when you have created a PowerApps environment expressly for the purpose of provisioning Talent, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="8c012-119">Druhá možnost je vhodná, pokud máte zřízené prostředí PowerApps naplněné mnoha daty, která jsou využita v PowerApps a tocích.</span><span class="sxs-lookup"><span data-stu-id="8c012-119">The second option is appropriate when you have an established PowerApps environment populated with rich data that's leveraged in PowerApps and Flows.</span></span>

> [!Important]
> <span data-ttu-id="8c012-120">Před odstraněním prostředí PowerApps ověřte, že se již nepoužívá pro bohaté datové integrace mimo aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="8c012-120">Before removing the PowerApps environment, ensure it is not being used for rich data integrations outside the scope of Talent.</span></span> <span data-ttu-id="8c012-121">Povšimněte si též, že výchozí prostředí PowerApps nelze odstranit.</span><span class="sxs-lookup"><span data-stu-id="8c012-121">Also note that the default PowerApps environments cannot be removed.</span></span> 

<span data-ttu-id="8c012-122">Chcete-li odebrat celé prostředí PowerApps, včetně prostředí Talent a přidružených aplikací a toků:</span><span class="sxs-lookup"><span data-stu-id="8c012-122">To remove the entire PowerApps environment, including Talent and the associated Apps and Flows:</span></span>

1. <span data-ttu-id="8c012-123">Přejděte na [Centrum správy PowerApps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="8c012-123">Navigate to the [PowerApps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="8c012-124">Vyberte **Prostředí**.</span><span class="sxs-lookup"><span data-stu-id="8c012-124">Select **Environments**.</span></span>
3. <span data-ttu-id="8c012-125">Vyberte prostředí, které má být odstraněno.</span><span class="sxs-lookup"><span data-stu-id="8c012-125">Select the environment to be removed.</span></span>
4. <span data-ttu-id="8c012-126">Vyberte **Odstranit** a potvrďte rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="8c012-126">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="8c012-127">Počkejte, dokud není dokončeno odstranění.</span><span class="sxs-lookup"><span data-stu-id="8c012-127">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="8c012-128">Přihlaste se do [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) pomocí účtu, který jste použili pro přihlášení se k odběru aplikace Talent.</span><span class="sxs-lookup"><span data-stu-id="8c012-128">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Talent.</span></span> 
7. <span data-ttu-id="8c012-129">Vyberte projekt Talent obsahující prostředí.</span><span class="sxs-lookup"><span data-stu-id="8c012-129">Select the Talent Project that contains the environment.</span></span> 
8. <span data-ttu-id="8c012-130">Ve svém LCS projektu vyberte dlaždici **Správa aplikace Talent**.</span><span class="sxs-lookup"><span data-stu-id="8c012-130">In your LCS project, select the **Talent App Management** tile.</span></span> 
9. <span data-ttu-id="8c012-131">Vyberte instanci, kterou chcete odebrat.</span><span class="sxs-lookup"><span data-stu-id="8c012-131">Select the instance to remove.</span></span> 
10. <span data-ttu-id="8c012-132">Vyberte **Odebrat instanci** a potvrďte vaše rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="8c012-132">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="8c012-133">Chcete-li odebrat prostředí Talent z existujícího prostředí PowerApps, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="8c012-133">To remove a Talent environment from an existing PowerApps environment, complete the following steps.</span></span> <span data-ttu-id="8c012-134">Všimněte si, že nutnost zahrnout podporu a kontaktovat tým Talent DevOps je dočasná, dokud tato funkce nebude povolena přímo v LCS.</span><span class="sxs-lookup"><span data-stu-id="8c012-134">Note that the need to involve support and contact the Talent DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="8c012-135">Požádejte podporu o zahájení požadavku na odebrání.</span><span class="sxs-lookup"><span data-stu-id="8c012-135">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="8c012-136">Tým podpory iniciuje požadavek na odebrání s týmem Talent DevOps.</span><span class="sxs-lookup"><span data-stu-id="8c012-136">The Support team will initiate a removal request with the Talent DevOps team.</span></span> 
3. <span data-ttu-id="8c012-137">Pokračujte po zobrazení informace, že bylo prostředí odebráno.</span><span class="sxs-lookup"><span data-stu-id="8c012-137">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="8c012-138">Přihlaste se do LCS pomocí účtu, který jste použili pro přihlášení se k odběru aplikace Talent.</span><span class="sxs-lookup"><span data-stu-id="8c012-138">Sign in to LCS using the account that you used to subscribe to Talent.</span></span> 
5. <span data-ttu-id="8c012-139">Vyberte projekt Talent obsahující prostředí.</span><span class="sxs-lookup"><span data-stu-id="8c012-139">Select the Talent project that contains the environment.</span></span> 
6. <span data-ttu-id="8c012-140">Ve svém LCS projektu vyberte dlaždici **Správa aplikace Talent**.</span><span class="sxs-lookup"><span data-stu-id="8c012-140">In your LCS project, select the **Talent App Management** tile.</span></span> 
7. <span data-ttu-id="8c012-141">Vyberte instanci, kterou chcete odebrat. Ta by měla být označena stavem nasazení **Neúspěšný**.</span><span class="sxs-lookup"><span data-stu-id="8c012-141">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="8c012-142">Vyberte **Odebrat instanci** a potvrďte vaše rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="8c012-142">Select **Remove instance** and confirm your decision.</span></span> 

