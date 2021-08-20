---
title: Upgrade správy skladu z Microsoft Dynamics AX 2012 do Supply Chain Management
description: Toto téma poskytuje přehled možností migrace produktů a řízení skladu.
author: perlynne
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ac8c0d8781e5146186fbf71ce619f90ca3556ccefefe7e974efded7e0eb86dd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775428"
---
# <a name="upgrade-warehouse-management-from-microsoft-dynamics-ax-2012-to-supply-chain-management"></a>Upgrade správy skladu z Microsoft Dynamics AX 2012 do Supply Chain Management 


[!include [banner](../includes/banner.md)]

Toto téma uvádí přehled procesu upgradu z Microsoft Dynamics AX 2012 R3, s modulem WMSII do Supply Chain Management.

Supply Chain Management již nepodporuje zastaralý modul **WMSII** aplikace Microsoft Dynamics AX 2012. Místo toho můžete použít modul **Řízení skladu**. V modulu WMSII by mohlo být možné vybrat dimenze Skladové místo a ID palety pro finanční zásoby, dimenzi zásob ID palety však nelze použít pro finanční zásoby v modulu Supply Chain Management.

Během upgradu jsou všechny produkty, které jsou přiřazeny ke skupině dimenzí úložiště, která používá dimenzi zásob ID palety, označené jako blokované a Nezpracováno pro upgrade.

## <a name="upgrading-to-supply-chain-management-when-ax-2012-r3-wmsii-is-used"></a>Upgrade na Supply Chain Management při použití AX 2012 R3 WMSII
Po upgradu však můžete možnosti sady migrace v procesu **změnit skupinu dimenzí úložiště položek** použít k odblokování produktů, které byly zablokovány během upgradu, a následně zpracovat transakce pro tyto produkty.

### <a name="enabling-items-in-supply-chain-management"></a>Povolení položek v Supply Chain Management 
V aplikaci Supply Chain Management je tato změna potřeba, protože sledování položky je součástí procesů řízení skladu. Pro tyto procesy musí být všechny sklady a jejich umístění spojena s profilem skladového místa. Konceptuálně platí, že pokud chcete používat procesy řízení skladů, je nutné nakonfigurovat následující:
-   Existují sklady musí být povoleny, aby bylo možné používat procesy správy skladu. 
-   Existující uvolněné produkty musí mít přiřazenu skupinu dimenzí úložiště, která používá procesy správy skladu. 

Pokud zdrojové skupiny dimenze úložiště používají dimenzi zásob ID palety, musí být umístění stávajících zásob na skladě, které používají dimenzi skladu ID palety přidružené k profilu umístění, kde je vybrán parametr **Použít sledování registrační značky**. Pokud nemusí být stávající sklady povoleny, aby mohly používat procesy řízení skladů, můžete změnit skupiny dimenzí úložiště ze stávajících zásob na skladě do skupin, které zpracovávají pouze dimenze Pracoviště, Sklad a Umístění zásob. 

> [!NOTE] 
>  Můžete změnit skupinu dimenze úložiště i v případě, že existují otevřené skladové transakce.

## <a name="find-products-that-were-blocked-because-of-pallet-id"></a>Vyhledejte produkty, které byly blokovány z důvodu ID palety
Pokud chcete zobrazit seznam vydaných produktů, které byly zablokovány během upgradu a nelze je zpracovat, klikněte na tlačítko **řízení zásob** &gt; **Nastavení** &gt; **zásoby** &gt; **Položky blokované pro aktualizaci zásob**.

## <a name="change-storage-dimension-group-for-blocked-products"></a>Změnit skupinu dimenze úložiště Blokované produkty 
 
Položky, které budou použity jako součást procesů správy skladu, musí být přidruženy ke skupině dimenze úložiště, kde je vybrán parametr **Používat procesy správy skladu**, aby mohly být použity jako součást procesu řízení skladu. Pokud je vybráno toto nastavení, budou aktivní dimenzí zásob pracoviště, sklad, stav skladu, umístění a registrační značku vozidla.

