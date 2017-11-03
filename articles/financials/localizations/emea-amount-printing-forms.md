---
title: "Aktualizovat zobrazení částek v sestavách a dokumentech"
description: "Toto téma obsahuje informace o tom, jak aktualizovat zobrazení částek v sestavách a jiných dokumentech pro Estonsko, Lotyšsko, Litvu, Polsko, Českou republiku, Maďarsko a Rusko."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 264254
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a9e63af61b42ef3f5ef1d05a659cbec572e04a4f
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a><span data-ttu-id="073af-103">Aktualizovat zobrazení částek v sestavách a dokumentech</span><span class="sxs-lookup"><span data-stu-id="073af-103">Update how amounts are displayed on reports and documents</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="073af-104">Toto téma obsahuje informace o tom, jak aktualizovat zobrazení částek v sestavách a jiných dokumentech pro Estonsko, Lotyšsko, Litvu, Polsko, Českou republiku, Maďarsko a Rusko.</span><span class="sxs-lookup"><span data-stu-id="073af-104">This topic provides information about how to update how amounts are displayed on reports and other documents for Estonia, Latvia, Lithuania, Poland, Czech Republic, Hungary, and Russia.</span></span>

<span data-ttu-id="073af-105">Pro právnické osoby v Estonsku, Lotyšsku, Litvě, Polsku, Maďarsku, České republice a Rusku můžete nastavit úplné názvy nebo zkrácené názvy pro měnové jednotky a podjednotky.</span><span class="sxs-lookup"><span data-stu-id="073af-105">For legal entities in Estonia, Latvia, Lithuania, Poland, Czech Republic, Hungary, and Russia, you can set up full names and short names for currency units and subunits.</span></span> <span data-ttu-id="073af-106">Tyto názvy slouží k transformaci zastoupení částky na dokladech a sestavách.</span><span class="sxs-lookup"><span data-stu-id="073af-106">These names can be used to transform how amounts are represented on documents and reports.</span></span> <span data-ttu-id="073af-107">Příklad: částka **LTL 100,20** může být zobrazena jako **100 Litas 20 Centas**.</span><span class="sxs-lookup"><span data-stu-id="073af-107">For example: The amount **LTL 100.20** can be displayed as **100 Litas 20 Centas**.</span></span>

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a><span data-ttu-id="073af-108">Nastavení úplného a krátkého názvu pro měnové jednotky a podjednotky</span><span class="sxs-lookup"><span data-stu-id="073af-108">Set up full and short names for currency units and subunits</span></span>
<span data-ttu-id="073af-109">Pro nastavení úplného a krátkého názvu měnových jednotek a podjednotek pro daný jazyk proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="073af-109">To set up full and short names for currency units and subunits for a language, complete the following steps:</span></span>

