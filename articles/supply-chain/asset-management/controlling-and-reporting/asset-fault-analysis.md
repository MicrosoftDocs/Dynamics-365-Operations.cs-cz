---
title: Analýza závady majetku
description: V tomto tématu je vysvětlena analýza závady majetku v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c9330cc7b3a8839d94c8945418548033254786b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918434"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="0fde8-103">Analýza závady majetku</span><span class="sxs-lookup"><span data-stu-id="0fde8-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="0fde8-104">V modulu Správa majetku můžete analyzovat registrace závad majetku s cílem získat přehled o celkovém počtu závad zaregistrovaných během určitého období.</span><span class="sxs-lookup"><span data-stu-id="0fde8-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="0fde8-105">Registrace závad lze analyzovat z různých perspektiv, například se zaměřením na majetek, typy majetku, funkční místa, příznaky závad nebo typy závad.</span><span class="sxs-lookup"><span data-stu-id="0fde8-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="0fde8-106">Klikněte na **Správa majetku** > **Dotazy** > **Závada majetku** > **Analýza závad majetku**.</span><span class="sxs-lookup"><span data-stu-id="0fde8-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="0fde8-107">V dialogovém okně **Výpočet analýzy závad majetku** můžete pomocí pole **Úroveň** označit, jak detailní mají být řádky závad majetku, pokud jde o funkční místa.</span><span class="sxs-lookup"><span data-stu-id="0fde8-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> <span data-ttu-id="0fde8-108">Pokud například do pole zadáte číslo „1“ a máte strukturu funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny řádky závad majetku pro funkční místo, a proto lze hodiny na řádku navýšit z funkčních míst na nižší úrovni.</span><span class="sxs-lookup"><span data-stu-id="0fde8-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="0fde8-109">Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky závad majetku na všech úrovních funkčních míst, ke kterým se vztahují.</span><span class="sxs-lookup"><span data-stu-id="0fde8-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="0fde8-110">Chcete-li hledání omezit, můžete vybrat konkrétní majetek, data závad, příčiny závad a nápravy závad na záložce s náhledem **Záznamy k zahrnutí**.</span><span class="sxs-lookup"><span data-stu-id="0fde8-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="0fde8-111">Výpočet zahájíte klepnutím na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="0fde8-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="0fde8-112">Na kartě **Analýza závad majetku** klikněte na jedno nebo více tlačítek ve skupinách podokna akcí **Seskupit podle...** pro zobrazení úrovně podrobností, které chcete zobrazit.</span><span class="sxs-lookup"><span data-stu-id="0fde8-112">On the **Asset fault analysis** tab, click one or more buttons in the **Group by...** action pane groups to display the detail level you want to see.</span></span> <span data-ttu-id="0fde8-113">Aktivovaná tlačítka jsou zvýrazněna.</span><span class="sxs-lookup"><span data-stu-id="0fde8-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="0fde8-114">Kliknutím na tlačítko jej aktivujte nebo deaktivujte.</span><span class="sxs-lookup"><span data-stu-id="0fde8-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="0fde8-115">Kliknutím na **Aktualizovat výpočty** zobrazíte své výběry na obrazovce.</span><span class="sxs-lookup"><span data-stu-id="0fde8-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="0fde8-116">Při každém aktivaci nebo deaktivaci tlačítek ve skupině podoken akcí **Seskupit podle...** nezapomeňte po změně výběrů kliknout na tlačítko **Aktualizovat výpočty**.</span><span class="sxs-lookup"><span data-stu-id="0fde8-116">Every time you activate or deactivate buttons in the **Group by...** action pane groups, remember to click the **Update calculations** button after you changed the selections.</span></span> <span data-ttu-id="0fde8-117">To je nutné, protože při přepočtu pravděpodobnosti závady se zpracovává velké množství dat.</span><span class="sxs-lookup"><span data-stu-id="0fde8-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

