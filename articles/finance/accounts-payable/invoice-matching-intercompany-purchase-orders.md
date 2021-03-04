---
title: Párování faktur a mezipodnikové nákupní objednávky
description: Nakupující právnická osoba, která se účastní mezipodnikové obchodní transakce, je pravděpodobně nastavena pro použití párování faktur závazků. V tomto případě požadavky zaúčtování pro párování mezipodnikových obchodních účtů a účtů závazků je třeba splnit dříve, než lze zaúčtovat mezipodnikové faktury dodavatele.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchLineMatchingPolicy
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3101
ms.assetid: 9c7c2e44-45f8-4325-b6de-a09fe790f9cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aaa4a08f65e4a3452782cf2b928464dff27ed59b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440985"
---
# <a name="invoice-matching-and-intercompany-purchase-orders"></a>Párování faktur a mezipodnikové nákupní objednávky

[!include [banner](../includes/banner.md)]

Nakupující právnická osoba, která se účastní mezipodnikové obchodní transakce, je pravděpodobně nastavena pro použití párování faktur závazků. Když je pole **Zaúčtovat fakturu s odchylkami** ve formuláři **Parametry závazků** nastaveno na **Vyžadovat schválení**, bude provedeno ověření párování faktury. V tomto případě požadavky zaúčtování pro párování mezipodnikových obchodních účtů a účtů závazků je třeba splnit dříve, než lze zaúčtovat mezipodnikové faktury dodavatele.

V příkladech v tomto tématu je pro mezipodnikový obchod použito toto nastavení:
-   Fabrikam Purchase je nakupující právnická osoba.
-   Fabrikam Sales je prodávající právnická osoba.
-   Ve společnosti Fabrikam Sales existuje odběratel 4020.
-   Ve společnosti Fabrikam Purchase existuje dodavatel 3024.
-   Ve společnosti Fabrikam Purchase jsou mezipodnikové informace určeny pro dodavatele 3024. Jako společnost zákazníka je zadána Fabrikam Sales a jako zákaznický účet odpovídající právnické osobě Fabrikam Purchase je uveden 4020.
-   Ve společnosti Fabrikam Sales jsou mezipodnikové informace určeny pro dodavatele 4020. Jako společnost dodavatele je zadána Fabrikam Purchase a jako účet dodavatele odpovídající právnické osobě Fabrikam Sales je uveden 3024.

V těchto příkladech je pro společnost Fabrikam Purchase použito následující nastavení párování faktur závazků:
-   Na stránce Parametry závazků je zvolena možnost Povolit ověření párování faktur.
-   Na stránce Parametry závazků je v poli Zaúčtovat fakturu s odchylkami zvolena možnost Vyžadovat schválení.
-   Procentuální tolerance ceny u právnických osob činí 2 procenta.

## <a name="example-price-matching-and-intercompany-trade"></a> Příklad: Párování cen a mezipodnikový obchod
Čisté částky na mezipodnikové faktuře dodavatele a mezipodnikové faktuře odběratele se musí shodovat. Tento požadavek má větší důležitost než všechna použitá schválení párování faktur a všechny použité procentuální hodnoty tolerance cen. Postupujte například podle těchto kroků.
1.  Ve společnosti Fabrikam Purchase vytvořte prodejní objednávku SO888 pro odběratele 4020. Ve společnosti Fabrikam Purchase bude automaticky vytvořena mezipodniková nákupní objednávka ICPO222 pro dodavatele 3024 a ve společnosti Fabrikam Sales bude automaticky vytvořena prodejní objednávka ICSO888.
2.  Ve společnosti Fabrikam Sales zaregistrujte fakt, že byly přijaty položky a zaúčtován dodací list . Stav objednávky ICSO888 se změní na Dodáno. Stav objednávky ICPO222 se změní na Přijato.
3.  Ve společnosti Fabrikam Sales aktualizujte fakturu pro objednávku ICSO888. Jednotková cena je 0,45 a bylo aktualizováno 100 položek.
4.  Ve společnosti Fabrikam Purchase vytvořte fakturu pro objednávku ICPO222. Změňte čistou cenu z hodnoty 45,00 na hodnotu 54,00 (simulace omylu). Zobrazí se ikona upozorňující na skutečnost, že cena překročila přípustnou 2procentní toleranci.
5.  Na stránce Podrobnosti o párování faktur zvolte možnost pro schválení zaúčtování s odlišnostmi v párování. Na stránce Faktura dodavatele klikněte na tlačítko OK. Pokud faktura dodavatele nebyla mezipodnikovou fakturou dodavatele, proběhne zaúčtování úspěšně. Nicméně vzhledem k tomu, že pracujete s mezipodnikovou fakturou dodavatele, zaúčtování neproběhne úspěšně. U mezipodnikového obchodu se musí celková fakturovaná částka na mezipodnikové prodejní objednávce shodovat s celkovou fakturovanou částkou na odpovídající mezipodnikové nákupní objednávce. Tento problém je nutné vyřešit tak, že opravíte čistou cenu na faktuře zpět na výchozí částku 45,00.

## <a name="example-quantity-matching-with-intercompany-trade"></a> Příklad: Párování množství v rámci mezipodnikového obchodu
Množství na mezipodnikové nákupní objednávce a na mezipodnikové prodejní objednávce se musí shodovat. Tento požadavek má větší důležitost než všechna použitá schválení párování faktur. V tomto příkladu je pro mezipodnikový obchod použito toto dodatečné nastavení:
-   Ve společnosti Fabrikam Purchase jsou zásady akcí pro nákupní objednávku pro dodavatele 3024 nastaveny na automatické zaúčtování původní faktury odběratele i mezipodnikové faktury dodavatele.

V tomto příkladu je pro společnost Fabrikam Purchase použito následující dodatečné nastavení pro párování faktur závazků:
-   Na stránce Skupiny modelů položek pro skupinu modelů, která je použita položkou B-R14, je zvolena možnost Přijetí požadavků.
-   Množství na skladě pro položku B-R14 je 0 (nula).

Postupujte například podle těchto kroků.
1.  Ve společnosti Fabrikam Purchase vytvořte prodejní objednávku SO999 pro odběratele 4020. Objednávka obsahuje jednu položku řádku: 100 baterií (zboží B R14) za jednotkovou cenu 1,00 ks. Ve společnosti Fabrikam Purchase bude automaticky vytvořena mezipodniková nákupní objednávka ICPO333 pro dodavatele 3024 a ve společnosti Fabrikam Sales bude automaticky vytvořena prodejní objednávka ICSO999.
2.  Ve společnosti Fabrikam Sales aktualizujte fakturu pro objednávku ICSO999. Zaúčtování skončí neúspěchem, protože položka není na skladě a nebyla dosud přijata. Z tohoto důvodu nelze finanční informace aktualizovat.
3.  Ve společnosti Fabrikam Sales zaregistrujte přijetí a zaúčtujte dodací list pro objednávku ICSO999. Příjemka produktu pro objednávku ICPO333 se automaticky zaúčtuje ve společnosti Fabrikam Purchase. Ve společnosti Fabrikam Purchase se přijaté množství pro položku B-R14 změní na hodnotu 100.
4.  Ve společnosti Fabrikam Sales aktualizujte fakturu pro objednávku ICSO999. Zaúčtování proběhne u obou právnických osob úspěšně. Ve společnosti Fabrikam Purchase se zakoupené množství pro položku B-R14 změní na hodnotu 100. 







[!INCLUDE[footer-include](../../includes/footer-banner.md)]