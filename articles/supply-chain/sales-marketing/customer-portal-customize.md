---
title: Přizpůsobení a použití zákaznického portálu
description: Toto téma vysvětluje, jak přizpůsobit zákaznický portál poté, co byl přidán do vašeho systému.
author: dasani-madipalli
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6d4cc52a90b25406080032c7a98caa59f53ce188
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908993"
---
# <a name="customize-and-use-the-customer-portal"></a><span data-ttu-id="c7ccf-103">Přizpůsobení a použití zákaznického portálu</span><span class="sxs-lookup"><span data-stu-id="c7ccf-103">Customize and use the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c7ccf-104">Toto téma popisuje různé stránky, které jsou ihned k dispozici na zákaznickém portálu.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-104">This topic describes the different pages that available in the Customer portal out of the box.</span></span> <span data-ttu-id="c7ccf-105">Vysvětluje, co stránky dělají a jak je můžete přizpůsobit.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-105">It explains what the pages do and how you can customize them.</span></span>

<span data-ttu-id="c7ccf-106">Zákaznický portál nabízí ihned několik webových stránek a akcí.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-106">The Customer portal offers a few webpages and actions out of the box.</span></span> <span data-ttu-id="c7ccf-107">Následující mapa webu poskytuje přehled těchto webových stránek a akcí a rolí, které mohou akce provádět.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-107">The following site map provides an overview of those webpages and actions, and the roles that can perform the actions.</span></span>

<span data-ttu-id="c7ccf-108">![Mapa webu zákaznického portálu](media/customer-portal-site-map.png "Mapa webu zákaznického portálu")</span><span class="sxs-lookup"><span data-stu-id="c7ccf-108">![Customer portal site map](media/customer-portal-site-map.png "Customer portal site map")</span></span>

## <a name="typical-customizations"></a><span data-ttu-id="c7ccf-109">Typické úpravy</span><span class="sxs-lookup"><span data-stu-id="c7ccf-109">Typical customizations</span></span>

<span data-ttu-id="c7ccf-110">Následující témata vám pomohou naučit se základy Power Apps portálů a jak můžete portály přizpůsobit:</span><span class="sxs-lookup"><span data-stu-id="c7ccf-110">The following topics will help you learn the basics about Power Apps portals and how you can customize portals:</span></span>

- <span data-ttu-id="c7ccf-111">[Práce se šablonami](/powerapps/maker/portals/work-with-templates) - Toto téma poskytuje obecný přehled o tom, jak Power Apps portály fungují a jak můžete provádět jednoduché přizpůsobení portálů.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-111">[Work with templates](/powerapps/maker/portals/work-with-templates) – This topic provides a general overview of how Power Apps portals works and how you can do simple customizations of portals.</span></span>
- <span data-ttu-id="c7ccf-112">[Správa obsahu portálu](/dynamics365/portals/manage-portal-content) - Toto téma vysvětluje, jak můžete spravovat a přizpůsobovat obsah, který se objeví na vašem portálu.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-112">[Manage portal content](/dynamics365/portals/manage-portal-content) – This topic explains how you can manage and customize the content that you surface in your portal.</span></span>
- <span data-ttu-id="c7ccf-113">[Upravit CSS](/powerapps/maker/portals/edit-css) - Toto téma vám pomůže provádět složitější úpravy uživatelského rozhraní (UI) vašeho portálu.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-113">[Edit CSS](/powerapps/maker/portals/edit-css) – This topic helps you make more complex customizations to the user interface (UI) of your portal.</span></span>
- <span data-ttu-id="c7ccf-114">[Vytvořte téma pro svůj portál](/dynamics365/portals/create-theme) - Toto téma vám pomůže vytvořit motiv uživatelského rozhraní pro váš portál.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-114">[Create a theme for your portal](/dynamics365/portals/create-theme) – This topic helps you create a UI theme for your portal.</span></span>
- <span data-ttu-id="c7ccf-115">[Vytvářejte a exponujte obsah portálu snadno](/dynamics365/portals/create-expose-portal-content) - Toto téma vám pomůže spravovat základní data a tabulky, které používáte pro svůj portál.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-115">[Create and expose portal content easily](/dynamics365/portals/create-expose-portal-content) – This topic helps you manage the underlying data and tables that you use for your portal.</span></span>
- <span data-ttu-id="c7ccf-116">[Nakonfigurujte kontakt pro použití na portálu](/powerapps/maker/portals/configure/configure-contacts) - Toto téma vysvětluje, jak vytvářet a přizpůsobovat uživatelské role a jak funguje zabezpečení a ověřování Power Apps portálů.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-116">[Configure a contact for use on a portal](/powerapps/maker/portals/configure/configure-contacts) – This topic explains how to create and customize user roles, and how security and authentication work in Power Apps portals.</span></span>
- <span data-ttu-id="c7ccf-117">[Nakonfigurujte poznámky pro formuláře tabulky a webové formuláře na portálech](/powerapps/maker/portals/configure-notes) - Toto téma vysvětluje, jak přidat dokumenty a další úložiště na váš portál.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-117">[Configure notes for table forms and web forms on portals](/powerapps/maker/portals/configure-notes) – This topic explains how to add documents and additional storage to your portal.</span></span>
- <span data-ttu-id="c7ccf-118">[Chyba při manipulaci s webovým portálem](/powerapps/maker/portals/admin/view-portal-error-log) - Toto téma vysvětluje, jak zobrazit protokoly chyb portálu a uložit je do vašeho účtu úložiště blob Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-118">[Error handling for portal website](/powerapps/maker/portals/admin/view-portal-error-log) – This topic explains how to view portal error logs and store them in your Microsoft Azure Blob storage account.</span></span>

