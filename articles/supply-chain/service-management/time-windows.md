---
title: Časová okna
description: Časová okna slouží k optimalizaci plánování řádků servisních zakázek.
author: ShylaThompson
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99a958c76e8bd31b57e3f89b2be45028c0597a58
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824287"
---
# <a name="time-windows"></a>Časová okna  

[!include [banner](../includes/banner.md)]

Časová okna slouží k optimalizaci plánování řádků servisních zakázek. Systém lze nastavit tak, aby automaticky vytvořil servisní zakázky. Na základě kritérií určených časovým oknem můžete připojit co nejvíce řádků servisních objednávek k co možná nejméně servisním objednávkám.

Časová okna určují, jak daleko lze přesunout řádek servisní zakázky z jeho vypočteného data. Vypočtené datum je datem, na které byl naplánován řádek servisní zakázky. Datum je založeno na nastavení intervalu a servisním období, které jste definovali na stránce **Vytváření servisních zakázek**. Časové okno definujete pomocí hodnot v následující tabulce:

| Metoda | popis                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Týden   | Datum, kdy řádek servisní zakázky lze přesunout na libovolný otevřený den ve stejném týdnu jako počáteční vypočtené datum.                                                                                                                                                                                    |
| Měsíc  | Datum, kdy řádek servisní zakázky lze přesunout na libovolný otevřený den ve stejném měsíci jako počáteční vypočtené datum. Například vypočítané datum pro řádek servisní zakázky je 15. února 2017. Řádek servisní zakázky lze naplánovat pro všechny pracovní dny mezi 1. a 28. únorem 2017. |
| Ruční | Definujte maximální počet dní před nebo po vypočteném datu, kdy lze přesunout řádek servisní zakázky.                                                                                                                                                                           |

Pokud neurčíte pro řádek servisní smlouvy žádné časové okno, je nutné provést řádek servisní zakázky odvozené od servisní smlouvy přesně v den, na který bylo jeho provedení původně plánováno.

## <a name="related-topics"></a>Související témata

[Tvorba časových oken](create-time-windows.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]