---
title: Nastavení nákladů na dodatečnou službu centra a hlavních dodatečných služeb
description: Tento postup popisuje vytvoření hlavní dodatečnou služby pro centrum a použití této hlavní položky k vytvoření poplatků za dodatečnou službu centra.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad89afe0a21261c57311c439153b969d837748e4
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/29/2020
ms.locfileid: "4424274"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="f3971-103">Nastavení nákladů na dodatečnou službu centra a hlavních dodatečných služeb</span><span class="sxs-lookup"><span data-stu-id="f3971-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f3971-104">Tento postup popisuje vytvoření hlavní dodatečnou služby pro centrum a použití této hlavní položky k vytvoření poplatků za dodatečnou službu centra.</span><span class="sxs-lookup"><span data-stu-id="f3971-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="f3971-105">Procedura používá soubor dat USMF.</span><span class="sxs-lookup"><span data-stu-id="f3971-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="f3971-106">Toto nastavení obvykle provádí koordinátor přepravy.</span><span class="sxs-lookup"><span data-stu-id="f3971-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="f3971-107">Nastavení hlavního centra</span><span class="sxs-lookup"><span data-stu-id="f3971-107">Set up a hub master</span></span>
1. <span data-ttu-id="f3971-108">Přejděte do nabídky Správa přepravy > Nastavení > Ohodnocení > Hlavní dodatečné služby.</span><span class="sxs-lookup"><span data-stu-id="f3971-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="f3971-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="f3971-109">Click New.</span></span>
3. <span data-ttu-id="f3971-110">Zadejte hodnotu do pole Hlavní dodatečná služba.</span><span class="sxs-lookup"><span data-stu-id="f3971-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="f3971-111">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="f3971-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f3971-112">Vyberte možnost Centrum v poli Typ dodatečné služby.</span><span class="sxs-lookup"><span data-stu-id="f3971-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="f3971-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="f3971-113">Click Save.</span></span>
7. <span data-ttu-id="f3971-114">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="f3971-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="f3971-115">Nastavení poplatků za dodatečnou službu centra</span><span class="sxs-lookup"><span data-stu-id="f3971-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="f3971-116">Přejděte do nabídky Správa přepravy > Nastavení > Ohodnocení > Poplatky za dodatečnou službu centra.</span><span class="sxs-lookup"><span data-stu-id="f3971-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="f3971-117">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="f3971-117">Click New.</span></span>
3. <span data-ttu-id="f3971-118">Zadejte hodnotu do pole ID dodatečné služby centra.</span><span class="sxs-lookup"><span data-stu-id="f3971-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="f3971-119">V poli Centrum kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="f3971-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f3971-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="f3971-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="f3971-121">Vyberte možnost v poli Pozice centra.</span><span class="sxs-lookup"><span data-stu-id="f3971-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="f3971-122">Můžete vytvořit náklady za vyzvednutí nebo za předání.</span><span class="sxs-lookup"><span data-stu-id="f3971-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="f3971-123">V závislosti na výběru se náklady použijí na odpovídající segment přepravy na trase.</span><span class="sxs-lookup"><span data-stu-id="f3971-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="f3971-124">V poli Hlavní dodatečná služba kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="f3971-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="f3971-125">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="f3971-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f3971-126">Vyberte hlavní položku, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="f3971-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="f3971-127">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="f3971-127">Click Save.</span></span>
10. <span data-ttu-id="f3971-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="f3971-128">Close the page.</span></span>

