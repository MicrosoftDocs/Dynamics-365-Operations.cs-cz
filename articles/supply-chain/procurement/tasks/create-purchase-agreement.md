---
title: Vytvoření nákupní smlouvy
description: Toto téma vás provede vytvořením nákupní smlouvy.
author: RichardLuan
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fb3d397b277429954ef91e13445189fe21560b6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237196"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="4c079-103">Vytvoření nákupní smlouvy</span><span class="sxs-lookup"><span data-stu-id="4c079-103">Create a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c079-104">Toto téma vás provede vytvořením nákupní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="4c079-104">This topic guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="4c079-105">Toto by obvykle prováděl vedoucí nákupu.</span><span class="sxs-lookup"><span data-stu-id="4c079-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="4c079-106">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="4c079-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="4c079-107">Než začnete, je třeba nastavit klasifikace nákupní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="4c079-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="4c079-108">Vytvořenou smlouvu můžete použít při vytváření nákupní objednávky; tím se zkopírují podmínky nákupní smlouvy do záhlaví a jakýchkoli řádků objednávky ovlivněných touto smlouvou.</span><span class="sxs-lookup"><span data-stu-id="4c079-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="4c079-109">Vytvoření nové nákupní smlouvy</span><span class="sxs-lookup"><span data-stu-id="4c079-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="4c079-110">Přejděte na **Navigační podokno > Moduly > Zásobování a zdroje > Nákupní smlouvy > Nákupní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="4c079-110">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase agreements > Purchase agreements**.</span></span>
2. <span data-ttu-id="4c079-111">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="4c079-111">Click **New**.</span></span>
3. <span data-ttu-id="4c079-112">V poli **Účet dodavatele** vyberte rozevírací nabídku a zvolte řádek požadovaného záznamu.</span><span class="sxs-lookup"><span data-stu-id="4c079-112">In the **Vendor account** field, select the drop-down menu and select the row of the desired record.</span></span>
4. <span data-ttu-id="4c079-113">V poli **Klasifikace nákupní smlouvy** vyberte rozevírací nabídku a zvolte řádek požadovaného záznamu.</span><span class="sxs-lookup"><span data-stu-id="4c079-113">In the **Purchase agreement classification** field, select the drop-down menu and select the row of the desired record.</span></span>
5. <span data-ttu-id="4c079-114">Rozbalte pevnou záložku **Obecné**.</span><span class="sxs-lookup"><span data-stu-id="4c079-114">Expand the **General** FastTab.</span></span>
6. <span data-ttu-id="4c079-115">Do pole **Datum vypršení platnosti** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="4c079-115">In the **Expiration date** field, enter a date.</span></span>

    - <span data-ttu-id="4c079-116">Toto datum vypršení platnosti bude výchozí pro všechny řádky závazků a určí, jak dlouho budou jednotlivé závazky platné.</span><span class="sxs-lookup"><span data-stu-id="4c079-116">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  

