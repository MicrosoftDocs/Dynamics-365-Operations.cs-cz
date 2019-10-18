---
title: DPH stornovacího poplatku
description: Toto téma popisuje určení přenesení daňové povinnosti (reverse charge) pro DPH u evropských zemí, v Saúdské Arábii a Singapuru.
author: epodkolz
manager: AnnBe
ms.date: 07/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Saudi Arabia, Spain, Sweden, United Kingdom, Singapore
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 530ff52abb1dd36c473ae436d61ea925c5696a30
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183482"
---
# <a name="reverse-charge-vat"></a><span data-ttu-id="3634f-103">DPH stornovacího poplatku</span><span class="sxs-lookup"><span data-stu-id="3634f-103">Reverse charge VAT</span></span>


[!include [banner](../includes/banner.md)]


<span data-ttu-id="3634f-104">Toto téma popisuje obecný postup pro určení přenesení daňové povinnosti (reverse charge) pro DPH u evropských zemí, pro Saúdskou Arábii a Singapur.</span><span class="sxs-lookup"><span data-stu-id="3634f-104">This topic describes a generic approach for setting up reverse charge value-added tax (VAT) for Saudi Arabia, Singapore, and European countries.</span></span>

<span data-ttu-id="3634f-105">Mechanismus reverse charge znamená přenesení odpovědnosti za účetnictví a vykazování DPH z prodávajícího na kupujícího.</span><span class="sxs-lookup"><span data-stu-id="3634f-105">Reverse Charge is a tax schema that moves the responsibility for the accounting and reporting of VAT from the seller to the buyer of goods and/or services.</span></span> <span data-ttu-id="3634f-106">Příjemce tedy do výkazu DPH uvádí DPH na výstupu (v roli prodávajícího) i DPH na vstupu (v roli kupujícího).</span><span class="sxs-lookup"><span data-stu-id="3634f-106">Therefore, recipients of goods and/or services report both the output VAT (in the role of a seller) and the input VAT (in the role of a purchaser) on their VAT statement.</span></span>

<span data-ttu-id="3634f-107">V některých zemích nebo regionech se tedy mechanismus reverse charge uplatňuje jen na některé druhy zboží nebo služeb a mohou platit další podmínky nebo prahové hodnoty pro částky prodeje.</span><span class="sxs-lookup"><span data-stu-id="3634f-107">In some countries or regions, the Reverse Charge schema is implemented only for some goods and/or services, and there are additional conditions or thresholds on sales amounts.</span></span> <span data-ttu-id="3634f-108">V jiných zemích nebo regionech závisí odpovědnost za placení DPH na statusu dodavatele a kupujícího.</span><span class="sxs-lookup"><span data-stu-id="3634f-108">In other countries or regions, the responsibility for VAT payment depends on the status of the supplier and the buyer.</span></span> <span data-ttu-id="3634f-109">Pokud je kupující plátcem DPH, tato skutečnost musí být jasně uvedena na faktuře vydané dodavatelem.</span><span class="sxs-lookup"><span data-stu-id="3634f-109">If the buyer is liable to pay VAT, this fact must be clearly indicated on the invoice that the supplier issues.</span></span> <span data-ttu-id="3634f-110">Faktura například musí obsahovat výraz „reverse charge“ (přenesení daňové povinnosti) a informace o tom, na co se tento mechanismus vztahuje.</span><span class="sxs-lookup"><span data-stu-id="3634f-110">For example, the invoice must include the words "Reverse charge" and must indicate which positions are under the Reverse Charge schema.</span></span> 

<span data-ttu-id="3634f-111">Abyste mohli mechanismus reverse charge použít, je třeba provést následující nastavení.</span><span class="sxs-lookup"><span data-stu-id="3634f-111">To apply the reverse charge, you must complete the following setup.</span></span>

