---
title: "Nastavení požadavků pro správu"
description: "Tento postup použijte pro povolení procesů správy neshod."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4bb4af7cb7aff101a8b9e6162823515f63b12886
ms.openlocfilehash: 9b5b05a3c00f093066a2714964bb99146427c3bc
ms.contentlocale: cs-cz
ms.lasthandoff: 11/02/2017

---
# <a name="set-up-prerequisites-for-management"></a><span data-ttu-id="13f1a-103">Nastavení požadavků pro správu</span><span class="sxs-lookup"><span data-stu-id="13f1a-103">Set up prerequisites for management</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="13f1a-104">Tento postup použijte pro povolení procesů správy neshod.</span><span class="sxs-lookup"><span data-stu-id="13f1a-104">Use this procedure to enable nonconformance management processes.</span></span> <span data-ttu-id="13f1a-105">Neshoda popisuje postup nebo položku, která má potíže s kvalitou, a kde popisné informace zahrnují zdroj a typ problému.</span><span class="sxs-lookup"><span data-stu-id="13f1a-105">A nonconformance describes a procedure or item that has a quality problem, where the descriptive information includes the source and type of problem.</span></span> <span data-ttu-id="13f1a-106">Tato procedura používá data ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="13f1a-106">This procedure uses the USMF demo data company.</span></span> <span data-ttu-id="13f1a-107">Tento postup obvykle provádí správce řízení kvality.</span><span class="sxs-lookup"><span data-stu-id="13f1a-107">This procedure is typically performed by a quality manager.</span></span>


## <a name="enable-quality-management-processes-within-the-company"></a><span data-ttu-id="13f1a-108">Povolení procesů správy kvality v rámci společnosti</span><span class="sxs-lookup"><span data-stu-id="13f1a-108">Enable quality management processes within the company</span></span>
1. <span data-ttu-id="13f1a-109">Přejděte do nabídky Řízení zásob > Nastavení > Parametry řízení zásob a skladu.</span><span class="sxs-lookup"><span data-stu-id="13f1a-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="13f1a-110">Klepněte na kartu Správa kvality.</span><span class="sxs-lookup"><span data-stu-id="13f1a-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="13f1a-111">Vyberte možnost Ano v poli Použít správu kvality.</span><span class="sxs-lookup"><span data-stu-id="13f1a-111">Select Yes in the Use quality management field.</span></span>
    * <span data-ttu-id="13f1a-112">Vyberte tento parametr, pokud chcete povolit proces správy kvality u společnosti.</span><span class="sxs-lookup"><span data-stu-id="13f1a-112">Select this parameter to enable quality management processes for the company.</span></span>  
4. <span data-ttu-id="13f1a-113">V poli Hodinová sazba je třeba zadat číslo.</span><span class="sxs-lookup"><span data-stu-id="13f1a-113">In the Hourly rate field, enter a number.</span></span>
    * <span data-ttu-id="13f1a-114">Do pole Hodinová sazba zadejte hodinovou pracovní sazbu v místní měně.</span><span class="sxs-lookup"><span data-stu-id="13f1a-114">Use the Hourly rate field to enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="13f1a-115">Hodinová sazba se používá pro výpočet nákladů na operace, které souvisejí s odstraněním neshody.</span><span class="sxs-lookup"><span data-stu-id="13f1a-115">The hourly rate is used for calculating costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="13f1a-116">Hodinová sazba a vypočtené náklady poskytují referenční informace o neshodách a navzájem se neovlivňují s dalšími funkcemi.</span><span class="sxs-lookup"><span data-stu-id="13f1a-116">The hourly rate and calculated costs provide reference information for a nonconformance, and they do not interact with other functionality.</span></span>  
5. <span data-ttu-id="13f1a-117">Klikněte na Nastavení sestavy.</span><span class="sxs-lookup"><span data-stu-id="13f1a-117">Click Report setup.</span></span>
    * <span data-ttu-id="13f1a-118">Tato stránka umožňuje definovat typy poznámek k sestavě kvality, které budou použity pro různé typy sestav správy kvality.</span><span class="sxs-lookup"><span data-stu-id="13f1a-118">This page allows you to define the quality report note types that will be used on different kinds of quality management reports.</span></span>  
6. <span data-ttu-id="13f1a-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="13f1a-119">Close the page.</span></span>
7. <span data-ttu-id="13f1a-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="13f1a-120">Close the page.</span></span>

