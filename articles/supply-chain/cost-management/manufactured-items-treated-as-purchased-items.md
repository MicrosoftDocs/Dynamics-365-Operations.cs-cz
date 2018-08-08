---
title: "Nastavení produktů, které mohou být vyrobeny nebo pořízeny"
description: "Produkty mohou být odebírány různými způsoby – mohou být produkovány (vyrobeny) nebo získané (nakupované). Tento článek popisuje některé typické body, které je třeba zvážit při konfiguraci produktů pro podporu více zdrojů."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: a910b5782c8f15cfdd4cf93ea883bc28a5ce8e1a
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---

# <a name="set-up-products-that-can-be-produced-or-procured"></a><span data-ttu-id="fd542-104">Nastavení produktů, které mohou být vyrobeny nebo pořízeny</span><span class="sxs-lookup"><span data-stu-id="fd542-104">Set up products that can be produced or procured</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd542-105">Produkty mohou být odebírány různými způsoby – mohou být produkovány (vyrobeny) nebo získané (nakupované).</span><span class="sxs-lookup"><span data-stu-id="fd542-105">Products can be sourced in various ways -  they can be produced (manufactured) or procured (purchased).</span></span> <span data-ttu-id="fd542-106">Tento článek popisuje některé typické body, které je třeba zvážit při konfiguraci produktů pro podporu více zdrojů.</span><span class="sxs-lookup"><span data-stu-id="fd542-106">This article describes some typical points to consider when you configure products to support multi-sourcing.</span></span> 

<span data-ttu-id="fd542-107">Získávání z více zdrojů se obvykle používá k zakoupení položky, která je příležitostně vyráběna, nebo v případě, že položka byla především vyráběna a byla změněna, takže je aktuálně převážně kupovaná.</span><span class="sxs-lookup"><span data-stu-id="fd542-107">Multi-sourcing is typically used for a purchased item that is occasionally manufactured, or when an item that was primarily a manufactured item is changed so that it's now primarily a purchased item.</span></span> <span data-ttu-id="fd542-108">Daná položka je nejprve označena jako vyráběná položka s cílem definování údajů kusovníku a údajů o postupu nebo s cílem podpory výrobních zakázek pro danou položku.</span><span class="sxs-lookup"><span data-stu-id="fd542-108">The item is first designated as a manufactured item, so that bill of materials (BOM) and route information can be defined, and to support production orders for the item.</span></span> <span data-ttu-id="fd542-109">Typ výroby je třeba nastavit na **Kusovník** (nebo pro výrobní proces **Vzorec** nebo **Souběžný produkt**).</span><span class="sxs-lookup"><span data-stu-id="fd542-109">The production type should be set to **BOM** (or, for process manufacturing, **Formula** or **Co-Product**).</span></span>

<span data-ttu-id="fd542-110">Při použití standardních nákladů lze pro vyráběnou položku vypočítat záznam o nákladech položky.</span><span class="sxs-lookup"><span data-stu-id="fd542-110">When you use standard cost, the item cost record can be calculated for the manufactured item.</span></span> <span data-ttu-id="fd542-111">Záznam o nákladech na položku však nemusí odpovídat standardním nákladům, které požadujete pro účely nákupu.</span><span class="sxs-lookup"><span data-stu-id="fd542-111">However, the item cost record might not match the standard cost that you want for purchasing purposes.</span></span> <span data-ttu-id="fd542-112">V tomto případě je nutno standardní náklady ručně zadat a aktivovat pro záznam o nákladech na položku.</span><span class="sxs-lookup"><span data-stu-id="fd542-112">In this case, the standard cost must be manually entered and activated for the item cost record.</span></span> <span data-ttu-id="fd542-113">Pro výpočet nákladů zvažte použití zvláštního kusovníku a postupu, který představuje kombinaci zásobování produktu v průběhu fiskálního období za účelem minimalizace odchylek během určité doby.</span><span class="sxs-lookup"><span data-stu-id="fd542-113">For the cost calculation, consider using a special BOM and route that represent the supply mix of the product over the course of a fiscal period, to minimize the variances over time.</span></span> <span data-ttu-id="fd542-114">Položku vyráběnou na jednom pracovišti lze také převést na jiné pracoviště.</span><span class="sxs-lookup"><span data-stu-id="fd542-114">Additionally, a manufactured item at one site can be transferred to another site.</span></span> <span data-ttu-id="fd542-115">Z toho vyplývá, že náklady na položku je nutné ručně zadat a aktivovat pro pracoviště, na které položka převádí.</span><span class="sxs-lookup"><span data-stu-id="fd542-115">Therefore, the item's cost must be manually entered and activated for the site that the item is transferred to.</span></span> <span data-ttu-id="fd542-116">Pokud vyráběnou položku použijete jako komponentu pro výrobky vyšší úrovně, je třeba s náklady na tuto komponentu pracovat jako se zakoupenou položkou.</span><span class="sxs-lookup"><span data-stu-id="fd542-116">When you use the manufactured item as a component in higher-level products, the component's costs should be treated as a purchased item.</span></span> <span data-ttu-id="fd542-117">Tato směrnice platí bez ohledu na to, zda náklady komponenty byly vypočteny nebo ručně zadány.</span><span class="sxs-lookup"><span data-stu-id="fd542-117">This guideline applies, regardless of whether the component’s costs were calculated or manually entered.</span></span> <span data-ttu-id="fd542-118">To znamená, že výpočet kusovníku musí pracovat s náklady na položku jako se zakoupenou komponentou namísto použití údajů o kusovníku a postupu položky k výpočtu nákladů.</span><span class="sxs-lookup"><span data-stu-id="fd542-118">In other words, a BOM calculation should treat the item's costs as a purchased component instead of using the item's BOM and route information to calculate costs.</span></span> 

<span data-ttu-id="fd542-119">Výpočtu lze předejít výběrem příznaku **Zastavit rozpad**, který je vložen do skupiny výpočtu kusovníku přiřazené k dané položce.</span><span class="sxs-lookup"><span data-stu-id="fd542-119">To prevent the calculation from occurring, select the **Stop explosion** flag that is embedded in the BOM calculation group that is assigned to the item.</span></span> <span data-ttu-id="fd542-120">Chcete-li zabránit požadavkům na rozpad u výpočtů hlavního plánování prostřednictvím položky, nastavte ochrannou dobu rozpadu na hodnotu 0 (nula) dní pro disponibilitu položky nebo ve skupině disponibility.</span><span class="sxs-lookup"><span data-stu-id="fd542-120">To prevent master scheduling calculations from exploding requirements through the item, set the explosion fence to 0 (zero) days in item coverage or in the coverage group.</span></span> <span data-ttu-id="fd542-121">Kalkulace hlavního plánování bude pracovat s položkou jako s nakoupenou položkou a nebudou prováděny další výpočty pro údaje o kusovníku a postupu položky.</span><span class="sxs-lookup"><span data-stu-id="fd542-121">The master scheduling calculation will then treat the item as a purchased item and won't perform more calculations for the item's BOM and route information.</span></span>






