---
title: "Vytvořit výrobní zakázky"
description: "Při vytvoření výrobní zakázky je iniciován požadavek pro zahájení výroby položky. Výrobní zakázka obsahuje informace o tom, jaký produkt bude vyroben, kolik kusů produktu bude vyrobeno a plánované datum dokončení. Také zahrnuje informace o materiálech, které se spotřebují a který proces se má při výrobě položky použít."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 33d2e4f1a6bc8bc28e43b4c985d9a780a9481e97
ms.lasthandoff: 03/31/2017


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





