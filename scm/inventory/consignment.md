---
title: "Zásilka"
description: "Toto téma vysvětluje, jak používat procesy příchozí skladové zásilky."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentDraftReplenishmentOrderJournal, ConsignmentProductReceiptLines, ConsignmentReplenishmentOrder, ConsignmentVendorPortalOnHand, InventJournalOwnershipChange, InventOnHandItemListPage, PurchTable, PurchVendorPortalConfirmedOrders
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220834
ms.assetid: 3c9d6de4-45d4-459a-aef7-0d9ad2c22b3a
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a6e3f0e58e14cc4d68d2249a4e3b69515f23e838
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="consignment"></a>Zásilka

[!include[banner](../includes/banner.md)]


Toto téma vysvětluje, jak používat procesy příchozí skladové zásilky.

Zásoby dodávky jsou zásoby, které vlastní dodavatel, ale jsou uloženy ve vaší společnosti. Až budete připraveni spotřebovat nebo použít zásoby, převezmete vlastnictví zásob. Toto téma obsahuje informace o tom, jak fyzicky přijmout zásoby dodavatele na skladě bez nutnosti vytvoření transakcí v hlavní knize, jak spustit výrobní proces, kde lze fyzicky rezervovat zásoby vlastněné dodavatele, a jak změnit vlastnictví suroviny, aby bylo možné zpracovat spotřebu jakou součást zpracování výrobní zakázky. Je zda také pár informací o tom, jak může dodavatel sledovat spotřebu skladových zásob pomocí rozhraní dodavatelské spolupráce. Zobrazit informace o způsobech, jak povolit a konfigurovat procesy příchozí zásilky, můžete na [Nastavení zásilky](set-up-consignment.md).

## <a name="overview-of-the-consignment-process"></a>Přehled procesu zásilky
V tomto vzorovém scénáři společnost USMF má smlouvu o zásilce s dodavatelem US-104 na suroviny M9211CI.

1.  Objednávka doplňovací zásilky se vytváří ručně někým z USMF na základě očekávané poptávky. Vytvoří se objednávka pro dodavatele US-104 a pro položku MS9211CI je přidán řádek.
2.  Dodavatel obdrží informaci o očekávaném datu dodání. K tomu může dojít jedním z následujících tří způsobů:
    -   Pracovník v USMF odešle dodavateli informaci o objednávce.
    -   Dodavatel může také monitorovat očekávané zásoby na skladě u zákazníka pomocí rozhraní dodavatelské spolupráce.
    -   Pracovník v USMF filtruje data na stránce **Zásoby na skladě** a zobrazuje pouze záznamy dodavatele US-104, kde je stav příjmu **Objednáno**. Tyto informace pak odešle dodavateli.

3.  Zásoby jsou přesunuty od US-104 do USMF.
4.  Když materiál dorazí do USMF, objednávka doplňovací zásilky se při přijetí produktu aktualizuje. Zaznamenává se pouze fyzické množství zásob vlastněné dodavatelem. Nevytváří se žádné transakce do hlavní knihy, protože zásoby jsou doposud ve vlastnictví dodavatele.
5.  Dodavatel sleduje aktualizace fyzických zásob na skladě pomocí stránky **Zásoby dodávky na skladě**.
6.  Když jsou nyní fyzické zásoby na skladě, výrobní proces rezervuje zásoby vlastněné dodavatelem a uvede do chodu výrobní zakázky pro dokončené zboží, které spotřebuje suroviny M9211CI.
7.  Vlastník rezervovaných surovin, které mají být spotřebovány v dnešní výrobě je změněn z US-104 na USMF. To se provádí pomocí změny vlastnictví zásob v deníku. Tento proces vytvoří nákupní objednávky, kde pole **Původ** je nastaveno na **Dodávka**.
8.  Dodavatel sleduje spotřebu (změnu vlastnictví) na stránce **Přijaté produkty ze zásob dodávky** a fakturuje na základě smluv mezi těmito dvěma společnostmi.
9.  Výrobní proces spotřebovává suroviny prostřednictvím výrobních výdejek. Fyzické rezervace se automaticky aktualizuje a odráží fakt, že USMF vlastní zásoby na skladě.
10. Faktura od US-104 se zpracovává proti nákupním objednávkám, které byly automaticky generované, když se začaly zpracovávat změny vlastnictví v deníku. Provede se platba dodavateli US-104 za spotřebované zásoby.

