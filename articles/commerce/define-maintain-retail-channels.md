---
title: Definování a udržování maloobchodní sítě
description: V tomto tématu je přehled procesu pro nastavení kamenných obchodů, které se v aplikaci Dynamics 365 Commerce označují jako obchody. Jsou zde informace o úkolech, které je nutné dokončit před a po nastavení obchodu.
author: mugunthanm
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7a2db169adafa1b8a0113024f3f58522c2cee6d2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802014"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="46137-104">Definování a udržování maloobchodní sítě</span><span class="sxs-lookup"><span data-stu-id="46137-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="46137-105">V tomto tématu je přehled procesu pro nastavení kamenných obchodů, které se v aplikaci Dynamics 365 Commerce označují jako obchody.</span><span class="sxs-lookup"><span data-stu-id="46137-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as stores in Dynamics 365 Commerce.</span></span> <span data-ttu-id="46137-106">Jsou zde informace o úkolech, které je nutné dokončit před a po nastavení obchodu.</span><span class="sxs-lookup"><span data-stu-id="46137-106">It includes information about the tasks that you must complete both before and after you set up a store.</span></span>

<span data-ttu-id="46137-107">Commerce podporuje více obchodních sítí, jako například online obchody, kontaktní střediska a kamenné obchody.</span><span class="sxs-lookup"><span data-stu-id="46137-107">Commerce supports multiple channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="46137-108">Kamenný obchod se nazývá obchod.</span><span class="sxs-lookup"><span data-stu-id="46137-108">A brick-and-mortar store is called a store.</span></span> <span data-ttu-id="46137-109">Každý obchod může mít vlastní metodu plateb, cenové skupiny, pokladny na pokladních místech (POS), účty příjmů a výdajů a zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="46137-109">Each store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="46137-110">Všechny tyto prvky je třeba nastavit pro obchod před jeho vytvořením.</span><span class="sxs-lookup"><span data-stu-id="46137-110">You must set up all these elements for a store before you create it.</span></span> <span data-ttu-id="46137-111">Po vytvoření obchodu přiřadíte produkty, které má obchod obsahovat.</span><span class="sxs-lookup"><span data-stu-id="46137-111">After you create the store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="46137-112">K obchodu můžete také přiřadit zaměstnance, pokladny a odběratele.</span><span class="sxs-lookup"><span data-stu-id="46137-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="46137-113">Nakonec přidejte nový obchod do organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="46137-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-stores"></a><span data-ttu-id="46137-114">Nastavení obchodů</span><span class="sxs-lookup"><span data-stu-id="46137-114">Setting up stores</span></span>

<span data-ttu-id="46137-115">Před nastavením maloobchodu v Commerce je nutné dokončit některé předpoklady.</span><span class="sxs-lookup"><span data-stu-id="46137-115">Before you can set up a store in Commerce, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="46137-116">Poté můžete vytvořit obchod a přidat podrobné informace.</span><span class="sxs-lookup"><span data-stu-id="46137-116">You can then create the store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="46137-117">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="46137-117">Prerequisites</span></span>

<span data-ttu-id="46137-118">Před nastavením obchodu je nutné dokončit následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="46137-118">You must complete the following tasks before you can set up a store:</span></span>

1. <span data-ttu-id="46137-119">Nastavte organizační strukturu a upravte nastavení organizační hierarchie pro sortiment, doplnění a vykazování maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="46137-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="46137-120">Vytvořte sklad, který bude obchod představovat.</span><span class="sxs-lookup"><span data-stu-id="46137-120">Set up a warehouse that represents the store.</span></span>
3. <span data-ttu-id="46137-121">Nastavte číselné řady pro obchod, příkazy obchodu a doklady výkazu obchodu.</span><span class="sxs-lookup"><span data-stu-id="46137-121">Set up number sequences for stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="46137-122">Konfigurovat parametry pro Commerce.</span><span class="sxs-lookup"><span data-stu-id="46137-122">Configure parameters for Commerce.</span></span>
5. <span data-ttu-id="46137-123">Nastavení metody platby, kterou obchod přijímá.</span><span class="sxs-lookup"><span data-stu-id="46137-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="46137-124">Pro zpracování transakcí platebních karet v pokladním místě (POS) můžete také nastavit platební služby.</span><span class="sxs-lookup"><span data-stu-id="46137-124">To process credit card transactions at POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="46137-125">Nastavení skupin DPH.</span><span class="sxs-lookup"><span data-stu-id="46137-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="46137-126">Nastavení produktů.</span><span class="sxs-lookup"><span data-stu-id="46137-126">Set up products.</span></span> <span data-ttu-id="46137-127">V rámci této úlohy můžete také nastavit hierarchie obchodních produktů, varianty produktu a sortiment produktů.</span><span class="sxs-lookup"><span data-stu-id="46137-127">As part of this task, you also set up product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="46137-128">Nastavení cenových skupin výrobků.</span><span class="sxs-lookup"><span data-stu-id="46137-128">Set up product price groups.</span></span>
10. <span data-ttu-id="46137-129">Nastavit ceny produktu.</span><span class="sxs-lookup"><span data-stu-id="46137-129">Set up product pricing.</span></span> <span data-ttu-id="46137-130">V rámci této úlohy můžete také nastavit úpravy cen, slevy a období slevy.</span><span class="sxs-lookup"><span data-stu-id="46137-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="46137-131">Nastavení zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="46137-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="46137-132">Poznámka: Je nutné také přiřadit příslušná oprávnění zaměstnancům, aby se mohli přihlásit a provést úlohy pomocí systému POS.</span><span class="sxs-lookup"><span data-stu-id="46137-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the POS system.</span></span>

