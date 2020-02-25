---
title: Odebrání instance
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c5f875ad9361c31af4fbe863488b881cdd97a6e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008307"
---
# <a name="remove-an-instance"></a><span data-ttu-id="58178-102">Odebrání instance</span><span class="sxs-lookup"><span data-stu-id="58178-102">Remove an instance</span></span>

<span data-ttu-id="58178-103">Tento článek vás provede procesem odebrání zkušební jednotky nebo výrobního prostředí pro aplikaci Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="58178-103">This article walks you through the process of removing a test drive or production environment for Microsoft Dynamics 365 Human Resources.</span></span>

## <a name="remove-a-test-drive-environment"></a><span data-ttu-id="58178-104">Odebrání testovacího prostředí</span><span class="sxs-lookup"><span data-stu-id="58178-104">Remove a test drive environment</span></span>

<span data-ttu-id="58178-105">Testovací jednotky aplikace Human Resources jsou zřizovány s 60denním vypršením platnosti.</span><span class="sxs-lookup"><span data-stu-id="58178-105">Human Resources test drives are provisioned with a 60-day expiration policy.</span></span> <span data-ttu-id="58178-106">Vlastníci prostředí testovací jednotky však mají možnost ukončit své zkušební verze dříve podle následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="58178-106">However, owners of test drive environments have the option to end their trial early by completing the following steps.</span></span> 

