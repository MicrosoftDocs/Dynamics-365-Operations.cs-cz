--- 
title: "Registrace položek pro položky umožňující pokročilé uskladnění s použitím deníku doručení zboží"
description: "Tento postup popisuje, jak zaregistrovat položky pomocí deníku doručení položek, když použijete pokročilé postupy řízení skladu."
author: BibiSp
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 09d5d61a1950a5ab341d3bb3c814b6985d5e910e
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="2b08f-103">Registrace položek pro položky umožňující pokročilé uskladnění s použitím deníku doručení zboží</span><span class="sxs-lookup"><span data-stu-id="2b08f-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2b08f-104">Tento postup popisuje, jak zaregistrovat položky pomocí deníku doručení položek, když použijete pokročilé postupy řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="2b08f-104">This procedure shows you how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="2b08f-105">To obvykle provádí přijímající pracovník.</span><span class="sxs-lookup"><span data-stu-id="2b08f-105">This would usually be done by a receiving clerk.</span></span> 

<span data-ttu-id="2b08f-106">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="2b08f-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="2b08f-107">Před zahájením tohoto průvodce musíte mít potvrzenou nákupní objednávku s otevřeným řádkem nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="2b08f-107">You need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="2b08f-108">Položky na řádku musí být na skladě a nesmí používat varianty produktu a nesmí obsahovat sledovací dimenze.</span><span class="sxs-lookup"><span data-stu-id="2b08f-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="2b08f-109">Položka zároveň musí být přidružena ke skupině dimenzí úložiště, kde jsou aktivní postupy řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="2b08f-109">And the item needs to be associated with a warehouse management process enabled storage dimension group.</span></span> <span data-ttu-id="2b08f-110">Sklad, který se používá, musí být povolen pro procesy správy skladu a umístění, které používáte pro příjem, musí být řízeno registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="2b08f-110">The warehouse that’s used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span> <span data-ttu-id="2b08f-111">V případě, že používáte USMF, můžete k vytvoření nákupní objednávky použít účet společnosti 1001, sklad 51 a položku M9200.</span><span class="sxs-lookup"><span data-stu-id="2b08f-111">If you’re using USMF, you can use company account 1001, Warehouse 51, and item M9200 to create your PO.</span></span> 

<span data-ttu-id="2b08f-112">Poznamenejte si číslo nákupní objednávky, kterou vytvoříte, a také si poznamenejte číslo položky a pracoviště, které se používá pro váš řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="2b08f-112">Make a note of the number of the purchase order that you create, and also note the item number and the site that you used for your purchase order line.</span></span>


## <a name="create-an-item-arrival-journal-header"></a><span data-ttu-id="2b08f-113">Vytvoření záhlaví deníku pro doručení položky</span><span class="sxs-lookup"><span data-stu-id="2b08f-113">Create an item arrival journal header</span></span>
1. <span data-ttu-id="2b08f-114">Přejděte na Doručení položky.</span><span class="sxs-lookup"><span data-stu-id="2b08f-114">Go to Item arrival.</span></span>
2. <span data-ttu-id="2b08f-115">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="2b08f-115">Click New.</span></span>
3. <span data-ttu-id="2b08f-116">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="2b08f-116">In the Name field, type a value.</span></span>
    * <span data-ttu-id="2b08f-117">Pokud používáte data USMF, můžete zadat „WHS“.</span><span class="sxs-lookup"><span data-stu-id="2b08f-117">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="2b08f-118">Pokud používáte jiná data, deník s názvem, který zvolíte, musí mít následující vlastnosti: u možnosti Zkontrolovat výdejní skl. místo musí být nastavena hodnota Ne a u Řízení karantény musí být nastavena hodnota Ne.</span><span class="sxs-lookup"><span data-stu-id="2b08f-118">If you’re using other data, the journal whose name you choose has to have the following properties: Check picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="2b08f-119">Zadejte hodnotu do pole Číslo.</span><span class="sxs-lookup"><span data-stu-id="2b08f-119">In the Number field, type a value.</span></span>
