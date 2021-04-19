---
title: Vytvoření výchozího odběratele
description: V tomto tématu je popsán postup při vytvoření výchozího odběratele, který se použije při vytváření kanálu v aplikaci Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ecdf4e5618d3397527bf83977857fbe3f8dbb265
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799172"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="f7120-103">Vytvoření výchozího odběratele</span><span class="sxs-lookup"><span data-stu-id="f7120-103">Create a default customer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f7120-104">V tomto tématu je popsán postup při vytvoření výchozího odběratele, který se použije při vytváření kanálu v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f7120-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f7120-105">Při vytváření kanálu budete muset zadat výchozího odběratele.</span><span class="sxs-lookup"><span data-stu-id="f7120-105">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="f7120-106">Po prvním vytvoření skupiny odběratelů a adresáře odběratelů lze snadno vytvořit výchozího odběratele.</span><span class="sxs-lookup"><span data-stu-id="f7120-106">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="f7120-107">Vytvoření skupiny odběratelů</span><span class="sxs-lookup"><span data-stu-id="f7120-107">Create a customer group</span></span>

<span data-ttu-id="f7120-108">Pokud žádné skupiny odběratelů dosud neexistují, můžete je vytvořit.</span><span class="sxs-lookup"><span data-stu-id="f7120-108">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="f7120-109">Příklady mohou být skupiny, které představují různé skupiny odběratelů (například velkoobchod, maloobchod, Internet, zaměstnanci atd.).</span><span class="sxs-lookup"><span data-stu-id="f7120-109">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="f7120-110">Pokud chcete vytvořit skupinu odběratelů, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="f7120-110">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="f7120-111">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Zákazníci \> Skupiny zákazníků**.</span><span class="sxs-lookup"><span data-stu-id="f7120-111">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="f7120-112">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="f7120-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f7120-113">Do pole **Skupina zákazníků** zadejte ID skupiny.</span><span class="sxs-lookup"><span data-stu-id="f7120-113">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="f7120-114">Je-li to nutné, zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="f7120-114">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="f7120-115">Do pole **Podmínky plateb** zadejte příslušnou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="f7120-115">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="f7120-116">Do pole **Čas mezi datem splatnosti a datem platby** zadejte odpovídající hodnotu.</span><span class="sxs-lookup"><span data-stu-id="f7120-116">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="f7120-117">Do pole **výchozí daňová skupina** zadejte, pokud je to vhodné, daňovou skupinu.</span><span class="sxs-lookup"><span data-stu-id="f7120-117">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="f7120-118">Zaškrtněte políčko **Ceny zahrnují DPH** v připadě potřeby.</span><span class="sxs-lookup"><span data-stu-id="f7120-118">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="f7120-119">Do pole **výchozí důvod odpisu** zadejte odpovídající hodnotu v připadě potřeby.</span><span class="sxs-lookup"><span data-stu-id="f7120-119">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="f7120-120">Následující obrázek znázorňuje několik konfigurovaných skupin odběratelů.</span><span class="sxs-lookup"><span data-stu-id="f7120-120">The following image shows several configured customer groups.</span></span>

