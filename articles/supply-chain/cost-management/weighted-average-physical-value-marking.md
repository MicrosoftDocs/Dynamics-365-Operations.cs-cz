---
title: Vážený průměr s fyzickou hodnotou a označením
description: Vážený průměr představuje skladový model založený na principu váženého aritmetického průměru. V tomto modelu jsou při uzávěrce skladové výdeje oceňovány průměrnou cenou položek přijatých na sklad plus jakékoli množství na skladě z předcházejícího období.
author: AndersGirke
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65501
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c124716b70be837573506a738ef2034397f2bda
ms.sourcegitcommit: addae271ddfc5a8b0721c23337f69916153db4cd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/21/2022
ms.locfileid: "8330219"
---
# <a name="weighted-average-with-physical-value-and-marking"></a>Vážený průměr s fyzickou hodnotou a označením

[!include [banner](../includes/banner.md)]

Vážený průměr je model zásob založený na průměru, který je výsledkem vynásobení každé složky (transakce položky) koeficientem (nákladová cena) odrážejícím její důležitost (množství). Jiným způsobem, jak to říci, je, že vážený průměr je model zásob, který přiřazuje náklady na emisní transakce na základě průměrné hodnoty všech zásob přijatých během období plus veškerých zásob na skladě z předchozího období.

Když spustíte uzávěrku zásob pomocí modelu váženého průměru zásob, existují dva způsoby, jak lze vytvořit vypořádání. Typicky jsou všechny příjmy vyrovnány jedním virtuálním výdejem, který představuje celkové přijaté množství i celkovou hodnotu. Tento virtuální výdej má odpovídající virtuální příjem, kterým jsou výdeje vyrovnány. Tímto způsobem budou mít všechny výdeje stejnou průměrnou cenu. Virtuální výdej a příjem lze zobrazit jako virtuální převod pojmenovaný vážený průměr – *převod uzávěrky skladu*. Tato metoda vypořádání se nazývá *souhrnné vypořádání s váženým průměrem*. Existuje-li pouze jeden příjem, mohou jím být vyrovnány všechny výdeje a virtuální převod nebude vytvořen. Tento způsob vypořádání se označuje jako *přímé vypořádání*. Zásoby, které jsou k dispozici po ukončení inventury, jsou oceněny váženým průměrem z předchozího období a zahrnuty do výpočtu váženého průměru v následujícím období.

Princip váženého průměru můžete přepsat tak, že označíte skladové transakce, aby byl příjem určitých položek vyrovnán konkrétním výdejem. Pravidelná uzávěrka skladu je vyžadována, když používáte model zásob váženého průměru k vytváření vyrovnání a úpravě hodnoty výdejů podle principu váženého průměru. Dokud nespustíte proces uzavření zásob, jsou transakce vydávání oceňovány průběžným průměrem, kdy došlo k fyzickým a finančním aktualizacím. Pokud nepoužíváte označování, průběžný průměr se vypočítá při provedení fyzické nebo finanční aktualizace.

Pro výpočet ceny váženým aritmetickým průměrem se používá následující vzorec:

- Vážený průměr = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q *n* × P *n*\]) ÷ (Q1 + Q2 + Q *n*)

Q = množství transakce  
P = cena transakce

Jako vyrovnání jsou označována zaúčtování uzávěrky skladu, při nichž jsou výdeje přiřazeny ke správnému váženému průměru k datu uzávěrky. V následujících příkladech je znázorněn dopad použití váženého průměru v pěti různých konfiguracích:

- Přímé vyrovnání váženého průměru bez možnosti **Zahrnovat fyzickou hodnotu**
- Souhrnné vyrovnání váženého průměru bez možnosti **Zahrnovat fyzickou hodnotu**
- Přímé vyrovnání váženého průměru s možností **Zahrnovat fyzickou hodnotu**
- Souhrnné vyrovnání váženého průměru s možností **Zahrnovat fyzickou hodnotu**
- Vážený průměr s označením

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Přímé vyrovnání váženého průměru bez možnosti Zahrnovat fyzickou hodnotu

Princip přímého vypořádání vytváří vypořádání přímo mezi příjmy a výdeji bez vytváření dalších transakcí se zásobami. V systému je tato metoda přímého vyrovnání použita v následujících situacích:

