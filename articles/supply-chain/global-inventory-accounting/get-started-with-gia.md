---
title: Začínáme s modulem Globální účetnictví zásob
description: Toto téma popisuje, jak začít s globálním účetnictvím zásob.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 59f9db309312bbbc88b4fa47c12c4c02f09e7c6d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301691"
---
# <a name="get-started-with-global-inventory-accounting"></a><span data-ttu-id="de755-103">Začínáme s modulem Globální účetnictví zásob</span><span class="sxs-lookup"><span data-stu-id="de755-103">Get started with Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="de755-104">Globální účetnictví zásob umožňuje provádět účetnictví pro více skladů ve vámi vytvořených hlavních knihách globálního účetnictví zásob.</span><span class="sxs-lookup"><span data-stu-id="de755-104">Global Inventory Accounting lets you do multiple inventory accountings in the Global Inventory Accounting ledgers that you've set up.</span></span> <span data-ttu-id="de755-105">Jednotlivé hlavní knihy globálního účetnictví zásob je nutné přidružit ke *konvencím*.</span><span class="sxs-lookup"><span data-stu-id="de755-105">You must associate each Global Inventory Accounting ledger with a *convention*.</span></span> <span data-ttu-id="de755-106">Konvence je kolekce následujících typů zásad účetnictví:</span><span class="sxs-lookup"><span data-stu-id="de755-106">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="de755-107">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="de755-107">Cost object</span></span>
- <span data-ttu-id="de755-108">Základ pro měření vstupu</span><span class="sxs-lookup"><span data-stu-id="de755-108">Input measurement basis</span></span>
- <span data-ttu-id="de755-109">Předpoklad toku nákladů</span><span class="sxs-lookup"><span data-stu-id="de755-109">Cost flow assumption</span></span>
- <span data-ttu-id="de755-110">Prvek nákladů</span><span class="sxs-lookup"><span data-stu-id="de755-110">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="de755-111">I po zapnutí služby Globálního účetnictví zásob můžete v systému Microsoft Dynamics 365 Supply Chain Management stále provádět skladové účetnictví obvyklým způsobem.</span><span class="sxs-lookup"><span data-stu-id="de755-111">Even after you turn on Global Inventory Accounting, you can still do inventory accounting in Microsoft Dynamics 365 Supply Chain Management in the usual way.</span></span>

<span data-ttu-id="de755-112">Globální účetnictví zásob je doplněk.</span><span class="sxs-lookup"><span data-stu-id="de755-112">Global Inventory Accounting is an add-in.</span></span> <span data-ttu-id="de755-113">Chcete-li zpřístupnit její funkce, musíte ji nainstalovat z Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="de755-113">To make its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="de755-114">Můžete ji vyhodnotit v testovacím prostředí před tím, než ji zapnete v provozním prostředí.</span><span class="sxs-lookup"><span data-stu-id="de755-114">You can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="de755-115">Globální účetnictví zásob v současné době nepodporuje všechny funkce správy nákladů, které jsou integrovány do Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="de755-115">Global Inventory Accounting doesn't currently support all the cost management features that are built into Supply Chain Management.</span></span> <span data-ttu-id="de755-116">Proto je důležité, abyste vyhodnotili, zda sada funkcí, která je aktuálně k dispozici, bude vyhovovat vašim požadavkům.</span><span class="sxs-lookup"><span data-stu-id="de755-116">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a><span data-ttu-id="de755-117">Jak získat public preview globálního účetnictví zásob</span><span class="sxs-lookup"><span data-stu-id="de755-117">How to get the Global Inventory Accounting public preview</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de755-118">Chcete-li použít globální účetnictví zásob, musíte mít prostředí s vysokou dostupností LCS (nikoli prostředí OneBox).</span><span class="sxs-lookup"><span data-stu-id="de755-118">To use Global Inventory Accounting, you must have an LCS-enabled high-availability environment (not a OneBox environment).</span></span> <span data-ttu-id="de755-119">Kromě toho musíte používat Supply Chain Management verze 10.0.19 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="de755-119">Additionally, you must be running Supply Chain Management version 10.0.19 or later.</span></span>

