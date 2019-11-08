---
title: Co je nového nebo změněného v aplikaci Dynamics AX verze 7.0.1 (květen 2016)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics AX verze 7.0.1. Tato verze byla vydána v květnu 2016 a má číslo sestavení 7.0.1265.23014.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 4524eb14ff06561ad186cf63654e6a716632a3f4
ms.sourcegitcommit: 4d6ec2b1a9674712e1efb8c46b919d554f21a2b3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2019
ms.locfileid: "2627606"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a><span data-ttu-id="8ba10-104">Co je nového nebo změněného v aplikaci Dynamics AX verze 7.0.1 (květen 2016)</span><span class="sxs-lookup"><span data-stu-id="8ba10-104">What's new or changed in Dynamics AX application version 7.0.1 (May 2016)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ba10-105">Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics AX verze 7.0.1.</span><span class="sxs-lookup"><span data-stu-id="8ba10-105">This article describes features that are either new or changed in Microsoft Dynamics AX application version 7.0.1.</span></span> <span data-ttu-id="8ba10-106">Tato verze byla vydána v květnu 2016 a má číslo sestavení 7.0.1265.23014.</span><span class="sxs-lookup"><span data-stu-id="8ba10-106">This version was released in May 2016 and has a build number of 7.0.1265.23014.</span></span>

## <a name="electronic-reporting-er"></a><span data-ttu-id="8ba10-107">Elektronické výkaznictví (EV)</span><span class="sxs-lookup"><span data-stu-id="8ba10-107">Electronic reporting (ER)</span></span>

| <span data-ttu-id="8ba10-108">Co můžete udělat?</span><span class="sxs-lookup"><span data-stu-id="8ba10-108">What can you do?</span></span> | <span data-ttu-id="8ba10-109">Proč je to důležité?</span><span class="sxs-lookup"><span data-stu-id="8ba10-109">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="8ba10-110">Nakonfigurujte běhové dialogové okno pro navrhování sestav elektronické vykazování (EV), aby tak uživatelé mohli vybírat požadované finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="8ba10-110">Configure a run-time dialog box for designing Electronic reporting (ER) reports, so that users can select the financial dimensions that they want.</span></span> | <span data-ttu-id="8ba10-111">V době spuštění v dialogovém okně pro spuštění sestavy EV mohou uživatelé vybírat z více finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="8ba10-111">At run time, in the dialog box for running an ER report, users can select multiple financial dimensions.</span></span> <span data-ttu-id="8ba10-112">Zobrazí se podrobné informace o vybraných finančních dimenzích v elektronickém dokumentu, který je generován.</span><span class="sxs-lookup"><span data-stu-id="8ba10-112">The details of the selected financial dimensions will be displayed in the electronic document that is generated.</span></span> |
| <span data-ttu-id="8ba10-113">Při návrhu sestavy EV nastavte přístup k více finančním dimenzím prostřednictvím jednotného mapování požadovaného zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="8ba10-113">Configure access to multiple financial dimensions during the design of an ER report, via a single mapping to the desired data source.</span></span> | <span data-ttu-id="8ba10-114">Stejnou konfiguraci sestavy EV lze použít ke generování elektronických dokumentů, které obsahují transakční data a podrobnosti o finančních dimenzích, bez ohledu na počet finančních dimenzí, které jsou vybrané uživatelem nebo nakonfigurovány pro aktuální právnickou osobu nebo instanci.</span><span class="sxs-lookup"><span data-stu-id="8ba10-114">The same ER report configuration can be used to generate electronic documents that present transactional data together with details of financial dimensions, regardless of the number of financial dimensions that are either selected by the user or configured for the current legal entity or instance.</span></span> |
| <span data-ttu-id="8ba10-115">Nakonfigurujte sestavu EV pro zadávání dat v dynamicky generovaných sloupcích elektronického dokumentu, který je vytvořen ve formátu listu OPENXML.</span><span class="sxs-lookup"><span data-stu-id="8ba10-115">Configure an ER report to enter data in dynamically generated columns of an electronic document that is created in OPENXML worksheet format.</span></span> | <span data-ttu-id="8ba10-116">Zpráva EV umožňuje zadávání dat ve vygenerovaném listu OPENXML pomocí vodorovně replikovaných sloupců.</span><span class="sxs-lookup"><span data-stu-id="8ba10-116">An ER report can enter data in an OPENXML worksheet that is generated, via horizontally replicating columns.</span></span> <span data-ttu-id="8ba10-117">Proto stejnou konfigurací sestavy EV lze znovu použít ke generování elektronických dokumentů, které mají různý počet dynamicky generovaných sloupců.</span><span class="sxs-lookup"><span data-stu-id="8ba10-117">Therefore, the same ER report configuration can be reused to generate electronic documents that have a different number of dynamically generated columns.</span></span> |
| <span data-ttu-id="8ba10-118">Nakonfigurujte cíle EV tak, aby výstupní výsledek formátu byl směrován do určitého cíle: soubor, e-mail nebo archív (složka Microsoft SharePoint nebo Microsoft Azure Storage).</span><span class="sxs-lookup"><span data-stu-id="8ba10-118">Configure ER destinations so that the output result of a format is directed to specific destination: file, email, or archive (Microsoft SharePoint folder or Microsoft Azure Storage).</span></span> | <span data-ttu-id="8ba10-119">Dříve se při spuštění konfigurace EV zobrazilo okno se zprávou akce požadující po uživateli akci pro uložení nebo otevření souboru.</span><span class="sxs-lookup"><span data-stu-id="8ba10-119">Previously, when you ran an ER configuration, a message box appeared that required user action to save or open a file.</span></span> <span data-ttu-id="8ba10-120">Pro každou konfiguraci formátu a její komponenty (složku nebo soubor) lze nově předem konfigurovat cíl samostatně.</span><span class="sxs-lookup"><span data-stu-id="8ba10-120">You can now pre-configure a destination for each format configuration and for each output component (a folder or a file) separately.</span></span> <span data-ttu-id="8ba10-121">Uživatelé, kterým jsou udělena přístupová práva, mohou také měnit nastavení cíle v době běhu.</span><span class="sxs-lookup"><span data-stu-id="8ba10-121">Users who have appropriate access rights can also modify destination settings at run time.</span></span> |

