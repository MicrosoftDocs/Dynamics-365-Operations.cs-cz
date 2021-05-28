---
title: Podpora daňové funkce u převodních příkazů
description: Toto téma vysvětluje novou podporu daňové funkce u převodních příkazů, která využívá službu výpočtu daně.
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3a5c2b6fb48d98ba045c77ed034d976f7d89af98
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021362"
---
# <a name="tax-feature-support-for-transfer-orders"></a><span data-ttu-id="47a95-103">Podpora daňové funkce u převodních příkazů</span><span class="sxs-lookup"><span data-stu-id="47a95-103">Tax feature support for transfer orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="47a95-104">Toto téma poskytuje informace o výpočtu daně a integraci účtování v převodních příkazech.</span><span class="sxs-lookup"><span data-stu-id="47a95-104">This topic provides information about tax calculation and posting integration in transfer orders.</span></span> <span data-ttu-id="47a95-105">Tato funkce umožňuje nastavit výpočet daně a účtování v převodních příkazech pro převody akcií.</span><span class="sxs-lookup"><span data-stu-id="47a95-105">This functionality lets you set up tax calculation and posting in transfer orders for stock transfers.</span></span> <span data-ttu-id="47a95-106">Podle předpisů Evropské unie (EU) o dani z přidané hodnoty (DPH) se převody akcií považují za intrakomunitární dodávku a intrakomunitární pořízení.</span><span class="sxs-lookup"><span data-stu-id="47a95-106">Under European Union (EU) value-added tax (VAT) regulations, stock transfers are considered intra-community supply and intra-community acquisitions.</span></span>

<span data-ttu-id="47a95-107">Chcete-li konfigurovat a používat tuto funkci, musíte provést tři hlavní kroky:</span><span class="sxs-lookup"><span data-stu-id="47a95-107">To configure and use this functionality, you must complete three main steps:</span></span>

1. <span data-ttu-id="47a95-108">**Nastavení RCS:** Ve službě Regulatory Configuration Service nastavte daňovou funkci, daňové kódy a použitelnost daňových kódů pro určení daňového kódu v převodních příkazech.</span><span class="sxs-lookup"><span data-stu-id="47a95-108">**RCS setup:** In Regulatory Configuration Service, set up the tax feature, tax codes, and tax codes applicability for tax code determination in transfer orders.</span></span>
2. <span data-ttu-id="47a95-109">**Nastavení aplikace Finance:** V Microsoft Dynamics 365 Finance zapněte funkci **Daň v převodním příkazu**, nastavte parametry daňové služby pro zásoby a nastavte základní parametry daně.</span><span class="sxs-lookup"><span data-stu-id="47a95-109">**Finance setup:** In Microsoft Dynamics 365 Finance, turn on the **Tax in transfer order** feature, set up the tax service parameters for inventory, and set up core tax parameters.</span></span>
3. <span data-ttu-id="47a95-110">**Nastavení zásob:** Nastavte konfiguraci zásob pro transakce převodních příkazů.</span><span class="sxs-lookup"><span data-stu-id="47a95-110">**Inventory setup:** Set up the inventory configuration for transfer order transactions.</span></span>

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a><span data-ttu-id="47a95-111">Nastavte ve službě RCS daně a transakce převodních příkazů</span><span class="sxs-lookup"><span data-stu-id="47a95-111">Set up RCS for tax and transfer order transactions</span></span>

<span data-ttu-id="47a95-112">Podle těchto pokynů nastavíte daň, která je zahrnuta v převodním příkazu.</span><span class="sxs-lookup"><span data-stu-id="47a95-112">Follow these steps to set up the tax that is involved in a transfer order.</span></span> <span data-ttu-id="47a95-113">Ve zde zobrazeném příkladu je převodní příkaz směrován z Nizozemska do Belgie.</span><span class="sxs-lookup"><span data-stu-id="47a95-113">In the example that is shown here, the transfer order is from the Netherlands to Belgium.</span></span>

