---
title: Nastavení kódů srážkové daně pro typy daně TDS
description: Toto téma vysvětluje, jak nastavit kódy daně odečtené u zdroje (TDS).
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
ms.openlocfilehash: d56a23f7af7633e1761a8a7c48f71381d6f14df2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023100"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a><span data-ttu-id="8a7f7-103">Nastavení kódů srážkové daně pro typy daně TDS</span><span class="sxs-lookup"><span data-stu-id="8a7f7-103">Set up withholding tax codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a7f7-104">Toto téma vysvětluje, jak nastavit kódy daně odečtené u zdroje (TDS).</span><span class="sxs-lookup"><span data-stu-id="8a7f7-104">This topic explains how to set up tax codes for Tax Deducted at Source (TDS).</span></span>

1. <span data-ttu-id="8a7f7-105">Přejděte na **Daň \> Nepřímé daně \> Srážková daň \> Kódy srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax codes**.</span></span>

    <span data-ttu-id="8a7f7-106">[![Stránka Kódy srážkové daně](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span><span class="sxs-lookup"><span data-stu-id="8a7f7-106">[![Withholding tax codes page](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span></span>

2. <span data-ttu-id="8a7f7-107">V podokně akcí vyberte **Nový** pro vytvoření kódu srážkové daně pro TDS a zadejte požadované podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-107">On the Action Pane, select **New** to create a withholding tax code for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="8a7f7-108">Na pevné záložce **Obecné** v poli **Typ daně** vyberte **TDS** ke kategorizaci kódu daně jako kódu daně TDS.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-108">On the **General** FastTab, in the **Tax type** field, select **TDS** to categorize the tax code as a TDS tax code.</span></span>
4. <span data-ttu-id="8a7f7-109">V poli **Období vypořádání** vyberte období vypořádání TDS pro kód daně TDS.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-109">In the **Settlement period** field, select the TDS settlement period for the TDS tax code.</span></span>
5. <span data-ttu-id="8a7f7-110">V poli **Hlavní účet** vyberte účet hlavní knihy, na který by měla být zaúčtována částka TDS.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-110">In the **Main account** field, select the ledger account that the TDS amount should be posted to.</span></span>
6. <span data-ttu-id="8a7f7-111">V poli **Pohledávka** vyberte pohledávku, na kterou má být zaúčtována částka TDS odečtená v prodejních transakcích.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-111">In the **Receivable account** field, select the receivable account that the TDS amount that is deducted in sales transactions should be posted to.</span></span>

    <span data-ttu-id="8a7f7-112">Pole **Původ** je automaticky nastaveno na hodnotu **Procento z hrubé částky**, kterou nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-112">The **Origin** field is automatically set to **Percentage of gross amount**, and the value can't be changed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8a7f7-113">Nemůžete nastavit původ na **Procento čisté částky** pro daňové kódy typu daně TDS.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-113">You can't set the origin to **Percentage of net amount** for tax codes of the TDS tax type.</span></span>

7. <span data-ttu-id="8a7f7-114">V poli **Komponenta srážkové daně** vyberte skupinu komponent srážkové daně pro kód daně TDS.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-114">In the **Withholding tax component** field, select the TDS tax component for the TDS tax code.</span></span>
8. <span data-ttu-id="8a7f7-115">V podokně akcí vyberte **Hodnoty** k otevření stránky **Hodnoty srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-115">On the Action Pane, select **Values** to open the **Withholding tax values** page.</span></span>
9. <span data-ttu-id="8a7f7-116">V poli **Od data** zadejte počáteční datum pro hodnotu TDS.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-116">In the **From date** field, enter the start date for the TDS value.</span></span> <span data-ttu-id="8a7f7-117">V poli **Do data** zadejte koncové datum.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-117">In the **To date** field, enter the end date.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8a7f7-118">Pole **Minimální limit**, **Horní limit** a **% vyloučení** nejsou k dispozici pro daňové kódy typu daně TDS.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-118">The **Minimum limit**, **Upper limit**, and **Exclude %** fields aren't available for tax codes of the TDS tax type.</span></span>

10. <span data-ttu-id="8a7f7-119">V poli **Hodnota** zadejte procento TDS používané pro kód daně TDS.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-119">In the **Value** field, enter the percentage of TDS for the TDS tax code.</span></span>
11. <span data-ttu-id="8a7f7-120">Zavřete stránku **Hodnoty srážkové daně** pro návrat na stránku **Kódy srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-120">Close the **Withholding tax values** page to return to the **Withholding tax codes** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8a7f7-121">Tlačítko **Limity** na stránce **Kódy srážkové daně** není k dispozici pro daňové kódy typu daně TDS.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-121">The **Limits** button on the **Withholding tax codes** page isn't available for tax codes of the TDS tax type.</span></span>

12. <span data-ttu-id="8a7f7-122">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8a7f7-122">Close the page.</span></span>
