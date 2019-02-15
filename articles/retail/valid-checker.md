---
title: Kontrola konzistence maloobchodních transakcí
description: Toto téma popisuje funkci kontroly konzistence maloobchodních transakcí v aplikaci Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: db01a12b92574b41f1f4fe7281c23992e0d36027
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "302023"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="e98ed-103">Kontrola konzistence maloobchodních transakcí</span><span class="sxs-lookup"><span data-stu-id="e98ed-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="e98ed-104">Toto téma popisuje funkci kontroly konzistence maloobchodních transakcí uvedenou v aplikaci Microsoft Dynamics 365 for Finance and Operations, verze 8.1.3.</span><span class="sxs-lookup"><span data-stu-id="e98ed-104">This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</span></span> <span data-ttu-id="e98ed-105">Kontrola konzistence identifikuje a izoluje nekonzistentní transakce před tím, než se dostanou k procesu zaúčtování výkazů.</span><span class="sxs-lookup"><span data-stu-id="e98ed-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="e98ed-106">Při zaúčtování výkazu v aplikaci Retail může zaúčtování selhat kvůli nekonzistentním datům v tabulkách maloobchodních transakcí.</span><span class="sxs-lookup"><span data-stu-id="e98ed-106">When a statement is posted in Retail, posting can fail due to inconsistent data in the retail transaction tables.</span></span> <span data-ttu-id="e98ed-107">Problém s daty může být způsoben nepředvídanými potížemi v aplikaci Point of Sale (POS), nebo tím, že transakce byly nesprávně naimportovány z POS systémů třetích stran.</span><span class="sxs-lookup"><span data-stu-id="e98ed-107">The data issue may be caused by by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="e98ed-108">Příklady toho, jak mohou tyto nekonzistence vypadat, zahrnují:</span><span class="sxs-lookup"><span data-stu-id="e98ed-108">Examples of how these inconsistencies may appear include:</span></span> 

  - <span data-ttu-id="e98ed-109">Celková částka transakce v tabulce záhlaví neodpovídá celkové částce transakce na řádcích.</span><span class="sxs-lookup"><span data-stu-id="e98ed-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
  - <span data-ttu-id="e98ed-110">Počet řádků v tabulce záhlaví neodpovídá počtu řádků v tabulce transakcí.</span><span class="sxs-lookup"><span data-stu-id="e98ed-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
  - <span data-ttu-id="e98ed-111">Daně v tabulce záhlaví neodpovídají celkové částce daně na řádcích.</span><span class="sxs-lookup"><span data-stu-id="e98ed-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 
  
<span data-ttu-id="e98ed-112">Když jsou nekonzistentní transakce přejaty procesem zaúčtování výkazů, vytvoří se nekonzistentní prodejní faktury a deníky plateb, následkem čehož celý proces zaúčtování výkazu selže.</span><span class="sxs-lookup"><span data-stu-id="e98ed-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="e98ed-113">Obnovení výkazů z takového stavu představuje složité opravy dat napříč mnoha tabulkami transakcí.</span><span class="sxs-lookup"><span data-stu-id="e98ed-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="e98ed-114">Kontrola konzistence maloobchodních transakcí těmto problémům zabraňuje.</span><span class="sxs-lookup"><span data-stu-id="e98ed-114">The retail transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="e98ed-115">Následujíc tabulka znázorňuje proces zaúčtování s kontrolou konzistence transakcí.</span><span class="sxs-lookup"><span data-stu-id="e98ed-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="e98ed-116">![Proces zaúčtování výkazu s kontrolou konzistence transakcí](./media/validchecker.png "Proces zaúčtování výkazu s kontrolou konzistence transakcí")</span><span class="sxs-lookup"><span data-stu-id="e98ed-116">![Statement posting process with retail transaction consistency checker](./media/validchecker.png "Statement posting process with retail transsaction consistency checker")</span></span>

