---
title: Kontrola konfigurované komponenty ER zabraňující problémům za běhu
description: Toto téma vysvětluje, jak zkontrolovat konfigurované komponenty elektronického výkaznictví (ER), aby se předešlo problémům za běhu, ke kterým může dojít.
author: NickSelin
manager: AnnBe
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72db7660c07b2f57f8609ab6c14964193e842d75
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688560"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a><span data-ttu-id="19e1c-103">Kontrola konfigurované komponenty ER zabraňující problémům za běhu</span><span class="sxs-lookup"><span data-stu-id="19e1c-103">Inspect the configured ER component to prevent runtime issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="19e1c-104">Každá konfigurovaná komponenta pro [formátování](general-electronic-reporting.md#FormatComponentOutbound) a [mapování modelu](general-electronic-reporting.md#data-model-and-model-mapping-components) [elektronického výkaznictví (ER)](general-electronic-reporting.md) může projít [ověřením platnosti](er-fillable-excel.md#validate-an-er-format) v době návrhu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-104">Every configured [Electronic reporting (ER)](general-electronic-reporting.md) [format](general-electronic-reporting.md#FormatComponentOutbound) and [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component can be [validated](er-fillable-excel.md#validate-an-er-format) at design time.</span></span> <span data-ttu-id="19e1c-105">Během tohoto ověřování se provádí kontrola konzistence, která pomáhá předcházet výskytu problémů za běhu, jako jsou chyby spuštění a snížení výkonu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-105">During this validation, a consistency check is done to help prevent runtime issues that might occur, such as execution errors and performance degradation.</span></span> <span data-ttu-id="19e1c-106">U každého nalezeného problému je uvedena cesta k problematickému prvku.</span><span class="sxs-lookup"><span data-stu-id="19e1c-106">For every issue that is found, the path of a problematic element is provided.</span></span> <span data-ttu-id="19e1c-107">U některých problémů je k dispozici automatická oprava.</span><span class="sxs-lookup"><span data-stu-id="19e1c-107">For some issues, an automatic fix is available.</span></span>

<span data-ttu-id="19e1c-108">Ve výchozím nastavení se v následujících případech ověření automaticky použije u konfigurace ER, která obsahuje dříve zmíněné komponenty ER:</span><span class="sxs-lookup"><span data-stu-id="19e1c-108">By default, the validation is automatically applied in the following cases for an ER configuration that contains the previously mentioned ER components:</span></span>

- <span data-ttu-id="19e1c-109">[Importujte](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) novou [verzi](general-electronic-reporting.md#component-versioning) konfigurace ER do vaší instance Microsoftu Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="19e1c-109">You [import](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) a new [version](general-electronic-reporting.md#component-versioning) of an ER configuration into your instance of Microsoft Dynamics 365 Finance.</span></span>
- <span data-ttu-id="19e1c-110">Změňte [stav](general-electronic-reporting.md#component-versioning) upravitelné konfigurace ER z hodnoty **Koncept** na **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-110">You change the [status](general-electronic-reporting.md#component-versioning) of the editable ER configuration from **Draft** to **Completed**.</span></span>
- <span data-ttu-id="19e1c-111">[Přeneste změny](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) do upravitelné konfigurace ER použitím nové základní verze.</span><span class="sxs-lookup"><span data-stu-id="19e1c-111">You [rebase](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) an editable ER configuration by applying a new base version.</span></span>

<span data-ttu-id="19e1c-112">Toto ověření můžete explicitně spustit.</span><span class="sxs-lookup"><span data-stu-id="19e1c-112">You can explicitly run this validation.</span></span> <span data-ttu-id="19e1c-113">Vyberte jednu z následujících tří možností a postupujte podle uvedených kroků:</span><span class="sxs-lookup"><span data-stu-id="19e1c-113">Select one of the following three options, and follow the steps that are provided:</span></span>

- <span data-ttu-id="19e1c-114">Možnost 1:</span><span class="sxs-lookup"><span data-stu-id="19e1c-114">Option 1:</span></span>

    1. <span data-ttu-id="19e1c-115">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-115">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="19e1c-116">Ve stromu konfigurací v levém podokně vyberte požadovanou konfiguraci ER, která obsahuje komponentu formátu nebo mapování modelu ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-116">In the configurations tree in the left pane, select the desired ER configuration that contains the ER format or ER model mapping component.</span></span>
    3. <span data-ttu-id="19e1c-117">Na pevné záložce **Verze** vyberte požadovanou verzi vybrané konfigurace ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-117">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="19e1c-118">V podokně Akce klikněte na možnost **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-118">On the Action Pane, select **Validate**.</span></span>

- <span data-ttu-id="19e1c-119">Možnost 2, pro formát ER:</span><span class="sxs-lookup"><span data-stu-id="19e1c-119">Option 2, for an ER format:</span></span>

    1. <span data-ttu-id="19e1c-120">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-120">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="19e1c-121">Ve stromu konfigurací v levém podokně vyberte požadovanou konfiguraci ER, která obsahuje komponentu formátu ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-121">In the configurations tree in the left pane, select the desired ER configuration that contains the ER format component.</span></span>
    3. <span data-ttu-id="19e1c-122">Na pevné záložce **Verze** vyberte požadovanou verzi vybrané konfigurace ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-122">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="19e1c-123">V podokně akcí zvolte **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-123">On the Action Pane, select **Designer**.</span></span>
    5. <span data-ttu-id="19e1c-124">Na stránce **Návrhář formátu** v podokně akcí vyberte **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-124">On the **Format designer** page, on the Action Pane, select **Validate**.</span></span>

- <span data-ttu-id="19e1c-125">Možnost 3, pro mapování modelu ER:</span><span class="sxs-lookup"><span data-stu-id="19e1c-125">Option 3, for an ER model mapping:</span></span>

    1. <span data-ttu-id="19e1c-126">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-126">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="19e1c-127">Ve stromu konfigurací v levém podokně vyberte požadovanou konfiguraci ER, která obsahuje komponentu mapování modelu ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-127">In the configurations tree in the left pane, select the desired ER configuration that contains the ER model mapping component.</span></span>
    3. <span data-ttu-id="19e1c-128">Na pevné záložce **Verze** vyberte požadovanou verzi vybrané konfigurace ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-128">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="19e1c-129">V podokně akcí zvolte **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-129">On the Action Pane, select **Designer**.</span></span>
    5. <span data-ttu-id="19e1c-130">Na stránce **Mapování modelu na zdroj dat** v podokně Akce vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-130">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>
    6. <span data-ttu-id="19e1c-131">Na stránce **Návrhář mapování modelu** v podokně Akce vyberte možnost **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-131">On the **Model mapping designer** page, on the Action Pane, select **Validate**.</span></span>

<span data-ttu-id="19e1c-132">Chcete-li přeskočit ověření při importu konfigurace, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="19e1c-132">To skip the validation when the configuration is imported, follow these steps.</span></span>

1. <span data-ttu-id="19e1c-133">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-133">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="19e1c-134">Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-134">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="19e1c-135">Nastavte možnost **Po importu ověřit konfiguraci** na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-135">Set the **Validate the configuration after importing** option to **No**.</span></span>

<span data-ttu-id="19e1c-136">Chcete-li přeskočit ověření, když je změněn stav verze nebo základ, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="19e1c-136">To skip the validation when the version's status is changed or rebased, follow these steps.</span></span>

1. <span data-ttu-id="19e1c-137">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-137">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="19e1c-138">Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-138">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="19e1c-139">Nastavte možnost **Přeskočit ověření při změně stavu konfigurace a základu** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-139">Set the **Skip validation at configuration's status change and rebase** option to **Yes**.</span></span>

<span data-ttu-id="19e1c-140">ER používá k seskupení inspekcí kontroly konzistence následující kategorie:</span><span class="sxs-lookup"><span data-stu-id="19e1c-140">ER uses the following categories to group consistency check inspections:</span></span>

- <span data-ttu-id="19e1c-141">**Proveditelnost** - Inspekce, které detekují kritické problémy, ke kterým by za běhu mohlo dojít.</span><span class="sxs-lookup"><span data-stu-id="19e1c-141">**Executability** – Inspections that detect critical issues that might happen at runtime.</span></span> <span data-ttu-id="19e1c-142">Tyto problémy jsou většinou na úrovni **Chyba**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-142">These issues are mostly at an **Error** level.</span></span> 
- <span data-ttu-id="19e1c-143">**Výkon** - Inspekce, které detekují problémy, které by mohly způsobit neefektivní provádění konfigurovaných komponent ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-143">**Performance** – Inspections that detect issues that might cause inefficient execution of configured ER components.</span></span> <span data-ttu-id="19e1c-144">Tyto problémy jsou většinou na úrovni **Upozornění**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-144">These issues are mostly at a **Warning** level.</span></span>
- <span data-ttu-id="19e1c-145">**Integrita dat** - Inspekce, které detekují problémy, které by mohly způsobit ztrátu dat nebo problémy běhového prostředí.</span><span class="sxs-lookup"><span data-stu-id="19e1c-145">**Data integrity** – Inspections that detect issues that might cause data loss or runtime issues.</span></span> <span data-ttu-id="19e1c-146">Tyto problémy jsou většinou na úrovni **Upozornění**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-146">These issues are mostly at a **Warning** level.</span></span>

## <a name="list-of-inspections"></a><span data-ttu-id="19e1c-147">Seznam inspekcí</span><span class="sxs-lookup"><span data-stu-id="19e1c-147">List of inspections</span></span>

<span data-ttu-id="19e1c-148">Následující tabulka poskytuje přehled inspekcí, které ER poskytuje.</span><span class="sxs-lookup"><span data-stu-id="19e1c-148">The following table provides an overview of the inspections that ER provides.</span></span> <span data-ttu-id="19e1c-149">Další informace o těchto inspekcích získáte pomocí odkazů v prvním sloupci, kterými přejdete na příslušné části tohoto tématu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-149">For more information about these inspections, use the links in the first column to go to the relevant sections of this topic.</span></span> <span data-ttu-id="19e1c-150">Tyto oddíly vysvětlují typy komponent, u kterých ER poskytuje kontroly, a návod na rekonfiguraci komponent ER, abyste zabránili problémům.</span><span class="sxs-lookup"><span data-stu-id="19e1c-150">Those sections explain the types of components that ER provides inspections for and how you can reconfigure ER components to help prevent issues.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="19e1c-151">Jméno</span><span class="sxs-lookup"><span data-stu-id="19e1c-151">Name</span></span></th>
<th><span data-ttu-id="19e1c-152">Kategorie</span><span class="sxs-lookup"><span data-stu-id="19e1c-152">Category</span></span></th>
<th><span data-ttu-id="19e1c-153">Úroveň</span><span class="sxs-lookup"><span data-stu-id="19e1c-153">Level</span></span></th>
<th><span data-ttu-id="19e1c-154">Zpráva</span><span class="sxs-lookup"><span data-stu-id="19e1c-154">Message</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="19e1c-155"><a href='#i1'>Převod typu</a></span><span class="sxs-lookup"><span data-stu-id="19e1c-155"><a href='#i1'>Type conversion</a></span></span></td>
<td><span data-ttu-id="19e1c-156">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="19e1c-156">Executability</span></span></td>
<td><span data-ttu-id="19e1c-157">Chyba</span><span class="sxs-lookup"><span data-stu-id="19e1c-157">Error</span></span></td>
<td>
<p><span data-ttu-id="19e1c-158">Nelze převést výraz typu &lt;typ&gt; na pole typu &lt;typ&gt;.</span><span class="sxs-lookup"><span data-stu-id="19e1c-158">Cannot convert expression of type &lt;type&gt; to field of type &lt;type&gt;.</span></span></p>
<p><span data-ttu-id="19e1c-159"><b>Chyba za běhu:</b> Výjimka typu</span><span class="sxs-lookup"><span data-stu-id="19e1c-159"><b>Runtime error:</b> Exception of type</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="19e1c-160"><a href='#i2'>Kompatibilita typů</a></span><span class="sxs-lookup"><span data-stu-id="19e1c-160"><a href='#i2'>Type compatibility</a></span></span></td>
<td><span data-ttu-id="19e1c-161">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="19e1c-161">Executability</span></span></td>
<td><span data-ttu-id="19e1c-162">Chyba</span><span class="sxs-lookup"><span data-stu-id="19e1c-162">Error</span></span></td>
<td>
<p><span data-ttu-id="19e1c-163">Konfigurovaný výraz nelze použít jako vazbu aktuálního prvku formátu ke zdroji dat, protože tento výraz vrací hodnotu datového typu &lt;typ&gt;, tedy mimo rámec datových typů, které jsou podporovány aktuálním prvkem formátu typu &lt;typ&gt;.</span><span class="sxs-lookup"><span data-stu-id="19e1c-163">The configured expression cannot be used as the binding of the current format element to a data source as this expression returns value of the data type &lt;type&gt; that is beyond the scope of data types that are supported by the current format element of type &lt;type&gt;.</span></span></p>
<p><span data-ttu-id="19e1c-164"><b>Chyba za běhu:</b> Výjimka typu</span><span class="sxs-lookup"><span data-stu-id="19e1c-164"><b>Runtime error:</b> Exception of type</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="19e1c-165"><a href='#i3'>Chybějící konfigurační prvek</a></span><span class="sxs-lookup"><span data-stu-id="19e1c-165"><a href='#i3'>Missing configuration element</a></span></span></td>
<td><span data-ttu-id="19e1c-166">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="19e1c-166">Executability</span></span></td>
<td><span data-ttu-id="19e1c-167">Chyba</span><span class="sxs-lookup"><span data-stu-id="19e1c-167">Error</span></span></td>
<td>
<p><span data-ttu-id="19e1c-168">Cesta nenalezena: &lt;cesta&gt;.</span><span class="sxs-lookup"><span data-stu-id="19e1c-168">Path not found &lt;path&gt;.</span></span></p>
<p><span data-ttu-id="19e1c-169"><b>Chyba za běhu:</b> Prvek konfigurace &lt; cesta&gt; nenalezen</span><span class="sxs-lookup"><span data-stu-id="19e1c-169"><b>Runtime error:</b> Element of the configuration &lt;path&gt; not found</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="19e1c-170"><a href='#i4'>Spustitelnost výrazu s funkcí FILTER</a></span><span class="sxs-lookup"><span data-stu-id="19e1c-170"><a href='#i4'>Executability of an expression with FILTER function</a></span></span></td>
<td><span data-ttu-id="19e1c-171">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="19e1c-171">Executability</span></span></td>
<td><span data-ttu-id="19e1c-172">Chyba</span><span class="sxs-lookup"><span data-stu-id="19e1c-172">Error</span></span></td>
<td>
<p><span data-ttu-id="19e1c-173">Výraz seznamu funkce FILTER není dotazovatelný.</span><span class="sxs-lookup"><span data-stu-id="19e1c-173">The list expression of FILTER function is not queryable.</span></span></p>
<p><span data-ttu-id="19e1c-174"><b>Chyba za běhu:</b> Filtrování není podporováno.</span><span class="sxs-lookup"><span data-stu-id="19e1c-174"><b>Runtime error:</b> Filtering is not supported.</span></span> <span data-ttu-id="19e1c-175">Chcete-li získat další podrobnosti o chybě, ověřte konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="19e1c-175">Validate the configuration to get more details about this.</span></span></p>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="19e1c-176"><a href='#i5'>Spustitelnost zdroje dat GROUPBY</a></span><span class="sxs-lookup"><span data-stu-id="19e1c-176"><a href='#i5'>Executability of a GROUPBY data source</a></span></span></td>
<td><span data-ttu-id="19e1c-177">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="19e1c-177">Executability</span></span></td>
<td><span data-ttu-id="19e1c-178">Chyba</span><span class="sxs-lookup"><span data-stu-id="19e1c-178">Error</span></span></td>
<td><span data-ttu-id="19e1c-179">Cesta &lt;cesta&gt; nepodporuje dotazování.</span><span class="sxs-lookup"><span data-stu-id="19e1c-179">Path &lt;path&gt; does not support querying.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19e1c-180">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="19e1c-180">Executability</span></span></td>
<td><span data-ttu-id="19e1c-181">Chyba</span><span class="sxs-lookup"><span data-stu-id="19e1c-181">Error</span></span></td>
<td>
<p><span data-ttu-id="19e1c-182">Seskupení podle funkce nelze provést pomocí dotazu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-182">Group by function cannot be executed with query.</span></span></p>
<p><span data-ttu-id="19e1c-183"><b>Chyba za běhu:</b> Seskupení podle funkce nelze provést pomocí dotazu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-183"><b>Runtime error:</b> Group by function can't be executed with query.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="19e1c-184"><a href='#i6'>Spustitelnost zdroje dat JOIN</a></span><span class="sxs-lookup"><span data-stu-id="19e1c-184"><a href='#i6'>Executability of a JOIN data source</a></span></span></td>
<td><span data-ttu-id="19e1c-185">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="19e1c-185">Executability</span></span></td>
<td><span data-ttu-id="19e1c-186">Chyba</span><span class="sxs-lookup"><span data-stu-id="19e1c-186">Error</span></span></td>
<td>
<p><span data-ttu-id="19e1c-187">Nelze připojit seznam &lt;cesta&gt;, který není filtrem v dotazu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-187">Cannot join a list &lt;path&gt; that is not a filter in query.</span></span></p>
<p><span data-ttu-id="19e1c-188"><b>Chyba za běhu:</b> Funkce datového zdroje JOIN by měla být výrazem filtru vypočítaného pole, který byl nesprávně volán.</span><span class="sxs-lookup"><span data-stu-id="19e1c-188"><b>Runtime error:</b> Function Joined datasource should be a filter expression calculated field has been incorrectly called.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="19e1c-189"><a href='#i7'>Je vhodnější funkce FILTER nebo WHERE?</a></span><span class="sxs-lookup"><span data-stu-id="19e1c-189"><a href='#i7'>Preferability of FILTER vs WHERE function</a></span></span></td>
<td><span data-ttu-id="19e1c-190">Výkonnost</span><span class="sxs-lookup"><span data-stu-id="19e1c-190">Performance</span></span></td>
<td><span data-ttu-id="19e1c-191">Upozornění</span><span class="sxs-lookup"><span data-stu-id="19e1c-191">Warning</span></span></td>
<td><span data-ttu-id="19e1c-192">Použití funkce FILTER ve výrazu je z hlediska výkonu vhodnější než použití funkce WHERE.</span><span class="sxs-lookup"><span data-stu-id="19e1c-192">Using FILTER function for the expression is preferable than WHERE from the performance perspective.</span></span> <span data-ttu-id="19e1c-193">Vyberte možnost Opravit, aby došlo k automatickému nahrazení.</span><span class="sxs-lookup"><span data-stu-id="19e1c-193">Select Fix to replace it automatically.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19e1c-194"><a href='#i8'>Je vhodnější funkce ALLITEMSQUERY nebo ALLITEMS?</a></span><span class="sxs-lookup"><span data-stu-id="19e1c-194"><a href='#i8'>Preferability of ALLITEMSQUERY vs ALLITEMS function</a></span></span></td>
<td><span data-ttu-id="19e1c-195">Výkonnost</span><span class="sxs-lookup"><span data-stu-id="19e1c-195">Performance</span></span></td>
<td><span data-ttu-id="19e1c-196">Upozornění</span><span class="sxs-lookup"><span data-stu-id="19e1c-196">Warning</span></span></td>
<td><span data-ttu-id="19e1c-197">Použití funkce ALLITEMSQUERY ve výrazu je z hlediska výkonu vhodnější než použití funkce ALLITEMS.</span><span class="sxs-lookup"><span data-stu-id="19e1c-197">Using ALLITEMSQUERY function for the expression is preferable than ALLITEMS from the performance perspective.</span></span> <span data-ttu-id="19e1c-198">Vyberte možnost Opravit, aby došlo k automatickému nahrazení.</span><span class="sxs-lookup"><span data-stu-id="19e1c-198">Select Fix to replace it automatically.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19e1c-199"><a href='#i9'>Možnost výskytů prázdného seznamu</a></span><span class="sxs-lookup"><span data-stu-id="19e1c-199"><a href='#i9'>Consideration of empty list cases</a></span></span></td>
<td><span data-ttu-id="19e1c-200">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="19e1c-200">Executability</span></span></td>
<td><span data-ttu-id="19e1c-201">Upozornění</span><span class="sxs-lookup"><span data-stu-id="19e1c-201">Warning</span></span></td>
<td>
<p><span data-ttu-id="19e1c-202">Seznam &lt;cesta&gt; nemá žádnou kontrolu výskytu prázdného seznamu, což může způsobit chybu za běhu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-202">List &lt;path&gt; does not have any check for empty list case, it can result an error at run time.</span></span> <span data-ttu-id="19e1c-203">Přidejte kontrolu výskytu prázdného seznamu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-203">Add a check for empty list case.</span></span></p>
<p><span data-ttu-id="19e1c-204"><b>Chyba za běhu:</b> Seznam je prázdný v cestě &lt;cesta&gt;</span><span class="sxs-lookup"><span data-stu-id="19e1c-204"><b>Runtime error:</b> List is empty at &lt;path&gt;</span></span></p>
<p><span data-ttu-id="19e1c-205"><b><a href='#i9a'>Potenciální problém</a> :</b> Řádek se naplní jednou, zatímco zdroj dat, ze kterého je naplněn, obsahuje více záznamů</span><span class="sxs-lookup"><span data-stu-id="19e1c-205"><b><a href='#i9a'>Potential issue</a>:</b> Line is getting populated once while a data source it is populated from contains multiple records</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="19e1c-206"><a href='#i10'>Spustitelnost výrazu s funkcí FILTER (použití mezipaměti)</a></span><span class="sxs-lookup"><span data-stu-id="19e1c-206"><a href='#i10'>Executability of an expression with FILTER function (caching)</a></span></span></td>
<td><span data-ttu-id="19e1c-207">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="19e1c-207">Executability</span></span></td>
<td><span data-ttu-id="19e1c-208">Chyba</span><span class="sxs-lookup"><span data-stu-id="19e1c-208">Error</span></span></td>
<td>
<p><span data-ttu-id="19e1c-209">Funkci FILTER nelze použít na vybraný typ zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="19e1c-209">FILTER function cannot be applied to the selected type of data source.</span></span> <span data-ttu-id="19e1c-210">Zdroj dat typu Záznamy tabulky je použitelný pouze v případě, že není uložen do mezipaměti a nemá žádné ručně přidané vnořené zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="19e1c-210">A data source of the Table records type is applicable only when it is not cached and has no manually added nested data sources.</span></span></p>
<p><span data-ttu-id="19e1c-211"><b>Chyba za běhu:</b> Filtrování není podporováno.</span><span class="sxs-lookup"><span data-stu-id="19e1c-211"><b>Runtime error:</b> Filtering is not supported.</span></span> <span data-ttu-id="19e1c-212">Chcete-li získat další podrobnosti o chybě, ověřte konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="19e1c-212">Validate the configuration to get more details about this.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="19e1c-213"><a href='#i11'>Chybějící vazba</a></span><span class="sxs-lookup"><span data-stu-id="19e1c-213"><a href='#i11'>Missing binding</a></span></span></td>
<td><span data-ttu-id="19e1c-214">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="19e1c-214">Executability</span></span></td>
<td><span data-ttu-id="19e1c-215">Upozornění</span><span class="sxs-lookup"><span data-stu-id="19e1c-215">Warning</span></span></td>
<td>
<p><span data-ttu-id="19e1c-216">Cesta &lt;cesta&gt; nemá žádnou vazbu na žádný zdroj dat při používání mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-216">Path &lt;path&gt; has no binding to any datasource in using model's mapping.</span></span></p>
<p><span data-ttu-id="19e1c-217"><b>Chyba za běhu:</b> Cesta &lt;cesta&gt; není vázána</span><span class="sxs-lookup"><span data-stu-id="19e1c-217"><b>Runtime error:</b> Path &lt;path&gt; is not bound</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="19e1c-218"><a href='#i12'>Nepropojená šablona</a></span><span class="sxs-lookup"><span data-stu-id="19e1c-218"><a href='#i12'>Not linked template</a></span></span></td>
<td><span data-ttu-id="19e1c-219">Integrita dat</span><span class="sxs-lookup"><span data-stu-id="19e1c-219">Data integrity</span></span></td>
<td><span data-ttu-id="19e1c-220">Upozornění</span><span class="sxs-lookup"><span data-stu-id="19e1c-220">Warning</span></span></td>
<td><span data-ttu-id="19e1c-221">Soubor &lt;název&gt; není propojen s žádnými souborovými komponentami a bude odstraněn po změně stavu verze konfigurace.</span><span class="sxs-lookup"><span data-stu-id="19e1c-221">File &lt;name&gt; is linked to no file components and will be removed after changing status of configuration version.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="19e1c-222"><a href='#i13'>Nesynchronizovaný formát</a></span><span class="sxs-lookup"><span data-stu-id="19e1c-222"><a href='#i13'>Not synced format</a></span></span></td>
<td><span data-ttu-id="19e1c-223">Integrita dat</span><span class="sxs-lookup"><span data-stu-id="19e1c-223">Data integrity</span></span></td>
<td><span data-ttu-id="19e1c-224">Upozornění</span><span class="sxs-lookup"><span data-stu-id="19e1c-224">Warning</span></span></td>
<td><span data-ttu-id="19e1c-225">Definovaný název &lt;název komponenty&gt; neexistuje v listu aplikace Excel &lt;název listu&gt;</span><span class="sxs-lookup"><span data-stu-id="19e1c-225">Defined name &lt;component name&gt; does not exist in Excel sheet &lt;sheet name&gt;</span></span></td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a><span data-ttu-id="19e1c-226">Převod typu</span><span class="sxs-lookup"><span data-stu-id="19e1c-226">Type conversion</span></span>

<span data-ttu-id="19e1c-227">ER kontroluje, zda je datový typ pole datového modelu kompatibilní s datovým typem výrazu, který je konfigurován jako vazba daného pole.</span><span class="sxs-lookup"><span data-stu-id="19e1c-227">ER checks whether the data type of a data model field is compatible with the data type of an expression that is configured as the binding of that field.</span></span> <span data-ttu-id="19e1c-228">Pokud jsou datové typy nekompatibilní, dojde v návrháři mapování modelu ER k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="19e1c-228">If the data types are incompatible, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="19e1c-229">Zpráva, kterou obdržíte, uvádí, že ER nemůže převést výraz typu A na pole typu B.</span><span class="sxs-lookup"><span data-stu-id="19e1c-229">The message that you receive states that ER can't convert an expression of type A to a field of type B.</span></span>

<span data-ttu-id="19e1c-230">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="19e1c-230">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="19e1c-231">Začněte konfigurovat datový model ER a komponenty mapování modelu ER současně.</span><span class="sxs-lookup"><span data-stu-id="19e1c-231">Start to configure the ER data model and the ER model mapping components simultaneously.</span></span>
2. <span data-ttu-id="19e1c-232">Ve stromu datového modelu přidejte pole s názvem **X** a jako datový typ vyberte **Celé číslo**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-232">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>

    ![Pole X a datový typ Celé číslo byly přidány do stromu datového modelu na stránce Datový model](./media/er-components-inspections-01.png)

3. <span data-ttu-id="19e1c-234">V podokně zdrojů dat mapování modelu přidejte zdroj dat typu **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-234">In the model mapping data sources pane, add a data source of the **Calculated field** type.</span></span>
4. <span data-ttu-id="19e1c-235">Pojmenujte nový zdroj dat jako **Y** a konfigurujte jej tak, aby obsahoval výraz `INTVALUE(100)`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-235">Name the new data source **Y**, and configure it so that it contains the expression `INTVALUE(100)`.</span></span>
5. <span data-ttu-id="19e1c-236">Navažte **X** na **Y**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-236">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="19e1c-237">V návrháři datového modelu změňte datový typ pole **X** z hodnoty **Celé číslo** na **Int64**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-237">In the data model designer, change the data type of the **X** field from **Integer** to **Int64**.</span></span>
7. <span data-ttu-id="19e1c-238">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu mapování modelu na stránce **Návrhář mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-238">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![ověřování upravitelné komponenty mapování modelu na stránce Návrhář mapování modelu](./media/er-components-inspections-01.gif)

8. <span data-ttu-id="19e1c-240">Výběrem příkazu **Ověřit** zkontrolujete komponentu mapování modelu vybrané konfigurace ER na stránce **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-240">Select **Validate** to inspect the model mapping component of the selected ER configuration on the **Configurations** page.</span></span>

    ![Ověření komponenty mapování modelu na stránce Konfigurace](./media/er-components-inspections-01a.png)

9. <span data-ttu-id="19e1c-242">Všimněte si, že dojde k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="19e1c-242">Notice that a validation error occurs.</span></span> <span data-ttu-id="19e1c-243">Zpráva uvádí, že hodnotu typu **Celé číslo**, kterou vrátí výraz `INTVALUE(100)` zdroje dat **Y**, nelze uložit do pole datového modelu **X** typu **Int64**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-243">The message states that the value of the **Integer** type that the `INTVALUE(100)` expression of the **Y** data source returns can't be stored in the **X** data model field of the **Int64** type.</span></span>

<span data-ttu-id="19e1c-244">Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění a výběrem příkazu **Spustit** spustíte formát, který má konfigurováno použití mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-244">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![Chyby za běhu na stránce Návrhář formátu](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="19e1c-246">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-246">Automatic resolution</span></span>

<span data-ttu-id="19e1c-247">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="19e1c-247">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="19e1c-248">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-248">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="19e1c-249">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="19e1c-249">Option 1</span></span>

<span data-ttu-id="19e1c-250">Aktualizujte strukturu datového modelu změnou datového typu pole datového modelu tak, aby odpovídal datovému typu výrazu, který je konfigurován pro vazbu daného pole.</span><span class="sxs-lookup"><span data-stu-id="19e1c-250">Update the data model structure by changing the data type of the data model field so that it matches the data type of the expression that is configured for the binding of that field.</span></span> <span data-ttu-id="19e1c-251">V předchozím příkladu musíte datový typ pole **X** změnit zpět na **Celé číslo**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-251">For the preceding example, the data type of the **X** field must be changed back to **Integer**.</span></span>

#### <a name="option-2"></a><span data-ttu-id="19e1c-252">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="19e1c-252">Option 2</span></span>

<span data-ttu-id="19e1c-253">Aktualizujte mapování modelu změnou výrazu zdroje dat, který je svázán s polem datového modelu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-253">Update the model mapping by changing the expression of the data source that is bound with the data model field.</span></span> <span data-ttu-id="19e1c-254">V předchozím příkladu musíte změnit výraz zdroje dat **Y** na `INT64VALUE(100)`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-254">For the preceding example, the expression of the **Y** data source must be changed to `INT64VALUE(100)`.</span></span>

## <a name="type-compatibility"></a><a id="i2"></a><span data-ttu-id="19e1c-255">Kompatibilita typů</span><span class="sxs-lookup"><span data-stu-id="19e1c-255">Type compatibility</span></span>

<span data-ttu-id="19e1c-256">ER kontroluje, zda je datový typ prvku formátu kompatibilní s datovým typem výrazu, který je konfigurován jako vazba daného prvku formátu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-256">ER checks whether the data type of a format element is compatible with the data type of an expression that is configured as the binding of that format element.</span></span> <span data-ttu-id="19e1c-257">Pokud jsou datové typy nekompatibilní, dojde v návrháři operací ER k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="19e1c-257">If the data types are incompatible, a validation error occurs in the ER Operations designer.</span></span> <span data-ttu-id="19e1c-258">Zpráva, kterou obdržíte, říká, že konfigurovaný výraz nelze použít jako vazbu aktuálního prvku formátu ke zdroji dat, protože tento výraz vrací hodnotu datového typu A, tedy mimo rámec datových typů, které jsou podporovány aktuálním prvkem formátu typu B.</span><span class="sxs-lookup"><span data-stu-id="19e1c-258">The message that you receive states that the configured expression can't be used as the binding of the current format element to a data source, because the expression returns a value of data type A that is beyond the scope of the data types that are supported by the current format element of type B.</span></span>

<span data-ttu-id="19e1c-259">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="19e1c-259">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="19e1c-260">Začněte konfigurovat datový model ER a komponenty formátu ER současně.</span><span class="sxs-lookup"><span data-stu-id="19e1c-260">Start to configure the ER data model and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="19e1c-261">Ve stromu datového modelu přidejte pole s názvem **X** a jako datový typ vyberte **Celé číslo**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-261">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>
3. <span data-ttu-id="19e1c-262">Ve stromu struktury formátu přidejte prvek formátu typu **Číslo**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-262">In the format structure tree, add a format element of the **Numeric** type.</span></span>
4. <span data-ttu-id="19e1c-263">Pojmenujte nový prvek formátu jako **Y**. V poli **Číselný typ** vyberte jako datový typ hodnotu **Celé číslo**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-263">Name the new format element **Y**. In the **Numeric type** field, select **Integer** as the data type.</span></span>
5. <span data-ttu-id="19e1c-264">Navažte **X** na **Y**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-264">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="19e1c-265">Ve stromu struktury formátu změňte datový typ prvku formátu **Y** z hodnoty **Celé číslo** na **Int64**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-265">In the format structure tree, change the data type of the **Y** format element from **Integer** to **Int64**.</span></span>
7. <span data-ttu-id="19e1c-266">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu formátu na stránce **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-266">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![Ověření kompatibility typů na stránce Návrhář formátu](./media/er-components-inspections-02.gif)

8. <span data-ttu-id="19e1c-268">Všimněte si, že dojde k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="19e1c-268">Notice that a validation error occurs.</span></span> <span data-ttu-id="19e1c-269">Zpráva uvádí, že konfigurovaný výraz může přijmout pouze hodnoty typu **Int64**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-269">The message states that the configured expression can accept only **Int64** values.</span></span> <span data-ttu-id="19e1c-270">Proto nelze hodnotu pole datového modelu **X** typu **Celé číslo** zadat do prvku formátu **Y**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-270">Therefore, the value of the **X** data model field of the **Integer** type can't be entered in the **Y** format element.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="19e1c-271">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-271">Automatic resolution</span></span>

<span data-ttu-id="19e1c-272">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="19e1c-272">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="19e1c-273">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-273">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="19e1c-274">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="19e1c-274">Option 1</span></span>

<span data-ttu-id="19e1c-275">Aktualizujte strukturu formátu změnou datového typu prvku formátu **Číslo** tak, aby odpovídal datovému typu výrazu, který je konfigurován pro vazbu tohoto prvku.</span><span class="sxs-lookup"><span data-stu-id="19e1c-275">Update the format structure by changing the data type of the **Numeric** format element so that it matches the data type of the expression that is configured for the binding of that element.</span></span> <span data-ttu-id="19e1c-276">V předchozím příkladu musíte datový typ **Číslo** prvku formátu **X** změnit zpět **Celé číslo**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-276">In the preceding example, the **Numeric type** value of the **X** format element must be changed back to **Integer**.</span></span>

#### <a name="option-2"></a><span data-ttu-id="19e1c-277">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="19e1c-277">Option 2</span></span>

<span data-ttu-id="19e1c-278">Aktualizujte mapování formátu prvku formátu **X** změnou výrazu z `model.X` na `INT64VALUE(model.X)`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-278">Update the format mapping of the **X** format element by changing the expression from `model.X` to `INT64VALUE(model.X)`.</span></span>

## <a name="missing-configuration-element"></a><a id="i3"></a><span data-ttu-id="19e1c-279">Chybějící konfigurační prvek</span><span class="sxs-lookup"><span data-stu-id="19e1c-279">Missing configuration element</span></span>

<span data-ttu-id="19e1c-280">ER zkontroluje, zda vazební výrazy obsahují pouze zdroje dat, které jsou konfigurovány v upravitelné komponentě ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-280">ER checks whether the binding expressions contain only data sources that are configured in the editable ER component.</span></span> <span data-ttu-id="19e1c-281">U každé vazby, která obsahuje zdroj dat, který chybí v upravitelné komponentě ER, dojde k chybě ověření v návrháři operací ER nebo návrháři mapování modelu ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-281">For every binding that contains a data source that is missing in the editable ER component, a validation error occurs in the ER Operations designer or the ER model mapping designer.</span></span>

<span data-ttu-id="19e1c-282">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="19e1c-282">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="19e1c-283">Začněte konfigurovat datový model ER a komponenty mapování modelu ER současně.</span><span class="sxs-lookup"><span data-stu-id="19e1c-283">Start to configure the ER data model and the ER model mapping components simultaneously.</span></span>
2. <span data-ttu-id="19e1c-284">Ve stromu datového modelu přidejte pole s názvem **X** a jako datový typ vyberte **Celé číslo**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-284">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>

    ![Strom datového modelu s polem X a datovým typem Celé číslo na stránce Datový model](./media/er-components-inspections-01.png)

3. <span data-ttu-id="19e1c-286">V podokně zdrojů dat mapování modelu přidejte zdroj dat typu **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-286">In the model mapping data sources pane, add a data source of the **Calculated field** type.</span></span>
4. <span data-ttu-id="19e1c-287">Pojmenujte nový zdroj dat jako **Y** a konfigurujte jej tak, aby obsahoval výraz `INTVALUE(100)`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-287">Name the new data source **Y**, and configure it so that it contains the expression `INTVALUE(100)`.</span></span>
5. <span data-ttu-id="19e1c-288">Navažte **X** na **Y**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-288">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="19e1c-289">V návrháři mapování modelu v podokně zdroje dat odstraňte zdroj dat **Y**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-289">In the model mapping designer, in the data sources pane, delete the **Y** data source.</span></span>
7. <span data-ttu-id="19e1c-290">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu mapování modelu na stránce **Návrhář mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-290">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![kontrola upravitelné komponenty mapování modelu ER na stránce Návrhář mapování modelu](./media/er-components-inspections-03.gif)

8. <span data-ttu-id="19e1c-292">Všimněte si, že dojde k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="19e1c-292">Notice that a validation error occurs.</span></span> <span data-ttu-id="19e1c-293">Zpráva uvádí, že vazba pole datového modelu **X** obsahuje cestu, která odkazuje na zdroj dat **Y**, ale tento zdroj dat nebyl nalezen.</span><span class="sxs-lookup"><span data-stu-id="19e1c-293">The message states that the binding of the **X** data model field contains the path that refers to the **Y** data source, but this data source isn't found.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="19e1c-294">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-294">Automatic resolution</span></span>

<span data-ttu-id="19e1c-295">Výběrem příkazu **Odpojit** automaticky opravíte tento problém odstraněním vazby na chybějící zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="19e1c-295">Select **Unbind** to automatically fix this issue by removing the missing data source binding.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="19e1c-296">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-296">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="19e1c-297">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="19e1c-297">Option 1</span></span>

<span data-ttu-id="19e1c-298">Odpojte pole datového modelu **X**, aby přestalo odkazovat na neexistující zdroj dat **Y**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-298">Unbind the **X** data model field to stop referring to the nonexistent **Y** data source.</span></span>

#### <a name="option-2"></a><span data-ttu-id="19e1c-299">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="19e1c-299">Option 2</span></span>

<span data-ttu-id="19e1c-300">V podokně zdrojů dat návrháře mapování modelu ER přidejte znovu zdroj dat **Y**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-300">In the data sources pane of the ER model mapping designer, add the **Y** data source again.</span></span>

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a><span data-ttu-id="19e1c-301">Spustitelnost výrazu s funkcí FILTER</span><span class="sxs-lookup"><span data-stu-id="19e1c-301">Executability of an expression with FILTER function</span></span>

<span data-ttu-id="19e1c-302">Integrovaná funkce ER [FILTER](er-functions-list-filter.md) se používá pro přístup k aplikačním tabulkám, pohledům nebo datovým entitám umístěním jediného volání SQL, které získá požadovaná data jako seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="19e1c-302">The built-in [FILTER](er-functions-list-filter.md) ER function is used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="19e1c-303">Zdroj dat typu **Seznam záznamů** se používá jako argument této funkce a určuje zdroj aplikace pro volání.</span><span class="sxs-lookup"><span data-stu-id="19e1c-303">A data source of the **Record list** type is used as an argument of this function and specifies the application source for the call.</span></span> <span data-ttu-id="19e1c-304">ER kontroluje, zda lze navázat přímý dotaz SQL do zdroje dat, na který se odkazuje ve funkci `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-304">ER checks whether a direct SQL query can be established to a data source that is referred to in the `FILTER` function.</span></span> <span data-ttu-id="19e1c-305">Pokud nelze navázat přímý dotaz, dojde v návrháři mapování modelu ER k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="19e1c-305">If a direct query can't be established, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="19e1c-306">Zpráva, kterou obdržíte, uvádí, že výraz ER obsahující funkci `FILTER` nelze spustit za běhu programu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-306">The message that you receive states that the ER expression that includes the `FILTER` function can't be run at runtime.</span></span> 

<span data-ttu-id="19e1c-307">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="19e1c-307">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="19e1c-308">Začněte konfigurací komponenty mapování modelu ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-308">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="19e1c-309">Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-309">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="19e1c-310">Pojmenujte nový zdroj dat jako **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-310">Name the new data source **Vendor**.</span></span> <span data-ttu-id="19e1c-311">V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.</span><span class="sxs-lookup"><span data-stu-id="19e1c-311">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="19e1c-312">Přidejte zdroj dat typu **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-312">Add a data source of the **Calculated field** type.</span></span>
5. <span data-ttu-id="19e1c-313">Pojmenujte nový zdroj dat jako **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `FILTER(Vendor, Vendor.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-313">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum="US-101")`.</span></span>
6. <span data-ttu-id="19e1c-314">Výběrem příkazu **Ověřit** zkontrolujte upravitelnou komponentu mapování modelu na stránce **návrháře mapování modelů** stránku a ověřte, zda výraz `FILTER(Vendor, Vendor.AccountNum="US-101")` ve zdroji dat **Vendor** lze používat v dotazech.</span><span class="sxs-lookup"><span data-stu-id="19e1c-314">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression in the **Vendor** data source can be queried.</span></span>
7. <span data-ttu-id="19e1c-315">Upravte zdroj dat **Vendor** přidáním vnořeného pole typu **Vypočítané pole** a získejte oříznuté číslo účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="19e1c-315">Modify the **Vendor** data source by adding a nested field of the **Calculated field** type to get the trimmed vendor account number.</span></span>
8. <span data-ttu-id="19e1c-316">Pojmenujte nové vnořené pole jako **$AccNumber** a konfigurujte jej tak, aby obsahovalo výraz `TRIM(Vendor.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-316">Name the new nested field **$AccNumber**, and configure it so that it contains the expression `TRIM(Vendor.AccountNum)`.</span></span>
9. <span data-ttu-id="19e1c-317">Výběrem příkazu **Ověřit** zkontrolujte upravitelnou komponentu mapování modelu na stránce **návrháře mapování modelů** stránku a ověřte, zda výraz `FILTER(Vendor, Vendor.AccountNum="US-101")` ve zdroji dat **Vendor** lze používat v dotazech.</span><span class="sxs-lookup"><span data-stu-id="19e1c-317">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression in the **Vendor** data source can be queried.</span></span>

    ![Ověření výrazu lze zkontrolovat dotazem na stránce Návrhář mapování modelů](./media/er-components-inspections-04.gif)

10. <span data-ttu-id="19e1c-319">Všimněte si, že dojde k chybě ověření, protože zdroj dat **Vendor** obsahuje vnořené pole typu **Vypočítané pole**, které neumožňuje přeložit výraz **FilteredVendor** zdroje dat na přímý příkaz SQL.</span><span class="sxs-lookup"><span data-stu-id="19e1c-319">Notice that a validation error occurs, because the **Vendor** data source contains a nested field of the **Calculated field** type that doesn't allow the expression of the **FilteredVendor** data source to be translated to the direct SQL statement.</span></span>

<span data-ttu-id="19e1c-320">Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění a výběrem příkazu **Spustit** spustíte formát, který má konfigurováno použití mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-320">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![Chyby za běhu, ke kterým dochází při spuštění upravitelného formátu na stránce Návrhář formátů](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a><span data-ttu-id="19e1c-322">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-322">Automatic resolution</span></span>

<span data-ttu-id="19e1c-323">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="19e1c-323">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="19e1c-324">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-324">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="19e1c-325">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="19e1c-325">Option 1</span></span>

<span data-ttu-id="19e1c-326">Místo přidání vnořeného pole typu **Vypočítané pole** do zdroje dat **Vendor** přidejte vnořené pole **$AccNumber** do zdroje dat **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `TRIM(FilteredVendor.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-326">Instead of adding a nested field of the **Calculated field** type to the **Vendor** data source, add the **$AccNumber** nested field to the **FilteredVendor** data source, and configure it so that it contains the expression `TRIM(FilteredVendor.AccountNum)`.</span></span> <span data-ttu-id="19e1c-327">Tímto způsobem lze výraz `FILTER(Vendor, Vendor.AccountNum="US-101")` spustit na úrovni SQL a vypočítat vnořené pole **$AccNumber** později.</span><span class="sxs-lookup"><span data-stu-id="19e1c-327">In this way, the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression can be run at the SQL level and calculate the **$AccNumber** nested field afterward.</span></span>

#### <a name="option-2"></a><span data-ttu-id="19e1c-328">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="19e1c-328">Option 2</span></span>

<span data-ttu-id="19e1c-329">Změňte výraz zdroje dat **FilteredVendor** z `FILTER(Vendor, Vendor.AccountNum="US-101")` na `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-329">Change the expression of the **FilteredVendor** data source from `FILTER(Vendor, Vendor.AccountNum="US-101")` to `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span> <span data-ttu-id="19e1c-330">Nedoporučujeme měnit výraz pro tabulku, která obsahuje velké množství dat (transakční tabulka), protože budou načteny všechny záznamy a výběr požadovaných záznamů bude proveden v paměti.</span><span class="sxs-lookup"><span data-stu-id="19e1c-330">We don't recommend that you change the expression for a table that has a large volume of data (transactional table), because all records will be fetched, and selection of the required records will be done in memory.</span></span> <span data-ttu-id="19e1c-331">Tento přístup proto může způsobit špatný výkon.</span><span class="sxs-lookup"><span data-stu-id="19e1c-331">Therefore, this approach can cause poor performance.</span></span> <span data-ttu-id="19e1c-332">Další informace viz část [Funkce WHERE ER](er-functions-list-where.md).</span><span class="sxs-lookup"><span data-stu-id="19e1c-332">For more information, see [WHERE ER function](er-functions-list-where.md).</span></span>

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a><span data-ttu-id="19e1c-333">Spustitelnost zdroje dat GROUPBY</span><span class="sxs-lookup"><span data-stu-id="19e1c-333">Executability of a GROUPBY data source</span></span>

<span data-ttu-id="19e1c-334">Zdroj dat **GROUPBY** rozděluje výsledek dotazu do skupin záznamů, obvykle za účelem provedení jedné nebo více agregací v každé skupině.</span><span class="sxs-lookup"><span data-stu-id="19e1c-334">The **GROUPBY** data source divides the query result into groups of records, usually for the purpose of doing one or more aggregations on each group.</span></span> <span data-ttu-id="19e1c-335">Každý zdroj dat **GROUPBY** lze konfigurovat tak, aby běžel na úrovni databáze nebo v paměti.</span><span class="sxs-lookup"><span data-stu-id="19e1c-335">Every **GROUPBY** data source can be configured so that it's run either at the database level or in memory.</span></span> <span data-ttu-id="19e1c-336">Když je zdroj dat **GROUPBY** konfigurován tak, aby byl spuštěn na úrovni databáze, ER zkontroluje, zda lze navázat přímý dotaz SQL do zdroje dat, na který se tento zdroj dat odkazuje.</span><span class="sxs-lookup"><span data-stu-id="19e1c-336">When a **GROUPBY** data source is configured so that it's run at the database level, ER checks whether a direct SQL query can be established to a data source that is referred to in that data source.</span></span> <span data-ttu-id="19e1c-337">Pokud nelze navázat přímý dotaz, dojde v návrháři mapování modelu ER k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="19e1c-337">If a direct query can't be established, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="19e1c-338">Zpráva, kterou obdržíte, uvádí, že konfigurovaný zdroj dat **GROUPBY** nelze spustit za běhu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-338">The message that you receive states that the configured **GROUPBY** data source can't be run at runtime.</span></span>

<span data-ttu-id="19e1c-339">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="19e1c-339">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="19e1c-340">Začněte konfigurací komponenty mapování modelu ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-340">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="19e1c-341">Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-341">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="19e1c-342">Pojmenujte nový zdroj dat jako **Trans**. V poli **Tabulka** vyberte hodnotu **VendTrans** a určete tak, že tento zdroj dat bude vyžadovat tabulku VendTrans.</span><span class="sxs-lookup"><span data-stu-id="19e1c-342">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
4. <span data-ttu-id="19e1c-343">Přidejte zdroj dat typu **Seskupit podle**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-343">Add a data source of the **Group by** type.</span></span>
5. <span data-ttu-id="19e1c-344">Pojmenujte nový zdroj dat jako **GroupedTrans** a konfigurujte jej následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="19e1c-344">Name the new data source **GroupedTrans**, and configure it in the following way:</span></span>

    - <span data-ttu-id="19e1c-345">Vyberte zdroj dat **Trans** jako zdroj záznamů, které by měly být seskupeny.</span><span class="sxs-lookup"><span data-stu-id="19e1c-345">Select the **Trans** data source as the source of records that should be grouped.</span></span>
    - <span data-ttu-id="19e1c-346">V poli **Místo provedení** vyberte **Dotaz** a určete tak, že chcete spustit tento zdroj dat na úrovni databáze.</span><span class="sxs-lookup"><span data-stu-id="19e1c-346">In the **Execution location** field, select **Query** to specify that you want to run this data source at the database level.</span></span>

    ![Konfigurace zdroje dat na stránce Upravit parametry „Seskupit podle“](./media/er-components-inspections-05a.gif)

6. <span data-ttu-id="19e1c-348">Výběrem příkazu **Ověřit** zkontrolujte upravitelnou komponentu mapování modelu na stránce **návrháře mapování modelů** a ověřte, zda je možné konfigurovaný zdroj dat **GroupedTrans** používat v dotazech.</span><span class="sxs-lookup"><span data-stu-id="19e1c-348">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **GroupedTrans** data source can be queried.</span></span>
7. <span data-ttu-id="19e1c-349">Upravte zdroj dat **Trans** přidáním vnořeného pole typu **Vypočítané pole** a získejte oříznuté číslo účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="19e1c-349">Modify the **Trans** data source by adding a nested field of the **Calculated field** type to get the trimmed vendor account number.</span></span>
8. <span data-ttu-id="19e1c-350">Pojmenujte nový zdroj dat jako **$AccNumber** a konfigurujte jej tak, aby obsahoval výraz `TRIM(Trans.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-350">Name the new data source **$AccNumber**, and configure it so that it contains the expression `TRIM(Trans.AccountNum)`.</span></span>

    ![Konfigurace zdroje dat na stránce návrháře mapování modelů](./media/er-components-inspections-05a.png)

9. <span data-ttu-id="19e1c-352">Výběrem příkazu **Ověřit** zkontrolujte upravitelnou komponentu mapování modelu na stránce **návrháře mapování modelů** a ověřte, zda je možné konfigurovaný zdroj dat **GroupedTrans** používat v dotazech.</span><span class="sxs-lookup"><span data-stu-id="19e1c-352">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **GroupedTrans** data source can be queried.</span></span>

    ![Po ověření komponenty mapování modelu ER a ověření konfigurovaného zdroje dat je možné zdroj dat GroupedTrans používat v dotazech na stránce návrháře mapování modelů](./media/er-components-inspections-05b.png)

10. <span data-ttu-id="19e1c-354">Všimněte si, že dojde k chybě ověření, protože zdroj dat **Trans** obsahuje vnořené pole typu **Vypočítané pole**, které neumožňuje přeložit volání určené pro zdroj dat **GroupedTrans** na přímý příkaz SQL.</span><span class="sxs-lookup"><span data-stu-id="19e1c-354">Notice that a validation error occurs, because the **Trans** data source contains a nested field of the **Calculated field** type that doesn't allow the call for the **GroupedTrans** data source to be translated to the direct SQL statement.</span></span>

<span data-ttu-id="19e1c-355">Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění a výběrem příkazu **Spustit** spustíte formát, který má konfigurováno použití mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-355">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![Chyby za běhu, ke kterým dochází při ignorování upozornění na stránce Návrhář formátů](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a><span data-ttu-id="19e1c-357">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-357">Automatic resolution</span></span>

<span data-ttu-id="19e1c-358">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="19e1c-358">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="19e1c-359">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-359">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="19e1c-360">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="19e1c-360">Option 1</span></span>

<span data-ttu-id="19e1c-361">Místo přidání vnořeného pole typu **Vypočítané pole** zadejte do zdroje dat **Trans** přidejte vnořené pole **$AccNumber** pro položku **GroupedTrans.lines** zdroje dat **GroupedTrans** a konfigurujte jej tak, aby obsahovalo výraz `TRIM(GroupedTrans.lines.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-361">Instead of adding a nested field of the **Calculated field** type to the **Trans** data source, add the **$AccNumber** nested field for the **GroupedTrans.lines** item of the **GroupedTrans** data source, and configure it so that it contains the expression `TRIM(GroupedTrans.lines.AccountNum)`.</span></span> <span data-ttu-id="19e1c-362">Tímto způsobem lze zdroj dat **GroupedTrans** spustit na úrovni SQL a vypočítat vnořené pole **$AccNumber** později.</span><span class="sxs-lookup"><span data-stu-id="19e1c-362">In this way, the **GroupedTrans** data source can be run at the SQL level and calculate the **$AccNumber** nested field afterward.</span></span>

#### <a name="option-2"></a><span data-ttu-id="19e1c-363">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="19e1c-363">Option 2</span></span>

<span data-ttu-id="19e1c-364">Změňte hodnotu pole **Místo provedení** pro zdroj dat **GroupedTrans** z hodnoty **Dotaz** na **V paměti**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-364">Change the value of the **Execution location** field for the **GroupedTrans** data source from **Query** to **In memory**.</span></span> <span data-ttu-id="19e1c-365">Nedoporučujeme měnit hodnotu pro tabulku, která obsahuje velké množství dat (transakční tabulka), protože budou načteny všechny záznamy a seskupení spolu s agregací budou provedeny v paměti.</span><span class="sxs-lookup"><span data-stu-id="19e1c-365">We don't recommend that you change the value for a table that has a large volume of data (transactional table), because all records will be fetched, and grouping and aggregation will be done in memory.</span></span> <span data-ttu-id="19e1c-366">Tento přístup proto může způsobit špatný výkon.</span><span class="sxs-lookup"><span data-stu-id="19e1c-366">Therefore, this approach can cause poor performance.</span></span>

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a><span data-ttu-id="19e1c-367">Spustitelnost zdroje dat JOIN</span><span class="sxs-lookup"><span data-stu-id="19e1c-367">Executability of a JOIN data source</span></span>

<span data-ttu-id="19e1c-368">Zdroj dat [JOIN](er-join-data-sources.md) kombinuje záznamy ze dvou nebo více databázových tabulek na základě souvisejících polí.</span><span class="sxs-lookup"><span data-stu-id="19e1c-368">The [JOIN](er-join-data-sources.md) data source combines records from two or more database tables, based on related fields.</span></span> <span data-ttu-id="19e1c-369">Každý zdroj dat **JOIN** lze konfigurovat tak, aby běžel na úrovni databáze nebo v paměti.</span><span class="sxs-lookup"><span data-stu-id="19e1c-369">Every **JOIN** data source can be configured so that it's run either at the database level or in memory.</span></span> <span data-ttu-id="19e1c-370">Když je zdroj dat **JOIN** konfigurován tak, aby byl spuštěn na úrovni databáze, ER zkontroluje, zda lze navázat přímý dotaz SQL do zdrojů dat, na které se tento zdroj dat odkazuje.</span><span class="sxs-lookup"><span data-stu-id="19e1c-370">When a **JOIN** data source is configured so that it's run at the database level, ER checks whether a direct SQL query can be established to data sources that are referred to in that data source.</span></span> <span data-ttu-id="19e1c-371">Pokud nelze navázat přímý dotaz SQL s nejméně jedním odkazovaným zdrojem dat, dojde v návrháři mapování modelu ER k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="19e1c-371">If a direct SQL query can't be established with at least one referenced data source, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="19e1c-372">Zpráva, kterou obdržíte, uvádí, že konfigurovaný zdroj dat **JOIN** nelze spustit za běhu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-372">The message that you receive states that the configured **JOIN** data source can't be run at runtime.</span></span>

<span data-ttu-id="19e1c-373">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="19e1c-373">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="19e1c-374">Začněte konfigurací komponenty mapování modelu ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-374">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="19e1c-375">Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-375">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="19e1c-376">Pojmenujte nový zdroj dat jako **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-376">Name the new data source **Vendor**.</span></span> <span data-ttu-id="19e1c-377">V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.</span><span class="sxs-lookup"><span data-stu-id="19e1c-377">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="19e1c-378">Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-378">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
5. <span data-ttu-id="19e1c-379">Pojmenujte nový zdroj dat jako **Trans**. V poli **Tabulka** vyberte hodnotu **VendTrans** a určete tak, že tento zdroj dat bude vyžadovat tabulku VendTrans.</span><span class="sxs-lookup"><span data-stu-id="19e1c-379">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
6. <span data-ttu-id="19e1c-380">Přidejte zdroj dat typu **Vypočítané pole** jako vnořené pole zdroje dat **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-380">Add a data source of the **Calculated field** type as the nested field of the **Vendor** data source.</span></span>
7. <span data-ttu-id="19e1c-381">Pojmenujte nový zdroj dat jako **FilteredTrans** a konfigurujte jej tak, aby obsahoval výraz `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-381">Name the new data source **FilteredTrans**, and configure it so that it contains the expression `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span></span>
8. <span data-ttu-id="19e1c-382">Přidejte zdroj dat typu **Spojit**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-382">Add a data source of the **Join** type.</span></span>
9. <span data-ttu-id="19e1c-383">Pojmenujte nový zdroj dat jako **JoinedList** a konfigurujte jej následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="19e1c-383">Name the new data source **JoinedList**, and configure it in the following way:</span></span>

    1. <span data-ttu-id="19e1c-384">Přidejte zdroj dat **Vendor** jako první sadu záznamů, která bude spojena.</span><span class="sxs-lookup"><span data-stu-id="19e1c-384">Add the **Vendor** data source as the first set of records to join.</span></span>
    2. <span data-ttu-id="19e1c-385">Přidejte zdroj dat **Vendor.FilteredTrans** jako druhou sadu záznamů, která bude spojena.</span><span class="sxs-lookup"><span data-stu-id="19e1c-385">Add the **Vendor.FilteredTrans** data source as the second set of records to join.</span></span> <span data-ttu-id="19e1c-386">Vyberte typ spojení **INNER**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-386">Select **INNER** as the type.</span></span>
    3. <span data-ttu-id="19e1c-387">V poli **Provést** vyberte **Dotaz** a určete tak, že chcete spustit tento zdroj dat na úrovni databáze.</span><span class="sxs-lookup"><span data-stu-id="19e1c-387">In the **Execute** field, select **Query** to specify that you want to run this data source at the database level.</span></span>

    ![Konfigurace zdroje dat na stránce návrháře spojení](./media/er-components-inspections-06a.gif)

10. <span data-ttu-id="19e1c-389">Výběrem příkazu **Ověřit** zkontrolujte upravitelnou komponentu mapování modelu na stránce **návrháře mapování modelů** a ověřte, zda je možné konfigurovaný zdroj dat **JoinedList** používat v dotazech.</span><span class="sxs-lookup"><span data-stu-id="19e1c-389">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **JoinedList** data source can be queried.</span></span>
11. <span data-ttu-id="19e1c-390">Změňte výraz zdroje dat **Vendor.FilteredTrans** z `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` na `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-390">Change the expression of the **Vendor.FilteredTrans** data source from `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` to `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span></span>
12. <span data-ttu-id="19e1c-391">Výběrem příkazu **Ověřit** zkontrolujte upravitelnou komponentu mapování modelu na stránce **návrháře mapování modelů** a ověřte, zda je možné konfigurovaný zdroj dat **JoinedList** používat v dotazech.</span><span class="sxs-lookup"><span data-stu-id="19e1c-391">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **JoinedList** data source can be queried.</span></span>

    ![Výběrem příkazu Ověřit zkontrolujte upravitelnou komponentu mapování modelu a ověřte že je možné konfigurovaný zdroj dat JoinedList používat v dotazech na stránce návrháře mapování modelu](./media/er-components-inspections-06b.png)

13. <span data-ttu-id="19e1c-393">Všimněte si, že dojde k chybě ověření, protože výraz zdroje dat **Vendor.FilteredTrans** nelze přeložit na přímé volání SQL.</span><span class="sxs-lookup"><span data-stu-id="19e1c-393">Notice that a validation error occurs, because the expression of the **Vendor.FilteredTrans** data source can't be translated to the direct SQL call.</span></span> <span data-ttu-id="19e1c-394">Přímé volání SQL navíc neumožňuje volání zdroje dat **JoinedList**, které má být přeloženo do přímého příkazu SQL.</span><span class="sxs-lookup"><span data-stu-id="19e1c-394">Additionally, the direct SQL call doesn't allow the call for the **JoinedList** data source to be translated to the direct SQL statement.</span></span>

    ![Chyby za běhu z neúspěšného ověření zdroje dat JoinedList na stránce návrháře mapování modelů](./media/er-components-inspections-06c.png)

<span data-ttu-id="19e1c-396">Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění a výběrem příkazu **Spustit** spustíte formát, který má konfigurováno použití mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-396">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![Spuštění upravitelného formátu na stránce Návrhář formátů](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="19e1c-398">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-398">Automatic resolution</span></span>

<span data-ttu-id="19e1c-399">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="19e1c-399">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="19e1c-400">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-400">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="19e1c-401">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="19e1c-401">Option 1</span></span>

<span data-ttu-id="19e1c-402">Změňte výraz zdroje dat **Vendor.FilteredTrans** z `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` zpět na `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, jak doporučovalo zobrazené upozornění.</span><span class="sxs-lookup"><span data-stu-id="19e1c-402">Change the expression of the **Vendor.FilteredTrans** data source from `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` back to `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, as the warning advised.</span></span>

![Aktualizovaný výraz zdroje dat na stránce návrháře mapování modelů](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a><span data-ttu-id="19e1c-404">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="19e1c-404">Option 2</span></span>

<span data-ttu-id="19e1c-405">Změňte hodnotu pole **Provést** pro zdroj dat **JoinedList** z hodnoty **Dotaz** na **V paměti**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-405">Change the value of the **Execute** field for the **JoinedList** data source from **Query** to **In memory**.</span></span> <span data-ttu-id="19e1c-406">Nedoporučujeme měnit hodnotu v tabulce, která obsahuje velké množství dat (transakční tabulka), protože budou načteny všechny záznamy a seskupení bude provedeno v paměti.</span><span class="sxs-lookup"><span data-stu-id="19e1c-406">We don't recommend that you change the value for a table that has a large volume of data (transactional table), because all records will be fetched, and the join will be done in memory.</span></span> <span data-ttu-id="19e1c-407">Tento přístup proto může způsobit špatný výkon.</span><span class="sxs-lookup"><span data-stu-id="19e1c-407">Therefore, this approach can cause poor performance.</span></span> <span data-ttu-id="19e1c-408">Zobrazí se upozornění ověření, které vás bude informovat o tomto riziku.</span><span class="sxs-lookup"><span data-stu-id="19e1c-408">A validation warning is shown to inform you about this risk.</span></span>

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a><span data-ttu-id="19e1c-409">Je vhodnější funkce FILTER nebo WHERE?</span><span class="sxs-lookup"><span data-stu-id="19e1c-409">Preferability of FILTER vs WHERE function</span></span>

<span data-ttu-id="19e1c-410">Integrovaná funkce ER [FILTER](er-functions-list-filter.md) se používá pro přístup k aplikačním tabulkám, pohledům nebo datovým entitám umístěním jediného volání SQL, které získá požadovaná data jako seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="19e1c-410">The built-in [FILTER](er-functions-list-filter.md) ER function is used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="19e1c-411">Funkce [WHERE](er-functions-list-where.md) načte všechny záznamy z daného zdroje a provede výběr záznamů v paměti.</span><span class="sxs-lookup"><span data-stu-id="19e1c-411">The [WHERE](er-functions-list-where.md) function fetches all records from the given source and does record selection in memory.</span></span> <span data-ttu-id="19e1c-412">Zdroj dat typu **Seznam záznamů** se používá jako argument obou funkcí a určuje zdroj pro načtení záznamů.</span><span class="sxs-lookup"><span data-stu-id="19e1c-412">A data source of the **Record list** type is used as an argument of both functions and specifies a source for getting records.</span></span> <span data-ttu-id="19e1c-413">ER kontroluje, zda lze navázat přímé volání SQL do zdroje dat, na který se odkazuje ve funkci **WHERE**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-413">ER checks whether a direct SQL call can be established to a data source that is referred to in the **WHERE** function.</span></span> <span data-ttu-id="19e1c-414">Pokud nelze navázat přímé volání, je v návrháři mapování modelu ER vyvoláno upozornění ověření.</span><span class="sxs-lookup"><span data-stu-id="19e1c-414">If a direct call can be established, a validation warning occurs in the ER model mapping designer.</span></span> <span data-ttu-id="19e1c-415">Zpráva, kterou obdržíte, doporučuje použít funkci **FILTER** namísto **WHERE**, která pomůže zlepšit efektivitu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-415">The message that you receive recommends that you use the **FILTER** function instead of the **WHERE** function to help improve efficiency.</span></span>

<span data-ttu-id="19e1c-416">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="19e1c-416">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="19e1c-417">Začněte konfigurací komponenty mapování modelu ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-417">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="19e1c-418">Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-418">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="19e1c-419">Pojmenujte nový zdroj dat jako **Trans**. V poli **Tabulka** vyberte hodnotu **VendTrans** a určete tak, že tento zdroj dat bude vyžadovat tabulku VendTrans.</span><span class="sxs-lookup"><span data-stu-id="19e1c-419">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
4. <span data-ttu-id="19e1c-420">Přidejte zdroj dat typu **Vypočítané pole** jako vnořené pole zdroje dat **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-420">Add a data source of the **Calculated field** type as the nested field of the **Vendor** data source.</span></span>
5. <span data-ttu-id="19e1c-421">Pojmenujte nový zdroj dat jako **FilteredTrans** a konfigurujte jej tak, aby obsahoval výraz `WHERE(Trans, Trans.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-421">Name the new data source **FilteredTrans**, and configure it so that it contains the expression `WHERE(Trans, Trans.AccountNum="US-101")`.</span></span>
6. <span data-ttu-id="19e1c-422">Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-422">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="19e1c-423">Pojmenujte nový zdroj dat jako **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-423">Name the new data source **Vendor**.</span></span> <span data-ttu-id="19e1c-424">V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.</span><span class="sxs-lookup"><span data-stu-id="19e1c-424">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="19e1c-425">Přidejte zdroj dat typu **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-425">Add a data source of the **Calculated field** type.</span></span>
9. <span data-ttu-id="19e1c-426">Pojmenujte nový zdroj dat jako **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-426">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span>
10. <span data-ttu-id="19e1c-427">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu mapování modelu na stránce **Návrhář mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-427">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![Výběrem příkazu Ověřit zkontrolujete upravitelnou komponentu mapování modelu na stránce návrháře mapování modelu](./media/er-components-inspections-07a.png)

11. <span data-ttu-id="19e1c-429">Všimněte si, že upozornění ověření doporučují používat funkci **FILTER** namísto funkce **WHERE** u zdrojů dat **FilteredVendor** a **FilteredTrans**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-429">Notice that validation warnings recommend that you use the **FILTER** function instead of the **WHERE** function for the **FilteredVendor** and **FilteredTrans** data sources.</span></span>

    ![Upozornění ověření doporučující funkci FILTER namísto funkce WHERE na stránce návrháře mapování modelů](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="19e1c-431">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-431">Automatic resolution</span></span>

<span data-ttu-id="19e1c-432">Výběrem příkazu **Opravit** automaticky nahradíte funkci **WHERE** funkcí **FILTER** ve výrazu všech zdrojů dat, které se objevují v mřížce na kartě **Upozornění** pro tento typ kontroly.</span><span class="sxs-lookup"><span data-stu-id="19e1c-432">Select **Fix** to automatically replace the **WHERE** function with the **FILTER** function in the expression of all data sources that appear in the grid on the **Warnings** tab for this type of inspection.</span></span>

<span data-ttu-id="19e1c-433">Alternativně můžete vybrat řádek pro jedno upozornění v mřížce a poté vybrat příkaz **Opravit vybrané**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-433">Alternatively, you can select the row for a single warning in the grid and then select **Fix selected**.</span></span> <span data-ttu-id="19e1c-434">V tomto případě se výraz automaticky změní pouze ve zdroji dat, který je uveden ve vybraném upozornění.</span><span class="sxs-lookup"><span data-stu-id="19e1c-434">In this case, the expression is automatically changed only in the data source that is mentioned in the selected warning.</span></span>

![Výběrem možnosti Opravit automaticky nahradíte funkci WHERE funkcí FILTER na stránce návrháře mapování modelů](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a><span data-ttu-id="19e1c-436">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-436">Manual resolution</span></span>

<span data-ttu-id="19e1c-437">Výrazy všech zdrojů dat, které jsou uvedeny v ověřovací mřížce, můžete ručně upravit nahrazením funkce **WHERE** za funkci **FILTER**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-437">You can manually adjust the expressions of all the data sources that are mentioned in the validation grid by replacing the **WHERE** function with the **FILTER** function.</span></span>

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a><span data-ttu-id="19e1c-438">Je vhodnější funkce ALLITEMSQUERY nebo ALLITEMS?</span><span class="sxs-lookup"><span data-stu-id="19e1c-438">Preferability of ALLITEMSQUERY vs ALLITEMS function</span></span>

<span data-ttu-id="19e1c-439">Integrované funkce ER [ALLITEMS](er-functions-list-allitems.md) a [ALLITEMSQUERY](er-functions-list-allitemsquery.md) se používají k získání ploché hodnoty **seznamu záznamů**, která se skládá ze seznamu záznamů, které představují všechny položky odpovídající zadané cestě.</span><span class="sxs-lookup"><span data-stu-id="19e1c-439">The built-in [ALLITEMS](er-functions-list-allitems.md) and [ALLITEMSQUERY](er-functions-list-allitemsquery.md) ER functions are used to get a flattened **Record list** value that consists of a list of records that represent all items that match the specified path.</span></span> <span data-ttu-id="19e1c-440">ER kontroluje, zda lze navázat přímé volání SQL do zdroje dat, na který se odkazuje ve funkci **ALLITEMS**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-440">ER checks whether a direct SQL call can be established to a data source that is referred to in the **ALLITEMS** function.</span></span> <span data-ttu-id="19e1c-441">Pokud nelze navázat přímé volání, je v návrháři mapování modelu ER vyvoláno upozornění ověření.</span><span class="sxs-lookup"><span data-stu-id="19e1c-441">If a direct call can be established, a validation warning occurs in the ER model mapping designer.</span></span> <span data-ttu-id="19e1c-442">Zpráva, kterou obdržíte, doporučuje použít funkci **ALLITEMSQUERY** namísto **ALLITEMS**, která pomůže zlepšit efektivitu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-442">The message that you receive recommends that you use the **ALLITEMSQUERY** function instead of the **ALLITEMS** function to help improve efficiency.</span></span>

<span data-ttu-id="19e1c-443">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="19e1c-443">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="19e1c-444">Začněte konfigurací komponenty mapování modelu ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-444">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="19e1c-445">Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-445">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="19e1c-446">Pojmenujte nový zdroj dat jako **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-446">Name the new data source **Vendor**.</span></span> <span data-ttu-id="19e1c-447">V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.</span><span class="sxs-lookup"><span data-stu-id="19e1c-447">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="19e1c-448">K získání záznamů za několik dodavatelů přidejte zdroj dat typu **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-448">Add a data source of the **Calculated field** type to get records for several vendors.</span></span>
5. <span data-ttu-id="19e1c-449">Pojmenujte nový zdroj dat jako **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-449">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.</span></span>
6. <span data-ttu-id="19e1c-450">K získání transakcí všech vyfiltrovaných dodavatelů přidejte zdroj dat typu **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-450">Add a data source of the **Calculated field** type to get transactions of all filtered vendors.</span></span>
7. <span data-ttu-id="19e1c-451">Pojmenujte nový zdroj dat jako **FilteredVendorTrans** a konfigurujte jej tak, aby obsahoval výraz `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-451">Name the new data source **FilteredVendorTrans**, and configure it so that it contains the expression `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.</span></span>
8. <span data-ttu-id="19e1c-452">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu mapování modelu na stránce **Návrhář mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-452">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![Stránka návrháře mapování modelů, tlačítko Ověřit](./media/er-components-inspections-08a.png)

9. <span data-ttu-id="19e1c-454">Všimněte si, že se zobrazí upozornění ověření.</span><span class="sxs-lookup"><span data-stu-id="19e1c-454">Notice that a validation warning occurs.</span></span> <span data-ttu-id="19e1c-455">Zpráva doporučuje použít funkci **ALLITEMSQUERY** namísto funkce **ALLITEMS** pro zdroj dat **FilteredVendorTrans**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-455">The message recommends that you use the **ALLITEMSQUERY** function instead of the **ALLITEMS** function for the **FilteredVendorTrans** data source.</span></span>

    ![Upozornění ověření s radou použít funkci ALLITEMSQUERY namísto funkce ALLITEMS v komponentě mapování modelu ER na stránce návrháře mapování modelů](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="19e1c-457">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-457">Automatic resolution</span></span>

<span data-ttu-id="19e1c-458">Výběrem příkazu **Opravit** automaticky nahradíte funkci **ALLITEMS** funkcí **ALLITEMSQUERY** ve výrazu všech zdrojů dat, které se objevují v mřížce na kartě **Upozornění** pro tento typ kontroly.</span><span class="sxs-lookup"><span data-stu-id="19e1c-458">Select **Fix** to automatically replace the **ALLITEMS** function with the **ALLITEMSQUERY** function in the expression of all data sources that appear in the grid on the **Warnings** tab for this type of inspection.</span></span>

<span data-ttu-id="19e1c-459">Alternativně můžete vybrat řádek pro jedno upozornění v mřížce a poté vybrat příkaz **Opravit vybrané**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-459">Alternatively, you can select the row for a single warning in the grid and then select **Fix selected**.</span></span> <span data-ttu-id="19e1c-460">V tomto případě se výraz automaticky změní pouze ve zdroji dat, který je uveden ve vybraném upozornění.</span><span class="sxs-lookup"><span data-stu-id="19e1c-460">In this case, the expression is automatically changed only in the data source that is mentioned in the selected warning.</span></span>

![Na stránce návrháře mapování modelů vyberte příkaz Opravit vybrané](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a><span data-ttu-id="19e1c-462">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-462">Manual resolution</span></span>

<span data-ttu-id="19e1c-463">Výrazy všech zdrojů dat, které jsou uvedeny v ověřovací mřížce, můžete ručně upravit nahrazením funkce **ALLITEMS** za funkci **ALLITEMSQUERY**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-463">You can manually adjust the expressions of all the data sources that are mentioned in the validation grid by replacing the **ALLITEMS** function with the **ALLITEMSQUERY** function.</span></span>

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a><span data-ttu-id="19e1c-464">Možnost výskytů prázdného seznamu</span><span class="sxs-lookup"><span data-stu-id="19e1c-464">Consideration of empty list cases</span></span>

<span data-ttu-id="19e1c-465">Komponentu formátu nebo mapování modelu ER můžete konfigurovat tak, abyste získali hodnotu pole zdroje dat typu **Seznam záznamů**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-465">You can configure your ER format or model mapping component to get the field value of a data source of the **Record list** type.</span></span> <span data-ttu-id="19e1c-466">ER zkontroluje, zda váš návrh zohledňuje případ, kdy zdroj dat, který je volán, neobsahuje žádné záznamy (tedy je prázdný), aby se předešlo chybám za běhu při načtení hodnoty z pole neexistujícího záznamu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-466">ER checks whether your design considers the case where a data source that is called contains no records (that is, it's empty), to prevent runtime errors when a value is fetched from a field of a nonexistent record.</span></span>

<span data-ttu-id="19e1c-467">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="19e1c-467">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="19e1c-468">Začněte konfigurovat datový model ER, mapování modelu ER a komponenty formátu ER současně.</span><span class="sxs-lookup"><span data-stu-id="19e1c-468">Start to configure the ER data model, the ER model mapping, and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="19e1c-469">Ve stromu datového modelu přidejte kořenovou položku s názvem **Root3**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-469">In the data model tree, add a root item that is named **Root3**.</span></span>
3. <span data-ttu-id="19e1c-470">Upravte položku **Root3** přidáním vnořené položky typu **Seznam záznamů**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-470">Modify the **Root3** item by adding a nested item of the **Record list** type.</span></span>
4. <span data-ttu-id="19e1c-471">Pojmenujte novou vnořenou položku jako **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-471">Name the new nested item **Vendor**.</span></span>
5. <span data-ttu-id="19e1c-472">Upravte položku **Vendor** následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="19e1c-472">Modify the **Vendor** item in the following way:</span></span>

    - <span data-ttu-id="19e1c-473">Přidejte vnořené pole typu **Řetězec** a pojmenujte jej jako **Name**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-473">Add a nested field of the **String** type, and name it **Name**.</span></span>
    - <span data-ttu-id="19e1c-474">Přidejte vnořené pole typu **Řetězec** a pojmenujte jej jako **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-474">Add a nested field of the **String** type, and name it **AccountNumber**.</span></span>

    ![Přidání vnořených polí na stránce Datový model](./media/er-components-inspections-09a.png)

6. <span data-ttu-id="19e1c-476">V podokně zdrojů dat mapování modelu přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-476">In the model mapping data sources pane, add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="19e1c-477">Pojmenujte nový zdroj dat jako **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-477">Name the new data source **Vendor**.</span></span> <span data-ttu-id="19e1c-478">V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.</span><span class="sxs-lookup"><span data-stu-id="19e1c-478">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="19e1c-479">Přidejte zdroj dat typu **Všeobecné \\ Uživatelský vstupní parametr** pro vyhledání účtu dodavatele v dialogovém okně modulu runtime.</span><span class="sxs-lookup"><span data-stu-id="19e1c-479">Add a data source of the **General \\ User input parameter** type to search for a vendor account in the runtime dialog box.</span></span>
9. <span data-ttu-id="19e1c-480">Pojmenujte nový zdroj dat jako **RequestedAccountNum**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-480">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="19e1c-481">Do pole **Popisek** zadejte **Číslo účtu dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-481">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="19e1c-482">V poli **Název datového typu Operations** ponechte výchozí hodnotu **Popis**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-482">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
10. <span data-ttu-id="19e1c-483">K vyfiltrování dodavatele, o kterého se zajímáte, přidejte zdroj dat typu **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-483">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
11. <span data-ttu-id="19e1c-484">Pojmenujte nový zdroj dat jako **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-484">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
12. <span data-ttu-id="19e1c-485">Vytvořte vazbu položek datového modelu na konfigurované zdroje dat následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="19e1c-485">Bind the data model items to configured data sources in the following way:</span></span>

    - <span data-ttu-id="19e1c-486">Vytvořte vazbu položky **FilteredVendor** na položku **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-486">Bind **FilteredVendor** to **Vendor**.</span></span>
    - <span data-ttu-id="19e1c-487">Vytvořte vazbu položky **FilteredVendor.AccountNum** na položku **Vendor.AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-487">Bind **FilteredVendor.AccountNum** to **Vendor.AccountNumber**.</span></span>
    - <span data-ttu-id="19e1c-488">Vytvořte vazbu položky **FilteredVendor.'name()'** na položku **Vendor.Name**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-488">Bind **FilteredVendor.'name()'** to **Vendor.Name**.</span></span>

    ![Vázání položek datového modelu na stránce návrháře mapování modelů](./media/er-components-inspections-09b.png)

13. <span data-ttu-id="19e1c-490">Ve stromu struktury formátu přidejte následující položky, které generují odchozí dokument ve formátu XML obsahující podrobnosti o dodavateli:</span><span class="sxs-lookup"><span data-stu-id="19e1c-490">In the format structure tree, add the following items to generate an outbound document in XML format that contains the vendor details:</span></span>

    1. <span data-ttu-id="19e1c-491">Přidejte kořenový prvek XML **Statement**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-491">Add the **Statement** root XML element.</span></span>
    2. <span data-ttu-id="19e1c-492">U prvku XML **Statement** přidejte vnořený prvek XML **Party**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-492">For the **Statement** XML element, add the nested **Party** XML element.</span></span>
    3. <span data-ttu-id="19e1c-493">U prvku XML **Party** přidejte následující vnořené atributy XML:</span><span class="sxs-lookup"><span data-stu-id="19e1c-493">For the **Party** XML element, add the following nested XML attributes:</span></span>

        - <span data-ttu-id="19e1c-494">Jméno</span><span class="sxs-lookup"><span data-stu-id="19e1c-494">Name</span></span>
        - <span data-ttu-id="19e1c-495">AccountNum</span><span class="sxs-lookup"><span data-stu-id="19e1c-495">AccountNum</span></span>

14. <span data-ttu-id="19e1c-496">Navažte prvky formátu na poskytnuté zdroje dat následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="19e1c-496">Bind format elements to provided data sources in the following way:</span></span>

    - <span data-ttu-id="19e1c-497">Vytvořte vazbu prvku formátu **Statement\\Party\\Name** na pole zdroje dat **model.Vendor.Name**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-497">Bind the **Statement\\Party\\Name** format element to the **model.Vendor.Name** data source field.</span></span>
    - <span data-ttu-id="19e1c-498">Vytvořte vazbu prvku formátu **Statement\\Party\\AccountNum** na pole zdroje dat **model.Vendor.AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-498">Bind the **Statement\\Party\\AccountNum** format element to the **model.Vendor.AccountNumber** data source field.</span></span>

15. <span data-ttu-id="19e1c-499">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu formátu na stránce **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-499">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![Ověření prvků formátu navázaných na zdroje dat na stránce Návrhář formátů](./media/er-components-inspections-09c.png)

16. <span data-ttu-id="19e1c-501">Všimněte si, že dojde k chybám ověření.</span><span class="sxs-lookup"><span data-stu-id="19e1c-501">Notice that a validation errors occur.</span></span> <span data-ttu-id="19e1c-502">Zpráva uvádí, že chyba může být za běhu vyvolána u konfigurovaných komponent formátu **Statement\\Party\\Name** a **Statement\\Party\\AccountNum**, pokud je seznam **model.Vendor** prázdný.</span><span class="sxs-lookup"><span data-stu-id="19e1c-502">The message states that an error might be thrown for the configured **Statement\\Party\\Name** and **Statement\\Party\\AccountNum** format components at runtime if the **model.Vendor** list is empty.</span></span>

    ![Chyba ověření, která upozorňuje na potenciální chybu u konfigurovaných komponent formátu](./media/er-components-inspections-09d.png)

<span data-ttu-id="19e1c-504">Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění, vyberete příkaz **Spustit** a zvolíte číslo účtu neexistujícího dodavatele.</span><span class="sxs-lookup"><span data-stu-id="19e1c-504">The following illustration shows the runtime error that occurs if you ignore the warning, select **Run** to run the format, and select the account number of a nonexistent vendor.</span></span> <span data-ttu-id="19e1c-505">Protože požadovaný dodavatel neexistuje, seznam **model.Vendor** bude prázdný (to znamená, že nebude obsahovat žádné záznamy).</span><span class="sxs-lookup"><span data-stu-id="19e1c-505">Because the requested vendor doesn't exist, the **model.Vendor** list will be empty (that is, it will contain no records).</span></span>

![Chyby za běhu, ke kterým došlo za běhu mapování formátu](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="19e1c-507">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-507">Automatic resolution</span></span>

<span data-ttu-id="19e1c-508">Pro vybraný řádek v mřížce na kartě **Upozornění** můžete vybrat příkaz **Zrušit vazbu**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-508">For the selected row in the grid on the **Warnings** tab, you can select **Unbind**.</span></span> <span data-ttu-id="19e1c-509">Vazba, na kterou se ukazuje ve sloupci **Cesta**, je automaticky odebrána z prvků formátu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-509">The binding that is pointed to in the **Path** column is automatically removed from the format elements.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="19e1c-510">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-510">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="19e1c-511">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="19e1c-511">Option 1</span></span>

<span data-ttu-id="19e1c-512">Můžete navázat prvek formátu **Statement\\Party\\Name** na položku zdroje dat **model.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-512">You can bind the **Statement\\Party\\Name** format element to the **model.Vendor** data source item.</span></span> <span data-ttu-id="19e1c-513">Za běhu tato vazba volá nejprve zdroj dat **model.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-513">At runtime, this binding calls the **model.Vendor** data source first.</span></span> <span data-ttu-id="19e1c-514">Když **model.Vendor** vrátí prázdný seznam záznamů, vnořené prvky formátu se nespustí.</span><span class="sxs-lookup"><span data-stu-id="19e1c-514">When **model.Vendor** returns an empty record list, the nested format elements aren't run.</span></span> <span data-ttu-id="19e1c-515">Proto u této konfigurace formátu nejsou vyvolána žádná upozornění ověření.</span><span class="sxs-lookup"><span data-stu-id="19e1c-515">Therefore, no validation warnings occur for this format configuration.</span></span>

![Vazba prvku formátu na položku zdroje dat na stránce Návrhář formátů](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a><span data-ttu-id="19e1c-517">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="19e1c-517">Option 2</span></span>

<span data-ttu-id="19e1c-518">Změňte vazbu prvku formátu **Statement\\Party\\Name** z `model.Vendor.Name` na `FIRSTORNULL(model.Vendor).Name`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-518">Change the binding of the **Statement\\Party\\Name** format element from `model.Vendor.Name` to `FIRSTORNULL(model.Vendor).Name`.</span></span> <span data-ttu-id="19e1c-519">Aktualizovaná vazba podmíněně převede první záznam zdroje dat **model.Vendor** typu **Seznam záznamů** na nový zdroj dat typu **Záznam**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-519">The updated binding conditionally converts the first record of the **model.Vendor** data source of the **Record list** type to a new data source of the **Record** type.</span></span> <span data-ttu-id="19e1c-520">Tento nový zdroj dat obsahuje stejnou sadu polí.</span><span class="sxs-lookup"><span data-stu-id="19e1c-520">This new data source contains the same set of fields.</span></span>

- <span data-ttu-id="19e1c-521">Pokud je ve zdroji dat **model.Vendor** k dispozici alespoň jeden záznam, pole tohoto záznamu jsou vyplněna hodnotami polí prvního záznamu zdroje dat **model.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-521">If at least one record is available in the **model.Vendor** data source, the fields of that record are filled with the values of the fields of the first record of the **model.Vendor** data source.</span></span> <span data-ttu-id="19e1c-522">V takovém případě aktualizovaná vazba vrátí název dodavatele.</span><span class="sxs-lookup"><span data-stu-id="19e1c-522">In this case, the updated binding returns the vendor name.</span></span>
- <span data-ttu-id="19e1c-523">V opačném případě je každé pole vytvořeného záznamu vyplněno výchozí hodnotou pro datový typ daného pole.</span><span class="sxs-lookup"><span data-stu-id="19e1c-523">Otherwise, every field of the record that is created is filled with the default value for the data type of that field.</span></span> <span data-ttu-id="19e1c-524">V tomto případě je vrácen prázdný řetězec jako výchozí hodnota datového typu **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-524">In this case, the blank string is returned as the default value of the **String** data type.</span></span>

<span data-ttu-id="19e1c-525">Proto se pro prvek formátu **Statement\\Party\\Name** nevyskytují žádná upozornění ověření, když je vázán na výraz `FIRSTORNULL(model.Vendor).Name`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-525">Therefore, no validation warnings occur for the **Statement\\Party\\Name** format element when it's bound to the `FIRSTORNULL(model.Vendor).Name` expression.</span></span>

![Změněná vazba řeší upozornění ověření na stránce Návrhář formátů](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a><span data-ttu-id="19e1c-527">Možnost 3</span><span class="sxs-lookup"><span data-stu-id="19e1c-527">Option 3</span></span>

<span data-ttu-id="19e1c-528">Pokud chcete explicitně určit data, která se zadávají do generovaného dokumentu, když zdroj dat **model.Vendor** typu **Seznam záznamů** nevrátí žádné záznamy (v tomto příkladu text **Not available**), změňte vazbu prvku formátu **Statement\\Party\\Name** z hodnoty `model.Vendor.Name` na `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-528">If you want to explicitly specify the data that is entered in a generated document when the **model.Vendor** data source of the **Record list** type returns no records (the text **Not available** in this example), change the binding of the **Statement\\Party\\Name** format element from `model.Vendor.Name` to `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`.</span></span> <span data-ttu-id="19e1c-529">Můžete také použít výraz `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-529">You can also use the expression `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.</span></span>

### <a name="additional-consideration"></a><a id="i9a"></a><span data-ttu-id="19e1c-530">Další faktor ke zvážení</span><span class="sxs-lookup"><span data-stu-id="19e1c-530">Additional consideration</span></span>

<span data-ttu-id="19e1c-531">Inspekce vás také upozorňuje na další možný problém.</span><span class="sxs-lookup"><span data-stu-id="19e1c-531">The inspection also warns you about another potential issue.</span></span> <span data-ttu-id="19e1c-532">Ve výchozím nastavení při vazbě prvků formátu **Statement\\Party\\Name** a **Statement\\Party\\AccountNum** na příslušná pole zdroje dat **model.Vendor** typu **Seznam záznamů** budou tyto vazby spuštěny a načtou hodnoty odpovídajících polí prvního záznamu zdroje dat **model.Vendor**, pokud tento seznam není prázdný.</span><span class="sxs-lookup"><span data-stu-id="19e1c-532">By default, as you bind the **Statement\\Party\\Name** and **Statement\\Party\\AccountNum** format elements to the appropriate fields of the **model.Vendor** data source of the **Record list** type, those bindings will be run and will take the values of the appropriate fields of the first record of the **model.Vendor** data source, if that list isn't empty.</span></span>

<span data-ttu-id="19e1c-533">Protože jste nevytvořili vazbu prvku formátu **Statement\\Party** se zdrojem dat **model.Vendor**, prvek **Statement\\Party** nebude během provádění formátu iterován pro každý záznam zdroje dat **model.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-533">Because you haven't bound the **Statement\\Party** format element with the **model.Vendor** data source, the **Statement\\Party** element won't be iterated for every record of the **model.Vendor** data source during format execution.</span></span> <span data-ttu-id="19e1c-534">Místo toho bude vygenerovaný dokument vyplněn informacemi pouze z prvního záznamu seznamu záznamů, pokud tento seznam obsahuje více záznamů.</span><span class="sxs-lookup"><span data-stu-id="19e1c-534">Instead, a generated document will be filled with information from only the first record of the record list, if that list contains multiple records.</span></span> <span data-ttu-id="19e1c-535">Proto může nastat problém, pokud je formát určen k vyplnění generovaného dokumentu informacemi o všech dodavatelích ze zdroje dat **model.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-535">Therefore, there might be an issue if the format is intended to fill a generated document with information about all vendors from the **model.Vendor** data source.</span></span> <span data-ttu-id="19e1c-536">Chcete-li tento problém napravit, vytvořte vazbu prvku **Statement\\Party** se zdrojem dat **model.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-536">To fix this issue, bind the **Statement\\Party** element with the **model.Vendor** data source.</span></span>

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a><span data-ttu-id="19e1c-537">Spustitelnost výrazu s funkcí FILTER (použití mezipaměti)</span><span class="sxs-lookup"><span data-stu-id="19e1c-537">Executability of an expression with FILTER function (caching)</span></span>

<span data-ttu-id="19e1c-538">Některé Integrované funkce ER, včetně [FILTER](er-functions-list-filter.md) a [ALLITEMSQUERY](er-functions-list-allitemsquery.md), se používají pro přístup k aplikačním tabulkám, pohledům nebo datovým entitám umístěním jediného volání SQL, které získá požadovaná data jako seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="19e1c-538">Several built-in ER functions, including [FILTER](er-functions-list-filter.md) and [ALLITEMSQUERY](er-functions-list-allitemsquery.md), are used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="19e1c-539">Zdroj dat typu **Seznam záznamů** se používá jako argument každé z těchto funkcí a určuje zdroj aplikace pro volání.</span><span class="sxs-lookup"><span data-stu-id="19e1c-539">A data source of the **Record list** type is used as an argument of each of these functions and specifies an application source for the call.</span></span> <span data-ttu-id="19e1c-540">ER kontroluje, zda lze navázat přímé volání SQL do zdroje dat, na který se odkazuje v jedné z těchto funkcí.</span><span class="sxs-lookup"><span data-stu-id="19e1c-540">ER checks whether a direct SQL call can be established to a data source that is referred to in one of these functions.</span></span> <span data-ttu-id="19e1c-541">Pokud nelze navázat přímé volání, protože zdroj dat byl označen jako [ukládaný do mezipaměti](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace), dojde v návrháři mapování modelu ER k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="19e1c-541">If a direct call can't be established because the data source was marked as [cached](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace), a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="19e1c-542">Zpráva, kterou obdržíte, uvádí, že výraz ER obsahující jednu z těchto funkcí nelze spustit za běhu programu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-542">The message that you receive states that the ER expression that contains one of these functions can't be run at runtime.</span></span>

<span data-ttu-id="19e1c-543">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="19e1c-543">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="19e1c-544">Začněte konfigurací komponenty mapování modelu ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-544">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="19e1c-545">Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-545">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="19e1c-546">Pojmenujte nový zdroj dat jako **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-546">Name the new data source **Vendor**.</span></span> <span data-ttu-id="19e1c-547">V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.</span><span class="sxs-lookup"><span data-stu-id="19e1c-547">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="19e1c-548">Přidejte zdroj dat typu **Všeobecné \\ Uživatelský vstupní parametr** pro vyhledání účtu dodavatele v dialogovém okně modulu runtime.</span><span class="sxs-lookup"><span data-stu-id="19e1c-548">Add a data source of the **General \\ User input parameter** type to search for a vendor account in the runtime dialog box.</span></span>
5. <span data-ttu-id="19e1c-549">Pojmenujte nový zdroj dat jako **RequestedAccountNum**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-549">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="19e1c-550">Do pole **Popisek** zadejte **Číslo účtu dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-550">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="19e1c-551">V poli **Název datového typu Operations** ponechte výchozí hodnotu **Popis**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-551">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
6. <span data-ttu-id="19e1c-552">K vyfiltrování dodavatele, o kterého se zajímáte, přidejte zdroj dat typu **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-552">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
7. <span data-ttu-id="19e1c-553">Pojmenujte nový zdroj dat jako **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-553">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
8. <span data-ttu-id="19e1c-554">Označte konfigurovaný zdroj dat **Vendor** jako ukládaný v mezipaměti.</span><span class="sxs-lookup"><span data-stu-id="19e1c-554">Mark the configured **Vendor** data source as cached.</span></span>

    ![Konfigurace komponenty mapování modelu na stránce Návrhář mapování modelu](./media/er-components-inspections-10a.gif)

9. <span data-ttu-id="19e1c-556">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu mapování modelu na stránce **Návrhář mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-556">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![Ověření funkce FILTER použité na zdroj dat dodavatele ukládaný do mezipaměti na stránce návrháře mapování modelů](./media/er-components-inspections-10a.png)

10. <span data-ttu-id="19e1c-558">Všimněte si, že dojde k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="19e1c-558">Notice that a validation error occurs.</span></span> <span data-ttu-id="19e1c-559">Zpráva uvádí, že funkci **FILTER** nelze použít na zdroj dat **Vendor**, který je ukládán do mezipaměti.</span><span class="sxs-lookup"><span data-stu-id="19e1c-559">The message states that the **FILTER** function can't be applied to the cached **Vendor** data source.</span></span>

<span data-ttu-id="19e1c-560">Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění a výběrem příkazu **Spustit** spustíte formát.</span><span class="sxs-lookup"><span data-stu-id="19e1c-560">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run the format.</span></span>

![Chyba za běhu, ke které dojde během provádění mapování formátu na stránce Návrhář formátů](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="19e1c-562">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-562">Automatic resolution</span></span>

<span data-ttu-id="19e1c-563">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="19e1c-563">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="19e1c-564">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-564">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="19e1c-565">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="19e1c-565">Option 1</span></span>

<span data-ttu-id="19e1c-566">Odstraňte příznak **Mezipaměť** ze zdroje dat **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-566">Remove the **Cache** flag from the **Vendor** data source.</span></span> <span data-ttu-id="19e1c-567">Zdroj dat **FilteredVendor** zdroj dat se poté stane spustitelným, ale zdroj dat **Vendor**, na který se odkazuje v tabulce VendTable, bude přístupný pokaždé, když je volán zdroj dat **FilteredVendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-567">The **FilteredVendor** data source will then become executable, but the **Vendor** data source that is referred to in the VendTable table will be accessed every time that the **FilteredVendor** data source is called.</span></span>

#### <a name="option-2"></a><span data-ttu-id="19e1c-568">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="19e1c-568">Option 2</span></span>

<span data-ttu-id="19e1c-569">Změňte výraz zdroje dat **FilteredVendor** z `FILTER(Vendor, Vendor.AccountNum="US-101")` na `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-569">Change the expression of the **FilteredVendor** data source from `FILTER(Vendor, Vendor.AccountNum="US-101")` to `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span> <span data-ttu-id="19e1c-570">V tomto případě bude ke zdroji dat **Vendor**, na který se odkazuje v tabulce VendTable, přistupováno pouze během prvního volání zdroje dat **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-570">In this case, the **Vendor** data source that is referred to in the VendTable table will be accessed only during the first call of the **Vendor** data source.</span></span> <span data-ttu-id="19e1c-571">Výběr záznamů se však provede v paměti.</span><span class="sxs-lookup"><span data-stu-id="19e1c-571">However, the selection of records will be done in memory.</span></span> <span data-ttu-id="19e1c-572">Tento přístup proto může způsobit špatný výkon.</span><span class="sxs-lookup"><span data-stu-id="19e1c-572">Therefore, this approach can cause poor performance.</span></span>

## <a name="missing-binding"></a><a id="i11"></a><span data-ttu-id="19e1c-573">Chybějící vazba</span><span class="sxs-lookup"><span data-stu-id="19e1c-573">Missing binding</span></span>

<span data-ttu-id="19e1c-574">Když konfigurujete komponentu formátu ER, nabídne se základní datový model ER jako výchozí zdroj dat pro formát ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-574">When you configure an ER format component, the base ER data model is offered as a default data source for the ER format.</span></span> <span data-ttu-id="19e1c-575">Když je spuštěn konfigurovaný formát ER, použije se k vyplnění datového modelu aplikačními daty [výchozí mapování modelu](er-country-dependent-model-mapping.md) pro základní model.</span><span class="sxs-lookup"><span data-stu-id="19e1c-575">When the configured ER format is run, the [default model mapping](er-country-dependent-model-mapping.md) for the base model is used to fill the data model with application data.</span></span> <span data-ttu-id="19e1c-576">Návrhář formátu ER zobrazí upozornění, pokud vytvoříte vazbu prvku formátu na položku datového modelu, která není vázána na žádný zdroj dat v tom mapování modelu, který je aktuálně vybrán jako výchozí mapování modelu pro upravitelný formát.</span><span class="sxs-lookup"><span data-stu-id="19e1c-576">The ER format designer shows a warning if you bind a format element to a data model item that isn't bound to any data source in the model mapping that is currently selected as the default model mapping for the editable format.</span></span> <span data-ttu-id="19e1c-577">Tento typ vazby nelze spustit za běhu, protože spuštěný formát nemůže vyplnit vázaný prvek daty aplikace.</span><span class="sxs-lookup"><span data-stu-id="19e1c-577">This type of binding can't be run at runtime, because the format that runs can't fill a bound element with application data.</span></span> <span data-ttu-id="19e1c-578">Proto za běhu dojde k chybě.</span><span class="sxs-lookup"><span data-stu-id="19e1c-578">Therefore, an error occurs at runtime.</span></span>

<span data-ttu-id="19e1c-579">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="19e1c-579">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="19e1c-580">Začněte konfigurovat datový model ER, mapování modelu ER a komponenty formátu ER současně.</span><span class="sxs-lookup"><span data-stu-id="19e1c-580">Start to configure the ER data model, the ER model mapping, and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="19e1c-581">Ve stromu datového modelu přidejte kořenovou položku s názvem **Root3**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-581">In the data model tree, add a root item that is named **Root3**.</span></span>
3. <span data-ttu-id="19e1c-582">Upravte položku **Root3** a přidejte do ní novou vnořenou položku typu **Seznam záznamů**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-582">Modify the **Root3** item by adding a new nested item of the **Record list** type.</span></span>
4. <span data-ttu-id="19e1c-583">Pojmenujte novou vnořenou položku jako **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-583">Name the new nested item **Vendor**.</span></span>
5. <span data-ttu-id="19e1c-584">Upravte položku **Vendor** následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="19e1c-584">Modify the **Vendor** item in the following way:</span></span>

    - <span data-ttu-id="19e1c-585">Přidejte vnořené pole typu **Řetězec** a pojmenujte jej jako **Name**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-585">Add a nested field of the **String** type, and name it **Name**.</span></span>
    - <span data-ttu-id="19e1c-586">Přidejte vnořené pole typu **Řetězec** a pojmenujte jej jako **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-586">Add a nested field of the **String** type, and name it **AccountNumber**.</span></span>

    ![Přidání vnořených polí k položce dodavatele na stránce Datový model](./media/er-components-inspections-11a.png)

6. <span data-ttu-id="19e1c-588">V podokně zdrojů dat mapování modelu přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-588">In the model mapping data sources pane, add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="19e1c-589">Pojmenujte nový zdroj dat jako **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-589">Name the new data source **Vendor**.</span></span> <span data-ttu-id="19e1c-590">V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.</span><span class="sxs-lookup"><span data-stu-id="19e1c-590">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="19e1c-591">Přidejte zdroj dat typu **Všeobecné \\ Uživatelský vstupní parametr** pro získání informací o účtu dodavatele v dialogovém okně modulu runtime.</span><span class="sxs-lookup"><span data-stu-id="19e1c-591">Add a data source of the **General \\ User input parameter** type to inquire about a vendor account in the runtime dialog box.</span></span>
<span data-ttu-id="19e1c-592">9 Pojmenujte nový zdroj dat jako **RequestedAccountNum**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-592">9 Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="19e1c-593">Do pole **Popisek** zadejte **Číslo účtu dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-593">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="19e1c-594">V poli **Název datového typu Operations** ponechte výchozí hodnotu **Popis**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-594">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
10. <span data-ttu-id="19e1c-595">K vyfiltrování dodavatele, o kterého se zajímáte, přidejte zdroj dat typu **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-595">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
11. <span data-ttu-id="19e1c-596">Pojmenujte nový zdroj dat jako **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="19e1c-596">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
12. <span data-ttu-id="19e1c-597">Vytvořte vazbu položek datového modelu na konfigurované zdroje dat následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="19e1c-597">Bind the data model items to configured data sources in the following way:</span></span>

    - <span data-ttu-id="19e1c-598">Vytvořte vazbu položky **FilteredVendor** na položku **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-598">Bind **FilteredVendor** to **Vendor**.</span></span>
    - <span data-ttu-id="19e1c-599">Vytvořte vazbu položky **FilteredVendor.AccountNum** na položku **Vendor.AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-599">Bind **FilteredVendor.AccountNum** to **Vendor.AccountNumber**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="19e1c-600">Pole datového modelu **Vendor.Name** zůstává nevázané.</span><span class="sxs-lookup"><span data-stu-id="19e1c-600">The **Vendor.Name** data model field remains unbound.</span></span>

    ![Položky datového modelu vázané na konfigurované zdroje dat a položka datového režimu na stránce Návrháře mapování modelů](./media/er-components-inspections-11b.png)

13. <span data-ttu-id="19e1c-602">Ve stromu struktury formátu přidejte následující položky, které generují odchozí dokument ve formátu XML obsahující podrobnosti o dodavatelích, kteří vás zajímají:</span><span class="sxs-lookup"><span data-stu-id="19e1c-602">In the format structure tree, add the following items to generate an outbound document in XML format that contains the details of the vendors that are inquired about:</span></span>

    1. <span data-ttu-id="19e1c-603">Přidejte kořenový prvek XML **Statement**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-603">Add the **Statement** root XML element.</span></span>
    2. <span data-ttu-id="19e1c-604">U prvku XML **Statement** přidejte vnořený prvek XML **Party**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-604">For the **Statement** XML element, add the nested **Party** XML element.</span></span>
    3. <span data-ttu-id="19e1c-605">U prvku XML **Party** přidejte následující vnořené atributy XML:</span><span class="sxs-lookup"><span data-stu-id="19e1c-605">For the **Party** XML element, add the following nested XML attributes:</span></span>

        - <span data-ttu-id="19e1c-606">Jméno</span><span class="sxs-lookup"><span data-stu-id="19e1c-606">Name</span></span>
        - <span data-ttu-id="19e1c-607">AccountNum</span><span class="sxs-lookup"><span data-stu-id="19e1c-607">AccountNum</span></span>

14. <span data-ttu-id="19e1c-608">Navažte prvky formátu na poskytnuté zdroje dat následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="19e1c-608">Bind the format elements to provided data sources in the following way:</span></span>

    - <span data-ttu-id="19e1c-609">Vytvořte vazbu prvku formátu **Statement\\Party** na položku zdroje dat **model.Vendor**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-609">Bind the **Statement\\Party** format element to the **model.Vendor** data source item.</span></span>
    - <span data-ttu-id="19e1c-610">Vytvořte vazbu prvku formátu **Statement\\Party\\Name** na pole zdroje dat **model.Vendor.Name**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-610">Bind the **Statement\\Party\\Name** format element to the **model.Vendor.Name** data source field.</span></span>
    - <span data-ttu-id="19e1c-611">Vytvořte vazbu prvku formátu **Statement\\Party\\AccountNum** na pole zdroje dat **model.Vendor.AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-611">Bind the **Statement\\Party\\AccountNum** format element to the **model.Vendor.AccountNumber** data source field.</span></span>

15. <span data-ttu-id="19e1c-612">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu formátu na stránce **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-612">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![Ověření komponenty formátu ER na stránce Návrhář formátů](./media/er-components-inspections-11c.png)

16. <span data-ttu-id="19e1c-614">Všimněte si, že se zobrazí upozornění ověření.</span><span class="sxs-lookup"><span data-stu-id="19e1c-614">Notice that a validation warning occurs.</span></span> <span data-ttu-id="19e1c-615">Zpráva uvádí, že pole zdroje dat **model.Vendor.Name** není vázáno na žádný zdroj dat v mapování modelu, který je konfigurován pro použití ve formátu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-615">The message states that the **model.Vendor.Name** data source field isn't bound to any data source in the model mapping that is configured to be used by the format.</span></span> <span data-ttu-id="19e1c-616">Proto prvek formátu **Statement\\Party\\Name** nemusí být za běhu vyplněn a může dojít k výjimce za běhu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-616">Therefore, the **Statement\\Party\\Name** format element might not be filled at runtime, and a runtime exception might occur.</span></span>

    ![Ověření komponenty formátu ER na stránce Návrhář formátů](./media/er-components-inspections-11d.png)

<span data-ttu-id="19e1c-618">Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění a výběrem příkazu **Spustit** spustíte formát.</span><span class="sxs-lookup"><span data-stu-id="19e1c-618">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run the format.</span></span>

![Spuštění upravitelného formátu na stránce Návrhář formátů](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="19e1c-620">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-620">Automatic resolution</span></span>

<span data-ttu-id="19e1c-621">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="19e1c-621">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="19e1c-622">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-622">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="19e1c-623">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="19e1c-623">Option 1</span></span>

<span data-ttu-id="19e1c-624">Upravte konfigurované mapování modelu přidáním vazby pro pole zdroje dat **model.Vendor.Name**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-624">Modify the configured model mapping by adding a binding for the **model.Vendor.Name** data source field.</span></span>

#### <a name="option-2"></a><span data-ttu-id="19e1c-625">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="19e1c-625">Option 2</span></span>

<span data-ttu-id="19e1c-626">Upravte konfigurovaný formát odebráním vazby pro prvek formátu **Statement\\Party\\Name**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-626">Modify the configured format by removing a binding for the **Statement\\Party\\Name** format element.</span></span>

## <a name="not-linked-template"></a><a id="i12"></a><span data-ttu-id="19e1c-627">Nepropojená šablona</span><span class="sxs-lookup"><span data-stu-id="19e1c-627">Not linked template</span></span>

<span data-ttu-id="19e1c-628">Když [ručně](er-fillable-excel.md#manual-entry) nakonfigurujete komponentu formátu ER tak, aby pomocí šablony generovala odchozí dokument, musíte ručně přidat prvek **Excel\\File**, přidat požadovanou šablonu jako přílohu upravitelné komponenty, a vybrat tuto přílohu v přidaném prvku **Excel\\File**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-628">When you [manually](er-fillable-excel.md#manual-entry) configure an ER format component to use a template to generate an outbound document, you must manually add the **Excel\\File** element, add the required template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span> <span data-ttu-id="19e1c-629">Tímto způsobem dáváte najevo, že přidaný prvek za běhu vyplní vybranou šablonu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-629">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="19e1c-630">Při konfiguraci verze komponenty formátu ve [stavu](general-electronic-reporting.md#component-versioning) **Návrh** můžete do upravitelné komponenty přidat několik šablon a poté vybrat každou šablonu v prvku **Excel\\File**, aby spustila formát ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-630">When you configure a format component version in **Draft** [status](general-electronic-reporting.md#component-versioning), you might add several templates to the editable component, and then select each template in the **Excel\\File** element to run the ER format.</span></span> <span data-ttu-id="19e1c-631">Tímto způsobem můžete vidět, jak jsou různé šablony vyplněny za běhu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-631">In this way, you can see how different templates are filled at runtime.</span></span> <span data-ttu-id="19e1c-632">Pokud máte šablony, které nejsou vybrány v žádném prvku **Excel\\File**, návrhář formátu ER vás upozorní, že tyto šablony budou odstraněny z upravitelné verze komponenty formátu ER, když se jeho stav změní z **Návrh** na **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-632">If you have templates that aren't selected in any **Excel\\File** elements, the ER format designer warns you that those templates will be deleted from the editable ER format component version when its status is changed from **Draft** to **Completed**.</span></span>

<span data-ttu-id="19e1c-633">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="19e1c-633">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="19e1c-634">Začněte konfigurací komponenty formátu ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-634">Start to configure the ER format component.</span></span>
2. <span data-ttu-id="19e1c-635">Ve stromu struktury formátu přidejte prvek **Excel\\File**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-635">In the format structure tree, add the **Excel\\File** element.</span></span>
3. <span data-ttu-id="19e1c-636">U prvku **Excel\\File**, který jste právě přidali, přidejte soubor sešitu aplikace Excel **A.xlsx** jako přílohu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-636">For the **Excel\\File** element that you just added, add an Excel workbook file, **A.xlsx**, as an attachment.</span></span> <span data-ttu-id="19e1c-637">Použijte typ dokumentu, který je konfigurován v [parametrech ER](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) k určení úložiště šablon formátu ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-637">Use the document type that is configured in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) to specify the storage of ER format templates.</span></span>
4. <span data-ttu-id="19e1c-638">U prvku **Excel\\File**, který jste právě přidali, přidejte další soubor sešitu aplikace Excel **B.xlsx** jako přílohu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-638">For the **Excel\\File** element, add another Excel workbook file, **B.xlsx**, as an attachment.</span></span> <span data-ttu-id="19e1c-639">Použijte stejný typ dokumentu jako u souboru sešitu A.</span><span class="sxs-lookup"><span data-stu-id="19e1c-639">Use the same document type that is used for workbook file A.</span></span>
5. <span data-ttu-id="19e1c-640">V prvku **Excel\\File** vyberte soubor sešitu A.</span><span class="sxs-lookup"><span data-stu-id="19e1c-640">In the **Excel\\File** element, select workbook file A.</span></span>
6. <span data-ttu-id="19e1c-641">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu formátu na stránce **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-641">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![Ověření komponenty upravitelného formátu souboru sešitu na stránce Návrhář formátů](./media/er-components-inspections-12a.gif)

7. <span data-ttu-id="19e1c-643">Všimněte si, že se zobrazí upozornění ověření.</span><span class="sxs-lookup"><span data-stu-id="19e1c-643">Notice that a validation warning occurs.</span></span> <span data-ttu-id="19e1c-644">Zpráva uvádí, že soubor sešitu **B.xlsx** není propojen se žádnými komponentami a že bude odstraněn po změně stavu verze konfigurace.</span><span class="sxs-lookup"><span data-stu-id="19e1c-644">The message states that workbook file **B.xlsx** isn't linked to any components, and that it will be removed after the status of the configuration version is changed.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="19e1c-645">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-645">Automatic resolution</span></span>

<span data-ttu-id="19e1c-646">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="19e1c-646">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="19e1c-647">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-647">Manual resolution</span></span>

<span data-ttu-id="19e1c-648">Upravte konfigurovaný formát odebráním všech šablon, které nejsou propojeny s žádným prvkem **Excel\\File**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-648">Modify the configured format by removing all templates that aren't linked to any **Excel\\File** element.</span></span>

## <a name="not-synced-format"></a><a id="i13"></a><span data-ttu-id="19e1c-649">Nesynchronizovaný formát</span><span class="sxs-lookup"><span data-stu-id="19e1c-649">Not synced format</span></span>

<span data-ttu-id="19e1c-650">Když [nakonfigurujete](er-fillable-excel.md) komponentu formátu ER tak, aby pomocí šablony Excelu generovala odchozí dokument, můžete ručně přidat prvek **Excel\\File**, přidat požadovanou šablonu jako přílohu upravitelné komponenty, a vybrat tuto přílohu v přidaném prvku **Excel\\File**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-650">When you [configure](er-fillable-excel.md) an ER format component to use an Excel template to generate an outbound document, you can manually add the **Excel\\File** element, add the required template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span> <span data-ttu-id="19e1c-651">Tímto způsobem dáváte najevo, že přidaný prvek za běhu vyplní vybranou šablonu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-651">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="19e1c-652">Protože přidaná šablona Excelu byla navržena externě, může upravitelný formát ER obsahovat názvy aplikace Excel, které v přidané šabloně chybí.</span><span class="sxs-lookup"><span data-stu-id="19e1c-652">Because the added Excel template has been externally designed, the editable ER format might contain Excel names that are missing from the added template.</span></span> <span data-ttu-id="19e1c-653">Návrhář formátu ER vás upozorní na jakékoli nesrovnalosti mezi vlastnostmi prvků formátu ER odkazující na názvy, které nejsou zahrnuty v přidané šabloně Excelu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-653">The ER format designer warns you about any inconsistencies between the properties of the ER format elements that refer to names that aren't included in the added Excel template.</span></span>

<span data-ttu-id="19e1c-654">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="19e1c-654">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="19e1c-655">Začněte konfigurací komponenty formátu ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-655">Start to configure the ER format component.</span></span>
2. <span data-ttu-id="19e1c-656">Ve stromu struktury formátu přidejte prvek **Excel\\File** s názvem **Report**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-656">In the format structure tree, add the **Excel\\File** element **Report**.</span></span>
3. <span data-ttu-id="19e1c-657">U prvku **Excel\\File**, který jste právě přidali, přidejte soubor sešitu aplikace Excel **A.xlsx** jako přílohu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-657">For the **Excel\\File** element that you just added, add an Excel workbook file, **A.xlsx**, as an attachment.</span></span> <span data-ttu-id="19e1c-658">Použijte typ dokumentu, který je konfigurován v [parametrech ER](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) k určení úložiště šablon formátu ER.</span><span class="sxs-lookup"><span data-stu-id="19e1c-658">Use the document type that is configured in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) to specify the storage of ER format templates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="19e1c-659">Ujistěte se, že přidaný sešit Excelu neobsahuje název **ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-659">Make sure that the added Excel workbook doesn't contain the name **ReportTitle**.</span></span>

4. <span data-ttu-id="19e1c-660">Přidejte následující prvek **Excel\\Cell** s názvem **Title** jako vnořený prvek prvku **Report**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-660">Add the following **Excel\\Cell** element **Title** as the nested element of the **Report** element.</span></span> <span data-ttu-id="19e1c-661">Do pole **Oblast Excelu** zadejte **ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-661">In the **Excel range** field, enter **ReportTitle**.</span></span>
5. <span data-ttu-id="19e1c-662">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu formátu na stránce **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="19e1c-662">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![Ověření vnořených prvků a polí na stránce Návrhář formátu](./media/er-components-inspections-13a.png)

6. <span data-ttu-id="19e1c-664">Všimněte si, že se zobrazí upozornění ověření.</span><span class="sxs-lookup"><span data-stu-id="19e1c-664">Notice that a validation warning occurs.</span></span> <span data-ttu-id="19e1c-665">Zpráva uvádí, že název **ReportTitle** neexistuje v listu **Sheet1** šablony aplikace Excel, kterou používáte.</span><span class="sxs-lookup"><span data-stu-id="19e1c-665">The message states that the name **ReportTitle** doesn't exist on sheet **Sheet1** of the Excel template that you're using.</span></span>

    ![Upozornění ověření na fakt, že název ReportTitle neexistuje na listu Sheet1 šablony aplikace Excel](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="19e1c-667">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-667">Automatic resolution</span></span>

<span data-ttu-id="19e1c-668">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="19e1c-668">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="19e1c-669">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="19e1c-669">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="19e1c-670">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="19e1c-670">Option 1</span></span>

<span data-ttu-id="19e1c-671">Upravte konfigurovaný formát odebráním všech prvků odkazujících na názvy aplikace Excel, které v šabloně chybí.</span><span class="sxs-lookup"><span data-stu-id="19e1c-671">Modify the configured format by removing all elements that refer to Excel names that are missing from the template.</span></span>

#### <a name="option-2"></a><span data-ttu-id="19e1c-672">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="19e1c-672">Option 2</span></span>

<span data-ttu-id="19e1c-673">[Aktualizujte](er-fillable-excel.md#template-import) upravitelný formát ER importem šablony aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="19e1c-673">[Update](er-fillable-excel.md#template-import) the editable ER format by importing an Excel template.</span></span> <span data-ttu-id="19e1c-674">Struktura upravitelného formátu ER bude [synchronizována](modify-electronic-reporting-format-reapply-excel-template.md) se strukturou importované šablony Excelu.</span><span class="sxs-lookup"><span data-stu-id="19e1c-674">The structure of the editable ER format will be [synced](modify-electronic-reporting-format-reapply-excel-template.md) with the structure of the imported Excel template.</span></span>

### <a name="additional-consideration"></a><span data-ttu-id="19e1c-675">Další faktor ke zvážení</span><span class="sxs-lookup"><span data-stu-id="19e1c-675">Additional consideration</span></span>

<span data-ttu-id="19e1c-676">Chcete-li se naučit synchronizovat strukturu formátu se šablonou ER v editoru šablon [Správy obchodních dokumentů](er-business-document-management.md), přečtěte si část [Aktualizace struktury šablony obchodního dokumentu](er-bdm-update-structure.md).</span><span class="sxs-lookup"><span data-stu-id="19e1c-676">To learn how the format structure can be synced with an ER template in the template editor of [Business document management](er-business-document-management.md), see [Update the structure of a business document template](er-bdm-update-structure.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19e1c-677">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="19e1c-677">Additional resources</span></span>

[<span data-ttu-id="19e1c-678">Funkce elektronického výkaznictví ALLITEMS</span><span class="sxs-lookup"><span data-stu-id="19e1c-678">ALLITEMS ER function</span></span>](er-functions-list-allitems.md)

[<span data-ttu-id="19e1c-679">Funkce elektronického výkaznictví ALLITEMSQUERY</span><span class="sxs-lookup"><span data-stu-id="19e1c-679">ALLITEMSQUERY ER function</span></span>](er-functions-list-allitemsquery.md)

[<span data-ttu-id="19e1c-680">Funkce el. výkaznictví INT64VALUE</span><span class="sxs-lookup"><span data-stu-id="19e1c-680">INT64VALUE ER function</span></span>](er-functions-conversion-int64value.md)

[<span data-ttu-id="19e1c-681">Funkce INTVALUE ER</span><span class="sxs-lookup"><span data-stu-id="19e1c-681">INTVALUE ER function</span></span>](er-functions-conversion-intvalue.md)

[<span data-ttu-id="19e1c-682">Funkce elektronického výkaznictví FILTER</span><span class="sxs-lookup"><span data-stu-id="19e1c-682">FILTER ER function</span></span>](er-functions-list-filter.md)

[<span data-ttu-id="19e1c-683">Funkce elektronického výkaznictví WHERE</span><span class="sxs-lookup"><span data-stu-id="19e1c-683">WHERE ER function</span></span>](er-functions-list-where.md)

[<span data-ttu-id="19e1c-684">Použití zdrojů dat JOIN v mapování modelu ER k získání dat z více aplikačních tabulek</span><span class="sxs-lookup"><span data-stu-id="19e1c-684">Use JOIN data sources to get data from multiple application tables in ER model mappings</span></span>](er-join-data-sources.md)

[<span data-ttu-id="19e1c-685">Sledování provedení formátů elektronického výkaznictví pro při řešení problémů s výkonem</span><span class="sxs-lookup"><span data-stu-id="19e1c-685">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="19e1c-686">Přehled správy obchodních dokumentů</span><span class="sxs-lookup"><span data-stu-id="19e1c-686">Business document management overview</span></span>](er-business-document-management.md)
