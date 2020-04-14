---
title: Inventura zásob ve skladu
description: Toto téma popisuje proces vytvoření a zaúčtování deníku inventury zásob za účelem spočítání specifického zboží v jednom umístění ve skladu.
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 53e9457074b696efaf5958b3a3b4616f06f5a6ff
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145749"
---
# <a name="count-inventory-in-a-warehouse"></a>Inventura zásob ve skladu

[!include [banner](../../includes/banner.md)]

Toto téma popisuje proces vytvoření a zaúčtování deníku inventury zásob za účelem spočítání specifického zboží v jednom umístění ve skladu. Tento postup lze použít pro funkce „základního uskladnění“, dostupného v modulu Řízení zásob, ne pro funkce uskladnění, které jsou k dispozici v modulu Řízení skladu. Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat. Používáte-li vlastní data, ujistěte se, že máte nastaveny produkty a umístění a že jste vytvořili název deníku zásob pro deníky inventury. Inventuru skladu běžně provádí zaměstnanec skladu.


## <a name="create-an-inventory-counting-journal"></a>Vytvořte deník inventur zásob
1. Přejděte na **Navigační podokno > Moduly > Správa zásob > Deníkové položky > Počet položek > Inventury**.
2. Zvolte **Nové**.
3. V poli **Název** vyberte z rozevíracího seznamu název deníku inventur zásob, který chcete použít. Některá další pole budou vyplněna na základě nastavení názvu deníku inventur zásob, který jste vybrali.  
4. V poli **Pracovník** klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Ze seznamu **vyberte** pracovníka, kterého chcete použít.
6. Vyberte **OK**.

## <a name="create-journal-lines"></a>Vytvořit řádky deníku
1. Zvolte **Nové**.
2. V poli **Číslo položky** vyberte z rozevíracího seznamu požadovaný záznam. Používáte-li ukázková data společnosti USMF vyberte hodnotu **A0001**.  
3. V poli **Pracoviště** vyberte z rozevíracího seznamu požadovaný záznam. Používáte-li ukázková data společnosti USMF, vyberte pracoviště **2**.
4. V poli **Sklad** vyberte z rozevíracího seznamu požadovaný záznam. Používáte-li ukázková data společnosti USMF, vyberte sklad **24**.  
5. V poli **Umístění** vyberte z rozevíracího seznamu požadovaný záznam. Používáte-li ukázková data společnosti USMF, vyberte umístění **BULK-001**.  
6. Zadejte číslo do pole Spočteno. Pokud zadáte číslo inventury, které se liší od čísla uvedeného v poli **Na skladě**, pole **množství** se aktualizuje a zobrazí odchylku.  
7. Zvolte **Uložit**.

## <a name="post-the-inventory-counting-journal"></a>Zaúčtujte deník inventury zásob
1. Zvolte **Zaúčtovat**. Když tento deník inventury skladu zaúčtujete, a zaúčtovaná částka se bude lišit od částky nahlášené v poli **Na skladě**, zaúčtuje se příjem nebo výdej zásob, změní se úroveň a hodnota zásob a vygeneruje se transakce hlavní knihy.
2. Vyberte **OK**.

## <a name="view-inventory-transactions"></a>Zobrazit skladové transakce
1. Vyberte **skladový model**.
2. Vyberte **Transakce**. V tomto poli se zobrazí všechny související transakce vytvořené při zaúčtování deníku inventury zásob.   

