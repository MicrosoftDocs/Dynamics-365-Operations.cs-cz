---
title: "Správa ověření mezinárodního čísla bankovního účtu (IBAN)"
description: "Toto téma vysvětluje správu ověření mezinárodního čísla bankovního účtu (IBAN)."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: cs-cz
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="5134f-103">Správa ověření mezinárodního čísla bankovního účtu (IBAN)</span><span class="sxs-lookup"><span data-stu-id="5134f-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5134f-104">Ověření mezinárodního čísla bankovního účtu (IBAN) zvyšuje množství ověření, které se provádí při přidání čísla IBAN k bankovnímu účtu.</span><span class="sxs-lookup"><span data-stu-id="5134f-104">International Bank Account Number (IBAN) account validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="5134f-105">Struktura čísla IBAN je uložena v aplikaci Microsoft Dynamics 365 for Finance and Operation a je automaticky načtena, když poprvé použijete IBAN na bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="5134f-105">The structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operation, and is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="5134f-106">Číslo bankovního účtu je součástí struktury definované pro číslo IBAN.</span><span class="sxs-lookup"><span data-stu-id="5134f-106">The bank account number is part of the structure defined for an IBAN number.</span></span> <span data-ttu-id="5134f-107">Na základě této struktury se zobrazí upozornění, pokud pozice a délka čísla účtu v IBAN neodpovídají pozici, která je definována ve struktuře pro každou zemi nebo oblast.</span><span class="sxs-lookup"><span data-stu-id="5134f-107">Based on that structure, if the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you will receive warning messages.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="5134f-108">Nastavení struktur čísla IBAN</span><span class="sxs-lookup"><span data-stu-id="5134f-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="5134f-109">Přejděte do **Pokladna a banka \> Nastavení \> IBAN struktury**.</span><span class="sxs-lookup"><span data-stu-id="5134f-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="5134f-110">Všimněte si, že IBAN struktury pro každou zemi nebo oblast byly vytvořeny automaticky.</span><span class="sxs-lookup"><span data-stu-id="5134f-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="5134f-111">Pokud potřebujete přizpůsobit struktury pro konkrétní zemi nebo region, můžete je upravit.</span><span class="sxs-lookup"><span data-stu-id="5134f-111">If you must customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="5134f-112">Definice struktury budou částí každé nové verze.</span><span class="sxs-lookup"><span data-stu-id="5134f-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="5134f-113">Lze použít nabídku **Resetovat struktury** pro načtení nejnovějších definic po každé aktualizaci.</span><span class="sxs-lookup"><span data-stu-id="5134f-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="5134f-114">Ověření IBAN struktury v bankovním účtu</span><span class="sxs-lookup"><span data-stu-id="5134f-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="5134f-115">Přejděte do části **Pokladna a banka \> Bankovní účty \> Bankovní účty**.</span><span class="sxs-lookup"><span data-stu-id="5134f-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="5134f-116">Vytvořte bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="5134f-116">Create a bank account.</span></span>
3. <span data-ttu-id="5134f-117">Na pevné kartě **Doplňkové informace** zadejte IBAN.</span><span class="sxs-lookup"><span data-stu-id="5134f-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="5134f-118">Pokud pozice a délka čísla účtu v IBAN neodpovídají pozici, která je definována ve struktuře pro každou zemi nebo oblast, zobrazí se upozornění.</span><span class="sxs-lookup"><span data-stu-id="5134f-118">If the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you receive a message.</span></span> <span data-ttu-id="5134f-119">Nelze pokračovat, pokud délka čísla IBAN neodpovídá délce ve struktuře IBAN.</span><span class="sxs-lookup"><span data-stu-id="5134f-119">You can't continue if the length of the IBAN doesn't match the length in the IBAN structure.</span></span>

    <span data-ttu-id="5134f-120">Ověření také kontroluje, že číslo bankovního účtu odpovídá části IBAN, která představuje číslo bankovního účtu.</span><span class="sxs-lookup"><span data-stu-id="5134f-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="5134f-121">Pokud číslo bankovního účtu neodpovídá, zobrazí se upozornění.</span><span class="sxs-lookup"><span data-stu-id="5134f-121">If the bank account number doesn't match, you receive a warning message.</span></span> <span data-ttu-id="5134f-122">Tato zpráva je pouze upozornění.</span><span class="sxs-lookup"><span data-stu-id="5134f-122">This message is only a warning.</span></span> <span data-ttu-id="5134f-123">Můžete pokračovat i v případě, že číslo bankovního účtu neodpovídá.</span><span class="sxs-lookup"><span data-stu-id="5134f-123">You can continue even if the bank account number doesn't match.</span></span>

