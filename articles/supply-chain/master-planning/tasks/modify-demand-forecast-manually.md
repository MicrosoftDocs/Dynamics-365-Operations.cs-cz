---
title: Ruční úprava prognózy poptávky
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
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889017"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="f4113-103">Ruční úprava prognózy poptávky</span><span class="sxs-lookup"><span data-stu-id="f4113-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f4113-104">Tento postup popisuje postup úpravy prognózy pro položku.</span><span class="sxs-lookup"><span data-stu-id="f4113-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="f4113-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="f4113-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f4113-106">Tento postup je určen pro plánujícího produkce.</span><span class="sxs-lookup"><span data-stu-id="f4113-106">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="f4113-107">Upravení prognózy pro vybranou položku</span><span class="sxs-lookup"><span data-stu-id="f4113-107">Modify the forecast for a selected item</span></span>

<span data-ttu-id="f4113-108">Upravení prognózy pro vybranou položku:</span><span class="sxs-lookup"><span data-stu-id="f4113-108">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="f4113-109">Přejděte na **Moduly \> Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="f4113-109">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="f4113-110">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="f4113-110">In the list, find and select the desired record.</span></span> <span data-ttu-id="f4113-111">Vyberte položku, u které chcete změnit typ prognózu.</span><span class="sxs-lookup"><span data-stu-id="f4113-111">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="f4113-112">V podokně akcí otevřete kartu **Plán** a vyberte **Prognóza poptávky**.</span><span class="sxs-lookup"><span data-stu-id="f4113-112">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="f4113-113">V seznamu vyberte řádek.</span><span class="sxs-lookup"><span data-stu-id="f4113-113">In the list, select a row.</span></span> <span data-ttu-id="f4113-114">Pokud neexistují žádné řádky prognózy, vytvořte nový řádek výběrem možnosti **Nový** v podokně Akce.</span><span class="sxs-lookup"><span data-stu-id="f4113-114">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="f4113-115">Do pole **Prodejní množství** zadejte kladné číslo.</span><span class="sxs-lookup"><span data-stu-id="f4113-115">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="f4113-116">Toto číslo představuje předpovídané množství položky.</span><span class="sxs-lookup"><span data-stu-id="f4113-116">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="f4113-117">Pokud zadáte záporné číslo, zobrazí se chyba.</span><span class="sxs-lookup"><span data-stu-id="f4113-117">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="f4113-118">Podle potřeby vyplňte ostatní pole.</span><span class="sxs-lookup"><span data-stu-id="f4113-118">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="f4113-119">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f4113-119">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a><span data-ttu-id="f4113-120">Úprava prognózy pro jednu nebo více položek Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="f4113-120">Modify the forecast for one or more items Microsoft Excel</span></span>

<span data-ttu-id="f4113-121">Úprava prognózy pro jednu nebo více položek Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="f4113-121">To modify the forecast for one or more items Microsoft Excel:</span></span>

1. <span data-ttu-id="f4113-122">Proveďte některou z následujících akcí:</span><span class="sxs-lookup"><span data-stu-id="f4113-122">Do one of the following:</span></span>
    - <span data-ttu-id="f4113-123">Otevřete stránku **Prognóza poptávky** pro libovolnou položku (nezáleží na tom kterou), jak je popsáno v předchozí části.</span><span class="sxs-lookup"><span data-stu-id="f4113-123">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="f4113-124">Přejděte na **Hlavní plánování \> Prognózování \> Ruční zadání prognózy \> Řádky prognózy poptávky**.</span><span class="sxs-lookup"><span data-stu-id="f4113-124">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="f4113-125">V podokně akcí vyberte **Otevřít v Microsoft Office \> Záznamy prognózy poptávky**.</span><span class="sxs-lookup"><span data-stu-id="f4113-125">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="f4113-126">Vyberte umístění pro stažení, uložte a poté otevřete stažený soubor v aplikaci Excel.</span><span class="sxs-lookup"><span data-stu-id="f4113-126">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="f4113-127">Pokud se zobrazí varování, zvolte možnost **Povolit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="f4113-127">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="f4113-128">V aplikaci Excel se přihlaste do Supply Chain Management pomocí podokna úloh Microsoft Dynamics.</span><span class="sxs-lookup"><span data-stu-id="f4113-128">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="f4113-129">Musíte se přihlásit s aktivní možností **Zachovat přihlášení** a aplikaci pro datové připojení musíte důvěřovat.</span><span class="sxs-lookup"><span data-stu-id="f4113-129">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="f4113-130">Tabulka Excel nyní zobrazuje všechny aktuální řádky prognózy poptávky pro vaši společnost.</span><span class="sxs-lookup"><span data-stu-id="f4113-130">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="f4113-131">Podle potřeby řádky prognózy poptávky můžete přidávat, odstraňovat a upravovat.</span><span class="sxs-lookup"><span data-stu-id="f4113-131">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="f4113-132">Vyberte **Publikovat** v podokně úloh Microsoft Dynamics a nahrajte své změny zpět do Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f4113-132">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
