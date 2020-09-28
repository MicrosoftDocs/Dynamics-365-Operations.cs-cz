---
title: Import konfigurace ze služby Lifecycle Services
description: Tohle téma popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může importovat novou verzi konfigurace elektronického výkaznictví ze služby Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59dbbf820f7a3de1e5fb31f781943320b8b1a60a
ms.sourcegitcommit: 9857d5cbdc0ab2fc9db049ac5ad118fc2b29bedc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/14/2020
ms.locfileid: "3810636"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="cd279-103">Import konfigurace ze služby Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="cd279-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cd279-104">Tohle téma popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může importovat novou verzi [konfigurace elektronického výkaznictví](../general-electronic-reporting.md#Configuration) z [knihovny majetku na úrovni projektu](../../lifecycle-services/asset-library.md) ve službě Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="cd279-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="cd279-105">V tomto příkladu zvolíte požadovanou verzi konfigurace elektronického výkaznictví a importujete ji pro vzorovou společnost s názvem Litware, Inc. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace elektronického výkaznictví se sdílí mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="cd279-105">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="cd279-106">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu [Odeslání konfigurace elektronického výkaznictví do služby Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="cd279-106">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="cd279-107">Je rovněž vyžadován přístup k LCS.</span><span class="sxs-lookup"><span data-stu-id="cd279-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="cd279-108">Přihlaste se k aplikaci použitím některé z následující role:</span><span class="sxs-lookup"><span data-stu-id="cd279-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="cd279-109">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="cd279-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="cd279-110">Správce systému</span><span class="sxs-lookup"><span data-stu-id="cd279-110">System administrator</span></span>

2. <span data-ttu-id="cd279-111">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="cd279-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="cd279-112">Vyberte **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="cd279-112">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="cd279-113">Ujistěte se, že aktuální uživatel Dynamics 365 Finance je členem projektu LCS, který obsahuje knihovnu majetku, ke které chce uživatel [přístup](../../lifecycle-services/asset-library.md#asset-library-support) kvůli importu konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="cd279-113">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="cd279-114">K projektu LCS nemůžete přistupovat z úložiště elektronického výkaznictví, které představuje jinou doménu, než je doména použitá v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="cd279-114">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="cd279-115">Pokud to zkusíte, zobrazí se prázdný seznam projektů LCS a nebudete moci importovat konfigurace elektronického výkaznictví z knihovny majetku na úrovni projektu v LCS.</span><span class="sxs-lookup"><span data-stu-id="cd279-115">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="cd279-116">Chcete-li získat přístup ke knihovnám majektu na úrovni projektu z úložiště elektronického výkaznictví, které slouží k importu konfigurací elektronického výkaznictví, přihlaste se do aplikace Finance pomocí přihlašovacích údajů uživatele, který patří ke klientovi (doméně), pro který byla zřízena aktuální instance Finance.</span><span class="sxs-lookup"><span data-stu-id="cd279-116">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="cd279-117">Odstranění sdílené verze konfigurace modelu dat</span><span class="sxs-lookup"><span data-stu-id="cd279-117">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="cd279-118">Na stránce **Konfigurace** ve stromové struktuře konfigurací vyberte položku **Vzorová konfigurace modelu**.</span><span class="sxs-lookup"><span data-stu-id="cd279-118">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="cd279-119">Vytvořili jste první verzi vzorové konfigurace modelu dat a publikovali ji v LCS po provedení kroků v části [Odeslání konfigurace do služby Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="cd279-119">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="cd279-120">V tomto postupu tuto verzi konfigurace elektronického výkaznictví odstraníte.</span><span class="sxs-lookup"><span data-stu-id="cd279-120">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="cd279-121">Danou verzi poté importujete z LCS dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="cd279-121">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="cd279-122">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="cd279-122">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="cd279-123">Pro tento příklad vyberte verzi této konfigurace ve stavu **Sdíleno**.</span><span class="sxs-lookup"><span data-stu-id="cd279-123">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="cd279-124">Tento stav označuje, že byla konfigurace publikována do LCS.</span><span class="sxs-lookup"><span data-stu-id="cd279-124">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="cd279-125">Vyberte **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="cd279-125">Select **Change status**.</span></span>
4. <span data-ttu-id="cd279-126">Vyberte **Ukončit**.</span><span class="sxs-lookup"><span data-stu-id="cd279-126">Select **Discontinue**.</span></span>

    <span data-ttu-id="cd279-127">Změnou stavu vybrané verze ze **Sdíleno** na **Ukončeno** umožníte její odstranění.</span><span class="sxs-lookup"><span data-stu-id="cd279-127">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="cd279-128">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd279-128">Select **OK**.</span></span>
6. <span data-ttu-id="cd279-129">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="cd279-129">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="cd279-130">Pro tento příklad vyberte verzi této konfigurace ve stavu **Ukončeno**.</span><span class="sxs-lookup"><span data-stu-id="cd279-130">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="cd279-131">Zvolte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="cd279-131">Select **Delete**.</span></span>
8. <span data-ttu-id="cd279-132">Vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="cd279-132">Select **Yes**.</span></span>

    <span data-ttu-id="cd279-133">Všimněte si, že pouze 2. verze návrhu vybrané konfigurace modelu dat je k nyní dispozici.</span><span class="sxs-lookup"><span data-stu-id="cd279-133">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="cd279-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cd279-134">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="cd279-135">Import sdílené verze konfigurace modelu dat z LCS</span><span class="sxs-lookup"><span data-stu-id="cd279-135">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="cd279-136">Přejděte do části **Správa organizace \> Pracovní prostory \> Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="cd279-136">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="cd279-137">V části **Zprostředkovatelé konfigurace** vyberte dlaždici **Litware Inc.**</span><span class="sxs-lookup"><span data-stu-id="cd279-137">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="cd279-138">Na dlaždici **Litware, Inc.** vyberte **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="cd279-138">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="cd279-139">Nyní můžete otevřít seznam úložišť pro poskytovatele konfigurace Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="cd279-139">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="cd279-140">Zvolte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="cd279-140">Select **Open**.</span></span>

    <span data-ttu-id="cd279-141">V tomto příkladu vyberte úložiště **LCS** a otevřete jej.</span><span class="sxs-lookup"><span data-stu-id="cd279-141">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="cd279-142">Musíš mít [přístup](#accessconditions) k projektu LCS a knihovně majetku, ke které má přístup vybrané úložiště elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="cd279-142">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="cd279-143">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="cd279-143">In the list, mark the selected row.</span></span>

    <span data-ttu-id="cd279-144">V tomto případě vyberte první verzi **vzorové konfigurace modelu** v seznamu verzí.</span><span class="sxs-lookup"><span data-stu-id="cd279-144">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="cd279-145">Vyberte **Import**.</span><span class="sxs-lookup"><span data-stu-id="cd279-145">Select **Import**.</span></span>
7. <span data-ttu-id="cd279-146">Volbou **Ano** potvrďte import vybrané verze z LCS.</span><span class="sxs-lookup"><span data-stu-id="cd279-146">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="cd279-147">Informační zpráva potvrzuje, že vybraná verze byla úspěšně importována.</span><span class="sxs-lookup"><span data-stu-id="cd279-147">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="cd279-148">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cd279-148">Close the page.</span></span>
9. <span data-ttu-id="cd279-149">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cd279-149">Close the page.</span></span>
10. <span data-ttu-id="cd279-150">Vyberte **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="cd279-150">Select **Configurations**.</span></span>
11. <span data-ttu-id="cd279-151">Ve stromovém zobrazení vyberte možnost **Vzorová konfigurace modelu**.</span><span class="sxs-lookup"><span data-stu-id="cd279-151">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="cd279-152">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="cd279-152">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="cd279-153">Pro tento příklad vyberte verzi této konfigurace ve stavu **Sdíleno**.</span><span class="sxs-lookup"><span data-stu-id="cd279-153">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="cd279-154">Všimněte si, že nyní je k dispozici také sdílená 1. verze vybrané konfigurace datového modelu.</span><span class="sxs-lookup"><span data-stu-id="cd279-154">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>
