---
title: Podrobnosti transakce zásob
description: Toto téma poskytuje přehled stránky Podrobnosti transakcí, která zobrazuje podrobnosti o vybrané transakci zásob.
author: rachel-profitt
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventTrans, InventTransDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: fd1416f21ce15dc832dd41ea4110c93bf5bb41a2
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735908"
---
# <a name="inventory-transaction-details"></a>Podrobnosti transakce zásob

Na stránce **Podrobnosti transakce** najdete detaily jakékoli vybrané transakce zásob.

## <a name="open-the-transaction-details-page"></a>Otevření stránky Podrobnosti transakce

Chcete-li otevřít stránku **Podrobnosti transakce**, postupujte takto.

1. Přejděte na **Řízení zásob \> Dotazy a sestavy \> Transakce**.
1. Vyberte transakci, kterou chcete prozkoumat.
1. V podokně akcí zvolte **Podrobnosti transakce**.

## <a name="fasttabs-overview"></a>Přehled pevných záložek

Stránka **Podrobnosti transakce** je rozdělena do několika pevných záložek. Následující tabulka popisuje účel každé pevné záložky.

| Pevná záložka | Popis |
|---|---|
| Obecná | Tato pevná záložka zobrazuje základní informace o vybrané transakci zásob. Kromě polí, která se zobrazují na stránce **Transakce zásob**, obsahuje další pole, která jsou popsána dále v tomto tématu. |
| Aktualizace | Tato pevná záložka zobrazuje informace, které souvisejí s fyzickými, finančními a zúčtovacími aspekty vybrané transakce zásob. V závislosti na aktuálním stavu transakce mohou být některá pole prázdná. Tato pole však budou automaticky nastavena při zaúčtování transakcí. Kromě polí, která se zobrazují na stránce **Transakce zásob**, obsahuje tato pevná záložka další pole, která jsou popsána dále v tomto tématu. |
| Zaúčtování do hlavní knihy | Tato pevná záložka zobrazuje typ zaúčtování a účet hlavní knihy, které se používají pro fyzickou aktualizaci, finanční aktualizaci, fyzické příjmy, fyzické poplatky, finanční příjmy a finanční poplatky související s vybranou transakcí zásob. |
| Odkazy | Tato pevná záložka zobrazuje další informace o zdrojové transakci, která vytvořila vybranou transakci zásob. Tyto informace mohou například zahrnovat podrobnosti z nákupní objednávky nebo prodejní objednávky. |
| Související informace | Tato pevná záložka zobrazuje další informace o vybrané transakci zásob. Tato pole nemusejí být nastavena, pokud nepoužíváte některé funkce, jako jsou kategorie zásobování nebo projekty. |
| Finanční dimenze – fyzické | Tato pevná záložka zobrazuje hodnoty finanční dimenze, které byly použity při zaúčtování fyzické aktualizace. Pokud fyzická aktualizace nebyla zaúčtována, pole budou prázdná. |
| Finanční dimenze – finanční | Tato pevná záložka zobrazuje hodnoty finanční dimenze, které byly použity při zaúčtování finanční aktualizace. Pokud finanční aktualizace nebyla zaúčtována, pole budou prázdná. |
| Dimenze zásob | Tato pevná záložka zobrazuje hodnoty dimenzí zásob, které jsou přiřazeny k vybrané transakci zásob. Tyto hodnoty zahrnují místo, sklad, velikost, barvu, konfiguraci, umístění, číslo šarže, sériové číslo, stav zásob, registrační značku a vlastníka. |

## <a name="fields-on-the-general-fasttab"></a>Pole na pevné záložce Obecné

Následující tabulka popisuje pole na pevné záložce **Obecné**, které se nezobrazují také na stránce **Transakce se zásobami**.

