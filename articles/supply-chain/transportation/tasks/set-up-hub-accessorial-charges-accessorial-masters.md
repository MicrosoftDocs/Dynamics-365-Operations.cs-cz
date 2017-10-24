--- 
title: "Nastavení nákladů na dodatečnou službu centra a hlavních dodatečných služeb"
description: "Tento postup popisuje vytvoření hlavní dodatečnou služby pro centrum a použití této hlavní položky k vytvoření poplatků za dodatečnou službu centra."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6381416640ffacf0a9d96d7da96bc33612ca7137
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="7fd2b-103">Nastavení nákladů na dodatečnou službu centra a hlavních dodatečných služeb</span><span class="sxs-lookup"><span data-stu-id="7fd2b-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7fd2b-104">Tento postup popisuje vytvoření hlavní dodatečnou služby pro centrum a použití této hlavní položky k vytvoření poplatků za dodatečnou službu centra.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="7fd2b-105">Procedura používá soubor dat USMF.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="7fd2b-106">Toto nastavení obvykle provádí koordinátor přepravy.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="7fd2b-107">Nastavení hlavního centra</span><span class="sxs-lookup"><span data-stu-id="7fd2b-107">Set up a hub master</span></span>
1. <span data-ttu-id="7fd2b-108">Přejděte do nabídky Správa přepravy > Nastavení > Ohodnocení > Hlavní dodatečné služby.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="7fd2b-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-109">Click New.</span></span>
3. <span data-ttu-id="7fd2b-110">Zadejte hodnotu do pole Hlavní dodatečná služba.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="7fd2b-111">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="7fd2b-112">Vyberte možnost Centrum v poli Typ dodatečné služby.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="7fd2b-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-113">Click Save.</span></span>
7. <span data-ttu-id="7fd2b-114">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="7fd2b-115">Nastavení poplatků za dodatečnou službu centra</span><span class="sxs-lookup"><span data-stu-id="7fd2b-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="7fd2b-116">Přejděte do nabídky Správa přepravy > Nastavení > Ohodnocení > Poplatky za dodatečnou službu centra.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="7fd2b-117">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-117">Click New.</span></span>
3. <span data-ttu-id="7fd2b-118">Zadejte hodnotu do pole ID dodatečné služby centra.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="7fd2b-119">V poli Centrum kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="7fd2b-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="7fd2b-121">Vyberte možnost v poli Pozice centra.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="7fd2b-122">Můžete vytvořit náklady za vyzvednutí nebo za předání.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="7fd2b-123">V závislosti na výběru se náklady použijí na odpovídající segment přepravy na trase.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="7fd2b-124">V poli Hlavní dodatečná služba kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="7fd2b-125">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7fd2b-126">Vyberte hlavní položku, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="7fd2b-127">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-127">Click Save.</span></span>
10. <span data-ttu-id="7fd2b-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7fd2b-128">Close the page.</span></span>