1. <span data-ttu-id="58178-107">Přejděte do [Centra pro správu Power Apps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="58178-107">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="58178-108">Vyberte **Prostředí**.</span><span class="sxs-lookup"><span data-stu-id="58178-108">Select **Environments**.</span></span>
3. <span data-ttu-id="58178-109">Vyberte testovací prostředí, které má podobný vzorec pojmenování jako tento: TestDrive - alias@domain</span><span class="sxs-lookup"><span data-stu-id="58178-109">Select the test drive environment, which has a naming pattern similar to this: TestDrive - alias@domain</span></span>
4. <span data-ttu-id="58178-110">Vyberte **Odstranit** a potvrďte rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="58178-110">Select **Delete** and confirm the decision.</span></span> 

<span data-ttu-id="58178-111">Existující testovací prostředí bude odstraněno.</span><span class="sxs-lookup"><span data-stu-id="58178-111">The existing test drive environment will be removed.</span></span> <span data-ttu-id="58178-112">Po odebrání se můžete přihlásit k novému testovacímu prostředí.</span><span class="sxs-lookup"><span data-stu-id="58178-112">When it is removed, you can sign up for a new test drive environment.</span></span> 

## <a name="remove-a-production-environment"></a><span data-ttu-id="58178-113">Odebrání produkčního prostředí</span><span class="sxs-lookup"><span data-stu-id="58178-113">Remove a production environment</span></span>

<span data-ttu-id="58178-114">Tento článek předpokládá, že jste si zakoupili aplikaci Human Resources prostřednictvím poskytovatele cloudového řešení (CSP) nebo smlouvy o podnikové architektuře (EA).</span><span class="sxs-lookup"><span data-stu-id="58178-114">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or an enterprise architecture (EA) agreement.</span></span> 

<span data-ttu-id="58178-115">Vzhledem k tomu, že jedno prostředí aplikace Human Resources je obsaženo v jednom prostředí Power Apps, existují dvě možnosti ke zvážení.</span><span class="sxs-lookup"><span data-stu-id="58178-115">Since a single Human Resources environment is contained within a single Power Apps environment, there are two options to consider.</span></span> <span data-ttu-id="58178-116">První možnost zahrnuje odebrání celého prostředí Power Apps; druhá možnost vyžaduje odebrání pouze aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="58178-116">The first option involves removing the entire Power Apps environment; the second option involves removing only Human Resources.</span></span> <span data-ttu-id="58178-117">První volba je upřednostňována při vytvoření prostředí Power Apps výslovně za účelem zřízení aplikace Human Resources a při začátku implementace, nebo když nemáte žádné ustavené integrace.</span><span class="sxs-lookup"><span data-stu-id="58178-117">The first option is preferred when you have created a Power Apps environment expressly for the purpose of provisioning Human Resources, and you've just begun implementation, or you don’t have any established integrations.</span></span> <span data-ttu-id="58178-118">Druhá možnost je vhodná, pokud máte zřízené prostředí Power Apps naplněné mnoha daty, která jsou využita v Power Apps a Power Automate.</span><span class="sxs-lookup"><span data-stu-id="58178-118">The second option is appropriate when you have an established Power Apps environment populated with rich data that's leveraged in Power Apps and Power Automate.</span></span>

> [!Important]
> <span data-ttu-id="58178-119">Před odstraněním prostředí Power Apps ověřte, že se již nepoužívá pro bohaté datové integrace mimo aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="58178-119">Before removing the Power Apps environment, ensure it is not being used for rich data integrations outside the scope of Human Resources.</span></span> <span data-ttu-id="58178-120">Povšimněte si též, že výchozí prostředí Power Apps nelze odstranit.</span><span class="sxs-lookup"><span data-stu-id="58178-120">Also note that the default Power Apps environments cannot be removed.</span></span> 

<span data-ttu-id="58178-121">Chcete-li odebrat celé prostředí Power Apps, včetně prostředí Human Resources a přidružených aplikací a toků:</span><span class="sxs-lookup"><span data-stu-id="58178-121">To remove the entire Power Apps environment, including Human Resources and the associated apps and flows:</span></span>

1. <span data-ttu-id="58178-122">Přejděte do [Centra pro správu Power Apps](https://admin.businessplatform.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="58178-122">Navigate to the [Power Apps Admin center](https://admin.businessplatform.microsoft.com/).</span></span>
2. <span data-ttu-id="58178-123">Vyberte **Prostředí**.</span><span class="sxs-lookup"><span data-stu-id="58178-123">Select **Environments**.</span></span>
3. <span data-ttu-id="58178-124">Vyberte prostředí, které má být odstraněno.</span><span class="sxs-lookup"><span data-stu-id="58178-124">Select the environment to be removed.</span></span>
4. <span data-ttu-id="58178-125">Vyberte **Odstranit** a potvrďte rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="58178-125">Select **Delete** and confirm the decision.</span></span> 
5. <span data-ttu-id="58178-126">Počkejte, dokud není dokončeno odstranění.</span><span class="sxs-lookup"><span data-stu-id="58178-126">Wait until the deletion is complete.</span></span>
6. <span data-ttu-id="58178-127">Přihlaste se do [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) pomocí účtu, který jste použili pro přihlášení se k odběru aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="58178-127">Sign in to [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) using the account that you used to subscribe to Human Resources.</span></span> 
7. <span data-ttu-id="58178-128">Vyberte projekt Human Resources obsahující prostředí.</span><span class="sxs-lookup"><span data-stu-id="58178-128">Select the Human Resources Project that contains the environment.</span></span> 
8. <span data-ttu-id="58178-129">Ve svém LCS projektu vyberte dlaždici **Správa aplikace Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="58178-129">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
9. <span data-ttu-id="58178-130">Vyberte instanci, kterou chcete odebrat.</span><span class="sxs-lookup"><span data-stu-id="58178-130">Select the instance to remove.</span></span> 
10. <span data-ttu-id="58178-131">Vyberte **Odebrat instanci** a potvrďte vaše rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="58178-131">Select **Remove instance** and confirm your decision.</span></span>  

<span data-ttu-id="58178-132">Chcete-li odebrat prostředí Human Resources z existujícího prostředí Power Apps, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="58178-132">To remove a Human Resources environment from an existing Power Apps environment, complete the following steps.</span></span> <span data-ttu-id="58178-133">Všimněte si, že nutnost zahrnout podporu a kontaktovat tým Human Resources DevOps je dočasná, dokud tato funkce nebude povolena přímo v LCS.</span><span class="sxs-lookup"><span data-stu-id="58178-133">Note that the need to involve support and contact the Human Resources DevOps team is temporary until this feature is enabled directly in LCS.</span></span>

1. <span data-ttu-id="58178-134">Požádejte podporu o zahájení požadavku na odebrání.</span><span class="sxs-lookup"><span data-stu-id="58178-134">Contact Support to initiate a removal request.</span></span>
2. <span data-ttu-id="58178-135">Tým podpory iniciuje požadavek na odebrání s týmem Human Resources DevOps.</span><span class="sxs-lookup"><span data-stu-id="58178-135">The Support team will initiate a removal request with the Human Resources DevOps team.</span></span> 
3. <span data-ttu-id="58178-136">Pokračujte po zobrazení informace, že bylo prostředí odebráno.</span><span class="sxs-lookup"><span data-stu-id="58178-136">Continue after you receive word that the environment has been removed.</span></span>
4.  <span data-ttu-id="58178-137">Přihlaste se do LCS pomocí účtu, který jste použili pro přihlášení k odběru aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="58178-137">Sign in to LCS using the account that you used to subscribe to Human Resources.</span></span> 
5. <span data-ttu-id="58178-138">Vyberte projekt Human Resources obsahující prostředí.</span><span class="sxs-lookup"><span data-stu-id="58178-138">Select the Human Resources project that contains the environment.</span></span> 
6. <span data-ttu-id="58178-139">Ve svém LCS projektu vyberte dlaždici **Správa aplikace Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="58178-139">In your LCS project, select the **Human Resources App Management** tile.</span></span> 
7. <span data-ttu-id="58178-140">Vyberte instanci, kterou chcete odebrat. Ta by měla být označena stavem nasazení **Neúspěšný**.</span><span class="sxs-lookup"><span data-stu-id="58178-140">Select the instance you would like to remove, which should be marked with a Deployment status of **Failed**.</span></span>
8. <span data-ttu-id="58178-141">Vyberte **Odebrat instanci** a potvrďte vaše rozhodnutí.</span><span class="sxs-lookup"><span data-stu-id="58178-141">Select **Remove instance** and confirm your decision.</span></span> 
