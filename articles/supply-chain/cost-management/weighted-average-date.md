---
title: Denní vážený průměr se zahrnutím fyzické hodnoty a označením
description: Datum váženého průměru je skladovým modelem založeným na principu váženého průměru, kde jsou výdeje ze skladu oceňovány průměrnou cenou položek přijatých na sklad v jednotlivých dnech období uzávěrky skladu.
author: JennySong-SH
ms.date: 03/04/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28991
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1497cb08f4cc5a455c832b9bf125c309cd90aa3d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672115"
---
# <a name="weighted-average-date-with-include-physical-value-and-marking"></a>Denní vážený průměr se zahrnutím fyzické hodnoty a označením

[!include [banner](../includes/banner.md)]

*Denní vážený průměr* je model zásob založený na průměru vypočítaném vynásobením každé složky (transakce položky) koeficientem (nákladová cena) odrážejícím její důležitost (množství) za každý den v období. Jinými slovy, tento model zásob přiřazuje náklady na výdejové transakce na základě průměrné hodnoty všech zásob přijatých během každého dne plus veškerých zásob na skladě z předchozího dne.

Když spustíte uzávěrku zásob pomocí modelu zásob Denní vážený průměr, existují dva způsoby, jak lze vytvořit vyrovnání. Typicky jsou všechny příjmy vyrovnány jedním virtuálním výdejem, který představuje celkové přijaté množství i celkovou hodnotu. Tento virtuální výdej má odpovídající virtuální příjem, kterým jsou výdeje vyrovnány. Tímto způsobem budou mít všechny výdeje každý den stejnou průměrnou cenu. Virtuální výdej a virtuální účtenku lze považovat za virtuální převod. Tento virtuální převod se označuje jako *vážený průměr – převod uzávěrky skladu*. Proto se tato metoda vyrovnání nazývá *souhrnné vyrovnání s váženým průměrem*. Existuje-li pouze jeden příjem, mohou jím být vyrovnány všechny výdeje a nebude vytvořen žádný virtuální převod. Tento způsob vyrovnání se označuje jako *přímé vyrovnání*. Zásoby, které jsou k dispozici po ukončení inventury, jsou oceněny váženým průměrem z posledního dne předchozího období a zahrnuty do výpočtu denního váženého průměru v následujícím období.

Princip denního váženého průměru můžete přepsat tak, že označíte skladové transakce, aby byl příjem určitých položek vyrovnán konkrétním výdejem. Pravidelná uzávěrka skladu je vyžadována, když používáte model zásob denního váženého průměru k vytváření vyrovnání a úpravě hodnoty výdejů podle principu denního váženého průměru. Dokud nespustíte uzavření zásob, jsou transakce vydávání oceňovány průběžným průměrem, kdy došlo k fyzickým a finančním aktualizacím. Pokud nepoužíváte označování, průběžný průměr se vypočítá při provedení fyzické nebo finanční aktualizace.

U metody ocenění skladu denním váženým průměrem se každý den používá následující vzorec:

