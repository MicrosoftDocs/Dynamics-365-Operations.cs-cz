---
title: Vytvoření rozšířených smluv pro účtování na základě průběhu
description: Toto téma vysvětluje, jak vytvořit projektové smlouvy, aby bylo možné vygenerovat faktury pro odběratele na základě procenta dokončené práce.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282815"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="34254-103">Vytvoření rozšířených smluv pro účtování na základě průběhu</span><span class="sxs-lookup"><span data-stu-id="34254-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="34254-104">Toto téma vysvětluje, jak vytvořit projektové smlouvy, aby bylo možné tvořit faktury pro odběratele na základě procenta dokončené práce.</span><span class="sxs-lookup"><span data-stu-id="34254-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="34254-105">Fakturované částky se počítají automaticky pro rozpočtové kategorie práce, které jste nastavili pro projekt.</span><span class="sxs-lookup"><span data-stu-id="34254-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="34254-106">Načasování faktur se nastavuje při vyjednávání projektové smlouvy s odběratelem.</span><span class="sxs-lookup"><span data-stu-id="34254-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="34254-107">Postupy v tomto tématu slouží k nastavení smlouvy, souvisejícího projektu a pravidel účtování pro výpočet fakturovaných částek pro rozpočtové kategorie práce, které jste nastavili pro projekt.</span><span class="sxs-lookup"><span data-stu-id="34254-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="34254-108">Po vytvoření smlouvy a projektu můžete nastavit podrobnosti o projektu.</span><span class="sxs-lookup"><span data-stu-id="34254-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="34254-109">Můžete například definovat aktivity a přiřadit zaměstnance do projektu.</span><span class="sxs-lookup"><span data-stu-id="34254-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="34254-110">Příklad</span><span class="sxs-lookup"><span data-stu-id="34254-110">Example</span></span>

<span data-ttu-id="34254-111">Vaše organizace se zabývá vývojem softwaru.</span><span class="sxs-lookup"><span data-stu-id="34254-111">Your organization is a software development firm.</span></span> <span data-ttu-id="34254-112">Souhlasíte s tím, že pro zákazníka vyvinete balíček pro mzdové účetnictví za celkový poplatek 20 000 USD.</span><span class="sxs-lookup"><span data-stu-id="34254-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="34254-113">Vaše organizace souhlasila s fakturací zákazníka vždy po dokončení určité procentuální části práce na projektu.</span><span class="sxs-lookup"><span data-stu-id="34254-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="34254-114">Pro práci nastavíte následující kategorie projektu, aby je bylo možné použít v procesu fakturace:</span><span class="sxs-lookup"><span data-stu-id="34254-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="34254-115">Konzultace</span><span class="sxs-lookup"><span data-stu-id="34254-115">Consulting</span></span>
- <span data-ttu-id="34254-116">Návrh</span><span class="sxs-lookup"><span data-stu-id="34254-116">Design</span></span>
- <span data-ttu-id="34254-117">Instalace</span><span class="sxs-lookup"><span data-stu-id="34254-117">Installation</span></span>

<span data-ttu-id="34254-118">Můžete také nastavit pravidla účtování, která automaticky vypočítají částky faktur pro procentuální část práce projektu dokončenou v každé kategorii.</span><span class="sxs-lookup"><span data-stu-id="34254-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="34254-119">Správce rozpočtu vytvoří rozpočet pro kategorie projektu.</span><span class="sxs-lookup"><span data-stu-id="34254-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="34254-120">Množství dokončené práce se vypočítá automaticky jako procentuální hodnota dokončené práce z množství práce v rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="34254-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="34254-121">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="34254-121">Prerequisites</span></span>

