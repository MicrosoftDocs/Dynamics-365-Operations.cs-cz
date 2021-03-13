---
title: Odeslání konfigurace do služby Lifecycle Services
description: Toto téma popisuje, jak vytvořit novou konfiguraci elektronického výkaznictví (ER) a nahrát ji do Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92fc6d7a8b2508c9a1f7b56ca8115adbd6ae00ea
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092534"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="acdfc-103">Odeslání konfigurace do služby Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="acdfc-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="acdfc-104">Tohle téma popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou [konfiguraci elektronického výkaznictví](../general-electronic-reporting.md#Configuration) a odeslat ji do [knihovny majetku na úrovni projektu](../../lifecycle-services/asset-library.md) ve službě Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="acdfc-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="acdfc-105">V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost s názvem Litware, Inc a odešlete ji do služby LCS. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace elektronického výkaznictví se sdílí mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="acdfc-105">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="acdfc-106">K provedení těchto kroků musíte v RCS nejprve dokončit jednotlivé kroky v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="acdfc-106">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="acdfc-107">Je rovněž vyžadován přístup k LCS.</span><span class="sxs-lookup"><span data-stu-id="acdfc-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="acdfc-108">Přihlaste se k aplikaci použitím některé z následující role:</span><span class="sxs-lookup"><span data-stu-id="acdfc-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="acdfc-109">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="acdfc-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="acdfc-110">Správce systému</span><span class="sxs-lookup"><span data-stu-id="acdfc-110">System administrator</span></span>

2. <span data-ttu-id="acdfc-111">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="acdfc-112">Vyberte **Litware, Inc.** a označte ji jako **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-112">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="acdfc-113">Vyberte **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-113">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="acdfc-114">Ujistěte se, že aktuální uživatel Dynamics 365 Finance je členem projektu LCS, který obsahuje [knihovnu majetku](../../lifecycle-services/asset-library.md#asset-library-support), která slouží k importu konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="acdfc-114">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="acdfc-115">K projektu LCS nemůžete přistupovat z úložiště elektronického výkaznictví, které představuje jinou doménu, než je doména použitá v aplikaci Finance.</span><span class="sxs-lookup"><span data-stu-id="acdfc-115">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="acdfc-116">Pokud to zkusíte, zobrazí se prázdný seznam projektů LCS a nebudete moci importovat konfigurace elektronického výkaznictví z knihovny majetku na úrovni projektu v LCS.</span><span class="sxs-lookup"><span data-stu-id="acdfc-116">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="acdfc-117">Chcete-li získat přístup ke knihovnám majektu na úrovni projektu z úložiště elektronického výkaznictví, které slouží k importu konfigurací elektronického výkaznictví, přihlaste se do aplikace Finance pomocí přihlašovacích údajů uživatele, který patří ke klientovi (doméně), pro který byla zřízena aktuální instance Finance.</span><span class="sxs-lookup"><span data-stu-id="acdfc-117">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="acdfc-118">Vytvoření nové konfigurace datového modelu</span><span class="sxs-lookup"><span data-stu-id="acdfc-118">Create a new data model configuration</span></span>

1. <span data-ttu-id="acdfc-119">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-119">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="acdfc-120">Na stránce **Konfigurace** výběrem možnosti **Vytvořit konfiguraci** otevřete rozevírací dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="acdfc-120">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="acdfc-121">V tomto příkladu vytvoříte konfiguraci, která obsahuje vzorový model dat pro elektronické doklady.</span><span class="sxs-lookup"><span data-stu-id="acdfc-121">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="acdfc-122">Tato konfigurace modelu dat bude odeslána do LCS později.</span><span class="sxs-lookup"><span data-stu-id="acdfc-122">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="acdfc-123">V poli **Název** zadejte **Vzorová konfigurace modelu**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-123">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="acdfc-124">V poli **Popis** zadejte **Vzorová konfigurace modelu**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-124">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="acdfc-125">Vyberte **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-125">Select **Create configuration**.</span></span>
6. <span data-ttu-id="acdfc-126">Vyberte **Návrhář modelů**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-126">Select **Model designer**.</span></span>
7. <span data-ttu-id="acdfc-127">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-127">Select **New**.</span></span>
8. <span data-ttu-id="acdfc-128">Do pole **Název** zadejte **Vstupní bod**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-128">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="acdfc-129">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-129">Select **Add**.</span></span>
10. <span data-ttu-id="acdfc-130">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-130">Select **Save**.</span></span>
11. <span data-ttu-id="acdfc-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="acdfc-131">Close the page.</span></span>
12. <span data-ttu-id="acdfc-132">Vyberte **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-132">Select **Change status**.</span></span>
13. <span data-ttu-id="acdfc-133">Zvolte **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-133">Select **Complete**.</span></span>
14. <span data-ttu-id="acdfc-134">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-134">Select **OK**.</span></span>
15. <span data-ttu-id="acdfc-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="acdfc-135">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="acdfc-136">Registrace nového úložiště</span><span class="sxs-lookup"><span data-stu-id="acdfc-136">Register a new repository</span></span>

1. <span data-ttu-id="acdfc-137">Přejděte do části **Správa organizace \> Pracovní prostory \> Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-137">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="acdfc-138">V části **Zprostředkovatelé konfigurace** vyberte dlaždici **Litware Inc.**</span><span class="sxs-lookup"><span data-stu-id="acdfc-138">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="acdfc-139">Na dlaždici **Litware, Inc.** vyberte **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-139">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="acdfc-140">Nyní můžete otevřít seznam úložišť pro poskytovatele konfigurace Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="acdfc-140">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="acdfc-141">Výběrem možnosti **Přidat** otevřete rozevírací dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="acdfc-141">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="acdfc-142">Nyní můžete přidat nové úložiště.</span><span class="sxs-lookup"><span data-stu-id="acdfc-142">You can now add a new repository.</span></span>

5. <span data-ttu-id="acdfc-143">V poli **Typ úložiště konfigurace** vyberte **LCS**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-143">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="acdfc-144">Zvolte **Vytvořit úložiště**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-144">Select **Create repository**.</span></span>
7. <span data-ttu-id="acdfc-145">V poli **Projekt** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="acdfc-145">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="acdfc-146">V tomto příkladu vyberte požadovaný projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="acdfc-146">For this example, select the desired LCS project.</span></span> <span data-ttu-id="acdfc-147">Musíte mít [přístup](#accessconditions) k tomuto projektu.</span><span class="sxs-lookup"><span data-stu-id="acdfc-147">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="acdfc-148">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-148">Select **OK**.</span></span>

    <span data-ttu-id="acdfc-149">Vytvořte nový záznam v úložišti.</span><span class="sxs-lookup"><span data-stu-id="acdfc-149">Complete a new repository entry.</span></span>

9. <span data-ttu-id="acdfc-150">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="acdfc-150">In the list, mark the selected row.</span></span>

    <span data-ttu-id="acdfc-151">V tomto příkladu vyberte záznam úložiště **LCS**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-151">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="acdfc-152">Všimněte si, že registrované úložiště je označeno aktuálním poskytovatelem.</span><span class="sxs-lookup"><span data-stu-id="acdfc-152">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="acdfc-153">Jinými slovy, do tohoto úložiště lze umístit pouze konfigurace, které vlastní tento poskytovatel, a proto je možné je odeslat do vybraného projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="acdfc-153">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="acdfc-154">Zvolte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-154">Select **Open**.</span></span>

    <span data-ttu-id="acdfc-155">Tím otevřete úložiště se seznamem konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="acdfc-155">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="acdfc-156">Pokud vybraný projekt zatím nebyl použit pro sdílení konfigurací elektronického výkaznictví, seznam bude prázdný.</span><span class="sxs-lookup"><span data-stu-id="acdfc-156">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="acdfc-157">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="acdfc-157">Close the page.</span></span>
12. <span data-ttu-id="acdfc-158">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="acdfc-158">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="acdfc-159">Odeslání konfigurace do LCS</span><span class="sxs-lookup"><span data-stu-id="acdfc-159">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="acdfc-160">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-160">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="acdfc-161">Na stránce **Konfigurace** ve stromové struktuře konfigurací vyberte položku **Vzorová konfigurace modelu**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-161">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="acdfc-162">Muíte vybrat vytvořenou konfiguraci, která již byla dokončena.</span><span class="sxs-lookup"><span data-stu-id="acdfc-162">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="acdfc-163">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="acdfc-163">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="acdfc-164">Pro tento příklad vyberte verzi vybrané konfigurace ve stavu **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-164">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="acdfc-165">Vyberte **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-165">Select **Change status**.</span></span>
5. <span data-ttu-id="acdfc-166">Vyberte **Sdílet**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-166">Select **Share**.</span></span>

    <span data-ttu-id="acdfc-167">Stav konfigurace se změní z **Dokončeno** na **Sdíleno**, když je konfigurace publikována v LCS.</span><span class="sxs-lookup"><span data-stu-id="acdfc-167">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="acdfc-168">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-168">Select **OK**.</span></span>
7. <span data-ttu-id="acdfc-169">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="acdfc-169">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="acdfc-170">Pro tento příklad vyberte verzi této konfigurace ve stavu **Sdíleno**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-170">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="acdfc-171">Všimněte si, že stav vybrané verze se změnil z **Dokončeno** na **Sdíleno**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-171">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="acdfc-172">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="acdfc-172">Close the page.</span></span>
9. <span data-ttu-id="acdfc-173">Vyberte **Úložiště**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-173">Select **Repositories**.</span></span>

    <span data-ttu-id="acdfc-174">Nyní můžete otevřít seznam úložišť pro poskytovatele konfigurace Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="acdfc-174">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="acdfc-175">Zvolte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-175">Select **Open**.</span></span>

    <span data-ttu-id="acdfc-176">V tomto příkladu vyberte úložiště **LCS** a otevřete jej.</span><span class="sxs-lookup"><span data-stu-id="acdfc-176">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="acdfc-177">Všimněte si, že vybraná konfigurace je zobrazena jako majetek vybraného projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="acdfc-177">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="acdfc-178">Otevřete LCS přechodem na <https://lcs.dynamics.com>.</span><span class="sxs-lookup"><span data-stu-id="acdfc-178">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="acdfc-179">Otevřete projekt, který byl dříve použit pro registraci úložiště.</span><span class="sxs-lookup"><span data-stu-id="acdfc-179">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="acdfc-180">Otevřete knihovnu majetku projektu.</span><span class="sxs-lookup"><span data-stu-id="acdfc-180">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="acdfc-181">Vyberte typ majetku **Konfigurace GER**.</span><span class="sxs-lookup"><span data-stu-id="acdfc-181">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="acdfc-182">V seznamu by měla být uvedena konfigurace elektronického výkaznictví, kterou jste nahráli.</span><span class="sxs-lookup"><span data-stu-id="acdfc-182">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="acdfc-183">Všimněte si, že odeslané konfigurace LCS je možné importovat do jiné instance, pokud poskytovatelé mají přístupová práva k tomuto projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="acdfc-183">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>
