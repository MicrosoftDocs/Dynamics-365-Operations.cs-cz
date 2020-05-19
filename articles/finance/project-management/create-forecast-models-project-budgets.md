---
title: Vytvořte prognózové modely pro rozpočty projektu
description: Toto téma popisuje, jak vytvořit předpovědní model pro zbývající rozpočty.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321772"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="f1729-103">Vytvořte prognózové modely pro rozpočty projektu</span><span class="sxs-lookup"><span data-stu-id="f1729-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1729-104">Toto téma popisuje, jak vytvořit předpovědní model pro zbývající rozpočty.</span><span class="sxs-lookup"><span data-stu-id="f1729-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="f1729-105">Projekt, který je předmětem kontroly rozpočtu, používá dva typy rozpočtů: původní a zbývající.</span><span class="sxs-lookup"><span data-stu-id="f1729-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="f1729-106">Při vytváření rozpočtu projektu je nutné zadat modely prognóz původního a zbývajícího rozpočtu, které byly vytvořeny na stránce **Modely prognózy**.</span><span class="sxs-lookup"><span data-stu-id="f1729-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="f1729-107">Rozpočty projektu založené na zadaných modelech jsou vytvořeny při potvrzení rozpočtu projektu.</span><span class="sxs-lookup"><span data-stu-id="f1729-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="f1729-108">Model prognózy, který se používá pro kontrolu rozpočtu, nemůže obsahovat dílčí model a nelze jej použít jako dílčí model.</span><span class="sxs-lookup"><span data-stu-id="f1729-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="f1729-109">Vyberte **Řízení a účetnictví projektu** > **Nastavení** > **Prognózy**  > **Modely prognózy**.</span><span class="sxs-lookup"><span data-stu-id="f1729-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="f1729-110">Vyberte **Nový** k vytvoření nového modelu prognózy. Poté zadejte identifikační číslo a název nového modelu.</span><span class="sxs-lookup"><span data-stu-id="f1729-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="f1729-111">Nastavte možnost **Zastaveno** na **Ano**, aby se zabránilo jakýmkoli změnám v liniích prognózy pro model prognózy.</span><span class="sxs-lookup"><span data-stu-id="f1729-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="f1729-112">Pokud mají řádky prognózy, s nimiž je spojen model, generovat prognózy cash flow v hlavní knize, nastavte **Zahrnout do prognóz Cash Flow** na **Ano.**</span><span class="sxs-lookup"><span data-stu-id="f1729-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="f1729-113">Chcete-li jako datum fakturace použít datum projektu, nastavte **Prognóza data fakturace** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="f1729-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="f1729-114">V poli **Typ rozpočtu** vyberte jednu z následujících typů modelu:</span><span class="sxs-lookup"><span data-stu-id="f1729-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="f1729-115">**Původní rozpočet**: Tento typ modelu slouží pro původní částky rozpočtu, které jsou potvrzeny, když je původní rozpočet vytvořen a schválen.</span><span class="sxs-lookup"><span data-stu-id="f1729-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="f1729-116">**Zbývající rozpočet**: Použijte tento typ modelu pro zbývající částky rozpočtu po dobu trvání projektu.</span><span class="sxs-lookup"><span data-stu-id="f1729-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="f1729-117">Zůstatky v tomto modelu prognózy jsou sníženy o skutečné transakce a sníženy nebo zvýšeny o revize rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="f1729-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="f1729-118">**Převést do dalšího období**: Tento typ modelu slouží pro převod částek rozpočtu do dalšího období.</span><span class="sxs-lookup"><span data-stu-id="f1729-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="f1729-119">Převod do dalšího období je volitelný proces, který lze spustit za účelem převedení nevyužitých částek rozpočtu z jednoho fiskálního roku do jiného.</span><span class="sxs-lookup"><span data-stu-id="f1729-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="f1729-120">Podle potřeby nastavte následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="f1729-120">Set the following options as required:</span></span>

   - <span data-ttu-id="f1729-121">Chcete-li jako datum fakturace použít datum projektu, nastavte **Prognóza data fakturace** na Ano.</span><span class="sxs-lookup"><span data-stu-id="f1729-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="f1729-122">Povolte **Prognóza s WIP** pro prognózu na základě probíhající práce (WIP) a poté vyberte typ WIP.</span><span class="sxs-lookup"><span data-stu-id="f1729-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="f1729-123">Můžete ponechat výchozí **Typ rozpočtu** jako **Žádný** nebo zadat nový typ.</span><span class="sxs-lookup"><span data-stu-id="f1729-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="f1729-124">Typ rozpočtu není možné po změně záznamu změnit.</span><span class="sxs-lookup"><span data-stu-id="f1729-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="f1729-125">Pokud změníte výchozí typ rozpočtu, nebudou žádné další možnosti k dispozici pro aktualizace a tento model prognóz nelze znovu použít.</span><span class="sxs-lookup"><span data-stu-id="f1729-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

