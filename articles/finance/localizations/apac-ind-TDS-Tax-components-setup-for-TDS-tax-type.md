---
title: Nastavení složek daně pro typ daně TDS
description: Toto téma vysvětluje, jak nastavit složky srážkové daně pro daňový typ se srážkou daně u zdroje (TDS). Vysvětluje také, jak definovat prahovou hranici, která se používá k výpočtu TDS pro každou složku TDS.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 6e0a6a05fcb4afb8c8965e25c3089bc1b3d98431
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023083"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a><span data-ttu-id="9821e-104">Nastavení složek daně pro typ daně TDS</span><span class="sxs-lookup"><span data-stu-id="9821e-104">Set up tax components for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9821e-105">Toto téma vysvětluje, jak nastavit složky srážkové daně pro daňový typ se srážkou daně u zdroje (TDS).</span><span class="sxs-lookup"><span data-stu-id="9821e-105">This topic explains how to set up withholding tax components for the Tax Deducted at Source (TDS) tax type.</span></span> <span data-ttu-id="9821e-106">Složky TDS jsou TDS, příplatek, PE-Cess a SHE Cess.</span><span class="sxs-lookup"><span data-stu-id="9821e-106">The TDS components are TDS, surcharge, PE-Cess, and SHE Cess.</span></span> <span data-ttu-id="9821e-107">Toto téma vysvětluje, jak definovat prahovou hranici, která se používá k výpočtu TDS pro každou složku TDS.</span><span class="sxs-lookup"><span data-stu-id="9821e-107">This topic also explains how to define the threshold that is used to calculate TDS for each TDS component.</span></span> <span data-ttu-id="9821e-108">Dále můžete definovat prahovou hodnotu výjimky, která se používá k výpočtu TDS pro každou složku TDS.</span><span class="sxs-lookup"><span data-stu-id="9821e-108">Additionally, you can define an exception threshold that is used to calculate TDS for each TDS component.</span></span>

<span data-ttu-id="9821e-109">Chcete-li nastavit složky TDS, postupujte následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="9821e-109">Follow these steps to set up TDS components.</span></span>

