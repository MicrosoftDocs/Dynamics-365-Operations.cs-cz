---
title: Analýza příchozích dokumentů ve formátu Excel
description: Toto téma obsahuje informace o vytváření formátů elektronického výkaznictví pro analýzu obsahu v příchozích souborech aplikace Microsoft Excel.
author: NickSelin
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: d4ebad1b800abe77871bfa3e550a95f1fe2bfcc4692301cf79fb8b98a0b3f233
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772906"
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

Pokud jste si ještě nepřehráli následujícího průvodce záznamem úloh [ER – Vytvoření požadovaných konfigurací pro import dat z externího souboru](./tasks/er-required-configurations-import-data.md) v aktuální aplikaci Finance and Operations, stáhněte si následující soubor.

| Popis obsahu    | Soubor                                                            |
|------------------------|-----------------------------------------------------------------|
| Konfigurace modelu ER | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=862266) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]