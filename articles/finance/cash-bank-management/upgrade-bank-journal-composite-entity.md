---
title: Aktualizace složité entity bankovního deníku
description: Pomocí následujících kroků přidejte další pole BankTransactionType field do složitého záznamu BankJournalEntity.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7e265915cf3f53a8243788b50a9374d521efbbae
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819595"
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
    -   Vystavte typ **Bankovní transakce** v rozložení **Zdrojová data**.
        -   Formát zdrojových dat = XML-Element
        -   Název entity = Bankovní deník
        -   Odeslaný datový soubor = SampleBankJournalCompositeEntity.xml nové verze
        -   Kliknutím na možnost **Ano** přepíšete existující soubor.
        -   Klikněte na **Ano**, pokud chcete mapování generovat od začátku.
        -   Ověřte, že je namapován typ bankovní transakce.
            -   V entitě Řádek klepněte na **Zobrazit mapu**.
            -   Ověřte, že typ bankovní transakce je namapován ze zdroje do fázování.

3.  Importujte nový výkaz.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]