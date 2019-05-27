---
title: Dimenze objektu nákladů
description: Když analyzujete náklady, používáte ke stanovení, kam jsou náklady převáděny, dimenze prvku nákladů. Dimenze objektu nákladů používáte k určení, kde byste měli přiřadit náklady. V tomto tématu jsou informace o dimenzích objektu nákladů.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 60a6575387a6ebe3b349a61368a7561d78dc69f3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565408"
---
# <a name="cost-object-dimensions"></a><span data-ttu-id="d355c-105">Dimenze objektu nákladů</span><span class="sxs-lookup"><span data-stu-id="d355c-105">Cost object dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d355c-106">Když analyzujete náklady, používáte ke stanovení, kam jsou náklady převáděny, dimenze prvku nákladů.</span><span class="sxs-lookup"><span data-stu-id="d355c-106">When you analyze costs, you use cost element dimensions to determine where costs flow to.</span></span> <span data-ttu-id="d355c-107">Dimenze objektu nákladů používáte k určení, kde byste měli přiřadit náklady.</span><span class="sxs-lookup"><span data-stu-id="d355c-107">You use cost object dimensions to determine where you should assign costs.</span></span> <span data-ttu-id="d355c-108">V tomto tématu jsou informace o dimenzích objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="d355c-108">This topic provides information about cost object dimensions.</span></span>

<span data-ttu-id="d355c-109">Objekt nákladů může být jakýkoliv typ objektu, který chcete odhadnout, přidělit k němu náklady nebo přímo změřit.</span><span class="sxs-lookup"><span data-stu-id="d355c-109">A cost object can be any type of object that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="d355c-110">Typické objekty nákladů zahrnují produkty, projekty, prostředky, oddělení, nákladová střediska a geografické oblasti.</span><span class="sxs-lookup"><span data-stu-id="d355c-110">Typical cost objects include products, projects, resources, departments, cost centers, and geographical regions.</span></span> <span data-ttu-id="d355c-111">Vedení používá objekty nákladů, aby mohlo kvantifikovat náklady a také provést analýzu ziskovosti.</span><span class="sxs-lookup"><span data-stu-id="d355c-111">Management uses cost objects to quantify costs and also to drive profitability analysis.</span></span>

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a><span data-ttu-id="d355c-112">Dimenze objektu nákladů a členy dimenze objektu nákladů</span><span class="sxs-lookup"><span data-stu-id="d355c-112">Cost object dimensions and cost object dimension members</span></span>
<span data-ttu-id="d355c-113">Objekty nákladů se označují jako *dimenze objektu nákladů*.</span><span class="sxs-lookup"><span data-stu-id="d355c-113">Cost objects are known as *cost object dimensions*.</span></span> <span data-ttu-id="d355c-114">Až se rozhodnete, které k jaké osobě by se měl objekt dimenze nákladů vztahovat, musíte zadat jednotlivé hodnoty dimenzí nebo je importovat do nákladového účetnictví z jiných zdrojových systémů.</span><span class="sxs-lookup"><span data-stu-id="d355c-114">After you’ve decided which entity the cost object dimension should refer to, you must specify the individual dimension values or import them into Cost accounting from other source systems.</span></span> <span data-ttu-id="d355c-115">tyto hodnoty jednotlivých dimenzí se nazývají *členy dimenze objektu nákladů*.</span><span class="sxs-lookup"><span data-stu-id="d355c-115">These individual dimension values are known as *cost object dimension members*.</span></span> <span data-ttu-id="d355c-116">Chcete například použít finanční dimenzi, které se říká nákladové středisko, jako dimenzi objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="d355c-116">For example, you want to use the financial dimension that is named Cost center as the cost object dimension.</span></span> <span data-ttu-id="d355c-117">Pokud chcete zobrazit, jak náklady míří do jednotlivých nákladových středisek, musíte importovat členy dimenze objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="d355c-117">To see how costs flow to the individual cost centers, you must import the cost object dimension members.</span></span> <span data-ttu-id="d355c-118">V tomto případě členy dimenze objektu náklady jsou skutečná nákladová střediska, jako například prodej, výroba, administrativa a geografická umístění.</span><span class="sxs-lookup"><span data-stu-id="d355c-118">In this case, the cost object dimension members are the actual cost centers, such as Sales, Production, Administration, and Geographic locations.</span></span> <span data-ttu-id="d355c-119">Následující obrázek znázorňuje příklad nákladového střediska jako dimenze objektu nákladů s jeho aktuálními nákladovými středisky jako členy dimenze objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="d355c-119">The following screenshot shows an example of Cost Centers as the cost object dimension with its actual cost centers as cost object dimension members.</span></span> 

<span data-ttu-id="d355c-120">[![Dimenze objektu nákladů](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="d355c-120">[![cost-object-dimensions](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span></span>

## <a name="import-cost-object-dimension-members-through-data-connectors"></a><span data-ttu-id="d355c-121">Import členů dimenze objektu nákladů pomocí datových konektorů</span><span class="sxs-lookup"><span data-stu-id="d355c-121">Import cost object dimension members through data connectors</span></span>
<span data-ttu-id="d355c-122">Ve snaze usnadnit import členů dimenze objektů nákladů používáte datové spojnicemi konektory, abyste mohli načíst hodnoty z osob, které mají být použity jako dimenze objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="d355c-122">To make the import of cost object dimension members easier, you use data connectors to retrieve the values from the entities that you want to use as cost object dimensions.</span></span> <span data-ttu-id="d355c-123">Můžete použít buď předem připravené datové konektory nebo vlastní datové konektory, které vytvoříte.</span><span class="sxs-lookup"><span data-stu-id="d355c-123">You can use either the pre-built data connectors or custom data connectors that you build.</span></span>



