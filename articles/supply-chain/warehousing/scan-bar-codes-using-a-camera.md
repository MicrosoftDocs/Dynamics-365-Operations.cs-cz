---
title: Skenování čárových kódů pomocí fotoaparátu v mobilní aplikaci Řízení skladu
description: Toto téma vysvětluje, jak nastavit mobilní aplikaci Řízení skladu pro skenování čárových kódů pomocí fotoaparátu na mobilním zařízení.
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831211"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="a38b6-103">Skenování čárových kódů pomocí fotoaparátu v mobilní aplikaci Řízení skladu</span><span class="sxs-lookup"><span data-stu-id="a38b6-103">Scan bar codes using a camera in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a38b6-104">Toto téma vysvětluje, jak nastavit mobilní aplikaci Řízení skladu pro skenování čárových kódů pomocí fotoaparátu na mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="a38b6-104">This topic explains how to set up the Warehouse Management mobile app to scan bar codes using a camera on a mobile device.</span></span>

## <a name="setup"></a><span data-ttu-id="a38b6-105">Nastavení</span><span class="sxs-lookup"><span data-stu-id="a38b6-105">Setup</span></span>

<span data-ttu-id="a38b6-106">V nastavení zobrazení mobilní aplikace Řízení skladu můžete vybrat, zda má být použit fotoaparát ke skenování čárových kódů.</span><span class="sxs-lookup"><span data-stu-id="a38b6-106">In the display settings of the Warehouse Management mobile app, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="a38b6-107">Pokud povolíte možnost **Použít fotoaparát jako skener**, lze použít fotoaparát pro každé pole pro zadávání s upřednostňovaným vstupním režimem nastaveným na **Skenování**.</span><span class="sxs-lookup"><span data-stu-id="a38b6-107">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span>

<span data-ttu-id="a38b6-108">K určení, zda vstupní pole má být skenovatelné, nastavte na stránce **Názvy polí aplikace Sklady** v **Upřednostňovaný režim vstupu** na **Skenování**.</span><span class="sxs-lookup"><span data-stu-id="a38b6-108">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="a38b6-109">Pokud je vybrána tato možnost, fotoaparát slouží pro skenování v mobilní aplikaci Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="a38b6-109">When this option is selected, a camera can be used for scanning in the Warehouse Management mobile app.</span></span> <span data-ttu-id="a38b6-110">Další informace viz [Konfigurace polí pro mobilní aplikaci Řízení skladu](configure-app-field-names-priorities-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="a38b6-110">For more information, see [Configure fields for the Warehouse Management mobile app](configure-app-field-names-priorities-warehouse.md).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="a38b6-111">Podporované formáty čárového kódu</span><span class="sxs-lookup"><span data-stu-id="a38b6-111">Supported bar code formats</span></span>

<span data-ttu-id="a38b6-112">Jsou podporovány nejběžnější formáty čárového kódu, včetně kódu 128, kódu 39, kódu 93, EAN-8, EAN-13, UPC-E, UPC-A a QR kódů</span><span class="sxs-lookup"><span data-stu-id="a38b6-112">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span>

## <a name="navigation"></a><span data-ttu-id="a38b6-113">Navigace</span><span class="sxs-lookup"><span data-stu-id="a38b6-113">Navigation</span></span>

<span data-ttu-id="a38b6-114">Stránka fotoaparátu bude spuštěna na každé stránce, kde má vstupní pole **preferovaný vstupní režim** nastavený na *Skenování*. Když se nacházíte na stránce fotoaparátu, použijte pro navigaci následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="a38b6-114">The camera page will be initiated on each page where the input field has its **Preferred input mode** set to *Scanning*, when you are on the camera page use the following options to navigate:</span></span>

- <span data-ttu-id="a38b6-115">Vyberte tlačítko Zpět pro návrat na stránku **úloh a podrobností**.</span><span class="sxs-lookup"><span data-stu-id="a38b6-115">Select the back button to go back to the **Task and details** page.</span></span>
- <span data-ttu-id="a38b6-116">Vyberte ikonu tužky na stránce **úloh a podrobností** a přejděte na stránku, kde můžete zadávat vstup ručně.</span><span class="sxs-lookup"><span data-stu-id="a38b6-116">Select the pencil on the **Task and details** page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="a38b6-117">Vyberte ikonu fotoaparátu na stránce **úloh a podrobností** pro návrat na stránku fotoaparátu.</span><span class="sxs-lookup"><span data-stu-id="a38b6-117">Select the camera on the **Task and details** page to go back to the camera page.</span></span>

<span data-ttu-id="a38b6-118">Na stránce fotoaparátu po výběru tlačítka fotoaparátu bude toto tlačítko šedé při pokusu o identifikaci čárového kódu.</span><span class="sxs-lookup"><span data-stu-id="a38b6-118">On the camera page, when you select the camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="a38b6-119">Pokud čárový kód není identifikován do 5 sekund, proces vyprší a tlačítko fotoaparátu bude opět dostupné.</span><span class="sxs-lookup"><span data-stu-id="a38b6-119">If a bar code is not identified within 5 seconds, the process will time out and the camera button will become available again.</span></span> <span data-ttu-id="a38b6-120">Budete pak moci se pokusit znovu o naskenování čárového kódu.</span><span class="sxs-lookup"><span data-stu-id="a38b6-120">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="a38b6-121">Jestliže zaměříte fotoaparátu na čárový kód, udržujte čárový kód zarovnaný mezi čarami pro dosažení nejlepších výsledků.</span><span class="sxs-lookup"><span data-stu-id="a38b6-121">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="a38b6-122">Při úspěšném naskenování čárového kódu bude zpracován výsledek a budete navedeni k dalšímu kroku.</span><span class="sxs-lookup"><span data-stu-id="a38b6-122">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="a38b6-123">Pokud další krok obsahuje jiné vstupní pole s upřednostňovaným vstupním režimem nastaveným na Skenování, stránka fotoaparátu se znovu spustí.</span><span class="sxs-lookup"><span data-stu-id="a38b6-123">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="a38b6-124">Pokud není dalším krokem skenovací pole, stránka kamery se nespustí.</span><span class="sxs-lookup"><span data-stu-id="a38b6-124">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]