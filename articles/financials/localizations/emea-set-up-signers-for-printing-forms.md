---
title: Nastavení podepisujících uživatelů pro tiskové formuláře
description: Pro právnické osoby v České republice, Estonsku, Maďarsku, Litvě, Lotyšsku, Polsku a Rusku můžete nastavit podepisující osoby a tituly pro odběratele a dodavatele, kteří tisknou dokumenty, jako jsou faktury a platební příkazy.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 263464
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c3b97de064d7e151c6136d77d993ff4323055bc8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537643"
---
# <a name="set-up-signers-for-print-forms"></a><span data-ttu-id="def2d-103">Nastavení podepisujících uživatelů pro tiskové formuláře</span><span class="sxs-lookup"><span data-stu-id="def2d-103">Set up signers for print forms</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="def2d-104">Pro právnické osoby v České republice, Estonsku, Maďarsku, Litvě, Lotyšsku, Polsku a Rusku můžete nastavit podepisující osoby a tituly pro odběratele a dodavatele, kteří tisknou dokumenty, jako jsou faktury a platební příkazy.</span><span class="sxs-lookup"><span data-stu-id="def2d-104">For legal entities in Czech Republic, Estonia, Hungary, Lithuania, Latvia, Poland, and Russia, you can set up signers and titles for customers and vendors that print documents such as invoices and cash orders.</span></span>

<a name="set-up-default-values"></a><span data-ttu-id="def2d-105">Nastavení výchozích hodnot</span><span class="sxs-lookup"><span data-stu-id="def2d-105">Set up default values</span></span>
---------------------

