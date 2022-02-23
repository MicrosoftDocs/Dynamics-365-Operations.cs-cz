---
title: Datum LIFO s fyzickou hodnotou a označením
description: Metoda LIFO (Datum LIFO) je skladový model vycházející z principu LIFO. Výdeje ze skladu jsou vyrovnávány vůči posledním příjmům na sklad podle data skladové transakce. Pokud v případě data LIFO nepředchází výdeji žádný příjem, výdej je vyrovnán proti jakýmkoli příjmům, ke kterým dojde po datu výdeje. Několik výdejů ve stejný den lze vyrovnat v pořadí posledního výdeje a posledního příjmu.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 51592
ms.assetid: d9f13274-3268-444f-85c8-b686fd39286d
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2c06443532519ad5d6c36a6f4ed1f1c4d136664
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967626"
---
# <a name="lifo-date-with-physical-value-and-marking"></a>Datum LIFO s fyzickou hodnotou a označením

[!include [banner](../includes/banner.md)]

Metoda LIFO (Datum LIFO) je skladový model vycházející z principu LIFO. Výdeje ze skladu jsou vyrovnávány vůči posledním příjmům na sklad podle data skladové transakce. Pokud v případě data LIFO nepředchází výdeji žádný příjem, výdej je vyrovnán proti jakýmkoli příjmům, ke kterým dojde po datu výdeje. Několik výdejů ve stejný den lze vyrovnat v pořadí posledního výdeje a posledního příjmu. 

Při použití skladového modelu LIFO (Datum LIFO) nepředchází výdeji žádný příjem, výdej je vyrovnán proti jakýmkoli příjmům, ke kterým dojde po datu výdeje. Několik výdejů ve stejný den lze vyrovnat v pořadí posledního výdeje a posledního příjmu. Při použití metody Datum LIFO není nutné použití pravidla Datum LIFO. Místo toho můžete označit skladové transakce tak, aby byl příjem určitých položek vyrovnán konkrétním výdejem. 

Pokud používáte skladový model data LIFO, doporučujeme provádět periodickou skladovou uzávěrku. 

Následující příklady ilustrují dopad použití metody Datum LIFO ve třech různých konfiguracích:

-   Metoda Datum LIFO bez použití volby **Zahrnout fyzickou hodnotu**
-   Metoda Datum LIFO s použitím volby **Zahrnout fyzickou hodnotu**
-   Metoda Datum LIFO s označením

## <a name="lifo-date-without-the-include-physical-value-option"></a>Metoda Datum LIFO bez použití volby Zahrnout fyzickou hodnotu
V tomto příkladu není skupina modelů položek označena, aby obsahovala fyzickou hodnotu. Následující obrázek znázorňuje tyto transakce:

-   1a. Fyzický příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
-   1b. Finanční příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
-   2a. Fyzický příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
-   2b. Finanční příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
-   3a. Fyzický příjem ve skladu pro množství 1 při ceně 25,00 USD za kus
-   4a. Fyzický výdej ze skladu pro množství 1 při ceně 15,00 USD (průběžná průměrná cena finančně aktualizovaných transakcí).
-   4b. Finanční výdej ze skladu pro množství 1 při ceně 15,00 USD (průběžná průměrná cena finančně aktualizovaných transakcí).
-   5a. Fyzický příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
-   5b. Finanční příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
-   6. Je provedena uzávěrka skladu. Na základě metody Datum LIFO bude poslední finančně aktualizovaný výdej podle data vyrovnán oproti poslednímu finančně aktualizovanému příjmu. Pro transakci výdeje bude provedena úprava 5,00 USD. Tyto transakce budou vyrovnány vzájemně.

Nová průběžná průměrná cena bude odrážet průměrnou hodnotu finančně aktualizovaných transakcí ve výši 15,00 USD. 

Následující obrázek ukazuje účinek skladového modelu Datum LIFO, když není použita možnost **Zahrnovat fyzickou hodnotu**. ![Datum LIFO s funkcí Zahrnovat fyzickou hodnotu](./media/lifodatewithoutincludephysicalvalue.gif) 

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

