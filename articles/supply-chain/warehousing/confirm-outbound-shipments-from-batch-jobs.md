---
title: Potvrdit odchozí dodávky z dávkových úloh
description: Toto téma popisuje, jak nastavit dávkovou úlohu, která automaticky potvrzuje odchozí zásilky převodu objednávek pro zatížení připravená k odeslání.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 41dbfb90b7b19c964e725ee0a4c769402414fb17
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652217"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Potvrdit odchozí dodávky z dávkových úloh

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak nastavit dávkovou úlohu, která automaticky potvrzuje odchozí zásilky převodu objednávek pro zatížení připravená k odeslání. Zde popsaná dávková úloha se vztahuje pouze na přepravu objednávek, nikoli na prodejní objednávky.

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a>Povolte funkci Potvrdit odchozí zásilky z dávkových úloh

Než budete moci použít tuto funkci, musíte ji povolit ve svém systému. Správci mohou pomocí stránky [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a povolit je v případě potřeby. Tato funkce je uvedena jako:

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
