---
title: Aktualizace složité entity bankovního deníku
description: Tento článek uvádí kroky potřebné k přidání dalšího pole BankTransactionType field do složitého záznamu BankJournalEntity.
author: angelad116
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f8bf3bbcbd8036015757799a2e58b23fd9bd2b38
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151603"
---
# <a name="update-the-bank-journal-composite-entity"></a>Aktualizace složité entity bankovního deníku

[!include [banner](../includes/banner.md)]

Tento článek uvádí kroky potřebné k přidání dalšího pole BankTransactionType field do složitého záznamu BankJournalEntity.

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
