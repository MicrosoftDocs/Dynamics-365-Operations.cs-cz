---
title: "Vážený průměr s fyzickou hodnotou a označením"
description: "Vážený průměr představuje skladový model založený na principu váženého aritmetického průměru. V tomto modelu jsou při uzávěrce skladové výdeje oceňovány průměrnou cenou položek přijatých na sklad plus jakékoli množství na skladě z předcházejícího období."
author: AndersGirke
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 65501
ms.assetid: 25041ff0-bafe-484d-a94a-e1772ad43204
ms.search.region: Global
ms.search.industry: Retail
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ec7f1ef643d864a2729642d78d19fc43d5f6a7fb
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="weighted-average-with-physical-value-and-marking"></a>Vážený průměr s fyzickou hodnotou a označením

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Vážený průměr představuje skladový model založený na principu váženého aritmetického průměru. V tomto modelu jsou při uzávěrce skladové výdeje oceňovány průměrnou cenou položek přijatých na sklad plus jakékoli množství na skladě z předcházejícího období.

Když spustíte uzávěrku skladu, všechny příjmy jsou vyrovnány jedním virtuálním výdejem, který představuje celkové přijaté množství i celkovou hodnotu. Tento virtuální výdej má odpovídající virtuální příjem, kterým jsou výdeje vyrovnány. Tímto způsobem budou mít všechny výdeje stejnou průměrnou cenu. Virtuální výdej a příjem lze zobrazit jako virtuální převod pojmenovaný vážený průměr – převod uzávěrky skladu.

Existuje-li pouze jeden příjem, mohou jím být vyrovnány všechny výdeje a virtuální převod nebude vytvořen. 

Při používání váženého průměru můžete označit skladové transakce tak, aby místo pravidla váženého aritmetického průměru byl příjem určitých položek vyrovnán konkrétním výdejem. 

Používáte-li jako skladový model vážený průměr, doporučujeme provádět uzávěrku skladu měsíčně. 

Pro výpočet ceny váženým aritmetickým průměrem se používá následující vzorec:
-   Vážený průměr = (Q1\*P1 + Q2\*P2 + Qn\*Pn) / (Q1 + Q2 + Qn)

Skladové transakce opouštějící výdeje zásob. Jedná se o prodejní objednávky, deníky zásob a výrobní zakázky, ke kterým došlo při dosažení odhadované nákladové ceny k datu zaúčtování. Této odhadované nákladové ceně se také říká průběžný průměr. Systém při uzávěrce skladu provede analýzu skladových transakcí za předchozí a aktuální období a určí, jaká metoda provádění uzávěrky se použije.
-   Přímé vyrovnání
-   Souhrnné vyrovnání

Jako vyrovnání jsou označována zaúčtování uzávěrky skladu, při nichž jsou výdeje přiřazeny ke správnému váženému průměru k datu uzávěrky. V následujících příkladech je znázorněn dopad použití váženého průměru v pěti různých konfiguracích:
-   Přímé vyrovnání váženého průměru bez možnosti Zahrnovat fyzickou hodnotu
-   Souhrnné vyrovnání váženého průměru bez možnosti Zahrnovat fyzickou hodnotu
-   Přímé vyrovnání váženého průměru s možností Zahrnovat fyzickou hodnotu
-   Souhrnné vyrovnání váženého průměru s možností Zahrnovat fyzickou hodnotu
-   Vážený průměr s označením

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Přímé vyrovnání váženého průměru bez možnosti Zahrnovat fyzickou hodnotu
Princip přímého vyrovnání je stejný jako pro vážený průměr ve starších verzích. V systému jsou provedena přímá vyrovnání mezi příjmy a výdeji. V systému je tato metoda přímého vyrovnání použita v určitých specifických situacích:
-   V daném období byl zaúčtován jeden příjem a jeden nebo několik výdejů
-   V daném období byly zaúčtovány pouze výdeje a na skladě jsou položky z předchozí uzávěrky

V následujícím scénáři byl zaúčtován finančně aktualizovaný příjem a výdej. Během skladové uzávěrky v systému bude příjem vyrovnán přímo oproti výdeji a pro daný výdej nebude nutné provádět žádnou úpravu nákladové ceny. V grafu jsou znázorněny následující transakce.
-   1a. zaúčtovaný fyzický příjem 5 kusů po 10 Kč
-   1b. zaúčtovaný finanční příjem 5 kusů po 10 Kč
-   2a. zaúčtovaný fyzický výdej 2 kusů po 10 Kč
-   2b. zaúčtovaný finanční výdej 2 kusů po 10 Kč
-   3. Uzávěrka skladu je provedena metodou přímého vyrovnání tak, aby došlo k vyrovnání finančního příjmu s finančním výdejem.

