---
title: Migrace z aplikace AX 2012 na aplikaci Finance and Operations
description: "Tento článek poskytuje přehled možností migrace produktů a řízení skladů v aplikaci Dynamics 365 for Finance and Operations."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: cacf48bc10be5c06154816c2f9951ab4bbaee1c1
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---

# <a name="migrate-from-ax-2012-to-finance-and-operations"></a>Migrace z aplikace AX 2012 na aplikaci Finance and Operations

Toto téma poskytuje přehled možností migrace produktů a řízení skladů v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

<a name="introduction"></a>Úvod
------------

Během upgradu na aplikaci Finance and Operations jsou blokovány produkty, pokud mají přidruženou skupinu dimenzí úložiště, která obsahuje nastavení nesplňující požadavky na nastavení skupiny dimenze úložiště dané aplikací Finance and Operations. Po upgradu však můžete možnosti sady migrace v procesu **změnit skupinu dimenzí úložiště položek** použít k odblokování produktů, které byly zablokovány během upgradu. Poté můžete zpracovávat transakce k těmto produktům. Některé položky mohou již souviset se skupinami dimenze úložiště, kde jsou aktivní a fyzicky sledované dimenze Pracoviště, Sklad a Místo. V takovém případě můžete použít proces **Změnit skupinu dimenze úložiště položek**, aby bylo možné používat tyto položky v procesech správy skladu. Tato funkce je užitečná, pokud chcete použít funkci správy skladu pro existující položky.

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a>Upgrade na Finance and Operations při použití aplikace AX 2012 R3 WMSII
Finance and Operations již nepodporuje zastaralý modul **WMSII** aplikace Microsoft Dynamics AX 2012. Místo toho můžete použít nový modul **Řízení skladu**. V předchozích verzích bylo možné vybírat dimenze Místo a ID palety pro finančních zásoby. V rámci procesu upgradu však již nelze dimenzi zásob ID palety povolit pro finanční zásoby. Všechny produkty, které jsou přidružené ke skupině dimenzí úložiště, jež používá dimenzi zásob ID palety, bude zablokována a nebude zpracována.

### <a name="enabling-items-in-finance-and-operations"></a>Povolení položek v aplikaci Finance and Operations

V aplikaci Finance and Operations musí být položky, které budou použity jako součást procesů správy skladu, přidruženy ke skupině dimenze úložiště, kde je vybrán parametr **Používat procesy správy skladu**. Pokud je vybráno toto nastavení, budou aktivní dimenzí zásob pracoviště, sklad, stav skladu, umístění a registrační značku vozidla. Na tento typ skupiny dimenze úložiště můžete přejít pouze u položek, které jsou již přidruženy ke skupinám dimenzí úložiště, kde je aktivní skladové místo skladových zásob.

### <a name="items-that-are-blocked-for-inventory-updates"></a>Položky se zablokovanými aktualizacemi zásob

Pokud chcete zobrazit seznam vydaných produktů, které byly zablokovány během upgradu a nelze je zpracovat, klikněte na tlačítko **řízení zásob** &gt; **Nastavení** &gt; **zásoby** &gt; **Položky blokované pro aktualizaci zásob**.

### <a name="reapplying-blocked-products"></a>Opětovné použití blokovaných produktů

Pokud chcete odblokovat produkty, které byly zablokovány během upgradu, musíte vybrat novou skupinu dimenzí úložiště pro produkty. Mějte na paměti, že můžete změnit skupinu dimenze úložiště i v případě, že existují otevřené skladové transakce. Chcete-li používat položky, které byly zablokovány během upgradu, jsou k dispozici dvě možnosti:

-   Změňte skupinu dimenze úložiště pro položku na skupinu dimenzí úložiště, která používá pouze dimenze Pracoviště, Sklad a Místo. Výsledkem této změny je, že se přestane používat dimenze zásob ID palety.
-   Změňte skupinu dimenze úložiště pro položku na skupinu dimenzí úložiště, která používá proces řízení skladů. Výsledkem této změny je, že se nyní začne používat dimenze Registrační značka.