- V daném období byl zaúčtován jeden příjem a jeden nebo několik výdejů.
- V daném období byly zaúčtovány pouze výdeje a na skladě jsou položky z předchozí uzávěrky.

V tomto příkladu není políčko **Zahrnout fyzickou hodnotu** ve **skupině modelů položek** pro vydaný produkt zaškrtnuto. Následující obrázek znázorňuje tyto transakce:

- 1a. Fyzický příjem ve skladu pro množství 10 při ceně 10,00 USD za kus
- 1b. Finanční příjem ve skladu pro množství 10 při ceně 10,00 USD za kus
- 2a. Fyzický příjem ve skladu pro množství 10 při ceně 20,00 USD za kus
- 3a. Fyzický výdej ze skladu pro množství 1 při ceně 10,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).
- 3b. Finanční výdej ze skladu pro množství 1 při ceně 10,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).
- 4a. Fyzický výdej ze skladu pro množství 1 při ceně 10,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).
- 4b. Finanční výdej ze skladu pro množství 1 při ceně 10,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).
- 5a. Fyzický výdej ze skladu pro množství 1 při ceně 10,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).
- 6\. Je provedena uzávěrka skladu. Na základě metody váženého průměru systém používá metodu přímého zúčtování, protože v daném období je finančně aktualizována pouze jedna účtenka. V tomto příkladu je vytvořeno jedno vyrovnání mezi 1b a 3b a další mezi 1b a 4b. Neprovádí se žádná úprava, protože klouzavý průměr je stejný jako vážený průměr.

Následující diagram ilustruje tuto sérii transakcí, včetně dopadu volby váženého průměru jako skladového modelu a principu přímého vyrovnání bez možnosti **Zahrnovat fyzickou hodnotu**.

![Metoda WeightedAverage DS bez možnosti Zahrnovat fyzickou hodnotu.](media/weighted-average-direct-settlement-without-include-physical-value.png)

**Klíč k diagramu**

- Skladové transakce jsou reprezentovány svislými šipkami.
- Fyzické transakce jsou znázorněny kratšími světle šedými šipkami.
- Finanční transakce jsou znázorněny delšími černými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod osou.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Každé datum v diagramu je odděleno tenkou černou svislou čarou. Datum je uvedeno ve spodní části diagramu.
- Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou.
- Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými šikmými přerušovanými šipkami směřujícími od určitého příjmu k výdeji.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Souhrnné vyrovnání váženého průměru bez možnosti Zahrnovat fyzickou hodnotu

Když je v období více příjmů, vážený průměr používá princip souhrnného vyrovnání, kdy všechny příjmy v období uzávěrky jsou sečteny v podobě převodu, která se nazývá *Uzávěrka skladu – vážený průměr*. Všechny příjmy v období budou vyrovnány výdejem nově vytvořené transakce zásob. Všechny výdeje v období budou vyrovnány příjmem nové transakce zásob. Pokud budou po uzávěrce skladu hodnota na skladě zásoby, hodnota zásob na skladě je zahrnuta do transakce příjmu transakce uzávěrky skladu s váženým průměrem.

V grafu jsou uvedeny následující transakce:

- 1a. Fyzický příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
- 1b. Finanční příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
- 2a. Fyzický příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
- 2b. Finanční příjem ve skladu pro množství 1 při ceně 22,00 USD za kus
- 3a. Fyzický výdej ze skladu pro množství 1 při ceně 16,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).
- 3b. Finanční výdej ze skladu pro množství 1 při ceně 16,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).
- 4a. Fyzický příjem ve skladu pro množství 1 při ceně 25,00 USD za kus
- 5a. Fyzický příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
- 5b. Finanční příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
- 6a. Fyzický výdej ze skladu pro množství 1 při ceně 23,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).
- 7\. Je provedena uzávěrka skladu.
- 7a. Je vytvořena transakce Uzávěrka skladu – vážený průměr finančního výdeje, která představuje součet vyrovnání všech finančních příjmů zásob.
  - Transakce 1b je vypořádána za množství 1 s vypořádanou částkou 10,00 USD.
  - Transakce 2b je vypořádána za množství 1 s vypořádanou částkou 22,00 USD.
  - Transakce 5b je vypořádána za množství 1 s vypořádanou částkou 30,00 USD.
  - Transakce 7a. je vytvořena za množství 3 s vypořádanou částkou 62,00 USD. Tato transakce kompenzuje součet tří příjmových transakcí, které jsou v daném období finančně aktualizovány.
