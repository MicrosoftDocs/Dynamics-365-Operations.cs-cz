---
title: Aktualizovat zobrazení částek v sestavách a dokumentech
description: Toto téma obsahuje informace o tom, jak aktualizovat zobrazení částek v sestavách a jiných dokumentech pro Estonsko, Lotyšsko, Litvu, Polsko, Českou republiku, Maďarsko a Rusko.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Currency
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 264254
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 61d3ebe7204a248b6d4287215fc9ad42e9d08b76
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "370112"
---
# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a><span data-ttu-id="3a6a0-103">Aktualizovat zobrazení částek v sestavách a dokumentech</span><span class="sxs-lookup"><span data-stu-id="3a6a0-103">Update how amounts are displayed on reports and documents</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a6a0-104">Toto téma obsahuje informace o tom, jak aktualizovat zobrazení částek v sestavách a jiných dokumentech pro Estonsko, Lotyšsko, Litvu, Polsko, Českou republiku, Maďarsko a Rusko.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-104">This topic provides information about how to update how amounts are displayed on reports and other documents for Estonia, Latvia, Lithuania, Poland, Czech Republic, Hungary, and Russia.</span></span>

<span data-ttu-id="3a6a0-105">Pro právnické osoby v Estonsku, Lotyšsku, Litvě, Polsku, Maďarsku, České republice a Rusku můžete nastavit úplné názvy nebo zkrácené názvy pro měnové jednotky a podjednotky.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-105">For legal entities in Estonia, Latvia, Lithuania, Poland, Czech Republic, Hungary, and Russia, you can set up full names and short names for currency units and subunits.</span></span> <span data-ttu-id="3a6a0-106">Tyto názvy slouží k transformaci zastoupení částky na dokladech a sestavách.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-106">These names can be used to transform how amounts are represented on documents and reports.</span></span> <span data-ttu-id="3a6a0-107">Příklad: částka **LTL 100,20** může být zobrazena jako **100 Litas 20 Centas**.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-107">For example: The amount **LTL 100.20** can be displayed as **100 Litas 20 Centas**.</span></span>

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a><span data-ttu-id="3a6a0-108">Nastavení úplného a krátkého názvu pro měnové jednotky a podjednotky</span><span class="sxs-lookup"><span data-stu-id="3a6a0-108">Set up full and short names for currency units and subunits</span></span>
<span data-ttu-id="3a6a0-109">Pro nastavení úplného a krátkého názvu měnových jednotek a podjednotek pro daný jazyk proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="3a6a0-109">To set up full and short names for currency units and subunits for a language, complete the following steps:</span></span>

