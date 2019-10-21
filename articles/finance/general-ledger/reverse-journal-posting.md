---
title: Stornování zaúčtování deníků
description: V tomto tématu jsou popsány funkce, které umožňují stornovat doklady ze seznamu transakcí dokladu nebo z finančních deníků.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248578"
---
# <a name="reverse-journal-posting"></a>Stornování zaúčtování deníků

[!include [banner](../includes/banner.md)]

Toto téma popisuje funkce schopnosti Microsoft Dynamics 365 Finance, které umožňují stornovat celý deník nebo stornovat jeden nebo více dokladů ze seznamu transakcí dokladu bez ohledu na jejich původ. 

## <a name="reversing-journals"></a>Storno deníků

Řádky deníku můžete stornovat jednotlivě. Při zaúčtování storna deníku můžete také stornovat celý finanční deník. Postup stornování deníku: 
- Otevření finančního deníku a filtrování podle zaúčtovaných deníků
- Klikněte na nabídku Stornovat v horní části stránky
- Zobrazí se celkový počet dokladů a řádků dokladů a také celková částka stornovaných řádků.
- Vyberte možnost Ano, chcete-li použít existující data transakcí nebo hodnotu Ne a zadat novou. V některých případech může být období původní transakce uzavřeno a pro stornování bude nutné zadat nové datum transakce.
- Pokud jste vybrali možnost Ne, zadejte datum transakce pro stornování. 
- Zadejte poznámku, kterou chcete přidat k transakci storna.
- Klikněte na tlačítko Stornovat.

Transakce budou stornovány. 

Pokud počet řádků dokladu překročí 100 řádků, bude proces storna proveden pomocí dávkového zpracování. Výsledky stornování můžete zkontrolovat zobrazením komentářů v dávkové úloze, která byla spuštěna. Všechny chyby budou zaznamenány v historii dávkové úlohy.

Pokud je počet řádků dokladu 100 nebo méně, bude proces storna spuštěn okamžitě. Výsledky budou uvedeny v dialogovém okně, ve kterém je zobrazen libovolný doklad, který nelze vrátit, a důvod, proč jej nelze stornovat. Kliknutím na tlačítko OK dialogové okno zavřete.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Stornování dokladů ze seznamu transakcí dokladu. 

Můžete také stornovat doklady ze **seznamu transakcí dokladu** ve všech dílčích knihách. Kromě toho lze najednou stornovat více dokladů. 

Chcete-li stornovat jeden nebo více dokladů, postupujte takto: 
- Klikněte na nabídku Stornovat v horní části stránky
- Zobrazí se celkový počet dokladů a řádků dokladů a také celková částka stornovaných řádků.
- Vyberte možnost Ano, chcete-li použít existující data transakcí nebo hodnotu Ne a zadat novou. V některých případech může být období původní transakce uzavřeno a pro stornování bude nutné zadat nové datum transakce.
- Pokud jste vybrali možnost Ne, zadejte datum transakce pro stornování. 
- Zadejte poznámku, kterou chcete přidat k transakci storna.
- Klikněte na tlačítko Stornovat.

Transakce budou stornovány. 

Pokud počet řádků dokladu překročí 100 řádků, bude proces storna proveden pomocí dávkového zpracování. Výsledky stornování můžete zkontrolovat zobrazením komentářů v dávkové úloze, která byla spuštěna. Všechny chyby budou zaznamenány v historii dávkové úlohy.

Pokud je počet řádků dokladu 100 nebo méně, bude proces storna spuštěn okamžitě. Výsledky budou uvedeny v dialogovém okně, ve kterém je zobrazen libovolný doklad, který nelze vrátit, a důvod, proč jej nelze stornovat. Kliknutím na tlačítko OK dialogové okno zavřete.