1. <span data-ttu-id="9821e-110">Přejděte do nabídky **Daň \> Nastavení \> Srážková daň \> Složky srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="9821e-110">Go to **Tax \> Setup \> Withholding tax \> Withholding tax components**.</span></span>

    <span data-ttu-id="9821e-111">[![Stránka Složky srážkové daně](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span><span class="sxs-lookup"><span data-stu-id="9821e-111">[![Withholding tax components page](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span></span>

2. <span data-ttu-id="9821e-112">V poli **Typ daně** vyberte **TDS** a nastavte složky srážkové daně pro typ daně TDS.</span><span class="sxs-lookup"><span data-stu-id="9821e-112">In the **Tax type** field, select **TDS** to set up withholding tax components for the TDS tax type.</span></span>
3. <span data-ttu-id="9821e-113">V podokně Akce vyberte možnost **Nový** a vytvořte řádek.</span><span class="sxs-lookup"><span data-stu-id="9821e-113">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="9821e-114">Do pole **Složka srážkové daně** zadejte název složky TDS.</span><span class="sxs-lookup"><span data-stu-id="9821e-114">In the **Withholding tax component** field, enter a name for the TDS component.</span></span>
5. <span data-ttu-id="9821e-115">V poli **Skupina složek srážkové daně** vyberte skupinu složek TDS srážkové daně, ke které chcete složku TDS připojit.</span><span class="sxs-lookup"><span data-stu-id="9821e-115">In the **Withholding tax component group** field, select the TDS withholding tax component group to attach the TDS component to.</span></span>
6. <span data-ttu-id="9821e-116">Na pevné záložce **Obecné** v poli **Popis** zadejte popis složky TDS.</span><span class="sxs-lookup"><span data-stu-id="9821e-116">On the **General** FastTab, in the **Description** field, enter a description of  the TDS component.</span></span>
7. <span data-ttu-id="9821e-117">V podokně akcí vyberte **Mezní hodnota** k otevření stránky **Mezní hodnota** stránka, abyste mohli definovat mezí hodnotu, která se použije pro výpočet TDS pro složku TDS.</span><span class="sxs-lookup"><span data-stu-id="9821e-117">On the Action Pane, select **Threshold** to open **Threshold** page, so that you can define the threshold that is used to calculate TDS for the TDS component.</span></span>
8. <span data-ttu-id="9821e-118">Použijte pole **Od data** a **Do data** k definování období, na které se prahová hodnota vztahuje.</span><span class="sxs-lookup"><span data-stu-id="9821e-118">Use the **From date** and **To date** fields to define the period that the threshold is applicable to.</span></span>
9. <span data-ttu-id="9821e-119">Na rychlé kartě **Všeobecné** do pole **Mezní hodnota** zadejte mezní hodnotu, která se použije pro výpočet TDS pro komponentu TDS.</span><span class="sxs-lookup"><span data-stu-id="9821e-119">On the **General** FastTab, in the **Threshold** field, enter the threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="9821e-120">Daň bude odečtena u zdroje, pouze pokud kumulativní částka faktury překročí prahovou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9821e-120">The tax will be deducted at the source only when the cumulative invoice amount crosses the threshold.</span></span>

    <span data-ttu-id="9821e-121">Například pokud je prahová částka 10 000, TDS se vypočítá poté, co kumulativní částka faktury přesáhne 10 000 (jinými slovy, když je to 10 001 nebo více).</span><span class="sxs-lookup"><span data-stu-id="9821e-121">For example, if the threshold amount is 10,000, TDS is calculated after the cumulative invoice amount exceeds 10,000 (in other words, when it's 10,001 or more).</span></span>

10. <span data-ttu-id="9821e-122">Do pole **Mezní hodnota výjimky** zadejte mezní hodnotu výjimky, která se použije pro výpočet TDS pro komponentu TDS.</span><span class="sxs-lookup"><span data-stu-id="9821e-122">In the **Exception threshold** field, enter the exception threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="9821e-123">Daň na řádku faktury bude odečtena u zdroje, pouze pokud faktury překročí prahovou hodnotu výjimky.</span><span class="sxs-lookup"><span data-stu-id="9821e-123">The tax on an invoice line will be deducted at the source only when the amount crosses the exception threshold.</span></span>

    <span data-ttu-id="9821e-124">Například pokud je prahová hodnota pro výjimku 5000, TDS se vypočítá na konkrétním řádku faktury, pokud částka faktury přesáhne 5000 (jinými slovy, pokud je to 5001 nebo více).</span><span class="sxs-lookup"><span data-stu-id="9821e-124">For example, if the exception threshold amount is 5,000, TDS is calculated on a specific invoice line if the invoice line amount exceeds 5,000 (in other words, if it's 5,001 or more).</span></span>

    <span data-ttu-id="9821e-125">[![Stránka Mezní hodnota](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span><span class="sxs-lookup"><span data-stu-id="9821e-125">[![Threshold page](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="9821e-126">Výše mezní hodnoty výjimky musí být menší nebo rovna mezní hodnotě.</span><span class="sxs-lookup"><span data-stu-id="9821e-126">The exception threshold amount must be less than or equal to the threshold amount.</span></span>
    >
    > <span data-ttu-id="9821e-127">Daň se odečte za transakci, pokud částka transakce překročí mezní hodnotu pro výjimku, i když kumulativní částka faktury nepřekročí mezní hodnotu uvedenou v poli **Mezní hodnota**.</span><span class="sxs-lookup"><span data-stu-id="9821e-127">The tax is deducted for a transaction if the transaction amount crosses the exception threshold, even if the cumulative invoice amount doesn't cross the threshold that is specified in the **Threshold** field.</span></span>

11. <span data-ttu-id="9821e-128">Zavřete stránku **Mezní hodnota** pro návrat na stránku **Složky srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="9821e-128">Close the **Threshold** page to return to the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="9821e-129">V podokně akcí vyberte **Kopírovat** k otevření dialogového okna **Zkopírovat složky srážkové daně**, abyste mohli zkopírovat složky TDS, které byly nastaveny pro jednu skupinu složek TDS, do jiné skupiny složek TDS.</span><span class="sxs-lookup"><span data-stu-id="9821e-129">On the Action Pane, select **Copy** to open the **Copy withholding tax components** dialog box, so that you can copy the TDS components that were set up for one TDS component group to another TDS component group.</span></span>
13. <span data-ttu-id="9821e-130">V poli **Z** vyberte skupinu složek TDS, ze které chcete kopírovat složky TDS.</span><span class="sxs-lookup"><span data-stu-id="9821e-130">In the **From** field, select the TDS component group to copy the TDS components from.</span></span> <span data-ttu-id="9821e-131">V poli **Do** vyberte skupinu složek srážkové daně, do které chcete kopírovat složky TDS.</span><span class="sxs-lookup"><span data-stu-id="9821e-131">In the **To** field, select the withholding tax component group to copy the TDS components to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9821e-132">Společné složky TDS, které jsou připojeny k oběma skupinám složek TDS, se nekopírují.</span><span class="sxs-lookup"><span data-stu-id="9821e-132">Common TDS components that are attached to both TDS component groups aren't copied.</span></span>

14. <span data-ttu-id="9821e-133">Vyberte **OK** ke zkopírování a vytvoření složek TDS pro další skupinu složek TDS na stránce **Složky srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="9821e-133">Select **OK** to copy and create TDS components for the other TDS component group on the **Withholding tax components** page.</span></span>

    <span data-ttu-id="9821e-134">[![Dialogové okno Zkopírovat složky srážkové daně](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span><span class="sxs-lookup"><span data-stu-id="9821e-134">[![Copy withholding tax components dialog box](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span></span>

15. <span data-ttu-id="9821e-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9821e-135">Close the page.</span></span>
