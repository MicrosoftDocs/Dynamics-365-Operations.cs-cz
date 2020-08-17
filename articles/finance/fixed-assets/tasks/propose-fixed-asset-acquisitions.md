---
title: Nabídka pořízení dlouhodobého majetku
description: Toto téma popisuje získání dlouhodobého majetku pomocí návrhu pořízení v deníku dlouhodobého majetku.
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0997af638c141661afb677e2407a90a883168aed
ms.sourcegitcommit: a8201e0b9033c2afc2b1702b0337facaf7ad4b92
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/28/2020
ms.locfileid: "3628878"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="dee73-103">Nabídka pořízení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="dee73-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dee73-104">Toto téma popisuje získání dlouhodobého majetku pomocí návrhu pořízení v deníku dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="dee73-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="dee73-105">Využívá účetní role a ukázková data pro právnické osoby USMF.</span><span class="sxs-lookup"><span data-stu-id="dee73-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="dee73-106">Chcete-li získat dlouhodobý majetek prostřednictvím deníku návrhu dlouhodobého majetku, musíte nejprve vytvořit záznam dlouhodobého majetku a poté definovat pořizovací cenu v majetkové knize.</span><span class="sxs-lookup"><span data-stu-id="dee73-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

1. <span data-ttu-id="dee73-107">V navigačním podokně přejděte na **Moduly > Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="dee73-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="dee73-108">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="dee73-108">Select **New**.</span></span>
3. <span data-ttu-id="dee73-109">V poli **Název** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dee73-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="dee73-110">V podokně akcí zvolte **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="dee73-110">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="dee73-111">Vyberte **Návrhy**.</span><span class="sxs-lookup"><span data-stu-id="dee73-111">Select **Proposals**.</span></span>
6. <span data-ttu-id="dee73-112">Vyberte **Návrh pořízení**.</span><span class="sxs-lookup"><span data-stu-id="dee73-112">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="dee73-113">Vyberte **Filtr**.</span><span class="sxs-lookup"><span data-stu-id="dee73-113">Select **Filter**.</span></span> <span data-ttu-id="dee73-114">Kliknutím na tlačítko **Vynulovat** vymažte předchozí hodnoty.</span><span class="sxs-lookup"><span data-stu-id="dee73-114">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="dee73-115">Vyberte řádek **Číslo dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="dee73-115">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="dee73-116">V poli **Kritéria** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dee73-116">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="dee73-117">Nastavte zbývající kritéria pro dlouhodobý majetek, který chcete získat s tímto návrhem.</span><span class="sxs-lookup"><span data-stu-id="dee73-117">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="dee73-118">Chcete-li ukončit podokno, klepněte dvakrát na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="dee73-118">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="dee73-119">Ověřte, že byly vytvořeny řádky transakce.</span><span class="sxs-lookup"><span data-stu-id="dee73-119">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="dee73-120">V návrhu pořízení bude zahrnut pouze dlouhodobý majetek s datem pořízení a pořizovací cenou nastavenou v knize.</span><span class="sxs-lookup"><span data-stu-id="dee73-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="dee73-121">Na stránce vyberte kartu **Knihy**.</span><span class="sxs-lookup"><span data-stu-id="dee73-121">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="dee73-122">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="dee73-122">Select **Post**.</span></span>
