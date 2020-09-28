---
title: Typ cílového místa elektronického výkaznictví archivu
description: Toto téma obsahuje informace o tom, jak konfigurovat cíl archivu pro každou komponentu SLOŽKA nebo SOUBOR formátu elektronického výkaznictví, který je nakonfigurován pro generování odchozích dokumentů.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
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
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8797a68507a5116c6adbf1f2d805838fa507958c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745578"
---
# <a name="archive-destination"></a>Cíl archivace

[!include [banner](../includes/banner.md)]

Můžete konfigurovat cíl archivu pro každou komponentu SLOŽKA nebo SOUBOR formátu elektronického výkaznictví, který je nakonfigurován pro generování odchozích dokumentů. Vygenerovaný dokument je na základě nastavení cíle uložen jako příloha záznamu seznamu úloh elektronického výkaznictví.

Tuto možnost můžete použít k odeslání vygenerovaného dokumentu do složky Microsoft SharePoint nebo úložiště Microsoft Azure. Nastavením **Povoleno** na **Ano** dojde k odeslání výstupu do cíle, který je definován pro vybraný typ dokumentu. K dispozici pro výběr jsou pouze typy dokumentu, kde je skupina nastavena na **Soubor**. [Typy](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) dokumentů definujete pomocí **Správa organizace** \> **Správa dokumentů** \> **Typy dokumentů**. Konfigurace pro cíle EV je stejná, jako nastavení pro systém správy dokumentů.

[![Stránka typu dokumentu](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

Umístění určuje, kde bude soubor uložen. Po povolení cíle **Archiv** lze výsledky uložit do archivu úloh. Výsledky můžete zobrazit pod **Správa organizace** \> **Elektronické výkaznictví** \> **Archivované úlohy elektronického výkaznictví**.

> [!NOTE]
> Vyberte typ dokumentu pro archiv úloh přechodem na **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví** \> **Parametry elektronického výkaznictví**. Další informace získáte v tématu [Konfigurace rámce elektronického výkaznictví](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).

## <a name="sharepoint"></a>SharePoint

Soubor můžete uložit do určené složky SharePoint. Výchozí server SharePoint definujete v nabídce **Správa organizace** \> **Správa dokumentu** \> **Parametry správy dokumentů**. Na kartě **SharePoint** nakonfigurujte složku SharePoint. Poté ji můžete vybrat jako složku, do které bude uložen výstup elektronického výkaznictví. V tomto typu dokumentu musí být vybráno místo **SharePoint**.

[![Výběr složky služby SharePoint](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Úložiště Azure

Pokud je umístění typu dokumentu nastaveno na **Azure storage**, můžete soubor uložit do úložiště Azure.

## <a name="additional-resources"></a>Další zdroje

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Místa určení elektronického výkaznictví](electronic-reporting-destinations.md)
- [Konfigurace správy dokumentů](../../fin-ops/organization-administration/configure-document-management.md)
