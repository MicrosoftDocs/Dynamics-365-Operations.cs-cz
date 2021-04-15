---
title: Vytvoření dlouhodobého majetku
description: Toto téma vysvětluje, jak vytvořit nový záznam o dlouhodobém majetku na stránce se seznamem dlouhodobého majetku.
author: moaamer
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 770390092342e2db496dde850a75b2f7736bd4c0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817094"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="6fee3-103">Vytvoření dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="6fee3-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6fee3-104">Toto téma vysvětluje, jak vytvořit nový záznam o dlouhodobém majetku na stránce se seznamem **dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="6fee3-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="6fee3-105">Systém přiřadí číslo aktiva na základě číselné řady, která je přiřazena skupině dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="6fee3-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="6fee3-106">Pokud používáte šablonu dlouhodobého majetku k importu majetku prostřednictvím doplňku Microsoft Excel, nebo pokud použijete jinou úlohu importu, systém automaticky vytvoří záznamy dlouhodobého majetku a zvýší číslo aktiva.</span><span class="sxs-lookup"><span data-stu-id="6fee3-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="6fee3-107">Chcete-li ručně vytvořit záznam o majetku, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="6fee3-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="6fee3-108">Přejděte na **Podokno navigace \> Moduly \> Dlouhodobý majetek \> Dlouhodobý majetek \> Dlouhodobý majetek**.</span><span class="sxs-lookup"><span data-stu-id="6fee3-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="6fee3-109">V **podokně akcí** zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="6fee3-109">On the **Action pane**, select **New**.</span></span>
3. <span data-ttu-id="6fee3-110">Zadejte nebo vyberte hodnotu v poli **Skupina dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="6fee3-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="6fee3-111">Pole **Číslo** bude výchozí, pokud je povolena funkce **Automaticky číslovat dlouhodobý majetek** v možnostech **Parametry dlouhodobého majetku** a **Skupina dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="6fee3-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="6fee3-112">Pokud ne, je třeba zadat jednoznačné číslo k identifikaci dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="6fee3-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="6fee3-113">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="6fee3-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="6fee3-114">Zadejte další informace, které vaše firma potřebuje pro tento majetek.</span><span class="sxs-lookup"><span data-stu-id="6fee3-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="6fee3-115">V **podokně akcí** vyberte **Knihy**.</span><span class="sxs-lookup"><span data-stu-id="6fee3-115">On the **Action pane**, select **Books**.</span></span>
6. <span data-ttu-id="6fee3-116">Zadejte datum do pole **Datum pořízení**.</span><span class="sxs-lookup"><span data-stu-id="6fee3-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="6fee3-117">Zadejte číslo do pole **Pořizovací cena**.</span><span class="sxs-lookup"><span data-stu-id="6fee3-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="6fee3-118">Zadejte další informace, které vaše firma potřebuje pro tuto knihu.</span><span class="sxs-lookup"><span data-stu-id="6fee3-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="6fee3-119">Zadejte další informace, které vaše firma potřebuje pro zbývající knihy.</span><span class="sxs-lookup"><span data-stu-id="6fee3-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="6fee3-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6fee3-120">Close the page.</span></span>

<span data-ttu-id="6fee3-121">Dlouhodobý majetek můžete také importovat pomocí doplňku Excel nebo spuštěním úlohy importu z pracovního prostoru **Správa dat**.</span><span class="sxs-lookup"><span data-stu-id="6fee3-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="6fee3-122">Před spuštěním importu zadejte do šablony hodnoty pro požadovaná pole.</span><span class="sxs-lookup"><span data-stu-id="6fee3-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="6fee3-123">Pokud jste nedefinovali číslo dlouhodobého majetku v šabloně doplňku aplikace Excel nebo ve správě dat, systém vytvoří číslo dlouhodobého majetku pro každé importované aktivum a automaticky zvýší číselnou sekvenci pro každý.</span><span class="sxs-lookup"><span data-stu-id="6fee3-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="6fee3-124">Pokud však importujete majetek a v šabloně definujete čísla majetku, systém to automaticky **nezvýší** číselnou sekvenci.</span><span class="sxs-lookup"><span data-stu-id="6fee3-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="6fee3-125">V takovém případě bude muset správce ručně aktualizovat číselnou posloupnost.</span><span class="sxs-lookup"><span data-stu-id="6fee3-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="6fee3-126">Pokud jste definovali číslo dlouhodobého majetku v šabloně doplňku Excel, systém použije definované číslo dlouhodobého majetku a zvýší číselnou sekvenci.</span><span class="sxs-lookup"><span data-stu-id="6fee3-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="6fee3-127">Po zaúčtování odpisů budou pole **Uvedeno do užívání** a **Datum zahájení odpisu** uzamčena na stránce **Kniha**.</span><span class="sxs-lookup"><span data-stu-id="6fee3-127">After posting the depreciation, the **Placed in service** and **Depreciation run date** fields will be locked on the **Book** page.</span></span> <span data-ttu-id="6fee3-128">Ani jedno pole nebude aktualizováno z datové entity.</span><span class="sxs-lookup"><span data-stu-id="6fee3-128">Also, both neither field will be updated from the data entity.</span></span>

> [!WARNING]
> <span data-ttu-id="6fee3-129">Záznam dlouhodobého majetku nebude odstraněn, pokud byly transakce zaúčtovány do přidružené knihy nebo pokud je nově vytvořený dlouhodobý majetek zadán na řádku deníku, ale nebyl zaúčtován.</span><span class="sxs-lookup"><span data-stu-id="6fee3-129">The fixed asset record won't be deleted if transactions were posted to the associated book, or if the newly created fixed asset is entered on a journal line but not posted.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]