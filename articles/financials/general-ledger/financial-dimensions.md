---
title: "Finanční dimenze"
description: "Toto téma popisuje různé typy finančních dimenzí a způsob jejich nastavení."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 274a5e696bfde4f5e27bc186fadbab69f5fc655d
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="financial-dimensions"></a><span data-ttu-id="9d63c-103">Finanční dimenze</span><span class="sxs-lookup"><span data-stu-id="9d63c-103">Financial dimensions</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9d63c-104">Toto téma popisuje různé typy finančních dimenzí a způsob jejich nastavení.</span><span class="sxs-lookup"><span data-stu-id="9d63c-104">This topic explains the various types of financial dimensions and how they are set up.</span></span>

<span data-ttu-id="9d63c-105">Pomocí stránky **Finanční dimenze** můžete vytvářet finanční dimenze, které lze použít jako segmenty účtu pro účtové osnovy.</span><span class="sxs-lookup"><span data-stu-id="9d63c-105">Use the **Financial dimensions** page to create financial dimensions that you can use as account segments for charts of accounts.</span></span> <span data-ttu-id="9d63c-106">Existují dva typy finančních dimenzí – vlastní dimenze a dimenze zajištěné entitou.</span><span class="sxs-lookup"><span data-stu-id="9d63c-106">There are two types of financial dimensions: custom dimensions and entity-backed dimensions.</span></span> <span data-ttu-id="9d63c-107">Vlastní dimenze jsou společné pro více právnických osob a jejich hodnoty zadávají a spravují uživatelé.</span><span class="sxs-lookup"><span data-stu-id="9d63c-107">Custom dimensions are shared across legal entities, and the values are entered and maintained by users.</span></span> <span data-ttu-id="9d63c-108">U dimenzí zajištěných entitou jsou hodnoty definovány jinde v systému, například v entitách Odběratelé nebo Obchody.</span><span class="sxs-lookup"><span data-stu-id="9d63c-108">For entity-backed dimensions, the values are defined somewhere else in the system, such as Customers or Stores entities.</span></span> <span data-ttu-id="9d63c-109">Některé dimenze zajištěné entitami jsou společné pro více právnických osob, zatímco jiné platí pro konkrétní společnost.</span><span class="sxs-lookup"><span data-stu-id="9d63c-109">Some entity-backed dimensions are shared across legal entities, whereas other entity-backed dimensions are company-specific.</span></span> 

<span data-ttu-id="9d63c-110">Po vytvoření finančních dimenzí použijte stránku **Hodnoty finanční dimenze** k přiřazení dalších vlastností ke každé finanční dimenzi.</span><span class="sxs-lookup"><span data-stu-id="9d63c-110">After you've created the financial dimensions, use the **Financial dimension values** page to assign additional properties to each financial dimension.</span></span> 

<span data-ttu-id="9d63c-111">Finanční dimenze mohou reprezentovat právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="9d63c-111">You can use financial dimensions to represent legal entities.</span></span> <span data-ttu-id="9d63c-112">V aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition nemusíte právnické osoby vytvářet.</span><span class="sxs-lookup"><span data-stu-id="9d63c-112">You don't have to create the legal entities in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="9d63c-113">Finanční dimenze však nejsou určeny k řešení provozních nebo obchodních požadavků právnických osob.</span><span class="sxs-lookup"><span data-stu-id="9d63c-113">However, financial dimensions aren’t designed to address the operational or business requirements of legal entities.</span></span> <span data-ttu-id="9d63c-114">Funkce mezijednotkového účetnictví v aplikaci Finance and Operations je určena pouze k práci s účetními položkami vytvořenými jednotlivými transakcemi.</span><span class="sxs-lookup"><span data-stu-id="9d63c-114">The interunit accounting functionality in Finance and Operations is designed to address only the accounting entries that are created by each transaction.</span></span> 

<span data-ttu-id="9d63c-115">Než nastavíte finanční dimenze jako právnické osoby, vyhodnoťte obchodní procesy v následujících oblastech a určete, zda bude tento systém ve vaší organizaci fungovat:</span><span class="sxs-lookup"><span data-stu-id="9d63c-115">Before you set up financial dimensions as legal entities, evaluate your business processes in the following areas to determine whether this setup will work for your organization:</span></span>

