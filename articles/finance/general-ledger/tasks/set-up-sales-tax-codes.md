---
title: Nastavit kódy DPH
description: Toto téma vysvětluje, jak nastavit kódy DPH v aplikaci Dynamics 365 Finance.
author: twheeloc
ms.date: 09/27/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2539d701dda4ef5e1484d095b2d86d1f68a0dc98
ms.sourcegitcommit: 86f0574363fb869482ef73ff294f345f81d17c5b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7562095"
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

    Pokud je vybrána hodnota **Částka za jednotku** v poli **Původ** na pevné **Výpočet**, vynásobí se množstvím v transakci a vypočítá se částka DPH.  Pokud kód daně není daní na základě jednotky, hodnota je procentuální a použije se pro Původ pro tento kód daně k výpočtu částky DPH.     

11. Zvolte možnost **Uložit**.
12. Zavřete stránku.
13. Zvolte možnost **Uložit**.

Počínaje verzí 10.0.22 aplikace Microsoft Dynamics 365 Finance platí toto: pokud používáte [Daňovou službu](../../localizations/global-tax-calcuation-service-overview.md) a funkce [**Podporovat více DIČ**](../../localizations/emea-multiple-vat-registration-numbers.md) je povolena v pracovním prostoru **Správa funkcí**, můžete pole **Typ daně** použít k zadání typu daňového kódu. K dispozici jsou následující hodnoty:

- Standardní DPH
- Snížená DPH
- DPH 0 %
- Spotřební daň
- Jiné

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
