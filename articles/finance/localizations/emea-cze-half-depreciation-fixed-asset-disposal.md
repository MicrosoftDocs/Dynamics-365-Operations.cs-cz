---
title: Pololetní odpisy vyřazení dlouhodobého majetku pro Českou republiku
description: Toto téma vysvětluje, jak nastavit pololetní odpisy, tak abyste mohli použít pololetní odpisy dlouhodobého majetku, který je prodaný nebo jinak vyřazený.
author: EvgenyPopovMBS
ms.date: 10/31/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 264554
ms.search.region: Czech Republic
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: af0262763e004f4960c8f25fff35fa773f7a0b6a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839859"
---
# <a name="half-year-depreciation-on-fixed-asset-disposal-for-the-czech-republic"></a><span data-ttu-id="898d6-103">Pololetní odpisy vyřazení dlouhodobého majetku pro Českou republiku</span><span class="sxs-lookup"><span data-stu-id="898d6-103">Half year depreciation on fixed asset disposal for the Czech Republic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="898d6-104">Toto téma vysvětluje, jak nastavit pololetní odpisy, tak abyste mohli použít pololetní odpisy dlouhodobého majetku, který je prodaný nebo jinak vyřazený.</span><span class="sxs-lookup"><span data-stu-id="898d6-104">This topic explains how to set up half-yearly depreciation, so that you can apply half the yearly depreciation for fixed assets that are sold or otherwise disposed of.</span></span>

<span data-ttu-id="898d6-105">Při prodeji nebo jiném vyřazení dlouhodobého majetku můžete použít pololetní odpisy majetku pro daňové účely.</span><span class="sxs-lookup"><span data-stu-id="898d6-105">When a fixed asset is sold or otherwise disposed of, you can apply half the yearly depreciation for the asset, for tax purposes.</span></span> <span data-ttu-id="898d6-106">Pololetní odpisy lze použít bez ohledu na datum vyřazení.</span><span class="sxs-lookup"><span data-stu-id="898d6-106">This half-yearly depreciation can be applied regardless of the disposal date.</span></span>

## <a name="set-up-depreciation-methods-for-the-depreciation-profile"></a><span data-ttu-id="898d6-107">Nastavení metod odpisů pro odpisový profil</span><span class="sxs-lookup"><span data-stu-id="898d6-107">Set up depreciation methods for the depreciation profile</span></span>
<span data-ttu-id="898d6-108">Použijte metody odpisů Rovnoměrné CZ a Zrychlené CZ pro uplatnění pololetních odpisů pro dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="898d6-108">Use the Regular CZ and Accelerated CZ depreciation methods to apply half-yearly depreciation for a fixed asset.</span></span>

1.  <span data-ttu-id="898d6-109">Klikněte na **Dlouhodobý majetek** &gt; **Nastavení** &gt; **Odpisy** &gt; **Odpisové plány**.</span><span class="sxs-lookup"><span data-stu-id="898d6-109">Click **Fixed assets** &gt; **Setup** &gt; **Depreciation** &gt; **Depreciation profiles**.</span></span>
2.  <span data-ttu-id="898d6-110">Klepněte na tlačítko **Nový** a vytvořte odpisový plán.</span><span class="sxs-lookup"><span data-stu-id="898d6-110">Click **New** to create a depreciation profile.</span></span>
3.  <span data-ttu-id="898d6-111">V poli **Metoda** vyberte **Rovnoměrné CZ** nebo **Zrychlené CZ**.</span><span class="sxs-lookup"><span data-stu-id="898d6-111">In the **Method** field, select **Regular CZ** or **Accelerated CZ**.</span></span>
4.  <span data-ttu-id="898d6-112">V poli **Odpisový rok** vyberte jako základ pro výpočet odpisů možnost **Kalendář**.</span><span class="sxs-lookup"><span data-stu-id="898d6-112">In the **Depreciation year** field, select **Calendar** as the basis for the calculation of depreciation.</span></span>
5.  <span data-ttu-id="898d6-113">V poli **Frekvence období** vyberte **Roční**.</span><span class="sxs-lookup"><span data-stu-id="898d6-113">In the **Period frequency** field, select **Yearly**.</span></span>

