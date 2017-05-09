---
title: "Běžné zdroje výrobních odchylek"
description: "Tento článek vysvětluje různé obvyklé zdroje každého typu výrobní odchylky."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: de0c0df36edb1dedcae480aac3ae26ee8301a099
ms.lasthandoff: 03/31/2017


---

# <a name="common-sources-of-production-variances"></a>Běžné zdroje výrobních odchylek

[!include[banner](../includes/banner.md)]


Tento článek vysvětluje různé obvyklé zdroje každého typu výrobní odchylky. 

Zde jsou některé typické zdroje odchylek ve **velikosti šarže**:

-   Množství zboží pro výrobní zakázku se liší od množství pro výpočet používané ve standardním výpočtu nákladů. Toto množství poskytuje základ pro amortizaci konstantních nákladů.
-   Hodnota konstantních nákladů ve výrobní zakázce se liší od konstantních nákladů používaných ve standardním výpočtu nákladů. Konstantní náklady ve výrobní zakázce se mohou lišit z několika důvodů. Konstantní náklady mohou například odrážet následující faktory:
    -   ruční změny ve výrobním kusovníku, kusovníku nebo postupu;
    -   výběr jiné verze kusovníku nebo verze postupu při vytváření výrobní zakázky;
    -   plánované technické změny verze kusovníku nebo verze postupu, která je přiřazena k položce.

Zde jsou některé typické zdroje odchylek ve **výrobní ceně**:

-   Kategorie nákladů (a cena kategorie nákladů) vykazované spotřeby operace postupu se liší od kategorie nákladů používané ve standardním výpočtu nákladů.
-   Aktivní náklad ceny kategorie nákladů se liší od ceny kategorie nákladů používané ve standardním výpočtu nákladů.

Zde jsou některé typické zdroje odchylek ve **výrobním množství**:

-   nadměrný příjem materiálové komponenty nebo nedostatečný příjem materiálové komponenty;
-   nadměrný nebo nedostatečný čas sestavy pro operace postupu;
-   nadměrný nebo nedostatečný příjem množství zboží nadřazené položky, ve vztahu k množství objednávky. Avšak vydáte komponenty a plně vykážete operace na základě objednaného množství ve výrobní zakázce.

Zde jsou některé typické zdroje odchylek v **nahrazení výroby**:

-   výdej materiálové komponenty, která se nenachází ve výrobním kusovníku;
-   ruční přidání komponenty do výrobního kusovníku a vykázání této komponenty jako spotřebované;
-   vykázání položky jako spotřebované, avšak bez ručního přidání této položky do výrobního kusovníku;
-   ruční přidání operace do výrobního postupu a vykázání této operace jako spotřebované;
-   při vytváření výrobní zakázky vyberete verzi kusovníku, která se liší od verze kusovníku používané ve standardním výpočtu nákladů;
-   při vytváření výrobní zakázky vyberete verzi postupu, která se liší od verze postupu používané ve standardním výpočtu nákladů.





