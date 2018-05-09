---
title: "Přehled upgradu knihy odpisů"
description: "V předchozích verzích existovaly dva koncepty ocenění pro dlouhodobý majetek - oceňovací modely a knihy odpisů. V aplikaci Microsoft Dynamics 365 for Operations (1611) byly funkce modelu hodnoty a knihy odpisů sloučeny do jednoho koncept, který je označován jako kniha. Toto téma obsahuje informace, které je třeba zvážit pro upgrade."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7093023713a81980010b8254708801b58bc68475
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="depreciation-book-upgrade-overview"></a><span data-ttu-id="f5f94-105">Přehled upgradu knihy odpisů</span><span class="sxs-lookup"><span data-stu-id="f5f94-105">Depreciation book upgrade overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5f94-106">V předchozích verzích existovaly dva koncepty ocenění pro dlouhodobý majetek - oceňovací modely a knihy odpisů.</span><span class="sxs-lookup"><span data-stu-id="f5f94-106">In previous releases, there were two valuation concepts for fixed assets -  value models and depreciation books.</span></span> <span data-ttu-id="f5f94-107">V aplikaci Microsoft Dynamics 365 for Operations (1611) byly funkce modelu hodnoty a knihy odpisů sloučeny do jednoho koncept, který je označován jako kniha.</span><span class="sxs-lookup"><span data-stu-id="f5f94-107">In Microsoft Dynamics 365 for Operations (1611), the value model functionality and depreciation book functionality have been merged into a single concept that is known as a book.</span></span> <span data-ttu-id="f5f94-108">Toto téma obsahuje informace, které je třeba zvážit pro upgrade.</span><span class="sxs-lookup"><span data-stu-id="f5f94-108">This topic provides some things to consider for the upgrade.</span></span> 

<span data-ttu-id="f5f94-109">Proces upgradu přesune vaše existující nastavení a všechny existující transakce na novou účetní strukturu.</span><span class="sxs-lookup"><span data-stu-id="f5f94-109">The upgrade process will move your existing setup and all existing transactions to the new book structure.</span></span> <span data-ttu-id="f5f94-110">Oceňovací modely zůstanou, jaké momentálně jsou, tedy jako knihy, které se účtují do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="f5f94-110">Value models will remain as they currently are, as a book that posts to the general ledger.</span></span> <span data-ttu-id="f5f94-111">Knihy odpisů budou přesunuty do knihy, která má možnost **Zaúčtovat do hlavní knihy** nastavenu na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="f5f94-111">Depreciation books will be moved to a book that has the **Post to general ledger** option set to **No**.</span></span> <span data-ttu-id="f5f94-112">Názvy deníku knihy odpisů budou přesunuty do názvu deníku hlavní knihy s účtovací vrstvou nastavenou na **Žádná**.</span><span class="sxs-lookup"><span data-stu-id="f5f94-112">Depreciation book journal names will be moved to a general ledger journal name with the posting layer set to **None**.</span></span> <span data-ttu-id="f5f94-113">Transakce knihy odpisů budou přesunuty na transakce dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="f5f94-113">Depreciation book transactions will be moved to Fixed asset transactions.</span></span> 

<span data-ttu-id="f5f94-114">Před spuštěním upgradu dat byste se měli seznámit se dvěma možnostmi dostupnými pro upgradování řádku deníků knihy odpisů na transakční doklady a s číselnou řadou, která se bude používat pro řadu dokladů.</span><span class="sxs-lookup"><span data-stu-id="f5f94-114">Before running the data upgrade, you should understand the two options available for upgrading depreciation book journal lines to transaction vouchers, and the number sequence that will be used for the voucher series.</span></span> 