- 7b. Jako protiúčet k finančně zaúčtovaným výdejům je vytvořen finanční příjem transakce uzávěrky skladu s použitím váženého průměru.
  - Transakce 3b je vypořádána za množství 1 s vypořádanou částkou 20,67 USD. Tato transakce je upravena o 4,67 USD tak, aby byla původní hodnota místo 16,00 USD 20,67, což je vážený průměr finančně zaúčtovaných transakcí za dané období.
  - Transakce 7b. je vytvořena za množství 1 s vypořádanou částkou 20,67 USD k vykompenzování 3b. Tato transakce kompenzuje součet jedné výdejové transakce, která je v daném období finančně aktualizována.

Následující diagram ilustruje tuto sérii transakcí, včetně dopadu volby váženého průměru jako skladového modelu a principu souhrnného vyrovnání bez možnosti **Zahrnovat fyzickou hodnotu**.

![Metoda Vážený průměr SS bez možnosti Zahrnovat fyzickou hodnotu.](media/weighted-average-summarized-settlement-without-include-physical-value.png)

**Klíč k diagramu**

- Skladové transakce jsou reprezentovány svislými šipkami.
- Fyzické transakce jsou znázorněny kratšími světle šedými šipkami.
- Finanční transakce jsou znázorněny delšími černými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod osou.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Každé datum v diagramu je odděleno tenkou černou svislou čarou. Datum je uvedeno ve spodní části diagramu.
- Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou.
- Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými šikmými přerušovanými šipkami směřujícími od určitého příjmu k výdeji.

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Přímé vyrovnání váženého průměru s možností Zahrnovat fyzickou hodnotu

Parametr **Zahrnovat fyzickou hodnotu** funguje se skladovým modelem váženého průměru jinak než ve starších verzích produktu. Pokud vyberete pole **Zahrnovat fyzickou hodnotu** pro položku na formuláři **Skupina modelů zboží**, systém použije fyzicky aktualizované příjmy při výpočtu odhadované nákladové ceny výdeje nebo průběžného průměru. Výdeje v průběhu období budou zaúčtovány na základě této odhadované nákladové ceny. Při uzávěrce skladu budou při výpočtu váženého aritmetického průměru zohledněny pouze finančně zaúčtované příjmy.

V grafu jsou uvedeny následující transakce:

- 1a. Fyzický příjem ve skladu pro množství 10 při ceně 10,00 USD za kus
- 1b. Finanční příjem ve skladu pro množství 10 při ceně 10,00 USD za kus
- 2a. Fyzický příjem ve skladu pro množství 10 při ceně 20,00 USD za kus
- 3a. Fyzický výdej ze skladu pro množství 1 při ceně 15,00 USD (průběžná průměrná hodnota fyzicky a finančně zaúčtovaných transakcí).
- 3b. Finanční výdej ze skladu pro množství 1 při ceně 15,00 USD (průběžná průměrná hodnota fyzicky a finančně zaúčtovaných transakcí).
- 4a. Fyzický výdej ze skladu pro množství 1 při ceně 15,00 USD (průběžná průměrná hodnota fyzicky a finančně zaúčtovaných transakcí).
- 4b. Finanční výdej ze skladu pro množství 1 při ceně 15,00 USD (průběžná průměrná hodnota fyzicky a finančně zaúčtovaných transakcí).
- 5a. Fyzický výdej ze skladu pro množství 1 při ceně 15,00 USD (průběžná průměrná hodnota fyzicky a finančně zaúčtovaných transakcí).
- 6\. Je provedena uzávěrka skladu. Na základě metody váženého průměru systém používá metodu přímého zúčtování, protože v daném období je finančně aktualizována pouze jedna účtenka. V tomto příkladu je vytvořeno jedno vyrovnání mezi 1b a 3b a další mezi 1b a 4b. Transakce 3b a 4b jsou upraveny o −5,00 USD, aby se hodnota dostala na 10,00 USD.

Následující diagram ilustruje tuto sérii transakcí, včetně dopadu volby váženého průměru jako skladového modelu a principu přímého vyrovnání s možností **Zahrnovat fyzickou hodnotu**.

