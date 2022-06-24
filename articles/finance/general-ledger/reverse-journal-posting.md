---
title: Stornování zaúčtování deníku
description: V tomto článku jsou popsány funkce, které umožňují stornovat doklady ze seznamu transakcí dokladu nebo z finančních deníků.
author: kweekley
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
ms.openlocfilehash: bec7d5d0dd64a2d89b00e2aa630a4fe670feaa2b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868395"
---
# <a name="reverse-journal-posting"></a>Stornování zaúčtování deníku

[!include [banner](../includes/banner.md)]

Tento článek popisuje funkce schopnosti Microsoft Dynamics 365 Finance, které umožňují stornovat celý deník nebo jeden nebo více dokladů ze seznamu transakcí dokladu bez ohledu na jejich původ. 

Než budete moci použít některou z funkcí popsaných v tomto článku, je třeba je v systému zapnout. Správci mohou pomocí pracovního prostoru **Správa funkcí** zkontrolovat stav funkce a zapnout ji, pokud je třeba. Funkce je zde uvedena následujícím způsobem:
 - Modul: Hlavní kniha
 - Název funkce: **Hromadné vracení více dokumentů**

## <a name="reversing-journals"></a>Storno deníků

Řádky deníku můžete stornovat jednotlivě. Při zaúčtování storna deníku můžete také stornovat celý finanční deník. Postup stornování deníku: 

- Filtrujte zaúčtované deníky a otevřete zobrazení **Řádky** deníku.
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

- Vyberte na nabídku **Stornovat celou rozevírací nabídku deníku** v horní části stránky.
- Zobrazí se celkový počet dokladů a řádků dokladů a také celková částka stornovaných řádků.
- Vyberte možnost **Ano**, chcete-li použít existující data transakcí nebo hodnotu **Ne** a zadat novou. V některých případech může být období původní transakce uzavřeno a pro stornování bude nutné zadat nové datum transakce.
- Pokud vyberete možnost **Ne**, zadejte datum transakce pro stornování. 
- Zadejte komentář popisující transakci stornování.
- Zvolte tlačítko **Stornovat**.

Transakce budou stornovány. 

Pokud počet řádků dokladu obsahuje více než 100 řádků dokladu, bude proces storna proveden pomocí dávkového zpracování. Výsledky můžete zkontrolovat zobrazením komentářů v dávkové úloze. Všechny transakce, u nichž nelze provést stornování, budou uvedeny v historii dávkové úlohy.

Pokud je počet řádků dokladu 100 nebo méně, bude proces storna spuštěn okamžitě. Výsledky se zobrazí v dialogovém okně, ve kterém je zobrazen libovolný doklad, který nelze vrátit, a důvod, proč jej nelze stornovat. Zvolte **OK** a zavřete dialogové okno.

Transakce lze stornovat pouze v případě, že vyhovují obchodním pravidlům pro jejich stornování. Platby dodavatele nelze stornovat pomocí možnosti popsané v tomto článku. Platby dodavatelů je nutné stornovat podle kroků uvedených v části [Stornování platby dodavatele](../accounts-payable/reverse-vendor-payment.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
