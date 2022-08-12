---
title: Metoda LIFO s fyzickou hodnotou a označením
description: U skladového modelu LIFO (Last in, First out) jsou poslední (nejnovější) příjmy vydány jako první. Výdeje ze skladu jsou vyrovnávány vůči posledním příjmům na sklad podle data skladové transakce.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55021
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1acc103291c5d648ac7e179a598348cd9cc2a93
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135562"
---
# <a name="lifo-with-physical-value-and-marking"></a>Metoda LIFO s fyzickou hodnotou a označením

[!include [banner](../includes/banner.md)]

LIFO je metoda řízení zásob a oceňování, kdy zásoby, které byly vyrobeny nebo pořízeny jako poslední, jsou prodány, použity nebo vyřazeny jako první. Během procesu uzávěrky skladu v Microsoft Dynamics 365 Supply Chain Management systém vytvoří vyrovnání, kde se poslední příjemka spáruje s prvním výdejem atd. Princip vypořádání a párování je založen na finančním datu transakcí se zásobami. Předběžné posouzení vypořádání a úprav lze provést spuštěním procesu přepočtu zásob.

Princip LIFO můžete přepsat tak, že označíte skladové transakce, aby byl příjem určitých položek vyrovnán konkrétním výdejem. Pravidelná uzávěrka skladu je vyžadována, když používáte model zásob LIFO k vytváření vyrovnání a úpravě hodnoty výdejů podle principu LIFO. Dokud nespustíte proces uzavření zásob, jsou transakce vydávání oceňovány průběžným průměrem, kdy došlo k fyzickým a finančním aktualizacím. Pokud nepoužíváte označování, průběžný průměr se vypočítá při provedení fyzické nebo finanční aktualizace.

Následující příklady ilustrují dopad použití metody LIFO ve třech různých konfiguracích:

- Metoda LIFO bez možnosti **Zahrnovat fyzickou hodnotu**
- Metoda LIFO s možností **Zahrnovat fyzickou hodnotu**
- Metoda LIFO s označením

## <a name="lifo-without-the-include-physical-value-option"></a>Metoda LIFO bez možnosti Zahrnovat fyzickou hodnotu

V tomto příkladu není políčko **Zahrnout fyzickou hodnotu** ve skupině modelů položek pro vydaný produkt zaškrtnuto. Následující obrázek znázorňuje tyto transakce:

- 1a. Fyzický příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
- 1b. Finanční příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
- 2a. Fyzický příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
- 2b. Finanční příjem ve skladu pro množství 1 při ceně 22,00 USD za kus
- 3a. Fyzický výdej ze skladu pro množství 1 při ceně 16,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).
- 3b. Finanční výdej ze skladu pro množství 1 při ceně 16,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí).
- 4a. Fyzický příjem ve skladu pro množství 1 při ceně 25,00 USD za kus
- 5a. Fyzický příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
- 5b. Finanční příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
- 6a. Fyzický výdej ze skladu pro množství 1 při ceně 23,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí)
- 7\. Je provedena uzávěrka skladu. Na základě metody LIFO bude první finančně zaúčtovaný výdej vyrovnán posledním finančně zaúčtovaným příjmem atd. V tomto příkladu je vytvořeno jedno vyrovnání mezi 5b a 3b. Úprava částky 14,00 USD bude provedena u 3b a výsledná konečná cena bude 30,00 USD.

Následující obrázky ukazují účinky skladového modelu FIFO na tuto sérii transakcí, když není použita možnost **Zahrnovat fyzickou hodnotu**.

![Metoda LIFO bez možnosti Zahrnovat fyzickou hodnotu.](./media/lifo-without-including-physical-value.png)

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

## <a name="lifo-with-the-include-physical-value-option"></a>Metoda LIFO s možností Zahrnovat fyzickou hodnotu

Pokud zaškrtnete políčko **Zahrnovat fyzickou hodnotu** pro položku na stránce **Skupiny modelů zboží**, systém pro výpočet průběžné průměrné ceny použije transakce fyzického i finančního příjmu. V případě potřeby budou v systému také provedeny úpravy fyzicky aktualizované transakce výdeje. Pokud je zaškrtnutí políčka **Zahrnovat fyzickou hodnotu** odstraněno, budou při uzávěrce skladu s použitím skladového modelu LIFO provedena vyrovnání pouze pro finančně aktualizované transakce.

