---
title: Převedení dlouhodobého majetku
description: Tento průvodce záznamem úloh převede finanční informace pro knihu dlouhodobého majetku z jedné sady finančních dimenzí do nové sady finančních dimenzí.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eb38483d3ac61acb4513e87d8c36ddd0f8863a10
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441169"
---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="5fba3-103">Převedení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="5fba3-103">Transfer a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5fba3-104">Tento průvodce záznamem úloh převede finanční informace pro knihu dlouhodobého majetku z jedné sady finančních dimenzí do nové sady finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="5fba3-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="5fba3-105">Využívá účetní role a ukázková data pro právnické osoby USMF.</span><span class="sxs-lookup"><span data-stu-id="5fba3-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="5fba3-106">V navigačním podokně přejděte na **Moduly > Dlouhodobý majetek > Dlouhodobý majetek > Dlouhodobý majetek**.</span><span class="sxs-lookup"><span data-stu-id="5fba3-106">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="5fba3-107">V seznamu najděte a vyberte dlouhodobý majetek, který chcete přenést.</span><span class="sxs-lookup"><span data-stu-id="5fba3-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="5fba3-108">V podokně akcí klikněte na možnost **Dlouhodobý majetek**.</span><span class="sxs-lookup"><span data-stu-id="5fba3-108">On the Action Pane, click **Fixed asset**.</span></span>
4. <span data-ttu-id="5fba3-109">Klikněte na **Převést dlouhodobý majetek**.</span><span class="sxs-lookup"><span data-stu-id="5fba3-109">Click **Transfer fixed assets**.</span></span>
5. <span data-ttu-id="5fba3-110">Do pole **Datum převodu** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="5fba3-110">In the **Transfer date** field, enter a date.</span></span>
6. <span data-ttu-id="5fba3-111">Zadejte komentáře popisující převod.</span><span class="sxs-lookup"><span data-stu-id="5fba3-111">Enter comments to describe the transfer.</span></span>
    
    <span data-ttu-id="5fba3-112">Tento seznam zobrazuje všechny knihy pro dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="5fba3-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="5fba3-113">Označte knihy, které chcete převést do nové sady finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="5fba3-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="5fba3-114">Tento seznam zobrazuje hodnoty aktuální finanční dimenze pro vybranou knihu.</span><span class="sxs-lookup"><span data-stu-id="5fba3-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="5fba3-115">Zvolte finanční dimenzi, kterou chcete aktualizovat pro vybranou knihu dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="5fba3-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="5fba3-116">V poli **Finanční dimenze** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5fba3-116">In the **Financial dimension** field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="5fba3-117">Podle potřeby nastavte jiné hodnoty finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="5fba3-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="5fba3-118">Veškeré hodnoty finanční dimenze se změní, jakmile dojde k převodu, a to podle toho, zda byla zadána hodnota nebo ponechána prázdná.</span><span class="sxs-lookup"><span data-stu-id="5fba3-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="5fba3-119">Například pokud je zadána hodnota pro organizační jednotku a hodnota pro finanční dimenze nákladového centra a oddělení ponechána prázdná.</span><span class="sxs-lookup"><span data-stu-id="5fba3-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="5fba3-120">Pokud vaše účetní struktura umožňuje prázdné hodnoty pro nákladové centrum a oddělení, převod způsobí, že každý oceňovací model bude mít novou hodnotu pro obchodní jednotku a prázdnou hodnotu nákladové centrum a oddělení.</span><span class="sxs-lookup"><span data-stu-id="5fba3-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="5fba3-121">Klikněte na položku **Aktualizovat**.</span><span class="sxs-lookup"><span data-stu-id="5fba3-121">Click **Update**.</span></span>
    * <span data-ttu-id="5fba3-122">Budete moci vytvořit náhled změn před uzavřením převodu.</span><span class="sxs-lookup"><span data-stu-id="5fba3-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="5fba3-123">Zkontrolujte výsledky před přenesením knih dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="5fba3-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="5fba3-124">Klikněte na položku **Převod**.</span><span class="sxs-lookup"><span data-stu-id="5fba3-124">Click **Transfer**.</span></span>

