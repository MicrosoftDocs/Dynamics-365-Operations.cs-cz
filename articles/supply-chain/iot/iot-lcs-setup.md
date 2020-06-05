---
title: Instalace doplňku IoT Intelligence v LCS
description: Toto téma vysvětluje, jak nainstalovat doplněk IoT Intelligence ve službě Microsoft Dynamics Lifecycle Services (LCS).
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 04333b3659f090b15cc0d0ee216f14dabc588883
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386493"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="37308-103">Instalace doplňku IoT Intelligence v LCS</span><span class="sxs-lookup"><span data-stu-id="37308-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="37308-104">Toto téma vysvětluje, jak nainstalovat doplněk IoT Intelligence ve službě Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="37308-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="37308-105">Před instalací doplňku musíte [vytvořit zdroje Azure](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="37308-105">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="37308-106">Nastavení prostředí LCS</span><span class="sxs-lookup"><span data-stu-id="37308-106">Set up the LCS environment</span></span>

1. <span data-ttu-id="37308-107">Otevřete LCS a přejděte do prostředí Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="37308-107">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="37308-108">Přejděte do části **Doplňky prostředí**.</span><span class="sxs-lookup"><span data-stu-id="37308-108">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="37308-109">Vyberte **Nainstalovat nový doplněk** a zobrazte seznam doplňků, které byly pro dané prostředí povoleny.</span><span class="sxs-lookup"><span data-stu-id="37308-109">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="37308-110">V dialogovém okně **Vybrat doplněk pro instalaci** vyberte **IoT Intelligence**.</span><span class="sxs-lookup"><span data-stu-id="37308-110">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="37308-111">V dialogovém okně **Nastavení doplňku** zadejte podrobnosti vašeho centra IoT a Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="37308-111">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="37308-112">Požadované hodnoty najdete v úložišti klíčů, které jste vytvořili v části [Vytvoření zdrojů Azure](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="37308-112">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="37308-113">**ID klienta** - Na portálu Azure přejděte do úložiště klíčů a poté v levém navigačním podokně vyberte možnost **Přehled** a zkopírujte hodnotu **ID adresáře**.</span><span class="sxs-lookup"><span data-stu-id="37308-113">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="37308-114">Vložte tuto hodnotu do dialogového okna **Nastavení doplňku**.</span><span class="sxs-lookup"><span data-stu-id="37308-114">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="37308-115">**URI Key Vault koncového bodu kompatibilní s centrem událostí IoT** - Přejděte do úložiště klíčů a poté v levém navigačním podokně vyberte možnost **Přehled** a zkopírujte hodnotu **Název DNS**.</span><span class="sxs-lookup"><span data-stu-id="37308-115">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="37308-116">Vložte tuto hodnotu do dialogového okna **Nastavení doplňku**.</span><span class="sxs-lookup"><span data-stu-id="37308-116">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="37308-117">**Název tajného klíče koncového bodu kompatibilní s centrem událostí IoT** - Přejděte do úložiště klíčů a poté v levém navigačním podokně vyberte možnost **Tajné klíče** a zkopírujte název tajného klíče tam, kde je uložen řetězec připojení k centru událostí pro centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="37308-117">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="37308-118">Vložte tuto hodnotu do dialogového okna **Nastavení doplňku**.</span><span class="sxs-lookup"><span data-stu-id="37308-118">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="37308-119">**URI úložiště klíčů Redis Cache** - Přejděte do úložiště klíčů a poté v levém navigačním podokně vyberte možnost **Přehled** a zkopírujte hodnotu **Název DNS**.</span><span class="sxs-lookup"><span data-stu-id="37308-119">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="37308-120">Vložte tuto hodnotu do dialogového okna **Nastavení doplňku**.</span><span class="sxs-lookup"><span data-stu-id="37308-120">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="37308-121">**Název tajného klíče koncového bodu Redis Cache** - Přejděte do úložiště klíčů a poté v levém navigačním podokně vyberte možnost **Tajné klíče** a zkopírujte název tajného klíče tam, kde je uložen řetězec připojení pro Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="37308-121">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="37308-122">Vložte tuto hodnotu do dialogového okna **Nastavení doplňku**.</span><span class="sxs-lookup"><span data-stu-id="37308-122">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="37308-123">Zaškrtnutím políčka přijměte smluvní podmínky.</span><span class="sxs-lookup"><span data-stu-id="37308-123">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="37308-124">Vyberte **Instalovat**.</span><span class="sxs-lookup"><span data-stu-id="37308-124">Select **Install**.</span></span>
8. <span data-ttu-id="37308-125">Zobrazí se okno se zprávou, že „Doplněk byl úspěšně spuštěn pro instalaci.“</span><span class="sxs-lookup"><span data-stu-id="37308-125">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="37308-126">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="37308-126">Select **OK**.</span></span>

<span data-ttu-id="37308-127">Nastavení LCS je nyní dokončeno.</span><span class="sxs-lookup"><span data-stu-id="37308-127">LCS setup is now completed.</span></span> <span data-ttu-id="37308-128">Dalším krokem je [nastavení scénáře](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="37308-128">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="37308-129">Odinstalace doplňku</span><span class="sxs-lookup"><span data-stu-id="37308-129">Uninstall the add-in</span></span>

1. <span data-ttu-id="37308-130">V aplikaci Supply Chain Management [zakažte scénáře](iot-scenario-setup.md#how-to-disable-a-scenario).</span><span class="sxs-lookup"><span data-stu-id="37308-130">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#how-to-disable-a-scenario).</span></span>
2. <span data-ttu-id="37308-131">V LCS přejděte k podrobnostem prostředí Supply Chain Management .</span><span class="sxs-lookup"><span data-stu-id="37308-131">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="37308-132">Přejděte do části **Doplňky prostředí**.</span><span class="sxs-lookup"><span data-stu-id="37308-132">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="37308-133">Vyberte **Odinstalovat** pro doplněk IoT Intelligence.</span><span class="sxs-lookup"><span data-stu-id="37308-133">Select **Uninstall** for the IoT Intelligence add-in.</span></span>