---
title: Limity pro místo uskladnění
description: Toto téma popisuje funkčnost limitů pro místo uskladnění.
author: perlynne
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 208662f38b06b1f230bdde5247946a9fefd57cea
ms.sourcegitcommit: d2dea9ce480f35d0c0b10615c18862695e107d55
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/23/2020
ms.locfileid: "4607272"
---
# <a name="location-stocking-limits"></a><span data-ttu-id="2f9da-103">Limity pro místo uskladnění</span><span class="sxs-lookup"><span data-stu-id="2f9da-103">Location stocking limits</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f9da-104">Můžete použít stránku **Limity pro místo uskladnění** (**Řízení skladu \> Nastavení \> Sklad \> Limity pro místo uskladnění**) ke kontrole kapacity vytížení v místech uskladnění, aniž byste museli používat pokročilejší procesy pro objemové výpočty fyzických produktů.</span><span class="sxs-lookup"><span data-stu-id="2f9da-104">You can use the **Location stocking limits** page (**Warehouse management \> Setup \> Warehouse \> Location stocking limits**) to control the load capacity at warehouse locations without having to use the more advanced processes for volumetric calculations of physical products.</span></span>

<span data-ttu-id="2f9da-105">Účelem limitů pro místo uskladnění je vyhodnotit maximální množství, které může skladové místo obsahovat.</span><span class="sxs-lookup"><span data-stu-id="2f9da-105">The purpose of location stocking limits is to evaluate the maximum quantity that a location can contain.</span></span> <span data-ttu-id="2f9da-106">Tuto funkci můžete nastavit na kterékoli ze tří úrovní, z nichž každá má svou vlastní kartu na stránce **Limity pro místo uskladnění**:</span><span class="sxs-lookup"><span data-stu-id="2f9da-106">You can set up the feature on any of three levels, each of which has its own tab on the **Location stocking limits** page:</span></span>

- <span data-ttu-id="2f9da-107">Produkty</span><span class="sxs-lookup"><span data-stu-id="2f9da-107">Products</span></span>
- <span data-ttu-id="2f9da-108">Varianty produktu</span><span class="sxs-lookup"><span data-stu-id="2f9da-108">Product variants</span></span>
- <span data-ttu-id="2f9da-109">Typy kontejneru</span><span class="sxs-lookup"><span data-stu-id="2f9da-109">Container types</span></span>

<span data-ttu-id="2f9da-110">Pro každou úroveň můžete definovat různé hodnoty polí.</span><span class="sxs-lookup"><span data-stu-id="2f9da-110">For each level, you can define different field values.</span></span> <span data-ttu-id="2f9da-111">Systém poté vyhodnotí kapacitu konkrétního skladového místa na základě hodnot **Množství** a **Jednotka** pro každý řádek.</span><span class="sxs-lookup"><span data-stu-id="2f9da-111">The system will then evaluate the capacity of a specific location, based on the **Quantity** and **Unit** values for each row.</span></span> <span data-ttu-id="2f9da-112">Nejprve vybere nejpodrobnější odpovídající záznam.</span><span class="sxs-lookup"><span data-stu-id="2f9da-112">It will select the most detailed matching record first.</span></span> <span data-ttu-id="2f9da-113">Například řádek, který má hodnotu v poli **ID profilu skladového místa**, bude vyhodnocen před řádkem, který má hodnotu pouze v poli **Sklad**.</span><span class="sxs-lookup"><span data-stu-id="2f9da-113">For example, a row that has a value in the **Location profile ID** field will be evaluated before a row that has a value only in the **Warehouse** field.</span></span> <span data-ttu-id="2f9da-114">Zbývající kapacita bude rovněž hodnocena na základě hodnoty **Množství** pro použitý záznam limitu pro místo uskladnění.</span><span class="sxs-lookup"><span data-stu-id="2f9da-114">The remaining capacity will also be evaluated, based on the **Quantity** value for the location stocking limit record that is used.</span></span>

