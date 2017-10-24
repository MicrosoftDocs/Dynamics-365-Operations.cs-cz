--- 
title: "Nastavení knih"
description: "Tento postup popisuje, jak vytvořit novou knihu dlouhodobého majetku a přidružit ji ke skupině dlouhodobého majetku."
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a29cae6cdcd03903359a3a468243c6ad03c7adc6
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-books"></a><span data-ttu-id="072a5-103">Nastavení knih</span><span class="sxs-lookup"><span data-stu-id="072a5-103">Set up books</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="072a5-104">Tento postup popisuje, jak vytvořit novou knihu dlouhodobého majetku a přidružit ji ke skupině dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="072a5-104">This procedure shows you to how create a new fixed asset book and associate it with a fixed asset group.</span></span> <span data-ttu-id="072a5-105">Využívá účetní role a ukázková data pro právnické osoby USMF.</span><span class="sxs-lookup"><span data-stu-id="072a5-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-book"></a><span data-ttu-id="072a5-106">Vytvoření knihy</span><span class="sxs-lookup"><span data-stu-id="072a5-106">Create a book</span></span>
1. <span data-ttu-id="072a5-107">Přejděte do části Dlouhodobý majetek > Nastavení > Knihy.</span><span class="sxs-lookup"><span data-stu-id="072a5-107">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="072a5-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="072a5-108">Click New.</span></span>
3. <span data-ttu-id="072a5-109">Zadejte hodnotu do pole Kniha.</span><span class="sxs-lookup"><span data-stu-id="072a5-109">In the Book field, type a value.</span></span>
4. <span data-ttu-id="072a5-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="072a5-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="072a5-111">Pokud je vybrána možnost Výpočet odpisu, přidružené knihy majetku budou zahrnuty v návrzích odpisů.</span><span class="sxs-lookup"><span data-stu-id="072a5-111">If Calculate depreciation is selected, the associated asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="072a5-112">Pokud není hodnota vybrána, nebude se kniha majetku automaticky odepisovat.</span><span class="sxs-lookup"><span data-stu-id="072a5-112">If it is not selected, the asset book will not be automatically depreciated.</span></span>  
5. <span data-ttu-id="072a5-113">Vyberte možnost Ano v poli Výpočet odpisu.</span><span class="sxs-lookup"><span data-stu-id="072a5-113">Select Yes in the Calculate depreciation field.</span></span>
6. <span data-ttu-id="072a5-114">V poli Profil odpisu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="072a5-114">In the Depreciation profile field, enter or select a value.</span></span>
    * <span data-ttu-id="072a5-115">Pro alternativní odpisový plán se rovněž používá označení přepínací způsob odpisu.</span><span class="sxs-lookup"><span data-stu-id="072a5-115">An alternative depreciation profile is also known as a switchover method of depreciation.</span></span> <span data-ttu-id="072a5-116">Návrh odpisu se přepne na tento profil při výpočtu částky odpisu v alternativním profilu, která je rovna nebo větší než hodnota výchozího odpisového profilu.</span><span class="sxs-lookup"><span data-stu-id="072a5-116">The depreciation proposal will switch to this profile when the alternative profile calculates a depreciation amount that is equal to or greater than the default depreciation profile.</span></span>  
    * <span data-ttu-id="072a5-117">Plán mimořádných odpisů se používá pro dodatečný odpis majetku při neobvyklých okolností.</span><span class="sxs-lookup"><span data-stu-id="072a5-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="072a5-118">Například to můžete použít k záznamu odpisů, které je výsledkem živelné pohromy.</span><span class="sxs-lookup"><span data-stu-id="072a5-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
    * <span data-ttu-id="072a5-119">Pokud vyberete možnost Vytvořit úpravy odpisů s úpravami základu, úpravy odpisů se vytvoří automaticky při aktualizaci hodnoty majetku.</span><span class="sxs-lookup"><span data-stu-id="072a5-119">If Create depreciation adjustments with basis adjustments is selected, depreciation adjustments will be automatically created when the value of the asset is updated.</span></span> <span data-ttu-id="072a5-120">Jestliže není možnost zaškrtnuta, aktualizované hodnoty majetku ovlivní pouze výpočty odpisů do budoucna.</span><span class="sxs-lookup"><span data-stu-id="072a5-120">If it is not selected, the updated asset value will only affect depreciation calculations going forward.</span></span>  
