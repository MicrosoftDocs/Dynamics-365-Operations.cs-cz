---
title: Vytvoření a použití podmínek zadržení plateb dodavateli
description: Toto téma obsahuje informace o tom, jak nastavit a udržovat podmínky zadržení plateb dodavatelům.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
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
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410201"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="4bbc0-103">Vytvoření a použití podmínek zadržení plateb dodavateli</span><span class="sxs-lookup"><span data-stu-id="4bbc0-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="4bbc0-104">Nastavení podmínek zadržení plateb dodavateli pro projekt je užitečné, pokud si vaše organizace přeje ponechat část plateb provedených některému dodavateli.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="4bbc0-105">Například pokud chcete pozastavit platbu dodavateli, dokud dodané produkty nesplní vaše očekávání.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="4bbc0-106">Podmínky zadržení platby dodavateli lze upřesnit, když vyjednáváte smlouvu s dodavatelem.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="4bbc0-107">Vytvoření podmínek zadržení platby dodavateli</span><span class="sxs-lookup"><span data-stu-id="4bbc0-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="4bbc0-108">Můžete zadat procento zadržené platby dodavateli a procento dříve zadržené částky, kterou chcete vydat.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="4bbc0-109">Částky jsou automaticky zachovány na faktuře dodavateli, dokud smlouva nedosáhne určeného stavu dokončení.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="4bbc0-110">Po nastavení podmínek zadržení je můžete použít pro jakýkoli projekt tohoto dodavatele.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="4bbc0-111">Pomocí následujícího postupu můžete nastavit a spravovat podmínky zadržení plateb dodavatelům.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="4bbc0-112">Přejděte na **Řízení projektů a účetnictví** > **Zadržení** > **Podmínky zadržení plateb dodavateli**.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="4bbc0-113">Volbou **Nová** přidáte nové podmínky zadržení platby dodavateli.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="4bbc0-114">Automaticky se zadá hodnota **ID pravidla** pro novou podmínku.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="4bbc0-115">Do pole **Popis** zadejte krátký popis a na záložce s náhledem **Podmínky** volbou **Přidat řádek** zadejte hodnoty podmínek pro následující:</span><span class="sxs-lookup"><span data-stu-id="4bbc0-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="4bbc0-116">**Procento dodaných jednotek**: Zadejte procento dokončení pro daný termín.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="4bbc0-117">Na faktuře dodavatele se částka automaticky zachová, dokud není fáze dokončení projektu rovna zadanému procentu.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="4bbc0-118">Například pokud zadáte hodnotu 50,00, částky budou zachovány, dokud nebude projekt dokončen z 50 procent.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="4bbc0-119">**Procento k zadržení**: Zadejte procento zadržené částky faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="4bbc0-120">Například pokud zadáte hodnotu 10,00, 10 procent z částky na faktuře dodavatele na zůstane zachováno až dokud projektu nedosáhne procenta dokončení zadaného v poli **Procento dodaných jednotek**.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="4bbc0-121">**Procento k uvolnění**: Volbou **Přidat řádek** zadejte procento libovolné dříve zachované částky, kterou chcete vydat po dosažení vybrané úrovně dokončení projektu.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="4bbc0-122">Pokud máte více než jeden milník pro různé úrovně dokončení projektu, zadejte samostatný řádek s retenčními podmínky dodavateli pro každé retenční pravidlo.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="4bbc0-123">Každý řádek můžete představovat jiné procento zadržení a uvolnění pro každou uvedenou úroveň dokončení projektu.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="4bbc0-124">Po vytvoření podmínek zadržení platby dodavateli je můžete použít na projekt.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="4bbc0-125">Použití podmínek zadržení platby dodavateli na projekt</span><span class="sxs-lookup"><span data-stu-id="4bbc0-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="4bbc0-126">Přejděte na **Řízení projektů a účetnictví** > **Projekty** > **Všechny projekty** a otevřete projekt ze stránky seznamu projektů.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="4bbc0-127">Na pevné kartě **Smlouvy s dodavatelem** vyberte tlačítko **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="4bbc0-128">V poli **Kód účtu** vyberte jednu z následujících možností:</span><span class="sxs-lookup"><span data-stu-id="4bbc0-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="4bbc0-129">**Tabulka**: Podmínky zadržení platby dodavateli se vztahují na jednoho dodavatele.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="4bbc0-130">**Skupina**: Podmínky zadržení platby dodavateli se vztahují na všechny dodavatele ve skupině dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="4bbc0-131">**Vše**: Podmínky zadržení platby dodavateli se vztahují na všechny dodavatele.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="4bbc0-132">V poli **Dodavatel/ skupina dodavatelů** vyberte dodavatele nebo skupinu dodavatelů, na kterou se vztahují podmínky zadržení platby dodavateli.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="4bbc0-133">Pokud jste v rámci předchozího kroku vybrali možnost **Vše**, toto pole nebude k dispozici.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="4bbc0-134">V poli **Podmínky zádržného dodavatele** vyberte podmínky zádržného, které jste vytvořili v předchozích krocích.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="4bbc0-135">Pokud projekt u daného dodavatele využívá také podmínky zaplacení po zaplacení (ZPZ), v poli **Procento prahu ZPZ** zadejte procentuální prahovou hodnotu pro projekt.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="4bbc0-136">Retenční podmínky dodavateli se také zobrazují na nákupních objednávkách vytvořených pro dodavatele.</span><span class="sxs-lookup"><span data-stu-id="4bbc0-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
