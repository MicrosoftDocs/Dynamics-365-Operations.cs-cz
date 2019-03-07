---
title: Vytvoření požadavku na nabídku
description: Tato procedura popisuje způsob ručního vytváření požadavku na nabídku.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchCreateRFQCase, InventLocationIdLookup, PurchRFQCaseTable, InventItemIdLookupSimple, EcoResCategorySingleLookup, UnitOfMeasureLookup, PurchRFQEditLines, PurchRFQEditLinesPrintOptions, VendRFQJournal, SrsReportViewerForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4c09149fcbe5731126c2e48a37fafdf71c1d49df
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "334443"
---
# <a name="create-a-request-for-quotation"></a><span data-ttu-id="74ab1-103">Vytvoření požadavku na nabídku</span><span class="sxs-lookup"><span data-stu-id="74ab1-103">Create a request for quotation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="74ab1-104">Tato procedura popisuje způsob ručního vytváření požadavku na nabídku.</span><span class="sxs-lookup"><span data-stu-id="74ab1-104">This procedure shows you how to create a request for quotation.</span></span> <span data-ttu-id="74ab1-105">Toto by obvykle prováděl nákupčí.</span><span class="sxs-lookup"><span data-stu-id="74ab1-105">This would typically be done by a purchasing agent.</span></span> <span data-ttu-id="74ab1-106">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="74ab1-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="74ab1-107">Než začnete, je třeba nastavit typy oslovení.</span><span class="sxs-lookup"><span data-stu-id="74ab1-107">You need to have set up solicitation types before you start.</span></span> <span data-ttu-id="74ab1-108">Po dokončení tohoto úkolu a po vytvoření a odeslání požadavku na nabídku můžete zadat odpovědí pro každého dodavatele, porovnat je a nejlepší smlouvu vybrat.</span><span class="sxs-lookup"><span data-stu-id="74ab1-108">Once you’ve completed this task and you’ve created and sent an RFQ you can then enter the replies per vendor, compare them, and award the contract.</span></span>


## <a name="prepare-a-new-rfq"></a><span data-ttu-id="74ab1-109">Příprava nového požadavku na nabídku</span><span class="sxs-lookup"><span data-stu-id="74ab1-109">Prepare a new RFQ</span></span>
1. <span data-ttu-id="74ab1-110">Přejděte na Zásobování a zdroje > Požadavky na nabídky > Všechny požadavky na nabídky.</span><span class="sxs-lookup"><span data-stu-id="74ab1-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="74ab1-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="74ab1-111">Click New.</span></span>
    * <span data-ttu-id="74ab1-112">K dispozici jsou následující typy nákupu – Nákupní objednávka (výchozí): dokument, který potvrzuje nabídku pro zakoupení produktů nebo přijetí nabídky pro prodej produktů za úplatu.</span><span class="sxs-lookup"><span data-stu-id="74ab1-112">The following purchase types are available: Purchase order (this is the default): a document that confirms the offer to buy products, or the acceptance of an offer to sell products in exchange for payment.</span></span> <span data-ttu-id="74ab1-113">Nákupní žádanka: tento typ je automaticky zaškrtnut, pokud vytvoříte RFQ přímo z nákupní žádanky.</span><span class="sxs-lookup"><span data-stu-id="74ab1-113">Purchase requisition: this type is automatically selected if you create an RFQ directly from a purchase requisition.</span></span> <span data-ttu-id="74ab1-114">Při ručním výběru této možnosti se zobrazí chybové hlášení.</span><span class="sxs-lookup"><span data-stu-id="74ab1-114">If you manually select this option, you’ll get an error.</span></span> <span data-ttu-id="74ab1-115">Nákupní smlouva: dohoda o nákupu určitého množství nebo hodnoty produktu během času.</span><span class="sxs-lookup"><span data-stu-id="74ab1-115">Purchase agreement: an agreement to purchase a specific quantity or value of product over time.</span></span> <span data-ttu-id="74ab1-116">Pokud vyberete tuto možnost, je nutné vybrat rozsah dat, který se vztahuje na nákupní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="74ab1-116">If you select this option, you must select the date range that applies to the purchase agreement.</span></span>  
