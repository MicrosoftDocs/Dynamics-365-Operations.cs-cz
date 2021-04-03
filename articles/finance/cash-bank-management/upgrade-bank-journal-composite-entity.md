---
title: Aktualizace složité entity bankovního deníku
description: Pomocí následujících kroků přidejte další pole BankTransactionType field do složitého záznamu BankJournalEntity.
author: ShylaThompson
manager: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 18137ca8cecc43b4269f14b36df2eb8063192e52
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236340"
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