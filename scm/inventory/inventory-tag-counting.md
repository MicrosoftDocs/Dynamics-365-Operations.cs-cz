---
title: "Inventura zásob podle štítků"
description: "Tento článek obsahuje informace o inventuře podle štítků, kterou lze použít k porovnání skutečného obsahu skladu s množstvím na skladě."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 61a48a61963f643c8969e9090c2e84b5499b716a
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="inventory-tag-counting"></a>Inventura zásob podle štítků

[!include[banner](../includes/banner.md)]


Tento článek obsahuje informace o inventuře podle štítků, kterou lze použít k porovnání skutečného obsahu skladu s množstvím na skladě. 

Vytvořením řádků na stránce **Inventura podle štítků** přidáte číslo štítku ke každé skladové položce, například číslo od 1 do 500. Během inventury zadejte číslo položky a množství na příslušném štítku. Tento štítek pak slouží jako základ pro vstup do deníku inventur podle štítků. Po zaúčtování deníku inventur štítků se na stránce **Inventura** vytvoří nový deník inventur. Nový deník vychází z řádků v deníku inventur podle štítků, které jste vytvořili. Pro inventuru položek podle určité skladové dimenze vyberte dimenzi na stránce **Zobrazení dimenzí**, která se zobrazí při vytvoření deníku inventur podle štítků. Například k provedení inventury položek v konkrétním skladu zaškrtněte políčko **Sklad**. Pokud je vybraný posuvník **Uzamknout položky během inventury** na stránce **Parametry modulu Řízení zásob a skladu**, položky nelze během inventury fyzicky aktualizovat. Položky v denících inventur však během inventury nejsou uzamknuty. Skladové transakce se nevytvoří, dokud se řádky inventur štítků nezaúčtují a nepřenesou do deníku inventur. Pokud jsou štítky vloženy náhodně a vy chcete určit chybějící štítky, klikněte na záhlaví sloupce **Štítek** a seřaďte řádky podle štítků.

<a name="see-also"></a>Viz také
--------

[Cyklická inventura](../warehousing/cycle-counting.md)