3. <span data-ttu-id="74ab1-117">Zadejte hodnotu do pole Název dokumentu.</span><span class="sxs-lookup"><span data-stu-id="74ab1-117">In the Document title field, type a value.</span></span>
4. <span data-ttu-id="74ab1-118">V poli Typ oslovení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="74ab1-118">In the Solicitation type field, enter or select a value.</span></span>
    * <span data-ttu-id="74ab1-119">Pokud je s typem oslovení spojena metoda hodnocení, tato funkce poslouží jako výchozí metoda hodnocení pro vytvářený požadavek na nabídku.</span><span class="sxs-lookup"><span data-stu-id="74ab1-119">If a scoring method is associated with the solicitation type, this will be the default scoring method for the RFQ that you’re creating.</span></span> <span data-ttu-id="74ab1-120">Metodu hodnocení je možné změnit později.</span><span class="sxs-lookup"><span data-stu-id="74ab1-120">It is possible to change the scoring method later.</span></span>  
    * <span data-ttu-id="74ab1-121">Zadejte datum do pole Datum dodání.</span><span class="sxs-lookup"><span data-stu-id="74ab1-121">In the Delivery date field, enter a date.</span></span>  
    * <span data-ttu-id="74ab1-122">Vyberte datum, k němuž chcete obdržet položky.</span><span class="sxs-lookup"><span data-stu-id="74ab1-122">Select the date by which you want to receive the items.</span></span>  
    * <span data-ttu-id="74ab1-123">Do pole Datum a čas vypršení platnosti zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="74ab1-123">In the Expiration date and time field, enter a date and time.</span></span>  
    * <span data-ttu-id="74ab1-124">Zadejte datum a čas, do kdy musí dodavatelé odpovědět na požadavek na nabídku.</span><span class="sxs-lookup"><span data-stu-id="74ab1-124">Specify the date and time by which vendors must respond to the RFQ.</span></span>  
5. <span data-ttu-id="74ab1-125">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="74ab1-125">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="74ab1-126">Jako výchozí dodací adresa je nastavena adresa skladu.</span><span class="sxs-lookup"><span data-stu-id="74ab1-126">The delivery address will default to the warehouse address.</span></span>  
6. <span data-ttu-id="74ab1-127">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="74ab1-127">Click OK.</span></span>

## <a name="add-lines"></a><span data-ttu-id="74ab1-128">Přidat řádky</span><span class="sxs-lookup"><span data-stu-id="74ab1-128">Add lines</span></span>
    * <span data-ttu-id="74ab1-129">Po zadání základních informací o RFQ je třeba zadat zboží nebo služby, pro které chcete vytvořit nabídku od dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="74ab1-129">After you’ve specified the basic information about your RFQ, you specify the goods or services that you want vendors to bid on.</span></span> <span data-ttu-id="74ab1-130">Položka je výchozí typ řádku.</span><span class="sxs-lookup"><span data-stu-id="74ab1-130">Item is the default line type.</span></span>   
1. <span data-ttu-id="74ab1-131">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="74ab1-131">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="74ab1-132">Pokud používáte data USMF, můžete vybrat T0020.</span><span class="sxs-lookup"><span data-stu-id="74ab1-132">If you're using USMF, you can select T0020.</span></span>  
2. <span data-ttu-id="74ab1-133">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="74ab1-133">In the Quantity field, enter a number.</span></span>
3. <span data-ttu-id="74ab1-134">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="74ab1-134">Click Add line.</span></span>
4. <span data-ttu-id="74ab1-135">V poli Typ řádku vyberte Kategorie.</span><span class="sxs-lookup"><span data-stu-id="74ab1-135">In the Line type field, select 'Category'.</span></span>
    * <span data-ttu-id="74ab1-136">Můžete použít typ Řádek kategorie a vytvořit požadavky na nabídku pro položky bez skladu zboží nebo služeb.</span><span class="sxs-lookup"><span data-stu-id="74ab1-136">You can use the Category line type to create RFQs for non-inventory goods or services.</span></span> <span data-ttu-id="74ab1-137">Poté musíte vybrat typ zboží nebo služeb z hierarchií kategorií zásobování.</span><span class="sxs-lookup"><span data-stu-id="74ab1-137">You then need to select the type of goods or services from a hierarchy of procurement categories.</span></span>  
