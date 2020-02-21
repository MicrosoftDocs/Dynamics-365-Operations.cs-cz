---
title: Úprava a audit transakcí maloobchodu
description: V tomto tématu je popsána funkce pro úpravy a audit transakcí obchodu.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
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
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 97211ee36dbaa704d3a967e9b742ff1cae708707
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004382"
---
# <a name="edit-and-audit-retail-store-transactions"></a><span data-ttu-id="1ec52-103">Úprava a audit transakcí maloobchodu</span><span class="sxs-lookup"><span data-stu-id="1ec52-103">Edit and audit retail store transactions</span></span>

[!include [banner](includes/banner.md)]



<span data-ttu-id="1ec52-104">Zákazníci Dynamics 365 Commerce používají aplikace prvních stran, stejně jako pokladní místo (POS) třetích stran.</span><span class="sxs-lookup"><span data-stu-id="1ec52-104">Dynamics 365 Commerce customers use first-party as well as third-party point of sale (POS) applications.</span></span> <span data-ttu-id="1ec52-105">V aplikaci POS první strany jsou transakce obchodu načteny do Headquarters z kanálů pomocí dávkového zpracování.</span><span class="sxs-lookup"><span data-stu-id="1ec52-105">With the first-party POS application, store transactions are pulled into Headquarters from the channels through a batch process.</span></span> <span data-ttu-id="1ec52-106">U aplikací třetích stran jsou transakce načítány do Headquarters pomocí integrace.</span><span class="sxs-lookup"><span data-stu-id="1ec52-106">With third-party applications, transactions are pulled into Headquarters through integration.</span></span> <span data-ttu-id="1ec52-107">V obou případech, po načtení transakcí do Headquarters, je nutné spustit proces kontroly konzistence, který spustí více ověření na transakcích tak, aby do výkazu, který má být zaúčtován v Headquarters, byly načteny pouze úspěšně ověřené transakce.</span><span class="sxs-lookup"><span data-stu-id="1ec52-107">In both cases, after transactions are pulled into Headquarters, a consistency check process needs to be executed that runs multiple validations on the transactions so that only successfully validated transactions are pulled into the statement to be posted in Headquarters.</span></span> 

<span data-ttu-id="1ec52-108">Transakce obchodu se nedaří ověřit z různých důvodů.</span><span class="sxs-lookup"><span data-stu-id="1ec52-108">Commerce transactions fail validation for various reasons.</span></span> <span data-ttu-id="1ec52-109">Například chyba v integračním kódu nebo chyba v aplikaci POS může způsobit nekonzistentní data. Nebo chyba uživatele, například odstranění produktu po synchronizaci s kanálem nebo uzavření fiskálního období bez zaúčtování transakcí za toto období, může způsobit nekonzistentní data.</span><span class="sxs-lookup"><span data-stu-id="1ec52-109">For example, a bug in the integration code or a bug in the POS application may cause inconsistent data, or a user error, such as deleting a product after it was synchronized to the channel or closing a fiscal period without posting transactions for that period, can cause inconsistent data.</span></span>

<span data-ttu-id="1ec52-110">Zatímco tyto transakce jsou označeny a vyloučeny z výkazů, mohou transakce rušit každodenní zákazníkův proces zaúčtování denního prodeje do financí.</span><span class="sxs-lookup"><span data-stu-id="1ec52-110">While these transactions get flagged and are excluded from the statements, the transactions can disrupt a customer’s daily process of posting daily sales to the financials.</span></span>

<span data-ttu-id="1ec52-111">V aplikaci Commerce můžete upravit konkrétní transakce, jejichž ověření se nezdařilo při zachování auditu všech změn.</span><span class="sxs-lookup"><span data-stu-id="1ec52-111">In Commerce, you can edit the specific transactions that fail validation while maintaining audit of all the changes.</span></span> 

## <a name="edit-and-audit-transactions"></a><span data-ttu-id="1ec52-112">Úprava a audit transakcí</span><span class="sxs-lookup"><span data-stu-id="1ec52-112">Edit and audit transactions</span></span>