<span data-ttu-id="34254-122">Před vytvořením projektu, který používá pravidla účtování, je nutné nastavit číselné řady pro pravidla účtování a deník poplatků, který se použije pro zaúčtování vyúčtování postupu.</span><span class="sxs-lookup"><span data-stu-id="34254-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="34254-123">Přejděte na **Řízení a účetnictví projektů** \> **Nastavení** \> **Parametry modulu Řízení a účetnictví projektu**.</span><span class="sxs-lookup"><span data-stu-id="34254-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="34254-124">Na stránce **Parametry modulu Řízení a účetnictví projektu** na kartě **Číselné řady** nastavte číselnou řadu, kterou chcete použít při vytváření pravidel účtování.</span><span class="sxs-lookup"><span data-stu-id="34254-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="34254-125">Přejděte na **Řízení a účetnictví projektů** \> **Deníky** \> **Poplatek**.</span><span class="sxs-lookup"><span data-stu-id="34254-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="34254-126">Na stránce **Deník poplatků** vyberte možnost **Nový** a zadejte název deníku.</span><span class="sxs-lookup"><span data-stu-id="34254-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="34254-127">Vytvoření smlouvy pro postupné vyúčtování</span><span class="sxs-lookup"><span data-stu-id="34254-127">Create a contract for progress billings</span></span>

<span data-ttu-id="34254-128">Tento postup můžete použít k vytvoření projektové smlouvy pro projekt s pevnou cenou.</span><span class="sxs-lookup"><span data-stu-id="34254-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="34254-129">Fakturu projektu vytvoříte poté, co práce provedená na projektu dosáhne určité procentuální hodnoty.</span><span class="sxs-lookup"><span data-stu-id="34254-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="34254-130">Přejděte na **Řízení projektu a účetnictví** \> **Projekty** \> **Projektové smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="34254-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="34254-131">Na stránce **Projektové smlouvy** zvolte **Nová**.</span><span class="sxs-lookup"><span data-stu-id="34254-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="34254-132">V dialogovém okně **Nová projektová smlouva** nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="34254-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="34254-133">**Jméno**</span><span class="sxs-lookup"><span data-stu-id="34254-133">**Name**</span></span>
    - <span data-ttu-id="34254-134">**Typ financování**</span><span class="sxs-lookup"><span data-stu-id="34254-134">**Funding type**</span></span>
    - <span data-ttu-id="34254-135">**Zdroj financování**</span><span class="sxs-lookup"><span data-stu-id="34254-135">**Funding source**</span></span>
    - <span data-ttu-id="34254-136">**Měna prodeje** – Ve výchozím nastavení je tato měna používaná pro faktury odběratelů, které jsou přidruženy ke smlouvě projektu.</span><span class="sxs-lookup"><span data-stu-id="34254-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="34254-137">Prodejní měnu však můžete v konkrétní faktuře odběratele upravit.</span><span class="sxs-lookup"><span data-stu-id="34254-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="34254-138">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="34254-138">Select **OK**.</span></span> <span data-ttu-id="34254-139">Informace se zkopírují do záhlaví stránky **Projektových smluv**.</span><span class="sxs-lookup"><span data-stu-id="34254-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="34254-140">Na stránce **Projektové smlouvy** vyplňte zbývající informace o projektu.</span><span class="sxs-lookup"><span data-stu-id="34254-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="34254-141">Vytvoření projektu pro postupné vyúčtování</span><span class="sxs-lookup"><span data-stu-id="34254-141">Create a project for progress billings</span></span>

<span data-ttu-id="34254-142">Tyto kroky proveďte k vytvoření projektu a jakýchkoli dílčích projektů spojených s projektovou smlouvou.</span><span class="sxs-lookup"><span data-stu-id="34254-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="34254-143">Přejděte na **Řízení projektu a účetnictví** \> **Projekty** \> **Všechny projekty**.</span><span class="sxs-lookup"><span data-stu-id="34254-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="34254-144">Na stránce **Všechny projekty** zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="34254-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="34254-145">V dialogovém okně **Nový projekt** v poli **Typ projektu** vyberte možnost **Čas a materiál**.</span><span class="sxs-lookup"><span data-stu-id="34254-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="34254-146">Vyberte skupinu projektů.</span><span class="sxs-lookup"><span data-stu-id="34254-146">Select a project group.</span></span> <span data-ttu-id="34254-147">Skupina projektu definuje informace o zaúčtování pro projekty přiřazené ke skupině.</span><span class="sxs-lookup"><span data-stu-id="34254-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="34254-148">Zvolte **Vytvořit projekt**.</span><span class="sxs-lookup"><span data-stu-id="34254-148">Select **Create project**.</span></span>
6. <span data-ttu-id="34254-149">Po vytvoření projektu nastavte fázi projektu na **Zpracovává se**.</span><span class="sxs-lookup"><span data-stu-id="34254-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="34254-150">Vytvoření rozpočtu pro projekt</span><span class="sxs-lookup"><span data-stu-id="34254-150">Create a budget for a project</span></span>

