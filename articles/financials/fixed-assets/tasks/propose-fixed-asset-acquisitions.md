---
title: Nabídka pořízení dlouhodobého majetku
description: Tento postup popisuje získání dlouhodobého majetku pomocí návrhu pořízení v deníku dlouhodobého majetku.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1891206bb266b126eccfa789b8c8062c9bfa688b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570873"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="50a20-103">Nabídka pořízení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="50a20-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="50a20-104">Tento postup popisuje získání dlouhodobého majetku pomocí návrhu pořízení v deníku dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="50a20-104">This procedure shows how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="50a20-105">Využívá účetní role a ukázková data pro právnické osoby USMF.</span><span class="sxs-lookup"><span data-stu-id="50a20-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="50a20-106">Přejděte na Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="50a20-106">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="50a20-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="50a20-107">Click New.</span></span>
3. <span data-ttu-id="50a20-108">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50a20-108">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="50a20-109">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="50a20-109">Click Lines.</span></span>
5. <span data-ttu-id="50a20-110">Klepněte na tlačítko Návrhy.</span><span class="sxs-lookup"><span data-stu-id="50a20-110">Click Proposals.</span></span>
6. <span data-ttu-id="50a20-111">Klikněte na Návrh pořizovací ceny.</span><span class="sxs-lookup"><span data-stu-id="50a20-111">Click Acquisition proposal.</span></span>
7. <span data-ttu-id="50a20-112">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="50a20-112">Click Filter.</span></span>
8. <span data-ttu-id="50a20-113">Kliknutím na tlačítko Vynulovat vymažte předchozí hodnoty.</span><span class="sxs-lookup"><span data-stu-id="50a20-113">Click Reset to clear out previous values.</span></span>
9. <span data-ttu-id="50a20-114">Vyberte řádek Číslo dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="50a20-114">Select the Fixed asset number row.</span></span>
10. <span data-ttu-id="50a20-115">V poli Kritéria zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50a20-115">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="50a20-116">Nastavte zbývající kritéria pro dlouhodobý majetek, který chcete získat s tímto návrhem.</span><span class="sxs-lookup"><span data-stu-id="50a20-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
11. <span data-ttu-id="50a20-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="50a20-117">Click OK.</span></span>
12. <span data-ttu-id="50a20-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="50a20-118">Click OK.</span></span>
    * <span data-ttu-id="50a20-119">Ověřte, že byly vytvořeny řádky transakce.</span><span class="sxs-lookup"><span data-stu-id="50a20-119">Verify the transaction lines created.</span></span>  
    * <span data-ttu-id="50a20-120">V návrhu pořízení bude zahrnut pouze dlouhodobý majetek s datem pořízení a pořizovací cenou nastavenou v knize.</span><span class="sxs-lookup"><span data-stu-id="50a20-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
13. <span data-ttu-id="50a20-121">Klikněte na kartu Knihy.</span><span class="sxs-lookup"><span data-stu-id="50a20-121">Click the Books tab.</span></span>
14. <span data-ttu-id="50a20-122">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="50a20-122">Click Post.</span></span>

