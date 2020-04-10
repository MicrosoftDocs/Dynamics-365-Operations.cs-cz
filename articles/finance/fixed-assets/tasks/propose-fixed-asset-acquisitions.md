---
title: Nabídka pořízení dlouhodobého majetku
description: Toto téma popisuje získání dlouhodobého majetku pomocí návrhu pořízení v deníku dlouhodobého majetku.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
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
ms.openlocfilehash: e08177aad2db2438c2d5d4ddd294c1056b88167c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142724"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="e621b-103">Nabídka pořízení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="e621b-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e621b-104">Toto téma popisuje získání dlouhodobého majetku pomocí návrhu pořízení v deníku dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="e621b-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="e621b-105">Využívá účetní role a ukázková data pro právnické osoby USMF.</span><span class="sxs-lookup"><span data-stu-id="e621b-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="e621b-106">V navigačním podokně přejděte na **Moduly > Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="e621b-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="e621b-107">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="e621b-107">Select **New**.</span></span>
3. <span data-ttu-id="e621b-108">V poli **Název** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e621b-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="e621b-109">V podokně akcí zvolte **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="e621b-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="e621b-110">Vyberte **Návrhy**.</span><span class="sxs-lookup"><span data-stu-id="e621b-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="e621b-111">Vyberte **Návrh pořízení**.</span><span class="sxs-lookup"><span data-stu-id="e621b-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="e621b-112">Vyberte **Filtr**.</span><span class="sxs-lookup"><span data-stu-id="e621b-112">Select **Filter**.</span></span> <span data-ttu-id="e621b-113">Kliknutím na tlačítko **Vynulovat** vymažte předchozí hodnoty.</span><span class="sxs-lookup"><span data-stu-id="e621b-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="e621b-114">Vyberte řádek **Číslo dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="e621b-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="e621b-115">V poli **Kritéria** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e621b-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="e621b-116">Nastavte zbývající kritéria pro dlouhodobý majetek, který chcete získat s tímto návrhem.</span><span class="sxs-lookup"><span data-stu-id="e621b-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="e621b-117">Chcete-li ukončit podokno, klepněte dvakrát na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="e621b-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="e621b-118">Ověřte, že byly vytvořeny řádky transakce.</span><span class="sxs-lookup"><span data-stu-id="e621b-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="e621b-119">V návrhu pořízení bude zahrnut pouze dlouhodobý majetek s datem pořízení a pořizovací cenou nastavenou v knize.</span><span class="sxs-lookup"><span data-stu-id="e621b-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="e621b-120">Na stránce vyberte kartu **Knihy**.</span><span class="sxs-lookup"><span data-stu-id="e621b-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="e621b-121">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="e621b-121">Select **Post**.</span></span>

