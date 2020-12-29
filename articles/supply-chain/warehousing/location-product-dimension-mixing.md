---
title: Směšování dimenzí produktu na skladovém místě
description: Toto téma poskytuje informace o míchání dimenzí produktů na skladovém místě. Tato funkce profilu skladového místa pomáhá zlepšit správu skladového místa, pokud se používají varianty produktu nebo produkty, které mají různé dimenze, jako například v módním průmyslu. Funkce umožní rozhodnout, zda je možné konfigurace, barvy, styly a velikosti pro konkrétní profil skladového místa míchat, nebo zda lze na jedno skladové místo umístit pouze jednu dimenzi nebo kombinaci.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 73519f3fe79d3d7d917d3044255f735640b8ccfd
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424136"
---
# <a name="location-product-dimension-mixing"></a><span data-ttu-id="4c716-105">Směšování dimenzí produktu na skladovém místě</span><span class="sxs-lookup"><span data-stu-id="4c716-105">Location product dimension mixing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c716-106">Míchání dimenzí produktu na skladovém místě je funkce profilu skladového místa, jež pomáhá zlepšit správu skladového místa, pokud se používají varianty produktu nebo produkty, které mají dimenze, jako například v módním průmyslu.</span><span class="sxs-lookup"><span data-stu-id="4c716-106">Location product dimension mixing is location profile functionality that helps improve location management when product variants or products that have dimensions are used, such as in the fashion industry.</span></span> <span data-ttu-id="4c716-107">Funkce umožní rozhodnout, zda je možné konfigurace, barvy, styly a velikosti pro konkrétní profil skladového místa míchat, nebo zda lze na jedno skladové místo umístit pouze jednu dimenzi nebo kombinaci.</span><span class="sxs-lookup"><span data-stu-id="4c716-107">It lets you decide whether configurations, colors, styles, and sizes can be mixed for a specific location profile, or whether just one of these dimensions or a combination of them can be put to the same location.</span></span>

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a><span data-ttu-id="4c716-108">Zapnutí funkce míchání dimenzí produktů na skladovém místě</span><span class="sxs-lookup"><span data-stu-id="4c716-108">Turn on the Location product dimension mixing feature</span></span>

<span data-ttu-id="4c716-109">Než můžete použít funkci Míchání dimenzí rozměrů produktů na skladovém místě, musíte ji v systému zapnout.</span><span class="sxs-lookup"><span data-stu-id="4c716-109">Before you can use location product dimension mixing, the feature must be turned on in your system.</span></span> <span data-ttu-id="4c716-110">Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba.</span><span class="sxs-lookup"><span data-stu-id="4c716-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="4c716-111">Funkce je zde uvedena následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="4c716-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="4c716-112">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="4c716-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="4c716-113">**Název funkce:** *Míchání dimenzí produktu na skladovém místě*</span><span class="sxs-lookup"><span data-stu-id="4c716-113">**Feature name:** *Location product dimension mixing*</span></span>

## <a name="setup"></a><span data-ttu-id="4c716-114">Nastavení</span><span class="sxs-lookup"><span data-stu-id="4c716-114">Setup</span></span>

<span data-ttu-id="4c716-115">Každé skladové místo ve skladu musí mít přidružený profil skladového místa, který popisuje vlastnosti skladového místa.</span><span class="sxs-lookup"><span data-stu-id="4c716-115">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location.</span></span> <span data-ttu-id="4c716-116">Na všech skladových místech, jež používají stejný profil skladového místa, proto bude možné po nastavení využívat míchání dimenzí produktů na skladovém místě.</span><span class="sxs-lookup"><span data-stu-id="4c716-116">Therefore, all locations that use the same location profile will be able to allow product dimension mixing after it has been set up.</span></span>

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a><span data-ttu-id="4c716-117">Konfigurace profilů skladových míst, aby umožňovaly míchání dimenzí produktů</span><span class="sxs-lookup"><span data-stu-id="4c716-117">Configure location profiles to allow product dimension mixing</span></span>

1. <span data-ttu-id="4c716-118">Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Profily skladových míst**.</span><span class="sxs-lookup"><span data-stu-id="4c716-118">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="4c716-119">V seznamu profilů polohy vyberte možnost **HROMADNĚ**.</span><span class="sxs-lookup"><span data-stu-id="4c716-119">In the list of location profiles, select **BULK**.</span></span>
1. <span data-ttu-id="4c716-120">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="4c716-120">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4c716-121">Na záložce s náhledem **Všeobecné** nastavte u položky **Povolit míchání dimenzí produktu na skladovém místě** hodnotu *Ano*.</span><span class="sxs-lookup"><span data-stu-id="4c716-121">On the **General** FastTab, set the **Enable location product dimension specific mixing** option to *Yes*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4c716-122">U této možnosti můžete nastavit hodnotu *Ano*, pouze když je u možnosti **Povolit míchání položek** nastavena možnost *Ne*.</span><span class="sxs-lookup"><span data-stu-id="4c716-122">You can set this option to *Yes* only if the **Allow mixed items** option is set to *No*.</span></span>

