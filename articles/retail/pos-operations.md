---
title: Online a offline operace pokladního místa (POS)
description: Toto téma obsahuje podrobnosti týkající se operací pokladních míst (POS) v aplikaci Microsoft Dynamics 365 for Retail. Určuje, kde lze v aplikaci vyvolat operace, a zda jsou k dispozici v offline režimu.
author: jblucher
manager: AnnBe
ms.date: 10/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-09-27
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9354e0dbf8bed9383a9dfcc383a2c9db57457dd0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "353809"
---
# <a name="online-and-offline-point-of-sale-pos-operations"></a>Online a offline operace pokladního místa (POS)

[!include [banner](includes/banner.md)]

Většina akcí, které uživatel provede v pokladním místě, se považuje za operace. Operace jsou konfigurovány a spravovány v účetním systému Microsoft Dynamics 365 for Retail. Mnohé operace lze přidat k tlačítkům v POS mřížce tlačítek. Uživatelé mohou potom vybírat tlačítka k vyvolání operací a provádění jejich funkcí. Další operace jsou součástí hlavní aplikace POS a jsou vyvolávány buď pomocí tlačítek na obrazovce nebo jako součást jiných workflow nebo procesů.

Následující tabulka obsahuje podrobnosti o operacích, které jsou k dispozici v Retail Modern POS a Cloud POS pro Dynamics 365 for Retail. Tabulka rovněž určuje, kde lze v aplikaci vyvolat operace, a zda jsou k dispozici, když je pokladní místo (POS) v offline režimu.

Některé operace nejsou v současné době dostupné v Retail Modern POS nebo Cloud POS pro Dynamics 365 for Retail. Některé z těchto operací jsou buď operacemi specifickými pro národní prostředí, která vyžadují další rozšíření a konfigurace. Jiné jsou funkce aplikace Microsoft Dynamics AX 2012, které nejsou aktuálně podporovány.

Následující sloupce určují, kde lze operace vyvolat:

- **Mřížka tlačítek** – Operace může být přiřazena k tlačítkům v mřížkách tlačítek POS, které jsou součástí rozložení obrazovky POS.
- **Obrazovka transakce** – Operaci lze vyvolat z mřížek tlačítek POS, které jsou konfigurovány na obrazovce transakcí POS.
- **Uvítací obrazovka** – Operaci lze vyvolat z mřížek tlačítek POS, které jsou konfigurovány na uvítací obrazovce POS.

> [!NOTE]
> Následující operace se vztahují na nejnovější verzi aplikace Dynamics 365 for Retail. Některé operace se mohly změnit, nebo nemusí být k dispozici v předchozích verzích.

