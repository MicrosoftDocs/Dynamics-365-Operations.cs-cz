---
title: Časová okna
description: Časová okna slouží k optimalizaci plánování řádků servisních zakázek.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d79e3d3756b8dc402d6f293437209b2e108be38e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423973"
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