## <a name="pos--microsoft-dynamics-ax-retail"></a><span data-ttu-id="8ba10-122">POS – Microsoft Dynamics AX maloobchod</span><span class="sxs-lookup"><span data-stu-id="8ba10-122">POS – Microsoft Dynamics AX Retail</span></span>

| <span data-ttu-id="8ba10-123">Co můžete udělat?</span><span class="sxs-lookup"><span data-stu-id="8ba10-123">What can you do?</span></span> | <span data-ttu-id="8ba10-124">Proč je to důležité?</span><span class="sxs-lookup"><span data-stu-id="8ba10-124">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="8ba10-125">Použijte prohlížeč Google Chrome.</span><span class="sxs-lookup"><span data-stu-id="8ba10-125">Use the Google Chrome browser.</span></span> | <span data-ttu-id="8ba10-126">Prodejci mohou nově spouštět Cloud POS z prohlížeče Chrome a využívat tak všechny funkce, které jsou k dispozici ve verzi Cloud POS pro Microsoft Edge a Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="8ba10-126">Retailers can now start Cloud POS from the Chrome browser, and can experience all the functionality that is available in the Microsoft Edge and Internet Explorer version of Cloud POS.</span></span> |

## <a name="financial-reporting"></a><span data-ttu-id="8ba10-127">Finanční výkaznictví</span><span class="sxs-lookup"><span data-stu-id="8ba10-127">Financial reporting</span></span>

| <span data-ttu-id="8ba10-128">Co můžete udělat?</span><span class="sxs-lookup"><span data-stu-id="8ba10-128">What can you do?</span></span> | <span data-ttu-id="8ba10-129">Proč je to důležité?</span><span class="sxs-lookup"><span data-stu-id="8ba10-129">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="8ba10-130">Znovu sestavte datové tržiště finančního vykazování.</span><span class="sxs-lookup"><span data-stu-id="8ba10-130">Rebuild the Financial reporting data mart.</span></span> | <span data-ttu-id="8ba10-131">Při přesunutí databází aplikace Dynamics AX mezi prostředími nebo provádění jiných invazivních změn v prostředí může být potřeba znovu sestavit databázi finančního vykazování.</span><span class="sxs-lookup"><span data-stu-id="8ba10-131">When you move Dynamics AX databases between environments or make other invasive changes to the environment, the Financial reporting database might have to be rebuilt.</span></span> <span data-ttu-id="8ba10-132">Nyní je dostupný skript prostředí Windows PowerShell, který znovu sestaví databázi za vás.</span><span class="sxs-lookup"><span data-stu-id="8ba10-132">A Windows PowerShell script is now provided to rebuild the database for you.</span></span> |
| <span data-ttu-id="8ba10-133">Nově již není možné vybrat možnosti návrháře sestav, které nejsou platné.</span><span class="sxs-lookup"><span data-stu-id="8ba10-133">You can no longer select report designer options that aren't valid.</span></span> | <span data-ttu-id="8ba10-134">Některé možnosti návrháře sestav, které byly použity ve verzích trhu v aplikaci Management Reporter, se na tuto verzi Dynamics AX nevztahují.</span><span class="sxs-lookup"><span data-stu-id="8ba10-134">Several report designer options that were used in the in-market versions of Management reporter don't apply to this version of Dynamics AX.</span></span> <span data-ttu-id="8ba10-135">Tyto možnosti souvisejí s návrhem, výstupem a propojením finanční sestavy.</span><span class="sxs-lookup"><span data-stu-id="8ba10-135">These options were related to financial report design, output, and linking.</span></span> <span data-ttu-id="8ba10-136">Tyto možnosti byly odebrány z návrháře finančních sestav, aby nedocházelo k chybám uživatele.</span><span class="sxs-lookup"><span data-stu-id="8ba10-136">These options have been removed from the financial report designer to prevent user errors.</span></span> |