![Skupiny odběratelů](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="f7120-122">Vytvoření adresáře odběratelů</span><span class="sxs-lookup"><span data-stu-id="f7120-122">Create a customer address book</span></span>

<span data-ttu-id="f7120-123">Zákazník musí být přidružen k adresáři.</span><span class="sxs-lookup"><span data-stu-id="f7120-123">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="f7120-124">Pokud ještě nebyla vytvořena, je třeba ji vytvořit.</span><span class="sxs-lookup"><span data-stu-id="f7120-124">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="f7120-125">Při vytváření nového adresáře odběratelů postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="f7120-125">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="f7120-126">V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Adresáře**.</span><span class="sxs-lookup"><span data-stu-id="f7120-126">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="f7120-127">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="f7120-127">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f7120-128">Do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="f7120-128">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="f7120-129">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="f7120-129">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="f7120-130">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f7120-130">On the action pane, select **Save**.</span></span>

<span data-ttu-id="f7120-131">Následující obrázek znázorňuje příklad adreáře.</span><span class="sxs-lookup"><span data-stu-id="f7120-131">The following image shows an example address book.</span></span>

![Adresář](media/address-book.png)

## <a name="create-a-default-customer&quot;></a><span data-ttu-id=&quot;f7120-133&quot;>Vytvoření výchozího odběratele</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f7120-133&quot;>Create a default customer</span></span>

<span data-ttu-id=&quot;f7120-134&quot;>Pokud chcete vytvořit výchozího odběratele, postupujte takto.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f7120-134&quot;>To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id=&quot;f7120-135&quot;>V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Zákazníci \> Všichni odběratelé**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f7120-135&quot;>In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id=&quot;f7120-136&quot;>V podokně akcí zvolte **Nový**.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f7120-136&quot;>On the action pane, select **New**.</span></span>
1. <span data-ttu-id=&quot;f7120-137&quot;>V rozevíracím seznamu **Typ** vyberte &quot;Osoba&quot;.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f7120-137&quot;>In the **Type** drop-down list, select &quot;Person&quot;.</span></span>
1. <span data-ttu-id=&quot;f7120-138&quot;>V rozevíracím seznamu **účet odběratele** vyberte nebo zadejte číslo účtu (například &quot;100001").</span><span class="sxs-lookup"><span data-stu-id="f7120-138">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="f7120-139">V rozevíracím seznamu **Křestní jméno** vyberte nebo zadejte název (například "výchozí").</span><span class="sxs-lookup"><span data-stu-id="f7120-139">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="f7120-140">V rozevíracím seznamu **Prostřední jméno** vyberte nebo zadejte název (například "Retail").</span><span class="sxs-lookup"><span data-stu-id="f7120-140">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="f7120-141">V rozevíracím seznamu **Příjmení** vyberte nebo zadejte název (například "Zákazník").</span><span class="sxs-lookup"><span data-stu-id="f7120-141">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="f7120-142">V rozevíracím seznamu **Měna** vyberte nebo zadejte měnu (například "USD").</span><span class="sxs-lookup"><span data-stu-id="f7120-142">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="f7120-143">V rozevíracím seznamu **Měna** vyberte skupinu odběratelů, která byla vytvořena dříve.</span><span class="sxs-lookup"><span data-stu-id="f7120-143">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="f7120-144">V rozevíracím seznamu **Adresáře** vyberte existující adresář odběratele.</span><span class="sxs-lookup"><span data-stu-id="f7120-144">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="f7120-145">Výběrem **Uložit** uložte a vrátíte se do obrazovky s podrobnostmi o odběrateli pro nového odběratele.</span><span class="sxs-lookup"><span data-stu-id="f7120-145">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="f7120-146">Není nutné přidávat adresu výchozího odběratele.</span><span class="sxs-lookup"><span data-stu-id="f7120-146">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="f7120-147">Na následujícím obrázku je znázorněn příklad vytvoření zákazníka.</span><span class="sxs-lookup"><span data-stu-id="f7120-147">The following image shows an example of customer creation.</span></span>

![Vytvoření výchozího odběratele](media/default-customer-creation.png)

<span data-ttu-id="f7120-149">Následující obrázek znázorňuje výchozí konfiguraci odběratele.</span><span class="sxs-lookup"><span data-stu-id="f7120-149">The following image shows a default customer configuration.</span></span>

![Konfigurace ukázkového odběratele](media/default-customer-configuration1.png)

<span data-ttu-id="f7120-151">Většina výchozích hodnot na obrazovce podrobností odběratele může zůstat, ale je třeba změnit dvě hodnoty.</span><span class="sxs-lookup"><span data-stu-id="f7120-151">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="f7120-152">Na obrazovce Podrobnosti o odběrateli rozbalte **Výhozí nastavení prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="f7120-152">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="f7120-153">V rozevíracím seznamu **Umístění** vyberte nebo zadejte přednastavené umístění.</span><span class="sxs-lookup"><span data-stu-id="f7120-153">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="f7120-154">V rozevíracím seznamu **Sklad** vyberte nebo zadejte přednastavený sklad.</span><span class="sxs-lookup"><span data-stu-id="f7120-154">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="f7120-155">Na následujícím obrázku je znázorněn příklad konfigurace zákazníka.</span><span class="sxs-lookup"><span data-stu-id="f7120-155">The following image shows an example customer configuration.</span></span>

![Konfigurace ukázkového odběratele](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="f7120-157">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="f7120-157">Additional resources</span></span>

[<span data-ttu-id="f7120-158">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="f7120-158">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="f7120-159">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="f7120-159">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
