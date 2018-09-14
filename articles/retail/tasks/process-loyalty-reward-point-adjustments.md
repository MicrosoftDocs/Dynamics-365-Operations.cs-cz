--- 
title: " Zpracování úprav bodů věrnostních odměn"
description: "Tato procedura demonstruje vyhledávání informace o věrnostní kartě a úpravu bodů věrnostních odměn."
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailLoyaltyCards, RetailLoyaltyCardRewardPointTrans, RetailLoyaltyCardRewardPointAdjustment, RetailAffiliationLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 85aaa82bf56d55c69f39bab49682c79f51247251
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="process-loyalty-reward-point-adjustments"></a><span data-ttu-id="b0af5-103"> Zpracování úprav bodů věrnostních odměn</span><span class="sxs-lookup"><span data-stu-id="b0af5-103">Process loyalty reward point adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b0af5-104">Tato procedura demonstruje vyhledávání informace o věrnostní kartě a úpravu bodů věrnostních odměn.</span><span class="sxs-lookup"><span data-stu-id="b0af5-104">This procedure demonstrates how to look up loyalty card information and adjust loyalty reward points.</span></span> <span data-ttu-id="b0af5-105">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="b0af5-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="b0af5-106">Tato úloha je určena pro roli Manažer maloobchodních operací nebo roli Manažer odběratelského servisu.</span><span class="sxs-lookup"><span data-stu-id="b0af5-106">This task is intended for the Retail operations manager role or a Customer service manager role.</span></span>

1. <span data-ttu-id="b0af5-107">Přejděte na možnost Věrnostní karty.</span><span class="sxs-lookup"><span data-stu-id="b0af5-107">Go to Loyalty cards.</span></span>
2. <span data-ttu-id="b0af5-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b0af5-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b0af5-109">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b0af5-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b0af5-110">Klikněte na Transakce karet.</span><span class="sxs-lookup"><span data-stu-id="b0af5-110">Click Card transactions.</span></span>
    * <span data-ttu-id="b0af5-111">Na této stránce můžete zobrazit všechny věrnostní transakce pro vybrané věrnostní karty.</span><span class="sxs-lookup"><span data-stu-id="b0af5-111">On this page you can view all loyalty transactions for the selected loyalty card.</span></span>  
5. <span data-ttu-id="b0af5-112">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b0af5-112">Close the page.</span></span>
6. <span data-ttu-id="b0af5-113">Klikněte na Úpravy karty.</span><span class="sxs-lookup"><span data-stu-id="b0af5-113">Click Card adjustments.</span></span>
7. <span data-ttu-id="b0af5-114">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b0af5-114">Click New.</span></span>
8. <span data-ttu-id="b0af5-115">V poli Bod odměny zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0af5-115">In the Reward point field, enter or select a value.</span></span>
9. <span data-ttu-id="b0af5-116">V poli Množství nebo částka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="b0af5-116">In the Amount or quantity field, enter a number.</span></span>
    * <span data-ttu-id="b0af5-117">Můžete přidat nebo odebrat body z věrnostní karty pomocí kladného nebo záporného množství.</span><span class="sxs-lookup"><span data-stu-id="b0af5-117">You can add or remove points from the loyalty card by using positive or negative amounts.</span></span>  
10. <span data-ttu-id="b0af5-118">V poli Věrnostní program zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0af5-118">In the Loyalty program field, enter or select a value.</span></span>
11. <span data-ttu-id="b0af5-119">Zadejte hodnotu do pole Komentář.</span><span class="sxs-lookup"><span data-stu-id="b0af5-119">In the Comment field, type a value.</span></span>
12. <span data-ttu-id="b0af5-120">Klikněte na možnost Zaúčtovat úpravu.</span><span class="sxs-lookup"><span data-stu-id="b0af5-120">Click Post adjustment.</span></span>
13. <span data-ttu-id="b0af5-121">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="b0af5-121">Click Yes.</span></span>
14. <span data-ttu-id="b0af5-122">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b0af5-122">Close the page.</span></span>
    * <span data-ttu-id="b0af5-123">Obvykle byste v tomto bodě obnovili stránku k zobrazení výsledku úpravy věrnostních bodů na kartě Souhrn bodů odměny. Pokud provádíte spuštění jako průvodce úkolem, neprovádějte nyní obnovení. V opačném případě bude průvodce úkolem zastaven.</span><span class="sxs-lookup"><span data-stu-id="b0af5-123">Normally at this point you'd refresh the page to see the result of the reward points adjustment in the Reward point summary tab. But if you are running this as a task guide, don't refresh now because if you do, the task guide will stop.</span></span>  
15. <span data-ttu-id="b0af5-124">Klikněte na Transakce karet.</span><span class="sxs-lookup"><span data-stu-id="b0af5-124">Click Card transactions.</span></span>
16. <span data-ttu-id="b0af5-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b0af5-125">Close the page.</span></span>


