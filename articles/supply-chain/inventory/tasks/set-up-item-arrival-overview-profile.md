--- 
title: "Nastavení profilu přehledu doručení zboží"
description: "Tento úkol je zaměřen na nastavení profilu přehledu doručení."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 5ddc491d73bbb6ac02e37a9c9b9d93545f6f9556
ms.contentlocale: cs-cz
ms.lasthandoff: 02/07/2018

---
# <a name="set-up-an-item-arrival-overview-profile"></a>Nastavení profilu přehledu doručení zboží

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


