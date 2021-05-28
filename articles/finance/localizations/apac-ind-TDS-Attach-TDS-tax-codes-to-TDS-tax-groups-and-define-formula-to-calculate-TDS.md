---
title: Připojení daňových kódů TDS k daňovým skupinám TDS a definování vzorce pro výpočet TDS
description: Toto téma vysvětluje, jak nastavit daňové skupiny odečtené u zdroje (TDS) a připojit daňové kódy TDS k daňovým skupinám TDS. Chcete-li vypočítat TDS pro daňovou skupinu TDS, musíte definovat vzorec pro daňové kódy TDS, který je k ní připojen.
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
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023097"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a><span data-ttu-id="37ef6-104">Připojení daňových kódů TDS k daňovým skupinám TDS a definování vzorce pro výpočet TDS</span><span class="sxs-lookup"><span data-stu-id="37ef6-104">Attach TDS tax codes to TDS tax groups and define the formula for calculating TDS</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37ef6-105">Toto téma vysvětluje, jak nastavit daňové skupiny odečtené u zdroje (TDS) a připojit daňové kódy TDS k daňovým skupinám TDS.</span><span class="sxs-lookup"><span data-stu-id="37ef6-105">This topic explains how to set up Tax Deducted at Source (TDS) tax groups and attach TDS tax codes to TDS tax groups.</span></span> <span data-ttu-id="37ef6-106">Chcete-li vypočítat TDS pro daňovou skupinu TDS, musíte definovat vzorec pro daňové kódy TDS, který je k ní připojen.</span><span class="sxs-lookup"><span data-stu-id="37ef6-106">To calculate TDS for a TDS tax group, you must define the formula for TDS tax codes that are attached to it.</span></span>

<span data-ttu-id="37ef6-107">Pomocí těchto kroků můžete nastavit daňovou skupinu TDS, připojit k ní daňové kódy TDS a definovat vzorec pro výpočet TDS.</span><span class="sxs-lookup"><span data-stu-id="37ef6-107">Follow these steps to set up a TDS tax group, attach TDS tax codes to it, and define the formula for calculating TDS.</span></span>