1. <span data-ttu-id="4c716-123">Na záložce s náhledem **Povolit míchání položek** nastavte u položky **Velikost** hodnotu *Ano*.</span><span class="sxs-lookup"><span data-stu-id="4c716-123">On the **Allowed product dimension mixing** FastTab, set the **Size** option to *Yes*.</span></span> <span data-ttu-id="4c716-124">Ve scénáři popsaném v tomto tématu lze míchání provádět pouze u produktů, které se liší dimenzí **Velikost**.</span><span class="sxs-lookup"><span data-stu-id="4c716-124">In the scenario that is described in this topic, mixing can be done only for products that have different **Size** dimensions.</span></span> <span data-ttu-id="4c716-125">K dispozici jsou však také další možnosti.</span><span class="sxs-lookup"><span data-stu-id="4c716-125">However, other options are also available.</span></span>
1. <span data-ttu-id="4c716-126">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="4c716-126">Select **Save**.</span></span>

### <a name="create-a-new-product-master-and-product-variants"></a><span data-ttu-id="4c716-127">Vytvoření nového základního produktu a variant produktů</span><span class="sxs-lookup"><span data-stu-id="4c716-127">Create a new product master and product variants</span></span>

1. <span data-ttu-id="4c716-128">Přejděte do nabídky **Řízení informací o produktech \> Produkty \> Základní produkty**.</span><span class="sxs-lookup"><span data-stu-id="4c716-128">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="4c716-129">V podokně akcí vyberte možnost **Nový** a vytvořte základní produkt.</span><span class="sxs-lookup"><span data-stu-id="4c716-129">On the Action Pane, select **New** to create a product master.</span></span>
1. <span data-ttu-id="4c716-130">V dialogovém okně **Nový produkt** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="4c716-130">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="4c716-131">**Typ produktu:** *Položka*</span><span class="sxs-lookup"><span data-stu-id="4c716-131">**Product type:** *Item*</span></span>
    - <span data-ttu-id="4c716-132">**Podtyp produktu:** *Základní produkt*</span><span class="sxs-lookup"><span data-stu-id="4c716-132">**Product subtype:** *Product master*</span></span>
    - <span data-ttu-id="4c716-133">**Číslo produktu:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="4c716-133">**Product number:** *B0001*</span></span>
    - <span data-ttu-id="4c716-134">**Název produktu:** *B0001 Velikost*</span><span class="sxs-lookup"><span data-stu-id="4c716-134">**Product name:** *B0001 Size*</span></span>
    - <span data-ttu-id="4c716-135">**Skupina dimenzí produktů:** *Velikost*</span><span class="sxs-lookup"><span data-stu-id="4c716-135">**Product dimension group:** *Size*</span></span>
    - <span data-ttu-id="4c716-136">**Konfigurační technologie:** *Předdefinovaná varianta*</span><span class="sxs-lookup"><span data-stu-id="4c716-136">**Configuration technology:** *Predefined variant*</span></span>

1. <span data-ttu-id="4c716-137">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c716-137">Select **OK**.</span></span>
1. <span data-ttu-id="4c716-138">Na stránce **Podrobnosti produktu** nastavte na záložce s náhledem **Všeobecné** následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="4c716-138">On the **Product details** page, on the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="4c716-139">**Automaticky generovat varianty:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="4c716-139">**Generate variants automatically:** *Yes*</span></span>
    - <span data-ttu-id="4c716-140">**Velikostní skupina:** *CASUALDHIR*</span><span class="sxs-lookup"><span data-stu-id="4c716-140">**Size group:** *CASUALDHIR*</span></span>

1. <span data-ttu-id="4c716-141">Chcete-li zobrazit předdefinované varianty, vyberte v podokně Akce možnost **Varianty produktu**.</span><span class="sxs-lookup"><span data-stu-id="4c716-141">To view the predefined variants, on the Action Pane, select **Product variants**.</span></span>

    <span data-ttu-id="4c716-142">Zobrazí se stránka **Varianty produktu** a na ní seznam variant z konfigurace velikostní skupiny.</span><span class="sxs-lookup"><span data-stu-id="4c716-142">The **Product variants** page appears and shows a list of variants from the configuration of the size group.</span></span>