USMF provede dodatečné periodické procesy:

-   Fyzické přesunutí zásob vlastněných dodavatelem mezi různými sklady se zpracovává pomocí deníku převodu.
-   Fyzické zásoby na skladě se aktualizují pomocí deníku**Sčítání položek**. Sčítání může být také využito dodavatelem pro aktualizaci zásob na skladě, pokud k tomu má oprávnění.

Dodavatel US-104 můžete sledovat aktualizace pomocí stránky **Zásoby zásilky na skladě**.

## <a name="consignment-replenishment-orders"></a>Zakázky na doplnění stavu zásob dodávky
Objednávka doplňovací zásilky je dokument, který se používá pro zažádání a sledovat skladového množství produktů, které má dodavatel v úmyslu dodat do určitého data vytvořením transakcí objednaných zásob. Obvykle se to bude opírat o prognózy a skutečnou poptávku specifických produktů. Zásoby, které má získat oproti objednávce doplňující zásilky, zůstávají ve vlastnictví dodavatele. Zaznamenává se pouze změna vlastnictví produktů souvisejících s fyzickým příjmem, a proto nedochází k žádné aktualizaci transakcí hlavní knihy. Dimenze **Vlastník** se používá k oddělení informací o tom, které zásoby vlastní dodavatel a které vlastní přijímající právnická osoba. Řádky objednávky doplnění stavu zásob dodávky mají stav **Otevřená objednávka**, dokud nedojde k přijetí nebo zrušení úplného množství řádků. Až dojde k přijetí nebo zrušení úplného množství, stav se změní na **Dokončeno**. Fyzické zásoby na skladě související s objednávkou doplňovací dodávky lze zaznamenat pomocí registračního procesu a také procesu aktualizace příjemky produktu. Registraci lze provést jako součást procesu doručení položky, nebo lze ručně aktualizovat řádky objednávky. Při procesu aktualizace příjemky produktu se provádí záznam do deníku příjemek produktů, který pro dodavatele slouží k potvrzení o přijetí zboží. 

[![Zakázka na doplnění stavu zásob dodávky](./media/consignment-replenishment-order.png)](./media/consignment-replenishment-order.png)

## <a name="inventory-ownership-change-journal"></a>Deník změn vlastnictví zásob
Proces změn vlastnictví zásob dodavatele na přijímající právnickou osobu se provádí pomocí deníku změn vlastníka zásob. V deníku nejsou vytvořeny žádné očekávané skladové transakce. Jsou vytvořeny pouze transakce, které se vztahují k zaúčtovanému deníku. Kdy je deník zaúčtován:

-   Zásoby vlastněné dodavatelem se vydávají pomocí odkazu na **změny vlastnictví** se stavem **Prodáno**.
-   Zásoby na skladě jsou pak přijaty právní osobou, která je bude využívat, pomocí skladové transakce, která je aktualizována příjemkou produktu na nákupní objednávce. To nastaví stav objednávky na **přijato**. Nákupní objednávky použité pro dodávku mají pole **Původ** nastaveno na **Dodávka**.

Není možné aktualizovat množství v řádcích nákupní objednávky po vytvoření objednávky. 

[![Deník-změn-vlastnictví-zásob](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Dodavatelská spolupráce v procesech zásilky
Rozhraní dodavatelské spolupráce má tři stránky související s procesem příchozí zásilky:

-   **Nákupní objednávky** **spotřebovávající zásoby dodávek** - zobrazí podrobné informace o nákupní objednávce související se změnou vlastnictví z procesu zásilky.
-   **Produkty přijaty ze skladové zásilky** – zobrazuje informace o položkách a množství, jejichž příjemky produktu se aktualizují při změně procesu vlastnictví.
-   **Zásoby dodávky na skladě** - zobrazí informace o dodávce položky, které mají dle očekávání dorazit a položky, které jsou již fyzicky k dispozici u zákazníka.





