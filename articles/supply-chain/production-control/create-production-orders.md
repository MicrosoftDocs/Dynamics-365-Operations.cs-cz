---
title: Přehled životního cyklu výrobní zakázky
description: Při vytvoření výrobní zakázky je iniciován požadavek pro zahájení výroby položky. Výrobní zakázka obsahuje informace o tom, jaký produkt bude vyroben, kolik kusů produktu bude vyrobeno a plánované datum dokončení. Také zahrnuje informace o materiálech, které se spotřebují a který proces se má při výrobě položky použít.
author: johanhoffmann
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80031737ab0d0c4ab1e4dbd5646ad91f1a010cd5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423958"
---
# <a name="production-order-lifecycle-overview"></a>Přehled životního cyklu výrobní zakázky

[!include [banner](../includes/banner.md)]

Při vytvoření výrobní zakázky je iniciován požadavek pro zahájení výroby položky. Výrobní zakázka obsahuje informace o tom, jaký produkt bude vyroben, kolik kusů produktu bude vyrobeno a plánované datum dokončení. Také zahrnuje informace o materiálech, které se spotřebují a který proces se má při výrobě položky použít.

Výrobní zakázka prochází výrobního cyklu několik fázemi. Zakázce je po vytvoření přiřazen stav **Vytvořeno**. Jakmile je objednávka dokončena, je jí přiřazen stav **Ukončeno**. Díky možnosti nastavení parametrů v každé fázi může uživatel nakonfigurovat jednotlivé kroky. Nastavení může být nastaveno pro jednoho uživatele nebo pro všechny uživatele.

Hlavními entitami výrobní zakázky jsou výrobní kusovník a výrobní postup. Tyto položky jsou zkopírovány do výrobní zakázky na základě vybrané položky a množství, které chcete vyrobit. Před zahájením výrobní zakázky je možné výrobní kusovník a postup upravit.

Výrobní zakázku lze vytvořit v následujících situacích:

-   Vytvoření při provedení hlavního plánování založeného na potřebném materiálu.
-   Vytvoření přímo z řádku prodejní objednávky nebo při vytvoření a odhadnutí výrobní zakázky vyšší úrovně (doložená dodávka).
-   Ruční vytvoření.