7. <span data-ttu-id="4c079-117">V poli **Název dokumentu** zadejte název nákupní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="4c079-117">In the **Document title** field, type a name for your purchase agreement.</span></span>

    - <span data-ttu-id="4c079-118">Ponechejte pole **Výchozí závazek** nastavené na hodnotu **Závazek – množství produktu** (nebo pokud je nastavená jiná hodnota, změňte ji).</span><span class="sxs-lookup"><span data-stu-id="4c079-118">Leave the **Default commitment** field set to **Product quantity commitment** (or change it if it's not set to this).</span></span>  
    - <span data-ttu-id="4c079-119">Výchozí hodnota závazku určuje možnosti na řádcích smlouvy.</span><span class="sxs-lookup"><span data-stu-id="4c079-119">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="4c079-120">Pokud potřebujete nový typ závazku při vytváření řádků smlouvy, je nutné změnit výchozí závazek v záhlaví.</span><span class="sxs-lookup"><span data-stu-id="4c079-120">If you need a new commitment type when you're creating the agreement lines, you need to change the default commitment on the header.</span></span> <span data-ttu-id="4c079-121">Jsou k dispozici 4 typy závazků: **Závazek – množství produktu** pro určité množství produktu; **Závazek – hodnota produktu** pro konkrétní částku měny pro produkt; **Závazek – hodnota kategorie produktu** pro konkrétní částku měny v kategorii zásobování, kde částka může být pro katalogovou položku nebo nekatalogovou položku; **Závazek ohledně hodnoty** pro konkrétní částku měny, která může být splněna jakýmkoli produktem nebo jakoukoli kategorií zásobování.</span><span class="sxs-lookup"><span data-stu-id="4c079-121">There are 4 types of commitments: **Product quantity commitment** - for a specific quantity of a product; **Product value commitment** - for a specific currency amount of a product; **Product category value commitment** - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; **Value commitment** - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  

8. <span data-ttu-id="4c079-122">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c079-122">Select **OK**.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="4c079-123">Přidání závazku</span><span class="sxs-lookup"><span data-stu-id="4c079-123">Add a commitment</span></span>
1. <span data-ttu-id="4c079-124">Vyberte **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="4c079-124">Select **Add line**.</span></span>
2. <span data-ttu-id="4c079-125">V poli **Číslo položky** vyberte z rozevírací nabídky požadovaný záznam.</span><span class="sxs-lookup"><span data-stu-id="4c079-125">In the **Item number** field, select the desired record from the drop-down menu.</span></span>
3. <span data-ttu-id="4c079-126">Zadejte číslo do pole **Množství**.</span><span class="sxs-lookup"><span data-stu-id="4c079-126">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="4c079-127">Toto je celkového množství, které podle dohody zakoupíte od dodavatele.</span><span class="sxs-lookup"><span data-stu-id="4c079-127">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
4. <span data-ttu-id="4c079-128">Zadejte číslo do pole **Jednotková cena**.</span><span class="sxs-lookup"><span data-stu-id="4c079-128">In the **Unit price** field, enter a number.</span></span>
5. <span data-ttu-id="4c079-129">Rozbalte sekci **Podrobnosti řádku**.</span><span class="sxs-lookup"><span data-stu-id="4c079-129">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="4c079-130">Nastavte možnost **Max je vynuceno** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="4c079-130">Set the **Max is enforced** option to **Yes**.</span></span> <span data-ttu-id="4c079-131">Možnost **Max je vynuceno** omezuje použití závazku.</span><span class="sxs-lookup"><span data-stu-id="4c079-131">The **Max is enforced** option limits the use of the commitment.</span></span> <span data-ttu-id="4c079-132">Můžete produkt zakoupit pouze do množství zadaného v poli **Množství** pro daný řádek.</span><span class="sxs-lookup"><span data-stu-id="4c079-132">You can only purchase up to the quantity that's specified in the **Quantity** field for the line.</span></span>  

## <a name="add-header-conditions"></a><span data-ttu-id="4c079-133">Přidání podmínek záhlaví</span><span class="sxs-lookup"><span data-stu-id="4c079-133">Add header conditions</span></span>
1. <span data-ttu-id="4c079-134">V podokně akcí vyberte **Možnosti**.</span><span class="sxs-lookup"><span data-stu-id="4c079-134">On the Action Pane, select **Options**.</span></span>
2. <span data-ttu-id="4c079-135">Vyberte **Změnit zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="4c079-135">Select **Change view**.</span></span>
3. <span data-ttu-id="4c079-136">Vyberte **Zobrazení záhlaví**.</span><span class="sxs-lookup"><span data-stu-id="4c079-136">Select **Header view**.</span></span>
4. <span data-ttu-id="4c079-137">Rozbalte část **Podmínky**.</span><span class="sxs-lookup"><span data-stu-id="4c079-137">Expand the **Terms** section.</span></span>
5. <span data-ttu-id="4c079-138">V poli **Metoda platby** vyberte požadovaný záznam v rozevírací nabídce.</span><span class="sxs-lookup"><span data-stu-id="4c079-138">In the **Method of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="4c079-139">Zde jsou ve výchozím nastavení zobrazené platební podmínky z účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="4c079-139">The payment terms from the vendor account are shown here by default.</span></span>  
6. <span data-ttu-id="4c079-140">V poli **Způsob dodání** vyberte požadovaný záznam v rozevírací nabídce.</span><span class="sxs-lookup"><span data-stu-id="4c079-140">In the **Mode of delivery** field, select the desired record in the drop-down menu.</span></span>
7. <span data-ttu-id="4c079-141">V poli **Dodací podmínky** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="4c079-141">In the **Delivery terms** field, select the drop-down button to open the lookup.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="4c079-142">Potvrzení a aktivace smlouvy</span><span class="sxs-lookup"><span data-stu-id="4c079-142">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="4c079-143">V podokně akcí klikněte na možnost **Nákupní smlouva**.</span><span class="sxs-lookup"><span data-stu-id="4c079-143">On the Action Pane, select **Purchase agreement**.</span></span>
2. <span data-ttu-id="4c079-144">Vyberte **Potvrzení**.</span><span class="sxs-lookup"><span data-stu-id="4c079-144">Select **Confirmation**.</span></span> <span data-ttu-id="4c079-145">Nastavte možnost **Označit smlouvu jako platnou** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="4c079-145">Set the **Mark agreement as effective** option to **Yes**.</span></span>  
3. <span data-ttu-id="4c079-146">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c079-146">Select **OK**.</span></span>
4. <span data-ttu-id="4c079-147">V podokně akcí klikněte na možnost **Nákupní smlouva**.</span><span class="sxs-lookup"><span data-stu-id="4c079-147">On the Action Pane, select **Purchase agreement**.</span></span>
5. <span data-ttu-id="4c079-148">Zvolte **Potvrzení nákupní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="4c079-148">Select **Purchase agreement confirmations**.</span></span> <span data-ttu-id="4c079-149">Možnost **Náhled/tisk** umožňuje generovat dokument pro nákupní smlouvu, který pak můžete vytisknout nebo odeslat dodavateli.</span><span class="sxs-lookup"><span data-stu-id="4c079-149">The **Preview/Print** option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="4c079-150">Pokud smlouvu aktualizujete a znovu potvrdíte později, zobrazí se zde obě verze.</span><span class="sxs-lookup"><span data-stu-id="4c079-150">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="4c079-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4c079-151">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]