---
title: " Konfigurace pracovníka"
description: Tato procedura ukazuje, jak nakonfigurovat pracovníka jako obchodního zástupce, který má nárok na provizi z prodeje v POS.
author: jblucher
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 43e65de1fda223c2d0503848e7e57936898c1b73
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804058"
---
# <a name="configure-a-worker"></a> Konfigurace pracovníka

[!include [banner](../includes/banner.md)]

Tato procedura ukazuje, jak nakonfigurovat pracovníka jako obchodního zástupce, který má nárok na provizi z prodeje v POS. Tato procedura používá data ukázkové společnosti USRT.


## <a name="create-a-commission-sales-group-for-the-worker"></a>Vytvoření skupiny prodejní provize pro pracovníka
1. Přejděte na Prodej a marketing > Provize > Prodejní skupiny.
    * Pracovníky lze přiřadit k jedné nebo více prodejních skupin. V POS můžete vybrat libovolnou prodejní skupinu, která obsahuje pracovníky z adresáře prodejny.  
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Skupina.
4. Zadejte hodnotu do pole Název.
5. Klikněte na položku Uložit.
6. V podokně akcí klikněte na položku Obecné.
7. Klepněte na Obchodní zástupce.
    * Prodejní skupina může obsahovat více než jednoho pracovníka. Provize můžete rozdělit mezi pracovníky podle toho, jak definujete podíl na provizi.  
8. V poli Název zadejte nebo vyberte hodnotu.
9. V poli Podíl na provizi zadejte číslo.
10. Klikněte na položku Uložit.
11. Zavřete stránku.
12. Zavřete stránku.

## <a name="assign-the-workers-default-sales-group"></a>Přiřazení výchozí prodejní skupiny pracovníkům
1. Přejděte na Maloobchodní a velkoobchodní prodej > Zaměstnanci > Pracovníci.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Klikněte na kartu Velkoobchod.
    * Pracovníka lze přiřadit výchozí prodejní skupině. Výchozí prodejní skupina bude automaticky přidána do prodejních linek v POS, pokud je tato možnost povolena v profilu funkčnosti pro prodejnu.  
5. Klikněte na položku Upravit.
6. V poli Výchozí skupina zadejte nebo vyberte hodnotu.
7. Klikněte na položku Uložit.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]