### <a name="release-products-to-the-usmf-company"></a><span data-ttu-id="4c716-143">Uvolnění produktů společností USMF</span><span class="sxs-lookup"><span data-stu-id="4c716-143">Release products to the USMF company</span></span>

1. <span data-ttu-id="4c716-144">V podokně Akce vyberte možnost **Uvolnit produkty**.</span><span class="sxs-lookup"><span data-stu-id="4c716-144">On the Action Pane, select **Release products**.</span></span>
1. <span data-ttu-id="4c716-145">Na stránce **Výběr produktů k uvolnění** si zkontrolujte, že je produkt číslo *B0001* v seznamu, poté vyberte možnost **Další**.</span><span class="sxs-lookup"><span data-stu-id="4c716-145">On the **Select products to release** page, confirm that product number *B0001* is in the list, and then select **Next**.</span></span>
1. <span data-ttu-id="4c716-146">Výběrem možnosti **Další** potvrzujete varianty produktu k uvolnění.</span><span class="sxs-lookup"><span data-stu-id="4c716-146">Select **Next** to confirm the product variants to release.</span></span>
1. <span data-ttu-id="4c716-147">Na stránce **Výběr společností k uvolnění** vyberte možnost *USMF*, poté výběr potvrďte kliknutím na **Další**.</span><span class="sxs-lookup"><span data-stu-id="4c716-147">On the **Select companies to release to** page, select *USMF*, and then select **Next** to confirm the selection.</span></span>
1. <span data-ttu-id="4c716-148">Na stránce **Potvrzení výběru** klikněte na **Dokončit**, tím se uvolnění dokončí.</span><span class="sxs-lookup"><span data-stu-id="4c716-148">On the **Confirm selection** page, select **Finish** to complete the release.</span></span>

    <span data-ttu-id="4c716-149">Zobrazí se zpráva „Operace dokončena“.</span><span class="sxs-lookup"><span data-stu-id="4c716-149">You receive an "Operation completed" message.</span></span>

### <a name="update-a-released-product-in-the-usmf-company"></a><span data-ttu-id="4c716-150">Aktualizace uvolněného produktu ve společnosti USMF</span><span class="sxs-lookup"><span data-stu-id="4c716-150">Update a released product in the USMF company</span></span>

1. <span data-ttu-id="4c716-151">Ujistěte se, že jste přihlášeni do společnosti **USMF**.</span><span class="sxs-lookup"><span data-stu-id="4c716-151">Make sure that you're signed in to the **USMF** company.</span></span>
1. <span data-ttu-id="4c716-152">Přejděte do **Řízení informací o produktech \> Produkty \> Uvolněné produkty**, vytváření uvolněného produktu se dokončí.</span><span class="sxs-lookup"><span data-stu-id="4c716-152">Go to **Product information management \> Products \> Released products** to finish creating the released product.</span></span>
1. <span data-ttu-id="4c716-153">Najděte a vyberte položku číslo *B0001*. Otevřete stránku **Podrobnosti uvolněného produktu**.</span><span class="sxs-lookup"><span data-stu-id="4c716-153">Find and select item number *B0001* to open the **Released product details** page.</span></span>
1. <span data-ttu-id="4c716-154">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="4c716-154">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4c716-155">Na záložce s náhledem **Všeobecné** se ujistěte, že je v poli **Skupina modelů položek** zadána hodnota *FIFO*.</span><span class="sxs-lookup"><span data-stu-id="4c716-155">On the **General** FastTab, make sure that the **Item model group** field is set to *FIFO*.</span></span>
1. <span data-ttu-id="4c716-156">V podokně Akce na kartě **Produkt** ve skupině **Nastavení** zvolte **Skupiny dimenzí**.</span><span class="sxs-lookup"><span data-stu-id="4c716-156">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Dimension groups**.</span></span>
1. <span data-ttu-id="4c716-157">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="4c716-157">Set the following values:</span></span>

    - <span data-ttu-id="4c716-158">**Skupina dimenze úložiště:** *Ware*</span><span class="sxs-lookup"><span data-stu-id="4c716-158">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="4c716-159">**Skupina sledovací dimenze:** *Žádná*</span><span class="sxs-lookup"><span data-stu-id="4c716-159">**Tracking dimension group:** *None*</span></span>