12. <span data-ttu-id="46137-133">Konfigurace profilů POS pro přiřazení k obchodu.</span><span class="sxs-lookup"><span data-stu-id="46137-133">Configure the POS profiles to assign to the store.</span></span> <span data-ttu-id="46137-134">Tato úloha zahrnuje mnoho dalších úloh, například nastavení pokladny, nastavení profilu offline a nastavení formátů a profilů účtenky.</span><span class="sxs-lookup"><span data-stu-id="46137-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="46137-135">Zobrazte všechny úkoly, které jsou zahrnuty v předpokladech, a dokončete pouze úlohy, které se vás týkají.</span><span class="sxs-lookup"><span data-stu-id="46137-135">Review all the tasks that are included in the prerequisites, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-store"></a><span data-ttu-id="46137-136">Nastavit obchod</span><span class="sxs-lookup"><span data-stu-id="46137-136">Set up a store</span></span>

<span data-ttu-id="46137-137">Po dokončení požadovaných úloh dokončete tyto úlohy a nastavte tak podrobné informace o obchodě:</span><span class="sxs-lookup"><span data-stu-id="46137-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the store:</span></span>

1. <span data-ttu-id="46137-138">Vytvoření obchodu.</span><span class="sxs-lookup"><span data-stu-id="46137-138">Create a store.</span></span>
2. <span data-ttu-id="46137-139">Přiřazení skupiny DPH k obchodu.</span><span class="sxs-lookup"><span data-stu-id="46137-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="46137-140">Přiřazení způsobů plateb přijímaných v obchodě.</span><span class="sxs-lookup"><span data-stu-id="46137-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="46137-141">Přidejte podrobnosti do popisu produktu u produktů nabízených ve vašich obchodech.</span><span class="sxs-lookup"><span data-stu-id="46137-141">Add details to the product descriptions for products that you offer in your stores.</span></span> <span data-ttu-id="46137-142">Můžete například přidat formátovaný text a obrázky.</span><span class="sxs-lookup"><span data-stu-id="46137-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="46137-143">Tyto podrobnosti k produktu se zobrazují v různých kontextech, například v pokladně POS nebo na vytištěných štítcích.</span><span class="sxs-lookup"><span data-stu-id="46137-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="46137-144">Přidejte obchod do výchozí organizační hierarchie, která je přiřazena k účelu **Maloobchodní sortiment**, **Doplnění maloobchodu** nebo **Vykazování maloobchodu**.</span><span class="sxs-lookup"><span data-stu-id="46137-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-store"></a><span data-ttu-id="46137-145">Po nastavení obchodu</span><span class="sxs-lookup"><span data-stu-id="46137-145">After you set up a store</span></span>

<span data-ttu-id="46137-146">Po zadání podrobností pro obchod dokončete tyto úlohy a odešlete nová data obchodu do POS:</span><span class="sxs-lookup"><span data-stu-id="46137-146">After you enter the details for the store, complete these tasks to send the new store data to POS:</span></span>

1. <span data-ttu-id="46137-147">Nastavte pokladny POS pro obchod.</span><span class="sxs-lookup"><span data-stu-id="46137-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="46137-148">Přiřazení sortimentů produktů k obchodu.</span><span class="sxs-lookup"><span data-stu-id="46137-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="46137-149">Zpracujte sortiment, vytvořte seznam produktů, které jsou zahrnuty v sortimentu a zpřístupněte produkty v obchodu.</span><span class="sxs-lookup"><span data-stu-id="46137-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the store.</span></span>
4. <span data-ttu-id="46137-150">Odešlete data, jako číselné řady, profily hardwaru a rozložení obrazovky POS, do pokladen POS.</span><span class="sxs-lookup"><span data-stu-id="46137-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the POS registers.</span></span>
5. <span data-ttu-id="46137-151">Publikujte obchod a odešlete tak data obchodu do POS.</span><span class="sxs-lookup"><span data-stu-id="46137-151">Publish the store to send store data to POS.</span></span>
6. <span data-ttu-id="46137-152">Spusťte úlohu a odešlete tak data obchodu do POS.</span><span class="sxs-lookup"><span data-stu-id="46137-152">Run the jobs to send the store data to POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="46137-153">Organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="46137-153">Organization hierarchies</span></span>

<span data-ttu-id="46137-154">Commerce používá hierarchie organizace pro potřeby strukturování obchodních kanálů.</span><span class="sxs-lookup"><span data-stu-id="46137-154">Commerce uses organization hierarchies to structure channels.</span></span> <span data-ttu-id="46137-155">Organizační hierarchie představuje vztahy mezi organizacemi, které tvoří váš podnik.</span><span class="sxs-lookup"><span data-stu-id="46137-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="46137-156">Při nastavování obchodů je můžete přidat do organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="46137-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="46137-157">Obchody poté budou sdílet data, která se používají pro sortimenty, doplnění a vykazování.</span><span class="sxs-lookup"><span data-stu-id="46137-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="46137-158">Chcete-li použít funkci Commerce prodeje, je nutné povolit konfigurační klíč **Více dodacích adres**.</span><span class="sxs-lookup"><span data-stu-id="46137-158">To use Commerce sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="46137-159">Tento konfigurační klíč je k dispozici v klíčích **Obchodní konfigurace** ve složce **Správa systému**\> **Nastavení** \> **Konfigurace licence**.</span><span class="sxs-lookup"><span data-stu-id="46137-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="46137-160">To je vyžadováno z důvodu různých ověření na základě dodací adresy nakonfigurované na úrovni řádku prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="46137-160">This is required due to various validations based on the delivery address configured at the sales order line level.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]