<span data-ttu-id="2f9da-115">V sekci **Produkty** stránky můžete definovat následující hodnoty polí pro hledání limitů pro místo uskladnění:</span><span class="sxs-lookup"><span data-stu-id="2f9da-115">In the **Products** section of the page, you can define the following field values for the search for location stocking limits:</span></span>

- <span data-ttu-id="2f9da-116">Sklad</span><span class="sxs-lookup"><span data-stu-id="2f9da-116">Warehouse</span></span>
- <span data-ttu-id="2f9da-117">ID profilu skladového místa</span><span class="sxs-lookup"><span data-stu-id="2f9da-117">Location profile ID</span></span>
- <span data-ttu-id="2f9da-118">Skladové místo</span><span class="sxs-lookup"><span data-stu-id="2f9da-118">Location</span></span>
- <span data-ttu-id="2f9da-119">ID kategorie velikosti balení</span><span class="sxs-lookup"><span data-stu-id="2f9da-119">Pack size category ID</span></span>
- <span data-ttu-id="2f9da-120">Č. položky</span><span class="sxs-lookup"><span data-stu-id="2f9da-120">Item number</span></span>
- <span data-ttu-id="2f9da-121">Jednotka</span><span class="sxs-lookup"><span data-stu-id="2f9da-121">Unit</span></span>

> [!NOTE]
> <span data-ttu-id="2f9da-122">Nemusíte definovat hodnotu **Jednotka** pro každý záznam limitu pro místo uskladnění.</span><span class="sxs-lookup"><span data-stu-id="2f9da-122">You don't have to define a **Unit** value for each location stocking limit record.</span></span> <span data-ttu-id="2f9da-123">Výpočty kapacity místa budou založeny na množství jednotek zásob.</span><span class="sxs-lookup"><span data-stu-id="2f9da-123">The location capacity calculations will be based on the inventory unit quantities.</span></span> <span data-ttu-id="2f9da-124">Pokud není pro použitou hodnotu definován žádný převod jednotek, bude přeskočen záznam limitu pro místo uskladnění, jako by pro něj byla definována jiná hodnota **Číslo položky**.</span><span class="sxs-lookup"><span data-stu-id="2f9da-124">If no unit conversion is defined for a value that is used, the location stocking limit record will be skipped, as if another **Item number** value is defined for it.</span></span>

## <a name="example--purchase-order-receiving"></a><span data-ttu-id="2f9da-125">Příklad - Přijetí nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="2f9da-125">Example – Purchase order receiving</span></span>

<span data-ttu-id="2f9da-126">Tento příklad je založen na čisté ukázkové sadě dat *USMF*, kde jsou na kartě **Varianty produktu** stránky **Limity pro místo uskladnění** nastaveny následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="2f9da-126">This example is based on a clean *USMF* demo data set, where the following values are set on the **Product variants** tab of the **Location stocking limits** page.</span></span>

