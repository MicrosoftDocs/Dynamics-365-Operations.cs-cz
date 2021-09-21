---
title: Transakce lze zaúčtovat na pozastavený účet hlavní knihy
description: Pokud je příjemka produktu zrušena, systém umožňuje zaúčtování transakcí na pozastavené účty hlavní knihy, i když jsou pozastaveny hlavní účty
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 20df0ee4107ad62bec0dd9a683660fe2375a3dd1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475844"
---
# <a name="transactions-can-be-posted-to-a-suspended-ledger-account"></a>Transakce lze zaúčtovat na pozastavený účet hlavní knihy

## <a name="symptoms"></a>Příznaky

Pokud je příjemka produktu zrušena, systém umožňuje zaúčtování transakcí na pozastavené účty hlavní knihy, i když jsou pozastaveny hlavní účty.

## <a name="reproduce-the-issue"></a>Reprodukování problému

Následující postup ukazuje jeden způsob, jak reprodukovat problém.

1. Na stránce **Parametry závazků** na kartě **Obecné** se ujistěte, že možnost **Zaúčtovat příjemku produktu do hlavní knihy** je nastavena na *Ano*.
1. Vytvořte nákupní objednávku a přidejte řádek objednávky s množstvím *1 000* pro produkt.
1. Potvrďte nákupní objednávku.
1. Zaúčtujte příjemku produktu a zkontrolujte doklady.
1. Pozastavte příslušné hlavní účty, *200140* a *140200*.
1. Zrušte zaúčtovanou příjemku produktu.
1. Všimněte si, že transakce lze zaúčtovat na pozastavené účty hlavní knihy.

## <a name="resolution"></a>Řešení

Transakce lze zaúčtovat na pozastavené účty hlavní knihy, když jsou zrušeny příjemky produktu, protože toto chování umožňuje správné zaúčtování.