*Náklady* = \[(*Q*<sub>*b*</sub> × *P*<sub>*b*</sub>) + &#x2211;<sub>*n*</sub>(*Q*<sub>*n*</sub> × *P*<sub>*n*</sub>)\] ÷ (*Q*<sub>*b*</sub> + &#x2211;<sub>*n*</sub>*Q*<sub>*n*</sub>)

- *Q* = Množství transakce
- *P* = Cena transakce

Jinými slovy, vážený průměr nákladů se rovná počátečnímu množství krát počáteční cena plus součet každého množství účtenky krát jeho cena příjmu, to vše děleno počátečním množstvím plus součtem množství příjmu.

Při uzávěrce skladu je výpočet proveden denně během období uzávěrky.

> [!NOTE]
> Další informace o vyrovnání naleznete v tématu [Uzávěrka skladu](inventory-close.md).

V následujících příkladech je znázorněn dopad použití denního váženého průměru v pěti konfiguracích:

- Přímé vyrovnání s použitím data váženého průměru bez volby **Zahrnout fyzickou hodnotu**
- Souhrnné vyrovnání s použitím data váženého průměru bez volby **Zahrnout fyzickou hodnotu**.
- Přímé vyrovnání s použitím data váženého průměru s volbou **Zahrnout fyzickou hodnotu**
- Souhrnné vyrovnání s použitím data váženého průměru s volbou **Zahrnout fyzickou hodnotu**
- Datum váženého průměru s použitím označení

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Přímé vyrovnání s použitím data váženého průměru bez volby Zahrnout fyzickou hodnotu

Princip přímého vyrovnání vytváří vyrovnání přímo mezi příjmy a výdeji, bez vytváření dalších transakcí se zásobami. V systému je tato metoda přímého vyrovnání použita v následujících situacích:

- V daném období byl zaúčtován jeden příjem a jeden nebo několik výdejů.
- V daném období byly zaúčtovány pouze výdeje a na skladě jsou položky z předchozí uzávěrky.

V tomto příkladu není políčko **Zahrnout fyzickou hodnotu** na stránce **skupině modelů položek** pro vydaný produkt zaškrtnuto. Následující schéma znázorňuje tyto transakce:

**Den 1:**

- 1a. Fyzický příjem ve skladu pro množství 10 při ceně 10,00 USD za kus
- 1b. Finanční příjem ve skladu pro množství 10 při ceně 10,00 USD za kus
- 2a. Fyzický příjem ve skladu pro množství 10 při ceně 20,00 USD za kus
- 3a. Fyzický výdej ze skladu pro množství 1 při ceně 10,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).
- 3b. Finanční výdej ze skladu pro množství 1 při ceně 10,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).

**Den 2:**

- 4a. Fyzický příjem ve skladu pro množství 1 při ceně 25,00 USD za kus
- 5a. Fyzický příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
- 5b. Finanční příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
- 6a. Finanční výdej ze skladu pro množství 1 při ceně 20,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).

**Den 3:**

- 7\. Je provedena uzávěrka skladu. Na základě metody denního váženého průměru systém používá metodu přímého vyrovnání pro 30. prosinec (30. 12.), protože ke 30. prosinci je finančně aktualizována pouze jedna účtenka. V tomto příkladu je vytvořeno jedno vyrovnání mezi transakcemi 1b a 3b. Je provedena úprava 10,00 USD, aby se hodnota transakce 3b zvýšila na 20,00. Dne 31. prosince (31. 12.) se neprovádí žádná úprava ani vyrovnání, protože 31. prosince nejsou žádné finančně aktualizované výdeje.

Následující diagram ukazuje tuto sérii transakcí a dopad použití váženého průměru jako skladového modelu a principu přímého vyrovnání bez možnosti **Zahrnovat fyzickou hodnotu**.

![Přímé vyrovnání s použitím data váženého průměru bez volby Zahrnout fyzickou hodnotu.](media/weighted-average-date-direct-settlement-without-include-physical-value.png)

**Vysvětlivky k diagramu:**

- Skladové transakce jsou reprezentovány svislými šipkami.
- Fyzické transakce jsou znázorněny kratšími světle šedými šipkami.
- Finanční transakce jsou znázorněny delšími černými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod osou.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Data jsou oddělena tenkými černými svislými čarami. Kalendářní data jsou uvedena ve spodní části diagramu.
- Uzávěrky skladu jsou reprezentovány červenými svislými přerušovanými čarami.
- Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými šikmými přerušovanými šipkami směřujícími od určitého příjmu k výdeji.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Souhrnné vyrovnání s použitím data váženého průměru bez volby Zahrnout fyzickou hodnotu

