---
title: "Sestavy deníku zásob"
description: "Při použití konfigurovatelných sestav zásob založených na elektronickém výkaznictví je třeba vytvořit vztah mezi konkrétní sestavou a typem deníku."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalName
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations, Core
ms.custom: 265144
ms.search.region: Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b3418ca37b01917ca9f2c19e06653363ab99fa65
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="inventory-journal-reports"></a>Sestavy deníku zásob

[!include[banner](../includes/banner.md)]


Při použití konfigurovatelných sestav zásob založených na elektronickém výkaznictví je třeba vytvořit vztah mezi konkrétní sestavou a typem deníku.

Chcete-li nastavit vztah mezi konkrétní sestavou a typem deníku, na stránce **Názvy deníků zásob** (**Řízení zásob** &gt; **Nastavení** &gt; **Názvy deníků** &gt; **Zásoby**) zadejte název sestavy. **Poznámka:** Pro nastavení podporovaných konfigurací si stáhněte požadované konfigurace elektronického vykazování. Další informace viz [Stažení konfigurace elektronického vykazování ze služby Lifecycle Services](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs). V následující tabulce jsou uvedeny příklady sestavy zásob s podporovanou konfigurací v Evropě.
|                    |                                     |                  |                                         |
|--------------------|-------------------------------------|------------------|-----------------------------------------|
| **Země**        | **Popis sestavy**              | **Typ deníku** | **Název mapování formátu**                 |
| Litva, Maďarsko | Sestava stavu zásob          | Inventura         | Výkaz inventury majetku (HU, LT)            |
| Lotyšsko, Polsko     | Dokument reklasifikace zásob | Převod         | InventoryReclassificationDocument\_PLLV |
| Estonsko            | Dokument reklasifikace zásob | Převod         | InventoryReclassificationDocument\_EE   |
| Polsko             | Interní PW/RW                      | Pohyb         | InventJournalLinesDocPL                 |
| Lotyšsko             |  Doklad o Přesunu zásob         | Pohyb         | Movement\_LV                            |
| Lotyšsko             | Dokument hodnoty zásob       | Úprava       | InventJournalLines\_LV                  |
| Lotyšsko             | Poznámka k převodu              | Převod         | InternalTransferDeliveryNote\_LV        |
| Lotyšsko             | Sestava dokumentu inventury            | Inventura         | CountedDocument\_LV                     |
| Lotyšsko             | Sestava inventurního seznamu                | Inventura         | Inventurní seznam                           |