<span data-ttu-id="def2d-106">K nastavení podepisujících dokumentů, které společnost tiskne, použijte stránku **Úředníci**.</span><span class="sxs-lookup"><span data-stu-id="def2d-106">To set up signers for the documents that a company prints, use the **Officials** page.</span></span> <span data-ttu-id="def2d-107">Pro firmu i pro zákazníky nebo dodavatele můžete nastavit podepisující osoby a jejich jména, v závislosti na typu dokumentu.</span><span class="sxs-lookup"><span data-stu-id="def2d-107">You can set up signers and their titles both for the company and for customers or vendors, depending on the document type.</span></span> <span data-ttu-id="def2d-108">Následující tabulka popisuje karty na stránce **Úředníci**.</span><span class="sxs-lookup"><span data-stu-id="def2d-108">The following table describes the tabs on the **Officials** page.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="def2d-109">Karta</span><span class="sxs-lookup"><span data-stu-id="def2d-109">Tab</span></span></th>
<th><span data-ttu-id="def2d-110">popis</span><span class="sxs-lookup"><span data-stu-id="def2d-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="def2d-111">Obecné</span><span class="sxs-lookup"><span data-stu-id="def2d-111">General</span></span></td>
<td><span data-ttu-id="def2d-112">Přidání pozic a souvisejících informací pro podepisující osoby (ředitel a hlavní účetní), který může podepisovat tištěné doklady všech typů.</span><span class="sxs-lookup"><span data-stu-id="def2d-112">Add positions and related information for signers (Director and Chief accountant) who can sign print documents of all types.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="def2d-113">Hlavní kniha</span><span class="sxs-lookup"><span data-stu-id="def2d-113">Ledger</span></span></td>
<td><span data-ttu-id="def2d-114">Přidejte pozici a související informace o uživatelích, kteří mohou podepsat následující interní finanční dokumenty, které souvisí s cashflow:</span><span class="sxs-lookup"><span data-stu-id="def2d-114">Add the position and related information for signers who can sign the following internal financial documents that are related to cash flow:</span></span>
<ul>
<li><span data-ttu-id="def2d-115">Pokladní doklady</span><span class="sxs-lookup"><span data-stu-id="def2d-115">Cash slips</span></span></li>
<li><span data-ttu-id="def2d-116">Sestava záloh</span><span class="sxs-lookup"><span data-stu-id="def2d-116">Advance report</span></span></li>
<li><span data-ttu-id="def2d-117">Stránka pokladní knihy</span><span class="sxs-lookup"><span data-stu-id="def2d-117">Page of cash book</span></span></li>
<li><span data-ttu-id="def2d-118">Výpis inventury</span><span class="sxs-lookup"><span data-stu-id="def2d-118">Count statement</span></span></li>
<li><span data-ttu-id="def2d-119">Časově rozlišené položky<em></span><span class="sxs-lookup"><span data-stu-id="def2d-119">Deferrals<em></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="def2d-120">Prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="def2d-120">Sales orders</span></span></td>
<td><span data-ttu-id="def2d-121">Přidejte pozice a související informace o uživatelích, kteří mohou podepsat následující odchozí primární dokumenty, které souvisí s cashflow:</span><span class="sxs-lookup"><span data-stu-id="def2d-121">Add positions and related information for signers who can sign the following outgoing primary documents that are related to customers:</span></span>
<ul>
<li><span data-ttu-id="def2d-122">Faktura pro platbu</span><span class="sxs-lookup"><span data-stu-id="def2d-122">Invoice for payment</span></span></em></li>
<li><span data-ttu-id="def2d-123">Faktura</span><span class="sxs-lookup"><span data-stu-id="def2d-123">Invoice</span></span></li>
<li><span data-ttu-id="def2d-124">Faktura<em></span><span class="sxs-lookup"><span data-stu-id="def2d-124">Facture<em></span></span></li>
<li><span data-ttu-id="def2d-125">Faktura – dobropis</span><span class="sxs-lookup"><span data-stu-id="def2d-125">Invoice - credit-note</span></span></li>
<li><span data-ttu-id="def2d-126">Dílčí faktura – dobropis</span><span class="sxs-lookup"><span data-stu-id="def2d-126">Facture - credit-note</span></span></em></li>
<li><span data-ttu-id="def2d-127">Faktura daňové transakce (zákazník)<em></span><span class="sxs-lookup"><span data-stu-id="def2d-127">Tax transaction facture (client)<em></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="def2d-128">Nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="def2d-128">Purchase orders</span></span></td>
<td><span data-ttu-id="def2d-129">Přidejte pozice a související informace o uživatelích, kteří mohou podepsat následující příchozí primární dokumenty, které souvisí s dodavateli:</span><span class="sxs-lookup"><span data-stu-id="def2d-129">Add positions and related information for signers who can sign the following incoming primary documents that are related to vendors:</span></span>
<ul>
<li><span data-ttu-id="def2d-130">Faktura</span><span class="sxs-lookup"><span data-stu-id="def2d-130">Invoice</span></span></li>
<li><span data-ttu-id="def2d-131">Faktura</span><span class="sxs-lookup"><span data-stu-id="def2d-131">Facture</span></span></em></li>
<li><span data-ttu-id="def2d-132">Faktura – dobropis</span><span class="sxs-lookup"><span data-stu-id="def2d-132">Invoice - credit-note</span></span></li>
<li><span data-ttu-id="def2d-133">Dílčí faktura – dobropis<em></span><span class="sxs-lookup"><span data-stu-id="def2d-133">Facture - credit-note<em></span></span></li>
<li><span data-ttu-id="def2d-134">Faktura pro platbu</span><span class="sxs-lookup"><span data-stu-id="def2d-134">Invoice for payment</span></span></em></li>
<li><span data-ttu-id="def2d-135">Faktura daňové transakce (dodavatel)<em></span><span class="sxs-lookup"><span data-stu-id="def2d-135">Tax transaction facture (vendor)<em></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="def2d-136">Řízení skladových položek</span><span class="sxs-lookup"><span data-stu-id="def2d-136">Inventory item management</span></span></td>
<td><span data-ttu-id="def2d-137">Přidejte pozice a informace týkající se u uživatelů, kteří mohou podepsat následující skladové doklady, když je zákazníkovi vydán hmotný majetek nebo když je převzat od dodavatele.</span><span class="sxs-lookup"><span data-stu-id="def2d-137">Add positions and related information for signers who can sign the following warehouse documents when tangible assets are issued to a customer or received from a vendor:</span></span>
<ul>
<li><span data-ttu-id="def2d-138">Výdejní list pro prodejní objednávku (M-15)</span><span class="sxs-lookup"><span data-stu-id="def2d-138">Issue slip for sales order (M-15)</span></span></em></li>
<li><span data-ttu-id="def2d-139">Refund.</span><span class="sxs-lookup"><span data-stu-id="def2d-139">Rmb.</span></span> <span data-ttu-id="def2d-140">doklad/Příjemka</span><span class="sxs-lookup"><span data-stu-id="def2d-140">slip/Receipt order</span></span></li>
<li><span data-ttu-id="def2d-141">Výdejní list pro převodní příkaz (M-15)\*</span><span class="sxs-lookup"><span data-stu-id="def2d-141">Issue slip for transfer order (M-15)\*</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="def2d-142">\* Tento typ dokumentu je k dispozici pouze pro právnické osoby, které mají primární adresu v Rusku.</span><span class="sxs-lookup"><span data-stu-id="def2d-142">\* This document type is available only for legal entities that have their primary address in Russia.</span></span> <span data-ttu-id="def2d-143">Následující tabulka popisuje pole na stránce **Úředníci**.</span><span class="sxs-lookup"><span data-stu-id="def2d-143">The following table describes the fields on the **Officials** page.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="def2d-144">Pole</span><span class="sxs-lookup"><span data-stu-id="def2d-144">Field</span></span></th>
<th><span data-ttu-id="def2d-145">popis</span><span class="sxs-lookup"><span data-stu-id="def2d-145">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="def2d-146">Pozice</span><span class="sxs-lookup"><span data-stu-id="def2d-146">Position</span></span></td>
<td><span data-ttu-id="def2d-147">Vyberte název pozice autora podpisu.</span><span class="sxs-lookup"><span data-stu-id="def2d-147">Select the signer’s post title.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="def2d-148">Jméno</span><span class="sxs-lookup"><span data-stu-id="def2d-148">Name</span></span></td>
<td><span data-ttu-id="def2d-149">Vyberte jméno autora podpisu.</span><span class="sxs-lookup"><span data-stu-id="def2d-149">Select the signer’s name.</span></span> <span data-ttu-id="def2d-150">Jména v seznamu pocházejí z tabulky Kontakty nebo tabulky Zaměstnanci v závislosti na typu podepisující osoby (tj. v závislosti na tom, zda je zaškrtnuto políčko <strong>Naši</strong>).</span><span class="sxs-lookup"><span data-stu-id="def2d-150">The names in the list come from either the Contacts table or the Employees table, depending on the type of signer (that is, depending on whether the <strong>Our</strong> check box is selected).</span></span> <span data-ttu-id="def2d-151">Není-li jméno podepisující osoby v seznamu, ručně zadejte celé jméno podepisující osoby.</span><span class="sxs-lookup"><span data-stu-id="def2d-151">If the signer&#39;s name isn&#39;t in the list, manually enter the signer’s full name.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="def2d-152">Pracovní titul</span><span class="sxs-lookup"><span data-stu-id="def2d-152">Job title</span></span></td>
<td><span data-ttu-id="def2d-153">Vyberte titul autora podpisu.</span><span class="sxs-lookup"><span data-stu-id="def2d-153">Select the signer’s job title.</span></span> <span data-ttu-id="def2d-154">Není-li titul podepisující osoby v seznamu, ručně ho zadejte.</span><span class="sxs-lookup"><span data-stu-id="def2d-154">If the signer’s title isn&#39;t in the list, manually enter the signer’s title.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="def2d-155">Kód účtu</span><span class="sxs-lookup"><span data-stu-id="def2d-155">Account code</span></span></td>
<td><span data-ttu-id="def2d-156">Vyberte, zda mohou podepisující podepsat všechny dokumenty pro vybraný typ dokumentu nebo pouze doklady pro určitého odběratele nebo dodavatele.</span><span class="sxs-lookup"><span data-stu-id="def2d-156">Select whether the signer can sign all documents of the selected document type, or only documents for a specific customer or vendor.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="def2d-157">Odkaz na účet</span><span class="sxs-lookup"><span data-stu-id="def2d-157">Account relation</span></span></td>
<td><span data-ttu-id="def2d-158">Vyberte účet odběratele nebo dodavatele, vztahující se ke kódu vybraného účtu.</span><span class="sxs-lookup"><span data-stu-id="def2d-158">Select the customer or vendor account that is related to the selected account code.</span></span> <span data-ttu-id="def2d-159">Toto pole je k dispozici pouze, pokud vyberete <strong>Záznam</strong> v poli <strong>Kód účtu</strong>.</span><span class="sxs-lookup"><span data-stu-id="def2d-159">This field is available only if you select <strong>Record</strong> in the <strong>Account code</strong> field.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="def2d-160">Naše</span><span class="sxs-lookup"><span data-stu-id="def2d-160">Our</span></span></td>
<td><span data-ttu-id="def2d-161">Zaškrtnuté políčko označuje, že jde o interní pozici</span><span class="sxs-lookup"><span data-stu-id="def2d-161">A selected check box indicates that the position is internal.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="def2d-162">Spojení se skladem</span><span class="sxs-lookup"><span data-stu-id="def2d-162">Association with warehouse</span></span></td>
<td><span data-ttu-id="def2d-163">Vyberte, zda je podepisující je přiřazen všem skladům nebo jen určitému.</span><span class="sxs-lookup"><span data-stu-id="def2d-163">Select whether the signer is assigned to all warehouses or only a specific warehouse.</span></span> <span data-ttu-id="def2d-164">Existují tyto možnosti:</span><span class="sxs-lookup"><span data-stu-id="def2d-164">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="def2d-165"><strong>Všechny</strong> – podepisující je přiřazen všem skladům.</span><span class="sxs-lookup"><span data-stu-id="def2d-165"><strong>All</strong> – The signer is assigned to all warehouses.</span></span></li>
<li><span data-ttu-id="def2d-166"><strong>Záznam</strong> – podepisující je přiřazen jen určitému skladu.</span><span class="sxs-lookup"><span data-stu-id="def2d-166"><strong>Record</strong> – The signer is assigned to a specific warehouse.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="def2d-167">Sklad</span><span class="sxs-lookup"><span data-stu-id="def2d-167">Warehouse</span></span></td>
<td><span data-ttu-id="def2d-168">Vyberte kód skladu, který odpovídá skladu, jemuž je podepisující přiřazen.</span><span class="sxs-lookup"><span data-stu-id="def2d-168">Select the warehouse code that corresponds to the warehouse that the signer is assigned to.</span></span> <span data-ttu-id="def2d-169">Toto pole je k dispozici pouze, pokud vyberete <strong>Záznam</strong> v poli <strong>Přidružení ke skladu</strong>.</span><span class="sxs-lookup"><span data-stu-id="def2d-169">This field is available only if you select <strong>Record</strong> in the <strong>Association with warehouse</strong> field.</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-a-number-sequence-code-for-officials"></a><span data-ttu-id="def2d-170">Nastavení kódu číselného pořadí pro státní úředníky</span><span class="sxs-lookup"><span data-stu-id="def2d-170">Set up a number sequence code for officials</span></span>
<span data-ttu-id="def2d-171">Můžete přiřadit kód číselné řady pro úředníky v části **Číselné řady** stránky **Právnické osoby**.</span><span class="sxs-lookup"><span data-stu-id="def2d-171">You can assign a number sequence code for officials in the **Number sequences** section of the **Legal entities** page.</span></span> <span data-ttu-id="def2d-172">Vyberte kód číselné řady reference **ID relace úředních osob**.</span><span class="sxs-lookup"><span data-stu-id="def2d-172">Select a number sequence code for the **Officials session ID** reference.</span></span>

