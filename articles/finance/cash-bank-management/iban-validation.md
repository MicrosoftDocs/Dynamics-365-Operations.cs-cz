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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: f3e7376827a42034e68cb0ee492b82f7274930ea
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253980"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="a0ef6-103">Správa ověření mezinárodního čísla bankovního účtu (IBAN)</span><span class="sxs-lookup"><span data-stu-id="a0ef6-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0ef6-104">Ověření mezinárodního čísla bankovního účtu (IBAN) zvyšuje množství ověření, které se provádí při přidání čísla IBAN k bankovnímu účtu.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="a0ef6-105">Informace o struktuře kódu IBAN jsou uloženy v aplikaci Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="a0ef6-106">Tyto informace se načtou automaticky, když použijete kód IBAN na bankovní účty poprvé.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="a0ef6-107">Obsahuje délku kódu IBAN počáteční pozice čísla bankovního účtu a směrového čísla, a délku čísla bankovního účtu a směrového čísla.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="a0ef6-108">Nastavení struktur čísla IBAN</span><span class="sxs-lookup"><span data-stu-id="a0ef6-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="a0ef6-109">Přejděte do **Pokladna a banka \> Nastavení \> IBAN struktury**.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="a0ef6-110">Všimněte si, že IBAN struktury pro každou zemi nebo oblast byly vytvořeny automaticky.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="a0ef6-111">Pokud chcete přizpůsobit struktury pro konkrétní zemi nebo region, můžete je upravit.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="a0ef6-112">Definice struktury budou částí každé nové verze.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="a0ef6-113">Lze použít nabídku **Resetovat struktury** pro načtení nejnovějších definic po každé aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="a0ef6-114">Ověření IBAN struktury v bankovním účtu</span><span class="sxs-lookup"><span data-stu-id="a0ef6-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="a0ef6-115">Přejděte do části **Pokladna a banka \> Bankovní účty \> Bankovní účty**.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="a0ef6-116">Vytvořte bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-116">Create a bank account.</span></span>
3. <span data-ttu-id="a0ef6-117">Na pevné kartě **Doplňkové informace** zadejte IBAN.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="a0ef6-118">Pokud délka kódu IBAN neodpovídá délce, která je definována pro každou zemi nebo oblast, dostanete zprávu s upozorněním.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="a0ef6-119">Nelze pokračovat, pokud délka čísla IBAN neodpovídá délce určené ve struktuře IBAN.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="a0ef6-120">Ověření také kontroluje, že číslo bankovního účtu odpovídá části IBAN, která představuje číslo bankovního účtu.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="a0ef6-121">Pokud číslo bankovního účtu neodpovídá, dostanete zprávu s upozorněním.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="a0ef6-122">Tato zpráva je pouze upozornění.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-122">This message is only a warning.</span></span> <span data-ttu-id="a0ef6-123">Můžete pokračovat i v případě, že číslo bankovního účtu neodpovídá.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="a0ef6-124">Ověření také kontroluje, že číslo směrový kód banky odpovídá části IBAN, která představuje směrový kód banky.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="a0ef6-125">Směrový kód obsahuje číslo banky a často další pobočku banky.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="a0ef6-126">Pokud směrový kód neodpovídá, dostanete zprávu s upozorněním.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="a0ef6-127">Tato zpráva je pouze upozornění.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-127">This message is only a warning.</span></span> <span data-ttu-id="a0ef6-128">Můžete pokračovat i v případě, že směrový kód neodpovídá.</span><span class="sxs-lookup"><span data-stu-id="a0ef6-128">You can continue even if the bank routing number doesn't match.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]