---
title: Registrace položek pro položky umožňující pokročilé uskladnění s použitím deníku doručení zboží
description: Tohle téma popisuje postup, jak zaregistrovat položky pomocí deníku doručení položek, když použijete pokročilé postupy řízení skladu.
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c58aa1cec6c0bfe33fa1ef90267dcd8ac1218157
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830827"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="d2cea-103">Registrace položek pro položky umožňující pokročilé uskladnění s použitím deníku doručení zboží</span><span class="sxs-lookup"><span data-stu-id="d2cea-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d2cea-104">Tohle téma popisuje postup, jak zaregistrovat položky pomocí deníku doručení položek, když použijete pokročilé postupy řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="d2cea-104">This topic presents a scenario that shows how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="d2cea-105">To obvykle provádí přijímající pracovník.</span><span class="sxs-lookup"><span data-stu-id="d2cea-105">This would usually be done by a receiving clerk.</span></span>

## <a name="enable-sample-data"></a><span data-ttu-id="d2cea-106">Povolit ukázková data</span><span class="sxs-lookup"><span data-stu-id="d2cea-106">Enable sample data</span></span>

<span data-ttu-id="d2cea-107">Chcete-li projít tímto scénářem pomocí ukázkových záznamů a hodnot uvedených v tomto tématu, musíte používat systém, ve kterém jsou nainstalována standardní ukázková data, a než začnete, musíte vybrat právnickou osobu *USMF*.</span><span class="sxs-lookup"><span data-stu-id="d2cea-107">To work through this scenario using the sample records and values specified in this topic, you must be using a system where the standard demo data is installed, and you must select the *USMF* legal entity before you begin.</span></span>

<span data-ttu-id="d2cea-108">Místo toho můžete projít tímto scénářem nahrazením hodnot ze svých vlastních dat za předpokladu, že máte k dispozici následující data:</span><span class="sxs-lookup"><span data-stu-id="d2cea-108">You can instead work through this scenario by substituting values from your own data provided that you have the following data available:</span></span>

- <span data-ttu-id="d2cea-109">Musíte mít potvrzenou nákupní objednávku s otevřeným řádkem nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="d2cea-109">You must have a confirmed purchase order with an open purchase order line.</span></span>
- <span data-ttu-id="d2cea-110">Položka na řádku musí být na skladě.</span><span class="sxs-lookup"><span data-stu-id="d2cea-110">The item on the line must be stocked.</span></span> <span data-ttu-id="d2cea-111">Nesmí používat varianty produktu a nesmí mít sledovací dimenze.</span><span class="sxs-lookup"><span data-stu-id="d2cea-111">It must not use product variants, and must not have tracking dimensions.</span></span>
- <span data-ttu-id="d2cea-112">Položka musí být přidružena ke skupině dimenzí úložiště, která má povolen proces řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="d2cea-112">The item must be associated with a storage dimension group that has warehouse management process enabled.</span></span>
- <span data-ttu-id="d2cea-113">Sklad, který se používá, musí být povolen pro procesy správy skladu a umístění, které používáte pro příjem, musí být řízeno registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="d2cea-113">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span>

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a><span data-ttu-id="d2cea-114">Vytvoření záhlaví deníku pro doručení položky, které používá řízení skladu</span><span class="sxs-lookup"><span data-stu-id="d2cea-114">Create an item arrival journal header that uses warehouse management</span></span>

<span data-ttu-id="d2cea-115">Následující scénář ukazuje, jak vytvořit záhlaví deníku pro doručení položky, která používá řízení skladu:</span><span class="sxs-lookup"><span data-stu-id="d2cea-115">The following scenario shows how to create an item arrival journal header that uses warehouse management:</span></span>

