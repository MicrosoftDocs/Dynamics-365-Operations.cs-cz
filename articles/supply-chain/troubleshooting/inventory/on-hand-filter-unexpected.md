---
title: Podokno filtru na stránce Seznamu na skladě nefunguje podle očekávání
description: Filtry v podokně filtru na stránce seznam na skladě nefiltrují výsledky podle mého očekávání.
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
ms.openlocfilehash: df11b1c1e7de36fa0458cd931d4be7f84a15d143
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475825"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Podokno filtru na stránce Seznamu na skladě nefunguje podle očekávání

## <a name="symptoms"></a>Příznaky

Filtry v podokně filtru na stránce **seznam na skladě**  nefiltrují výsledky podle mého očekávání.

## <a name="resolution"></a>Řešení

Stránka  **Seznam na skladě**  je sestavena z podrobné tabulky zásob na skladě, která obsahuje všechny dostupné rozměry. Seznam na této stránce je však shrnutím. Proto by mohl kombinovat řádky ze zdrojové tabulky agregováním hodnot podle zobrazených rozměrů.

Filtry, které jsou nastaveny v podokně filtrů se vztahují na zdrojovou tabulku, nikoli na agregovaný seznam. Toto chování může někdy způsobit neočekávané výsledky, jak je uvedeno v [těchto příkladech](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples).

Nicméně  [filtry poskytované v mřížce](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters) *platí*  pro agregovaný seznam. Tyto filtry zahrnují QuickFilter v horní části mřížky a filtr pro každou hlavičku sloupce.
