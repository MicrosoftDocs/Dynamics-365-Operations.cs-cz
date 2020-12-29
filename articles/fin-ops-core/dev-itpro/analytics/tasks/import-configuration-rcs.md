---
title: (Elektronické výkaznictví) Import konfigurací z RSC
description: Toto téma obsahuje informace o tom, jak může uživatel importovat novou verzi konfigurace elektronického výkaznictví z RCS.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b591df3d384e8dc59646ebb9d0205001db040a55
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684180"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="e2b10-103">(Elektronické výkaznictví) Import konfigurací z RSC</span><span class="sxs-lookup"><span data-stu-id="e2b10-103">(ER) Import configurations from RCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e2b10-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může importovat novou verzi konfigurace formátu pro elektronické výkaznictví ze služby Microsoft Regulatory Configuration Services (RCS).</span><span class="sxs-lookup"><span data-stu-id="e2b10-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="e2b10-105">V tomto příkladu vyberete verzi konfigurace elektronického výkaznictví, která byla nakonfigurována v instanci RCS, a importujte ji do aktuální instance pro vzorovou společnost, Litware, Inc. Tyto kroky lze provádět ve všech společnostech, protože konfigurace Felektronického výkaznictví je sdílena mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="e2b10-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="e2b10-106">K provedení těchto kroků musíte v RCS nejprve dokončit jednotlivé kroky v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e2b10-106">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="e2b10-107">Chcete-li dokončit tento postup, musíte mít také přístup k instanci RCS, která obsahuje alespoň jednu konfiguraci elektronického výkaznictví ve stavu **dokončeno** nebo **sdíleno**.</span><span class="sxs-lookup"><span data-stu-id="e2b10-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="e2b10-108">Přejděte na **Správa organizace** > **Pracovní prostory** > **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="e2b10-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="e2b10-109">Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="e2b10-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="e2b10-110">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e2b10-110">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="e2b10-111">Nemáte-li pro vaši společnost zřízeno žádné RCS prostředí, vyberte externí odkaz **Regulatory Services – Konfigurace** a postupujte podle pokynů pro zřízení RCS prostředí.</span><span class="sxs-lookup"><span data-stu-id="e2b10-111">If you have no RCS environment provisioned to your company, select **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="e2b10-112">Vyberte **Parametry elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="e2b10-112">Select **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="e2b10-113">Vyberte kartu **RCS**.</span><span class="sxs-lookup"><span data-stu-id="e2b10-113">Select the **RCS** tab.</span></span> 
6. <span data-ttu-id="e2b10-114">Pokud jste již RCS prostředí pro vaši společnost zřídili, použijte pro přístup k ní uvedené adresy URL na stránce.</span><span class="sxs-lookup"><span data-stu-id="e2b10-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="e2b10-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e2b10-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="e2b10-116">Registrace nového úložiště elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="e2b10-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="e2b10-117">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="e2b10-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="e2b10-118">Vyberte poskytovatele Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="e2b10-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="e2b10-119">Vyberte Úložiště.</span><span class="sxs-lookup"><span data-stu-id="e2b10-119">Select Repositories.</span></span> 
4. <span data-ttu-id="e2b10-120">Kliknutím na Přidat otevřete dialogové okno pro přetažení.</span><span class="sxs-lookup"><span data-stu-id="e2b10-120">Select Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="e2b10-121">V poli Typ úložiště konfigurace zadejte RCS.</span><span class="sxs-lookup"><span data-stu-id="e2b10-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="e2b10-122">Zvolte Vytvořit úložiště.</span><span class="sxs-lookup"><span data-stu-id="e2b10-122">Select Create repository.</span></span> 
7. <span data-ttu-id="e2b10-123">V poli zobrazovaného názvu prostředí RCS zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e2b10-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="e2b10-124">Vyberte příslušnou instanci RCS.</span><span class="sxs-lookup"><span data-stu-id="e2b10-124">Select the desired RCS instance.</span></span> <span data-ttu-id="e2b10-125">Můžete jich mít několik.</span><span class="sxs-lookup"><span data-stu-id="e2b10-125">You can have several of them.</span></span> 
9. <span data-ttu-id="e2b10-126">Vyberte OK.</span><span class="sxs-lookup"><span data-stu-id="e2b10-126">Select OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="e2b10-127">Import konfigurací elektronického z úložiště založeného na RCS</span><span class="sxs-lookup"><span data-stu-id="e2b10-127">Import ER configurations from RCS-based repository</span></span>
1. <span data-ttu-id="e2b10-128">Vyberte **Zobrazit filtry**.</span><span class="sxs-lookup"><span data-stu-id="e2b10-128">Select **Show filters**.</span></span> 
2. <span data-ttu-id="e2b10-129">Zadejte hodnotu filtru „RCS“ v poli **Název** za použití operátoru filtru **začíná na**.</span><span class="sxs-lookup"><span data-stu-id="e2b10-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="e2b10-130">Po otevření vybraného úložiště na stránce **Připojit k Regulatory Configuration Services** vyberte odkaz **Zde vyberte pro připojení k Regulatory Configuration Services**.</span><span class="sxs-lookup"><span data-stu-id="e2b10-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, select **Select here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="e2b10-131">Zvolte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="e2b10-131">Select **Open**.</span></span> 
5. <span data-ttu-id="e2b10-132">Vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="e2b10-132">Select **Close**.</span></span> 
6. <span data-ttu-id="e2b10-133">Vyberte požadovanou verzi konfigurace elektronického výkaznictví a výběrem možnosti **Import** ji převeďte do aktuální instance.</span><span class="sxs-lookup"><span data-stu-id="e2b10-133">Select the desired version of ER configuration and select **Import** to bring it in the current instance.</span></span>