Když je v období více příjmů, denní vážený průměr používá princip souhrnného vyrovnání, kdy všechny příjmy v jednom dni jsou sečteny do transakce s názvem *Uzávěrka skladu – denní vážený průměr*. Všechny příjmy v tomto dni budou vyrovnány výdejem nově vytvořené transakce zásob. Všechny výdeje v tomto dni budou vyrovnány příjmem nové transakce zásob. Pokud budou po uzávěrce skladu hodnota na skladě zásoby, hodnota zásob na skladě je zahrnuta do transakce příjmu transakce uzávěrky skladu s váženým průměrem.

Následující schéma znázorňuje tyto transakce:

**Den 1:**

- 1a. Fyzický příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
- 1b. Finanční příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
- 2a. Fyzický příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
- 2b. Finanční příjem ve skladu pro množství 1 při ceně 22,00 USD za kus
- 3a. Fyzický výdej ze skladu pro množství 1 při ceně 16,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).
- 3b. Finanční výdej ze skladu pro množství 1 při ceně 16,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).

**Den 2:**

- 4a. Fyzický příjem ve skladu pro množství 1 při ceně 25,00 USD za kus
- 5a. Fyzický příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
- 5b. Finanční příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
- 6a. Fyzický výdej ze skladu pro množství 1 při ceně 23,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).

**Den 3:**

- 7\. Je provedena uzávěrka skladu.
- 7a. Je vytvořena transakce Uzávěrka skladu – vážený průměr finančního výdeje, která představuje součet vyrovnání všech finančních příjmů zásob.

    - Transakce 1b je vyrovnána za množství 1 s vyrovnanou částkou 10,00 USD.
    - Transakce 2b je vyrovnána za množství 1 s vyrovnanou částkou 22,00 USD.
    - Transakce 7a je vytvořena pro množství 2 s vyrovnanou částkou 32,00 USD. Tato transakce kompenzuje součet dvou příjmových transakcí, které jsou v daném období finančně aktualizovány.

- 7b. Jako protiúčet pro finančně zaúčtované výdeje je vytvořen finanční příjem transakce uzávěrky skladu s použitím váženého průměru.

    - Transakce 3b je vyrovnána za množství 1 s vyrovnanou částkou 16,00 USD. Tato transakce není upravena, protože se jedná o vážený průměr finančně zaúčtovaných transakcí za 1. prosinec (12/1).
    - Transakce 7b je vytvořena pro množství 2 s finanční částkou 32,00 USD a vyrovnanou částkou 16,00 USD k vyrovnání transakce 3b. Tato transakce kompenzuje součet jedné výdejové transakce, která je v daném období finančně aktualizována. Transakce zůstává otevřená, protože je stále jedna jednotka skladem.

Následující schéma ilustruje tuto sérii transakcí a dopad volby váženého průměru jako skladového modelu a principu souhrnného vyrovnání bez možnosti **Zahrnovat fyzickou hodnotu**.

![Souhrnné vyrovnání s použitím data váženého průměru bez volby Zahrnout fyzickou hodnotu.](media/weighted-average-date-summarized-settlement-without-include-physical-value.png)

**Vysvětlivky k diagramu:**

- Skladové transakce jsou reprezentovány svislými šipkami.
- Fyzické transakce jsou znázorněny kratšími světle šedými šipkami.
- Finanční transakce jsou znázorněny delšími černými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod osou.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Data jsou oddělena tenkými černými svislými čarami. Kalendářní data jsou uvedena ve spodní části diagramu.
- Uzávěrky skladu jsou reprezentovány červenými svislými přerušovanými čarami.
- Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými šikmými přerušovanými šipkami směřujícími od určitého příjmu k výdeji.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Přímé vyrovnání s použitím data váženého průměru s volbou Zahrnout fyzickou hodnotu

