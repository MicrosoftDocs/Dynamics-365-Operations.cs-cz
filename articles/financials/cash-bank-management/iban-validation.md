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

# <a name="manage-international-bank-account-number-iban-account-validation"></a>Správa ověření mezinárodního čísla bankovního účtu (IBAN)

[!include [banner](../includes/banner.md)]

Ověření mezinárodního čísla bankovního účtu (IBAN) zvyšuje množství ověření, které se provádí při přidání čísla IBAN k bankovnímu účtu.

Struktura čísla IBAN je uložena v aplikaci Microsoft Dynamics 365 for Finance and Operation a je automaticky načtena, když poprvé použijete IBAN na bankovní účty. Číslo bankovního účtu je součástí struktury definované pro číslo IBAN. Na základě této struktury se zobrazí upozornění, pokud pozice a délka čísla účtu v IBAN neodpovídají pozici, která je definována ve struktuře pro každou zemi nebo oblast.

## <a name="set-up-iban-structures"></a>Nastavení struktur čísla IBAN

1. Přejděte do **Pokladna a banka \> Nastavení \> IBAN struktury**.
2. Všimněte si, že IBAN struktury pro každou zemi nebo oblast byly vytvořeny automaticky.
3. Pokud potřebujete přizpůsobit struktury pro konkrétní zemi nebo region, můžete je upravit.
4. Definice struktury budou částí každé nové verze. Lze použít nabídku **Resetovat struktury** pro načtení nejnovějších definic po každé aktualizaci.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Ověření IBAN struktury v bankovním účtu

1. Přejděte do části **Pokladna a banka \> Bankovní účty \> Bankovní účty**.
2. Vytvořte bankovní účet.
3. Na pevné kartě **Doplňkové informace** zadejte IBAN.

    Pokud pozice a délka čísla účtu v IBAN neodpovídají pozici, která je definována ve struktuře pro každou zemi nebo oblast, zobrazí se upozornění. Nelze pokračovat, pokud délka čísla IBAN neodpovídá délce ve struktuře IBAN.

    Ověření také kontroluje, že číslo bankovního účtu odpovídá části IBAN, která představuje číslo bankovního účtu. Pokud číslo bankovního účtu neodpovídá, zobrazí se upozornění. Tato zpráva je pouze upozornění. Můžete pokračovat i v případě, že číslo bankovního účtu neodpovídá.