![Metoda Vážený průměr DS s možností Zahrnovat fyzickou hodnotu.](media/weighted-average-direct-settlement-with-include-physical-value.png)

**Klíč k diagramu**

- Skladové transakce jsou reprezentovány svislými šipkami.
- Fyzické transakce jsou znázorněny kratšími světle šedými šipkami.
- Finanční transakce jsou znázorněny delšími černými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod osou.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Každé datum v diagramu je odděleno tenkou černou svislou čarou. Datum je uvedeno ve spodní části diagramu.
- Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou.
- Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými šikmými přerušovanými šipkami směřujícími od určitého příjmu k výdeji.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Souhrnné vyrovnání váženého průměru s možností Zahrnovat fyzickou hodnotu

Parametr **Zahrnovat fyzickou hodnotu** funguje s váženým průměrem jinak než ve starších verzích. Vyberte políčko **Zahrnout fyzickou hodnotu** pro položku na stránce **Skupina modelů zboží**. Systém potom při výpočtu odhadované nákladové ceny nebo při spuštění průměrné hodnoty použije fyzicky aktualizované příjmy. Výdeje v průběhu období budou zaúčtovány na základě této odhadované nákladové ceny. Při uzávěrce skladu budou při výpočtu váženého aritmetického průměru zohledněny pouze finančně zaúčtované příjmy. Používáte-li jako skladový model vážený průměr, doporučujeme provádět uzávěrku skladu měsíčně. V tomto příkladu souhrnného vyrovnání váženého průměru je u skladového modelu označeno, že má obsahovat fyzickou hodnotu.

V grafu jsou uvedeny následující transakce:

- 1a. Fyzický příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
- 1b. Finanční příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
- 2a. Fyzický příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
- 2b. Finanční příjem ve skladu pro množství 1 při ceně 22,00 USD za kus
- 3a. Fyzický výdej ze skladu pro množství 1 při ceně 16,00 USD (průběžná průměrná hodnota fyzicky a finančně zaúčtovaných transakcí).
- 3b. Finanční výdej ze skladu pro množství 1 při ceně 16,00 USD (průběžná průměrná hodnota fyzicky a finančně zaúčtovaných transakcí).
- 4a. Fyzický příjem ve skladu pro množství 1 při ceně 25,00 USD za kus
- 5a. Fyzický příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
- 5b. Finanční příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
- 6a. Fyzický výdej ze skladu pro množství 1 při ceně 23,67 USD (průběžná průměrná hodnota fyzicky a finančně zaúčtovaných transakcí).
- 7\. Je provedena uzávěrka skladu.
- 7a. Je vytvořena transakce Uzávěrka skladu – vážený průměr finančního výdeje, která představuje součet vyrovnání všech finančních příjmů zásob.
  - Transakce 1b je vypořádána za množství 1 s vypořádanou částkou 10,00 USD.
  - Transakce 2b je vypořádána za množství 1 s vypořádanou částkou 22,00 USD.
  - Transakce 5b je vypořádána za množství 1 s vypořádanou částkou 30,00 USD.
  - Transakce 7a. je vytvořena za množství 3 s vypořádanou částkou 62,00 USD.  
- 7b. Jako protiúčet k finančně uzavřeným transakcí výdeje je vytvořen finanční příjem transakce uzávěrky skladu s použitím váženého průměru.
  - Transakce 3b je vypořádána za množství 1 s vypořádanou částkou 20,67 USD. Tato transakce je upravena o 4,67 USD tak, aby byla původní hodnota místo 16,00 USD 20,67, což je vážený průměr finančně zaúčtovaných transakcí za dané období.
  - Transakce 7b. je vytvořena za množství 1 s vypořádanou částkou 20,67 USD k vykompenzování 3b.

Následující diagram ilustruje tuto sérii transakcí, včetně dopadu volby váženého průměru jako skladového modelu a principu souhrnného vyrovnání bez možnosti **Zahrnovat fyzickou hodnotu**.

![Metoda WeightedAverage SS s možností Zahrnovat fyzickou hodnotu.](media/weighted-average-summarized-settlement-with-include-physical-value.png)

**Klíč k diagramu**

- Skladové transakce jsou reprezentovány svislými šipkami.
- Fyzické transakce jsou znázorněny kratšími světle šedými šipkami.
- Finanční transakce jsou znázorněny delšími černými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod osou.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Každé datum v diagramu je odděleno tenkou černou svislou čarou. Datum je uvedeno ve spodní části diagramu.
- Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou.
- Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými šikmými přerušovanými šipkami směřujícími od určitého příjmu k výdeji.

