---
title: Aktualizace standardních nákladů ve výrobním prostředí
description: V tomto článku jsou pokyny k tomu, jak aktualizovat standardní náklady ve výrobním prostředí.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8acbcb79fa45ea2f225775068e0d061a44cba1f7
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675228"
---
# <a name="update-standard-costs-in-a-manufacturing-environment"></a>Aktualizace standardních nákladů ve výrobním prostředí

[!include [banner](../includes/banner.md)]

V tomto článku jsou pokyny k tomu, jak aktualizovat standardní náklady ve výrobním prostředí. 

Aktualizace mohou odrážet nové položky, kategorie nákladů nebo vzorce nepřímého výpočtu nákladů. Můžete také odrážet opravy a změny nákladů. Typ aktualizace má vliv na kroky, které je nutno provést k aktualizaci standardních nákladů, jak je uvedeno v následujících příkladech:

-   Určete očekávané standardní změny nákladů pro zakoupené položky a poté pro příslušné datum změňte stav záznamů o nákladech na položku na hodnotu **Aktivní**. Neprovádějte však přepočítání nákladů na vyrobené položky, které používají zakoupené položky.
-   Určete standardní náklady na nově zakoupenou položku, avšak neprovádějte přepočítání nákladů vyrobených položek s verzemi kusovníku, které jako komponentu obsahuje nově zakoupenou položku.
-   Opravte nebo změňte náklady na zakoupenou položku nebo změňte nákladovou skupinu přiřazenou k zakoupené položce a vypočtěte náklady pro všechny vyrobené položky s verzí kusovníku, která jako součást obsahuje zakoupenou položku.
-   Změňte náklady pro kategorii nákladů a vypočtěte náklady pro všechny vypočtené položky s verzí postupu, která obsahuje operace postupu používající danou kategorii nákladů.
-   Změňte kategorie nákladů, které jsou přiřazeny k operacím postupů, nebo nákladovou skupinu, která je přiřazena k nákladovým kategoriím. Potom vypočtěte náklady pro všechny vyrobené položky s verzí postupu, která obsahuje operace postupu používající danou kategorii nákladů.
-   Změňte vzorec nepřímého výpočtu nákladů a vypočtěte náklady pro všechny vyráběné položky, na které bude mít uvedená změna vliv.
-   Pro vyráběnou položku změňte nebo přidejte výrobní pracoviště a vypočtěte výrobní náklady položky pro dané pracoviště.
-   Vypočítejte nebo přepočítejte náklady na vyráběnou položku a přepočítejte náklady pro všechny vyráběné položky s verzí kusovníku, která obsahuje vyráběnou položku jako součást.
-   Vypočtěte náklady pro nově vyráběnou položku na základě údajů definovaného, schváleného a aktivního kusovníku a postupu.

Každý případ vyžaduje pečlivé zvážení způsobu aktualizace standardních nákladů.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]