## <a name="customize-the-order-creation-process"></a><span data-ttu-id="c7ccf-119">Přizpůsobte proces vytváření objednávek</span><span class="sxs-lookup"><span data-stu-id="c7ccf-119">Customize the order creation process</span></span>

<span data-ttu-id="c7ccf-120">Když uživatel odešle objednávku pomocí zákaznického portálu, objednávka se automaticky synchronizuje s odpovídajícím prostředím Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-120">When a user submits an order by using the Customer portal, the order is automatically synced to the corresponding Dynamics 365 Supply Chain Management environment.</span></span> <span data-ttu-id="c7ccf-121">Protože je uživatel externím zákazníkem, některé požadované informace jsou před ním úmyslně skryty.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-121">Because the user is an external customer, some required information is intentionally hidden from him or her.</span></span> <span data-ttu-id="c7ccf-122">Tato informace bude automaticky vyplněna při odeslání formuláře.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-122">This information will automatically be filled in when the form is submitted.</span></span>

<span data-ttu-id="c7ccf-123">Tato část ukazuje, jak byste měli nastavit kontakty, abyste se vyhnuli chybám.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-123">This section shows how you should set up contacts to avoid errors.</span></span> <span data-ttu-id="c7ccf-124">Vysvětluje pole, která jsou automaticky nastavena a jak můžete upravit hodnotu těchto polí, pokud je to nutné.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-124">It explains fields that are automatically set and how you can modify the value of those fields if you must.</span></span>

### <a name="the-out-of-box-order-creation-process"></a><span data-ttu-id="c7ccf-125">Dodávaný proces vytváření objednávek</span><span class="sxs-lookup"><span data-stu-id="c7ccf-125">The out-of-box order creation process</span></span>

<span data-ttu-id="c7ccf-126">Zde jsou standardní kroky pro odeslání objednávky ze zákaznického portálu.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-126">Here are the standard steps for submitting an order from the Customer portal.</span></span>

