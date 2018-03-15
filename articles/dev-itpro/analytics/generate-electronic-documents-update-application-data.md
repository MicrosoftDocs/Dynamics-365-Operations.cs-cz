---
title: "Generování elektronických dokumentů a aktualizace dat aplikace pomocí nástroje elektronického výkaznictví"
description: "Můžete vytvářet formáty elektronického výkaznictví (ER), které lze použít v aplikaci Finance and Operations ke generování odchozích elektronických dokumentů. Můžete vytvořit také formáty ER, které analyzují příchozí elektronické dokumenty, a použít jejich obsah k aktualizaci dat aplikace."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: af7f9a373496eee4df354d5dd9e5a25c51317c43
ms.openlocfilehash: e2447274016f517db3ec0eb8f55c6b3163822f50
ms.contentlocale: cs-cz
ms.lasthandoff: 02/27/2018

---

# <a name="generate-electronic-documents-and-update-application-data-using-the-electronic-reporting-tool"></a>Generování elektronických dokumentů a aktualizace dat aplikace pomocí nástroje elektronického výkaznictví

[!include[banner](../includes/banner.md)]

Můžete vytvářet formáty elektronického výkaznictví (ER), které lze použít v aplikaci Finance and Operations ke generování odchozích elektronických dokumentů. Můžete vytvořit také formáty ER, které analyzují příchozí elektronické dokumenty, a použít jejich obsah k aktualizaci dat aplikace. 

Pomocí této funkce lze použít jeden formát ER pro generování odchozích elektronických dokumentů a následné aktualizaci dat aplikace. Tuto funkci lze využít v těchto případech:

- Abyste zabránili opakovanému použití dat aplikace u dalších procesů, můžete je označit hned poté, co budou využita k vygenerování elektronických dokumentů. Můžete například označit platební transakce jako zpracované ihned po jejich začlenění do vygenerované zprávy o platbě.
- Můžete uložit podrobnosti o zpracování elektronických dokumentů vygenerovaných pomocí logiky ER. Může se jednat například o jedinečnou identifikaci zpráv o platbě vygenerovanou pomocí výrazu ER. Výraz je založen na informacích zadaných v dialogovém okně ER při spuštění formátu ER za účelem vygenerování dokumentů.

Další informace o této funkci získáte v průvodcích záznamem úloh pro generování dokumentů ER s aktualizací dat aplikace (součást obchodního procesu 7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)), které vás provedou procesy výkaznictví a archivace Intrastat. K dokončení některých kroků v průvodcích jsou nutné následující soubory. Stáhněte si je a uložte je do místního počítače.

- [Konfigurace modelu dat ER: Intrastat (model)](https://go.microsoft.com/fwlink/?linkid=849038)
- [Konfigurace mapování modelu ER: Intrastat (mapování)](https://go.microsoft.com/fwlink/?linkid=849038)
- [Konfigurace formátu ER: Intrastat (formát)](https://go.microsoft.com/fwlink/?linkid=849038)

