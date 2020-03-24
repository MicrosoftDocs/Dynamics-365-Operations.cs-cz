---
title: Typ cílového místa elektronického výkaznictví tiskárny
description: Toto téma vysvětluje, jak můžete konfigurovat cíl tiskárny pro každou komponentu SLOŽKA nebo SOUBOR formátu elektronického výkaznictví, který je nakonfigurován pro generování odchozích dokumentů buď v PDF nebo formátech Microsoft Office (Excel nebo Word).
author: NickSelin
manager: AnnBe
ms.date: 01/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58e067baa130458e3a8e788d978604f208140a03
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019667"
---
# <a name="PrinterDestinationType"></a>Cílové místo tiskárny

[!include [banner](../includes/banner.md)]

Vygenerovaný dokument můžete odeslat přímo do síťové tiskárny pro přímý tisk.

## <a name="prerequisites"></a>Předpoklady

Dříve než začnete, je nutné nainstalovat a nakonfigurovat směrovacího agenta dokumentů a poté zaregistrovat síťové tiskárny. Více informací naleznete v části [Instalace agenta směrování dokumentu pro aktivaci síťového tisku](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).

## <a name="make-the-printer-destination-available"></a>Zpřístupnění cíle tiskárny

Chcete-li zpřístupnit cíl **tiskárny** v aktuální instanci Microsoft Dynamics 365 Finance, přejděte do do pracovního prostoru **Správa funkcí** a zapněte následující funkce v tomto pořadí:

1. Převod odchozích dokumentů elektronického výkaznictví z formátů Microsoft Office do formátu PDF
2. Agent pro směrování dokumentů jako cílové umístění elektronického výkaznictví pro odchozí dokumenty

[![Zapnutí cíle tiskárny elektronického výkaznictví ve správě funkcí](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Použitelnost

Cíl **tiskárny** lze konfigurovat pouze pro součásti souboru, které jsou použity ke generování výstupu ve formátu tisknutelného PDF (PDF Merger nebo prvky formátu souboru PDF) nebo formátu Microsoft Office Excel/Word. Když je výstup generován ve formátu PDF, je odeslán do tiskárny. Když je výstup generován ve formátu Microsoft Office, je automaticky převeden do formátu PDF a poté odeslán do tiskárny.

### <a name="limitations"></a>Omezení

Tato funkce je funkcí Preview a podléhá podmínkám použití, které jsou popsány v [doplňujících podmínkách použití pro funkce Preview Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2105274).

Cíl **tiskárny** je implementován pouze pro nasazení v cloudu.

### <a name="use-the-printer-destination"></a>Použití cíle tiskárny

1. Chcete-li odeslat vygenerovaný dokument do tiskárny, nastavte možnost **povoleno** na **Ano**.
2. V poli **Název tiskárny** vyberte požadovanou síťovou tiskárnu.
3. Chcete nastavit ukládání v tiskovém archivu, nastavte možnost **Uložit do tiskového archivu?** na **Ano**, aby byl k dispozici pro další tisk. Chcete-li získat přístup k archivovanému výstupu později, přejděte na **Správa organizace** \> **Dotazy a sestavy** \> **Archive sestav**.

[![Použití cíle tiskárny](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Pokud konfigurujete cíl **tiskárny**, možnost **převést do PDF** není nutné mít zapnutou. Převod souboru PDF pro účely tisku bude proveden i v případě, že je tato možnost vypnuta.

## <a name="additional-resources"></a>Další zdroje

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Místa určení elektronického výkaznictví](electronic-reporting-destinations.md)