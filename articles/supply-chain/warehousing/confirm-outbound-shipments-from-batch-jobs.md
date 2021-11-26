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
ms.openlocfilehash: 4af84383fe1d214849d5d05463bd0cbfad7d0536
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778466"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Potvrdit odchozí dodávky z dávkových úloh

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak nastavit dávkovou úlohu, která automaticky potvrzuje odchozí zásilky převodu objednávek pro zatížení připravená k odeslání. Zde popsaná dávková úloha se vztahuje pouze na přepravu objednávek, nikoli na prodejní objednávky.

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a>Povolte funkci Potvrdit odchozí zásilky z dávkových úloh

Od verze Supply Chain Management 10.0.21 je tato funkce ve výchozím nastavení zapnuta. Správci mohou pomocí stránky [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a povolit či zakázat ji v případě potřeby. Tato funkce je uvedena jako:

- **Modul** - *Řízení skladu*
- **Název funkce** - *Potvrdit odchozí zásilky z dávkových úloh*

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