5. <span data-ttu-id="2b08f-120">Zadejte hodnotu do pole Pracoviště.</span><span class="sxs-lookup"><span data-stu-id="2b08f-120">In the Site field, type a value.</span></span>
    * <span data-ttu-id="2b08f-121">Vyberte pracoviště, které jste používali pro na řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="2b08f-121">Select the site that you used for your purchase order line.</span></span> <span data-ttu-id="2b08f-122">To bude sloužit jako výchozí hodnota, která bude výchozí pro všechny řádky v deníku.</span><span class="sxs-lookup"><span data-stu-id="2b08f-122">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="2b08f-123">Pokud jste použili sklad 51 USMF, zvolte pracoviště 5.</span><span class="sxs-lookup"><span data-stu-id="2b08f-123">If you used warehouse 51 in USMF, choose site 5.</span></span>  
6. <span data-ttu-id="2b08f-124">Zadejte hodnotu do pole Sklad.</span><span class="sxs-lookup"><span data-stu-id="2b08f-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="2b08f-125">Vyberte platný sklad pro pracoviště, které jste vybrali.</span><span class="sxs-lookup"><span data-stu-id="2b08f-125">Select a valid warehouse for the site that you’ve selected.</span></span> <span data-ttu-id="2b08f-126">To bude sloužit jako výchozí hodnota, která bude výchozí pro všechny řádky v deníku.</span><span class="sxs-lookup"><span data-stu-id="2b08f-126">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="2b08f-127">Používáte-li například hodnoty v USMF, vyberte 51.</span><span class="sxs-lookup"><span data-stu-id="2b08f-127">If you’re using the example values in USMF, select 51.</span></span>  
7. <span data-ttu-id="2b08f-128">Zadejte hodnotu do pole Místo konání.</span><span class="sxs-lookup"><span data-stu-id="2b08f-128">In the Location field, type a value.</span></span>
    * <span data-ttu-id="2b08f-129">Vyberte platné umístění ve skladu, který jste vybrali.</span><span class="sxs-lookup"><span data-stu-id="2b08f-129">Select a valid location in the warehouse that you’ve selected.</span></span> <span data-ttu-id="2b08f-130">Skladové místo musí být přiděleno k profilu skladového místa, které je řízeno registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="2b08f-130">The location has to be associated with a location profile, which is license plate controlled.</span></span> <span data-ttu-id="2b08f-131">To bude sloužit jako výchozí hodnota, která bude výchozí pro všechny řádky v deníku.</span><span class="sxs-lookup"><span data-stu-id="2b08f-131">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="2b08f-132">Používáte-li například hodnoty v USMF, vyberte Bulk-008.</span><span class="sxs-lookup"><span data-stu-id="2b08f-132">If you’re using the example values in USMF, select Bulk-008.</span></span>  