## <a name="lifo-date-with-the-include-physical-value-option"></a>Metoda Datum LIFO s použitím volby Zahrnout fyzickou hodnotu
Můžete vybrat políčko **Zahrnout fyzickou hodnotu** pro položku na stránce **Skupiny modelů zboží**. V tomto případě systém použije pro výpočet průběžné průměrné ceny použity transakce fyzického i finančního příjmu. V případě potřeby budou v systému také provedeny úpravy fyzicky aktualizované transakce výdeje. Pokud je zaškrtnutí políčka **Zahrnovat fyzickou hodnotu** odstraněno, budou při uzávěrce skladu s použitím skladového modelu Datum LIFO provedena vyrovnání pouze pro finančně aktualizované transakce. 

V tomto příkladu je skupina modelů položek označena, aby obsahovala fyzickou hodnotu. 

Následující obrázek znázorňuje tyto transakce:

-   1a. Fyzický příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
-   1b. Finanční příjem ve skladu pro množství 1 při ceně 10,00 USD za kus
-   2a. Fyzický příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
-   2b. Finanční příjem ve skladu pro množství 1 při ceně 20,00 USD za kus
-   3a. Fyzický příjem ve skladu pro množství 1 při ceně 25,00 USD za kus
-   4a. Fyzický výdej ze skladu pro množství 1 při ceně 18,33 USD za kus (průběžná průměrná cena finančně aktualizovaných transakcí).
-   4b. Finanční výdej ze skladu pro množství 1 při ceně 18,33 USD za kus (průběžná průměrná cena finančně aktualizovaných transakcí).
-   5a. Fyzický příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
-   5b. Finanční příjem ve skladu pro množství 1 při ceně 30,00 USD za kus
-   6. Je provedena uzávěrka skladu. Na základě metody Datum LIFO bude poslední aktualizovaný výdej podle data upraven nebo vyrovnán oproti poslednímu aktualizovanému finančnímu příjmu. Tyto transakce nebudou vzájemně vyrovnány, protože transakce finančního příjmu je upravena na transakci fyzické aktualizace. Namísto toho bude pro transakci výdeje provedena pouze úprava 6,67 USD.

Nová průběžná průměrná cena bude odrážet průměrnou hodnotu finančně aktualizovaných transakcí ve výši 20,00 USD. 

Následující obrázek ukazuje účinek skladového modelu LIFO, když je použita možnost **Zahrnovat fyzickou hodnotu**. ![Datum LIFO s funkcí Zahrnovat fyzickou hodnotu](./media/lifodatewithincludephysicalvalue.gif) 

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

## <a name="lifo-date-with-marking"></a>Metoda Datum LIFO s označením
Termínem označení se popisuje proces, který umožňuje propojit transakci výdeje s transakcí příjmu, neboli je označit jako propojené. Označení lze provést před zaúčtováním transakce nebo po ní. Označení lze provést tehdy, pokud chcete zjistit přesné náklady skladu při zaúčtování transakce nebo při provedení uzávěrky skladu. 

Předpokládejme například, že oddělení služeb odběratelům přijalo spěšnou objednávku od důležitého odběratele. Vzhledem k tomu, že se u této objednávky jedná o spěšnou objednávku, bude nutné při splnění požadavku zákazníka za tuto položku zaplatit více. Přitom si musíte být jisti, že pro fakturu této prodejní objednávky se náklady na tuto skladovou položku odrazí v marži nebo v nákladech na prodané zboží. 

Při zaúčtování nákupní objednávky bude ve skladu zaznamenán příjem s náklady 120,00 USD. Je-li tento dokument prodejní objednávky propojen s nákupní objednávkou před zaúčtováním dodacího listu nebo faktury, budou náklady na prodané zboží činit 120,00 USD, namísto aktuální průběžné průměrné hodnoty nákladů na položku. Pokud jsou faktura nebo dodací list prodejní objednávky zaúčtovány ještě předtím, než dojde k tomuto propojení, budou náklady na prodané zboží zaúčtovány s použitím průběžné průměrné ceny. 

I před provedením uzávěrky skladu lze tyto dvě transakce vzájemně propojit. 

Například příjmová transakce je propojena s transakcí výdeje. V tomto případě metoda ocenění definovaná pro skupinu modelů položky nebude brána v úvahu. Systém vyrovná tyto transakce navzájem. 

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

Nová průběžná průměrná cena bude odrážet průměrnou hodnotu finančně a fyzicky aktualizovaných transakcí ve výši 27,50 USD. 

Následující obrázek ukazuje účinek skladového modelu LIFO, když je použito propojení mezi příjmy a výdeji. ![Metoda Datum LIFO s označením](./media/lifodatewithmarking.gif) 

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




