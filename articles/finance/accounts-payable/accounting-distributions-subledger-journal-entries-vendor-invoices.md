---
title: Rozúčtování a položky dílčích hlavních knih deníku pro faktury dodavatele
description: Rozúčtování slouží k definování, jak budou zaúčtovány částky, například jak budou výdaje, daně a náklady zaúčtovány na fakturách dodavatele. Každá částka, která musí být zaúčtována, když je dodavatelská faktura zapsána do deníku, bude mít jedno nebo více rozúčtování.
author: abruer
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8e38e6a571bb7f08b32548bcb4af823807a4340
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176867"
---
# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a><span data-ttu-id="58070-104">Rozúčtování a položky dílčích hlavních knih deníku pro faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="58070-104">Accounting distributions and subledger journal entries for vendor invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58070-105">Rozúčtování slouží k definování, jak budou zaúčtovány částky, například jak budou výdaje, daně a náklady zaúčtovány na fakturách dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="58070-106">Každá částka, která musí být zaúčtována, když je dodavatelská faktura zapsána do deníku, bude mít jedno nebo více rozúčtování.</span><span class="sxs-lookup"><span data-stu-id="58070-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

<a name="accounting-distributions"></a><span data-ttu-id="58070-107">Rozúčtování</span><span class="sxs-lookup"><span data-stu-id="58070-107">Accounting distributions</span></span> 
-------------------------

<span data-ttu-id="58070-108">Můžete použít následující tlačítka na stránce Faktura dodavatele pro zobrazení a případnou úpravu rozúčtování pro každou částku na faktuře dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="58070-109">**Rozúčtovat částky** – zobrazení a úprava rozúčtování pro každý řádek a také všechny podřízené řádky, jako jsou například daně a poplatky.</span><span class="sxs-lookup"><span data-stu-id="58070-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="58070-110">Lze také zobrazit a změnit rozúčtování pro podřízený řádek přímo na stránce Transakcí DPH nebo na stránce Transakce nákladů.</span><span class="sxs-lookup"><span data-stu-id="58070-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="58070-111">Úprava částek záhlaví faktury dodavatele, například náklady nebo částky zaokrouhlení měny.</span><span class="sxs-lookup"><span data-stu-id="58070-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="58070-112">Úprava částek řádku faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="58070-113">**Zobrazit distribuce** – Zobrazení rozúčtování pro všechny řádky v dokumentu.</span><span class="sxs-lookup"><span data-stu-id="58070-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="58070-114">Nelze upravit rozúčtování z tohoto zobrazení.</span><span class="sxs-lookup"><span data-stu-id="58070-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="58070-115">Zobrazení záhlaví a částek řádku.</span><span class="sxs-lookup"><span data-stu-id="58070-115">View header and line amounts.</span></span>

