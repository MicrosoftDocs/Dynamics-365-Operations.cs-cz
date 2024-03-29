---
title: Nastavení dodavatelů, odběratelů a položek pro mezipodnikový obchod
description: Tento článek vysvětluje, jak nastavit dodavatele, odběratele a položky pro mezipodnikový obchod
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4c928435a4e66832b09dbc805664934cfb1236be
ms.sourcegitcommit: b666289f5113d0a3fa2220fe337d5aacf07cbd92
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/08/2022
ms.locfileid: "8945748"
---
# <a name="set-up-vendors-customers-and-items-for-intercompany-trade"></a>Nastavení dodavatelů, odběratelů a položek pro mezipodnikový obchod

[!include [banner](../../includes/banner.md)]

Chcete-li připravit svou organizaci na mezipodnikový obchod, musíte definovat dodavatele a odběratele, se kterými budete interně obchodovat. Poté musíte tyto dodavatele a odběratele spojit s položkami, které budete kupovat nebo prodávat.

1. Přejděte na **Zásobování a zdroje \> Dodavatelé \> Všichni dodavatelé**.
1. Vyberte dodavatele, kterého chcete definovat jako mezipodnikového dodavatele.
1. V podokně akcí na kartě **Obecné** zvolte **Mezipodnikové**.
1. Zadejte parametry nastavení mezipodnikových operací pro účet dodavatele. Tyto parametry zahrnují právnickou osobu a účet odběratele, zásady prodejních objednávek, zásady nákupních objednávek, mapování hodnot a zásady kupních a prodejních smluv. Můžete také určit, zda chcete použít základní hodnoty dat z účtu dodavatele nebo z účtu odběratele u jiné právnické osoby.
1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Na stránce se seznamem **Uvolněné produkty** vyberte položky, které chcete přiřadit dodavateli, aby byly k dispozici pro mezipodnikový obchod. U každé položky otevřete stránku **Podrobnosti uvolněného produktu**. Na kartě **Nákup** zadejte číslo dodavatele do pole **Dodavatel**.
1. Přejděte na **Pohledávky \> Odběratelé \> Všichni odběratelé**.
1. Vyberte odběratele, kterého chcete definovat jako mezipodnikového odběratele.
1. V podokně akcí na kartě **Obecné** zvolte **Mezipodnikové**.
1. Zadejte parametry nastavení mezipodnikových operací pro účet odběratele. Tyto parametry zahrnují právnickou osobu a účet dodavatele, zásady prodejních objednávek, zásady nákupních objednávek, mapování hodnot a zásady kupních a prodejních smluv. Můžete také určit, zda chcete použít základní hodnoty dat z účtu odběratele nebo z účtu dodavatele u jiné právnické osoby.
1. Až budete s nastavením mezipodnikových parametrů hotovi, zavřete stránku **Mezipodnikové** pro návrat k údajům o vybraném zákazníkovi.
1. Rozbalte kartu s náhledem **Různé detaily** a nastavte **Vytvářet mezipodnikové objednávky** na *Ano*. Pokud také chcete, aby byly objednávky doručovány přímo odběratelům, nastavte **Přímá dodávka** na *Ano*.

    > [!NOTE]
    > Jestliže existují položky, které má vaše organizace na skladě a dodává je odběratelům, možná nebudete chtít vytvářet mezipodnikové objednávky automaticky ani v případě, že položku máte na skladě. Chcete-li deaktivovat automatickou tvorbu objednávek u položek, které možná máte na skladě, nastavte **Vytvořit mezipodnikové objednávky** na *Ne*.

1. Pokud chcete povolit nepřímé vytváření dalších řádků na prodejní objednávce, nastavte **Vytvořit řádky objednávky nepřímo** na *Ano*. Uživatel poté může přidávat řádky do původní prodejní objednávky z mezipodnikové prodejní objednávky.

> [!WARNING]
> Jestliže povolíte nepřímé vytváření řádků objednávky, povolujete tak všechny řádky vložené do původní prodejní objednávky z mezipodnikové prodejní objednávky. Každé přidání je poté zpracováno prostřednictvím odběratele a je přidáno do objednávky a na fakturu. Každý dokument, který je součástí prodeje, je navíc vytištěn a zaúčtován automaticky. Uživatelé nejsou na přidání upozorněni.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