1. <span data-ttu-id="37ef6-108">Přejděte na **Daň \> Nepřímé daně \> Srážková daň \> Skupiny srážkové daně**.</span><span class="sxs-lookup"><span data-stu-id="37ef6-108">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax groups**.</span></span>

    <span data-ttu-id="37ef6-109">[![Stránka Skupiny srážkové daně](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span><span class="sxs-lookup"><span data-stu-id="37ef6-109">[![Withholding tax groups page](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span></span>

2. <span data-ttu-id="37ef6-110">V podokně akcí vyberte **Nový** pro vytvoření skupiny srážkové daně pro TDS a zadejte požadované podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="37ef6-110">On the Action Pane, select **New** to create a withholding tax group for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="37ef6-111">V poli **Typ daně** vyberte **TDS**.</span><span class="sxs-lookup"><span data-stu-id="37ef6-111">In the **Tax type** field, select **TDS**.</span></span>
4. <span data-ttu-id="37ef6-112">Na pevné záložce **Nastavení** výběrem tlačítka **Přidat** vytvořte nový řádek.</span><span class="sxs-lookup"><span data-stu-id="37ef6-112">On the **Setup** FastTab, select **Add** to create a line.</span></span>
5. <span data-ttu-id="37ef6-113">V poli **Kód srážkové daně** vyberte kód daně TDS pro skupinu daní TDS.</span><span class="sxs-lookup"><span data-stu-id="37ef6-113">In the **Withholding tax code** field, select the TDS tax code for the TDS tax group.</span></span> <span data-ttu-id="37ef6-114">Pole **Název srážkové daně** zobrazuje název daňového kódu TDS a pole **Hodnota** zobrazuje hodnotu.</span><span class="sxs-lookup"><span data-stu-id="37ef6-114">The **Withholding tax name** field shows the name of the TDS tax code, and the **Value** field shows the value.</span></span>
6. <span data-ttu-id="37ef6-115">Chcete-li ignorovat mezní limit a mezní limit výjimky, které jsou definovány pro daňovou složku TDS, která je připojena k daňovému zákonu TDS v transakcích TDS, zaškrtněte políčko **Přehlédnout prahovou hodnotu**.</span><span class="sxs-lookup"><span data-stu-id="37ef6-115">To ignore the threshold limit and exception threshold limit that are defined for the TDS tax component that is attached to the TDS tax code in TDS transactions, select the **Overlook threshold** check box.</span></span>
7. <span data-ttu-id="37ef6-116">Aby se zabránilo výpočtu této daňové skupiny v transakcích, zaškrtněte políčko **Vyloučit**.</span><span class="sxs-lookup"><span data-stu-id="37ef6-116">To prevent the tax group from being calculated in transactions, select the **Exempt** check box.</span></span>
8. <span data-ttu-id="37ef6-117">V podokně Akce vyberte **Návrhář** k otevření návrháře vzorců, abyste mohli definovat vzorec pro výpočet TDS pro daňovou skupinu TDS.</span><span class="sxs-lookup"><span data-stu-id="37ef6-117">On the Action Pane, select **Designer** to open the formula designer, so that you can define the formula for calculating TDS for the TDS tax group.</span></span> <span data-ttu-id="37ef6-118">Na stránce **Návrhář** karta **Daně** zobrazuje daňové kódy TDS, které byly vybrány pro daňovou skupinu TDS.</span><span class="sxs-lookup"><span data-stu-id="37ef6-118">On the **Designer** page, the **Taxes** tab shows the TDS tax codes that have been selected for the TDS tax group.</span></span>

    <span data-ttu-id="37ef6-119">[![Stránka návrháře](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span><span class="sxs-lookup"><span data-stu-id="37ef6-119">[![Designer page](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span></span>

9. <span data-ttu-id="37ef6-120">Na kartě **Výpočet** vyberte **Alt + N** k vytvoření čáry.</span><span class="sxs-lookup"><span data-stu-id="37ef6-120">On the **Calculation** tab, select **Alt+N** to create a line.</span></span> <span data-ttu-id="37ef6-121">Pole **ID** zobrazuje automaticky generované ID priority pro výpočet TDS.</span><span class="sxs-lookup"><span data-stu-id="37ef6-121">The **ID** field shows the automatically generated priority ID for TDS calculation.</span></span>
10. <span data-ttu-id="37ef6-122">V poli **Kód daně** vyberte kód daně TDS, pro kterou se má vzorec definovat.</span><span class="sxs-lookup"><span data-stu-id="37ef6-122">In the **Tax code** field, select the TDS tax code to define the formula for.</span></span> <span data-ttu-id="37ef6-123">V tomto poli jsou k dispozici pro výběr všechny daňové kódy TDS, které byly vybrány pro daňovou skupinu TDS.</span><span class="sxs-lookup"><span data-stu-id="37ef6-123">All the TDS tax codes that have been selected for the TDS tax group are available for selection in this field.</span></span>
11. <span data-ttu-id="37ef6-124">V poli **Zdanitelný základ** vyberte základ pro výpočet TDS:</span><span class="sxs-lookup"><span data-stu-id="37ef6-124">In the **Taxable basis** field, select the basis for calculating TDS:</span></span>

    - <span data-ttu-id="37ef6-125">**Hrubá částka** – Vypočítat TDS na základě hrubé částky transakce (tj. částky faktury) pomocí výrazu výpočtu, který je definován pro daňový zákon.</span><span class="sxs-lookup"><span data-stu-id="37ef6-125">**Gross amount** – Calculate TDS based on the gross transaction amount (that is, the invoice amount) by using the calculation expression that is defined for the tax code.</span></span>
    - <span data-ttu-id="37ef6-126">**Bez hrubé částky** – Výpočet TDS na základě výrazu výpočtu, který je definován pro daňový zákon.</span><span class="sxs-lookup"><span data-stu-id="37ef6-126">**Excl Gross amount** – Calculate TDS based on the calculation expression that is defined for the tax code.</span></span>

    > [!NOTE]
    > <span data-ttu-id="37ef6-127">Pole **Zdanitelný základ** nelze nastavit na **Bez hrubé částky** pro daňový zákon TDS, který má ID priority **1**.</span><span class="sxs-lookup"><span data-stu-id="37ef6-127">The **Taxable basis** field can't be set to **Excl Gross amount** for the TDS tax code that has a priority ID of **1**.</span></span>

12. <span data-ttu-id="37ef6-128">Výpočet TDS je založen na vzorci, který je definován v poli **Výpočetní výraz** pro každý daňový kód, který je připojen k daňové skupině TDS.</span><span class="sxs-lookup"><span data-stu-id="37ef6-128">The TDS calculation is based on the formula that is defined in the **Calculation expression** field for each tax code that is attached to the TDS tax group.</span></span> <span data-ttu-id="37ef6-129">Vyberte tlačítko plus (**+**), znaménko minus (**-**), znak násobení (**\**_) nebo znak dělení (_*/**) pro zadání výrazu výpočtu pro vybraný daňový kód TDS v poli **Výpočetní výraz**.</span><span class="sxs-lookup"><span data-stu-id="37ef6-129">Select the plus sign (**+**), minus sign (**-**), multiplication sign (**\**_), or division sign (_*/**) button to enter the calculation expression for the selected TDS tax code in the **Calculation expression** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="37ef6-130">Pro daňový kód TDS, který má ID priority **1**, nelze definovat žádný výpočetní výraz.</span><span class="sxs-lookup"><span data-stu-id="37ef6-130">No calculation expression can be defined for the TDS tax code that has a priority ID of **1**.</span></span>

13. <span data-ttu-id="37ef6-131">Chcete-li definovat výraz výpočtu pro daňový kód TDS v poli **Výpočetní výraz**, přidejte daňové kódy TDS, které jsou k dispozici na kartě **Daně**. Chcete-li přidat daňové kódy TDS do pole **Výpočetní výraz**, můžete použít některou z následujících metod:</span><span class="sxs-lookup"><span data-stu-id="37ef6-131">To define the calculation expression for the TDS tax code in the **Calculation expression** field, add TDS tax codes that are available on the **Taxes** tab. To add TDS tax codes in the **Calculation expression** field, you can use any of the following methods:</span></span>

    - <span data-ttu-id="37ef6-132">Přetáhněte požadovaný daňový kód z karty **Daně** do pole **Výpočetní výraz**.</span><span class="sxs-lookup"><span data-stu-id="37ef6-132">Drag the required tax code from the **Taxes** tab to the **Calculation expression** field.</span></span>
    - <span data-ttu-id="37ef6-133">Dvakrát klepněte (nebo dvakrát klikněte) na požadovaný daňový zákon na kartě **Daně**.</span><span class="sxs-lookup"><span data-stu-id="37ef6-133">Double-tap (or double-click) the required tax code on the **Taxes** tab.</span></span>
    - <span data-ttu-id="37ef6-134">Podržte (nebo klikněte pravým tlačítkem) požadovaný daňový kód na kartě **Daně** a poté vyberte **Přidat daňový kód**.</span><span class="sxs-lookup"><span data-stu-id="37ef6-134">Select and hold (or right-click) the required tax code on the **Taxes** tab, and then select **Add tax code**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="37ef6-135">Před každý daňový zákon TDS vložte výpočetní výraz.</span><span class="sxs-lookup"><span data-stu-id="37ef6-135">Insert a calculation expression before each TDS tax code.</span></span> <span data-ttu-id="37ef6-136">Daňové kódy TDS, které byly přidány do výrazu výpočtu, se zobrazí v závorkách (\[ ...\]).</span><span class="sxs-lookup"><span data-stu-id="37ef6-136">The TDS tax codes that have been added to the calculation expression appear in brackets (\[...\]).</span></span>

14. <span data-ttu-id="37ef6-137">Chcete-li vymazat výpočetní výraz, který je definován pro daňový zákon v poli **Výpočetní výraz**, vyberte tlačítko **C**.</span><span class="sxs-lookup"><span data-stu-id="37ef6-137">To clear the calculation expression that is defined for a tax code in the **Calculation expression** field, select the **C** button.</span></span>
15. <span data-ttu-id="37ef6-138">Odstranění záznamu na serveru kartě **Výpočet**, vyberte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="37ef6-138">To delete a record on the **Calculation** tab, select **Delete**.</span></span>
16. <span data-ttu-id="37ef6-139">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="37ef6-139">Close the page.</span></span>