Následující diagram ilustruje tuto sérii transakcí, včetně dopadu volby váženého průměru jako skladového modelu a principu přímého vyrovnání bez možnosti Zahrnovat fyzickou hodnotu. 

![Metoda Vážený průměr DS bez možnosti Zahrnovat fyzickou hodnotu](./media/weightedaveragedirectsettlementwithoutincludephysicalvalue.gif) 

**Klíč k diagramu**
- Skladové transakce jsou reprezentovány svislými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad časovou osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod časovou osou.
- Nad (nebo pod) každou svislou šipkou je zadána hodnota skladové transakce ve formátu Quantity@Unitprice.
- Hodnota skladové transakce uzavřená do hranatých závorek označuje, že skladová transakce je fyzicky zaúčtována do skladu.
- Hodnota skladové transakce bez hranatých závorek označuje, že skladová transakce je finančně zaúčtována do skladu.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou a označeny popiskem Uzávěrka skladu.
- Vyrovnání vytvořená při uzávěrce skladu znázorňují červené tečkované šipky směřující šikmo od příjmu k výdeji.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Souhrnné vyrovnání váženého průměru bez možnosti Zahrnovat fyzickou hodnotu
Vážený průměr používá princip vyrovnání, kdy všechny příjmy v období uzávěrky jsou sečteny v podobě převodu, která se nazývá Uzávěrka skladu – vážený průměr. Všechny příjmy v období budou vyrovnány výdejem nově vytvořené transakce převodu zásob. Všechny výdeje v období  budou vyrovnány příjmem nové transakce převodu zásob. Pokud bude po uzávěrce skladu hodnota zásob na skladě kladná, budou sečteny hodnota zásob na skladě a hodnota zásob v rámci nové transakce převodu skladu (příjem). Pokud bude po uzávěrce skladu hodnota zásob na skladě záporná, bude hodnota zásob na skladě a hodnota zásob tvořena souhrnem jednotlivých položek, které nebyly úplně vyrovnány. V následujícím scénáři bylo finančně zaúčtováno několik příjmů a jeden výdej. 

Při uzávěrce skladu aplikace systém vygeneruje a zaúčtuje souhrnnou transakci převodu zásob a vyrovná příjmy za období s touto souhrnnou transakcí převodu zásob. Všechny výdeje zaúčtované ve stejném období budou vyrovnány souhrnnou transakcí převodu zásob. Vypočítaný vážený průměr činí 15 Kč. Výdej byl původně zaúčtován s odhadovanou nákladovou cenou 14,67 Kč. K transakci výdeje bude proto vytvořena a zaúčtována úprava ve výši 0,33 Kč. Ke dni uzávěrky jsou na skladě 3 kusy v celkové hodnotě 45 Kč. 

V grafu jsou uvedeny následující transakce:
-   1a. Zaúčtovaný fyzický příjem 2 kusů po 11 Kč.
-   1b. Zaúčtovaný finanční příjem 2 kusů po 14 Kč.
-   2a. Zaúčtovaný fyzický příjem 1 kusu za 12 Kč.
-   2b. Zaúčtovaný finanční příjem 1 kusu za 16 Kč.
-   3a. Zaúčtovaný fyzický výdej 1 kusu za 14,67 Kč (průběžný průměr).
-   3b. Zaúčtovaný finanční výdej 1 kusu za 14,67 Kč (průběžný průměr).
-   4a. Zaúčtovaný fyzický příjem 1 kusu za 14 Kč.
-   4b. Zaúčtovaný finanční příjem 1 kusu za 16 Kč.
-   5. Je provedena uzávěrka skladu.
-   6a. Je vytvořena transakce „Uzávěrka skladu – vážený průměr“ finančního výdeje, která představuje součet vyrovnání všech finančních příjmů zásob.
-   6b. Je vytvořena transakce „Uzávěrka skladu – vážený průměr“ finančního příjmu, která vyrovnává transakci 5a.

