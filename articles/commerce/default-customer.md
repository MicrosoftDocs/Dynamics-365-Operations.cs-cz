---
title: Vytvoření výchozího odběratele
description: V tomto tématu je popsán postup při vytvoření výchozího odběratele, který se použije při vytváření kanálu v aplikaci Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 1dd4dfc5b8ca7af66941d081b4c20be0f5d6001d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993393"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="59a64-103">Vytvoření výchozího odběratele</span><span class="sxs-lookup"><span data-stu-id="59a64-103">Create a default customer</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="59a64-104">V tomto tématu je popsán postup při vytvoření výchozího odběratele, který se použije při vytváření kanálu v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="59a64-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="59a64-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="59a64-105">Overview</span></span>

<span data-ttu-id="59a64-106">Při vytváření kanálu budete muset zadat výchozího odběratele.</span><span class="sxs-lookup"><span data-stu-id="59a64-106">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="59a64-107">Po prvním vytvoření skupiny odběratelů a adresáře odběratelů lze snadno vytvořit výchozího odběratele.</span><span class="sxs-lookup"><span data-stu-id="59a64-107">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="59a64-108">Vytvoření skupiny odběratelů</span><span class="sxs-lookup"><span data-stu-id="59a64-108">Create a customer group</span></span>

<span data-ttu-id="59a64-109">Pokud žádné skupiny odběratelů dosud neexistují, můžete je vytvořit.</span><span class="sxs-lookup"><span data-stu-id="59a64-109">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="59a64-110">Příklady mohou být skupiny, které představují různé skupiny odběratelů (například velkoobchod, maloobchod, Internet, zaměstnanci atd.).</span><span class="sxs-lookup"><span data-stu-id="59a64-110">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="59a64-111">Pokud chcete vytvořit skupinu odběratelů, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="59a64-111">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="59a64-112">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Zákazníci \> Skupiny zákazníků**.</span><span class="sxs-lookup"><span data-stu-id="59a64-112">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="59a64-113">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="59a64-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="59a64-114">Do pole **Skupina zákazníků** zadejte ID skupiny.</span><span class="sxs-lookup"><span data-stu-id="59a64-114">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="59a64-115">Je-li to nutné, zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="59a64-115">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="59a64-116">Do pole **Podmínky plateb** zadejte příslušnou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="59a64-116">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="59a64-117">Do pole **Čas mezi datem splatnosti a datem platby** zadejte odpovídající hodnotu.</span><span class="sxs-lookup"><span data-stu-id="59a64-117">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="59a64-118">Do pole **výchozí daňová skupina** zadejte, pokud je to vhodné, daňovou skupinu.</span><span class="sxs-lookup"><span data-stu-id="59a64-118">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="59a64-119">Zaškrtněte políčko **Ceny zahrnují DPH** v připadě potřeby.</span><span class="sxs-lookup"><span data-stu-id="59a64-119">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="59a64-120">Do pole **výchozí důvod odpisu** zadejte odpovídající hodnotu v připadě potřeby.</span><span class="sxs-lookup"><span data-stu-id="59a64-120">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="59a64-121">Následující obrázek znázorňuje několik konfigurovaných skupin odběratelů.</span><span class="sxs-lookup"><span data-stu-id="59a64-121">The following image shows several configured customer groups.</span></span>

