---
title: "Sestavy deníku zásob"
description: "Při použití konfigurovatelných sestav zásob založených na elektronickém výkaznictví je třeba vytvořit vztah mezi konkrétní sestavou a typem deníku."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventJournalName
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265144
ms.assetid: 0f07f62f-1053-46e9-b235-a7b38cbda409
ms.search.region: Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: eed3398651612743958722814ec5594ec34e4e5e
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-journal-reports"></a>Sestavy deníku zásob

[!include[banner](../includes/banner.md)]


Při použití konfigurovatelných sestav zásob založených na elektronickém výkaznictví je třeba vytvořit vztah mezi konkrétní sestavou a typem deníku.

Chcete-li nastavit vztah mezi konkrétní sestavou a typem deníku, na stránce **Názvy deníků zásob** (**Řízení zásob** &gt; **Nastavení** &gt; **Názvy deníků** &gt; **Zásoby**) zadejte název sestavy. **Poznámka:** Pro nastavení podporovaných konfigurací si stáhněte požadované konfigurace elektronického vykazování. Další informace viz [1Stažení konfigurace elektronického vykazování ze služby Lifecycle Services](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs). V následující tabulce jsou uvedeny příklady sestavy zásob s podporovanou konfigurací v Evropě.
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






