---
title: Nastavení dodavatelů a bankovních účtů dodavatelů pro převody kreditu ve formátu ISO20022
description: Tento postup popisuje způsob nastavení informací o dodavateli a konkrétním bankovním účtu dodavatele požadovaných pro převedení kreditu SEPA nebo jakéhokoli jiného generování souboru pro platbu dodavatele podle normy ISO20022.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab8c52b9b457505c2cf2bfca46cb938e73c0142e
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848666"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="1a20a-103">Nastavení dodavatelů a bankovních účtů dodavatelů pro převody kreditu ve formátu ISO20022</span><span class="sxs-lookup"><span data-stu-id="1a20a-103">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1a20a-104">Tento postup popisuje způsob nastavení informací o dodavateli a konkrétním bankovním účtu dodavatele požadovaných pro převedení kreditu SEPA nebo jakéhokoli jiného generování souboru pro platbu dodavatele podle normy ISO20022.</span><span class="sxs-lookup"><span data-stu-id="1a20a-104">This procedure demonstrates how to set up the vendor and vendor specific bank account information required for ISO20022 Credit transfer or any other vendor payment file generation.</span></span> 

<span data-ttu-id="1a20a-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="1a20a-105">The demo data company used to create this procedure is DEMF.</span></span>
<span data-ttu-id="1a20a-106">Toto je čtvrtý z pěti úkolů, které společně popisují proces platby dodavatele pomocí konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="1a20a-106">This is the fourth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="1a20a-107">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="1a20a-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-bank-details"></a><span data-ttu-id="1a20a-108">Nastavení podrobností o bance</span><span class="sxs-lookup"><span data-stu-id="1a20a-108">Set up bank details</span></span>
1. <span data-ttu-id="1a20a-109">Přejděte do části Závazky > Dodavatelé > Všichni dodavatelé.</span><span class="sxs-lookup"><span data-stu-id="1a20a-109">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="1a20a-110">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="1a20a-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1a20a-111">V poli Účet dodavatele můžete například filtrovat pomocí hodnoty „DE-001“.</span><span class="sxs-lookup"><span data-stu-id="1a20a-111">For example, filter on the Vendor account field with a value of 'DE-001'.</span></span>
3. <span data-ttu-id="1a20a-112">Klepnutím na položku DE-001 zobrazíte podrobnosti o dodavateli.</span><span class="sxs-lookup"><span data-stu-id="1a20a-112">Click DE-001 to open vendor details.</span></span>
4. <span data-ttu-id="1a20a-113">V podokně akcí klikněte na možnost Dodavatel.</span><span class="sxs-lookup"><span data-stu-id="1a20a-113">On the Action Pane, click Vendor.</span></span>
5. <span data-ttu-id="1a20a-114">Klikněte na možnost Bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="1a20a-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="1a20a-115">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="1a20a-115">Click Edit.</span></span>
    * <span data-ttu-id="1a20a-116">Pokud není k dispozici žádný bankovní účet, musíte vytvořit nový.</span><span class="sxs-lookup"><span data-stu-id="1a20a-116">If there is no bank account available, you need to create a new one.</span></span>  
7. <span data-ttu-id="1a20a-117">V poli Kód SWIFT zadejte hodnotu COBADEFFXXX".</span><span class="sxs-lookup"><span data-stu-id="1a20a-117">In the SWIFT code field, type 'COBADEFFXXX'.</span></span>
8. <span data-ttu-id="1a20a-118">Zadejte do pole IBAN hodnotu „DE36200400000628808808“.</span><span class="sxs-lookup"><span data-stu-id="1a20a-118">In the IBAN field, type 'DE36200400000628808808'.</span></span>
9. <span data-ttu-id="1a20a-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1a20a-119">Close the page.</span></span>

## <a name="set-up-a-method-of-payment-for-the-vendor"></a><span data-ttu-id="1a20a-120">Nastavení metody platby pro dodavatele</span><span class="sxs-lookup"><span data-stu-id="1a20a-120">Set up a method of payment for the vendor</span></span>
1. <span data-ttu-id="1a20a-121">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="1a20a-121">Click Edit.</span></span>
2. <span data-ttu-id="1a20a-122">Rozbalte nebo sbalte oddíl Platba.</span><span class="sxs-lookup"><span data-stu-id="1a20a-122">Expand or collapse the Payment section.</span></span>
3. <span data-ttu-id="1a20a-123">V poli Způsob platby kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="1a20a-123">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="1a20a-124">Klikněte na odkaz na řádku SEPA CT v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1a20a-124">In the list, click the link in the SEPA CT row.</span></span>
5. <span data-ttu-id="1a20a-125">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1a20a-125">Click Save.</span></span>

