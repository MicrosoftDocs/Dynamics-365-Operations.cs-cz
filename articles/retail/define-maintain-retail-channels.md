---
title: Definování a udržování maloobchodní sítě
description: V tomto tématu je přehled procesu pro nastavení kamenných obchodů, které se v aplikaci Dynamics 365 Retail označují jako maloobchody. Jsou zde informace o úkolech, které je nutné dokončit před a po nastavení maloobchodu.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 45d0386d215da15103a417502debb245c91f6309
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934601"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="cc2a6-104">Definování a udržování maloobchodní sítě</span><span class="sxs-lookup"><span data-stu-id="cc2a6-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cc2a6-105">V tomto tématu je přehled procesu pro nastavení kamenných obchodů, které se v aplikaci Dynamics 365 Retail označují jako maloobchody.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Dynamics 365 Retail.</span></span> <span data-ttu-id="cc2a6-106">Jsou zde informace o úkolech, které je nutné dokončit před a po nastavení maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="cc2a6-107">Retail podporuje více maloobchodních sítí, jako např. online obchody, call centra a kamenné obchody.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-107">Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="cc2a6-108">Kamenný obchod se nazývá maloobchod.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="cc2a6-109">Každý maloobchod může mít vlastní metodu plateb, cenové skupiny, pokladny na pokladních místech (POS), účty příjmů a výdajů a zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="cc2a6-110">Všechny tyto prvky je třeba nastavit pro maloobchod před jeho vytvořením.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="cc2a6-111">Po vytvoření maloobchodu přiřadíte produkty, které má obchod obsahovat.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="cc2a6-112">K obchodu můžete také přiřadit zaměstnance, pokladny a odběratele.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="cc2a6-113">Nakonec přidejte nový obchod do organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="cc2a6-114">Nastavení maloobchodů</span><span class="sxs-lookup"><span data-stu-id="cc2a6-114">Setting up retail stores</span></span>

<span data-ttu-id="cc2a6-115">Před nastavením maloobchodu v aplikaci Retail je nutné dokončit některé předpoklady.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-115">Before you can set up a retail store in Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="cc2a6-116">Poté můžete vytvořit maloobchod a přidat podrobné informace.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="cc2a6-117">Požadavky</span><span class="sxs-lookup"><span data-stu-id="cc2a6-117">Prerequisites</span></span>

<span data-ttu-id="cc2a6-118">Před nastavením maloobchodu je nutné dokončit následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="cc2a6-118">You must complete the following tasks before you can set up a retail store:</span></span>

1. <span data-ttu-id="cc2a6-119">Nastavte organizační strukturu a upravte nastavení organizační hierarchie pro sortiment, doplnění a vykazování maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="cc2a6-120">Vytvořte sklad, který bude maloobchod představovat.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-120">Set up a warehouse that represents the retail store.</span></span>
3. <span data-ttu-id="cc2a6-121">Nastavte číselné řady pro maloobchod, příkazy obchodu a doklady výkazu obchodu.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="cc2a6-122">Konfigurujte parametry pro maloobchod.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-122">Configure parameters for Retail.</span></span>
5. <span data-ttu-id="cc2a6-123">Nastavení metody platby, kterou obchod přijímá.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="cc2a6-124">Pro zpracování transakcí platebních karet v maloobchodním pokladním místě (POS) můžete také nastavit platební služby.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="cc2a6-125">Nastavení skupin DPH.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="cc2a6-126">Nastavení maloobchodních produktů.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-126">Set up retail products.</span></span> <span data-ttu-id="cc2a6-127">V rámci této úlohy můžete také nastavit hierarchie maloobchodních produktů, varianty produktu a sortiment produktů.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="cc2a6-128">Nastavení cenových skupin výrobků.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-128">Set up product price groups.</span></span>
10. <span data-ttu-id="cc2a6-129">Nastavení tvorby cen maloobchodních produktů.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-129">Set up retail product pricing.</span></span> <span data-ttu-id="cc2a6-130">V rámci této úlohy můžete také nastavit úpravy cen, slevy a období slevy.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="cc2a6-131">Nastavení zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cc2a6-132">Poznámka: Je nutné také přiřadit příslušná oprávnění zaměstnancům, aby se mohli přihlásit a provést úlohy pomocí systému Retail POS.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Retail POS system.</span></span>

