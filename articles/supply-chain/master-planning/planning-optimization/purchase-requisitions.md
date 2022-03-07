---
title: Nákupní žádanky
description: Toto téma popisuje, jak jsou v optimalizaci plánování podporovány nákupní žádanky.
author: ChristianRytt
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 20b4012e054a25d7d21c6f017d8ebcf18f6ee28d
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501071"
---
# <a name="purchase-requisitions"></a>Nákupní žádanky

Hlavní plánování může doplnit schválené nákupní žádanky. K pokrytí nákupních žádanek proto uživatelé nemusí k vytváření nákupních objednávek používat workflow. Místo toho lze nákupní žádanky pokrýt hlavním plánováním. Z důvodu této funkce může nákupní žádanka vyprodukovat nákupní objednávku, objednávku převodu nebo výrobní zakázku v závislosti na hodnotě **Plánovaný typ objednávky**, která je nastavena pro související produkt.

## <a name="enable-master-plans-to-include-requisitions"></a>Povolení hlavních plánů pro zahrnutí žádanek

Chcete-li během výpočtu pokrytí hlavního plánu zahrnout požadavky, postupujte takto.

1. Přejděte na **Hlavní plánování** \> **Nastavení** \> **Plány** \> **Hlavní plány**.
1. Vyberte nebo vytvořte hlavní plán.
1. Na pevné záložce **Obecné** nastavte možnost **Zahrnout žádanky** na *Ano*.
1. Opakujte kroky 2 a 3 pro každý další hlavní plán, do něhož chcete zahrnout žádosti.

## <a name="approved-requisitions-time-fence"></a>Ochranná doba schválených žádanek

*Ochranná doba schválených žádanek* stanoví, jak daleko zpět (ve dnech) bude hlavní plán zahrnovat požadavek ze schválených požadavků na doplnění. Ochrannou lhůtu schváleného požadavku můžete nastavit jak na úrovni skupiny pokrytí, tak na úrovni hlavního plánu.

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a>Nastavení ochranné lhůty schválené žádosti pro skupinu pokrytí

1. Přejděte na **Hlavní plánování** \> **Nastavení** \> **Disponibilita** \> **Skupiny disponibility**.
1. Vytvořte nebo vyberte skupinu pokrytí.
1. Na kartě s náhledem **Ostatní** nastavte pole **Ochranná lhůta schválených žádanek (dny)** na počet dní pro zahrnutí ochranné lhůty.
1. Opakujte kroky 2 a 3 pro každou další skupinu pokrytí, kde chcete nastavit ochrannou lhůtu schválených žádostí.

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a>Nastavení ochranné lhůty schválené žádosti pro individuální hlavní plány

Když nastavíte časové ohraničení schváleného požadavku pro jednotlivý hlavní plán, nastavení přepíše nastavení časového ohraničení pro jakoukoli příslušnou skupinu pokrytí.

1. Přejděte na **Hlavní plánování** \> **Nastavení** \> **Plány** \> **Hlavní plány**.
1. Vyberte nebo vytvořte hlavní plán.
1. Na kartě s náhledem **Ochranná lhůta ve dnech** nastavte pole **Ochranná lhůta schválených žádanek (dny)** na počet dní pro zahrnutí ochranné lhůty.
1. Opakujte kroky 2 a 3 pro každý další hlavní plán, kde chcete nastavit ochrannou lhůtu schválených žádostí.

> [!IMPORTANT]
> **Již brzy:** Schválené ochranné lhůty na žádosti nejsou dosud pro optimalizaci plánování podporovány. Dokud nebudou podporovány, všechny hodnoty, které zadáte do pole **Schválené ochranné lhůty žádanky (dny)**, bude pole ignorováno.

## <a name="independent-supply-regardless-of-coverage-code"></a>Nezávislá dodávka bez ohledu na kód pokrytí

Požadavky na nákup jsou vždy pokryty nezávislými plánovanými objednávkami, bez ohledu na kód pokrytí. Toto chování zajišťuje jasnou sledovatelnost a pracovní toky mezi požadavky na objednávku a objednávkami na doplnění.

### <a name="example-1"></a>Příklad 1

Produkt je nastaven tak, aby měl hodnotu **Kód pokrytí** *Min./max*. Má následující stavy zásob a požadavků:

- Množství zásob na skladě = 10.
- Minimální množství zásob = 15.
- Maximální množství zásob = 20.
- Existuje požadavek na nákup jednoho kusu. Má požadované datum dnes.

Při spuštění hlavního plánování se vytvoří dvě plánované objednávky: jedna na 10 kusů k doplnění zásob na maximální množství a jedna na jeden kus k doplnění požadavku na nákup.

### <a name="example-2"></a>Příklad 2

Produkt je nastaven tak, aby měl hodnotu **Kód pokrytí** *Min./max*. Má následující stavy zásob a požadavků:

- Množství zásob na skladě = 17.
- Minimální množství zásob = 15.
- Maximální množství zásob = 20.
- Existuje požadavek na nákup jednoho kusu. Má požadované datum dnes.

Když běží hlavní plánování, vytvoří se jedna plánovaná objednávka pro jeden kus, aby se doplnila objednávka.

### <a name="example-3"></a>Příklad 3

Produkt je nastaven tak, aby měl hodnotu **Kód pokrytí** *Období* a období sedm dní. Má následující stavy zásob, prodejní objednávky a požadavku:

- Množství zásob na skladě = 0.
- Existuje prodejní objednávka na pět kusů. Má očekávané datum expedice dnes plus jeden den.
- Existuje požadavek na nákup tří kusů. Má požadované datum dnes plus tři dny.

Při spuštění hlavního plánování se vytvoří dvě plánované objednávky: jedna na tři kusy k doplnění zásob na maximální množství a jedna na pět kusů k doplnění požadavku na nákupní objednávku.

> [!NOTE]
> Po spuštění plánované objednávky, která je vázána na nákupní objednávku, plánovací modul udržuje vázání na nákupní objednávku. Pokud později zjistíte, že ve schválené objednávce chybí určité množství, které je nutné ke splnění požadavku na nákup, systém vytvoří novou plánovanou objednávku rozdílu.

Další obecné informace o nákupních žádankách naleznete v tématu [Přehled nákupní žádanky](../../procurement/purchase-requisitions-overview.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]