<span data-ttu-id="f5f94-115">Možnost 1:  **číselné řady definované systémem** – výchozí možnost pro optimalizaci výkonu upgradu.</span><span class="sxs-lookup"><span data-stu-id="f5f94-115">Option 1:  **System-defined number sequence** - This is the default option to optimize upgrade performance.</span></span> <span data-ttu-id="f5f94-116">Upgrade nebude používat systém číselných řad, ale namísto toho bude přidělovat doklady podle sad.</span><span class="sxs-lookup"><span data-stu-id="f5f94-116">The upgrade will not use the number sequences framework, but instead will allocate vouchers with a set-based approach.</span></span> <span data-ttu-id="f5f94-117">Po upgradu bude vytvořena nová číselná řada s **další sadou čísel** odpovídajícím způsobem na základě upgradovaných transakcí.</span><span class="sxs-lookup"><span data-stu-id="f5f94-117">After the upgrade, the new number sequence will be created with the **Next number set** appropriately based on the upgraded transactions.</span></span> <span data-ttu-id="f5f94-118">Použitá číselná řada bude ve výchozím nastavení ve formátu FADBUpgr\#\#\#\#\#\#\#\#\#.</span><span class="sxs-lookup"><span data-stu-id="f5f94-118">By default, the number sequence used will be in the FADBUpgr\#\#\#\#\#\#\#\#\# format.</span></span> <span data-ttu-id="f5f94-119">Při použití tohoto přístupu je k dispozici několik parametrů pro úpravu formátu:</span><span class="sxs-lookup"><span data-stu-id="f5f94-119">There are a few parameters available to you to adjust the format when using this approach:</span></span>

-   <span data-ttu-id="f5f94-120">**Kód číselné řady** – kód pro identifikaci číselné řady.</span><span class="sxs-lookup"><span data-stu-id="f5f94-120">**Number sequence code** – The code to identify the number sequence.</span></span> <span data-ttu-id="f5f94-121">Tento kód číselné řady nemůže existovat, protože bude vytvořen v upgradu.</span><span class="sxs-lookup"><span data-stu-id="f5f94-121">This number sequence code cannot exist since it will be created by the upgrade.</span></span>
    -   <span data-ttu-id="f5f94-122">Název konstanty: **NumberSequenceDefaultCode**</span><span class="sxs-lookup"><span data-stu-id="f5f94-122">Constant name: **NumberSequenceDefaultCode**</span></span>
    -   <span data-ttu-id="f5f94-123">Výchozí hodnota: "FADBUpgr"</span><span class="sxs-lookup"><span data-stu-id="f5f94-123">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="f5f94-124">**Předpona** – hodnota řetězce konstanty, která bude použita jako předpony čísla dokladů.</span><span class="sxs-lookup"><span data-stu-id="f5f94-124">**Prefix** – The constant string value that will be used as a prefix for the voucher numbers.</span></span>
    -   <span data-ttu-id="f5f94-125">Název konstanty: **NumberSequenceDefaultParameterPrefix**</span><span class="sxs-lookup"><span data-stu-id="f5f94-125">Constant name: **NumberSequenceDefaultParameterPrefix**</span></span>
    -   <span data-ttu-id="f5f94-126">Výchozí hodnota: "FADBUpgr"</span><span class="sxs-lookup"><span data-stu-id="f5f94-126">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="f5f94-127">**Délka alfanumerické řady** – délka alfanumerického segmentu číselné řady.</span><span class="sxs-lookup"><span data-stu-id="f5f94-127">**Alphanumeric length** – The length of the alphanumeric segment of the number sequence.</span></span>
    -   <span data-ttu-id="f5f94-128">Název konstanty: **NumberSequenceDefaultParameterAlpanumericLength **</span><span class="sxs-lookup"><span data-stu-id="f5f94-128">Constant name: **NumberSequenceDefaultParameterAlpanumericLength **</span></span>
    -   <span data-ttu-id="f5f94-129">Výchozí hodnota: 9</span><span class="sxs-lookup"><span data-stu-id="f5f94-129">Default value: 9</span></span>
-   <span data-ttu-id="f5f94-130">**Počáteční číslo** – první číslo pro použití v číselné řadě.</span><span class="sxs-lookup"><span data-stu-id="f5f94-130">**Start number** - The first number to be used in the number sequence.</span></span>
    -   <span data-ttu-id="f5f94-131">Název konstanty: **NumberSequenceDefaultParameterStartNumber  **</span><span class="sxs-lookup"><span data-stu-id="f5f94-131">Constant name: **NumberSequenceDefaultParameterStartNumber  **</span></span>
    -   <span data-ttu-id="f5f94-132">Výchozí hodnota: 1</span><span class="sxs-lookup"><span data-stu-id="f5f94-132">Default value: 1</span></span>