| <span data-ttu-id="2f9da-127">Sklad</span><span class="sxs-lookup"><span data-stu-id="2f9da-127">Warehouse</span></span> | <span data-ttu-id="2f9da-128">ID profilu skladového místa</span><span class="sxs-lookup"><span data-stu-id="2f9da-128">Location profile ID</span></span> | <span data-ttu-id="2f9da-129">Č. položky</span><span class="sxs-lookup"><span data-stu-id="2f9da-129">Item number</span></span> | <span data-ttu-id="2f9da-130">Velikost</span><span class="sxs-lookup"><span data-stu-id="2f9da-130">Size</span></span> | <span data-ttu-id="2f9da-131">Množství</span><span class="sxs-lookup"><span data-stu-id="2f9da-131">Quantity</span></span> | <span data-ttu-id="2f9da-132">Jednotka</span><span class="sxs-lookup"><span data-stu-id="2f9da-132">Unit</span></span> |
|-----------|---------------------|-------------|------|----------|------|
| <span data-ttu-id="2f9da-133">24</span><span class="sxs-lookup"><span data-stu-id="2f9da-133">24</span></span>        | <span data-ttu-id="2f9da-134">FLOOR</span><span class="sxs-lookup"><span data-stu-id="2f9da-134">FLOOR</span></span>               | <span data-ttu-id="2f9da-135">D0013</span><span class="sxs-lookup"><span data-stu-id="2f9da-135">D0013</span></span>       | <span data-ttu-id="2f9da-136">mil.</span><span class="sxs-lookup"><span data-stu-id="2f9da-136">M</span></span>    | <span data-ttu-id="2f9da-137">300</span><span class="sxs-lookup"><span data-stu-id="2f9da-137">300</span></span>      | <span data-ttu-id="2f9da-138">Ea</span><span class="sxs-lookup"><span data-stu-id="2f9da-138">Ea</span></span>   |
| <span data-ttu-id="2f9da-139">24</span><span class="sxs-lookup"><span data-stu-id="2f9da-139">24</span></span>        | <span data-ttu-id="2f9da-140">FLOOR</span><span class="sxs-lookup"><span data-stu-id="2f9da-140">FLOOR</span></span>               | <span data-ttu-id="2f9da-141">D0013</span><span class="sxs-lookup"><span data-stu-id="2f9da-141">D0013</span></span>       | <span data-ttu-id="2f9da-142">L</span><span class="sxs-lookup"><span data-stu-id="2f9da-142">L</span></span>    | <span data-ttu-id="2f9da-143">240</span><span class="sxs-lookup"><span data-stu-id="2f9da-143">240</span></span>      | <span data-ttu-id="2f9da-144">Ea</span><span class="sxs-lookup"><span data-stu-id="2f9da-144">Ea</span></span>   |
| <span data-ttu-id="2f9da-145">24</span><span class="sxs-lookup"><span data-stu-id="2f9da-145">24</span></span>        | <span data-ttu-id="2f9da-146">FLOOR</span><span class="sxs-lookup"><span data-stu-id="2f9da-146">FLOOR</span></span>               | <span data-ttu-id="2f9da-147">D0013</span><span class="sxs-lookup"><span data-stu-id="2f9da-147">D0013</span></span>       | <span data-ttu-id="2f9da-148">S</span><span class="sxs-lookup"><span data-stu-id="2f9da-148">S</span></span>    | <span data-ttu-id="2f9da-149">360</span><span class="sxs-lookup"><span data-stu-id="2f9da-149">360</span></span>      | <span data-ttu-id="2f9da-150">Ea</span><span class="sxs-lookup"><span data-stu-id="2f9da-150">Ea</span></span>   |

<span data-ttu-id="2f9da-151">Pro produkty jsou nastaveny různé varianty produktu měrných jednotek.</span><span class="sxs-lookup"><span data-stu-id="2f9da-151">Different unit of measure product variants are set up for the products.</span></span> <span data-ttu-id="2f9da-152">Tyto varianty jsou v souladu s limity pro místo uskladnění pro tři palety (PL):</span><span class="sxs-lookup"><span data-stu-id="2f9da-152">These variants are aligned with the location stocking limits for three pallets (PL):</span></span>

- <span data-ttu-id="2f9da-153">**Velikost M:** 1 PL = 100 každá (Ea)</span><span class="sxs-lookup"><span data-stu-id="2f9da-153">**Size M:** 1 PL = 100 each (Ea)</span></span>
- <span data-ttu-id="2f9da-154">**Velikost L:** 1 PL = 80 Ea</span><span class="sxs-lookup"><span data-stu-id="2f9da-154">**Size L:** 1 PL = 80 Ea</span></span>
- <span data-ttu-id="2f9da-155">**Velikost S:** 1 PL = 120 Ea</span><span class="sxs-lookup"><span data-stu-id="2f9da-155">**Size S:** 1 PL = 120 Ea</span></span>

