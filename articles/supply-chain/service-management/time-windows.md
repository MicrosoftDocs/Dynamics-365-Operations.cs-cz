---
title: Časová okna
description: Časová okna slouží k optimalizaci plánování řádků servisních zakázek.
author: ShylaThompson
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f748268f6cb85ff835919485da2828689eee23c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "347208"
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