## <a name="weighted-average-with-marking"></a>Vážený průměr s označením

Termínem označení se popisuje proces, který umožňuje propojit transakci výdeje s transakcí příjmu, neboli je označit jako propojené. Označení lze provést před zaúčtováním transakce nebo po ní. Označení lze provést tehdy, pokud chcete zjistit přesné náklady skladu při zaúčtování transakce, nebo při provedení uzávěrky skladu.

Předpokládejme například, že oddělení pro servisní služby odběratelům přijalo spěšnou objednávku od některého důležitého odběratele. Vzhledem k tomu, že se jedná o spěšnou objednávku, bude nutné při splnění požadavku zákazníka za tuto položku zaplatit více. Přitom si musíte být jisti, že pro fakturu této prodejní objednávky se náklady na tuto skladovou položku odrazí v marži nebo v nákladech na prodané zboží.

Při zaúčtování nákupní objednávky bude ve skladu zaznamenán příjem s náklady 120,00 USD. Například dokument prodejní objednávky je propojen s nákupní objednávkou před zaúčtováním dodacího listu nebo faktury. Náklady na prodané zboží budou místo aktuální průběžné průměrné ceny položky činit 120,00 Kč. Pokud jsou dodací list nebo faktura zaúčtovány ještě před vytvořením propojení, budou náklady na prodané zboží zaúčtovány s použitím průběžné průměrné nákladové ceny.

I před provedením uzávěrky skladu lze tyto dvě transakce vzájemně propojit.

Příjmová transakce je propojena s transakcí výdeje. Metoda ocenění je poté vybraná pro skupinu modelů položky nebude brána v úvahu a systém vyrovná tyto transakce navzájem.

Před zaúčtováním transakce je možné označit transakci výdeje s příjmem. To lze provést na řádku prodejní objednávky na stránce **Podrobnosti prodejní objednávky**. Můžete zobrazit otevřené transakce příjmu na stránce **Označení**.

Po zaúčtování transakce je možné označit transakci výdeje s příjmem. Můžete spárovat nebo označit transakci výdeje pro transakci otevřených příjmů u naskladněné položky z deníku úpravy zaúčtované inventury.

V grafu jsou uvedeny následující transakce:

- 1a. Fyzický příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
- 1b. Finanční příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
- 2a. Fyzický příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
- 2b. Finanční příjem ve skladu pro množství 1 při ceně 22,00 USD za kus
- 3a. Fyzický výdej ze skladu pro množství 1 při ceně 16,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).
- 3b. Finanční výdej ze skladu pro množství 1 při ceně 16,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).
- 3c. Finanční výdej zásob pro 3b je označen jako finanční výdej zásob pro 2b.
- 4a. Fyzický příjem ve skladu pro množství 1 při ceně 25,00 USD za kus
- 5a. Fyzický příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
- 5b. Finanční příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
- 6a. Fyzický výdej ze skladu pro množství 1 při ceně 23,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).
- 7\. Je provedena uzávěrka skladu. Na základě principu značení, které využívá metodu váženého průměru, jsou označené transakce vzájemně vyrovnány. V tomto příkladu se 3b vyrovná proti 2b a úprava pro 6,00 USD se zaúčtuje do 3b, aby se hodnota dostala na 22,00 USD. V tomto příkladu nejsou prováděna žádná další vyrovnání, protože uzavření vytváří vyrovnání pouze pro finančně aktualizované transakce.

Následující diagram ilustruje tuto sérii transakcí, včetně dopadu volby váženého průměru jako skladového modelu s označením.

![Vážený průměr s označením.](media/weighted-average-with-marking.png)

**Klíč k diagramu**

- Skladové transakce jsou reprezentovány svislými šipkami.
- Fyzické transakce jsou znázorněny kratšími světle šedými šipkami.
- Finanční transakce jsou znázorněny delšími černými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod osou.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Každé datum v diagramu je odděleno tenkou černou svislou čarou. Datum je uvedeno ve spodní části diagramu.
- Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou.
- Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými šikmými přerušovanými šipkami směřujícími od určitého příjmu k výdeji.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
