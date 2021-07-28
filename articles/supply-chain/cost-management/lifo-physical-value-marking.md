---
title: Metoda LIFO s fyzickou hodnotou a označením
description: U skladového modelu LIFO (Last in, First out) jsou poslední (nejnovější) příjmy vydány jako první. Výdeje ze skladu jsou vyrovnávány vůči posledním příjmům na sklad podle data skladové transakce.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55021
ms.assetid: 49c492b0-b018-44e0-928f-9671e54eee20
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dcac72a60eac6abb29a017eb4ce02a71dca572d3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344537"
---
# <a name="lifo-with-physical-value-and-marking"></a>Metoda LIFO s fyzickou hodnotou a označením

[!include [banner](../includes/banner.md)]

U skladového modelu LIFO (Last in, First out) jsou poslední (nejnovější) příjmy vydány jako první. Výdeje ze skladu jsou vyrovnávány vůči posledním příjmům na sklad podle data skladové transakce. 

Ve skladovém modelu LIFO (Last In, First Out) jsou poslední (nejnovější) příjmy vydávány jako první. Výdeje ze skladu jsou vyrovnávány vůči posledním příjmům na sklad podle data skladové transakce. Při použití metody LIFO není nutné použití pravidla LIFO. Místo toho můžete označit skladové transakce tak, aby bylo vydání určitých položek přijato konkrétním výdejem. Používáte-li skladový model LIFO, doporučujeme vám provádět pravidelné skladové uzávěrky. 

Následující příklady ilustrují dopad použití metody LIFO ve třech různých konfiguracích:

-   Metoda LIFO bez možnosti **Zahrnovat fyzickou hodnotu**
-   Metoda LIFO s možností **Zahrnovat fyzickou hodnotu**
-   Metoda LIFO s označením

## <a name="lifo-without-the-include-physical-value-option"></a>Metoda LIFO bez možnosti Zahrnovat fyzickou hodnotu
V tomto příkladu není skupina modelů položek označena, aby obsahovala fyzickou hodnotu. Následující obrázek znázorňuje tyto transakce:

-   1a. Fyzický příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
-   1b. Finanční příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
-   2a. Fyzický příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
-   2b. Finanční příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
-   3a. Fyzický příjem ve skladu pro množství 1 při ceně 25,00 USD za kus
-   4a. Fyzický příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
-   4b. Finanční příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
-   5a. Fyzický výdej 1 kusu za 20 Kč (průběžný průměr z finančně zaúčtovaných transakcí).
-   5b. Finanční výdej 1 kusu za 20 Kč (průběžný průměr z finančně zaúčtovaných transakcí).
-   6. Je provedena uzávěrka skladu. Podle metody LIFO bude poslední finančně zaúčtovaný výdej vyrovnán posledním finančně zaúčtovaným příjmem. K transakci výdeje bude vytvořena úprava ve výši 10 Kč.

Nová průběžná průměrná cena bude odrážet průměrnou hodnotu finančně aktualizovaných transakcí ve výši 15,00 USD. Následující obrázky ukazují účinky skladového modelu LIFO na tuto sérii transakcí, když není použita možnost **Zahrnovat fyzickou hodnotu**. 

![LIFO bez funkce Zahrnovat fyzickou hodnotu.](./media/lifowithoutincludephysicalvalue.gif) 

**Klíč k diagramu**

- Skladové transakce jsou reprezentovány svislými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad časovou osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod časovou osou.
- Nad (nebo pod) každou svislou šipkou je zadána hodnota skladové transakce ve formátu Množství@Jednotková cena.
- Hodnota skladové transakce uzavřená do závorek označuje, že skladová transakce je fyzicky zaúčtována do skladu.
- Hodnota skladové transakce neuzavřená do závorek označuje, že skladová transakce je finančně zaúčtována do skladu.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou a označeny popiskem *Uzávěrka skladu*.
- Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými šikmými přerušovanými šipkami směřujícími od určitého příjmu k výdeji.

## <a name="lifo-with-the-include-physical-value-option"></a>Metoda LIFO s možností Zahrnovat fyzickou hodnotu
Pokud zaškrtnete políčko **Zahrnovat fyzickou hodnotu** pro položku na stránce **Skupiny modelů zboží**, systém pro výpočet průběžné průměrné ceny použije transakce fyzického i finančního příjmu. V případě potřeby budou v systému také provedeny úpravy fyzicky aktualizované transakce výdeje. Pokud je zaškrtnutí políčka **Zahrnovat fyzickou hodnotu** odstraněno, budou při uzávěrce skladu s použitím skladového modelu LIFO provedena vyrovnání pouze pro finančně aktualizované transakce. 

Následující obrázek znázorňuje tyto transakce:

-   1a. Fyzický příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
-   1b. Finanční příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
-   2a. Fyzický příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
-   2b. Finanční příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
-   3a. Fyzický příjem ve skladu pro množství 1 při ceně 25,00 USD za kus
-   4a. Fyzický příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
-   4b. Finanční příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
-   5a. Fyzický výdej 1 kusu v nákladové ceně 21,25 Kč (průběžný průměr finančně i fyzicky zaúčtovaných transakcí).
-   5b. Finanční výdej 1 kusu v nákladové ceně 21,25 Kč (průběžný průměr finančně i fyzicky zaúčtovaných transakcí).
-   6a. Fyzický výdej ze skladu pro množství 1 při ceně 21,25 USD za kus.
-   7. Je provedena uzávěrka skladu. Podle metody LIFO bude poslední transakce výdeje opravena či vyrovnána posledním zaúčtovaným příjmem.