- <span data-ttu-id="9d63c-116">Zásoby</span><span class="sxs-lookup"><span data-stu-id="9d63c-116">Inventory</span></span>
- <span data-ttu-id="9d63c-117">Nákup a prodej mezi finančními dimenzemi a právnickými osobami</span><span class="sxs-lookup"><span data-stu-id="9d63c-117">Sales and purchases between financial dimensions and legal entities</span></span>
- <span data-ttu-id="9d63c-118">Výpočet a vykazování DPH</span><span class="sxs-lookup"><span data-stu-id="9d63c-118">Sales tax calculation and reporting</span></span>
- <span data-ttu-id="9d63c-119">Operační vykazování</span><span class="sxs-lookup"><span data-stu-id="9d63c-119">Operational reporting</span></span>

<span data-ttu-id="9d63c-120">Zde jsou uvedena některá omezení:</span><span class="sxs-lookup"><span data-stu-id="9d63c-120">Here are some of the limitations:</span></span>

- <span data-ttu-id="9d63c-121">Funkci DPH lze používat pouze s právnickými osobami, ale ne s finančními dimenzemi.</span><span class="sxs-lookup"><span data-stu-id="9d63c-121">You can use sales tax functionality only with legal entities, not with financial dimensions.</span></span>
- <span data-ttu-id="9d63c-122">Některé sestavy neobsahují finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="9d63c-122">Some reports don't include financial dimensions.</span></span> <span data-ttu-id="9d63c-123">Pokud tedy budete chtít tyto dimenze v sestavách použít, bude možná nutné sestavy upravit.</span><span class="sxs-lookup"><span data-stu-id="9d63c-123">Therefore, to report by financial dimension, you might have to modify the reports.</span></span>

## <a name="custom-dimensions"></a><span data-ttu-id="9d63c-124">Vlastní dimenze</span><span class="sxs-lookup"><span data-stu-id="9d63c-124">Custom dimensions</span></span>

