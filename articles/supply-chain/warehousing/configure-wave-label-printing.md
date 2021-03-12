---
title: Nastavte a použijte tisk popisků vlny
description: Toto téma popisuje tisk popisků vlny a vysvětluje, jak je nastavit.
author: GarmMSFT
manager: PJacobse
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 862987b8ccdc4272bdd404e78391ad447bc290b3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996344"
---
# <a name="set-up-and-use-wave-label-printing"></a><span data-ttu-id="ccd8e-103">Nastavte a použijte tisk popisků vlny</span><span class="sxs-lookup"><span data-stu-id="ccd8e-103">Set up and use wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ccd8e-104">Tisk popisků vlny nabízí alternativní přístup k tisku štítků zavedením nové metody vlnových kroků, která umožňuje vytvářet a tisknout štítky přímo ze šablony vln během provádění vln.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="ccd8e-105">Proto budou štítky již k dispozici dříve, než pracovníci spustí pracovní příkaz na mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="ccd8e-106">Pracovníci pak mohou při sběru namísto po sběru připojit požadované štítky.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="ccd8e-107">Tisk popisků vlny používá k vytvoření rozložení štítků programovací jazyk Zebra (ZPL).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="ccd8e-108">Rozložení štítků je rozděleno do tří částí (záhlaví, tělo a zápatí), aby bylo možné vytvořit štítky, které mají opakující se strukturu.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="ccd8e-109">Šablony vlnových štítků říkají systému, které rozvržení štítků se má použít.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="ccd8e-110">Uživatelé mohou určit, která tiskárna bude použita.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-110">Users can specify which printer is used.</span></span> <span data-ttu-id="ccd8e-111">Mohou také tisknout štítky na více tiskáren současně, jak vyžadují.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="ccd8e-112">Stránka **Historie popisků vlny** zobrazuje záznam všech štítků, které byly vytvořeny pomocí tohoto nastavení.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="ccd8e-113">Štítky můžete tisknout a třídit na základě záhlaví práce, můžete tisknout štítky přestávky na pracovní hlavičku a můžete tisknout štítky obsahu kontejneru, štítky velkých písmen a další podobné štítky.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="ccd8e-114">Tato funkce nenahrazuje stávající funkce tisku štítků, která je založena na směrování dokumentů.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="ccd8e-115">Tisk popisků vlny nabízí následující vylepšení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="ccd8e-116">Štítky tiskněte podle počtu kartonů na jednu pracovní linku bez použití kontejnerizace.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="ccd8e-117">(„Karton“ je jednotka, která je určena na řádcích skupin sekvencí jednotek.)</span><span class="sxs-lookup"><span data-stu-id="ccd8e-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="ccd8e-118">Vytiskněte několik různých štítků (například štítky kartonů a palet).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="ccd8e-119">Zahrňte výčet štítků (například 1/124, 2/124, ... 124/124) a definujte rozsah výčtu (například pracovní linie, nákladová linie nebo zásilka).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="ccd8e-120">Před vygenerováním přepravního dokladu vytvořte a vytiskněte ID přepravního dokladu na štítky.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="ccd8e-121">Pro každý karton vytvořte jedinečný kód sériového přepravního kontejneru (SSCC) a vložte jej do každého štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="ccd8e-122">Vytvořte číselné sekvence kompatibilní s GS1 pro ID přepravních dokladů a SSCC.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="ccd8e-123">Opakovaně tiskněte štítky z mobilních zařízení i z bohatého klienta.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="ccd8e-124">Anulujte štítky (například ve scénářích krátkého výběru) a znovu je vytiskněte.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="ccd8e-125">Vyčistěte historii vlnového štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="ccd8e-126">Vylepšení rozvržení rozvržení dokumentu jsou sdílena mezi rozvrženími směrování dokumentů a rozvržením popisků vlny.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="ccd8e-127">(Více informací viz [Rozvržení směrování dokumentů pro poznávací značky](../warehousing/document-routing-layout-for-license-plates.md).)</span><span class="sxs-lookup"><span data-stu-id="ccd8e-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="ccd8e-128">Tato vylepšení zefektivňují označování kartonů před paletizací.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="ccd8e-129">Výhodou jsou zejména pro společnosti, které dodávají velkým maloobchodníkům, kteří automaticky potvrzují příjmy z objednávek skenováním každého kartonu samostatně.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="ccd8e-130">Konfigurační scénáře popsané v tomto tématu můžete implementovat samostatně nebo v kombinaci, v závislosti na vašich obchodních požadavcích.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="ccd8e-131">Můžete navrhnout několik šablon popisků vlny, které fungují v sekvenci (jak je znázorněno ve scénáři 3).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="ccd8e-132">Například můžete použít scénář 1 pro tisk štítků na kartonech a scénář 2 pro tisk štítků na paletách (pokud se palety na skladě liší ve velikosti a složení).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="ccd8e-133">Zapnutí funkce tisku popisků vlny</span><span class="sxs-lookup"><span data-stu-id="ccd8e-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="ccd8e-134">Než můžete použít funkci *Tisk popisků vlny*, musíte ji v systému zapnout.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="ccd8e-135">Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="ccd8e-136">Funkce je zde uvedena následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ccd8e-137">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ccd8e-138">**Název funkce:** *Tisk popisků vlny*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="ccd8e-139">Scénář 1: Tisk popisků vlny, kde je generován jeden popisek vlny</span><span class="sxs-lookup"><span data-stu-id="ccd8e-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="ccd8e-140">Tento scénář ukazuje, jak může společnost tisknout přepravní štítky pro velkého maloobchodníka, který automaticky potvrzuje potvrzení o objednávce skenováním každého kartonu samostatně.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="ccd8e-141">Tento scénář ukazuje průběh toku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="ccd8e-142">Zpřístupnění ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="ccd8e-142">Make demo data available</span></span>

<span data-ttu-id="ccd8e-143">Pokud chcete provést tento scénář, musíte mít nainstalována ukázková data a musíte vybrat právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="ccd8e-144">Ujistěte se, že je k dispozici metoda popisku vlny</span><span class="sxs-lookup"><span data-stu-id="ccd8e-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="ccd8e-145">Možná bude třeba obnovit metody zpracování vln, abyste měli dostupnou metodu tisku popisků vlny.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="ccd8e-146">Přejděte do **Řízení skladu \> Nastavení \> Vlny \> Metody zpracování vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="ccd8e-147">Potvrďte, že **waveLabelPrinting** je v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="ccd8e-148">Pokud není, vyberte **Obnovit metody** v podokně Akce, abyste ji přidali.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="ccd8e-149">Konfigurujte šablonu vlny</span><span class="sxs-lookup"><span data-stu-id="ccd8e-149">Configure a wave template</span></span>