## <a name="financial-management"></a><span data-ttu-id="8ba10-137">Správa financí</span><span class="sxs-lookup"><span data-stu-id="8ba10-137">Financial management</span></span>

| <span data-ttu-id="8ba10-138">Co můžete udělat?</span><span class="sxs-lookup"><span data-stu-id="8ba10-138">What can you do?</span></span> | <span data-ttu-id="8ba10-139">Proč je to důležité?</span><span class="sxs-lookup"><span data-stu-id="8ba10-139">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="8ba10-140">Generování souborů kladných plateb pro platby závazků.</span><span class="sxs-lookup"><span data-stu-id="8ba10-140">Generate positive pay files for accounts payable payments.</span></span> | <span data-ttu-id="8ba10-141">Je možné generovat soubory kladných plateb, které pomáhají bankám zabránit podvodným šekům.</span><span class="sxs-lookup"><span data-stu-id="8ba10-141">Positive pay files can be generated to help prevent check fraud.</span></span> |

## <a name="warehouse-and-production"></a><span data-ttu-id="8ba10-142">Sklad a výroba</span><span class="sxs-lookup"><span data-stu-id="8ba10-142">Warehouse and production</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="8ba10-143">Co můžete udělat?</span><span class="sxs-lookup"><span data-stu-id="8ba10-143">What can you do?</span></span></th>
<th><span data-ttu-id="8ba10-144">Proč je to důležité?</span><span class="sxs-lookup"><span data-stu-id="8ba10-144">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8ba10-145">Definujte zásady práce ve skladu, které řídí vytváření práce pro sadu produktů v jednotlivých místech.</span><span class="sxs-lookup"><span data-stu-id="8ba10-145">Define a warehouse work policy that controls the creation of work for a set of products at specific locations.</span></span></td>
<td><span data-ttu-id="8ba10-146">Skladové procesy ne vždy zahrnují práci.</span><span class="sxs-lookup"><span data-stu-id="8ba10-146">Warehouse processes don't always include work.</span></span> <span data-ttu-id="8ba10-147">Použitím nových zásad práce ve skladu můžete zabránit vytváření práce pro výdej surovin, ale také vyskladnění dokončených výrobků pro sérii produktů v konkrétních umístěních.</span><span class="sxs-lookup"><span data-stu-id="8ba10-147">By using the new warehouse work policy, you can prevent work from being created for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ba10-148">Určete, že výstupní místo výroby není řízeno pomocí registračních značek.</span><span class="sxs-lookup"><span data-stu-id="8ba10-148">Specify that a production output location isn't license plate–controlled.</span></span></td>
<td><span data-ttu-id="8ba10-149">Nově můžete určit, že výstupní místo výrobku není řízeno pomocí registračních značek.</span><span class="sxs-lookup"><span data-stu-id="8ba10-149">You can now specify that a product output location isn't license plate–controlled.</span></span> <span data-ttu-id="8ba10-150">Tato funkce je například užitečná, pokud nadřazená výrobní objednávka vykazuje dokončené položky přímo do umístění, které slouží jako vstupní místo výroby pro navazující výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="8ba10-150">For example, this feature is useful when an upstream production order reports items as finished directly to a location that acts as production input location for a downstream production order.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ba10-151">Podpora kusovníků, která obsahuje položky s různými dimenzemi produktů pro stejnou položku.</span><span class="sxs-lookup"><span data-stu-id="8ba10-151">Support BOMs that include items with different product dimensions of the same item.</span></span></td>
<td><span data-ttu-id="8ba10-152">Používáte-li jednu nebo více dimenzí produktu ve výrobě, mohou nastat situace, kde chcete vytvořit položku na základě na různých variant téhož zboží.</span><span class="sxs-lookup"><span data-stu-id="8ba10-152">When using one or multiple of the product dimensions in production, you can have situations where you would like to produce an item, based on a different variant of the same item.</span></span> <span data-ttu-id="8ba10-153">Další informace naleznete v <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">tomto blogu</a>.</span><span class="sxs-lookup"><span data-stu-id="8ba10-153">For more information, see <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">this blog</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ba10-154">Výrobní zakázky s cyklickými strukturami na první úrovni jejich kusovníků jsou vyloučeny z výpočtu kusovníku pro plánování materiálových zdrojů.</span><span class="sxs-lookup"><span data-stu-id="8ba10-154">Production orders with circular structures at the first level of their BOMs are excluded from BOM level calculation for material resource planning.</span></span></td>
<td><span data-ttu-id="8ba10-155">Není možné přiřadit správné úrovně kusovníku k variantám produktů u výrobních zakázek, které způsobují cyklické vztahy v hierarchii kusovníku.</span><span class="sxs-lookup"><span data-stu-id="8ba10-155">It is not possible to assign correct BOM levels to product variants for production orders that cause circularity in the BOM hierarchy.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8ba10-156">Výpočet samostatných úrovní kusovníku pro plánování materiálových zdrojů a výpočet nákladů:</span><span class="sxs-lookup"><span data-stu-id="8ba10-156">Calculate separate BOM levels for material resource planning and cost calculation:</span></span>
<ul>
<li><span data-ttu-id="8ba10-157">Pro plánování materiálových zdrojů se úrovně kusovníku počítají v nové tabulce <strong>ReqItemLevel</strong>.</span><span class="sxs-lookup"><span data-stu-id="8ba10-157">For material resource planning, BOM levels are calculated in the new <strong>ReqItemLevel</strong> table.</span></span> <span data-ttu-id="8ba10-158">Ve výpočtu jsou ignorovány ukončené výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="8ba10-158">Ended production orders are ignored in the calculation.</span></span></li>
<li><span data-ttu-id="8ba10-159">Pro výpočet výrobních nákladů se úrovně kusovníku počítají v tabulce <strong>InventTable</strong>.</span><span class="sxs-lookup"><span data-stu-id="8ba10-159">For production cost calculation, BOM levels are calculated in the <strong>InventTable</strong>.</span></span> <span data-ttu-id="8ba10-160">Ve výpočtu jsou zahrnuty ukončené výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="8ba10-160">Ended production orders are included in the calculation.</span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="8ba10-161">Při spuštění plánování materiálových zdrojů, jako je například plánování hlavního plánu a rozpad, je nutné přepočítat pouze úrovně kusovníku používané pro plánování materiálových zdrojů.</span><span class="sxs-lookup"><span data-stu-id="8ba10-161">When running material resource planning, for example, master planning plan scheduling and explosion, only BOM levels used for material resource planning need to be recalculated.</span></span> <span data-ttu-id="8ba10-162">Jinými slovy není třeba vypočítat úrovně kusovníku, které jsou použity pro výpočet výrobních nákladů.</span><span class="sxs-lookup"><span data-stu-id="8ba10-162">In other words, there is no need to calculate BOM levels used for production costing calculation.</span></span></li>
<li><span data-ttu-id="8ba10-163">Při spuštění operací pro výpočet nákladů, jako jsou například skladové uzávěrky, je nutné přepočítat pouze úrovně kusovníku používané pro výpočet výrobních nákladů.</span><span class="sxs-lookup"><span data-stu-id="8ba10-163">When running costing operations, for example, inventory closing, only BOM levels used for production costing calculation need to be recalculated.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="8ba10-164">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="8ba10-164">Additional resources</span></span>

[<span data-ttu-id="8ba10-165">Co je nového a co se změnilo</span><span class="sxs-lookup"><span data-stu-id="8ba10-165">What's new or changed</span></span>](whats-new-changed.md)

[<span data-ttu-id="8ba10-166">Noví nebo aktualizovaní průvodci úkolem (květen 2016)</span><span class="sxs-lookup"><span data-stu-id="8ba10-166">New or updated task guides (May 2016)</span></span>](new-updated-task-guides-available-may-2016.md)
