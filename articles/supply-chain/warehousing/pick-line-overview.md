---
title: Nastavte položku nabídky mobilního zařízení a poskytněte přehled řádků výdeje
description: Toto téma vysvětluje, jak definovat, kdy se seznam všech řádků práce zobrazí pracovníkům skladu, kteří zpracovávají skladovou práci na mobilním zařízení. Tato funkce může být užitečná pro pracovníky skladu, kteří často vyžadují přehled řádků výdeje v pracovním příkazu, aby mohli optimalizovat sekvenci výdeje.
author: MarkusFogelberg
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6eaba6da313f398c8d30f9a26c959ee971812e21
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818865"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a><span data-ttu-id="a0367-104">Nastavte položku nabídky mobilního zařízení a poskytněte přehled řádků výdeje</span><span class="sxs-lookup"><span data-stu-id="a0367-104">Set up a mobile device menu item to provide a pick line overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0367-105">Toto téma vysvětluje, jak konfigurovat možnosti, které souvisejí s přehledem řádku výdeje pro položky nabídky mobilního zařízení, které se používají ke zpracování práce výdeje.</span><span class="sxs-lookup"><span data-stu-id="a0367-105">This topic explains how to configure options that are related to the pick line overview for mobile device menu items that are used to process picking work.</span></span> <span data-ttu-id="a0367-106">Přehled řádků výdeje umožňuje pracovníkům skladu zobrazit a vybrat ze seznamu všech řádků práce, které souvisejí s jejich aktuálním úkolem.</span><span class="sxs-lookup"><span data-stu-id="a0367-106">The pick line overview lets warehouse workers view and select from a list of all the work lines that are related to their current task.</span></span> <span data-ttu-id="a0367-107">Tato schopnost může pracovníkům pomoci optimalizovat jejich sekvenci vychystávání.</span><span class="sxs-lookup"><span data-stu-id="a0367-107">This capability can help workers optimize their picking sequence.</span></span> <span data-ttu-id="a0367-108">Tato funkce poskytuje možnosti, které nahrazují standardní tlačítko **Přeskočit**, které umožňuje pracovníkům procházet řádky jeden po druhém v pevném pořadí.</span><span class="sxs-lookup"><span data-stu-id="a0367-108">The feature provides options that replace the standard **Skip** button that lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="a0367-109">(Možnost použít toto tlačítko je však stále k dispozici.)</span><span class="sxs-lookup"><span data-stu-id="a0367-109">(However, the option to use that button is still available.)</span></span>

<span data-ttu-id="a0367-110">Správci mohou nakonfigurovat každou položku nabídky samostatně, aby určili, jak, kdy a kde mobilní aplikace Řízení skladu zobrazuje přehled řádků výdeje.</span><span class="sxs-lookup"><span data-stu-id="a0367-110">Admins can configure each menu item individually to control how, when, and where the Warehouse Management mobile app presents the pick line overview.</span></span>

## <a name="turn-on-the-work-pick-line-overview-feature"></a><span data-ttu-id="a0367-111">Zapnutí funkce přehledu řádků práce výdeje</span><span class="sxs-lookup"><span data-stu-id="a0367-111">Turn on the Work pick line overview feature</span></span>

<span data-ttu-id="a0367-112">Než můžete použít tuto funkci, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="a0367-112">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="a0367-113">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba.</span><span class="sxs-lookup"><span data-stu-id="a0367-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="a0367-114">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="a0367-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a0367-115">**Modul:** _Řízení skladu_</span><span class="sxs-lookup"><span data-stu-id="a0367-115">**Module:** _Warehouse management_</span></span>
- <span data-ttu-id="a0367-116">**Název funkce:** _Přehled řádků práce výdeje_</span><span class="sxs-lookup"><span data-stu-id="a0367-116">**Feature name:** _Work pick line overview_</span></span>

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a><span data-ttu-id="a0367-117">Nakonfigurujte položky nabídky tak, aby zobrazovaly seznam všech pracovních řádků</span><span class="sxs-lookup"><span data-stu-id="a0367-117">Configure menu items to show a list of all work lines</span></span>

<span data-ttu-id="a0367-118">Chcete-li nastavit položku nabídky mobilního zařízení a poskytnout tak přehled řádků výdeje, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="a0367-118">To set up a mobile device menu item to provide a pick line overview, follow these steps.</span></span>