Pokud chcete odblokovat produkty, které byly zablokovány během upgradu, musíte vybrat novou skupinu dimenzí úložiště pro produkty. Mějte na paměti, že můžete změnit skupinu dimenze úložiště i v případě, že existují otevřené skladové transakce. Chcete-li používat položky, které byly zablokovány během upgradu, jsou k dispozici dvě možnosti:

-   Změňte skupinu dimenze úložiště pro položku na skupinu dimenzí úložiště, která používá pouze dimenze Pracoviště, Sklad a Místo. Výsledkem této změny je, že se přestane používat dimenze zásob ID palety.
-   Změňte skupinu dimenze úložiště pro položku na skupinu dimenzí úložiště, která používá proces řízení skladů. Výsledkem této změny je, že se nyní začne používat dimenze Registrační značka.

## <a name="configure-warehouse-management-processes"></a>Konfigurovat procesy řízení skladu
Než bude možné použít vydané produkty v modulu **Řízení skladu**, musí produkty používat skupinu dimenze úložiště, ve které je vybraný parametr **Používat procesy řízení skladu**.

### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Povolení skladům používat procesy řízení skladu

1.  Vytvořte alespoň jeden nový profil skladového místa
2.  Klikněte na **řízení skladu** &gt; **Nastavení** &gt; **Povolit procesy řízení skladu** &gt; **Povolit nastavení skladu**.
3.  Na stránce **Povolit nastavení skladu** přidejte sklady, které mají být povoleny. Tento krok můžete dokončit přímo na stránce nebo pomocí integrace aplikace Microsoft Office.
4.  Přiřadíte profil skladového místa všem skladovým místům. Tento krok můžete snadno dokončit pomocí integrace aplikace Microsoft Office přímo na stránce. Můžete exportovat a importovat data nebo použít zpracování datové entity v modulu [Správa dat](../../fin-ops-core/dev-itpro/data-entities/data-entities.md).
5.  Ověřte změny. V rámci procesu ověření probíhají různá ověření integrity dat. V rámci rozsáhlejšího procesu upgradu může být nutné upravit problémy, které nastanou, ve zdrojové implementaci. V tomto případě bude vyžadován další upgrade dat.
6.  Zpracujte změny.

### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Změňte skupinu dimenzí úložiště pro položky tak, aby používaly procesy řízení skladu.

1.  Vytvořte novou hodnotu **Stav zásob** a přiřaďte ji jako **výchozí ID stavu zásob** v nastavení **parametry správy skladu**.
2.  Vytvořte novou skupinu dimenzí úložiště, kde je vybrán parametr **používat procesy správy skladu**.
3.  Na stránce **Hierarchie rezervací** definujte novou hierarchii rezervací podle skupiny skladu a dimenzí sledování.
4.  Vytvořte jednu nebo více skupin klasifikace jednotek, které obsahují přinejmenším stejné jednotky, jaké se používají pro skladové položky.
5.  Klikněte na **Řízení skladu** &gt; **Nastavení** &gt; **Povolit procesy řízení skladu** &gt; **Změnit skupinu dimenzí úložiště pro položky**.
6.  Na stránce **Změnit skupinu dimenzí úložiště položek** přidejte čísla položky, skupiny dimenze úložiště a skupiny klasifikace jednotek. Tento krok můžete dokončit přímo na stránce pomocí integrace Microsoft Office nebo procesu entity dat v modulu [Správa data](../../fin-ops-core/dev-itpro/data-entities/data-entities.md).
7.  Ověřte změny. V rámci procesu ověření probíhají různá ověření integrity dat. V rámci rozsáhlejšího procesu upgradu může být nutné upravit problémy, které nastanou, ve zdrojové implementaci. V tomto případě bude vyžadován další upgrade dat.
8.  Zpracujte změny. Aktualizace všech dimenzí zásob může chvíli trvat. Průběh můžete sledovat pomocí úkolů dávkové úlohy můžete sledovat.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]