1. <span data-ttu-id="4c716-160">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c716-160">Select **OK**.</span></span>
1. <span data-ttu-id="4c716-161">V podokně Akce na kartě **Produkt** ve skupině **Nastavení** zvolte **Hierarchie rezervací**.</span><span class="sxs-lookup"><span data-stu-id="4c716-161">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Reservation hierarchy**.</span></span>
1. <span data-ttu-id="4c716-162">Nastavte v poli **Hierarchie rezervací** hodnotu *Výchozí*, poté klikněte na **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c716-162">Set the **Reservation hierarchy** field to *Default*, and then select **OK**.</span></span>
1. <span data-ttu-id="4c716-163">Na záložce s náhledem **Všeobecné** si v části **Správa** všimněte, že byl výběr aktualizován.</span><span class="sxs-lookup"><span data-stu-id="4c716-163">On the **General** FastTab, in the **Administration** section, notice that your selections have been updated.</span></span>
1. <span data-ttu-id="4c716-164">Na záložce s náhledem **Nákup** zadejte do pole **Cena** hodnotu *10*.</span><span class="sxs-lookup"><span data-stu-id="4c716-164">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="4c716-165">Na záložce s náhledem **Řízení nákladů** zadejte do pole **Skupina položek** hodnotu *Audio*.</span><span class="sxs-lookup"><span data-stu-id="4c716-165">On the **Manage costs** FastTab, in the **Item group** field, enter *Audio*.</span></span>
1. <span data-ttu-id="4c716-166">Na záložce s náhledem **Nákup** zadejte do pole **Cena** hodnotu *10*.</span><span class="sxs-lookup"><span data-stu-id="4c716-166">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="4c716-167">Na záložce s náhledem **Sklad** zadejte v poli **ID skupiny pořadí jednotek** hodnotu *ks*.</span><span class="sxs-lookup"><span data-stu-id="4c716-167">On the **Warehouse** FastTab, in the **Unit sequence group ID** field, enter *ea*.</span></span>
1. <span data-ttu-id="4c716-168">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="4c716-168">Select **Save**.</span></span>

### <a name="create-a-location-directive"></a><span data-ttu-id="4c716-169">Vytvoření směrnice skladového místa</span><span class="sxs-lookup"><span data-stu-id="4c716-169">Create a location directive</span></span>

1. <span data-ttu-id="4c716-170">Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="4c716-170">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="4c716-171">V levém podokně vyberte v poli **Typ pracovního příkazu** hodnotu *Nákupní objednávky*.</span><span class="sxs-lookup"><span data-stu-id="4c716-171">In the left pane, in the **Work order type** field, select *Purchase orders*.</span></span>
1. <span data-ttu-id="4c716-172">V seznamu vyberte směrnici skladového místa, jež se jmenuje *24 PO Direct*.</span><span class="sxs-lookup"><span data-stu-id="4c716-172">In the list, select the location directive that is named *24 PO Direct*.</span></span>
1. <span data-ttu-id="4c716-173">Na záložce s náhledem **Akce směrnice skladového místa** přidejte řádek do mřížky výběrem možnosti **Nová**.</span><span class="sxs-lookup"><span data-stu-id="4c716-173">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="4c716-174">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="4c716-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="4c716-175">**Pořadové číslo:** *1*</span><span class="sxs-lookup"><span data-stu-id="4c716-175">**Sequence number:** *1*</span></span>

        <span data-ttu-id="4c716-176">Nový řádek by měl být před již dříve existujícím řádkem.</span><span class="sxs-lookup"><span data-stu-id="4c716-176">The new line should be in front of the previously existing line.</span></span> <span data-ttu-id="4c716-177">Chcete-li provést změnu, použijte tlačítka **Pohyb nahoru** a **Pohyb dolů** na panelu nástrojů nebo změňte hodnotu v poli **Pořadové číslo** stávajících řádků na *2*.</span><span class="sxs-lookup"><span data-stu-id="4c716-177">To make the change, use the **Move up** and **Move down** buttons on the toolbar, or change the existing line's **Sequence number** value to *2*.</span></span>

    - <span data-ttu-id="4c716-178">**Název:** *Vložení do profilu skladového místa BULK*</span><span class="sxs-lookup"><span data-stu-id="4c716-178">**Name:** *Put to BULK Location profile*</span></span>
    - <span data-ttu-id="4c716-179">**Využití pevného skladového místa:** *Pevná a nepevná skladová místa*</span><span class="sxs-lookup"><span data-stu-id="4c716-179">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>
    - <span data-ttu-id="4c716-180">**Povolit záporný stav zásob:** *Zrušte zaškrtnutí tohoto políčka (= Ne)*</span><span class="sxs-lookup"><span data-stu-id="4c716-180">**Allow negative inventory:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="4c716-181">**Dávka povolena:** *Zrušte zaškrtnutí tohoto políčka (= Ne)*</span><span class="sxs-lookup"><span data-stu-id="4c716-181">**Batch enabled:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="4c716-182">**Strategie:** *Žádná*</span><span class="sxs-lookup"><span data-stu-id="4c716-182">**Strategy:** *None*</span></span>

