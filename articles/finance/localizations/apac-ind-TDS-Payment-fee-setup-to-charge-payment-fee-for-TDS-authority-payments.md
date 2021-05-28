---
title: Nastavení platebních poplatků pro platby autoritě TDS
description: Toto téma vysvětluje, jak nastavit poplatky za platby, které se účtují za platby autority pro daně odečtené u zdroje (TDS).
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
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023103"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a><span data-ttu-id="cdffb-103">Nastavení platebních poplatků pro platby autoritě TDS</span><span class="sxs-lookup"><span data-stu-id="cdffb-103">Set up payment fees for TDS authority payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cdffb-104">Toto téma vysvětluje, jak nastavit poplatky za platby, které se účtují za platby autority pro daně odečtené u zdroje (TDS).</span><span class="sxs-lookup"><span data-stu-id="cdffb-104">This topic explains how to set up payment fees that are charged for Tax Deducted at Source (TDS) authority payments.</span></span>

1. <span data-ttu-id="cdffb-105">Přejděte do nabídky **Závazky \> Nastavení platby \> Platební poplatek**.</span><span class="sxs-lookup"><span data-stu-id="cdffb-105">Go to **Accounts payable \> Payment setup \> Payment fee**.</span></span>

    <span data-ttu-id="cdffb-106">[![Stránka Platební poplatek](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span><span class="sxs-lookup"><span data-stu-id="cdffb-106">[![Payment fee page](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span></span>

2. <span data-ttu-id="cdffb-107">Vybráním možnosti **Nové** vytvořte platební poplatek a poté zadejte požadované informace.</span><span class="sxs-lookup"><span data-stu-id="cdffb-107">Select **New** to create a payment fee, and enter the required details.</span></span>
3. <span data-ttu-id="cdffb-108">V poli **Typ poplatku** vyberte typ platebního poplatku.</span><span class="sxs-lookup"><span data-stu-id="cdffb-108">In the **Fee type** field, select the type of payment fee:</span></span>

    - <span data-ttu-id="cdffb-109">**Není**</span><span class="sxs-lookup"><span data-stu-id="cdffb-109">**None**</span></span>
    - <span data-ttu-id="cdffb-110">**Úrok** – Úroky jsou účtovány za pozdní platby, které jsou provedeny dodavateli autority TDS.</span><span class="sxs-lookup"><span data-stu-id="cdffb-110">**Interest** – Interest is charged on late payments that are made to the TDS authority vendor.</span></span>
    - <span data-ttu-id="cdffb-111">**Jiné** – Jiné platby jsou účtovány za pozdní platby, které jsou provedeny dodavateli autority TDS.</span><span class="sxs-lookup"><span data-stu-id="cdffb-111">**Others** – Other charges are charged on late payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="cdffb-112">Pokud vyberete **Úrok** nebo **Ostatní**, pole **Účtovat** je automaticky nastaveno na **Hlavní kniha**.</span><span class="sxs-lookup"><span data-stu-id="cdffb-112">If you select **Interest** or **Others**, the **Charge** field is automatically set to **Ledger**.</span></span>

4. <span data-ttu-id="cdffb-113">Pokud jste vybrali **Úrok** nebo **Ostatní** v poli **Typ pole**, v poli **Hlavní účet** vyberte účet hlavní knihy, do kterého chcete zaúčtovat úrok nebo jiné poplatky.</span><span class="sxs-lookup"><span data-stu-id="cdffb-113">If you selected **Interest** or **Others** in the **Field type** field, in the **Main account** field, select the ledger account to post the interest or other charges to.</span></span>
5. <span data-ttu-id="cdffb-114">Zadejte další požadované údaje.</span><span class="sxs-lookup"><span data-stu-id="cdffb-114">Enter the other required details.</span></span>
6. <span data-ttu-id="cdffb-115">V podokně Akce vyberte **Nastavení platebního poplatku** k otevření stránky **Nastavení platebního poplatku**, kde můžete nastavit poplatky za platby pro různé kombinace bank, způsobů plateb, platebních podmínek, měn a časových intervalů.</span><span class="sxs-lookup"><span data-stu-id="cdffb-115">On the Action Pane, select **Payment fee setup** to open the **Payment fee setup** page, where you can set up payment fees for various combinations of banks, methods of payment, payment specifications, currencies, and date intervals.</span></span>

    <span data-ttu-id="cdffb-116">[![Stránka Nastavení platebních poplatků](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span><span class="sxs-lookup"><span data-stu-id="cdffb-116">[![Payment fee setup page](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span></span>

7. <span data-ttu-id="cdffb-117">Na kartě **Přehled** v poli **Seskupení** uveďte, u kterých bank nastavujete poplatek za platbu:</span><span class="sxs-lookup"><span data-stu-id="cdffb-117">On the **Overview** tab, in the **Groupings** field, specify which banks you're setting up the payment fee for:</span></span>

    - <span data-ttu-id="cdffb-118">**Tabulka** – Poplatek platí pro konkrétní bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="cdffb-118">**Table** – The fee is valid for a specific bank account.</span></span>
    - <span data-ttu-id="cdffb-119">**Skupina** – Poplatek platí pro konkrétní skupinu bank.</span><span class="sxs-lookup"><span data-stu-id="cdffb-119">**Group** – The fee is valid for a specific bank group.</span></span>
    - <span data-ttu-id="cdffb-120">**Vše** – Poplatek je platný pro všechny bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="cdffb-120">**All** – The fee is valid for all the bank accounts.</span></span>

8. <span data-ttu-id="cdffb-121">Pokud jste vybrali **Tabulka** nebo **Skupina** v poli **Seskupení**, v poli **Bankovní relace** vyberte konkrétní bankovní účet nebo bankovní skupinu, pro kterou nastavujete poplatek za platbu.</span><span class="sxs-lookup"><span data-stu-id="cdffb-121">If you selected **Table** or **Group** in the **Groupings** field, in the **Bank relation** field, select the specific bank account or bank group that you're setting up the payment fee for.</span></span>
9. <span data-ttu-id="cdffb-122">V poli **Metoda platby** vyberte metodu platby, která má být použita pro platbu platebního poplatku.</span><span class="sxs-lookup"><span data-stu-id="cdffb-122">In the **Method of payment** field, select the method of payment for the payment of fees.</span></span>
10. <span data-ttu-id="cdffb-123">V poli **Specifikace platby** vyberte nebo zadejte kód specifikace platby, který byl vygenerován na stránce **Specifikace platby**.</span><span class="sxs-lookup"><span data-stu-id="cdffb-123">In the **Payment specification** field, select or enter the payment specification code that was generated on the **Payment specification** page.</span></span>
    - <span data-ttu-id="cdffb-124">Specifikace platby se používají pro platbu metodou elektronického převodu finančních prostředků.</span><span class="sxs-lookup"><span data-stu-id="cdffb-124">The Payment specification is used with electronic fund transfer methods of payment.</span></span>
12. <span data-ttu-id="cdffb-125">V poli **Měna platby** vyberte měnu, která poplatek aktivuje.</span><span class="sxs-lookup"><span data-stu-id="cdffb-125">In the **Payment currency** field, select the currency that activates the fee.</span></span> <span data-ttu-id="cdffb-126">Poplatek mohou aktivovat pouze transakce, které používají vybranou měnu.</span><span class="sxs-lookup"><span data-stu-id="cdffb-126">Only transactions that use the selected currency can activate the fee.</span></span> <span data-ttu-id="cdffb-127">Pokud toto pole nevyplníte, všechny měny aktivují poplatek.</span><span class="sxs-lookup"><span data-stu-id="cdffb-127">If you leave this field blank, all currencies activate the fee.</span></span>
13. <span data-ttu-id="cdffb-128">V poli **Procento/částka** vyberte metodu výpočtu.</span><span class="sxs-lookup"><span data-stu-id="cdffb-128">In the **Percentage/Amount** field, select the calculation method.</span></span> <span data-ttu-id="cdffb-129">Možnosti jsou **Částka**, **Procento** a **Interval**.</span><span class="sxs-lookup"><span data-stu-id="cdffb-129">The options are **Amount**, **Percent**, and **Interval**.</span></span>
14. <span data-ttu-id="cdffb-130">Do pole **Částka poplatku** zadejte částku poplatku jako procento platby nebo částku za jednu platbu.</span><span class="sxs-lookup"><span data-stu-id="cdffb-130">In the **Fee amount** field, specify the fee amount as either a percentage of the payment or the amount for one payment.</span></span>
15. <span data-ttu-id="cdffb-131">V poli **Měna poplatku** zadejte kód měny pro poplatek.</span><span class="sxs-lookup"><span data-stu-id="cdffb-131">In the **Fee currency** field, specify the currency code for the fee.</span></span>
16. <span data-ttu-id="cdffb-132">Vyberte kartu **Všeobecné** k zobrazení nebo úpravě údajů vybraného bankovního účtu.</span><span class="sxs-lookup"><span data-stu-id="cdffb-132">Select the **General** tab to view or modify the details for the selected bank account.</span></span>

    <span data-ttu-id="cdffb-133">[![Karta Obecné](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span><span class="sxs-lookup"><span data-stu-id="cdffb-133">[![General tab](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span></span>

16. <span data-ttu-id="cdffb-134">Do pole **Minimum** zadejte minimální částku transakce, která aktivuje poplatek.</span><span class="sxs-lookup"><span data-stu-id="cdffb-134">In the **Minimum** field, enter the minimum transaction amount that activates the fee.</span></span>
17. <span data-ttu-id="cdffb-135">Do pole **Maximum** zadejte maximální částku transakce, která aktivuje poplatek.</span><span class="sxs-lookup"><span data-stu-id="cdffb-135">In the **Maximum** field, enter the maximum transaction amount that activates the fee.</span></span>
18. <span data-ttu-id="cdffb-136">V polích **Od data** a **K datu** definujte časové období pro výpočet poplatků.</span><span class="sxs-lookup"><span data-stu-id="cdffb-136">In the **From date** and **To date** fields, define a date range for calculating fees.</span></span>
19. <span data-ttu-id="cdffb-137">Do pole **Minimální poplatek** zadejte částku poplatku jako procento platby nebo částku za jednu platbu.</span><span class="sxs-lookup"><span data-stu-id="cdffb-137">In the **Minimum fee** field, specify the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
20. <span data-ttu-id="cdffb-138">Do pole **Skupina DPH** vyberte skupinu DPH, která se má použít k výpočtu DPH pro částku poplatku.</span><span class="sxs-lookup"><span data-stu-id="cdffb-138">In the **Sales tax group** field, select the sales tax group to use to calculate the sales tax for the fee amount.</span></span>
21. <span data-ttu-id="cdffb-139">Do pole **Skupina DPH položky** vyberte skupinu DPH položky, která se má použít k výpočtu DPH položky pro částku poplatku.</span><span class="sxs-lookup"><span data-stu-id="cdffb-139">In the **Item sales tax group** field, select the item sales tax group to use to calculate the item sales tax for the fee amount.</span></span>
22. <span data-ttu-id="cdffb-140">Vyberte kartu **Interval**.</span><span class="sxs-lookup"><span data-stu-id="cdffb-140">Select the **Interval** tab.</span></span> 

    <span data-ttu-id="cdffb-141">[![Karta Interval](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span><span class="sxs-lookup"><span data-stu-id="cdffb-141">[![Interval tab](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span></span>

23. <span data-ttu-id="cdffb-142">Do pole **Dny** zadejte počet dní mezi datem zaúčtování (datem slevy) platby a datem splatnosti vlastní směnky.</span><span class="sxs-lookup"><span data-stu-id="cdffb-142">In the **Days** field, enter the number of days between the posting date (discounting date) of the payment and the due date of the promissory note.</span></span>
24. <span data-ttu-id="cdffb-143">V poli **Procento/částka** vyberte, zda je specifikace procentem nebo stanovenou částkou.</span><span class="sxs-lookup"><span data-stu-id="cdffb-143">In the **Percentage/Amount** field, select whether the specification is a percentage or a set amount.</span></span>
25. <span data-ttu-id="cdffb-144">Do pole **Částka poplatku** zadejte částku poplatku jako procento platby nebo částku za jednu platbu.</span><span class="sxs-lookup"><span data-stu-id="cdffb-144">In the **Fee amount** field, enter the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
26. <span data-ttu-id="cdffb-145">Zavřete stránku **Nastavení platebního poplatku**.</span><span class="sxs-lookup"><span data-stu-id="cdffb-145">Close the **Payment fee setup** page.</span></span>
27. <span data-ttu-id="cdffb-146">Zavřete stránku **Platební poplatek**.</span><span class="sxs-lookup"><span data-stu-id="cdffb-146">Close the **Payment fee** page.</span></span>
