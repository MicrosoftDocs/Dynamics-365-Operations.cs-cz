---
title: Odeslání konfigurace do služby Lifecycle Services
description: Toto téma popisuje, jak vytvořit novou konfiguraci elektronického výkaznictví (ER) a nahrát ji do Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41a8fcf2592bde4901aba703e0cd124b1155dac6
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270552"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="291a3-103">Odeslání konfigurace do služby Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="291a3-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="291a3-104">Tohle téma popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou [konfiguraci elektronického výkaznictví](../general-electronic-reporting.md#Configuration) a odeslat ji do [knihovny majetku na úrovni projektu](../../lifecycle-services/asset-library.md) ve službě Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="291a3-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="291a3-105">Používání služby LCS jako úložiště pro konfigurace elektronického výkaznictví (ER) je označeno jako [zastaralé](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="291a3-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="291a3-106">Další informace viz [Regulatory Configuration Service (RCS) – ukončení podpory úložiště Lifecycle Services (LCS)](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="291a3-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="291a3-107">V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost s názvem Litware, Inc a odešlete ji do služby LCS. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace elektronického výkaznictví se sdílí mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="291a3-107">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="291a3-108">K provedení těchto kroků musíte v RCS nejprve dokončit jednotlivé kroky v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="291a3-108">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="291a3-109">Je rovněž vyžadován přístup k LCS.</span><span class="sxs-lookup"><span data-stu-id="291a3-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="291a3-110">Přihlaste se k aplikaci použitím některé z následující role:</span><span class="sxs-lookup"><span data-stu-id="291a3-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="291a3-111">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="291a3-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="291a3-112">Správce systému</span><span class="sxs-lookup"><span data-stu-id="291a3-112">System administrator</span></span>

2. <span data-ttu-id="291a3-113">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="291a3-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="291a3-114">Vyberte **Litware, Inc.** a označte ji jako **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="291a3-114">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="291a3-115">Vyberte **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="291a3-115">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="291a3-116">Ujistěte se, že aktuální uživatel Dynamics 365 Finance je členem projektu LCS, který obsahuje [knihovnu majetku](../../lifecycle-services/asset-library.md#asset-library-support), která slouží k importu konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="291a3-116">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="291a3-117">K projektu LCS nemůžete přistupovat z úložiště elektronického výkaznictví, které představuje jinou doménu, než je doména použitá v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="291a3-117">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="291a3-118">Pokud to zkusíte, zobrazí se prázdný seznam projektů LCS a nebudete moci importovat konfigurace elektronického výkaznictví z knihovny majetku na úrovni projektu v LCS.</span><span class="sxs-lookup"><span data-stu-id="291a3-118">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="291a3-119">Chcete-li získat přístup ke knihovnám majektu na úrovni projektu z úložiště elektronického výkaznictví, které slouží k importu konfigurací elektronického výkaznictví, přihlaste se do aplikace Finance pomocí přihlašovacích údajů uživatele, který patří ke klientovi (doméně), pro který byla zřízena aktuální instance Finance.</span><span class="sxs-lookup"><span data-stu-id="291a3-119">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="291a3-120">Vytvoření nové konfigurace datového modelu</span><span class="sxs-lookup"><span data-stu-id="291a3-120">Create a new data model configuration</span></span>

1. <span data-ttu-id="291a3-121">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="291a3-121">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="291a3-122">Na stránce **Konfigurace** výběrem možnosti **Vytvořit konfiguraci** otevřete rozevírací dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="291a3-122">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="291a3-123">V tomto příkladu vytvoříte konfiguraci, která obsahuje vzorový model dat pro elektronické doklady.</span><span class="sxs-lookup"><span data-stu-id="291a3-123">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="291a3-124">Tato konfigurace modelu dat bude odeslána do LCS později.</span><span class="sxs-lookup"><span data-stu-id="291a3-124">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="291a3-125">V poli **Název** zadejte **Vzorová konfigurace modelu**.</span><span class="sxs-lookup"><span data-stu-id="291a3-125">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="291a3-126">V poli **Popis** zadejte **Vzorová konfigurace modelu**.</span><span class="sxs-lookup"><span data-stu-id="291a3-126">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="291a3-127">Vyberte **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="291a3-127">Select **Create configuration**.</span></span>
6. <span data-ttu-id="291a3-128">Vyberte **Návrhář modelů**.</span><span class="sxs-lookup"><span data-stu-id="291a3-128">Select **Model designer**.</span></span>
7. <span data-ttu-id="291a3-129">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="291a3-129">Select **New**.</span></span>
8. <span data-ttu-id="291a3-130">Do pole **Název** zadejte **Vstupní bod**.</span><span class="sxs-lookup"><span data-stu-id="291a3-130">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="291a3-131">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="291a3-131">Select **Add**.</span></span>
10. <span data-ttu-id="291a3-132">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="291a3-132">Select **Save**.</span></span>
11. <span data-ttu-id="291a3-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="291a3-133">Close the page.</span></span>
12. <span data-ttu-id="291a3-134">Vyberte **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="291a3-134">Select **Change status**.</span></span>
13. <span data-ttu-id="291a3-135">Zvolte **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="291a3-135">Select **Complete**.</span></span>
14. <span data-ttu-id="291a3-136">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="291a3-136">Select **OK**.</span></span>
15. <span data-ttu-id="291a3-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="291a3-137">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="291a3-138">Registrace nového úložiště</span><span class="sxs-lookup"><span data-stu-id="291a3-138">Register a new repository</span></span>

1. <span data-ttu-id="291a3-139">Přejděte do části **Správa organizace \> Pracovní prostory \> Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="291a3-139">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="291a3-140">V části **Zprostředkovatelé konfigurace** vyberte dlaždici **Litware Inc.**</span><span class="sxs-lookup"><span data-stu-id="291a3-140">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="291a3-141">Na dlaždici **Litware, Inc.** vyberte **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="291a3-141">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="291a3-142">Nyní můžete otevřít seznam úložišť pro poskytovatele konfigurace Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="291a3-142">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="291a3-143">Výběrem možnosti **Přidat** otevřete rozevírací dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="291a3-143">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="291a3-144">Nyní můžete přidat nové úložiště.</span><span class="sxs-lookup"><span data-stu-id="291a3-144">You can now add a new repository.</span></span>

5. <span data-ttu-id="291a3-145">V poli **Typ úložiště konfigurace** vyberte **LCS**.</span><span class="sxs-lookup"><span data-stu-id="291a3-145">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="291a3-146">Zvolte **Vytvořit úložiště**.</span><span class="sxs-lookup"><span data-stu-id="291a3-146">Select **Create repository**.</span></span>
7. <span data-ttu-id="291a3-147">V poli **Projekt** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="291a3-147">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="291a3-148">V tomto příkladu vyberte požadovaný projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="291a3-148">For this example, select the desired LCS project.</span></span> <span data-ttu-id="291a3-149">Musíte mít [přístup](#accessconditions) k tomuto projektu.</span><span class="sxs-lookup"><span data-stu-id="291a3-149">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="291a3-150">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="291a3-150">Select **OK**.</span></span>

    <span data-ttu-id="291a3-151">Vytvořte nový záznam v úložišti.</span><span class="sxs-lookup"><span data-stu-id="291a3-151">Complete a new repository entry.</span></span>

9. <span data-ttu-id="291a3-152">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="291a3-152">In the list, mark the selected row.</span></span>

    <span data-ttu-id="291a3-153">V tomto příkladu vyberte záznam úložiště **LCS**.</span><span class="sxs-lookup"><span data-stu-id="291a3-153">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="291a3-154">Všimněte si, že registrované úložiště je označeno aktuálním poskytovatelem.</span><span class="sxs-lookup"><span data-stu-id="291a3-154">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="291a3-155">Jinými slovy, do tohoto úložiště lze umístit pouze konfigurace, které vlastní tento poskytovatel, a proto je možné je odeslat do vybraného projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="291a3-155">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="291a3-156">Zvolte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="291a3-156">Select **Open**.</span></span>

    <span data-ttu-id="291a3-157">Tím otevřete úložiště se seznamem konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="291a3-157">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="291a3-158">Pokud vybraný projekt zatím nebyl použit pro sdílení konfigurací elektronického výkaznictví, seznam bude prázdný.</span><span class="sxs-lookup"><span data-stu-id="291a3-158">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="291a3-159">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="291a3-159">Close the page.</span></span>
12. <span data-ttu-id="291a3-160">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="291a3-160">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="291a3-161">Odeslání konfigurace do LCS</span><span class="sxs-lookup"><span data-stu-id="291a3-161">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="291a3-162">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="291a3-162">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="291a3-163">Na stránce **Konfigurace** ve stromové struktuře konfigurací vyberte položku **Vzorová konfigurace modelu**.</span><span class="sxs-lookup"><span data-stu-id="291a3-163">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="291a3-164">Muíte vybrat vytvořenou konfiguraci, která již byla dokončena.</span><span class="sxs-lookup"><span data-stu-id="291a3-164">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="291a3-165">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="291a3-165">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="291a3-166">Pro tento příklad vyberte verzi vybrané konfigurace ve stavu **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="291a3-166">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="291a3-167">Vyberte **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="291a3-167">Select **Change status**.</span></span>
5. <span data-ttu-id="291a3-168">Vyberte **Sdílet**.</span><span class="sxs-lookup"><span data-stu-id="291a3-168">Select **Share**.</span></span>

    <span data-ttu-id="291a3-169">Stav konfigurace se změní z **Dokončeno** na **Sdíleno**, když je konfigurace publikována v LCS.</span><span class="sxs-lookup"><span data-stu-id="291a3-169">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="291a3-170">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="291a3-170">Select **OK**.</span></span>
7. <span data-ttu-id="291a3-171">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="291a3-171">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="291a3-172">Pro tento příklad vyberte verzi této konfigurace ve stavu **Sdíleno**.</span><span class="sxs-lookup"><span data-stu-id="291a3-172">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="291a3-173">Všimněte si, že stav vybrané verze se změnil z **Dokončeno** na **Sdíleno**.</span><span class="sxs-lookup"><span data-stu-id="291a3-173">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="291a3-174">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="291a3-174">Close the page.</span></span>
9. <span data-ttu-id="291a3-175">Vyberte **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="291a3-175">Select **Repositories**.</span></span>

    <span data-ttu-id="291a3-176">Nyní můžete otevřít seznam úložišť pro poskytovatele konfigurace Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="291a3-176">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="291a3-177">Zvolte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="291a3-177">Select **Open**.</span></span>

    <span data-ttu-id="291a3-178">V tomto příkladu vyberte úložiště **LCS** a otevřete jej.</span><span class="sxs-lookup"><span data-stu-id="291a3-178">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="291a3-179">Všimněte si, že vybraná konfigurace je zobrazena jako majetek vybraného projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="291a3-179">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="291a3-180">Otevřete LCS přechodem na <https://lcs.dynamics.com>.</span><span class="sxs-lookup"><span data-stu-id="291a3-180">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="291a3-181">Otevřete projekt, který byl dříve použit pro registraci úložiště.</span><span class="sxs-lookup"><span data-stu-id="291a3-181">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="291a3-182">Otevřete knihovnu majetku projektu.</span><span class="sxs-lookup"><span data-stu-id="291a3-182">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="291a3-183">Vyberte typ majetku **Konfigurace GER**.</span><span class="sxs-lookup"><span data-stu-id="291a3-183">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="291a3-184">V seznamu by měla být uvedena konfigurace elektronického výkaznictví, kterou jste nahráli.</span><span class="sxs-lookup"><span data-stu-id="291a3-184">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="291a3-185">Všimněte si, že odeslané konfigurace LCS je možné importovat do jiné instance, pokud poskytovatelé mají přístupová práva k tomuto projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="291a3-185">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
