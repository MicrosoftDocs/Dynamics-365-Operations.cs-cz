---
title: "Aktualizace složité entity bankovního deníku"
description: "Pomocí následujících kroků přidejte další pole BankTransactionType field do složitého záznamu BankJournalEntity."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a8b11df3b21f8d97986d934ff3c65931aa7ee0c6
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="update-the-bank-journal-composite-entity"></a>Aktualizace složité entity bankovního deníku

[!include [banner](../includes/banner.md)]

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