1. <span data-ttu-id="a0367-119">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="a0367-119">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="a0367-120">Vyberte nebo vytvořte položku nabídky, která souvisí s výběrem práce, a nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a0367-120">Select or create a menu item that is related to picking work, and set the following values:</span></span>

    - <span data-ttu-id="a0367-121">**Režim:** *Práce*</span><span class="sxs-lookup"><span data-stu-id="a0367-121">**Mode:** *Work*</span></span>
    - <span data-ttu-id="a0367-122">**Použít existující práci:** - *Ano*</span><span class="sxs-lookup"><span data-stu-id="a0367-122">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="a0367-123">**Řídí:** *Uživatel* nebo *Systém*</span><span class="sxs-lookup"><span data-stu-id="a0367-123">**Directed by:** *User directed* or *System directed*</span></span>

    <span data-ttu-id="a0367-124">Další informace o tom, jak vytvořit položky nabídky a použít různá nastavení, která jsou k dispozici na stránce **Položky nabídky mobilního zařízení**, přečtěte si [Nastavte mobilní zařízení pro práci ve skladu](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="a0367-124">For more information about how to create menu items and use the various settings that are available on the **Mobile device menu items** page, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

1. <span data-ttu-id="a0367-125">Na pevné záložce **Obecné** nakonfigurujte funkci nastavením pole **Zobrazit seznam řádků práce** na jednu z následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="a0367-125">On the **General** FastTab, configure the feature by setting the **Show work line list** field to one of the following values:</span></span>

    - <span data-ttu-id="a0367-126">**Zobrazit pouze na vyžádání** - Pracovníci se mohou rozhodnout zobrazit seznam výběrových řádků výběrem tlačítka **Přeskočit na** v mobilní aplikaci Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="a0367-126">**Show only upon request** – Workers can choose to view the pick line list by selecting the **Skip to** button in the Warehouse Management mobile app.</span></span>
    - <span data-ttu-id="a0367-127">**Zobrazit na začátku každého výdeje** - Pracovníci vidí seznam pokaždé, když zahájí nebo dokončí výdej.</span><span class="sxs-lookup"><span data-stu-id="a0367-127">**Show at the start of every pick** – Workers see the list every time that they start or finish a pick line.</span></span> <span data-ttu-id="a0367-128">Seznam mohou také znovu zobrazit výběrem tlačítka **Přeskočit na** v mobilní aplikaci Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="a0367-128">They can also view the list again by selecting the **Skip to** button in the Warehouse Management mobile app.</span></span>
    - <span data-ttu-id="a0367-129">**Zobrazit pouze na začátku prvního výdeje** - Pracovníci uvidí seznam pokaždé, když zahájí novou práci výdeje, ale ne po každém řádku.</span><span class="sxs-lookup"><span data-stu-id="a0367-129">**Show at the start of the first pick only** – Workers see the list every time that they start new picking work, but not after each line.</span></span> <span data-ttu-id="a0367-130">Seznam mohou také znovu zobrazit výběrem tlačítka **Přeskočit na** v mobilní aplikaci Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="a0367-130">They can also view the list again by selecting the **Skip to** button in the Warehouse Management mobile app.</span></span>
    - <span data-ttu-id="a0367-131">**Nikdy neukazovat** - Standardní tlačítko **Přeskočit** se zobrazí v mobilní aplikaci Řízení skladu a zobrazení seznamu pracovních řádků je vypnuto.</span><span class="sxs-lookup"><span data-stu-id="a0367-131">**Never show** – The standard **Skip** button appears in the Warehouse Management mobile app, and display of the work line list is turned off.</span></span> <span data-ttu-id="a0367-132">Tlačítko **Přeskočit** umožňuje pracovníkům procházet řádky jeden po druhém, v pevném pořadí.</span><span class="sxs-lookup"><span data-stu-id="a0367-132">The **Skip** button lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="a0367-133">Mohou také procházet seznamem tolikrát, kolikrát vyžadují, dokud nebudou zpracovány všechny řádky.</span><span class="sxs-lookup"><span data-stu-id="a0367-133">They can also cycle through the list as many times as they require, until all lines have been processed.</span></span>

1. <span data-ttu-id="a0367-134">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a0367-134">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="a0367-135">Pokud nastavíte pole **Zobrazit seznam řádků práce** na libovolnou hodnotu kromě *Nikdy neukazovat*, tlačítko **Seznam polí** v podokně akcí bude k dispozici.</span><span class="sxs-lookup"><span data-stu-id="a0367-135">If you set the **Show work line list** field to any value except *Never show*, the **Field list** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="a0367-136">V podokně akcí vyberte možnost **Seznam polí**.</span><span class="sxs-lookup"><span data-stu-id="a0367-136">On the Action Pane, select **Field list**.</span></span>
1. <span data-ttu-id="a0367-137">Na stránce **Seznam polí** nakonfigurujte informace, které mobilní aplikace Řízení skladu zobrazuje pro každý řádek v seznamu.</span><span class="sxs-lookup"><span data-stu-id="a0367-137">On the **Field list** page, configure the information that the Warehouse Management mobile app shows for each line in the list.</span></span>

    - <span data-ttu-id="a0367-138">Pole **Primární ovládací prvek** je vždy nastaveno na *LineNum*.</span><span class="sxs-lookup"><span data-stu-id="a0367-138">The **Primary control** field is always set to *LineNum*.</span></span> <span data-ttu-id="a0367-139">Každý řádek v seznamu proto začíná číslem řádku.</span><span class="sxs-lookup"><span data-stu-id="a0367-139">Therefore, each row in the list begins with a line number.</span></span>
    - <span data-ttu-id="a0367-140">Použijte zbývající pole **Zobrazit pole** pro přidání až sedmi dalších polí zobrazení, jak požadujete.</span><span class="sxs-lookup"><span data-stu-id="a0367-140">Use the remaining **Display field** fields to add up to seven additional display fields, as you require.</span></span> <span data-ttu-id="a0367-141">V každém poli **Zobrazit pole** vyberte název pole řádku práce.</span><span class="sxs-lookup"><span data-stu-id="a0367-141">In each **Display field** field, select the name of a work line field.</span></span> <span data-ttu-id="a0367-142">Každý řádek poté zobrazí hodnotu pro toto pole.</span><span class="sxs-lookup"><span data-stu-id="a0367-142">Each line will then show a value for that field.</span></span> <span data-ttu-id="a0367-143">Hodnoty se zobrazí v pořadí, které zde vyberete.</span><span class="sxs-lookup"><span data-stu-id="a0367-143">The values will be shown in the order that you select here.</span></span> <span data-ttu-id="a0367-144">Můžete nachat některá z polí **Zobrazit pole** prázdná, pokud nevyžadujete všech sedm hodnot.</span><span class="sxs-lookup"><span data-stu-id="a0367-144">You can leave some of the **Display field** fields blank if you don't require all seven values.</span></span>

1. <span data-ttu-id="a0367-145">V podokně akcí vyberte **Uložit** a pak vyberte stránku **Seznam polí**.</span><span class="sxs-lookup"><span data-stu-id="a0367-145">On the Action Pane, select **Save**, and then close the **Field list** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]