## <a name="enable-user-for-nonconformance-processing"></a><span data-ttu-id="13f1a-121">Povolení zpracování neshody</span><span class="sxs-lookup"><span data-stu-id="13f1a-121">Enable user for nonconformance processing</span></span>
1. <span data-ttu-id="13f1a-122">Přejděte do nabídky Správa systému > Uživatelé > Uživatelé.</span><span class="sxs-lookup"><span data-stu-id="13f1a-122">Go to System administration > Users > Users.</span></span>
    * <span data-ttu-id="13f1a-123">Aby bylo možné zpracovat schválení neshody, uživatel, který schválí nebo zamítne neshodu, musí mít hodnotu "Název" přiřazenou na stránce Uživatelé.</span><span class="sxs-lookup"><span data-stu-id="13f1a-123">To process the approval of a nonconformance the user who  approves or rejects nonconformances must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="13f1a-124">Aby bylo možné použít poznámky k dokumentům, uživatel musí také mít aktivováno řízení dokumentů v možnostech uživatele.</span><span class="sxs-lookup"><span data-stu-id="13f1a-124">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
2. <span data-ttu-id="13f1a-125">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="13f1a-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="13f1a-126">Můžete například filtrovat v poli Jméno pomocí hodnoty „Ricardo“.</span><span class="sxs-lookup"><span data-stu-id="13f1a-126">For example, filter on the Name field with a value of 'Ricardo'.</span></span>
    * <span data-ttu-id="13f1a-127">Filtr umožňuje vyhledat uživatele, který bude schvalovat nebo zamítat záznamy neshody.</span><span class="sxs-lookup"><span data-stu-id="13f1a-127">Use the filter to find the user who will be approving or rejecting the nonconformance records.</span></span>  
3. <span data-ttu-id="13f1a-128">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="13f1a-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="13f1a-129">Aby bylo možné zpracovat schválení neshody, uživatel, který schválí nebo zamítne neshodu, musí mít hodnotu "Název" přiřazenou na stránce Uživatelé.</span><span class="sxs-lookup"><span data-stu-id="13f1a-129">To process the approval of a nonconformance, make sure the user who approves or rejects nonconformances has a “Name” value assigned on the Users page.</span></span>  
4. <span data-ttu-id="13f1a-130">Klikněte na Možnosti uživatelů.</span><span class="sxs-lookup"><span data-stu-id="13f1a-130">Click User options.</span></span>
5. <span data-ttu-id="13f1a-131">Klepněte na kartu Předvolby.</span><span class="sxs-lookup"><span data-stu-id="13f1a-131">Click the Preferences tab.</span></span>
6. <span data-ttu-id="13f1a-132">Vyberte možnost Ano v poli Povolit manipulaci s dokumenty.</span><span class="sxs-lookup"><span data-stu-id="13f1a-132">Select Yes in the Enable document handling field.</span></span>
    * <span data-ttu-id="13f1a-133">Aby bylo možné použít poznámky k dokumentům, uživatel musí také mít aktivováno řízení dokumentů v možnostech uživatele.</span><span class="sxs-lookup"><span data-stu-id="13f1a-133">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
7. <span data-ttu-id="13f1a-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="13f1a-134">Close the page.</span></span>
8. <span data-ttu-id="13f1a-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="13f1a-135">Close the page.</span></span>
9. <span data-ttu-id="13f1a-136">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="13f1a-136">Close the page.</span></span>

## <a name="define-diagnostic-types-for-nonconformance-processing"></a><span data-ttu-id="13f1a-137">Definice typů diagnostiky v rámci zpracování neshod</span><span class="sxs-lookup"><span data-stu-id="13f1a-137">Define diagnostic types for nonconformance processing</span></span>
1. <span data-ttu-id="13f1a-138">Přejděte na Řízení zásob > Nastavení > Správa kvality > Typy diagnostiky.</span><span class="sxs-lookup"><span data-stu-id="13f1a-138">Go to Inventory management > Setup > Quality management > Diagnostic types.</span></span>
    * <span data-ttu-id="13f1a-139">Pomocí stránky Typy diagnostiky definujte klasifikaci akcí diagnostiky.</span><span class="sxs-lookup"><span data-stu-id="13f1a-139">Use the Diagnostic types page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="13f1a-140">Oprava určuje, jaký typ diagnostické akce má být proveden pro schválenou neshodu, kdo ji má provést a jaké je požadované a plánované datum dokončení.</span><span class="sxs-lookup"><span data-stu-id="13f1a-140">A correction identifies what type of diagnostic action should be taken on an approved nonconformance, who should perform it, and the requested and planned completion date.</span></span>  
