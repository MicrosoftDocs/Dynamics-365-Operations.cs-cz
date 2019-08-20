---
title: Správa ověření mezinárodního čísla bankovního účtu (IBAN)
description: Toto téma vysvětluje správu ověření mezinárodního čísla bankovního účtu (IBAN).
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 70c497ec575ffcaa6f2fdc3fe77bae7b41dc02fb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842418"
---
# <a name="manage-international-bank-account-number-iban-validation"></a><span data-ttu-id="623ff-103">Správa ověření mezinárodního čísla bankovního účtu (IBAN)</span><span class="sxs-lookup"><span data-stu-id="623ff-103">Manage International Bank Account Number (IBAN) validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="623ff-104">Ověření mezinárodního čísla bankovního účtu (IBAN) zvyšuje množství ověření, které se provádí při přidání čísla IBAN k bankovnímu účtu.</span><span class="sxs-lookup"><span data-stu-id="623ff-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="623ff-105">Informace o struktuře kódu IBAN jsou uloženy v aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="623ff-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="623ff-106">Tyto informace se načtou automaticky, když použijete kód IBAN na bankovní účty poprvé.</span><span class="sxs-lookup"><span data-stu-id="623ff-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="623ff-107">Obsahuje délku kódu IBAN počáteční pozice čísla bankovního účtu a směrového čísla, a délku čísla bankovního účtu a směrového čísla.</span><span class="sxs-lookup"><span data-stu-id="623ff-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="623ff-108">Nastavení struktur čísla IBAN</span><span class="sxs-lookup"><span data-stu-id="623ff-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="623ff-109">Přejděte do **Pokladna a banka \> Nastavení \> IBAN struktury**.</span><span class="sxs-lookup"><span data-stu-id="623ff-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="623ff-110">Všimněte si, že IBAN struktury pro každou zemi nebo oblast byly vytvořeny automaticky.</span><span class="sxs-lookup"><span data-stu-id="623ff-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="623ff-111">Pokud chcete přizpůsobit struktury pro konkrétní zemi nebo region, můžete je upravit.</span><span class="sxs-lookup"><span data-stu-id="623ff-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="623ff-112">Definice struktury budou částí každé nové verze.</span><span class="sxs-lookup"><span data-stu-id="623ff-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="623ff-113">Lze použít nabídku **Resetovat struktury** pro načtení nejnovějších definic po každé aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="623ff-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="623ff-114">Ověření IBAN struktury v bankovním účtu</span><span class="sxs-lookup"><span data-stu-id="623ff-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="623ff-115">Přejděte do části **Pokladna a banka \> Bankovní účty \> Bankovní účty**.</span><span class="sxs-lookup"><span data-stu-id="623ff-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="623ff-116">Vytvořte bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="623ff-116">Create a bank account.</span></span>
3. <span data-ttu-id="623ff-117">Na pevné kartě **Doplňkové informace** zadejte IBAN.</span><span class="sxs-lookup"><span data-stu-id="623ff-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="623ff-118">Pokud délka kódu IBAN neodpovídá délce, která je definována pro každou zemi nebo oblast, dostanete zprávu s upozorněním.</span><span class="sxs-lookup"><span data-stu-id="623ff-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="623ff-119">Nelze pokračovat, pokud délka čísla IBAN neodpovídá délce určené ve struktuře IBAN.</span><span class="sxs-lookup"><span data-stu-id="623ff-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="623ff-120">Ověření také kontroluje, že číslo bankovního účtu odpovídá části IBAN, která představuje číslo bankovního účtu.</span><span class="sxs-lookup"><span data-stu-id="623ff-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="623ff-121">Pokud číslo bankovního účtu neodpovídá, dostanete zprávu s upozorněním.</span><span class="sxs-lookup"><span data-stu-id="623ff-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="623ff-122">Tato zpráva je pouze upozornění.</span><span class="sxs-lookup"><span data-stu-id="623ff-122">This message is only a warning.</span></span> <span data-ttu-id="623ff-123">Můžete pokračovat i v případě, že číslo bankovního účtu neodpovídá.</span><span class="sxs-lookup"><span data-stu-id="623ff-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="623ff-124">Ověření také kontroluje, že číslo směrový kód banky odpovídá části IBAN, která představuje směrový kód banky.</span><span class="sxs-lookup"><span data-stu-id="623ff-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="623ff-125">Směrový kód obsahuje číslo banky a často další pobočku banky.</span><span class="sxs-lookup"><span data-stu-id="623ff-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="623ff-126">Pokud směrový kód neodpovídá, dostanete zprávu s upozorněním.</span><span class="sxs-lookup"><span data-stu-id="623ff-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="623ff-127">Tato zpráva je pouze upozornění.</span><span class="sxs-lookup"><span data-stu-id="623ff-127">This message is only a warning.</span></span> <span data-ttu-id="623ff-128">Můžete pokračovat i v případě, že směrový kód neodpovídá.</span><span class="sxs-lookup"><span data-stu-id="623ff-128">You can continue even if the bank routing number doesn't match.</span></span>