1. <span data-ttu-id="d2cea-116">Ujistěte se, že váš systém obsahuje potvrzenou nákupní objednávku, která splňuje požadavky uvedené v předchozí části.</span><span class="sxs-lookup"><span data-stu-id="d2cea-116">Make sure your system contains a confirmed purchase order that fulfils the requirements outlined in the previous section.</span></span> <span data-ttu-id="d2cea-117">Tento scénář používá nákupní objednávku pro společnost *USMF*, účet dodavatele *1001*, sklad *51* s řádkem objednávky pro *10 PL* (10 palet) čísla položky *M9200*.</span><span class="sxs-lookup"><span data-stu-id="d2cea-117">This scenario uses a purchase order for company *USMF*, vendor account *1001*, warehouse *51*, with an order line for *10 PL* (10 pallets) of item number *M9200*.</span></span>
1. <span data-ttu-id="d2cea-118">Poznamenejte si číslo nákupní objednávky, které ještě použijete.</span><span class="sxs-lookup"><span data-stu-id="d2cea-118">Make a note of the purchase order number that you will use.</span></span>
1. <span data-ttu-id="d2cea-119">Přejděte na **Řízení zásob \> Položky deníku \> Doručení položky \> Doručení položky**.</span><span class="sxs-lookup"><span data-stu-id="d2cea-119">Go to **Inventory management \> Journal entries \> Item arrival \> Item arrival**.</span></span>
1. <span data-ttu-id="d2cea-120">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d2cea-120">Select **New** on the Action Pane.</span></span>
1. <span data-ttu-id="d2cea-121">Otevře se dialogové okno **Vytvoření deníku řízení skladu**.</span><span class="sxs-lookup"><span data-stu-id="d2cea-121">The **Create warehouse management journal** dialog box opens.</span></span> <span data-ttu-id="d2cea-122">V poli **Název** vyberte název deníku.</span><span class="sxs-lookup"><span data-stu-id="d2cea-122">Select a journal name in the **Name** field.</span></span>
    - <span data-ttu-id="d2cea-123">Používáte-li ukázková data *USMF* vyberte hodnotu *WHS*.</span><span class="sxs-lookup"><span data-stu-id="d2cea-123">If you are using *USMF* sample data, select *WHS*.</span></span>
    - <span data-ttu-id="d2cea-124">Pokud používáte svá vlastní data, deník, který vyberete, musí mít parametr **Zkontrolovat výdejní skl. místo** nastaven na *Ne* a **Řízení karantény** na *Ne*.</span><span class="sxs-lookup"><span data-stu-id="d2cea-124">If you're using your own data, the journal you choose must have **Check picking location** set to *No* and **Quarantine management** set to *No*.</span></span>
1. <span data-ttu-id="d2cea-125">Nastavte **Odkaz** na *Nákupní objednávka*.</span><span class="sxs-lookup"><span data-stu-id="d2cea-125">Set **Reference** to *Purchase order*.</span></span>
1. <span data-ttu-id="d2cea-126">Nastavte **Číslo účtu** na *1001*.</span><span class="sxs-lookup"><span data-stu-id="d2cea-126">Set **Account number** to *1001*.</span></span>
1. <span data-ttu-id="d2cea-127">Nastavte **Číslo** na číslo nákupní objednávky, které jste identifikovali pro toto cvičení.</span><span class="sxs-lookup"><span data-stu-id="d2cea-127">Set **Number** to the number of the purchase order that you identified for this exercise.</span></span>

    <span data-ttu-id="d2cea-128">![Deník doručení položky](../media/item-arrival-journal-header.png "Deník doručení položky")</span><span class="sxs-lookup"><span data-stu-id="d2cea-128">![Item arrival journal](../media/item-arrival-journal-header.png "Item arrival journal")</span></span>

