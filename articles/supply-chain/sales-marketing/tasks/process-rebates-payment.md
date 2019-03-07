---
title: Zpracování rabatu pro platbu
description: Tento postup ukazuje převod schválených a zpracovaných rabatů odběratele na dobropisy.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2d97a59ae782af0a3d5ab71903961ef244a8e62
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "363308"
---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="1cd67-103">Zpracování rabatu pro platbu</span><span class="sxs-lookup"><span data-stu-id="1cd67-103">Process rebates for payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1cd67-104">Tento postup ukazuje převod schválených a zpracovaných rabatů odběratele na dobropisy.</span><span class="sxs-lookup"><span data-stu-id="1cd67-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="1cd67-105">Tohoto průvodce můžete použít s ukázkovou společností USMF.</span><span class="sxs-lookup"><span data-stu-id="1cd67-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="1cd67-106">Předpokladem pro tohoto průvodce je existence jednoho nebo více nároků na rabat ve stavu Označit.</span><span class="sxs-lookup"><span data-stu-id="1cd67-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="1cd67-107">Pokud používáte data USMF, před použitím tohoto průvodce použijte průvodce "Generování a zpracování rabatů odběratele".</span><span class="sxs-lookup"><span data-stu-id="1cd67-107">If you’re using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="1cd67-108">Převedení nároků na rabat na dobropis</span><span class="sxs-lookup"><span data-stu-id="1cd67-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="1cd67-109">Přejděte do nabídky Všichni odběratelé.</span><span class="sxs-lookup"><span data-stu-id="1cd67-109">Go to All customers.</span></span>
2. <span data-ttu-id="1cd67-110">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="1cd67-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1cd67-111">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1cd67-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1cd67-112">V podokně akcí klikněte na možnost Kolekce.</span><span class="sxs-lookup"><span data-stu-id="1cd67-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="1cd67-113">Klikněte na možnost Vyrovnat transakce.</span><span class="sxs-lookup"><span data-stu-id="1cd67-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="1cd67-114">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="1cd67-114">Click Functions.</span></span>
7. <span data-ttu-id="1cd67-115">Klikněte na možnost Rabatový program.</span><span class="sxs-lookup"><span data-stu-id="1cd67-115">Click Rebate program.</span></span>
    * <span data-ttu-id="1cd67-116">Stránka Rabat uvádí nároky na rabat, které jste zpracovali na pracovní ploše pro rabat odběratele a které jsou ve stavu Označit.</span><span class="sxs-lookup"><span data-stu-id="1cd67-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="1cd67-117">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="1cd67-117">Click Edit.</span></span>
    * <span data-ttu-id="1cd67-118">Zaškrtněte políčka v poli Označit u nároků, které chcete zahrnout do dobropisu.</span><span class="sxs-lookup"><span data-stu-id="1cd67-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="1cd67-119">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="1cd67-119">Click Functions.</span></span>
10. <span data-ttu-id="1cd67-120">Klikněte na možnost Vytvořit dobropis.</span><span class="sxs-lookup"><span data-stu-id="1cd67-120">Click Create credit note.</span></span>
    * <span data-ttu-id="1cd67-121">Zobrazí se zpráva informující o tom, že byl zaúčtován deník (je to ten deník spotřeby pohledávek zadaný na stránce Parametry pohledávek).</span><span class="sxs-lookup"><span data-stu-id="1cd67-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="1cd67-122">To způsobí, že se skutečná částka závazku (Dal) přesune do zůstatku odběratele.</span><span class="sxs-lookup"><span data-stu-id="1cd67-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="1cd67-123">To znamená, že na účtu odběratele bylo provedeno připsání a na účtu časového rozlišení rabatu bylo provedeno odepsání.</span><span class="sxs-lookup"><span data-stu-id="1cd67-123">This means that the customer’s account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="1cd67-124">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1cd67-124">Close the page.</span></span>
12. <span data-ttu-id="1cd67-125">Klikněte na možnost Zrušit.</span><span class="sxs-lookup"><span data-stu-id="1cd67-125">Click Cancel.</span></span>
    * <span data-ttu-id="1cd67-126">Aktualizuje stránku, aby se zobrazily aktualizace.</span><span class="sxs-lookup"><span data-stu-id="1cd67-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="1cd67-127">V podokně akcí klikněte na možnost Kolekce.</span><span class="sxs-lookup"><span data-stu-id="1cd67-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="1cd67-128">Klikněte na možnost Vyrovnat transakce.</span><span class="sxs-lookup"><span data-stu-id="1cd67-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="1cd67-129">Všimněte si, že transakce pro zápornou částku představující celkovou částku rabatu bez referenčního čísla faktury byla přidána k zůstatku odběratele.</span><span class="sxs-lookup"><span data-stu-id="1cd67-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="1cd67-130">Klikněte na možnost Zrušit.</span><span class="sxs-lookup"><span data-stu-id="1cd67-130">Click Cancel.</span></span>

