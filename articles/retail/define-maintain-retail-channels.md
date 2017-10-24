---
title: "Definování a udržování maloobchodní sítě"
description: "V tomto článku je přehled procesu pro nastavení kamenných obchodů, které se v aplikaci Microsoft Dynamics 365 for Retail označují jako maloobchody. Jsou zde informace o úkolech, které je nutné dokončit před a po nastavení maloobchodu."
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 700b8868a68be7f0172202d737b4f1ae9813ecf3
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="5fe49-104">Definování a udržování maloobchodní sítě</span><span class="sxs-lookup"><span data-stu-id="5fe49-104">Define and maintain retail channels</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="5fe49-105">V tomto článku je přehled procesu pro nastavení kamenných obchodů, které se v aplikaci Microsoft Dynamics 365 for Retail označují jako maloobchody.</span><span class="sxs-lookup"><span data-stu-id="5fe49-105">This article provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="5fe49-106">Jsou zde informace o úkolech, které je nutné dokončit před a po nastavení maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="5fe49-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="5fe49-107">Dynamics 365 for Retail podporuje více maloobchodních sítí, jako např. online obchody, kontaktní střediska a kamenné obchody.</span><span class="sxs-lookup"><span data-stu-id="5fe49-107">Dynamics 365 for Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="5fe49-108">Kamenný obchod se nazývá maloobchod.</span><span class="sxs-lookup"><span data-stu-id="5fe49-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="5fe49-109">Každý maloobchod může mít vlastní metodu plateb, cenové skupiny, pokladny na pokladních místech (POS), účty příjmů a výdajů a zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="5fe49-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="5fe49-110">Všechny tyto prvky je třeba nastavit pro maloobchod před jeho vytvořením.</span><span class="sxs-lookup"><span data-stu-id="5fe49-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="5fe49-111">Po vytvoření maloobchodu přiřadíte produkty, které má obchod obsahovat.</span><span class="sxs-lookup"><span data-stu-id="5fe49-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="5fe49-112">K obchodu můžete také přiřadit zaměstnance, pokladny a odběratele.</span><span class="sxs-lookup"><span data-stu-id="5fe49-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="5fe49-113">Nakonec přidejte nový obchod do organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="5fe49-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="5fe49-114">Nastavení maloobchodů</span><span class="sxs-lookup"><span data-stu-id="5fe49-114">Setting up retail stores</span></span>
<span data-ttu-id="5fe49-115">Před nastavením maloobchodu v aplikaci Microsoft Dynamics 365 for Retail je nutné dokončit některé předpoklady.</span><span class="sxs-lookup"><span data-stu-id="5fe49-115">Before you can set up a retail store in Dynamics 365 for Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="5fe49-116">Poté můžete vytvořit maloobchod a přidat podrobné informace.</span><span class="sxs-lookup"><span data-stu-id="5fe49-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="5fe49-117">Požadavky</span><span class="sxs-lookup"><span data-stu-id="5fe49-117">Prerequisites</span></span>

<span data-ttu-id="5fe49-118">Před nastavením maloobchodu je nutné dokončit následující úkoly:</span><span class="sxs-lookup"><span data-stu-id="5fe49-118">You must complete the following tasks before you can set up a retail store:</span></span>

1.  <span data-ttu-id="5fe49-119">Nastavte organizační strukturu a upravte nastavení organizační hierarchie pro sortiment, doplnění a vykazování maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="5fe49-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2.  <span data-ttu-id="5fe49-120">Vytvořte sklad, který bude maloobchod představovat.</span><span class="sxs-lookup"><span data-stu-id="5fe49-120">Set up a warehouse that represents the retail store.</span></span>
3.  <span data-ttu-id="5fe49-121">Nastavte číselné řady pro maloobchod, příkazy obchodu a doklady výkazu obchodu.</span><span class="sxs-lookup"><span data-stu-id="5fe49-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4.  <span data-ttu-id="5fe49-122">Konfigurujte parametry pro maloobchod.</span><span class="sxs-lookup"><span data-stu-id="5fe49-122">Configure parameters for Retail.</span></span>
5.  <span data-ttu-id="5fe49-123">Nastavení metody platby, kterou obchod přijímá.</span><span class="sxs-lookup"><span data-stu-id="5fe49-123">Set up the methods of payment that the store accepts.</span></span>
6.  <span data-ttu-id="5fe49-124">Pro zpracování transakcí platebních karet v maloobchodním pokladním místě (POS) můžete také nastavit platební služby.</span><span class="sxs-lookup"><span data-stu-id="5fe49-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7.  <span data-ttu-id="5fe49-125">Nastavení skupin DPH.</span><span class="sxs-lookup"><span data-stu-id="5fe49-125">Set up sales tax groups.</span></span>
8.  <span data-ttu-id="5fe49-126">Nastavení maloobchodních produktů.</span><span class="sxs-lookup"><span data-stu-id="5fe49-126">Set up retail products.</span></span> <span data-ttu-id="5fe49-127">V rámci této úlohy můžete také nastavit hierarchie maloobchodních produktů, varianty produktu a sortiment produktů.</span><span class="sxs-lookup"><span data-stu-id="5fe49-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9.  <span data-ttu-id="5fe49-128">Nastavení cenových skupin výrobků.</span><span class="sxs-lookup"><span data-stu-id="5fe49-128">Set up product price groups.</span></span>
10. <span data-ttu-id="5fe49-129">Nastavení tvorby cen maloobchodních produktů.</span><span class="sxs-lookup"><span data-stu-id="5fe49-129">Set up retail product pricing.</span></span> <span data-ttu-id="5fe49-130">V rámci této úlohy můžete také nastavit úpravy cen, slevy a období slevy.</span><span class="sxs-lookup"><span data-stu-id="5fe49-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="5fe49-131">Nastavení zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="5fe49-131">Set up staff members.</span></span> <span data-ttu-id="5fe49-132">**Poznámka:** Je nutné také přiřadit příslušná oprávnění zaměstnancům, aby se mohli přihlásit a provést úlohy pomocí aplikace Dynamics 365 for Retail pro systém Retail POS.</span><span class="sxs-lookup"><span data-stu-id="5fe49-132">**Note:** You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Dynamics 365 for Retail for Retail POS system.</span></span>
12. <span data-ttu-id="5fe49-133">Konfigurace profilů Retail POS pro přiřazení k obchodu.</span><span class="sxs-lookup"><span data-stu-id="5fe49-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="5fe49-134">Tato úloha zahrnuje mnoho dalších úloh, například nastavení pokladny, nastavení profilu offline a nastavení formátů a profilů účtenky.</span><span class="sxs-lookup"><span data-stu-id="5fe49-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="5fe49-135">Zobrazte všechny úkoly, které jsou zahrnuty v předpokladech, a dokončete pouze úlohy, které se vás týkají.</span><span class="sxs-lookup"><span data-stu-id="5fe49-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="5fe49-136">Nastavení maloobchodní prodejny</span><span class="sxs-lookup"><span data-stu-id="5fe49-136">Set up a retail store</span></span>

