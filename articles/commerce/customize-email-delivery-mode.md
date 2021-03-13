---
title: Přizpůsobení transakčních e-mailů podle způsobu doručení
description: Toto téma popisuje, jak nastavit vlastní e-mailové šablony pro konkrétní typy oznámení a způsoby doručení v Microsoft Dynamics 365 Commerce.
author: stuharg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: f4ecb990cfe792e92142f922c43c71ef8494e117
ms.sourcegitcommit: da17648c296b22d517eadb2f71c7803672e5648d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031841"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a><span data-ttu-id="a7001-103">Přizpůsobení transakčních e-mailů podle způsobu doručení</span><span class="sxs-lookup"><span data-stu-id="a7001-103">Customize transactional emails by mode of delivery</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a7001-104">Toto téma popisuje, jak nastavit vlastní e-mailové šablony pro konkrétní typy oznámení a způsoby doručení v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a7001-104">This topic describes how to set up custom email templates for specific notification types and modes of delivery in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a7001-105">Transakční e-maily lze nyní přizpůsobit pro kombinaci typu oznámení (například **Objednávka byla vytvořena**, **Objednávka byla zabalena** nebo **Objednávka byla fakturována**) a způsobu doručení (například přes noc, vyzvednutí na prodejně nebo pouliční výdej).</span><span class="sxs-lookup"><span data-stu-id="a7001-105">Transactional emails can now be customized for a combination of a notification type (for example, **Order created**, **Order packed**, or **Order invoiced**) and a mode of delivery (for example, overnight, in-store pickup, or curbside pickup).</span></span> <span data-ttu-id="a7001-106">Vlastní transakční e-maily umožňují maloobchodníkům poskytnout svým zákazníkům objednávku, která je přizpůsobena způsobu jejího doručení.</span><span class="sxs-lookup"><span data-stu-id="a7001-106">Custom transactional emails let retailers provide their customers order with fulfillment experiences that are tailored to the order's mode of delivery.</span></span> <span data-ttu-id="a7001-107">Například událost „objednávka byla zabalena“ lze například přizpůsobit tak, aby poskytovala pokyny pro pouliční výdej pro zákazníky, kteří si jej vybrali.</span><span class="sxs-lookup"><span data-stu-id="a7001-107">For example, the "order packed" event can be customized so that it provides curbside pickup instructions for customers who choose curbside pickup.</span></span> <span data-ttu-id="a7001-108">Alternativně může obsahovat přepravce a informace o doručení pro zákazníky, kteří se rozhodnou nechat svou objednávku odeslat.</span><span class="sxs-lookup"><span data-stu-id="a7001-108">Alternatively, it can provide shipping carrier and delivery information for customers who choose to have their order shipped.</span></span>

> [!NOTE]
> <span data-ttu-id="a7001-109">Chcete-li použít funkci přizpůsobených transakčních e-mailů, musíte nejprve zapnout funkci **Přizpůsobení šablon transakčních e-mailů podle způsobu doručení** přechodem na **Pracovní prostory \> Správa funkcí** v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="a7001-109">To use the functionality for customized transactional emails, you first must turn on the **Customize transactional email templates by mode of delivery** feature by going to **Workspaces \> Feature management** in Commerce headquarters.</span></span>

<span data-ttu-id="a7001-110">E-maily lze přizpůsobit podle způsobu doručení pro následující typy oznámení:</span><span class="sxs-lookup"><span data-stu-id="a7001-110">Emails can be customized by mode of delivery for the following notification types:</span></span>

- <span data-ttu-id="a7001-111">**Objednávka byla stornována** – Tento typ e-mailového oznámení je nový.</span><span class="sxs-lookup"><span data-stu-id="a7001-111">**Order cancellation** – This email notification type is new.</span></span>
- <span data-ttu-id="a7001-112">**Objednávka byla vytvořena**</span><span class="sxs-lookup"><span data-stu-id="a7001-112">**Order created**</span></span>
- <span data-ttu-id="a7001-113">**Objednávka byla potvrzena.**</span><span class="sxs-lookup"><span data-stu-id="a7001-113">**Order confirmed**</span></span>
- <span data-ttu-id="a7001-114">**Objednávka byla fakturována** – Tento typ e-mailového oznámení je nový.</span><span class="sxs-lookup"><span data-stu-id="a7001-114">**Order invoiced** – This email notification type is new.</span></span> <span data-ttu-id="a7001-115">Může být použit místo typu oznámení **Objednávka byla poslána**, které odešle oznámení o jakékoli fakturační události, která má expedovaný způsob doručení (nikoli vyzvednutí, vyvezení nebo elektronický způsob doručení).</span><span class="sxs-lookup"><span data-stu-id="a7001-115">It can be used instead of the **Order shipped** notification type that will send a notification for any invoice event that has a shipped mode of delivery (not a pickup, carry out, or electronic mode of delivery).</span></span>
- <span data-ttu-id="a7001-116">**Objednávka byla vyskladněna**</span><span class="sxs-lookup"><span data-stu-id="a7001-116">**Order picked**</span></span>
- <span data-ttu-id="a7001-117">**Objednávka byla zabalena**</span><span class="sxs-lookup"><span data-stu-id="a7001-117">**Order packed**</span></span>
- <span data-ttu-id="a7001-118">**Objednávka připravena k vyzvednutí** – Tento typ oznámení lze upravit podle způsobu doručení, pouze pokud je zapnuta funkce **Podpora více způsobů vyzvednutí/doručení**.</span><span class="sxs-lookup"><span data-stu-id="a7001-118">**Order ready for pickup** – This notification type can be customized by mode of delivery only if the **Support for multiple pickup delivery modes** feature is turned on.</span></span> <span data-ttu-id="a7001-119">V takovém případě je tento typ oznámení funkčně ekvivalentní s typem oznámení **Objednávka byla zabalena**.</span><span class="sxs-lookup"><span data-stu-id="a7001-119">In that case, this notification type is functionally equivalent to the **Order packed** notification type.</span></span>
- <span data-ttu-id="a7001-120">**Platba se nezdařila.**</span><span class="sxs-lookup"><span data-stu-id="a7001-120">**Payment failed**</span></span>
- <span data-ttu-id="a7001-121">**Objednávka náhrady byla vytvořena.**</span><span class="sxs-lookup"><span data-stu-id="a7001-121">**Replacement order created**</span></span>

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a><span data-ttu-id="a7001-122">Konfigurace e-mailových šablon pro konkrétní způsoby doručení</span><span class="sxs-lookup"><span data-stu-id="a7001-122">Configure email templates for specific modes of delivery</span></span>