<span data-ttu-id="1ec52-113">Ve verzi 10.0.5 aplikace Retail jsou transakce cash and carry, jako prodej a vrácení, jediné transakce, které lze upravit.</span><span class="sxs-lookup"><span data-stu-id="1ec52-113">In Retail version 10.0.5, cash and carry transactions like sales and returns are the only transactions that can be edited.</span></span> <span data-ttu-id="1ec52-114">Úprava objednávek zákazníků nebo online objednávek není podporována.</span><span class="sxs-lookup"><span data-stu-id="1ec52-114">Editing customer orders or online orders is not supported.</span></span> <span data-ttu-id="1ec52-115">V aplikaci Retail verze 10.0.6 a vyšších jsou také podporovány úpravy transakcí správy hotovosti.</span><span class="sxs-lookup"><span data-stu-id="1ec52-115">In Retail version 10.0.6 and higher, editing cash management transactions is also supported.</span></span>

1. <span data-ttu-id="1ec52-116">Nainstalujte doplněk Dynamics Excel.</span><span class="sxs-lookup"><span data-stu-id="1ec52-116">Install the Dynamics Excel Add-in.</span></span>

2. <span data-ttu-id="1ec52-117">Přejděte do pracovního prostoru **Finance obchodu**.</span><span class="sxs-lookup"><span data-stu-id="1ec52-117">Go to the **Store financials** workspace.</span></span> <span data-ttu-id="1ec52-118">Dlaždice **Selhání ověření transakcí** obsahuje předfiltrované zobrazení formuláře transakcí, u kterého se nezdařilo jedno nebo více pravidel ověření.</span><span class="sxs-lookup"><span data-stu-id="1ec52-118">The **Transaction validation failures** tile provides a pre-filtered view of the transaction form that failed one or more of the validation rules.</span></span>
 
3. <span data-ttu-id="1ec52-119">Otevřete formulář.</span><span class="sxs-lookup"><span data-stu-id="1ec52-119">Open the form.</span></span> <span data-ttu-id="1ec52-120">Klikněte na záznam, jehož ověření se nezdařilo, klikněte na **Doplněk Office** a pak klikněte na **Upravit zvolenou transakci**.</span><span class="sxs-lookup"><span data-stu-id="1ec52-120">Click the record that failed validation, click **Office Add in**, and then click **Edit selected transaction**.</span></span> <span data-ttu-id="1ec52-121">Otevře se soubor aplikace Excel s podrobnostmi vybrané transakce s následujícími listy:</span><span class="sxs-lookup"><span data-stu-id="1ec52-121">An Excel file with the details of the selected transaction opens, with the following worksheets:</span></span>

    - <span data-ttu-id="1ec52-122">Řádky: Tento list obsahuje záhlaví a řádky produktu a související data transakce.</span><span class="sxs-lookup"><span data-stu-id="1ec52-122">Lines: This worksheet has the header and product lines and related data for the transaction.</span></span>
    - <span data-ttu-id="1ec52-123">Platby: Tento list obsahuje podrobnosti o řádcích platby dané transakce.</span><span class="sxs-lookup"><span data-stu-id="1ec52-123">Payments: This worksheet has the details of the payment lines for the transaction.</span></span>
    - <span data-ttu-id="1ec52-124">Slevy: Tento list obsahuje podrobnosti transakce související se slevami.</span><span class="sxs-lookup"><span data-stu-id="1ec52-124">Discounts: This worksheet has the discount-related details for the transaction.</span></span>
    - <span data-ttu-id="1ec52-125">Daně: Tento list obsahuje podrobnosti transakce související s daněmi.</span><span class="sxs-lookup"><span data-stu-id="1ec52-125">Taxes: This worksheet has the tax-related details for the transaction.</span></span>
    - <span data-ttu-id="1ec52-126">Náklady: Tento list obsahuje data transakce související s náklady.</span><span class="sxs-lookup"><span data-stu-id="1ec52-126">Charges: This worksheet has the charges-related data for the transaction.</span></span>

