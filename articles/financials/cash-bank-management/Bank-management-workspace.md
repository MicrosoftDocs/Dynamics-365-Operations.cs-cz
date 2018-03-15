---
title: "Pracovní prostor správy banky"
description: "Toto téma poskytuje informace o pracovním prostoru Správa banky. Tento pracovní prostor zobrazuje Informace, které se vztahují k bankovním účtům společnosti a obsahují souhrnné zobrazení a stránku analýzy. Souhrnné zobrazení ukazuje souhrnné dlaždice, informace o bankovním účtu, graf zůstatku a související informace. Na stránce analýzy se používají funkce Microsoft Power BI k zobrazení vizuálů, které se vztahují k zůstatkům na bankovním účtu."
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 92a52646063c145d733b9d2960253004e8eab80a
ms.openlocfilehash: 3c38807e9ed3b2ced37ada35b72e388c125bd654
ms.contentlocale: cs-cz
ms.lasthandoff: 03/05/2018

---
# <a name="bank-management-workspace"></a>Pracovní prostor správy banky

[!include[banner](../includes/banner.md)]

Pracovní prostor **Správa banky** zobrazuje informace, které se vztahují k bankovním účtům společnosti. Tento pracovní prostor obsahuje zobrazení **Souhrn** a stránku **Analýzy**. Zobrazení **Souhrn** ukazuje souhrnné dlaždice, informace o bankovním účtu, graf zůstatku a související informace. Stránka **Analýza** používá funkce Microsoft Power BI k zobrazení vizuálů, které se vztahují k zůstatkům na bankovním účtu.

## <a name="summary-view"></a>Souhrnné zobrazení

### <a name="summary"></a>Souhrn

Dlaždice v části **Souhrn** poskytují přehled o bankovních účtech a umožňují rychlý přístup ke stránkám, které musíte používat nejčastěji. Informace o odsouhlasení banky je specifická vůči funkci rozšířeného odsouhlasení banky. Informace jsou zahrnuty pouze pro ty bankovní účty, které mají možnost **Rozšířené odsouhlasení banky** nastaveno na **Ano** na stránce **Bankovní účet**. Z části **Souhrn** můžete importovat elektronické bankovní soubory pro bankovní účty napříč všemi právnickými osobami.

### <a name="bank-accounts"></a>Bankovní účty

Každý bankovní účet v právnické osobě je představován kartou v části **Bankovní účty**. Je zobrazen aktuální zůstatek a vy můžete procházet podrobnosti transakcí, které tvoří souhrnnou částku zůstatku. Částka **Překlenovací transakce** také umožňuje přejít k podrobnostem transakcí, které tvoří souhrnnou částku. Překlenovací transakce jsou všechny čekající transakce, které byly zaúčtovány pomocí překlenovací funkce, ale které nebyly dosud byly proplaceny. Částka **Čekající zůstatek** je aktuální zůstatek minus překlenovací, nebo čekající, transakce.

Karta rovněž zobrazuje, kdy byl naposledy bankovní účet odsouhlasen. Tyto informace se zobrazí pouze tehdy, pokud je povoleno Rozšířené odsouhlasení banky pro bankovní účet.

### <a name="balance"></a>Rozvaha

Graf **Zůstatek** zobrazuje buď historické informace o zůstatku pro účet zvolený v části **Bankovní účty**, nebo souhrn historických informací o zůstatku pro všechny bankovní účty právnické osoby. Tyto informace jsou k dispozici pro různá období: aktuální týden, aktuální měsíc, aktuální rok, posledních pět let a všechna období (úplná historie bankovního účtu). 

Pokud zobrazíte graf **Zůstatek** pro jeden bankovní účet, historické zůstatky jsou zobrazeny v měně bankovního účtu. Pokud zobrazíte graf pro všechny bankovní účty právnické osoby, historické zůstatky jsou zobrazeny v zúčtovací měně.

Informace o poslední aktualizaci dat se zobrazí v horní části grafu. Můžete data aktualizovat podle potřeby.

### <a name="related-information"></a>Související informace

Z části **Související informace** je možné otevřít stránku **Hlavní deníku** pro dokončení bankovních převodů. Můžete otevřít rychle také stránky **Bankovní transakce** a **Překlenovací transakce**.

## <a name="analytics-view"></a>Zobrazení analýzy

Stránka **Analýza** poskytuje důležité metriky o bankovních účtech v aktuální společnosti. Na stránce jsou k dispozici následující vizualizace:

-   Celkový bankovní zůstatek v měně systému
-   Zůstatek podle právnické osoby
-   Dnešní skutečný a předpokládaný zůstatek v měně bankovního účtu
-   Zůstatek podle bankovního účtu
-   Zůstatek podle měny

Zobrazit bankovní analýzu napříč všemi společnostmi můžete z pracovního prostoru **Přehled hotovosti – všechny společnosti**.