## <a name="set-up-sales-tax-codes"></a><span data-ttu-id="3634f-112">Nastavit kódy DPH</span><span class="sxs-lookup"><span data-stu-id="3634f-112">Set up sales tax codes</span></span>
<span data-ttu-id="3634f-113">Doporučujeme používat pro nákupní a prodejní operace samostatné kódy DPH.</span><span class="sxs-lookup"><span data-stu-id="3634f-113">We recommend that you use separate sales tax codes for sales operations and purchase operations.</span></span>

<table>
<body>
<tr>
<td><span data-ttu-id="3634f-114"><strong>Kód DPH u prodeje</strong></span><span class="sxs-lookup"><span data-stu-id="3634f-114"><strong>Sales tax code for sales</strong></span></span></td>
<td><span data-ttu-id="3634f-115">Vytvořte kód daně z prodeje pro operace prodeje zpětného účtování (<strong>Daň</strong> &gt; <strong>Nepřímé daně</strong> &gt; <strong>Daň z prodeje</strong> &gt; <strong>Kódy daně z prodeje</strong>).</span><span class="sxs-lookup"><span data-stu-id="3634f-115">Create a sales tax code for reverse charge sales operations (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax codes</strong>).</span></span>
</td>
</tr>
<tr>
<td><span data-ttu-id="3634f-116"><strong>Kód DPH u nákupu</strong></span><span class="sxs-lookup"><span data-stu-id="3634f-116"><strong>Sales tax code for purchases</strong></span></span></td>
<td><p><span data-ttu-id="3634f-117">Vytvořte kladné a záporné kódy DPH pro mechanismus reverse charge VAT pro nákupy (<strong>Daň</strong> &gt; <strong>Nepřímé daně</strong> &gt; <strong>Daň z prodeje</strong> &gt; <strong>Kódy daně z prodeje</strong>).</span><span class="sxs-lookup"><span data-stu-id="3634f-117">Create positive and negative sales tax codes for the reverse charge VAT for purchases (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax codes</strong>).</span></span></p>
<ol>
<li><span data-ttu-id="3634f-118">Vytvořte kód DPH s kladnou hodnotou.</span><span class="sxs-lookup"><span data-stu-id="3634f-118">Create a sales tax code that has a positive value.</span></span></li>
<li><span data-ttu-id="3634f-119">Vytvořte kód DPH se zápornou hodnotou.</span><span class="sxs-lookup"><span data-stu-id="3634f-119">Create a sales tax code that has a negative value.</span></span> <span data-ttu-id="3634f-120">Nastavte možnost <strong>Povolit záporné procento DPH</strong> na <strong>Ano</strong>.</span><span class="sxs-lookup"><span data-stu-id="3634f-120">Set the <strong>Allow negative sales tax percentage</strong> option to <strong>Yes</strong>.</span></span>
<span data-ttu-id="3634f-121">Skupině DPH položek je třeba přiřadit tento záporný kód DPH a pak přiřadit tuto skupinu DPH položkám, kterých se mechanismus reverse charge týká.</span><span class="sxs-lookup"><span data-stu-id="3634f-121">You must assign this negative sales tax code to an item sales tax group and then assign that item sales tax group to the items that are subject to the reverse charge VAT.</span></span></li>
</ol>
<p><span data-ttu-id="3634f-122">Další informace najdete v následující části &quot;Nastavení skupin DPH a skupin DPH položek.&quot;</span><span class="sxs-lookup"><span data-stu-id="3634f-122">For more information, see the next section, &quot;Set up sales tax groups and item sales tax groups.&quot;</span></span></p>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="3634f-123">Nastavení skupin DPH a skupin DPH položky</span><span class="sxs-lookup"><span data-stu-id="3634f-123">Set up sales tax groups and item sales tax groups</span></span>
<span data-ttu-id="3634f-124">Doporučujeme používat pro nákupní a prodejní operace samostatné skupiny DPH.</span><span class="sxs-lookup"><span data-stu-id="3634f-124">We recommend that you use separate sales tax groups for sales operations and purchase operations.</span></span>

