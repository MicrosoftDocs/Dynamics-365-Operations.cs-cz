---
title: Průvodce řešením potíží s integrací dat
description: Toto téma obsahuje informace o odstraňování potíží s integrací dat mezi Microsoft Dynamics 365 for Finance and Operations a Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797268"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="b1743-103">Průvodce řešením potíží s integrací dat</span><span class="sxs-lookup"><span data-stu-id="b1743-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a><span data-ttu-id="b1743-104">Povolení sledování modulu plug-in v Common Data Service a kontrola podrobností o chybě modulu plug-in dvojího zápisu</span><span class="sxs-lookup"><span data-stu-id="b1743-104">Enable Plugin Trace in Common Data Service and check the dual-write Plugin error details</span></span>

<span data-ttu-id="b1743-105">Pokud čelíte problému nebo chybě při synchronizaci s dvojím zápisem, můžete zkontrolovat chyby v protokolu sledování:</span><span class="sxs-lookup"><span data-stu-id="b1743-105">If you are facing an issue or error with dual-write synchronization, you can inspect the errors in the trace log:</span></span>

1. <span data-ttu-id="b1743-106">Před tím, než budete moci zkontrolovat chyby, je nutné povolit sledování modulů plug-in pomocí pokynů v části [Registrace modulu plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) pro povolení sledování modulů plug-in.</span><span class="sxs-lookup"><span data-stu-id="b1743-106">Before you can inspect the errors, you must enable Plugin trace using the instructions in [Register plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) to enable Plugin trace.</span></span> <span data-ttu-id="b1743-107">Nyní můžete zkontrolovat chyby.</span><span class="sxs-lookup"><span data-stu-id="b1743-107">Now you can inspect the errors.</span></span>
2. <span data-ttu-id="b1743-108">Přihaste se do Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="b1743-108">Login to Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="b1743-109">Klikněte na ikonu Nastavení (ozubené kolo) a vyberte možnost **Pokročilá nastavení**.</span><span class="sxs-lookup"><span data-stu-id="b1743-109">Click on the Settings icon (a gear), and select **Advanced Settings**.</span></span>
4. <span data-ttu-id="b1743-110">V nabídce **Nastavení** vyberte **Přizpůsobení > Protokol sledování modulu plug-in**.</span><span class="sxs-lookup"><span data-stu-id="b1743-110">In the **Settings** menu, choose **Customization > Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="b1743-111">Chcete-li zobrazit podrobnosti o chybě, klikněte na název typu **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span><span class="sxs-lookup"><span data-stu-id="b1743-111">Click the type name **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** to display the error details.</span></span>

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="b1743-112">Kontrola chyb synchronizace s dvojím zápisem v aplikaci Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b1743-112">Check dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="b1743-113">Chyby můžete zkontrolovat při testování pomocí následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="b1743-113">You can check the errors during testing by following these steps:</span></span>

+ <span data-ttu-id="b1743-114">Přihlaste se do LifeCycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="b1743-114">Login to LifeCycle Services (LCS).</span></span>
+ <span data-ttu-id="b1743-115">Otevřete projekt LCS, který jste zvolili pro testování dvojího zápisu.</span><span class="sxs-lookup"><span data-stu-id="b1743-115">Open the LCS project that you chose to perform dual-write testing.</span></span>
+ <span data-ttu-id="b1743-116">Přejděte do prostředí hostovaných na cloudu.</span><span class="sxs-lookup"><span data-stu-id="b1743-116">Go to Cloud Hosted Environments.</span></span>
+ <span data-ttu-id="b1743-117">Vzdálená plocha pro Finance and Operations VM pomocí místního účtu, který je zobrazen v LCS.</span><span class="sxs-lookup"><span data-stu-id="b1743-117">Remote desktop to Finance and Operations VM using local account that is displayed in LCS.</span></span>
+ <span data-ttu-id="b1743-118">Otevřít prohlížeč událostí.</span><span class="sxs-lookup"><span data-stu-id="b1743-118">Open the event viewer.</span></span> 
+ <span data-ttu-id="b1743-119">Přejděte na **Protokoly aplikací a služeb > Microsoft > Dynamics > AX-DualWriteSync > Provozní**.</span><span class="sxs-lookup"><span data-stu-id="b1743-119">Navigate to **Applications and Services logs > Microsoft > Dynamics > AX-DualWriteSync > Operational**.</span></span> <span data-ttu-id="b1743-120">Zobrazí se chybové zprávy a podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="b1743-120">The errors and details are displayed.</span></span>

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a><span data-ttu-id="b1743-121">Jak odpojit a propojit jiné prostředí Common Data Service z Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b1743-121">How to unlink and link another Common Data Service environment from Finance and Operations</span></span>

<span data-ttu-id="b1743-122">Propojení můžete aktualizovat pomocí následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="b1743-122">You can update links by following these steps:</span></span>

+ <span data-ttu-id="b1743-123">Přejděte do prostředí Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b1743-123">Navigate to the Finance and Operations environment.</span></span>
+ <span data-ttu-id="b1743-124">Otevřete správu dat.</span><span class="sxs-lookup"><span data-stu-id="b1743-124">Open Data Management.</span></span>
+ <span data-ttu-id="b1743-125">Klikněte na **Odkaz na CDS for apps**.</span><span class="sxs-lookup"><span data-stu-id="b1743-125">Click on **Link to CDS for apps**.</span></span>
+ <span data-ttu-id="b1743-126">Vyberte všechna spuštěná mapování a klikněte na **Zastavit**.</span><span class="sxs-lookup"><span data-stu-id="b1743-126">Select all the running mappings and click **Stop**.</span></span> 
+ <span data-ttu-id="b1743-127">Vyberte všechna mapování a klikněte na **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="b1743-127">Select all the mappings and click **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b1743-128">Volba **Odstranit** se neobjeví, pokud je vybrána šablona **CustomerV3-Account**.</span><span class="sxs-lookup"><span data-stu-id="b1743-128">The **Delete** option will not appear if **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="b1743-129">V případě potřeby výběr zrušte.</span><span class="sxs-lookup"><span data-stu-id="b1743-129">Unselect it if needed.</span></span> <span data-ttu-id="b1743-130">**CustomerV3-Account** je starší zřízená šablona a spolupracuje s řešením Zpeněžení potenciálního zákazníka.</span><span class="sxs-lookup"><span data-stu-id="b1743-130">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="b1743-131">Protože je globálně vydaná, zobrazí se pod všemi šablonami.</span><span class="sxs-lookup"><span data-stu-id="b1743-131">Because it is globally released, it shows up under all templates.</span></span>

+ <span data-ttu-id="b1743-132">Klikněte na **Odpojit prostředí**.</span><span class="sxs-lookup"><span data-stu-id="b1743-132">Click **Unlink environment**.</span></span>
+ <span data-ttu-id="b1743-133">Potvrďte kliknutím na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="b1743-133">Click **Yes** for confirmation.</span></span>
+ <span data-ttu-id="b1743-134">Chcete-li nové prostředí propojit, postupujte podle pokynů v [instalační příručce](https://aka.ms/dualwrite-docs).</span><span class="sxs-lookup"><span data-stu-id="b1743-134">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>