<span data-ttu-id="ccd8e-150">Šablony vln vám umožní propojit konkrétní příklady vlnových metod s odpovídající šablonou vlnových štítků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="ccd8e-151">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="ccd8e-152">Vyberte šablonu, např. **Vychozí dodávka 62**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="ccd8e-153">Na pevné záložce **Metody** přesuňte metodu **Tisk popisků vlny** do sloupce **Vybrané metody**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="ccd8e-154">V sloupci **Vybrané metody** vyberte metodu **Tisk popisků vlny** a nastavte její pole **Kód kroku vlny** na *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="ccd8e-155">Další informace o kódech kroku vlny viz [Kódy kroku vlny](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="ccd8e-156">Vytvořte rozvržení vlnového štítku</span><span class="sxs-lookup"><span data-stu-id="ccd8e-156">Create a wave label layout</span></span>

<span data-ttu-id="ccd8e-157">Rozvržení štítku řídí, jaké informace jsou na štítku vytištěny a jak jsou rozloženy. Zde zadáte kód ZPL, který je odeslán do tiskárny.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="ccd8e-158">Přejděte na **Správa skladu \> Nastavení \> Směrování dokumentu \> Rozložení popisku vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="ccd8e-159">Vytvořte záznam, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-160">**ID rozložení štítku:** *Kartón*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="ccd8e-161">**Popis:** *Karton (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="ccd8e-162">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="ccd8e-163">V podokně Akce vyberte **Nastavení řádku popisku vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="ccd8e-164">Zobrazí se stránka **Nastavení řádku popisku vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="ccd8e-165">Zde můžete nakonfigurovat dynamickou část štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="ccd8e-166">Přidejte řádek, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-167">**ID řádku:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="ccd8e-168">**Název tabulky řádků:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="ccd8e-169">**Pozice počátku řádku:** *0*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="ccd8e-170">Toto pole definuje vertikální polohu, kde bude řádek začínat na štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="ccd8e-171">**Výška řádku:** *0*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-171">**Row height:** *0*</span></span>

        <span data-ttu-id="ccd8e-172">Toto pole definuje výšku každého řádku (v bodech) podle standardu ZPL.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="ccd8e-173">Výška řádku je kladná pro vodorovné štítky a záporná pro vertikální štítky.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="ccd8e-174">Protože v tomto příkladu je pouze jeden řádek, můžete nastavit hodnotu na *0* (nula).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="ccd8e-175">**Řádky na stránku:** *1*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="ccd8e-176">Toto pole definuje počet řádků, které lze vytisknout na každý štítek.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="ccd8e-177">Toto nastavení způsobí, že se pro každý záznam v tabulce vlnových štítků vytiskne samostatný štítek ZPL.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="ccd8e-178">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-178">Close the page.</span></span>
1. <span data-ttu-id="ccd8e-179">V podokně akcí vyberte **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="ccd8e-180">V dialogovém okně Editor dotazů na kartě **Oblast** přidejte řádek, který má nasledující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-181">**Tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="ccd8e-182">**Odvozená tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="ccd8e-183">**Pole:** *Typ práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="ccd8e-184">**Kritéria:** *Výdej*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="ccd8e-185">Tento dotaz zajišťuje, že na štítek budou vytištěny pouze pracovní řádky typu pick, nikoli pracovní řádky typu put.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="ccd8e-186">Pokud chcete mít možnost vytisknout nákladní list, na kartě **Připojí se** vyberte záložku **Pracovní řádky** a připojte k nim tabulku **Zásilky**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="ccd8e-187">Zavřete dialogové okno editoru dotazů.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="ccd8e-188">Pevná záložka **Rozložení textu tiskárny** má tři oddíly, kde můžete psát kód tiskárny: **Sekce záhlaví**, **Sekce text** a **Sekce zápatí**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="ccd8e-189">V **Sekci záhlaví** v poli **Hlavička štítku** zadejte kód pro požadovanou hlavičku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="ccd8e-190">Pokud například používáte tiskárny Zebra, můžete použít následující kód.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="ccd8e-191">V **Sekci text** v poli **Text štítku** zadejte kód ZPL pro požadovaný text.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="ccd8e-192">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-192">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="ccd8e-193">V **Sekci text** v poli **Zápatí štítku** zadejte kód ZPL pro požadované zápatí.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="ccd8e-194">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="ccd8e-195">Toto nastavení vytiskne jednu kopii každého štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="ccd8e-196">Pokud potřebujete více kopií (například jednu kopii pro každou stranu palety), nastavte hodnotu **n** pro sekci **\^PQn** v zápatí na požadovaný počet kopií.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="ccd8e-197">Chcete-li například vytisknout čtyři kopie každého štítku, zadejte **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="ccd8e-198">Váš štítek je nyní připraven k použití.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="ccd8e-199">Vytvořte typ vlnového štítku</span><span class="sxs-lookup"><span data-stu-id="ccd8e-199">Create a wave label type</span></span>

<span data-ttu-id="ccd8e-200">Typy vlnových štítků se používají k propojení šablon vlnových štítků s jednotkou na řádcích skupin sekvencí jednotek.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="ccd8e-201">Přejděte na **Správa skladu \> Nastavení \> Směrování dokumentu \> Typy popisků vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="ccd8e-202">Přidejte typ popisku vlny, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-203">**Typ štítku:** *Kartón*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="ccd8e-204">**Popis:** *Kartón*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="ccd8e-205">Nastavit skupiny klasifikace jednotek</span><span class="sxs-lookup"><span data-stu-id="ccd8e-205">Set up unit sequence groups</span></span>

<span data-ttu-id="ccd8e-206">Dále nastavte skupinu sekvencí jednotek pro typ vlnového štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="ccd8e-207">Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Skupiny sekvenci jednotek**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="ccd8e-208">Vyberte skupinu **Ea Box PL**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="ccd8e-209">Pro řádek **Krabice** nastavte **Typ úrovně vlny** na *Kartón*.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="ccd8e-210">Vytvoření šablony vlnového štítku</span><span class="sxs-lookup"><span data-stu-id="ccd8e-210">Create a wave label template</span></span>

<span data-ttu-id="ccd8e-211">Dále vytvořte šablonu vlnového štítku pro typ vlnového štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="ccd8e-212">Přejděte na **Správa skladu \> Nastavení \> Směrování dokumentu \> Šablony popisku vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="ccd8e-213">Přidejte šsblonu úrovně vlnx a nastavte následující hodnoty v záhlaví:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="ccd8e-214">**Název šablony štítku:** *Štítky kartonu*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="ccd8e-215">**Popis:** *Štítky kartonů*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="ccd8e-216">**Kód kroku vlny:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="ccd8e-217">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="ccd8e-218">Na pevné záložce **Všeobecné** nastavte pole **Typ vlnového štítku** na *Karton*.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="ccd8e-219">Na pevné záložce **Podrobnosti o šabloně vlnového štítku** přidejte nový řádek, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-220">**ID rozložení štítku:** *Kartón*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="ccd8e-221">**Název tiskárny:** Vyberte vhodnou tiskárnu ZPL.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="ccd8e-222">**Spustit dotaz:** *Ano* (Toto nastavení je volitelné, ale pro optimální výkon se doporučuje.)</span><span class="sxs-lookup"><span data-stu-id="ccd8e-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="ccd8e-223">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="ccd8e-224">Volitelné: Pokud nastavujete design štítků specifických pro zákazníka, musíte vytvořit dotaz, abyste našli účet zákazníka.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="ccd8e-225">Na pevné záložce **Podrobnosti o šabloně vlnového štítku** vyberte **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="ccd8e-226">Pak v dialogovém okně Editor dotazů na kartě **Oblast** přidejte řádek, který má nasledující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-227">**Tabulka:** *Dodávky*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="ccd8e-228">**Odvozená tabulka:** *Dodávky*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="ccd8e-229">**Pole:** *Číslo účtu*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="ccd8e-230">**Kritéria:** Zadejte příslušné číslo zákaznického účtu.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="ccd8e-231">Po dokončení vyberte **OK** a zavřete dialogové okno editoru dotazů.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="ccd8e-232">V podokně Akce zvolte **Upravit dotaz** a otevřete dialogové okno editor dotazů pro celou šablonu štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="ccd8e-233">V dialogovém okně Editor dotazů na kartě **Třídění** přidejte řádek, který má nasledující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-234">**Tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="ccd8e-235">**Odvozená tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="ccd8e-236">**Pole:** *ID referenčního nákladového řádku (ID záznamu)*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="ccd8e-237">**Směr hledání:** *Vzestupně*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="ccd8e-238">Vyberte **OK** a dialogové okno editor dotazu zavřete.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="ccd8e-239">Okno se zprávou vás vyzve k potvrzení operace resetování seskupení.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="ccd8e-240">Pokračujte výběrem tlačítka **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="ccd8e-241">V podokně Akce vyberte možnost **Skupina šablon úrovně vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="ccd8e-242">V dialogovém okně **Skupina šablon úrovně vlny** vyberte řádek, ve kterém je pole **Název referenčního pole** nastaveno na *ID referenčního nákladového řádku* a poté zaškrtněte **ID sestavení štítku** pro tento řádek.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id*, and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ccd8e-243">Toto nastavení vytvoří jednu sekvenci štítků („Karton 1 z X“) na řádek zatížení po celé vlně, bez ohledu na nastavení pracovní skupiny.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="ccd8e-244">Tuto sekvenci štítků lze vytisknout na rozvržení štítků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="ccd8e-245">Konfigurace rozšíření posloupnosti čísel</span><span class="sxs-lookup"><span data-stu-id="ccd8e-245">Configure number sequence extensions</span></span>

<span data-ttu-id="ccd8e-246">Rozšíření číselných sekvencí řídí dodržování specifických číselných sekvencí GS1.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="ccd8e-247">Tato konfigurace je pro aktuální scénář volitelná.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="ccd8e-248">Další informace a pokyny k konfiguraci najdete v části [Konfigurovat rozšíření posloupnosti čísel](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="ccd8e-249">Vytvořte prodejní objednávku a uvolněte ji do skladu</span><span class="sxs-lookup"><span data-stu-id="ccd8e-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="ccd8e-250">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="ccd8e-251">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-252">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="ccd8e-253">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="ccd8e-254">Přidejte dva řádky prodejní objednávky s následujícím nastavením:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="ccd8e-255">Řádek prodejní objednávky 1:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-255">Sales order line 1:</span></span>

        - <span data-ttu-id="ccd8e-256">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="ccd8e-257">**Množství:** *9024*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="ccd8e-258">**Jednotka:** *ea* (9024 ea = 376 Box = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="ccd8e-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="ccd8e-259">Řádek prodejní objednávky 2:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-259">Sales order line 2:</span></span>

        - <span data-ttu-id="ccd8e-260">**Číslo položky:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="ccd8e-261">**Množství:** *9016*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="ccd8e-262">**Jednotka:** *ea* (9016 ea = 322 Box = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="ccd8e-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="ccd8e-263">Položky a množství, které jsou zde uvedeny, jsou pouze příklady.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="ccd8e-264">Musí používat skupinu sekvencí jednotek, kterou jste definovali dříve, vhodné převody jednotek *ea* na *Box* na *PL* musí být pro ně definovány a musí mít zásoby ve skladu *62*.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="ccd8e-265">Další informace viz [Měrná jednotka a politika skladování](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="ccd8e-266">Vyberte řádek prodejní objednávky 1.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-266">Select sales order line 1.</span></span> <span data-ttu-id="ccd8e-267">Pak v sekci **Řádek prodejní objednávky** v nabídce **Zásoby** vyberte možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="ccd8e-268">Na stránce **Rezervace** vyberte v podokně Akce možnost **Rezervovat šarži** a zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-268">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="ccd8e-269">Opakujte kroky 4 a 5 pro řádek 2 prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="ccd8e-270">V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="ccd8e-271">Dojde k následujícím událostem:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-271">The following events occur:</span></span>

    - <span data-ttu-id="ccd8e-272">Systém zpracovává vytvořenou zásilku pomocí šablony, která zahrnuje krok tisku štítků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="ccd8e-273">Rozvržení štítků se použije k definování formátu štítků a výsledkem bude štítek, který se vytiskne na tiskárně vybrané v šabloně štítků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="ccd8e-274">Štítky vlny se generují a tisknou.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="ccd8e-275">Počet štítků se bude rovnat počtu kartonů (v tomto příkladu 376 štítků pro řádek 1 a 322 štítků pro řádek 2).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="ccd8e-276">Pro zásilky je vygenerován nový přepravní doklad.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="ccd8e-277">Pokud jste nakonfigurovali rozšíření číselných sekvencí, budou ID popisků vlny sledovat formát čísla **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="ccd8e-278">vlnové štítky můžete zobrazit a znovu vytisknout z následujících stránek.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="ccd8e-279">V podokně akcí každé ze stránek **Dodávky** ve skupině **Související informace** vyberte **vlnové štítky**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="ccd8e-280">Všechny zásilky \> Podrobnosti o zásilce</span><span class="sxs-lookup"><span data-stu-id="ccd8e-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="ccd8e-281">Všechny náklady \> Načíst podrobnosti</span><span class="sxs-lookup"><span data-stu-id="ccd8e-281">All loads \> Load details</span></span>
- <span data-ttu-id="ccd8e-282">Všechny vlny</span><span class="sxs-lookup"><span data-stu-id="ccd8e-282">All waves</span></span>
- <span data-ttu-id="ccd8e-283">Štítky vlny</span><span class="sxs-lookup"><span data-stu-id="ccd8e-283">Wave labels</span></span>
- <span data-ttu-id="ccd8e-284">Historie popisků vlny</span><span class="sxs-lookup"><span data-stu-id="ccd8e-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="ccd8e-285">Scénář 2: Tisk vlnových štítků pro kontejnerizaci (bez záznamů vlnových štítků)</span><span class="sxs-lookup"><span data-stu-id="ccd8e-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="ccd8e-286">Tento scénář umožňuje tisknout štítky vln, když pomocí kontejnerizace automaticky rozdělujete položky do kartonů, a proto nevyžadují záznam vlnových štítků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="ccd8e-287">V tomto případě ID kontejneru funguje jako zástupný symbol pro SSCC.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="ccd8e-288">Zde jsou hlavní rozdíly mezi tímto scénářem a scénářem 1:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="ccd8e-289">**Šablony vlnových štítků:** Nevyberete typ vlnového štítku v šabloně vlnového štítku a nebudete vyžadovat seskupení sestavení štítků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="ccd8e-290">V opačném případě nakonfigurujete šablonu popisku vlny a odkaz na šablonu vlny stejným způsobem, jaký je popsán ve scénáři 1.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="ccd8e-291">Chcete-li zabránit generování štítků vlny, musíte ponechat typ vlnového štítku prázdný.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="ccd8e-292">**Rozvržení vlnových štítků:** Nakonfigurujete nastavení řádků rozvržení vlnových štítků pro pracovní řádky namísto záznamů vlnových štítků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="ccd8e-293">Nastavení řádků pro rozvržení štítků musíte nakonfigurovat pomocí tabulky **WHSWorkLine** místo tabulky **WHSWaveLabel**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="ccd8e-294">Nastavení **Řádky na stránce** řídí počet řádků, které bude mít sekce text.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="ccd8e-295">Tato konfigurace je také vhodná pro obchodní scénáře, kde je více různých položek zabaleno do jednoho označeného pole nebo do palety, a tento proces balení lze definovat vytvořením práce (například práce, která je seskupena podle zásilky).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="ccd8e-296">Tento scénář ukazuje průběh toku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="ccd8e-297">Zpřístupnění ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="ccd8e-297">Make demo data available</span></span>

<span data-ttu-id="ccd8e-298">Pokud chcete provést tento scénář, musíte mít nainstalována ukázková data a musíte vybrat právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="ccd8e-299">Ujistěte se, že je k dispozici metoda popisku vlny</span><span class="sxs-lookup"><span data-stu-id="ccd8e-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="ccd8e-300">Možná bude třeba obnovit metody zpracování vln, abyste měli dostupnou metodu tisku popisků vlny.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="ccd8e-301">Přejděte do **Řízení skladu \> Nastavení \> Vlny \> Metody zpracování vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="ccd8e-302">Potvrďte, že **waveLabelPrinting** je v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="ccd8e-303">Pokud není, vyberte **Obnovit metody** v podokně Akce, abyste ji přidali.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="ccd8e-304">Nastavení šablony vlny</span><span class="sxs-lookup"><span data-stu-id="ccd8e-304">Set up a wave template</span></span>

<span data-ttu-id="ccd8e-305">Šablony vln vám umožní propojit konkrétní příklady vlnových metod s odpovídající šablonou vlnových štítků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="ccd8e-306">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="ccd8e-307">Vyberte šablonu, např. **Kontejnerizace 63**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="ccd8e-308">Na pevné záložce **Metody** přesuňte metodu **Tisk popisků vlny** do sloupce **Vybrané metody**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="ccd8e-309">V sloupci **Vybrané metody** vyberte metodu **Tisk popisků vlny** a nastavte její pole **Kód kroku vlny** na *PrintLabel*.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="ccd8e-310">Další informace o kódech kroku vlny viz [Kódy kroku vlny](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="ccd8e-311">Vytvořte rozvržení vlnového štítku</span><span class="sxs-lookup"><span data-stu-id="ccd8e-311">Create a wave label layout</span></span>

1. <span data-ttu-id="ccd8e-312">Přejděte na **Správa skladu \> Nastavení \> Směrování dokumentu \> Rozložení popisku vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="ccd8e-313">Vytvořte záznam, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-314">**ID rozložení štítku:** *Kartón*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="ccd8e-315">**Popis:** *Karton (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="ccd8e-316">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="ccd8e-317">V podokně Akce vyberte **Nastavení řádku popisku vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="ccd8e-318">Zobrazí se stránka **Nastavení řádku popisku vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="ccd8e-319">Zde můžete nakonfigurovat dynamickou část štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="ccd8e-320">Přidejte řádek, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-321">**ID řádku:** *WorkLine*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="ccd8e-322">**Název tabulky řádků:** *WHSWorkLine*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="ccd8e-323">**Pozice počátku řádku:** *500*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="ccd8e-324">Toto pole definuje vertikální polohu, kde bude řádek začínat na štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="ccd8e-325">**Výška řádku** *-50*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="ccd8e-326">Toto pole definuje výšku každého řádku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-326">This field defines the height of each row.</span></span> <span data-ttu-id="ccd8e-327">Výška řádku je kladná pro vodorovné štítky a záporná pro vertikální štítky.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="ccd8e-328">**Řádky na stránku:** *5*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="ccd8e-329">Toto pole definuje počet řádků, které lze vytisknout na každý štítek.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="ccd8e-330">Toto nastavení vytiskne několik štítků ZPL na dílo, kde každá stránka pojme až pět pracovních řádků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="ccd8e-331">Pokud je například štítek vytištěn pro kontejner, který má 12 řádků, vytisknou se tři štítky.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="ccd8e-332">Pokud chcete vytisknout samostatný štítek pro každý řádek výběru, nastavte tuto hodnotu na *1*.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="ccd8e-333">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-333">Close the page.</span></span>
1. <span data-ttu-id="ccd8e-334">V podokně akcí vyberte **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="ccd8e-335">V dialogovém okně Editor dotazů na kartě **Oblast** přidejte řádek, který má nasledující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-336">**Tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="ccd8e-337">**Odvozená tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="ccd8e-338">**Pole:** *Typ práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="ccd8e-339">**Kritéria:** *Výdej*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="ccd8e-340">Pokud chcete mít možnost vytisknout nákladní list, na kartě **Připojí se** vyberte záložku **Pracovní řádky** a připojte k nim tabulku **Zásilky**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="ccd8e-341">Zavřete dialogové okno editoru dotazů.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="ccd8e-342">Pevná záložka **Rozložení textu tiskárny** má tři oddíly, kde můžete psát kód tiskárny: **Sekce záhlaví**, **Sekce text** a **Sekce zápatí**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="ccd8e-343">V **Sekci záhlaví** v poli **Hlavička štítku** zadejte kód pro požadovanou hlavičku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="ccd8e-344">Pokud například používáte tiskárny Zebra, můžete použít následující kód.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="ccd8e-345">V **Sekci text** v poli **Text štítku** zadejte kód ZPL pro požadovaný text.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="ccd8e-346">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-346">Here is an example.</span></span>

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="ccd8e-347">V **Sekci text** v poli **Zápatí štítku** zadejte kód ZPL pro požadované zápatí.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="ccd8e-348">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="ccd8e-349">Toto nastavení vytiskne jednu kopii každého štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="ccd8e-350">Pokud potřebujete více kopií (například jednu kopii pro každou stranu palety), nastavte hodnotu **n** pro sekci **\^PQn** v zápatí na požadovaný počet kopií.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="ccd8e-351">Chcete-li například vytisknout čtyři kopie každého štítku, zadejte **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="ccd8e-352">Váš štítek je nyní připraven k použití.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="ccd8e-353">Vytvoření šablony vlnového štítku</span><span class="sxs-lookup"><span data-stu-id="ccd8e-353">Create a wave label template</span></span>

1. <span data-ttu-id="ccd8e-354">Přejděte na **Správa skladu \> Nastavení \> Směrování dokumentu \> Šablony popisku vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="ccd8e-355">Přidejte šsblonu úrovně vlnx a nastavte následující hodnoty v záhlaví:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="ccd8e-356">**Název šablony štítku:** *Štítky kontejneru*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="ccd8e-357">**Popis:** *Štítky kontejnerů*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="ccd8e-358">**Kód kroku vlny:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="ccd8e-359">**Sklad:** *63*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="ccd8e-360">Na pevné záložce **Podrobnosti o šabloně vlnového štítku** přidejte řádek, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-361">**ID rozložení štítku:** *Kontejner*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="ccd8e-362">**Název tiskárny:** Vyberte vhodnou tiskárnu ZPL.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="ccd8e-363">**Spustit dotaz:** *Ano* (Toto nastavení je volitelné, ale pro optimální výkon se doporučuje.)</span><span class="sxs-lookup"><span data-stu-id="ccd8e-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="ccd8e-364">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="ccd8e-365">Volitelné: Pokud nastavujete design štítků specifických pro zákazníka, musíte vytvořit dotaz, abyste našli účet zákazníka.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="ccd8e-366">Na pevné záložce **Podrobnosti o šabloně vlnového štítku** vyberte **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="ccd8e-367">Pak v dialogovém okně Editor dotazů na kartě **Oblast** přidejte řádek, který má nasledující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-368">**Tabulka:** *Dodávky*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="ccd8e-369">**Odvozená tabulka:** *Dodávky*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="ccd8e-370">**Pole:** *Číslo účtu*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="ccd8e-371">**Kritéria:** Zadejte příslušné číslo zákaznického účtu.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="ccd8e-372">Po dokončení vyberte **OK** a zavřete dialogové okno editoru dotazů.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="ccd8e-373">Konfigurace rozšíření posloupnosti čísel</span><span class="sxs-lookup"><span data-stu-id="ccd8e-373">Configure number sequence extensions</span></span>

<span data-ttu-id="ccd8e-374">Rozšíření číselných sekvencí řídí dodržování specifických číselných sekvencí GS1.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="ccd8e-375">Tato konfigurace je pro aktuální scénář volitelná.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="ccd8e-376">Další informace a pokyny k konfiguraci najdete v části [Konfigurovat rozšíření posloupnosti čísel](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="ccd8e-377">Vytvořte prodejní objednávku a uvolněte ji do skladu</span><span class="sxs-lookup"><span data-stu-id="ccd8e-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="ccd8e-378">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="ccd8e-379">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-380">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="ccd8e-381">**Sklad:** *63*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="ccd8e-382">Přidejte pět řádků prodejní objednávky:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="ccd8e-383">Řádek prodejní objednávky 1:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-383">Sales order line 1:</span></span>

        - <span data-ttu-id="ccd8e-384">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="ccd8e-385">**Množství:** *10*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="ccd8e-386">Řádek prodejní objednávky 2:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-386">Sales order line 2:</span></span>

        - <span data-ttu-id="ccd8e-387">**Číslo položky:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="ccd8e-388">**Množství:** *20*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="ccd8e-389">Řádek prodejní objednávky 3:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-389">Sales order line 3:</span></span>

        - <span data-ttu-id="ccd8e-390">**Číslo položky:** *L0006*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="ccd8e-391">**Množství:** *20*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="ccd8e-392">Řádek prodejní objednávky 4:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-392">Sales order line 4:</span></span>

        - <span data-ttu-id="ccd8e-393">**Číslo položky:** *L0100*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="ccd8e-394">**Množství:** *40*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="ccd8e-395">Řádek prodejní objednávky 5:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-395">Sales order line 5:</span></span>

        - <span data-ttu-id="ccd8e-396">**Číslo položky:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="ccd8e-397">**Množství:** *50*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="ccd8e-398">Položky a množství, které jsou zde uvedeny, jsou pouze příklady.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="ccd8e-399">Musí mít zásoby v určeném skladu.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="ccd8e-400">Vyberte řádek prodejní objednávky 1.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-400">Select sales order line 1.</span></span> <span data-ttu-id="ccd8e-401">Pak v sekci **Řádek prodejní objednávky** v nabídce **Zásoby** vyberte možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="ccd8e-402">Na stránce **Rezervace** vyberte v podokně Akce možnost **Rezervovat šarži** a zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-402">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="ccd8e-403">Opakujte kroky 4 a 5 pro každý další řádek prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="ccd8e-404">V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="ccd8e-405">Dojde k následujícím událostem:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-405">The following events occur:</span></span>

    - <span data-ttu-id="ccd8e-406">Systém zpracovává vytvořenou zásilku pomocí šablony, která zahrnuje krok tisku štítků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="ccd8e-407">Rozvržení štítků se použije k definování formátu štítků a konečným výsledkem bude štítek, který má pět řádků a vytiskne se na tiskárně vybrané v šabloně štítků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="ccd8e-408">Pro zásilky je vygenerován nový přepravní doklad.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="ccd8e-409">Pokud jste nakonfigurovali rozšíření číselných sekvencí, budou ID popisků vlny sledovat formát čísla **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="ccd8e-410">Tyto štítky vln můžete znovu vytisknout tak, že přejdete na **Správa skladu \> Dotazy a sestavy \> Historie vlnových štítků**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="ccd8e-411">Scénář 3: Tisk vlnových štítků pro vícevrstvé štítky</span><span class="sxs-lookup"><span data-stu-id="ccd8e-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="ccd8e-412">Tento scénář ukazuje, jak používat funkci tisku vlnových štítků, když procesy skladování vyžadují několik úrovní přepravních štítků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="ccd8e-413">Například samostatné štítky mohou být vytištěny na kartony a palety a štítek zalomení musí být vytištěn na celou zásilku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="ccd8e-414">Štítky zalomení jsou samostatný typ štítku, který lze použít jako oddělovač mezi rolemi a kontejnery, jako jsou například štítky pro ID zásilky a čárový kód, takže štítky lze po vytištění snadno třídit.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="ccd8e-415">Hlavní rozdíl mezi konfigurací tohoto scénáře a konfigurací scénáře 1, kromě skutečnosti, že jsou povoleny štítky zalomení, spočívá v tom, že více šablon štítků musí být spojeno se šablonami štítků vln a řádky skupin sekvencí jednotek.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="ccd8e-416">Chcete-li provést tuto konfiguraci, nastavte pro tento scénář následující prvky:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="ccd8e-417">**Metody zpracování vln:** Metodu označování vln označíte jako „opakovatelnou“, přidáte ji dvakrát (nebo vícekrát) do šablony vln a nastavíte různé kódy vlnových kroků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="ccd8e-418">**Šablony vlnových štítků:** Nakonfigurujete šablony vlnových štítků a propojíte je s vlnovou šablonou.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="ccd8e-419">Každá šablona štítků vln má svůj vlastní typ štítků vln.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="ccd8e-420">**Rozvržení vlnových štítků:** Vytvoříte více rozvržení vlnových štítků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="ccd8e-421">Pro každou „vrstvu“ štítků bude existovat samostatné rozvržení štítků a také rozvržení přerušení štítků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="ccd8e-422">Tento scénář ukazuje průběh toku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="ccd8e-423">Zpřístupnění ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="ccd8e-423">Make demo data available</span></span>

<span data-ttu-id="ccd8e-424">Pokud chcete provést tento scénář, musíte mít nainstalována ukázková data a musíte vybrat právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="ccd8e-425">Nastavení metody vlnového procesu</span><span class="sxs-lookup"><span data-stu-id="ccd8e-425">Set up a wave process method</span></span>

1. <span data-ttu-id="ccd8e-426">Přejděte do **Řízení skladu \> Nastavení \> Vlny \> Metody zpracování vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="ccd8e-427">Potvrďte, že **waveLabelPrinting** je v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="ccd8e-428">Pokud není, vyberte **Obnovit metody** v podokně Akce, abyste ji přidali.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="ccd8e-429">Pro metodu **waveLabelPrinting** zaškrtněte **Zajistit opakovatelnost metody**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="ccd8e-430">Nastavení šablony vlny</span><span class="sxs-lookup"><span data-stu-id="ccd8e-430">Set up a wave template</span></span>

1. <span data-ttu-id="ccd8e-431">Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="ccd8e-432">Vyberte šablonu, např. **Vychozí dodávka 62**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="ccd8e-433">Na pevné záložce **Metody** přesuňte metodu **Tisk popisků vlny** do sloupce **Vybrané metody**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="ccd8e-434">V sloupci **Vybrané metody** přiřaďte hodnotu **Kód kroku vlny**, například *Karton*, k metodě **Tisk štítků vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton*, to the **Wave label printing** method.</span></span> <span data-ttu-id="ccd8e-435">Další informace o kódech kroku vlny viz [Kódy kroku vlny](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="ccd8e-436">Přesuňte metodu **Tisk popisků vlny** do sloupce **Vybrané metody** podruhé.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="ccd8e-437">V sloupci **Vybrané metody** přiřaďte jinou hodnotu **Kód kroku vlny**, například *Paleta*, k druhé metodě **Tisk štítků vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet*, to the second **Wave label printing** method.</span></span> <span data-ttu-id="ccd8e-438">Další informace o kódech kroku vlny viz [Kódy kroku vlny](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="ccd8e-439">Vytvořte tři rozvržení vlnového štítku</span><span class="sxs-lookup"><span data-stu-id="ccd8e-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="ccd8e-440">Přejděte na **Správa skladu \> Nastavení \> Směrování dokumentu \> Rozložení popisku vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="ccd8e-441">Vytvořte záznam, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-442">**ID rozložení štítku:** *Kartón*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="ccd8e-443">**Popis:** *Karton (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="ccd8e-444">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="ccd8e-445">V podokně Akce vyberte **Nastavení řádku popisku vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="ccd8e-446">Zobrazí se stránka **Nastavení řádku popisku vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="ccd8e-447">Zde můžete nakonfigurovat dynamickou část štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="ccd8e-448">Přidejte řádek, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-449">**ID řádku:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="ccd8e-450">**Název tabulky řádků:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="ccd8e-451">**Pozice počátku řádku:** *0*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="ccd8e-452">Toto pole definuje vertikální polohu, kde bude řádek začínat na štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="ccd8e-453">**Výška řádku:** *0*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-453">**Row height:** *0*</span></span>

        <span data-ttu-id="ccd8e-454">Toto pole definuje výšku každého řádku (v bodech) podle standardu ZPL.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="ccd8e-455">Výška řádku je kladná pro vodorovné štítky a záporná pro vertikální štítky.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="ccd8e-456">Protože v tomto příkladu je pouze jeden řádek, můžete nastavit hodnotu na *0* (nula).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="ccd8e-457">**Řádky na stránku:** *1*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="ccd8e-458">Toto pole definuje počet řádků, které lze vytisknout na každý štítek.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="ccd8e-459">Toto nastavení způsobí, že se pro každý záznam v tabulce vlnových štítků vytiskne samostatný štítek ZPL.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="ccd8e-460">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-460">Close the page.</span></span>
1. <span data-ttu-id="ccd8e-461">V podokně akcí vyberte **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="ccd8e-462">V dialogovém okně Editor dotazů na kartě **Oblast** přidejte řádek, který má nasledující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-463">**Tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="ccd8e-464">**Odvozená tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="ccd8e-465">**Pole:** *Typ práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="ccd8e-466">**Kritéria:** *Výdej*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="ccd8e-467">Tento dotaz zajišťuje, že na štítek budou vytištěny pouze pracovní řádky typu pick, nikoli pracovní řádky typu put.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="ccd8e-468">Pokud chcete mít možnost vytisknout nákladní list, na kartě **Připojí se** vyberte záložku **Pracovní řádky** a připojte k nim tabulku **Zásilky**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="ccd8e-469">Zavřete dialogové okno editoru dotazů.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="ccd8e-470">Pevná záložka **Rozložení textu tiskárny** má tři oddíly, kde můžete psát kód tiskárny: **Sekce záhlaví**, **Sekce text** a **Sekce zápatí**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="ccd8e-471">V **Sekci záhlaví** v poli **Hlavička štítku** zadejte kód pro požadovanou hlavičku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="ccd8e-472">Pokud například používáte tiskárny Zebra, můžete použít následující kód.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="ccd8e-473">V **Sekci text** v poli **Text štítku** zadejte kód ZPL pro požadovaný text.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="ccd8e-474">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-474">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="ccd8e-475">V **Sekci text** v poli **Zápatí štítku** zadejte kód ZPL pro požadované zápatí.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="ccd8e-476">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="ccd8e-477">Toto nastavení vytiskne jednu kopii každého štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="ccd8e-478">Pokud potřebujete více kopií (například jednu kopii pro každou stranu palety), nastavte hodnotu **n** pro sekci **\^PQn** v zápatí na požadovaný počet kopií.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="ccd8e-479">Chcete-li například vytisknout čtyři kopie každého štítku, zadejte **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="ccd8e-480">První štítek je nyní připraven k použití.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="ccd8e-481">Vytvořte druhý záznam rozvržení, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-482">**ID rozložení štítku:** *Paleta*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="ccd8e-483">**Popis:** *Paleta*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="ccd8e-484">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="ccd8e-485">V podokně Akce vyberte **Nastavení řádku popisku vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="ccd8e-486">Zobrazí se stránka **Nastavení řádku popisku vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="ccd8e-487">Zde můžete nakonfigurovat dynamickou část štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="ccd8e-488">Přidejte řádek, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-489">**ID řádku:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="ccd8e-490">**Název tabulky řádků:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="ccd8e-491">**Pozice počátku řádku:** *0*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="ccd8e-492">Toto pole definuje vertikální polohu, kde bude řádek začínat na štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="ccd8e-493">**Výška řádku:** *0*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-493">**Row height:** *0*</span></span>

        <span data-ttu-id="ccd8e-494">Toto pole definuje výšku každého řádku (v bodech) podle standardu ZPL.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="ccd8e-495">Výška řádku je kladná pro vodorovné štítky a záporná pro vertikální štítky.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="ccd8e-496">Protože v tomto příkladu je pouze jeden řádek, můžete nastavit hodnotu na *0* (nula).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="ccd8e-497">**Řádky na stránku:** *1*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="ccd8e-498">Toto pole definuje počet řádků, které lze vytisknout na každý štítek.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="ccd8e-499">Toto nastavení způsobí, že se pro každý záznam v tabulce vlnových štítků vytiskne samostatný štítek ZPL.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="ccd8e-500">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-500">Close the page.</span></span>
1. <span data-ttu-id="ccd8e-501">V podokně akcí vyberte **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="ccd8e-502">V dialogovém okně Editor dotazů na kartě **Oblast** přidejte řádek, který má nasledující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-503">**Tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="ccd8e-504">**Odvozená tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="ccd8e-505">**Pole:** *Typ práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="ccd8e-506">**Kritéria:** *Výdej*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="ccd8e-507">Tento dotaz zajišťuje, že na štítek budou vytištěny pouze pracovní řádky typu pick, nikoli pracovní řádky typu put.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="ccd8e-508">Pokud chcete mít možnost vytisknout nákladní list, na kartě **Připojí se** vyberte záložku **Pracovní řádky** a připojte k nim tabulku **Zásilky**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="ccd8e-509">Zavřete dialogové okno editoru dotazů.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="ccd8e-510">Pevná záložka **Rozložení textu tiskárny** má tři oddíly, kde můžete psát kód tiskárny: **Sekce záhlaví**, **Sekce text** a **Sekce zápatí**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="ccd8e-511">V **Sekci záhlaví** v poli **Hlavička štítku** zadejte kód pro požadovanou hlavičku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="ccd8e-512">Pokud například používáte tiskárny Zebra, můžete použít následující kód.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="ccd8e-513">V **Sekci text** v poli **Text štítku** zadejte kód ZPL pro požadovaný text.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="ccd8e-514">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="ccd8e-515">V **Sekci text** v poli **Zápatí štítku** zadejte kód ZPL pro požadované zápatí.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="ccd8e-516">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="ccd8e-517">Toto nastavení vytiskne jednu kopii každého štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="ccd8e-518">Pokud potřebujete více kopií (například jednu kopii pro každou stranu palety), nastavte hodnotu **n** pro sekci **\^PQn** v zápatí na požadovaný počet kopií.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="ccd8e-519">Chcete-li například vytisknout čtyři kopie každého štítku, zadejte **\^PQ4**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="ccd8e-520">Druhý štítek je nyní připraven k použití.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="ccd8e-521">Vytvořte třetí záznam rozvržení, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-522">**ID rozložení štítku:** *Přerušení*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="ccd8e-523">**Popis:** *Štítek přerušení*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="ccd8e-524">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="ccd8e-525">Pevná záložka **Rozložení textu tiskárny** má tři oddíly, kde můžete psát kód tiskárny: **Sekce záhlaví**, **Sekce text** a **Sekce zápatí**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="ccd8e-526">V **Sekci záhlaví** v poli **Hlavička štítku** zadejte kód ZPL pro požadovanou hlavičku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="ccd8e-527">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="ccd8e-528">Tentokrát není nutný nžádný text.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-528">This time, no body is required.</span></span> <span data-ttu-id="ccd8e-529">Proto jednoduše zadejte požadovaný text do **Sekce zápatí**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="ccd8e-530">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="ccd8e-531">Třetí štítek je nyní připraven k použití.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ccd8e-532">Tento třetí štítek je štítek přerušení, který bude použit jako oddělovač mezi svitky štítků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="ccd8e-533">Vytvořte dva typy vlnového štítku</span><span class="sxs-lookup"><span data-stu-id="ccd8e-533">Create two wave label types</span></span>

1. <span data-ttu-id="ccd8e-534">Přejděte na **Správa skladu \> Nastavení \> Směrování dokumentu \> Typy popisků vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="ccd8e-535">Vytvořte záznam, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-536">**Typ štítku:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="ccd8e-537">**Popis:** *Kartón*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="ccd8e-538">Vytvořte druhý záznam, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-539">**Typ štítku:** *Paleta*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="ccd8e-540">**Popis:** *Paleta*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="ccd8e-541">Nastavit skupiny klasifikace jednotek</span><span class="sxs-lookup"><span data-stu-id="ccd8e-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="ccd8e-542">Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Skupiny sekvenci jednotek**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="ccd8e-543">Vyberte nebo vytvořte skupinu **Ea Box PL**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="ccd8e-544">Pro řádek **Krabice** nastavte **Typ úrovně vlny** na *Kartón*.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="ccd8e-545">Pro řádek **PL** nastavte **Typ úrovně vlny** na *Paletu*.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="ccd8e-546">Vytvoření šablon vlnového štítku</span><span class="sxs-lookup"><span data-stu-id="ccd8e-546">Create wave label templates</span></span>

1. <span data-ttu-id="ccd8e-547">Přejděte na **Správa skladu \> Nastavení \> Směrování dokumentu \> Šablony popisku vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="ccd8e-548">Vytvořte šablonu popisku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-549">**Název šablony štítku:** *Štítky kartonu*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="ccd8e-550">**Popis:** *Štítky kartonů*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="ccd8e-551">**Kód kroku vlny:** *Karton*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="ccd8e-552">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="ccd8e-553">Na záložce s náhledem **Obecné** v poli **Typ popisků vlny** vyberte hodnotu, např. *Karton*.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="ccd8e-554">Na pevné záložce **Podrobnosti o šabloně vlnového štítku** přidejte řádek, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-555">**ID rozložení štítku:** *Kartón*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="ccd8e-556">**Název tiskárny:** Vyberte vhodnou tiskárnu ZPL.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="ccd8e-557">**Spustit dotaz:** *Ano* (Toto nastavení je volitelné, ale pro optimální výkon se doporučuje.)</span><span class="sxs-lookup"><span data-stu-id="ccd8e-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="ccd8e-558">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="ccd8e-559">Volitelné: Pokud nastavujete design štítků specifických pro zákazníka, musíte vytvořit dotaz, abyste našli účet zákazníka.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="ccd8e-560">Na pevné záložce **Podrobnosti o šabloně vlnového štítku** vyberte **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="ccd8e-561">Pak v dialogovém okně Editor dotazů na kartě **Oblast** přidejte řádek, který má nasledující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-562">**Tabulka:** *Dodávky*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="ccd8e-563">**Odvozená tabulka:** *Dodávky*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="ccd8e-564">**Pole:** *Číslo účtu*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="ccd8e-565">**Kritéria:** Zadejte příslušné číslo zákaznického účtu.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="ccd8e-566">Po dokončení vyberte **OK** a zavřete dialogové okno editoru dotazů.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="ccd8e-567">V podokně Akce zvolte **Upravit dotaz** a otevřete dialogové okno editor dotazů pro celou šablonu štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="ccd8e-568">V dialogovém okně Editor dotazů na kartě **Třídění** přidejte řádek, který má nasledující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-569">**Tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="ccd8e-570">**Odvozená tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="ccd8e-571">**Pole:** *ID referenčního nákladového řádku (ID záznamu)*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="ccd8e-572">**Směr hledání:** *Vzestupně*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="ccd8e-573">Přidejte druhý řádek, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-574">**Tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="ccd8e-575">**Odvozená tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="ccd8e-576">**Pole:** *ID dodávky*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="ccd8e-577">**Směr hledání:** *Vzestupně*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="ccd8e-578">Vyberte **OK** a dialogové okno editor dotazu zavřete.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="ccd8e-579">Okno se zprávou vás vyzve k potvrzení operace resetování seskupení.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="ccd8e-580">Pokračujte výběrem tlačítka **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="ccd8e-581">V podokně Akce vyberte možnost **Skupina šablon úrovně vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="ccd8e-582">V dialogovém okně **Skupina šablon popisků vlny** pro řádek, kde je pole **Název referenčního pole** nastaveno na *ID zásilky*, nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="ccd8e-583">**Tisk štítku přerušení:** Zaškrtněte toto políčko.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="ccd8e-584">**ID rozložení štítku:** Vyberte štítek přerušení.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="ccd8e-585">(Například vyberte štítek *Přerušení*, který jste vytvořili dříve v tomto scénáři.)</span><span class="sxs-lookup"><span data-stu-id="ccd8e-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="ccd8e-586">**Název tiskárny:** Vyberte tiskárnu pro štítek přerušení.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="ccd8e-587">(Obvykle byste za účelem rozdělení rolí štítků měli vybrat stejnou tiskárnu, která je vybrána na pevné záložce **Podrobnosti o šabloně vlnového štítku**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="ccd8e-588">Jsou však možné i jiné scénáře.)</span><span class="sxs-lookup"><span data-stu-id="ccd8e-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="ccd8e-589">Pro řádek, kde je pole **Název referenčního pole** nastaveno na *ID referenčního zatížení*, zaškrtněte **ID sestavení štítku**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-589">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ccd8e-590">Toto nastavení vytvoří jednu sekvenci štítků („Karton 1 z X“) na řádek zatížení po celé vlně, bez ohledu na nastavení pracovní skupiny.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="ccd8e-591">Tuto sekvenci štítků lze vytisknout na rozvržení štítků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="ccd8e-592">Štítky pro různé zásilky budou navíc odděleny vybraným štítkem přerušení.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="ccd8e-593">Vyberte **OK**, chcete-li zavřít dialogové okno **Skupina šablon popisku vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="ccd8e-594">Vytvořte druhou šablonu popisku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-595">**Název šablony štítku:** *Štítky palet*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="ccd8e-596">**Popis:** *Štítky palet*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="ccd8e-597">**Kód kroku vlny:** *Paleta*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="ccd8e-598">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="ccd8e-599">Na záložce s náhledem **Obecné** v poli **Typ popisků vlny** vyberte hodnotu, např. *Paleta*.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="ccd8e-600">Na pevné záložce **Podrobnosti o šabloně vlnového štítku** přidejte řádek, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-601">**ID rozložení štítku:** *Paleta*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="ccd8e-602">**Název tiskárny:** Vyberte vhodnou tiskárnu ZPL.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="ccd8e-603">**Spustit dotaz:** *Ano* (Toto nastavení je volitelné, ale pro optimální výkon se doporučuje.)</span><span class="sxs-lookup"><span data-stu-id="ccd8e-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="ccd8e-604">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="ccd8e-605">Volitelné: Pokud nastavujete design štítků specifických pro zákazníka, musíte vytvořit dotaz, abyste našli účet zákazníka.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="ccd8e-606">Na pevné záložce **Podrobnosti o šabloně vlnového štítku** vyberte **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="ccd8e-607">Pak v dialogovém okně Editor dotazů na kartě **Oblast** přidejte řádek, který má nasledující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-608">**Tabulka:** *Dodávky*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="ccd8e-609">**Odvozená tabulka:** *Dodávky*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="ccd8e-610">**Pole:** *Číslo účtu*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="ccd8e-611">**Kritéria:** Zadejte příslušné číslo zákaznického účtu.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="ccd8e-612">Po dokončení vyberte **OK** a zavřete dialogové okno editoru dotazů.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="ccd8e-613">V podokně Akce zvolte **Upravit dotaz** a otevřete dialogové okno editor dotazů pro celou šablonu štítku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="ccd8e-614">V dialogovém okně Editor dotazů na kartě **Třídění** přidejte řádek, který má nasledující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-615">**Tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="ccd8e-616">**Odvozená tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="ccd8e-617">**Pole:** *ID referenčního nákladového řádku (ID záznamu)*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="ccd8e-618">**Směr hledání:** *Vzestupně*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="ccd8e-619">Přidejte druhý řádek, který má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-620">**Tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="ccd8e-621">**Odvozená tabulka:** *Řádky práce*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="ccd8e-622">**Pole:** *ID dodávky*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="ccd8e-623">**Směr hledání:** *Vzestupně*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="ccd8e-624">Vyberte **OK** a dialogové okno editor dotazu zavřete.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="ccd8e-625">Okno se zprávou vás vyzve k potvrzení operace resetování seskupení.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="ccd8e-626">Pokračujte výběrem tlačítka **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="ccd8e-627">V podokně Akce vyberte možnost **Skupina šablon úrovně vlny**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="ccd8e-628">V dialogovém okně **Skupina šablon popisků vlny** pro řádek, kde je pole **Název referenčního pole** nastaveno na *ID zásilky*, nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="ccd8e-629">**Tisk štítku přerušení:** Zaškrtněte toto políčko.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="ccd8e-630">**ID rozložení štítku:** Vyberte štítek přerušení.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="ccd8e-631">(Například vyberte štítek *Přerušení*, který jste vytvořili dříve v tomto scénáři.)</span><span class="sxs-lookup"><span data-stu-id="ccd8e-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="ccd8e-632">**Název tiskárny:** Vyberte tiskárnu pro štítek přerušení.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="ccd8e-633">(Obvykle byste za účelem rozdělení rolí štítků měli vybrat stejnou tiskárnu, která je vybrána na pevné záložce **Podrobnosti o šabloně vlnového štítku**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="ccd8e-634">Jsou však možné i jiné scénáře.)</span><span class="sxs-lookup"><span data-stu-id="ccd8e-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="ccd8e-635">Pro řádek, kde je pole **Název referenčního pole** nastaveno na *ID referenčního zatížení*, zaškrtněte **ID sestavení štítku**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-635">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ccd8e-636">Toto nastavení vytvoří jednu sekvenci štítků („Karton 1 z X“) na řádek zatížení po celé vlně, bez ohledu na nastavení pracovní skupiny.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="ccd8e-637">Tuto sekvenci štítků lze vytisknout na rozvržení štítků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="ccd8e-638">Štítky pro různé zásilky budou navíc odděleny vybraným štítkem přerušení.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="ccd8e-639">Konfigurace rozšíření posloupnosti čísel</span><span class="sxs-lookup"><span data-stu-id="ccd8e-639">Configure number sequence extensions</span></span>

<span data-ttu-id="ccd8e-640">Rozšíření číselných sekvencí řídí dodržování specifických číselných sekvencí GS1.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="ccd8e-641">Tato konfigurace je pro aktuální scénář volitelná.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="ccd8e-642">Další informace a pokyny k konfiguraci najdete v části [Konfigurovat rozšíření posloupnosti čísel](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="ccd8e-643">Vytvořte prodejní objednávku a uvolněte ji do skladu</span><span class="sxs-lookup"><span data-stu-id="ccd8e-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="ccd8e-644">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="ccd8e-645">Vytvořte prodejní objednávku, která má následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="ccd8e-646">**Účet zákazníka:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="ccd8e-647">**Sklad:** *62*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="ccd8e-648">Přidejte dva řádky prodejní objednávky:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="ccd8e-649">Řádek prodejní objednávky 1:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-649">Sales order line 1:</span></span>

        - <span data-ttu-id="ccd8e-650">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="ccd8e-651">**Množství:** *9024*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="ccd8e-652">**Jednotka:** *ea* (9024 ea = 376 Box = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="ccd8e-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="ccd8e-653">Řádek prodejní objednávky 2:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-653">Sales order line 2:</span></span>

        - <span data-ttu-id="ccd8e-654">**Číslo položky:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="ccd8e-655">**Množství:** *9016*</span><span class="sxs-lookup"><span data-stu-id="ccd8e-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="ccd8e-656">**Jednotka:** *ea* (9016 ea = 322 Box = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="ccd8e-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="ccd8e-657">Položky a množství, které jsou zde uvedeny, jsou pouze příklady.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="ccd8e-658">Musí používat skupinu sekvencí jednotek, kterou jste definovali dříve, vhodné převody jednotek *ea* na *Box* na *PL* musí být pro ně definovány a musí mít zásoby ve skladu *62*.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="ccd8e-659">Další informace viz [Měrná jednotka a politika skladování](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="ccd8e-660">Vyberte řádek prodejní objednávky 1.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-660">Select sales order line 1.</span></span> <span data-ttu-id="ccd8e-661">Pak v sekci **Řádek prodejní objednávky** v nabídce **Zásoby** vyberte možnost **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="ccd8e-662">Na stránce **Rezervace** vyberte v podokně Akce možnost **Rezervovat šarži** a zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-662">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="ccd8e-663">Opakujte kroky 4 a 5 pro řádek 2 prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="ccd8e-664">V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="ccd8e-665">Dojde k následujícím událostem:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-665">The following events occur:</span></span> 

    - <span data-ttu-id="ccd8e-666">Systém zpracovává vytvořenou zásilku pomocí šablony, která zahrnuje krok tisku štítků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="ccd8e-667">Rozvržení štítků se použije k definování formátu štítků a výsledkem bude štítek, který se vytiskne na tiskárně vybrané v šabloně štítků.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="ccd8e-668">Štítky vlny se generují a tisknou.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="ccd8e-669">Počet štítků se bude rovnat počtu kartonů (v tomto příkladu 376 štítků pro řádek 1, 322 štítků krabic pro řádek 2, 47 štítků palet pro řádek 1, 47 štítků PL pro řádek 2 a dva štítky přerušení, které mají ID zásilky).</span><span class="sxs-lookup"><span data-stu-id="ccd8e-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="ccd8e-670">Pro zásilky je vygenerován nový přepravní doklad.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="ccd8e-671">Pokud jste nakonfigurovali rozšíření číselných sekvencí, budou ID popisků vlny sledovat formát čísla **SSCC-18**.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="ccd8e-672">Štítky vln můžete zobrazit a znovu vytisknout z následujících stránek:</span><span class="sxs-lookup"><span data-stu-id="ccd8e-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="ccd8e-673">Všechny zásilky \> Podrobnosti o zásilce</span><span class="sxs-lookup"><span data-stu-id="ccd8e-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="ccd8e-674">Všechny náklady \> Načíst podrobnosti</span><span class="sxs-lookup"><span data-stu-id="ccd8e-674">All loads \> Load details</span></span>
- <span data-ttu-id="ccd8e-675">Všechny vlny</span><span class="sxs-lookup"><span data-stu-id="ccd8e-675">All waves</span></span>
- <span data-ttu-id="ccd8e-676">Štítky vlny</span><span class="sxs-lookup"><span data-stu-id="ccd8e-676">Wave labels</span></span>
- <span data-ttu-id="ccd8e-677">Historie popisků vlny</span><span class="sxs-lookup"><span data-stu-id="ccd8e-677">Wave label history</span></span>

<span data-ttu-id="ccd8e-678">U většiny těchto stránek najdete příslušnou funkci výběrem **Vlnové štítky** ve skupině **Související informace** na kartě **Zásilky** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="ccd8e-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>
