---
title: Datum váženého průměru
description: Datum váženého průměru je skladovým modelem založeným na principu váženého průměru, kde jsou výdeje ze skladu oceňovány průměrnou cenou položek přijatých na sklad v jednotlivých dnech období uzávěrky skladu.
author: AndersGirke
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 28991
ms.assetid: 945d5088-a99d-4e54-bc42-d2bd61c61e22
ms.search.region: Global
ms.search.industry: Retail
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9963c17d8ac1854a42cac2a0e19615f13e8cc006
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "355396"
---
# <a name="weighted-average-date"></a>Datum váženého průměru

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Datum váženého průměru je skladový model založený na principu váženého průměru. Pro princip váženého průměru jsou vydání ze skladu zváženy pomocí průměrné hodnoty položek přijatých do skladu pro každý den v období uzávěrky skladu. 

Při spuštění uzávěrky skladu s použitím data váženého průměru budou všechny denní příjmy vyrovnány s jedním virtuálním výdejem. Tento virtuální výdej obsahuje celkové přijaté množství a hodnotu za daný den. Virtuální výdej má odpovídající virtuální příjem, kterým jsou výdeje vyrovnány. Proto budou mít všechny příjmy stejnou průměrnou cenu. Na virtuální výdej a příjem lze nahlížet jako na virtuální převod, označovaný také jako *převod uzávěrky skladu s váženým průměrem*”. 

Pokud dojde pouze k jednomu příjmu k datu nebo před ním, není nutné počítat průměrnou hodnotu. Protože všechny výdeje jsou vyrovnány z daného příjmu, virtuální převod nebude vytvořen. Podobně pokud dojde k výdejům pouze v den s daným datem, nejsou k dispozici žádné příjmy, ze kterých by bylo možné vypočítat průměrnou hodnotu, a virtuální přenosy nebudou vytvořeny. Při používání data váženého průměru můžete označit skladové transakce tak, aby byl příjem určitých položek vyrovnán konkrétním výdejem. V takovém případě nepoužíváte pravidlo data váženého průměru. Používáte-li jako skladový model datum váženého průměru, doporučujeme provádět uzávěrku skladu měsíčně. 

Následující vzorec se používá pro výpočet nákladové metody s datem váženého průměru: 

Vážený průměr = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q*n* × P*n*\]) ÷ (Q1 + Q2 + Q*n*) 

Při uzávěrce skladu je výpočet proveden denně prostřednictvím období uzávěrky, jak je uvedeno na následujícím obrázku. 

![Model denního výpočtu data váženého průměru](./media/weightedaveragedatedailycalculationmodel.gif) 

Skladové transakce, které opustí sklad, jako například prodejní objednávky, deníky zásob a výrobních zakázky, probíhají v odhadované nákladové ceně k datu zaúčtování. Tato odhadovaná nákladová cena se také označuje jako průběžná průměrná nákladová cena. K datu uzávěrky skladu systém analyzuje skladové transakce za předchozí období, předchozí dny a pro aktuální den. Tato analýza slouží k určení, která z následujících metod uzávěrky má být použita:

-   Přímé vyrovnání
-   Souhrnné vyrovnání

Jako vyrovnání jsou označována zaúčtování uzávěrky skladu, při nichž jsou výdeje přiřazeny ke správnému váženému průměru k datu uzávěrky. 

**Poznámka:** Další informace o vyrovnání naleznete v článku o skladových uzávěrkách. V následujících příkladech je znázorněn dopad použití váženého průměru v pěti konfiguracích:

