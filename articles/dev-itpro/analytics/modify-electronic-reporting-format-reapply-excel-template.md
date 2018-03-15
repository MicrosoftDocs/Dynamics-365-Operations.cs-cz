---
title: "Úprava formátu elektronického výkaznictví opětovným použitím šablony aplikace Microsoft Excel"
description: "Toto téma poskytuje informace o tom, jak můžete upravit formát elektronického výkaznictví (ER), který se používá ke generování obchodních dokumentů opětovným použitím šablony aplikace Excel."
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: af7f9a373496eee4df354d5dd9e5a25c51317c43
ms.openlocfilehash: fca7fb75b965886c2ebc06b12940434f2ffc2543
ms.contentlocale: cs-cz
ms.lasthandoff: 02/27/2018

---
# <a name="modify-an-electronic-reporting-format-by-reapplying-a-microsoft-excel-template"></a>Úprava formátu elektronického výkaznictví opětovným použitím šablony aplikace Microsoft Excel

[!include[banner](../includes/banner.md)]

Nástroj elektronického výkaznictví (ER) slouží ke generování obchodních dokumentů v elektronické podobě. Ke generování obchodních dokumentů musíte vytvořit formátu elektronického výkaznictví a pak použít návrháře elektronického výkaznictví k definování rozvržení obchodního dokument a určení dat, která v něm mají být obsažena. Poté lze spustit ER formát pro generování obchodního dokumentu.

Nástroj elektronického výkaznictví slouží ke generování obchodních dokumentů jako souborů aplikace Microsoft Excel. Dokument Excel lze použít jako šablonu pro tyto dokumenty. Chcete-li definovat rozvržení dokumentu v návrháři elektronického výkaznictví, můžete importovat obsah dokumentu aplikace Excel, který chcete použít, jako šablonu do definovaného formátu elektronického výkaznictví. Abyste se podrobně seznámili s tímto postupem a procvičili si tento scénář, přehrajte si průvodce záznamem úlohy **Elektronické vykazování – Návrh konfigurace pro generování sestav ve formátu OPENXML** (součást obchodního procesu 7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)).

Pokud upravíte dokument aplikace Excel, který je použit jako šablona pro obchodní dokument, nová funkce elektronického výkaznictví vám umožní znovu použít aktualizovanou šablonu do formátu elektronického výkaznictví. Formát ER se pak aktualizuje tak, aby odpovídal aktualizované šabloně. Abyste se podrobně seznámili s tímto postupem, přehrajte si průvodce záznamem úlohy **Elektronické vykazování – Úprava formátu opětovným použitím šablony aplikace Excel** (součást obchodního procesu 7.5.5.3 Získání/vývoj součástí IT služeb/řešení (10683)). V rámci kroku průvodce záznamem úlohy, kde importujete aktualizovanou šablonu, použijte jako šablonu upravenou šablonu souboru aplikace Excel sestavy platby s názvem SampleVendPaymWsReport2.