7. <span data-ttu-id="072a5-121">V poli Vytvořit úpravy odpisů s úpravami základu vyberte Ano.</span><span class="sxs-lookup"><span data-stu-id="072a5-121">Select Yes in the Create depreciation adjustments with basis adjustments field.</span></span>
    * <span data-ttu-id="072a5-122">Ve výchozím nastavení se do hlavní knihy zaúčtují transakce knihy dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="072a5-122">By default, fixed asset book transactions will post to the general ledger.</span></span> <span data-ttu-id="072a5-123">Zaúčtování knihy do hlavní knihy můžete zakázat nastavením hodnoty v poli Zaúčtovat do hlavní knihy na hodnotu Ne.</span><span class="sxs-lookup"><span data-stu-id="072a5-123">You can disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="072a5-124">Knihy, které nebudou zaúčtovány do hlavní knihy, se obvykle používají pro účely vykazování daně.</span><span class="sxs-lookup"><span data-stu-id="072a5-124">Books that do not post to the general ledger are typically used for tax reporting purposes.</span></span> <span data-ttu-id="072a5-125">To vám dává další flexibilitu k odstranění historických transakcí pro knihu majetku, protože nebyly potvrzeny do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="072a5-125">This gives you additional flexibility to delete historical transactions for the asset book because they have not been committed to the general ledger.</span></span>  
    * <span data-ttu-id="072a5-126">Pokud se kniha zaúčtuje do hlavní knihy, účtovací vrstva bude mít ve výchozím nastavení hodnotu Aktuální vrstva a pokud se do hlavní knihy nezaúčtuje, bude mít hodnotu Žádný.</span><span class="sxs-lookup"><span data-stu-id="072a5-126">The Posting layer defaults to the Current layer if the book posts to general ledger, and None if it does not post to general ledger.</span></span> <span data-ttu-id="072a5-127">Aktualizujte Účtovací vrstvu, pokud potřebujete, aby transakce pro tuto knihu byly zaúčtovány do jiné vrstvy.</span><span class="sxs-lookup"><span data-stu-id="072a5-127">Update Posting layer if you need transactions for this book to be posted to a different layer.</span></span>  
8. <span data-ttu-id="072a5-128">V poli Kalendář zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="072a5-128">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="072a5-129">Odvozené knihy budou zaúčtovávat transakce do různých knih najednou.</span><span class="sxs-lookup"><span data-stu-id="072a5-129">Derived books will post transactions to different books at the same time.</span></span> <span data-ttu-id="072a5-130">Vytvoříte transakce s primární knihou a při zaúčtovávání se přesná kopie transakce zaúčtuje do odvozené knihy.</span><span class="sxs-lookup"><span data-stu-id="072a5-130">You create the transactions with the primary book and during posting, an exact copy of the transaction is posted to the derived book.</span></span> <span data-ttu-id="072a5-131">Neexistuje žádný přepočet s transakcemi odvozených knih, proto není vhodné použít je pro transakce odpisů.</span><span class="sxs-lookup"><span data-stu-id="072a5-131">There is no recalculation with derived book transactions, so it should not be used for depreciation transactions.</span></span>  

## <a name="associate-the-book-with-a-fixed-asset-group"></a><span data-ttu-id="072a5-132">Přiřazení knihy ke skupině dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="072a5-132">Associate the book with a fixed asset group</span></span>
1. <span data-ttu-id="072a5-133">Klikněte na Skupiny dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="072a5-133">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="072a5-134">Zadejte nebo vyberte hodnotu v poli Skupina dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="072a5-134">In the Fixed asset group field, enter or select a value.</span></span>
3. <span data-ttu-id="072a5-135">Zadejte číslo do pole Doba životnosti.</span><span class="sxs-lookup"><span data-stu-id="072a5-135">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="072a5-136">Všimněte si, že hodnota pole Období odpisu se vypočítá po nastavení doby životnosti.</span><span class="sxs-lookup"><span data-stu-id="072a5-136">Note that Depreciation periods is calculated after setting the Service life.</span></span>  
    * <span data-ttu-id="072a5-137">Způsob odpisu je možné nastavit podle potřeby pro daňové účely.</span><span class="sxs-lookup"><span data-stu-id="072a5-137">You are able to set the depreciation convention as required for tax purposes.</span></span>  


