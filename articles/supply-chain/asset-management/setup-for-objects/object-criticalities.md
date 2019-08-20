---
title: Typy kritičnosti majetku
description: Téma vysvětluje typy kritičnosti majetku v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 660038060826ade9301e50143e49b53ba3fcd3ab
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783129"
---
# <a name="asset-criticalities"></a><span data-ttu-id="86a73-103">Typy kritičnosti</span><span class="sxs-lookup"><span data-stu-id="86a73-103">Asset criticalities</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="86a73-104">Téma vysvětluje typy kritičnosti majetku v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="86a73-104">The topic explains asset criticality types in Asset Management.</span></span> <span data-ttu-id="86a73-105">Kritičnost majetku se vztahuje k majetku a je převedena na pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="86a73-105">Asset criticality is related to assets and is transferred to work orders.</span></span> <span data-ttu-id="86a73-106">Nelze ji změnit v pracovním příkazu.</span><span class="sxs-lookup"><span data-stu-id="86a73-106">It can't be changed on a work order.</span></span> <span data-ttu-id="86a73-107">Kritičnost majetku se používá k výpočtu kritičnosti pracovního příkazu během plánování pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="86a73-107">Asset criticality is used to calculate work order criticality during work order scheduling.</span></span> <span data-ttu-id="86a73-108">Jinými slovy, používá se k výpočtu míry, do jaké ovlivňuje práce údržby na majetku plán výroby a produktivitu vaší firmy.</span><span class="sxs-lookup"><span data-stu-id="86a73-108">In other words, it's used to calculate the extent to which a maintenance job on an asset affects the production schedule and productivity in your company.</span></span> <span data-ttu-id="86a73-109">Další informace o nastavení, které souvisí s výpočtem skóre hodnocení pro plánování pracovních příkazů, naleznete v tématu [Parametry Správy majetku](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="86a73-109">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span>

<span data-ttu-id="86a73-110">Chcete-li nastavit kritičnost, nejprve vytvořte typy kritičnosti, které by měly být použity v nastavení majetku.</span><span class="sxs-lookup"><span data-stu-id="86a73-110">To set up criticality, you first create the criticality types that should be used in the asset setup.</span></span> <span data-ttu-id="86a73-111">Potom nastavíte kritičnost majetku.</span><span class="sxs-lookup"><span data-stu-id="86a73-111">You then set up asset criticalities.</span></span>

## <a name="set-up-criticality-types"></a><span data-ttu-id="86a73-112">Nastavit typy kritičnosti</span><span class="sxs-lookup"><span data-stu-id="86a73-112">Set up criticality types</span></span>