5. <span data-ttu-id="74ab1-138">V Kategorie zásobování zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="74ab1-138">In the Procurement category field, enter or select a value.</span></span>
6. <span data-ttu-id="74ab1-139">Do pole Název produktu zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="74ab1-139">In the Product name field, type a value.</span></span>
7. <span data-ttu-id="74ab1-140">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="74ab1-140">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="74ab1-141">V poli Jednotka zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="74ab1-141">In the Unit field, enter or select a value.</span></span>

## <a name="add-vendors"></a><span data-ttu-id="74ab1-142">Přidat dodavatele</span><span class="sxs-lookup"><span data-stu-id="74ab1-142">Add vendors</span></span>
1. <span data-ttu-id="74ab1-143">Klepnutím na Záhlaví můžete změnit zobrazení řádků na zobrazení záhlaví.</span><span class="sxs-lookup"><span data-stu-id="74ab1-143">Click Header to change from the Lines view to the Header view.</span></span> 
2. <span data-ttu-id="74ab1-144">Rozbalte sekci Dodavatel.</span><span class="sxs-lookup"><span data-stu-id="74ab1-144">Expand the Vendor section.</span></span>
3. <span data-ttu-id="74ab1-145">Klikněte na Automatické přidání dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="74ab1-145">Click Auto-add vendors.</span></span>
    * <span data-ttu-id="74ab1-146">Můžete přidávat dodavatele do RFQ automaticky podle kategorie zásobování požadovaných položek.</span><span class="sxs-lookup"><span data-stu-id="74ab1-146">You can add vendors to the RFQ automatically, based on the procurement category of the items requested.</span></span> <span data-ttu-id="74ab1-147">Pokud nejsou na řádcích zahrnuti žádní schválení dodavatelé pro kategorie, můžete je přidat ručně.</span><span class="sxs-lookup"><span data-stu-id="74ab1-147">If there are no vendors approved for the categories included in the lines you can add vendors manually.</span></span>  
4. <span data-ttu-id="74ab1-148">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="74ab1-148">Click Add.</span></span>
5. <span data-ttu-id="74ab1-149">V poli Účet dodavatele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="74ab1-149">In the Vendor account field, enter or select a value.</span></span>
6. <span data-ttu-id="74ab1-150">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="74ab1-150">Click Add.</span></span>
7. <span data-ttu-id="74ab1-151">V poli Účet dodavatele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="74ab1-151">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="74ab1-152">Jakmile vyberete dodavatele, změní se stav na Vytvořeno.</span><span class="sxs-lookup"><span data-stu-id="74ab1-152">Once you’ve selected a vendor, the status is Created.</span></span> <span data-ttu-id="74ab1-153">To znamená, že informace o dodavateli jsou uloženy do RFQ, ale nebyly odesláno RFQ dodavateli.</span><span class="sxs-lookup"><span data-stu-id="74ab1-153">This means that the vendor information has been saved in the RFQ, but you have not sent the RFQ to the vendor.</span></span> <span data-ttu-id="74ab1-154">Dodavatele lze přidat do RFQ bez ohledu na stav dodavatele.</span><span class="sxs-lookup"><span data-stu-id="74ab1-154">You can add a vendor to an RFQ regardless of the vendor status.</span></span>  