1. <span data-ttu-id="47a95-114">Na stránce **Daňové funkce** na kartě **Verze** vyberte verzi konceptu funkce a poté vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="47a95-114">On the **Tax features** page, on the **Versions** tab, select the draft feature version, and then select **Edit**.</span></span>

    ![Výběr možnosti Upravit](../media/tax-feature-support-01.png)

2. <span data-ttu-id="47a95-116">Na stránce **Nastavení daňových funkcí** na kartě **Daňové kódy** vyberte příkaz **Přidat** a vytvořte nové daňové kódy.</span><span class="sxs-lookup"><span data-stu-id="47a95-116">On the **Tax features setup** page, on the **Tax codes** tab, select **Add** to create new tax codes.</span></span> <span data-ttu-id="47a95-117">V tomto příkladu jsou vytvořeny tři daňové kódy: **NL-Exempt**, **BE-RC-21** a **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="47a95-117">For this example, three tax codes are created: **NL-Exempt**, **BE-RC-21**, and **BE-RC+21**.</span></span>

    - <span data-ttu-id="47a95-118">Když je převodní příkaz odeslán ze skladu v Nizozemsku, je použito nizozemský daňový kód osvobození od DPH (**NL-Exempt**) .</span><span class="sxs-lookup"><span data-stu-id="47a95-118">When a transfer order is shipped from a warehouse in the Netherlands, the Netherlands VAT exempted tax code (**NL-Exempt**) is applied.</span></span>
      
        <span data-ttu-id="47a95-119">Vytvořte daňový kód **NL-Exempt**.</span><span class="sxs-lookup"><span data-stu-id="47a95-119">Create the tax code **NL-Exempt**.</span></span>
        1. <span data-ttu-id="47a95-120">Vyberte příkaz **Přidat** a zapište **NL-Exempt** do pole **Daňový kód**.</span><span class="sxs-lookup"><span data-stu-id="47a95-120">Select **Add**, enter **NL-Exempt** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="47a95-121">Vyberte hodnotu **Podle čisté částky** v poli **Daňová komponenta**.</span><span class="sxs-lookup"><span data-stu-id="47a95-121">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="47a95-122">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="47a95-122">Select **Save**.</span></span>
        4. <span data-ttu-id="47a95-123">Vyberte příkaz **Přidat** v tabulce **Sazba**.</span><span class="sxs-lookup"><span data-stu-id="47a95-123">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="47a95-124">Přepněte pole **Je osvobozeno** na **Ano** v části **Všeobecné**.</span><span class="sxs-lookup"><span data-stu-id="47a95-124">Swtich **Is Exempt** to **Yes** in the **General** section.</span></span>

        ![Daňový kód NL-Exempt](../media/tax-feature-support-02.png)

    - <span data-ttu-id="47a95-126">Když je v belgickém skladu přijat převodní příkaz, použije se mechanismus přenesení daňové povinnosti pomocí daňových kódů **BE-RC-21** a **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="47a95-126">When a transfer order is received at a Belgium warehouse, the reverse charge mechanism is applied by using the **BE-RC-21** and **BE-RC+21** tax codes.</span></span>
        
        <span data-ttu-id="47a95-127">Vytvořte daňový kód **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="47a95-127">Create the tax code **BE-RC-21**.</span></span>      
        1. <span data-ttu-id="47a95-128">Vyberte příkaz **Přidat** a zapište **BE-RC-21** do pole **Daňový kód**.</span><span class="sxs-lookup"><span data-stu-id="47a95-128">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="47a95-129">Vyberte hodnotu **Podle čisté částky** v poli **Daňová komponenta**.</span><span class="sxs-lookup"><span data-stu-id="47a95-129">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="47a95-130">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="47a95-130">Select **Save**.</span></span>
        4. <span data-ttu-id="47a95-131">Vyberte příkaz **Přidat** v tabulce **Sazba**.</span><span class="sxs-lookup"><span data-stu-id="47a95-131">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="47a95-132">Zapište **-21** do pole **Sazba daně**.</span><span class="sxs-lookup"><span data-stu-id="47a95-132">Enter **-21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="47a95-133">Přepněte pole **Je přenesení daňové povinnosti** na **Ano** v části **Všeobecné**.</span><span class="sxs-lookup"><span data-stu-id="47a95-133">Swtich **Is Reverse Charge** to **Yes** in the **General** section.</span></span>
        7. <span data-ttu-id="47a95-134">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="47a95-134">Select **Save**.</span></span>

        ![Daňový kód BE-RC-21 pro přenesení daňové povinnosti](../media/tax-feature-support-03.png)
        
        <span data-ttu-id="47a95-136">Vytvořte daňový kód **BE-RC+21**.</span><span class="sxs-lookup"><span data-stu-id="47a95-136">Create the tax code **BE-RC+21**.</span></span>
        1. <span data-ttu-id="47a95-137">Vyberte příkaz **Přidat** a zapište **BE-RC-21** do pole **Daňový kód**.</span><span class="sxs-lookup"><span data-stu-id="47a95-137">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="47a95-138">Vyberte hodnotu **Podle čisté částky** v poli **Daňová komponenta**.</span><span class="sxs-lookup"><span data-stu-id="47a95-138">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="47a95-139">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="47a95-139">Select **Save**.</span></span>
        4. <span data-ttu-id="47a95-140">Vyberte příkaz **Přidat** v tabulce **Sazba**.</span><span class="sxs-lookup"><span data-stu-id="47a95-140">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="47a95-141">Zapište **21** do pole **Sazba daně**.</span><span class="sxs-lookup"><span data-stu-id="47a95-141">Enter **21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="47a95-142">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="47a95-142">Select **Save**.</span></span>

        ![Daňový kód BE-RC+21 pro přenesení daňové povinnosti](../media/tax-feature-support-04.png)

