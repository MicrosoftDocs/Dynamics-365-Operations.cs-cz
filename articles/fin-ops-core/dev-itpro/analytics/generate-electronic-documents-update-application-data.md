---
title: Generování elektronických dokumentů a aktualizace dat aplikace pomocí elektronického výkaznictví
description: Můžete vytvářet formáty elektronického výkaznictví (ER), které lze použít v aplikaci ke generování odchozích elektronických dokumentů.
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 1be618d16be2ce9e50c2a43864040dfd23a8ff69
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269654"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>Generování elektronických dokumentů a aktualizace dat aplikace pomocí elektronického výkaznictví

[!include [banner](../includes/banner.md)]

Můžete vytvářet formáty elektronického výkaznictví (ER), které lze použít v aplikaci ke generování odchozích elektronických dokumentů. Můžete vytvořit také formáty ER, které analyzují příchozí elektronické dokumenty, a použít jejich obsah k aktualizaci dat aplikace.

Pomocí této funkce lze použít jeden formát ER pro generování odchozích elektronických dokumentů a následné aktualizaci dat aplikace. Tuto funkci lze využít v těchto případech:

- Abyste zabránili opakovanému použití dat aplikace u dalších procesů, můžete je označit hned poté, co budou využita k vygenerování elektronických dokumentů. Můžete například označit platební transakce jako zpracované ihned po jejich začlenění do vygenerované zprávy o platbě.
- Můžete uložit podrobnosti o zpracování elektronických dokumentů vygenerovaných pomocí logiky ER. Může se jednat například o jedinečnou identifikaci zpráv o platbě vygenerovanou pomocí výrazu ER. Výraz je založen na informacích zadaných v dialogovém okně ER při spuštění formátu ER za účelem vygenerování dokumentů.

Další informace o této funkci získáte v průvodcích záznamem úloh pro generování dokumentů ER s aktualizací dat aplikace (součást obchodního procesu 7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677)), které vás provedou procesy výkaznictví a archivace Intrastat. K dokončení některých kroků v průvodcích jsou nutné následující soubory. Stáhněte si je a uložte je do místního počítače.

- [Konfigurace modelu dat ER: Intrastat (model)](https://download.microsoft.com/download/9/c/e/9ceeacbe-c13e-422e-96f2-594c4a6b45b7/Intrastatmodel.xml)
- [Konfigurace mapování modelu ER: Intrastat (mapování)](https://download.microsoft.com/download/2/1/d/21ddaaeb-64c5-4408-a35f-1ccb922d40a4/Intrastatmapping.xml)
- [Konfigurace formátu ER: Intrastat (formát)](https://download.microsoft.com/download/8/b/b/8bbb8891-e88d-4739-b92a-2d1d2fffcb79/Intrastatformat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