<span data-ttu-id="0fde8-118">Existuje mnoho způsobů analýzy registrací závad.</span><span class="sxs-lookup"><span data-stu-id="0fde8-118">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="0fde8-119">Níže vidíte příklady na pěti snímcích obrazovek, v nichž různé výběry dat poskytují různé informace.</span><span class="sxs-lookup"><span data-stu-id="0fde8-119">Below you see examples in five screenshots of how different data selections provide different pieces of information.</span></span> <span data-ttu-id="0fde8-120">Zjistíte, jakým způsobem různé výběry poskytují lepší přehled a podrobnosti při analýze registrací závad majetku.</span><span class="sxs-lookup"><span data-stu-id="0fde8-120">You will see how different selections provide more insight and detail when analyzing asset fault registrations.</span></span>

<span data-ttu-id="0fde8-121">Na níže uvedeném snímku obrazovky je vybráno pouze tlačítko **Příznak**.</span><span class="sxs-lookup"><span data-stu-id="0fde8-121">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="0fde8-122">Registrace závad byly provedeny se třemi příznaky poruch: únik vzduchu, vyhořelá pojistka a ucpané zařízení.</span><span class="sxs-lookup"><span data-stu-id="0fde8-122">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="0fde8-123">Ve sloupci **Pravděpodobnost %** se všechny procentuální hodnoty sčítají až do 100%.</span><span class="sxs-lookup"><span data-stu-id="0fde8-123">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="0fde8-124">Pravděpodobnost je založena na všech registracích **příznaku** v této analýze závad.</span><span class="sxs-lookup"><span data-stu-id="0fde8-124">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![Obrázek č. 1](media/06-controlling-and-reporting.png)


<span data-ttu-id="0fde8-126">Na níže uvedeném snímku obrazovky se přidají **Rok** a **Měsíc**, aby se zobrazil způsob zobrazení registrace závad během vybraného období.</span><span class="sxs-lookup"><span data-stu-id="0fde8-126">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="0fde8-127">Příznaky závad jsou nyní zobrazeny jako registrace za rok/měsíc.</span><span class="sxs-lookup"><span data-stu-id="0fde8-127">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="0fde8-128">Pokud do sloupce **Pravděpodobnost %** přidáte všechna procenta pro každý měsíc, přidá se až 100%.</span><span class="sxs-lookup"><span data-stu-id="0fde8-128">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="0fde8-129">Pravděpodobnost je založena na registracích **příznaku** v této analýze závad.</span><span class="sxs-lookup"><span data-stu-id="0fde8-129">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="0fde8-130">Máte-li v majetku velký počet řádků, ale velké procento vyčnívá na řádku, bude to indikací příznaku závady, který je třeba blíže prozkoumat a nalézt způsob, jak omezit počet registrací pro tento příznak závady.</span><span class="sxs-lookup"><span data-stu-id="0fde8-130">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Obrázek č. 2](media/07-controlling-and-reporting.png)


- <span data-ttu-id="0fde8-132">Kombinace majetku a typu majetku se používá jako základ pro výpočty zobrazené na třech snímcích obrazovek, což zvýší úroveň podrobností.</span><span class="sxs-lookup"><span data-stu-id="0fde8-132">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  
- <span data-ttu-id="0fde8-133">Obecně tlačítka ve skupině podoken akcí **Seskupit podle data**, **Seskupit podle majetku**, **Seskupit podle funkčního místa**, stejně jako tlačítko **Závada** (ID závady) obsahují období nebo relace majetku.</span><span class="sxs-lookup"><span data-stu-id="0fde8-133">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** action pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="0fde8-134">Tlačítka **Příznak**, **Oblast**, **Typ**, **Příčina** a **Náprava** jsou kategorizace používané ve správě závad pro analýzu registrací závad majetku a poukázání na problémové oblasti.</span><span class="sxs-lookup"><span data-stu-id="0fde8-134">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="0fde8-135">Na níže uvedeném snímku obrazovky byl přidán **Majetek** a **Typ majetku**, kde jsou uvedeny další podrobnosti týkající se registrací závad.</span><span class="sxs-lookup"><span data-stu-id="0fde8-135">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="0fde8-136">Příznaky závad jsou nyní rozděleny do kombinací **Majetek** / **Typ majetku** / **Příznak**.</span><span class="sxs-lookup"><span data-stu-id="0fde8-136">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="0fde8-137">Pokud do sloupce **Pravděpodobnost %** přidáte všechna procenta pro kombinaci **Majetek** / **Typ majetku** / **Příznak**, každá dosáhne 100%.</span><span class="sxs-lookup"><span data-stu-id="0fde8-137">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="0fde8-138">Pravděpodobnost je založena na registracích **příznaku** v této analýze závad.</span><span class="sxs-lookup"><span data-stu-id="0fde8-138">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="0fde8-139">Máte-li v majetku velký počet řádků, ale velké procento vyčnívá na řádku, bude to indikací příznaku závady, který je třeba blíže prozkoumat a nalézt způsob, jak omezit počet registrací pro tento příznak závady.</span><span class="sxs-lookup"><span data-stu-id="0fde8-139">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Obrázek č. 3](media/08-controlling-and-reporting.png)


