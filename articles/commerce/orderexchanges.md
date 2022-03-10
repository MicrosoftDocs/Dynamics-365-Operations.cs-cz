---
title: Konfigurace a zpracování výměny u vratek
description: Toto téma vysvětluje, jak nakonfigurovat výměnu u vratky v aplikaci Dynamics 365 Commerce.
author: josaw1
ms.date: 07/28/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 488f6fb5af6451bc462566a9714054b49eb1a80b8264528778797f6a39647764
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758329"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>Konfigurace a zpracování výměny u vratek

[!include [banner](includes/banner.md)]

V předchozích verzích aplikace Dynamics 365 Commerce se vrácení proti objednávkám odběratele zpracovávala pomocí dokumentu vratky v modulu Headquarters. Dokument vratky lze však použít pouze pro zpracování produktů, které jsou vráceny. Vrácené produkty jsou označeny negativním množstvím na řádcích vratky. Naopak prodej je označen kladným množstvím. Dokument vratky však nepodporuje kladná množství. Kvůli této limitaci předchozí verze aplikace nepodporovaly scénáře, kde dochází k výměně produktu pomocí dokumentu vratky.

Byla však přidána funkcionality pro podporu scénářů, kde jsou výměny prováděny u vratek. Aplikace Commerce nyní používá dokument prodejní objednávky namísto dokumentu vratky pro zpracování těchto typů transakcí.

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a>Konfigurace aplikace Commerce pro podporu výměn u vratek

> [!NOTE]
> Ve verzi aplikace Commerce 10.0.20 a novější je k dispozici nová funkce nazvaná „Sjednocené prostředí pro zpracování vrácení na pokladním místě“. Pokud tuto funkci povolíte, níže uvedené kroky nastavení nejsou nutné. **Zpracování vratek jako prodejních objednávek** se stane trvale nakonfigurovaným nastavením a nebude jej možné změnit.

Podle těchto kroků nakonfigurujte systém tak, aby podporoval výměny při vratkách (pokud nemáte povolenu funkci **Sjednocené prostředí pro zpracování vrácení na pokladním místě**).

1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry aplikace Commerce**. Na pevné záložce **Objednávky odběratele** nastavte možnost **Zpracovat vratky jako prodejní objednávky** na **Ano**.
2. Spusťte úlohu **Globální plán distribuce konfigurace** (**1110**).

## <a name="make-an-exchange"></a>Provedení výměny

Poté, co je systém nakonfigurován podle popisu v předchozí části, uživatel pokladního místa nadále bude vybírat prodejní objednávku nebo prodejní fakturu pro zpracování vratky, jako v předchozích verzích aplikace. Nicméně když jsou vrácené položky přidány do košíku, uživatel bude moct přidat do košíku nové prodejní řádky.

Pro tyto nové prodejní řádky musí uživatel definovat všechny atributy, které jsou nutné ke zpracování řádku objednávky odběratele. Tyto atributy zahrnují způsob doručení a místo plnění. Platba, která je splatná za transakci, bude čistá částka řádků vratky a prodejní objednávky. Když je platba za transakci vyrovnána, vratka bude zaúčtována jako dokument prodejní objednávky v Headquarters a systém okamžitě vyfakturuje řádky vratky.

Za účelem lepší viditelnosti různých částek košíku byla ke košíku přidána tři nová pole částek. Můžete použít návrháře obrazovky a zpřístupnit tato nová pole v uživatelském rozhraní pokladního místa.

- **Použitá záloha** – Částka zálohy použitá na transakci, když uživatel provede výdej objednávky odběratele. Pokud neexistuje přepsání zálohy a je nakonfigurována 10% záloha, částka v tomto poli je 90 % celkové částky objednávky odběratele.
- **Vyvézt částku** – Celková částka pro řádky, kde byl způsob doručení nastaven na **Vyvézt** při vytvoření nebo úpravě objednávky odběratele, nebo při výměně objednávky odběratele. Částka v tomto poli zahrnuje daně a poplatky.
- **Částka k vrácení** – Celková částka řádků s negativním množstvím během výměny objednávky odběratele. Částka v tomto poli zahrnuje daně a poplatky.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
