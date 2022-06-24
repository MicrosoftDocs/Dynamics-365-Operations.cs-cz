---
title: Typ cílového místa elektronického výkaznictví tiskárny
description: Tento článek vysvětluje, jak nakonfigurovat cíl tiskárny pro každou SLOŽKU nebo SOUBOR ve formátu elektronického výkaznictví (ER).
author: NickSelin
ms.date: 02/14/2022
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
ms.openlocfilehash: 826455d0901a45ef26755fd323ee2a2737b5eec0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845563"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Cílové místo tiskárny

[!include [banner](../includes/banner.md)]

Vygenerovaný dokument můžete odeslat přímo do síťové tiskárny pro přímý tisk.

## <a name="prerequisites"></a>Předpoklady

Dříve než začnete, je nutné nainstalovat a nakonfigurovat směrovacího agenta dokumentů a poté zaregistrovat síťové tiskárny. Více informací naleznete v části [Instalace agenta směrování dokumentu pro aktivaci síťového tisku](./install-document-routing-agent.md).

## <a name="make-the-printer-destination-available"></a>Zpřístupnění cíle tiskárny

Chcete-li zpřístupnit cíl **tiskárny** v aktuální instanci Microsoft Dynamics 365 Finance, přejděte do do pracovního prostoru **Správa funkcí** a zapněte následující funkce v tomto pořadí:

1. Převod odchozích dokumentů elektronického výkaznictví z formátů Microsoft Office do formátu PDF
2. Agent pro směrování dokumentů jako cílové umístění elektronického výkaznictví pro odchozí dokumenty

[![Zapnutí cíle tiskárny elektronického výkaznictví ve správě funkcí.](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Použitelnost

#### <a name="pdf-printing"></a>Tisk PDF

Ve verzích Finance před 10.0.18 lze cíl **Tiskárna** konfigurovat pouze pro součásti souboru, které jsou použity ke generování výstupu ve formátu tisknutelného PDF (**PDF Merger** nebo prvky formátu **souboru PDF**) nebo formátu Microsoft Office Excel a Word (prvek formátu **Soubor Excel**). Když je výstup generován ve formátu PDF, je odeslán do tiskárny. Když je výstup generován ve formátu Office pomocí prvku formátu **Soubor Excel**, je automaticky převeden do formátu PDF a poté odeslán do tiskárny.

Od verze 10.0.18 však můžete nakonfigurovat cíl **Tiskárna** pro prvek formátu **Soubor Common**. Tento prvek formátu se většinou používá pro generování výstupu buď ve formátu TXT, nebo XML. Můžete nakonfigurovat formát ER, který obsahuje prvek formátu **Soubor Common** jako kořenový prvek formátu a formátu **Binární obsah** jako jediný vnořený element pod ním. V tomto případě prvek formátu **Soubor Common** vytvoří výstup ve formátu, který je určen vazbou, kterou konfigurujete pro prvek formátu **Binární obsah**. Tuto vazbu můžete například nakonfigurovat k [vyplnění](tasks/er-document-management-files-5.md#modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format) tohoto prvku obsahem přílohy [Správa dokumentů](../../fin-ops/organization-administration/configure-document-management.md) přílohu ve formátu PDF nebo Office (Excel nebo Word). Výstup můžete vytisknout pomocí nakonfigurovaného cíle **Tiskárna**. 

> [!NOTE]
> Když vyberete prvek formátu **Common\\File** pro konfiguraci cíle **Tiskárna**, neexistuje způsob, jak v době návrhu zaručit, že vybraný prvek vytvoří výstup ve formátu PDF, nebo výstup, který lze převést do formátu PDF. Proto se zobrazí následující varovná zpráva: „Ujistěte se prosím, že výstup generovaný vybranou komponentou formátu lze převést do PDF. V opačném případě zrušte zaškrtnutí možnosti „Převést do PDF“.“ Musíte podniknout kroky, které pomohou předejít problémům za běhu, když je k tisku za běhu poskytnut výstup bez PDF nebo nekonvertibilní do PDF. Pokud očekáváte, že budete přijímat výstup ve formátu Office (Excel nebo Word), možnost **Převést do PDF** musí být vybrána.
>
> Ve verzi 10.0.26 a k použití možnosti **Převést do PDF** musíte vybrat **PDF** jako parametr **Typ směrování dokumentu** konfigurovaného cíle **Tiskárna**.

#### <a name="zpl-printing"></a>Tisk ZPL

Ve verzi 10.0.26 a novější můžete nakonfigurovat cíl **Tiskárna** pro prvek formátu **Common\\File** výběrem **ZPL** jako parametru **Typ směrování dokumentu**. V tomto případě je možnost **Převést do PDF** za běhu ignorována a výstup TXT nebo XML je odeslán přímo na vybranou tiskárnu pomocí smlouvy Zebra Programming Language (ZPL) [Agent pro směrování dokumentů (DRA)](install-document-routing-agent.md). Tuto funkci použijte pro formát ER, který představuje rozložení štítků ZPL II pro tisk různých štítků.

[![Nastavení parametru Typ směrování dokumentu v dialogovém okně Nastavení cíle.](./media/ER_Destinations-SetDocumentRoutingType.png)](./media/ER_Destinations-SetDocumentRoutingType.png)

Další informace o této funkci viz [Návrh nového ER řešení pro tisk štítků ZPL](er-design-zpl-labels.md).

### <a name="limitations"></a>Omezení

Cíl **tiskárny** je implementován pouze pro nasazení v cloudu.

### <a name="use-the-printer-destination"></a>Použití cíle tiskárny

1. Chcete-li odeslat vygenerovaný dokument do tiskárny, nastavte možnost **povoleno** na **Ano**.
2. V poli **Název tiskárny** vyberte požadovanou síťovou tiskárnu.
3. Chcete nastavit ukládání v tiskovém archivu, nastavte možnost **Uložit do tiskového archivu?** na **Ano**, aby byl k dispozici pro další tisk. Chcete-li získat přístup k archivovanému výstupu později, přejděte na **Správa organizace** \> **Dotazy a sestavy** \> **Archive sestav**.

[![Použití cíle tiskárny.](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Pokud konfigurujete cíl **tiskárny**, možnost **převést do PDF** není nutné mít zapnutou. Převod souboru PDF pro účely tisku bude proveden i v případě, že je tato možnost vypnuta.

Chcete-li při tisku odchozího dokumentu ve formátu aplikace Excel použít určitou [orientaci stránky](electronic-reporting-destinations.md#SelectPdfPageOrientation), je nutné zapnout možnost **převést na PDF**. Nastavíte-li volbu **převést na PDF** na hodnotu **Ano**, zpřístupní se pole **Orientace stránky**. V poli **Orientace stránky** můžete vybrat orientaci stránky.

## <a name="additional-resources"></a>Další prostředky

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Místa určení elektronického výkaznictví](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