## <a name="send-the-rfq-to-vendors"></a><span data-ttu-id="74ab1-155">Odešlete RFQ dodavatelům</span><span class="sxs-lookup"><span data-stu-id="74ab1-155">Send the RFQ to vendors</span></span>
1. <span data-ttu-id="74ab1-156">Klepněte na tlačítko Odeslat.</span><span class="sxs-lookup"><span data-stu-id="74ab1-156">Click Send.</span></span>
    * <span data-ttu-id="74ab1-157">Na stránce Odesílání požadavku na nabídku se ujistěte, že dodavatelé v seznamu jsou dodavateli, kteří mají přijmout požadavek na nabídku.</span><span class="sxs-lookup"><span data-stu-id="74ab1-157">In the Sending request for quotation page, check that the vendors in the list are the ones that you want to receive the RFQ.</span></span>  
2. <span data-ttu-id="74ab1-158">Klepněte na položku Tisk.</span><span class="sxs-lookup"><span data-stu-id="74ab1-158">Click Print.</span></span>
    * <span data-ttu-id="74ab1-159">Toto dialogové okno umožňuje vytisknout požadavek na nabídku.</span><span class="sxs-lookup"><span data-stu-id="74ab1-159">This dialog allows you to print the RFQ.</span></span> <span data-ttu-id="74ab1-160">Pokud zvolíte tisk listu s odpovědí, obsah bude definován v parametrech zásobování a zdroje.</span><span class="sxs-lookup"><span data-stu-id="74ab1-160">If you choose to print a reply sheet, the contents of this are defined in Procurement and Sourcing parameters.</span></span> <span data-ttu-id="74ab1-161">Chcete-li vybrat, jak vytisknout list s odpovědí po otevření dialogového okna Tisk, klepněte na Rozšířené možnosti tisku.</span><span class="sxs-lookup"><span data-stu-id="74ab1-161">To choose how to print reply sheets, once you’ve opened the Print dialog, click Advanced printing options.</span></span> <span data-ttu-id="74ab1-162">Bude vytištěn jeden požadavek na nabídku pro každého dodavatele, který obsahuje řádky se stavem Vytvořeno neb Odesláno.</span><span class="sxs-lookup"><span data-stu-id="74ab1-162">One RFQ will be printed for each vendor containing the lines that have the status of Created or Sent.</span></span> <span data-ttu-id="74ab1-163">Zrušené řádky a řádky s registrovanými odpověďmi nebudou vytištěny.</span><span class="sxs-lookup"><span data-stu-id="74ab1-163">Canceled lines and lines with registered replies will not be printed.</span></span>   
3. <span data-ttu-id="74ab1-164">Klikněte na možnost Zrušit.</span><span class="sxs-lookup"><span data-stu-id="74ab1-164">Click Cancel.</span></span>
4. <span data-ttu-id="74ab1-165">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="74ab1-165">Click OK.</span></span>
5. <span data-ttu-id="74ab1-166">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="74ab1-166">Close the page.</span></span>
6. <span data-ttu-id="74ab1-167">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="74ab1-167">Close the page.</span></span>

## <a name="view-the-rfq-journal"></a><span data-ttu-id="74ab1-168">Zobrazení deníku požadavku na nabídku</span><span class="sxs-lookup"><span data-stu-id="74ab1-168">View the RFQ journal</span></span>
1. <span data-ttu-id="74ab1-169">Přejděte na Zásobování a zdroje > Požadavky na nabídky > Požadavek na zpracování nabídek > Deníky požadavků na nabídku.</span><span class="sxs-lookup"><span data-stu-id="74ab1-169">Go to Procurement and sourcing > Requests for quotations > Request for quotations follow-up > Request for quotation journals.</span></span>
2. <span data-ttu-id="74ab1-170">Klikněte na Náhled/tisk.</span><span class="sxs-lookup"><span data-stu-id="74ab1-170">Click Preview/Print.</span></span>
3. <span data-ttu-id="74ab1-171">Klepněte na Náhled originálu.</span><span class="sxs-lookup"><span data-stu-id="74ab1-171">Click Original preview.</span></span>
4. <span data-ttu-id="74ab1-172">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="74ab1-172">Close the page.</span></span>
5. <span data-ttu-id="74ab1-173">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="74ab1-173">Close the page.</span></span>