<span data-ttu-id="f5f94-133">Možnost 2: **Existující uživatelem definovaná číselná řada** – tato možnost vám umožní definovat číselnou řadu, která má být použita pro upgrade.</span><span class="sxs-lookup"><span data-stu-id="f5f94-133">Option 2: **Existing user-defined number sequence** - This option will allow you to define the number sequence to be used for the upgrade.</span></span> <span data-ttu-id="f5f94-134">Zvažte použití této možnosti, pokud potřebujete pokročilou konfiguraci číselné řady.</span><span class="sxs-lookup"><span data-stu-id="f5f94-134">Consider using this option if you need advanced number sequence configuration.</span></span> <span data-ttu-id="f5f94-135">Pokud chcete použít číselnou řadu, je nutné změnit třídu pro upgrade ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans pomocí následujících informací</span><span class="sxs-lookup"><span data-stu-id="f5f94-135">To use a number sequence, you must modify the upgrade class ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans with the following information:</span></span>

-   <span data-ttu-id="f5f94-136">**Kód číselné řady** – kód číselné řady.</span><span class="sxs-lookup"><span data-stu-id="f5f94-136">**Number sequence code** – The code of the number sequence.</span></span>
    -   <span data-ttu-id="f5f94-137">Název konstanty: **NumberSequenceExistingCode **</span><span class="sxs-lookup"><span data-stu-id="f5f94-137">Constant name: **NumberSequenceExistingCode **</span></span>
    -   <span data-ttu-id="f5f94-138">Výchozí hodnota: žádná výchozí hodnota, musíte aktualizovat na kód číselné řady.</span><span class="sxs-lookup"><span data-stu-id="f5f94-138">Default value: No default, this must be updated to the number sequence code.</span></span>
-   <span data-ttu-id="f5f94-139">**Sdílená číselná řada** – logická hodnota k identifikaci v rámci číselné řady.</span><span class="sxs-lookup"><span data-stu-id="f5f94-139">**Shared number sequence** – A boolean value to identify the scope of the number sequence.</span></span> <span data-ttu-id="f5f94-140">Pro sdílené číselné řady ve všech společnostech použijte hodnotu true a pro rozsah specifický pro společnost hodnotu false.</span><span class="sxs-lookup"><span data-stu-id="f5f94-140">Use "true" for shared number sequences across all companies, and "false" for a company-specific scope.</span></span> <span data-ttu-id="f5f94-141">Použijete-li false, číselná řada se zadaným názvem musí existovat v každé společnosti, která obsahuje transakce knihy odpisů.</span><span class="sxs-lookup"><span data-stu-id="f5f94-141">When using "false", the number sequence with the specified name must exist in every company that contains depreciation book transactions.</span></span> <span data-ttu-id="f5f94-142">Sdílené číselné řady existují v každém oddílu obsahujícím transakce knihy odpisů.</span><span class="sxs-lookup"><span data-stu-id="f5f94-142">Shared number sequences exist in every partition that contains depreciation book transactions.</span></span>
    -   <span data-ttu-id="f5f94-143">Název konstanty: **NumberSequenceExistingIsShared **</span><span class="sxs-lookup"><span data-stu-id="f5f94-143">Constant name: **NumberSequenceExistingIsShared **</span></span>
    -   <span data-ttu-id="f5f94-144">Výchozí hodnota: true</span><span class="sxs-lookup"><span data-stu-id="f5f94-144">Default value: true</span></span>

<span data-ttu-id="f5f94-145">Parametry jsou umístěny na začátku třídy ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="f5f94-145">The parameters are located at the beginning of the ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans class.</span></span> 

<span data-ttu-id="f5f94-146">*//Určete preferovanou metodu přidělení dokladů* 
 *// true, pokud chcete použít existující kód číselné řady* 
 *// false, chcete-li použití číselnou řadu (výchozí) definovanou systémem* boolean const NumberSequenceUseExistingCode = false;</span><span class="sxs-lookup"><span data-stu-id="f5f94-146">*// Specify a preferable approach of vouchers allocation* 
 *// true, if you want to use an existing number sequence code* 
 *// false, if you intend to use the system-defined number sequence (default)* const boolean NumberSequenceUseExistingCode = false;</span></span>  

<span data-ttu-id="f5f94-147">*// Pokud použijete způsob definované systémem číselné řady, zadejte parametry pro číselnou řadu.*
 *// Vytvoří se nová číselná řada s těmito parametry.*</span><span class="sxs-lookup"><span data-stu-id="f5f94-147">*// If using the system-defined number sequence approach, specify the parameters for the number sequence.*
 *// A new number sequence will be created with these parameters.*</span></span> <span data-ttu-id="f5f94-148">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span><span class="sxs-lookup"><span data-stu-id="f5f94-148">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span></span>   