1. <span data-ttu-id="4c716-183">Dokud je ještě nový řádek vybrán, klikněte na **Upravit dotaz** nad mřížkou.</span><span class="sxs-lookup"><span data-stu-id="4c716-183">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="4c716-184">V dialogovém okně dotazu na kartě **Oblast** přidejte tlačítkem **Přidat** nový řádek mřížky.</span><span class="sxs-lookup"><span data-stu-id="4c716-184">In the query dialog box, on the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="4c716-185">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="4c716-185">On the new line, set the following values:</span></span>

    - <span data-ttu-id="4c716-186">**Tabulka:** *umístění*</span><span class="sxs-lookup"><span data-stu-id="4c716-186">**Table:** *Locations*</span></span>
    - <span data-ttu-id="4c716-187">**Odvozená tabulka:** *Skladová místa*</span><span class="sxs-lookup"><span data-stu-id="4c716-187">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="4c716-188">**Pole:** *ID profilu skladového místa*</span><span class="sxs-lookup"><span data-stu-id="4c716-188">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="4c716-189">**Kritéria:** *BULK*</span><span class="sxs-lookup"><span data-stu-id="4c716-189">**Criteria:** *BULK*</span></span>

1. <span data-ttu-id="4c716-190">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c716-190">Select **OK**.</span></span>
1. <span data-ttu-id="4c716-191">Na stránce **Směrnice skladového místa** v podokně Akce vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="4c716-191">On the **Location directives** page, on the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="4c716-192">Na záložce s náhledem **Akce směrnice skladového místa** v poli **Strategie**: pokud používáte strategii skladových míst *Konsolidace*, bude nastavení na záložce s náhledem **Povolit míchání dimenzí produktů** na stránce **Profily skladových míst** přepsáno a položky budou ukládány do stejného skladového místa, i když nastavení takové chování nepovoluje.</span><span class="sxs-lookup"><span data-stu-id="4c716-192">On the **Location Directive Actions** FastTab **Strategy** field, if you use the *Consolidate* location strategy, the setup of the **Allowed product dimension mixing** FastTab on the **Location profiles** will be overridden, and items will be put to the same location even if this behavior isn't allowed by the setup.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="4c716-193">Vytvoření položky nabídky mobilních zařízení</span><span class="sxs-lookup"><span data-stu-id="4c716-193">Create a mobile device menu item</span></span>

1. <span data-ttu-id="4c716-194">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="4c716-194">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="4c716-195">V podokně Akce vyberte možnost **Nová**, vytvoří se položka nabídky, jež se bude používat k třídění.</span><span class="sxs-lookup"><span data-stu-id="4c716-195">On the Action Pane, select **New** to create a menu item to use for sorting.</span></span>
1. <span data-ttu-id="4c716-196">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="4c716-196">In the header, set the following values:</span></span>

    - <span data-ttu-id="4c716-197">**Název položky nabídky:** *Příjem řádku PO*</span><span class="sxs-lookup"><span data-stu-id="4c716-197">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="4c716-198">**Název:** *Příjem řádku PO*</span><span class="sxs-lookup"><span data-stu-id="4c716-198">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="4c716-199">**Režim:** *Práce*</span><span class="sxs-lookup"><span data-stu-id="4c716-199">**Mode:** *Work*</span></span>
    - <span data-ttu-id="4c716-200">**Použít existující práci:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="4c716-200">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="4c716-201">Na záložce s náhledem **Obecné** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="4c716-201">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="4c716-202">**Proces tvorby práce:** *Příjem a vyskladnění řádku nákupní objednávky*</span><span class="sxs-lookup"><span data-stu-id="4c716-202">**Work creation process:** *Purchase order line receiving and putaway*</span></span>
    - <span data-ttu-id="4c716-203">**Generovat registrační značky:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="4c716-203">**Generate license plate:** *Yes*</span></span>

1. <span data-ttu-id="4c716-204">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="4c716-204">Select **Save**.</span></span>

### <a name="configure-the-mobile-device-menu"></a><span data-ttu-id="4c716-205">Proveďte konfiguraci nabídky mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="4c716-205">Configure the mobile device menu</span></span>