<span data-ttu-id="58070-116">Pokud faktura dodavatele odkazuje na nákupní objednávku, můžete rozdělit a změnit rozúčtování pro řádky obsahující zboží, které není na skladě.</span><span class="sxs-lookup"><span data-stu-id="58070-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="58070-117">Pokud řádek faktury dodavatele neobsahuje odkaz na řádek nákupní objednávky, můžete odstranit také rozúčtování.</span><span class="sxs-lookup"><span data-stu-id="58070-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="58070-118">Nelze rozdělit ani odstranit řádky, například na daně, náklady a řádkové slevy.</span><span class="sxs-lookup"><span data-stu-id="58070-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="58070-119">Účet hlavní knihy můžete upravit, ale nelze změnit částky ani procentuální hodnoty.</span><span class="sxs-lookup"><span data-stu-id="58070-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="58070-120">Pokud nadřazený řádek obsahuje zboží, které není na skladě a je rozděleno rozúčtování, podřízený řádek bude rozdělen automaticky, aby odpovídal finanční dimenzi nadřazeného řádku.</span><span class="sxs-lookup"><span data-stu-id="58070-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="58070-121">Rozúčtování pro podřízený řádek nelze dále rozdělit ani odstranit, ale v závislosti na nastavení podřízeného řádku je možné upravit účet hlavní knihy pro rozúčtování podřízeného řádku.</span><span class="sxs-lookup"><span data-stu-id="58070-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="58070-122">Distribuce částek</span><span class="sxs-lookup"><span data-stu-id="58070-122">Distributing amounts</span></span>
<span data-ttu-id="58070-123">Když zadáváte fakturu dodavatele, jednotlivé částky budou rozděleny následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="58070-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="58070-124">Typ řádku faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="58070-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="58070-125">Pořadí priorit, které určuje, odkud se zobrazuje hlavní účet</span><span class="sxs-lookup"><span data-stu-id="58070-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="58070-126">Pořadí priority, které určuje, jaká výchozí finanční dimenze je zobrazena</span><span class="sxs-lookup"><span data-stu-id="58070-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="58070-127">Produkt na skladě</span><span class="sxs-lookup"><span data-stu-id="58070-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="58070-128">Rozúčtování řádku nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="58070-129">Na stránce Zaúčtování se vybere pole Hlavní účet při výběru Nákupní výdaj pro produkt.</span><span class="sxs-lookup"><span data-stu-id="58070-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="58070-130">Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="58070-131">Použijte výchozí hodnoty finanční dimenze na faktuře dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58070-132">Kategorie zásobování nebo produkt, který není na skladě</span><span class="sxs-lookup"><span data-stu-id="58070-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="58070-133">Rozúčtování pro řádek nákupní objednávky, pokud faktura dodavatele obsahuje odkaz na řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="58070-134">Na stránce Zaúčtování se vybere pole Hlavní účet při výběru Nákupní výdaj pro výdaje.</span><span class="sxs-lookup"><span data-stu-id="58070-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="58070-135">Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="58070-136">Je-li hlavní účet účet přidělení, použijte výchozí hodnotu z definice účtu přidělení.</span><span class="sxs-lookup"><span data-stu-id="58070-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="58070-137">Použijte výchozí hodnoty finanční dimenze na faktuře dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="58070-138">Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="58070-139">Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</span><span class="sxs-lookup"><span data-stu-id="58070-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58070-140">Dlouhodobý majetek</span><span class="sxs-lookup"><span data-stu-id="58070-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="58070-141">Rozúčtování pro řádek nákupní objednávky, pokud faktura dodavatele obsahuje odkaz na řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="58070-142">Je-li v poli Typ transakce ve formuláři Faktura dodavatele vybráno Pořízení, vybere se také pole Hlavní účet po zvolení Pořízení na stránce Účetní profily dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="58070-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="58070-143">Je-li v poli Typ transakce vybrána Oprava pořizovací ceny, vybere se také pole Hlavní účet po zvolení Oprava pořizovací ceny na stránce Účetní profily dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="58070-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="58070-144">Použijte rozúčtování pro řádek nákupní objednávky, pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="58070-145">Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="58070-146">Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</span><span class="sxs-lookup"><span data-stu-id="58070-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58070-147">Projekt definovaný na řádku faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="58070-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="58070-148">Rozúčtování pro řádek nákupní objednávky, pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="58070-149">Pokud vyberete Zůstatek v poli Zaúčtovat náklady – položka na stránce Skupiny projektů, vybere se pole Hlavní účet po zvolení možnosti Náklady na stránce Nastavení účtování hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="58070-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="58070-150">Pokud vyberete Zisk a ztráta v poli Zaúčtovat náklady – položka na stránce Skupiny projektů, vybere se pole Hlavní účet po zvolení možnosti Náklady - položka na stránce Nastavení účtování hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="58070-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="58070-151">Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58070-152">Řádková sleva</span><span class="sxs-lookup"><span data-stu-id="58070-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="58070-153">Rozúčtování pro řádek nákupní objednávky, pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="58070-154">Pole Hlavní účet při výběru možnosti Sleva na stránce Zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="58070-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="58070-155">Není-li hlavní účet pro slevu definován v profilu zaúčtování, rozúčtování rozšířené ceny na řádku nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="58070-156">Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="58070-157">Použijte finanční dimenze z rozúčtování pro rozšířenou cenu na řádku faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="58070-158">Použijte hodnoty finanční dimenze pro řádek faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="58070-159">Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</span><span class="sxs-lookup"><span data-stu-id="58070-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58070-160">Náklady nákupu, které byly zadány na kartě Cena a sleva řádku nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="58070-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="58070-161">Rozúčtování pro řádek nákupní objednávky, pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="58070-162">Rozúčtování rozšířené ceny na řádku nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="58070-163">Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="58070-164">Použijte finanční dimenze z rozúčtování pro rozšířenou cenu na řádku faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58070-165">Náklady na řádek</span><span class="sxs-lookup"><span data-stu-id="58070-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="58070-166">Rozúčtování pro řádek nákupní objednávky, pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="58070-167">Pokud vyberete Účet hlavní knihy v poli Typ ve formuláři Kód nákladů, vybere se pole Účet Má dáti na stránce Kód nákladů.</span><span class="sxs-lookup"><span data-stu-id="58070-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="58070-168">Pokud je vybrána Položka v poli Typ debetu ve formuláři Kód nákladů, vyberete rozúčtování pro rozšířenou cenu na řádku nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="58070-169">Pokud vyberete Odběratel/Dodavatel v poli Typ ve formuláři Kód nákladů, vybere se pole Účet Dal na stránce Kód nákladů.</span><span class="sxs-lookup"><span data-stu-id="58070-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="58070-170">Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="58070-171">Použijte finanční dimenze z rozúčtování pro rozšířenou cenu na řádku faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="58070-172">Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="58070-173">Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</span><span class="sxs-lookup"><span data-stu-id="58070-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58070-174">Daň s následující podmínkou:</span><span class="sxs-lookup"><span data-stu-id="58070-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="58070-175">Na stránce Parametry hlavní knihy je zaškrtnuto políčko Použít daňové předpisy platné v USA.</span><span class="sxs-lookup"><span data-stu-id="58070-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="58070-176">Rozúčtování pro řádek nákupní objednávky, pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="58070-177">Rozúčtování rozšířené ceny nebo nákladů.</span><span class="sxs-lookup"><span data-stu-id="58070-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="58070-178">Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="58070-179">Použijte finanční dimenze z rozúčtování pro rozšířenou cenu na řádku faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="58070-180">Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58070-181">Daň s následujícími podmínkami:</span><span class="sxs-lookup"><span data-stu-id="58070-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58070-182">Na stránce Parametry hlavní knihy je zrušeno označení políčka Použít daňové předpisy platné v USA.</span><span class="sxs-lookup"><span data-stu-id="58070-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="58070-183">Na stránce Skupiny prodejní daně je pro skupinu DPH zrušeno označení pole Importní DPH.</span><span class="sxs-lookup"><span data-stu-id="58070-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="58070-184">Pokud je částka DPH vratná, vybere se pole DPH na vstupu na stránce Účetní skupiny.</span><span class="sxs-lookup"><span data-stu-id="58070-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="58070-185">Pokud není částka daně vratná, rozšířená cena nebo rozúčtování pro náklady.</span><span class="sxs-lookup"><span data-stu-id="58070-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="58070-186">Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="58070-187">Použijte finanční dimenze z rozšířené ceny nebo rozúčtování pro náklady na řádku faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="58070-188">Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="58070-189">Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</span><span class="sxs-lookup"><span data-stu-id="58070-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58070-190">Daň s následujícími podmínkami:</span><span class="sxs-lookup"><span data-stu-id="58070-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="58070-191">Na stránce Parametry hlavní knihy je zrušeno označení políčka Použít daňové předpisy platné v USA.</span><span class="sxs-lookup"><span data-stu-id="58070-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="58070-192">Na stránce Skupiny prodejní daně je pro skupinu DPH vybráno pole Importní DPH.</span><span class="sxs-lookup"><span data-stu-id="58070-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="58070-193">Pokud je částka DPH vratná, vybere se pole DPH na vstupu na stránce Účetní skupiny.</span><span class="sxs-lookup"><span data-stu-id="58070-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="58070-194">Pokud částka DPH není vratná, vybere se pole Importní DPH – výdaj na stránce Účetní skupiny.</span><span class="sxs-lookup"><span data-stu-id="58070-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="58070-195">Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="58070-196">Použijte finanční dimenze z rozšířené ceny nebo rozúčtování pro náklady na řádku faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="58070-197">Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="58070-198">Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</span><span class="sxs-lookup"><span data-stu-id="58070-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="58070-199">Náklady v záhlaví</span><span class="sxs-lookup"><span data-stu-id="58070-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="58070-200">Pokud vyberete Účet hlavní knihy v poli Typ ve formuláři Kód nákladů, vybere se pole Účet Má dáti na stránce Kód nákladů.</span><span class="sxs-lookup"><span data-stu-id="58070-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="58070-201">Pokud vyberete Odběratel/Dodavatel v poli Typ ve formuláři Kód nákladů, vybere se pole Účet Dal na stránce Kód nákladů.</span><span class="sxs-lookup"><span data-stu-id="58070-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="58070-202">Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="58070-203">Je-li hlavní účet účet přidělení, použijte výchozí hodnotu z definice účtu přidělení.</span><span class="sxs-lookup"><span data-stu-id="58070-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="58070-204">Použijte hodnoty výchozí šablony finanční dimenze ze záhlaví faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="58070-205">Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="58070-206">Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</span><span class="sxs-lookup"><span data-stu-id="58070-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="58070-207">Sleva záhlaví</span><span class="sxs-lookup"><span data-stu-id="58070-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="58070-208">Pole Hlavní účet pro typ zaúčtování Sleva faktury dodavatele na stránce Účty pro automatické transakce.</span><span class="sxs-lookup"><span data-stu-id="58070-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="58070-209">Pokud řádek faktury obsahuje odkaz na řádek nákupní objednávky, použijte rozúčtování pro řádek nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="58070-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="58070-210">Použijte finanční dimenze z rozúčtování pro rozšířenou cenu na řádku faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="58070-211">Použijte hodnoty finanční dimenze z řádku faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="58070-212">Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</span><span class="sxs-lookup"><span data-stu-id="58070-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a><span data-ttu-id="58070-213">Distribuce daní</span><span class="sxs-lookup"><span data-stu-id="58070-213">Distributing taxes</span></span>
------------------