2. <span data-ttu-id="13f1a-141">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="13f1a-141">Click New.</span></span>
3. <span data-ttu-id="13f1a-142">Zadejte hodnotu do pole Diagnostika.</span><span class="sxs-lookup"><span data-stu-id="13f1a-142">In the Diagnostic field, type a value.</span></span>
4. <span data-ttu-id="13f1a-143">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="13f1a-143">In the Description field, type a value.</span></span>
5. <span data-ttu-id="13f1a-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="13f1a-144">Close the page.</span></span>

## <a name="define-quality-charges-for-nonconformance-processing"></a><span data-ttu-id="13f1a-145">Definice nákladů kvality v rámci zpracování neshod</span><span class="sxs-lookup"><span data-stu-id="13f1a-145">Define quality charges for nonconformance processing</span></span>
1. <span data-ttu-id="13f1a-146">Přejděte na Řízení zásob > Nastavení > Správa kvality > Náklady kvality.</span><span class="sxs-lookup"><span data-stu-id="13f1a-146">Go to Inventory management > Setup > Quality management > Quality charges.</span></span>
    * <span data-ttu-id="13f1a-147">Na stránce Náklady kvality definujte klasifikaci nákladů, které se použily v rámci operací souvisejících s neshodami.</span><span class="sxs-lookup"><span data-stu-id="13f1a-147">Use the Quality charges page to define a classification of charges that will used in operations related to nonconformances.</span></span>  
2. <span data-ttu-id="13f1a-148">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="13f1a-148">Click New.</span></span>
3. <span data-ttu-id="13f1a-149">Zadejte hodnotu do pole Kód nákladů.</span><span class="sxs-lookup"><span data-stu-id="13f1a-149">In the Charges code field, type a value.</span></span>
4. <span data-ttu-id="13f1a-150">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="13f1a-150">In the Description field, type a value.</span></span>
5. <span data-ttu-id="13f1a-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="13f1a-151">Close the page.</span></span>

## <a name="define-the-operations-for-nonconformance-processing"></a><span data-ttu-id="13f1a-152">Definice operací v rámci zpracování neshod</span><span class="sxs-lookup"><span data-stu-id="13f1a-152">Define the operations for nonconformance processing</span></span>
1. <span data-ttu-id="13f1a-153">Přejděte na Řízení zásob > Nastavení > Správa kvality > Operace.</span><span class="sxs-lookup"><span data-stu-id="13f1a-153">Go to Inventory management > Setup > Quality management > Operations.</span></span>
    * <span data-ttu-id="13f1a-154">Na stránce Operace definujte klasifikaci práce, která může být provedena pro schválenou neshodu.</span><span class="sxs-lookup"><span data-stu-id="13f1a-154">Use the Operations page to define a classification of the work that may be performed for an approved nonconformance.</span></span> <span data-ttu-id="13f1a-155">Přiřadíte-li k neshodě související operaci, můžete definovat informace o přiřazeném materiálu, pracovní době a různých poplatcích vyžadovaných pro provedení této operace.</span><span class="sxs-lookup"><span data-stu-id="13f1a-155">When you relate an operation to a nonconformance, you can define information about the associated material, labor hours, and miscellaneous charges that are required to perform the operation.</span></span> <span data-ttu-id="13f1a-156">Tyto informace tvoří základ výpočtu odhadovaných nákladů na provedení operace.</span><span class="sxs-lookup"><span data-stu-id="13f1a-156">This information provides the basis for calculating an estimated cost for performing the operation.</span></span>  
2. <span data-ttu-id="13f1a-157">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="13f1a-157">Click New.</span></span>
3. <span data-ttu-id="13f1a-158">Zadejte hodnotu do pole Operace.</span><span class="sxs-lookup"><span data-stu-id="13f1a-158">In the Operation field, type a value.</span></span>
4. <span data-ttu-id="13f1a-159">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="13f1a-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="13f1a-160">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="13f1a-160">Close the page.</span></span>

