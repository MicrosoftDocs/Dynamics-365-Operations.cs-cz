---
title: Nastavení nákladů na dodatečnou službu centra a hlavních dodatečných služeb
description: Tento postup popisuje vytvoření hlavní dodatečnou služby pro centrum a použití této hlavní položky k vytvoření poplatků za dodatečnou službu centra.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9959c20f9a8fd07cbf0cfd76f7760b44d7b5cae1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "331890"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="9045c-103">Nastavení nákladů na dodatečnou službu centra a hlavních dodatečných služeb</span><span class="sxs-lookup"><span data-stu-id="9045c-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9045c-104">Tento postup popisuje vytvoření hlavní dodatečnou služby pro centrum a použití této hlavní položky k vytvoření poplatků za dodatečnou službu centra.</span><span class="sxs-lookup"><span data-stu-id="9045c-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="9045c-105">Procedura používá soubor dat USMF.</span><span class="sxs-lookup"><span data-stu-id="9045c-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="9045c-106">Toto nastavení obvykle provádí koordinátor přepravy.</span><span class="sxs-lookup"><span data-stu-id="9045c-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="9045c-107">Nastavení hlavního centra</span><span class="sxs-lookup"><span data-stu-id="9045c-107">Set up a hub master</span></span>
1. <span data-ttu-id="9045c-108">Přejděte do nabídky Správa přepravy > Nastavení > Ohodnocení > Hlavní dodatečné služby.</span><span class="sxs-lookup"><span data-stu-id="9045c-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="9045c-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="9045c-109">Click New.</span></span>
3. <span data-ttu-id="9045c-110">Zadejte hodnotu do pole Hlavní dodatečná služba.</span><span class="sxs-lookup"><span data-stu-id="9045c-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="9045c-111">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="9045c-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9045c-112">Vyberte možnost Centrum v poli Typ dodatečné služby.</span><span class="sxs-lookup"><span data-stu-id="9045c-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="9045c-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="9045c-113">Click Save.</span></span>
7. <span data-ttu-id="9045c-114">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9045c-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="9045c-115">Nastavení poplatků za dodatečnou službu centra</span><span class="sxs-lookup"><span data-stu-id="9045c-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="9045c-116">Přejděte do nabídky Správa přepravy > Nastavení > Ohodnocení > Poplatky za dodatečnou službu centra.</span><span class="sxs-lookup"><span data-stu-id="9045c-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="9045c-117">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="9045c-117">Click New.</span></span>
3. <span data-ttu-id="9045c-118">Zadejte hodnotu do pole ID dodatečné služby centra.</span><span class="sxs-lookup"><span data-stu-id="9045c-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="9045c-119">V poli Centrum kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="9045c-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="9045c-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="9045c-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="9045c-121">Vyberte možnost v poli Pozice centra.</span><span class="sxs-lookup"><span data-stu-id="9045c-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="9045c-122">Můžete vytvořit náklady za vyzvednutí nebo za předání.</span><span class="sxs-lookup"><span data-stu-id="9045c-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="9045c-123">V závislosti na výběru se náklady použijí na odpovídající segment přepravy na trase.</span><span class="sxs-lookup"><span data-stu-id="9045c-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="9045c-124">V poli Hlavní dodatečná služba kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="9045c-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="9045c-125">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9045c-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9045c-126">Vyberte hlavní položku, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="9045c-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="9045c-127">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="9045c-127">Click Save.</span></span>
10. <span data-ttu-id="9045c-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9045c-128">Close the page.</span></span>