<span data-ttu-id="f5f94-149">*// Používáte-li přístup existující číselné řady, zadejte existující kód číselné řady..* 
 *// Přidělení dokladu půjde po řádcích existující číselné řady.*</span><span class="sxs-lookup"><span data-stu-id="f5f94-149">*// If using the existing number sequence approach, specify the existing number sequence code.* 
 *// Voucher allocation will go row-by-row for existing number sequences.*</span></span> <span data-ttu-id="f5f94-150">const str NumberSequenceExistingCode = ''; *// Zadejte identifikační kód pro číselnou řadu.* 
 *// true, pokud je sdílená určená číselné řada* 
 *// false, pokud je určená číselná řada podle společnosti* 
 *// Výchozí číselná řada definovaná systémem se použije, pokud nebude nalezen kód číselné řady se zadaným rozsahem.*</span><span class="sxs-lookup"><span data-stu-id="f5f94-150">const str NumberSequenceExistingCode = ''; *// Specify the scope of the existing number sequence code* 
 *// true, if the specified number sequence is shared* 
 *// false, if the specified number sequence is per-company* 
 *// The default system-defined number sequence will be used if a number sequence code with the specified scope is not found.*</span></span> <span data-ttu-id="f5f94-151">const boolean NumberSequenceExistingIsShared = true;</span><span class="sxs-lookup"><span data-stu-id="f5f94-151">const boolean NumberSequenceExistingIsShared = true;</span></span> 

<span data-ttu-id="f5f94-152">Znovu vytvořte projekt obsahující třídu po změně konstant.</span><span class="sxs-lookup"><span data-stu-id="f5f94-152">Rebuild the project that contains the class after the constants have been modified.</span></span> 

<span data-ttu-id="f5f94-153">Používáte-li přístup generování číselné řady (možnost 1), bude při upgradu použito zpracování založené na sadě k přidělení čísel dokladů, jak je uvedeno v parametrech skriptu pro upgrade.</span><span class="sxs-lookup"><span data-stu-id="f5f94-153">When using the system-generated number sequence approach (option 1), the upgrade will use set-based processing to allocate the voucher numbers as specified in the upgrade script parameters.</span></span> <span data-ttu-id="f5f94-154">Dále bude vytvořena nová číselná řadu se zadanými parametry po přidělení.</span><span class="sxs-lookup"><span data-stu-id="f5f94-154">It will also create a new number sequence with specified parameters after the allocation.</span></span> 

<span data-ttu-id="f5f94-155">Používáte-li přístup vytvoření vlastní existující číselné řady (možnost 2), upgrade dat zkontroluje, zda existuje číselná řada s se zadaným rozsahem v databázi pro každý oddíl a společnost s transakcemi knihy odpisů.</span><span class="sxs-lookup"><span data-stu-id="f5f94-155">When using the user-defined existing number sequence approach (option 2), the data upgrade checks whether the number sequence with the specified scope exists in the database for each partition and company with depreciation book transactions.</span></span> <span data-ttu-id="f5f94-156">Pokud existuje, bude při upgradu použito zpracování po řádcích k přidělení čísel dokladů podle číselné řady pomocí rámce číselné řady.</span><span class="sxs-lookup"><span data-stu-id="f5f94-156">If it does exist, the upgrade will use row-by-row processing to allocate the voucher numbers as specified by the number sequence using the number sequence framework.</span></span> <span data-ttu-id="f5f94-157">Pokud číselná řada neexistuje se zadaným oborem, upgrade bude používat výchozí systémem definovaný přístup číselné řady pro přidělení čísel dokladů a vytvoří novou číselnou řadu se zadanými výchozími parametry po přidělení.</span><span class="sxs-lookup"><span data-stu-id="f5f94-157">If the number sequence does not exist with the specified scope, the upgrade will use the default system-defined number sequence approach to allocate the voucher numbers, and will create a new number sequence with specified default parameters after the allocation.</span></span>

<span data-ttu-id="f5f94-158">S každým přístupem bude skript pro upgrade dat používat také číselnou řadu pro pole **Řada dokladů** v nových názvech deníku hlavní knihy vytvořených pro dřívější názvy deníku knihy odpisů.</span><span class="sxs-lookup"><span data-stu-id="f5f94-158">With either approach, the data upgrade script will also use the number sequence for the **Voucher series** field on the new general ledger journal names created for the former depreciation book journal names.</span></span>