Následující diagram ilustruje tuto sérii transakcí, včetně dopadu volby váženého průměru jako skladového modelu a principu souhrnného vyrovnání bez možnosti Zahrnovat fyzickou hodnotu. 

![Metoda Vážený průměr SS bez možnosti Zahrnovat fyzickou hodnotu](./media/weightedaveragesummarizedsettlementwithoutincludephysicalvalue.gif) 

**Klíč k diagramu**
- Skladové transakce jsou reprezentovány svislými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad časovou osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod časovou osou.
- Nad (nebo pod) každou svislou šipkou je zadána hodnota skladové transakce ve formátu Quantity@Unitprice.
- Hodnota skladové transakce uzavřená do hranatých závorek označuje, že skladová transakce je fyzicky zaúčtována do skladu.
- Hodnota skladové transakce bez hranatých závorek označuje, že skladová transakce je finančně zaúčtována do skladu.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou a označeny popiskem Uzávěrka skladu.
- Vyrovnání vytvořená při uzávěrce skladu znázorňují červené tečkované šipky směřující šikmo od příjmu k výdeji.
- Červené šipky znázorňují vyrovnání transakcí příjmu transakcí výdeje vytvořenou systémem.
- Zelená šipka znázorňuje vyrovnávací transakci příjmu generovanou systémem, kterou je vyrovnána původně zaúčtovaná transakce výdeje.

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Přímé vyrovnání váženého průměru s možností Zahrnovat fyzickou hodnotu
Parametr Zahrnovat fyzickou hodnotu funguje se skladovým modelem váženého průměru jinak než ve starších verzích produktu. Vyberte políčko Zahrnout fyzickou hodnotu pro položku ve formuláři Skupina modelů zboží. Systém potom při výpočtu odhadované nákladové ceny nebo při spuštění průměrné hodnoty použije fyzicky aktualizované příjmy. Výdeje budou během daného období zaúčtovány na základě odhadované nákladové ceny. Při uzávěrce skladu budou při výpočtu váženého aritmetického průměru zohledněny pouze finančně zaúčtované příjmy. Používáte-li jako skladový model vážený průměr, doporučujeme provádět uzávěrku skladu měsíčně. V tomto příkladu přímého vyrovnání váženého průměru je u skupiny modelu položky označeno, že má obsahovat fyzickou hodnotu. 

V níže uvedeném grafu jsou znázorněny následující transakce:
-   1a. Zaúčtovaný fyzický příjem 1 kusu za 11 Kč.
-   1b. Zaúčtovaný finanční příjem 1 kusu za 10 Kč.
-   2a. Zaúčtovaný fyzický příjem 1 kusu za 15 Kč.
-   3a. Zaúčtovaný fyzický výdej 1 kusu za 12,50 Kč (cena odpovídá výši průběžného průměru, protože je zohledněna fyzicky přijatá hodnota).
-   3b. Zaúčtovaný finanční výdej 1 kusu za 12,50 Kč (cena odpovídá výši průběžného průměru, protože je zohledněna fyzicky přijatá hodnota).
-   4. Je provedena uzávěrka skladu. Při uzávěrce skladu systém bude ignorovat všechny skladové transakce, které byly pouze fyzicky aktualizovány. Namísto toho bude použit princip přímého vyrovnání, protože existuje pouze jeden finanční příjem. Úprava ve výši 2,50 Kč se zaúčtuje do skladové transakce, která byla finančně vydána k datu uzávěrky skladu. Po uzávěrce skladu budou zásoby na skladě v množství 1 s průběžnou průměrnou cenou 15,00 Kč.

Následující diagram ilustruje tuto sérii transakcí, včetně dopadu volby váženého průměru jako skladového modelu a principu přímého vyrovnání s možností Zahrnovat fyzickou hodnotu. 

![Metoda Vážený průměr DS s možností Zahrnovat fyzickou hodnotu](./media/weightedaveragedirectsettlementwithincludephysicalvalue.gif) 