4. <span data-ttu-id="1ec52-127">V souboru aplikace Excel upravte příslušná pole a poté odešlete data zpět do Headquarters pomocí funkce publikování doplňku Dynamics Excel.</span><span class="sxs-lookup"><span data-stu-id="1ec52-127">In the Excel file, you modify the appropriate fields and then upload the data back into Headquarters using the Dynamics Excel Add-in publish functionality.</span></span> <span data-ttu-id="1ec52-128">Po publikování se změny projeví v systému.</span><span class="sxs-lookup"><span data-stu-id="1ec52-128">Once published, the changes will be reflected in the system.</span></span> <span data-ttu-id="1ec52-129">Během publikování se neprovádí žádné ověření u změn, které uživatelé provedou.</span><span class="sxs-lookup"><span data-stu-id="1ec52-129">During publish, no validation is done on changes that users make.</span></span>

5. <span data-ttu-id="1ec52-130">Úplný záznam auditu změn lze zobrazit kliknutím na **Zobrazit záznam auditu** v záhlaví **Maloobchodní transakce** pro změny na úrovni záhlaví a v příslušné sekci a provést záznam na příslušné stránce transakce.</span><span class="sxs-lookup"><span data-stu-id="1ec52-130">A complete audit trail of the changes can be viewed by clicking **View audit trail** in the **Retail transaction** header for the header-level changes and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="1ec52-131">Například všechny změny související s řádky prodeje budou viditelné na stránce **Prodejní transakce**, změny týkající se plateb budou zobrazeny na stránce **Platební transakce** atd. Podrobnosti o auditu, které jsou udržovány pro změny, jsou následující.</span><span class="sxs-lookup"><span data-stu-id="1ec52-131">For example, all changes relating to sales lines will be visible on the **Sales transactions** page, changes relating to payments will be visible on the **Payment transactions** page, etc. The audit details that are maintained for the changes are as follows.</span></span>

   - <span data-ttu-id="1ec52-132">Datum a čas úpravy</span><span class="sxs-lookup"><span data-stu-id="1ec52-132">Modified date and time</span></span>
   - <span data-ttu-id="1ec52-133">Pole</span><span class="sxs-lookup"><span data-stu-id="1ec52-133">Field</span></span> 
   - <span data-ttu-id="1ec52-134">Stará hodnota</span><span class="sxs-lookup"><span data-stu-id="1ec52-134">Old value</span></span>
   - <span data-ttu-id="1ec52-135">Nová hodnota</span><span class="sxs-lookup"><span data-stu-id="1ec52-135">New value</span></span>
   - <span data-ttu-id="1ec52-136">Upravil/a</span><span class="sxs-lookup"><span data-stu-id="1ec52-136">Modified by</span></span>

6. <span data-ttu-id="1ec52-137">Po provedení změn a jejich publikování spusťte znovu možnost **Ověřit transakce obchodu** a ověřte, že provedené změny jsou konzistentní a platné.</span><span class="sxs-lookup"><span data-stu-id="1ec52-137">After your changes are made and published, run the **Validate store transactions** option again to validate that the changes you made are consistent and valid.</span></span>

> [!NOTE]
> <span data-ttu-id="1ec52-138">Upravovat lze pouze transakce, jejichž ověření se nezdařilo.</span><span class="sxs-lookup"><span data-stu-id="1ec52-138">You can only edit transactions that failed validation.</span></span> <span data-ttu-id="1ec52-139">Chcete-li upravit transakce, které prošly ověřením, změňte stav ověření transakce, kterou chcete změnit, na **Chyba** nebo **Žádná**, a poté ji budete moci upravit.</span><span class="sxs-lookup"><span data-stu-id="1ec52-139">If you want to edit transactions that passed validation, change the validation status of the transaction you want to change to **Error** or **None** and then you will be able to edit it.</span></span> 