3. <span data-ttu-id="47a95-144">Definujte použitelnost daňových kódů.</span><span class="sxs-lookup"><span data-stu-id="47a95-144">Define the applicability of the tax codes.</span></span>

    1. <span data-ttu-id="47a95-145">Vyberte příkaz **Spravovat sloupce** a poté vyberte sloupce, které budou použity k sestavení tabulky použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="47a95-145">Select **Manage columns**, and then select columns that should be used to build the applicability table.</span></span>

        > [!NOTE]
        > <span data-ttu-id="47a95-146">Nezapomeňte do tabulky přidat sloupce **Obchodní proces** a **Daňové pokyny**.</span><span class="sxs-lookup"><span data-stu-id="47a95-146">Be sure to add the **Business process** and **Tax directions** columns to the table.</span></span> <span data-ttu-id="47a95-147">Oba sloupce jsou nezbytné pro funkčnost daně v převodních příkazech.</span><span class="sxs-lookup"><span data-stu-id="47a95-147">Both columns are essential to the functionality for tax in transfer orders.</span></span>

    2. <span data-ttu-id="47a95-148">Přidejte pravidla použitelnosti.</span><span class="sxs-lookup"><span data-stu-id="47a95-148">Add applicability rules.</span></span> <span data-ttu-id="47a95-149">Pole **Daňové kódy**, **Daňová skupina** a **Daňová skupina zboží** nenechávejte prázdná.</span><span class="sxs-lookup"><span data-stu-id="47a95-149">Don't leave the **Tax codes**, **Tax group**, and **Item tax group** fields blank.</span></span>
        
        <span data-ttu-id="47a95-150">Přidejte nové pravidlo pro dodávku převodního příkazu.</span><span class="sxs-lookup"><span data-stu-id="47a95-150">Add a new rule for transfer order shipment.</span></span>
        1. <span data-ttu-id="47a95-151">Vyberte příkaz **Přidat** v tabulce **Pravidla použitelnosti**.</span><span class="sxs-lookup"><span data-stu-id="47a95-151">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="47a95-152">V poli **Obchodní proces** vyberte **Zásoby**, aby bylo pravidlo použitelné na převodní příkaz.</span><span class="sxs-lookup"><span data-stu-id="47a95-152">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="47a95-153">V poli **Odeslat ze země / oblasti** zadejte **NLD**.</span><span class="sxs-lookup"><span data-stu-id="47a95-153">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="47a95-154">V poli **Odeslat do země / oblasti** zadejte **BEL**.</span><span class="sxs-lookup"><span data-stu-id="47a95-154">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="47a95-155">V poli **Směr daně** vyberte **Výstup**, aby bylo pravidlo použitelné na dodávku převodního příkazu.</span><span class="sxs-lookup"><span data-stu-id="47a95-155">In the **Tax direction** field, select **Output** to make the rule applicable to transfer order shipment.</span></span>
        6. <span data-ttu-id="47a95-156">V poli **Daňové kódy** vyberte **NL-Exempt**.</span><span class="sxs-lookup"><span data-stu-id="47a95-156">In the **Tax codes** field, select **NL-Exempt**.</span></span>
        7. <span data-ttu-id="47a95-157">V polích **Daňová skupina** a **Daňová skupina zboží** zadejte související skupinu DPH a skupinu DPH zboží, které jsou definovány ve vašem systému Finance.</span><span class="sxs-lookup"><span data-stu-id="47a95-157">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>
        
        <span data-ttu-id="47a95-158">Přidejte další pravidlo pro příjemku převodního příkazu.</span><span class="sxs-lookup"><span data-stu-id="47a95-158">Add another rule for transfer order receipt.</span></span>
        1. <span data-ttu-id="47a95-159">Vyberte příkaz **Přidat** v tabulce **Pravidla použitelnosti**.</span><span class="sxs-lookup"><span data-stu-id="47a95-159">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="47a95-160">V poli **Obchodní proces** vyberte **Zásoby**, aby bylo pravidlo použitelné na převodní příkaz.</span><span class="sxs-lookup"><span data-stu-id="47a95-160">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="47a95-161">V poli **Odeslat ze země / oblasti** zadejte **NLD**.</span><span class="sxs-lookup"><span data-stu-id="47a95-161">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="47a95-162">V poli **Odeslat do země / oblasti** zadejte **BEL**.</span><span class="sxs-lookup"><span data-stu-id="47a95-162">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="47a95-163">V poli **Směr daně** vyberte **Vstup**, aby bylo pravidlo použitelné na příjemku převodního příkazu.</span><span class="sxs-lookup"><span data-stu-id="47a95-163">In the **Tax direction** field, select **Input** to make the rule applicable to transfer order receipt.</span></span>
        6. <span data-ttu-id="47a95-164">V poli **Daňové kódy** vyberte **BE-RC+21** a **BE-RC-21**.</span><span class="sxs-lookup"><span data-stu-id="47a95-164">In the **Tax codes** field, select **BE-RC+21** and **BE-RC-21**.</span></span>
        7. <span data-ttu-id="47a95-165">V polích **Daňová skupina** a **Daňová skupina zboží** zadejte související skupinu DPH a skupinu DPH zboží, které jsou definovány ve vašem systému Finance.</span><span class="sxs-lookup"><span data-stu-id="47a95-165">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>

        ![Pravidla použitelnosti](../media/image5.png)

