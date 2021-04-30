---
title: Stornování zaúčtování deníků
description: V tomto tématu jsou popsány funkce, které umožňují stornovat doklady ze seznamu transakcí dokladu nebo z finančních deníků.
author: MikeFalkner
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ab53f4b8888f77cd41ccbd7956ed307ba1b54ff
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897129"
---
# <a name="reverse-journal-posting"></a>Stornování zaúčtování deníků

[!include [banner](../includes/banner.md)]

Toto téma popisuje funkce schopnosti Microsoft Dynamics 365 Finance, které umožňují stornovat celý deník nebo jeden nebo více dokladů ze seznamu transakcí dokladu bez ohledu na jejich původ. 

## <a name="reversing-journals"></a>Storno deníků

Řádky deníku můžete stornovat jednotlivě. Při zaúčtování storna deníku můžete také stornovat celý finanční deník. Postup stornování deníku: 

- Otevřete finanční deník a filtrujte podle zaúčtovaných deníků.
- Vyberte na nabídku **Stornovat** v horní části stránky.
- Zobrazí se celkový počet dokladů a řádků dokladů a také celková částka stornovaných řádků.
- Vyberte možnost **Ano**, chcete-li použít existující data transakcí nebo hodnotu **Ne** a zadat novou. V některých případech může být období původní transakce uzavřeno a pro stornování bude nutné zadat nové datum transakce.
- Pokud vyberete možnost **Ne**, zadejte datum transakce pro stornování. 
- Zadejte poznámku, kterou chcete přidat k transakci storna.
- Zvolte tlačítko **Stornovat**.

Transakce budou stornovány. 

Pokud počet řádků dokladu obsahuje více než 100 řádků, bude proces storna proveden pomocí dávkového zpracování. Výsledky můžete zkontrolovat zobrazením komentářů v dávkové úloze. Všechny transakce, u nichž nelze provést stornování, budou uvedeny v historii dávkové úlohy.

Pokud doklad obsahuje 100 nebo méně řádků, bude proces storna spuštěn okamžitě. Výsledky budou uvedeny v dialogovém okně, ve kterém je zobrazen libovolný doklad, který nelze vrátit, a důvod, proč jej nelze stornovat. Zvolte **OK** a zavřete dialogové okno.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Stornování dokladů ze seznamu transakcí dokladu. 

Můžete také stornovat doklady ze **seznamu transakcí dokladu** ve všech dílčích knihách. Kromě toho lze najednou stornovat více dokladů. 

Chcete-li stornovat jeden nebo více dokladů, postupujte takto: 

- Vyberte na nabídku **Stornovat** v horní části stránky.
- Zobrazí se celkový počet dokladů a řádků dokladů a také celková částka stornovaných řádků.
- Vyberte možnost **Ano**, chcete-li použít existující data transakcí nebo hodnotu **Ne** a zadat novou. V některých případech může být období původní transakce uzavřeno a pro stornování bude nutné zadat nové datum transakce.
- Pokud vyberete možnost **Ne**, zadejte datum transakce pro stornování. 
- Zadejte komentář popisující transakci stornování.
- Zvolte tlačítko **Stornovat**.

Transakce budou stornovány. 

Pokud počet řádků dokladu obsahuje více než 100 řádků dokladu, bude proces storna proveden pomocí dávkového zpracování. Výsledky můžete zkontrolovat zobrazením komentářů v dávkové úloze. Všechny transakce, u nichž nelze provést stornování, budou uvedeny v historii dávkové úlohy.

Pokud je počet řádků dokladu 100 nebo méně, bude proces storna spuštěn okamžitě. Výsledky se zobrazí v dialogovém okně, ve kterém je zobrazen libovolný doklad, který nelze vrátit, a důvod, proč jej nelze stornovat. Zvolte **OK** a zavřete dialogové okno.

Transakce lze stornovat pouze v případě, že vyhovují obchodním pravidlům pro jejich stornování. Platby dodavatele nelze stornovat pomocí možnosti popsané v tomto tématu. Platby dodavatelů je nutné stornovat podle kroků uvedených v části [Stornování platby dodavatele](../accounts-payable/reverse-vendor-payment.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]