1.  <span data-ttu-id="073af-110">Otevřete stránku **Měny**.</span><span class="sxs-lookup"><span data-stu-id="073af-110">Open the **Currencies** page.</span></span>
2.  <span data-ttu-id="073af-111">Vyberte měnu.</span><span class="sxs-lookup"><span data-stu-id="073af-111">Select a currency.</span></span>
3.  <span data-ttu-id="073af-112">V podokně akcí klikněte na možnost **Kolísání**.</span><span class="sxs-lookup"><span data-stu-id="073af-112">On the Action Pane, click **Declension**.</span></span>
4.  <span data-ttu-id="073af-113">Úplný název a krátký název pro jazyk přidáte kliknutím na tlačítko **Nová** a vyplněním následujících polí.</span><span class="sxs-lookup"><span data-stu-id="073af-113">To add full name and short name for a language, click **New** and complete the following fields.</span></span>
    |                                                           |                                                                                                                                                                                                                    |
    |-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="073af-114">**Pole**</span><span class="sxs-lookup"><span data-stu-id="073af-114">**Field**</span></span>                                                 | <span data-ttu-id="073af-115">**Popis**</span><span class="sxs-lookup"><span data-stu-id="073af-115">**Description**</span></span>                                                                                                                                                                                                    |
    | <span data-ttu-id="073af-116">**Jazyk**</span><span class="sxs-lookup"><span data-stu-id="073af-116">**Language**</span></span>                                              | <span data-ttu-id="073af-117">Vyberte jazyk pro aktuální text.</span><span class="sxs-lookup"><span data-stu-id="073af-117">Select the language for the current text.</span></span>                                                                                                                                                                          |
    | <span data-ttu-id="073af-118">**1. pád jednotného čísla (název skupiny polí jednotek)**</span><span class="sxs-lookup"><span data-stu-id="073af-118">**Singular nominative (Name of units field group)**</span></span>       | <span data-ttu-id="073af-119">Zadejte jednotné číslo názvu měny.</span><span class="sxs-lookup"><span data-stu-id="073af-119">Enter the singular form of the currency.</span></span> <span data-ttu-id="073af-120">Například jednotné číslo slova Litas je Litas.</span><span class="sxs-lookup"><span data-stu-id="073af-120">For example, the singular form of Litas is Litas.</span></span>                                                                                                                         |
    | <span data-ttu-id="073af-121">**1. pád množného čísla (název skupiny polí jednotek)**</span><span class="sxs-lookup"><span data-stu-id="073af-121">**Plural nominative (Name of units field group)**</span></span>         | <span data-ttu-id="073af-122">Zadejte množné číslo názvu měny.</span><span class="sxs-lookup"><span data-stu-id="073af-122">Enter the plural form of the currency.</span></span> <span data-ttu-id="073af-123">Například zadejte Litai.</span><span class="sxs-lookup"><span data-stu-id="073af-123">For example, enter Litai.</span></span> <span data-ttu-id="073af-124">**Poznámka:**: pole **2. pád jednotného čísla** a **2. pád množného čísla** jsou k dispozici na základě jazyka, který jste vybrali v poli **Jazyk**.</span><span class="sxs-lookup"><span data-stu-id="073af-124">**Note**: The **Singular genitive** and **Plural genitive** fields are available based on the language that you select in the **Language** field.</span></span> |
    | <span data-ttu-id="073af-125">**Pole 1. pád jednotného čísla (název skupiny polí podjednotek)**</span><span class="sxs-lookup"><span data-stu-id="073af-125">**Singular nominative field (Name of parts field group)**</span></span> | <span data-ttu-id="073af-126">Zadejte jednotné číslo podjednotky měny.</span><span class="sxs-lookup"><span data-stu-id="073af-126">Enter the singular form of the subunit of the currency.</span></span>                                                                                                                                                            |
    | <span data-ttu-id="073af-127">**1. pád množného čísla (název skupiny polí podjednotek)**</span><span class="sxs-lookup"><span data-stu-id="073af-127">**Plural nominative (Name of parts field group)**</span></span>         | <span data-ttu-id="073af-128">Zadejte množné číslo podjednotky měny.</span><span class="sxs-lookup"><span data-stu-id="073af-128">Enter the plural form of the subunit of the currency.</span></span>                                                                                                                                                              |
    | <span data-ttu-id="073af-129">**Krátký název jednotek (krátký název skupiny polí)**</span><span class="sxs-lookup"><span data-stu-id="073af-129">**Shortcut name of units (Short name field group)**</span></span>       | <span data-ttu-id="073af-130">Zadejte ISO kód pro identifikaci měny.</span><span class="sxs-lookup"><span data-stu-id="073af-130">Enter the ISO code to identify the currency.</span></span> <span data-ttu-id="073af-131">Například zadejte LTL k identifikaci Litas.</span><span class="sxs-lookup"><span data-stu-id="073af-131">For example, enter LTL to identify Litas.</span></span>                                                                                                                             |
    | <span data-ttu-id="073af-132">**Krátký název podjednotek (skupina polí krátkého názvu)**</span><span class="sxs-lookup"><span data-stu-id="073af-132">**Shortcut name for parts (Short name field group)**</span></span>      | <span data-ttu-id="073af-133">Zadejte název podjednotky měny.</span><span class="sxs-lookup"><span data-stu-id="073af-133">Enter the denomination of the currency subunit.</span></span> <span data-ttu-id="073af-134">Například zadejte Centas.</span><span class="sxs-lookup"><span data-stu-id="073af-134">For example, enter Centas.</span></span>                                                                                                                                         |
    | <span data-ttu-id="073af-135">**Spojka 'a' mezi jednotkami a podjednotkami**</span><span class="sxs-lookup"><span data-stu-id="073af-135">**Conjunction 'and' between units and parts**</span></span>             | <span data-ttu-id="073af-136">Zvolte tuto možnost, chcete-li vytisknout spojku „a“ mezi jednotkami a podjednotkami.</span><span class="sxs-lookup"><span data-stu-id="073af-136">Select to print the conjunction “and” between the currency units and unit parts.</span></span> <span data-ttu-id="073af-137">Například částka LTL 100,20 se zobrazí na fakturách nebo v sestavách jako 100 litas and 20 centas.</span><span class="sxs-lookup"><span data-stu-id="073af-137">For example, on invoices or reports, the amount for LTL 100.20 will be displayed as 100 Litas and 20 Centas.</span></span>                      |

5.  <span data-ttu-id="073af-138">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="073af-138">Click **Save**.</span></span>