4. <span data-ttu-id="47a95-167">Dokončete a publikujte novou verzi daňové funkce.</span><span class="sxs-lookup"><span data-stu-id="47a95-167">Complete and publish the new tax feature version.</span></span>

    <span data-ttu-id="47a95-168">[![Změna stavu nové verze](../media/image6.png)](../media/image6.png)</span><span class="sxs-lookup"><span data-stu-id="47a95-168">[![Changing the status of the new version](../media/image6.png)](../media/image6.png)</span></span>

## <a name="set-up-finance-for-transfer-order-transactions"></a><span data-ttu-id="47a95-169">Nastavte v aplikaci Finance daně a transakce převodních příkazů</span><span class="sxs-lookup"><span data-stu-id="47a95-169">Set up Finance for transfer order transactions</span></span>

<span data-ttu-id="47a95-170">Chcete-li povolit a nastavit daně pro převodní příkazy, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="47a95-170">Follow these steps to enable and set up taxes for transfer orders.</span></span>

1. <span data-ttu-id="47a95-171">Ve Finance přejděte na **Pracovní prostory** \> **Správa funkcí**.</span><span class="sxs-lookup"><span data-stu-id="47a95-171">In Finance, go to **Workspaces** \> **Feature management**.</span></span>
2. <span data-ttu-id="47a95-172">V seznamu najděte a vyberte funkci **Daň v převodním příkazu** a poté ji zapněte výběrem možnosti **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="47a95-172">In the list, find and select the **Tax in transfer order** feature, and then select **Enable now** to turn it on.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="47a95-173">Funkce **Daň v převodním příkazu** plně závisí na daňové službě.</span><span class="sxs-lookup"><span data-stu-id="47a95-173">The **Tax in transfer order** feature is fully dependent on the tax service.</span></span> <span data-ttu-id="47a95-174">Lze ji tedy zapnout až po instalaci daňové služby.</span><span class="sxs-lookup"><span data-stu-id="47a95-174">Therefore, it can be turned on only after you've installed the tax service.</span></span>

    ![Daň ve funkci převodního příkazu](../media/image7.png)