1. <span data-ttu-id="d2cea-129">Vyberte **OK** k vytvoření záhlaví deníku.</span><span class="sxs-lookup"><span data-stu-id="d2cea-129">Select the **OK** to create the journal header.</span></span>
1. <span data-ttu-id="d2cea-130">V sekci **Řádky deníku** vyberte **Přidat řádek** a zadejte následující údaje:</span><span class="sxs-lookup"><span data-stu-id="d2cea-130">In the **Journal lines** section, select **Add line** and enter the following data:</span></span>
    - <span data-ttu-id="d2cea-131">**Číslo položky** – nastavte na *M9200*.</span><span class="sxs-lookup"><span data-stu-id="d2cea-131">**Item number** – Set to *M9200*.</span></span> <span data-ttu-id="d2cea-132">**Lokalita**, **Sklad** a **Množství** se nastaví na základě údajů o transakcích zásob pro 10 palet (1000 kusů).</span><span class="sxs-lookup"><span data-stu-id="d2cea-132">The **Site**, **Warehouse**, and **Quantity** will get set based on the inventory transaction data for the 10 pallets (1000 ea.).</span></span>
    - <span data-ttu-id="d2cea-133">**Umístění** – Nastavte na *001*.</span><span class="sxs-lookup"><span data-stu-id="d2cea-133">**Location** – Set to  *001*.</span></span> <span data-ttu-id="d2cea-134">Toto konkrétní umístění nesleduje registrační značky.</span><span class="sxs-lookup"><span data-stu-id="d2cea-134">This specific location does not track license plates.</span></span>

    <span data-ttu-id="d2cea-135">![Řádek deníku pro doručení položky](../media/item-arrival-journal-line.png "Řádek deníku pro doručení položky")</span><span class="sxs-lookup"><span data-stu-id="d2cea-135">![Item arrival journal line](../media/item-arrival-journal-line.png "Item arrival journal line")</span></span>

    > [!NOTE]
    > <span data-ttu-id="d2cea-136">Pole **Datum** určuje datum, kdy bude na skladě registrováno množství této položky.</span><span class="sxs-lookup"><span data-stu-id="d2cea-136">The **Date** field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    >
    > <span data-ttu-id="d2cea-137">**ID šarže** bude vyplněno systémem, pokud může být jedinečně identifikováno z uvedených informací.</span><span class="sxs-lookup"><span data-stu-id="d2cea-137">The **Lot ID** will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="d2cea-138">V opačném případě bude nutné jej zadat ručně.</span><span class="sxs-lookup"><span data-stu-id="d2cea-138">Otherwise you will have to enter this manually.</span></span> <span data-ttu-id="d2cea-139">Toto je povinné pole, které propojí tuto registraci k řádku konkrétního zdrojového dokumentu.</span><span class="sxs-lookup"><span data-stu-id="d2cea-139">This is a required field, which links this registration to a specific source document line.</span></span>  

1. <span data-ttu-id="d2cea-140">V podokně Akce klikněte na možnost **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="d2cea-140">Select **Validate** on the Action Pane.</span></span> <span data-ttu-id="d2cea-141">To kontroluje, zda je deník připraven k zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="d2cea-141">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="d2cea-142">Jestliže se ověření nezdaří, které bude nutné před zaúčtováním deníku opravit chyby.</span><span class="sxs-lookup"><span data-stu-id="d2cea-142">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
1. <span data-ttu-id="d2cea-143">Otevře se dialogové okno **Kontrola deníku**.</span><span class="sxs-lookup"><span data-stu-id="d2cea-143">The **Check journal** dialog box opens.</span></span> <span data-ttu-id="d2cea-144">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2cea-144">Select **OK**.</span></span>
1. <span data-ttu-id="d2cea-145">Prohlédněte si panel zpráv.</span><span class="sxs-lookup"><span data-stu-id="d2cea-145">Review the message bar.</span></span> <span data-ttu-id="d2cea-146">Měla by se na něm nacházet zpráva že operace byla dokončena.</span><span class="sxs-lookup"><span data-stu-id="d2cea-146">There should be a message denoting that the operation was completed.</span></span>  
1. <span data-ttu-id="d2cea-147">V podokně akcí zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="d2cea-147">Select **Post** on the Action Pane.</span></span>
1. <span data-ttu-id="d2cea-148">Otevře se dialogové okno **Zaúčtování deníku**.</span><span class="sxs-lookup"><span data-stu-id="d2cea-148">The **Post journal** dialog box opens.</span></span> <span data-ttu-id="d2cea-149">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2cea-149">Select **OK**.</span></span>
1. <span data-ttu-id="d2cea-150">Prohlédněte si panel zpráv.</span><span class="sxs-lookup"><span data-stu-id="d2cea-150">Review the message bar.</span></span> <span data-ttu-id="d2cea-151">Měli byste vidět zprávu, že operace byla dokončena.</span><span class="sxs-lookup"><span data-stu-id="d2cea-151">There should be messages denoting that the operation completed.</span></span>
1. <span data-ttu-id="d2cea-152">Vyberte **Funkce > Příjem produktu** v podokně akcí, čímž aktualizujete řádek nákupní objednávky a zaúčtujte příjemku produktu.</span><span class="sxs-lookup"><span data-stu-id="d2cea-152">Select **Functions > Product receipt** on the Action Pane to update the purchase order line and post a product receipt.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
