---
title: Vytvoření a získání majetku z modulu Závazky
description: Tento průvodce úkolem vás provede vytvořením a pořízením dlouhodobého majetku s procesem nákupu.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2626877c907994d03cdae960c8501a858ca214bd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840018"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a><span data-ttu-id="c10b6-103">Vytvoření a získání majetku z modulu Závazky</span><span class="sxs-lookup"><span data-stu-id="c10b6-103">Create and acquire assets from Accounts payable</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c10b6-104">Tento průvodce úkolem vás provede vytvořením a pořízením dlouhodobého majetku s procesem nákupu.</span><span class="sxs-lookup"><span data-stu-id="c10b6-104">This task guide will walk through creation and acquisition of a fixed asset with the purchasing process.</span></span>  <span data-ttu-id="c10b6-105">Používá účetní a úředníky závazků a vzorovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="c10b6-105">It uses the Accountant and Accounts payable clerks and the demo company USMF .</span></span>


## <a name="set-fixed-assets-parameters"></a><span data-ttu-id="c10b6-106">Nastavení parametrů dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="c10b6-106">Set Fixed assets parameters</span></span>
1. <span data-ttu-id="c10b6-107">Přejděte na Dlouhodobý majetek > Nastavení > Parametry dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="c10b6-107">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="c10b6-108">Rozbalte nebo sbalte oddíl Nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="c10b6-108">Expand or collapse the Purchase orders section.</span></span>
3. <span data-ttu-id="c10b6-109">Označte pole Povolit pořízení majetku v části Nakupování.</span><span class="sxs-lookup"><span data-stu-id="c10b6-109">Check the Allow asset acquisition from Purchasing checkbox.</span></span>
4. <span data-ttu-id="c10b6-110">Označte pole Vytvořit majetek při zaúčtování příjemky produktu nebo faktury.</span><span class="sxs-lookup"><span data-stu-id="c10b6-110">Check the Create asset during product receipt or invoice posting checkbox.</span></span>

## <a name="create-a-new-vendor-invoice"></a><span data-ttu-id="c10b6-111">Vytvoření nové faktury dodavatele</span><span class="sxs-lookup"><span data-stu-id="c10b6-111">Create a new vendor invoice</span></span>
1. <span data-ttu-id="c10b6-112">Přejděte na Závazky > Pracovní prostory > Záznam faktury dodavatele.</span><span class="sxs-lookup"><span data-stu-id="c10b6-112">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="c10b6-113">Klikněte na Nová faktura dodavatele.</span><span class="sxs-lookup"><span data-stu-id="c10b6-113">Click New vendor invoice.</span></span>
3. <span data-ttu-id="c10b6-114">V poli Účet faktury kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="c10b6-114">In the Invoice account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c10b6-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="c10b6-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c10b6-116">Zadejte hodnotu do pole Číslo.</span><span class="sxs-lookup"><span data-stu-id="c10b6-116">In the Number field, type a value.</span></span>
6. <span data-ttu-id="c10b6-117">V poli Datum zaúčtování zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="c10b6-117">In the Posting date field, enter a date.</span></span>
7. <span data-ttu-id="c10b6-118">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="c10b6-118">Click Add line.</span></span>
8. <span data-ttu-id="c10b6-119">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="c10b6-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c10b6-120">Pro pořízení dlouhodobého majetku lze použít neskladované zboží nebo kategorie zásobování.</span><span class="sxs-lookup"><span data-stu-id="c10b6-120">Either non-stocked items or procurement categories can be used for fixed asset acquisition.</span></span>  
9. <span data-ttu-id="c10b6-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="c10b6-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="c10b6-122">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="c10b6-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="c10b6-123">Jeden řádek faktury vytvoří pouze jeden dlouhodobý majetek bez ohledu na množství.</span><span class="sxs-lookup"><span data-stu-id="c10b6-123">One invoice line will only create one fixed asset, regardless of quantity.</span></span>  <span data-ttu-id="c10b6-124">Hodnota pole Množství na faktuře se přesune do množství dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="c10b6-124">The invoice quantity field value will be transferred to the fixed asset quantity.</span></span>  
11. <span data-ttu-id="c10b6-125">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="c10b6-125">In the Unit price field, enter a number.</span></span>
12. <span data-ttu-id="c10b6-126">Rozbalte nebo sbalte oddíl Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="c10b6-126">Expand or collapse the Line details section.</span></span>
13. <span data-ttu-id="c10b6-127">Klikněte na kartu Dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="c10b6-127">Click the Fixed assets tab.</span></span>
14. <span data-ttu-id="c10b6-128">Označte pole Vytvořit nový dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="c10b6-128">Check the Create a new fixed asset checkbox.</span></span>
15. <span data-ttu-id="c10b6-129">V poli Skupina dlouhodobého majetku kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="c10b6-129">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="c10b6-130">V seznamu vyberte skupinu dlouhodobého majetku, kterou chcete použít pro vytvoření nového dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="c10b6-130">In the list, select the fixed asset group to be used when creating the new fixed asset.</span></span>
17. <span data-ttu-id="c10b6-131">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="c10b6-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="c10b6-132">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="c10b6-132">Click Post.</span></span>
    * <span data-ttu-id="c10b6-133">Dlouhodobý majetek se vytvoří a pořídí při zaúčtování faktury.</span><span class="sxs-lookup"><span data-stu-id="c10b6-133">The fixed asset will be created and acquired when the invoice is posted.</span></span>  