## <a name="bulk-edit-transactions"></a><span data-ttu-id="1ec52-140">Hromadná úprava transakcí</span><span class="sxs-lookup"><span data-stu-id="1ec52-140">Bulk edit transactions</span></span>

<span data-ttu-id="1ec52-141">Ve verzi 10.0.6 aplikace Retail a vyšší je podporována možnost hromadné úpravy transakcí na úrovni výkazů.</span><span class="sxs-lookup"><span data-stu-id="1ec52-141">In Retail version 10.0.6 and higher, the option to bulk edit transactions at a statement level is supported.</span></span> 

1. <span data-ttu-id="1ec52-142">Použijte doplněk aplikace Excel k otevření výkazu s transakcemi, které chcete upravit, pomocí kroků 1-3.</span><span class="sxs-lookup"><span data-stu-id="1ec52-142">Use the Excel Add-in to open a statement that has transactions you want to modify using steps 1-3 above.</span></span>

2. <span data-ttu-id="1ec52-143">Vyberte jednu z níže uvedených možností.</span><span class="sxs-lookup"><span data-stu-id="1ec52-143">Choose one of the options below.</span></span>

    - <span data-ttu-id="1ec52-144">**Upravit transakce cash and carry**.</span><span class="sxs-lookup"><span data-stu-id="1ec52-144">**Edit cash and carry transactions**.</span></span> <span data-ttu-id="1ec52-145">Tato možnost umožňuje úpravu všech cash and carry transakcí zahrnutých do výkazu.</span><span class="sxs-lookup"><span data-stu-id="1ec52-145">This option enables you to edit all the cash and carry transactions included in the statement.</span></span> <span data-ttu-id="1ec52-146">K dispozici jsou následující akci listy aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="1ec52-146">The following Excel worksheets are available.</span></span>
    
       - <span data-ttu-id="1ec52-147">**Transakce**: Tento list obsahuje všechny informace na úrovni záhlaví pro prodejní transakce.</span><span class="sxs-lookup"><span data-stu-id="1ec52-147">**Transaction**: This worksheet has all the header-level information for the sales transactions.</span></span>
       - <span data-ttu-id="1ec52-148">**Prodejní transakce**: Tento list obsahuje všechny informace na úrovni řádků pro prodejní transakce.</span><span class="sxs-lookup"><span data-stu-id="1ec52-148">**Sales transaction**: This worksheet has all the lines-level information for the sales transactions.</span></span>
       - <span data-ttu-id="1ec52-149">**Platební transakce**: Tento list obsahuje všechny informace řádků platby pro prodejní transakce.</span><span class="sxs-lookup"><span data-stu-id="1ec52-149">**Payment transactions**: This worksheet has all the payment lines information for the sales transactions.</span></span>
       - <span data-ttu-id="1ec52-150">**Slevové transakce**: Tento list obsahuje všechny informace řádků slevy pro prodejní transakce.</span><span class="sxs-lookup"><span data-stu-id="1ec52-150">**Discount transactions**: This worksheet has all the discount lines information for the sales transactions.</span></span>
       - <span data-ttu-id="1ec52-151">**Daňové transakce**: Tento list obsahuje všechny informace řádků daně pro prodejní transakce.</span><span class="sxs-lookup"><span data-stu-id="1ec52-151">**Tax transactions**: This worksheet has all the tax lines information for the sales transactions.</span></span>
       - <span data-ttu-id="1ec52-152">**Nákladové transakce**: Tento list obsahuje všechny informace řádků nákladů pro prodejní transakce.</span><span class="sxs-lookup"><span data-stu-id="1ec52-152">**Charge transactions**: This worksheet has all the charge lines information for the sales transactions.</span></span>

    - <span data-ttu-id="1ec52-153">**Upravit transakce řízení hotovosti**.</span><span class="sxs-lookup"><span data-stu-id="1ec52-153">**Edit cash management transactions**.</span></span> <span data-ttu-id="1ec52-154">Tato možnost umožňuje úpravu všech transakcí řízení hotovosti zahrnutých do výkazu.</span><span class="sxs-lookup"><span data-stu-id="1ec52-154">This option enables you to edit all the cash management transactions included in the statement.</span></span> <span data-ttu-id="1ec52-155">K dispozici jsou následující akci listy aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="1ec52-155">The following Excel worksheets are available.</span></span>
     
       - <span data-ttu-id="1ec52-156">**Transakce**: Tento list obsahuje všechny informace na úrovni záhlaví pro transakce řízení hotovosti.</span><span class="sxs-lookup"><span data-stu-id="1ec52-156">**Transaction**: This worksheet has all the header-level information for the cash management transactions.</span></span>
       - <span data-ttu-id="1ec52-157">**Transakce odvodu úhrad do banky**: Tento list obsahuje všechny podrobnosti o transakcích odvodu do banky.</span><span class="sxs-lookup"><span data-stu-id="1ec52-157">**Bank tender transactions**: This worksheet has all the bank drop transaction details.</span></span>
       - <span data-ttu-id="1ec52-158">**Transakce odvodu úhrad do trezoru**: Tento list obsahuje všechny podrobnosti o transakcích odvodu do trezoru.</span><span class="sxs-lookup"><span data-stu-id="1ec52-158">**Safe tender transactions**: This worksheet has all the safe drop transaction details.</span></span>
       - <span data-ttu-id="1ec52-159">**Výkaz úhrad**: Tento list obsahuje všechny podrobnosti o transakcích výkazu úhrad.</span><span class="sxs-lookup"><span data-stu-id="1ec52-159">**Tender declaration**: This worksheet has all the tender declaration transaction details.</span></span>
       - <span data-ttu-id="1ec52-160">**Transakce příjmů/výdajů**: Tento list obsahuje všechny podrobnosti řádku transakce příjmů a výdajů.</span><span class="sxs-lookup"><span data-stu-id="1ec52-160">**Income-expense transaction**: This worksheet has all the income-expense transaction line details.</span></span>
       - <span data-ttu-id="1ec52-161">**Platební transakce**: Tento list obsahuje všechny informace související s platbou pro operaci **Zaplatit fakturu** a transakci příjmů a výdajů.</span><span class="sxs-lookup"><span data-stu-id="1ec52-161">**Payment transactions**: This worksheet has all the payment-related information for the **Pay invoice** operation as well as the income-expense transaction.</span></span>