![Skupiny odběratelů](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="59a64-123">Vytvoření adresáře odběratelů</span><span class="sxs-lookup"><span data-stu-id="59a64-123">Create a customer address book</span></span>

<span data-ttu-id="59a64-124">Zákazník musí být přidružen k adresáři.</span><span class="sxs-lookup"><span data-stu-id="59a64-124">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="59a64-125">Pokud ještě nebyla vytvořena, je třeba ji vytvořit.</span><span class="sxs-lookup"><span data-stu-id="59a64-125">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="59a64-126">Při vytváření nového adresáře odběratelů postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="59a64-126">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="59a64-127">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Adresáře**.</span><span class="sxs-lookup"><span data-stu-id="59a64-127">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="59a64-128">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="59a64-128">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="59a64-129">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="59a64-129">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="59a64-130">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="59a64-130">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="59a64-131">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="59a64-131">On the action pane, select **Save**.</span></span>

<span data-ttu-id="59a64-132">Následující obrázek znázorňuje příklad adreáře.</span><span class="sxs-lookup"><span data-stu-id="59a64-132">The following image shows an example address book.</span></span>

![Adresář](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="59a64-134">Vytvoření výchozího odběratele</span><span class="sxs-lookup"><span data-stu-id="59a64-134">Create a default customer</span></span>

<span data-ttu-id="59a64-135">Pokud chcete vytvořit výchozího odběratele, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="59a64-135">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="59a64-136">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Zákazníci \> Všichni odběratelé**.</span><span class="sxs-lookup"><span data-stu-id="59a64-136">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="59a64-137">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="59a64-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="59a64-138">V rozevíracím seznamu **Typ** vyberte "Osoba".</span><span class="sxs-lookup"><span data-stu-id="59a64-138">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="59a64-139">V rozevíracím seznamu **účet odběratele** vyberte nebo zadejte číslo účtu (například "100001").</span><span class="sxs-lookup"><span data-stu-id="59a64-139">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="59a64-140">V rozevíracím seznamu **Křestní jméno** vyberte nebo zadejte název (například "výchozí").</span><span class="sxs-lookup"><span data-stu-id="59a64-140">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="59a64-141">V rozevíracím seznamu **Prostřední jméno** vyberte nebo zadejte název (například "Retail").</span><span class="sxs-lookup"><span data-stu-id="59a64-141">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="59a64-142">V rozevíracím seznamu **Příjmení** vyberte nebo zadejte název (například "Zákazník").</span><span class="sxs-lookup"><span data-stu-id="59a64-142">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="59a64-143">V rozevíracím seznamu **Měna** vyberte nebo zadejte měnu (například "USD").</span><span class="sxs-lookup"><span data-stu-id="59a64-143">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="59a64-144">V rozevíracím seznamu **Měna** vyberte skupinu odběratelů, která byla vytvořena dříve.</span><span class="sxs-lookup"><span data-stu-id="59a64-144">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="59a64-145">V rozevíracím seznamu **Adresáře** vyberte existující adresář odběratele.</span><span class="sxs-lookup"><span data-stu-id="59a64-145">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="59a64-146">Výběrem **Uložit** uložte a vrátíte se do obrazovky s podrobnostmi o odběrateli pro nového odběratele.</span><span class="sxs-lookup"><span data-stu-id="59a64-146">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="59a64-147">Není nutné přidávat adresu výchozího odběratele.</span><span class="sxs-lookup"><span data-stu-id="59a64-147">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="59a64-148">Na následujícím obrázku je znázorněn příklad vytvoření zákazníka.</span><span class="sxs-lookup"><span data-stu-id="59a64-148">The following image shows an example of customer creation.</span></span>

![Vytvoření výchozího odběratele](media/default-customer-creation.png)

<span data-ttu-id="59a64-150">Následující obrázek znázorňuje výchozí konfiguraci odběratele.</span><span class="sxs-lookup"><span data-stu-id="59a64-150">The following image shows a default customer configuration.</span></span>

![Konfigurace ukázkového odběratele](media/default-customer-configuration1.png)

<span data-ttu-id="59a64-152">Většina výchozích hodnot na obrazovce podrobností odběratele může zůstat, ale je třeba změnit dvě hodnoty.</span><span class="sxs-lookup"><span data-stu-id="59a64-152">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="59a64-153">Na obrazovce Podrobnosti o odběrateli rozbalte **Výhozí nastavení prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="59a64-153">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="59a64-154">V rozevíracím seznamu **Umístění** vyberte nebo zadejte přednastavené umístění.</span><span class="sxs-lookup"><span data-stu-id="59a64-154">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="59a64-155">V rozevíracím seznamu **Sklad** vyberte nebo zadejte přednastavený sklad.</span><span class="sxs-lookup"><span data-stu-id="59a64-155">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="59a64-156">Na následujícím obrázku je znázorněn příklad konfigurace zákazníka.</span><span class="sxs-lookup"><span data-stu-id="59a64-156">The following image shows an example customer configuration.</span></span>

![Konfigurace ukázkového odběratele](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="59a64-158">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="59a64-158">Additional resources</span></span>

[<span data-ttu-id="59a64-159">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="59a64-159">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="59a64-160">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="59a64-160">Channel setup prerequisites</span></span>](channels-prerequisites.md)
