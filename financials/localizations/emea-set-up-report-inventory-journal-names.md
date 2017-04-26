---
title: "Sestavy deníků zásob"
description: "Při použití zásob konfigurovatelné sestavy založené na elektronických sestav, je třeba vytvořit vztah mezi konkrétní sestavu a typ deníku."
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

# <a name="inventory-journal-reports"></a>Sestavy deníků zásob

[!include[banner](../includes/banner.md)]


Při použití zásob konfigurovatelné sestavy založené na elektronických sestav, je třeba vytvořit vztah mezi konkrétní sestavu a typ deníku.

Chcete-li nastavit vztah mezi konkrétní sestavu a typu deníku na **názvy deníků zásob** stránky (**řízení zásob**&gt;**nastavení**&gt;**názvy deníku**&gt;**zásob**), zadejte název sestavy. **Poznámka:** podporovaných konfigurací nastavení, stáhnout požadované konfigurace elektronické hlášení. Další informace naleznete v tématu [stáhnout elektronické vykazování konfigurace služby životního cyklu](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs). V následující tabulce jsou uvedeny příklady sestavy zásob s podporovanou konfigurací v Evropě.
|                    |                                     |                  |                                         |
|--------------------|-------------------------------------|------------------|-----------------------------------------|
| **Country**        | **Popis sestavy**              | **Journal type** | **Mapování názvu formátu**                 |
| Lotyšsko, Maďarsko | Výkaz zásob          | Inventura         | Výkaz zásob (HU, LT)            |
| Lotyšsko, Polsko     | Dokument reklasifikace zásob | Převod         | InventoryReclassificationDocument\_PLLV |
| Estonsko            | Dokument reklasifikace zásob | Převod         | InventoryReclassificationDocument\_é   |
| Polsko             | Vnitřní PW/RW                      | Pohyb         | InventJournalLinesDocPL                 |
| Lotyšsko             |  Doklad o Přesunu zásob         | Pohyb         | Pohyb\_LV                            |
| Lotyšsko             | Doklad o znehodnocení zásob       | Úprava       | InventJournalLines\_LV                  |
| Lotyšsko             | Poznámka k převodu              | Převod         | InternalTransferDeliveryNote\_LV        |
| Lotyšsko             | Načítání dokumentu sestavy            | Inventura         | CountedDocument\_LV                     |
| Lotyšsko             | Inventurní seznam sestavy                | Inventura         | Inventurní seznam                           |






