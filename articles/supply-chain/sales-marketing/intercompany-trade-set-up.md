---
title: Nastavení mezipodnikového obchodu
description: Tento článek vysvětluje, jak nastavit mezipodnikový obchod
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage, InterCompanyTradingRelationSetupCustomer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8d956c60db9f3acf2f1759dc3e1922da40d8a514
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905624"
---
# <a name="set-up-intercompany-trade"></a>Nastavení mezipodnikového obchodu

[!include [banner](../../includes/banner.md)]

Chcete-li povolit provádění mezipodnikového obchodu v aplikaci Microsoft Dynamics 365 Supply Chain Management, je nutné konfigurovat odběratele a dodavatele pro spuštění mezipodnikového obchodu. Nastavit musíte také Závazky, Pohledávky, Zásobování a zdroje a Prodej a marketing.

## <a name="before-you-set-up-intercompany-trade"></a>Před konfigurací mezipodnikového obchodu

Před konfigurací mezipodnikového obchodu je nutné určit, kteří odběratelé patří mezi mezipodnikové odběratele a kteří dodavatelé mezi mezipodnikové dodavatele. U každé právnické osoby v aplikaci Microsoft Dynamics 365 Supply Chain Management je nutné se rozhodnout, které obchodní zásady mají být uplatněny pro mezipodnikové obchodní vztahy s určitým mezipodnikovým odběratelem nebo dodavatelem.

Zejména doporučujeme, abyste se vy a vaše organizace seznámili s mezipodnikovými parametry.

- Diskutujte o důsledcích provedených nastavení s manažery, kteří jsou odpovědní za mezipodnikový obchod v každé právnické osobě.
- Nastavte příslušné hodnoty pro každou právnickou osobu.

## <a name="set-up-trading-relations"></a>Nastavení obchodních vztahů

Chcete-li nastavit mezipodnikový obchod u zákazníků a dodavatelů, postupujte takto.

1. Přejděte na **Pohledávky \> Odběratelé \> Všichni odběratelé**.
1. Výběr účtu zákazníka.
1. V podokně akcí na kartě **Obecné** zvolte **Mezipodnikové**.
1. Zadejte parametry nastavení mezipodnikových operací pro účet odběratele. Tyto parametry zahrnují právnickou osobu, která obsahuje příslušného dodavatele a účet dodavatele. Parametry zahrnují zásady nákupních objednávek, zásady prodejních objednávek, mapování hodnot a zásady kupních a prodejních smluv. Můžete také určit, zda chcete použít základní hodnoty dat z účtu odběratele nebo z účtu dodavatele u jiné právnické osoby.
1. Opakujte kroky 1 až 4 pro zbývající mezipodnikové odběratele v právnické osobě.
1. Přejděte do části **Pohledávky \> Dodavatelé \> Všichni dodavatelé**.
1. Vyberte účet dodavatele.
1. V podokně akcí na kartě **Obecné** zvolte **Mezipodnikové**.
1. Zadejte parametry nastavení mezipodnikových operací pro účet dodavatele. Tyto parametry zahrnují právnickou osobu, která obsahuje příslušného odběratele a účet odběratele. Parametry zahrnují zásady prodejních objednávek, zásady nákupních objednávek, mapování hodnot a zásady kupních a prodejních smluv. Můžete také určit, zda chcete použít základní hodnoty dat z účtu dodavatele nebo z účtu odběratele u jiné právnické osoby.
1. Opakujte kroky 6 až 9 pro zbývající mezipodnikové dodavatele v právnické osobě.

## <a name="set-up-products"></a>Nastavení produktů

Chcete-li nastavit mezipodnikový obchod u zákazníků a dodavatelů, postupujte takto.

1. Klikněte na **Řízení informací o produktech \> Produkty \> Všechny produkty a základní produkty**.
1. Definujte produkty, které jsou uvolněny pro právnické osoby, kde chcete provádět mezipodnikový obchod.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