-   Přímé vyrovnání s použitím data váženého průměru bez volby **Zahrnout fyzickou hodnotu**
-   Souhrnné vyrovnání s použitím data váženého průměru bez volby **Zahrnout fyzickou hodnotu**
-   Přímé vyrovnání s použitím data váženého průměru s volbou **Zahrnout fyzickou hodnotu**
-   Souhrnné vyrovnání s použitím data váženého průměru s volbou **Zahrnout fyzickou hodnotu**
-   Datum váženého průměru s použitím označení

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Přímé vyrovnání s použitím data váženého průměru bez volby Zahrnout fyzickou hodnotu
Aktuální verze používá stejnou metodu přímého vyrovnání, která je použitá pro datum váženého průměru v předchozích verzích. V systému jsou provedena přímá vyrovnání mezi příjmy a výdeji. Systém tuto metodu přímého vyrovnání používá v určitých situacích:

-   V daném období byl zaúčtován jeden příjem a jeden nebo několik výdejů.
-   V daném období byly zaúčtovány pouze výdeje a na skladě jsou položky z předchozí uzávěrky.

V následujícím scénáři byl zaúčtován finančně aktualizovaný příjem a výdej. Během skladové uzávěrky systém vyrovná příjem přímo oproti výdeji a pro daný výdej nebude nutné provádět žádnou úpravu nákladové ceny. 

Následující obrázek znázorňuje tyto transakce:

-   1a. Je provedena aktualizace fyzického příjmu ve skladu pro množství 5 při ceně 10,00 USD za kus.
-   1b. Je provedena aktualizace finančního příjmu ve skladu pro množství 5 při ceně 10,00 USD za kus.
-   2a. Je provedena aktualizace fyzického výdeje ve skladu pro množství 2 při ceně 10,00 USD za kus.
-   2b. je provedena aktualizace finančního výdeje ve skladu pro množství 2 při ceně 10,00 USD za kus.
-   3. Je provedena uzávěrka skladu s použitím metody přímého vyrovnání s cílem vyrovnat finanční příjem skladu oproti finančnímu výdeji skladu.

![Přímé vyrovnání s použitím data váženého průměru bez volby Zahrnout fyzickou hodnotu](./media/weightedaveragedatedirectsettlementwithoutincludephysicalvalue.gif) 

**Popis obrázku:**

-   Skladové transakce jsou reprezentovány svislými šipkami.
-   Příjmy do skladu jsou reprezentovány svislými šipkami nad časovou osou.
-   Výdeje ze skladu jsou reprezentovány svislými šipkami pod časovou osou.
-   Nad nebo pod každou svislou šipkou je zadána hodnota skladové transakce ve formě *Množství*@*Jednotková cena*.
-   Pokud je hodnota skladové transakce uzavřená do hranatých závorek, označuje, že skladová transakce je fyzicky zaúčtována do skladu.
-   Pokud není hodnota skladové transakce uzavřená do hranatých závorek, označuje, že skladová transakce je finančně zaúčtována do skladu.
-   Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
-   Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
-   Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou a označeny popiskem *Uzávěrka skladu*.
-   Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými tečkovanými šipkami, směřujícími diagonálně od určitého příjmu k výdeji.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Souhrnné vyrovnání s použitím data váženého průměru bez volby Zahrnout fyzickou hodnotu
Vážený průměr je založen na principu, kdy všechny příjmy v období uzávěrky jsou sečteny do nové transakce převodu zásob. Tato transakce se nazývá *Uzávěrka skladu – vážený průměr*. Všechny příjmy pro daný den budou vyrovnány oproti výdeji nově vytvořené transakce převodu skladu. Všechny výdeje pro daný den budou vyrovnány oproti příjmu nové transakce převodu skladu. Pokud bude po uzávěrce skladu hodnota zásob na skladě kladná, budou sečteny hodnota zásob na skladě a hodnota zásob v rámci nové transakce převodu skladu (příjem). Pokud bude po uzávěrce skladu hodnota zásob na skladě záporná, bude hodnota zásob na skladě a hodnota zásob tvořena souhrnem jednotlivých položek, které nebyly úplně vyrovnány. 

V níže uvedeném scénáři bylo během daného období zaúčtováno několik finančně aktualizovaných příjmů a výdejů. Při skladové uzávěrce systém vyhodnotí každý den s cílem určit postup při uzávěrce jednotlivých dní. 

