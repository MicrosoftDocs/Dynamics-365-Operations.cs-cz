---
title: Typ cílového místa elektronického výkaznictví archivu
description: Toto téma poskytuje informace o tom, jak nakonfigurovat cíl archivu pro každou SLOŽKU nebo SOUBOR ve formátu elektronického výkaznictví (ER).
author: NickSelin
manager: AnnBe
ms.date: 11/30/2020
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
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 72b896ca692a54200ff79b14d0b5dc6ab4b0fe27
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562039"
---
# <a name="archive-er-destination-type"></a>Typ cílového místa elektronického výkaznictví archivu

[!include [banner](../includes/banner.md)]

Můžete konfigurovat cíl archivu pro každou komponentu **Složka** nebo **Soubor** formátu elektronického výkaznictví, který je nakonfigurován pro generování odchozích dokumentů. Vygenerovaný dokument je na základě nastavení cíle uložen jako příloha záznamu seznamu úloh elektronického výkaznictví. Výsledky můžete zobrazit přechodem do nabídky **Správa organizace** \> **Elektronické výkaznictví** \> **Úlohy elektronického výkaznictví**.

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

> [!NOTE] 
> Architektura ER trvale ukládá soubory v úložišti objektů Azure Blob na rozdíl od architektury správy dat, která aplikuje sedmidenní zásadu uchovávání dokumentů, které musí být zpracovány. Další informace najdete v tématech [Rozhraní API pro získání stavu zprávy](../data-entities/recurring-integrations.md#api-for-getting-message-status) a [Rozhraní API pro kontrolu stavu](../data-entities/data-management-api.md#status-check-api). Soubory související s ER budou uloženy v úložišti Azure Blob jako přílohy záznamů tabulky aplikace, pokud to bude nutné. Jeden soubor bude odstraněn z úložiště Azure Blob spolu se záznamem tabulky aplikace, ke kterému byl tento soubor připojen.

## <a name="additional-resources"></a>Další prostředky

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Místa určení elektronického výkaznictví](electronic-reporting-destinations.md)
- [Konfigurace správy dokumentů](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]