<span data-ttu-id="9d63c-125">Pokud chcete vytvořit uživatelskou finanční dimenzi, vyberte v poli **Použít hodnoty od** možnost **&lt;Vlastní dimenze&gt;**.</span><span class="sxs-lookup"><span data-stu-id="9d63c-125">To create a user-defined financial dimension, in the **Use values from** field, select **&lt; Custom dimension &gt;**.</span></span> <span data-ttu-id="9d63c-126">Můžete také učit účetní masku pro omezení množství a typů informací, které můžete zadat pro hodnoty dimenze.</span><span class="sxs-lookup"><span data-stu-id="9d63c-126">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span> <span data-ttu-id="9d63c-127">Můžete zadat znaky, které zůstanou u všech hodnot dimenze stejné, například písmena nebo spojovníky (-).</span><span class="sxs-lookup"><span data-stu-id="9d63c-127">You can enter characters that remain the same for each dimension value, such as letters or a hyphen (-).</span></span> <span data-ttu-id="9d63c-128">Můžete také zadat znaky čísel (\#) a znak ampersand (&) jako zástupné symboly pro písmena a čísla, která se změní pokaždé, když je hodnota dimenze vytvořena.</span><span class="sxs-lookup"><span data-stu-id="9d63c-128">You can also enter number signs (\#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="9d63c-129">Použijte znak čísla (\#) jako zástupný symbol pro číslo a ampersand (&) jako zástupný symbol pro písmeno.</span><span class="sxs-lookup"><span data-stu-id="9d63c-129">Use a number sign (\#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span> <span data-ttu-id="9d63c-130">Pole masky formátu je k dispozici pouze tehdy, pokud vyberete možnost **&lt;Vlastní dimenze&gt;** v poli **Použít hodnoty od**.</span><span class="sxs-lookup"><span data-stu-id="9d63c-130">The field for the format mask is available only when you select **&lt; Custom dimension &gt;** in the **Use values from** field.</span></span>

<span data-ttu-id="9d63c-131">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="9d63c-131">**Example**</span></span>

<span data-ttu-id="9d63c-132">Chcete-li omezit hodnotu dimenze na písmena „CC“ a tři čísla, zadejte jako masku formátu **CC-\#\#\#**.</span><span class="sxs-lookup"><span data-stu-id="9d63c-132">To limit the dimension value to the letters "CC" and three numbers, enter **CC-\#\#\#** as the format mask.</span></span>

## <a name="entity-backed-dimensions"></a><span data-ttu-id="9d63c-133">Dimenze zajištěné entitou</span><span class="sxs-lookup"><span data-stu-id="9d63c-133">Entity-backed dimensions</span></span>

<span data-ttu-id="9d63c-134">Pokud chcete použít finanční dimenzi zajištěnou entitou, vyberte v poli **Použít hodnoty od** systémem definovanou entitu, která bude základem dimenze.</span><span class="sxs-lookup"><span data-stu-id="9d63c-134">To create an entity-backed financial dimension, in the **Use values from** field, select a system-defined entity to base the financial dimension on.</span></span> <span data-ttu-id="9d63c-135">Hodnoty finanční dimenze se vytvoří z této entity.</span><span class="sxs-lookup"><span data-stu-id="9d63c-135">Financial dimension values are then created from that entity.</span></span> <span data-ttu-id="9d63c-136">Chcete-li například vytvořit hodnoty dimenze pro projekty, vyberte možnost **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="9d63c-136">For example, to create dimension values for projects, select **Projects**.</span></span> <span data-ttu-id="9d63c-137">Hodnota dimenze se vytvoří pro každý název projektu.</span><span class="sxs-lookup"><span data-stu-id="9d63c-137">A dimension value is then created for each project name.</span></span> <span data-ttu-id="9d63c-138">Stránka **Hodnoty finanční dimenze** uvádí hodnoty pro entitu.</span><span class="sxs-lookup"><span data-stu-id="9d63c-138">The **Financial dimension values** page shows the values for the entity.</span></span> <span data-ttu-id="9d63c-139">Pokud tyto hodnoty platí pro konkrétní společnost, zobrazí se i její název.</span><span class="sxs-lookup"><span data-stu-id="9d63c-139">If those values are company-specific, the page also shows the company.</span></span>

## <a name="activating-dimensions"></a><span data-ttu-id="9d63c-140">Aktivační dimenze</span><span class="sxs-lookup"><span data-stu-id="9d63c-140">Activating dimensions</span></span>

<span data-ttu-id="9d63c-141">Při aktivaci finanční dimenze se tabulka aktualizuje a zobrazí se v ní název dimenze.</span><span class="sxs-lookup"><span data-stu-id="9d63c-141">When you activate a financial dimension, the table is updated so that it includes the name of the financial dimension.</span></span> <span data-ttu-id="9d63c-142">Odstraněné dimenze budou odebrány.</span><span class="sxs-lookup"><span data-stu-id="9d63c-142">Deleted dimensions are removed.</span></span> <span data-ttu-id="9d63c-143">Před aktivací finanční dimenze můžete zadat hodnoty dimenze.</span><span class="sxs-lookup"><span data-stu-id="9d63c-143">You can enter dimension values before you activate a financial dimension.</span></span> <span data-ttu-id="9d63c-144">Finanční dimenze lze však upotřebit až po aktivaci.</span><span class="sxs-lookup"><span data-stu-id="9d63c-144">However, a financial dimension can't be consumed anywhere until it's activated.</span></span> <span data-ttu-id="9d63c-145">Například nelze přidat finanční dimenzi do účetní struktury, dokud ji neaktivujete.</span><span class="sxs-lookup"><span data-stu-id="9d63c-145">For example, you can't add a financial dimension to an account structure until the financial dimension has been activated.</span></span> <span data-ttu-id="9d63c-146">Po kliknutí na možnost **Aktivovat** se všechny dimenze aktualizují a zobrazí se změny stavu.</span><span class="sxs-lookup"><span data-stu-id="9d63c-146">When you click **Activate**, all dimensions are updated and show status changes.</span></span> 

## <a name="translations"></a><span data-ttu-id="9d63c-147">Překlady</span><span class="sxs-lookup"><span data-stu-id="9d63c-147">Translations</span></span>

<span data-ttu-id="9d63c-148">Na stránce **Překlad textu** můžete zadat text vybrané finanční dimenze v různých jazycích.</span><span class="sxs-lookup"><span data-stu-id="9d63c-148">On the **Text translation** page, you can enter text for the selected financial dimension in various languages.</span></span> <span data-ttu-id="9d63c-149">Na stránce **Překlad hlavního účtu** můžete zadat text hlavního účtu v různých jazycích.</span><span class="sxs-lookup"><span data-stu-id="9d63c-149">On the **Main account translation** page, you can enter text for the main account in various languages.</span></span> 

## <a name="legal-entity-overrides"></a><span data-ttu-id="9d63c-150">Přepisy právnických osob</span><span class="sxs-lookup"><span data-stu-id="9d63c-150">Legal entity overrides</span></span>

<span data-ttu-id="9d63c-151">Ne všechny dimenze jsou u všech právnických osob platné.</span><span class="sxs-lookup"><span data-stu-id="9d63c-151">Not all dimensions are valid for all legal entities.</span></span> <span data-ttu-id="9d63c-152">Některé dimenze kromě toho mohou platit jen v určitém období.</span><span class="sxs-lookup"><span data-stu-id="9d63c-152">Additionally, some dimensions might be relevant only for a specific period.</span></span> <span data-ttu-id="9d63c-153">V takových případech lze pomocí části **Přepisy právnických osob** určit společnosti, u kterých má být použití dimenze pozastaveno, kdo je vlastníkem a období aktivity dimenze.</span><span class="sxs-lookup"><span data-stu-id="9d63c-153">In these cases, you can use the **Legal entity overrides** section to specify the companies that the dimension should be suspended for, the owner, and the period when the dimension is active.</span></span>

## <a name="deleting-financial-dimensions"></a><span data-ttu-id="9d63c-154">Odstranění finančních dimenzí</span><span class="sxs-lookup"><span data-stu-id="9d63c-154">Deleting financial dimensions</span></span>

<span data-ttu-id="9d63c-155">V zájmu udržení referenční integrity dat lze finanční dimenze v řídkých případech odstranit.</span><span class="sxs-lookup"><span data-stu-id="9d63c-155">To help maintain referential integrity of the data, financial dimensions can rarely be deleted.</span></span> <span data-ttu-id="9d63c-156">Při pokusu o odstranění finanční dimenze jsou vyhodnocena následující kritéria:</span><span class="sxs-lookup"><span data-stu-id="9d63c-156">If you try to delete a financial dimension, the following criteria are evaluated:</span></span>

- <span data-ttu-id="9d63c-157">Byla finanční dimenze použita pro zaúčtované a nezaúčtované transakce nebo jakýkoli typ kombinace hodnot dimenzí?</span><span class="sxs-lookup"><span data-stu-id="9d63c-157">Has the financial dimension been used on any posted or unposted transactions, or any type of dimension value combination?</span></span>
- <span data-ttu-id="9d63c-158">Používá se finanční dimenze v nějaké aktivní účetní struktuře, struktuře rozšířeného pravidla nebo sadě finančních dimenzí?</span><span class="sxs-lookup"><span data-stu-id="9d63c-158">Is the financial dimension used in any active account structure, advanced rule structure, or financial dimension set?</span></span>
- <span data-ttu-id="9d63c-159">Je finanční dimenze součástí výchozího formátu integrace finanční dimenze?</span><span class="sxs-lookup"><span data-stu-id="9d63c-159">Is the financial dimension part of a default financial dimension integration format?</span></span>
- <span data-ttu-id="9d63c-160">Byla finanční dimenze nastavena jako výchozí dimenze?</span><span class="sxs-lookup"><span data-stu-id="9d63c-160">Has the financial dimension been set up as a default dimension?</span></span>

<span data-ttu-id="9d63c-161">Pokud je odpověď na některou z těchto otázek kladná, finanční dimenzi nelze odstranit.</span><span class="sxs-lookup"><span data-stu-id="9d63c-161">If any of the criteria are met, you can't delete the financial dimension.</span></span>


<span data-ttu-id="9d63c-162">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="9d63c-162">For more information, see the following topics:</span></span>
- [<span data-ttu-id="9d63c-163">Definování finančních dimenzí</span><span class="sxs-lookup"><span data-stu-id="9d63c-163">Define financial dimensions</span></span>](tasks/define-financial-dimensions.md)
- [<span data-ttu-id="9d63c-164">Udržování výchozích šablon finančních dimenzí</span><span class="sxs-lookup"><span data-stu-id="9d63c-164">Maintain financial dimension default templates</span></span>](tasks/maintain-financial-dimension-default-templates.md)