<table>
<tr>
<td><span data-ttu-id="3634f-125"><strong>Skupiny DPH u prodeje</strong></span><span class="sxs-lookup"><span data-stu-id="3634f-125"><strong>Sales tax groups for sales</strong></span></span></td>
<td><span data-ttu-id="3634f-126">Vytvořte skupinu DPH pro operace prodeje s nastavením reverse charge (<strong>Daň</strong> &gt; <strong>Nepřímé daně</strong> &gt; <strong>Daň z prodeje</strong> &gt; <strong>Skupiny daně z prodeje</strong>).</span><span class="sxs-lookup"><span data-stu-id="3634f-126">Create a sales tax group for sales operations that have the reverse charge (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax groups</strong>).</span></span> <span data-ttu-id="3634f-127">Na kartě <strong>Nastavení</strong> přidejte do této skupiny kód DPH pro reverse charge.</span><span class="sxs-lookup"><span data-stu-id="3634f-127">On the <strong>Setup</strong> tab, include the sales tax code for the reverse charge in this group.</span></span> <span data-ttu-id="3634f-128">Zaškrtněte možnosti <strong>Osvobozené od daně</strong> a <strong>Stornovací poplatek</strong> u příslušného kódu.</span><span class="sxs-lookup"><span data-stu-id="3634f-128">Select the <strong>Exempt</strong> and <strong>Reverse charge</strong> check boxes for the sales tax code.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3634f-129"><strong>Skupiny DPH u nákupu</strong></span><span class="sxs-lookup"><span data-stu-id="3634f-129"><strong>Sales tax groups for purchases</strong></span></span></td>
<td><span data-ttu-id="3634f-130">Vytvořte skupinu DPH pro operace nákupu s nastavením reverse charge (<strong>Daň</strong> &gt; <strong>Nepřímé daně</strong> &gt; <strong>Daň z prodeje</strong> &gt; <strong>Skupiny daně z prodeje</strong>).</span><span class="sxs-lookup"><span data-stu-id="3634f-130">Create a sales tax group for purchase operations that have the reverse charge (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Sales tax groups</strong>).</span></span> <span data-ttu-id="3634f-131">Na kartě <strong>Nastavení</strong> přidejte do této skupiny kladný a záporný kód DPH.</span><span class="sxs-lookup"><span data-stu-id="3634f-131">On the <strong>Setup</strong> tab, include both positive and negative sales tax codes in this group.</span></span> <span data-ttu-id="3634f-132">U kódu se zápornou hodnotou zaškrtněte políčko <strong>Stornovací poplatek</strong>.</span><span class="sxs-lookup"><span data-stu-id="3634f-132">Select the <strong>Reverse charge</strong> check box for the sales tax code that has a negative value.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3634f-133"><strong>Skupiny DPH položky</strong></span><span class="sxs-lookup"><span data-stu-id="3634f-133"><strong>Item sales tax groups</strong></span></span></td>
<td><span data-ttu-id="3634f-134">Vytvořte nebo aktualizujte skupinu DPH položky pomocí kódu DPH se zápornou hodnotou (<strong>Daň</strong> &gt; <strong>Nepřímé daně</strong> &gt; <strong>Daň z prodeje</strong> &gt; <strong>Skupiny daně z prodeje zboží</strong>).</span><span class="sxs-lookup"><span data-stu-id="3634f-134">Create or update the item sales tax group with the sales tax code that has a negative value (<strong>Tax</strong> &gt; <strong>Indirect taxes</strong> &gt; <strong>Sales tax</strong> &gt; <strong>Item sales tax groups</strong>).</span></span> <span data-ttu-id="3634f-135">Výchozí skupinu DPH položky je třeba přiřadit k produktům a kategoriím, na které se mechanismus reverse charge vztahuje.</span><span class="sxs-lookup"><span data-stu-id="3634f-135">You must assign the default item sales tax group to the products and categories that are subject to the reverse charge.</span></span></td>
</tr>
</table>