<span data-ttu-id="a7001-123">U tohoto postupu se předpokládá, že jste již vytvořili své nové, vlastní e-mailové šablony a přidali je na stránku **E-mailové šablony organizace**.</span><span class="sxs-lookup"><span data-stu-id="a7001-123">For this procedure, the assumption is that you've already created your new, custom email templates and added them to the **Organization email templates** page.</span></span> <span data-ttu-id="a7001-124">Informace, jak vytvořit a nahrát e-mailové šablony, najdete v části [Vytvoření e-mailových šablon pro transakční události](email-templates-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="a7001-124">For information about how to create and upload email templates, see [Create email templates for transactional events](email-templates-transactions.md).</span></span>

<span data-ttu-id="a7001-125">Chcete-li nakonfigurovat e-mailové šablony pro konkrétní způsoby doručení v centrále Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="a7001-125">To configure email templates for specific modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a7001-126">Jděte na **Profil e-mailového oznámení Commerce**.</span><span class="sxs-lookup"><span data-stu-id="a7001-126">Go to **Commerce email notification profile**.</span></span>
1. <span data-ttu-id="a7001-127">Pod **Nastavení maloobchodního oznámení události** vyberte existující typ oznámení.</span><span class="sxs-lookup"><span data-stu-id="a7001-127">Under **Retail event notification settings**, select an existing notification type.</span></span>
1. <span data-ttu-id="a7001-128">Ponechte vybrán typ oznámení a vyberte **Konfigurace způsobů doručení**.</span><span class="sxs-lookup"><span data-stu-id="a7001-128">While the notification type is still selected, select **Configure modes of delivery**.</span></span>
1. <span data-ttu-id="a7001-129">V dialogovém okně **Způsoby doručení** zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="a7001-129">In the **Modes of delivery** dialog box, select **New**.</span></span>
1. <span data-ttu-id="a7001-130">V novém řádku v poli **Způsob doručení** zvolte způsob doručení.</span><span class="sxs-lookup"><span data-stu-id="a7001-130">In the new row, in the **Mode of delivery** field, select a mode of delivery.</span></span>
1. <span data-ttu-id="a7001-131">V poli **ID e-mailu** vyberte e-mailovou šablonu, kterou chcete namapovat na způsob doručení.</span><span class="sxs-lookup"><span data-stu-id="a7001-131">In the **Email ID** field, select the email template to map to the mode of delivery.</span></span>
1. <span data-ttu-id="a7001-132">Zaškrtněte políčko **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="a7001-132">Select the **Active** check box.</span></span>
1. <span data-ttu-id="a7001-133">Opakováním kroků 4 až 7 přidejte další způsoby doručení.</span><span class="sxs-lookup"><span data-stu-id="a7001-133">Repeat steps 4 through 7 to add more modes of delivery.</span></span>
1. <span data-ttu-id="a7001-134">Po dokončení zvolte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7001-134">When you've finished, select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="a7001-135">Pokud je v prodejní objednávce na řádcích více než jeden způsob doručení, použije se výchozí šablona.</span><span class="sxs-lookup"><span data-stu-id="a7001-135">When more than one mode of delivery is present across lines in a sales order, the default template will be used.</span></span> <span data-ttu-id="a7001-136">Výchozí šablona je šablona, která je namapována na typ oznámení na stránce **Profil e-mailového oznámení Commerce**.</span><span class="sxs-lookup"><span data-stu-id="a7001-136">The default template is the template that is mapped to the notification type on the **Commerce email notification profile** page.</span></span>
> - <span data-ttu-id="a7001-137">Pokud má prodejní objednávka způsob doručení, který nebyl nakonfigurován pro vlastní e-mailovou šablonu, použije se výchozí e-mailová šablona.</span><span class="sxs-lookup"><span data-stu-id="a7001-137">If a sales order has a mode of delivery that hasn't been configured for a custom email template, the default email template will be used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a7001-138">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="a7001-138">Additional resources</span></span>

[<span data-ttu-id="a7001-139">Vytváření objednávek v kontaktním středisku</span><span class="sxs-lookup"><span data-stu-id="a7001-139">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="a7001-140">Změna způsobu dodání v POS</span><span class="sxs-lookup"><span data-stu-id="a7001-140">Change mode of delivery in POS</span></span>](pos-change-delivery-mode.md)