**Klíč k diagramu**
- Skladové transakce jsou reprezentovány svislými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad časovou osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod časovou osou.
- Nad (nebo pod) každou svislou šipkou je zadána hodnota skladové transakce ve formátu Quantity@Unitprice.
- Hodnota skladové transakce uzavřená do hranatých závorek označuje, že skladová transakce je fyzicky zaúčtována do skladu.
- Hodnota skladové transakce bez hranatých závorek označuje, že skladová transakce je finančně zaúčtována do skladu.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou a označeny popiskem Uzávěrka skladu.
- Vyrovnání vytvořená při uzávěrce skladu znázorňují červené tečkované šipky směřující šikmo od příjmu k výdeji.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Souhrnné vyrovnání váženého průměru s možností Zahrnovat fyzickou hodnotu
Parametr Zahrnovat fyzickou hodnotu funguje s váženým průměrem jinak než ve starších verzích. Vyberte políčko Zahrnout fyzickou hodnotu pro položku na stránce Skupina modelů zboží. Systém potom při výpočtu odhadované nákladové ceny nebo při spuštění průměrné hodnoty použije fyzicky aktualizované příjmy. Výdeje v průběhu období budou zaúčtovány na základě této odhadované nákladové ceny. Při uzávěrce skladu budou při výpočtu váženého aritmetického průměru zohledněny pouze finančně zaúčtované příjmy. Používáte-li jako skladový model vážený průměr, doporučujeme provádět uzávěrku skladu měsíčně. V tomto příkladu souhrnného vyrovnání váženého průměru je u skladového modelu označeno, že má obsahovat fyzickou hodnotu. 

V grafu jsou uvedeny následující transakce:
-   1a. Zaúčtovaný fyzický příjem 2 kusů po 11 Kč.
-   1b. Zaúčtovaný finanční příjem 2 kusů po 14 Kč.
-   2. Byla provedena aktualizace fyzického příjmu ve skladu pro množství 1 při ceně 10,00 Kč za kus.
-   3a. Zaúčtovaný fyzický příjem 1 kusu za 12 Kč.
-   3b. Zaúčtovaný finanční příjem 1 kusu za 16 Kč.
-   4a. Zaúčtovaný fyzický výdej 1 kusu za 13,50 Kč (cena odpovídá výši průběžného průměru, protože je zohledněna fyzicky přijatá hodnota).
-   4b. Zaúčtovaný finanční výdej 1 kusu za 13,50 Kč (cena odpovídá výši průběžného průměru, protože je zohledněna fyzicky přijatá hodnota).
-   5a. Zaúčtovaný fyzický příjem 1 kusu za 14 Kč.
-   5b. Zaúčtovaný finanční příjem 1 kusu za 16 Kč.
-   6. Je provedena uzávěrka skladu. Při uzávěrce skladu systém bude ignorovat všechny skladové transakce, které jsou aktualizovány pouze fyzicky. Namísto toho bude použit princip souhrnného vyrovnání, protože existuje pouze jeden finanční příjem. Úprava ve výši 1,50 Kč se zaúčtuje do skladové transakce, která byla finančně vydána k datu uzávěrky skladu. Po uzávěrce skladu budou zásoby na skladě v množství 3 s průběžnou průměrnou cenou 15,00 Kč.
-   7a. Je vytvořena transakce „Uzávěrka skladu – vážený průměr“ finančního výdeje, která představuje součet vyrovnání všech finančních příjmů zásob.
-   7b. Je vytvořena transakce „Uzávěrka skladu – vážený průměr“ finančního příjmu, která vyrovnává transakci 5a.

Následující diagram ilustruje tuto sérii transakcí, včetně dopadu volby váženého průměru jako skladového modelu a principu souhrnného vyrovnání bez možnosti Zahrnovat fyzickou hodnotu. 

![Metoda Vážený průměr SS s možností Zahrnovat fyzickou hodnotu](./media/weightedaveragesummarizedsettlementwithincludephysicalvalue.gif) 

**Klíč k diagramu**
- Skladové transakce jsou reprezentovány svislými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad časovou osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod časovou osou.
- Nad (nebo pod) každou svislou šipkou je zadána hodnota skladové transakce ve formátu Quantity@Unitprice.
- Hodnota skladové transakce uzavřená do hranatých závorek označuje, že skladová transakce je fyzicky zaúčtována do skladu.
- Hodnota skladové transakce bez hranatých závorek označuje, že skladová transakce je finančně zaúčtována do skladu.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například 1a). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou a označeny popiskem Uzávěrka skladu.
- Vyrovnání vytvořená při uzávěrce skladu znázorňují červené tečkované šipky směřující šikmo od příjmu k výdeji.
- Červené šipky znázorňují vyrovnání transakcí příjmu transakcí výdeje vytvořenou systémem.
- Zelená šipka znázorňuje vyrovnávací transakci příjmu generovanou systémem, kterou je vyrovnána původně zaúčtovaná transakce výdeje.

