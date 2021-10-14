---
title: Nastavení informací o přepravě
description: Toto téma popisuje, jak nastavit informace o přepravě pro modul nákladů za doručení.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 86350acfd056be2b43fc856e3b76b1632989a804
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579681"
---
# <a name="shipping-information-setup"></a>Nastavení informací o přepravě

[!include [banner](../../includes/banner.md)]

Toto téma popisuje, jak nastavit informace o přepravě pro modul **nákladů za doručení**.

## <a name="description-of-goods"></a><a name="description-of-goods"></a>Popis zboží

Popisy zboží pomáhají identifikovat cestu, přepravní kontejner nebo folio zboží a zboží v něm. Popis zboží můžete vybrat v záhlaví přepravního kontejneru nebo záhlaví folia.

Chcete-li pracovat s popisy zboží, přejděte na **Náklady za doručení \> Nastavení informací o přepravě \> Popis zboží**. Zde můžete prohlížet, otevírat, vytvářet a mazat záznamy popisů zboží. V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.

| Pole | popis |
|---|---|
| Popis zboží | Zadejte jedinečný identifikační název / číslo pro typ zboží, které bude používat tento popis. |
| popis | Zadejte popis typu zboží v této kategorii. |

## <a name="vessels"></a><a name="vessels"></a>Plavidla

Plavidlo je jedinečný název lodi nebo plavidla, který používá přepravní společnost nebo agentura. Když vytváříte plavbu, musíte pro ni vždy vybrat nebo zadat plavidlo. Pokud často používáte stejná plavidla, můžete vytvořit novou cestu rychleji a snadněji vytvořením záznamu plavidla pro každou z nich, což uživatelům umožní vybrat si plavidlo ze seznamu místo toho, abyste museli pokaždé ručně zadávat název nebo číslo.

Chcete-li pracovat s loďmi, přejděte na uzel **Náklady za doručení \> Nastavení informací o doručení \> Lodě**. Zde můžete prohlížet, otevírat, vytvářet a mazat záznamy lodí. V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.

| Pole | popis |
|---|---|
| Plavidlo | Zadejte jedinečný identifikační název / číslo lodi, která bude použita k přepravě zboží na cestě. |
| popis | Zadejte popis lodě. Tento popis obvykle identifikuje název lodi a přepravní společnost / agenta. |
| Způsob dodání | Vyberte způsob doručení, který loď používá (např _Vzduch_, _Oceán_ nebo _Vlak_). |

## <a name="exporters"></a>Vývozci

Každý záznam vývozce identifikuje dodavatele nebo vývozce, kterého lze definovat jako prodejce pro cestu. Vývozce může být spojen s cestou a použit pro hlášení.

Chcete-li pracovat s vývozci, přejděte na uzel **Náklady za doručení \> Nastavení informací o doručení \> Vývozci**. Zde můžete prohlížet, otevírat, vytvářet a mazat záznamy vývozců. V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.

| Pole | popis |
|---|---|
| Vývozce | Zadejte jedinečný identifikační název / číslo vývozce zboží, které se přepravuje lodí. |
| popis | Zadejte popis vývozce. Tento popis obvykle identifikuje celý název přepravní společnosti / agenta. |

## <a name="commodity-codes"></a>Kódy komodit

Pomocí komoditních kódů pomáháte s celní identifikací a výpočtem celních sazeb za zboží na cestě. Kódy komodit můžete vybrat na stránce **Vydané produkty**.

Chcete-li pracovat s kódy zboží, přejděte na uzel **Náklady za doručení \> Nastavení informací o přepravě \> Kódy zboží**. Zde můžete prohlížet, otevírat, vytvářet a mazat záznamy kódů zboží. V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.

| Pole | popis |
|---|---|
| Kód zboží | Zadejte jedinečný kód pro tento typ komodity. |
| popis | Zadejte popis typu komodity. |

## <a name="customs-description"></a>Popis cla

Celní popisy pomáhají identifikovat zboží pro celní účely. Celní popis můžete vybrat na stránce **Vydané produkty** nebo na řádcích nákupní objednávky.

Chcete-li pracovat s celními popisy, přejděte na **Náklady za doručení \> Nastavení informací o přepravě \> Celní popis**. Zde můžete prohlížet, otevírat, vytvářet a mazat záznamy celních popisů. V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.

| Pole | popis |
|---|---|
| Popis cla | Zadejte jedinečný kód pro tento typ klasifikace cla. Tento kód bude často oficiálním popisem poskytovaným celním úřadem pro popis a kvalitativní hodnotu zboží. |
| popis | Zadejte popis klasifikace cla. |