1. <span data-ttu-id="4c716-206">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="4c716-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="4c716-207">V seznamu nabídek vyberte možnost **Vstupní**.</span><span class="sxs-lookup"><span data-stu-id="4c716-207">In the list of menus, select **Inbound**.</span></span>
1. <span data-ttu-id="4c716-208">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="4c716-208">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4c716-209">V seznamu **Dostupné nabídky a položky nabídky** najděte a vyberte položku nabídky **Příjem řádku PO**.</span><span class="sxs-lookup"><span data-stu-id="4c716-209">In the **Available Menus And Menu Items** list, find and select the **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="4c716-210">Stisknutím tlačítka se šipkou doprava přesuňte položku nabídky **Příjem řádku PO** do seznamu **Struktura nabídky**.</span><span class="sxs-lookup"><span data-stu-id="4c716-210">Select the right arrow button to move the **PO line receiving** menu item to the **Menu Structure** list.</span></span> <span data-ttu-id="4c716-211">Tímto způsobem se přidá nová položka nabídky do vybrané nabídky.</span><span class="sxs-lookup"><span data-stu-id="4c716-211">In this way, you add your new menu item to the selected menu.</span></span>
1. <span data-ttu-id="4c716-212">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="4c716-212">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="4c716-213">Scénář</span><span class="sxs-lookup"><span data-stu-id="4c716-213">Scenario</span></span>

<span data-ttu-id="4c716-214">Tento ukázkový scénář demonstruje, jak lze umístit dvě různé varianty produktu na stejné skladové místo, když profil skladového místa neumožňuje směšování položek, ale je povolena funkce *Směšování dimenzí produktu na skladovém místě*.</span><span class="sxs-lookup"><span data-stu-id="4c716-214">This demo scenario shows how two different product variants can be put to the same location when the location profile doesn't allow for mixed items, but the *Location product dimension mixing* feature is enabled.</span></span> <span data-ttu-id="4c716-215">V tomto případě využijeme jako kritérium variantu **velikosti**.</span><span class="sxs-lookup"><span data-stu-id="4c716-215">In this case, you will use the **Size** variant as the criterion.</span></span>

<span data-ttu-id="4c716-216">Než začnete, ujistěte se, že jsou ve skladu *24* prázdná místa, jež využívají profil skladového místa *BULK*.</span><span class="sxs-lookup"><span data-stu-id="4c716-216">Before you begin, make sure that there are empty locations in warehouse *24* that use the *BULK* location profile.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="4c716-217">Vytvoření nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="4c716-217">Create a purchase order</span></span>

<span data-ttu-id="4c716-218">Vytvoříte nákupní objednávku, která má tři řádky: dva řádky pro stejné číslo produktu, ale v odlišné variantě **Velikost**, třetí řádek bude pro jiný produkt, který nemá varianty.</span><span class="sxs-lookup"><span data-stu-id="4c716-218">You will create a purchase order that has three lines: two lines for the same product number but different **Size** variants, and a third line for a different product that has no variants.</span></span>

1. <span data-ttu-id="4c716-219">Přejděte na **Závazky \> Nákupní objednávky \> Všechny nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="4c716-219">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="4c716-220">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="4c716-220">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4c716-221">V dialogovém okně **Vytvoření nákupní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="4c716-221">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="4c716-222">**Účet dodavatele:** *1001*</span><span class="sxs-lookup"><span data-stu-id="4c716-222">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="4c716-223">**Sklad:** *24*</span><span class="sxs-lookup"><span data-stu-id="4c716-223">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="4c716-224">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c716-224">Select **OK**.</span></span>
1. <span data-ttu-id="4c716-225">Vytvoří se nákupní objednávka a na záložce s náhledem **Řádky nákupní objednávky** bude přidán nový řádek.</span><span class="sxs-lookup"><span data-stu-id="4c716-225">The purchase order is created, and a new line is added on the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="4c716-226">Poznamenejte si číslo nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="4c716-226">Make a note of the purchase order number.</span></span>
1. <span data-ttu-id="4c716-227">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="4c716-227">On the new line, set the following values:</span></span>

    - <span data-ttu-id="4c716-228">**Číslo položky:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="4c716-228">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="4c716-229">**Velikost** *L*</span><span class="sxs-lookup"><span data-stu-id="4c716-229">**Size** *L*</span></span>
    - <span data-ttu-id="4c716-230">**Množství:** *2*</span><span class="sxs-lookup"><span data-stu-id="4c716-230">**Quantity:** *2*</span></span>

1. <span data-ttu-id="4c716-231">Chcete-li přidat druhý řádek objednávky, klikněte na položku **Přidat řádek** nad mřížkou a nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="4c716-231">Select **Add line** above the grid to add a second purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="4c716-232">**Číslo položky:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="4c716-232">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="4c716-233">**Velikost** *XL*</span><span class="sxs-lookup"><span data-stu-id="4c716-233">**Size** *XL*</span></span>
    - <span data-ttu-id="4c716-234">**Množství:** *2*</span><span class="sxs-lookup"><span data-stu-id="4c716-234">**Quantity:** *2*</span></span>