1. <span data-ttu-id="86a73-113">Vyberte **Správa majetku**\>**Nastavení**\> **Majetek** \>**Typy kritičnosti**.</span><span class="sxs-lookup"><span data-stu-id="86a73-113">Select **Asset management** \> **Setup** \> **Assets** \> **Criticality types**.</span></span>
2. <span data-ttu-id="86a73-114">Zvolte **Nový** pro vytvoření záznamu.</span><span class="sxs-lookup"><span data-stu-id="86a73-114">Select **New** to create a record.</span></span>
3. <span data-ttu-id="86a73-115">Do pole **Kritičnost** zadejte číslo označující kritičnost.</span><span class="sxs-lookup"><span data-stu-id="86a73-115">In the **Criticality** field, enter a number that indicates the criticality.</span></span>
4. <span data-ttu-id="86a73-116">V poli **Název** zadejte název typu kritičnosti.</span><span class="sxs-lookup"><span data-stu-id="86a73-116">In the **Name** field, enter a name for the criticality type.</span></span>
5. <span data-ttu-id="86a73-117">Do pole **Faktor** zadejte faktor.</span><span class="sxs-lookup"><span data-stu-id="86a73-117">In the **Factor** field, enter a factor.</span></span> <span data-ttu-id="86a73-118">Tento faktor se používá při výpočtu plánování pracovních příkazů k určení záznamu kritičnosti, který by měl být použit.</span><span class="sxs-lookup"><span data-stu-id="86a73-118">This factor is used during the calculation of work order scheduling to determine the criticality record that should be used.</span></span> <span data-ttu-id="86a73-119">(Záznam s nejvyšším faktorem je vždy použit.) Toto nastavení je důležité, pokud, jak je znázorněno na následujícím obrázku, jsou vytvořeny řádky kritičnosti, které mají stejnou hodnotu kritičnosti.</span><span class="sxs-lookup"><span data-stu-id="86a73-119">(The record that has the highest factor is always used.) This setting is relevant if, as shown in the following illustration, criticality lines are created that have the same criticality value.</span></span>

    ![Obrázek č. 1](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a><span data-ttu-id="86a73-121">Nastavení kritičnosti majetku</span><span class="sxs-lookup"><span data-stu-id="86a73-121">Set up asset criticalities</span></span>

1. <span data-ttu-id="86a73-122">Vyberte **Správa majetku** \> **Nastavení** \> **Kritičnost majetku**.</span><span class="sxs-lookup"><span data-stu-id="86a73-122">Select **Asset management** \> **Setup** \> **Asset criticalities**.</span></span>
2. <span data-ttu-id="86a73-123">Zvolte **Nový** pro vytvoření záznamu.</span><span class="sxs-lookup"><span data-stu-id="86a73-123">Select **New** to create a record.</span></span>
3. <span data-ttu-id="86a73-124">V závislosti na požadované úrovni podrobností o majetku proveďte příslušné výběry v polích **Funkční umístění**, **Typ majetku**, **Výrobce**, **Model**, **Majetek**, **Kategorie typu práce**, **Typ práce**, **Varianta typu práce** a **Požadavek na práci**.</span><span class="sxs-lookup"><span data-stu-id="86a73-124">Depending on the required level of detail for asset criticality, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="86a73-125">Pokud je vybrána kritičnost majetku, projde Správa majetku všemi záznamy o kritičnosti majetku, aby mohla zkontrolovat možnou shodu.</span><span class="sxs-lookup"><span data-stu-id="86a73-125">When an asset criticality is selected, Asset Management goes through all asset criticality records to check for a possible match.</span></span> <span data-ttu-id="86a73-126">Vždy zkontroluje nejdříve nejkonkrétnější kombinaci.</span><span class="sxs-lookup"><span data-stu-id="86a73-126">It always checks the most specific combination first.</span></span> <span data-ttu-id="86a73-127">Jinými slovy, Správa majetku nejprve zkontroluje **Požadavek na práci**.</span><span class="sxs-lookup"><span data-stu-id="86a73-127">In other words, Asset Management first checks **Job requirement**.</span></span> <span data-ttu-id="86a73-128">Není-li nalezena shoda, kontroluje **Varianta typu práce**.</span><span class="sxs-lookup"><span data-stu-id="86a73-128">If no match is found, it checks **Job type variant**.</span></span> <span data-ttu-id="86a73-129">Není-li nalezena shoda, kontroluje **Typ práce** a tak dále.</span><span class="sxs-lookup"><span data-stu-id="86a73-129">If no match is found, it checks **Job type**, and so on.</span></span> <span data-ttu-id="86a73-130">Jak vidíte v rozvržení stránky, toto chování znamená, že pro nalezení nejspecifičtější kombinace zkontroluje Správa majetku každý záznam zprava doleva pro nalezení shody.</span><span class="sxs-lookup"><span data-stu-id="86a73-130">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="86a73-131">Není-li nalezena shoda, použije se "výchozí" záznam, který nemá žádné výběry.</span><span class="sxs-lookup"><span data-stu-id="86a73-131">If no match is found, the "default" record that has no selections is used.</span></span>

4. <span data-ttu-id="86a73-132">V poli **Kritičnost** vyberte jednu z hodnot kritičnosti, které jste vytvořili v předchozích krocích.</span><span class="sxs-lookup"><span data-stu-id="86a73-132">In the **Criticality** field, select one of the criticality values that you created in the previous procedure.</span></span>

### <a name="notes-about-criticality-setup"></a><span data-ttu-id="86a73-133">Poznámky o nastavení kritičnosti</span><span class="sxs-lookup"><span data-stu-id="86a73-133">Notes about criticality setup</span></span>

- <span data-ttu-id="86a73-134">Změníte-li v tomto nastavení kritičnost majetku poté, co jste jej již použili v pracovním příkazu, nebude tato kritičnost v pracovním příkazu odpovídajícím způsobem aktualizována.</span><span class="sxs-lookup"><span data-stu-id="86a73-134">If you change an asset criticality in this setup after you've already used it on a work order, the criticality on the work order isn't updated accordingly.</span></span>
- <span data-ttu-id="86a73-135">Kritičnost na pracovním příkazu je přepočítána pokaždé, když je v pracovním příkazu přidán nebo odstraněn řádek.</span><span class="sxs-lookup"><span data-stu-id="86a73-135">The criticality on a work order is recalculated every time that a work order line is added to or deleted from the work order.</span></span>
- <span data-ttu-id="86a73-136">Pokud pracovní příkaz obsahuje několik prací pracovního příkazu, v pracovním příkazu je vždy použita nejvyšší kritičnost podle pole **Faktor** na stránce **Typy kritičnosti**.</span><span class="sxs-lookup"><span data-stu-id="86a73-136">If a work order contains several work order jobs, the highest criticality, according to the **Factor** field on the **Criticality types** page, is always used on the work order.</span></span>
- <span data-ttu-id="86a73-137">Obecně platí, že kritičnost majetku se může v průběhu období změnit.</span><span class="sxs-lookup"><span data-stu-id="86a73-137">Generally, asset criticality can change over a period.</span></span> <span data-ttu-id="86a73-138">Kritičnost může být ovlivněna nákupem nového vybavení, rekonstrukcí a tak dále.</span><span class="sxs-lookup"><span data-stu-id="86a73-138">Criticality can be affected by the purchase of new equipment, refurbishments, and so on.</span></span> <span data-ttu-id="86a73-139">Zvažte možnost přehodnocením kritičnosti svého majetku v pravidelných intervalech (například jednou za rok nebo každý druhý rok), abyste zajistili, že se vaše definice kritičnosti shodují s aktuálním nastavením výroby.</span><span class="sxs-lookup"><span data-stu-id="86a73-139">Consider reevaluating your asset criticalities at regular intervals (for example, once per year or every other year) to make sure that your criticality definitions match your current production setup.</span></span>
