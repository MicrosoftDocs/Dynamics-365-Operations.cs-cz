---
title: Analýza příchozích dokumentů ve formátu Excel
description: Toto téma obsahuje informace o vytváření formátů elektronického výkaznictví pro analýzu obsahu v příchozích souborech aplikace Microsoft Excel.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 490a9325be25908564a40478a1ee29feea67fc02
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "367471"
---
# <a name="parse-incoming-documents-in-excel-format"></a>Analýza příchozích dokumentů ve formátu Excel

[!include[banner](../includes/banner.md)]

Můžete navrhovat formáty elektronického výkaznictví pro analýzu příchozích souborů aplikace Microsoft Excel, které představují data v sešitech aplikace Microsoft Excel (soubory ve formátu XLSX). Poté můžete obsah z těchto souborů použít k aktualizaci dat aplikace. Je to užitečné, když:

- Navrhujete nový model a formát a chcete ho otestovat v běhu. V tomto případě bude Excel simulovat data skutečné aplikace.
- Spravujete data za vaší aplikací v aplikaci Excel a chcete tato data importovat pro odeslání konkrétní sestavy.

Pro další informace o této funkci si přehrajte průvodce úloh **ER import dat ze souboru aplikace Microsoft Excel (část 1: Návrh formátu)** a **ER import dat ze souboru aplikace Microsoft Excel (část 2: Import dat)** (části 7.5.4.3 komponent Pořízení/Vývoj IT služby/řešení (10677) obchodního procesu). Tyto průvodci záznamem úloh vám ukáží, jak lze analyzovat příchozí Excel soubor pomocí ER formátu pro import informací z příchozích dokumentů a aktualizaci dat aplikace. Průvodce záznamem úloh můžete stáhnout z [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).

Pro dokončení průvodce záznamem úloh stáhněte následující soubory.

| Popis obsahu                         | Soubor                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| Příchozí soubor ve formátu XLSX - šablona    | [1099import-template.xlsx](https://go.microsoft.com/fwlink/?linkid=862266) |
| Příchozí soubor ve formátu XLSX - vzorová data | [1099import-data.xlsx](https://go.microsoft.com/fwlink/?linkid=862266)     |

Pokud jste si ještě nepřehráli následující průvodce záznamem úloh [ER vytvoření požadované konfigurace pro import dat z externího souboru](./tasks/er-required-configurations-import-data.md) v aktuální aplikaci Dynamics 365 for Finance and Operations, stáhněte si následující soubor.

| Popis obsahu    | Soubor                                                            |
|------------------------|-----------------------------------------------------------------|
| Konfigurace modelu ER | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |
