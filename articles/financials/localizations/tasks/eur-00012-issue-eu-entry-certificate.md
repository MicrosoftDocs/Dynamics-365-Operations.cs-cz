---
title: EUR-00012 Vydání vstupního certifikátu EU
description: Tento postup vás provede povolením vstupního certifikátu EU, konfigurací účtu odběratele pro použití vstupních certifikátů a vydáním certifikátu.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustTable, SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CustEntryCertificateJour_W, SrsReportViewerForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee04632eee45aff1fe4b286c65024b0bc57bbb73
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537632"
---
# <a name="eur-00012-issue-an-eu-entry-certificate"></a><span data-ttu-id="43121-103">EUR-00012 Vydání vstupního certifikátu EU</span><span class="sxs-lookup"><span data-stu-id="43121-103">EUR-00012 Issue an EU entry certificate</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43121-104">Tento postup vás provede povolením vstupního certifikátu EU, konfigurací účtu odběratele pro použití vstupních certifikátů a vydáním certifikátu.</span><span class="sxs-lookup"><span data-stu-id="43121-104">This procedure walks you through enabling an EU entry certificate, configuring a customer account to use entry certificates and issue a certificate.</span></span> <span data-ttu-id="43121-105">Tato procedura byla vytvořena pomocí ukázkových dat společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="43121-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="enable-entry-certificate-management"></a><span data-ttu-id="43121-106">Povolit správu vstupních certifikátů</span><span class="sxs-lookup"><span data-stu-id="43121-106">Enable entry certificate management</span></span>
1. <span data-ttu-id="43121-107">Přejděte do nabídky Pohledávky > Nastavení > Parametry pohledávek.</span><span class="sxs-lookup"><span data-stu-id="43121-107">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="43121-108">Klikněte na kartu Dodávky.</span><span class="sxs-lookup"><span data-stu-id="43121-108">Click the Shipments tab.</span></span>
3. <span data-ttu-id="43121-109">Rozbalte oddíl Vstupní certifikát.</span><span class="sxs-lookup"><span data-stu-id="43121-109">Expand the Entry certificate section.</span></span>
4. <span data-ttu-id="43121-110">Zvolte Ano v poli Povolit správu vstupních certifikátů.</span><span class="sxs-lookup"><span data-stu-id="43121-110">Select Yes in the Enable entry certificate management field.</span></span>
5. <span data-ttu-id="43121-111">Zvolte Ano v poli Povolit vystavování vstupních certifikátů.</span><span class="sxs-lookup"><span data-stu-id="43121-111">Select Yes in the Enable entry certificate issuing field.</span></span>
6. <span data-ttu-id="43121-112">Klikněte na kartu Číselné řady.</span><span class="sxs-lookup"><span data-stu-id="43121-112">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="43121-113">V seznamu najděte a vyberte řádek vstupního certifikátu.</span><span class="sxs-lookup"><span data-stu-id="43121-113">In the list, find and select Entry certificate row.</span></span>
8. <span data-ttu-id="43121-114">V poli Kód číselné řady zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="43121-114">In the Number sequence code field, enter or select a value.</span></span>

## <a name="set-up-a-customer"></a><span data-ttu-id="43121-115">Nastavení odběratele</span><span class="sxs-lookup"><span data-stu-id="43121-115">Set up a customer</span></span>
1. <span data-ttu-id="43121-116">Přejděte na Pohledávky > Zákazníci > Všichni odběratelé.</span><span class="sxs-lookup"><span data-stu-id="43121-116">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="43121-117">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="43121-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="43121-118">V poli Účet můžete například filtrovat pomocí hodnoty „DE-015“.</span><span class="sxs-lookup"><span data-stu-id="43121-118">For example, filter on the Account field with a value of 'DE-015'.</span></span>
3. <span data-ttu-id="43121-119">Otevřete podrobnosti o účtu odběratele.</span><span class="sxs-lookup"><span data-stu-id="43121-119">Open customer account details.</span></span>
4. <span data-ttu-id="43121-120">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="43121-120">Click Edit.</span></span>
5. <span data-ttu-id="43121-121">Rozbalte oddíl Faktury a dodávky.</span><span class="sxs-lookup"><span data-stu-id="43121-121">Expand the Invoice and delivery section.</span></span>
6. <span data-ttu-id="43121-122">Zvolte Ano v poli Požadován vstupní certifikát.</span><span class="sxs-lookup"><span data-stu-id="43121-122">Select Yes in the Entry certificate required field.</span></span>
7. <span data-ttu-id="43121-123">Zvolte Ano v poli Vystavit vstupní certifikát.</span><span class="sxs-lookup"><span data-stu-id="43121-123">Select Yes in the Issue entry certificate field.</span></span>
8. <span data-ttu-id="43121-124">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="43121-124">Click Save.</span></span>