Transakce 6a bude upravena podle příjmové transakce 4b. Systém tyto transakce nevyrovná, protože příjem je zaúčtován pouze fyzicky, ale nikoli finančně. Místo toho bude k transakci fyzického výdeje zaúčtována úprava ve výši 8,75 Kč. Transakce 5b bude opravena podle transakce fyzického příjmu 3a. Systém tyto transakce nevyrovná, protože ani jedna není finančně zaúčtované. Místo toho bude k této transakci výdeje zaúčtována úprava ve výši -3,75 Kč. Nová průběžná průměrná cena bude odrážet průměrnou hodnotu finančně a fyzicky aktualizovaných transakcí ve výši 20,00 Kč. 

Následující obrázek ukazuje účinek skladového modelu LIFO na tuto sérii transakcí, když není použita možnost **Zahrnovat fyzickou hodnotu**. 

![LIFO s funkcí Zahrnovat fyzickou hodnotu.](./media/lifowithincludephysicalvalue.gif) 

**Klíč k diagramu**

- Skladové transakce jsou reprezentovány svislými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad časovou osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod časovou osou.
- Nad (nebo pod) každou svislou šipkou je zadána hodnota skladové transakce ve formátu Množství@Jednotková cena.
- Hodnota skladové transakce uzavřená do závorek označuje, že skladová transakce je fyzicky zaúčtována do skladu.
- Hodnota skladové transakce neuzavřená do závorek označuje, že skladová transakce je finančně zaúčtována do skladu.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou a označeny popiskem *Uzávěrka skladu*.
- Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými šikmými přerušovanými šipkami směřujícími od určitého příjmu k výdeji.

## <a name="lifo-with-marking"></a>Metoda LIFO s označením
Termínem označení se popisuje proces, který umožňuje propojit transakci výdeje s transakcí příjmu, neboli je označit jako propojené. Označení lze provést před zaúčtováním transakce nebo po ní. Označení lze provést tehdy, pokud chcete zjistit přesné náklady skladu při zaúčtování transakce nebo při provedení uzávěrky skladu. Předpokládejme například, že oddělení služeb odběratelům přijalo spěšnou objednávku od důležitého odběratele. Vzhledem k tomu, že se jedná o spěšnou objednávku, bude nutné pro splnění požadavku zákazníka za tuto položku zaplatit více. 

Přitom si musíte být jisti, že pro fakturu této prodejní objednávky se náklady na tuto skladovou položku odrazí v marži nebo v nákladech na prodané zboží. Při zaúčtování nákupní objednávky bude ve skladu zaznamenán příjem s náklady 120,00 USD. Je-li tento dokument prodejní objednávky propojen s nákupní objednávkou před zaúčtováním dodacího listu nebo faktury, budou náklady na prodané zboží činit 120,00 USD, namísto aktuální průběžné průměrné hodnoty nákladů na položku. Pokud jsou faktura nebo dodací list prodejní objednávky zaúčtovány ještě předtím, než dojde k tomuto propojení, budou náklady na prodané zboží zaúčtovány s použitím průběžné průměrné ceny. 

I před provedením uzávěrky skladu lze tyto dvě transakce vzájemně propojit. 

Před zaúčtováním transakce je možné označit transakci výdeje s příjmem. To lze provést na řádku prodejní objednávky na stránce **Podrobnosti prodejní objednávky**. Můžete zobrazit otevřené transakce příjmu na stránce **Označení**. 

Po zaúčtování transakce je možné také označit transakci výdeje s příjmem. Můžete spárovat nebo označit transakci výdeje pro transakci otevřených příjmů u naskladněné položky z deníku úpravy zaúčtované inventury. 

Následující obrázek znázorňuje tyto transakce:

-   1a. Fyzický příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
-   1b. Finanční příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
-   2a. Fyzický příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
-   2b. Finanční příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
-   3a. Fyzický příjem ve skladu pro množství 1 při ceně 25,00 USD za kus
-   4a. Fyzický příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
-   4b. Finanční příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
-   5a. Fyzický výdej ze skladu pro množství 1 při ceně 21,25 USD za kus (průběžná průměrná hodnota finančních a fyzických aktualizovaných transakcí).
-   5b. Finanční výdej ze skladu pro množství 1 je před zaúčtováním transakce propojen s příjmem ve skladu 2b. Tato transakce je zaúčtována s nákladovou cenou 20,00 USD za kus.
-   6a. Fyzický výdej ze skladu pro množství 1 při ceně 21,25 USD za kus.
-   7. Je provedena uzávěrka skladu. Vzhledem k tomu, že finančně aktualizovaná transakce FIFO je propojena s existujícím příjmem, budou tyto transakce vzájemně vyrovnány a nebudou provedeny žádné úpravy.

Nová průběžná průměrná cena bude odrážet průměrnou hodnotu finančně a fyzicky aktualizovaných transakcí ve výši 27,50 Kč. 

Následující obrázek ukazuje účinek volby skladového modelu LIFO na tuto sérii transakcí při použití označení propojení mezi výdeji a příjmy. 

![Metoda LIFO s označením.](./media/lifowithmarking.gif) 

**Klíč k diagramu**

- Skladové transakce jsou reprezentovány svislými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad časovou osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod časovou osou.
- Nad (nebo pod) každou svislou šipkou je zadána hodnota skladové transakce ve formátu Množství@Jednotková cena.
- Hodnota skladové transakce uzavřená do závorek označuje, že skladová transakce je fyzicky zaúčtována do skladu.
- Hodnota skladové transakce neuzavřená do závorek označuje, že skladová transakce je finančně zaúčtována do skladu.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou a označeny popiskem *Uzávěrka skladu*.
- Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými šikmými přerušovanými šipkami směřujícími od určitého příjmu k výdeji.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]