## <a name="set-up-reverse-charge-groups"></a><span data-ttu-id="3634f-136">Nastavení skupin pro reverse charge</span><span class="sxs-lookup"><span data-stu-id="3634f-136">Set up reverse charge groups</span></span>
<span data-ttu-id="3634f-137">Na stránce **Stornovací poplatek – skupiny položek** (**Daň** &gt; **Nastavení** &gt; **DPH** &gt; **Stornovací poplatek – skupiny položek**) je možné definovat skupiny produktů nebo služeb (případně jednotlivé produkty či služby), pro které má mechanismus reverse charge platit.</span><span class="sxs-lookup"><span data-stu-id="3634f-137">On the **Reverse charge item groups** page (**Tax** &gt; **Setup** &gt; **Sales tax** &gt; **Reverse charge item groups**), you can define groups of products or services, or individual products or services, that the reverse charge can be applied to.</span></span> <span data-ttu-id="3634f-138">U každé skupiny položek pro reverse charge definujte seznam položek, skupin položek a kategorií pro prodej nebo nákup.</span><span class="sxs-lookup"><span data-stu-id="3634f-138">For each reverse charge item group, define the list of items, item groups, and categories for sales and/or purchases.</span></span>

## <a name="set-up-reverse-charge-rules"></a><span data-ttu-id="3634f-139">Nastavení pravidel pro reverse charge</span><span class="sxs-lookup"><span data-stu-id="3634f-139">Set up reverse charge rules</span></span>
<span data-ttu-id="3634f-140">Na stránce **Pravidla pro stornovací poplatek** (**Daň** &gt; **Nastavení** &gt; **DPH** &gt; **Pravidla pro stornovací poplatek**) je možné definovat pravidla pro účely nákupu a prodeje.</span><span class="sxs-lookup"><span data-stu-id="3634f-140">On the **Reverse charge rules** page (**Tax** &gt; **Setup** &gt; **Sales tax** &gt; **Reverse charge rules**), you can define the applicability rules for purchase and sales purposes.</span></span> <span data-ttu-id="3634f-141">Je možné nakonfigurovat sadu pravidel pro platnost mechanismu reverse charge.</span><span class="sxs-lookup"><span data-stu-id="3634f-141">You can configure a set of reverse charge applicability rules.</span></span> <span data-ttu-id="3634f-142">U každého pravidla je třeba nastavit tato pole:</span><span class="sxs-lookup"><span data-stu-id="3634f-142">For each rule, set the following fields:</span></span>