## <a name="modify-signers-in-primary-documents"></a><span data-ttu-id="def2d-173">Změna podepisujících osob v primárních dokumentech</span><span class="sxs-lookup"><span data-stu-id="def2d-173">Modify signers in primary documents</span></span>
<span data-ttu-id="def2d-174">Funkce Úředníci zobrazuje výchozí předdefinované podepisující z tabulky úředníků.</span><span class="sxs-lookup"><span data-stu-id="def2d-174">The Officials functionality shows the default predefined signers from the Officials table.</span></span> <span data-ttu-id="def2d-175">Na stránce **Zaúčtování faktury** na kartě **Úředníci** můžete změnit jméno podepisující osoby a název primárního dokladu pro následující typy dokumentů:</span><span class="sxs-lookup"><span data-stu-id="def2d-175">On the **Posting invoice** page, on the **Officials** tab, you can modify a signer’s name and title on the primary document for the following document types:</span></span>

-   <span data-ttu-id="def2d-176">Faktura odběratele</span><span class="sxs-lookup"><span data-stu-id="def2d-176">Customer invoice</span></span>
-   <span data-ttu-id="def2d-177">Faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="def2d-177">Vendor invoice</span></span>
-   <span data-ttu-id="def2d-178">Převodní příkaz expedice</span><span class="sxs-lookup"><span data-stu-id="def2d-178">Ship transfer order</span></span>
-   <span data-ttu-id="def2d-179">Pokladní doklad</span><span class="sxs-lookup"><span data-stu-id="def2d-179">Cash order</span></span>

<span data-ttu-id="def2d-180">**Poznámka:** Po zaúčtování dokumentu nelze úředníky upravit.</span><span class="sxs-lookup"><span data-stu-id="def2d-180">**Note:** After a document is posted, officials can't be edited.</span></span>



