---
title: Odpisy dlouhodobého majetku
description: Toto téma podává přehled odpisu pro dlouhodobý majetek.
author: ShylaThompson
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ec8544b885485781b0b9c0a59ec47f90fdceb6b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826875"
---
# <a name="fixed-asset-depreciation"></a><span data-ttu-id="84a2f-103">Odpisy dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="84a2f-103">Fixed asset depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84a2f-104">Toto téma podává přehled odpisu pro dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="84a2f-104">This topic provides an overview of depreciation for fixed assets.</span></span>

<span data-ttu-id="84a2f-105">Odpis představuje periodickou transakci, která obvykle snižuje hodnotu dlouhodobého majetku v rozvaze a v knize zisků a ztrát účtována jako výdaj.</span><span class="sxs-lookup"><span data-stu-id="84a2f-105">Depreciation is a periodic transaction that typically reduces the value of the fixed asset on the balance sheet, and is charged as an expenditure to a profit and loss account.</span></span> <span data-ttu-id="84a2f-106">Proto se hlavní účet obvykle použije pro odepsání pravidelného odpisu do rozvahy.</span><span class="sxs-lookup"><span data-stu-id="84a2f-106">Therefore, a main account is typically used to credit the periodic depreciation on the balance sheet.</span></span> <span data-ttu-id="84a2f-107">Protiúčet je účtem v části zisků a ztrát účtové osnovy.</span><span class="sxs-lookup"><span data-stu-id="84a2f-107">An offset account is an account in the profit and loss part of the chart of accounts.</span></span>

## <a name="depreciation-adjustment"></a><span data-ttu-id="84a2f-108">Oprava odpisu</span><span class="sxs-lookup"><span data-stu-id="84a2f-108">Depreciation adjustment</span></span>
<span data-ttu-id="84a2f-109">Obvykle je pouze oprava již zaúčtované transakce odpisu zaúčtována jako oprava odpisu.</span><span class="sxs-lookup"><span data-stu-id="84a2f-109">Usually, only a correction to a posted depreciation transaction is posted as a depreciation adjustment.</span></span> <span data-ttu-id="84a2f-110">Proto se hlavní účet a protiúčet nastaví stejně jako účty pro odpis.</span><span class="sxs-lookup"><span data-stu-id="84a2f-110">Therefore, both the main account and the offset account are set up just like the accounts for depreciation.</span></span> <span data-ttu-id="84a2f-111">Opravy odpisu lze provést u kladné i záporné částky, avšak funkce hlavního účtu (jako účet rozvahy) a protiúčtu (obvykle jako účet zisků a ztrát) zůstane stejná.</span><span class="sxs-lookup"><span data-stu-id="84a2f-111">A depreciation adjustment can be either a positive amount or a negative amount, but the functionality of the main account (as a balance sheet account) and the functionality of the offset account (usually as a profit and loss account) remain the same.</span></span>

## <a name="extraordinary-depreciation"></a><span data-ttu-id="84a2f-112">Mimořádný odpis</span><span class="sxs-lookup"><span data-stu-id="84a2f-112">Extraordinary depreciation</span></span>
<span data-ttu-id="84a2f-113">Mimořádné odpisy fungují stejně jako základní.</span><span class="sxs-lookup"><span data-stu-id="84a2f-113">Extraordinary depreciation works like basic depreciation.</span></span> <span data-ttu-id="84a2f-114">Proto se hlavní účet používá k zaúčtování částky odpisu do rozvahy a snížení hodnoty dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="84a2f-114">Therefore, a main account is used to credit the depreciation amount to the balance sheet and reduce the value of the fixed asset.</span></span> <span data-ttu-id="84a2f-115">Protiúčet je účet zisků a ztrát, kde je odpis, který se vypočítá pro fiskální období, účtován jako výdaj.</span><span class="sxs-lookup"><span data-stu-id="84a2f-115">An offset account is a profit and loss account, where the depreciation that is calculated for the fiscal period is charged as an expenditure.</span></span> 

<span data-ttu-id="84a2f-116">Mimořádný odpis není závislý na základním odpisu.</span><span class="sxs-lookup"><span data-stu-id="84a2f-116">Extraordinary depreciation works independently of basic depreciation.</span></span> <span data-ttu-id="84a2f-117">Pokud máte mimořádný odpis jako samostatný typ transakce, můžete mimořádný odpis zaúčtovat a vykazovat nezávisle na základním odpisu.</span><span class="sxs-lookup"><span data-stu-id="84a2f-117">By having extraordinary depreciation as a separate transaction type, you can post and report the extraordinary depreciation separately from the basic depreciation.</span></span>

