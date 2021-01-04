---
title: Regulatory Configuration Services (RCS) - funkce globalizace
description: Toto téma vysvětluje, jak pomocí služby Microsoft Regulatory Configuration Services  (RCS) a globálního úložiště vytvářet a používat funkce globalizace.
author: JaneA07
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: ae46dab5250fbe8096f43e420cb7ef33a5862af0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441065"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a><span data-ttu-id="079be-103">Regulatory Configuration Services (RCS) - funkce globalizace</span><span class="sxs-lookup"><span data-stu-id="079be-103">Regulatory Configuration Services (RCS) - Globalization features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="079be-104">Službu Microsoft Regulatory Configuration Services (RCS) můžete použít k vytvoření funkce globalizace, kterou lze použít v globalizačních službách, jako je například služba elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="079be-104">You can use Microsoft Regulatory Configuration Services (RCS) to create a Globalization feature that can be used in Globalization services, such as an e-invoicing service.</span></span> <span data-ttu-id="079be-105">RCS umožňuje provádět tyto úkoly:</span><span class="sxs-lookup"><span data-stu-id="079be-105">RCS lets you perform these tasks:</span></span>

- <span data-ttu-id="079be-106">Definovat související komponenty funkce.</span><span class="sxs-lookup"><span data-stu-id="079be-106">Define related components of a feature.</span></span>
- <span data-ttu-id="079be-107">Spravovat životní cyklus funkce prostřednictvím stavu funkce.</span><span class="sxs-lookup"><span data-stu-id="079be-107">Manage the feature lifecycle through a feature's status.</span></span>
- <span data-ttu-id="079be-108">Zpřístupnit funkci pro definované prostředí.</span><span class="sxs-lookup"><span data-stu-id="079be-108">Make a feature available for defined environments.</span></span>
- <span data-ttu-id="079be-109">Sdílet funkci s jinými organizacemi.</span><span class="sxs-lookup"><span data-stu-id="079be-109">Share a feature with other organizations.</span></span>

<span data-ttu-id="079be-110">Následující postupy vysvětlují, jak může uživatel v RCS přidat funkci globalizace a související součásti, aktualizovat stav funkce a zpřístupnit tuto funkci tak, aby ji bylo možné použít ve službách globalizace.</span><span class="sxs-lookup"><span data-stu-id="079be-110">The following procedures explain how a user in RCS can add a Globalization feature and related components, update the feature's status, and make the feature available so that it can be used in Globalization services.</span></span>

<span data-ttu-id="079be-111">Před dokončením postupů musíte provést kroky související s následujícími úkoly:</span><span class="sxs-lookup"><span data-stu-id="079be-111">Before you complete the procedures, you must complete the steps that are related to the following tasks:</span></span>

