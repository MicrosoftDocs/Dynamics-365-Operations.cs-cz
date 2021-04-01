---
title: Generování a spuštění předpřipravených sestav
description: Použijte tohoto průvodce úkolem ke spuštění předem připravených sestav v centrále z jiných pracovních prostorů a dotazy a prodejní sestavy, které jsou umístěny pod Velkoobchodní prodej.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d3dd941eb4e682e61c8b3d10ef0ccd14239f090c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232706"
---
# <a name="generate-and-run-out-of-box-reports"></a>Generování a spuštění předpřipravených sestav

[!include [banner](../includes/banner.md)]

Použijte tohoto průvodce úkolem ke spuštění předem připravených sestav v centrále z jiných pracovních prostorů a dotazy a prodejní sestavy, které jsou umístěny pod Velkoobchodní prodej.

K vytvoření tohoto záznamu jsou použita ukázková data společnosti USRT. Tento záznam je určen pro roli Správce systému.

## <a name="launch-reports-from-workspaces"></a>Spuštění sestav z pracovních ploch
1. Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Produkty a kategorie > Správa kategorií a produktů.
2. Kliknutím na šipku rozbalte nebo sbalte oddíl Sestavy.
3. Klikněte na Sestava nejlepších produktů.
4. Zadejte datum do pole Od data.
5. Do pole Do data zadejte datum.
6. V poli Kanál kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. Ve stromovém zobrazení vyberte „Contoso Retail\Contoso Retail USA\Central\Houston“.
    * Tím se zobrazí výchozí hierarchie organizace maloobchodu pro účely vykazování velkoobchodu.   Přejděte do nabídky Správa organizace > Organizace > Účely organizační hierarchie, vyberte Vykazování velkoobchodu a ověřte v poli Přiřazené hierarchie název hierarchie, u které je zaškrtnut Výchozí sloupec. Jako součást ukázkových dat (použitých k záznamu tohoto úkolu) si můžete všimnout, že možnost Obchody podle regionu je výchozí organizační hierarchie pro účely obchodního vykazování.     
8. Klepněte na tlačítko OK.
9. Vyberte volbu v poli Zobrazení.
10. Vyberte volbu v poli Podle.
11. Klepněte na tlačítko OK.

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a>Spouštění sestav z dotazů a prodejních sestav
1. Přejděte na Maloobchodní a velkoobchodní prodej > Dotazy a sestavy > Prodejní sestavy > Prodejní sestava kategorií.
2. Zadejte datum do pole Od data.
3. Do pole Do data zadejte datum.
4. V poli Kanál kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Ve stromovém zobrazení vyberte „Contoso Retail\Contoso Retail USA\West\Seattle“.
    * Tím se zobrazí výchozí hierarchie organizace maloobchodu pro účely vykazování velkoobchodu. Přejděte do nabídky Správa organizace > Organizace > Účely organizační hierarchie, vyberte Vykazování velkoobchodu a ověřte v poli Přiřazené hierarchie název hierarchie, u které je zaškrtnut Výchozí sloupec. Jako součást ukázkových dat (použitých k záznamu tohoto úkolu) si můžete všimnout, že možnost Obchody podle regionu je výchozí organizační hierarchie pro účely obchodního vykazování.     
6. Klepněte na tlačítko OK.
7. Klepněte na tlačítko OK.

## <a name="export-an-hq-reports"></a>Exportujte sestavy HQ
1. Přejděte na Maloobchodní a velkoobchodní prodej > Dotazy a sestavy > Prodejní sestavy > Sestava prodejů organizace.
2. Zadejte datum do pole Od data.
3. Do pole Do data zadejte datum.
4. Klikněte na tlačítko OK.
5. Klikněte na Exportovat.
6. Klikněte na PDF.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]