---
title: Principy vyprazdňování
description: Toto téma popisuje čtyři principy vyprazdňování, které se používají při spotřebě materiálu.
author: johanhoffmann
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgShopSupervisorReleaseOrders
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9f7546b70ddef30d88a79b00fe31d4e82d9bfb9b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423748"
---
# <a name="flushing-principles"></a>Principy vyprazdňování

[!include [banner](../includes/banner.md)]

Principy vyprazdňování odrážejí různé strategie spotřeby surovin, které se používají ve výrobních procesech. Spotřeba je proces, kdy se odečítá materiálu ze zásob na skladě a nastavení této hodnoty pro spotřebované materiály **nedokončené výroby** (výroby NV) pro výrobní zakázky a dávkové objednávky. Obvykle jsou suroviny využívány z umístění, které je nakonfigurováno pro proces, kterým se spotřebuje materiál. Toto skladové místo se označuje jako vstupní místo výroby.

Před zahájením spotřeby materiálu jsou materiály přesunuty do vstupního místa. Následující obrázek znázorňuje proces.

[![scenario4a](./media/scenario4a.png)](./media/scenario4a.png)

1. Sklad materiálu
2. Výdej suroviny
3. Vstupní místo výroby
4. Spotřeba surovin
5. Výrobní proces

Kontrola spotřeby surovin se řídí pomocí následujících čtyř principů vyprazdňování:

- Ruční
- Spuštění
- Dokončit
- K dispozici na skladě

Zásady spotřeby se konfigurují v hierarchii výchozích hodnot. Hierarchie začíná uvolněným produktem, kde má Princip vyprazdňování hodnotu **počáteční**. V kusovníku nebo řádku receptury je možné princip vyprazdňování z produktu přepsat. Výchozí princip vyprazdňování na řádcích kusovníku nebo dávkové objednávky je převzat z produktu nebo přepsané hodnoty v Kusovníku nebo recepturách.

## <a name="description-of-the-flushing-principles"></a>Popis zásad vyprázdnění

### <a name="manual"></a>Ruční
Princip ručního vyprazdňování označuje, že registrace spotřeby materiálu je ruční operace. Tento princip je relevantní, pokud například chcete mít možnost sledování času a musí být vzato v úvahu množství spotřebovaných dávkových nebo sériových čísel pro účely sledování. Ruční spotřeba je registrována v deníku výrobních výdejek. Pro položky, které jsou povoleny pro rozšířené skladové procesy lze použít ručního tok.

### <a name="start"></a>Spuštění
Počáteční princip vyprazdňování určuje, že materiály budou automaticky spotřebovávány při zahájení výrobní zakázky. Množství materiálu, který je spotřebován, je úměrné počátečnímu množství. Když je počáteční princip vyprazdňování použit společně s principem provedení výroby, lze ho použít také k vyprázdnění materiálů při zahájení operace nebo úlohy procesu. Tento princip je relevantní, pokud je například odchylka spotřeby kusovníku nízká, materiály jsou s nízkou hodnotou, neexistují žádné požadavky na sledování a na operace je krátká doba zpracování. 

### <a name="finish"></a>Dokončit
Princip vyprazdňování Dokončit určuje, že materiál bude automaticky spotřebován, když je výrobní zakázka hlášena jako dokončená a operace, která je nastavena na spotřebu materiálu je registrovaná jako dokončená. Množství materiálu, který je spotřebován, je úměrné počátečnímu množství, které je nahlášeno jako dokončené. Když je konečný princip vyprazdňování použit společně s principem provedení výroby, lze ho použít také k vyprázdnění materiálů při dokončení operace nebo úlohy procesu. Tento princip je relevantní ve stejných situacích jako počáteční princip. Princip dokončení je však určen pro operace, které jste mají delší dobu zpracování, kdy by materiály neměly být nastaveny na hodnotu nedokončené výroby před dokončením této operace. 

### <a name="available-at-location"></a>K dispozici na skladě
Princip vyprazdňování K dispozici ve skladovém místě určuje, že materiál bude automaticky spotřebovávaný po registraci jako výdeje pro výrobu. Materiál je registrován jako vyskladněný ze skladového místa po dokončení výdeje surovin, případně když je k dispozici na vstupním místě výroby a uvolnění řádku kusovníku do skladu. Výdejka vytvořená během procesu je zaúčtována v dávkové úloze. Tento princip je relevantní, pokud například máte mnoho aktivit výdeje pro jednu výrobní zakázku. V takovém případě není nutné ručně aktualizovat výdejku a lze získat aktuální zobrazení zůstatku nedokončené výroby.