<span data-ttu-id="2f9da-156">Proto každé místo, kde je hodnota **ID profilu skladového místa** nastavena na *FLOOR* může nést *3* *PL* čísla položky *D0013*.</span><span class="sxs-lookup"><span data-stu-id="2f9da-156">Therefore, each location where the **Location profile ID** value is set to *FLOOR* can carry *3* *PL* of item number *D0013*.</span></span>

### <a name="prepare-for-the-example"></a><span data-ttu-id="2f9da-157">Připravte se na příklad</span><span class="sxs-lookup"><span data-stu-id="2f9da-157">Prepare for the example</span></span>

<span data-ttu-id="2f9da-158">V tomto příkladu spustíte tok přijímání nákupní objednávky pro dva řádky.</span><span class="sxs-lookup"><span data-stu-id="2f9da-158">In this example, you will run a purchase order receiving flow for two lines.</span></span> <span data-ttu-id="2f9da-159">Nejprve však musíte aktualizovat ukázková data následujícím způsobem, aby bylo zajištěno, že umístění umožňuje kombinované položky, pouze prázdná umístění *FL-002* přes *FL-004* se použijí a neexistuje žádná otevřená příchozí práce.</span><span class="sxs-lookup"><span data-stu-id="2f9da-159">However, you must first update the demo data in the following way to ensure that the locations allow mixed items to be carried, only the empty locations *FL-002* through *FL-004* are used, and there is no open inbound work.</span></span>

1. <span data-ttu-id="2f9da-160">Pro umístění *FL-001* změňte hodnotu pole **Profil umístění** z *FLOOR* na *FLOOR-05*.</span><span class="sxs-lookup"><span data-stu-id="2f9da-160">For location *FL-001*, change the value of the **Location profile** field from *FLOOR* to *FLOOR-05*.</span></span>
1. <span data-ttu-id="2f9da-161">Pro profil místa *FLOOR* nastavte možnost **Povolit smíšené položky** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="2f9da-161">For the *FLOOR* location profile, set the **Allow mixed items** option to *Yes*.</span></span>
1. <span data-ttu-id="2f9da-162">Vytvořte nákupní objednávku, který má následující dva řádky:</span><span class="sxs-lookup"><span data-stu-id="2f9da-162">Create a purchase order that has the following two lines.</span></span>

    | <span data-ttu-id="2f9da-163">Sklad</span><span class="sxs-lookup"><span data-stu-id="2f9da-163">Warehouse</span></span> | <span data-ttu-id="2f9da-164">Č. položky</span><span class="sxs-lookup"><span data-stu-id="2f9da-164">Item number</span></span> | <span data-ttu-id="2f9da-165">Velikost</span><span class="sxs-lookup"><span data-stu-id="2f9da-165">Size</span></span> | <span data-ttu-id="2f9da-166">Množství</span><span class="sxs-lookup"><span data-stu-id="2f9da-166">Quantity</span></span> | <span data-ttu-id="2f9da-167">Jednotka</span><span class="sxs-lookup"><span data-stu-id="2f9da-167">Unit</span></span> |
    |-----------|-------------|------|----------|------|
    | <span data-ttu-id="2f9da-168">24</span><span class="sxs-lookup"><span data-stu-id="2f9da-168">24</span></span>        | <span data-ttu-id="2f9da-169">D0013</span><span class="sxs-lookup"><span data-stu-id="2f9da-169">D0013</span></span>       | <span data-ttu-id="2f9da-170">S</span><span class="sxs-lookup"><span data-stu-id="2f9da-170">S</span></span>    | <span data-ttu-id="2f9da-171">4</span><span class="sxs-lookup"><span data-stu-id="2f9da-171">4</span></span>        | <span data-ttu-id="2f9da-172">PL</span><span class="sxs-lookup"><span data-stu-id="2f9da-172">PL</span></span>   |
    | <span data-ttu-id="2f9da-173">24</span><span class="sxs-lookup"><span data-stu-id="2f9da-173">24</span></span>        | <span data-ttu-id="2f9da-174">D0013</span><span class="sxs-lookup"><span data-stu-id="2f9da-174">D0013</span></span>       | <span data-ttu-id="2f9da-175">L</span><span class="sxs-lookup"><span data-stu-id="2f9da-175">L</span></span>    | <span data-ttu-id="2f9da-176">4</span><span class="sxs-lookup"><span data-stu-id="2f9da-176">4</span></span>        | <span data-ttu-id="2f9da-177">PL</span><span class="sxs-lookup"><span data-stu-id="2f9da-177">PL</span></span>   |