8. <span data-ttu-id="2b08f-133">Klepněte pravým tlačítkem myši na šipku rozevíracího seznamu v poli Registrační značka, a pak vyberte možnost Zobrazit podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="2b08f-133">Right-click on the drop-down arrow in the License plate field and then select View details.</span></span>
9. <span data-ttu-id="2b08f-134">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="2b08f-134">Click New.</span></span>
10. <span data-ttu-id="2b08f-135">V poli Registrační značka zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2b08f-135">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="2b08f-136">Poznamenejte si hodnoty.</span><span class="sxs-lookup"><span data-stu-id="2b08f-136">Make a note of the value.</span></span>  
11. <span data-ttu-id="2b08f-137">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="2b08f-137">Click Save.</span></span>
12. <span data-ttu-id="2b08f-138">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2b08f-138">Close the page.</span></span>
13. <span data-ttu-id="2b08f-139">V poli Registrační značka zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2b08f-139">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="2b08f-140">Zadejte hodnotu registrační značky, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="2b08f-140">Enter the value of the license plate that you just created.</span></span> <span data-ttu-id="2b08f-141">To bude sloužit jako výchozí hodnota, která bude výchozí pro všechny řádky v deníku.</span><span class="sxs-lookup"><span data-stu-id="2b08f-141">This will serve as a default value, which will default to all lines in the journal.</span></span>  
14. <span data-ttu-id="2b08f-142">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="2b08f-142">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="2b08f-143">Přidání řádku</span><span class="sxs-lookup"><span data-stu-id="2b08f-143">Add a line</span></span>
1. <span data-ttu-id="2b08f-144">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="2b08f-144">Click Add line.</span></span>
2. <span data-ttu-id="2b08f-145">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="2b08f-145">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="2b08f-146">Zadejte číslo položky, která je použita na řádku nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="2b08f-146">Enter the item number that you used on the purchase order line.</span></span>  
3. <span data-ttu-id="2b08f-147">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="2b08f-147">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="2b08f-148">Zadejte množství, které chcete registrovat.</span><span class="sxs-lookup"><span data-stu-id="2b08f-148">Enter the quantity that you want to register.</span></span>  
    * <span data-ttu-id="2b08f-149">Pole Datum určuje datum, kdy bude na skladě registrováno množství této položky.</span><span class="sxs-lookup"><span data-stu-id="2b08f-149">The Date field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    * <span data-ttu-id="2b08f-150">ID šarže bude vyplněno systémem, pokud může být jedinečně identifikováno z uvedených informací.</span><span class="sxs-lookup"><span data-stu-id="2b08f-150">The lot ID will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="2b08f-151">V opačném případě bude nutné ho přidat ručně.</span><span class="sxs-lookup"><span data-stu-id="2b08f-151">Otherwise you will have to add this manually.</span></span> <span data-ttu-id="2b08f-152">Toto je povinné pole, které propojí tuto registraci k řádku konkrétního zdrojového dokumentu.</span><span class="sxs-lookup"><span data-stu-id="2b08f-152">This is a mandatory field, which links this registration to a specific source document line.</span></span>  

## <a name="complete-the-registration"></a><span data-ttu-id="2b08f-153">Dokončení registrace</span><span class="sxs-lookup"><span data-stu-id="2b08f-153">Complete the registration</span></span>
1. <span data-ttu-id="2b08f-154">Klikněte na tlačítko Ověřit.</span><span class="sxs-lookup"><span data-stu-id="2b08f-154">Click Validate.</span></span>
    * <span data-ttu-id="2b08f-155">To kontroluje, zda je deník připraven k zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="2b08f-155">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="2b08f-156">Jestliže se ověření nezdaří, které bude nutné před zaúčtováním deníku opravit chyby.</span><span class="sxs-lookup"><span data-stu-id="2b08f-156">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
2. <span data-ttu-id="2b08f-157">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="2b08f-157">Click OK.</span></span>
    * <span data-ttu-id="2b08f-158">Poté, co jste klepnuli na tlačítko OK, zkontrolujte zprávu.</span><span class="sxs-lookup"><span data-stu-id="2b08f-158">After you clicked OK, check the message.</span></span> <span data-ttu-id="2b08f-159">Musí existovat zpráva o tom, že deník je v pořádku.</span><span class="sxs-lookup"><span data-stu-id="2b08f-159">There should be a message saying that the journal is OK.</span></span>  
3. <span data-ttu-id="2b08f-160">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="2b08f-160">Click Post.</span></span>
4. <span data-ttu-id="2b08f-161">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="2b08f-161">Click OK.</span></span>
    * <span data-ttu-id="2b08f-162">Poté, co jste kliknuli na tlačítko OK, zkontrolujte pruh zpráv.</span><span class="sxs-lookup"><span data-stu-id="2b08f-162">After you have clicked OK, check the message bar.</span></span> <span data-ttu-id="2b08f-163">Musí existovat zpráva o tom, že operace byla dokončena.</span><span class="sxs-lookup"><span data-stu-id="2b08f-163">There should be a message saying that the operation completed.</span></span>  
5. <span data-ttu-id="2b08f-164">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2b08f-164">Close the page.</span></span>


