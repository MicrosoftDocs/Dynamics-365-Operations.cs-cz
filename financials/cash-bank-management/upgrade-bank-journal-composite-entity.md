---
title: "Aktualizace složité entity bankovního deníku"
description: "Pomocí následujících kroků přidejte další pole BankTransactionType field do složitého záznamu BankJournalEntity."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 364bdff8f8d825cc50760631bb533b531f8b2121
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="update-the-bank-journal-composite-entity"></a>Aktualizace složité entity bankovního deníku

[!include[banner](../includes/banner.md)]


Pomocí následujících kroků přidejte další pole BankTransactionType field do složitého záznamu BankJournalEntity.

Pomocí následujících kroků přidejte další pole BankTransactionType field do složitého záznamu BankJournalEntity.

1.  Nakompilujte a synchronizujte následující složité entity, entity a tabulky fázování bankovního deníku:
    -   Složitá entita\\EntitaBankovníhoDeníku
    -   Entita\\EntitaZáhlavíBankovníhoDeníku
    -   Entita\\EntitaŘádkuBankovníhoDeníku
    -   Tabulka\\FázeZáhlavíBankovníhoDeníku
    -   Tabulka\\FázeŘádkuBankovníhoDeníku

2.  Správa dat\\datové projekty
    -   Vystavte typ **Bankovní transakce**v rozložení **Zdrojová data**.
        -   Formát zdrojových dat = XML-Element
        -   Název entity = Bankovní deník
        -   Odeslaný datový soubor = SampleBankJournalCompositeEntity.xml nové verze
        -   Kliknutím na možnost **Ano** přepíšete existující soubor.
        -   Klikněte na **Ano**, pokud chcete mapování generovat od začátku.
        -   Ověřte, že je namapován typ bankovní transakce.
            -   V entitě Řádek klepněte na **Zobrazit mapu**.
            -   Ověřte, že typ bankovní transakce je namapován ze zdroje do fázování.

3.  Importujte nový výkaz.