| Pole | Popis |
|---|---|
| Strana | Název příslušné strany pro vybranou transakci zásob. Například transakce nákupní objednávky zobrazuje jméno dodavatele na nákupní objednávce a transakce prodejní objednávky zobrazuje jméno zákazníka. Toto pole není dostupné u všech typů transakcí zásob. |
| Odkaz zásob | Pokud s vybranou transakcí zásob souvisí jiná transakce zásob, typ této jiné transakce. Pokud je například nákupní objednávka označena proti prodejní objednávce, pole **Reference zásob** transakce nákupní objednávky bude nastaveno na *Prodejní objednávka*. Označení probíhá automaticky u objednávek přímé dodávky a vnitropodnikových objednávek. Když používáte označení s jinými metodami výpočtu nákladů než *standardní náklady* a *klouzavý průměr*, systém vytvoří zúčtování a úpravy u transakcí, které jsou označeny. Tímto způsobem můžete dosáhnout výpočtu „skutečných“ nákladů, který přepíše logiku pro model zásob FIFO, LIFO nebo vážený průměr. |
| Číslo zásob | Konkrétní transakce, která souvisí s vybranou transakcí zásob. Pokud je například nákupní objednávka označena proti prodejní objednávce, pole **Číslo zásob** transakce nákupní objednávky bude nastaveno na číslo prodejní objednávky. |
| ID projektu | Pokud se vybraná transakce zásob vztahuje k projektu, je toto pole nastaveno na číslo projektu. |
| ID šarže | Jedinečné ID šarže, které systém přiřadil vybrané transakci zásob. |
| Odkaz na šarži | Pokud s vybranou transakcí zásob souvisí jiná transakce zásob, ID šarže této jiné transakce. Pokud je například nákupní objednávka označena proti prodejní objednávce, pole **Odkaz na šarži** transakce nákupní objednávky bude nastaveno na hodnotu **ID šarže** transakce zásob řádku prodejní objednávky. |
| Číslo dimenze | Jedinečné ID, které představuje kombinaci všech hodnot dimenze zásob, které jsou přiřazeny k vybrané transakci zásob. |
| Otevřená hodnota | Hodnota, která udává, zda byla vybraná transakce zásob vypořádána procesem uzávěrky zásob. Je-li toto pole nastaveno na *Ano*, transakce nebyla vyrovnána. |
| Očekávané datum | U příjmových transakcí datum, kdy se očekává, že dojde k příjmu zásob. Toto pole může například zobrazovat očekávané datum příjmu na objednávce blokování zásob nebo datum dodání na řádku nákupní objednávky. |
| Datum zásob | Toto pole je nastaveno, když byla provedena transakce registrace na účtence před zaúčtováním fyzické účtenky. |
| Nefinanční převod | Hodnota, která udává, zda je vybraná transakce zásob nefinančním převodem. K nefinančnímu převodu dochází, když změna dimenzí zásob není finančně sledována na stránce **Skupina modelů položek**. |
| ID šarže převodu | Pokud je vybraná transakce zásob nefinančním převodem, je toto pole nastaveno na **ID šarže** jiné transakce zásob, proti které je vybraná transakce vypořádána. |

## <a name="fields-on-the-updates-fasttab"></a>Pole na pevné záložce Aktualizace

Následující tabulka popisuje pole na pevné záložce **Aktualizace**, které se nezobrazují také na stránce **Transakce se zásobami**.

| Pole | Popis |
|---|---|
| Fyzický doklad | Číslo dokladu z hlavní knihy, kde bylo vygenerováno fyzické účtování pro vybranou skladovou transakci. |
| Trasa | Trasa související s vybranou transakcí zásob. Toto pole je nastaveno pouze pro transakce výrobní výdejky, kde se kusovník (BOM) nebo řádek vzorce vztahuje ke konkrétní položce. |
| Dodací list | Číslo dodacího listu, které bylo zadáno pro transakci příjmu produktu nákupní objednávky. |
| Fyzická částka nákladů | Částka, která byla zaúčtována do hlavní knihy pro fyzickou aktualizaci. U produktu se standardní cenou tato částka představuje standardní cenu. U ostatních metod výpočtu nákladů představuje vážený průměr pro produkt v době zaúčtování. |
| Fyzické výnosy | Částka odložených výnosů, která byla zaúčtována do hlavní knihy pro fyzickou aktualizaci. |
| ID nákladu | Pokud se aktuální transakce vztahuje k vytížení ve Správě dopravy, toto pole zobrazuje jedinečné číslo vytížení, které položku zahrnuje. |
| Fyzicky zaúčtováno | Hodnota, která označuje, zda byla vybraná transakce zásob fyzicky zaúčtována. Pokud je aktuální transakce zaúčtována do hlavní knihy, bude k dispozici i fyzický doklad. |
| Finančně zúčtováno | Hodnota, která označuje, zda byla vybraná transakce zásob finančně zaúčtována. Pokud je aktuální transakce zaúčtována do hlavní knihy, bude k dispozici i finanční doklad. |
| Zaúčtovaný fyzický poplatek | Hodnota, která udává, zda byly zaúčtovány fyzické poplatky související s vybranou transakcí zásob. |
| Zaúčtovaný finanční poplatek | Hodnota, která udává, zda byly zaúčtovány finanční poplatky související s vybranou transakcí zásob. |
| Finanční doklad | Číslo dokladu v hlavní knize, kde bylo vygenerováno finanční vyúčtování. |
| Faktura | Vygenerované číslo faktury, například pro nákupní objednávku nebo prodejní objednávku. |
| Úprava | Částka, která byla upravena u vybrané transakce zásob z procesu uzavření a úpravy zásob. |
| Zisk a ztráta, zaúčtovaná částka | Částka vybrané transakce zásob, která byla zaúčtována do výkazu zisků a ztrát. |
| Nezaúčtovaná faktura | Číslo faktury související nákupní objednávky, které se zobrazí na stránce **Nevyřízená faktura dodavatele**. |
| Finančně uzavřeno | Datum úplného vypořádání transakce. |
| Pokryté množství v SH | Skutečná hmotnost, na kterou se vztahuje vyrovnání. |
| Vyrovnané množství | Množství, které bylo vypořádáno pro vybranou transakci zásob. |
| Uhrazená částka | Hodnota, která byla vypořádána pro vybranou transakci zásob. |
