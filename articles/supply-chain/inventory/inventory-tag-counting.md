---
title: "Inventura zásob podle štítků"
description: "Tento článek obsahuje informace o inventuře podle štítků, kterou lze použít k porovnání skutečného obsahu skladu s množstvím na skladě."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1b1281c41e3427148cdbd7bd874f3408056e3df1
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="inventory-tag-counting"></a>Inventura zásob podle štítků

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Tento článek obsahuje informace o inventuře podle štítků, kterou lze použít k porovnání skutečného obsahu skladu s množstvím na skladě.

Vytvořením řádků na stránce **Inventura podle štítků** přidáte číslo štítku ke každé skladové položce, například číslo od 1 do 500. Během inventury zadejte číslo položky a množství na příslušném štítku. Tento štítek pak slouží jako základ pro vstup do deníku inventur podle štítků. Po zaúčtování deníku inventur štítků se na stránce **Inventura** vytvoří nový deník inventur. Nový deník vychází z řádků v deníku inventur podle štítků, které jste vytvořili. Pro inventuru položek podle určité skladové dimenze vyberte dimenzi na stránce **Zobrazení dimenzí**, která se zobrazí při vytvoření deníku inventur podle štítků. Například k provedení inventury položek v konkrétním skladu zaškrtněte políčko **Sklad**. Pokud je vybraný posuvník **Uzamknout položky během inventury** na stránce **Parametry modulu Řízení zásob a skladu**, položky nelze během inventury fyzicky aktualizovat. Položky v denících inventur však během inventury nejsou uzamknuty. Skladové transakce se nevytvoří, dokud se řádky inventur štítků nezaúčtují a nepřenesou do deníku inventur. Pokud jsou štítky vloženy náhodně a vy chcete určit chybějící štítky, klikněte na záhlaví sloupce **Štítek** a seřaďte řádky podle štítků.

<a name="additional-resources"></a>Další zdroje
--------

[Cyklická inventura](../warehousing/cycle-counting.md)

