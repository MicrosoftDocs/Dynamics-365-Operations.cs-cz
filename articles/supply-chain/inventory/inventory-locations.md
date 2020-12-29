---
title: Skladová místa
description: Skladová místa se používají se základní funkcí skladu (WMS I) k určení toho, kde jsou položky uskladněny, a kde se položky vybírají v rámci skladu WMS I.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSLocation, WMSBlockingCause, WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 490f510ca0a5522d7bc892733ff066ebc65bcd24
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424220"
---
# <a name="inventory-locations"></a>Skladová místa

[!include [banner](../includes/banner.md)]

Skladová místa se používají se základní funkcí skladu (WMS I) k určení toho, kde jsou položky uskladněny, a kde se položky vybírají v rámci skladu WMS I.

V tomto tématu se týká funkcí v modulu Správa zboží. Nevztahuje se na funkce v modulu Řízení skladu.

Termín skladové místo je definován jako místo, ze kterého se vybírají, a kam se ukládají položky.

Lze také určit místo vložení položky pro každé skladové místo. Implicitně jsou totožná. Položky se obvykle ukládají a vybírají ze stejné strany skladového místa, ale ne vždy. Například položky uložené v průběžných regálech se vkládají z jedné uličky a vybírají se z druhé uličky. Hlavním vstupním údajem je název skladového místa, který je obvykle určen svými souřadnicemi: sklad, ulička, stojan, police a přihrádka. Tento název nebo ID lze zadat ručně nebo vytvořit ze souřadnic skladového místa – například 01-02-03-4, kde platí, že ulička = 1, stojan = 2, police = 3, přihrádka = 4 (stránka Skladové místo).
Vlastnosti skladového místa

Skladové místo má následující charakteristiky:
-   Velikost (výška, šířka a hloubka a tím také objem)
-   Sklad, Ulička, Stojan, Police a Přihrádka
-   Typ skladového místa (velkosklad, výdejní skladové místo, vstupní přepraviště, výstupní přepraviště, vstupní místo výroby, inspekční umístění nebo kanbanový zásobník materiálu)

V online systémech lze pomocí kontrolního textu ověřit, že operátor pro určitou položku vybral správné skladové místo. Tento kontrolní text lze vytvořit ručně nebo lze použít výchozí.

## <a name="sort-codes"></a>Kódy třídění
Kódy třídění se používají k optimalizaci zpracování řádků výdeje, ve kterých jsou uvedeny informace nutné pro výdej položek ze skladu včetně objednávky výdeje. Kódy třídění lze určovat podle uličky a dalších souřadnic nebo je lze přiřazovat skladovému místu ručně.

## <a name="blocked-locations"></a>Blokovaná skladová místa
Příležitostně je nutné skladové místo na určitou dobu zablokovat, například kvůli opravám. Jindy bude třeba spustit blokování jen pro vstup nebo výstup.

## <a name="tree-structure"></a>Stromová struktura

Na stránce Skladová místa můžete zobrazit rozvržení skladu ve stromové struktuře podle souřadnic umístění zásob, a to v definovaném formátu zobrazení.

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a>Spravovat skladová místa pomocí formuláře Sklad

Je možné kopírovat umístění z jednoho skladu do jiného a vytvořit umístění pomocí průvodce. Před spuštěním průvodce se ujistěte, že jste definovali výchozí názvy skladového místa na stránce Sklad.



<a name="additional-resources"></a>Další zdroje
--------

[Vytvoření nového rozvržení skladu](tasks/create-new-warehouse-layout.md)
