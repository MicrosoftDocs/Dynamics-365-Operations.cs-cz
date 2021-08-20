---
title: Metoda FIFO s fyzickou hodnotou a označením
description: Metoda (FIFO, First in, First out) představuje skladový model, ve kterém jsou nejprve vydávány první uskladněné položky. Finančně aktualizované výdeje ze skladu jsou vyrovnány oproti prvním finančně aktualizovaným příjmům do skladu na základě finančního data skladové transakce.
author: AndersGirke
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.assetid: dc0e2855-83a0-41a7-a398-3c7852597d1a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e2a8b9badcca82c8041158a9911f8d91b7d54d773610054361b7e1cc232ca5e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769580"
---
# <a name="fifo-with-physical-value-and-marking"></a>Metoda FIFO s fyzickou hodnotou a označením

[!include [banner](../includes/banner.md)]

Metoda (FIFO, First in, First out) představuje skladový model, ve kterém jsou nejprve vydávány první uskladněné položky. Finančně aktualizované výdeje ze skladu jsou vyrovnány oproti prvním finančně aktualizovaným příjmům do skladu na základě finančního data skladové transakce. 

Při použití metody FIFO není nutné použití pravidla FIFO. Místo toho můžete označit skladové transakce tak, aby byl příjem určitých položek vyrovnán konkrétním výdejem. Pokud používáte skladový model FIFO, doporučujeme provádět periodickou skladovou uzávěrku. Následující příklady ilustrují dopad použití metody FIFO ve třech různých konfiguracích:

-   Metoda FIFO bez možnosti **Zahrnovat fyzickou hodnotu**
-   Metoda FIFO s možností **Zahrnovat fyzickou hodnotu**
-   Metoda FIFO s označením

## <a name="fifo-without-the-include-physical-value-option"></a>Metoda FIFO bez možnosti Zahrnovat fyzickou hodnotu
V tomto příkladu není skupina modelů položek označena, aby obsahovala fyzickou hodnotu. Následující obrázek znázorňuje tyto transakce:

-   1a. Fyzický příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
-   1b. Finanční příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
-   2a. Fyzický příjem ve skladu pro množství 2 při ceně 10,00 USD za kus
-   2b. Finanční příjem ve skladu pro množství 2 při ceně 10,00 USD za kus
-   3a. Fyzický příjem ve skladu pro množství 1 při ceně 25,00 USD za kus
-   4a. Fyzický příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
-   4b. Finanční příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
-   5a. Fyzický výdej 1 kusu za 20 Kč (průběžný průměr z finančně zaúčtovaných transakcí).
-   5b. Finanční výdej 1 kusu za nákladovou cenu 20 Kč (průběžný průměr z finančně zaúčtovaných transakcí).
-   6. Je provedena uzávěrka skladu. Podle metody FIFO bude první finančně zaúčtovaný výdej vyrovnán prvním finančně zaúčtovaným příjmem. Pro transakci výdeje bude provedena úprava 5,00 Kč.

Nová průběžná průměrná nákladová cena představuje průměr finančně zaúčtovaných transakcí. Následující obrázky ukazují účinky skladového modelu FIFO na tuto sérii transakcí, když není použita možnost **Zahrnovat fyzickou hodnotu**. 

![FIFO bez funkce Zahrnovat fyzickou hodnotu.](./media/fifowithoutincludephysicalvalue.gif) 

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

## <a name="fifo-with-the-include-physical-value-option"></a>Metoda FIFO s možností Zahrnovat fyzickou hodnotu
Pokud zaškrtnete políčko **Zahrnovat fyzickou hodnotu** pro položku na stránce **Skupina modelů zboží**, systém pro výpočet průběžné průměrné ceny použije transakce fyzického i finančního příjmu. V případě potřeby budou v systému také provedeny úpravy fyzicky aktualizované transakce výdeje. Pokud je zaškrtnutí políčka **Zahrnovat fyzickou hodnotu** odstraněno, budou při uzávěrce skladu s použitím skladového modelu FIFO provedena vyrovnání pouze pro finančně aktualizované transakce. Následující obrázek znázorňuje tyto transakce:

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
-   7. Je provedena uzávěrka skladu. Podle metody FIFO bude první finanční transakce výdeje opravena či vyrovnána podle prvního zaúčtovaného příjmu bez ohledu na to, zda se jedná o finanční nebo fyzický příjem.

