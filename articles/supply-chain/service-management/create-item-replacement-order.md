---
title: Vytvoření objednávky náhrady položky
description: Objednávky náhrady položek jsou obvykle vytvořeny po vrácení a kontrole výrobku.
author: josaw1
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e63c175d12cac91648cb57a3f41d1769e81d57af
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830092"
---
# <a name="create-an-item-replacement-order"></a><span data-ttu-id="03901-103">Vytvoření objednávky náhrady položky</span><span class="sxs-lookup"><span data-stu-id="03901-103">Create an item replacement order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="03901-104">Objednávky náhrady položek jsou obvykle vytvořeny po vrácení a kontrole výrobku.</span><span class="sxs-lookup"><span data-stu-id="03901-104">Item replacement orders are usually created after a product is returned and inspected.</span></span> <span data-ttu-id="03901-105">Pokud je však nutné položku nahradit ještě před vrácením nebo pokud původní položka nebude vrácená, můžete vytvořit objednávku náhrady bezprostředně po vytvoření vratky.</span><span class="sxs-lookup"><span data-stu-id="03901-105">However, when an item must be replaced before it has been returned, or when the original item will not be returned, you can create an item replacement order immediately after you create a return order.</span></span>

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a><span data-ttu-id="03901-106">Vytvořit objednávku náhrady po přijetí vráceného zboží</span><span class="sxs-lookup"><span data-stu-id="03901-106">Create a replacement order after you receive an item that is returned</span></span>

1.  <span data-ttu-id="03901-107">Klikněte na **Prodej a marketing** \> **Společné** \> **Objednávky vratky** \> **Všechny objednávky vratky**.</span><span class="sxs-lookup"><span data-stu-id="03901-107">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="03901-108">Vytvořte novou objednávku vratky nebo vyberte objednávku vratky ze seznamu a otevřete formulář **Vratka - číslo RMA: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="03901-108">Create a new return order, or select a returned order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="03901-109">Klepněte na tlačítko **řádek vratky**a poté vyberte **náhradní součást**.</span><span class="sxs-lookup"><span data-stu-id="03901-109">Click **Return line**, and then select **Replacement item**.</span></span>

4.  <span data-ttu-id="03901-110">Vyberte položku, kterou chcete nahradit vrácené zboží.</span><span class="sxs-lookup"><span data-stu-id="03901-110">Select the item to replace the returned item with.</span></span> <span data-ttu-id="03901-111">Zadejte specifikace položky a klikněte na tlačítko **Použít**.</span><span class="sxs-lookup"><span data-stu-id="03901-111">Enter the item specifications, and then click **Apply**.</span></span>

5.  <span data-ttu-id="03901-112">Klikněte na **Dodací list** k vygenerování dodacího listu pro objednávku vratky.</span><span class="sxs-lookup"><span data-stu-id="03901-112">Click **Packing slip** to generate the packing slip for the return order.</span></span> <span data-ttu-id="03901-113">Prodejní objednávka je generována pro náhradní zboží, které jste vybrali.</span><span class="sxs-lookup"><span data-stu-id="03901-113">A sales order is generated for the replacement item that you selected.</span></span>
    
    <span data-ttu-id="03901-114">Po vytvoření prodejní objednávky náhradního zboží jsou prodejní smlouvy automaticky prohledány, a pokud existuje příslušná prodejní smlouva, je použita na prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="03901-114">After the sales order is created for the replacement item, sales agreements are automatically searched and if there is an applicable sales agreement, it is applied to the sales order.</span></span>

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a><span data-ttu-id="03901-115">Vytvoření objednávky náhrady dříve, než je přijata vracená položka</span><span class="sxs-lookup"><span data-stu-id="03901-115">Create a replacement order before you receive an item that will be returned</span></span>