<span data-ttu-id="de755-120">Chcete-li se zaregistrovat do public preview Globálního účetnictví zásob, odešlete své ID prostředí LCS e-mailem na adresu [Tým globálního účetnictví zásob](mailto:GlobalInventoryAccounting@service.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="de755-120">To sign up for the Global Inventory Accounting public preview, send your LCS environment ID by email to the [Global Inventory Accounting team](mailto:GlobalInventoryAccounting@service.microsoft.com).</span></span> <span data-ttu-id="de755-121">Po vašech schválení do programu vám tým pošle následný e-mail, který obsahuje klíč beta globálního účetnictví zásob a vaše koncové body služby.</span><span class="sxs-lookup"><span data-stu-id="de755-121">After you're approved for the program, the team will send you a follow-up email that contains a Global Inventory Accounting beta key and your service endpoints.</span></span> <span data-ttu-id="de755-122">Poté, co obdržíte klíč beta, můžete [nainstalovat doplněk](#install).</span><span class="sxs-lookup"><span data-stu-id="de755-122">After you receive the beta key, you can [install the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="de755-123">Licence</span><span class="sxs-lookup"><span data-stu-id="de755-123">Licensing</span></span>

<span data-ttu-id="de755-124">Globální účetnictví zásob je licencováno společně se standardními funkcemi skladového účetnictví, které jsou k dispozici pro řešení Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="de755-124">Global Inventory Accounting is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="de755-125">Chcete-li používat Globální účetnictví zásob, nemusíte kupovat další licenci.</span><span class="sxs-lookup"><span data-stu-id="de755-125">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="de755-126">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="de755-126">Prerequisites</span></span>

### <a name="set-up-microsoft-power-platform-integration"></a><span data-ttu-id="de755-127">Nastavit integraci aplikace Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="de755-127">Set up Microsoft Power Platform integration</span></span>

<span data-ttu-id="de755-128">Než budete moci povolit funkce doplňku, musíte jej integrovat s Microsoft Power Platform provedením těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="de755-128">Before you can enable add-in functionality, you must integrate with Microsoft Power Platform by following these steps.</span></span>

1. <span data-ttu-id="de755-129">Otevřete prostředí LCS, do kterého chcete službu přidat.</span><span class="sxs-lookup"><span data-stu-id="de755-129">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="de755-130">Přejděte na **Úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="de755-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="de755-131">V části **Integrace Power Platform** vyberte **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="de755-131">In the **Power Platform Integration** section, select **Setup**.</span></span>
1. <span data-ttu-id="de755-132">V dialogovém okně **Nastavení prostředí Power Platform** zaškrtněte políčko a poté vyberte **Založit**.</span><span class="sxs-lookup"><span data-stu-id="de755-132">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="de755-133">Nastavení obvykle trvá 60 až 90 minut.</span><span class="sxs-lookup"><span data-stu-id="de755-133">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="de755-134">Po nastavení prostředí Microsoft Power Platform stránka zobrazí název vašeho prostředí.</span><span class="sxs-lookup"><span data-stu-id="de755-134">After setup of the Microsoft Power Platform environment is completed, the page shows the name of your environment.</span></span> <span data-ttu-id="de755-135">Navíc je v sekci **Integrace Power Platform** uvedena věta „Nastavení prostředí Power Platform je dokončeno.“</span><span class="sxs-lookup"><span data-stu-id="de755-135">Additionally, the **Power Platform Integration** section shows the statement, "Power Platform environment setup is complete."</span></span> <span data-ttu-id="de755-136">Globální účetnictví zásob nevyžaduje aplikaci pro dvojí zápis.</span><span class="sxs-lookup"><span data-stu-id="de755-136">Global Inventory Accounting doesn't require a dual-write application.</span></span>

<span data-ttu-id="de755-137">Další informace naleznete v tématu [Nastavení po nasazení prostředí](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span><span class="sxs-lookup"><span data-stu-id="de755-137">For more information, see [Set up after environment deployment](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span></span>

### <a name="set-up-dataverse"></a><span data-ttu-id="de755-138">Nastavit Dataverse</span><span class="sxs-lookup"><span data-stu-id="de755-138">Set up Dataverse</span></span>

<span data-ttu-id="de755-139">Před nastavením Dataverse přidejte principy služby Globální účetnictví zásob do svého klienta podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="de755-139">Before you set up Dataverse, add the Global Inventory Accounting service principles to your tenant by following these steps.</span></span>

1. <span data-ttu-id="de755-140">Nainstalujte Modul Azure AD pro Windows PowerShell v2 dle popisu v tématu [Instalace Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="de755-140">Install Azure AD Module for Windows PowerShell v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
1. <span data-ttu-id="de755-141">Spusťte následující příkaz PowerShellu:</span><span class="sxs-lookup"><span data-stu-id="de755-141">Run the following PowerShell command.</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

<span data-ttu-id="de755-142">Dále vytvořte uživatele aplikace pro globální účetnictví zásob v Dataverse provedením těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="de755-142">Next, create application users for Global Inventory Accounting in Dataverse by following these steps.</span></span>

1. <span data-ttu-id="de755-143">Otevřete adresu URL svého prostředí Dataverse.</span><span class="sxs-lookup"><span data-stu-id="de755-143">Open the URL of your Dataverse environment.</span></span>
1. <span data-ttu-id="de755-144">Přejděte do uzlu **Pokročilá nastavení \> Systém \> Zabezpečení \> Uživatelé** a vytvořte uživatele aplikace.</span><span class="sxs-lookup"><span data-stu-id="de755-144">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="de755-145">Pomocí pole **Zobrazit** změňte zobrazení stránky na *Uživatelé aplikace*.</span><span class="sxs-lookup"><span data-stu-id="de755-145">Use the **View** field to change the page view to *Application users*.</span></span>
1. <span data-ttu-id="de755-146">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="de755-146">Select **New**.</span></span>
1. <span data-ttu-id="de755-147">Nastavte pole **ID aplikace** na *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span><span class="sxs-lookup"><span data-stu-id="de755-147">Set the **Application ID** field to *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span></span>
1. <span data-ttu-id="de755-148">Vyberte příkaz **Přiřadit roli** a potom vyberte *Správce systému*.</span><span class="sxs-lookup"><span data-stu-id="de755-148">Select **Assign Role**, and then select *System Administrator*.</span></span> <span data-ttu-id="de755-149">Pokud existuje role, která je pojmenována *Uživatel Common Data Service*, vyberte ji také.</span><span class="sxs-lookup"><span data-stu-id="de755-149">If there is a role that is named *Common Data Service User*, select it too.</span></span>
1. <span data-ttu-id="de755-150">Opakujte předchozí kroky, ale nastavte pole **ID aplikace** na *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span><span class="sxs-lookup"><span data-stu-id="de755-150">Repeat the preceding steps, but set the **Application ID** field to *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span></span>

<span data-ttu-id="de755-151">Další informace naleznete v tématu [Vytvoření uživatele aplikace](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="de755-151">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

<span data-ttu-id="de755-152">Pokud výchozí jazyk vaší instalace Dataverse není angličtina, postupujte podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="de755-152">If the default language of your Dataverse installation isn't English, follow these steps.</span></span>

1. <span data-ttu-id="de755-153">Přejděte do **Pokročilé nastavení \> Správa \> Jazyky**.</span><span class="sxs-lookup"><span data-stu-id="de755-153">Go to **Advanced Setting \> Administration \> Languages**.</span></span>
1. <span data-ttu-id="de755-154">Vyberte *Angličtina* (*LanguageCode = 1033*) a vyberte **Použít**.</span><span class="sxs-lookup"><span data-stu-id="de755-154">Select *English* (*LanguageCode=1033*), and then select **Apply**.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="de755-155">Instalace doplňku</span><span class="sxs-lookup"><span data-stu-id="de755-155">Install the add-in</span></span>

<span data-ttu-id="de755-156">Podle těchto pokynů nainstalujte doplněk, abyste mohli používat Globální účetnictví zásob.</span><span class="sxs-lookup"><span data-stu-id="de755-156">Follow these steps to install the add-in so that you can use Global Inventory Accounting.</span></span>

1. <span data-ttu-id="de755-157">[Zaregistrujte se](#sign-up) k public preview globálního účetnictví zásob.</span><span class="sxs-lookup"><span data-stu-id="de755-157">[Sign up](#sign-up) for the Global Inventory Accounting public preview.</span></span>
1. <span data-ttu-id="de755-158">Přihlaste se do [LCS](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="de755-158">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="de755-159">Přejděte na **Správu funkcí Preview**.</span><span class="sxs-lookup"><span data-stu-id="de755-159">Go to **Preview feature management**.</span></span>
1. <span data-ttu-id="de755-160">Vyberte znaménko plus (**+**).</span><span class="sxs-lookup"><span data-stu-id="de755-160">Select the plus sign (**+**).</span></span>
1. <span data-ttu-id="de755-161">Do pole **Kód** zadejte pro svůj beta klíč pro doplněk Globální účetnictví zásob.</span><span class="sxs-lookup"><span data-stu-id="de755-161">In the **Code** field, enter your add-in beta key for Global Inventory Accounting.</span></span> <span data-ttu-id="de755-162">(Beta klíč jste měli obdržet e-mailem po zaregistraci.)</span><span class="sxs-lookup"><span data-stu-id="de755-162">(You should have received your beta key by email when you signed up.)</span></span>
1. <span data-ttu-id="de755-163">Vyberte **Odblokovat**.</span><span class="sxs-lookup"><span data-stu-id="de755-163">Select **Unblock**.</span></span>
1. <span data-ttu-id="de755-164">Otevřete prostředí LCS, do kterého chcete službu přidat.</span><span class="sxs-lookup"><span data-stu-id="de755-164">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="de755-165">Přejděte na **Úplné podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="de755-165">Go to **Full details**.</span></span>
1. <span data-ttu-id="de755-166">Přejděte na **Integrace Power Platform** a vyberte **Nastavit**.</span><span class="sxs-lookup"><span data-stu-id="de755-166">Go to **Power Platform Integration**, and select **Setup**.</span></span>
1. <span data-ttu-id="de755-167">V dialogovém okně **Nastavení prostředí Power Platform** zaškrtněte políčko a poté vyberte **Založit**.</span><span class="sxs-lookup"><span data-stu-id="de755-167">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="de755-168">Nastavení obvykle trvá 60 až 90 minut.</span><span class="sxs-lookup"><span data-stu-id="de755-168">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="de755-169">Po nastavení prostředí Microsoft Power Platform na pevné záložce **Doplňky prostředí** vyberte **Nainstalovat nový doplněk**.</span><span class="sxs-lookup"><span data-stu-id="de755-169">After setup of the Microsoft Power Platform environment is completed, on the **Environment add-ins** FastTab, select **Install a new add-in**.</span></span>
1. <span data-ttu-id="de755-170">Vyberte **Globální účetnictví zásob**.</span><span class="sxs-lookup"><span data-stu-id="de755-170">Select **Global inventory accounting**.</span></span>
1. <span data-ttu-id="de755-171">Postupujte podle pokynů instalační příručky a vyjádřete souhlas s podmínkami a ujednáními.</span><span class="sxs-lookup"><span data-stu-id="de755-171">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="de755-172">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="de755-172">Select **Install**.</span></span>
1. <span data-ttu-id="de755-173">Na záložce s náhledem **Doplňky prostředí** byste měli vidět, že je instalována služba Globální účetnictví zásob.</span><span class="sxs-lookup"><span data-stu-id="de755-173">On the **Environment add-ins** FastTab, you should see that Global Inventory Accounting is being installed.</span></span> <span data-ttu-id="de755-174">Po několika minutách by se stav měl změnit z *Probíhá instalace* na *Nainstalováno*.</span><span class="sxs-lookup"><span data-stu-id="de755-174">After a few minutes, the status should change from *Installing* to *Installed*.</span></span> <span data-ttu-id="de755-175">(Tato změna se může projevit až po aktualizaci stránky.) V tomto okamžiku je Globální účetnictví zásob připraveno k použití.</span><span class="sxs-lookup"><span data-stu-id="de755-175">(You might have to refresh the page to see this change.) At that point, Global Inventory Accounting is ready to use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="de755-176">Nastavení integrace</span><span class="sxs-lookup"><span data-stu-id="de755-176">Set up the integration</span></span>

<span data-ttu-id="de755-177">Pomocí těchto kroků nastavíte integraci mezi Globálním účetnictvím zásob a Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="de755-177">Follow these steps to set up the integration between Global Inventory Accounting and Supply Chain Management.</span></span>

1. <span data-ttu-id="de755-178">Přihlaste se k aplikaci Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="de755-178">Sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="de755-179">Přejděte do nabídky **Správa systému \> Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="de755-179">Go to **System administration \> Feature Management**.</span></span>
1. <span data-ttu-id="de755-180">Vyberte možnost **Zkontrolovat aktualizace**.</span><span class="sxs-lookup"><span data-stu-id="de755-180">Select **Check for updates**.</span></span>
1. <span data-ttu-id="de755-181">Na kartě **Všechny** vyhledejte pojmenovanou funkci *Globální účetnictví zásob*.</span><span class="sxs-lookup"><span data-stu-id="de755-181">On the **All** tab, search for the feature that is named *Global inventory accounting*.</span></span>
1. <span data-ttu-id="de755-182">Vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="de755-182">Select **Enable now**.</span></span>
1. <span data-ttu-id="de755-183">Přejděte na **Globální účetnictví zásob \> Nastavit \> Parametry Globálního účetnictví zásob \> Parametry integrace**.</span><span class="sxs-lookup"><span data-stu-id="de755-183">Go to **Global inventory accounting \> Setup \> Global inventory accounting parameters \> Integrations parameters**.</span></span>
1. <span data-ttu-id="de755-184">Do pole **Koncový bod datové služby** a **Koncový bod globálního účetnictví zásob** zadejte adresy URL z e-mailu, který tým globálního účetnictví zásob poslal, když jste se přihlásili k náhledu.</span><span class="sxs-lookup"><span data-stu-id="de755-184">In the **Data service endpoint** and **Global inventory accounting endpoint** fields, enter the URLs from the email that the Global Inventory Accounting team sent when you signed up for the preview.</span></span>

<span data-ttu-id="de755-185">Globální účetnictví zásob je nyní připraveno k použití.</span><span class="sxs-lookup"><span data-stu-id="de755-185">Global Inventory Accounting is now ready to use.</span></span>
