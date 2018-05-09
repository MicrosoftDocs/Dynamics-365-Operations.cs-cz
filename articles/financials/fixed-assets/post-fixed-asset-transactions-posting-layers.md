---
title: "Transakce dlouhodobého majetku zaúčtované do účtovací vrstvy"
description: "V tomto článku naleznete přehled o funkci účtovací vrstvy pro transakce dlouhodobého majetku."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3001
ms.assetid: 7dabde57-0843-47c3-85ef-f36b6f472e30
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a1d12f5910e38f683ee161f6fab9422db715745b
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="post-fixed-asset-transactions-to-posting-layers"></a><span data-ttu-id="ecb74-103">Transakce dlouhodobého majetku zaúčtované do účtovací vrstvy</span><span class="sxs-lookup"><span data-stu-id="ecb74-103">Post fixed asset transactions to posting layers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecb74-104">V tomto článku naleznete přehled o funkci účtovací vrstvy pro transakce dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="ecb74-104">This article gives an overview of posting layer functionality for fixed asset transactions.</span></span>

<span data-ttu-id="ecb74-105">Dlouhodobý majetek se často odepisuje různými způsoby za různými účely.</span><span class="sxs-lookup"><span data-stu-id="ecb74-105">A fixed asset is often depreciated in different ways for different purposes.</span></span> <span data-ttu-id="ecb74-106">Odpisy pro daňové účely se vypočítávají pomocí platných daňových pravidel pro dosažení co nejvyšších odpisů před zdaněním, ale odpisy pro účely vykazování se vypočítávají podle účetních zákonů a pravidel.</span><span class="sxs-lookup"><span data-stu-id="ecb74-106">Depreciation for tax purposes is calculated by using current tax rules to achieve the highest possible depreciation before taxes, but depreciation for reporting purposes is calculated according to accounting laws and standards.</span></span> <span data-ttu-id="ecb74-107">Různé druhy odpisů se vypočítávají a zaznamenávají odděleně v účtovacích vrstvách.</span><span class="sxs-lookup"><span data-stu-id="ecb74-107">The various kinds of depreciation are calculated and recorded separately in the posting layers.</span></span>

<span data-ttu-id="ecb74-108">Každá kniha, která je připojena k dlouhodobému majetku, se vytváří pro určitou účtovací vrstvu, která má celkový cíl odpisu.</span><span class="sxs-lookup"><span data-stu-id="ecb74-108">Each book that is attached to a fixed asset is set up for a particular posting layer that has an overall depreciation objective.</span></span> <span data-ttu-id="ecb74-109">Existuje deset účtovacích vrstev: Aktuální, Operace, Daň a sedm vlastních vrstev.</span><span class="sxs-lookup"><span data-stu-id="ecb74-109">There are ten posting layers: Current, Operations, Tax, and seven Custom layers.</span></span> <span data-ttu-id="ecb74-110">Zaúčtování knihy do hlavní knihy také můžete zakázat nastavením hodnoty v poli Zaúčtovat do hlavní knihy na hodnotu Ne.</span><span class="sxs-lookup"><span data-stu-id="ecb74-110">You can also disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="ecb74-111">Pole Účtovací vrstva se automaticky nastaví na Žádná.</span><span class="sxs-lookup"><span data-stu-id="ecb74-111">The Posting layer field is then automatically set to None.</span></span> <span data-ttu-id="ecb74-112">Knihy, které nebudou zaúčtovány do hlavní knihy, se obvykle používají pro účely vykazování daně.</span><span class="sxs-lookup"><span data-stu-id="ecb74-112">Typically, books that don’t post to the general ledger are used for tax reporting purposes.</span></span> <span data-ttu-id="ecb74-113">Tento přístup vám dává další flexibilitu k odstranění historických transakcí pro knihu majetku, protože nebyly potvrzeny do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="ecb74-113">This approach gives you the additional flexibility to delete historical transactions for the asset book, because they haven’t been committed to the general ledger.</span></span>