- <span data-ttu-id="3634f-143">**Typ dokumentu** – vyberte možnost **Nákupní objednávka**, **Deník faktur dodavatele**, **Prodejní objednávka**, **Volná faktura**, **Deník faktur odběratele** a/nebo **Faktura dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="3634f-143">**Document type** – Select **Purchase order**, **Vendor invoice journal**, **Sales order**, **Free text invoice**, **Customer invoice journal**, and/or **Vendor invoice**.</span></span>
- <span data-ttu-id="3634f-144">**Typ země/oblasti partnera** – vyberte možnost **Domácí**, **EU** nebo **Cizí**.</span><span class="sxs-lookup"><span data-stu-id="3634f-144">**Country/region type of the partner** – Select **Domestic**, **EU**, or **Foreign**.</span></span> <span data-ttu-id="3634f-145">Pokud lze pravidlo použít pro všechny partnery (bez ohledu na zemi či oblast, kde se adresa nachází), vyberte možnost **Vše**.</span><span class="sxs-lookup"><span data-stu-id="3634f-145">Alternatively, if the rule can be applied to all trade partners, regardless of the country or region of their address, select **All**.</span></span>
- <span data-ttu-id="3634f-146">**Domácí adresa dodání** – zaškrtnutím tohoto políčka použijete pravidlo u dodávek ve stejné zemi nebo oblasti.</span><span class="sxs-lookup"><span data-stu-id="3634f-146">**Domestic delivery address** – Select this check box to apply the rule to deliveries within the same country or region.</span></span> <span data-ttu-id="3634f-147">U typů dokumentů **Deník faktur dodavatele** a **Deník faktur odběratele** nelze toto políčko zaškrtnout.</span><span class="sxs-lookup"><span data-stu-id="3634f-147">This check box can't be selected for the **Vendor invoice journal** and **Customer invoice journal** document types.</span></span>
- <span data-ttu-id="3634f-148">**Stornovací poplatek – skupina položek** – vyberte skupinu, pro kterou má pravidlo platit.</span><span class="sxs-lookup"><span data-stu-id="3634f-148">**Reverse charge item group** – Select the group that the rule can be applied to.</span></span>
- <span data-ttu-id="3634f-149">**Prahová částka** – mechanismus reverse charge se u faktury použije pouze v případě, že hodnota položek nebo služeb ve skupině překročí zde zadanou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="3634f-149">**Threshold amount** – The Reverse Charge schema is applied to an invoice only if the value of items and/or services that are included in the reverse charge item group exceeds the limit that you specify here.</span></span>

<span data-ttu-id="3634f-150">Období platnosti pravidla lze také nastavit pomocí polí **Datum platnosti** a **Datum vypršení platnosti**.</span><span class="sxs-lookup"><span data-stu-id="3634f-150">You can also use the **Effective date** and **Expiration date** fields to define the period when the rule is effective.</span></span>

<span data-ttu-id="3634f-151">Je také možné určit, zda se má zobrazit oznámení a zda se má a řádek dokumentu aktualizovat podle výchozí skupiny DPH pro reverse charge, pokud bude splněna příslušná podmínka.</span><span class="sxs-lookup"><span data-stu-id="3634f-151">Additionally, you can specify whether a notification appears and the document line is updated with the default reverse charge sales tax group if the condition for that document line is met.</span></span> <span data-ttu-id="3634f-152">Existují tyto možnosti:</span><span class="sxs-lookup"><span data-stu-id="3634f-152">The following options are available:</span></span>

- <span data-ttu-id="3634f-153">**Žádné** – řádek dokumentu se neaktualizuje.</span><span class="sxs-lookup"><span data-stu-id="3634f-153">**None** – The document line isn't updated.</span></span>
- <span data-ttu-id="3634f-154">**Výzva** – zobrazí se oznámení s potvrzením o použitelnosti mechanismu reverse charge.</span><span class="sxs-lookup"><span data-stu-id="3634f-154">**Prompt** – A notification appears to confirm that the reverse charge can be applied.</span></span>
- <span data-ttu-id="3634f-155">**Nastavit** – řádek dokumentu se aktualizuje bez oznámení.</span><span class="sxs-lookup"><span data-stu-id="3634f-155">**Set** – The document line is updated without additional notification.</span></span>

## <a name="set-up-default-parameters"></a><span data-ttu-id="3634f-156">Nastavení výchozích parametrů</span><span class="sxs-lookup"><span data-stu-id="3634f-156">Set up default parameters</span></span>
<span data-ttu-id="3634f-157">Funkci reverse charge VAT aktivujete tak, že na stránce **Parametry hlavní knihy** na kartě **Stornovací poplatek** nastavíte možnost **Povolit stornovací poplatek** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="3634f-157">To enable the functionality for reverse charge VAT, on the **General ledger parameters** page, on the **Reverse charge** tab, set the **Enable reverse charge** option to **Yes**.</span></span> <span data-ttu-id="3634f-158">V polích **Nákupní objednávka – skupina DPH** a **Prodejní objednávka – skupina DPH** vyberte výchozí skupiny DPH.</span><span class="sxs-lookup"><span data-stu-id="3634f-158">In the **Purchase order sales tax group** and **Sales order tax group** fields, select the default sales tax groups.</span></span> <span data-ttu-id="3634f-159">Při splnění podmínky použitelnosti přenesení daňové povinnosti se u řádku nákupní nebo prodejní objednávky aktualizují tyto skupiny DPH.</span><span class="sxs-lookup"><span data-stu-id="3634f-159">When a reverse charge applicability condition is met, the sales or purchase order line is updated with these sales tax groups.</span></span>

