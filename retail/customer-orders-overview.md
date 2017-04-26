---
title: "Přehled objednávek zákazníka"
description: "Toto téma obsahuje informace o objednávkách v maloobchodní moderní POS (MPOS). Objednávky odběratele jsou označovány také jako speciální objednávky. Téma obsahuje diskuse související parametry a toků transakcí."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2f466dfe53ccf0be15ed0793b4a6dd371bdacc0d
ms.lasthandoff: 03/31/2017


---

# <a name="customer-orders-overview"></a>Přehled objednávek zákazníka

[!include[banner](includes/banner.md)]


Toto téma obsahuje informace o objednávkách v maloobchodní moderní POS (MPOS). Objednávky odběratele jsou označovány také jako speciální objednávky. Téma obsahuje diskuse související parametry a toků transakcí.

Ve světě maloobchodu omni-channel řada maloobchodníků poskytují možnost zákazníka objednávky nebo speciální objednávky různých produktů a splnění požadavků. Zde jsou některé typické scénáře:

-   Zákazník chce produkty k určitému datu doručení na konkrétní adresu.
-   Zákazník chce vyzvednout výrobky z úložiště nebo umístění, které se liší od skladu nebo umístění, kde zákazník zakoupil tyto produkty.
-   Zákazník chce někdo na vyzvednutí produktů, které zákazník zakoupil.

Maloobchodníci také použít objednávky odběratele pro minimalizaci ztráta prodejů, způsobující výpadky zásob může být jinak, protože zboží lze doručení nebo vyzvednutí v jiné době nebo místě.

## <a name="set-up-customer-orders"></a>Nastavení objednávky zákazníka
Zde jsou některé parametry, které lze nastavit na **parametry programu Retail** stránku definujete, jak splnění objednávky zákazníka:

-   **Výchozí procento z vkladu** – zadejte částku, kterou musí zákazník zaplatit jako vklad před lze potvrdit objednávku. Výchozí částka vkladu se počítá jako procento z hodnoty objednávky. V závislosti na oprávněních, zaměstnanec obchodu budete moci přepsat částku pomocí **přepsání vkladu**.
-   **Procento poplatku za zrušení** -Pokud se použije poplatek při zrušení objednávky zákazníka určit výši tohoto poplatku.
-   **Kód poplatku za zrušení** -Pokud poplatek bude použito při zrušení objednávky odběratele, že poplatek se odrazí v kód nákladů na prodejní objednávky v aplikaci Microsoft Dynamics AX. Tento parametr slouží k definování kód poplatku za zrušení.
-   **Kódu dopravného** – prodejců můžete účtovat dodatečný poplatek pro dodání zboží zákazníkovi. Výši tohoto poplatku expedice se odrazí v kód nákladů na prodejní objednávky v aplikaci Dynamics AX. Tento parametr použijte k mapování kód poplatku za dodávky přepravní náklady v objednávce zákazníka.
-   **Náhrada nákladů na dodání** – určit, zda jsou nevratné dopravné, které jsou spojeny s objednávkou zákazníka.
-   **Maximální částka bez schválení** -Pokud je přepravní poplatky jsou nevratné, určit maximální výši náhrady nákladů dopravy přes objednávky vratky. Pokud dojde k překročení této částky, je nutné přepsat správce pokračovat s náhradou. Pro následující scénáře, náhrada poplatky za dodání mohou překročit částku, která byla původně vyplacena:
    -   Poplatky jsou použity na úrovni záhlaví prodejní objednávky a při nějaké množství produktové řady je vrácena, maximální náhrady přepravní poplatky, které jsou povoleny pro produkty a množství nelze stanovit způsobem, který funguje pro všechny maloobchodní zákazníky.
    -   Pro každou instanci expedice vzniká dopravné. Pokud zákazník vrací produkty vícekrát a prodejce zásad určuje, že prodejce bude hradit náklady na dopravné vratky, vratky Dopravné bude větší než skutečné přepravní náklady.

## <a name="transaction-flow-for-customer-orders"></a>Tok transakcí pro objednávky zákazníka
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Vytvoření objednávky zákazníka v programu Retail POS moderní

1.  Přidejte zákazníka do transakce
2.  Přidáte produkty do košíku.
3.  Klepněte na tlačítko **vytvořit objednávku odběratele**a potom vyberte typ objednávky. Zadaný typ může být buď **objednávka odběratele** nebo **nabídka**.
4.  Klepněte na tlačítko **loď vybrána** nebo **dodat všechny** k dodání výrobků na adresu na účet zákazníka, zadejte požadované datum expedice a určit dopravné.
5.  Klepněte na tlačítko **vyzvednout vybraná** nebo **odběr všech** výběr produktů, které bude být vyzvednuty z aktuální úložiště nebo jiné úložiště k určitému datu.
6.  Pokud je požadována záloha, shromažďovat částky zálohy.

### <a name="edit-an-existing-customer-order"></a>Upravit existující objednávky zákazníka

1.  Na domovské stránce klepněte na tlačítko **vyhledání objednávky**.
2.  Vyhledejte a vyberte objednávku, kterou chcete upravit. V dolní části stránky klepněte **úprava**.

### <a name="pick-up-an-order"></a>Vyzvednout objednávku

1.  Na domovské stránce klepněte na tlačítko **vyhledání objednávky**.
2.  Vyberte objednávku na vyzvednutí. V dolní části stránky klepněte na **výdeje a balení**.
3.  Klepněte na tlačítko **vyzvednout**.

### <a name="cancel-an-order"></a>Zrušení objednávky

1.  Na domovské stránce klepněte na tlačítko **vyhledání objednávky**.
2.  Vyberte objednávku, kterou chcete zrušit. V dolní části stránky klepněte na **zrušení**.

#### <a name="create-a-return-order"></a>Vytvořit vratku

1.  Na domovské stránce klepněte na tlačítko **vyhledání objednávky**.
2.  Vyberte objednávku, pro vrácení, vyberte faktury pro objednávku a poté vyberte produktovou řadu pro zboží k vrácení.
3.  V dolní části stránky klepněte **objednávka vratky**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Tok transakcí asynchronní pro objednávky zákazníka
Vytvořit objednávky zákazníka z místa prodeje (POS) klienta v buď synchronní nebo asynchronní režimu.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Povolit objednávky zákazníka, které mají být vytvořeny v asynchronním režimu

1.  V aplikaci Dynamics AX, klepněte na tlačítko **maloobchodní a commerce**&gt;**nastavení kanálu**&gt;**instalace POS**&gt;**profil POS**&gt;**funkční profily**.
2.  Na **Obecné** s náhledem nastavení **vytvoření objednávky zákazníků v režimu asynchronního přenosu** možnost na **Ano**.

Když **vytvoření objednávky zákazníků v režimu asynchronního přenosu** možnost je nastavena na **Ano**, objednávky zákazníků, se vždy vytvářejí v asynchronním režimu, i když program Retail Transaction Service (RTS) je k dispozici. Pokud nastavíte tuto možnost na **č**, objednávky zákazníků jsou vždy vytvářeny v synchronním režimu pomocí RTS. Při vytváření objednávek zákazníků v asynchronním režimu, jsou vyžádány a vložen do aplikace Dynamics AX úlohami Pull (P). Odpovídající prodejní objednávky vytvořené v aplikaci Dynamics AX při **synchronizovat objednávky** je spustit ručně nebo pomocí dávkového zpracování.

<a name="see-also"></a>Viz také
--------

[Hybrid objednávky zákazníka](hybrid-customer-orders.md)




