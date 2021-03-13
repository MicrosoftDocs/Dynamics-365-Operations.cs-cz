---
title: Nastavení duálního zápisu z Lifecycle Services
description: Toto téma vysvětluje, jak nastavit připojení pro duální zápis z Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: df67e498b963af3ded7464f46f37bb4b2ca7d852
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127586"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="0afd6-103">Nastavení duálního zápisu z Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="0afd6-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0afd6-104">V tomto tématu je vysvětleno, jak zřídit připojení s dvojím zápisem mezi novým prostředím Finance and Operations a novým prostředím Dataverse z Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="0afd6-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Dataverse environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0afd6-105">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="0afd6-105">Prerequisites</span></span>

<span data-ttu-id="0afd6-106">Připojení s dvojím zápisem může nastavit pouze správce.</span><span class="sxs-lookup"><span data-stu-id="0afd6-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="0afd6-107">Musíte mít přístup k tomuto klientovi.</span><span class="sxs-lookup"><span data-stu-id="0afd6-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="0afd6-108">Musíte být správce v prostředích Finance and Operations i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="0afd6-108">You must be an admin in both Finance and Operations environments and Dataverse environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="0afd6-109">Nastavení připojení s dvojím zápisem</span><span class="sxs-lookup"><span data-stu-id="0afd6-109">Set up a dual-write connection</span></span>

<span data-ttu-id="0afd6-110">Chcete-li nastavit připojení s dvojím zápisem, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="0afd6-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="0afd6-111">V LCS přejděte na svůj projekt.</span><span class="sxs-lookup"><span data-stu-id="0afd6-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="0afd6-112">Pro nasazení nového prostředí vyberte **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="0afd6-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="0afd6-113">Vyberte verzi.</span><span class="sxs-lookup"><span data-stu-id="0afd6-113">Select the version.</span></span> 
4. <span data-ttu-id="0afd6-114">Vyberte topologii.</span><span class="sxs-lookup"><span data-stu-id="0afd6-114">Select the topology.</span></span> <span data-ttu-id="0afd6-115">Je-li k dispozici pouze jedna topologie, bude automaticky vybrána.</span><span class="sxs-lookup"><span data-stu-id="0afd6-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="0afd6-116">Proveďte první kroky v průvodci **Nastavení nasazení**.</span><span class="sxs-lookup"><span data-stu-id="0afd6-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="0afd6-117">Na kartě **Dataverse** proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="0afd6-117">On the **Dataverse** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="0afd6-118">Pokud je prostředí Dataverse již pro klienta zřízeno, můžete je vybrat.</span><span class="sxs-lookup"><span data-stu-id="0afd6-118">If a Dataverse environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="0afd6-119">Nastavte možnost **Konfigurovat Dataverse** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="0afd6-119">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="0afd6-120">Ve sloupci **Dostupná prostředí** vyberte prostředí, které chcete integrovat s vašimi daty Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0afd6-120">In the **Available environments** column, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="0afd6-121">Seznam obsahuje všechna prostředí, v nichž máte oprávnění správce.</span><span class="sxs-lookup"><span data-stu-id="0afd6-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="0afd6-122">Zaškrtnutím políčka **Souhlasím** dáte najevo, že souhlasíte s podmínkami a ujednáními.</span><span class="sxs-lookup"><span data-stu-id="0afd6-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Karta Dataverse, když už je pro klienta zřízeno prostředí Dataverse](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="0afd6-124">Pokud váš klient ještě nemá prostředí Dataverse, bude zřízeno nové prostředí.</span><span class="sxs-lookup"><span data-stu-id="0afd6-124">If your tenant doesn't already have a Dataverse environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="0afd6-125">Nastavte možnost **Konfigurovat Dataverse** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="0afd6-125">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="0afd6-126">Zadejte název prostředí Dataverse.</span><span class="sxs-lookup"><span data-stu-id="0afd6-126">Enter a name for the Dataverse environment.</span></span>
        3. <span data-ttu-id="0afd6-127">Vyberte oblast, ve které má být prostředí nasazeno.</span><span class="sxs-lookup"><span data-stu-id="0afd6-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="0afd6-128">Vyberte výchozí jazyk a měnu pro prostředí.</span><span class="sxs-lookup"><span data-stu-id="0afd6-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="0afd6-129">Jazyk a měnu nelze později změnit.</span><span class="sxs-lookup"><span data-stu-id="0afd6-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="0afd6-130">Zaškrtnutím políčka **Souhlasím** dáte najevo, že souhlasíte s podmínkami a ujednáními.</span><span class="sxs-lookup"><span data-stu-id="0afd6-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Karta Dataverse, pokud váš klient ještě nemá prostředí Dataverse](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="0afd6-132">Proveďte zbývající kroky v průvodci **Nastavení nasazení**.</span><span class="sxs-lookup"><span data-stu-id="0afd6-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="0afd6-133">Poté, co má prostředí stav **Nasazeno** otevřete stránku s podrobnostmi o prostředí.</span><span class="sxs-lookup"><span data-stu-id="0afd6-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="0afd6-134">V sekci **Integrace prostředí Power Platform** jsou uvedeny názvy prostředí Finance and Operations a Dataverse, která jsou propojena.</span><span class="sxs-lookup"><span data-stu-id="0afd6-134">The **Power Platform Integration** section shows the names of the Finance and Operations environment and the Dataverse environment that are linked.</span></span>

    ![Sekce integrace Power Platform](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="0afd6-136">Správce prostředí Finance and Operations se musí přihlásit k LCS a dokončit propojení výběrem **Odkaz na CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="0afd6-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="0afd6-137">Na stránce s podrobnostmi o prostředí jsou uvedeny kontaktní informace na správce.</span><span class="sxs-lookup"><span data-stu-id="0afd6-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="0afd6-138">Po dokončení propojení se stav aktualizuje na **Propojení prostředí proběhlo úspěšně**.</span><span class="sxs-lookup"><span data-stu-id="0afd6-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="0afd6-139">Chcete-li otevřít pracovní prostor **Integrace dat** v prostředí Finance and Operations a ovládat šablony, které jsou k dispozici, vyberte možnost **Odkaz na CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="0afd6-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Tlačítko Odkaz na CDS for Apps v sekci s informacemi o Power Platform](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="0afd6-141">Nelze zrušit propojení prostředí pomocí LCS.</span><span class="sxs-lookup"><span data-stu-id="0afd6-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="0afd6-142">Chcete-li zrušit propojení prostředí, otevřete pracovní prostor **Integrace dat** v prostředí Finance and Operations a poté vyberte možnost **Zrušit propojení**.</span><span class="sxs-lookup"><span data-stu-id="0afd6-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

