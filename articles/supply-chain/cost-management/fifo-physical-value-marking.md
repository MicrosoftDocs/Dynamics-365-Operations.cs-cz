---
title: Metoda FIFO s fyzickou hodnotou a označením
description: Metoda (FIFO, First in, First out) představuje skladový model, ve kterém jsou nejprve vydávány první uskladněné položky. Finančně aktualizované výdeje ze skladu jsou vyrovnány oproti prvním finančně aktualizovaným příjmům do skladu na základě finančního data skladové transakce.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 663dce9f871e96fec7017616732428c49b1224a0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676236"
---
# <a name="fifo-with-physical-value-and-marking"></a>Metoda FIFO s fyzickou hodnotou a označením

[!include [banner](../includes/banner.md)]


FIFO je metoda řízení zásob a oceňování, kdy zásoby, které byly vyrobeny nebo pořízeny jako první, jsou prodány, použity nebo vyřazeny jako první. Během procesu uzávěrky skladu v Microsoft Dynamics 365 Supply Chain Management systém vytvoří vyrovnání, kde se první příjemka spáruje s prvním výdejem atd.

Princip vypořádání a párování je založen na finančním datu transakcí se zásobami. Předběžné posouzení vypořádání a úprav lze provést spuštěním procesu přepočtu zásob.

Princip FIFO můžete přepsat tak, že označíte skladové transakce, aby byl příjem určitých položek vyrovnán konkrétním výdejem. Pravidelná uzávěrka skladu je vyžadována, když používáte model zásob FIFO k vytváření vyrovnání a úpravě hodnoty výdejů podle principu FIFO. Dokud nespustíte proces uzavření zásob, jsou transakce vydávání oceňovány průběžným průměrem, kdy došlo k fyzickým a finančním aktualizacím. Pokud nepoužíváte označování, průběžný průměr se vypočítá při provedení fyzické nebo finanční aktualizace. Následující příklady ilustrují dopad použití metody FIFO ve třech různých konfiguracích:

- Metoda FIFO bez možnosti **Zahrnovat fyzickou hodnotu**
- Metoda FIFO s možností **Zahrnovat fyzickou hodnotu**
- Metoda FIFO s označením

## <a name="fifo-without-the-include-physical-value-option"></a>Metoda FIFO bez možnosti Zahrnovat fyzickou hodnotu

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
- 7\. Je provedena uzávěrka skladu. Podle metody FIFO bude první finančně zaúčtovaný výdej vyrovnán prvním finančně zaúčtovaným příjmem atd. V tomto příkladu je vytvořeno jedno vyrovnání mezi 1b a 3b. Úprava částky −6,00 USD bude provedena u 3b a výsledná konečná cena bude 10,00 USD.

Nová průběžná průměrná nákladová cena představuje průměr finančně zaúčtovaných transakcí. Následující obrázky ukazují účinky skladového modelu FIFO na tuto sérii transakcí, když není použita možnost **Zahrnovat fyzickou hodnotu**.

![Metoda FIFO bez možnosti Zahrnovat fyzickou hodnotu.](./media/fifo-without-include-physical-value.png)

**Klíč k diagramu**

- Skladové transakce jsou reprezentovány svislými šipkami.
- Fyzické transakce jsou znázorněny kratšími světle šedými šipkami.
- Finanční transakce jsou znázorněny delšími černými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad časovou osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod časovou osou.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Každé datum v diagramu je odděleno tenkou černou svislou čarou. Datum je uvedeno ve spodní části diagramu.
- Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou.
- Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými šikmými přerušovanými šipkami směřujícími od určitého příjmu k výdeji.

## <a name="fifo-with-the-include-physical-value-option"></a>Metoda FIFO s možností Zahrnovat fyzickou hodnotu

Pokud zaškrtnete políčko **Zahrnovat fyzickou hodnotu** pro položku na stránce **Skupina modelů zboží**, systém pro výpočet průběžné průměrné ceny použije transakce fyzického i finančního příjmu. V případě potřeby budou v systému také provedeny úpravy fyzicky aktualizované transakce výdeje. Uzavření zásob, které využívá model zásob FIFO, vyrovná pouze finančně zaúčtované transakce. Následující obrázek znázorňuje tyto transakce:

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
- 7\. Je provedena uzávěrka skladu. Podle metody FIFO bude první finančně zaúčtovaný výdej vyrovnán prvním finančně zaúčtovaným příjmem atd. V tomto příkladu je vytvořeno jedno vyrovnání mezi 1b a 3b. Úprava částky −6,00 USD bude provedena u 3b a výsledná konečná cena bude 10,00 USD. Transakce 6a dále bude upravena podle nákladů příjmové transakce 2b. Systém tyto transakce nevyrovná, protože příjem je zaúčtován pouze fyzicky, ale nikoli finančně. Místo toho bude k transakci fyzického výdeje zaúčtována pouze úprava −1,67 USD a výsledná upravená cena bude 22,00 USD.