## <a name="apply-the-half-yearly-depreciation-method"></a><span data-ttu-id="898d6-114">Použití pololetní metody odpisů</span><span class="sxs-lookup"><span data-stu-id="898d6-114">Apply the half yearly depreciation method</span></span>
<span data-ttu-id="898d6-115">Po nastavení metod odpisů lze použít pololetní odpisy majetku pro vyřazený majetek.</span><span class="sxs-lookup"><span data-stu-id="898d6-115">After you set up the depreciation methods, you can apply half the yearly depreciation for assets that were disposed of.</span></span>

1.  <span data-ttu-id="898d6-116">Klikněte na **Dlouhodobý majetek** &gt; **Deníky** &gt; **Dlouhodobý majetek**.</span><span class="sxs-lookup"><span data-stu-id="898d6-116">Click **Fixed assets** &gt; **Journals** &gt; **Fixed assets**.</span></span>
2.  <span data-ttu-id="898d6-117">Na kartě **Přehled** kliknutím na možnost **Nový** vytvořte deník a zadejte požadované podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="898d6-117">On the **Overview** tab, click **New** to create a journal, and then enter the required details.</span></span>
3.  <span data-ttu-id="898d6-118">Kliknutím na možnost **Řádky** otevřete stránku **Doklad deníku**.</span><span class="sxs-lookup"><span data-stu-id="898d6-118">Click **Lines** to open the **Journal voucher** page.</span></span>
4.  <span data-ttu-id="898d6-119">Vytvořte řádek deníku pro dlouhodobý majetek, který byl prodán nebo jinak vyřazen.</span><span class="sxs-lookup"><span data-stu-id="898d6-119">Create a journal line for the fixed asset that was sold or otherwise disposed of.</span></span>
5.  <span data-ttu-id="898d6-120">Klepnutím na **Návrhy** &gt; **Návrh odpisu** otevřete stránku **Návrh odpisu**.</span><span class="sxs-lookup"><span data-stu-id="898d6-120">Click **Proposals** &gt; **Depreciation proposal** to open the **Depreciation proposal** page.</span></span>
6.  <span data-ttu-id="898d6-121">Do pole **Do data** zadejte datum deníku.</span><span class="sxs-lookup"><span data-stu-id="898d6-121">In the **To date** field, enter the journal date.</span></span>
7.  <span data-ttu-id="898d6-122">Zaškrtněte políčko **Vypočítat půlroční částku odpisu**, aby byla vypočítána pololetní částka odpisu.</span><span class="sxs-lookup"><span data-stu-id="898d6-122">Select the **Calculate half-year depreciation amount** check box to calculate half-yearly depreciation.</span></span> <span data-ttu-id="898d6-123">Pokud je toto políčko zaškrtnuto, je roční částka odpisu vydělena dvěma a zaokrouhlena podle nastavení zaokrouhlení knihy odpisů.</span><span class="sxs-lookup"><span data-stu-id="898d6-123">When this check box is selected, the yearly depreciation amount is divided by two and rounded according to the rounding setup for the depreciation book.</span></span>
8.  <span data-ttu-id="898d6-124">Volitelné: Zaškrtněte políčko **Shrnout odpisy** pro shrnutí vypočteného odpisu pro každý dlouhodobý majetek nebo pro každý oceňovací model.</span><span class="sxs-lookup"><span data-stu-id="898d6-124">Optional: Select the **Summarize depreciation** check box to summarize the calculated depreciation for each fixed asset or for each value model.</span></span>
9.  <span data-ttu-id="898d6-125">Kliknutím na tlačítko **OK** zavřete stránku **Návrh odpisu**.</span><span class="sxs-lookup"><span data-stu-id="898d6-125">Click **OK** to close the **Depreciation proposal** page.</span></span>
10. <span data-ttu-id="898d6-126">Zaúčtovat deník</span><span class="sxs-lookup"><span data-stu-id="898d6-126">Post the journal.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]