12. <span data-ttu-id="cc2a6-133">Konfigurace profilů Retail POS pro přiřazení k obchodu.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="cc2a6-134">Tato úloha zahrnuje mnoho dalších úloh, například nastavení pokladny, nastavení profilu offline a nastavení formátů a profilů účtenky.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="cc2a6-135">Zobrazte všechny úkoly, které jsou zahrnuty v předpokladech, a dokončete pouze úlohy, které se vás týkají.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="cc2a6-136">Nastavení maloobchodní prodejny</span><span class="sxs-lookup"><span data-stu-id="cc2a6-136">Set up a retail store</span></span>

<span data-ttu-id="cc2a6-137">Po dokončení požadovaných úloh dokončete tyto úlohy a nastavte tak podrobné informace o maloobchodě:</span><span class="sxs-lookup"><span data-stu-id="cc2a6-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1. <span data-ttu-id="cc2a6-138">Vytvoření maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-138">Create a retail store.</span></span>
2. <span data-ttu-id="cc2a6-139">Přiřazení skupiny DPH k obchodu.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="cc2a6-140">Přiřazení způsobů plateb přijímaných v obchodě.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="cc2a6-141">Přidejte podrobnosti do popisu produktu u produktů nabízených ve vašem maloobchodě.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="cc2a6-142">Můžete například přidat formátovaný text a obrázky.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="cc2a6-143">Tyto podrobnosti k produktu se zobrazují v různých kontextech, například v pokladně POS nebo na vytištěných štítcích.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="cc2a6-144">Přidejte obchod do výchozí organizační hierarchie, která je přiřazena k účelu **Maloobchodní sortiment**, **Doplnění maloobchodu** nebo **Vykazování maloobchodu**.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="cc2a6-145">Po nastavení maloobchodu</span><span class="sxs-lookup"><span data-stu-id="cc2a6-145">After you set up a retail store</span></span>

<span data-ttu-id="cc2a6-146">Po zadání podrobností pro maloobchod dokončete tyto úlohy a odešlete nová data maloobchodu do Retail POS:</span><span class="sxs-lookup"><span data-stu-id="cc2a6-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1. <span data-ttu-id="cc2a6-147">Nastavte pokladny POS pro obchod.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="cc2a6-148">Přiřazení sortimentů produktů k obchodu.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="cc2a6-149">Zpracujte sortiment, vytvořte seznam produktů, které jsou zahrnuty v sortimentu a zpřístupněte produkty v maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4. <span data-ttu-id="cc2a6-150">Odešlete data, jako číselné řady, profily hardwaru a rozložení obrazovky POS, do pokladen Retail POS.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5. <span data-ttu-id="cc2a6-151">Publikujte maloobchod a odešlete tak data obchodu do Retail POS.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-151">Publish the retail store to send store data to Retail POS.</span></span>
6. <span data-ttu-id="cc2a6-152">Spusťte úlohy a odešlete data obchodu do Retail POS.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="cc2a6-153">Organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="cc2a6-153">Organization hierarchies</span></span>

<span data-ttu-id="cc2a6-154">Retail používá hierarchie organizace pro potřeby strukturování maloobchodních kanálů.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="cc2a6-155">Organizační hierarchie představuje vztahy mezi organizacemi, které tvoří váš podnik.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="cc2a6-156">Při nastavování obchodů je můžete přidat do organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="cc2a6-157">Obchody poté budou sdílet data, která se používají pro sortimenty, doplnění a vykazování.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="cc2a6-158">Chcete-li použít funkci maloobchodního prodeje, je nutné povolit konfigurační klíč **Více dodacích adres**.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-158">To use Retail sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="cc2a6-159">Tento konfigurační klíč je k dispozici v klíčích **Obchodní konfigurace** ve složce **Správa systému**\> **Nastavení** \> **Konfigurace licence**.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="cc2a6-160">To je vyžadováno z důvodu maloobchodní funkčnosti, která provádí různá ověření na základě dodací adresy nakonfigurované na úrovni řádku prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="cc2a6-160">This is required due to Retail functionality that performs various validations based on the delivery address configured at the sales order line level.</span></span>
