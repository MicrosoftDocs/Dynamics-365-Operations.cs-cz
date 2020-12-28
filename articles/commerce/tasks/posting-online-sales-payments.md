---
title: Zaúčtování online prodeje a plateb
description: Tato procedura vás provede konfigurací a spuštěním opakující se dávkové úlohy pro vytváření prodejních objednávek a plateb za transakce obchodu online.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3bac0cab764436a618fa570901c84ab720dbc86
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410825"
---
# <a name="posting-of-online-sales-and-payments"></a>Zaúčtování online prodeje a plateb

[!include [banner](../includes/banner.md)]

Tato procedura vás provede konfigurací a spuštěním opakující se dávkové úlohy pro vytváření prodejních objednávek a plateb za transakce obchodu online.

Účtování online prodejů a plateb je dvoustupňový proces.

- Probíhá přijímání dat obchodní transakce online do HQ.
- Synchronizace objednávek za účelem vytvoření prodejních objednávek v HQ.

Přenášení dat online transakce lze provést buď ručním spuštěním úlohy P nebo vytvořením opakující se dávkové úlohy.

### <a name="manually-running-the-p-job"></a>Ruční spuštění úlohy P.

1. Přejděte na Všechny pracovní prostory > Maloobchodní a velkoobchodní IT.
2. Klikněte na Plán distribuce
3. Vyberte P-0001.
4. V případě potřeby upravte skupiny databáze kanálů.
5. Klikněte na možnost Spustit.
6. Klepněte na tlačítko Ano.

### <a name="scheduling-a-recurring-p-job"></a>Plánování opakované úlohy P.

1. Přejděte na Všechny pracovní prostory > Maloobchodní a velkoobchodní IT.
2. Klikněte na Plán distribuce
3. Vyberte P-0001.
4. Klikněte na Vytvořit dávkovou úlohu.
5. Klikněte na Spustit na pozadí.
5. Povolte Dávkové zpracování.
6. Klepněte na tlačítko Opakování.
7. Vyberte možnost Bez koncového data.
8. Do pole Počet zadejte interval mezi spuštěními v minutách. Obvykle by to bylo 5-10.
9. Klepněte na tlačítko OK.
10. Klepněte na tlačítko OK.

Objednávky lze synchronizovat buď ručně spuštěním úlohy „Synchronizace objednávek“ nebo vytvořením opakované dávkové úlohy.

### <a name="manually-running-order-synchronization"></a>Ruční spuštění synchronizace objednávek 

Chcete-li ručně spustit úlohu „Synchronizovat objednávky“, postupujte podle následujících kroků.

1. Přejděte na Všechny pracovní prostory > Uložit finanční údaje.
2. Klikněte na Synchronizovat objednávky.
3. Vyberte „Obchody podle regionu“ v poli Organizační hierarchie.
    * Pokud chcete vytvořit dávkovou úlohu pro skupinu obchodů, vyberte určitý obchod online nebo vyberte uzel.  
    * Kliknutím na šipku přidejte výběr.  
4. Klikněte na kartu Spustit na pozadí.
5. Zakažte Dávkové zpracování.
6. Klepněte na tlačítko Opakování.
7. Vyberte možnost Konec po
8. Do pole Konec po zadejte hodnotu 1.
9. Klepněte na tlačítko OK.
10. Klepněte na tlačítko OK.

### <a name="scheduling-recurring-order-synchronization"></a>Plánování opakované synchronizace objednávek

Tato procedura vás provede konfigurací a spuštěním opakující se dávkové úlohy pro vytváření prodejních objednávek a plateb za transakce obchodu online. Tato procedura používá v ukázkových datech společnost USRT.

1. Přejděte na Všechny pracovní prostory > Uložit finanční údaje.
2. Klikněte na Synchronizovat objednávky.
3. Vyberte „Obchody podle regionu“ v poli Organizační hierarchie.
    * Pokud chcete vytvořit dávkovou úlohu pro skupinu obchodů, vyberte určitý obchod online nebo vyberte uzel.  
    * Kliknutím na šipku přidejte výběr.  
4. Klikněte na kartu Spustit na pozadí.
5. Povolte Dávkové zpracování
6. Klepněte na tlačítko Opakování.
7. Vyberte možnost Bez koncového data.
8. Do pole Počet zadejte interval mezi spuštěními v minutách. Obvykle by to bylo 2-20.
9. Klepněte na tlačítko OK.
10. Klepněte na tlačítko OK.

## <a name="data-entities-involved-in-the-process"></a>Datové entity zahrnuté do procesu

- RetailTransactionTable
- RetailTransactionAddressTrans
- RetailTransactionInfocodeTrans
- RetailTransactionTaxTrans
- RetailTransactionSalesTrans
- RetailTransactionTaxMeasure
- RetailTransactionDiscountTrans
- RetailTransactionTaxTransGTE
- RetailTransactionMarkupTrans
- RetailTransactionPaymentTrans
- RetailTransactionAttributeTrans
