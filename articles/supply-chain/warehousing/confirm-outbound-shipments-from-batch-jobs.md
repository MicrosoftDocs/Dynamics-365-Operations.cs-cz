---
title: Potvrdit odchozí dodávky z dávkových úloh
description: Toto téma popisuje, jak nastavit dávkovou úlohu, která automaticky potvrzuje odchozí zásilky převodu objednávek pro zatížení připravená k odeslání.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f68dcfc0c1454ee5b095e186c52faa6c83bf8dc6
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103908"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Potvrdit odchozí dodávky z dávkových úloh

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak nastavit dávkovou úlohu, která automaticky potvrzuje odchozí zásilky převodu objednávek pro zatížení připravená k odeslání. Zde popsaná dávková úloha se vztahuje pouze na přepravu objednávek, nikoli na prodejní objednávky.

## <a name="turn-the-confirm-outbound-shipments-from-batch-jobs-feature-on-or-off"></a>Zapnutí nebo vypnutí funkce Potvrdit odchozí zásilky z dávkových úloh

Chcete-li používat funkčnost popsanou v tomto tématu, musí být ve vašem systému zapnuta funkce *Potvrdit odchozí zásilky z dávkových úloh*. Od verze Supply Chain Management 10.0.21 je tato funkce ve výchozím nastavení zapnuta. Od verze Supply Chain Management 10.0.25 je tato funkce povinná a nelze ji vypnout. Pokud používáte verzi starší než 10.0.25, mohou správci tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Potvrdit odchozí zásilky z dávkových úloh* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="process-outbound-shipments"></a>Zpracovat odchozí dodávky

Chcete-li nastavit naplánovanou dávkovou úlohu pro spuštění potvrzení odchozí zásilky pro náklady, které jsou připraveny k odeslání:

1. Přejděte na **Správa skladu \> Periodické úkoly \> Zpracování odchozích zásilek**.
1. Otevře se dialogové okno **Potvrďte odeslání**. Na pevné záložce **záznamy, které mají být zahrnuty** vyberte možnost **Filtr**.
1. Otevře se dialogové okno editoru dotazů. Na kartě **Oblast** přidejte řádek s následujícími hodnotami:
    - **Tabulka** - *Náklady*
    - **Odvozená tabulka** - *Náklady*
    - **Pole** - *Stav nákladu*
    - **Kritéria** - *Naloženo*
1. Vyberte **OK**, chcte-li se vrátit do dialogového okna **Potvrďte odeslání**.
1. Na pevné záložce **Spustit na pozadí** nastavte **Dávkové zpracování** na **Ano**.
1. Na pevné záložce **Spustit na pozadí** vyberte možnost **Opakování**.
1. Otevře se dialogové okno **Definujte opakování**. Nastavte plán běhu podle potřeby pro vaše podnikání.
1. Vyberte **OK**, chcte-li se vrátit do dialogového okna **Potvrďte odeslání**.
1. Vyberte **OK** v dialogovém okně **Potvrďte odeslání** pro přidání dávkové úlohy do dávkové fronty.

Další informace viz [Přehled dávkového zpracování](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]