Následující obrázek znázorňuje tyto transakce: 

**Den 1:**

-   1a. Fyzický příjem ve skladu byl aktualizován pro množství 3 při ceně 15,00 USD za kus.
-   1b. Finanční příjem ve skladu byl aktualizován pro množství 3 při ceně 15,00 USD za kus.
-   2a. Fyzický výdej ze skladu pro množství 1 při průběžné průměrné ceně 15,00 USD.
-   2b. Finanční výdej ze skladu pro množství 1 při průběžné průměrné ceně 15,00 USD.

V systému bude pro den 1 použita metoda přímého vyrovnání. 

**Den 2:**

-   3a. Fyzický výdej ze skladu pro množství 1 při průběžné průměrné ceně 15,00 USD
-   3b. Finanční výdej ze skladu pro množství 1 při průběžné průměrné ceně 15,00 USD

V systému bude pro den 2 použita metoda přímého vyrovnání. 

**Den 3:**

-   4a. Fyzický výdej ze skladu pro množství 1 při průběžné průměrné ceně 15,00 USD
-   4b. Finanční výdej ze skladu pro množství 1 při průběžné průměrné ceně 15,00 USD
-   5a. Fyzický příjem ve skladu pro množství 1 při ceně 17,00 USD za kus
-   5b. Finanční příjem ve skladu pro množství 1 při ceně 17,00 USD za kus

Je provedena uzávěrka skladu. Bude třeba provést přímé vyrovnání, protože existuje více příjmů přes větší počet dnů.

-   7a. Je vytvořen finanční výdej transakce uzávěrky skladu s použitím váženého průměru pro množství 2 při ceně 32,00 USD s cílem sečíst vyrovnání všech finančních příjmů ve skladu k datu, které dosud nebylo uzavřeno.
-   7b. Jako protiúčet k bodu 7a je vytvořen finanční příjem transakce uzávěrky skladu s použitím váženého průměru.

Systém vygeneruje a zaúčtuje souhrnnou transakci převodu zásob. Navíc aplikace systém vyrovná všechny příjmy pro daný den a skladové zásoby pro předchozí dny s ohledem na souhrnnou transakci převodu zásob výdeje. Všechny výdeje pro daný den budou vyrovnány oproti sumarizované transakci příjmu pro převod skladu. Nákladová cena s použitím váženého průměru je vypočtena jako 16,00 USD. Pro výdej bude použita úprava 1,00 USD s cílem upravit náklady váženého průměru. Nová nákladová cena s použitím průběžného váženého průměru bude 16,00 USD. 

Následující obrázek ilustruje tuto sérii transakcí, včetně dopadu volby váženého průměru jako skladového modelu a principu souhrnného vyrovnání bez možnosti **Zahrnovat fyzickou hodnotu**. 

![Souhrnné vyrovnání s použitím data váženého průměru bez volby Zahrnout fyzickou hodnotu](./media/weightedaveragedatesummarizedsettlementwithoutincludephysicalvalue.gif) 

**Popis obrázku**

-   Skladové transakce jsou reprezentovány svislými šipkami.
-   Příjmy do skladu jsou reprezentovány svislými šipkami nad časovou osou.
-   Výdeje ze skladu jsou reprezentovány svislými šipkami pod časovou osou.
-   Nad nebo pod každou svislou šipkou je zadána hodnota skladové transakce ve formě *Množství*@*Jednotková cena*.
-   Pokud je hodnota skladové transakce uzavřená do hranatých závorek, označuje, že skladová transakce je fyzicky zaúčtována do skladu.
-   Pokud není hodnota skladové transakce uzavřená do hranatých závorek, označuje, že skladová transakce je finančně zaúčtována do skladu.
-   Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
-   Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
-   Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou a označeny popiskem *Uzávěrka skladu*.
-   Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými tečkovanými šipkami, směřujícími diagonálně od určitého příjmu k výdeji.
-   Plné červené diagonální šipky znázorňují transakce příjmu, pro které je prováděno vyrovnání s transakcí výdeje vytvořenou systémem.
-   Plná zelená diagonální šipka reprezentuje transakci příjmu vygenerovanou systémem vyrovnání, s níž je vyrovnána původně zaúčtovaná transakce výdeje.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Přímé vyrovnání s použitím data váženého průměru s volbou Zahrnout fyzickou hodnotu
Aktuální verze používá stejnou metodu přímého vyrovnání pro datum váženého průměru, která je použita v předchozích verzích. V systému jsou provedena přímá vyrovnání mezi příjmy a výdeji. Systém tuto metodu přímého vyrovnání používá v určitých situacích:

-   V daném období byl zaúčtován jeden příjem a jeden nebo několik výdejů.
-   V daném období byly zaúčtovány pouze výdeje a ve skladě se nacházejí skladové položky z předchozí uzávěrky.

Pokud označíte pole **Zahrnovat fyzickou hodnotu** pro položku na stránce **Skupina modelů zboží**, systém použije fyzicky aktualizované příjmy při výpočtu odhadované nákladové ceny nebo průběžného průměru. Výdeje budou během daného období zaúčtovány na základě odhadované nákladové ceny. Při uzávěrce skladu budou finančně aktualizované příjmy vzaty v potaz pouze ve výpočtu váženého průměru.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Souhrnné vyrovnání s použitím data váženého průměru s volbou Zahrnout fyzickou hodnotu
Pokud označíte pole **Zahrnovat fyzickou hodnotu** pro položku na stránce **Skupina modelů zboží**, systém použije fyzicky aktualizované příjmy při výpočtu odhadované nákladové ceny nebo průběžného průměru. Výdeje budou během daného období zaúčtovány na základě odhadované nákladové ceny. Při uzávěrce skladu budou finančně aktualizované příjmy vzaty v potaz pouze ve výpočtu váženého průměru. Vyrovnání váženého průměru je založeno na principu, že příjmy v období uzávěrky jsou sečteny do nové transakce převodu zásob, která se nazývá *Uzávěrka skladu – vážený průměr*. Všechny příjmy pro daný den budou vyrovnány oproti výdeji nově vytvořené transakce převodu skladu. Všechny výdeje pro daný den budou vyrovnány oproti příjmu nové transakce převodu skladu. Pokud bude po uzávěrce skladu hodnota zásob na skladě kladná, budou sečteny hodnota zásob na skladě a hodnota zásob v rámci nové transakce převodu skladu (příjem). Pokud bude po uzávěrce skladu hodnota zásob na skladě záporná, bude hodnota zásob na skladě a hodnota zásob tvořena souhrnem jednotlivých položek, které nebyly úplně vyrovnány.

## <a name="weighted-average-date-when-marking-is-used"></a>Datum váženého průměru s použitím označení
Označování je proces, který umožňuje propojit transakci výdeje s transakcí příjmu. Označení lze provést před zaúčtováním transakce nebo po ní. Označení lze provést tehdy, pokud chcete zjistit přesné náklady skladu při zaúčtování transakce, nebo při provedení uzávěrky skladu. 

Předpokládejme například, že oddělení pro servisní služby odběratelům přijalo spěšnou objednávku od některého důležitého odběratele. Vzhledem k tomu, že se jedná o spěšnou objednávku, bude nutné při splnění požadavku zákazníka za tuto položku zaplatit více. Přitom si musíte být jisti, že pro fakturu této prodejní objednávky se náklady na tuto skladovou položku odrazí v marži nebo v nákladech na prodané zboží. Při zaúčtování nákupní objednávky bude ve skladu zaznamenán příjem s náklady 120,00 USD. Dokument prodejní objednávky je propojen s nákupní objednávkou před zaúčtováním dodacího listu nebo faktury. Náklady na prodané zboží budou místo aktuální průběžné průměrné ceny položky činit 120,00 USD. Pokud jsou dodací list nebo faktura zaúčtovány ještě před vytvořením propojení, budou náklady na prodané zboží zaúčtovány s použitím průběžné průměrné nákladové ceny. I před provedením uzávěrky skladu lze tyto dvě transakce vzájemně propojit. Pokud je transakce příjmu propojena s transakcí výdeje, nebude metoda vyhodnocení definovaná ve skupině skladových modelů položky vzata v potaz. Místo toho systém vyrovná tyto transakce navzájem. 

