---
title: "Inventura zásob podle štítků"
description: "Tento článek obsahuje informace o inventuře podle štítků, kterou lze použít k porovnání skutečného obsahu skladu s množstvím na skladě."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 896b91647b65843bf67211cab68b4dd08e379b18
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-tag-counting"></a>Inventura zásob podle štítků

[!include[banner](../includes/banner.md)]


Tento článek obsahuje informace o inventuře podle štítků, kterou lze použít k porovnání skutečného obsahu skladu s množstvím na skladě. 

Vytvořte řádky na **inventura** stránce, umístěte číslo označení u každé položky zásob, jako je číslo od 1 do 500. Během inventury zadejte číslo položky a množství odpovídající značky. Tento štítek pak slouží jako základ pro vstup do deníku inventur podle štítků. Po zaúčtování deníku inventur štítků se na stránce **Inventura** vytvoří nový deník inventur. Nový deník vychází z řádků v deníku inventur podle štítků, které jste vytvořili. Pro inventuru položek podle určité skladové dimenze vyberte dimenzi na stránce **Zobrazení dimenzí**, která se zobrazí při vytvoření deníku inventur podle štítků. Například k provedení inventury položek v konkrétním skladu zaškrtněte políčko **Sklad**. Pokud je vybraný posuvník **Uzamknout položky během inventury** na stránce **Parametry modulu Řízení zásob a skladu**, položky nelze během inventury fyzicky aktualizovat. Položky v denících inventur však během inventury nejsou uzamknuty. Skladové transakce se nevytvoří, dokud se řádky inventur štítků nezaúčtují a nepřenesou do deníku inventur. Pokud jsou štítky vloženy náhodně a vy chcete určit chybějící štítky, klikněte na záhlaví sloupce **Štítek** a seřaďte řádky podle štítků.

<a name="see-also"></a>Viz také
--------

[Cycle counting](../warehousing/cycle-counting.md)