1. <span data-ttu-id="4c716-235">Chcete-li přidat třetí řádek nákupní objednávky, klikněte na **Přidat řádek** a zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="4c716-235">Select **Add line** to add a third purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="4c716-236">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="4c716-236">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="4c716-237">**Množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="4c716-237">**Quantity:** *1*</span></span>

<span data-ttu-id="4c716-238">1.Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="4c716-238">1.Select **Save**.</span></span>

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a><span data-ttu-id="4c716-239">Přijetí řádků objednávky ve skladové aplikaci</span><span class="sxs-lookup"><span data-stu-id="4c716-239">Receive purchase order lines in the warehouse app</span></span>

1. <span data-ttu-id="4c716-240">Přihlaste se do skladové aplikace jako uživatel, který má povolen sklad *24*.</span><span class="sxs-lookup"><span data-stu-id="4c716-240">Sign in to the warehouse app as a user who is enabled for warehouse *24*.</span></span>
1. <span data-ttu-id="4c716-241">Vyberte nabídku **Vstupní**.</span><span class="sxs-lookup"><span data-stu-id="4c716-241">Select the **Inbound** menu.</span></span>
1. <span data-ttu-id="4c716-242">Vyberte **Příjem řádku PO**.</span><span class="sxs-lookup"><span data-stu-id="4c716-242">Select **PO Line receiving**.</span></span>
1. <span data-ttu-id="4c716-243">Vyberte pole **ČÍSLOPO** a zadejte číslo nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="4c716-243">Select the **PONUM** field, and then enter the purchase order number.</span></span>
1. <span data-ttu-id="4c716-244">Zadání potvrďte výběrem tlačítka pro potvrzení (✔) ve spodní části stránky.</span><span class="sxs-lookup"><span data-stu-id="4c716-244">Confirm your entry by selecting the confirm button ( ✔ ) at the bottom of the page.</span></span>
1. <span data-ttu-id="4c716-245">Zadejte číslo řádku z nákupní objednávky, kterou přijímáte.</span><span class="sxs-lookup"><span data-stu-id="4c716-245">Enter the line number from the purchase order that is being received.</span></span> <span data-ttu-id="4c716-246">Vyberte pole **ČÍSLOŘÁDKU** a poté zadejte pomocí číselné klávesnice hodnotu *1*.</span><span class="sxs-lookup"><span data-stu-id="4c716-246">Select the **LINENUM** field, and then use the number pad to enter *1*.</span></span>
1. <span data-ttu-id="4c716-247">Potvrďte zadání.</span><span class="sxs-lookup"><span data-stu-id="4c716-247">Confirm your entry.</span></span>
1. <span data-ttu-id="4c716-248">Zadejte přijímané množství.</span><span class="sxs-lookup"><span data-stu-id="4c716-248">Enter the quantity to receive.</span></span> <span data-ttu-id="4c716-249">Klikněte dvakrát na tlačítko se znaménkem plus (**+**). Zvýšíte tím hodnotu v poli **Množ.** na *2*.</span><span class="sxs-lookup"><span data-stu-id="4c716-249">Select the plus sign (**+**) button two times to increase the value in the **Qty** field to *2*.</span></span>
1. <span data-ttu-id="4c716-250">Zaregistrujte záznam stiskem tlačítka (✔) v dolní části stránky a poté zadání potvrďte opětovným stisknutím tlačítka (✔).</span><span class="sxs-lookup"><span data-stu-id="4c716-250">Register your entry by selecting the button ( ✔ ) at the bottom of the page, and then confirm your entry by selecting the button ( ✔ ) again.</span></span>
1. <span data-ttu-id="4c716-251">Prohlédněte si informace na stránce **Nákupní objednávky: zaskladnění**.</span><span class="sxs-lookup"><span data-stu-id="4c716-251">View the information on the **Purchase orders: Put** page.</span></span> <span data-ttu-id="4c716-252">Tato stránka zobrazuje práci, která byla vytvořena pro zaskladnění (Práce 1).</span><span class="sxs-lookup"><span data-stu-id="4c716-252">This page shows the work that has been created for the put-away (Work 1).</span></span>

    <span data-ttu-id="4c716-253">Pro právě dokončený **Příjem řádku PO** se zobrazí místo, kam bude přijatá položka umístěna, registrační značka, položka, velikost a množství.</span><span class="sxs-lookup"><span data-stu-id="4c716-253">The location where the received item will be put away, the license plate, the item, the size, and the quantity of the **PO Line receiving** task that you just completed are shown.</span></span>

