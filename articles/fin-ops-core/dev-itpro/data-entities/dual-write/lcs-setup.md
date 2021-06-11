---
title: Nastavení duálního zápisu z Lifecycle Services
description: Toto téma vysvětluje, jak nastavit připojení pro duální zápis z Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103562"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="ff4fd-103">Nastavení duálního zápisu z Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="ff4fd-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ff4fd-104">Toto téma vysvětluje, jak povolit duální zápis z Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ff4fd-104">This topic explains how to enable dual-write from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ff4fd-105">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="ff4fd-105">Prerequisites</span></span>

<span data-ttu-id="ff4fd-106">Musíte vyplnit integraci Power Platform, jak je popsáno v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="ff4fd-106">You must complete the Power Platform integration as described in the following topics:</span></span>

+ [<span data-ttu-id="ff4fd-107">Integrace Power Platform - povolit během nasazení prostředí</span><span class="sxs-lookup"><span data-stu-id="ff4fd-107">Power Platform Integration - Enable during environment deployment</span></span>](../../power-platform/overview.md#enable-during-environment-deployment)
+ [<span data-ttu-id="ff4fd-108">Integrace Power Platform - nastavit po nasazení prostředí</span><span class="sxs-lookup"><span data-stu-id="ff4fd-108">Power Platform integration - Set up after environment deployment</span></span>](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a><span data-ttu-id="ff4fd-109">Nastavení duálního zápisu pro nová prostředí Dataverse</span><span class="sxs-lookup"><span data-stu-id="ff4fd-109">Set up dual-write for new Dataverse environments</span></span>

<span data-ttu-id="ff4fd-110">Podle těchto pokynů nastavíte duální zápis ze stránky LCS **Podrobnosti o prostředí**:</span><span class="sxs-lookup"><span data-stu-id="ff4fd-110">Follow these steps to set up dual-write from LCS **Environment Details** page:</span></span>

1. <span data-ttu-id="ff4fd-111">Na stránce **Podrobnosti o prostředí** rozbalte sekci **Integrace Power Platform**.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-111">On the **Environment Details** page, expand the **Power Platform Integration** section.</span></span>

2. <span data-ttu-id="ff4fd-112">Vyberte tlačítko **Aplikace pro dvojí zápis**.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-112">Select the **Dual-write application** button.</span></span>

    ![Integrace Power Platform](media/powerplat_integration_step2.png)

3. <span data-ttu-id="ff4fd-114">Zkontrolujte smluvní podmínky a poté vyberte **Konfigurovat**.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-114">Review the terms and conditions, and then select **Configure**.</span></span>

4. <span data-ttu-id="ff4fd-115">Pokračujte volbou tlačítka **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-115">Select **OK** to continue.</span></span>

5. <span data-ttu-id="ff4fd-116">Pokrok můžete sledovat pravidelným obnovováním stránky s podrobnostmi o prostředí.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-116">You can monitor the progress by periodically refreshing the environment details page.</span></span> <span data-ttu-id="ff4fd-117">Nastavení obvykle trvá 30 minut nebo méně.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-117">Setup typically takes 30 minutes or less.</span></span>  

6. <span data-ttu-id="ff4fd-118">Po dokončení nastavení vás bude informovat zpráva, zda byl proces úspěšný nebo zda došlo k selhání.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-118">When the setup is complete, a message will inform you if the process was successful or if there was a failure.</span></span> <span data-ttu-id="ff4fd-119">Pokud se nastavení nezdařilo, zobrazí se související chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-119">If the setup failed, then a related error message is displayed.</span></span> <span data-ttu-id="ff4fd-120">Před přechodem k dalšímu kroku musíte opravit všechny chyby.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-120">You must fix any errors before moving to the next step.</span></span>

7. <span data-ttu-id="ff4fd-121">Vyberte **Odkaz na prostředí Power Platform**, chcete-li vytvořit spojení mezi Dataverse a databázemi aktuálního prostředí.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-121">Select **Link to Power Platform environment** to create a link between Dataverse and the current environment's databases.</span></span> <span data-ttu-id="ff4fd-122">To obvykle trvá méně než 5 minut.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-122">This typically takes less than 5 minutes.</span></span>

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Odkaz na prostředí Power Platform":::

8. <span data-ttu-id="ff4fd-124">Po dokončení propojení se zobrazí hypertextový odkaz.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-124">When the linking is complete, a hyperlink is displayed.</span></span> <span data-ttu-id="ff4fd-125">Pomocí odkazu se přihlaste do oblasti správy duálního zápisu v prostředí Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-125">Use the link to sign in to the dual-write administration area in the Finance and Operations environment.</span></span> <span data-ttu-id="ff4fd-126">Odtud můžete nastavit mapování entit.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-126">From there, you can set up entity mappings.</span></span>

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a><span data-ttu-id="ff4fd-127">Nastavení duálního zápisu pro existující prostředí Dataverse</span><span class="sxs-lookup"><span data-stu-id="ff4fd-127">Set up dual-write for an existing Dataverse environment</span></span>

<span data-ttu-id="ff4fd-128">Chcete-li nastavit duální zápis pro existující prostředí Dataverse, musíte vytvořit [lístek podpory](../../lifecycle-services/lcs-support.md) společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-128">To set up dual-write for an existing Dataverse environment, you must create a Microsoft [support ticket](../../lifecycle-services/lcs-support.md).</span></span> <span data-ttu-id="ff4fd-129">Lístek musí obsahovat:</span><span class="sxs-lookup"><span data-stu-id="ff4fd-129">The ticket must include:</span></span>

+ <span data-ttu-id="ff4fd-130">ID vašeho prostředí Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-130">Your Finance and Operations environment ID.</span></span>
+ <span data-ttu-id="ff4fd-131">Název vašeho prostředí ze služby Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-131">Your environment name from Lifecycle Services.</span></span>
+ <span data-ttu-id="ff4fd-132">ID organizace Dataverse nebo ID prostředí Power Platform z Centra pro správu Power Platform.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-132">The Dataverse organization ID or Power Platform Environment ID from Power Platform Admin Center.</span></span> <span data-ttu-id="ff4fd-133">Ve svém lístku požádejte, aby ID bylo použito jako instance integrace Power Platform.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-133">In your ticket, request that the ID be the instance used for Power Platform integration.</span></span>

> [!NOTE]
> <span data-ttu-id="ff4fd-134">Nelze zrušit propojení prostředí pomocí LCS.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-134">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="ff4fd-135">Chcete-li zrušit propojení prostředí, otevřete pracovní prostor **Integrace dat** v prostředí Finance and Operations a poté vyberte možnost **Zrušit propojení**.</span><span class="sxs-lookup"><span data-stu-id="ff4fd-135">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
