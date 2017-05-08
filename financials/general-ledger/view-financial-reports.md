---
title: "Zobrazit finanční sestavy"
description: "Tento článek popisuje, jak zobrazit a prozkoumat finanční sestavy v aplikaci Microsoft Dynamics AX. Obsahuje informace o různých možnostech, které můžete použít pro finanční sestavy, když chcete změnit jejich vzhled a data, která obsahují."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10334
ms.assetid: d20f435f-fb65-4068-ab09-7efc7be683a6
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 5535a7897eb328e97a9c8a4ca7986ed5cf9381af
ms.lasthandoff: 03/31/2017


---

# <a name="view-financial-reports"></a>Zobrazit finanční sestavy

[!include[banner](../includes/banner.md)]


Tento článek popisuje, jak zobrazit a prozkoumat finanční sestavy v aplikaci Microsoft Dynamics AX. Obsahuje informace o různých možnostech, které můžete použít pro finanční sestavy, když chcete změnit jejich vzhled a data, která obsahují.

<a name="financial-reporting-overview"></a>Přehled finančního výkaznictví
----------------------------

## <a name="open-a-financial-report"></a>Otevření finanční sestavy
Chcete-li otevřít sestavu, vyberte název sestavy. Při prvním otevření se sestava automaticky generuje pro předchozí měsíc. Například pokud otevřete sestavu poprvé v srpnu 2015, je sestava generována pro 31. července 2015. Po otevření sestavy můžete začít s prohlížením rozbalením specifických částí dat a změnou možností sestavy.

## <a name="drill-down-on-a-financial-report"></a>Procházení finanční sestavy
Finanční sestavy mohou zahrnout více úrovní podrobností. První úroveň, která se při otevření finanční sestavy zobrazí, je finanční. Chcete-li přejít na úroveň účtu, vyberte data, na která se má přejít. Chcete-li například zobrazit podrobnosti o účtu pro prodej, vyberte data prodeje, která chcete prozkoumat. Na úrovni účtu lze přejít k zobrazení transakcí, které tvoří zůstatek účtu. Transakce lze zobrazit dvěma způsoby: transakce sestavy a transakce dokladu.

-   **Transakce sestavy** – transakce se zobrazují v naformátovaném zobrazení, které je zahrnuto do finanční sestavy. K zobrazení transakcí v naformátovaném zobrazení vyberte data, která chcete procházet, a klikněte na tlačítko **Zobrazit podrobnosti na úrovni transakce sestavy**.
-   **Transakce dokladu** – dotaz na transakci dokladu se otevře tam, kde se zobrazují transakce. K zobrazení transakcí v dotazu na transakce dokladu vyberte data, která chcete procházet, a klikněte na tlačítko **Otevřít transakce účtu**.

Jedná-li se o data rozpočtu, můžete otevřít účetní položky rozpočtu. Chcete-li zavřít úroveň zprávy a vrátit se na začátek, stiskněte klávesu Esc nebo klikněte na tlačítko **Zavřít** (**X**) vpravo nahoře.

## <a name="change-report-options"></a>Změna možností sestavy
Ve zprávě **Skutečnost versus rozpočet** můžete změnit datum sestavy, použít filtry atributů a dimenzí nebo změnit scénář rozpočtu. V podokně akcí klikněte na tlačítko **Možnosti sestavy**a poté proveďte jeden nebo více z následujících kroků:

-   Chcete-li změnit základní období a základní rok sestavy, vyberte základní období a základní rok a klikněte na tlačítko **OK**.
-   Chcete-li v sestavě použít filtry atributů, vyberte možnost **Přidat filtr atributu**. Vyberte atribut, zadejte hodnotu atributu a klikněte na tlačítko **OK**. Vyberete-li například atribut **Kategorie účtů**, zadejte hodnotu atributu **PRODEJE**. Chcete-li filtr atributu odebrat, klikněte na tlačítko **Vymazat**.
-   Chcete-li v sestavě použít filtry dimenzí, vyberte možnost **Přidat filtr dimenze**. Vyberte dimenzi a poté zadejte ID dimenze nebo vyberte dimenzi ze seznamu. Chcete-li filtr dimenze odebrat, klikněte na tlačítko **Vymazat**.
-   Chcete-li změnit scénář na sestavu **Skutečnost versus rozpočet**, vyberte nový scénář a klikněte na tlačítko **OK**. Je-li vybraný scénář pro jiný rok, je nutné aktualizovat základní rok. Například pokud je aktuální scénář pro fiskální rok 2015 a vy vyberete nový scénář pro fiskální rok 2016, musíte měnit základní rok na **2016**.

Po kliknutí na tlačítko **OK** se vybrané možnosti použijí pro sestavu. Pokud se rozhodnete, že nechcete použít vybrané možnosti, klikněte na tlačítko **Storno**.

