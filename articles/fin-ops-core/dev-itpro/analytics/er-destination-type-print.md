---
title: Typ cílového místa elektronického výkaznictví tiskárny
description: Toto téma vysvětluje, jak nakonfigurovat cíl tiskárny pro každou SLOŽKU nebo SOUBOR ve formátu elektronického výkaznictví (ER).
author: NickSelin
manager: AnnBe
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 19613d9dfba21d591d96a2df45bedb80c043b3a7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561943"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Cílové místo tiskárny

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

Cíl **tiskárny** je implementován pouze pro nasazení v cloudu.

### <a name="use-the-printer-destination"></a>Použití cíle tiskárny

1. Chcete-li odeslat vygenerovaný dokument do tiskárny, nastavte možnost **povoleno** na **Ano**.
2. V poli **Název tiskárny** vyberte požadovanou síťovou tiskárnu.
3. Chcete nastavit ukládání v tiskovém archivu, nastavte možnost **Uložit do tiskového archivu?** na **Ano**, aby byl k dispozici pro další tisk. Chcete-li získat přístup k archivovanému výstupu později, přejděte na **Správa organizace** \> **Dotazy a sestavy** \> **Archive sestav**.

[![Použití cíle tiskárny](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Pokud konfigurujete cíl **tiskárny**, možnost **převést do PDF** není nutné mít zapnutou. Převod souboru PDF pro účely tisku bude proveden i v případě, že je tato možnost vypnuta.

Chcete-li při tisku odchozího dokumentu ve formátu aplikace Excel použít určitou [orientaci stránky](electronic-reporting-destinations.md#SelectPdfPageOrientation), je nutné zapnout možnost **převést na PDF**. Nastavíte-li volbu **převést na PDF** na hodnotu **Ano**, zpřístupní se pole **Orientace stránky**. V poli **Orientace stránky** můžete vybrat orientaci stránky.

## <a name="additional-resources"></a>Další prostředky

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Místa určení elektronického výkaznictví](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