3. <span data-ttu-id="47a95-176">Povolte daňovou službu a vyberte obchodní proces **Zásoby**.</span><span class="sxs-lookup"><span data-stu-id="47a95-176">Enable the tax service, and select the **Inventory** business process.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="47a95-177">Tento krok musíte dokončit pro každou právnickou osobu ve Finance, kde chcete mít k dispozici daňovou službu a funkce daně v převodních příkazech.</span><span class="sxs-lookup"><span data-stu-id="47a95-177">You must complete this step for each legal entity in Finance where you want the tax service and the functionality for tax in transfer orders to be available.</span></span>

    1. <span data-ttu-id="47a95-178">Přejděte do nabídky **Daň** \> **Nastavení** \> **Daňová konfigurace** \> **Nastavení daňové služby**.</span><span class="sxs-lookup"><span data-stu-id="47a95-178">Go to **Tax** \> **Setup** \> **Tax configuration** \> **Tax service setup**.</span></span>
    2. <span data-ttu-id="47a95-179">V poli **Obchodní proces** vyberte **Zásoby**.</span><span class="sxs-lookup"><span data-stu-id="47a95-179">In the **Business process** field, select **Inventory**.</span></span>

    ![Nastavení pole Obchodní proces](../media/image8.png)

4. <span data-ttu-id="47a95-181">Zkontrolujte, zda je nastaven mechanismus přenesení daňové povinnosti.</span><span class="sxs-lookup"><span data-stu-id="47a95-181">Verify that the reverse charge mechanism is set up.</span></span> <span data-ttu-id="47a95-182">Přejděte do nabídky **Hlavní kniha** \> **Nastavení** \> **Parametry** a poté na kartě **Přenesená daňová povinnost** ověřte, že je možnost **Povolit přenesenou daňovou povinnost** nastavena na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="47a95-182">Go to **General ledger** \> **Setup** \> **Parameters**, and then, on the **Reverse charge** tab, verify that the **Enable reverse charge** option is set to **Yes**.</span></span>

    ![Povolení přenesené daňové povinnosti](../media/image9.png)