<span data-ttu-id="34254-151">Kategorie rozpočtu slouží k automatickému výpočtu částky faktury za procentuální část práce, která byla dokončena v jednotlivých kategoriích.</span><span class="sxs-lookup"><span data-stu-id="34254-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="34254-152">Chcete-li vytvořit kategorie rozpočtu pro odhadované náklady, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="34254-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="34254-153">Přejděte na **Řízení projektu a účetnictví** \> **Projekty** \> **Všechny projekty**.</span><span class="sxs-lookup"><span data-stu-id="34254-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="34254-154">Na stránce **Všechny projekty** vyberte a otevřete požadovaný projekt.</span><span class="sxs-lookup"><span data-stu-id="34254-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="34254-155">Na stránce **Projekty** v podokně akcí na kartě **Plán** ve skupině **Rozpočtu** vyberte možnost **Rozpočet projektu**.</span><span class="sxs-lookup"><span data-stu-id="34254-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="34254-156">Na stránce **Rozpočet projektu** zadejte odhadované náklady pro každou kategorii projektu.</span><span class="sxs-lookup"><span data-stu-id="34254-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="34254-157">Vytvoření fakturačních pravidel pro postupné vyúčtování</span><span class="sxs-lookup"><span data-stu-id="34254-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="34254-158">Přejděte na **Řízení projektu a účetnictví** \> **Projekty** \> **Projektové smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="34254-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="34254-159">Na stránce **Projektové smlouvy** vyberte a otevřete projektovou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="34254-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="34254-160">Na stránce Projektová smlouva na pevné záložce **Pravidla účtování** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="34254-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="34254-161">Na stránce **Pravidlo účtování** v poli **Typ řádku** vyberte možnost **Průběh**.</span><span class="sxs-lookup"><span data-stu-id="34254-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="34254-162">Na pevné záložce **Podrobnosti řádku pravidla účtování** zadejte do pole **Hodnota smlouvy** celkovou hodnotu smlouvy.</span><span class="sxs-lookup"><span data-stu-id="34254-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="34254-163">V poli **Kategorie** vyberte kategorii, do které chcete zaúčtovat transakci poplatku.</span><span class="sxs-lookup"><span data-stu-id="34254-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="34254-164">V poli **Projekt** vyberte projekt nebo úkol, který používá toto pravidlo účtování.</span><span class="sxs-lookup"><span data-stu-id="34254-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="34254-165">Vyolitelné: Pravidlo účtování můžete přiřadit dalším projektům.</span><span class="sxs-lookup"><span data-stu-id="34254-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="34254-166">Na pevné záložce **Projekt** v části **Dostupné projekty** vyberte projekt a poté výběrem tlačítka se šipkou vpravo přidejte projekt do oddílu **Vybrané projekty**.</span><span class="sxs-lookup"><span data-stu-id="34254-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="34254-167">Volitelné: Můžete zadat procento k výpočtu částky, kterou odběratel srazí z plateb na faktuře.</span><span class="sxs-lookup"><span data-stu-id="34254-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="34254-168">Na pevné záložce **Podmínky zadržení platby** vyberte zdroj financování a poté v poli **Procento zádržného** zadejte procento zádržného.</span><span class="sxs-lookup"><span data-stu-id="34254-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="34254-169">Opakujte tyto kroky a vytvořte další pravidla účtování pro projektovou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="34254-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