<span data-ttu-id="0fde8-141">Na níže uvedeném snímku obrazovky byla přidána **Oblast** k možnostem **Příznak**, **Majatek** a **Typ majetku**, kde jsou uvedeny další podrobnosti týkající se registrací závad.</span><span class="sxs-lookup"><span data-stu-id="0fde8-141">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="0fde8-142">Pokud do sloupce **Pravděpodobnost %** přidáte všechna procenta pro kombinaci **Majetek** / **Typ majetku** / **Příznak** na majetku, každá dosáhne 100%.</span><span class="sxs-lookup"><span data-stu-id="0fde8-142">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="0fde8-143">Pravděpodobnost je založena na kombinaci **příznaku** a **oblasti** v této analýze závad.</span><span class="sxs-lookup"><span data-stu-id="0fde8-143">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="0fde8-144">Máte-li v majetku velký počet řádků, ale velké procento vyčnívá na řádku, bude to indikací oblasti závady, kterou je třeba blíže prozkoumat a nalézt způsob, jak omezit počet registrací pro tuto oblast závady.</span><span class="sxs-lookup"><span data-stu-id="0fde8-144">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![Obrázek č. 4](media/09-controlling-and-reporting.png)


<span data-ttu-id="0fde8-146">Na snímku obrazovky níže byl přidán **Typ** a v tomto příkladu je zobrazen nejpřesnější výpočet.</span><span class="sxs-lookup"><span data-stu-id="0fde8-146">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="0fde8-147">Pokud do sloupce **Pravděpodobnost %** přidáte všechna procenta pro kombinaci **Majetek** / **Typ majetku** / **Příznak** na majetku, každá dosáhne 100%.</span><span class="sxs-lookup"><span data-stu-id="0fde8-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="0fde8-148">Pravděpodobnost je založena na kombinaci **příznaku**, **oblasti** a **typu** v této analýze závad.</span><span class="sxs-lookup"><span data-stu-id="0fde8-148">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="0fde8-149">Máte-li v majetku velký počet řádků, ale velké procento vyčnívá na řádku, bude to indikací typu závady, který je třeba blíže prozkoumat a nalézt způsob, jak omezit počet registrací pro tenti typ závady.</span><span class="sxs-lookup"><span data-stu-id="0fde8-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![Obrázek č. 5](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="0fde8-151">Pro získání přehledu všech registrací závad vytvořených v pracovních příkazech a požadavcích na údržbu klikněte na **Správa majetku** > **Dotazy** > **Závada majetku** > **Závady majetku**.</span><span class="sxs-lookup"><span data-stu-id="0fde8-151">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="0fde8-152">Na stránce **Závady majetku** vyberte registraci závad majetku a rozbalte podokno **Související informace**, abyste viděli informace týkající se souvisejícího pracovního příkazu nebo požadavku na údržbu.</span><span class="sxs-lookup"><span data-stu-id="0fde8-152">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>