<span data-ttu-id="e98ed-117">Dávkové zpracování **Ověřit transakce obchodu** kontroluje konzistenci tabulek maloobchodních transakcí pro následující scénáře:</span><span class="sxs-lookup"><span data-stu-id="e98ed-117">The **Validate store transactions** batch process checks the consistency of the retail transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="e98ed-118">Účet odběratele - Ověřuje, že účet odběratele existuje v tabulce maloobchodních transakcí v HQ hlavních datech odběratele.</span><span class="sxs-lookup"><span data-stu-id="e98ed-118">Customer account - Validates that the customer account in the retail transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="e98ed-119">Počet řádků - Ověřuje, že počet řádků, jak je zaznamenaný v tabulce záhlaví transakcí, odpovídá počtu řádků v tabulce prodejních transakcí.</span><span class="sxs-lookup"><span data-stu-id="e98ed-119">Line count - Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="e98ed-120">Nastavení kontroly konzistence</span><span class="sxs-lookup"><span data-stu-id="e98ed-120">Set up the consistency checker</span></span>
<span data-ttu-id="e98ed-121">Nakonfigurujte dávkové zpracování „Ověřit transakce obchodu“ pro periodická spuštění pomocí možností **Maloobchod \> IT pro maloobchod \> Zaúčtování POS**.</span><span class="sxs-lookup"><span data-stu-id="e98ed-121">Configure the "Validate store transactions" batch process, at **Retail \> Retail IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="e98ed-122">Dávkovou úlohu lze naplánovat na základě hierarchie organizace obchodu, podobným způsobem, jakým se nastavují zpracování „Vypočítat příkazy v dávkách“ a „Zaúčtovat příkazy v dávkách“.</span><span class="sxs-lookup"><span data-stu-id="e98ed-122">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="e98ed-123">Doporučujeme, abyste nakonfigurovali toto dávkové zpracování tak, aby se spouštělo několikrát denně, a naplánovali jeho spuštění na konec každého provedení úlohy P.</span><span class="sxs-lookup"><span data-stu-id="e98ed-123">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="e98ed-124">Výsledky procesu ověření</span><span class="sxs-lookup"><span data-stu-id="e98ed-124">Results of validation process</span></span>
<span data-ttu-id="e98ed-125">Výsledky procesu ověření podle dávkového zpracování jsou označeny na příslušné maloobchodní transakci.</span><span class="sxs-lookup"><span data-stu-id="e98ed-125">The results of the validation check by the batch process are tagged on the appropriate retail transaction.</span></span> <span data-ttu-id="e98ed-126">Pole **Stav ověření** na záznamu maloobchodní transakce je buď nastaveno na **Úspěšný** nebo **Chyba** a datum posledního spuštění ověření se zobrazí v poli **Poslední čas ověření**.</span><span class="sxs-lookup"><span data-stu-id="e98ed-126">The **Validation status** field on the retail transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="e98ed-127">Chcete-li zobrazit popisnější text chyby související se selháním ověření, zvolte příslušný záznam maloobchodní transakce a klikněte na tlačítko **Chyby ověřování**.</span><span class="sxs-lookup"><span data-stu-id="e98ed-127">To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="e98ed-128">Transakce, u kterých se nezdaří kontrola ověření, a transakce, které ještě nebyly ověřeny, nebudou publikovány do výkazů.</span><span class="sxs-lookup"><span data-stu-id="e98ed-128">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="e98ed-129">Během procesu „Vypočítat výkaz“ budou uživatelé upozorněni, pokud existují transakce, které mohly být zahrnuty ve výkazu, ale nebyly.</span><span class="sxs-lookup"><span data-stu-id="e98ed-129">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="e98ed-130">Pokud je nalezena chyba ověření, jediným způsobem její opravy je kontaktování podpory Microsoft Support.</span><span class="sxs-lookup"><span data-stu-id="e98ed-130">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="e98ed-131">V dalších verzích bude přidána funkce, aby mohli uživatelé opravit nepodařené záznamy prostřednictvím uživatelského rozhraní.</span><span class="sxs-lookup"><span data-stu-id="e98ed-131">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="e98ed-132">Rovněž budou zpřístupněny funkce protokolování a auditu pro sledování historie úprav.</span><span class="sxs-lookup"><span data-stu-id="e98ed-132">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="e98ed-133">V budoucích verzích bude přidáno více pravidel ověření pro podporu více scénářů.</span><span class="sxs-lookup"><span data-stu-id="e98ed-133">Additional validation rules to support more scenarios will be added in a future release.</span></span>