## <a name="special-depreciation-allowance"></a><span data-ttu-id="84a2f-118">Náhrada za zvláštní odpisy</span><span class="sxs-lookup"><span data-stu-id="84a2f-118">Special depreciation allowance</span></span>
<span data-ttu-id="84a2f-119">Náhrady za zvláštní odpisy umožňují odepsat mimořádné částky odpisu během prvního roku, ve kterém se majetek začal používat a odepisovat.</span><span class="sxs-lookup"><span data-stu-id="84a2f-119">You can use special depreciation allowances to take extra depreciation amounts during the first year that an asset is put in service and depreciated.</span></span> <span data-ttu-id="84a2f-120">Náhrady za zvláštní odpisy musí být provedeny před veškerými jinými výpočty odpisů.</span><span class="sxs-lookup"><span data-stu-id="84a2f-120">Special depreciation allowances must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="84a2f-121">Vzhledem k tomu, že náhrady za zvláštní odpisy jsou obvykle neznámé až do pozdější servisní životnosti dlouhodobého majetku, je nejvhodnější používat tento druh odpisů v knize, která nezaúčtovává do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="84a2f-121">Because special depreciation allowances are often unknown until later in the service life of the fixed asset, it's best to use this type of depreciation with a book that doesn't post to the general ledger.</span></span> <span data-ttu-id="84a2f-122">Můžete použít funkci Odstranit transakce, které nebyly zaúčtovány do hlavní knihy k odstranění historie transakcí pro tyto knihy.</span><span class="sxs-lookup"><span data-stu-id="84a2f-122">You can use the Delete transactions not posted to general ledger periodic function to delete the transaction history for these books.</span></span> <span data-ttu-id="84a2f-123">Pak lze odstranit historii odpisů pro knihu dlouhodobého majetku, zaúčtovat náhradu za zvláštní odpisy, když je známá, a zaúčtovat zbývající odpisovou transakci na rok.</span><span class="sxs-lookup"><span data-stu-id="84a2f-123">You can then delete the depreciation history for the fixed asset book, post the special depreciation allowance when it's known, and then post the remaining depreciation transactions for the year.</span></span> 

<span data-ttu-id="84a2f-124">Lze vytvořit neomezený počet záznamů náhrady za zvláštní odpisy.</span><span class="sxs-lookup"><span data-stu-id="84a2f-124">You can create an unlimited number of special depreciation allowance records.</span></span> <span data-ttu-id="84a2f-125">Jakmile tyto záznamy přiřadíte ke knize odpisů skupiny majetku, použijí se i v knize odpisů majetku.</span><span class="sxs-lookup"><span data-stu-id="84a2f-125">After you assign those records to an asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="84a2f-126">Náhrada za zvláštní odpisy se zadává jako procento nebo pevná částka.</span><span class="sxs-lookup"><span data-stu-id="84a2f-126">A special depreciation allowance is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="84a2f-127">Při zaúčtování návrhů na odpisy budou transakce náhrady za zvláštní odpisy zaúčtovány do knihy odpisů jako transakce, které jsou odděleny od odpisových transakcí.</span><span class="sxs-lookup"><span data-stu-id="84a2f-127">When you post depreciation proposals, special depreciation allowance transactions are posted to the book as transactions that are separate from the depreciation transactions.</span></span>

## <a name="depreciation-calendars"></a><span data-ttu-id="84a2f-128">Odpisové kalendáře</span><span class="sxs-lookup"><span data-stu-id="84a2f-128">Depreciation calendars</span></span>
<span data-ttu-id="84a2f-129">Každá kniha má kalendář, který se použije při odpisu dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="84a2f-129">Each book has a calendar that is used when you depreciate fixed assets.</span></span> <span data-ttu-id="84a2f-130">Kniha ve výchozím nastavení použije fiskální kalendář hlavní knihy, pokud neuvedete kalendář knihy.</span><span class="sxs-lookup"><span data-stu-id="84a2f-130">By default, if you don't indicate a calendar on the book, the book uses the ledger fiscal calendar.</span></span> <span data-ttu-id="84a2f-131">Pokud profil odpisů přidružený ke knize používá fiskální rok odpisů, je nutné vybrat fiskální kalendář pro knihu.</span><span class="sxs-lookup"><span data-stu-id="84a2f-131">You must select a fiscal calendar for a book when the depreciation profile that is associated with the book uses a fiscal depreciation year.</span></span> 

<span data-ttu-id="84a2f-132">Můžete vytvořit sdílené kalendáře pomocí stránky **Fiskální kalendáře** v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="84a2f-132">You can create shared calendars by using the **Fiscal calendars** page in General ledger.</span></span>

<span data-ttu-id="84a2f-133">Další informace naleznete v tématu [Odpisové metody a způsoby odpisu](depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="84a2f-133">For more information, see [Depreciation methods and conventions](depreciation-methods-conventions.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]