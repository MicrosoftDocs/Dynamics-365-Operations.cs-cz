---
title: "Vytvořit výrobní zakázky"
description: "Při vytvoření výrobní zakázky je iniciován požadavek pro zahájení výroby položky. Výrobní zakázka obsahuje informace o tom, jaký produkt bude vyroben, kolik kusů produktu bude vyrobeno a plánované datum dokončení. Také zahrnuje informace o materiálech, které se spotřebují a který proces se má při výrobě položky použít."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: bcbb07553d990c35057ba32fd56d26fbc9c6f71b
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="create-production-orders"></a>Vytvořit výrobní zakázky

[!include[banner](../includes/banner.md)]


Při vytvoření výrobní zakázky je iniciován požadavek pro zahájení výroby položky. Výrobní zakázka obsahuje informace o tom, jaký produkt bude vyroben, kolik kusů produktu bude vyrobeno a plánované datum dokončení. Také zahrnuje informace o materiálech, které se spotřebují a který proces se má při výrobě položky použít.

Výrobní zakázka prochází výrobního cyklu několik fázemi. Zakázce je po vytvoření přiřazen stav **Vytvořeno**. Jakmile je objednávka dokončena, je jí přiřazen stav **Ukončeno**. Díky možnosti nastavení parametrů v každé fázi může uživatel nakonfigurovat jednotlivé kroky. Nastavení může být nastaveno pro jednoho uživatele nebo pro všechny uživatele.

Hlavními entitami výrobní zakázky jsou výrobní kusovník a výrobní postup. Tyto položky jsou zkopírovány do výrobní zakázky na základě vybrané položky a množství, které chcete vyrobit. Před zahájením výrobní zakázky je možné výrobní kusovník a postup upravit.

Výrobní zakázku lze vytvořit v následujících situacích:

-   Vytvoření při provedení hlavního plánování založeného na potřebném materiálu.
-   Vytvoření přímo z řádku prodejní objednávky nebo při vytvoření a odhadnutí výrobní zakázky vyšší úrovně (doložená dodávka).
-   Ruční vytvoření.