Následující obrázek znázorňuje tyto transakce:

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
- 7\. Je provedena uzávěrka skladu. Na základě metody LIFO bude první finančně zaúčtovaný výdej vyrovnán posledním finančně zaúčtovaným příjmem atd. V tomto příkladu je vytvořeno jedno vyrovnání mezi 3b a 5b. Úprava částky 14,00 USD bude provedena u 3b a výsledná konečná cena bude 30,00 USD. Transakce 6a dále bude upravena podle nákladů příjmové transakce 4a. Systém tyto transakce nevyrovná, protože příjem je zaúčtován pouze fyzicky, ale nikoli finančně. Místo toho bude k transakci fyzického výdeje zaúčtována pouze úprava 1,33 USD a výsledná upravená cena bude 25,00 USD.

Následující obrázek ukazuje účinek skladového modelu LIFO na tuto sérii transakcí, když není použita možnost **Zahrnovat fyzickou hodnotu**.

![Metoda LIFO s možností Zahrnovat fyzickou hodnotu.](./media/lifo-with-included-physical-value.png)

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

## <a name="lifo-with-marking"></a>Metoda LIFO s označením

Termínem označení se popisuje proces, který umožňuje propojit transakci výdeje s transakcí příjmu, neboli je označit jako propojené. Označení lze provést před zaúčtováním transakce nebo po ní. Označení lze provést tehdy, pokud chcete zjistit přesné náklady skladu při zaúčtování transakce nebo při provedení uzávěrky skladu. Předpokládejme například, že oddělení služeb odběratelům přijalo spěšnou objednávku od důležitého odběratele. Vzhledem k tomu, že se jedná o spěšnou objednávku, bude nutné pro splnění požadavku zákazníka za tuto položku zaplatit více.

Přitom si musíte být jisti, že pro fakturu prodejní objednávky se náklady na tuto skladovou položku odrazí v marži nebo v nákladech na prodané zboží. Při zaúčtování nákupní objednávky bude ve skladu zaznamenán příjem s náklady 120,00 USD. Je-li tento dokument prodejní objednávky propojen s nákupní objednávkou před zaúčtováním dodacího listu nebo faktury, budou náklady na prodané zboží činit 120,00 USD, namísto aktuální průběžné průměrné hodnoty nákladů na položku. Pokud jsou faktura nebo dodací list prodejní objednávky zaúčtovány ještě předtím, než dojde k tomuto propojení, budou náklady na prodané zboží zaúčtovány s použitím průběžné průměrné ceny.

I před provedením uzávěrky skladu lze tyto dvě transakce vzájemně propojit.

Před zaúčtováním transakce je možné označit transakci výdeje s příjmem. Toto označení můžete provést z řádku prodejní objednávky na stránce **Podrobnosti prodejní objednávky** výběrem možnosti **Zásoby \> Označení** na záložce **Řádky prodejní objednávky**. Můžete zobrazit otevřené transakce příjmu na stránce **Označení**.

Po zaúčtování transakce je možné také označit transakci výdeje s příjmem. Můžete spárovat nebo označit transakci výdeje pro transakci otevřených příjmů u naskladněné položky z deníku úpravy zaúčtované inventury.

Následující obrázek znázorňuje tyto transakce:

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
- 6a. Fyzický výdej ze skladu pro množství 1 při ceně 23,00 USD (průběžná průměrná cena finančně zaúčtovaných transakcí)
- 7\. Je provedena uzávěrka skladu. Na základě principu značení, které využívá metodu LIFO, jsou označené transakce vzájemně vyrovnány. V tomto příkladu se 3b vyrovná proti 2b a úprava pro 6,00 USD se zaúčtuje do 3b, aby se hodnota dostala na 22,00 USD. V tomto příkladu nejsou prováděna žádná další vyrovnání, protože uzavření vytváří vyrovnání pouze pro finančně aktualizované transakce.

Nová průběžná průměrná cena bude odrážet průměrnou hodnotu finančně a fyzicky aktualizovaných transakcí ve výši 17,50 Kč.

Následující obrázek ukazuje účinek volby skladového modelu LIFO na tuto sérii transakcí při použití označení propojení mezi výdeji a příjmy.

![Metoda LIFO s označením.](./media/lifo-with-marking.png)

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
- Vyrovnání a označení, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými šikmými přerušovanými šipkami směřujícími od určitého příjmu k výdeji.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