## <a name="weighted-average-with-marking"></a>Vážený průměr s označením
Termínem označení se popisuje proces, který umožňuje propojit transakci výdeje s transakcí příjmu, neboli je označit jako propojené. Označení lze provést před zaúčtováním transakce nebo po ní. Označení lze provést tehdy, pokud chcete zjistit přesné náklady skladu při zaúčtování transakce, nebo při provedení uzávěrky skladu. 

Předpokládejme například, že oddělení pro servisní služby odběratelům přijalo spěšnou objednávku od některého důležitého odběratele. Vzhledem k tomu, že se jedná o spěšnou objednávku, bude nutné při splnění požadavku zákazníka za tuto položku zaplatit více. Přitom si musíte být jisti, že pro fakturu této prodejní objednávky se náklady na tuto skladovou položku odrazí v marži nebo v nákladech na prodané zboží. 

Při zaúčtování nákupní objednávky bude ve skladu zaznamenán příjem s náklady 120,00 USD. Například dokument prodejní objednávky je propojen s nákupní objednávkou před zaúčtováním dodacího listu nebo faktury. Náklady na prodané zboží budou místo aktuální průběžné průměrné ceny položky činit 120,00 Kč. Pokud jsou dodací list nebo faktura zaúčtovány ještě před vytvořením propojení, budou náklady na prodané zboží zaúčtovány s použitím průběžné průměrné nákladové ceny. 

I před provedením uzávěrky skladu lze tyto dvě transakce vzájemně propojit. 

Příjmová transakce je propojena s transakcí výdeje. Metoda ocenění je poté vybraná pro skupinu modelů položky nebude brána v úvahu a systém vyrovná tyto transakce navzájem. 

Před zaúčtováním transakce je možné označit transakci výdeje s příjmem. To lze provést na řádku prodejní objednávky na stránce Podrobnosti prodejní objednávky. Můžete zobrazit otevřené transakce příjmu na stránce Označení. 

Po zaúčtování transakce je možné označit transakci výdeje s příjmem. Můžete spárovat nebo označit transakci výdeje pro transakci otevřených příjmů u naskladněné položky z deníku úpravy zaúčtované inventury. 

V níže uvedeném grafu jsou znázorněny následující transakce:
-   1a. Fyzický příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
-   1b. Finanční příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
-   2a. Fyzický příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
-   2b. Finanční příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
-   3a. Fyzický příjem ve skladu pro množství 1 při ceně 25,00 USD za kus
-   4a. Fyzický příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
-   4b. Finanční příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
-   5a. Fyzický výdej 1 kusu v ceně 21,25 Kč (průběžný průměr zaúčtovaných finančních a fyzických transakcí).
-   5b. Finanční výdej 1 kusu je před zaúčtováním transakce označený, že patří k příjmu 2b. Tato transakce je zaúčtována s cenou 20 Kč.
-   6a. Fyzický výdej 1 kusu za cenu 21,25 Kč.
-   7. Provedení uzávěrky skladu. Vzhledem k označení finančně zaúčtované transakce, že patří ke stávajícímu příjmu, budou tyto transakce vyrovnány mezi sebou a nevytvoří se žádná oprava.

Nová průběžná průměrná cena bude odrážet průměrnou hodnotu finančně a fyzicky aktualizovaných transakcí ve výši 27,50 USD. 

Následující diagram ilustruje tuto sérii transakcí, včetně dopadu volby váženého průměru jako skladového modelu s označením. 

![Vážený průměr s označením](./media/weightedaveragewithmarking.gif) 

**Klíč k diagramu**
- Skladové transakce jsou reprezentovány svislými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad časovou osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod časovou osou.
- Nad (nebo pod) každou svislou šipkou je zadána hodnota skladové transakce ve formátu Quantity@"Unitprice".
- Hodnota skladové transakce uzavřená do hranatých závorek označuje, že skladová transakce je fyzicky zaúčtována do skladu.
- Hodnota skladové transakce bez hranatých závorek označuje, že skladová transakce je finančně zaúčtována do skladu.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou a označeny popiskem Uzávěrka skladu.
- Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými tečkovanými šipkami, směřujícími diagonálně od určitého příjmu k výdeji.