Před zaúčtováním transakce je možné označit transakci výdeje s příjmem. To lze provést na řádku prodejní objednávky na stránce **Podrobnosti prodejní objednávky**. Můžete zobrazit otevřené transakce příjmu na stránce **Označení**. Po zaúčtování transakce je možné označit transakci výdeje s příjmem. Můžete spárovat nebo označit transakci výdeje pro transakci otevřených příjmů u naskladněné položky z deníku úpravy zaúčtované inventury. Následující obrázek znázorňuje tyto transakce:

-   1a. Fyzický příjem ve skladu pro množství 1 při nákladové ceně 10,00 USD za kus
-   1b. Finanční příjem ve skladu pro množství 1 při nákladové ceně 10,00 USD za kus
-   2a. Fyzický příjem ve skladu pro množství 1 při nákladové ceně 20,00 USD za kus
-   2b. Finanční příjem ve skladu pro množství 1 při nákladové ceně 20,00 USD za kus
-   3a. Fyzický příjem ve skladu pro množství 1 při nákladové ceně 25,00 USD za kus
-   4a. Fyzický příjem ve skladu pro množství 1 při nákladové ceně 30,00 USD za kus
-   4b. Finanční příjem ve skladu pro množství 1 při nákladové ceně 30,00 USD za kus
-   5a. Fyzický výdej ze skladu pro množství 1 při ceně 21,25 USD (průběžná průměrná hodnota finančních a fyzických aktualizovaných transakcí).
-   5b. Finanční výdej ze skladu pro množství 1 je před zaúčtováním transakce propojen s příjmem ve skladu 2b. Tato transakce je zaúčtována s nákladovou cenou 20,00 USD.
-   6a. Fyzický výdej ze skladu pro množství 1 při ceně 21,25 USD.
-   7. Je provedena uzávěrka skladu. Vzhledem k tomu, že finančně aktualizovaná transakce je propojena s existujícím příjmem, budou tyto transakce vzájemně vyrovnány a nebudou provedeny žádné úpravy.

Nová průběžná průměrná cena bude odrážet průměrnou hodnotu finančně a fyzicky aktualizovaných transakcí ve výši 27,50 USD. Následující obrázek ilustruje tuto sérii transakcí, včetně dopadu použití váženého průměru jako skladového modelu data a s označením.

![Datum váženého průměru s označením](./media/weightedaveragedatewithmarking.gif) 

**Popis obrázku:**

-   Skladové transakce jsou reprezentovány svislými šipkami.
-   Příjmy do skladu jsou reprezentovány svislými šipkami nad časovou osou.
-   Výdeje ze skladu jsou reprezentovány svislými šipkami pod časovou osou.
-   Nad nebo pod každou svislou šipkou je zadána hodnota skladové transakce ve formě *Množství*@*Jednotková cena*.
-   Pokud je hodnota skladové transakce uzavřená do hranatých závorek, označuje, že skladová transakce je fyzicky zaúčtována do skladu.
-   Pokud není hodnota skladové transakce uzavřená do hranatých závorek, označuje, že skladová transakce je finančně zaúčtována do skladu.
-   Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
-   Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
-   Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou a označeny popiskem *Uzávěrka skladu*.
-   Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými tečkovanými šipkami, směřujícími diagonálně od určitého příjmu k výdeji.




