---
title: Nastavit kódy DPH
description: Toto téma vysvětluje, jak nastavit kódy DPH v aplikaci Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 594e8f0595ecace748a70860c1ccacaf90b7d279
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222184"
---
# <a name="set-up-sales-tax-codes"></a>Nastavit kódy DPH

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak nastavit kódy DPH. Kódy DPH se vytvoří pro každou nepřímou daň nebo clo, které je právnická osoba povinna vypočítávat, shromažďovat o nich informace a platit je finančním úřadům.

Tento úkol využívá ukázkovou společnost USMF.

1. Přejděte na **Navigační podokno > Daň > Nepřímé daně > DPH > Kódy DPH**.
2. Zvolte **Nové**.
3. V poli Kód **prodejní daně** zadejte hodnotu.
4. Zadejte hodnotu do pole **Název**.
5. Vyberte **Období vyrovnání** otevření rozbalovacího seznamu a určete, pro které finanční úřady a v jakých intervalech je tato DPH vykazována a zaplacena.
6. Vyberte možnost **Skupina zaúčtování hl. knihy** a určete hlavní účty pro zaúčtování DPH do hlavní knihy.
7. Rozbalte pevnou záložku **Výpočet**. Ta obsahuje několik polí určujících způsob výpočtu částky DPH. Vyplňte tato pole podle potřeby.  
8. V **Podokně akcí** v horní části rozhraní vyberte **Kód DPH**.
9. Vyberte **Hodnoty**.
10. Zadejte hodnotu tohoto daňového kódu do sloupce **hodnota**.
    - Pokud je vybrána možnost Částka za jednotku, hodnota na pevné záložce **Výpočet** v poli Zdroj se vynásobí množstvím v transakci a vypočítá se částka DPH.  Pokud kód daně není daní na základě jednotky, hodnota je procentuální a použije se pro Původ pro tento kód daně k výpočtu částky DPH.     
11. Zvolte **Uložit**.
12. Zavřete stránku.
13. Zvolte **Uložit**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]