<span data-ttu-id="58070-214">Dokud daně nejsou vypočítány, nelze pro ně vytvořit rozúčtování.</span><span class="sxs-lookup"><span data-stu-id="58070-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="58070-215">Při výpočtu DPH je třeba na stránce Faktura dodavatele provést jeden z následujících úkolů:</span><span class="sxs-lookup"><span data-stu-id="58070-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="58070-216">Zobrazit celkový součet faktury.</span><span class="sxs-lookup"><span data-stu-id="58070-216">View the invoice total.</span></span>
-   <span data-ttu-id="58070-217">Zobrazit DPH.</span><span class="sxs-lookup"><span data-stu-id="58070-217">View the sales tax.</span></span>
-   <span data-ttu-id="58070-218">Zobrazit dílčí hlavní knihu.</span><span class="sxs-lookup"><span data-stu-id="58070-218">View the subledger journal.</span></span>
-   <span data-ttu-id="58070-219">Zobrazit rozúčtování pro kompletní fakturu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="58070-220">Blokovat fakturu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="58070-221">Zaúčtovat fakturu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="58070-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="58070-222">Dílčí hlavní deníky pro faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="58070-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="58070-223">Před zaúčtováním faktury dodavatele můžete zobrazit celý účetní zápis faktury, který zahrnuje pohledávky a závazky, abyste ověřili, zda je faktura zaúčtována na správné účty.</span><span class="sxs-lookup"><span data-stu-id="58070-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="58070-224">Toto zobrazení celkového zápisu do účetnictví se nazývá dílčí hlavní kniha.</span><span class="sxs-lookup"><span data-stu-id="58070-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="58070-225">Pokud není položka dílčí hlavní knihy správná při zobrazení náhledu než zapíšete fakturu dodavatele do deníku, položku dílčí hlavní knihy nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="58070-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="58070-226">Namísto toho je nutné upravit rozúčtování nebo účetní profil.</span><span class="sxs-lookup"><span data-stu-id="58070-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="58070-227">Rozúčtování slouží k definování jedné strany účetní položky, má dáti nebo dal.</span><span class="sxs-lookup"><span data-stu-id="58070-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="58070-228">Vyrovnání účetní položky dílčí hlavní knihy je vytvořeno pomocí účetních profilů, jako je například účet dodavatele nebo daň.</span><span class="sxs-lookup"><span data-stu-id="58070-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>





