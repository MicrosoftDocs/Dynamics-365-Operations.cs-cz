---
title: Podokno filtru na stránce Seznamu na skladě nefunguje podle očekávání
description: Filtry v podokně filtru na stránce „Seznam zásob na skladě“ nefiltrují výsledky podle mého očekávání.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 3857ce3720430c6f512d5abc4c9c4d390a0c3377
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686676"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Podokno filtru na stránce Seznamu na skladě nefunguje podle očekávání

## <a name="symptoms"></a>Příznaky

Filtry v podokně filtru na stránce **Seznam zásob na skladě** nefiltrují výsledky podle mého očekávání.

## <a name="resolution"></a>Řešení

Stránka **Seznam na skladě** je sestavena z podrobné tabulky zásob na skladě, která obsahuje všechny dostupné rozměry. Seznam na této stránce je však shrnutím. Proto by mohl kombinovat řádky ze zdrojové tabulky agregováním hodnot podle zobrazených rozměrů.

Filtry, které jsou nastaveny v podokně filtrů se vztahují na zdrojovou tabulku, nikoli na agregovaný seznam. Toto chování může někdy způsobit neočekávané výsledky, jak je uvedeno v [těchto příkladech](/dynamics365/supply-chain/inventory/inventory-on-hand-list#examples).

Nicméně, [filtry poskytované v mřížce](/dynamics365/supply-chain/inventory/inventory-on-hand-list#grid-filters) *platí* pro agregovaný seznam. Tyto filtry zahrnují QuickFilter v horní části mřížky a filtr pro každou hlavičku sloupce.
