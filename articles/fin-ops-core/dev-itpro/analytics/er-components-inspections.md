---
title: Kontrola konfigurované komponenty ER zabraňující problémům za běhu
description: Toto téma vysvětluje, jak zkontrolovat konfigurované komponenty elektronického výkaznictví (ER), aby se předešlo problémům za běhu, ke kterým může dojít.
author: NickSelin
manager: AnnBe
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86db6dc27a8a76e90494e3dc7a7cc9c828f9ec37
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574118"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a><span data-ttu-id="c4408-103">Kontrola konfigurované komponenty ER zabraňující problémům za běhu</span><span class="sxs-lookup"><span data-stu-id="c4408-103">Inspect the configured ER component to prevent runtime issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c4408-104">Každá konfigurovaná komponenta pro [formátování](general-electronic-reporting.md#FormatComponentOutbound) a [mapování modelu](general-electronic-reporting.md#data-model-and-model-mapping-components) [elektronického výkaznictví (ER)](general-electronic-reporting.md) může projít [ověřením platnosti](er-fillable-excel.md#validate-an-er-format) v době návrhu.</span><span class="sxs-lookup"><span data-stu-id="c4408-104">Every configured [Electronic reporting (ER)](general-electronic-reporting.md) [format](general-electronic-reporting.md#FormatComponentOutbound) and [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component can be [validated](er-fillable-excel.md#validate-an-er-format) at design time.</span></span> <span data-ttu-id="c4408-105">Během tohoto ověřování se provádí kontrola konzistence, která pomáhá předcházet výskytu problémů za běhu, jako jsou chyby spuštění a snížení výkonu.</span><span class="sxs-lookup"><span data-stu-id="c4408-105">During this validation, a consistency check runs to help prevent runtime issues that might occur, such as execution errors and performance degradation.</span></span> <span data-ttu-id="c4408-106">U každého nalezeného problému poskytuje kontrola cestu k problematickému prvku.</span><span class="sxs-lookup"><span data-stu-id="c4408-106">For every issue that is found, the check provides the path of a problematic element.</span></span> <span data-ttu-id="c4408-107">U některých problémů je k dispozici automatická oprava.</span><span class="sxs-lookup"><span data-stu-id="c4408-107">For some issues, an automatic fix is available.</span></span>

<span data-ttu-id="c4408-108">Ve výchozím nastavení se v následujících případech ověření automaticky použije u konfigurace ER, která obsahuje dříve zmíněné komponenty ER:</span><span class="sxs-lookup"><span data-stu-id="c4408-108">By default, the validation is automatically applied in the following cases for an ER configuration that contains the previously mentioned ER components:</span></span>

- <span data-ttu-id="c4408-109">[Importujte](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) novou [verzi](general-electronic-reporting.md#component-versioning) konfigurace ER do vaší instance Microsoftu Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="c4408-109">You [import](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) a new [version](general-electronic-reporting.md#component-versioning) of an ER configuration into your instance of Microsoft Dynamics 365 Finance.</span></span>
- <span data-ttu-id="c4408-110">Změňte [stav](general-electronic-reporting.md#component-versioning) upravitelné konfigurace ER z hodnoty **Koncept** na **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="c4408-110">You change the [status](general-electronic-reporting.md#component-versioning) of the editable ER configuration from **Draft** to **Completed**.</span></span>
- <span data-ttu-id="c4408-111">[Přeneste změny](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) do upravitelné konfigurace ER použitím nové základní verze.</span><span class="sxs-lookup"><span data-stu-id="c4408-111">You [rebase](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) an editable ER configuration by applying a new base version.</span></span>

<span data-ttu-id="c4408-112">Toto ověření můžete explicitně spustit.</span><span class="sxs-lookup"><span data-stu-id="c4408-112">You can explicitly run this validation.</span></span> <span data-ttu-id="c4408-113">Vyberte jednu z následujících tří možností a postupujte podle uvedených kroků:</span><span class="sxs-lookup"><span data-stu-id="c4408-113">Select one of the following three options, and follow the steps that are provided:</span></span>

- <span data-ttu-id="c4408-114">Možnost 1:</span><span class="sxs-lookup"><span data-stu-id="c4408-114">Option 1:</span></span>

    1. <span data-ttu-id="c4408-115">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="c4408-115">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="c4408-116">Ve stromu konfigurací v levém podokně vyberte požadovanou konfiguraci ER, která obsahuje komponentu formátu nebo mapování modelu ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-116">In the configurations tree in the left pane, select the desired ER configuration that contains the ER format or ER model mapping component.</span></span>
    3. <span data-ttu-id="c4408-117">Na pevné záložce **Verze** vyberte požadovanou verzi vybrané konfigurace ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-117">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="c4408-118">V podokně Akce klikněte na možnost **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="c4408-118">On the Action Pane, select **Validate**.</span></span>

- <span data-ttu-id="c4408-119">Možnost 2, pro formát ER:</span><span class="sxs-lookup"><span data-stu-id="c4408-119">Option 2, for an ER format:</span></span>

    1. <span data-ttu-id="c4408-120">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="c4408-120">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="c4408-121">Ve stromu konfigurací v levém podokně vyberte požadovanou konfiguraci ER, která obsahuje komponentu formátu ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-121">In the configurations tree in the left pane, select the desired ER configuration that contains the ER format component.</span></span>
    3. <span data-ttu-id="c4408-122">Na pevné záložce **Verze** vyberte požadovanou verzi vybrané konfigurace ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-122">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="c4408-123">V podokně akcí zvolte **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="c4408-123">On the Action Pane, select **Designer**.</span></span>
    5. <span data-ttu-id="c4408-124">Na stránce **Návrhář formátu** v podokně akcí vyberte **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="c4408-124">On the **Format designer** page, on the Action Pane, select **Validate**.</span></span>

- <span data-ttu-id="c4408-125">Možnost 3, pro mapování modelu ER:</span><span class="sxs-lookup"><span data-stu-id="c4408-125">Option 3, for an ER model mapping:</span></span>

    1. <span data-ttu-id="c4408-126">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="c4408-126">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
    2. <span data-ttu-id="c4408-127">Ve stromu konfigurací v levém podokně vyberte požadovanou konfiguraci ER, která obsahuje komponentu mapování modelu ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-127">In the configurations tree in the left pane, select the desired ER configuration that contains the ER model mapping component.</span></span>
    3. <span data-ttu-id="c4408-128">Na pevné záložce **Verze** vyberte požadovanou verzi vybrané konfigurace ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-128">On the **Versions** FastTab, select the desired version of the selected ER configuration.</span></span>
    4. <span data-ttu-id="c4408-129">V podokně akcí zvolte **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="c4408-129">On the Action Pane, select **Designer**.</span></span>
    5. <span data-ttu-id="c4408-130">Na stránce **Mapování modelu na zdroj dat** v podokně Akce vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="c4408-130">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>
    6. <span data-ttu-id="c4408-131">Na stránce **Návrhář mapování modelu** v podokně Akce vyberte možnost **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="c4408-131">On the **Model mapping designer** page, on the Action Pane, select **Validate**.</span></span>

<span data-ttu-id="c4408-132">Chcete-li přeskočit ověření při importu konfigurace, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="c4408-132">To skip the validation when the configuration is imported, follow these steps.</span></span>

1. <span data-ttu-id="c4408-133">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="c4408-133">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="c4408-134">Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="c4408-134">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="c4408-135">Nastavte možnost **Po importu ověřit konfiguraci** na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="c4408-135">Set the **Validate the configuration after importing** option to **No**.</span></span>

<span data-ttu-id="c4408-136">Chcete-li přeskočit ověření, když je změněn stav verze nebo základ, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="c4408-136">To skip the validation when you change or rebase the version's status, follow these steps.</span></span>

1. <span data-ttu-id="c4408-137">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="c4408-137">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="c4408-138">Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="c4408-138">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="c4408-139">Nastavte možnost **Přeskočit ověření při změně stavu konfigurace a základu** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="c4408-139">Set the **Skip validation at configuration's status change and rebase** option to **Yes**.</span></span>

<span data-ttu-id="c4408-140">ER používá k seskupení inspekcí kontroly konzistence následující kategorie:</span><span class="sxs-lookup"><span data-stu-id="c4408-140">ER uses the following categories to group consistency check inspections:</span></span>

- <span data-ttu-id="c4408-141">**Proveditelnost** - Inspekce, které detekují kritické problémy, ke kterým by za běhu mohlo dojít.</span><span class="sxs-lookup"><span data-stu-id="c4408-141">**Executability** – Inspections that detect critical issues that might occur at runtime.</span></span> <span data-ttu-id="c4408-142">Tyto problémy jsou většinou na úrovni **Chyba**.</span><span class="sxs-lookup"><span data-stu-id="c4408-142">These issues are mostly at an **Error** level.</span></span> 
- <span data-ttu-id="c4408-143">**Výkon** - Inspekce, které detekují problémy, které by mohly způsobit neefektivní provádění konfigurovaných komponent ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-143">**Performance** – Inspections that detect issues that might cause inefficient execution of configured ER components.</span></span> <span data-ttu-id="c4408-144">Tyto problémy jsou většinou na úrovni **Upozornění**.</span><span class="sxs-lookup"><span data-stu-id="c4408-144">These issues are mostly at a **Warning** level.</span></span>
- <span data-ttu-id="c4408-145">**Integrita dat** - Inspekce, které detekují problémy, které by mohly způsobit ztrátu dat nebo problémy běhového prostředí.</span><span class="sxs-lookup"><span data-stu-id="c4408-145">**Data integrity** – Inspections that detect issues that might cause data loss or runtime issues.</span></span> <span data-ttu-id="c4408-146">Tyto problémy jsou většinou na úrovni **Upozornění**.</span><span class="sxs-lookup"><span data-stu-id="c4408-146">These issues are mostly at a **Warning** level.</span></span>

## <a name="list-of-inspections"></a><span data-ttu-id="c4408-147">Seznam inspekcí</span><span class="sxs-lookup"><span data-stu-id="c4408-147">List of inspections</span></span>

<span data-ttu-id="c4408-148">Následující tabulka poskytuje přehled inspekcí, které ER poskytuje.</span><span class="sxs-lookup"><span data-stu-id="c4408-148">The following table provides an overview of the inspections that ER provides.</span></span> <span data-ttu-id="c4408-149">Další informace o těchto inspekcích získáte pomocí odkazů v prvním sloupci, kterými přejdete na příslušné části tohoto tématu.</span><span class="sxs-lookup"><span data-stu-id="c4408-149">For more information about these inspections, use the links in the first column to go to the relevant sections of this topic.</span></span> <span data-ttu-id="c4408-150">Tyto oddíly vysvětlují typy komponent, u kterých ER poskytuje kontroly, a návod na rekonfiguraci komponent ER, abyste zabránili problémům.</span><span class="sxs-lookup"><span data-stu-id="c4408-150">Those sections explain the types of components that ER provides inspections for and how you can reconfigure ER components to help prevent issues.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c4408-151">Jméno</span><span class="sxs-lookup"><span data-stu-id="c4408-151">Name</span></span></th>
<th><span data-ttu-id="c4408-152">Kategorie</span><span class="sxs-lookup"><span data-stu-id="c4408-152">Category</span></span></th>
<th><span data-ttu-id="c4408-153">Úroveň</span><span class="sxs-lookup"><span data-stu-id="c4408-153">Level</span></span></th>
<th><span data-ttu-id="c4408-154">Zpráva</span><span class="sxs-lookup"><span data-stu-id="c4408-154">Message</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c4408-155"><a href='#i1'>Převod typu</a></span><span class="sxs-lookup"><span data-stu-id="c4408-155"><a href='#i1'>Type conversion</a></span></span></td>
<td><span data-ttu-id="c4408-156">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="c4408-156">Executability</span></span></td>
<td><span data-ttu-id="c4408-157">Chyba</span><span class="sxs-lookup"><span data-stu-id="c4408-157">Error</span></span></td>
<td>
<p><span data-ttu-id="c4408-158">Nelze převést výraz typu &lt;typ&gt; na pole typu &lt;typ&gt;.</span><span class="sxs-lookup"><span data-stu-id="c4408-158">Cannot convert expression of type &lt;type&gt; to field of type &lt;type&gt;.</span></span></p>
<p><span data-ttu-id="c4408-159"><b>Chyba za běhu:</b> Výjimka pro typ</span><span class="sxs-lookup"><span data-stu-id="c4408-159"><b>Runtime error:</b> Exception for type</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="c4408-160"><a href='#i2'>Kompatibilita typů</a></span><span class="sxs-lookup"><span data-stu-id="c4408-160"><a href='#i2'>Type compatibility</a></span></span></td>
<td><span data-ttu-id="c4408-161">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="c4408-161">Executability</span></span></td>
<td><span data-ttu-id="c4408-162">Chyba</span><span class="sxs-lookup"><span data-stu-id="c4408-162">Error</span></span></td>
<td>
<p><span data-ttu-id="c4408-163">Konfigurovaný výraz nelze použít jako vazbu aktuálního prvku formátu ke zdroji dat, protože tento výraz vrací hodnotu datového typu &lt;typ&gt;, tedy mimo rámec datových typů, které jsou podporovány aktuálním prvkem formátu typu &lt;typ&gt;.</span><span class="sxs-lookup"><span data-stu-id="c4408-163">The configured expression cannot be used as the binding of the current format element to a data source as this expression returns value of the data type &lt;type&gt; that is beyond the scope of data types that are supported by the current format element of type &lt;type&gt;.</span></span></p>
<p><span data-ttu-id="c4408-164"><b>Chyba za běhu:</b> Výjimka typu</span><span class="sxs-lookup"><span data-stu-id="c4408-164"><b>Runtime error:</b> Exception of type</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="c4408-165"><a href='#i3'>Chybějící konfigurační prvek</a></span><span class="sxs-lookup"><span data-stu-id="c4408-165"><a href='#i3'>Missing configuration element</a></span></span></td>
<td><span data-ttu-id="c4408-166">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="c4408-166">Executability</span></span></td>
<td><span data-ttu-id="c4408-167">Chyba</span><span class="sxs-lookup"><span data-stu-id="c4408-167">Error</span></span></td>
<td>
<p><span data-ttu-id="c4408-168">Cesta nenalezena: &lt;cesta&gt;.</span><span class="sxs-lookup"><span data-stu-id="c4408-168">Path not found &lt;path&gt;.</span></span></p>
<p><span data-ttu-id="c4408-169"><b>Chyba za běhu:</b> Prvek konfigurace &lt; cesta&gt; nenalezen</span><span class="sxs-lookup"><span data-stu-id="c4408-169"><b>Runtime error:</b> Element of the configuration &lt;path&gt; not found</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="c4408-170"><a href='#i4'>Spustitelnost výrazu s funkcí FILTER</a></span><span class="sxs-lookup"><span data-stu-id="c4408-170"><a href='#i4'>Executability of an expression with FILTER function</a></span></span></td>
<td><span data-ttu-id="c4408-171">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="c4408-171">Executability</span></span></td>
<td><span data-ttu-id="c4408-172">Chyba</span><span class="sxs-lookup"><span data-stu-id="c4408-172">Error</span></span></td>
<td>
<p><span data-ttu-id="c4408-173">Výraz seznamu funkce FILTER není dotazovatelný.</span><span class="sxs-lookup"><span data-stu-id="c4408-173">The list expression of FILTER function is not queryable.</span></span></p>
<p><span data-ttu-id="c4408-174"><b>Chyba za běhu:</b> Filtrování není podporováno.</span><span class="sxs-lookup"><span data-stu-id="c4408-174"><b>Runtime error:</b> Filtering is not supported.</span></span> <span data-ttu-id="c4408-175">Chcete-li získat další podrobnosti o chybě, ověřte konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="c4408-175">Validate the configuration to get more details about this.</span></span></p>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="c4408-176"><a href='#i5'>Spustitelnost zdroje dat GROUPBY</a></span><span class="sxs-lookup"><span data-stu-id="c4408-176"><a href='#i5'>Executability of a GROUPBY data source</a></span></span></td>
<td><span data-ttu-id="c4408-177">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="c4408-177">Executability</span></span></td>
<td><span data-ttu-id="c4408-178">Chyba</span><span class="sxs-lookup"><span data-stu-id="c4408-178">Error</span></span></td>
<td><span data-ttu-id="c4408-179">Cesta &lt;cesta&gt; nepodporuje dotazování.</span><span class="sxs-lookup"><span data-stu-id="c4408-179">Path &lt;path&gt; does not support querying.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4408-180">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="c4408-180">Executability</span></span></td>
<td><span data-ttu-id="c4408-181">Chyba</span><span class="sxs-lookup"><span data-stu-id="c4408-181">Error</span></span></td>
<td>
<p><span data-ttu-id="c4408-182">Seskupení podle funkce nelze provést pomocí dotazu.</span><span class="sxs-lookup"><span data-stu-id="c4408-182">Group by function cannot be executed with query.</span></span></p>
<p><span data-ttu-id="c4408-183"><b>Chyba za běhu:</b> Seskupení podle funkce nelze provést pomocí dotazu.</span><span class="sxs-lookup"><span data-stu-id="c4408-183"><b>Runtime error:</b> Group by function can't be executed with query.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="c4408-184"><a href='#i6'>Spustitelnost zdroje dat JOIN</a></span><span class="sxs-lookup"><span data-stu-id="c4408-184"><a href='#i6'>Executability of a JOIN data source</a></span></span></td>
<td><span data-ttu-id="c4408-185">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="c4408-185">Executability</span></span></td>
<td><span data-ttu-id="c4408-186">Chyba</span><span class="sxs-lookup"><span data-stu-id="c4408-186">Error</span></span></td>
<td>
<p><span data-ttu-id="c4408-187">Nelze připojit seznam &lt;cesta&gt;, který není filtrem v dotazu.</span><span class="sxs-lookup"><span data-stu-id="c4408-187">Cannot join a list &lt;path&gt; that is not a filter in query.</span></span></p>
<p><span data-ttu-id="c4408-188"><b>Chyba za běhu:</b> Funkce datového zdroje JOIN by měla být výrazem filtru vypočítaného pole, který byl nesprávně volán.</span><span class="sxs-lookup"><span data-stu-id="c4408-188"><b>Runtime error:</b> Function Joined datasource should be a filter expression calculated field has been incorrectly called.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="c4408-189"><a href='#i7'>Je vhodnější funkce FILTER nebo WHERE?</a></span><span class="sxs-lookup"><span data-stu-id="c4408-189"><a href='#i7'>Preferability of FILTER vs WHERE function</a></span></span></td>
<td><span data-ttu-id="c4408-190">Výkonnost</span><span class="sxs-lookup"><span data-stu-id="c4408-190">Performance</span></span></td>
<td><span data-ttu-id="c4408-191">Upozornění</span><span class="sxs-lookup"><span data-stu-id="c4408-191">Warning</span></span></td>
<td><span data-ttu-id="c4408-192">Použití funkce FILTER ve výrazu je z hlediska výkonu vhodnější než použití funkce WHERE.</span><span class="sxs-lookup"><span data-stu-id="c4408-192">Using FILTER function for the expression is preferable than WHERE from the performance perspective.</span></span> <span data-ttu-id="c4408-193">Vyberte možnost Opravit, aby došlo k automatickému nahrazení.</span><span class="sxs-lookup"><span data-stu-id="c4408-193">Select Fix to replace it automatically.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4408-194"><a href='#i8'>Je vhodnější funkce ALLITEMSQUERY nebo ALLITEMS?</a></span><span class="sxs-lookup"><span data-stu-id="c4408-194"><a href='#i8'>Preferability of ALLITEMSQUERY vs ALLITEMS function</a></span></span></td>
<td><span data-ttu-id="c4408-195">Výkonnost</span><span class="sxs-lookup"><span data-stu-id="c4408-195">Performance</span></span></td>
<td><span data-ttu-id="c4408-196">Upozornění</span><span class="sxs-lookup"><span data-stu-id="c4408-196">Warning</span></span></td>
<td><span data-ttu-id="c4408-197">Použití funkce ALLITEMSQUERY ve výrazu je z hlediska výkonu vhodnější než použití funkce ALLITEMS.</span><span class="sxs-lookup"><span data-stu-id="c4408-197">Using ALLITEMSQUERY function for the expression is preferable than ALLITEMS from the performance perspective.</span></span> <span data-ttu-id="c4408-198">Vyberte možnost Opravit, aby došlo k automatickému nahrazení.</span><span class="sxs-lookup"><span data-stu-id="c4408-198">Select Fix to replace it automatically.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4408-199"><a href='#i9'>Možnost výskytů prázdného seznamu</a></span><span class="sxs-lookup"><span data-stu-id="c4408-199"><a href='#i9'>Consideration of empty list cases</a></span></span></td>
<td><span data-ttu-id="c4408-200">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="c4408-200">Executability</span></span></td>
<td><span data-ttu-id="c4408-201">Upozornění</span><span class="sxs-lookup"><span data-stu-id="c4408-201">Warning</span></span></td>
<td>
<p><span data-ttu-id="c4408-202">Seznam &lt;cesta&gt; nemá žádnou kontrolu výskytu prázdného seznamu, což může způsobit chybu za běhu.</span><span class="sxs-lookup"><span data-stu-id="c4408-202">List &lt;path&gt; does not have any check for empty list case, it can result an error at run time.</span></span> <span data-ttu-id="c4408-203">Přidejte kontrolu výskytu prázdného seznamu.</span><span class="sxs-lookup"><span data-stu-id="c4408-203">Add a check for empty list case.</span></span></p>
<p><span data-ttu-id="c4408-204"><b>Chyba za běhu:</b> Seznam je prázdný v cestě &lt;cesta&gt;</span><span class="sxs-lookup"><span data-stu-id="c4408-204"><b>Runtime error:</b> List is empty at &lt;path&gt;</span></span></p>
<p><span data-ttu-id="c4408-205"><b><a href='#i9a'>Potenciální problém</a> :</b> Řádek se naplní jednou, zatímco zdroj dat, ze kterého je naplněn, obsahuje více záznamů</span><span class="sxs-lookup"><span data-stu-id="c4408-205"><b><a href='#i9a'>Potential issue</a>:</b> Line is getting populated once while a data source it is populated from contains multiple records</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="c4408-206"><a href='#i10'>Spustitelnost výrazu s funkcí FILTER (použití mezipaměti)</a></span><span class="sxs-lookup"><span data-stu-id="c4408-206"><a href='#i10'>Executability of an expression with FILTER function (caching)</a></span></span></td>
<td><span data-ttu-id="c4408-207">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="c4408-207">Executability</span></span></td>
<td><span data-ttu-id="c4408-208">Chyba</span><span class="sxs-lookup"><span data-stu-id="c4408-208">Error</span></span></td>
<td>
<p><span data-ttu-id="c4408-209">Funkci FILTER nelze použít na vybraný typ zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="c4408-209">FILTER function cannot be applied to the selected type of data source.</span></span> <span data-ttu-id="c4408-210">Zdroj dat typu Záznamy tabulky je použitelný pouze v případě, že není uložen do mezipaměti a nemá žádné ručně přidané vnořené zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="c4408-210">A data source of the Table records type is applicable only when it is not cached and has no manually added nested data sources.</span></span></p>
<p><span data-ttu-id="c4408-211"><b>Chyba za běhu:</b> Filtrování není podporováno.</span><span class="sxs-lookup"><span data-stu-id="c4408-211"><b>Runtime error:</b> Filtering is not supported.</span></span> <span data-ttu-id="c4408-212">Chcete-li získat další podrobnosti o chybě, ověřte konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="c4408-212">Validate the configuration to get more details about this.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="c4408-213"><a href='#i11'>Chybějící vazba</a></span><span class="sxs-lookup"><span data-stu-id="c4408-213"><a href='#i11'>Missing binding</a></span></span></td>
<td><span data-ttu-id="c4408-214">Proveditelnost</span><span class="sxs-lookup"><span data-stu-id="c4408-214">Executability</span></span></td>
<td><span data-ttu-id="c4408-215">Upozornění</span><span class="sxs-lookup"><span data-stu-id="c4408-215">Warning</span></span></td>
<td>
<p><span data-ttu-id="c4408-216">Cesta &lt;cesta&gt; nemá žádnou vazbu na žádný zdroj dat při používání mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="c4408-216">Path &lt;path&gt; has no binding to any datasource in using model's mapping.</span></span></p>
<p><span data-ttu-id="c4408-217"><b>Chyba za běhu:</b> Cesta &lt;cesta&gt; není vázána</span><span class="sxs-lookup"><span data-stu-id="c4408-217"><b>Runtime error:</b> Path &lt;path&gt; is not bound</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="c4408-218"><a href='#i12'>Nepropojená šablona</a></span><span class="sxs-lookup"><span data-stu-id="c4408-218"><a href='#i12'>Not linked template</a></span></span></td>
<td><span data-ttu-id="c4408-219">Integrita dat</span><span class="sxs-lookup"><span data-stu-id="c4408-219">Data integrity</span></span></td>
<td><span data-ttu-id="c4408-220">Upozornění</span><span class="sxs-lookup"><span data-stu-id="c4408-220">Warning</span></span></td>
<td><span data-ttu-id="c4408-221">Soubor &lt;název&gt; není propojen s žádnými souborovými komponentami a bude odstraněn po změně stavu verze konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c4408-221">File &lt;name&gt; is linked to no file components and will be removed after changing status of configuration version.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4408-222"><a href='#i13'>Nesynchronizovaný formát</a></span><span class="sxs-lookup"><span data-stu-id="c4408-222"><a href='#i13'>Not synced format</a></span></span></td>
<td><span data-ttu-id="c4408-223">Integrita dat</span><span class="sxs-lookup"><span data-stu-id="c4408-223">Data integrity</span></span></td>
<td><span data-ttu-id="c4408-224">Upozornění</span><span class="sxs-lookup"><span data-stu-id="c4408-224">Warning</span></span></td>
<td><span data-ttu-id="c4408-225">Definovaný název &lt;název komponenty&gt; neexistuje v listu aplikace Excel &lt;název listu&gt;</span><span class="sxs-lookup"><span data-stu-id="c4408-225">Defined name &lt;component name&gt; does not exist in Excel sheet &lt;sheet name&gt;</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c4408-226"><a href='#i14'>Nesynchronizovaný formát</a></span><span class="sxs-lookup"><span data-stu-id="c4408-226"><a href='#i14'>Not synced format</a></span></span></td>
<td><span data-ttu-id="c4408-227">Integrita dat</span><span class="sxs-lookup"><span data-stu-id="c4408-227">Data integrity</span></span></td>
<td><span data-ttu-id="c4408-228">Upozornění</span><span class="sxs-lookup"><span data-stu-id="c4408-228">Warning</span></span></td>
<td>
<p><span data-ttu-id="c4408-229">Značka &lt;Ovládání obsahu označených slov&gt; neexistuje v souboru šablony Wordu</span><span class="sxs-lookup"><span data-stu-id="c4408-229">&lt;Tagged Word content control&gt; tag does not exist in Word template file</span></span></p>
<p><span data-ttu-id="c4408-230"><b>Běhová chyba:</b> Značka &lt;Ovládání obsahu označených slov&gt; neexistuje v souboru šablony Wordu.</span><span class="sxs-lookup"><span data-stu-id="c4408-230"><b>Runtime error:</b> &lt;Tagged Word content control&gt; tag does not exist in Word template file.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="c4408-231"><a href='#i15'>Žádné výchozí mapování</a></span><span class="sxs-lookup"><span data-stu-id="c4408-231"><a href='#i15'>No default mapping</a></span></span></td>
<td><span data-ttu-id="c4408-232">Integrita dat</span><span class="sxs-lookup"><span data-stu-id="c4408-232">Data integrity</span></span></td>
<td><span data-ttu-id="c4408-233">Chyba</span><span class="sxs-lookup"><span data-stu-id="c4408-233">Error</span></span></td>
<td>
<p><span data-ttu-id="c4408-234">Existuje více než jedno mapování modelu pro datový model &lt;název modelu (deskriptor kořene)&gt; v konfiguracích &lt;názvy konfigurace oddělené čárkou&gt;.</span><span class="sxs-lookup"><span data-stu-id="c4408-234">More than one model mapping exists for the &lt;model name (root descriptor)&gt; data model in the configurations &lt;configuration names separated by comma&gt;.</span></span> <span data-ttu-id="c4408-235">Nastavte jednu z konfigurací jako výchozí</span><span class="sxs-lookup"><span data-stu-id="c4408-235">Set one of the configurations as default</span></span></p>
<p><span data-ttu-id="c4408-236"><b>Běhová chyba</b> Existuje více než jedno mapování modelu pro datový model &lt;název modelu (deskriptor kořene)&gt; v konfiguracích názvy &lt;konfigurace oddělené čárkou&gt;.</span><span class="sxs-lookup"><span data-stu-id="c4408-236"><b>Runtime error:</b> More than one model mapping exists for the &lt;model name (root descriptor)&gt; data model in the configurations &lt;configuration names separated by comma&gt;.</span></span> <span data-ttu-id="c4408-237">Nastavte jednu z konfigurací jako výchozí.</span><span class="sxs-lookup"><span data-stu-id="c4408-237">Set one of the configurations as default.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="c4408-238"><a href='#i16'>Nekonzistentní nastavení komponent záhlaví nebo zápatí</a></span><span class="sxs-lookup"><span data-stu-id="c4408-238"><a href='#i16'>Inconsistent setting of Header or Footer components</a></span></span></td>
<td><span data-ttu-id="c4408-239">Integrita dat</span><span class="sxs-lookup"><span data-stu-id="c4408-239">Data integrity</span></span></td>
<td><span data-ttu-id="c4408-240">Chyba</span><span class="sxs-lookup"><span data-stu-id="c4408-240">Error</span></span></td>
<td>
<p><span data-ttu-id="c4408-241">Záhlaví/zápatí (&lt;typ součásti: Záhlaví nebo zápatí&gt;) jsou nekonzistentní</span><span class="sxs-lookup"><span data-stu-id="c4408-241">Headers/footers (&lt;component type: Header or Footer&gt;) are inconsistent</span></span></p>
<p><span data-ttu-id="c4408-242"><b>Runtime:</b> Poslední nakonfigurovaná komponenta se používá za běhu, pokud je spuštěna konceptová verze nakonfigurovaného formátu ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-242"><b>Runtime:</b> The last configured component is used at runtime if the draft version of the configured ER format is executed.</span></span></p>
</td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a><span data-ttu-id="c4408-243">Převod typu</span><span class="sxs-lookup"><span data-stu-id="c4408-243">Type conversion</span></span>

<span data-ttu-id="c4408-244">ER kontroluje, zda je datový typ pole datového modelu kompatibilní s datovým typem výrazu, který je konfigurován jako vazba daného pole.</span><span class="sxs-lookup"><span data-stu-id="c4408-244">ER checks whether the data type of a data model field is compatible with the data type of an expression that is configured as the binding of that field.</span></span> <span data-ttu-id="c4408-245">Pokud jsou datové typy nekompatibilní, dojde v návrháři mapování modelu ER k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-245">If the data types are incompatible, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="c4408-246">Zpráva, kterou obdržíte, uvádí, že ER nemůže převést výraz typu A na pole typu B.</span><span class="sxs-lookup"><span data-stu-id="c4408-246">The message that you receive states that ER can't convert an expression of type A to a field of type B.</span></span>

<span data-ttu-id="c4408-247">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="c4408-247">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="c4408-248">Začněte konfigurovat datový model ER a komponenty mapování modelu ER současně.</span><span class="sxs-lookup"><span data-stu-id="c4408-248">Start to configure the ER data model and the ER model mapping components simultaneously.</span></span>
2. <span data-ttu-id="c4408-249">Ve stromu datového modelu přidejte pole s názvem **X** a jako datový typ vyberte **Celé číslo**.</span><span class="sxs-lookup"><span data-stu-id="c4408-249">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>

    ![Pole X a datový typ Celé číslo byly přidány do stromu datového modelu na stránce Datový model](./media/er-components-inspections-01.png)

3. <span data-ttu-id="c4408-251">V podokně **Zdroje dat** mapování modelu přidejte zdroj dat typu **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="c4408-251">In the model mapping designer, in the **Data sources** pane, add a data source of the **Calculated field** type.</span></span>
4. <span data-ttu-id="c4408-252">Pojmenujte nový zdroj dat jako **Y** a konfigurujte jej tak, aby obsahoval výraz `INTVALUE(100)`.</span><span class="sxs-lookup"><span data-stu-id="c4408-252">Name the new data source **Y**, and configure it so that it contains the expression `INTVALUE(100)`.</span></span>
5. <span data-ttu-id="c4408-253">Navažte **X** na **Y**.</span><span class="sxs-lookup"><span data-stu-id="c4408-253">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="c4408-254">V návrháři datového modelu změňte datový typ pole **X** z hodnoty **Celé číslo** na **Int64**.</span><span class="sxs-lookup"><span data-stu-id="c4408-254">In the data model designer, change the data type of the **X** field from **Integer** to **Int64**.</span></span>
7. <span data-ttu-id="c4408-255">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu mapování modelu na stránce **Návrhář mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="c4408-255">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![Ověřování upravitelné komponenty mapování modelu na stránce Návrhář mapování modelu](./media/er-components-inspections-01.gif)

8. <span data-ttu-id="c4408-257">Výběrem příkazu **Ověřit** zkontrolujete komponentu mapování modelu vybrané konfigurace ER na stránce **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="c4408-257">Select **Validate** to inspect the model mapping component of the selected ER configuration on the **Configurations** page.</span></span>

    ![Kontrola komponenty mapování modelu na stránce Konfigurace](./media/er-components-inspections-01a.png)

9. <span data-ttu-id="c4408-259">Všimněte si, že dojde k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-259">Notice that a validation error occurs.</span></span> <span data-ttu-id="c4408-260">Zpráva uvádí, že hodnotu typu **Celé číslo**, kterou vrátí výraz `INTVALUE(100)` zdroje dat **Y**, nelze uložit do pole datového modelu **X** typu **Int64**.</span><span class="sxs-lookup"><span data-stu-id="c4408-260">The message states that the value of the **Integer** type that the `INTVALUE(100)` expression of the **Y** data source returns can't be stored in the **X** data model field of the **Int64** type.</span></span>

<span data-ttu-id="c4408-261">Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění a výběrem příkazu **Spustit** spustíte formát, který má konfigurováno použití mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="c4408-261">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![Chyby za běhu na stránce Návrhář formátu](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="c4408-263">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-263">Automatic resolution</span></span>

<span data-ttu-id="c4408-264">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="c4408-264">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="c4408-265">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-265">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="c4408-266">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="c4408-266">Option 1</span></span>

<span data-ttu-id="c4408-267">Aktualizujte strukturu datového modelu změnou datového typu pole datového modelu tak, aby odpovídal datovému typu výrazu, který je konfigurován pro vazbu daného pole.</span><span class="sxs-lookup"><span data-stu-id="c4408-267">Update the data model structure by changing the data type of the data model field so that it matches the data type of the expression that is configured for the binding of that field.</span></span> <span data-ttu-id="c4408-268">V předchozím příkladu musíte datový typ pole **X** změnit zpět na **Celé číslo**.</span><span class="sxs-lookup"><span data-stu-id="c4408-268">For the preceding example, the data type of the **X** field must be changed back to **Integer**.</span></span>

#### <a name="option-2"></a><span data-ttu-id="c4408-269">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="c4408-269">Option 2</span></span>

<span data-ttu-id="c4408-270">Aktualizujte mapování modelu změnou výrazu zdroje dat, který je svázán s polem datového modelu.</span><span class="sxs-lookup"><span data-stu-id="c4408-270">Update the model mapping by changing the expression of the data source that is bound with the data model field.</span></span> <span data-ttu-id="c4408-271">V předchozím příkladu musíte změnit výraz zdroje dat **Y** na `INT64VALUE(100)`.</span><span class="sxs-lookup"><span data-stu-id="c4408-271">For the preceding example, the expression of the **Y** data source must be changed to `INT64VALUE(100)`.</span></span>

## <a name="type-compatibility"></a><a id="i2"></a><span data-ttu-id="c4408-272">Kompatibilita typů</span><span class="sxs-lookup"><span data-stu-id="c4408-272">Type compatibility</span></span>

<span data-ttu-id="c4408-273">ER kontroluje, zda je datový typ prvku formátu kompatibilní s datovým typem výrazu, který je konfigurován jako vazba daného prvku formátu.</span><span class="sxs-lookup"><span data-stu-id="c4408-273">ER checks whether the data type of a format element is compatible with the data type of an expression that is configured as the binding of that format element.</span></span> <span data-ttu-id="c4408-274">Pokud jsou datové typy nekompatibilní, dojde v návrháři operací ER k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-274">If the data types are incompatible, a validation error occurs in the ER Operations designer.</span></span> <span data-ttu-id="c4408-275">Zpráva, kterou obdržíte, říká, že konfigurovaný výraz nelze použít jako vazbu aktuálního prvku formátu ke zdroji dat, protože tento výraz vrací hodnotu datového typu A, tedy mimo rámec datových typů, které jsou podporovány aktuálním prvkem formátu typu B.</span><span class="sxs-lookup"><span data-stu-id="c4408-275">The message that you receive states that the configured expression can't be used as the binding of the current format element to a data source, because the expression returns a value of data type A that is beyond the scope of the data types that are supported by the current format element of type B.</span></span>

<span data-ttu-id="c4408-276">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="c4408-276">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="c4408-277">Začněte konfigurovat datový model ER a komponenty formátu ER současně.</span><span class="sxs-lookup"><span data-stu-id="c4408-277">Start to configure the ER data model and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="c4408-278">Ve stromu datového modelu přidejte pole s názvem **X** a jako datový typ vyberte **Celé číslo**.</span><span class="sxs-lookup"><span data-stu-id="c4408-278">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>
3. <span data-ttu-id="c4408-279">Ve stromu struktury formátu přidejte prvek formátu typu **Číslo**.</span><span class="sxs-lookup"><span data-stu-id="c4408-279">In the format structure tree, add a format element of the **Numeric** type.</span></span>
4. <span data-ttu-id="c4408-280">Pojmenujte nový prvek formátu jako **Y**. V poli **Číselný typ** vyberte jako datový typ hodnotu **Celé číslo**.</span><span class="sxs-lookup"><span data-stu-id="c4408-280">Name the new format element **Y**. In the **Numeric type** field, select **Integer** as the data type.</span></span>
5. <span data-ttu-id="c4408-281">Navažte **X** na **Y**.</span><span class="sxs-lookup"><span data-stu-id="c4408-281">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="c4408-282">Ve stromu struktury formátu změňte datový typ prvku formátu **Y** z hodnoty **Celé číslo** na **Int64**.</span><span class="sxs-lookup"><span data-stu-id="c4408-282">In the format structure tree, change the data type of the **Y** format element from **Integer** to **Int64**.</span></span>
7. <span data-ttu-id="c4408-283">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu formátu na stránce **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="c4408-283">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![Ověření kompatibility typů na stránce Návrhář formátu](./media/er-components-inspections-02.gif)

8. <span data-ttu-id="c4408-285">Všimněte si, že dojde k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-285">Notice that a validation error occurs.</span></span> <span data-ttu-id="c4408-286">Zpráva uvádí, že konfigurovaný výraz může přijmout pouze hodnoty typu **Int64**.</span><span class="sxs-lookup"><span data-stu-id="c4408-286">The message states that the configured expression can accept only **Int64** values.</span></span> <span data-ttu-id="c4408-287">Proto nelze hodnotu pole datového modelu **X** typu **Celé číslo** zadat do prvku formátu **Y**.</span><span class="sxs-lookup"><span data-stu-id="c4408-287">Therefore, the value of the **X** data model field of the **Integer** type can't be entered in the **Y** format element.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="c4408-288">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-288">Automatic resolution</span></span>

<span data-ttu-id="c4408-289">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="c4408-289">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="c4408-290">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-290">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="c4408-291">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="c4408-291">Option 1</span></span>

<span data-ttu-id="c4408-292">Aktualizujte strukturu formátu změnou datového typu prvku formátu **Číslo** tak, aby odpovídal datovému typu výrazu, který je konfigurován pro vazbu tohoto prvku.</span><span class="sxs-lookup"><span data-stu-id="c4408-292">Update the format structure by changing the data type of the **Numeric** format element so that it matches the data type of the expression that you configured for the binding of that element.</span></span> <span data-ttu-id="c4408-293">V předchozím příkladu musíte datový typ **Číslo** prvku formátu **X** změnit zpět **Celé číslo**.</span><span class="sxs-lookup"><span data-stu-id="c4408-293">In the preceding example, the **Numeric type** value of the **X** format element must be changed back to **Integer**.</span></span>

#### <a name="option-2"></a><span data-ttu-id="c4408-294">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="c4408-294">Option 2</span></span>

<span data-ttu-id="c4408-295">Aktualizujte mapování formátu prvku formátu **X** změnou výrazu z `model.X` na `INT64VALUE(model.X)`.</span><span class="sxs-lookup"><span data-stu-id="c4408-295">Update the format mapping of the **X** format element by changing the expression from `model.X` to `INT64VALUE(model.X)`.</span></span>

## <a name="missing-configuration-element"></a><a id="i3"></a><span data-ttu-id="c4408-296">Chybějící konfigurační prvek</span><span class="sxs-lookup"><span data-stu-id="c4408-296">Missing configuration element</span></span>

<span data-ttu-id="c4408-297">ER zkontroluje, zda vazební výrazy obsahují pouze zdroje dat, které jsou konfigurovány v upravitelné komponentě ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-297">ER checks whether the binding expressions contain only data sources that are configured in the editable ER component.</span></span> <span data-ttu-id="c4408-298">U každé vazby, která obsahuje zdroj dat, který chybí v upravitelné komponentě ER, dojde k chybě ověření v návrháři operací ER nebo návrháři mapování modelu ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-298">For every binding that contains a data source that is missing in the editable ER component, a validation error occurs in the ER Operations designer or the ER model mapping designer.</span></span>

<span data-ttu-id="c4408-299">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="c4408-299">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="c4408-300">Začněte konfigurovat datový model ER a komponenty mapování modelu ER současně.</span><span class="sxs-lookup"><span data-stu-id="c4408-300">Start to configure the ER data model and the ER model mapping components simultaneously.</span></span>
2. <span data-ttu-id="c4408-301">Ve stromu datového modelu přidejte pole s názvem **X** a jako datový typ vyberte **Celé číslo**.</span><span class="sxs-lookup"><span data-stu-id="c4408-301">In the data model tree, add a field that is named **X**, and select **Integer** as the data type.</span></span>

    ![Strom datového modelu s polem X a datovým typem Celé číslo na stránce Datový model](./media/er-components-inspections-01.png)

3. <span data-ttu-id="c4408-303">V podokně **Zdroje dat** mapování modelu přidejte zdroj dat typu **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="c4408-303">In the model mapping designer, in the **Data sources** pane, add a data source of the **Calculated field** type.</span></span>
4. <span data-ttu-id="c4408-304">Pojmenujte nový zdroj dat jako **Y** a konfigurujte jej tak, aby obsahoval výraz `INTVALUE(100)`.</span><span class="sxs-lookup"><span data-stu-id="c4408-304">Name the new data source **Y**, and configure it so that it contains the expression `INTVALUE(100)`.</span></span>
5. <span data-ttu-id="c4408-305">Navažte **X** na **Y**.</span><span class="sxs-lookup"><span data-stu-id="c4408-305">Bind **X** to **Y**.</span></span>
6. <span data-ttu-id="c4408-306">V návrháři mapování modelu v podokně **Zdroje dat** odstraňte zdroj dat **Y**.</span><span class="sxs-lookup"><span data-stu-id="c4408-306">In the model mapping designer, in the **Data sources** pane, delete the **Y** data source.</span></span>
7. <span data-ttu-id="c4408-307">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu mapování modelu na stránce **Návrhář mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="c4408-307">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![Kontrola upravitelné komponenty mapování modelu ER na stránce Návrhář mapování modelu](./media/er-components-inspections-03.gif)

8. <span data-ttu-id="c4408-309">Všimněte si, že dojde k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-309">Notice that a validation error occurs.</span></span> <span data-ttu-id="c4408-310">Zpráva uvádí, že vazba pole datového modelu **X** obsahuje cestu, která odkazuje na zdroj dat **Y**, ale tento zdroj dat nebyl nalezen.</span><span class="sxs-lookup"><span data-stu-id="c4408-310">The message states that the binding of the **X** data model field contains the path that refers to the **Y** data source, but this data source isn't found.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="c4408-311">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-311">Automatic resolution</span></span>

<span data-ttu-id="c4408-312">Výběrem příkazu **Odpojit** automaticky opravíte tento problém odstraněním vazby na chybějící zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="c4408-312">Select **Unbind** to automatically fix this issue by removing the missing data source binding.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="c4408-313">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-313">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="c4408-314">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="c4408-314">Option 1</span></span>

<span data-ttu-id="c4408-315">Odpojte pole datového modelu **X**, aby přestalo odkazovat na neexistující zdroj dat **Y**.</span><span class="sxs-lookup"><span data-stu-id="c4408-315">Unbind the **X** data model field to stop referring to the nonexistent **Y** data source.</span></span>

#### <a name="option-2"></a><span data-ttu-id="c4408-316">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="c4408-316">Option 2</span></span>

<span data-ttu-id="c4408-317">V podokně **Zdroje dat** návrháře mapování modelu přidejte znovu zdroj dat **Y**.</span><span class="sxs-lookup"><span data-stu-id="c4408-317">In the model mapping designer, in the **Data sources** pane, add the **Y** data source again.</span></span>

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a><span data-ttu-id="c4408-318">Spustitelnost výrazu s funkcí FILTER</span><span class="sxs-lookup"><span data-stu-id="c4408-318">Executability of an expression with FILTER function</span></span>

<span data-ttu-id="c4408-319">Integrovaná funkce ER [FILTER](er-functions-list-filter.md) se používá pro přístup k aplikačním tabulkám, pohledům nebo datovým entitám umístěním jediného volání SQL, které získá požadovaná data jako seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="c4408-319">The built-in [FILTER](er-functions-list-filter.md) ER function is used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="c4408-320">Zdroj dat typu **Seznam záznamů** se používá jako argument této funkce a určuje zdroj aplikace pro volání.</span><span class="sxs-lookup"><span data-stu-id="c4408-320">A data source of the **Record list** type is used as an argument of this function and specifies the application source for the call.</span></span> <span data-ttu-id="c4408-321">ER kontroluje, zda lze navázat přímý dotaz SQL do zdroje dat, na který se odkazuje ve funkci `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="c4408-321">ER checks whether a direct SQL query can be established to a data source that is referred to in the `FILTER` function.</span></span> <span data-ttu-id="c4408-322">Pokud nelze navázat přímý dotaz, dojde v návrháři mapování modelu ER k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-322">If a direct query can't be established, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="c4408-323">Zpráva, kterou obdržíte, uvádí, že výraz ER obsahující funkci `FILTER` nelze spustit za běhu programu.</span><span class="sxs-lookup"><span data-stu-id="c4408-323">The message that you receive states that the ER expression that includes the `FILTER` function can't be run at runtime.</span></span>

<span data-ttu-id="c4408-324">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="c4408-324">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="c4408-325">Začněte konfigurací komponenty mapování modelu ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-325">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="c4408-326">Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.</span><span class="sxs-lookup"><span data-stu-id="c4408-326">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="c4408-327">Pojmenujte nový zdroj dat jako **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="c4408-327">Name the new data source **Vendor**.</span></span> <span data-ttu-id="c4408-328">V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.</span><span class="sxs-lookup"><span data-stu-id="c4408-328">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="c4408-329">Přidejte zdroj dat typu **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="c4408-329">Add a data source of the **Calculated field** type.</span></span>
5. <span data-ttu-id="c4408-330">Pojmenujte nový zdroj dat jako **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `FILTER(Vendor, Vendor.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="c4408-330">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum="US-101")`.</span></span>
6. <span data-ttu-id="c4408-331">Výběrem příkazu **Ověřit** zkontrolujte upravitelnou komponentu mapování modelu na stránce **návrháře mapování modelů** stránku a ověřte, zda výraz `FILTER(Vendor, Vendor.AccountNum="US-101")` ve zdroji dat **Vendor** lze používat v dotazech.</span><span class="sxs-lookup"><span data-stu-id="c4408-331">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression in the **Vendor** data source can be queried.</span></span>
7. <span data-ttu-id="c4408-332">Upravte zdroj dat **Vendor** přidáním vnořeného pole typu **Vypočítané pole** a získejte oříznuté číslo účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="c4408-332">Modify the **Vendor** data source by adding a nested field of the **Calculated field** type to get the trimmed vendor account number.</span></span>
8. <span data-ttu-id="c4408-333">Pojmenujte nové vnořené pole jako **$AccNumber** a konfigurujte jej tak, aby obsahovalo výraz `TRIM(Vendor.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="c4408-333">Name the new nested field **$AccNumber**, and configure it so that it contains the expression `TRIM(Vendor.AccountNum)`.</span></span>
9. <span data-ttu-id="c4408-334">Výběrem příkazu **Ověřit** zkontrolujte upravitelnou komponentu mapování modelu na stránce **návrháře mapování modelů** stránku a ověřte, zda výraz `FILTER(Vendor, Vendor.AccountNum="US-101")` ve zdroji dat **Vendor** lze používat v dotazech.</span><span class="sxs-lookup"><span data-stu-id="c4408-334">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression in the **Vendor** data source can be queried.</span></span>

    ![Ověření výrazu lze zkontrolovat dotazem na stránce Návrhář mapování modelů](./media/er-components-inspections-04.gif)

10. <span data-ttu-id="c4408-336">Všimněte si, že dojde k chybě ověření, protože zdroj dat **Vendor** obsahuje vnořené pole typu **Vypočítané pole**, které neumožňuje přeložit výraz **FilteredVendor** zdroje dat na přímý příkaz SQL.</span><span class="sxs-lookup"><span data-stu-id="c4408-336">Notice that a validation error occurs, because the **Vendor** data source contains a nested field of the **Calculated field** type that doesn't allow the expression of the **FilteredVendor** data source to be translated to the direct SQL statement.</span></span>

<span data-ttu-id="c4408-337">Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění a výběrem příkazu **Spustit** spustíte formát, který má konfigurováno použití mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="c4408-337">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![Chyby za běhu, ke kterým dochází při spuštění upravitelného formátu na stránce Návrhář formátů](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a><span data-ttu-id="c4408-339">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-339">Automatic resolution</span></span>

<span data-ttu-id="c4408-340">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="c4408-340">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="c4408-341">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-341">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="c4408-342">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="c4408-342">Option 1</span></span>

<span data-ttu-id="c4408-343">Místo přidání vnořeného pole typu **Vypočítané pole** do zdroje dat **Vendor** přidejte vnořené pole **$AccNumber** do zdroje dat **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `TRIM(FilteredVendor.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="c4408-343">Instead of adding a nested field of the **Calculated field** type to the **Vendor** data source, add the **$AccNumber** nested field to the **FilteredVendor** data source, and configure it so that it contains the expression `TRIM(FilteredVendor.AccountNum)`.</span></span> <span data-ttu-id="c4408-344">Tímto způsobem lze výraz `FILTER(Vendor, Vendor.AccountNum="US-101")` spustit na úrovni SQL a vypočítat vnořené pole **$AccNumber** později.</span><span class="sxs-lookup"><span data-stu-id="c4408-344">In this way, the `FILTER(Vendor, Vendor.AccountNum="US-101")` expression can be run at the SQL level and calculate the **$AccNumber** nested field afterward.</span></span>

#### <a name="option-2"></a><span data-ttu-id="c4408-345">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="c4408-345">Option 2</span></span>

<span data-ttu-id="c4408-346">Změňte výraz zdroje dat **FilteredVendor** z `FILTER(Vendor, Vendor.AccountNum="US-101")` na `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="c4408-346">Change the expression of the **FilteredVendor** data source from `FILTER(Vendor, Vendor.AccountNum="US-101")` to `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span> <span data-ttu-id="c4408-347">Nedoporučujeme měnit výraz pro tabulku, která obsahuje velké množství dat (transakční tabulka), protože budou načteny všechny záznamy a výběr požadovaných záznamů bude proveden v paměti.</span><span class="sxs-lookup"><span data-stu-id="c4408-347">We don't recommend that you change the expression for a table that has a large volume of data (transactional table), because all records will be fetched, and selection of the required records will be done in memory.</span></span> <span data-ttu-id="c4408-348">Tento přístup proto může způsobit špatný výkon.</span><span class="sxs-lookup"><span data-stu-id="c4408-348">Therefore, this approach can cause poor performance.</span></span> <span data-ttu-id="c4408-349">Další informace viz část [Funkce WHERE ER](er-functions-list-where.md).</span><span class="sxs-lookup"><span data-stu-id="c4408-349">For more information, see [WHERE ER function](er-functions-list-where.md).</span></span>

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a><span data-ttu-id="c4408-350">Spustitelnost zdroje dat GROUPBY</span><span class="sxs-lookup"><span data-stu-id="c4408-350">Executability of a GROUPBY data source</span></span>

<span data-ttu-id="c4408-351">Zdroj dat **GROUPBY** rozděluje výsledek dotazu do skupin záznamů, obvykle za účelem provedení jedné nebo více agregací v každé skupině.</span><span class="sxs-lookup"><span data-stu-id="c4408-351">The **GROUPBY** data source divides the query result into groups of records, usually for the purpose of doing one or more aggregations on each group.</span></span> <span data-ttu-id="c4408-352">Každý zdroj dat **GROUPBY** lze konfigurovat tak, aby běžel na úrovni databáze nebo v paměti.</span><span class="sxs-lookup"><span data-stu-id="c4408-352">Every **GROUPBY** data source can be configured so that it's run either at the database level or in memory.</span></span> <span data-ttu-id="c4408-353">Když je zdroj dat **GROUPBY** konfigurován tak, aby byl spuštěn na úrovni databáze, ER zkontroluje, zda lze navázat přímý dotaz SQL do zdroje dat, na který se tento zdroj dat odkazuje.</span><span class="sxs-lookup"><span data-stu-id="c4408-353">When a **GROUPBY** data source is configured so that it's run at the database level, ER checks whether a direct SQL query can be established to a data source that is referred to in that data source.</span></span> <span data-ttu-id="c4408-354">Pokud nelze navázat přímý dotaz, dojde v návrháři mapování modelu ER k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-354">If a direct query can't be established, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="c4408-355">Zpráva, kterou obdržíte, uvádí, že konfigurovaný zdroj dat **GROUPBY** nelze spustit za běhu.</span><span class="sxs-lookup"><span data-stu-id="c4408-355">The message that you receive states that the configured **GROUPBY** data source can't be run at runtime.</span></span>

<span data-ttu-id="c4408-356">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="c4408-356">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="c4408-357">Začněte konfigurací komponenty mapování modelu ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-357">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="c4408-358">Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.</span><span class="sxs-lookup"><span data-stu-id="c4408-358">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="c4408-359">Pojmenujte nový zdroj dat jako **Trans**. V poli **Tabulka** vyberte hodnotu **VendTrans** a určete tak, že tento zdroj dat bude vyžadovat tabulku VendTrans.</span><span class="sxs-lookup"><span data-stu-id="c4408-359">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
4. <span data-ttu-id="c4408-360">Přidejte zdroj dat typu **Seskupit podle**.</span><span class="sxs-lookup"><span data-stu-id="c4408-360">Add a data source of the **Group by** type.</span></span>
5. <span data-ttu-id="c4408-361">Pojmenujte nový zdroj dat jako **GroupedTrans** a konfigurujte jej následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="c4408-361">Name the new data source **GroupedTrans**, and configure it in the following way:</span></span>

    - <span data-ttu-id="c4408-362">Vyberte zdroj dat **Trans** jako zdroj záznamů, které by měly být seskupeny.</span><span class="sxs-lookup"><span data-stu-id="c4408-362">Select the **Trans** data source as the source of records that should be grouped.</span></span>
    - <span data-ttu-id="c4408-363">V poli **Místo provedení** vyberte **Dotaz** a určete tak, že chcete spustit tento zdroj dat na úrovni databáze.</span><span class="sxs-lookup"><span data-stu-id="c4408-363">In the **Execution location** field, select **Query** to specify that you want to run this data source at the database level.</span></span>

    ![Konfigurace zdroje dat na stránce Upravit parametry „Seskupit podle“](./media/er-components-inspections-05a.gif)

6. <span data-ttu-id="c4408-365">Výběrem příkazu **Ověřit** zkontrolujte upravitelnou komponentu mapování modelu na stránce **návrháře mapování modelů** a ověřte, zda je možné konfigurovaný zdroj dat **GroupedTrans** používat v dotazech.</span><span class="sxs-lookup"><span data-stu-id="c4408-365">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **GroupedTrans** data source can be queried.</span></span>
7. <span data-ttu-id="c4408-366">Upravte zdroj dat **Trans** přidáním vnořeného pole typu **Vypočítané pole** a získejte oříznuté číslo účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="c4408-366">Modify the **Trans** data source by adding a nested field of the **Calculated field** type to get the trimmed vendor account number.</span></span>
8. <span data-ttu-id="c4408-367">Pojmenujte nový zdroj dat jako **$AccNumber** a konfigurujte jej tak, aby obsahoval výraz `TRIM(Trans.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="c4408-367">Name the new data source **$AccNumber**, and configure it so that it contains the expression `TRIM(Trans.AccountNum)`.</span></span>

    ![Konfigurace zdroje dat na stránce návrháře mapování modelů](./media/er-components-inspections-05a.png)

9. <span data-ttu-id="c4408-369">Výběrem příkazu **Ověřit** zkontrolujte upravitelnou komponentu mapování modelu na stránce **návrháře mapování modelů** a ověřte, zda je možné konfigurovaný zdroj dat **GroupedTrans** používat v dotazech.</span><span class="sxs-lookup"><span data-stu-id="c4408-369">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **GroupedTrans** data source can be queried.</span></span>

    ![Po ověření komponenty mapování modelu ER a ověření konfigurovaného zdroje dat je možné zdroj dat používat v dotazech na stránce návrháře mapování modelů](./media/er-components-inspections-05b.png)

10. <span data-ttu-id="c4408-371">Všimněte si, že dojde k chybě ověření, protože zdroj dat **Trans** obsahuje vnořené pole typu **Vypočítané pole**, které neumožňuje přeložit volání určené pro zdroj dat **GroupedTrans** na přímý příkaz SQL.</span><span class="sxs-lookup"><span data-stu-id="c4408-371">Notice that a validation error occurs, because the **Trans** data source contains a nested field of the **Calculated field** type that doesn't allow the call for the **GroupedTrans** data source to be translated to the direct SQL statement.</span></span>

<span data-ttu-id="c4408-372">Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění a výběrem příkazu **Spustit** spustíte formát, který má konfigurováno použití mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="c4408-372">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![Chyby za běhu, ke kterým dochází při ignorování upozornění na stránce Návrhář formátů](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a><span data-ttu-id="c4408-374">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-374">Automatic resolution</span></span>

<span data-ttu-id="c4408-375">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="c4408-375">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="c4408-376">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-376">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="c4408-377">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="c4408-377">Option 1</span></span>

<span data-ttu-id="c4408-378">Místo přidání vnořeného pole typu **Vypočítané pole** zadejte do zdroje dat **Trans** přidejte vnořené pole **$AccNumber** pro položku **GroupedTrans.lines** zdroje dat **GroupedTrans** a konfigurujte jej tak, aby obsahovalo výraz `TRIM(GroupedTrans.lines.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="c4408-378">Instead of adding a nested field of the **Calculated field** type to the **Trans** data source, add the **$AccNumber** nested field for the **GroupedTrans.lines** item of the **GroupedTrans** data source, and configure it so that it contains the expression `TRIM(GroupedTrans.lines.AccountNum)`.</span></span> <span data-ttu-id="c4408-379">Tímto způsobem lze zdroj dat **GroupedTrans** spustit na úrovni SQL a vypočítat vnořené pole **$AccNumber** později.</span><span class="sxs-lookup"><span data-stu-id="c4408-379">In this way, the **GroupedTrans** data source can be run at the SQL level and calculate the **$AccNumber** nested field afterward.</span></span>

#### <a name="option-2"></a><span data-ttu-id="c4408-380">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="c4408-380">Option 2</span></span>

<span data-ttu-id="c4408-381">Změňte hodnotu pole **Místo provedení** pro zdroj dat **GroupedTrans** z hodnoty **Dotaz** na **V paměti**.</span><span class="sxs-lookup"><span data-stu-id="c4408-381">Change the value of the **Execution location** field for the **GroupedTrans** data source from **Query** to **In memory**.</span></span> <span data-ttu-id="c4408-382">Nedoporučujeme měnit hodnotu pro tabulku, která obsahuje velké množství dat (transakční tabulka), protože budou načteny všechny záznamy a seskupení spolu s agregací budou provedeny v paměti.</span><span class="sxs-lookup"><span data-stu-id="c4408-382">We don't recommend that you change the value for a table that has a large volume of data (transactional table), because all records will be fetched, and grouping and aggregation will be done in memory.</span></span> <span data-ttu-id="c4408-383">Tento přístup proto může způsobit špatný výkon.</span><span class="sxs-lookup"><span data-stu-id="c4408-383">Therefore, this approach can cause poor performance.</span></span>

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a><span data-ttu-id="c4408-384">Spustitelnost zdroje dat JOIN</span><span class="sxs-lookup"><span data-stu-id="c4408-384">Executability of a JOIN data source</span></span>

<span data-ttu-id="c4408-385">Zdroj dat [JOIN](er-join-data-sources.md) kombinuje záznamy ze dvou nebo více databázových tabulek na základě souvisejících polí.</span><span class="sxs-lookup"><span data-stu-id="c4408-385">The [JOIN](er-join-data-sources.md) data source combines records from two or more database tables, based on related fields.</span></span> <span data-ttu-id="c4408-386">Každý zdroj dat **JOIN** lze konfigurovat tak, aby běžel na úrovni databáze nebo v paměti.</span><span class="sxs-lookup"><span data-stu-id="c4408-386">Every **JOIN** data source can be configured so that it's run either at the database level or in memory.</span></span> <span data-ttu-id="c4408-387">Když je zdroj dat **JOIN** konfigurován tak, aby byl spuštěn na úrovni databáze, ER zkontroluje, zda lze navázat přímý dotaz SQL do zdrojů dat, na které se tento zdroj dat odkazuje.</span><span class="sxs-lookup"><span data-stu-id="c4408-387">When a **JOIN** data source is configured so that it's run at the database level, ER checks whether a direct SQL query can be established to data sources that are referred to in that data source.</span></span> <span data-ttu-id="c4408-388">Pokud nelze navázat přímý dotaz SQL s nejméně jedním odkazovaným zdrojem dat, dojde v návrháři mapování modelu ER k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-388">If a direct SQL query can't be established with at least one referenced data source, a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="c4408-389">Zpráva, kterou obdržíte, uvádí, že konfigurovaný zdroj dat **JOIN** nelze spustit za běhu.</span><span class="sxs-lookup"><span data-stu-id="c4408-389">The message that you receive states that the configured **JOIN** data source can't be run at runtime.</span></span>

<span data-ttu-id="c4408-390">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="c4408-390">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="c4408-391">Začněte konfigurací komponenty mapování modelu ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-391">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="c4408-392">Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.</span><span class="sxs-lookup"><span data-stu-id="c4408-392">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="c4408-393">Pojmenujte nový zdroj dat jako **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="c4408-393">Name the new data source **Vendor**.</span></span> <span data-ttu-id="c4408-394">V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.</span><span class="sxs-lookup"><span data-stu-id="c4408-394">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="c4408-395">Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.</span><span class="sxs-lookup"><span data-stu-id="c4408-395">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
5. <span data-ttu-id="c4408-396">Pojmenujte nový zdroj dat jako **Trans**. V poli **Tabulka** vyberte hodnotu **VendTrans** a určete tak, že tento zdroj dat bude vyžadovat tabulku VendTrans.</span><span class="sxs-lookup"><span data-stu-id="c4408-396">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
6. <span data-ttu-id="c4408-397">Přidejte zdroj dat typu **Vypočítané pole** jako vnořené pole zdroje dat **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="c4408-397">Add a data source of the **Calculated field** type as the nested field of the **Vendor** data source.</span></span>
7. <span data-ttu-id="c4408-398">Pojmenujte nový zdroj dat jako **FilteredTrans** a konfigurujte jej tak, aby obsahoval výraz `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="c4408-398">Name the new data source **FilteredTrans**, and configure it so that it contains the expression `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span></span>
8. <span data-ttu-id="c4408-399">Přidejte zdroj dat typu **Spojit**.</span><span class="sxs-lookup"><span data-stu-id="c4408-399">Add a data source of the **Join** type.</span></span>
9. <span data-ttu-id="c4408-400">Pojmenujte nový zdroj dat jako **JoinedList** a konfigurujte jej následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="c4408-400">Name the new data source **JoinedList**, and configure it in the following way:</span></span>

    1. <span data-ttu-id="c4408-401">Přidejte zdroj dat **Vendor** jako první sadu záznamů, která bude spojena.</span><span class="sxs-lookup"><span data-stu-id="c4408-401">Add the **Vendor** data source as the first set of records to join.</span></span>
    2. <span data-ttu-id="c4408-402">Přidejte zdroj dat **Vendor.FilteredTrans** jako druhou sadu záznamů, která bude spojena.</span><span class="sxs-lookup"><span data-stu-id="c4408-402">Add the **Vendor.FilteredTrans** data source as the second set of records to join.</span></span> <span data-ttu-id="c4408-403">Vyberte typ spojení **INNER**.</span><span class="sxs-lookup"><span data-stu-id="c4408-403">Select **INNER** as the type.</span></span>
    3. <span data-ttu-id="c4408-404">V poli **Provést** vyberte **Dotaz** a určete tak, že chcete spustit tento zdroj dat na úrovni databáze.</span><span class="sxs-lookup"><span data-stu-id="c4408-404">In the **Execute** field, select **Query** to specify that you want to run this data source at the database level.</span></span>

    ![Konfigurace zdroje dat na stránce návrháře spojení](./media/er-components-inspections-06a.gif)

10. <span data-ttu-id="c4408-406">Výběrem příkazu **Ověřit** zkontrolujte upravitelnou komponentu mapování modelu na stránce **návrháře mapování modelů** a ověřte, zda je možné konfigurovaný zdroj dat **JoinedList** používat v dotazech.</span><span class="sxs-lookup"><span data-stu-id="c4408-406">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **JoinedList** data source can be queried.</span></span>
11. <span data-ttu-id="c4408-407">Změňte výraz zdroje dat **Vendor.FilteredTrans** z `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` na `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="c4408-407">Change the expression of the **Vendor.FilteredTrans** data source from `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` to `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.</span></span>
12. <span data-ttu-id="c4408-408">Výběrem příkazu **Ověřit** zkontrolujte upravitelnou komponentu mapování modelu na stránce **návrháře mapování modelů** a ověřte, zda je možné konfigurovaný zdroj dat **JoinedList** používat v dotazech.</span><span class="sxs-lookup"><span data-stu-id="c4408-408">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page and verify that the configured **JoinedList** data source can be queried.</span></span>

    ![Ověření upravitelné komponenty mapování modelu a ověření, že je možné konfigurovaný zdroj dat JoinedList používat v dotazech na stránce návrháře mapování modelu](./media/er-components-inspections-06b.png)

13. <span data-ttu-id="c4408-410">Všimněte si, že dojde k chybě ověření, protože výraz zdroje dat **Vendor.FilteredTrans** nelze přeložit na přímé volání SQL.</span><span class="sxs-lookup"><span data-stu-id="c4408-410">Notice that a validation error occurs, because the expression of the **Vendor.FilteredTrans** data source can't be translated to the direct SQL call.</span></span> <span data-ttu-id="c4408-411">Přímé volání SQL navíc neumožňuje volání zdroje dat **JoinedList**, které má být přeloženo do přímého příkazu SQL.</span><span class="sxs-lookup"><span data-stu-id="c4408-411">Additionally, the direct SQL call doesn't allow the call for the **JoinedList** data source to be translated to the direct SQL statement.</span></span>

    ![Chyby za běhu z neúspěšného ověření zdroje dat JoinedList na stránce návrháře mapování modelů](./media/er-components-inspections-06c.png)

<span data-ttu-id="c4408-413">Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění a výběrem příkazu **Spustit** spustíte formát, který má konfigurováno použití mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="c4408-413">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run a format that is configured to use the model mapping.</span></span>

![Spuštění upravitelného formátu na stránce Návrhář formátů](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="c4408-415">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-415">Automatic resolution</span></span>

<span data-ttu-id="c4408-416">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="c4408-416">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="c4408-417">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-417">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="c4408-418">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="c4408-418">Option 1</span></span>

<span data-ttu-id="c4408-419">Změňte výraz zdroje dat **Vendor.FilteredTrans** z `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` zpět na `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, jak doporučovalo zobrazené upozornění.</span><span class="sxs-lookup"><span data-stu-id="c4408-419">Change the expression of the **Vendor.FilteredTrans** data source from `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` back to `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, as the warning advised.</span></span>

![Aktualizovaný výraz zdroje dat na stránce návrháře mapování modelů](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a><span data-ttu-id="c4408-421">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="c4408-421">Option 2</span></span>

<span data-ttu-id="c4408-422">Změňte hodnotu pole **Provést** pro zdroj dat **JoinedList** z hodnoty **Dotaz** na **V paměti**.</span><span class="sxs-lookup"><span data-stu-id="c4408-422">Change the value of the **Execute** field for the **JoinedList** data source from **Query** to **In memory**.</span></span> <span data-ttu-id="c4408-423">Nedoporučujeme měnit hodnotu v tabulce, která obsahuje velké množství dat (transakční tabulka), protože budou načteny všechny záznamy a seskupení bude provedeno v paměti.</span><span class="sxs-lookup"><span data-stu-id="c4408-423">We don't recommend that you change the value for a table that has a large volume of data (transactional table), because all records will be fetched, and the join occurs in memory.</span></span> <span data-ttu-id="c4408-424">Tento přístup proto může způsobit špatný výkon.</span><span class="sxs-lookup"><span data-stu-id="c4408-424">Therefore, this approach can cause poor performance.</span></span> <span data-ttu-id="c4408-425">Zobrazí se upozornění ověření, které vás bude informovat o tomto riziku.</span><span class="sxs-lookup"><span data-stu-id="c4408-425">A validation warning is shown to inform you about this risk.</span></span>

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a><span data-ttu-id="c4408-426">Je vhodnější funkce FILTER nebo WHERE?</span><span class="sxs-lookup"><span data-stu-id="c4408-426">Preferability of FILTER vs WHERE function</span></span>

<span data-ttu-id="c4408-427">Integrovaná funkce ER [FILTER](er-functions-list-filter.md) se používá pro přístup k aplikačním tabulkám, pohledům nebo datovým entitám umístěním jediného volání SQL, které získá požadovaná data jako seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="c4408-427">The built-in [FILTER](er-functions-list-filter.md) ER function is used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="c4408-428">Funkce [WHERE](er-functions-list-where.md) načte všechny záznamy z daného zdroje a provede výběr záznamů v paměti.</span><span class="sxs-lookup"><span data-stu-id="c4408-428">The [WHERE](er-functions-list-where.md) function fetches all records from the given source and does record selection in memory.</span></span> <span data-ttu-id="c4408-429">Zdroj dat typu **Seznam záznamů** se používá jako argument obou funkcí a určuje zdroj pro načtení záznamů.</span><span class="sxs-lookup"><span data-stu-id="c4408-429">A data source of the **Record list** type is used as an argument of both functions and specifies a source for getting records.</span></span> <span data-ttu-id="c4408-430">ER kontroluje, zda lze navázat přímé volání SQL do zdroje dat, na který se odkazuje ve funkci **WHERE**.</span><span class="sxs-lookup"><span data-stu-id="c4408-430">ER checks whether a direct SQL call can be established to a data source that is referred to in the **WHERE** function.</span></span> <span data-ttu-id="c4408-431">Pokud nelze navázat přímé volání, je v návrháři mapování modelu ER vyvoláno upozornění ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-431">If a direct call can be established, a validation warning occurs in the ER model mapping designer.</span></span> <span data-ttu-id="c4408-432">Zpráva, kterou obdržíte, doporučuje použít funkci **FILTER** namísto **WHERE**, která pomůže zlepšit efektivitu.</span><span class="sxs-lookup"><span data-stu-id="c4408-432">The message that you receive recommends that you use the **FILTER** function instead of the **WHERE** function to help improve efficiency.</span></span>

<span data-ttu-id="c4408-433">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="c4408-433">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="c4408-434">Začněte konfigurací komponenty mapování modelu ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-434">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="c4408-435">Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.</span><span class="sxs-lookup"><span data-stu-id="c4408-435">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="c4408-436">Pojmenujte nový zdroj dat jako **Trans**. V poli **Tabulka** vyberte hodnotu **VendTrans** a určete tak, že tento zdroj dat bude vyžadovat tabulku VendTrans.</span><span class="sxs-lookup"><span data-stu-id="c4408-436">Name the new data source **Trans**. In the **Table** field, select **VendTrans** to specify that this data source will request the VendTrans table.</span></span>
4. <span data-ttu-id="c4408-437">Přidejte zdroj dat typu **Vypočítané pole** jako vnořené pole zdroje dat **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="c4408-437">Add a data source of the **Calculated field** type as the nested field of the **Vendor** data source.</span></span>
5. <span data-ttu-id="c4408-438">Pojmenujte nový zdroj dat jako **FilteredTrans** a konfigurujte jej tak, aby obsahoval výraz `WHERE(Trans, Trans.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="c4408-438">Name the new data source **FilteredTrans**, and configure it so that it contains the expression `WHERE(Trans, Trans.AccountNum="US-101")`.</span></span>
6. <span data-ttu-id="c4408-439">Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.</span><span class="sxs-lookup"><span data-stu-id="c4408-439">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="c4408-440">Pojmenujte nový zdroj dat jako **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="c4408-440">Name the new data source **Vendor**.</span></span> <span data-ttu-id="c4408-441">V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.</span><span class="sxs-lookup"><span data-stu-id="c4408-441">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="c4408-442">Přidejte zdroj dat typu **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="c4408-442">Add a data source of the **Calculated field** type.</span></span>
9. <span data-ttu-id="c4408-443">Pojmenujte nový zdroj dat jako **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="c4408-443">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span>
10. <span data-ttu-id="c4408-444">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu mapování modelu na stránce **Návrhář mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="c4408-444">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![Kontrola upravitelné komponenty mapování modelu ER na stránce Návrhář mapování modelu](./media/er-components-inspections-07a.png)

11. <span data-ttu-id="c4408-446">Všimněte si, že upozornění ověření doporučují používat funkci **FILTER** namísto funkce **WHERE** u zdrojů dat **FilteredVendor** a **FilteredTrans**.</span><span class="sxs-lookup"><span data-stu-id="c4408-446">Notice that validation warnings recommend that you use the **FILTER** function instead of the **WHERE** function for the **FilteredVendor** and **FilteredTrans** data sources.</span></span>

    ![Doporučení použití funkce FILTER namísto funkce WHERE na stránce návrháře mapování modelů](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="c4408-448">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-448">Automatic resolution</span></span>

<span data-ttu-id="c4408-449">Výběrem příkazu **Opravit** automaticky nahradíte funkci **WHERE** funkcí **FILTER** ve výrazu všech zdrojů dat, které se objevují v mřížce na kartě **Upozornění** pro tento typ kontroly.</span><span class="sxs-lookup"><span data-stu-id="c4408-449">Select **Fix** to automatically replace the **WHERE** function with the **FILTER** function in the expression of all data sources that appear in the grid on the **Warnings** tab for this type of inspection.</span></span>

<span data-ttu-id="c4408-450">Alternativně můžete vybrat řádek pro jedno upozornění v mřížce a poté vybrat příkaz **Opravit vybrané**.</span><span class="sxs-lookup"><span data-stu-id="c4408-450">Alternatively, you can select the row for a single warning in the grid and then select **Fix selected**.</span></span> <span data-ttu-id="c4408-451">V tomto případě se výraz automaticky změní pouze ve zdroji dat, který je uveden ve vybraném upozornění.</span><span class="sxs-lookup"><span data-stu-id="c4408-451">In this case, the expression is automatically changed only in the data source that is mentioned in the selected warning.</span></span>

![Výběrem možnosti Opravit automaticky nahradíte funkci WHERE funkcí FILTER na stránce návrháře mapování modelů](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a><span data-ttu-id="c4408-453">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-453">Manual resolution</span></span>

<span data-ttu-id="c4408-454">Výrazy všech zdrojů dat, které jsou uvedeny v ověřovací mřížce, můžete ručně upravit nahrazením funkce **WHERE** za funkci **FILTER**.</span><span class="sxs-lookup"><span data-stu-id="c4408-454">You can manually adjust the expressions of all the data sources in the validation grid by replacing the **WHERE** function with the **FILTER** function.</span></span>

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a><span data-ttu-id="c4408-455">Je vhodnější funkce ALLITEMSQUERY nebo ALLITEMS?</span><span class="sxs-lookup"><span data-stu-id="c4408-455">Preferability of ALLITEMSQUERY vs ALLITEMS function</span></span>

<span data-ttu-id="c4408-456">Integrované funkce ER [ALLITEMS](er-functions-list-allitems.md) a [ALLITEMSQUERY](er-functions-list-allitemsquery.md) se používají k získání ploché hodnoty **seznamu záznamů**, která se skládá ze seznamu záznamů, které představují všechny položky odpovídající zadané cestě.</span><span class="sxs-lookup"><span data-stu-id="c4408-456">The built-in [ALLITEMS](er-functions-list-allitems.md) and [ALLITEMSQUERY](er-functions-list-allitemsquery.md) ER functions return a flattened **Record list** value that consists of a list of records that represent all items that match the specified path.</span></span> <span data-ttu-id="c4408-457">ER kontroluje, zda lze navázat přímé volání SQL do zdroje dat, na který se odkazuje ve funkci **ALLITEMS**.</span><span class="sxs-lookup"><span data-stu-id="c4408-457">ER checks whether a direct SQL call can be established to a data source that is referred to in the **ALLITEMS** function.</span></span> <span data-ttu-id="c4408-458">Pokud nelze navázat přímé volání, je v návrháři mapování modelu ER vyvoláno upozornění ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-458">If a direct call can be established, a validation warning occurs in the ER model mapping designer.</span></span> <span data-ttu-id="c4408-459">Zpráva, kterou obdržíte, doporučuje použít funkci **ALLITEMSQUERY** namísto **ALLITEMS**, která pomůže zlepšit efektivitu.</span><span class="sxs-lookup"><span data-stu-id="c4408-459">The message that you receive recommends that you use the **ALLITEMSQUERY** function instead of the **ALLITEMS** function to help improve efficiency.</span></span>

<span data-ttu-id="c4408-460">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="c4408-460">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="c4408-461">Začněte konfigurací komponenty mapování modelu ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-461">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="c4408-462">Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.</span><span class="sxs-lookup"><span data-stu-id="c4408-462">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="c4408-463">Pojmenujte nový zdroj dat jako **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="c4408-463">Name the new data source **Vendor**.</span></span> <span data-ttu-id="c4408-464">V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.</span><span class="sxs-lookup"><span data-stu-id="c4408-464">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="c4408-465">K získání záznamů za několik dodavatelů přidejte zdroj dat typu **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="c4408-465">Add a data source of the **Calculated field** type to get records for several vendors.</span></span>
5. <span data-ttu-id="c4408-466">Pojmenujte nový zdroj dat jako **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.</span><span class="sxs-lookup"><span data-stu-id="c4408-466">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.</span></span>
6. <span data-ttu-id="c4408-467">K získání transakcí všech vyfiltrovaných dodavatelů přidejte zdroj dat typu **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="c4408-467">Add a data source of the **Calculated field** type to get the transactions of all filtered vendors.</span></span>
7. <span data-ttu-id="c4408-468">Pojmenujte nový zdroj dat jako **FilteredVendorTrans** a konfigurujte jej tak, aby obsahoval výraz `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.</span><span class="sxs-lookup"><span data-stu-id="c4408-468">Name the new data source **FilteredVendorTrans**, and configure it so that it contains the expression `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.</span></span>
8. <span data-ttu-id="c4408-469">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu mapování modelu na stránce **Návrhář mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="c4408-469">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![Kontrola upravitelné komponenty mapování modelu na stránce Návrhář mapování modelu](./media/er-components-inspections-08a.png)

9. <span data-ttu-id="c4408-471">Všimněte si, že se zobrazí upozornění ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-471">Notice that a validation warning occurs.</span></span> <span data-ttu-id="c4408-472">Zpráva doporučuje použít funkci **ALLITEMSQUERY** namísto funkce **ALLITEMS** pro zdroj dat **FilteredVendorTrans**.</span><span class="sxs-lookup"><span data-stu-id="c4408-472">The message recommends that you use the **ALLITEMSQUERY** function instead of the **ALLITEMS** function for the **FilteredVendorTrans** data source.</span></span>

    ![Doporučení použití funkce ALLITEMSQUERY namísto funkce ALLITEMS na stránce návrháře mapování modelů](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="c4408-474">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-474">Automatic resolution</span></span>

<span data-ttu-id="c4408-475">Výběrem příkazu **Opravit** automaticky nahradíte funkci **ALLITEMS** funkcí **ALLITEMSQUERY** ve výrazu všech zdrojů dat, které se objevují v mřížce na kartě **Upozornění** pro tento typ kontroly.</span><span class="sxs-lookup"><span data-stu-id="c4408-475">Select **Fix** to automatically replace the **ALLITEMS** function with the **ALLITEMSQUERY** function in the expression of all data sources that appear in the grid on the **Warnings** tab for this type of inspection.</span></span>

<span data-ttu-id="c4408-476">Alternativně můžete vybrat řádek pro jedno upozornění v mřížce a poté vybrat příkaz **Opravit vybrané**.</span><span class="sxs-lookup"><span data-stu-id="c4408-476">Alternatively, you can select the row for a single warning in the grid and then select **Fix selected**.</span></span> <span data-ttu-id="c4408-477">V tomto případě se výraz automaticky změní pouze ve zdroji dat, který je uveden ve vybraném upozornění.</span><span class="sxs-lookup"><span data-stu-id="c4408-477">In this case, the expression is automatically changed only in the data source that is mentioned in the selected warning.</span></span>

![Výběr příkazu Opravit vybrané na stránce návrháře mapování modelů](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a><span data-ttu-id="c4408-479">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-479">Manual resolution</span></span>

<span data-ttu-id="c4408-480">Výrazy všech zdrojů dat, které jsou uvedeny v ověřovací mřížce, můžete ručně upravit nahrazením funkce **ALLITEMS** za funkci **ALLITEMSQUERY**.</span><span class="sxs-lookup"><span data-stu-id="c4408-480">You can manually adjust the expressions of all the data sources that are mentioned in the validation grid by replacing the **ALLITEMS** function with the **ALLITEMSQUERY** function.</span></span>

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a><span data-ttu-id="c4408-481">Možnost výskytů prázdného seznamu</span><span class="sxs-lookup"><span data-stu-id="c4408-481">Consideration of empty list cases</span></span>

<span data-ttu-id="c4408-482">Komponentu formátu nebo mapování modelu ER můžete konfigurovat tak, abyste získali hodnotu pole zdroje dat typu **Seznam záznamů**.</span><span class="sxs-lookup"><span data-stu-id="c4408-482">You can configure your ER format or model mapping component to get the field value of a data source of the **Record list** type.</span></span> <span data-ttu-id="c4408-483">ER zkontroluje, zda váš návrh zohledňuje případ, kdy zdroj dat, který je volán, neobsahuje žádné záznamy (tedy je prázdný), aby se předešlo chybám za běhu při načtení hodnoty z pole neexistujícího záznamu.</span><span class="sxs-lookup"><span data-stu-id="c4408-483">ER checks whether your design considers the case where a data source that is called contains no records (that is, it's empty), to prevent runtime errors when a value is fetched from a field of a nonexistent record.</span></span>

<span data-ttu-id="c4408-484">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="c4408-484">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="c4408-485">Začněte konfigurovat datový model ER, mapování modelu ER a komponenty formátu ER současně.</span><span class="sxs-lookup"><span data-stu-id="c4408-485">Start to configure the ER data model, the ER model mapping, and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="c4408-486">Ve stromu datového modelu přidejte kořenovou položku s názvem **Root3**.</span><span class="sxs-lookup"><span data-stu-id="c4408-486">In the data model tree, add a root item that is named **Root3**.</span></span>
3. <span data-ttu-id="c4408-487">Upravte položku **Root3** přidáním vnořené položky typu **Seznam záznamů**.</span><span class="sxs-lookup"><span data-stu-id="c4408-487">Modify the **Root3** item by adding a nested item of the **Record list** type.</span></span>
4. <span data-ttu-id="c4408-488">Pojmenujte novou vnořenou položku jako **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="c4408-488">Name the new nested item **Vendor**.</span></span>
5. <span data-ttu-id="c4408-489">Upravte položku **Vendor** následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="c4408-489">Modify the **Vendor** item in the following way:</span></span>

    - <span data-ttu-id="c4408-490">Přidejte vnořené pole typu **Řetězec** a pojmenujte jej jako **Name**.</span><span class="sxs-lookup"><span data-stu-id="c4408-490">Add a nested field of the **String** type, and name it **Name**.</span></span>
    - <span data-ttu-id="c4408-491">Přidejte vnořené pole typu **Řetězec** a pojmenujte jej jako **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="c4408-491">Add a nested field of the **String** type, and name it **AccountNumber**.</span></span>

    ![Přidání vnořených polí na stránce Datový model](./media/er-components-inspections-09a.png)

6. <span data-ttu-id="c4408-493">V podokně **Zdroje dat** mapování modelu přidejte zdroj dat typu **Dynamics 365 for Operations \\ Záznamy tabulky**.</span><span class="sxs-lookup"><span data-stu-id="c4408-493">In the model mapping designer, in the **Data sources** pane, add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="c4408-494">Pojmenujte nový zdroj dat jako **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="c4408-494">Name the new data source **Vendor**.</span></span> <span data-ttu-id="c4408-495">V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.</span><span class="sxs-lookup"><span data-stu-id="c4408-495">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="c4408-496">Přidejte zdroj dat typu **Všeobecné \\ Uživatelský vstupní parametr** pro vyhledání účtu dodavatele v dialogovém okně modulu runtime.</span><span class="sxs-lookup"><span data-stu-id="c4408-496">Add a data source of the **General \\ User input parameter** type to search for a vendor account in the runtime dialog box.</span></span>
9. <span data-ttu-id="c4408-497">Pojmenujte nový zdroj dat jako **RequestedAccountNum**.</span><span class="sxs-lookup"><span data-stu-id="c4408-497">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="c4408-498">Do pole **Popisek** zadejte **Číslo účtu dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="c4408-498">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="c4408-499">V poli **Název datového typu Operations** ponechte výchozí hodnotu **Popis**.</span><span class="sxs-lookup"><span data-stu-id="c4408-499">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
10. <span data-ttu-id="c4408-500">K vyfiltrování dodavatele, o kterého se zajímáte, přidejte zdroj dat typu **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="c4408-500">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
11. <span data-ttu-id="c4408-501">Pojmenujte nový zdroj dat jako **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="c4408-501">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
12. <span data-ttu-id="c4408-502">Vytvořte vazbu položek datového modelu na konfigurované zdroje dat následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="c4408-502">Bind the data model items to configured data sources in the following way:</span></span>

    - <span data-ttu-id="c4408-503">Vytvořte vazbu položky **FilteredVendor** na položku **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="c4408-503">Bind **FilteredVendor** to **Vendor**.</span></span>
    - <span data-ttu-id="c4408-504">Vytvořte vazbu položky **FilteredVendor.AccountNum** na položku **Vendor.AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="c4408-504">Bind **FilteredVendor.AccountNum** to **Vendor.AccountNumber**.</span></span>
    - <span data-ttu-id="c4408-505">Vytvořte vazbu položky **FilteredVendor.'name()'** na položku **Vendor.Name**.</span><span class="sxs-lookup"><span data-stu-id="c4408-505">Bind **FilteredVendor.'name()'** to **Vendor.Name**.</span></span>

    ![Vázání položek datového modelu na stránce návrháře mapování modelů](./media/er-components-inspections-09b.png)

13. <span data-ttu-id="c4408-507">Ve stromu struktury formátu přidejte následující položky, které generují odchozí dokument ve formátu XML obsahující podrobnosti o dodavateli:</span><span class="sxs-lookup"><span data-stu-id="c4408-507">In the format structure tree, add the following items to generate an outbound document in XML format that contains the vendor details:</span></span>

    1. <span data-ttu-id="c4408-508">Přidejte kořenový prvek XML **Statement**.</span><span class="sxs-lookup"><span data-stu-id="c4408-508">Add the **Statement** root XML element.</span></span>
    2. <span data-ttu-id="c4408-509">U prvku XML **Statement** přidejte vnořený prvek XML **Party**.</span><span class="sxs-lookup"><span data-stu-id="c4408-509">For the **Statement** XML element, add the nested **Party** XML element.</span></span>
    3. <span data-ttu-id="c4408-510">U prvku XML **Party** přidejte následující vnořené atributy XML:</span><span class="sxs-lookup"><span data-stu-id="c4408-510">For the **Party** XML element, add the following nested XML attributes:</span></span>

        - <span data-ttu-id="c4408-511">Jméno</span><span class="sxs-lookup"><span data-stu-id="c4408-511">Name</span></span>
        - <span data-ttu-id="c4408-512">AccountNum</span><span class="sxs-lookup"><span data-stu-id="c4408-512">AccountNum</span></span>

14. <span data-ttu-id="c4408-513">Navažte prvky formátu na poskytnuté zdroje dat následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="c4408-513">Bind format elements to provided data sources in the following way:</span></span>

    - <span data-ttu-id="c4408-514">Vytvořte vazbu prvku formátu **Statement\\Party\\Name** na pole zdroje dat **model.Vendor.Name**.</span><span class="sxs-lookup"><span data-stu-id="c4408-514">Bind the **Statement\\Party\\Name** format element to the **model.Vendor.Name** data source field.</span></span>
    - <span data-ttu-id="c4408-515">Vytvořte vazbu prvku formátu **Statement\\Party\\AccountNum** na pole zdroje dat **model.Vendor.AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="c4408-515">Bind the **Statement\\Party\\AccountNum** format element to the **model.Vendor.AccountNumber** data source field.</span></span>

15. <span data-ttu-id="c4408-516">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu formátu na stránce **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="c4408-516">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![Ověření prvků formátu navázaných na zdroje dat na stránce Návrhář formátů](./media/er-components-inspections-09c.png)

16. <span data-ttu-id="c4408-518">Všimněte si, že dojde k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-518">Notice that a validation error occurs.</span></span> <span data-ttu-id="c4408-519">Zpráva uvádí, že chyba může být za běhu vyvolána u konfigurovaných komponent formátu **Statement\\Party\\Name** a **Statement\\Party\\AccountNum**, pokud je seznam `model.Vendor` prázdný.</span><span class="sxs-lookup"><span data-stu-id="c4408-519">The message states that an error might be thrown for the configured **Statement\\Party\\Name** and **Statement\\Party\\AccountNum** format components at runtime if the `model.Vendor` list is empty.</span></span>

    ![Chyba ověření, která upozorňuje na potenciální chybu u konfigurovaných komponent formátu](./media/er-components-inspections-09d.png)

<span data-ttu-id="c4408-521">Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění, vyberete příkaz **Spustit** a zvolíte číslo účtu neexistujícího dodavatele.</span><span class="sxs-lookup"><span data-stu-id="c4408-521">The following illustration shows the runtime error that occurs if you ignore the warning, select **Run** to run the format, and select the account number of a nonexistent vendor.</span></span> <span data-ttu-id="c4408-522">Protože požadovaný dodavatel neexistuje, seznam `model.Vendor` bude prázdný (to znamená, že nebude obsahovat žádné záznamy).</span><span class="sxs-lookup"><span data-stu-id="c4408-522">Because the requested vendor doesn't exist, the `model.Vendor` list will be empty (that is, it will contain no records).</span></span>

![Chyby za běhu, ke kterým došlo za běhu mapování formátu](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="c4408-524">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-524">Automatic resolution</span></span>

<span data-ttu-id="c4408-525">Pro vybraný řádek v mřížce na kartě **Upozornění** můžete vybrat příkaz **Zrušit vazbu**.</span><span class="sxs-lookup"><span data-stu-id="c4408-525">For the selected row in the grid on the **Warnings** tab, you can select **Unbind**.</span></span> <span data-ttu-id="c4408-526">Vazba, na kterou se ukazuje ve sloupci **Cesta**, je automaticky odebrána z prvků formátu.</span><span class="sxs-lookup"><span data-stu-id="c4408-526">The binding that is pointed to in the **Path** column is automatically removed from the format elements.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="c4408-527">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-527">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="c4408-528">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="c4408-528">Option 1</span></span>

<span data-ttu-id="c4408-529">Můžete navázat prvek formátu **Statement\\Party\\Name** na položku zdroje dat `model.Vendor`.</span><span class="sxs-lookup"><span data-stu-id="c4408-529">You can bind the **Statement\\Party\\Name** format element to the `model.Vendor` data source item.</span></span> <span data-ttu-id="c4408-530">Za běhu tato vazba volá nejprve zdroj dat `model.Vendor`.</span><span class="sxs-lookup"><span data-stu-id="c4408-530">At runtime, this binding calls the `model.Vendor` data source first.</span></span> <span data-ttu-id="c4408-531">Když `model.Vendor` vrátí prázdný seznam záznamů, vnořené prvky formátu se nespustí.</span><span class="sxs-lookup"><span data-stu-id="c4408-531">When `model.Vendor` returns an empty record list, the nested format elements aren't run.</span></span> <span data-ttu-id="c4408-532">Proto u této konfigurace formátu nejsou vyvolána žádná upozornění ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-532">Therefore, no validation warnings occur for this format configuration.</span></span>

![Vazba prvku formátu na položku zdroje dat na stránce Návrhář formátů](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a><span data-ttu-id="c4408-534">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="c4408-534">Option 2</span></span>

<span data-ttu-id="c4408-535">Změňte vazbu prvku formátu **Statement\\Party\\Name** z `model.Vendor.Name` na `FIRSTORNULL(model.Vendor).Name`.</span><span class="sxs-lookup"><span data-stu-id="c4408-535">Change the binding of the **Statement\\Party\\Name** format element from `model.Vendor.Name` to `FIRSTORNULL(model.Vendor).Name`.</span></span> <span data-ttu-id="c4408-536">Aktualizovaná vazba podmíněně převede první záznam zdroje dat `model.Vendor` typu **Seznam záznamů** na nový zdroj dat typu **Záznam**.</span><span class="sxs-lookup"><span data-stu-id="c4408-536">The updated binding conditionally converts the first record of the `model.Vendor` data source of the **Record list** type to a new data source of the **Record** type.</span></span> <span data-ttu-id="c4408-537">Tento nový zdroj dat obsahuje stejnou sadu polí.</span><span class="sxs-lookup"><span data-stu-id="c4408-537">This new data source contains the same set of fields.</span></span>

- <span data-ttu-id="c4408-538">Pokud je ve zdroji dat `model.Vendor` k dispozici alespoň jeden záznam, pole tohoto záznamu jsou vyplněna hodnotami polí prvního záznamu zdroje dat `model.Vendor`.</span><span class="sxs-lookup"><span data-stu-id="c4408-538">If at least one record is available in the `model.Vendor` data source, the fields of that record are filled with the values of the fields of the first record of the `model.Vendor` data source.</span></span> <span data-ttu-id="c4408-539">V takovém případě aktualizovaná vazba vrátí název dodavatele.</span><span class="sxs-lookup"><span data-stu-id="c4408-539">In this case, the updated binding returns the vendor name.</span></span>
- <span data-ttu-id="c4408-540">V opačném případě je každé pole vytvořeného záznamu vyplněno výchozí hodnotou pro datový typ daného pole.</span><span class="sxs-lookup"><span data-stu-id="c4408-540">Otherwise, every field of the record that is created is filled with the default value for the data type of that field.</span></span> <span data-ttu-id="c4408-541">V tomto případě je vrácen prázdný řetězec jako výchozí hodnota datového typu **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="c4408-541">In this case, the blank string is returned as the default value of the **String** data type.</span></span>

<span data-ttu-id="c4408-542">Proto se pro prvek formátu **Statement\\Party\\Name** nevyskytují žádná upozornění ověření, když je vázán na výraz `FIRSTORNULL(model.Vendor).Name`.</span><span class="sxs-lookup"><span data-stu-id="c4408-542">Therefore, no validation warnings occur for the **Statement\\Party\\Name** format element when it's bound to the `FIRSTORNULL(model.Vendor).Name` expression.</span></span>

![Změněná vazba řeší upozornění ověření na stránce Návrhář formátů](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a><span data-ttu-id="c4408-544">Možnost 3</span><span class="sxs-lookup"><span data-stu-id="c4408-544">Option 3</span></span>

<span data-ttu-id="c4408-545">Pokud chcete explicitně určit data, která se zadávají do generovaného dokumentu, když zdroj dat `model.Vendor` typu **Seznam záznamů** nevrátí žádné záznamy (v tomto příkladu text **Not available**), změňte vazbu prvku formátu **Statement\\Party\\Name** z hodnoty `model.Vendor.Name` na `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`.</span><span class="sxs-lookup"><span data-stu-id="c4408-545">If you want to explicitly specify the data that is entered in a generated document when the `model.Vendor` data source of the **Record list** type returns no records (the text **Not available** in this example), change the binding of the **Statement\\Party\\Name** format element from `model.Vendor.Name` to `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`.</span></span> <span data-ttu-id="c4408-546">Můžete také použít výraz `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.</span><span class="sxs-lookup"><span data-stu-id="c4408-546">You can also use the expression `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.</span></span>

### <a name="additional-consideration"></a><a id="i9a"></a><span data-ttu-id="c4408-547">Další faktor ke zvážení</span><span class="sxs-lookup"><span data-stu-id="c4408-547">Additional consideration</span></span>

<span data-ttu-id="c4408-548">Inspekce vás také upozorňuje na další možný problém.</span><span class="sxs-lookup"><span data-stu-id="c4408-548">The inspection also warns you about another potential issue.</span></span> <span data-ttu-id="c4408-549">Ve výchozím nastavení při vazbě prvků formátu **Statement\\Party\\Name** a **Statement\\Party\\AccountNum** na příslušná pole zdroje dat `model.Vendor` typu **Seznam záznamů** budou tyto vazby spuštěny a načtou hodnoty odpovídajících polí prvního záznamu zdroje da `model.Vendor`, pokud tento seznam není prázdný.</span><span class="sxs-lookup"><span data-stu-id="c4408-549">By default, as you bind the **Statement\\Party\\Name** and **Statement\\Party\\AccountNum** format elements to the appropriate fields of the `model.Vendor` data source of the **Record list** type, those bindings will be run and will take the values of the appropriate fields of the first record of the `model.Vendor` data source, if that list isn't empty.</span></span>

<span data-ttu-id="c4408-550">Protože jste nevytvořili vazbu prvku formátu **Statement\\Party** se zdrojem dat `model.Vendor`, prvek **Statement\\Party** enebude během provádění formátu iterován pro každý záznam zdroje dat `model.Vendor`.</span><span class="sxs-lookup"><span data-stu-id="c4408-550">Because you haven't bound the **Statement\\Party** format element with the `model.Vendor` data source, the **Statement\\Party** element won't be iterated for every record of the `model.Vendor` data source during format execution.</span></span> <span data-ttu-id="c4408-551">Místo toho bude vygenerovaný dokument vyplněn informacemi pouze z prvního záznamu seznamu záznamů, pokud tento seznam obsahuje více záznamů.</span><span class="sxs-lookup"><span data-stu-id="c4408-551">Instead, a generated document will be filled with information from only the first record of the record list, if that list contains multiple records.</span></span> <span data-ttu-id="c4408-552">Proto může nastat problém, pokud je formát určen k vyplnění generovaného dokumentu informacemi o všech dodavatelích ze zdroje dat `model.Vendor`.</span><span class="sxs-lookup"><span data-stu-id="c4408-552">Therefore, there might be an issue if the format is intended to fill a generated document with information about all vendors from the `model.Vendor` data source.</span></span> <span data-ttu-id="c4408-553">Chcete-li tento problém napravit, vytvořte vazbu prvku **Statement\\Party** se zdrojem dat `model.Vendor`.</span><span class="sxs-lookup"><span data-stu-id="c4408-553">To fix this issue, bind the **Statement\\Party** element with the `model.Vendor` data source.</span></span>

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a><span data-ttu-id="c4408-554">Spustitelnost výrazu s funkcí FILTER (použití mezipaměti)</span><span class="sxs-lookup"><span data-stu-id="c4408-554">Executability of an expression with FILTER function (caching)</span></span>

<span data-ttu-id="c4408-555">Některé Integrované funkce ER, včetně [FILTER](er-functions-list-filter.md) a [ALLITEMSQUERY](er-functions-list-allitemsquery.md), se používají pro přístup k aplikačním tabulkám, pohledům nebo datovým entitám umístěním jediného volání SQL, které získá požadovaná data jako seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="c4408-555">Several built-in ER functions, including [FILTER](er-functions-list-filter.md) and [ALLITEMSQUERY](er-functions-list-allitemsquery.md), are used to access application tables, views, or data entities by placing a single SQL call to get the required data as a list of records.</span></span> <span data-ttu-id="c4408-556">Zdroj dat typu **Seznam záznamů** se používá jako argument každé z těchto funkcí a určuje zdroj aplikace pro volání.</span><span class="sxs-lookup"><span data-stu-id="c4408-556">A data source of the **Record list** type is used as an argument of each of these functions and specifies an application source for the call.</span></span> <span data-ttu-id="c4408-557">ER kontroluje, zda lze navázat přímé volání SQL do zdroje dat, na který se odkazuje v jedné z těchto funkcí.</span><span class="sxs-lookup"><span data-stu-id="c4408-557">ER checks whether a direct SQL call can be established to a data source that is referred to in one of these functions.</span></span> <span data-ttu-id="c4408-558">Pokud nelze navázat přímé volání, protože zdroj dat byl označen jako [ukládaný do mezipaměti](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace), dojde v návrháři mapování modelu ER k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-558">If a direct call can't be established because the data source was marked as [cached](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace), a validation error occurs in the ER model mapping designer.</span></span> <span data-ttu-id="c4408-559">Zpráva, kterou obdržíte, uvádí, že výraz ER obsahující jednu z těchto funkcí nelze spustit za běhu programu.</span><span class="sxs-lookup"><span data-stu-id="c4408-559">The message that you receive states that the ER expression that contains one of these functions can't be run at runtime.</span></span>

<span data-ttu-id="c4408-560">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="c4408-560">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="c4408-561">Začněte konfigurací komponenty mapování modelu ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-561">Start to configure the ER model mapping component.</span></span>
2. <span data-ttu-id="c4408-562">Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.</span><span class="sxs-lookup"><span data-stu-id="c4408-562">Add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
3. <span data-ttu-id="c4408-563">Pojmenujte nový zdroj dat jako **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="c4408-563">Name the new data source **Vendor**.</span></span> <span data-ttu-id="c4408-564">V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.</span><span class="sxs-lookup"><span data-stu-id="c4408-564">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
4. <span data-ttu-id="c4408-565">Přidejte zdroj dat typu **Všeobecné \\ Uživatelský vstupní parametr** pro vyhledání účtu dodavatele v dialogovém okně modulu runtime.</span><span class="sxs-lookup"><span data-stu-id="c4408-565">Add a data source of the **General \\ User input parameter** type to search for a vendor account in the runtime dialog box.</span></span>
5. <span data-ttu-id="c4408-566">Pojmenujte nový zdroj dat jako **RequestedAccountNum**.</span><span class="sxs-lookup"><span data-stu-id="c4408-566">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="c4408-567">Do pole **Popisek** zadejte **Číslo účtu dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="c4408-567">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="c4408-568">V poli **Název datového typu Operations** ponechte výchozí hodnotu **Popis**.</span><span class="sxs-lookup"><span data-stu-id="c4408-568">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
6. <span data-ttu-id="c4408-569">K vyfiltrování dodavatele, o kterého se zajímáte, přidejte zdroj dat typu **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="c4408-569">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
7. <span data-ttu-id="c4408-570">Pojmenujte nový zdroj dat jako **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="c4408-570">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
8. <span data-ttu-id="c4408-571">Označte konfigurovaný zdroj dat **Vendor** jako ukládaný v mezipaměti.</span><span class="sxs-lookup"><span data-stu-id="c4408-571">Mark the configured **Vendor** data source as cached.</span></span>

    ![Konfigurace komponenty mapování modelu na stránce Návrhář mapování modelu](./media/er-components-inspections-10a.gif)

9. <span data-ttu-id="c4408-573">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu mapování modelu na stránce **Návrhář mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="c4408-573">Select **Validate** to inspect the editable model mapping component on the **Model mapping designer** page.</span></span>

    ![Ověření funkce FILTER použité na zdroj dat dodavatele ukládaný do mezipaměti na stránce návrháře mapování modelů](./media/er-components-inspections-10a.png)

10. <span data-ttu-id="c4408-575">Všimněte si, že dojde k chybě ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-575">Notice that a validation error occurs.</span></span> <span data-ttu-id="c4408-576">Zpráva uvádí, že funkci **FILTER** nelze použít na zdroj dat **Vendor**, který je ukládán do mezipaměti.</span><span class="sxs-lookup"><span data-stu-id="c4408-576">The message states that the **FILTER** function can't be applied to the cached **Vendor** data source.</span></span>

<span data-ttu-id="c4408-577">Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění a výběrem příkazu **Spustit** spustíte formát.</span><span class="sxs-lookup"><span data-stu-id="c4408-577">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run the format.</span></span>

![Chyba za běhu, ke které dojde během provádění mapování formátu na stránce Návrhář formátů](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="c4408-579">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-579">Automatic resolution</span></span>

<span data-ttu-id="c4408-580">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="c4408-580">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="c4408-581">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-581">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="c4408-582">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="c4408-582">Option 1</span></span>

<span data-ttu-id="c4408-583">Odstraňte příznak **Mezipaměť** ze zdroje dat **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="c4408-583">Remove the **Cache** flag from the **Vendor** data source.</span></span> <span data-ttu-id="c4408-584">Zdroj dat **FilteredVendor** zdroj dat se poté stane spustitelným, ale zdroj dat **Vendor**, na který se odkazuje v tabulce VendTable, bude přístupný pokaždé, když je volán zdroj dat **FilteredVendor**.</span><span class="sxs-lookup"><span data-stu-id="c4408-584">The **FilteredVendor** data source will then become executable, but the **Vendor** data source that is referred to in the VendTable table will be accessed every time that the **FilteredVendor** data source is called.</span></span>

#### <a name="option-2"></a><span data-ttu-id="c4408-585">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="c4408-585">Option 2</span></span>

<span data-ttu-id="c4408-586">Změňte výraz zdroje dat **FilteredVendor** z `FILTER(Vendor, Vendor.AccountNum="US-101")` na `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span><span class="sxs-lookup"><span data-stu-id="c4408-586">Change the expression of the **FilteredVendor** data source from `FILTER(Vendor, Vendor.AccountNum="US-101")` to `WHERE(Vendor, Vendor.AccountNum="US-101")`.</span></span> <span data-ttu-id="c4408-587">V tomto případě bude ke zdroji dat **Vendor**, na který se odkazuje v tabulce VendTable, přistupováno pouze během prvního volání zdroje dat **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="c4408-587">In this case, the **Vendor** data source that is referred to in the VendTable table will be accessed only during the first call of the **Vendor** data source.</span></span> <span data-ttu-id="c4408-588">Výběr záznamů se však provede v paměti.</span><span class="sxs-lookup"><span data-stu-id="c4408-588">However, the selection of records will be done in memory.</span></span> <span data-ttu-id="c4408-589">Tento přístup proto může způsobit špatný výkon.</span><span class="sxs-lookup"><span data-stu-id="c4408-589">Therefore, this approach can cause poor performance.</span></span>

## <a name="missing-binding"></a><a id="i11"></a><span data-ttu-id="c4408-590">Chybějící vazba</span><span class="sxs-lookup"><span data-stu-id="c4408-590">Missing binding</span></span>

<span data-ttu-id="c4408-591">Když konfigurujete komponentu formátu ER, nabídne se základní datový model ER jako výchozí zdroj dat pro formát ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-591">When you configure an ER format component, the base ER data model is offered as a default data source for the ER format.</span></span> <span data-ttu-id="c4408-592">Když je spuštěn konfigurovaný formát ER, použije se k vyplnění datového modelu aplikačními daty [výchozí mapování modelu](er-country-dependent-model-mapping.md) pro základní model.</span><span class="sxs-lookup"><span data-stu-id="c4408-592">When the configured ER format is run, the [default model mapping](er-country-dependent-model-mapping.md) for the base model is used to fill the data model with application data.</span></span> <span data-ttu-id="c4408-593">Návrhář formátu ER zobrazí upozornění, pokud vytvoříte vazbu prvku formátu na položku datového modelu, která není vázána na žádný zdroj dat v tom mapování modelu, který je aktuálně vybrán jako výchozí mapování modelu pro upravitelný formát.</span><span class="sxs-lookup"><span data-stu-id="c4408-593">The ER format designer shows a warning if you bind a format element to a data model item that isn't bound to any data source in the model mapping that is currently selected as the default model mapping for the editable format.</span></span> <span data-ttu-id="c4408-594">Tento typ vazby nelze spustit za běhu, protože spuštěný formát nemůže vyplnit vázaný prvek daty aplikace.</span><span class="sxs-lookup"><span data-stu-id="c4408-594">This type of binding can't be run at runtime, because the format that runs can't fill a bound element with application data.</span></span> <span data-ttu-id="c4408-595">Proto za běhu dojde k chybě.</span><span class="sxs-lookup"><span data-stu-id="c4408-595">Therefore, an error occurs at runtime.</span></span>

<span data-ttu-id="c4408-596">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="c4408-596">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="c4408-597">Začněte konfigurovat datový model ER, mapování modelu ER a komponenty formátu ER současně.</span><span class="sxs-lookup"><span data-stu-id="c4408-597">Start to configure the ER data model, the ER model mapping, and the ER format components simultaneously.</span></span>
2. <span data-ttu-id="c4408-598">Ve stromu datového modelu přidejte kořenovou položku s názvem **Root3**.</span><span class="sxs-lookup"><span data-stu-id="c4408-598">In the data model tree, add a root item that is named **Root3**.</span></span>
3. <span data-ttu-id="c4408-599">Upravte položku **Root3** a přidejte do ní novou vnořenou položku typu **Seznam záznamů**.</span><span class="sxs-lookup"><span data-stu-id="c4408-599">Modify the **Root3** item by adding a new nested item of the **Record list** type.</span></span>
4. <span data-ttu-id="c4408-600">Pojmenujte novou vnořenou položku jako **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="c4408-600">Name the new nested item **Vendor**.</span></span>
5. <span data-ttu-id="c4408-601">Upravte položku **Vendor** následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="c4408-601">Modify the **Vendor** item in the following way:</span></span>

    - <span data-ttu-id="c4408-602">Přidejte vnořené pole typu **Řetězec** a pojmenujte jej jako **Name**.</span><span class="sxs-lookup"><span data-stu-id="c4408-602">Add a nested field of the **String** type, and name it **Name**.</span></span>
    - <span data-ttu-id="c4408-603">Přidejte vnořené pole typu **Řetězec** a pojmenujte jej jako **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="c4408-603">Add a nested field of the **String** type, and name it **AccountNumber**.</span></span>

    ![Přidání vnořených polí k položce dodavatele na stránce Datový model](./media/er-components-inspections-11a.png)

6. <span data-ttu-id="c4408-605">V podokně **Zdroje dat** mapování modelu přidejte zdroj dat typu **Dynamics 365 for Operations \\ Záznamy tabulky**.</span><span class="sxs-lookup"><span data-stu-id="c4408-605">In the model mapping designer, in the **Data sources** pane, add a data source of the **Dynamics 365 for Operations \\ Table records** type.</span></span>
7. <span data-ttu-id="c4408-606">Pojmenujte nový zdroj dat jako **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="c4408-606">Name the new data source **Vendor**.</span></span> <span data-ttu-id="c4408-607">V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.</span><span class="sxs-lookup"><span data-stu-id="c4408-607">In the **Table** field, select **VendTable** to specify that this data source will request the VendTable table.</span></span>
8. <span data-ttu-id="c4408-608">Přidejte zdroj dat typu **Všeobecné \\ Uživatelský vstupní parametr** pro získání informací o účtu dodavatele v dialogovém okně modulu runtime.</span><span class="sxs-lookup"><span data-stu-id="c4408-608">Add a data source of the **General \\ User input parameter** type to inquire about a vendor account in the runtime dialog box.</span></span>
9. <span data-ttu-id="c4408-609">Pojmenujte nový zdroj dat jako **RequestedAccountNum**.</span><span class="sxs-lookup"><span data-stu-id="c4408-609">Name the new data source **RequestedAccountNum**.</span></span> <span data-ttu-id="c4408-610">Do pole **Popisek** zadejte **Číslo účtu dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="c4408-610">In the **Label** field, enter **Vendor account number**.</span></span> <span data-ttu-id="c4408-611">V poli **Název datového typu Operations** ponechte výchozí hodnotu **Popis**.</span><span class="sxs-lookup"><span data-stu-id="c4408-611">In the **Operations data type name** field, leave the default value, **Description**.</span></span>
10. <span data-ttu-id="c4408-612">K vyfiltrování dodavatele, o kterého se zajímáte, přidejte zdroj dat typu **Vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="c4408-612">Add a data source of the **Calculated field** type to filter a vendor that is inquired about.</span></span>
11. <span data-ttu-id="c4408-613">Pojmenujte nový zdroj dat jako **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span><span class="sxs-lookup"><span data-stu-id="c4408-613">Name the new data source **FilteredVendor**, and configure it so that it contains the expression `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.</span></span>
12. <span data-ttu-id="c4408-614">Vytvořte vazbu položek datového modelu na konfigurované zdroje dat následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="c4408-614">Bind the data model items to configured data sources in the following way:</span></span>

    - <span data-ttu-id="c4408-615">Vytvořte vazbu položky **FilteredVendor** na položku **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="c4408-615">Bind **FilteredVendor** to **Vendor**.</span></span>
    - <span data-ttu-id="c4408-616">Vytvořte vazbu položky **FilteredVendor.AccountNum** na položku **Vendor.AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="c4408-616">Bind **FilteredVendor.AccountNum** to **Vendor.AccountNumber**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c4408-617">Pole datového modelu **Vendor.Name** zůstává nevázané.</span><span class="sxs-lookup"><span data-stu-id="c4408-617">The **Vendor.Name** data model field remains unbound.</span></span>

    ![Položky datového modelu vázané na konfigurované zdroje dat a položka datového režimu, která zůstává neomezená na stránce Návrháře mapování modelů](./media/er-components-inspections-11b.png)

13. <span data-ttu-id="c4408-619">Ve stromu struktury formátu přidejte následující položky, které generují odchozí dokument ve formátu XML obsahující podrobnosti o dodavatelích, kteří vás zajímají:</span><span class="sxs-lookup"><span data-stu-id="c4408-619">In the format structure tree, add the following items to generate an outbound document in XML format that contains the details of the vendors that are inquired about:</span></span>

    1. <span data-ttu-id="c4408-620">Přidejte kořenový prvek XML **Statement**.</span><span class="sxs-lookup"><span data-stu-id="c4408-620">Add the **Statement** root XML element.</span></span>
    2. <span data-ttu-id="c4408-621">U prvku XML **Statement** přidejte vnořený prvek XML **Party**.</span><span class="sxs-lookup"><span data-stu-id="c4408-621">For the **Statement** XML element, add the nested **Party** XML element.</span></span>
    3. <span data-ttu-id="c4408-622">U prvku XML **Party** přidejte následující vnořené atributy XML:</span><span class="sxs-lookup"><span data-stu-id="c4408-622">For the **Party** XML element, add the following nested XML attributes:</span></span>

        - <span data-ttu-id="c4408-623">Jméno</span><span class="sxs-lookup"><span data-stu-id="c4408-623">Name</span></span>
        - <span data-ttu-id="c4408-624">AccountNum</span><span class="sxs-lookup"><span data-stu-id="c4408-624">AccountNum</span></span>

14. <span data-ttu-id="c4408-625">Navažte prvky formátu na poskytnuté zdroje dat následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="c4408-625">Bind the format elements to provided data sources in the following way:</span></span>

    - <span data-ttu-id="c4408-626">Vytvořte vazbu prvku formátu **Statement\\Party** na položku zdroje dat `model.Vendor`.</span><span class="sxs-lookup"><span data-stu-id="c4408-626">Bind the **Statement\\Party** format element to the `model.Vendor` data source item.</span></span>
    - <span data-ttu-id="c4408-627">Vytvořte vazbu prvku formátu **Statement\\Party\\Name** na pole zdroje dat **model.Vendor.Name**.</span><span class="sxs-lookup"><span data-stu-id="c4408-627">Bind the **Statement\\Party\\Name** format element to the **model.Vendor.Name** data source field.</span></span>
    - <span data-ttu-id="c4408-628">Vytvořte vazbu prvku formátu **Statement\\Party\\AccountNum** na pole zdroje dat **model.Vendor.AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="c4408-628">Bind the **Statement\\Party\\AccountNum** format element to the **model.Vendor.AccountNumber** data source field.</span></span>

15. <span data-ttu-id="c4408-629">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu formátu na stránce **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="c4408-629">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![Ověření komponenty formátu ER na stránce Návrhář formátů](./media/er-components-inspections-11c.png)

16. <span data-ttu-id="c4408-631">Všimněte si, že se zobrazí upozornění ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-631">Notice that a validation warning occurs.</span></span> <span data-ttu-id="c4408-632">Zpráva uvádí, že pole zdroje dat **model.Vendor.Name** není vázáno na žádný zdroj dat v mapování modelu, který je konfigurován pro použití ve formátu.</span><span class="sxs-lookup"><span data-stu-id="c4408-632">The message states that the **model.Vendor.Name** data source field isn't bound to any data source in the model mapping that is configured to be used by the format.</span></span> <span data-ttu-id="c4408-633">Proto prvek formátu **Statement\\Party\\Name** nemusí být za běhu vyplněn a může dojít k výjimce za běhu.</span><span class="sxs-lookup"><span data-stu-id="c4408-633">Therefore, the **Statement\\Party\\Name** format element might not be filled at runtime, and a runtime exception might occur.</span></span>

    ![Ověření komponenty formátu ER na stránce Návrhář formátů](./media/er-components-inspections-11d.png)

<span data-ttu-id="c4408-635">Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění a výběrem příkazu **Spustit** spustíte formát.</span><span class="sxs-lookup"><span data-stu-id="c4408-635">The following illustration shows the runtime error that occurs if you ignore the warning and select **Run** to run the format.</span></span>

![Spuštění upravitelného formátu na stránce Návrhář formátů](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a><span data-ttu-id="c4408-637">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-637">Automatic resolution</span></span>

<span data-ttu-id="c4408-638">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="c4408-638">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="c4408-639">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-639">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="c4408-640">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="c4408-640">Option 1</span></span>

<span data-ttu-id="c4408-641">Upravte konfigurované mapování modelu přidáním vazby pro pole zdroje dat **model.Vendor.Name**.</span><span class="sxs-lookup"><span data-stu-id="c4408-641">Modify the configured model mapping by adding a binding for the **model.Vendor.Name** data source field.</span></span>

#### <a name="option-2"></a><span data-ttu-id="c4408-642">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="c4408-642">Option 2</span></span>

<span data-ttu-id="c4408-643">Upravte konfigurovaný formát odebráním vazby pro prvek formátu **Statement\\Party\\Name**.</span><span class="sxs-lookup"><span data-stu-id="c4408-643">Modify the configured format by removing the binding for the **Statement\\Party\\Name** format element.</span></span>

## <a name="not-linked-template"></a><a id="i12"></a><span data-ttu-id="c4408-644">Nepropojená šablona</span><span class="sxs-lookup"><span data-stu-id="c4408-644">Not linked template</span></span>

<span data-ttu-id="c4408-645">Když [ručně](er-fillable-excel.md#manual-entry) nakonfigurujete komponentu formátu ER tak, aby pomocí šablony generovala odchozí dokument, musíte ručně přidat prvek **Excel\\File**, přidat požadovanou šablonu jako přílohu upravitelné komponenty, a vybrat tuto přílohu v přidaném prvku **Excel\\File**.</span><span class="sxs-lookup"><span data-stu-id="c4408-645">When you [manually](er-fillable-excel.md#manual-entry) configure an ER format component to use a template to generate an outbound document, you must manually add the **Excel\\File** element, add the required template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span> <span data-ttu-id="c4408-646">Tímto způsobem dáváte najevo, že přidaný prvek za běhu vyplní vybranou šablonu.</span><span class="sxs-lookup"><span data-stu-id="c4408-646">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="c4408-647">Při konfiguraci verze komponenty formátu ve [stavu](general-electronic-reporting.md#component-versioning) **Návrh** můžete do upravitelné komponenty přidat několik šablon a poté vybrat každou šablonu v prvku **Excel\\File**, aby spustila formát ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-647">When you configure a format component version in **Draft** [status](general-electronic-reporting.md#component-versioning), you might add several templates to the editable component and then select each template in the **Excel\\File** element to run the ER format.</span></span> <span data-ttu-id="c4408-648">Tímto způsobem můžete vidět, jak jsou různé šablony vyplněny za běhu.</span><span class="sxs-lookup"><span data-stu-id="c4408-648">In this way, you can see how different templates are filled at runtime.</span></span> <span data-ttu-id="c4408-649">Pokud máte šablony, které nejsou vybrány v žádném prvku **Excel\\File**, návrhář formátu ER vás upozorní, že tyto šablony budou odstraněny z upravitelné verze komponenty formátu ER, když se jeho stav změní z **Návrh** na **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="c4408-649">If you have templates that aren't selected in any **Excel\\File** elements, the ER format designer warns you that those templates will be deleted from the editable ER format component version when its status is changed from **Draft** to **Completed**.</span></span>

<span data-ttu-id="c4408-650">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="c4408-650">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="c4408-651">Začněte konfigurací komponenty formátu ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-651">Start to configure the ER format component.</span></span>
2. <span data-ttu-id="c4408-652">Ve stromu struktury formátu přidejte prvek **Excel\\File**.</span><span class="sxs-lookup"><span data-stu-id="c4408-652">In the format structure tree, add the **Excel\\File** element.</span></span>
3. <span data-ttu-id="c4408-653">U prvku **Excel\\File**, který jste právě přidali, přidejte soubor sešitu aplikace Excel **A.xlsx** jako přílohu.</span><span class="sxs-lookup"><span data-stu-id="c4408-653">For the **Excel\\File** element that you just added, add an Excel workbook file, **A.xlsx**, as an attachment.</span></span> <span data-ttu-id="c4408-654">Použijte typ dokumentu, který je konfigurován v [parametrech ER](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) k určení úložiště šablon formátu ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-654">Use the document type that is configured in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) to specify the storage of ER format templates.</span></span>
4. <span data-ttu-id="c4408-655">U prvku **Excel\\File**, který jste právě přidali, přidejte další soubor sešitu aplikace Excel **B.xlsx** jako přílohu.</span><span class="sxs-lookup"><span data-stu-id="c4408-655">For the **Excel\\File** element, add another Excel workbook file, **B.xlsx**, as an attachment.</span></span> <span data-ttu-id="c4408-656">Použijte stejný typ dokumentu jako u souboru sešitu A.</span><span class="sxs-lookup"><span data-stu-id="c4408-656">Use the same document type that is used for workbook file A.</span></span>
5. <span data-ttu-id="c4408-657">V prvku **Excel\\File** vyberte soubor sešitu A.</span><span class="sxs-lookup"><span data-stu-id="c4408-657">In the **Excel\\File** element, select workbook file A.</span></span>
6. <span data-ttu-id="c4408-658">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu formátu na stránce **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="c4408-658">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![Ověření komponenty upravitelného formátu souboru sešitu na stránce Návrhář formátů](./media/er-components-inspections-12a.gif)

7. <span data-ttu-id="c4408-660">Všimněte si, že se zobrazí upozornění ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-660">Notice that a validation warning occurs.</span></span> <span data-ttu-id="c4408-661">Zpráva uvádí, že soubor sešitu B.xlsx není propojen se žádnými komponentami a že bude odstraněn po změně stavu verze konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c4408-661">The message states that workbook file B.xlsx isn't linked to any components, and that it will be removed after the status of the configuration version is changed.</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="c4408-662">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-662">Automatic resolution</span></span>

<span data-ttu-id="c4408-663">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="c4408-663">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="c4408-664">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-664">Manual resolution</span></span>

<span data-ttu-id="c4408-665">Upravte konfigurovaný formát odebráním všech šablon, které nejsou propojeny s žádným prvkem **Excel\\File**.</span><span class="sxs-lookup"><span data-stu-id="c4408-665">Modify the configured format by removing all templates that aren't linked to any **Excel\\File** element.</span></span>

## <a name="not-synced-format"></a><a id="i13"></a><span data-ttu-id="c4408-666">Nesynchronizovaný formát</span><span class="sxs-lookup"><span data-stu-id="c4408-666">Not synced format</span></span>

<span data-ttu-id="c4408-667">Když [nakonfigurujete](er-fillable-excel.md) komponentu formátu ER tak, aby pomocí šablony Excelu generovala odchozí dokument, můžete ručně přidat prvek **Excel\\File**, přidat požadovanou šablonu jako přílohu upravitelné komponenty, a vybrat tuto přílohu v přidaném prvku **Excel\\File**.</span><span class="sxs-lookup"><span data-stu-id="c4408-667">When you [configure](er-fillable-excel.md) an ER format component to use an Excel template to generate an outbound document, you can manually add the **Excel\\File** element, add the required template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span> <span data-ttu-id="c4408-668">Tímto způsobem dáváte najevo, že přidaný prvek za běhu vyplní vybranou šablonu.</span><span class="sxs-lookup"><span data-stu-id="c4408-668">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="c4408-669">Protože přidaná šablona Excelu byla navržena externě, může upravitelný formát ER obsahovat názvy aplikace Excel, které v přidané šabloně chybí.</span><span class="sxs-lookup"><span data-stu-id="c4408-669">Because the added Excel template has been externally designed, the editable ER format might contain Excel names that are missing from the added template.</span></span> <span data-ttu-id="c4408-670">Návrhář formátu ER vás upozorní na jakékoli nesrovnalosti mezi vlastnostmi prvků formátu ER odkazující na názvy, které nejsou zahrnuty v přidané šabloně Excelu.</span><span class="sxs-lookup"><span data-stu-id="c4408-670">The ER format designer warns you about any inconsistencies between the properties of the ER format elements that refer to names that aren't included in the added Excel template.</span></span>

<span data-ttu-id="c4408-671">Následující kroky ukazují, jak může k tomuto problému dojít.</span><span class="sxs-lookup"><span data-stu-id="c4408-671">The following steps show how this issue might occur.</span></span>

1. <span data-ttu-id="c4408-672">Začněte konfigurací komponenty formátu ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-672">Start to configure the ER format component.</span></span>
2. <span data-ttu-id="c4408-673">Ve stromu struktury formátu přidejte prvek **Excel\\File** s názvem **Report**.</span><span class="sxs-lookup"><span data-stu-id="c4408-673">In the format structure tree, add the **Excel\\File** element **Report**.</span></span>
3. <span data-ttu-id="c4408-674">U prvku **Excel\\File**, který jste právě přidali, přidejte soubor sešitu aplikace Excel **A.xlsx** jako přílohu.</span><span class="sxs-lookup"><span data-stu-id="c4408-674">For the **Excel\\File** element that you just added, add an Excel workbook file, **A.xlsx**, as an attachment.</span></span> <span data-ttu-id="c4408-675">Použijte typ dokumentu, který je konfigurován v [parametrech ER](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) k určení úložiště šablon formátu ER.</span><span class="sxs-lookup"><span data-stu-id="c4408-675">Use the document type that is configured in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) to specify the storage of ER format templates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="c4408-676">Ujistěte se, že přidaný sešit Excelu neobsahuje název **ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="c4408-676">Make sure that the added Excel workbook doesn't contain the name **ReportTitle**.</span></span>

4. <span data-ttu-id="c4408-677">Přidejte prvek **Excel\\Cell** s názvem **Title** jako vnořený prvek prvku **Report**.</span><span class="sxs-lookup"><span data-stu-id="c4408-677">Add the **Excel\\Cell** element **Title** as a nested element of the **Report** element.</span></span> <span data-ttu-id="c4408-678">Do pole **Oblast Excelu** zadejte **ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="c4408-678">In the **Excel range** field, enter **ReportTitle**.</span></span>
5. <span data-ttu-id="c4408-679">Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu formátu na stránce **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="c4408-679">Select **Validate** to inspect the editable format component on the **Format designer** page.</span></span>

    ![Ověření vnořených prvků a polí na stránce Návrhář formátu](./media/er-components-inspections-13a.png)

6. <span data-ttu-id="c4408-681">Všimněte si, že se zobrazí upozornění ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-681">Notice that a validation warning occurs.</span></span> <span data-ttu-id="c4408-682">Zpráva uvádí, že název **ReportTitle** neexistuje v listu **Sheet1** šablony aplikace Excel, kterou používáte.</span><span class="sxs-lookup"><span data-stu-id="c4408-682">The message states that the name **ReportTitle** doesn't exist on sheet **Sheet1** of the Excel template that you're using.</span></span>

    ![Upozornění ověření na fakt, že název ReportTitle neexistuje na listu Sheet1 šablony aplikace Excel](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a><span data-ttu-id="c4408-684">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-684">Automatic resolution</span></span>

<span data-ttu-id="c4408-685">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="c4408-685">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="c4408-686">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-686">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="c4408-687">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="c4408-687">Option 1</span></span>

<span data-ttu-id="c4408-688">Upravte konfigurovaný formát odebráním všech prvků odkazujících na názvy aplikace Excel, které v šabloně chybí.</span><span class="sxs-lookup"><span data-stu-id="c4408-688">Modify the configured format by removing all elements that refer to Excel names that are missing from the template.</span></span>

#### <a name="option-2"></a><span data-ttu-id="c4408-689">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="c4408-689">Option 2</span></span>

<span data-ttu-id="c4408-690">[Aktualizujte](er-fillable-excel.md#template-import) upravitelný formát ER importem šablony aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="c4408-690">[Update](er-fillable-excel.md#template-import) the editable ER format by importing an Excel template.</span></span> <span data-ttu-id="c4408-691">Struktura upravitelného formátu ER bude [synchronizována](modify-electronic-reporting-format-reapply-excel-template.md) se strukturou importované šablony Excelu.</span><span class="sxs-lookup"><span data-stu-id="c4408-691">The structure of the editable ER format will be [synced](modify-electronic-reporting-format-reapply-excel-template.md) with the structure of the imported Excel template.</span></span>

### <a name="additional-consideration"></a><span data-ttu-id="c4408-692">Další faktor ke zvážení</span><span class="sxs-lookup"><span data-stu-id="c4408-692">Additional consideration</span></span>

<span data-ttu-id="c4408-693">Chcete-li se naučit synchronizovat strukturu formátu se šablonou ER v editoru šablon [Správy obchodních dokumentů](er-business-document-management.md), přečtěte si část [Aktualizace struktury šablony obchodního dokumentu](er-bdm-update-structure.md).</span><span class="sxs-lookup"><span data-stu-id="c4408-693">To learn how the format structure can be synced with an ER template in the template editor of [Business document management](er-business-document-management.md), see [Update the structure of a business document template](er-bdm-update-structure.md).</span></span>

## <a name="not-synced-with-a-word-template-format"></a><a id="i14"></a><span data-ttu-id="c4408-694">Není synchronizováno s formátem šablony Word</span><span class="sxs-lookup"><span data-stu-id="c4408-694">Not synced with a Word template format</span></span>

<span data-ttu-id="c4408-695">Když [nakonfigurujete](er-fillable-excel.md) komponentu formátu ER tak, aby pomocí šablony Wordu generovala odchozí dokument, můžete ručně přidat prvek **Excel\\File**, přidat požadovanou šablonu Wordu jako přílohu upravitelné komponenty, a vybrat tuto přílohu v přidaném prvku **Excel\\File**.</span><span class="sxs-lookup"><span data-stu-id="c4408-695">When you [configure](er-fillable-excel.md) an ER format component to use a Word template to generate an outbound document, you can manually add the **Excel\\File** element, add the required Word template as an attachment of the editable component, and select that attachment in the added **Excel\\File** element.</span></span>

> [!NOTE]
> <span data-ttu-id="c4408-696">Když je připojen dokument Word, návrhář formátu ER prezentuje upravitelný prvek jako **Word\\Soubor**.</span><span class="sxs-lookup"><span data-stu-id="c4408-696">When the Word document is attached, the ER format designer presents the editable element as **Word\\File**.</span></span>

<span data-ttu-id="c4408-697">Tímto způsobem dáváte najevo, že přidaný prvek za běhu vyplní vybranou šablonu.</span><span class="sxs-lookup"><span data-stu-id="c4408-697">In this way, you indicate that the added element will fill the selected template at runtime.</span></span> <span data-ttu-id="c4408-698">Protože přidaná šablona Wordu byla navržena externě, může upravitelný formát ER obsahovat odkazy na ovládací prvky obsahu Wordu, které v přidané šabloně chybí.</span><span class="sxs-lookup"><span data-stu-id="c4408-698">Because the added Word template has been externally designed, the editable ER format might contain references to Word content controls that are missing from the added template.</span></span> <span data-ttu-id="c4408-699">Návrhář formátu ER vás upozorní na jakékoli nesrovnalosti mezi vlastnostmi prvků formátu ER odkazující na ovládací prvky obsahu, které nejsou zahrnuty v přidané šabloně Wordu.</span><span class="sxs-lookup"><span data-stu-id="c4408-699">The ER format designer warns you about any inconsistencies between the properties of the ER format elements that refer to content controls that aren't included in the added Word template.</span></span>

<span data-ttu-id="c4408-700">Příklad, který ukazuje, jak může k tomuto problému dojít, viz [Konfigurace upravitelného formát tak, aby potlačil část shrnutí](er-design-configuration-word-suppress-controls.md#configure-to-suppress-control).</span><span class="sxs-lookup"><span data-stu-id="c4408-700">For an example that shows how this issue might occur, see [Configure the editable format to suppress the summary section](er-design-configuration-word-suppress-controls.md#configure-to-suppress-control).</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="c4408-701">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-701">Automatic resolution</span></span>

<span data-ttu-id="c4408-702">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="c4408-702">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="c4408-703">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-703">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="c4408-704">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="c4408-704">Option 1</span></span>

<span data-ttu-id="c4408-705">Upravte nakonfigurovaný formát odstraněním vzorce **Odstraněno** z prvku formátu, který je uveden ve upozornění na ověření.</span><span class="sxs-lookup"><span data-stu-id="c4408-705">Modify the configured format by deleting the **Removed** formula from the format element that is mentioned in the validation warning.</span></span>

#### <a name="option-2"></a><span data-ttu-id="c4408-706">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="c4408-706">Option 2</span></span>

<span data-ttu-id="c4408-707">Upravte použití šablony Word pomocí [přidání](er-design-configuration-word-suppress-controls.md#tag-control) požadované značky k příslušnému ovládacímu prvku obsahu Word.</span><span class="sxs-lookup"><span data-stu-id="c4408-707">Modify the using Word template by [adding](er-design-configuration-word-suppress-controls.md#tag-control) the required tag to the relevant Word content control.</span></span>

## <a name="no-default-mapping"></a><a id="i15"></a><span data-ttu-id="c4408-708">Žádné výchozí mapování</span><span class="sxs-lookup"><span data-stu-id="c4408-708">No default mapping</span></span>

<span data-ttu-id="c4408-709">Když je provedena kontrola [Chybí vazba](#i11), jsou zkontrolovány vazby kontrolovaného formátu proti vazbám příslušné komponenty mapování modelu.</span><span class="sxs-lookup"><span data-stu-id="c4408-709">When the [Missing binding](#i11) inspection is done, the inspected format bindings are evaluated against the bindings of the relevant model mapping component.</span></span> <span data-ttu-id="c4408-710">Protože můžete importovat [několik](./tasks/er-manage-model-mapping-configurations-july-2017.md) konfigurací mapování modelu ER na vaši instanci Finance a každá konfigurace může obsahovat příslušnou komponentu mapování modelu, musí být vybrána jedna konfigurace jako výchozí konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c4408-710">Because you can import [several](./tasks/er-manage-model-mapping-configurations-july-2017.md) ER model mapping configurations to your Finance instance, and each configuration might contain the applicable model mapping component, one configuration must be selected as the default configuration.</span></span> <span data-ttu-id="c4408-711">Jinak při pokusu o spuštění, úpravy nebo ověření kontrolovaného formátu ER dojde k výjimce a zobrazí se následující zpráva: „Existuje více než jedno mapování modelu pro datový model \<model name (root descriptor)\> v konfiguracích \<configuration names separated by comma\>.</span><span class="sxs-lookup"><span data-stu-id="c4408-711">Otherwise, when you try to run, edit, or validate the inspected ER format, an exception will occur, and you will receive the following message: "More than one model mapping exists for the \<model name (root descriptor)\> data model in the configurations \<configuration names separated by comma\>.</span></span> <span data-ttu-id="c4408-712">Nastavte jednu z konfigurací jako výchozí.“</span><span class="sxs-lookup"><span data-stu-id="c4408-712">Set one of the configurations as default."</span></span>

<span data-ttu-id="c4408-713">Příklad, který ukazuje, jak může k tomuto problému dojít a jak ho lze opravit, najdete v článku [Správa několika odvozených mapování pro jeden kořen modelu](er-multiple-model-mappings.md).</span><span class="sxs-lookup"><span data-stu-id="c4408-713">For an example that shows how this issue might occur and how it can be fixed, see [Manage several derived mappings for a single model root](er-multiple-model-mappings.md).</span></span>

## <a name="inconsistent-setting-of-header-or-footer-components"></a><a id="i16"></a><span data-ttu-id="c4408-714">Nekonzistentní nastavení komponent záhlaví nebo zápatí</span><span class="sxs-lookup"><span data-stu-id="c4408-714">Inconsistent setting of Header or Footer components</span></span>

<span data-ttu-id="c4408-715">Když [nakonfigurujete](er-fillable-excel.md) komponentu formátu ER na použití šablony aplikace Excel ke generování odchozího dokumentu, můžete přidat komponentu **Excel\\Záhlaví** k vyplnění záhlaví v horní části listu v sešitu aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="c4408-715">When you [configure](er-fillable-excel.md) an ER format component to use an Excel template to generate an outbound document, you can add the **Excel\\Header** component to fill in headers at the top of a worksheet in an Excel workbook.</span></span> <span data-ttu-id="c4408-716">Můžete také přidat komponentu **Excel\\Zápatí** k vyplnění zápatí ve spodní části listu.</span><span class="sxs-lookup"><span data-stu-id="c4408-716">You can also add the **Excel\\Footer** component to fill in footers at the bottom of a worksheet.</span></span> <span data-ttu-id="c4408-717">Pro každý komponent **Excel\\Záhlaví** nebo **Excel\\Zápatí**, který přidáte, musíte nastavit vlastnost **Vzhled záhlaví/zápatí** k určení stránek, pro které je komponenta spuštěna.</span><span class="sxs-lookup"><span data-stu-id="c4408-717">For every **Excel\\Header** or **Excel\\Footer** component that you add, you must set the **Header/footer appearance** property to specify the pages that the component is run for.</span></span> <span data-ttu-id="c4408-718">Protože jich můžete nakonfigurovat několik komponent **Excel\\Záhlaví** nebo **Excel\\Zápatí** pro jeden **List** a můžete vygenerovat různá záhlaví nebo zápatí pro různé typy stránek v listu aplikace Excel, musíte nakonfigurovat jednu komponentu **Excel\\Záhlaví** nebo **Excel\\Zápatí** komponenta pro konkrétní vlastnost **Vzhled záhlaví/zápatí**.</span><span class="sxs-lookup"><span data-stu-id="c4408-718">Because you can configure several **Excel\\Header** or **Excel\\Footer** components for a single **Sheet** component, and you can generate different headers or footers for different type of pages in an Excel worksheet, you must configure a single **Excel\\Header** or **Excel\\Footer** component for a specific value of the **Header/footer appearance** property.</span></span> <span data-ttu-id="c4408-719">Pokud je nakonfigurován více než jeden komponent **Excel\\Záhlaví** nebo **Excel\\Zápatí** pro konkrétní vlastnost **Vzhled záhlaví/zápatí**, dojde k chybě ověření a zobrazí se následující chybová zpráva: „Záhlaví/zápatí (&lt;typ komponenty: Záhlaví nebo zápatí&gt;) jsou nekonzistentní.“</span><span class="sxs-lookup"><span data-stu-id="c4408-719">If more than one **Excel\\Header** or **Excel\\Footer** component is configured for a specific value of the **Header/footer appearance** property, a validation error occurs, and you receive the following error message: "Headers/footers (&lt;component type: Header or Footer&gt;) are inconsistent."</span></span>

### <a name="automatic-resolution"></a><span data-ttu-id="c4408-720">Automatické řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-720">Automatic resolution</span></span>

<span data-ttu-id="c4408-721">Není k dispozici žádná možnost automatického řešení tohoto problému.</span><span class="sxs-lookup"><span data-stu-id="c4408-721">No option to automatically fix this issue is available.</span></span>

### <a name="manual-resolution"></a><span data-ttu-id="c4408-722">Ruční řešení</span><span class="sxs-lookup"><span data-stu-id="c4408-722">Manual resolution</span></span>

#### <a name="option-1"></a><span data-ttu-id="c4408-723">Možnost 1</span><span class="sxs-lookup"><span data-stu-id="c4408-723">Option 1</span></span>

<span data-ttu-id="c4408-724">Upravte nakonfigurovaný formát odstraněním jednoho z nekonzistentních komponent **Excel\\Záhlaví** nebo **Excel\\Zápatí**.</span><span class="sxs-lookup"><span data-stu-id="c4408-724">Modify the configured format by deleting one of the inconsistent **Excel\\Header** or **Excel\\Footer** components.</span></span>

#### <a name="option-2"></a><span data-ttu-id="c4408-725">Možnost 2</span><span class="sxs-lookup"><span data-stu-id="c4408-725">Option 2</span></span>

<span data-ttu-id="c4408-726">Upravte vlastnost **Vzhled záhlaví/zápatí** pro jeden z nekonzistentních komponent **Excel\\Záhlaví** nebo **Excel\\Zápatí**.</span><span class="sxs-lookup"><span data-stu-id="c4408-726">Modify the value of the **Header/footer appearance** property for one of the inconsistent **Excel\\Header** or **Excel\\Footer** components.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c4408-727">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="c4408-727">Additional resources</span></span>

[<span data-ttu-id="c4408-728">Funkce elektronického výkaznictví ALLITEMS</span><span class="sxs-lookup"><span data-stu-id="c4408-728">ALLITEMS ER function</span></span>](er-functions-list-allitems.md)

[<span data-ttu-id="c4408-729">Funkce elektronického výkaznictví ALLITEMSQUERY</span><span class="sxs-lookup"><span data-stu-id="c4408-729">ALLITEMSQUERY ER function</span></span>](er-functions-list-allitemsquery.md)

[<span data-ttu-id="c4408-730">Funkce el. výkaznictví INT64VALUE</span><span class="sxs-lookup"><span data-stu-id="c4408-730">INT64VALUE ER function</span></span>](er-functions-conversion-int64value.md)

[<span data-ttu-id="c4408-731">Funkce INTVALUE ER</span><span class="sxs-lookup"><span data-stu-id="c4408-731">INTVALUE ER function</span></span>](er-functions-conversion-intvalue.md)

[<span data-ttu-id="c4408-732">Funkce elektronického výkaznictví FILTER</span><span class="sxs-lookup"><span data-stu-id="c4408-732">FILTER ER function</span></span>](er-functions-list-filter.md)

[<span data-ttu-id="c4408-733">Funkce elektronického výkaznictví WHERE</span><span class="sxs-lookup"><span data-stu-id="c4408-733">WHERE ER function</span></span>](er-functions-list-where.md)

[<span data-ttu-id="c4408-734">Použití zdrojů dat JOIN v mapování modelu ER k získání dat z více aplikačních tabulek</span><span class="sxs-lookup"><span data-stu-id="c4408-734">Use JOIN data sources to get data from multiple application tables in ER model mappings</span></span>](er-join-data-sources.md)

[<span data-ttu-id="c4408-735">Sledování provedení formátů elektronického výkaznictví pro při řešení problémů s výkonem</span><span class="sxs-lookup"><span data-stu-id="c4408-735">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="c4408-736">Přehled správy obchodních dokumentů</span><span class="sxs-lookup"><span data-stu-id="c4408-736">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="c4408-737">Potlačit ovládací prvky obsahu Word v generovaných sestavách</span><span class="sxs-lookup"><span data-stu-id="c4408-737">Suppress Word content controls in generated reports</span></span>](er-design-configuration-word-suppress-controls.md)

[<span data-ttu-id="c4408-738">Správa několika odvozených mapování pro jeden kořen modelu</span><span class="sxs-lookup"><span data-stu-id="c4408-738">Manage several derived mappings for a single model root</span></span>](er-multiple-model-mappings.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