5. <span data-ttu-id="47a95-184">Ověřte, že související daňové kódy, daňové skupiny, daňové skupiny zboží a DIČ byly v aplikaci Finance nastaveny podle pokynů daňové služby.</span><span class="sxs-lookup"><span data-stu-id="47a95-184">Verify that the related tax codes, tax groups, item tax groups, and VAT registration numbers have been set up in Finance according to the tax service guidance.</span></span>
6. <span data-ttu-id="47a95-185">Nastavte účet prozatímního tranzitu.</span><span class="sxs-lookup"><span data-stu-id="47a95-185">Set up an interim transit account.</span></span> <span data-ttu-id="47a95-186">Tento krok je vyžadován pouze v případě, že se daň, která se vztahuje na převodní příkaz, nevztahuje na mechanismus osvobození od daně nebo přenesení daňové povinnosti.</span><span class="sxs-lookup"><span data-stu-id="47a95-186">This step is required only when the tax that is applied to a transfer order isn't applicable to a tax exempted or reverse charge mechanism.</span></span>

    1. <span data-ttu-id="47a95-187">Přejděte na **Daň** \> **Nastavení** \> **DPH** \> **Účetní skupiny**.</span><span class="sxs-lookup"><span data-stu-id="47a95-187">Go to **Tax** \> **Setup** \> **Sales tax** \> **Ledger posting groups**.</span></span>
    2. <span data-ttu-id="47a95-188">V poli **Prozatímní tranzit** vyberte účet hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="47a95-188">In the **Interim transit** field, select a ledger account.</span></span>

    ![Výběr účtu prozatímního tranzitu](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a><span data-ttu-id="47a95-190">Nastavte základní sklad pro transakce převodních příkazů</span><span class="sxs-lookup"><span data-stu-id="47a95-190">Set up basic inventory for transfer order transactions</span></span>

<span data-ttu-id="47a95-191">Podle těchto pokynů nastavte základní sklad, který umožní transakce převodních příkazů.</span><span class="sxs-lookup"><span data-stu-id="47a95-191">Follow these steps to set up basic inventory to enable transfer order transactions.</span></span>

1. <span data-ttu-id="47a95-192">Vytvořte pro své sklady v různých zemích nebo regionech místa odeslání a příjmu a pro každý web přidejte primární adresu.</span><span class="sxs-lookup"><span data-stu-id="47a95-192">Create ship-from and ship-to sites for your warehouses in different countries or regions, and add the primary address for each site.</span></span>

    1. <span data-ttu-id="47a95-193">Přejděte do nabídky **Řízení skladu** \> **Nastavení** \> **Sklad** \> **Pracoviště**.</span><span class="sxs-lookup"><span data-stu-id="47a95-193">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Sites**.</span></span>
    2. <span data-ttu-id="47a95-194">Výběrem položky **Nový** vytvoříte pracoviště, které později přiřadíte ke skladu.</span><span class="sxs-lookup"><span data-stu-id="47a95-194">Select **New** to create the site that you will assign to a warehouse later.</span></span>
    3. <span data-ttu-id="47a95-195">Opakujte krok 2 pro všechna ostatní pracoviště, které musíte vytvořit.</span><span class="sxs-lookup"><span data-stu-id="47a95-195">Repeat step 2 for all the other sites that you must create.</span></span>

    > [!NOTE]
    > <span data-ttu-id="47a95-196">Jedno z pracovišť, které vytvoříte, by se mělo jmenovat **Tranzit**.</span><span class="sxs-lookup"><span data-stu-id="47a95-196">One of the sites that you create should be named **Transit**.</span></span> <span data-ttu-id="47a95-197">V pozdějších krocích tohoto postupu přiřadíte toto pracoviště k tranzitnímu skladu, aby bylo možné zaúčtovat doklady zásob související s daní v transakcích „odeslání“ a „přijetí“ převodních příkazů.</span><span class="sxs-lookup"><span data-stu-id="47a95-197">In later steps of this procedure, you will assign this site to the transit warehouse, so that tax-related inventory vouchers can be posted in "ship" and "receive" transactions for transfer orders.</span></span> <span data-ttu-id="47a95-198">Adresa tranzitního pracoviště není pro výpočet daně relevantní.</span><span class="sxs-lookup"><span data-stu-id="47a95-198">The address of the transit site is irrelevant to tax calculation.</span></span> <span data-ttu-id="47a95-199">Proto je nemůžete nechat prázdné.</span><span class="sxs-lookup"><span data-stu-id="47a95-199">Therefore, you can leave it blank.</span></span>

    ![Nastavení pracovišť](../media/image11.png)

2. <span data-ttu-id="47a95-201">Vytvářejte expediční, tranzitní a dodací sklady.</span><span class="sxs-lookup"><span data-stu-id="47a95-201">Create ship-from, transit, and ship-to warehouses.</span></span> <span data-ttu-id="47a95-202">Veškeré informace o adrese uchovávané ve skladu přepíšou adresu pracoviště během výpočtu daně.</span><span class="sxs-lookup"><span data-stu-id="47a95-202">Any address information that is maintained in a warehouse will override the site address during tax calculation.</span></span>

    1. <span data-ttu-id="47a95-203">Přejděte na **Řízení skladu** \> **Nastavení** \> **Sklad** \> **Sklady**.</span><span class="sxs-lookup"><span data-stu-id="47a95-203">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Warehouses**.</span></span>
    2. <span data-ttu-id="47a95-204">Výběrem položky **Nový** vytvoříte sklad a přiřadíte ho k odpovídajícímu pracovišti.</span><span class="sxs-lookup"><span data-stu-id="47a95-204">Select **New** to create a warehouse, and assign it to the corresponding site.</span></span>
    3. <span data-ttu-id="47a95-205">Opakujte krok 2 a podle potřeby vytvořte sklad pro každé pracoviště.</span><span class="sxs-lookup"><span data-stu-id="47a95-205">Repeat step 2 to create a warehouse for each site as required.</span></span>

    ![Nastavení skladů](../media/image12.png)

    > [!NOTE]
    > <span data-ttu-id="47a95-207">U expedičního skladu musí být pro transakce převodních příkazů vybrán tranzitní sklad v poli **Tranzitní sklad**.</span><span class="sxs-lookup"><span data-stu-id="47a95-207">For a ship-from warehouse, a transit warehouse must be selected in the **Transit warehouse** field for transfer order transactions.</span></span>
    >
    > ![Výběr tranzitního skladu](../media/image13.png)

3. <span data-ttu-id="47a95-209">Zkontrolujte, že je pro transakce převodních příkazů nastavena konfigurace zaúčtování zásob.</span><span class="sxs-lookup"><span data-stu-id="47a95-209">Verify that the inventory posting configuration is set up for transfer order transactions.</span></span>

    1. <span data-ttu-id="47a95-210">Přejděte na **Řízení zásob** \> **Nastavení** \> **Zaúčtování** \> **Zaúčtování**.</span><span class="sxs-lookup"><span data-stu-id="47a95-210">Go to **Inventory management** \> **Setup** \> **Posting** \> **Posting**.</span></span>
    2. <span data-ttu-id="47a95-211">Na kartě **Zásoby** ověřte, zda je nastaven účet hlavní knihy pro oba typy zaúčtování **Skladový výdej** a **Příjem na sklad**.</span><span class="sxs-lookup"><span data-stu-id="47a95-211">On the **Inventory** tab, verify that a ledger account is set up for both **Inventory issue** and **Inventory receipt** posting.</span></span>

        ![Nastavení zaúčtování výdeje a příjmu zásob](../media/image14.png)

    3. <span data-ttu-id="47a95-213">Ověřte, že je nastaven účet hlavní knihy pro zaúčtování **Mezijednotkové závazky**.</span><span class="sxs-lookup"><span data-stu-id="47a95-213">Verify that a ledger account is set up for **Inter-unit payable** posting.</span></span>

        ![Nastavení účtování mezijednotkových závazků](../media/image15.png)

    4. <span data-ttu-id="47a95-215">Ověřte, že je nastaven účet hlavní knihy pro zaúčtování **Mezijednotkové pohledávky**.</span><span class="sxs-lookup"><span data-stu-id="47a95-215">Verify that a ledger account is set up for **Inter-unit receivable** posting.</span></span>

        ![Nastavení účtování mezijednotkových pohledávek](../media/image16.png)