V aktuální verzi produktu možnost **Zahrnovat fyzickou hodnotu** funguje se skladovým modelem denního váženého průměru jinak než ve starších verzích produktu. Když zaškrtnete políčko **Zahrnovat fyzickou hodnotu** pro položku na stránce **Skupina modelů zboží**, systém použije fyzicky aktualizované příjmy při výpočtu odhadované nákladové ceny výdeje nebo průběžného průměru. Výdeje v průběhu období budou zaúčtovány na základě této odhadované nákladové ceny. Při uzávěrce skladu budou finančně aktualizované příjmy vzaty v potaz pouze ve výpočtu váženého průměru.

Následující schéma znázorňuje tyto transakce:

**Den 1:**

- 1a. Fyzický příjem ve skladu pro množství 10 při ceně 10,00 USD za kus
- 1b. Finanční příjem ve skladu pro množství 10 při ceně 10,00 USD za kus
- 2a. Fyzický příjem ve skladu pro množství 10 při ceně 20,00 USD za kus
- 3a. Fyzický výdej ze skladu pro množství 1 při ceně 15,00 USD (průběžná průměrná hodnota fyzicky a finančně zaúčtovaných transakcí).
- 3b. Finanční výdej ze skladu pro množství 1 při ceně 15,00 USD (průběžná průměrná hodnota fyzicky a finančně zaúčtovaných transakcí).

**Den 2:**

- 4a. Fyzický příjem ve skladu pro množství 1 při ceně 25,00 USD za kus
- 5a. Fyzický příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
- 5b. Finanční příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
- 6a. Fyzický výdej ze skladu pro množství 1 při ceně 21,25 USD (průběžná průměrná hodnota fyzicky a finančně zaúčtovaných transakcí).

**Den 3:**

- 7\. Je provedena uzávěrka skladu. Na základě metody denního váženého průměru systém používá metodu přímého vyrovnání pro 30. prosinec (30. 12.), protože ke 30. prosinci je finančně aktualizována pouze jedna účtenka. V tomto příkladu je vytvořeno jedno vyrovnání mezi transakcemi 1b a 3b. K 30. 12. není u vydání provedena žádná úprava. Ani ke dni 31. prosince (31. 12.) se neprovádí žádná úprava ani vyrovnání, protože 31. prosince nejsou žádné finančně aktualizované výdeje.

Následující diagram ukazuje tuto sérii transakcí a dopad použití váženého průměru jako skladového modelu a principu přímého vyrovnání s možností **Zahrnovat fyzickou hodnotu**.

![Přímé vyrovnání váženého průměru s možností Zahrnovat fyzickou hodnotu.](media/weighted-average-date-direct-settlement-with-include-physical-value.png)

**Vysvětlivky k diagramu:**

- Skladové transakce jsou reprezentovány svislými šipkami.
- Fyzické transakce jsou znázorněny kratšími světle šedými šipkami.
- Finanční transakce jsou znázorněny delšími černými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod osou.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Data jsou oddělena tenkými černými svislými čarami. Kalendářní data jsou uvedena ve spodní části diagramu.
- Uzávěrky skladu jsou reprezentovány červenými svislými přerušovanými čarami.
- Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými šikmými přerušovanými šipkami směřujícími od určitého příjmu k výdeji.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Souhrnné vyrovnání s použitím data váženého průměru s volbou Zahrnout fyzickou hodnotu

V aktuální verzi produktu možnost **Zahrnovat fyzickou hodnotu** funguje se skladovým modelem váženého průměru jinak než ve starších verzích produktu. Když zaškrtnete políčko **Zahrnovat fyzickou hodnotu** pro položku na stránce **Skupina modelů zboží**, systém použije fyzicky aktualizované příjmy při výpočtu odhadované nákladové ceny nebo průběžného průměru. Výdeje v průběhu období budou zaúčtovány na základě této odhadované nákladové ceny. Při uzávěrce skladu budou finančně aktualizované příjmy vzaty v potaz pouze ve výpočtu váženého průměru. Používáte-li jako skladový model vážený průměr, doporučujeme provádět uzávěrku skladu měsíčně. V tomto příkladu souhrnného vyrovnání denního váženého průměru je u skladového modelu označeno, že má obsahovat fyzickou hodnotu.