## <a name="update-a-financial-report"></a>Aktualizace finanční sestavy
Finanční sestavu můžete obnovit (aktualizovat), aby zobrazovala aktuální data pro období a rok, pro které byla generována. Například při aktualizaci finanční sestavy, která byla vytvořena pro říjen 2015, sestava odráží všechny nové transakce, které byly zaúčtovány k říjnu 2015. Chcete-li aktualizovat finanční sestavu, v podokně akcí klikněte na tlačítko **Aktualizovat**. Aktualizovaná sestava je k dispozici pouze osobě, která ji aktualizovala. Aby se stejná data zobrazila i ostatním, je třeba sestavu publikovat.

## <a name="publish-a-financial-report"></a>Publikování finanční sestavy
Po dokončení aktualizace finanční sestavy ji můžete publikovat. Ostatní uživatelé v rámci organizace ji pak budou moci zobrazit. Chcete-li sestavu publikovat, v podokně akcí klikněte na tlačítko **Publikovat**.

## <a name="display-a-financial-report-in-a-different-currency"></a>Zobrazení finanční sestavy v různých měnách
Finanční sestavu lze kdykoli zobrazit v jiné měně. Chcete-li sestavu zobrazit v jiné měně, v podokně akcí klikněte na tlačítko **Měna**a vyberte požadovanou měnu. Sestava se převede do zvolené měny a zobrazí se výsledky. Kódy měn nebo symboly, které jsou součástí návrhu sestavy, se aktualizují, aby se nová měna zohlednila. Měny zobrazené v seznamu jsou měny vykazování, které se konfigurují v aplikaci Microsoft Dynamics AX.

## <a name="display-a-summarized-view-of-the-financial-report"></a>Souhrnné zobrazení finanční sestavy
Finanční sestava může obsahovat řádky podrobností a řádky souhrnů. Řádky podrobností jsou řádky, které obsahují hlavní účty nebo dimenze. Řádky souhrnů jsou řádky popisu, součtu a výpočtu. Chcete-li v sestavě zobrazit pouze řádky souhrnu, klikněte na možnost **Zobrazit** a poté na tlačítko **Pouze řádky souhrnu**. Sestava se sbalí a zobrazí se pouze řádky souhrnu. Chcete-li zobrazit řádky podrobností spolu s řádky souhrnu, klikněte na tlačítko **Zobrazit** na poté znovu na tlačítko **Pouze řádky souhrnu**.

## <a name="open-a-financial-report-from-a-previous-month"></a>Otevření finanční sestavy z předchozího měsíce
Sestavy pro aktuální nebo předchozí měsíc můžete zobrazit, aniž byste museli sestavu generovat znovu. K otevření sestavy pro předchozí měsíc klikněte na možnost **Zobrazit**a potom na tlačítko **Předchozí sestavy**. Zobrazí se seznam předchozích měsíců vygenerované sestavy. Rozbalte měsíc k zobrazení sestavy, vyberte datum a klikněte na tlačítko **OK**. Zobrazí se sestava pro předchozí měsíc. Chcete-li se vrátit k sestavě aktuálního měsíce, klikněte na tlačítko **Storno**.

## <a name="print-a-financial-report"></a>Tisk finanční sestavy
Chcete-li vytisknout finanční sestavu, v podokně akcí klikněte na tlačítko **Tisk** a poté proveďte jeden nebo více z následujících kroků, abyste nastavili volby tisku:

-   Chcete-li do vytištěné sestavy zahrnout různé úrovně podrobností, přepněte posuvník do hodnoty **Ano** nebo **Ne**. Pokud sestava používá strom výkaznictví, je možné zahrnout všechny jednotky výkaznictví nebo pouze aktuální jednotku výkaznictví.
-   Velikost stránky lze nastavit výběrem velikost stránky v seznamu.
-   Chcete-li nastavit rozvržení stránky, vyberte rozvržení v seznamu. Pokud se má obsah sestavy přizpůsobit vybrané šířce, přepněte posuvník do hodnoty **Ano**.
-   Chcete-li nastavit okraje stránky, zadejte velikost horního, dolního, levého a pravého okraje v palcích.

Po dokončení nastavení možností tisku sestavu vytisknete kliknutím na tlačítko **Tisk**. Pokud se rozhodnete, že sestavu nechcete tisknout, klikněte na tlačítko **Storno**. Zobrazí se náhled vytištěné sestavy. Můžete vybrat, do které tiskárny se sestava odešle, a rovněž upravit možnosti tisku.

## <a name="export-a-financial-report"></a>Exportování finanční sestavy
Chcete-li finanční sestavu exportovat, v podokně akcí klikněte na tlačítko **Exportovat**. Sestava se exportuje do aplikace Microsoft Excel a prohlížeč zobrazí výzvu k otevření nebo uložení exportovaného souboru. V exportované sestavě se použijí nastavení exportu definovaná v návrhu sestavy.    

<a name="see-also"></a>Viz také
--------

[Finanční výkaznictví pro aplikaci Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/analytics/financial-reporting-intro)



