---
title: Vytvoření bankovního účtu dodavatele
description: Tato procedura popisuje způsob vytváření bankovního účtu pro dodavatele.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3dc744ea8ac2ca9beb230977fef7608fdc9c2891
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844050"
---
# <a name="create-a-vendor-bank-account"></a>Vytvoření bankovního účtu dodavatele

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura popisuje způsob vytváření bankovního účtu pro dodavatele. Tento postup můžete projít v ukázkových datech společnosti USMF.

1. Přejděte na Zásobování a zdroje > Dodavatelé > Všichni dodavatelé.
2. Vyberte dodavatele, pro kterého chcete vytvořit bankovní účet, a klepněte na odkaz u ID účtu dodavatele.
3. V podokně akcí klikněte na možnost Dodavatel.
4. Klikněte na možnost Bankovní účty.
5. Klikněte na položku Nová.
6. Zadejte hodnotu do pole Bankovní účet.
    * Toto ID se použije k určení bankovního účtu v záznamu dodavatele.  
7. Zadejte hodnotu do pole Název.
8. V poli Bankovní skupiny zadejte nebo vyberte hodnotu.
9. V poli Typ směrového kódu vyberte vhodnou možnost.
    * Toto je typ směrového kódu banky používaného pro mezinárodní platby.  
10. Zadejte hodnotu do pole Číslo bankovního účtu.
11. V poli Kód SWIFT zadejte hodnotu.
12. Zadejte hodnotu do pole IBAN.
    * Číslo IBAN musí být ve správném formátu. Například DE89370400440532013000.  
    * Stav bankovního účtu je aktivní v případě, že bylo dosaženo aktivní datum, a nepřesáhli jste datum vypršení platnosti. Je rovněž aktivní, pokud je prázdné aktivní datum i pole Datum vypršení platnosti. Obsahují-li pole Aktivní datum i Datum vypršení platnosti data spadající do budoucnosti, elektronické platby nejsou k dispozici. Lze však použít jiné typy plateb a bankovní účet je aktivní.  
13. Rozbalte sekci Nastavení.
14. V poli Kód textu zadejte hodnotu.
    * Toto pole určuje kód, který se zobrazí na bankovním výpisu příjemce.  
15. Zadejte hodnotu do pole Zpráva bance.
16. Zadejte hodnotu do pole Odkaz na kurz.
    * Toto je referenční číslo sazby směnného kurzu pro fixní nebo budoucí datum.  
17. V poli Měna zadejte nebo vyberte hodnotu.
    * Při vystavení verifikační transakce poskytuje tato část přehled stavu (v čekání nebo schválené).  
18. Rozbalte sekci Adresa.
19. Rozbalte sekci Verifikační transakce.
20. Rozbalte oddíl Kontaktní informace.
21. Zadejte hodnotu do pole Telefon.
22. Zavřete stránku.
23. Klikněte na položku Upravit.
24. Rozbalte sekci Platba.
25. V poli Bankovní účet vyberte účet, který jste právě vytvořili.
26. Klikněte na položku Uložit.
    * Adresa může být zděděna z bankovní skupiny, pokud je určena, nebo ji můžete přidat zde.  

