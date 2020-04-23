---
title: Skenování čárových kódů pomocí fotoaparátu v aplikaci Dynamics 365 for Finance and Operations – Sklady
description: Toto téma vysvětluje, jak nastavit Dynamics 365 for Finance and Operations – Sklady pro skenování čárových kódů pomocí fotoaparátu na mobilním zařízení.
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9d3b807b18a0a9c7d24763a2a2a7ea9eccf9c2bb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205845"
---
# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-supply-chain-management---warehousing-app"></a><span data-ttu-id="82e48-103">Skenování čárových kódů pomocí fotoaparátu v aplikaci Dynamics 365 Supply Chain Management – sklady</span><span class="sxs-lookup"><span data-stu-id="82e48-103">Scan bar codes using a camera in Dynamics 365 Supply Chain Management - Warehousing app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82e48-104">Toto téma vysvětluje, jak nastavit Dynamics 365 for Finance and Operations – Sklady pro skenování čárových kódů pomocí fotoaparátu na mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="82e48-104">This topic explains how to set up Dynamics 365 for Finance and Operations – Warehousing app to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="82e48-105">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="82e48-105">Prerequisites</span></span>
<span data-ttu-id="82e48-106">Chcete-li použít tuto funkci, musíte mít nainstalovanou verzi 1.2.0.0 aplikace Sklady a vaše zařízení musí mít fotoaparát.</span><span class="sxs-lookup"><span data-stu-id="82e48-106">To use this feature, you need to have version 1.2.0.0 of the Warehousing app installed, and your device must have a camera.</span></span> <span data-ttu-id="82e48-107">Když otevřete aplikaci po aktualizaci, budete vyzváni, abyste povolili aplikaci použít fotoaparát.</span><span class="sxs-lookup"><span data-stu-id="82e48-107">When you open the app after updating, you will be prompted to allow the app to use the camera.</span></span> <span data-ttu-id="82e48-108">Pokud vaše zařízení nemá fotoaparát, nezobrazí se výzva a nebude možné používat fotoaparát jako skener.</span><span class="sxs-lookup"><span data-stu-id="82e48-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="82e48-109">Nastavení</span><span class="sxs-lookup"><span data-stu-id="82e48-109">Setup</span></span>
<span data-ttu-id="82e48-110">V nastavení displeje aplikace Sklady můžete vybrat, zda má být použit fotoaparát ke skenování čárových kódů.</span><span class="sxs-lookup"><span data-stu-id="82e48-110">In the Display settings of the Warehousing application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="82e48-111">Pokud povolíte možnost **Použít fotoaparát jako skener**, lze použít fotoaparát pro každé pole pro zadávání s upřednostňovaným vstupním režimem nastaveným na **Skenování**.</span><span class="sxs-lookup"><span data-stu-id="82e48-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="82e48-112">K určení, zda vstupní pole má být skenovatelné, nastavte na stránce **Názvy polí aplikace Sklady** v **Upřednostňovaný režim vstupu** na **Skenování**.</span><span class="sxs-lookup"><span data-stu-id="82e48-112">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="82e48-113">Pokud je vybrána tato možnost, fotoaparát slouží pro skenování v aplikaci Sklady.</span><span class="sxs-lookup"><span data-stu-id="82e48-113">When this option is selected, a camera can be used for scanning in the Warehousing app.</span></span> <span data-ttu-id="82e48-114">Informace o způsobu konfigurace názvů polí aplikace Sklady naleznete v tématu [Konfigurace názvů polí v aplikaci Sklady](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span><span class="sxs-lookup"><span data-stu-id="82e48-114">For information about how to configure app field names in Warehousing, see [Configure app field names in Warehousing app](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="82e48-115">Podporované formáty čárového kódu</span><span class="sxs-lookup"><span data-stu-id="82e48-115">Supported bar code formats</span></span>
<span data-ttu-id="82e48-116">Jsou podporovány nejběžnější formáty čárového kódu, včetně kódu 128, kódu 39, kódu 93, EAN-8, EAN-13, UPC-E, UPC-A a QR kódů</span><span class="sxs-lookup"><span data-stu-id="82e48-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="82e48-117">Navigace</span><span class="sxs-lookup"><span data-stu-id="82e48-117">Navigation</span></span>
<span data-ttu-id="82e48-118">Stránka fotoaparátu bude spuštěna na každé stránce, kde má vstupní pole preferovaný vstupní režim nastavený na Skenování. Když se nacházíte na stránce fotoaparátu, použijte pro navigaci následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="82e48-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="82e48-119">Klikněte na tlačítko Zpět pro návrat na stránku úloh a podrobností.</span><span class="sxs-lookup"><span data-stu-id="82e48-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="82e48-120">Klikněte na ikonu tužky na stránce úloh a podrobností a přejděte na stránku, kde můžete zadávat vstup ručně.</span><span class="sxs-lookup"><span data-stu-id="82e48-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="82e48-121">Klikněte na ikonu fotoaparátu na stránce úloh a podrobností pro návrat na stránku fotoaparátu.</span><span class="sxs-lookup"><span data-stu-id="82e48-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="82e48-122">Stránka úloh a podrobností</span><span class="sxs-lookup"><span data-stu-id="82e48-122">Task and details page</span></span> | <span data-ttu-id="82e48-123">Stránka fotoaparátu</span><span class="sxs-lookup"><span data-stu-id="82e48-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![Podrobná stránka s úkolem skenování pomocí kamery](./media/camera-scanning-example-task-detail-page50.png)          | ![Menší příklad stránky skenování pomocí kamery](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="82e48-126">Na stránce fotoaparátu po kliknutí na tlačítko fotoaparátu bude toto tlačítko šedé při pokusu o identifikaci čárového kódu.</span><span class="sxs-lookup"><span data-stu-id="82e48-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="82e48-127">Pokud čárový kód není identifikován do 5 sekund, proces vyprší a tlačítko fotoaparátu bude opět dostupné.</span><span class="sxs-lookup"><span data-stu-id="82e48-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="82e48-128">Budete pak moci se pokusit znovu o naskenování čárového kódu.</span><span class="sxs-lookup"><span data-stu-id="82e48-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="82e48-129">Jestliže zaměříte fotoaparátu na čárový kód, udržujte čárový kód zarovnaný mezi čarami pro dosažení nejlepších výsledků.</span><span class="sxs-lookup"><span data-stu-id="82e48-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="82e48-130">Při úspěšném naskenování čárového kódu bude zpracován výsledek a budete navedeni k dalšímu kroku.</span><span class="sxs-lookup"><span data-stu-id="82e48-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="82e48-131">Pokud další krok obsahuje jiné vstupní pole s upřednostňovaným vstupním režimem nastaveným na Skenování, stránka fotoaparátu se znovu spustí.</span><span class="sxs-lookup"><span data-stu-id="82e48-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="82e48-132">Pokud není dalším krokem skenovací pole, stránka kamery se nespustí.</span><span class="sxs-lookup"><span data-stu-id="82e48-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>

