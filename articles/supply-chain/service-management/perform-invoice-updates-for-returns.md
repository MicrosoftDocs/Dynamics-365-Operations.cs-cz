---
title: Provádění aktualizací faktur pro vrácení
description: Tato funkce aplikace  dále podporuje obchodní procesy organizací, které se rozhodly fakturovat vratky a prodejní objednávky najednou a stejnou osobou.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41d3b884d1ed11d2f79e968a5a099860486ef600
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810647"
---
# <a name="perform-invoice-updates-for-returns"></a>Provádění aktualizací faktur pro vrácení 

[!include [banner](../includes/banner.md)]


Vratka je typem prodejní objednávky označeným jako Vrácená položka. Proto se stránka se seznamem **Všechny prodejní objednávky** používá ke generování faktur vratek namísto formuláře **Vratky**. Tato funkce aplikace  dále podporuje obchodní procesy organizací, které se rozhodly fakturovat vratky a prodejní objednávky najednou a stejnou osobou.

Vzhledem k tomu, že pro vrácenou položku obsahuje zápornou částku, jedná se o dobropis.

Při nastavení aktualizace faktury pro dávkové zpracování musí prodejní objednávka typu **Vrácená položka** obsahovat stav řádku vrácenky **Přijato**, který indikuje, že byl aktualizován dodací list objednávky.

## <a name="post-an-invoice-for-a-return-order"></a>Zaúčtujte fakturu pro objednávku vratky

1.  Klikněte na **Pohledávky** \> **Společné** \> **Prodejní objednávky** \> **všechny prodejní objednávky**.

2.  Vyberte prodejní objednávku, pro kterou se v poli **Typ objednávky** zobrazí **Vratka**.

3.  V podokně akcí na kartě **Faktura** ve skupině **Generovat** klikněte na **Faktura**.

4.  Na kartě **Parametry** zaškrtněte políčko **Zaúčtování**.

5.  Zkontrolujte informace ve formuláři a proveďte potřebné změny.

6.  Klikněte na tlačítko **OK**. Zaúčtuje se dobropis.

## <a name="see-also"></a>Viz také

[Aktualizace dodacího listu pro vrácení](packing-slip-updates-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]