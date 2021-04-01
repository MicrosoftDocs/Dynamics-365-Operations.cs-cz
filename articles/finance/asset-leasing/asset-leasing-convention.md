---
title: Konvence leasingu aktiv
description: Toto téma popisuje konvence leasingu aktiv.
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7072c34ccbffc6bf135f55fd594cac4d9ea5a463
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237509"
---
# <a name="asset-leasing-conventions"></a>Konvence leasingu aktiv

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Toto téma popisuje konvence leasingu aktiv. K určení data zahájení knihy leasingu se používají konvence pro leasing. Pokud je konvence leasingu nastavena na **Žádný**, datum zahájení je stejné jako datum zahájení leasingu (tj. hodnota pole **Datum zahájení leasingu**). Pokud je konverze leasingu nastavena na **Celý měsíc**, jako datum zahájení se použije první den měsíce, do kterého spadá datum zahájení leasingu.

Datum zahájení určuje datum zahájení období pro plány amortizace závazků a odpisů aktiv. Úrokové náklady a odpisy jsou zaúčtovány k datu ukončení období příslušných plánů. Počáteční uznání a zápis do deníku úprav se zaúčtují v den zahájení.

> [!NOTE]
> Funkce pro konvence leasingu musí být zapnutá prostřednictvím správy funkcí. V pracovním prostoru **Správa funkcí** vyhledejte a vyberte funkci, která se jmenuje **Konvence leasingu pro leasing majetku** a poté vyberte **Povolit nyní**.

Konvence leasingu jsou přiřazeny nastavení pro knihu pronájmu aktiv.

Chcete-li zobrazit nebo přiřadit konvenci leasingu, postupujte takto.

1. Přejděte na **Leasing majetku \> Nastavení \> Leasingové knihy**.
2. V poli **Konvence leasingu** vyberte některou z následujících hodnot.

    | Leasingová smlouva | popis |
    |--------------------|-------------|
    | Není               | Odpisy závazků a odpisy majetku začínají dnem zahájení leasingu, protože datum zahájení se rovná datu zahájení leasingu. Datum ukončení je o měsíc později. Tato konvence leasingu nezaručuje, že úroky budou zaúčtovány v poslední den každého měsíce. |
    | Celý měsíc         | U leasingů, jejichž počáteční datum nastane kdykoli během měsíce, se odpisy závazků a odpisy aktiv začnou časově rozlišovat od prvního dne daného měsíce. Tato konvence leasingu zajišťuje, že úroky se kumulují poslední den každého měsíce po celý měsíc. |

3. Zvolte **Uložit**.

Když je vytvořen leasing, datum zahájení každé knihy se automaticky zadá na základě data zahájení, které je zadáno pro leasing, a leasingové konvence, která je pro knihu zadána.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]