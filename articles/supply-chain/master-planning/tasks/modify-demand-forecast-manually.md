---
title: 'Průvodce: Ruční úprava prognózy poptávky'
description: Toto téma popisuje postup úpravy prognózy pro položku
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12ccf90b9971379e8931bd48d6243a855bb795
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224003"
---
# <a name="guide-modify-a-demand-forecast-manually"></a><span data-ttu-id="7cc92-103">Průvodce: Ruční úprava prognózy poptávky</span><span class="sxs-lookup"><span data-stu-id="7cc92-103">Guide: Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7cc92-104">Tento postup popisuje postup úpravy prognózy pro položku.</span><span class="sxs-lookup"><span data-stu-id="7cc92-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="7cc92-105">Tento postup je určen pro plánujícího produkce.</span><span class="sxs-lookup"><span data-stu-id="7cc92-105">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="7cc92-106">Upravení prognózy pro vybranou položku</span><span class="sxs-lookup"><span data-stu-id="7cc92-106">Modify the forecast for a selected item</span></span>

<span data-ttu-id="7cc92-107">Upravení prognózy pro vybranou položku:</span><span class="sxs-lookup"><span data-stu-id="7cc92-107">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="7cc92-108">Přejděte na **Moduly \> Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="7cc92-108">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="7cc92-109">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="7cc92-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="7cc92-110">Vyberte položku, u které chcete změnit typ prognózu.</span><span class="sxs-lookup"><span data-stu-id="7cc92-110">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="7cc92-111">V podokně akcí otevřete kartu **Plán** a vyberte **Prognóza poptávky**.</span><span class="sxs-lookup"><span data-stu-id="7cc92-111">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="7cc92-112">V seznamu vyberte řádek.</span><span class="sxs-lookup"><span data-stu-id="7cc92-112">In the list, select a row.</span></span> <span data-ttu-id="7cc92-113">Pokud neexistují žádné řádky prognózy, vytvořte nový řádek výběrem možnosti **Nový** v podokně Akce.</span><span class="sxs-lookup"><span data-stu-id="7cc92-113">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="7cc92-114">Do pole **Prodejní množství** zadejte kladné číslo.</span><span class="sxs-lookup"><span data-stu-id="7cc92-114">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="7cc92-115">Toto číslo představuje předpovídané množství položky.</span><span class="sxs-lookup"><span data-stu-id="7cc92-115">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="7cc92-116">Pokud zadáte záporné číslo, zobrazí se chyba.</span><span class="sxs-lookup"><span data-stu-id="7cc92-116">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="7cc92-117">Podle potřeby vyplňte ostatní pole.</span><span class="sxs-lookup"><span data-stu-id="7cc92-117">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="7cc92-118">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="7cc92-118">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a><span data-ttu-id="7cc92-119">Úprava prognózy pro jednu nebo více položek v aplikaci Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="7cc92-119">Modify the forecast for one or more items with Microsoft Excel</span></span>

<span data-ttu-id="7cc92-120">Postup úpravy prognózy pro jednu nebo více položek v aplikaci Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="7cc92-120">To modify the forecast for one or more items with Microsoft Excel:</span></span>

1. <span data-ttu-id="7cc92-121">Proveďte některou z následujících akcí:</span><span class="sxs-lookup"><span data-stu-id="7cc92-121">Do one of the following:</span></span>
    - <span data-ttu-id="7cc92-122">Otevřete stránku **Prognóza poptávky** pro libovolnou položku (nezáleží na tom kterou), jak je popsáno v předchozí části.</span><span class="sxs-lookup"><span data-stu-id="7cc92-122">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="7cc92-123">Přejděte na **Hlavní plánování \> Prognózování \> Ruční zadání prognózy \> Řádky prognózy poptávky**.</span><span class="sxs-lookup"><span data-stu-id="7cc92-123">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="7cc92-124">V podokně akcí vyberte **Otevřít v Microsoft Office \> Záznamy prognózy poptávky**.</span><span class="sxs-lookup"><span data-stu-id="7cc92-124">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="7cc92-125">Vyberte umístění pro stažení, uložte a poté otevřete stažený soubor v aplikaci Excel.</span><span class="sxs-lookup"><span data-stu-id="7cc92-125">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="7cc92-126">Pokud se zobrazí varování, zvolte možnost **Povolit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="7cc92-126">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="7cc92-127">V aplikaci Excel se přihlaste do Supply Chain Management pomocí podokna úloh Microsoft Dynamics.</span><span class="sxs-lookup"><span data-stu-id="7cc92-127">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="7cc92-128">Musíte se přihlásit s aktivní možností **Zachovat přihlášení** a aplikaci pro datové připojení musíte důvěřovat.</span><span class="sxs-lookup"><span data-stu-id="7cc92-128">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="7cc92-129">Tabulka Excel nyní zobrazuje všechny aktuální řádky prognózy poptávky pro vaši společnost.</span><span class="sxs-lookup"><span data-stu-id="7cc92-129">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="7cc92-130">Podle potřeby řádky prognózy poptávky můžete přidávat, odstraňovat a upravovat.</span><span class="sxs-lookup"><span data-stu-id="7cc92-130">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="7cc92-131">Vyberte **Publikovat** v podokně úloh Microsoft Dynamics a nahrajte své změny zpět do Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7cc92-131">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
