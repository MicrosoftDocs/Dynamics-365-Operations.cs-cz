---
title: Úprava formátů elektronického výkaznictví opětovným použitím šablon aplikace Excel
description: Toto téma popisuje, jak můžete upravit formát elektronického výkaznictví (ER), který se používá ke generování obchodních dokumentů opětovným použitím šablony aplikace Excel.
author: NickSelin
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 626450b05789c93f63675a55e050649c862c86f6
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811383"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>Úprava formátů elektronického výkaznictví opětovným použitím šablon aplikace Excel

[!include [banner](../includes/banner.md)]

Nástroj elektronického výkaznictví (ER) slouží ke generování obchodních dokumentů v elektronické podobě. Ke generování obchodních dokumentů musíte vytvořit formátu elektronického výkaznictví a pak použít návrháře elektronického výkaznictví k definování rozvržení obchodního dokument a určení dat, která v něm mají být obsažena. Poté lze spustit ER formát pro generování obchodního dokumentu.

Nástroj elektronického výkaznictví slouží ke generování obchodních dokumentů jako souborů aplikace Microsoft Excel. Dokument Excel lze použít jako šablonu pro tyto dokumenty. Chcete-li definovat rozvržení dokumentu v návrháři elektronického výkaznictví, můžete importovat obsah dokumentu aplikace Excel, který chcete použít, jako šablonu do definovaného formátu elektronického výkaznictví. Abyste se podrobně seznámili s tímto postupem a procvičili si tento scénář, přehrajte si průvodce záznamem úlohy **Elektronické vykazování – Návrh konfigurace pro generování sestav ve formátu OPENXML** (součást obchodního procesu 7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)). V rámci kroku průvodce záznamem úlohy, kde importujete šablonu aplikace Excel, použijte úvodní šablonu v souboru aplikace Excel sestavy platby s názvem [SampleVendPaymWsReport](https://download.microsoft.com/download/e/6/b/e6bb79f0-cc08-44af-96fa-49c7929d4fb8/SampleVendPaymWsReport.xlsx).

Pokud upravíte dokument aplikace Excel, který je použit jako šablona pro obchodní dokument, nová funkce elektronického výkaznictví vám umožní znovu použít aktualizovanou šablonu do formátu elektronického výkaznictví. Formát ER se pak aktualizuje tak, aby odpovídal aktualizované šabloně. Abyste se podrobně seznámili s tímto postupem, přehrajte si průvodce záznamem úlohy **Elektronické vykazování – Úprava formátu opětovným použitím šablony aplikace Excel** (součást obchodního procesu 7.5.5.3 Získání/vývoj součástí IT služeb/řešení (10683)). V rámci kroku průvodce záznamem úlohy, kde importujete aktualizovanou šablonu, použijte jako šablonu upravenou šablonu souboru aplikace Excel sestavy platby s názvem [SampleVendPaymWsReport2](https://download.microsoft.com/download/3/1/0/3104d397-c9c5-4227-b68e-f98625313801/SampleVendPaymWsReport2.xlsx).

## <a name="additional-resources"></a>Další prostředky

[Aktualizace šablony](er-fillable-excel.md#update-a-template)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
