---
title: EUR-00015 Vyhledání strany pomocí DIČ
description: Tato procedura ukazuje, jak dokončit vyhledávání strany pomocí ID registrace.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, DirPartTaxRegistrationSearch
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c586de249575def120a6ae04fdc409aadfa1083d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4984825"
---
# <a name="eur-00015-party-search-using-vat-id"></a><span data-ttu-id="3294f-103">EUR-00015 Vyhledání strany pomocí DIČ</span><span class="sxs-lookup"><span data-stu-id="3294f-103">EUR-00015 Party search using VAT ID</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3294f-104">Tato procedura ukazuje, jak dokončit vyhledávání strany pomocí ID registrace.</span><span class="sxs-lookup"><span data-stu-id="3294f-104">This procedure shows how to complete a party search using a registration ID.</span></span> <span data-ttu-id="3294f-105">Před provedením této procedury musíte nastavit DIČ a zadat libovolná DIČ pro dodavatele, zákazníky nebo právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="3294f-105">Before you can complete this procedure, you must set up VAT IDs and enter any VAT IDs for vendors, customers, or legal entities.</span></span>

<span data-ttu-id="3294f-106">Postup se vztahuje na všechny evropské země/oblasti.</span><span class="sxs-lookup"><span data-stu-id="3294f-106">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="3294f-107">Procedura byla vytvořena za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Německu.</span><span class="sxs-lookup"><span data-stu-id="3294f-107">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="3294f-108">Tato procedura je určena pro manažera závazků nebo manažera pohledávek.</span><span class="sxs-lookup"><span data-stu-id="3294f-108">This procedure is intended for an accounts payable manager or accounts receivable manager.</span></span> <span data-ttu-id="3294f-109">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="3294f-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="3294f-110">Přejděte do nabídky Správa organizace > Globální adresář > Globální adresář.</span><span class="sxs-lookup"><span data-stu-id="3294f-110">Go to Organization administration > Global address book > Global address book.</span></span>
2. <span data-ttu-id="3294f-111">Klikněte na Vyhledávání registračního ID.</span><span class="sxs-lookup"><span data-stu-id="3294f-111">Click Registration ID search.</span></span>
3. <span data-ttu-id="3294f-112">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="3294f-112">Click Add.</span></span>
4. <span data-ttu-id="3294f-113">V poli Typ registrace zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="3294f-113">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="3294f-114">Například pokud jste chtěli najít strany s ID registrace typu DIČ, vyberte DIČ.</span><span class="sxs-lookup"><span data-stu-id="3294f-114">For example, if you wanted to find parties with a registration ID of type VAT ID, select VAT ID.</span></span>  
5. <span data-ttu-id="3294f-115">V poli Země/oblast zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="3294f-115">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="3294f-116">Zadejte například DEU.</span><span class="sxs-lookup"><span data-stu-id="3294f-116">For example, enter DEU.</span></span>  
6. <span data-ttu-id="3294f-117">Zadejte hodnotu do pole Číslo registrace.</span><span class="sxs-lookup"><span data-stu-id="3294f-117">In the Registration number field, type a value.</span></span>
7. <span data-ttu-id="3294f-118">Klepněte na tlačítko Najít.</span><span class="sxs-lookup"><span data-stu-id="3294f-118">Click Find.</span></span>
    * <span data-ttu-id="3294f-119">Zobrazí se všechny strany s tímto ID registrace.</span><span class="sxs-lookup"><span data-stu-id="3294f-119">All parties with that registration ID will be displayed.</span></span>  