1. <span data-ttu-id="c7ccf-127">Na domovské stránce vyberte dlaždici **Vytvořit objednávku** otevření průvodce **Vytvořit objednávku**.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-127">On the home page, select the **Create order** tile to open the **Create Order** wizard.</span></span>
1. <span data-ttu-id="c7ccf-128">Na stránce **Informace o objednávce** zadejte následující pole:</span><span class="sxs-lookup"><span data-stu-id="c7ccf-128">On the **Order Information** page, set the following fields:</span></span>

    - <span data-ttu-id="c7ccf-129">**Požadované datum přijetí** - Určete datum doručení.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-129">**Requested receipt date** – Specify the date of delivery.</span></span>
    - <span data-ttu-id="c7ccf-130">**Doručovací adresa** - Zadejte adresu, na kterou má být objednávka doručena.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-130">**Delivery address** – Enter the address that the order should be delivered to.</span></span>
    - <span data-ttu-id="c7ccf-131">**Společnost** - Vyberte název zákaznické společnosti.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-131">**Company** – Select the name of the customer company.</span></span> <span data-ttu-id="c7ccf-132">Toto pole je automaticky nastaveno pro neadministrátorské uživatele.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-132">This field is automatically set for non-admin users.</span></span>
    - <span data-ttu-id="c7ccf-133">**Číslo žádosti** - Zadejte číslo žádosti o objednávku.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-133">**Requisition number** – Enter the requisition number of the order.</span></span> <span data-ttu-id="c7ccf-134">Toto pole není povinné.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-134">This field isn't required.</span></span>
    - <span data-ttu-id="c7ccf-135">**Odeslat do země / oblasti** - Zadejte zemi nebo region, do kterého budou položky doručeny.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-135">**Ship to country/region** – Enter the country or region that the items will be delivered to.</span></span> <span data-ttu-id="c7ccf-136">Toto pole je automaticky nastaveno pro neadministrátorské uživatele.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-136">This field is automatically set for non-admin users.</span></span>

    <span data-ttu-id="c7ccf-137">![Stránka s informacemi o objednávce](media/customer-portal-order-information.png "Stránka s informacemi o objednávce")</span><span class="sxs-lookup"><span data-stu-id="c7ccf-137">![Order Information page](media/customer-portal-order-information.png "Order Information page")</span></span>

1. <span data-ttu-id="c7ccf-138">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-138">Select **Next**.</span></span>
1. <span data-ttu-id="c7ccf-139">Na stránce **Položky** vyberte **Přidat položku**.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-139">On the **Items** page, select **Add Item**.</span></span>

    <span data-ttu-id="c7ccf-140">![Stránka položek](media/customer-portal-items.png "Stránka položek")</span><span class="sxs-lookup"><span data-stu-id="c7ccf-140">![Items page](media/customer-portal-items.png "Items page")</span></span>

1. <span data-ttu-id="c7ccf-141">V dialogovém okně **Informace o položce** nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="c7ccf-141">In the **Item Information** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="c7ccf-142">**jméno výrobku** - Najděte a vyberte produkt, který chcete přidat do objednávky.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-142">**Product Name** – Find and select a product to add to the order.</span></span>
    - <span data-ttu-id="c7ccf-143">**Množství** - Zadejte množství vybraného produktu.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-143">**Quantity** – Enter the quantity of the selected product.</span></span>
    - <span data-ttu-id="c7ccf-144">**Jednotka** - Určete měrnou jednotku (například **ks**, **kg** nebo **krabice**).</span><span class="sxs-lookup"><span data-stu-id="c7ccf-144">**Unit** – Specify the unit of measure (for example, **ea.**, **kgs**, or **box**).</span></span>
    - <span data-ttu-id="c7ccf-145">**Odhadovaná čistá částka** - Hodnota se vypočítá jako odhadovaná cena položky × množství pro vybranou jednotku.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-145">**Estimated net amount** – The value is calculated as the estimated price of the item × the quantity for the selected unit.</span></span>

    <span data-ttu-id="c7ccf-146">![Dialogové okno Informace o položce](media/customer-portal-item-information.png "Dialogové okno Informace o položce")</span><span class="sxs-lookup"><span data-stu-id="c7ccf-146">![Item Information dialog box](media/customer-portal-item-information.png "Item Information dialog box")</span></span>