- <span data-ttu-id="079be-112">Přístup k instanci RCS.</span><span class="sxs-lookup"><span data-stu-id="079be-112">Accessing an RCS instance.</span></span>
- <span data-ttu-id="079be-113">Vytvoření a aktivace poskytovatele konfigurace.</span><span class="sxs-lookup"><span data-stu-id="079be-113">Creating and activating a configuration provider.</span></span> <span data-ttu-id="079be-114">Další informace naleznete ve [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="079be-114">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="079be-115">V instanci aplikací Finance and Operations proveďte následující postup.</span><span class="sxs-lookup"><span data-stu-id="079be-115">In your Finance and Operations apps instance, follow these steps.</span></span>

1. <span data-ttu-id="079be-116">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="079be-116">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="079be-117">Nemáte-li pro vaši společnost zřízeno žádné RCS prostředí, pro její zřízení vyberte odkaz **Regulatory Services – Konfigurace** a postupujte podle pokynů.</span><span class="sxs-lookup"><span data-stu-id="079be-117">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration**, and follow the instructions to provision one.</span></span>

> [!NOTE]
> <span data-ttu-id="079be-118">Pokud již bylo pro vaši společnost zřízeno prostředí RCS, přejděte do prostředí pomocí adresy URL výběrem možnosti přihlášení.</span><span class="sxs-lookup"><span data-stu-id="079be-118">If an RCS environment has already been provisioned for your company, use the page URL to access the environment by selecting the sign-in option.</span></span>

## <a name="turn-on-the-globalization-features"></a><span data-ttu-id="079be-119">Zapnutí funkcí globalizace</span><span class="sxs-lookup"><span data-stu-id="079be-119">Turn on the Globalization features</span></span>

1. <span data-ttu-id="079be-120">V instanci RCS vyberte dlaždici **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="079be-120">In your RCS instance, select the **Feature management** tile.</span></span>
2. <span data-ttu-id="079be-121">V pracovním prostoru **Správa funkcí** vyberte pracovní prostor **Funkce globalizace** v seznamu a poté vyberte **Povolit hned**.</span><span class="sxs-lookup"><span data-stu-id="079be-121">In the **Feature management** workspace, select **Globalization features** in the list, and then select **Enable now**.</span></span>

    ![Funkce globalizace ve správě funkcí](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a><span data-ttu-id="079be-123">Globalizační funkce</span><span class="sxs-lookup"><span data-stu-id="079be-123">Globalization features</span></span>

<span data-ttu-id="079be-124">Chcete-li použít funkci globalizace, musíte ji nejprve naimportovat z globálního úložiště a vytvořit si vlastní verzi.</span><span class="sxs-lookup"><span data-stu-id="079be-124">To use a Globalization feature, you must first import it from the the Global repository and create your own version of it.</span></span> <span data-ttu-id="079be-125">Existují dva způsoby, jak přidat funkce globalizace:</span><span class="sxs-lookup"><span data-stu-id="079be-125">There are two ways to add Globalization features:</span></span>

- <span data-ttu-id="079be-126">Přidejte odvozenou funkci, která je založena na existující funkci, která byla publikována nebo sdílena.</span><span class="sxs-lookup"><span data-stu-id="079be-126">Add a derived feature that is based on an existing feature that has been published or shared.</span></span>
- <span data-ttu-id="079be-127">Přidejte novou funkci, kterou jste vytvořili od nuly.</span><span class="sxs-lookup"><span data-stu-id="079be-127">Add a new feature that you've created from scratch.</span></span>

## <a name="access-globalization-features"></a><span data-ttu-id="079be-128">Přístup k funkcím globalizace</span><span class="sxs-lookup"><span data-stu-id="079be-128">Access Globalization features</span></span>

1. <span data-ttu-id="079be-129">Ujistěte se, že je funkce **Globalizační funkce** v okně Správa funkcí zapnutá, jak je popsáno dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="079be-129">Make sure that the **Globalization features** feature is turned on in Feature management, as described earlier in this topic.</span></span>
2. <span data-ttu-id="079be-130">Otevřete nový pracovní prostor **Globalizační funkce** a poté v části **Funkce** vyberte dlaždici **elektronická fakturace**.</span><span class="sxs-lookup"><span data-stu-id="079be-130">Open the new **Globalization Features** workspace, and then, under **Features**, select the **e-Invoicing** tile.</span></span>

    ![Pracovní prostor Globální funkce](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    <span data-ttu-id="079be-132">Stránka **Funkce elektronické fakturace** je otevřená.</span><span class="sxs-lookup"><span data-stu-id="079be-132">The **e-Invoicing Features** page is opened.</span></span>

    ![Stránka Funkce elektronické fakturace](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a><span data-ttu-id="079be-134">Přidejte odvozenou funkci globalizace</span><span class="sxs-lookup"><span data-stu-id="079be-134">Add a derived Globalization feature</span></span>

<span data-ttu-id="079be-135">Můžete přidat novou funkci globalizace odvozením z existující funkce, která byla publikována nebo sdílena.</span><span class="sxs-lookup"><span data-stu-id="079be-135">You can add a new Globalization feature by deriving it from an existing feature that has been published or shared.</span></span>

1. <span data-ttu-id="079be-136">Výběrem možnosti **Import** otevřete stránku **Import funkce z globálního úložiště**.</span><span class="sxs-lookup"><span data-stu-id="079be-136">Select **Import** to open the **Import feature from Global repository** page.</span></span>

    ![Import funkce ze stránky Globální úložiště](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. <span data-ttu-id="079be-138">Výběrem volby **Synchronizovat** získáte nejnovější funkce.</span><span class="sxs-lookup"><span data-stu-id="079be-138">Select **Synchronize** to get the latest features.</span></span>

    <span data-ttu-id="079be-139">Synchronizovaný seznam obsahuje funkce, které máte k dispozici buď proto, že byly publikovány společností Microsoft, nebo proto, že byly s vámi sdíleny jiným poskytovatelem konfigurace.</span><span class="sxs-lookup"><span data-stu-id="079be-139">The synced list includes features that are available to you either because they were published by Microsoft or because they were shared with you by another configuration provider.</span></span>

    ![Synchronizovaný seznam funkcí](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. <span data-ttu-id="079be-141">V seznamu vyberte funkce, které chcete importovat, a poté vyberte **Import**.</span><span class="sxs-lookup"><span data-stu-id="079be-141">In the list, select the features to import, and then select **Import**.</span></span> <span data-ttu-id="079be-142">Po úspěšném importu vybraných funkcí se zobrazí zpráva.</span><span class="sxs-lookup"><span data-stu-id="079be-142">You receive a message when the selected features have been successfully imported.</span></span>

    ![Zpráva o úspěšném importu](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. <span data-ttu-id="079be-144">Vyberte **Přidat** a poté v rozevíracím seznamu vyberte možnost **Na základě stávající verze**.</span><span class="sxs-lookup"><span data-stu-id="079be-144">Select **Add**, and then, in the drop-down dialog box, select the **Based on existing version** option.</span></span>
5. <span data-ttu-id="079be-145">Zadejte název a popis funkce.</span><span class="sxs-lookup"><span data-stu-id="079be-145">Enter a name and description for the feature.</span></span>
6. <span data-ttu-id="079be-146">V seznamu dostupných funkcí vyberte základní verzi funkce a poté vyberte **Vytvořit funkci**.</span><span class="sxs-lookup"><span data-stu-id="079be-146">In the list of available features, select the base version of the feature, and then select **Create feature**.</span></span>

    ![Přidání odvozené funkce](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    <span data-ttu-id="079be-148">Funkce, kterou jste přidali, je vytvořena a má stav **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="079be-148">The feature that you added is created and has a status of **Draft**.</span></span>

    ![Odvozená funkce, která má stav Koncept](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. <span data-ttu-id="079be-150">Zkontrolujte součásti funkcí a zjistěte, zda jsou vyžadovány aktualizace:</span><span class="sxs-lookup"><span data-stu-id="079be-150">Review the feature components to determine whether updates are required:</span></span>

    - <span data-ttu-id="079be-151">Prohlédněte si konfigurace v případě, že potřebujete přizpůsobit formáty elektronických zpráv (ER) a jejich vazby na mapování formátu pro verzi funkce.</span><span class="sxs-lookup"><span data-stu-id="079be-151">Review the configurations, in case you need to customize the Electronic reporting (ER) formats and their binding with format mappings for the feature version.</span></span>
    - <span data-ttu-id="079be-152">Zkontrolujte nastavení, v případě, že potřebujete přizpůsobit kartu **Akce**, kartu **Pravidla použitelnosti** nebo kartu **Proměnné** pro pro verzi funkce.</span><span class="sxs-lookup"><span data-stu-id="079be-152">Review the setup, in case you need to customize the **Actions** tab, **Applicability rules** tab, or **Variables** tab for the feature version.</span></span>

8. <span data-ttu-id="079be-153">Na kartě **Verze** vyberte datum **Účinné od** a zadejte popis, pokud je pole **Popis** prázdné.</span><span class="sxs-lookup"><span data-stu-id="079be-153">On the **Versions** tab, select an **Effective from** date, and enter a description if the **Description** field is blank.</span></span>
9. <span data-ttu-id="079be-154">Vyberte **Změnit stav** k dokončení funkce.</span><span class="sxs-lookup"><span data-stu-id="079be-154">Select **Change status** to complete the feature.</span></span> <span data-ttu-id="079be-155">Dokončené funkce mohou být zpřístupněny pro konkrétní prostředí, takže mohou být použity ve službách globalizace nebo mohou být publikovány do globálního úložiště.</span><span class="sxs-lookup"><span data-stu-id="079be-155">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="079be-156">Funkce, které mají hodnotu **Stav verze funkce** **Publikováno**, lze sdílet s externími organizacemi.</span><span class="sxs-lookup"><span data-stu-id="079be-156">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="add-a-new-globalization-feature"></a><span data-ttu-id="079be-157">Přidejte novou funkci globalizace</span><span class="sxs-lookup"><span data-stu-id="079be-157">Add a new Globalization feature</span></span>

<span data-ttu-id="079be-158">Můžete přidat novou funkci globalizace vytvořením od nuly.</span><span class="sxs-lookup"><span data-stu-id="079be-158">You can add a new Globalization feature by creating it from scratch.</span></span>

1. <span data-ttu-id="079be-159">Na stránce **Importovat funkci z globálního úložiště** vyberte **Přidat** a pak v dialogovém okně rozevíracího seznamu vyberte možnost **Nová funkce**.</span><span class="sxs-lookup"><span data-stu-id="079be-159">On the **Import feature from Global repository** page, select **Add**, and then, in the drop-down dialog box, select the **New feature** option.</span></span>
2. <span data-ttu-id="079be-160">Zadejte název a popis funkce.</span><span class="sxs-lookup"><span data-stu-id="079be-160">Enter a name and description for the feature.</span></span>
3. <span data-ttu-id="079be-161">Vyberte **Vytvořit funkci**.</span><span class="sxs-lookup"><span data-stu-id="079be-161">Select **Create feature**.</span></span>

    ![Přidání nové funkce](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. <span data-ttu-id="079be-163">Na kartě **Verze** vyberte datum **Platné od** a pak výběrem možnosti **Změnit stav** funkci dokončete.</span><span class="sxs-lookup"><span data-stu-id="079be-163">On the **Versions** tab, select an **Effective from** date, and then select **Change status** to complete the feature.</span></span> <span data-ttu-id="079be-164">Dokončené funkce mohou být zpřístupněny pro konkrétní prostředí, takže mohou být použity ve službách globalizace nebo mohou být publikovány do globálního úložiště.</span><span class="sxs-lookup"><span data-stu-id="079be-164">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="079be-165">Funkce, které mají hodnotu **Stav verze funkce** **Publikováno**, lze sdílet s externími organizacemi.</span><span class="sxs-lookup"><span data-stu-id="079be-165">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="feature-component-overview"></a><span data-ttu-id="079be-166">Přehled součástí funkce</span><span class="sxs-lookup"><span data-stu-id="079be-166">Feature component overview</span></span>

<span data-ttu-id="079be-167">Funkce globalizace mají několik součástí:</span><span class="sxs-lookup"><span data-stu-id="079be-167">Globalization features have several components:</span></span>

- <span data-ttu-id="079be-168">**Verze** - Tato součást podporuje správu životního cyklu funkce a umožňuje uživatelům spravovat stav různých verzí této funkce.</span><span class="sxs-lookup"><span data-stu-id="079be-168">**Version** – This component supports feature lifecycle management and lets users manage the status for different versions of the feature.</span></span>
- <span data-ttu-id="079be-169">**Konfigurace** - Tato součást umožňuje uživatelům spravovat, prohlížet a upravovat související formáty ER a mapování formátů.</span><span class="sxs-lookup"><span data-stu-id="079be-169">**Configurations** – This component lets users manage, view, and edit related ER formats and format mappings.</span></span>
- <span data-ttu-id="079be-170">**Nastavení** - Tato součást umožňuje uživatelům globalizačních služeb, jako je například elektronická fakturace, spravovat nastavení související verze funkce.</span><span class="sxs-lookup"><span data-stu-id="079be-170">**Setups** – This component lets users of Globalization services, such as an e-invoicing service, manage the setup of the related feature version.</span></span> <span data-ttu-id="079be-171">Proto podporuje flexibilní sestavování pravidel komunikace a odpovědí.</span><span class="sxs-lookup"><span data-stu-id="079be-171">Therefore, it supports the flexible construction of communication and responses rules.</span></span>
- <span data-ttu-id="079be-172">**Prostředí** - Tato součást umožňuje uživatelům globalizačních služeb, jako je například elektronická fakturace, spravovat prostředí, ve kterém se používá nastavení verze funkce, a udělit oprávnění uživatelům, kteří k nim budou mít přístup.</span><span class="sxs-lookup"><span data-stu-id="079be-172">**Environment** – This component lets users of Globalization services, such as an e-invoicing service, manage the environment where the feature version setup is used and grant authorization to the users who will have access to it.</span></span>
- <span data-ttu-id="079be-173">**Organizace** - Tato součást umožňuje uživatelům sdílet tuto funkci s externími organizacemi.</span><span class="sxs-lookup"><span data-stu-id="079be-173">**Organizations** – This component lets users to share the feature with external organizations.</span></span>

## <a name="configuring-feature-components"></a><span data-ttu-id="079be-174">Konfigurace součástí funkcí</span><span class="sxs-lookup"><span data-stu-id="079be-174">Configuring feature components</span></span>

### <a name="version-and-status"></a><span data-ttu-id="079be-175">Verze a stav</span><span class="sxs-lookup"><span data-stu-id="079be-175">Version and status</span></span>

<span data-ttu-id="079be-176">Tato verze se používá ke správě životního cyklu funkce globalizace.</span><span class="sxs-lookup"><span data-stu-id="079be-176">The version is used to manage the Globalization feature lifecycle.</span></span>

<span data-ttu-id="079be-177">Stav lze změnit v poli **Stav** na kartě **Verze**. K dispozici jsou následující stavy:</span><span class="sxs-lookup"><span data-stu-id="079be-177">The status can be changed in the **Status** field on the **Version** tab. The following statuses are available:</span></span>

- <span data-ttu-id="079be-178">**Koncept** - Funkci lze upravit, pouze pokud je v tomto stavu.</span><span class="sxs-lookup"><span data-stu-id="079be-178">**Draft** – The feature can be edited only when it's in this status.</span></span>
- <span data-ttu-id="079be-179">**Dokončit** - Funkce a všechny související součásti byly dokončeny (finalizovány) a nelze je upravovat.</span><span class="sxs-lookup"><span data-stu-id="079be-179">**Complete** – The feature and all related components have been finalized (completed) and can't be edited.</span></span>
- <span data-ttu-id="079be-180">**Publikováno** - Funkce a všechny související součásti byly publikovány v globálním úložišti.</span><span class="sxs-lookup"><span data-stu-id="079be-180">**Published** – The feature and all related components have been published to the Global repository.</span></span>
- <span data-ttu-id="079be-181">**Sdíleno** - Funkce a všechny související součásti byly sdíleny s externími organizacemi.</span><span class="sxs-lookup"><span data-stu-id="079be-181">**Shared** – The feature and all related components have been shared with external organizations.</span></span>
- <span data-ttu-id="079be-182">**Povoleno** - Funkce a všechny související součásti byly povoleny pro použití ve službě Globalizace, jako je služba elektronické fakturace.</span><span class="sxs-lookup"><span data-stu-id="079be-182">**Enabled** – The feature and all related components have been enabled for use in a Globalization service, such as an e-invoicing service.</span></span>

> [!NOTE]
> <span data-ttu-id="079be-183">Funkce se musí přes některé z těchto stavů postupně pohybovat.</span><span class="sxs-lookup"><span data-stu-id="079be-183">Features must move sequentially through some of these statuses.</span></span> <span data-ttu-id="079be-184">Proto nemusí být v každé fázi životního cyklu k dispozici každý stav.</span><span class="sxs-lookup"><span data-stu-id="079be-184">Therefore, not every status might be available at every lifecycle stage.</span></span>

### <a name="configurations"></a><span data-ttu-id="079be-185">Konfigurace</span><span class="sxs-lookup"><span data-stu-id="079be-185">Configurations</span></span>

<span data-ttu-id="079be-186">K dispozici jsou následující akce pro konfigurace:</span><span class="sxs-lookup"><span data-stu-id="079be-186">The following actions are available for configurations:</span></span>

- <span data-ttu-id="079be-187">**Zobrazení** - Prohlédněte si základní konfigurace funkcí, které nevyžadují žádnou aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="079be-187">**View** – View the underlying feature configurations that don't require any update.</span></span>
- <span data-ttu-id="079be-188">**Upravit** - Vytvořte pracovní verzi vybrané konfigurace, abyste mohli upravovat formát nebo mapování formátu v Návrháři formátů.</span><span class="sxs-lookup"><span data-stu-id="079be-188">**Edit** – Create a draft version of a selected configuration so that you can edit the format or format mapping in the Format designer.</span></span>
- <span data-ttu-id="079be-189">**Odstranit** - Odstranění vybrané konfigurace z funkce.</span><span class="sxs-lookup"><span data-stu-id="079be-189">**Delete** – Delete a selected configuration from the feature.</span></span>
- <span data-ttu-id="079be-190">**Přeskládat** - Přeskládejte funkci.</span><span class="sxs-lookup"><span data-stu-id="079be-190">**Rebase** – Rebase the feature.</span></span> <span data-ttu-id="079be-191">Další informace naleznete v části [Přeskládání odvozených funkcí globalizace](#rebase) dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="079be-191">For more information, see the [Rebase derived Globalization features](#rebase) section later in this topic.</span></span>

### <a name="setups"></a><span data-ttu-id="079be-192">Nastavení</span><span class="sxs-lookup"><span data-stu-id="079be-192">Setups</span></span>

<span data-ttu-id="079be-193">Pro nastavení funkcí jsou k dispozici následující akce:</span><span class="sxs-lookup"><span data-stu-id="079be-193">The following actions are available for feature setups:</span></span>

- <span data-ttu-id="079be-194">**Přidat** - Vytvoření nového nastavení funkce.</span><span class="sxs-lookup"><span data-stu-id="079be-194">**Add** – Create a new feature setup.</span></span> <span data-ttu-id="079be-195">Toto nastavení funkce lze odvodit z existujícího nastavení funkce nebo vytvořit od nuly.</span><span class="sxs-lookup"><span data-stu-id="079be-195">This feature setup can be derived from an existing feature setup or created from scratch.</span></span>
- <span data-ttu-id="079be-196">**Odstranit** - Odstraní vybrané nastavení funkce.</span><span class="sxs-lookup"><span data-stu-id="079be-196">**Delete** – Delete a selected feature setup.</span></span>
- <span data-ttu-id="079be-197">**Zobrazit** - Zobrazí základní nastavení funkce, které nevyžaduje žádné změny.</span><span class="sxs-lookup"><span data-stu-id="079be-197">**View** – View an underlying feature setup that doesn't require any changes.</span></span>
- <span data-ttu-id="079be-198">**Upravit** - Vytvoření, odstranění nebo úprava atributů tří hlavních součástí nastavení funkcí:</span><span class="sxs-lookup"><span data-stu-id="079be-198">**Edit** – Create, delete, or modify the attributes of the three main components of a feature setup:</span></span>

    - <span data-ttu-id="079be-199">Akce a jejich parametry</span><span class="sxs-lookup"><span data-stu-id="079be-199">Actions and their parameters</span></span>
    - <span data-ttu-id="079be-200">Pravidla použitelnosti</span><span class="sxs-lookup"><span data-stu-id="079be-200">Applicability rules</span></span>
    - <span data-ttu-id="079be-201">Proměnné</span><span class="sxs-lookup"><span data-stu-id="079be-201">Variables</span></span>

![Stránka nastavení verze funkce](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a><span data-ttu-id="079be-203">Prostředí</span><span class="sxs-lookup"><span data-stu-id="079be-203">Environments</span></span>

<span data-ttu-id="079be-204">K dispozici jsou následující akce pro prostředí:</span><span class="sxs-lookup"><span data-stu-id="079be-204">The following actions are available for environments:</span></span>

- <span data-ttu-id="079be-205">**Povolit** - U vybrané verze funkce vyberte publikované prostředí a vyberte datum **Platnost od**, odkdy by mělo být k dispozici.</span><span class="sxs-lookup"><span data-stu-id="079be-205">**Enable** – For a selected feature version, select a published environment, and select an **Effective from** date when it should be available.</span></span> <span data-ttu-id="079be-206">Další informace naleznete v části [Konfigurace prostředí pro povolení](#configureenvironment) dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="079be-206">For more information, see the [Configure environments for enablement](#configureenvironment) section later in this topic.</span></span>
- <span data-ttu-id="079be-207">**Zrušit** - Odebere prostředí pro nastavení funkce.</span><span class="sxs-lookup"><span data-stu-id="079be-207">**Cancel** – Remove an environment for a feature setup.</span></span>

### <a name="organizations"></a><span data-ttu-id="079be-208">Organizace</span><span class="sxs-lookup"><span data-stu-id="079be-208">Organizations</span></span>

<span data-ttu-id="079be-209">Chcete-li sdílet funkci globalizace s externí organizací, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="079be-209">Follow these steps to share a Globalization feature with an external organization.</span></span>

1. <span data-ttu-id="079be-210">Na stránce **Funkce elektronické fakturace** vyberte funkci a verzi funkce, kterou chcete sdílet.</span><span class="sxs-lookup"><span data-stu-id="079be-210">On the **e-Invoicing features** page, select the feature and the feature version to share.</span></span>
2. <span data-ttu-id="079be-211">Na kartě **Organizace** vyberte **Sdílet s** a poté v rozevíracím seznamu zadejte název domény organizace.</span><span class="sxs-lookup"><span data-stu-id="079be-211">On the **Organizations** tab, select **Share with**, and then, in the drop-down dialog box, enter the organization's domain name.</span></span>
3. <span data-ttu-id="079be-212">Vyberte **Sdílet**.</span><span class="sxs-lookup"><span data-stu-id="079be-212">Select **Share**.</span></span>

    ![Sdílení funkce s organizací.](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

<span data-ttu-id="079be-214">Funkce je sdílena s vybranou organizací a je k dispozici této organizaci v globálním úložišti.</span><span class="sxs-lookup"><span data-stu-id="079be-214">The feature is shared with the selected organization and is available for that organization in the Global repository.</span></span> <span data-ttu-id="079be-215">Odtud lze funkci importovat do instance RCS organizace nebo Dynamics 365 Finance, aby mohla být použita.</span><span class="sxs-lookup"><span data-stu-id="079be-215">From there, the feature can be imported into the organization's instance of RCS or Dynamics 365 Finance so that it can be used.</span></span>

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a><span data-ttu-id="079be-216">Přeskládání odvozené funkce globalizace</span><span class="sxs-lookup"><span data-stu-id="079be-216">Rebase derived Globalization features</span></span>

<span data-ttu-id="079be-217">Odvozenou funkci globalizace můžete znovu převést na novou nebo aktualizovanou základní verzi funkce.</span><span class="sxs-lookup"><span data-stu-id="079be-217">You can rebase a derived Globalization feature to the new or updated base feature version.</span></span> <span data-ttu-id="079be-218">Tímto způsobem lze automaticky aktualizovat změny, ke kterým došlo v základní verzi.</span><span class="sxs-lookup"><span data-stu-id="079be-218">In this way, changes that have occurred in the base version can be automatically updated.</span></span> <span data-ttu-id="079be-219">Aktualizovaná verze základní funkce je vytvořena původním poskytovatelem konfigurace a poté je publikována nebo sdílena.</span><span class="sxs-lookup"><span data-stu-id="079be-219">The updated base feature version is created by the originating configuration provider, and it's then published or shared.</span></span>

![Aktualizovaná verze základní funkce](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

<span data-ttu-id="079be-221">Pokud například chcete znovu převést odvozenou verzi funkce, kterou jste vytvořili, nejprve získáte nejnovější verzi funkce importem z globálního úložiště.</span><span class="sxs-lookup"><span data-stu-id="079be-221">For example, if you want to rebase the derived version of a feature that you created, you first get the latest version of the feature by importing it from the Global repository.</span></span>

1. <span data-ttu-id="079be-222">Na stránce **Funkce elektronické fakturace** vyberte **Import**.</span><span class="sxs-lookup"><span data-stu-id="079be-222">On the **e-Invoicing features** page, select **Import**.</span></span>
2. <span data-ttu-id="079be-223">Výběrem volby **Synchronizovat** získáte nejnovější funkce.</span><span class="sxs-lookup"><span data-stu-id="079be-223">Select **Synchronize** to get the latest features.</span></span>
3. <span data-ttu-id="079be-224">V seznamu funkcí vyberte funkce, které chcete importovat, a poté vyberte **Import**.</span><span class="sxs-lookup"><span data-stu-id="079be-224">In the list of features, select the features to import, and then select **Import**.</span></span>

    ![Import nejnovější verze funkce](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. <span data-ttu-id="079be-226">V seznamu funkcí vyberte funkci, kterou chcete obnovit.</span><span class="sxs-lookup"><span data-stu-id="079be-226">In the list of features, select the feature to rebase.</span></span>
5. <span data-ttu-id="079be-227">Na kartě **Verze** vyberte **Nový** pro vytvoření rámcové verze.</span><span class="sxs-lookup"><span data-stu-id="079be-227">On the **Version** tab, select **New** to create a draft version.</span></span>

    ![Vytvořená nová rámcová verze](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. <span data-ttu-id="079be-229">Vyberte **Přeskládat**.</span><span class="sxs-lookup"><span data-stu-id="079be-229">Select **Rebase**.</span></span>
7. <span data-ttu-id="079be-230">V dialogovém okně **Přeskládat** vyberte nejnovější verzi funkce, na kterou chcete znovu přejít.</span><span class="sxs-lookup"><span data-stu-id="079be-230">In the **Rebase** dialog box, select the latest version of the feature to rebase to.</span></span>

    ![Dialogové okno Přeskládat](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. <span data-ttu-id="079be-232">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="079be-232">Select **OK**.</span></span>
9. <span data-ttu-id="079be-233">Zkontrolujte součásti funkce a proveďte požadované změny.</span><span class="sxs-lookup"><span data-stu-id="079be-233">Review the feature components, and make any changes that are required.</span></span>
10. <span data-ttu-id="079be-234">Vyberte **Změnit stav** k dokončení funkce přeskládání.</span><span class="sxs-lookup"><span data-stu-id="079be-234">Select **Change status** to complete the rebased feature.</span></span> <span data-ttu-id="079be-235">Po dokončení přeskládání můžete provádět další akce.</span><span class="sxs-lookup"><span data-stu-id="079be-235">When the rebase is completed, you can perform additional actions.</span></span> <span data-ttu-id="079be-236">Tuto funkci můžete například zveřejnit a zpřístupnit ji pro použití v globalizačních službách.</span><span class="sxs-lookup"><span data-stu-id="079be-236">For example, you can publish the feature and make it available for use in Globalization services.</span></span>

    ![Stav funkce byl aktualizován na Dokončeno](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a><span data-ttu-id="079be-238">Konfigurace prostředí pro funkce globalizace</span><span class="sxs-lookup"><span data-stu-id="079be-238">Configure environments for Globalization features</span></span>

<span data-ttu-id="079be-239">Uživatelé globalizačních služeb mohou spravovat prostředí, aby nastavili funkci globalizace a udělili oprávnění ostatním uživatelům, kteří k ní budou mít přístup.</span><span class="sxs-lookup"><span data-stu-id="079be-239">Users of Globalization services can manage the environment to set up a Globalization feature and grant authorization to other users who will have access to it.</span></span>

1. <span data-ttu-id="079be-240">V pracovním prostoru **Funkce globalizace** v části **prostředí** vyberte dlaždici **elektronická fakturace**.</span><span class="sxs-lookup"><span data-stu-id="079be-240">In the **Globalization Features** workspace, under **Environments**, select the **e-Invoicing** tile.</span></span>

    ![Pracovní prostor Funkce globalizace](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. <span data-ttu-id="079be-242">Vyberte **Parametry úložiště klíčů** a poté výběrem možnost **Nový** vytvořte tajné úložiště klíčů Azure.</span><span class="sxs-lookup"><span data-stu-id="079be-242">Select **Key Vault parameters**, and then select **New** to create an Azure Key Vault secret.</span></span>
3. <span data-ttu-id="079be-243">Zadejte název a popis úložiště klíčů a poté do pole **URI úložiště klíčů** zadejte adresu URL, která identifikuje prostředek úložiště klíčů v Azure.</span><span class="sxs-lookup"><span data-stu-id="079be-243">Enter a name and description for the key vault, and then, in the **Key Vault URI** field, enter the URL that identifies the Key Vault resource in Azure.</span></span>
4. <span data-ttu-id="079be-244">Na pevné záložce **Certifikáty** vyberte **Přidat** pro přidání certifikátu a zadejte název a popis každého certifikátu.</span><span class="sxs-lookup"><span data-stu-id="079be-244">On the **Certificates** FastTab, select **Add** to add the certificate, and enter a name and description for each certificate.</span></span>

    ![Certifikát byl přidán](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. <span data-ttu-id="079be-246">Vyberte **Nový** pro vytvoření nového prostředí.</span><span class="sxs-lookup"><span data-stu-id="079be-246">Select **New** to create a new environment.</span></span>
6. <span data-ttu-id="079be-247">Zadejte název, popis a tajný token podpisu sdíleného přístupu požadovaný pro úložiště.</span><span class="sxs-lookup"><span data-stu-id="079be-247">Enter a name, a description, and the shared access signature token secret required for the storage.</span></span>
7. <span data-ttu-id="079be-248">Na pevné záložce **Uživatelé** vyberte **Nový** pro přidání uživatele, který bude mít oprávnění pro přístup do tohoto prostředí.</span><span class="sxs-lookup"><span data-stu-id="079be-248">On the **Users** FastTab, select **New** to add a user who will have permission to access this environment.</span></span>
8. <span data-ttu-id="079be-249">Zadejte ID a e-mailovou adresu uživatele.</span><span class="sxs-lookup"><span data-stu-id="079be-249">Enter the user's user ID and email address.</span></span>
9. <span data-ttu-id="079be-250">Chcete-li přidat další uživatele, zopakujte kroky 7 a 8.</span><span class="sxs-lookup"><span data-stu-id="079be-250">Repeat steps 7 and 8 to add more users.</span></span>
10. <span data-ttu-id="079be-251">Výběrem možnosti **Publikovat** publikujte prostředí.</span><span class="sxs-lookup"><span data-stu-id="079be-251">Select **Publish** to publish the environment.</span></span>

    ![Publikované prostředí](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)