## <a name="reverse-charge-on-a-sales-invoice"></a><span data-ttu-id="3634f-160">Reverse charge u prodejní faktury</span><span class="sxs-lookup"><span data-stu-id="3634f-160">Reverse charge on a sales invoice</span></span>
<span data-ttu-id="3634f-161">U prodeje s mechanismem reverse charge prodávající neúčtuje DPH.</span><span class="sxs-lookup"><span data-stu-id="3634f-161">For sales under the Reverse Charge schema, the seller doesn't charge VAT.</span></span> <span data-ttu-id="3634f-162">Místo toho jsou na faktuře uvedeny položky, na které se vztahuje reverse charge, a celková částka DPH pro reverse charge.</span><span class="sxs-lookup"><span data-stu-id="3634f-162">Instead, the invoice indicates both the items that are subject to the reverse charge VAT and the total amount of the reverse charge VAT.</span></span>

<span data-ttu-id="3634f-163">Při zaúčtování prodejní faktury s reverse charge mají transakce DPH směr **DPH na výstupu** a nulové DPH a je zaškrtnuto políčko **Stornovací poplatek**.</span><span class="sxs-lookup"><span data-stu-id="3634f-163">When a sales invoice that has the reverse charge is posted, the sales tax transactions have the **Sales tax payable** tax direction and zero sales tax, and the **Reverse charge** check box is selected.</span></span>

## <a name="reverse-charge-on-a-purchase-invoice"></a><span data-ttu-id="3634f-164">Reverse charge u nákupní faktury</span><span class="sxs-lookup"><span data-stu-id="3634f-164">Reverse charge on a purchase invoice</span></span>
<span data-ttu-id="3634f-165">U nákupů s mechanismem reverse charge funguje kupující, který přijímá fakturu s reverse charge, pro účely účetnictví DPH jako kupující i prodávající.</span><span class="sxs-lookup"><span data-stu-id="3634f-165">For purchases under the Reverse Charge schema, the purchaser who receives the invoice that has the reverse charge acts as a buyer and a seller for VAT accounting purposes.</span></span>

<span data-ttu-id="3634f-166">Při zaúčtování nákupní faktury s reverse charge se vytvoří dvě transakce DPH.</span><span class="sxs-lookup"><span data-stu-id="3634f-166">When a purchase invoice that has the reverse charge is posted, two sales tax transactions are created.</span></span> <span data-ttu-id="3634f-167">Jedna transakce má směr **DPH na vstupu**.</span><span class="sxs-lookup"><span data-stu-id="3634f-167">One transaction has the **Sales tax receivable** tax direction.</span></span> <span data-ttu-id="3634f-168">Druhá transakce má směr **DPH na výstupu** a je u ní zaškrtnuto políčko **Stornovací poplatek**.</span><span class="sxs-lookup"><span data-stu-id="3634f-168">The other transaction has the **Sales tax payable** tax direction, and the **Reverse charge** check box is selected.</span></span>

<span data-ttu-id="3634f-169">Následující snímek obrazovky má jedna transakce směr **DPH na vstupu** směru a druhá **DPH na výstupu**.</span><span class="sxs-lookup"><span data-stu-id="3634f-169">In the following screenshot, one transaction has the **Sales tax receivable** direction, and the other transaction has the **Sales tax payable** direction.</span></span> 

![Zaúčtování DPH](media/apac-sau-posted-sales-tax.png)