1. <span data-ttu-id="c7ccf-147">Vyberte **Odeslat** a přidejte položku do objednávky.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-147">Select **Submit** to add the item to the order.</span></span>
1. <span data-ttu-id="c7ccf-148">Opakujte kroky 4 až 6, dokud nepřidáte všechny položky, které chcete objednat.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-148">Repeat steps 4 through 6 until you've added all the items that you want to order.</span></span>
1. <span data-ttu-id="c7ccf-149">Po dokončení přidávání položek vyberte **Další** na stránce **Položky**.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-149">When you've finished adding items, select **Next** on the **Items** page.</span></span>
1. <span data-ttu-id="c7ccf-150">Stránka **Informace o objednávce** obsahuje shrnutí objednávky.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-150">The **Order Information** page provides a summary of the order.</span></span> <span data-ttu-id="c7ccf-151">Zkontrolujte obsah objednávky a podrobnosti o doručení.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-151">Review the order contents and delivery details.</span></span> <span data-ttu-id="c7ccf-152">Pokud vše vypadá správně, vyberte **Odeslat** k odeslání objednávky.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-152">If everything looks correct, select **Submit** to submit the order.</span></span>

    <span data-ttu-id="c7ccf-153">![Stránka s informacemi o objednávce](media/customer-portal-order-submit.png "Stránka s informacemi o objednávce")</span><span class="sxs-lookup"><span data-stu-id="c7ccf-153">![Order Information page](media/customer-portal-order-submit.png "Order Information page")</span></span>

### <a name="standard-data-setup"></a><span data-ttu-id="c7ccf-154">Standardní nastavení dat</span><span class="sxs-lookup"><span data-stu-id="c7ccf-154">Standard data setup</span></span>

<span data-ttu-id="c7ccf-155">Aby byl zajištěn hladký uživatelský dojem, portál pro zákazníky automaticky vyplňuje hodnoty pro několik požadovaných polí.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-155">To help ensure a smooth user experience, the Customer portal automatically fills in values for several required fields.</span></span> <span data-ttu-id="c7ccf-156">Tyto hodnoty vycházejí z informací v kontaktním záznamu zákazníka, který zadává objednávku.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-156">These values are based on information in the contact record of the customer who is submitting the order.</span></span>

<span data-ttu-id="c7ccf-157">Pro každý [záznam řádku](/powerapps/maker/portals/configure/configure-contacts) patřící zákazníkovi, který bude používat zákaznický portál k zadávání objednávek, je nutné zadat hodnoty pro následující povinná pole.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-157">For each [contact row](/powerapps/maker/portals/configure/configure-contacts) that belongs to a customer who will use the Customer portal to submit orders, values must be specified for the following required fields.</span></span> <span data-ttu-id="c7ccf-158">Jinak dojde k chybám.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-158">Otherwise, errors will occur.</span></span>

- <span data-ttu-id="c7ccf-159">**Společnost** – Právnická osoba, které náleží objednávka</span><span class="sxs-lookup"><span data-stu-id="c7ccf-159">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="c7ccf-160">**Potenciální zákazník** - Účet odběratele přidružený k objednávce</span><span class="sxs-lookup"><span data-stu-id="c7ccf-160">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="c7ccf-161">**Ceník** - Vlastní ceník pro zákazníka</span><span class="sxs-lookup"><span data-stu-id="c7ccf-161">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="c7ccf-162">**Měna** - Měna ceny</span><span class="sxs-lookup"><span data-stu-id="c7ccf-162">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="c7ccf-163">**Odeslat do země / oblasti** - Země nebo region, do kterého budou položky doručeny</span><span class="sxs-lookup"><span data-stu-id="c7ccf-163">**Ship to country/region** – The country or region that the items will be delivered to</span></span>

<span data-ttu-id="c7ccf-164">Pro tabulku prodejní objednávky jsou automaticky nastavena následující pole:</span><span class="sxs-lookup"><span data-stu-id="c7ccf-164">The following fields are automatically set for the sales order table:</span></span>