![Metoda FIFO s možností Zahrnovat fyzickou hodnotu.](./media/fifo-with-include-physical-value.png)

Všimněte si, že výsledek spuštění procesu uzavření inventáře je stejný bez ohledu na to, zda vyberete možnost **Zahrnout fyzickou hodnotu** na stránce **Modelová skupina položky**. Možnost **Zahrnout fyzickou hodnotu** ovlivňuje pouze klouzavý průměr.

**Klíč k diagramu**

- Skladové transakce jsou reprezentovány svislými šipkami.
- Fyzické transakce jsou znázorněny kratšími světle šedými šipkami.
- Finanční transakce jsou znázorněny delšími černými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad časovou osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod časovou osou.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Každé datum v diagramu je odděleno tenkou černou svislou čarou. Datum je uvedeno ve spodní části diagramu.
- Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou.
- Vyrovnání, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými šikmými přerušovanými šipkami směřujícími od určitého příjmu k výdeji.

## <a name="fifo-with-marking"></a>Metoda FIFO s označením

Termínem označení se popisuje proces, který umožňuje propojit transakci výdeje s transakcí příjmu, neboli je označit jako propojené. Označení lze provést před zaúčtováním transakce nebo po ní. Označení lze provést tehdy, pokud chcete zjistit přesné náklady skladu při zaúčtování transakce nebo při provedení uzávěrky skladu.

Předpokládejme například, že oddělení služeb odběratelům přijalo spěšnou objednávku od důležitého odběratele. Vzhledem k tomu, že se jedná o spěšnou objednávku, bude nutné pro splnění požadavku zákazníka za tuto položku zaplatit více. Přitom si musíte být jisti, že pro fakturu prodejní objednávky se náklady na tuto skladovou položku odrazí v marži nebo v nákladech na prodané zboží. Při zaúčtování nákupní objednávky bude ve skladu zaznamenán příjem s náklady 120,00 USD. Je-li dokument prodejní objednávky propojen s nákupní objednávkou před zaúčtováním dodacího listu nebo faktury, budou náklady na prodané zboží činit 120,00 USD, namísto aktuální průběžné průměrné hodnoty nákladů na položku. Pokud jsou faktura nebo dodací list prodejní objednávky zaúčtovány ještě předtím, než dojde k tomuto propojení, budou náklady na prodané zboží zaúčtovány s použitím průběžné průměrné ceny. I před provedením uzávěrky skladu lze tyto dvě transakce vzájemně propojit.

Pokud je transakce příjmu propojena s transakcí výdeje, nebude metoda vyhodnocení definovaná ve skupině skladových modelů položky vzata v potaz a tyto transakce budou v systému vzájemně vyrovnány. Označení transakce můžete ručně provést z řádku prodejní objednávky na stránce **Podrobnosti prodejní objednávky** výběrem možnosti **Zásoby \> Označení** na záložce **Řádky prodejní objednávky**. Můžete zobrazit otevřené transakce příjmu na stránce **Označení**. Můžete spárovat nebo označit transakci výdeje pro transakci otevřených příjmů u naskladněné položky z deníku úpravy zaúčtované inventury. Následující obrázek znázorňuje tyto transakce:

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
- 7\. Je provedena uzávěrka skladu. Na základě principu značení, které využívá metodu FIFO, jsou označené transakce vzájemně vyrovnány. V tomto příkladu se 3b vyrovná proti 2b a úprava pro 6,00 USD se zaúčtuje do 3b, aby se hodnota dostala na 22,00 USD. V tomto příkladu nejsou prováděna žádná další vyrovnání, protože uzavření vytváří vyrovnání pouze pro finančně aktualizované transakce.

Následující obrázek ukazuje účinek volby skladového modelu FIFO na tuto sérii transakcí při použití označení propojení mezi výdeji a příjmy.

![Metoda FIFO s označením.](./media/fifo-with-marking.png)

**Klíč k diagramu**

- Skladové transakce jsou reprezentovány svislými šipkami.
- Fyzické transakce jsou znázorněny kratšími světle šedými šipkami.
- Finanční transakce jsou znázorněny delšími černými šipkami.
- Příjmy do skladu jsou reprezentovány svislými šipkami nad časovou osou.
- Výdeje ze skladu jsou reprezentovány svislými šipkami pod časovou osou.
- Každá nová transakce příjmu nebo výdeje je označena novým popiskem.
- Každá svislá šipka je označena průběžným identifikátorem (například *1a*). Identifikátory označují pořadí zaúčtování skladových transakcí na časové ose.
- Každé datum v diagramu je odděleno tenkou černou svislou čarou. Datum je uvedeno ve spodní části diagramu.
- Uzávěrky skladu jsou reprezentovány červenou svislou přerušovanou čarou.
- Vyrovnání a označení, která jsou provedena při uzávěrce skladu, jsou reprezentována červenými šikmými přerušovanými šipkami směřujícími od určitého příjmu k výdeji.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