Transakce č. 5b bude vyrovnána transakcí příjmu č. 1b. K této transakci výdeje bude vytvořena záporná úprava ve výši 11,25 Kč. Nová průběžná průměrná cena bude odrážet průměrnou hodnotu finančně a fyzicky aktualizovaných transakcí ve výši 27,50 Kč. Následující obrázek ukazuje účinek skladového modelu FIFO na tuto sérii transakcí, když není použita možnost **Zahrnovat fyzickou hodnotu**. 

![FIFO s funkcí Zahrnovat fyzickou hodnotu.](./media/fifowithincludephysicalvalue.gif) 

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

## <a name="fifo-with-marking"></a>Metoda FIFO s označením
Termínem označení se popisuje proces, který umožňuje propojit transakci výdeje s transakcí příjmu, neboli je označit jako propojené. Označení lze provést před zaúčtováním transakce nebo po ní. Označení lze provést tehdy, pokud chcete zjistit přesné náklady skladu při zaúčtování transakce nebo při provedení uzávěrky skladu. Předpokládejme například, že oddělení služeb odběratelům přijalo spěšnou objednávku od důležitého odběratele. Vzhledem k tomu, že se jedná o spěšnou objednávku, bude nutné pro splnění požadavku zákazníka za tuto položku zaplatit více. Přitom si musíte být jisti, že pro fakturu této prodejní objednávky se náklady na tuto skladovou položku odrazí v marži nebo v nákladech na prodané zboží. Při zaúčtování nákupní objednávky bude ve skladu zaznamenán příjem s náklady 120,00 USD. Je-li tento dokument prodejní objednávky propojen s nákupní objednávkou před zaúčtováním dodacího listu nebo faktury, budou náklady na prodané zboží činit 120,00 USD, namísto aktuální průběžné průměrné hodnoty nákladů na položku. Pokud jsou faktura nebo dodací list prodejní objednávky zaúčtovány ještě předtím, než dojde k tomuto propojení, budou náklady na prodané zboží zaúčtovány s použitím průběžné průměrné ceny. I před provedením uzávěrky skladu lze tyto dvě transakce vzájemně propojit. Pokud je transakce příjmu propojena s transakcí výdeje, nebude metoda vyhodnocení definovaná ve skupině skladových modelů položky vzata v potaz a tyto transakce budou v systému vzájemně vyrovnány. Před zaúčtováním transakce je možné označit transakci výdeje s příjmem. To lze provést na řádku prodejní objednávky na stránce **Podrobnosti prodejní objednávky**. Můžete zobrazit otevřené transakce příjmu na stránce **Označení**. Po zaúčtování transakce je možné také označit transakci výdeje s příjmem. Můžete spárovat nebo označit transakci výdeje pro transakci otevřených příjmů u naskladněné položky z deníku úpravy zaúčtované inventury. Následující obrázek znázorňuje tyto transakce:

-   1a. Fyzický příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
-   1b. Finanční příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
-   2a. Fyzický příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
-   2b. Finanční příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
-   3a. Fyzický příjem ve skladu pro množství 1 při ceně 25,00 USD za kus
-   4a. Fyzický příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
-   4b. Finanční příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
-   5a. Fyzický výdej ze skladu pro množství 1 při ceně 21,25 USD za kus (průběžná průměrná hodnota finančních a fyzických aktualizovaných transakcí).
-   5b. Finanční výdej ze skladu pro množství 1 je před zaúčtováním transakce propojen s příjmem ve skladu 2b. Tato transakce je zaúčtována s nákladovou cenou 20 Kč.
-   6a. Fyzický výdej ze skladu pro množství 1 při ceně 21,25 USD za kus.
-   7. Je provedena uzávěrka skladu. Vzhledem k tomu, že finančně aktualizovaná transakce FIFO je propojena s existujícím příjmem, budou tyto transakce vzájemně vyrovnány a nebudou provedeny žádné úpravy.

Nová průběžná průměrná cena bude odrážet průměrnou hodnotu finančně a fyzicky aktualizovaných transakcí ve výši 27,50 Kč. Následující obrázek ukazuje účinek volby skladového modelu FIFO na tuto sérii transakcí při použití označení propojení mezi výdeji a příjmy. 

![Metoda FIFO s označením.](./media/fifowithmarking.gif) 

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