1. <span data-ttu-id="4c716-254">Potvrďte práci zaskladnění.</span><span class="sxs-lookup"><span data-stu-id="4c716-254">Confirm the put-away work.</span></span>
1. <span data-ttu-id="4c716-255">Opakujte kroky 4 až 11 pro řádek 2 objednávky.</span><span class="sxs-lookup"><span data-stu-id="4c716-255">Repeat the steps 4 through 11 for the purchase order line 2.</span></span> <span data-ttu-id="4c716-256">V kroku 8 však zadejte množství *1*.</span><span class="sxs-lookup"><span data-stu-id="4c716-256">However, in step 8, specify a quantity of *1*.</span></span>

    <span data-ttu-id="4c716-257">Nová práce zaskladnění (práce 2) bude vytvořena pro stejné skladové místo jako práce 1.</span><span class="sxs-lookup"><span data-stu-id="4c716-257">New put-away work (Work 2) is created for the same location as Work 1.</span></span>

1. <span data-ttu-id="4c716-258">Znovu opakujte kroky 4 až 11 pro řádek 2 objednávky.</span><span class="sxs-lookup"><span data-stu-id="4c716-258">Repeat the steps 4 through 11 again for purchase order line 2.</span></span> <span data-ttu-id="4c716-259">V kroku 8 zadejte zbývající množství *1*.</span><span class="sxs-lookup"><span data-stu-id="4c716-259">In step 8, specify the remaining quantity of *1*.</span></span>

    <span data-ttu-id="4c716-260">Nová práce zaskladnění (práce 3) bude vytvořena pro stejné skladové místo jako práce 1 a práce 2.</span><span class="sxs-lookup"><span data-stu-id="4c716-260">New put-away work (Work 3) is created for the same location as Work 1 and Work 2.</span></span> <span data-ttu-id="4c716-261">Toto chování je způsobeno tím, že se používá strategie směrnice skladového místa *Konsolidovat* a protože záložka s náhledem **Povolit míchání položek** v **profilu skladového místa** *Hromadně* umožňuje na skladovém místě míchat varianty **velikosti**.</span><span class="sxs-lookup"><span data-stu-id="4c716-261">This behavior occurs because the *Consolidate* location directive strategy is used, and the **Allowed product dimension mixing** FastTab on the *Bulk* **Location profiles** setup allows the **Size** variant to be mixed on a location.</span></span>

1. <span data-ttu-id="4c716-262">Opakujte kroky 4 až 11 pro řádek 3 objednávky.</span><span class="sxs-lookup"><span data-stu-id="4c716-262">Repeat the steps 4 through 11 for purchase order line 3.</span></span> <span data-ttu-id="4c716-263">V kroku 8 zadejte pro položku číslo *A0001* množství *1*.</span><span class="sxs-lookup"><span data-stu-id="4c716-263">In step 8, specify a quantity of *1* for item number *A0001*.</span></span>

    <span data-ttu-id="4c716-264">Nová zaskladňovací práce (práce 4) se vytvoří pro jiné skladové místo než to, jež se použilo pro řádky 1 a 2 objednávky.</span><span class="sxs-lookup"><span data-stu-id="4c716-264">New put-away work (Work 4) is created for a different location than the location that is used for purchase order lines 1 and 2.</span></span> <span data-ttu-id="4c716-265">K tomuto chování dochází, protože profil skladového místa neumožňuje míchání produktů, ale umožňuje míchání dimenzí stejného základního produktu.</span><span class="sxs-lookup"><span data-stu-id="4c716-265">This behavior occurs because the location profile doesn't allow for mixed products, but it does allow for mixed dimensions of the same product master.</span></span>

1. <span data-ttu-id="4c716-266">Stiskněte tlačítko nabídky v horní části stránky (tzv. „hamburgerové tlačítko“ nebo „hamburger“) a vyberte **Storno**, chcete-li **Příjem řádku PO** opustit.</span><span class="sxs-lookup"><span data-stu-id="4c716-266">Select the Menu button at the top of the page (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit **PO Line receiving**.</span></span>

> [!TIP]
> <span data-ttu-id="4c716-267">Tento scénář můžete opakovat, ale tentokrát nastavte **Velikost** - *Ne* na záložce s náhledem **Povolit míchání dimenzí produktu** v **profilu skladového místa** *BULK*. V takovém případě nebude možné dimenze produktů míchat.</span><span class="sxs-lookup"><span data-stu-id="4c716-267">You can repeat this scenario, but this time, set **Size** - *No* under the **Allow product dimension mixing** FastTab on the *BULK* **Location profiles**, so that none of the product dimensions can be mixed.</span></span> <span data-ttu-id="4c716-268">V tomto případě bude po obdržení nákupní objednávky každá varianta produktu umístěna na nové skladové místo.</span><span class="sxs-lookup"><span data-stu-id="4c716-268">In this case, when you receive the purchase order, each product variant will be put to a new location.</span></span>