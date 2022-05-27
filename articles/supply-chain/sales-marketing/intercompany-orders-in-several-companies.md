---
title: Vytváření mezipodnikových nákupních a prodejních objednávek v několika podnicích
description: Toto téma vysvětluje, jak vytvářet mezipodnikové nákupní nebo prodejní objednávky v několika společnostech
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8458a08c1a2e5e656c496eb74188d0e2e7257020
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673711"
---
# <a name="creating-intercompany-purchase-and-sales-orders-in-several-companies"></a>Vytváření mezipodnikových nákupních a prodejních objednávek v několika podnicích

[!include [banner](../../includes/banner.md)]

Aplikace Microsoft Dynamics 365 Supply Chain Management není omezena na práci pouze s jednou výrobní a několika prodejními společnostmi. Všechny společnosti s nastavenými mezipodnikovými operacemi mohou být obchodními stejně jako výrobními podniky.

Jestliže stejnou položku může dodat několik podniků, lze si libovolně vybrat, od kterého podniku bude nakoupena, a aktualizace se provedou, i když se z jedné prodejní objednávky stane několik nákupních objednávek.

Stejným způsobem, jakým automaticky vytvoříte jednu mezipodnikovou nákupní objednávku, lze vytvořit původní prodejní objednávku ve vašem podniku a pak nechat objednávku splnit několika mezipodnikovými dodavateli tak, že vytvoříte více než jednu mezipodnikovou nákupní objednávku. Aplikace Microsoft Dynamics 365 Supply Chain Management automaticky vytvoří mezipodnikové prodejní objednávky v dodavatelských podnicích.

K tomu účelu musejí být všechny společnosti nastaveny jako obchodní vztahy. Společnosti dodavatelů musejí být nastaveny v Microsoft Dynamics 365 Supply Chain Management jako mezipodnikoví dodavatelé a musejí být primárním dodavatelem příslušné položky. Na prodejní objednávce v **Zobrazení záhlaví** musíte vybrat pole **Automaticky vytvářet mezipodnikové objednávky** a pole **Přímá dodávka** na záložce **Mezipodniková nastavení**. Toto je výchozí nastavení.

Prodejní řádky vytvoříte obvyklým způsobem. Když opustíte záznam, zobrazí se zpráva informující o tom, že byly vytvořeny mezipodnikové nákupní objednávky a mezipodnikové prodejní objednávky. Zpráva obsahuje odkazy na nové objednávky. Chcete-li zobrazit mezipodnikové prodejní objednávky vytvořené ve vašich dodavatelských společnostech, otevřete původní prodejní objednávku a na kartě **Obecné** ve skupině **Související informace** vyberte **Reference**.

Když otevřete mezipodnikové nákupní objednávky pro dodavatele, vidíte, že aplikace Microsoft Dynamics 365 Supply Chain Management u jednotlivých dodavatelů automaticky vyplňuje číslo původní prodejní objednávky a číslo mezipodnikové prodejní objednávky.

Když obdobně otevřete mezipodnikové prodejní objednávky pro dodavatele, vidíte, že aplikace Microsoft Dynamics 365 Supply Chain Management u jednotlivých dodavatelů automaticky vyplňuje číslo původní prodejní objednávky a číslo mezipodnikové nákupní objednávky.

> [!NOTE]
> Jestliže položky na objednávce existují u jednoho mezipodnikového dodavatele, ale ne u jiného, aplikace Microsoft Dynamics 365 Supply Chain Management vytvoří mezipodnikové objednávky pro dodavatelský podnik, ve kterém tyto položky existují, ale zastaví tvorbu objednávek pro druhý podnik. Když k tomu dojde, objeví se oznámení.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
