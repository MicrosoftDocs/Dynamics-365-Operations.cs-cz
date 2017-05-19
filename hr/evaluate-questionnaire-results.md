---
title: "Zobrazení a zhodnocení výsledků dotazníku"
description: "Toto téma vysvětluje způsob, jakým lze zobrazit a vyhodnotit výsledky dotazníků, které respondenti dokončí."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 0285103ef30ebf8322f2bf60941b07c7496e9c70
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="view-and-evaluate-the-results-of-a-questionnaire"></a>Zobrazení a zhodnocení výsledků dotazníku

[!include[banner](includes/banner.md)]


Toto téma vysvětluje způsob, jakým lze zobrazit a vyhodnotit výsledky dotazníků, které respondenti dokončí. 

Jakmile respondenti vyplní dotazník, existuje několik způsobů, jak můžete výsledky dotazníku zobrazit a vyhodnotit:

-   **Relace vyplněných odpovědí** – Zobrazení podrobných informací o dotaznících, které respondenti vyplnili, a generování sestav pro souhrn odpovědí a získaných bodů.
-   **Skupiny výsledků** – Zobrazení podrobností skupin výsledků a statistik pro dotazníky. Statistiky skupin výsledků je možné generovat pro jednu relaci odpovědí dotazníku nebo všech relací odpovědí.
-   **Statistiky dotazníků** – Zadání kritérií pro výpočet statistik pro specifickou skupinu respondentů.

Lze rovněž generovat různé sestavy k zobrazení výsledků, které jsou seřazeny podle osoby, relace odpovědi nebo skupiny výsledků. K dispozici jsou následující sestavy, které souvisejí s vyplněnými dotazníky:

-   Odpovědi
-   Odpovědi za dotazník
-   Odpovědi za osobu
-   Analýza zpětné vazby

## <a name="answer-session-results"></a>Výsledky relace odpovědí
Jakmile respondenti dokončí dotazník, je možné zobrazit výsledky dokončených relací odpovědí. Relace odpovědí je odpověď jednoho uživatele k dotazníku. Můžete zobrazit podrobnosti o dokončených relacích odpovědí na stránce **Odpovědi**. Relace odpovědí, které jsou zahrnuty na stránce **Odpovědi**, jsou filtrovány různým způsobem, v závislosti na způsobu otevření stránky:

-   Všechny dotazníky
-   Konkrétní dotazník
-   Konkrétní osoba

Na stránce **Odpovědi** můžete zobrazit podrobnosti o odpovědích, získaných bodech, odpovědích respondenta v jednotlivých skupinách výsledků a hierarchii otázek použité na vybraném dotazníku, pokud byla hierarchie otázek použita. Je také možné vygenerovat a vytisknout následující sestavy:

-   **Sestava výsledků** – V této sestavě se zobrazí grafické znázornění bodů, které by byly získány pro skupinu výsledků pro vybranou relaci odpovědí.
-   **Sestava odpovědí** - V této sestavě se zobrazí odpovědi vybrané respondentem pro každou otázku dotazníku.
-   **Nesprávné odpovědi** – V této sestavě se zobrazí informace související s nesprávnými odpověďmi, které respondent vybral.

> **Poznámka**
>   Sestava **Výsledky** je k dispozici pouze v případě, že použijete skupiny výsledků v dotazníku a jestliže jste vybrali **stránku Výsledky** na stránce **Dotazníky**. Sestavy **Odpovědi** a **Nesprávné odpovědi** jsou k dispozici pouze v případě, že jste vybrali možnost **Sestava odpovědí** na stránce **Dotazníky**.

## <a name="questionnaire-statistics"></a>Statistiky dotazníků
Statistiky dotazníku slouží k analýze výsledků vyplněných dotazníků na základě výpočtů, které definujete. Chcete-li definovat výpočty, je nutné dokončit následující kroky:

-   Vyberte kritéria pro výpočet a zobrazení statistiky.
    -   Je možné zobrazit statistiky dle dotazníků, otázek, řádků otázek nebo skupin výsledků.
    -   Vyberte typ grafu, který bude použit při prohlížení výsledků.
    -   Vyberte typy osob v síti (zaměstnanci, kontaktní osoby nebo uchazeči), jejichž odpovědi mají být zahrnuty do statistiky. Je rovněž možné zahrnout odpovědi z dotazníků, které byly vyplněny anonymně.
    -   Nastavte intervaly, které jsou založeny na věku nebo služebním věku, pro analýzu výsledků.
-   Výběr nebo ověření nastavení, jež upřesní předmět statistiky. Například při výběru PSČ lze analyzovat výsledky pro všechny respondenty v dané geografické oblasti.
-   Vyberte nebo zkontrolujte kritéria pro analýzu výsledků dle charakteristiky respondenta nebo dotazníku. Například výběrem možnosti **PSČ** lze analyzovat korelaci mezi umístěním a správnými odpověďmi respondenta.

Definovaná nastavení budou uložena a lze je použít k periodickému přepočítávání výsledků.

<a name="see-also"></a>Viz také
--------

[Vytváření dotazníků](design-questionnaires.md)

[Používání dotazníků](questionnaires.md)

[Distribuování a vyplňování dotazníků](distribute-questionnaires.md)




