---
title: Rozšířené odsouhlasení bankovního výpisu MT940 Import – Aktualizace kombinované datové entity
description: Pořadové číslo musí být přidáno k importu bankovního výpisu entity pro podporu MT940 formátu.
author: panolte
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d6534cc0835eabe91ab485e1d71412885d12123f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827427"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Rozšířené odsouhlasení bankovního výpisu MT940 Import – Aktualizace kombinované datové entity

[!include [banner](../includes/banner.md)]

Pořadové číslo musí být přidáno k importu bankovního výpisu entity pro podporu MT940 formátu. 

Následující postup slouží k přidání importu bankovního výpisu entity pro podporu formátu MT940.

1.  Kompilovat a synchronizovat následující:
    -   Kombinovaná entita\\BankStatementImportEntity
    -   Entita\\BankStatementBalanceEntity
    -   Entita\\BankStatementDocumentEntity
    -   Entita\\BankStatementEntity
    -   Entita\\BankStatementLineEntity
    -   Tabulky\\BankStatementStaging

2.  Správa dat\\datové projekty.
    1.  Načíst projekt(y) importu MT940.
        1.  Změna požadavku XSLT.
            -   Klikněte na možnost **Zobrazit mapu**.
            -   Klepněte na tlačítko **Zobrazit mapu** na dokumentu bankovního výpisu.
            -   Klikněte na tlačítko **Transformace**
            -   Odstraňte soubor BankReconiliation-Composite.xslt.
            -   Přidejte novou verzi BankReconiliation-Composite.xsl.

        2.  Vystavte **Pořadové číslo** do rozvržení **Zdrojová data**.
            1.  Formát zdrojových dat = XML-Element.
            2.  Název entity = Výpisy banky.
            3.  Odeslaný datový soubor = Nová verze SampleBankJournalCompositeEntity.xml.
            4.  Kliknutím na možnost **Ano** přepíšete existující soubor.
            5.  Klikněte na **Ano**, pokud chcete generovat nové mapování.
            6.  Ověřte, že je S **equenceNumber** mapováno.
                -   Klepněte na tlačítko **Zobrazit mapu** na dokumentu výpisu entity.
                -   Ověřte, že **SequenceNumber** je namapováno ze zdroje do fázování.

3.  Importujte nový výkaz.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]