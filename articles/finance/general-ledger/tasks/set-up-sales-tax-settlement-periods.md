---
title: Nastavení období vyrovnání DPH
description: Toto téma vysvětluje, jak nastavit období vyrovnání DPH v aplikaci Dynamics 365 Finance.
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
ms.openlocfilehash: c17a0240c29dad58c958ab1ce844ee5d8384bd1f
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658922"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Nastavení období vyrovnání DPH

[!include [task guide banner](../../includes/task-guide-banner.md)]

Toto téma vysvětluje, jak nastavit období vyrovnání DPH. Období vyrovnání DPH obsahuje informace o intervalech období, pro které se musí DPH vykazovat a platit. Proces vyrovnání lze spustit pro období vyrovnání pro specifický časový interval. Všechny kódy daně, které jsou spojené s obdobím vyrovnání, budou vyrovnány. V závislosti na nastavení souvisejícího finančního úřadu je daňová povinnost zaúčtována pro dodavatele nebo na účet hlavní knihy.

Tento úkol využívá ukázkovou společnost USMF.

1. V navigačním podokně přejděte na **Moduly > Daň > Nepřímé daně > DPH > Období vyrovnání DPH**.
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Období vyrovnání**.
4. Zadejte hodnotu do pole **Popis**.
5. V poli **Úřad** vyberte finanční úřad, který přijímá sestavy a platby, které byly vytvořeny pro období vyrovnání.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. V poli **Platební podmínky** vyberte požadovaný záznam v rozevírací nabídce. Související finanční úřad lze nastavit jako dodavatele a vyrovnání DPH vytvoří otevřenou fakturu dodavatele. Platební podmínky definují Datum splatnosti pro otevřenou fakturu dodavatele.  
8. Vyberte typ pro intervaly období vyrovnání.
9. Zadejte počet jednotek intervalu období pro každé období. Například čtvrtletí má 3 měsíce.
10. Zaškrtněte nebo zrušte zaškrtnutí políčka **Použít dávkové zpracování pro vyrovnání DPH**. Proces vyrovnání pro období vyrovnání lze zpracovat jako dávkovou úlohu na pozadí. Tato možnost je vhodná velký počet daňových transakcí v rámci intervalu období.  
    > [!NOTE]
    > V současné době to není podporováno ve Španělsku, Japonsku a Nizozemsku.
11. Zaškrtněte nebo odškrtněte políčko **Zabránit generování daňové transakce protiúčtu**. Ve výchozím nastavení systém generuje daňové transakce protiúčtu během procesu vyrovnání, což může způsobit problémy s výkonností, pokud je v určitém časovém intervalu velký počet daňových transakcí. Zaškrtněte toto políčko, abyste zabránili generování daňové transakce protiúčtu.
12. Rozbalte kartu **Intervaly období**.
13. Vyberte **přidat**.
14. Zadejte datum do pole **Od data** v novém řádku.
15. Do pole **Do data** zadejte datum.
16. Vyberte **Nový interval období**. Po zadání prvního intervalu období lze vytvořit automaticky nová období. Můžete se vrátit a přidat nové intervaly období podle potřeby.  
17. Zavřete stránku.

