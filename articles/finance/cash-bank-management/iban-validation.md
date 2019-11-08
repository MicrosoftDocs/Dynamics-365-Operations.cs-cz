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
ms.openlocfilehash: 2aaccd7c09d6daf8a237a433cc22ac1bfc3c1541
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551241"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="55921-103">Správa ověření mezinárodního čísla bankovního účtu (IBAN)</span><span class="sxs-lookup"><span data-stu-id="55921-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55921-104">Ověření mezinárodního čísla bankovního účtu (IBAN) zvyšuje množství ověření, které se provádí při přidání čísla IBAN k bankovnímu účtu.</span><span class="sxs-lookup"><span data-stu-id="55921-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="55921-105">Informace o struktuře kódu IBAN jsou uloženy v aplikaci Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="55921-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="55921-106">Tyto informace se načtou automaticky, když použijete kód IBAN na bankovní účty poprvé.</span><span class="sxs-lookup"><span data-stu-id="55921-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="55921-107">Obsahuje délku kódu IBAN počáteční pozice čísla bankovního účtu a směrového čísla, a délku čísla bankovního účtu a směrového čísla.</span><span class="sxs-lookup"><span data-stu-id="55921-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="55921-108">Nastavení struktur čísla IBAN</span><span class="sxs-lookup"><span data-stu-id="55921-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="55921-109">Přejděte do **Pokladna a banka \> Nastavení \> IBAN struktury**.</span><span class="sxs-lookup"><span data-stu-id="55921-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="55921-110">Všimněte si, že IBAN struktury pro každou zemi nebo oblast byly vytvořeny automaticky.</span><span class="sxs-lookup"><span data-stu-id="55921-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="55921-111">Pokud chcete přizpůsobit struktury pro konkrétní zemi nebo region, můžete je upravit.</span><span class="sxs-lookup"><span data-stu-id="55921-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="55921-112">Definice struktury budou částí každé nové verze.</span><span class="sxs-lookup"><span data-stu-id="55921-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="55921-113">Lze použít nabídku **Resetovat struktury** pro načtení nejnovějších definic po každé aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="55921-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="55921-114">Ověření IBAN struktury v bankovním účtu</span><span class="sxs-lookup"><span data-stu-id="55921-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="55921-115">Přejděte do části **Pokladna a banka \> Bankovní účty \> Bankovní účty**.</span><span class="sxs-lookup"><span data-stu-id="55921-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="55921-116">Vytvořte bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="55921-116">Create a bank account.</span></span>
3. <span data-ttu-id="55921-117">Na pevné kartě **Doplňkové informace** zadejte IBAN.</span><span class="sxs-lookup"><span data-stu-id="55921-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="55921-118">Pokud délka kódu IBAN neodpovídá délce, která je definována pro každou zemi nebo oblast, dostanete zprávu s upozorněním.</span><span class="sxs-lookup"><span data-stu-id="55921-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="55921-119">Nelze pokračovat, pokud délka čísla IBAN neodpovídá délce určené ve struktuře IBAN.</span><span class="sxs-lookup"><span data-stu-id="55921-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="55921-120">Ověření také kontroluje, že číslo bankovního účtu odpovídá části IBAN, která představuje číslo bankovního účtu.</span><span class="sxs-lookup"><span data-stu-id="55921-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="55921-121">Pokud číslo bankovního účtu neodpovídá, dostanete zprávu s upozorněním.</span><span class="sxs-lookup"><span data-stu-id="55921-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="55921-122">Tato zpráva je pouze upozornění.</span><span class="sxs-lookup"><span data-stu-id="55921-122">This message is only a warning.</span></span> <span data-ttu-id="55921-123">Můžete pokračovat i v případě, že číslo bankovního účtu neodpovídá.</span><span class="sxs-lookup"><span data-stu-id="55921-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="55921-124">Ověření také kontroluje, že číslo směrový kód banky odpovídá části IBAN, která představuje směrový kód banky.</span><span class="sxs-lookup"><span data-stu-id="55921-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="55921-125">Směrový kód obsahuje číslo banky a často další pobočku banky.</span><span class="sxs-lookup"><span data-stu-id="55921-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="55921-126">Pokud směrový kód neodpovídá, dostanete zprávu s upozorněním.</span><span class="sxs-lookup"><span data-stu-id="55921-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="55921-127">Tato zpráva je pouze upozornění.</span><span class="sxs-lookup"><span data-stu-id="55921-127">This message is only a warning.</span></span> <span data-ttu-id="55921-128">Můžete pokračovat i v případě, že směrový kód neodpovídá.</span><span class="sxs-lookup"><span data-stu-id="55921-128">You can continue even if the bank routing number doesn't match.</span></span>