3.  <span data-ttu-id="1ec52-162">Ověření nejsou prováděna při publikování hromadně upravených transakcí.</span><span class="sxs-lookup"><span data-stu-id="1ec52-162">Validations are not performed when you publish bulk edited transactions.</span></span> <span data-ttu-id="1ec52-163">Je nutné zajistit, aby byly všechny úpravy přesné a aby byla zachována přesnost dat v jednotlivých listech.</span><span class="sxs-lookup"><span data-stu-id="1ec52-163">You must ensure that all your edits are accurate and the fidelity of data across the worksheets is maintained.</span></span> <span data-ttu-id="1ec52-164">Chcete-li například změnit datum transakce pro správu scénářů, kde je uzavřeno fiskální období nebo období zásob pro otevřené transakce, je nutné změnit datum ve všech listech aplikace Excel, které mají sloupec **Obchodní datum**.</span><span class="sxs-lookup"><span data-stu-id="1ec52-164">For example, if you want to change the transaction date to manage the scenarios where the fiscal or inventory period for the open transactions is closed, you need to change the date on all the Excel worksheets that have the **Business date** column.</span></span> <span data-ttu-id="1ec52-165">Chcete-li ověřit transakce po jejich úpravě, můžete použít **Znovu ověřit transakce** na stránce **Výkazy**.</span><span class="sxs-lookup"><span data-stu-id="1ec52-165">To validate transactions after they have been edited, you can use **Revalidate transactions** on the **Statements** page.</span></span>
