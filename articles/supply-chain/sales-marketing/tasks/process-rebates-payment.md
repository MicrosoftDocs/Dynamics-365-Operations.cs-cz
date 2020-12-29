---
title: Zpracování rabatu pro platbu
description: Tento postup ukazuje převod schválených a zpracovaných rabatů odběratele na dobropisy.
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 981068d26d232b10efd8d7288daaf7358aee3728
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423938"
---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="e5ed0-103">Zpracování rabatu pro platbu</span><span class="sxs-lookup"><span data-stu-id="e5ed0-103">Process rebates for payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e5ed0-104">Tento postup ukazuje převod schválených a zpracovaných rabatů odběratele na dobropisy.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="e5ed0-105">Tohoto průvodce můžete použít s ukázkovou společností USMF.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="e5ed0-106">Předpokladem pro tohoto průvodce je existence jednoho nebo více nároků na rabat ve stavu Označit.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="e5ed0-107">Pokud používáte USMF, před použitím tohoto průvodce použijte průvodce „Generování a zpracování rabatů odběratele“.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-107">If you're using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="e5ed0-108">Převedení nároků na rabat na dobropis</span><span class="sxs-lookup"><span data-stu-id="e5ed0-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="e5ed0-109">Přejděte do nabídky Všichni odběratelé.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-109">Go to All customers.</span></span>
2. <span data-ttu-id="e5ed0-110">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e5ed0-111">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="e5ed0-112">V podokně akcí klikněte na možnost Kolekce.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="e5ed0-113">Klikněte na možnost Vyrovnat transakce.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="e5ed0-114">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-114">Click Functions.</span></span>
7. <span data-ttu-id="e5ed0-115">Klikněte na možnost Rabatový program.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-115">Click Rebate program.</span></span>
    * <span data-ttu-id="e5ed0-116">Stránka Rabat uvádí nároky na rabat, které jste zpracovali na pracovní ploše pro rabat odběratele a které jsou ve stavu Označit.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="e5ed0-117">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-117">Click Edit.</span></span>
    * <span data-ttu-id="e5ed0-118">Zaškrtněte políčka v poli Označit u nároků, které chcete zahrnout do dobropisu.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="e5ed0-119">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-119">Click Functions.</span></span>
10. <span data-ttu-id="e5ed0-120">Klikněte na možnost Vytvořit dobropis.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-120">Click Create credit note.</span></span>
    * <span data-ttu-id="e5ed0-121">Zobrazí se zpráva informující o tom, že byl zaúčtován deník (je to ten deník spotřeby pohledávek zadaný na stránce Parametry pohledávek).</span><span class="sxs-lookup"><span data-stu-id="e5ed0-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="e5ed0-122">To způsobí, že se skutečná částka závazku (Dal) přesune do zůstatku odběratele.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="e5ed0-123">To znamená, že na účtu odběratele bylo provedeno připsání a na účtu časového rozlišení rabatu bylo provedeno odepsání.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-123">This means that the customer's account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="e5ed0-124">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-124">Close the page.</span></span>
12. <span data-ttu-id="e5ed0-125">Klikněte na možnost Zrušit.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-125">Click Cancel.</span></span>
    * <span data-ttu-id="e5ed0-126">Aktualizuje stránku, aby se zobrazily aktualizace.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="e5ed0-127">V podokně akcí klikněte na možnost Kolekce.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="e5ed0-128">Klikněte na možnost Vyrovnat transakce.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="e5ed0-129">Všimněte si, že transakce pro zápornou částku představující celkovou částku rabatu bez referenčního čísla faktury byla přidána k zůstatku odběratele.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="e5ed0-130">Klikněte na možnost Zrušit.</span><span class="sxs-lookup"><span data-stu-id="e5ed0-130">Click Cancel.</span></span>