1. <span data-ttu-id="3a6a0-110">Otevřete stránku **Měny**.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-110">Open the **Currencies** page.</span></span>
2. <span data-ttu-id="3a6a0-111">Vyberte měnu.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-111">Select a currency.</span></span>
3. <span data-ttu-id="3a6a0-112">V podokně akcí klikněte na možnost **Kolísání**.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-112">On the Action Pane, click **Declension**.</span></span>
4. <span data-ttu-id="3a6a0-113">Úplný název a krátký název pro jazyk přidáte kliknutím na tlačítko **Nová** a vyplněním následujících polí.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-113">To add full name and short name for a language, click **New** and complete the following fields.</span></span>

   |                                                                        |                                                                                                                                                                                                                                                                        |
   |------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |                         <span data-ttu-id="3a6a0-114"><strong>Pole</strong></span><span class="sxs-lookup"><span data-stu-id="3a6a0-114"><strong>Field</strong></span></span>                         |                                                                                                                      <span data-ttu-id="3a6a0-115"><strong>Popis</strong></span><span class="sxs-lookup"><span data-stu-id="3a6a0-115"><strong>Description</strong></span></span>                                                                                                                      |
   |                       <span data-ttu-id="3a6a0-116"><strong>Jazyk</strong></span><span class="sxs-lookup"><span data-stu-id="3a6a0-116"><strong>Language</strong></span></span>                        |                                                                                                               <span data-ttu-id="3a6a0-117">Vyberte jazyk pro aktuální text.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-117">Select the language for the current text.</span></span>                                                                                                                |
   |    <span data-ttu-id="3a6a0-118"><strong>1. pád jednotného čísla (název skupiny polí jednotek)</strong></span><span class="sxs-lookup"><span data-stu-id="3a6a0-118"><strong>Singular nominative (Name of units field group)</strong></span></span>    |                                                                                       <span data-ttu-id="3a6a0-119">Zadejte jednotné číslo názvu měny.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-119">Enter the singular form of the currency.</span></span> <span data-ttu-id="3a6a0-120">Například jednotné číslo slova Litas je Litas.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-120">For example, the singular form of Litas is Litas.</span></span>                                                                                       |
   |     <span data-ttu-id="3a6a0-121"><strong>1. pád množného čísla (název skupiny polí jednotek)</strong></span><span class="sxs-lookup"><span data-stu-id="3a6a0-121"><strong>Plural nominative (Name of units field group)</strong></span></span>     | <span data-ttu-id="3a6a0-122">Zadejte množné číslo názvu měny.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-122">Enter the plural form of the currency.</span></span> <span data-ttu-id="3a6a0-123">Například zadejte Litai.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-123">For example, enter Litai.</span></span> <span data-ttu-id="3a6a0-124"><strong>Poznámka:</strong>: pole <strong>2. pád jednotného čísla</strong> a <strong>2. pád množného čísla</strong> jsou k dispozici na základě jazyka, který jste vybrali v poli <strong>Jazyk</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-124"><strong>Note</strong>: The <strong>Singular genitive</strong> and <strong>Plural genitive</strong> fields are available based on the language that you select in the <strong>Language</strong> field.</span></span> |
   | <span data-ttu-id="3a6a0-125"><strong>Pole 1. pád jednotného čísla (název skupiny polí podjednotek)</strong></span><span class="sxs-lookup"><span data-stu-id="3a6a0-125"><strong>Singular nominative field (Name of parts field group)</strong></span></span> |                                                                                                        <span data-ttu-id="3a6a0-126">Zadejte jednotné číslo podjednotky měny.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-126">Enter the singular form of the subunit of the currency.</span></span>                                                                                                         |
   |     <span data-ttu-id="3a6a0-127"><strong>1. pád množného čísla (název skupiny polí podjednotek)</strong></span><span class="sxs-lookup"><span data-stu-id="3a6a0-127"><strong>Plural nominative (Name of parts field group)</strong></span></span>     |                                                                                                         <span data-ttu-id="3a6a0-128">Zadejte množné číslo podjednotky měny.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-128">Enter the plural form of the subunit of the currency.</span></span>                                                                                                          |
   |    <span data-ttu-id="3a6a0-129"><strong>Krátký název jednotek (krátký název skupiny polí)</strong></span><span class="sxs-lookup"><span data-stu-id="3a6a0-129"><strong>Shortcut name of units (Short name field group)</strong></span></span>    |                                                                                         <span data-ttu-id="3a6a0-130">Zadejte ISO kód pro identifikaci měny.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-130">Enter the ISO code to identify the currency.</span></span> <span data-ttu-id="3a6a0-131">Například zadejte LTL k identifikaci Litas.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-131">For example, enter LTL to identify Litas.</span></span>                                                                                         |
   |   <span data-ttu-id="3a6a0-132"><strong>Krátký název podjednotek (skupina polí krátkého názvu)</strong></span><span class="sxs-lookup"><span data-stu-id="3a6a0-132"><strong>Shortcut name for parts (Short name field group)</strong></span></span>    |                                                                                               <span data-ttu-id="3a6a0-133">Zadejte název podjednotky měny.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-133">Enter the denomination of the currency subunit.</span></span> <span data-ttu-id="3a6a0-134">Například zadejte Centas.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-134">For example, enter Centas.</span></span>                                                                                               |
   |       <span data-ttu-id="3a6a0-135"><strong>Spojka 'a' mezi jednotkami a podjednotkami</strong></span><span class="sxs-lookup"><span data-stu-id="3a6a0-135"><strong>Conjunction 'and' between units and parts</strong></span></span>       |                                     <span data-ttu-id="3a6a0-136">Zvolte tuto možnost, chcete-li vytisknout spojku „a“ mezi jednotkami a podjednotkami.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-136">Select to print the conjunction “and” between the currency units and unit parts.</span></span> <span data-ttu-id="3a6a0-137">Například částka LTL 100,20 se zobrazí na fakturách nebo v sestavách jako 100 litas and 20 centas.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-137">For example, on invoices or reports, the amount for LTL 100.20 will be displayed as 100 Litas and 20 Centas.</span></span>                                      |


5. <span data-ttu-id="3a6a0-138">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="3a6a0-138">Click **Save**.</span></span>