| ID | Operace | popis | Mřížka tlačítek | Obrazovka transakce | Uvítací obrazovka | K dispozici offline | Specifické pro národní prostředí |
|----|-----------|-------------|-------------|--------------------|----------------|-------------------|-----------------|
| 707 | Aktivovat zařízení | Aktivujte aktuální zařízení tím, že umožníte ověřenému uživateli poskytnout informace o připojení a přiřadit ID zařízení a pokladny. | Ne | Ne | Ne | Ne | Ne |
| 134 | Přidat umístění | Přidání předem vybraného umístění k transakci. Umístění vyberte na stránce **Vlastnosti tlačítka**. | Ano | Ano | Ne | Ano | Ne |
| 135 | Přidat umístění ze seznamu | Přidejte umístění k transakci tak, že ji vyberete ze seznamu. | Ano | Ano | Ano | Ano | Žádný |
| 137 | Přidat umístění k odběrateli | Přidejte umístění k odběrateli na stránce **Podrobnosti odběratele**. | Žádný | Žádný | Žádný | Ano | Žádný |
| 138 | Odstranit umístění od odběratele | Odstraňte umístění na stránce **Podrobnosti odběratele**. | Žádný | Žádný | Žádný | Ano | Žádný |
| 643 | Přidat kód kupónu | Přidejte kupón zadáním jeho kódu do POS. | Ano | Ano | Ne | Ano | Ne |
| 117 | Přidat věrnostní kartu | Vyzvěte uživatele k zadání čísla věrnostní karty, které budé přidáno do aktuální transakce. | Ano | Ano | Ne | Ano | Ne |
| 136 | Přidat sériové číslo | Tato operace umožňuje uživateli specifikovat sériové číslo pro aktuálně vybraný produkt. | Ano | Ano | Ne | Ano | Ne |
| 1214 | Přidat dodací adresu | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ne |
| 519 | Přidat k dárkovému poukazu | Umožňuje přidat peníze na vybraný dárkový poukaz. | Ano | Ano | Ne | Ne | Ne |
| 6000 | Povolit přeskočení registrační poklady | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ano |
| 1212 | Odvod do banky | Zaznamená finanční částku odeslanou do banky a další informace, například číslo bankovního balíčku. | Ano | Ano | Ano | Ano | Ne |
| 923 | Banka celkem – ověření | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ano |
| 915 | Prázdná operace | Tato operace představuje přizpůsobitelné tlačítko, které může vývojář softwaru naprogramovat na libovolnou specializovanou operaci, kterou firma potřebuje. | Ano | Ano | Ano | Ano | Ne |
| 1053 | Zavřít směnu bez zadání částky | Nastavte aktuální směnu na uzavřenou bez zadání částky a odhlaste uživatele. Směna uzavřená bez zadání částky je uzavřena pro další transakce, ale je stále otevřena pro operace zásuvky, jako jsou odebrání úhrady a výkaz úhrad. | Ano | Ano | Ano | Ne | Ne |
| 310 | Vypočítat součet | Při zpoždění výpočtu slev tato operace spustí výpočet pro aktuální transakci. | Ano | Ano | Ne | Ano | Ne |
| 642 | Vyvézt všechny produkty | Nastavte způsob dodání pro všechny řádky na **Carryout**. | Ano | Ano | Ne | Ano\* | Ne |
| 641 | Vyvézt vybrané produkty | Nastavte způsob dodání pro zvolené řádky na **Carryout**. | Ano | Ano | Ne | Ano\* | Ne |
| 1215 | Změnit heslo | Tato operace umožňuje uživateli POS měnit své heslo. | Ano | Ano | Ano | Ne | Ne |
| 123 | Změnit měrnou jednotku | Změňte měrnou jednotku pro vybranou položku řádku. | Ano | Ano | Ne | Ano | Ne |
| 639 | Vymazat výchozího prodejního zástupce u transakce | Odstraňte skupinu prodejní provize (obchodního zástupce) z transakce. | Ano | Ano | Ne | Ano | Ne |
| 106 | Vymazat množství | Resetujte množství na aktuálně vybraném řádku na **1**. | Ano | Ano | Ne | Ano | Ne |
| 640 | Vymazat prodejního zástupce na řádku | Odstraňte skupinu prodejní provize (obchodní zástupce) z aktuálně vybraného řádku. | Ano | Ano | Ne | Ano | Ne |
| 121 | Vymazat prodejce | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ne |
| 1055 | Zavřít směnu | Uzavřete aktuální směnu, vytiskněte sestavu Z a odhlaste uživatele ze systému. | Ano | Ano | Ano | Ne | Ne |
| 925 | Kopírovat bankovní šek | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ano |
| 620 | Vytvořit objednávku odběratele | Převeďte transakci POS na objednávku odběratele. | Ano | Ano | Ne | Ano\* | Ne |
| 621 | Vytvořit nabídku | Převeďte transakci POS na prodejní nabídku. | Ano | Ano | Ne | Ano\* | Ne |
| 636 | Vytvoření maloobchodní transakce | Tato operace umožňuje uživateli vytvořit standardní prodejní transakci, když má výchozí chování POS vytvářet objednávky odběratele. | Ano | Ano | Ne | Ano | Ne |
| 600 | Zákazník | Přidejte konkrétního zákazníka do transakce. | Ne | Ne | Ne | Ano | Ne |
| 1100 | Vklad na účet odběratele | Provede platbu na účet odběratele. | Ano | Ano | Ano | Ano | Ano |
| 612 | Přidat zákazníka | Tato operace umožňuje uživateli vytvořit nový záznam odběratele. | Ano | Ano | Ano | Ano† | Ne |
| 603 | Vymazat zákazníka | Odstraňte odběratele z aktuální transakce. | Ano | Ano | Ne | Ano | Ne |
| 602 | Hledat zákazníka | Tato operace umožní uživateli vyhledat záznam o odběrateli pomocí navigace na stránku vyhledávání odběratele v POS. | Ano | Ano | Ano | Ano | Ne |
| 609 | Transakce zákazníka | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ne |
| 917 | Stav připojení databáze | Tato operace umožňuje uživateli zobrazit aktuální nastavení připojení a přepínat mezi režimem online a offline. | Ano | Ano | Ano | Ano | Ne |
| 1200 | Počáteční částka výkazu | Deklaruje částku v zásuvce s hotovostí na začátku dne nebo směny. | Ano | Ano | Ano | Ano | Ne |
| 132 | Přepsání vkladu | Přepsání výchozího vkladu pro objednávky odběratelů. | Ano | Ano | Ne | Ano\* | Ne |
| 913 | Zakázat režim návrhu | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ne |
| 912 | Povolit režim návrhu | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ne |
| 1217 | Demontovat sady | Demontování sady na komponenty tvořené produkty. | Ano | Ano | Ano | Ano | Ne |
| 624 | Zobrazení částky refundace | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ano |
| 513 | Zobrazit součet | Zobrazte zůstatek transakce na displeji odběratele. | Ano | Ano | Ano | Ano | Ne |
| 623 | Upravit odběratele | Upravte podrobnosti aktuálního odběratele. | Ano | Ano | Ne | Ne | Ne |
| 614 | Upravit objednávku odběratele | Stornujte vybranou objednávku tak, aby ji bylo možné změnit v POS. | Ne | Ne | Ne | Ne | Ne |
| 615 | Upravit nabídku | Stornujte vybranou nabídku tak, aby ji bylo možné změnit v POS. | Ne | Ne | Ne | Ne | Ne |
| 518 | Účty výdajů | Zaznamená peníze odebrané ze zásuvky s hotovostí na příležitostné výdaje. | Ano | Ano | Ano | Ano | Ne |
| 919 | Rozšířené přihlášení | Přiřazení nebo odebrání oprávnění pro přihlášení naskenováním čárového kódu nebo pohybem karty. | Ano | Ano | Ano | Ne | Ne |
| 1201 | Zadání plovoucího zůstatku | Tato operace umožňuje uživateli přidat další peníze do aktuální zásuvky nebo směny. | Ano | Ano | Ano | Ano | Ne |
| 1218 | Vynutit odemčení periferního zařízení | Systém používá tuto operaci interně k odemknutí periferních zařízení v POS. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ne |
| 520 | Zůstatek dárkového poukazu | Zobrazí zůstatek dárkového poukazu. | Ano | Ano | Ne | Ne | Ne |
| 708 | Deaktivovat zařízení | Deaktivujte aktuální zařízení, aby ho nebylo možné použít jako pokladnu POS. | Ne | Ne | Ne | Ne | Ne |
| 517 | Účty příjmů | Zaznamená peníze, které jsou umístěny do zásuvky s hotovostí z jiného důvodu než kvůli prodeji. | Ano | Ano | Ano | Ano | Ne |
| 801 | Vyhledávání zásob | Vyhledejte dostupné množství, na objednávce, a množství dostupné pro slíbení (ATP) pro aktuální obchod a další dostupná umístění. | Ano | Ano | Ano | Ne | Ne |
| 122 | Komentář k faktuře | Tato operace umožňuje uživateli zadat poznámku týkající se aktuální transakce. | Ano | Ano | Ne | Ano | Ne |
| 511 | Vydat dobropis | Vydejte dobropis, abyste poskytli doklad namísto refundace. | Ano | Ano | Ne | Ne | Ne |
| 512 | Vydat dárkový poukaz | Vydejte nový dárkový poukaz pro konkrétní částku. | Ano | Ano | Ne | Ne | Ne |
| 625 | Vydat věrnostní kartu | Vydejte věrnostní kartu odběrateli. Odběratel se pak může účastnit věrnostního programu obchodu. | Ano | Ano | Ano | Ne | Ne |
| 300 | Částka řádkové slevy | Zadá částku slevy pro řádkovou položku v transakci. Tato operace se používá pouze pro položky, u nichž lze použít slevu, a pouze v rámci určeného rozmezí slev. | Ano | Ano | Ne | Ano | Ne |
| 301 | Procento řádkové slevy | Zadá procento slevy pro řádkovou položku v transakci. Tato operace se používá pouze pro položky, u nichž lze použít slevu, a pouze v rámci určeného rozmezí slev. | Ano | Ano | Ne | Ano | Ne |
| 703 | Zamknout pokladnu | Uzamkněte aktuální pokladnu, aby ji nebylo možné použít, ale neodhlašujte aktuálního uživatele. | Ne | Ne | Ne | Ano | Ne |
| 701 | Odhlásit | Odhlaste aktuálního uživatele z pokladny. | Ano | Ano | Ano | Ano | Ne |
| 521 | Zůstatek bodů na věrnostní kartě | Zobrazte zůstatek bodů pro konkrétní věrnostní kartu. | Ano | Ano | Žádný | Žádný | Žádný |
| 918 | Spravovat směny | Zobrazí seznam aktivních, pozastavených a bez zadání částky uzavřených směn. | Ano | Ano | Ano | Žádný | Žádný |
| 914 | Minimalizovat okno POS | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ne |
| 1 000 | Otevřít zásuvku | Proveďte operaci "bez prodeje" a otevřete aktuálně zvolené zásuvky s hotovostí. | Ano | Ano | Ano | Ano | Žádný |
| 928 | Plnění objednávek | Tato operace umožňuje uživatelům vydat, zabalit, expedovat nebo odvolat objednávky pro vyzvednutí v obchodě. | Ano | Ano | Ano | Žádný | Žádný |
| 129 | Přepsat daň řádkového produktu | Přepište daň u vybrané položky řádku a použijte jinou konkrétní daň. | Ano | Ano | Ne | Ano | Ne |
| 1.3.0 | Přepsat daň řádkového produktu ze seznamu | Přepište daň u vybrané položky řádku a použijte daň, kterou uživatel vybere ze seznamu. | Ano | Ano | Ne | Ano | Ne |
| 127 | Přepsat daň transakce | Přepište daň u transakce a použijte jinou konkrétní daň. | Ano | Ano | Ne | Ano | Ne |
| 128 | Přepsat daň transakce ze seznamu | Přepište daň u transakce a použijte daň, kterou uživatel vybere ze seznamu. | Ano | Ano | Ne | Ano | Ne |
| 131 | Dodací list | Vytvořte dodací list pro vybranou objednávku. | Ne | Ne | Ne | Ne | Ne |
| 710 | Párovat hardwarovou stanici | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ne |
| 201 | Platba kartou | Přijměte jako způsob platby kreditní nebo debetní kartu. | Ano | Ano | Ne | Ano | Ne |
| 200 | Platba v hotovosti | Přijme jako způsob platby hotovost. | Ano | Ano | Ne | Ano | Ne |
| 206 | Rychlá platba v hotovosti | Dokončete transakci jedním dotykem a přijměte částku, která je splatná v hotovosti (přesnou částku). | Ano | Ano | Ne | Ano | Ne |
| 204 | Platba šekem | Přijme jako způsob platby šek. | Ano | Ano | Ne | Ano | Ne |
| 213 | Platba dobropisem | Přijměte dobropis (doklad) vystavený obchodem. | Ano | Ano | Ne | Ne | Ne |
| 203 | Měna platby | Přijme platbu v různých měnách. | Ano | Ano | Ne | Ano | Ne |
| 202 | Platba z účtu zákazníka | Strhněte transakci z účtu odběratele. Tento způsob platby není platný pro vklady objednávky odběratele. | Ano | Ano | Ne | Ne | Ne |
| 214 | Platba dárkovým poukazem | Přijměte dárkový poukaz vydaný v obchodě. | Ano | Ano | Ne | Ne | Ne |
| 207 | Placení věrnostní kartou | Přijměte věrnostní kartu pro platbu a uplatněte body na kvalifikované produkty. | Ano | Ano | Ne | Ne | Ne |
| 634 | Historie plateb | Zobrazte historii plateb odběratele pro aktuální objednávku odběratele. | Ano | Ano | Ne | Ne | Ne |
| 803 | Výdej a příjem | Otevřete stránku **Výdej a příjem**, kde můžete vybrat objednávky k výdeji nebo příjmu v obchodě. | Ano | Ano | Ano | Ne | Ne |
| 632 | Vyzvednutí všech produktů | Nastavte metodu plnění na **Vyzvednutí v obchodě** pro všechny řádky. | Ano | Ano | Ne | Ano\* | Ne |
| 631 | Vydat vybrané produkty | Nastavte metodu plnění na **Vyzvednutí v obchodě** pro zvolené řádky. | Ano | Ano | Ne | Ano\* | Ne |
| 400 | Místní nabídka | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ne |
| 101 | Kontrola ceny | Tato operace umožňuje uživateli vyhledávání ceny pro určený produkt. | Ano | Ano | Ano | Ano | Ne |
| 104 | Přepsání ceny | Přepiště cenu produktu, pokud byl produkt nastaven tak, aby umožňoval přepsání ceny. | Ano | Ano | Ne | Ano | Ne |
| 1058 | Tisknout finanční sestavu X | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ano |
| 1059 | Tisknout finanční sestavu Z | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ano |
| 927 | Tisk štítku položky | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ne |
| 926 | Tisk štítku na polici | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ne |
| 1056 | Tisknout X | Vytiskněte sestavu X pro aktuální směnu. | Ano | Ano | Ano | Ne | Ne |
| 103 | Komentář k produktu | Přidá poznámku k vybrané řádkové položce transakce. | Ano | Ano | Ne | Ano | Ne |
| 100 | Prodej produktu | Přidejte konkrétní produkt do transakce. | Ano | Ano | Ano | Ano | Ne |
| 108 | Hledání produktu | Tato operace umožní uživateli vyhledat produkt pomocí navigace na stránku vyhledávání produktu v POS. | Ano | Ano | Ano | Ano | Ne |
| 633 | Datum vypršení platnosti nabídky | Tato operace umožňuje uživateli zobrazit nebo změnit datum vypršení platnosti prodejní nabídky. | Ano | Ano | Ne | Ano\* | Ne |
| 627 | Přepočítat | Přepočítejte všechny řádky objednávky odběratele a daně, založené na aktuální konfiguraci. | Ano | Ano | Ne | Ano\* | Ne |
| 515 | Odvolat objednávku | Tato operace umožňuje uživateli hledat a stornovat objednávky odběratele a prodejní nabídky. | Ano | Ano | Ano | Ne | Ne |
| 504 | Odvolat transakci | Tato operace umožňuje uživateli stornovat dříve pozastavené transakce z aktuálního obchodu. | Ano | Ano | Ne | Ano‡ | Ne |
| 305 | Uplatnit věrnostní body | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ano |
| 635 | Refundovat dopravné | Tato operace umožňuje uživateli refunovat dopravné u zrušené objednávky. | Ne | Ne | Ne | Ne | Ne |
| 644 | Odebrat kód kupónu | Vyzvěte uživatele k odstranění kupónů jejich výběrem v seznamu kupónů, které jsou aktuálně přidruženy k transakci. | Ano | Ano | Ne | Ano | Ne |
| 1057 | Znovu vytisknout Z | Znovu vytiskněte sestavu Z pro předchozí směnu nebo vybranou směnu. | Ano | Ano | Ano | Ne | Ne |
| 1216 | Zadejte nové heslo | Tato operace umožní uživateli, který má oprávnění k obnovení hesla, resetovat heslo jiného zaměstnance pomocí dočasného hesla. | Ano | Ano | Ano | Žádný | Žádný |
| 1219 | Otevření URL adresy v POS | Tato operace umožňuje uživateli otevření adresy URL konfigurované správcem v pokladním místě. | Ano | Ano | Ano | Ano | Ne | 
| 109 | Vrátit produkt | Provede vrácení jednotlivých produktů. Další naskenovaný produkt se zobrazí jako vracený produkt, který má záporné množství a cenu. | Ano | Ano | Ne | Ano | Ne |
| 114 | Transakce vracení | Stornujte předchozí transakci podle jejího čísla příjemky pro vrácení některého nebo všech produktů. | Ano | Ano | Ano | Ano§ | Ne |
| 1211 | Odvod do trezoru | Provede odvod do trezoru při přesunu peněz z pokladny do trezoru. | Ano | Ano | Ano | Ano | Ne |
| 516 | Prodejní faktura | Tato operace umožňuje odběrateli provést platby vůči vybrané prodejní faktuře. | Ano | Ano | Ne | Ne | Ne |
| 502 | Prodejce | Tato operace umožňuje uživateli nastavit hodnotu **Osoba přebírající zboží** na prodejní objednávce pro objednávky odběratelů v POS. | Ano | Ano | Ne | Ano\* | Ne |
| 2000 | Správa plánu | Tato operace umožňuje uživatelům vytvořit, upravit nebo zobrazit plány zaměstnance. | Ano | Ano | Ano | Ne | Ne |
| 2001 | Požadavky na plán | Tato operace umožňuje uživateli požádat o volno, zaměnit směny nebo nabídnout směny jiným zaměstnancům. | Ano | Ano | Ano | Ne | Ne |
| 622 | Vyhledat | Tato operace umožňuje uživatelům předem nakonfigurovat POS tlačítka k vyhledávání podle položek, odběratele nebo kategorie. | Ano | Ano | Ano | Ano | Ne |
| 1213 | Hledat dodací adresu | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ne |
| 709 | Vybrat hardwarovou stanici | Tato operace uživateli umožňuje vybrat hardwarovou stanici v seznamu dostupných hardwarových stanic. | Ano | Ano | Ano | Ano | Ne |
| 637 | Nastavit výchozího prodejního zástupce u transakce | Tato operace umožňuje uživateli vybrat jednu z možných skupin prodejní provize (obchodní zástupce) jako výchozího obchodního zástupce pro řádky, které jsou přidány později. | Ano | Ano | Ne | Ano | Ne |
| 105 | Nastavit množství | Změní množství řádkové položky v transakci. | Ano | Ano | Ne | Ano | Ne |
| 638 | Nastavit prodejního zástupce na řádku | Tato operace umožňuje uživateli vybrat jednu z možných skupin prodejní provize (obchodní zástupce) pro aktuálně zvolený řádek. | Ano | Ano | Ne | Ano | Ne |
| 630 | Expedovat všechny produkty | Nastavte režim plnění na **Expedice** pro všechny položky řádku. | Ano | Ano | Ne | Ano\* | Ne |
| 629 | Expedovat vybrané produkty | Nastavte způsob plnění pro zvolené řádky na **Expedice**. | Ano | Ano | Žádný | Ano\* | Žádný |
| 115 | Zobrazit deník | Zobrazte deník obchodu. Můžete zobrazit transakce, znovu vytisknout příjemky a dárkové příjemky a stornovat k vrácení. | Ano | Ano | Ano | Ano\*\* | Ne |
| 802 | Počet na skladě | Tato operace umožňuje uživateli vytvořit nebo upravit deníky inventur skladu pro fyzické zásoby nebo cyklické inventury. | Ano | Ano | Ano | Ne | Ne |
| 401 | Podnabídka | Tato operace zavede uživatele k jiné propojené mřížce tlačítek. | Ano | Ano | Ano | Ano | Ne |
| 1054 | Pozastavit směnu | Pozastavte aktuální směnu tak, aby nová nebo odlišná směna mohla být aktivována na aktuální pokladně. | Ano | Ano | Ano | Ne | Ne |
| 503 | Pozastavit transakci | Pozastavte aktuální prodejní transakce tak, aby je bylo možné stornovat později v obchodě. | Ano | Ano | Ne | Ano‡ | Ne |
| 1004 | Záznamník úkolů | Otevřete záznamník úkolů pro záznam kroků postupu v POS. | Ne | Ne | Ne | Ano | Ne |
| 1052 | Výkaz úhrad | Tato operace umožňuje uživateli zadat peněžní částku v zásuvce pro každou vypočtenou platební metodu. | Ano | Ano | Ano | Ano | Ne |
| 1210 | Odstranění úhrady | Tato operace umožňuje uživateli odebrat peníze z aktuální zásuvky nebo směny. | Ano | Ano | Ano | Ano | Ne |
| 920 | Časové hodiny | Tato operace uživatelům umožňuje přihlášení a odhlášení do pracovních směn a k přestávkám. | Ano | Ano | Ano | Ne | Ne |
| 302 | Částka celkové slevy | Zadání částku slevy pro transakci. Tato operace se používá pouze pro položky, u nichž lze použít slevu, a pouze v rámci určeného rozmezí slev. | Ano | Ano | Ne | Ano | Ne |
| 303 | Procento celkové slevy | Zadejte procento slevy pro transakci. Tato operace se používá pouze pro položky, u nichž lze použít slevu, a pouze v rámci určeného rozmezí slev. | Ano | Ano | Ne | Ano | Ne |
| 501 | Komentář k transakci | Přidejte k aktuální transakci poznámku. | Ano | Ano | Ne | Ano | Ne |
| 922 | Zobrazit podrobnosti produktu | Otevřete stránku podrobností produktů pro aktuáloně vybranou položku řádku. | Ano | Ano | Ne | Ano | Ne |
| 1003 | Zobrazit sestavy | Zobrazte sestavy, které byly konfigurovány pro aktuálního uživatele. | Ano | Ano | Ano | Ne | Ne |
| 921 | Zobrazit časové položky | Zobrazte časové záznamy pro všechny pracovníky v obchodě. | Ano | Ano | Ano | Ne | Ne |
| 211 | Anulovat platbu | Anulujte aktuálně vybraný řádek platby z transakce. | Ano | Ano | Ne | Ano | Ne |
| 102 | Anulovat produkt | Anulujte aktuálně vybranou položku řádku platby z transakce. | Ano | Ano | Ne | Ano | Ne |
| 500 | Anulovat transakci | Anulujte aktuální transakci. | Ano | Ano | Ne | Ano | Ne |
| 916 | Programovací model Windows Workflow Foundation | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ne |
| 924 | Sestava X pro bankovní karty | Tato operace není podporována. | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ano |

\* Operace je k dispozici v offline režimu pouze v případě, že vytváříte objednávku odběratele nebo prodejní nabídku, a pouze v případě, že v profilu funkce POS je nakonfigurováno offline vytvoření objednávky odběratele a prodejní nabídky. Operaci nelze provést při vytváření objednávek pomocí služby Real-time Service, nebo pokud jsou objednávky stronovány nebo upravovány.

† Operaci lze provést v offline režimu pouze v případě, že POS je nakonfigurováno tak, aby umožnilo offline vytvoření odběratelů v profilu funkce POS.

‡ Když je POS offline, pozastavené transakce lze stornovat pouze z offline databáze aktuální pokladny. Uživatelé nemohou pozastavit a odvolat transakce mezi pokladnami.

§ Když je POS offline, pouze transakce v aktuální offline databázi lze stornovat k vrácení.

\*\* Když je POS offline, pouze transakce v aktuální offline databázi kanálů se zobrazí v deníku.
