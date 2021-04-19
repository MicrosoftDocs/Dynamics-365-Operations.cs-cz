---
title: Instalace doplňku IoT Intelligence v LCS
description: Toto téma vysvětluje, jak nainstalovat doplněk IoT Intelligence ve službě Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2d1cc9a7535be05a3e466c27e53047d694cf0160
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826436"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="99371-103">Instalace doplňku IoT Intelligence v LCS</span><span class="sxs-lookup"><span data-stu-id="99371-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99371-104">Toto téma vysvětluje, jak nainstalovat doplněk IoT Intelligence ve službě Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="99371-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="99371-105">Upozorňujeme, že doplňky nelze nainstalovat v demo / zkušebním prostředí.</span><span class="sxs-lookup"><span data-stu-id="99371-105">Note that add-ins cannot be installed on a demo/trial environment.</span></span> <span data-ttu-id="99371-106">Před instalací doplňku musíte [vytvořit zdroje Azure](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="99371-106">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="99371-107">Nastavení prostředí LCS</span><span class="sxs-lookup"><span data-stu-id="99371-107">Set up the LCS environment</span></span>

1. <span data-ttu-id="99371-108">Otevřete LCS a přejděte do prostředí Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="99371-108">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="99371-109">Přejděte do části **Doplňky prostředí**.</span><span class="sxs-lookup"><span data-stu-id="99371-109">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="99371-110">Vyberte **Nainstalovat nový doplněk** a zobrazte seznam doplňků, které byly pro dané prostředí povoleny.</span><span class="sxs-lookup"><span data-stu-id="99371-110">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="99371-111">V dialogovém okně **Vybrat doplněk pro instalaci** vyberte **IoT Intelligence**.</span><span class="sxs-lookup"><span data-stu-id="99371-111">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="99371-112">V dialogovém okně **Nastavení doplňku** zadejte podrobnosti vašeho centra IoT a Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="99371-112">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="99371-113">Požadované hodnoty najdete v úložišti klíčů, které jste vytvořili v části [Vytvoření zdrojů Azure](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="99371-113">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="99371-114">**ID klienta** - Na portálu Azure přejděte do úložiště klíčů a poté v levém navigačním podokně vyberte možnost **Přehled** a zkopírujte hodnotu **ID adresáře**.</span><span class="sxs-lookup"><span data-stu-id="99371-114">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="99371-115">Vložte tuto hodnotu do dialogového okna **Nastavení doplňku**.</span><span class="sxs-lookup"><span data-stu-id="99371-115">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="99371-116">**URI Key Vault koncového bodu kompatibilní s centrem událostí IoT** - Přejděte do úložiště klíčů a poté v levém navigačním podokně vyberte možnost **Přehled** a zkopírujte hodnotu **Název DNS**.</span><span class="sxs-lookup"><span data-stu-id="99371-116">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="99371-117">Vložte tuto hodnotu do dialogového okna **Nastavení doplňku**.</span><span class="sxs-lookup"><span data-stu-id="99371-117">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="99371-118">**Název tajného klíče koncového bodu kompatibilní s centrem událostí IoT** - Přejděte do úložiště klíčů a poté v levém navigačním podokně vyberte možnost **Tajné klíče** a zkopírujte název tajného klíče tam, kde je uložen řetězec připojení k centru událostí pro centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="99371-118">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="99371-119">Vložte tuto hodnotu do dialogového okna **Nastavení doplňku**.</span><span class="sxs-lookup"><span data-stu-id="99371-119">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="99371-120">**URI úložiště klíčů Redis Cache** - Přejděte do úložiště klíčů a poté v levém navigačním podokně vyberte možnost **Přehled** a zkopírujte hodnotu **Název DNS**.</span><span class="sxs-lookup"><span data-stu-id="99371-120">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="99371-121">Vložte tuto hodnotu do dialogového okna **Nastavení doplňku**.</span><span class="sxs-lookup"><span data-stu-id="99371-121">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="99371-122">**Název tajného klíče koncového bodu Redis Cache** - Přejděte do úložiště klíčů a poté v levém navigačním podokně vyberte možnost **Tajné klíče** a zkopírujte název tajného klíče tam, kde je uložen řetězec připojení pro Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="99371-122">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="99371-123">Vložte tuto hodnotu do dialogového okna **Nastavení doplňku**.</span><span class="sxs-lookup"><span data-stu-id="99371-123">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="99371-124">Zaškrtnutím políčka přijměte smluvní podmínky.</span><span class="sxs-lookup"><span data-stu-id="99371-124">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="99371-125">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="99371-125">Select **Install**.</span></span>
8. <span data-ttu-id="99371-126">Zobrazí se okno se zprávou, že „Doplněk byl úspěšně spuštěn pro instalaci.“</span><span class="sxs-lookup"><span data-stu-id="99371-126">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="99371-127">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="99371-127">Select **OK**.</span></span>

<span data-ttu-id="99371-128">Nastavení LCS je nyní dokončeno.</span><span class="sxs-lookup"><span data-stu-id="99371-128">LCS setup is now completed.</span></span> <span data-ttu-id="99371-129">Dalším krokem je [nastavení scénáře](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="99371-129">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="99371-130">Odinstalace doplňku</span><span class="sxs-lookup"><span data-stu-id="99371-130">Uninstall the add-in</span></span>

1. <span data-ttu-id="99371-131">V aplikaci Supply Chain Management [zakažte scénáře](iot-scenario-setup.md#disable-a-scenario).</span><span class="sxs-lookup"><span data-stu-id="99371-131">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#disable-a-scenario).</span></span>
2. <span data-ttu-id="99371-132">V LCS přejděte k podrobnostem prostředí Supply Chain Management .</span><span class="sxs-lookup"><span data-stu-id="99371-132">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="99371-133">Přejděte do části **Doplňky prostředí**.</span><span class="sxs-lookup"><span data-stu-id="99371-133">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="99371-134">Vyberte **Odinstalovat** pro doplněk IoT Intelligence.</span><span class="sxs-lookup"><span data-stu-id="99371-134">Select **Uninstall** for the IoT Intelligence add-in.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]