1.  <span data-ttu-id="03901-116">Klikněte na **Prodej a marketing** \> **Společné** \> **Objednávky vratky** \> **Všechny objednávky vratky**.</span><span class="sxs-lookup"><span data-stu-id="03901-116">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="03901-117">Vytvořte novou vratku nebo vyberte vratku ze seznamu a otevřete formulář **Vratka - číslo RMA: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="03901-117">Create a new return order, or select a return order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="03901-118">Klikněte na **Najít prodejní objednávku**, pokud chcete identifikovat prodejní objednávku pro vrácenou položku.</span><span class="sxs-lookup"><span data-stu-id="03901-118">Click **Find sales order** if you want to identify the sales order for the returned item.</span></span> <span data-ttu-id="03901-119">Vyplňte formulář **Najít prodejní objednávku** a kliknutím na **OK** zavřete formulář a vraťte se do formuláře **Vratka – číslo RMA:%1, %2**.</span><span class="sxs-lookup"><span data-stu-id="03901-119">Complete the **Find sales order** form and then click **OK** to close the form and return to the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="03901-120">Řádek prodejní objednávky pro vrácené zboží se zkopíruje do objednávky vratky.</span><span class="sxs-lookup"><span data-stu-id="03901-120">The sales order line for the returned item is copied to the return order.</span></span>

4.  <span data-ttu-id="03901-121">Klepněte na tlačítko **náhradní objednávka** pro otevření formuláře **Vytvořit prodejní objednávku**.</span><span class="sxs-lookup"><span data-stu-id="03901-121">Click **Replacement order** to open the **Create sales order** form.</span></span>

5.  <span data-ttu-id="03901-122">Zaškrtnutím políčka **Kopírovat řádky vratek** přesuňte podrobnosti z vratky vybrané ve formuláři **Vratka – číslo RMA:%1, %2** do této prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="03901-122">Select the **Copy return order lines** check box to transfer details from the return order you selected on the **Return order - RMA number: %1, %2** form to this sales order.</span></span>

6.  <span data-ttu-id="03901-123">Podle potřeby zadejte nebo upravte podrobné údaje.</span><span class="sxs-lookup"><span data-stu-id="03901-123">Enter or modify details, as required.</span></span>
    
    <span data-ttu-id="03901-124">Pokud jste identifikovali v kroku 3 prodejní objednávku, a pokud je řádek prodejní objednávky pro vrácené zboží spojen s prodejní dohodou, identifikátor platné prodejní smlouvy pro objednávku náhradního zboží se automaticky zobrazí v poli **ID prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="03901-124">If you identified the sales order in step 3, and if the sales order line for the returned item is linked to a sales agreement, the identifier of the applicable sales agreement for the item replacement order will be automatically displayed in the **Sales agreement ID** field.</span></span>

7.  <span data-ttu-id="03901-125">Klikněte na tlačítko **OK**, zavřete formulář **Vytvořit prodejní objednávku** a otevřete formulář **Prodejní objednávka**, kde můžete pokračovat k zadání informací pro novou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="03901-125">Click **OK** to close the **Create sales order** form and open the **Sales order** form, where you can continue to enter information for the new sales order.</span></span> <span data-ttu-id="03901-126">Všechny řádky platné objednávky vratky budou zkopírovány do nové prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="03901-126">Any applicable return order lines will be copied to the new sales order.</span></span> 
    
    <span data-ttu-id="03901-127">Je-li identifikátor prodejní smlouvy automaticky zobrazen v poli **ID prodejní smlouvy**, pak prodejní smlouvu byla spojena se záhlavím prodejní objednávky náhradního zboží.</span><span class="sxs-lookup"><span data-stu-id="03901-127">If the identifier of the sales agreement is automatically displayed in the **Sales agreement ID** field, then the sales agreement has been linked to the sales order header for the item replacement order.</span></span> <span data-ttu-id="03901-128">Pokud je v prodejní smlouvě platný závazek, který ještě nebyl naplněn, a prodejní objednávka je vytvořena před vypršením platnosti prodejní smlouvy, je vytvořeno propojení mezi řádkem prodejní smlouvy a řádkem prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="03901-128">If there is an applicable commitment in the sales agreement that has not been fulfilled yet, and the sales order is created before the sales agreement expires, a link is established between the sales agreement line and the sales order line.</span></span> <span data-ttu-id="03901-129">Proto se informace z prodejní smlouvy, jako je cena zboží, zkopíruje do nového řádku prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="03901-129">Therefore, information from the sales agreement, such as item price, is copied to the new sales order line.</span></span> 
  