### <a name="process-the-example"></a><span data-ttu-id="2f9da-178">Zpracování příkladu</span><span class="sxs-lookup"><span data-stu-id="2f9da-178">Process the example</span></span>

<span data-ttu-id="2f9da-179">Nejprve obdržíte množství *4* jednotky *PL* ve velikosti *S* a zkontrolujte umístění řádku vložení pro vytvořenou práci.</span><span class="sxs-lookup"><span data-stu-id="2f9da-179">You will first receive a quantity of *4* of unit *PL* in size *S*, and review the put line locations for the work that is created.</span></span> <span data-ttu-id="2f9da-180">Pak obdržíte množství *4* jednotky *PL* ve velikosti *L* a zkontrolujte umístění řádku vložení pro vytvořenou práci.</span><span class="sxs-lookup"><span data-stu-id="2f9da-180">You will then receive a quantity of *4* of unit *PL* in size *L*, and review the put line locations for the work that is created.</span></span>

1. <span data-ttu-id="2f9da-181">Ve skladovací aplikaci se přihlaste pomocí čísla *24* ID uživatele a *1* jako heslo.</span><span class="sxs-lookup"><span data-stu-id="2f9da-181">In the warehouse app, sign in by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="2f9da-182">Vyberte **Příchozí** \> **Příjem nákupu**..</span><span class="sxs-lookup"><span data-stu-id="2f9da-182">Select **Inbound** \> **Purchase Receive**.</span></span>
1. <span data-ttu-id="2f9da-183">Přijměte *4* *PL* čísla položky *D0013* ve velikosti *S*.</span><span class="sxs-lookup"><span data-stu-id="2f9da-183">Receive *4* *PL* of item number *D0013* in size *S*.</span></span>
1. <span data-ttu-id="2f9da-184">Zkontrolujte vytvořenou práci založení.</span><span class="sxs-lookup"><span data-stu-id="2f9da-184">Review the putaway work that was created.</span></span> <span data-ttu-id="2f9da-185">Měl by se vám zobrazit následující výsledek:</span><span class="sxs-lookup"><span data-stu-id="2f9da-185">You should see the following result:</span></span>

    - <span data-ttu-id="2f9da-186">3 PL -\> FL-002</span><span class="sxs-lookup"><span data-stu-id="2f9da-186">3 PL -\> FL-002</span></span>
    - <span data-ttu-id="2f9da-187">1 PL -\> FL-003</span><span class="sxs-lookup"><span data-stu-id="2f9da-187">1 PL -\> FL-003</span></span>

