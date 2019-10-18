---
title: Průvodce řešením potíží s integrací dat
description: Toto téma obsahuje informace o odstraňování potíží pro integrací dat mezi Finance and Operations apps a Common Data Service.
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
ms.openlocfilehash: c16268338085d414468f17362294fb7e933d1b57
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249102"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="e40ae-103">Průvodce řešením potíží s integrací dat</span><span class="sxs-lookup"><span data-stu-id="e40ae-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="e40ae-104">Povolení protokolů sledování modulu plug-in v Common Data Service a kontrola podrobností o chybě modulu plug-in dvojího zápisu</span><span class="sxs-lookup"><span data-stu-id="e40ae-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="e40ae-105">Pokud při synchronizaci dvojího zápisu dojde k problému nebo chybě, postupujte podle následujících kroků ohledně kontroly chyb v protokolu sledování.</span><span class="sxs-lookup"><span data-stu-id="e40ae-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="e40ae-106">Před kontrolou chyb je nutné povolit protokoly sledování modulů plug-in.</span><span class="sxs-lookup"><span data-stu-id="e40ae-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="e40ae-107">Pokyny naleznete v části Zobrazení protokolů sledování [Kurzu: Zápis a registrace modulu plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span><span class="sxs-lookup"><span data-stu-id="e40ae-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="e40ae-108">Nyní můžete zkontrolovat chyby.</span><span class="sxs-lookup"><span data-stu-id="e40ae-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="e40ae-109">Přihlaste se do aplikace Microsoft Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="e40ae-109">Sign in to Microsoft Dynamics 365 Sales.</span></span>
3. <span data-ttu-id="e40ae-110">Vyberte tlačítko **Nastavení** (symbol ozubeného kola) a poté vyberte položku **Pokročilá nastavení**.</span><span class="sxs-lookup"><span data-stu-id="e40ae-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="e40ae-111">V nabídce **Nastavení** vyberte **Přizpůsobení \> Protokol sledování modulu plug-in**.</span><span class="sxs-lookup"><span data-stu-id="e40ae-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="e40ae-112">Chcete-li zobrazit podrobnosti o chybě, zvolte jako název typu **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span><span class="sxs-lookup"><span data-stu-id="e40ae-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors"></a><span data-ttu-id="e40ae-113">Zkontrujte chyby synchronizace dvojího zápisu</span><span class="sxs-lookup"><span data-stu-id="e40ae-113">Inspect dual-write synchronization errors</span></span>

<span data-ttu-id="e40ae-114">Chcete-li kontrolovat chyby během testování, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="e40ae-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="e40ae-115">Přihlaste se do Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="e40ae-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="e40ae-116">Otevřete projekt LCS, pro který chcete provést testování dvojího zápisu.</span><span class="sxs-lookup"><span data-stu-id="e40ae-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="e40ae-117">Zvolte **Prostředí hostovaná v cloudu**.</span><span class="sxs-lookup"><span data-stu-id="e40ae-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="e40ae-118">Vytvořte připojení ke vzdálené ploše k virtuálnímu počítači aplikace pomocí místního účtu zobrazeného na LCS.</span><span class="sxs-lookup"><span data-stu-id="e40ae-118">Make a Remote desktop connection to the application virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="e40ae-119">Otevřete prohlížeč událostí.</span><span class="sxs-lookup"><span data-stu-id="e40ae-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="e40ae-120">Přejděte na **Protokoly aplikací a služeb \> Microsoft \> Dynamics \> AX -DualWriteSync \> Provozní**.</span><span class="sxs-lookup"><span data-stu-id="e40ae-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="e40ae-121">Zobrazí se chybové zprávy a podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="e40ae-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a><span data-ttu-id="e40ae-122">Odpojte jedno prostředí Common Data Service z aplikace a připojte jiné prostředí</span><span class="sxs-lookup"><span data-stu-id="e40ae-122">Unlink one Common Data Service environment from the application and link another environment</span></span>

<span data-ttu-id="e40ae-123">Pro aktualizaci spojení postupujte podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="e40ae-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="e40ae-124">Přejděte do prostředí aplikace</span><span class="sxs-lookup"><span data-stu-id="e40ae-124">Go to the application environment.</span></span>
2. <span data-ttu-id="e40ae-125">Otevřete správu dat.</span><span class="sxs-lookup"><span data-stu-id="e40ae-125">Open Data Management.</span></span>
3. <span data-ttu-id="e40ae-126">Zvolte **Odkaz na CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="e40ae-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="e40ae-127">Vyberte všechna mapování, která jsou spuštěna, a poté vyberte **Zastavit**.</span><span class="sxs-lookup"><span data-stu-id="e40ae-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="e40ae-128">Vyberte všechna mapování a poté vyberte možnost **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="e40ae-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e40ae-129">Volba **Odstranit** není k dispozici, pokud je vybrána šablona **CustomerV3-Account**.</span><span class="sxs-lookup"><span data-stu-id="e40ae-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="e40ae-130">Zrušte výběr této šablony podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="e40ae-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="e40ae-131">**CustomerV3-Account** je starší zřízená šablona a spolupracuje s řešením Zpeněžení potenciálního zákazníka.</span><span class="sxs-lookup"><span data-stu-id="e40ae-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="e40ae-132">Protože je globálně vydaná, zobrazí se pod všemi šablonami.</span><span class="sxs-lookup"><span data-stu-id="e40ae-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="e40ae-133">Zvolte **Odpojit prostředí**.</span><span class="sxs-lookup"><span data-stu-id="e40ae-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="e40ae-134">Vyberte **Ano**, chcete-li potvrdit operaci.</span><span class="sxs-lookup"><span data-stu-id="e40ae-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="e40ae-135">Chcete-li nové prostředí propojit, postupujte podle pokynů v [instalační příručce](https://aka.ms/dualwrite-docs).</span><span class="sxs-lookup"><span data-stu-id="e40ae-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
