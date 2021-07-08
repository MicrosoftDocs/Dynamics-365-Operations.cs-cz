---
title: Import konfigurace ze služby Lifecycle Services
description: Toto téma popisuje, jak importovat novou verzi konfigurace elektronického výkaznictví (ER) z Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b58ecb8a7d6f52631dbca7642a4acbcf6ff895a3
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270830"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="2ccd8-103">Import konfigurace ze služby Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="2ccd8-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ccd8-104">Tohle téma popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může importovat novou verzi [konfigurace elektronického výkaznictví](../general-electronic-reporting.md#Configuration) z [knihovny majetku na úrovni projektu](../../lifecycle-services/asset-library.md) ve službě Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="2ccd8-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2ccd8-105">Používání služby LCS jako úložiště pro konfigurace elektronického výkaznictví (ER) je označeno jako [zastaralé](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="2ccd8-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="2ccd8-106">Další informace viz [Regulatory Configuration Service (RCS) – ukončení podpory úložiště Lifecycle Services (LCS)](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="2ccd8-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="2ccd8-107">V tomto příkladu zvolíte požadovanou verzi konfigurace elektronického výkaznictví a importujete ji pro vzorovou společnost s názvem Litware, Inc. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace elektronického výkaznictví se sdílí mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-107">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="2ccd8-108">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu [Odeslání konfigurace elektronického výkaznictví do služby Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="2ccd8-108">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="2ccd8-109">Je rovněž vyžadován přístup k LCS.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="2ccd8-110">Přihlaste se k aplikaci použitím některé z následující role:</span><span class="sxs-lookup"><span data-stu-id="2ccd8-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="2ccd8-111">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="2ccd8-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="2ccd8-112">Správce systému</span><span class="sxs-lookup"><span data-stu-id="2ccd8-112">System administrator</span></span>

2. <span data-ttu-id="2ccd8-113">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="2ccd8-114">Vyberte **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-114">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="2ccd8-115">Ujistěte se, že aktuální uživatel Dynamics 365 Finance je členem projektu LCS, který obsahuje knihovnu majetku, ke které chce uživatel [přístup](../../lifecycle-services/asset-library.md#asset-library-support) kvůli importu konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-115">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="2ccd8-116">K projektu LCS nemůžete přistupovat z úložiště elektronického výkaznictví, které představuje jinou doménu, než je doména použitá v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-116">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="2ccd8-117">Pokud to zkusíte, zobrazí se prázdný seznam projektů LCS a nebudete moci importovat konfigurace elektronického výkaznictví z knihovny majetku na úrovni projektu v LCS.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-117">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="2ccd8-118">Chcete-li získat přístup ke knihovnám majektu na úrovni projektu z úložiště elektronického výkaznictví, které slouží k importu konfigurací elektronického výkaznictví, přihlaste se do aplikace Finance pomocí přihlašovacích údajů uživatele, který patří ke klientovi (doméně), pro který byla zřízena aktuální instance Finance.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-118">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="2ccd8-119">Odstranění sdílené verze konfigurace modelu dat</span><span class="sxs-lookup"><span data-stu-id="2ccd8-119">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="2ccd8-120">Na stránce **Konfigurace** ve stromové struktuře konfigurací vyberte položku **Vzorová konfigurace modelu**.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-120">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="2ccd8-121">Vytvořili jste první verzi vzorové konfigurace modelu dat a publikovali ji v LCS po provedení kroků v části [Odeslání konfigurace do služby Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="2ccd8-121">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="2ccd8-122">V tomto postupu tuto verzi konfigurace elektronického výkaznictví odstraníte.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-122">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="2ccd8-123">Danou verzi poté importujete z LCS dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-123">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="2ccd8-124">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-124">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="2ccd8-125">Pro tento příklad vyberte verzi této konfigurace ve stavu **Sdíleno**.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-125">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="2ccd8-126">Tento stav označuje, že byla konfigurace publikována do LCS.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-126">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="2ccd8-127">Vyberte **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-127">Select **Change status**.</span></span>
4. <span data-ttu-id="2ccd8-128">Vyberte **Ukončit**.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-128">Select **Discontinue**.</span></span>

    <span data-ttu-id="2ccd8-129">Změnou stavu vybrané verze ze **Sdíleno** na **Ukončeno** umožníte její odstranění.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-129">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="2ccd8-130">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-130">Select **OK**.</span></span>
6. <span data-ttu-id="2ccd8-131">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-131">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="2ccd8-132">Pro tento příklad vyberte verzi této konfigurace ve stavu **Ukončeno**.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-132">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="2ccd8-133">Zvolte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-133">Select **Delete**.</span></span>
8. <span data-ttu-id="2ccd8-134">Vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-134">Select **Yes**.</span></span>

    <span data-ttu-id="2ccd8-135">Všimněte si, že pouze 2. verze návrhu vybrané konfigurace modelu dat je k nyní dispozici.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-135">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="2ccd8-136">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-136">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="2ccd8-137">Import sdílené verze konfigurace modelu dat z LCS</span><span class="sxs-lookup"><span data-stu-id="2ccd8-137">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="2ccd8-138">Přejděte do části **Správa organizace \> Pracovní prostory \> Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-138">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="2ccd8-139">V části **Zprostředkovatelé konfigurace** vyberte dlaždici **Litware Inc.**</span><span class="sxs-lookup"><span data-stu-id="2ccd8-139">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="2ccd8-140">Na dlaždici **Litware, Inc.** vyberte **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-140">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="2ccd8-141">Nyní můžete otevřít seznam úložišť pro poskytovatele konfigurace Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-141">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="2ccd8-142">Zvolte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-142">Select **Open**.</span></span>

    <span data-ttu-id="2ccd8-143">V tomto příkladu vyberte úložiště **LCS** a otevřete jej.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-143">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="2ccd8-144">Musíš mít [přístup](#accessconditions) k projektu LCS a knihovně majetku, ke které má přístup vybrané úložiště elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-144">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="2ccd8-145">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-145">In the list, mark the selected row.</span></span>

    <span data-ttu-id="2ccd8-146">V tomto případě vyberte první verzi **vzorové konfigurace modelu** v seznamu verzí.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-146">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="2ccd8-147">Vyberte **Import**.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-147">Select **Import**.</span></span>
7. <span data-ttu-id="2ccd8-148">Volbou **Ano** potvrďte import vybrané verze z LCS.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-148">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="2ccd8-149">Informační zpráva potvrzuje, že vybraná verze byla úspěšně importována.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-149">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="2ccd8-150">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-150">Close the page.</span></span>
9. <span data-ttu-id="2ccd8-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-151">Close the page.</span></span>
10. <span data-ttu-id="2ccd8-152">Vyberte **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-152">Select **Configurations**.</span></span>
11. <span data-ttu-id="2ccd8-153">Ve stromovém zobrazení vyberte možnost **Vzorová konfigurace modelu**.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-153">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="2ccd8-154">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-154">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="2ccd8-155">Pro tento příklad vyberte verzi této konfigurace ve stavu **Sdíleno**.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-155">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="2ccd8-156">Všimněte si, že nyní je k dispozici také sdílená 1. verze vybrané konfigurace datového modelu.</span><span class="sxs-lookup"><span data-stu-id="2ccd8-156">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