- <span data-ttu-id="c7ccf-165">**Jazyk** - Jazyk objednávky (ve výchozím nastavení je hodnota převzata z kontaktního záznamu.)</span><span class="sxs-lookup"><span data-stu-id="c7ccf-165">**Language** – The language of the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="c7ccf-166">**Odeslat do země / oblasti** - Země nebo region, do kterého budou položky doručeny (ve výchozím nastavení je hodnota převzata z kontaktního záznamu.)</span><span class="sxs-lookup"><span data-stu-id="c7ccf-166">**Ship to country/region** – The country or region that the items will be delivered to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="c7ccf-167">**Kontaktní osoba** - Uživatel, kterého lze kontaktovat pro informace o objednávce (Ve výchozím nastavení je hodnota převzata z kontaktního záznamu.)</span><span class="sxs-lookup"><span data-stu-id="c7ccf-167">**Contact person** – The user who can be contacted for information about the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="c7ccf-168">**Společnost** - Právnická osoba, které objednávka patří (ve výchozím nastavení je hodnota převzata z kontaktního záznamu.)</span><span class="sxs-lookup"><span data-stu-id="c7ccf-168">**Company** – The legal entity that the order belongs to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="c7ccf-169">**Potencionální zákazník** - Zákaznický účet, který je přidružen k objednávce (ve výchozím nastavení je hodnota převzata z kontaktního záznamu.)</span><span class="sxs-lookup"><span data-stu-id="c7ccf-169">**Potential customer** – The customer account that is associated with the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="c7ccf-170">**Zákazník na faktuře** - fakturační účet objednávky (ve výchozím nastavení je to potenciální zákazník z kontaktního záznamu.)</span><span class="sxs-lookup"><span data-stu-id="c7ccf-170">**Invoice customer** – The billing account of the order (The default value is the potential customer from the contact record.)</span></span>
- <span data-ttu-id="c7ccf-171">**Název prodejní objednávky** - Název prodejní objednávky (Výchozí hodnota je **prodejní objednávka** .)</span><span class="sxs-lookup"><span data-stu-id="c7ccf-171">**Sales order name** – The name of the sales order (The default value is **sales order**.)</span></span>
- <span data-ttu-id="c7ccf-172">**Měna** - Měna ceny (ve výchozím nastavení je hodnota převzata z kontaktního záznamu.)</span><span class="sxs-lookup"><span data-stu-id="c7ccf-172">**Currency** – The currency of the price (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="c7ccf-173">**Ceník** - Vlastní ceník pro zákazníka (Standardně je hodnota převzata z kontaktního záznamu.)</span><span class="sxs-lookup"><span data-stu-id="c7ccf-173">**Price list** – The custom price list for the customer (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="c7ccf-174">**Popis dodací adresy** - dodací adresa prodejní objednávky (výchozí hodnota je **popis dodací adresy** .)</span><span class="sxs-lookup"><span data-stu-id="c7ccf-174">**Delivery address description** – The delivery address of the sales order (The default value is **delivery address description**.)</span></span>

### <a name="modify-the-order-creation-process"></a><span data-ttu-id="c7ccf-175">Upravte proces vytváření objednávek</span><span class="sxs-lookup"><span data-stu-id="c7ccf-175">Modify the order creation process</span></span>

<span data-ttu-id="c7ccf-176">Pokud nezměníte základní proces vytváření objednávek, můžete libovolně upravovat vzhled a uživatelské rozhraní zákaznického portálu.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-176">You can freely modify the appearance and UI of the Customer portal if you don't change the basic order creation process.</span></span> <span data-ttu-id="c7ccf-177">Pokud chcete změnit proces vytváření objednávek, musíte mít na paměti několik bodů.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-177">If you want to change the order creation process, there are a few points that you must keep in mind.</span></span>

<span data-ttu-id="c7ccf-178">Neodstraňujte následující sloupce z tabulky prodejní objednávky v Microsoft Dataverse, protože musí vytvořit prodejní objednávku v režimu dvojitého zápisu:</span><span class="sxs-lookup"><span data-stu-id="c7ccf-178">Don't remove the following columns from the sales order table in Microsoft Dataverse, because they are required to create a sales order in dual-write:</span></span>

- <span data-ttu-id="c7ccf-179">**Společnost** – Právnická osoba, které náleží objednávka</span><span class="sxs-lookup"><span data-stu-id="c7ccf-179">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="c7ccf-180">**Název** – název prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="c7ccf-180">**Name** – The name of the sales order</span></span>
- <span data-ttu-id="c7ccf-181">**Měna** - Měna ceny</span><span class="sxs-lookup"><span data-stu-id="c7ccf-181">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="c7ccf-182">**Ceník** - Vlastní ceník pro zákazníka</span><span class="sxs-lookup"><span data-stu-id="c7ccf-182">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="c7ccf-183">**Odeslat do země / oblasti** - Země nebo region, do kterého budou položky doručeny</span><span class="sxs-lookup"><span data-stu-id="c7ccf-183">**Ship to country/region** – The country or region that the items will be delivered to</span></span>
- <span data-ttu-id="c7ccf-184">**Potenciální zákazník** - Účet odběratele přidružený k objednávce</span><span class="sxs-lookup"><span data-stu-id="c7ccf-184">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="c7ccf-185">**Jazyk** - Jazyk objednávky (Obvykle je tento jazyk jazykem potenciálního zákazníka.)</span><span class="sxs-lookup"><span data-stu-id="c7ccf-185">**Language** – The language of the order (Typically, this language is the language of the potential customer.)</span></span>
- <span data-ttu-id="c7ccf-186">**Popis dodací adresy** - dodací adresa prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="c7ccf-186">**Delivery address description** – The delivery address of the sales order</span></span>

<span data-ttu-id="c7ccf-187">U položek jsou požadovány následující sloupce:</span><span class="sxs-lookup"><span data-stu-id="c7ccf-187">For items, the following columns are required:</span></span>

- <span data-ttu-id="c7ccf-188">**Produkt** - Produkt k objednání</span><span class="sxs-lookup"><span data-stu-id="c7ccf-188">**Product** – The product to order</span></span>
- <span data-ttu-id="c7ccf-189">**Množství** - množství vybraného produktu</span><span class="sxs-lookup"><span data-stu-id="c7ccf-189">**Quantity** – The quantity of the selected product</span></span>
- <span data-ttu-id="c7ccf-190">**Jednotka** - Měrná jednotka (například **ks**, **kg** nebo **krabice**)</span><span class="sxs-lookup"><span data-stu-id="c7ccf-190">**Unit** – The unit of measure (for example, **ea.**, **kgs**, or **box**)</span></span>
- <span data-ttu-id="c7ccf-191">**Odeslat do země / oblasti** - Země nebo oblast doručení</span><span class="sxs-lookup"><span data-stu-id="c7ccf-191">**Ship to country/region** – The country or region of delivery</span></span>
- <span data-ttu-id="c7ccf-192">**Popis dodací adresy** - dodací adresa objednávky</span><span class="sxs-lookup"><span data-stu-id="c7ccf-192">**Delivery address description** – The delivery address of the order</span></span>

<span data-ttu-id="c7ccf-193">Musíte se ujistit, že váš zákaznický portál nějak předá hodnoty pro všechny tyto sloupce.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-193">You must make sure that your Customer portal somehow submits values for all these columns.</span></span>

<span data-ttu-id="c7ccf-194">Chcete-li na stránku přidat sloupce nebo je odstranit, viz [Vytvářejte nebo upravujte rychle vytvářené formuláře pro efektivnější zadávání dat](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span><span class="sxs-lookup"><span data-stu-id="c7ccf-194">If you want to add columns to the page, or remove columns, see [Create or edit quick create forms for a streamlined data entry experience](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span></span>

<span data-ttu-id="c7ccf-195">Pokud chcete změnit, jak jsou sloupce přednastaveny a jak jsou hodnoty nastaveny při uložení stránky, podívejte se na následující informace v dokumentaci portálů Power Apps:</span><span class="sxs-lookup"><span data-stu-id="c7ccf-195">If you want to change how columns are preset and how values are set when the page is saved, see the following information in the Power Apps portals documentation:</span></span>

- [<span data-ttu-id="c7ccf-196">Předem vyplněné pole</span><span class="sxs-lookup"><span data-stu-id="c7ccf-196">Prepopulate field</span></span>](/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [<span data-ttu-id="c7ccf-197">Nastavit hodnotu při uložení</span><span class="sxs-lookup"><span data-stu-id="c7ccf-197">Set Value On Save</span></span>](/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a><span data-ttu-id="c7ccf-198">Přizpůsobte domovskou stránku</span><span class="sxs-lookup"><span data-stu-id="c7ccf-198">Customize the home page</span></span>

<span data-ttu-id="c7ccf-199">Všechny ovládací prvky v zákaznickém portálu jsou vestavěné ovládací prvky portálů Power Apps.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-199">All the controls in the Customer portal are built-in Power Apps portals controls.</span></span> <span data-ttu-id="c7ccf-200">Můžete je upravit podle kroků v článku [Vytvořte stránku](/powerapps/maker/portals/compose-page) v dokumentaci portálů Power Apps.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-200">You can customize them by following the steps in [Compose a page](/powerapps/maker/portals/compose-page) in the Power Apps portals documentation.</span></span>

<span data-ttu-id="c7ccf-201">Jediný vlastní ovládací prvek, který je součástí šablony zákaznického portálu, se používá k vytvoření dlaždic na domovské stránce.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-201">The only custom control that is included in the Customer portal template is used to create the tiles on the home page.</span></span>

<span data-ttu-id="c7ccf-202">![Dlaždice na domovské stránce](media/customer-portal-home-page-tiles.png "Dlaždice na domovské stránce")</span><span class="sxs-lookup"><span data-stu-id="c7ccf-202">![Tiles on the home page](media/customer-portal-home-page-tiles.png "Tiles on the home page")</span></span>

<span data-ttu-id="c7ccf-203">Chcete-li upravit dlaždice, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-203">To modify the tiles, follow these steps.</span></span>

1. <span data-ttu-id="c7ccf-204">Otevřete [Aplikaci pro správu portálu](/powerapps/maker/portals/configure/configure-portal).</span><span class="sxs-lookup"><span data-stu-id="c7ccf-204">Open the [Portal Management app](/powerapps/maker/portals/configure/configure-portal).</span></span>
1. <span data-ttu-id="c7ccf-205">V navigačním podokně nalevo vyberte položku **Šablony stránky**.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-205">In the navigation pane on the left, select **Page Templates**.</span></span>

    <span data-ttu-id="c7ccf-206">![Navigační podokno správy portálu](media/customer-portal-nav.png "Navigační podokno správy portálu")</span><span class="sxs-lookup"><span data-stu-id="c7ccf-206">![Portal Management navigation pane](media/customer-portal-nav.png "Portal Management navigation pane")</span></span>

1. <span data-ttu-id="c7ccf-207">Vyberte šablonu stránky s názvem **Domov**.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-207">Select the page template that is named **Home**.</span></span>
1. <span data-ttu-id="c7ccf-208">V poli **Webová šablona** vyberte okaz **Domov** pro otevření zdrojového kódu pro tuto stránku.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-208">In the **Web Template** field, select the **Home** link to open the source code for that page.</span></span>

    <span data-ttu-id="c7ccf-209">![Pole webové šablony](media/customer-portal-web-template.png "Pole webové šablony")</span><span class="sxs-lookup"><span data-stu-id="c7ccf-209">![Web Template field](media/customer-portal-web-template.png "Web Template field")</span></span>

1. <span data-ttu-id="c7ccf-210">Nyní byste měli vidět veškerý zdrojový kód domovské stránky a můžete jej podle potřeby upravit.</span><span class="sxs-lookup"><span data-stu-id="c7ccf-210">You should now see all the source code for the home page and can modify it as you require.</span></span>

## <a name="resources"></a><span data-ttu-id="c7ccf-211">Prostředky</span><span class="sxs-lookup"><span data-stu-id="c7ccf-211">Resources</span></span>

<span data-ttu-id="c7ccf-212">Další informace o tom, jak můžete nastavit a přizpůsobit zákaznický portál, naleznete v následujících zdrojích:</span><span class="sxs-lookup"><span data-stu-id="c7ccf-212">To learn more about how you can set up and customize the Customer portal, see the following resources:</span></span>

- [<span data-ttu-id="c7ccf-213">Dokumentace portálů Power Apps</span><span class="sxs-lookup"><span data-stu-id="c7ccf-213">Power Apps portals documentation</span></span>](/powerapps/maker/portals/overview)
- [<span data-ttu-id="c7ccf-214">Dokumentace dvojitého zápisu</span><span class="sxs-lookup"><span data-stu-id="c7ccf-214">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [<span data-ttu-id="c7ccf-215">O životním cyklu portálu</span><span class="sxs-lookup"><span data-stu-id="c7ccf-215">About portal lifecycle</span></span>](/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="c7ccf-216">Upgradujte portál</span><span class="sxs-lookup"><span data-stu-id="c7ccf-216">Upgrade a portal</span></span>](/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="c7ccf-217">Migrace konfigurace portálu</span><span class="sxs-lookup"><span data-stu-id="c7ccf-217">Migrate portal configuration</span></span>](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="c7ccf-218">Správa životního cyklu řešení: aplikace Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="c7ccf-218">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]