1. <span data-ttu-id="2f9da-188">Přijměte *4* *PL* čísla položky *D0013* ve velikosti *L*.</span><span class="sxs-lookup"><span data-stu-id="2f9da-188">Receive *4* *PL* of item number *D0013* in size *L*.</span></span>
1. <span data-ttu-id="2f9da-189">Zkontrolujte vytvořenou práci založení.</span><span class="sxs-lookup"><span data-stu-id="2f9da-189">Review the putaway work that was created.</span></span> <span data-ttu-id="2f9da-190">Měl by se vám zobrazit následující výsledek:</span><span class="sxs-lookup"><span data-stu-id="2f9da-190">You should see the following result:</span></span>

    - <span data-ttu-id="2f9da-191">1 PL -\> FL-003</span><span class="sxs-lookup"><span data-stu-id="2f9da-191">1 PL -\> FL-003</span></span>
    - <span data-ttu-id="2f9da-192">3 PL -\> FL-004</span><span class="sxs-lookup"><span data-stu-id="2f9da-192">3 PL -\> FL-004</span></span>

<span data-ttu-id="2f9da-193">Na základě výsledků můžete dojít k závěru, že se systému nepodařilo přidělit správná místa založení.</span><span class="sxs-lookup"><span data-stu-id="2f9da-193">Based on the results, you might conclude that the system failed to allocate the correct putaway locations.</span></span> <span data-ttu-id="2f9da-194">V opačném případě, proč systém přidal pouze *1* *PL* velikosti *L* na místo *FL-003* v posledním kroku, a nikoliv *2* *PL*?</span><span class="sxs-lookup"><span data-stu-id="2f9da-194">Otherwise, why did the system add only *1* *PL* of size *L* to location *FL-003* in the last step, not *2* *PL*?</span></span> <span data-ttu-id="2f9da-195">Proč tam není celkem *3* *PL* pro založení na toto místo?</span><span class="sxs-lookup"><span data-stu-id="2f9da-195">That is, why isn't there is a total of *3* *PL* for putaway to that location?</span></span>

<span data-ttu-id="2f9da-196">Chcete-li vysvětlit toto zjevné selhání, musíte porozumět kritériím výběru limitů pro místo uskladnění.</span><span class="sxs-lookup"><span data-stu-id="2f9da-196">To explain this apparent failure, you must understand the selection criteria for the location stocking limits.</span></span> <span data-ttu-id="2f9da-197">Systém vybere nejpodrobnější odpovídající záznam.</span><span class="sxs-lookup"><span data-stu-id="2f9da-197">The system selects the most detailed matching record.</span></span> <span data-ttu-id="2f9da-198">V tomto příkladu je nejpodrobnějším odpovídajícím záznamem řádek, kde hodnota **Velikost** je *L*, **Množství** je *240* a **Jednotka** je *Ea*.</span><span class="sxs-lookup"><span data-stu-id="2f9da-198">In this example, the most detailed matching record is the line where the **Size** value is *L*, the **Quantity** value is *240*, and the **Unit** value is *Ea*.</span></span> <span data-ttu-id="2f9da-199">Protože již máte otevřenou práci z předchozího přijetí množství *120* *Ea* velikosti *S*, zbývající kapacita se vypočítá jako *240* – *120* = *120* *Ea*.</span><span class="sxs-lookup"><span data-stu-id="2f9da-199">Because you already have open work from the previous receipt of a quantity of *120* *Ea* of size *S*, the remaining capacity is calculated as *240* – *120* = *120* *Ea*.</span></span> <span data-ttu-id="2f9da-200">Zbývající kapacita tedy může být pouze *1* *PL* of *80* *Ea*.</span><span class="sxs-lookup"><span data-stu-id="2f9da-200">Therefore, the remaining capacity can carry only *1* *PL* of *80* *Ea*.</span></span>

> [!NOTE]
> <span data-ttu-id="2f9da-201">Limity pro místo uskladnění nemůžete použít například ke kontrole doplnění položek, které mají ve stejném umístění různá množství.</span><span class="sxs-lookup"><span data-stu-id="2f9da-201">You can't use location stocking limits to control, for example, the replenishment of items that have different quantities in the same location.</span></span> <span data-ttu-id="2f9da-202">V takovém případě použijte *šablonu doplnění*.</span><span class="sxs-lookup"><span data-stu-id="2f9da-202">In this case, use a *replenishment template*.</span></span>