## <a name="define-problem-types-for-nonconformance-processing"></a><span data-ttu-id="13f1a-161">Definice typů problému v rámci zpracování neshod</span><span class="sxs-lookup"><span data-stu-id="13f1a-161">Define problem types for nonconformance processing</span></span>
1. <span data-ttu-id="13f1a-162">Přejděte na Řízení zásob > Nastavení > Správa kvality > Typy problémů.</span><span class="sxs-lookup"><span data-stu-id="13f1a-162">Go to Inventory management > Setup > Quality management > Problem types.</span></span>
    * <span data-ttu-id="13f1a-163">Na stránce Typy problémů definujte klasifikaci problémů s kvalitou, k nimž dochází u různých typů neshod.</span><span class="sxs-lookup"><span data-stu-id="13f1a-163">Use the Problem types page to define a classification of quality problems that are encountered in the various nonconformance types.</span></span> <span data-ttu-id="13f1a-164">Mezi typy neshody patří: interní, odběratel, dodavatel, požadavek na službu, výroba a vedlejší produkt.</span><span class="sxs-lookup"><span data-stu-id="13f1a-164">The nonconformance types include Internal, Customer, Vendor, Service request, Production, and Co-product production.</span></span> <span data-ttu-id="13f1a-165">Jeden typ problému může být spojen s několika typy neshod.</span><span class="sxs-lookup"><span data-stu-id="13f1a-165">A single problem type can be associated with multiple nonconformance types.</span></span>  
2. <span data-ttu-id="13f1a-166">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="13f1a-166">Click New.</span></span>
3. <span data-ttu-id="13f1a-167">Zadejte hodnotu do pole Typ problému.</span><span class="sxs-lookup"><span data-stu-id="13f1a-167">In the Problem type field, type a value.</span></span>
4. <span data-ttu-id="13f1a-168">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="13f1a-168">In the Description field, type a value.</span></span>
5. <span data-ttu-id="13f1a-169">Klikněte na Typy neshody.</span><span class="sxs-lookup"><span data-stu-id="13f1a-169">Click Non conformance types.</span></span>
    * <span data-ttu-id="13f1a-170">Použijte stránku Typy neshody k povolení typu problému, který se má použít v jednom nebo více typech neshod.</span><span class="sxs-lookup"><span data-stu-id="13f1a-170">Use the Non conformance types page to authorize the use of a problem type for one or more of the nonconformance types.</span></span> <span data-ttu-id="13f1a-171">Typ problému zahrnující kód závady se může například vztahovat na všechny typy neshod, zatímco typ problému zahrnující stížnost odběratele se může týkat pouze typů neshod "odběratel" a "požadavek na službu".</span><span class="sxs-lookup"><span data-stu-id="13f1a-171">For example, a problem type regarding a defect code could apply to all nonconformance types, whereas a problem type about customer complaints may only apply to the customer and service request nonconformance types.</span></span>  
6. <span data-ttu-id="13f1a-172">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="13f1a-172">Click New.</span></span>
7. <span data-ttu-id="13f1a-173">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="13f1a-173">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="13f1a-174">Vyberte volbu v poli Typ neshody.</span><span class="sxs-lookup"><span data-stu-id="13f1a-174">In the Non conformance type field, select an option.</span></span>
9. <span data-ttu-id="13f1a-175">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="13f1a-175">Close the page.</span></span>
10. <span data-ttu-id="13f1a-176">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="13f1a-176">Close the page.</span></span>

## <a name="define-quarantine-zones-for-nonconformance-processing"></a><span data-ttu-id="13f1a-177">Definice karanténních zóny ke zpracování neshod</span><span class="sxs-lookup"><span data-stu-id="13f1a-177">Define quarantine zones for nonconformance processing</span></span>
1. <span data-ttu-id="13f1a-178">Přejděte na Řízení zásob > Nastavení > Správa kvality > Karanténní zóny.</span><span class="sxs-lookup"><span data-stu-id="13f1a-178">Go to Inventory management > Setup > Quality management > Quarantine zones.</span></span>
2. <span data-ttu-id="13f1a-179">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="13f1a-179">Click New.</span></span>
3. <span data-ttu-id="13f1a-180">Zadejte hodnotu do pole Karanténní zóna.</span><span class="sxs-lookup"><span data-stu-id="13f1a-180">In the Quarantine zone field, type a value.</span></span>
4. <span data-ttu-id="13f1a-181">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="13f1a-181">In the Description field, type a value.</span></span>
5. <span data-ttu-id="13f1a-182">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="13f1a-182">Close the page.</span></span>

