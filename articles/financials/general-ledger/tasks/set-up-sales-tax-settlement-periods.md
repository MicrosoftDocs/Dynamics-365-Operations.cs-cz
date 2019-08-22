---
title: Nastavit období vyrovnání DPH
description: Období vyrovnání DPH obsahuje informace o intervalech období, pro které se musí DPH vykazovat a platit.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8304d9e8997a5d31740ee1203aa4bf0603014056
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862981"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Nastavit období vyrovnání DPH

[!include [task guide banner](../../includes/task-guide-banner.md)]

Období vyrovnání DPH obsahuje informace o intervalech období, pro které se musí DPH vykazovat a platit. Proces vyrovnání lze spustit pro období vyrovnání pro specifický časový interval. Všechny kódy daně, které jsou spojené s obdobím vyrovnání, budou vyrovnány. V závislosti na nastavení souvisejícího finančního úřadu je daňová povinnost zaúčtována pro dodavatele nebo na účet hlavní knihy.



Tento úkol používá ukázkovou společnost USMF.



1. Přejděte na Daň > Nepřímé daně > DPH > Období vyrovnání DPH.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Období vyrovnání.
4. Zadejte nějakou hodnotu do pole Popis.
5. V poli Úřad vyberte finanční úřad, který přijímá sestavy a platby, které byly vytvořeny pro období vyrovnání.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. V poli Platební podmínky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Související finanční úřad lze nastavit jako dodavatele a vyrovnání DPH vytvoří otevřenou fakturu dodavatele. Platební podmínky definují Datum splatnosti pro otevřenou fakturu dodavatele.  
9. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
10. Klikněte na odkaz na vybraném řádku v seznamu.
11. Vyberte typ pro intervaly období vyrovnání.
12. Zadejte počet jednotek intervalu období pro každé období. Například čtvrtletí má 3 měsíce.
13. Zaškrtněte nebo zrušte zaškrtnutí políčka Použít dávkové zpracování pro vyrovnání DPH.
    * Proces vyrovnání pro období vyrovnání lze zpracovat jako dávkovou úlohu na pozadí. Tato možnost je vhodná velký počet daňových transakcí v rámci intervalu období.  
    > [!NOTE]
    > V současné době to není podporováno v Rakousku, Belgii, Španělsku, Itálii, Japonsku a Nizozemsku.
14. Zaškrtněte nebo odškrtněte políčko Zabránit generování daňové transakce protiúčtu.
    * Ve výchozím nastavení systém generuje daňové transakce protiúčtu během procesu vyrovnání, což může způsobit problémy s výkonností, pokud je v určitém časovém intervalu velký počet daňových transakcí. Zaškrtněte toto políčko, abyste zabránili generování daňové transakce protiúčtu.
15. Rozbalte kartu Intervaly období.
16. Klepněte na možnost Přidat.
17. Označte v seznamu vybraný řádek.
18. Zadejte datum do pole Od data.
19. Do pole Do data zadejte datum.
20. Klikněte na Nový interval období.
    * Po zadání prvního intervalu období lze vytvořit automaticky nová období. Můžete se vrátit a přidat nové intervaly období podle potřeby.  
21. Zavřete stránku.

