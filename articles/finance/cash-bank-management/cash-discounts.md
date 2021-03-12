---
title: Platební slevy
description: Platební slevy jsou nastaveny a sdílené pro závazky a pohledávky.  Dostupná platební sleva může být definovaná na faktuře odběratele nebo dodavatele a proběhne, jestliže bude faktura zaplacena v rámci data platební slevy.
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: roschlom
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d4f6d5bdf4f2fdc4529d9f51515ed2ac4b5b3b5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985305"
---
# <a name="cash-discounts"></a>Platební slevy

[!include [banner](../includes/banner.md)]

Platební slevy jsou nastaveny a sdílené pro závazky a pohledávky.  Dostupná platební sleva může být definovaná na faktuře odběratele nebo dodavatele a proběhne, jestliže bude faktura zaplacena v rámci data platební slevy. 

## <a name="cash-discounts"></a>Platební slevy

Na stránce Platební slevy lze vytvořit platební slevy pro odběratele nebo dodavatele. Pomocí pole Další kód slevy lze definovat také řadu platebních slev, které budou postupně následovat vždy, když vyprší platnost předchozí platební slevy. Další informace naleznete v části „Příklad: Řada platebních slev“ dále v tomto tématu. Pokud jsou faktura, transakce akreditivu (platba nebo dobropis) nebo obě tyto možnosti zadány v jiné měně než v zúčtovací měně právnické osoby, platební sleva se vypočítá pomocí směnného kurzu na základě data platby nebo dobropisu. Pokud jsou faktura a platební doklad zadány v jiných právnických osobách a zúčtovací měny se pro právnické osoby liší, směnný kurz je převzat z právnické osoby faktury k datu dokumentu akreditivu. Další informace naleznete v části „Příklad: Směnné kurzy pro platební slevy“ dále v tomto tématu.

## <a name="defaulting-order-of-cash-discount-main-account"></a>Výchozí objednávka hlavního účtu platební slevy

Pokud je faktura uhrazena v termínu opravňujícím k platební slevě, zaúčtuje se platební sleva automaticky na hlavní účet platebních slev podle následující výchozí priority:
1.  Hlavní účet určený v poli Alternativní účet pro slevu na odběratelově stránce Vyrovnat otevřené transakce a dodavatelově stránce Vyrovnat otevřené transakce.
2.  Hlavní účet určený v poli Platební sleva odběratele nebo Platební sleva dodavatele účetní skupiny hlavní knihy, která je přiřazena ke kódu DPH na faktuře. Na stránce Skupiny zaúčtování hlavní knihy nastavte účetní skupiny hlavní knihy a na stránce Kódy DPH je přiřaďte ke kódům DPH.
3.  Hlavní účtovací účet na stránce Platební slevy buď v poli Hlavní účet slev odběratele, nebo v poli Hlavní účet slev dodavatele pro kód platební slevy, který je na uhrazené faktuře.
4.  Hlavní účet pro platební slevy, který je definován na stránce Účty pro automatické transakce.

## <a name="example-series-of-cash-discounts"></a> Příklad: Řada platebních slev
vytvořte tři kódy platební slevy následujícím způsobem:
-   Kód 5D10% – platební sleva 10 % při uhrazení částky do 5 dní.
-   Kód 10D5% – platební sleva 5 % při uhrazení částky do 10 dní.
-   Kód 14D2% – platební sleva 2 % při uhrazení částky do 14 dní.

V poli Další kód slevy:
-   Pro kód 5D10%, vyberte 10D5%.
-   Pro kód 10D5%, vyberte 14D2%.
-   Pro kód 14D2% ponechte pole Další kód slevy prázdné.

Tři platební slevy následují po sobě tak, jak datum platby postupně překračuje datum dřívější platební slevy na faktuře. Při uhrazení faktury je poskytnuta pouze jedna platební sleva podle toho, jaké datum platební slevy bylo v řadě platebních slev splněno.

## <a name="example-exchange-rates-for-cash-discounts"></a> Příklad: Směnné kurzy pro platební slevy
Zúčtovací měna vaší právnické osoby je EUR a pro USD jsou zadány následující směnné kurty:
-   1. únor = 110
-   1. březen = 80

Faktura na 1000 USD s podmínkou platební slevy 20D2% je zaúčtována 15. února. Částka v zúčtovací měně faktury činí 1100 EUR. Platba za 980 USD je vyrovnána s fakturou 1. března. Částka platební slevy je 20 USD. Částka v zúčtovací měně u dané platby činí 784 EUR. Částka v zúčtovací měně u platební slevy je vypočítána pomocí směnného kurzu ke dni 1. března: 20 \* 80 / 100 = 16 EUR.

> [!NOTE]
> Je-li na stránce Parametry pohledávek nebo na stránce Parametry závazků zvolena možnost Vypočítat platební slevy pro částečné platby, použije se směnný kurz platný k datu jednotlivých částečných plateb. 