### <a name="migration-processes"></a>Procesy migrace

V aplikaci Finance and Operations je sledování položky součástí procesů řízení skladu. Pro tyto procesy musí být všechny sklady a jejich umístění spojena s profilem skladového místa. Konceptuálně platí, že pokud chcete používat procesy řízení skladů, je nutné zpracovat dva procesy:

-   Existují sklady musí být povoleny, aby bylo možné používat procesy správy skladu.
-   Existující uvolněné produkty musí mít přiřazenu novou skupinu dimenzí úložiště, která používá procesy správy skladu.

Pokud zdrojové skupiny dimenze úložiště používají dimenzi zásob ID palety, musí být umístění stávajících zásob na skladě, které používají dimenzi skladu ID palety přidružené k profilu umístění, kde je vybrán parametr **Použít sledování registrační značky**. Pokud nemusí být stávající sklady povoleny, aby mohly používat procesy řízení skladů, můžete změnit skupiny dimenzí úložiště ze stávajících zásob na skladě do skupin, které zpracovávají pouze dimenze Pracoviště, Sklad a Umístění zásob.

### <a name="using-the-warehouse-management-processes"></a>Použití procesů řízení skladu

Než bude možné použít vydané produkty v modulu **Řízení skladu**, musí produkty používat skupinu dimenze úložiště, ve které je vybraný parametr **Používat procesy řízení skladu**.

#### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Povolení skladům používat procesy řízení skladu

1.  Vytvořte alespoň jeden nový profil skladového místa
2.  Klikněte na **řízení skladu** &gt; **Nastavení** &gt; **Povolit procesy řízení skladu** &gt; **Povolit nastavení skladu**.
3.  Na stránce **Povolit nastavení skladu** přidejte sklady, které mají být povoleny. Tento krok můžete dokončit přímo na stránce nebo pomocí integrace aplikace Microsoft Office.
4.  Přiřadíte profil skladového místa všem skladovým místům. Tento krok můžete snadno dokončit pomocí integrace aplikace Microsoft Office přímo na stránce. Můžete exportovat a importovat data nebo použít zpracování datové entity v modulu [Správa dat](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities).
5.  Ověřte změny. V rámci procesu ověření probíhají různá ověření integrity dat. V rámci rozsáhlejšího procesu upgradu může být nutné upravit problémy, které nastanou, ve zdrojové implementaci. V tomto případě bude vyžadován další upgrade dat.
6.  Zpracujte změny.

#### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Změňte skupinu dimenzí úložiště pro položky tak, aby používaly procesy řízení skladu.

1.  Vytvořte novou hodnotu **Stav zásob** a přiřaďte ji jako **výchozí ID stavu zásob** v nastavení **parametry správy skladu**.
2.  Vytvořte novou skupinu dimenzí úložiště, kde je vybrán parametr **používat procesy správy skladu**.
3.  Na stránce **Hierarchie rezervací** definujte novou hierarchii rezervací podle skupiny skladu a dimenzí sledování.
4.  Vytvořte jednu nebo více skupin klasifikace jednotek, které obsahují přinejmenším stejné jednotky, jaké se používají pro skladové položky.
5.  Klikněte na **Řízení skladu** &gt; **Nastavení** &gt; **Povolit procesy řízení skladu** &gt; **Změnit skupinu dimenzí úložiště pro položky**.
6.  Na stránce **Změnit skupinu dimenzí úložiště položek** přidejte čísla položky, skupiny dimenze úložiště a skupiny klasifikace jednotek. Tento krok můžete dokončit přímo na stránce pomocí integrace Microsoft Office nebo procesu entity dat v modulu [Správa dat](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities).
7.  Ověřte změny. V rámci procesu ověření probíhají různá ověření integrity dat. V rámci rozsáhlejšího procesu upgradu může být nutné upravit problémy, které nastanou, ve zdrojové implementaci. V tomto případě bude vyžadován další upgrade dat.
8.  Zpracujte změny. Aktualizace všech dimenzí zásob může chvíli trvat. Průběh můžete sledovat pomocí úkolů dávkové úlohy můžete sledovat.