<span data-ttu-id="ecb74-114">Deníky dlouhodobého majetku jsou definovány na stránce Názvy deníků v části Hlavní kniha > Nastavení deníku > Názvy deníků.</span><span class="sxs-lookup"><span data-stu-id="ecb74-114">Fixed asset journals are defined by using the Journal names page at General ledger > Journal setup > Journal names.</span></span> <span data-ttu-id="ecb74-115">Každý deník, do kterého lze zaúčtovat odpisy, je určen svým názvem deníku platným jen pro jednu účtovací vrstvu.</span><span class="sxs-lookup"><span data-stu-id="ecb74-115">Each journal that you can post depreciations in is defined by its journal name for only one posting layer.</span></span> <span data-ttu-id="ecb74-116">Účtovací vrstvu v deníku nelze změnit.</span><span class="sxs-lookup"><span data-stu-id="ecb74-116">The posting layer in the journal can’t be changed.</span></span> <span data-ttu-id="ecb74-117">Toto omezení pomáhá zajistit, že transakce pro každou účtovací vrstvu jsou udržovány odděleně.</span><span class="sxs-lookup"><span data-stu-id="ecb74-117">This restriction helps guarantee that transactions for each posting layer are kept separate.</span></span> <span data-ttu-id="ecb74-118">Je nutné vytvořit alespoň jeden název deníku pro každou účtovací vrstvu.</span><span class="sxs-lookup"><span data-stu-id="ecb74-118">At least one journal name must be created for each posting layer.</span></span> <span data-ttu-id="ecb74-119">Pokud používáte knihy, které nechcete zaúčtovat do hlavní knihy, je také nutné vytvořit deník, kde je účtovací vrstva nastavena na Žádná.</span><span class="sxs-lookup"><span data-stu-id="ecb74-119">If you’re using books that don’t post to the general ledger, you must also create a journal where the posting layer is set to None.</span></span>

<span data-ttu-id="ecb74-120">Na stránce Účetní profily dlouhodobého majetku lze označit účty hlavní knihy pro transakce dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="ecb74-120">You can designate ledger accounts for fixed asset transactions on the Fixed asset posting profiles page.</span></span> <span data-ttu-id="ecb74-121">Pro každý účetní profil vyberte odpovídající typ transakce a knihy a potom označte účty hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="ecb74-121">For each posting profile, you must select the relevant transaction type and book, and then designate the ledger accounts.</span></span> <span data-ttu-id="ecb74-122">Nastavte záznam účetního profilu pro každou knihu, která se zaúčtuje do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="ecb74-122">Set up a posting profile record for each book that will post to the general ledger.</span></span>

> [!NOTE] 
> <span data-ttu-id="ecb74-123">Používání odvozených knih umožňuje zároveň zaúčtovat transakce do jiných účtovacích vrstev.</span><span class="sxs-lookup"><span data-stu-id="ecb74-123">By using derived books, you can post transactions to different posting layers at the same time.</span></span> <span data-ttu-id="ecb74-124">Vytvoříte transakce primární knihy v deníku s účtovací vrstvou, která odpovídá účtovací vrstvě knihy.</span><span class="sxs-lookup"><span data-stu-id="ecb74-124">You create the transactions of the primary book in a journal where the posting layer corresponds to the book posting layer.</span></span> <span data-ttu-id="ecb74-125">Při účtování se odvozené transakce knihy zaúčtují do příslušných účtovacích vrstev.</span><span class="sxs-lookup"><span data-stu-id="ecb74-125">During posting, the derived book transactions are posted to the appropriate posting layers.</span></span>

<span data-ttu-id="ecb74-126">Další informace naleznete v části [Odvozené knihy](derived-books.md) a [Zaúčtování pomocí odvozených knih](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="ecb74-126">For more information see, [Derived books](derived-books.md) and [Posting with derived books](post-derived-value-models.md).</span></span>




