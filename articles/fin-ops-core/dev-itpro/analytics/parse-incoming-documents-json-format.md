---
title: Analýza příchozích dokumentů ve formátu JSON
description: V tomto tématu je vysvětleno, jak nastavit formáty elektronického výkaznictví pro analýzu příchozích dokumentů ve formátu JSON.
author: kfend
manager: AnnBe
ms.date: 05/20/2019
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
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 92ef83bc1783b00a4d7d9739ca1c17e863c7ff44
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185260"
---
# <a name="parse-incoming-documents-in-json-format"></a>Analýza příchozích dokumentů ve formátu JSON

[!include[banner](../includes/banner.md)]

Formáty elektronického výkaznictví lze navrhovat k analýze příchozích elektronických dokumentů, které reprezentují data v textovém formátu založeném na jazyku JavaScript (jinými slovy, soubory ve formátu \[JSON\]).

Chcete-li získat další informace o této funkci, stáhněte soubory v následující tabulce a poté přehrajte průvodce záznamem úloh Vytvoření konfigurace formátu pro import dat z externího souboru JSON. Tento průvodce záznamem úloh ukazuje, jak lze použít formát elektronického výkaznictví k analýze příchozího souboru JSON pro aktualizaci dat aplikace.

| Titul                                  | Název souboru |
|----------------------------------------|-----------|
| Konfigurace formátu elektronického výkaznictví                | [Formát pro import souboru trans_JSON. XML dodavatelů](https://go.microsoft.com/fwlink/?linkid=874111) |
| Ukázka příchozího souboru ve formátu CSV | [1099entries_JSON.txt](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a>Požadavky

Před dokončením průvodce záznamem úloh Vytvoření konfigurace formátu pro import dat z externího souboru JSON je nutné splnit následující požadavky:

- Nadřazené prvky v souboru JSON mohou být pouze objektové prvky.
- Vnořené prvky pro objekt by měly být prvky vlastností, aby byla vytvořena platná struktura JSON.
- Pole JSON mohou být pouze vnořenými prvky prvků vlastnosti objektu.
- Pole JSON mohou obsahovat pouze objekty JSON. Nemohou obsahovat přímé řetězcové nebo číselné hodnoty a vnořená pole. Prvky v těchto polích budou analyzovány v pořadí, jak jsou uvedeny ve formátu. V každém objektu JSON bude zváženo nastavení násobnosti.

Dále je nutné dokončit průvodce záznamem úloh[Vytvoření požadovaných konfigurací importu dat z externího souboru pro elektronické vykazování](tasks/er-required-configurations-import-data.md) v případě, že jste ho ještě nedokončili. Pro dokončení průvodce záznamem úloh stáhněte následující soubor.

| Titul                  | Název souboru |
|------------------------|-----------|
| Konfigurace modelu ER | [1099model.xml](https://go.microsoft.com/fwlink/?linkid=874111) |