Následující schéma znázorňuje tyto transakce:

**Den 1:**

- 1a. Fyzický příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
- 1b. Finanční příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
- 2a. Fyzický příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
- 2b. Finanční příjem ve skladu pro množství 1 při ceně 22,00 USD za kus
- 3a. Fyzický výdej ze skladu pro množství 1 při ceně 16,00 USD (průběžná průměrná hodnota fyzicky a finančně zaúčtovaných transakcí).
- 3b. Finanční výdej ze skladu pro množství 1 při ceně 16,00 USD (průběžná průměrná hodnota fyzicky a finančně zaúčtovaných transakcí).

**Den 2:**

- 4a. Fyzický příjem ve skladu pro množství 1 při ceně 25,00 USD za kus
- 5a. Fyzický příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
- 5b. Finanční příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
- 6a. Fyzický výdej ze skladu pro množství 1 při ceně 23,67 USD (průběžná průměrná hodnota fyzicky a finančně zaúčtovaných transakcí).

**Den 3:**

- 7\. Je provedena uzávěrka skladu.
- 7a. Je vytvořena transakce Uzávěrka skladu – vážený průměr finančního výdeje, která představuje součet vyrovnání všech finančních příjmů zásob.

    - Transakce 1b je vyrovnána za množství 1 s vyrovnanou částkou 10,00 USD.
    - Transakce 2b je vyrovnána za množství 1 s vyrovnanou částkou 22,00 USD.
    - Transakce 7a je vytvořena pro množství 2 s vyrovnanou částkou 32,00 USD. Tato transakce kompenzuje součet dvou příjmových transakcí, které jsou v daném období finančně aktualizovány.

- 7b. Jako protiúčet pro finančně zaúčtované výdeje je vytvořen finanční příjem transakce uzávěrky skladu s použitím váženého průměru.

    - Transakce 3b je vyrovnána za množství 1 s vyrovnanou částkou 16,00 USD. Tato transakce není upravena, protože se jedná o vážený průměr finančně zaúčtovaných transakcí za 1. prosinec (12/1).
    - Transakce 7b je vytvořena pro množství 2 s finanční částkou 32,00 USD a vyrovnanou částkou 16,00 USD k vyrovnání transakce 3b. Tato transakce kompenzuje součet jedné výdejové transakce, která je v daném období finančně aktualizována. Transakce zůstává otevřená, protože je stále jedna jednotka skladem.

Následující diagram ukazuje tuto sérii transakcí a dopad použití váženého průměru jako skladového modelu a principu souhrnného vyrovnání bez možnosti **Zahrnovat fyzickou hodnotu**.

![Souhrnné vyrovnání váženého průměru s možností Zahrnovat fyzickou hodnotu.](media/weighted-average-date-summarized-settlement-with-include-physical-value.png)

**Vysvětlivky k diagramu:**

- Skladové transakce jsou reprezentovány svislými šipkami.
- Fyzické transakce jsou znázorněny kratšími světle šedými šipkami.
- Finanční transakce jsou znázorněny delšími černými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod osou.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Data jsou oddělena tenkými černými svislými čarami. Kalendářní data jsou uvedena ve spodní části diagramu.
- Uzávěrky skladu jsou reprezentovány červenými svislými přerušovanými čarami.
- Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými šikmými přerušovanými šipkami směřujícími od určitého příjmu k výdeji.

## <a name="weighted-average-date-when-marking-is-used"></a>Datum váženého průměru s použitím označení

Termínem označení se popisuje proces, který umožňuje propojit transakci výdeje s transakcí příjmu, neboli je označit jako propojené. Označení lze provést před zaúčtováním transakce nebo po ní. Označení lze provést tehdy, pokud chcete zjistit přesné náklady skladu při zaúčtování transakce, nebo při provedení uzávěrky skladu.

Předpokládejme například, že oddělení pro servisní služby odběratelům přijalo spěšnou objednávku od některého důležitého odběratele. Vzhledem k tomu, že se jedná o spěšnou objednávku, bude nutné při splnění požadavku zákazníka za tuto položku zaplatit více. Přitom si musíte být jisti, že pro fakturu této prodejní objednávky se náklady na tuto skladovou položku odrazí v marži nebo v nákladech na prodané zboží.

Při zaúčtování nákupní objednávky bude ve skladu zaznamenán příjem s náklady 120,00 USD. Je-li dokument prodejní objednávky propojen s nákupní objednávkou před zaúčtováním dodacího listu nebo faktury, budou náklady na prodané zboží činit 120,00 USD namísto aktuální průběžné průměrné hodnoty nákladů na položku. Pokud jsou dodací list nebo faktura zaúčtovány ještě před vytvořením označení, budou náklady na prodané zboží zaúčtovány s použitím průběžné průměrné nákladové ceny.

I před provedením uzávěrky skladu lze tyto dvě transakce vzájemně propojit.

Když je transakce příjmu propojena s transakcí výdeje, nebude metoda vyhodnocení vybraná pro skupinu skladových modelů položky vzata v potaz a tyto transakce budou v systému vzájemně vyrovnány.

Před zaúčtováním transakce je možné označit transakci výdeje s příjmem. Toto označení lze provést na řádku prodejní objednávky na stránce **Podrobnosti prodejní objednávky**. Můžete zobrazit otevřené transakce příjmu na stránce **Označení**.

Po zaúčtování transakce je možné také označit transakci výdeje s příjmem. Můžete spárovat nebo označit transakci výdeje pro transakci otevřených příjmů u naskladněné položky z deníku úpravy zaúčtované inventury.

Následující schéma znázorňuje tyto transakce:

**Den 1:**

- 1a. Fyzický příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
- 1b. Finanční příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
- 2a. Fyzický příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
- 2b. Finanční příjem ve skladu pro množství 1 při ceně 22,00 USD za kus
- 3a. Fyzický výdej ze skladu pro množství 1 při ceně 16,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).
- 3b. Finanční výdej ze skladu pro množství 1 při ceně 16,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).
- 3c. Finanční výdej zásob pro transakci 3b je označen jako finanční výdej zásob pro transakci 2b.

**Den 2:**

- 4a. Fyzický příjem ve skladu pro množství 1 při ceně 25,00 USD za kus
- 5a. Fyzický příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
- 5b. Finanční příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
- 6a. Fyzický výdej ze skladu pro množství 1 při ceně 23,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).

**Den 3:**

- 7\. Je provedena uzávěrka skladu. Na základě principu značení, které využívá metodu váženého průměru, jsou označené transakce vzájemně vyrovnány. V tomto příkladu se transakce 3b vyrovná proti transakci 2b a úprava pro 6,00 USD se zaúčtuje do transakce 3b, aby se hodnota dostala na 22,00 USD. V tomto příkladu nejsou prováděna žádná další vyrovnání, protože uzavření vytváří vyrovnání pouze pro finančně aktualizované transakce.

Následující schéma ukazuje tuto sérii transakcí a dopad použití váženého průměru jako skladového modelu s označením.

![Vážený průměr s označením.](media/weighted-average-date-with-marking.png)

**Vysvětlivky k diagramu:**

- Skladové transakce jsou reprezentovány svislými šipkami.
- Fyzické transakce jsou znázorněny kratšími světle šedými šipkami.
- Finanční transakce jsou znázorněny delšími černými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod osou.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Data jsou oddělena tenkými černými svislými čarami. Kalendářní data jsou uvedena ve spodní části diagramu.
- Uzávěrky skladu jsou reprezentovány červenými svislými přerušovanými čarami.
- Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými šikmými přerušovanými šipkami směřujícími od určitého příjmu k výdeji.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
