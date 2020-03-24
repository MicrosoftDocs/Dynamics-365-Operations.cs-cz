---
title: Použití relativní cesty v datových vazbách modelů a formátů elektronického výkaznictví
description: Nástroj elektronické výkaznictví umožňuje uživatelům definovat struktury elektronického formátu a pak popsat, jak by tyto struktury měly být vyplněny pomocí dat a algoritmů, které existují.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable , ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2940d99243ac52ee0d56a1c4423c4f0250f42f57
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091765"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a><span data-ttu-id="4b521-103">Použití relativní cesty v datových vazbách modelů a formátů elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="4b521-103">Use a relative path in data bindings of ER models and formats</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4b521-104">Nástroj elektronické výkaznictví umožňuje uživatelům definovat struktury elektronického formátu a pak popsat, jak by tyto struktury měly být vyplněny pomocí dat a algoritmů, které existují.</span><span class="sxs-lookup"><span data-stu-id="4b521-104">The Electronic reporting (ER) tool lets users define electronic format structures and then describe how those structures should be filled by using data and algorithms that exist in the application.</span></span> <span data-ttu-id="4b521-105">Další informace získáte v tématu [Vytvoření konfigurací elektronického výkaznictví](electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="4b521-105">For more information, see [Create Electronic reporting (ER) configurations](electronic-reporting-configuration.md).</span></span> <span data-ttu-id="4b521-106">Chcete-li určit datový tok pro načítání dat aplikace Finance and Operations a použít jej k vygenerování elektronického dokumentu, je nutné provést následující kroky:</span><span class="sxs-lookup"><span data-stu-id="4b521-106">To specify the data flow for retrieving Finance and Operations data and using it to generate  an electronic document, you need to do the following:</span></span>

- <span data-ttu-id="4b521-107">Navažte nakonfigurované zdroje dat na prvky navrženého datového modelu specifického pro určitou doménu.</span><span class="sxs-lookup"><span data-stu-id="4b521-107">Bind configured data sources to elements of the designed domain-specific data model.</span></span> <span data-ttu-id="4b521-108">Struktura modelu a vybrané zdroje dat mohou být součástí komplexní hierarchické struktury.</span><span class="sxs-lookup"><span data-stu-id="4b521-108">The model structure and selected data sources might be part of a complex hierarchical structure.</span></span> <span data-ttu-id="4b521-109">Z tohoto důvodu mohou být konečné vazby poměrně velké a obsahovat mnoho prvků různých typů (například vztahy, tabulky a metody).</span><span class="sxs-lookup"><span data-stu-id="4b521-109">Because of this, final bindings can be quite large and contain many elements of different types (for example, relations, tables, and methods,).</span></span> <span data-ttu-id="4b521-110">Vazby mohou být méně čitelné a poměrně složité pro kontrolu a pochopení, zejména pro nevlastníky.</span><span class="sxs-lookup"><span data-stu-id="4b521-110">The bindings can become less readable and quite complex to review and understand, especially for non-owners.</span></span> 
- <span data-ttu-id="4b521-111">Provažte prvky datového modelu s komponentami formátu pro definování toho, jaká data budou naplněna z datového modelu do výstupu generovaného formátu.</span><span class="sxs-lookup"><span data-stu-id="4b521-111">Bind data model elements with format components to define what data will be populated from the data model to the generated format’s output.</span></span>

<span data-ttu-id="4b521-112">Pro zlepšení použitelnosti návrhářů mapování elektronického výkaznictví byla vydána funkce relativní cesty.</span><span class="sxs-lookup"><span data-stu-id="4b521-112">To improve usability of ER mapping designers, the relative path feature has been released.</span></span> <span data-ttu-id="4b521-113">Ve výchozím nastavení je možnost zobrazení relativní cesty zapnuta pro každou novou instanci aplikace, kde je povoleno rozhraní návrháře elektronického výkaznictví (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service).</span><span class="sxs-lookup"><span data-stu-id="4b521-113">By default, the relative path representation option is turned on for any new instance of the application where ER design experience is enabled (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service).</span></span> <span data-ttu-id="4b521-114">Implementovali jsme parametr relativní cesty, aby uživatelé mohli používat úplnou cestu při práci s touto prezentací vazeb elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="4b521-114">We implemented the relative path parameter so that users can keep using the full path when work with this presentation of ER bindings.</span></span>

<span data-ttu-id="4b521-115">[![Parametry uživatele](./media/relative-path-01.png)](./media/relative-path-01.png)</span><span class="sxs-lookup"><span data-stu-id="4b521-115">[![User parameters](./media/relative-path-01.png)](./media/relative-path-01.png)</span></span>

 
<span data-ttu-id="4b521-116">Je-li zapnut parametr použití relativní cesty, nahradí jeden znak @ cestu k nadřazené položce ve vazbě aktuálního prvku modelu.</span><span class="sxs-lookup"><span data-stu-id="4b521-116">When the relative path usage parameter is turned on, a single @ character replaces the path to the parent item in the binding of the current model element.</span></span> <span data-ttu-id="4b521-117">Celá cesta vazby se stane kratší, takže celé mapování bude přehlednější a bude snazší pochopit.</span><span class="sxs-lookup"><span data-stu-id="4b521-117">The entire binding path becomes shorter, which makes the entire mapping more obvious and easier to understand.</span></span> <span data-ttu-id="4b521-118">Ve většině případů se v návrháři elektronického výkaznictví nevyžaduje žádné další posouvání, aby se zobrazily všechny vazby datového modelu.</span><span class="sxs-lookup"><span data-stu-id="4b521-118">In most cases, no additional scrolling is required in the ER designer to view all the bindings of the data model.</span></span>

<span data-ttu-id="4b521-119">[![Návrhář mapování modelu](./media/relative-path-02.png)](./media/relative-path-02.png)</span><span class="sxs-lookup"><span data-stu-id="4b521-119">[![Model mapping designer](./media/relative-path-02.png)](./media/relative-path-02.png)</span></span>
 
<span data-ttu-id="4b521-120">Když začnete navrhovat nový výraz elektronického výkaznictví, je třeba zadat pouze jeden znak, který definuje vazbu k poli nadřazené položky.</span><span class="sxs-lookup"><span data-stu-id="4b521-120">When you start designing a new ER expression, you need to enter only one character to define a binding to a field of the parent item.</span></span>

<span data-ttu-id="4b521-121">[![Návrhář receptur](./media/relative-path-03.png)](./media/relative-path-03.png)</span><span class="sxs-lookup"><span data-stu-id="4b521-121">[![Formula designer](./media/relative-path-03.png)](./media/relative-path-03.png)</span></span>
 
<span data-ttu-id="4b521-122">Pokud se rozhodnete změnit zdroj dat nadřazené položky modelu s použitím absolutní cesty, je nutné ručně znovu svázat tuto položku modelu a všechny vnořené položky s novým zdrojem dat.</span><span class="sxs-lookup"><span data-stu-id="4b521-122">When you decide to change the data source of the parent model item, with absolute path usage, you have to manually rebind this model item, as well as all nested items, to a new data source.</span></span> <span data-ttu-id="4b521-123">Je-li povoleno použití relativní cesty a vyberete nový zdroj dat, který má být svázán s nadřazenou položkou, bude vám nabídnuta možnost automatického obnovení vazby všech vnořených prvků této nadřazené položky jediným kliknutím.</span><span class="sxs-lookup"><span data-stu-id="4b521-123">When relative path usage is turned on, and you select a new data source to be bound to a parent item, you are offered an option to automatically rebind all nested elements of this parent item with one click.</span></span>

<span data-ttu-id="4b521-124">[![Nahrazení existující zprávy cesty](./media/relative-path-04.png)](./media/relative-path-04.png)</span><span class="sxs-lookup"><span data-stu-id="4b521-124">[![Replace existing path message](./media/relative-path-04.png)](./media/relative-path-04.png)</span></span>
 
<span data-ttu-id="4b521-125">Pokud potvrdíte opětovnou vazbu vnořených položek, nová nadřazená položka bude umístěna do cesty jednotlivých vnořených položek, které obsahují existující nadřazenou položku.</span><span class="sxs-lookup"><span data-stu-id="4b521-125">If you confirm rebinding of nested items, the new parent item will be placed to the path of each nested item containing the existing parent item.</span></span>
<span data-ttu-id="4b521-126">Tato funkce neruší zpětnou kompatibilitu architektury elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="4b521-126">This feature does not break the backward compatibility of the ER framework.</span></span> <span data-ttu-id="4b521-127">Všechny dříve navržené konfigurace elektronického výkaznictví budou fungovat s touto novou funkcí a nebudou požadovány žádné upgrady ani konverze.</span><span class="sxs-lookup"><span data-stu-id="4b521-127">All previously designed ER configurations will work with this new feature, and no upgrades or conversions are required.</span></span>

> [!NOTE]
> <span data-ttu-id="4b521-128">Všechny změny, které jsou zavedeny hromadnou změnou vazeb vnořených prvků v mapování modelu, jsou správně uloženy v rozdílu konfigurace (sledování změn).</span><span class="sxs-lookup"><span data-stu-id="4b521-128">All changes that are introduced by mass modification of bindings of nested elements in model mappings are correctly saved in a configuration delta (trace of changes).</span></span> <span data-ttu-id="4b521-129">To umožňuje zákazníkům znovu založit odvozenou verzi mapování modelů na libovolnou novou základní verzi, která byla upravena pomocí této nové funkce.</span><span class="sxs-lookup"><span data-stu-id="4b521-129">This allows customers to rebase their derived version of model mappings to any new base version of it that has been modified by using this new feature.</span></span>