## <a name="create-an-eu-entry-certificate-automatically"></a><span data-ttu-id="43121-125">Automatické vytvoření vstupního certifikátu EU</span><span class="sxs-lookup"><span data-stu-id="43121-125">Create an EU entry certificate automatically</span></span>
1. <span data-ttu-id="43121-126">Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="43121-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="43121-127">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="43121-127">Click New.</span></span>
3. <span data-ttu-id="43121-128">V poli Účet odběratele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="43121-128">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="43121-129">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="43121-129">Click OK.</span></span>
5. <span data-ttu-id="43121-130">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="43121-130">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="43121-131">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="43121-131">Click Save.</span></span>
7. <span data-ttu-id="43121-132">V podokně akcí klikněte na položku Vyskladnit a zabalit.</span><span class="sxs-lookup"><span data-stu-id="43121-132">On the Action Pane, click Pick and pack.</span></span>
8. <span data-ttu-id="43121-133">Klikněte na položku Zaúčtovat dodací list.</span><span class="sxs-lookup"><span data-stu-id="43121-133">Click Post packing slip.</span></span>
9. <span data-ttu-id="43121-134">Rozbalte sekci Parametry.</span><span class="sxs-lookup"><span data-stu-id="43121-134">Expand the Parameters section.</span></span>
10. <span data-ttu-id="43121-135">V poli Množství vyberte možnost Vše.</span><span class="sxs-lookup"><span data-stu-id="43121-135">In the Quantity field, select 'All'.</span></span>
11. <span data-ttu-id="43121-136">Zrušte zaškrtnutí políčka Vystavit vstupní certifikát.</span><span class="sxs-lookup"><span data-stu-id="43121-136">Clear the Issue entry certificate check box.</span></span>
    * <span data-ttu-id="43121-137">Při zaúčtování dodacího listu nebo při fakturaci objednávky lze vydat vstupní certifikát.</span><span class="sxs-lookup"><span data-stu-id="43121-137">An entry certificate can be issued during packing slip posting or during order invoicing.</span></span> <span data-ttu-id="43121-138">Ponechte políčko Vystavit vstupní certifikát nezaškrtnuté, abyste mohli certifikát vystavit později.</span><span class="sxs-lookup"><span data-stu-id="43121-138">Leave the Issue entry certificate checkbox unchecked to issue it later.</span></span>  
12. <span data-ttu-id="43121-139">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="43121-139">Click OK.</span></span>
13. <span data-ttu-id="43121-140">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="43121-140">Click OK.</span></span>
14. <span data-ttu-id="43121-141">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="43121-141">On the Action Pane, click Invoice.</span></span>
15. <span data-ttu-id="43121-142">Klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="43121-142">Click Invoice.</span></span>
    * <span data-ttu-id="43121-143">Ověřte, zda jsou zaškrtnuta políčka Požadován vstupní certifikát a Vystavit vstupní certifikát v části Přehled.</span><span class="sxs-lookup"><span data-stu-id="43121-143">Verify that the Entry certificate required and Issue entry certificate checkboxes in the Overview section are marked.</span></span>  <span data-ttu-id="43121-144">Můžete také vybrat políčko Vytisknout vstupní certifikát k povolení tisku certifikátu.</span><span class="sxs-lookup"><span data-stu-id="43121-144">You can also select the Print entry certificate check box to allow printing of the certificate.</span></span>  
16. <span data-ttu-id="43121-145">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="43121-145">Click OK.</span></span>
17. <span data-ttu-id="43121-146">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="43121-146">Click OK.</span></span>
18. <span data-ttu-id="43121-147">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="43121-147">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="43121-148">Klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="43121-148">Click Invoice.</span></span>
20. <span data-ttu-id="43121-149">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="43121-149">On the Action Pane, click Invoice.</span></span>
21. <span data-ttu-id="43121-150">Klikněte na možnost Zobrazit vystavené vstupní certifikáty.</span><span class="sxs-lookup"><span data-stu-id="43121-150">Click View issued entry certificates.</span></span>
22. <span data-ttu-id="43121-151">Klepněte na položku Tisk.</span><span class="sxs-lookup"><span data-stu-id="43121-151">Click Print.</span></span>
23. <span data-ttu-id="43121-152">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="43121-152">Close the page.</span></span>
24. <span data-ttu-id="43121-153">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="43121-153">Click Change status.</span></span>
25. <span data-ttu-id="43121-154">Vyberte možnost v poli Nový stav.</span><span class="sxs-lookup"><span data-stu-id="43121-154">In the New status field, select an option.</span></span>
26. <span data-ttu-id="43121-155">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="43121-155">Click OK.</span></span>
27. <span data-ttu-id="43121-156">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="43121-156">Close the page.</span></span>

## <a name="create-an-eu-entry-certificate-manually"></a><span data-ttu-id="43121-157">Ruční vytvoření vstupního certifikátu EU</span><span class="sxs-lookup"><span data-stu-id="43121-157">Create an EU entry certificate manually</span></span>
1. <span data-ttu-id="43121-158">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="43121-158">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="43121-159">Klikněte na možnost Vytvořit vstupní certifikát.</span><span class="sxs-lookup"><span data-stu-id="43121-159">Click Create entry certificate.</span></span>
3. <span data-ttu-id="43121-160">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="43121-160">Click OK.</span></span>
4. <span data-ttu-id="43121-161">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="43121-161">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="43121-162">Klikněte na možnost Zobrazit vystavené vstupní certifikáty.</span><span class="sxs-lookup"><span data-stu-id="43121-162">Click View issued entry certificates.</span></span>

