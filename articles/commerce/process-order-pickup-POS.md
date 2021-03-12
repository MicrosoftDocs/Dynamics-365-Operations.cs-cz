---
title: Zpracování vyzvednutí objednávek zákazníků v POS
description: Toto téma vysvětluje funkci, která je k dispozici v aplikaci POS (Point of Sale) pro zpracování vyzvednutí objednávky zákazníka.
author: Hhainesms
manager: annbe
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 2156542ed0932fab6fb4fa4035e009ad89eeb18f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003746"
---
# <a name="process-customer-order-pickups-in-pos"></a>Zpracování vyzvednutí objednávek zákazníků v POS

[!include [banner](includes/banner.md)]

Když je vytvořena [objednávka zákazníka](customer-orders-overview.md) pro vyzvednutí v obchodě, může uživatel obchodu zahájit vyzvednutí zásob pomocí aplikace POS (Point of Sale). POS spustí zachycení konečné platby podle potřeby. Dokončí také účtování zásob a financí pro množství, která jsou vyzvednuta.

Pokud jste uživatelem obchodu, můžete vyzvednutí provést buď pomocí operace **Odvolání objednávky** nebo **Vyřízení objednávky** v POS. Chcete-li mít operaci **Vyzvednout** k dispozici, musíte nejprve provést jeden z těchto kroků:

- Chcete-li použít operaci **Odvolání objednávky**, vyhledejte a vyberte objednávku, která bude vyzvednuta.
- Chcete-li použít operaci **Vyřízení objednávky**, vyhledejte a vyberte jeden nebo více řádků objednávky.

Pokud vybraná objednávka nebo řádky objednávky nejsou nakonfigurovány pro vyzvednutí v tomto konkrétním obchodě nebo pokud již byla objednávka plně vyzvednuta, operace **Vyzvednout** nebude k dispozici.

![Operace vyzvednutí](media/pickupoperation.png)

V Microsoft Dynamics 365 Commerce verze 10.0.17 a novější lze funkci **Vylepšené uživatelské prostředí pro zpracování vyzvednutí objednávek v pokladním místě** prostřednictvím správy funkcí v centrále Commerce. Pokud je tato funkce vypnutá, uživatelé nemohou vybrat množství vyzvednutí. Ve výchozím nastavení je celé množství objednané pro řádek množstvím, které bude vyzvednuto. Tato zkušenost může být problematická, protože uživatelé mohou zapomenout vybrat některé položky k vyzvednutí, když provádějí vyzvednutí prostřednictvím plnění objednávky.

Funkce **Vylepšené uživatelské prostředí pro zpracování vyzvednutí objednávek v pokladním místě** poskytuje uživatelům větší kontrolu nad výběrem produktů, které budou vyzvednuty, a nad množstvím produktů, které budou vyzvednuty. Uživatelé nemusí vybrat každý řádek prodejní objednávky na stránce plnění objednávky, než vyberou **Vyzvednout**. Zobrazí se všechny položky, které lze vyzvednout. Uživatelé mohou zadat více řádků pro vyzvednutí, i když je vybrána pouze jedna produktová řada.

Když je zapnutá funkce **Vylepšené uživatelské prostředí pro zpracování vyzvednutí objednávek v pokladním místě** a vyberete operaci **Vyzvednout**, zobrazí se dialogové okno **Vyzvednutí**. Zde můžete vybrat položky a množství, která budou vyzvednuta. Ve výchozím nastavení je jakékoli objednané množství, které má inventář ve vyzvednutém nebo zabaleném stavu, považováno za způsobilé k vyzvednutí. Ve výchozím nastavení je toto množství nastaveno jako množství vyzvednutí. Zadané množství můžete změnit za předpokladu, že množství není 0 (nula) a nepřekročí celkové otevřené (tj. nevyfakturované) množství pro vybraný řádek.

![Dialogové okno Vyzvednutí](media/pickupselect.png)

Poté, co vyberete množství, která budou vyzvednuta, a poté vyberte **Vyzvednout**, zobrazí se stránka transakce. Pokud je zapnutá funkce [vícekanálové platby](omni-channel-payments.md) existují předběžně autorizované platby kreditní kartou, musíte použít platbu.

Na stránce transakce systém vypočítá částky, které jsou splatné, výpočtem celkové částky, která je splatná u vybraných položek vyzvednutí, a poté odečte všechny dříve použité vklady nebo autorizované platby kreditní kartou. K dokončení transakce vyzvednutí musíte zpracovat platbu. Pokud je [rozložení obrazovky](pos-screen-layouts.md) stránky transakce nakonfigurováno tak, aby obsahovalo operaci **Uzavřít transakci** a není splatná žádná částka, můžete transakci dokončit bez výběru platební metody. Pokud operace **Uzavřít transakci** není k dispozici, můžete vybrat odkaz **Splatná částka 0,00 Kč** v podokně **Celkem** k uzavření transakce bez nutnosti výběru platební metody.

![Transakční stránka pro transakci vyzvednutí objednávky zákazníka](media/pickupcart.png)

## <a name="changing-pickup-lines-or-quantities"></a>Změna řádků vyzvednutí nebo množství

Pokud musíte změnit množství vyzvednutí poté, co vyberete položky, které budou vyzvednuty, můžete vybrat **Nastavit množství**. Množství vyzvednutí nemůžete nastavit na **0** (nula) nebo ji zvýšit na hodnotu, která přesahuje nevyfakturované množství, které pro objednaný řádek zbývá. Chcete-li odebrat řádek vyzvednutí z transakčního košíku, vyberte **Neplatná transakce**. Aktuální transakce bude zastavena a tok pro operaci **Vyzvednutí** bude restartován.

Pokud je zapnutá funkce **Vylepšit uživatelské prostředí pro zpracování vyzvednutí objednávek v pokladním místě**, mohou organizace přidat tlačítko pro operaci **Změnit řádky vyzvednutí** do rozložení obrazovky stránky transakce. Poté, co vytvoříte nákupní košík transakce vyzvednutí v POS a vyberete položky, můžete vybrat **Změnit řádky vyzvednutí**, pokud musíte změnit vyzvedávané položky, ale nechcete zneplatnit celou transakci. V dialogovém okně **Změnit řádky vyzvednutí** můžete změnit položky k vyzvednutí a množství. Košík transakcí se poté aktualizuje, aby odrážel vaše změny.

![Dialogové okno Změnit vyzvedávané položky](media/pickupchange.png)