<span data-ttu-id="5fe49-137">Po dokončení požadovaných úloh dokončete tyto úlohy a nastavte tak podrobné informace o maloobchodě:</span><span class="sxs-lookup"><span data-stu-id="5fe49-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1.  <span data-ttu-id="5fe49-138">Vytvoření maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="5fe49-138">Create a retail store.</span></span>
2.  <span data-ttu-id="5fe49-139">Přiřazení skupiny DPH k obchodu.</span><span class="sxs-lookup"><span data-stu-id="5fe49-139">Assign a sales tax group to the store.</span></span>
3.  <span data-ttu-id="5fe49-140">Přiřazení způsobů plateb přijímaných v obchodě.</span><span class="sxs-lookup"><span data-stu-id="5fe49-140">Assign the accepted payment methods to the store.</span></span>
4.  <span data-ttu-id="5fe49-141">Přidejte podrobnosti do popisu produktu u produktů nabízených ve vašem maloobchodě.</span><span class="sxs-lookup"><span data-stu-id="5fe49-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="5fe49-142">Můžete například přidat formátovaný text a obrázky.</span><span class="sxs-lookup"><span data-stu-id="5fe49-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="5fe49-143">Tyto podrobnosti k produktu se zobrazují v různých kontextech, například v pokladně POS nebo na vytištěných štítcích.</span><span class="sxs-lookup"><span data-stu-id="5fe49-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5.  <span data-ttu-id="5fe49-144">Přidejte obchod do výchozí organizační hierarchie, která je přiřazena k účelu **Maloobchodní sortiment**, **Doplnění maloobchodu** nebo **Vykazování maloobchodu**.</span><span class="sxs-lookup"><span data-stu-id="5fe49-144">Add the store to an the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="5fe49-145">Po nastavení maloobchodu</span><span class="sxs-lookup"><span data-stu-id="5fe49-145">After you set up a retail store</span></span>

<span data-ttu-id="5fe49-146">Po zadání podrobností pro maloobchod dokončete tyto úlohy a odešlete nová data maloobchodu do Retail POS:</span><span class="sxs-lookup"><span data-stu-id="5fe49-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1.  <span data-ttu-id="5fe49-147">Nastavte pokladny POS pro obchod.</span><span class="sxs-lookup"><span data-stu-id="5fe49-147">Configure the POS registers for the store.</span></span>
2.  <span data-ttu-id="5fe49-148">Přiřazení sortimentů produktů k obchodu.</span><span class="sxs-lookup"><span data-stu-id="5fe49-148">Assign product assortments to the store.</span></span>
3.  <span data-ttu-id="5fe49-149">Zpracujte sortiment, vytvořte seznam produktů, které jsou zahrnuty v sortimentu a zpřístupněte produkty v maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="5fe49-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4.  <span data-ttu-id="5fe49-150">Odešlete data, jako číselné řady, profily hardwaru a rozložení obrazovky POS, do pokladen Retail POS.</span><span class="sxs-lookup"><span data-stu-id="5fe49-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5.  <span data-ttu-id="5fe49-151">Publikujte maloobchod a odešlete tak data obchodu do Retail POS.</span><span class="sxs-lookup"><span data-stu-id="5fe49-151">Publish the retail store to send store data to Retail POS.</span></span>
6.  <span data-ttu-id="5fe49-152">Spusťte úlohy a odešlete data obchodu do Retail POS.</span><span class="sxs-lookup"><span data-stu-id="5fe49-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="5fe49-153">Organizační hierarchie</span><span class="sxs-lookup"><span data-stu-id="5fe49-153">Organization hierarchies</span></span>
<span data-ttu-id="5fe49-154">Retail používá hierarchie organizace pro potřeby strukturování maloobchodních kanálů.</span><span class="sxs-lookup"><span data-stu-id="5fe49-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="5fe49-155">Organizační hierarchie představuje vztahy mezi organizacemi, které tvoří váš podnik.</span><span class="sxs-lookup"><span data-stu-id="5fe49-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="5fe49-156">Při nastavování obchodů je můžete přidat do organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="5fe49-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="5fe49-157">Obchody poté budou sdílet data, která se používají pro sortimenty, doplnění a vykazování.</span><span class="sxs-lookup"><span data-stu-id="5fe49-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>




