---
title: "Nastavení profilu přehledu doručení zboží"
description: "Tento úkol je zaměřen na nastavení profilu přehledu doručení."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: ca70b6afbbadf1122f57285eff58125f8e10346b
ms.contentlocale: cs-cz
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-an-item-arrival-overview-profile"></a>Nastavení profilu přehledu doručení zboží

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento úkol je zaměřen na nastavení profilu přehledu doručení. Profil přehledu doručení je kolekce pravidel, která budou použita při otevření stránky přehledu doručení uživatelem. Tento postup můžete projít v ukázkových datech společnosti USMF. Tento proces obvykle provádí přijímající pracovník.





1. Přejděte do nabídky Řízení zásob > Nastavení > Distribuce > Profily přehledu doručení.
2. Klikněte na položku Nová.
    * Vzhledem k tomu, že budete téměř vždy pracovat ve stejném skladu s vykládkou úplných vytížení, pro zjednodušení procesu registrace přijatého zboží byste měli vytvořit profil přehledu doručení.  
3. Do pole Profil přehledu doručení zadejte hodnotu.
4. Vyberte možnost v poli Zobrazit řádky.
    * Vyberte řádky, které se mají zobrazit pro příjmy:  Vše – Zobrazení všech řádků bez ohledu na stav.   Probíhá: Zobrazí řádky pro příjmy s průběhem Dokončeno nebo Částečné. To znamená, že pro každý řádek bylo v deníku doručení zaregistrováno buď úplné množství, nebo jeho část.   Nedokončené: Zobrazí řádky pro příjmy s průběhem Žádné nebo Částečné. To znamená, že pro každý řádek nebylo v deníku doručení zaregistrováno nic nebo byla zaregistrována jen část.  
5. Rozbalte nebo sbalte oddíl Možnosti doručení.
6. Zadejte hodnotu do pole Dny dopředu.
    * Umožňuje nastavit filtr pro zobrazení řádků příjemky s očekávaným příjmem během několika příštích dní (v závislosti na vámi nastaveném čísle).  
7. Zadejte hodnotu do pole Dny zpětně.
    * Umožňuje nastavit filtr pro zobrazení řádků příjemky s očekávaným příjmem několik dní před aktuálním datem.  
8. Zadejte hodnotu do pole Sklady.
    * Filtrujte pomocí jednoho nebo více skladů.  
9. Vyberte hodnotu v poli Způsob dodání.
    * Umožňuje nastavit filtr, aby se zobrazovaly pouze řádky příjemky s tímto způsobem dodání.  
10. V poli Název vyberte WHS.
11. V poli Sklad vyberte sklad 24.
    * Toto je výchozí sklad, který bude použit pro registrované řádky příjemky, které používají tento profil.  
12. V poli Místo vyberte Baydoor.
    * Toto je výchozí umístění, které bude použito pro registrované řádky příjemky, které používají tento profil.  
13. Rozbalte nebo sbalte oddíl Podrobnosti dotazu k doručení.
14. V poli Omezit na pracoviště vyberte pracoviště 2.
    * Umožňuje nastavit filtr, aby se zobrazovaly pouze řádky příjemky s tímto sitem.  
15. Nastavte možnost Nákupní objednávky na hodnotu Ano.
    * Vyberte řádky příjemky z nákupních objednávek.  
16. Nastavte možnost Převodní příkazy na hodnotu Ano.
    * Vyberte řádky příjemky z převodních příkazů.  
17. Klikněte na položku Uložit.
18. Zavřete stránku.

