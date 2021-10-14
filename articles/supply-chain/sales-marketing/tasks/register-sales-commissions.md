---
title: Registrace prodejních provizí
description: V tomto tématu je vysvětleno, jak se počítají a registrují prodejní provize.
author: Henrikan
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f4aca37350938d54d4acf283093365bfcab64f70
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575356"
---
# <a name="register-sales-commissions"></a>Registrace prodejních provizí

[!include [banner](../../includes/banner.md)]

V tomto tématu je vysvětleno, jak se počítají a registrují prodejní provize. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. Před spuštěním této příručky, spusťte průvodce s názvem „Nastavení pravidel prodejní provize“ abyste měli všechna nezbytná nastavení výpočtu provize.

Poznamenejte si čísla odběratele a zboží, které jste zvolili pro proces provize a použijte je, když budete v této příručce vyzváni k vytvoření prodejní objednávky.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Faktura prodejní objednávky, která opravňuje prodejce získat provizi
1. V navigačním podokně přejděte na **Moduly > Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky**.
2. Zvolte **Nové**.
3. V poli **Účet odběratele** vyberte požadovaný záznam v rozevírací nabídce.
4. Vyberte **OK**.
5. V podokně akcí vyberte **Možnosti**.
6. Vyberte **Změnit zobrazení**.
7. Vyberte **Zobrazení záhlaví**.
8. Rozbalte sekci **Nastavení**.

    - Hodnota v poli **Prodejní skupina** představuje skupinu s jedním nebo více přiřazenými prodejními zástupci. Uživatelé ve skupině jsou ti, kteří po vyfakturování objednávky podle předdefinované sazby a distribuce obdrží provizi.   
    - Hodnota se zkopíruje z karty zákazníka, ale pokud chcete, lze ji změnit.  
    - Skupina prodeje se zkopíruje také do řádku prodejní objednávky. Můžete ji změnit tak, že se může lišit od skupiny uvedené v záhlaví a/nebo mezi řádky.  
    - Hodnota v poli **Skupina provize** představuje skupinu, kterou jste vytvořili pro jednoho nebo více odběratelů za účelem sledování provizí.   
    - Hodnota se zkopíruje z karty zákazníka, ale pokud chcete, lze ji změnit.   

9. V podokně akcí vyberte **Možnosti**.
10. Vyberte **Změnit zobrazení**.
11. Vyberte **Zobrazení řádku**.
12. V rozevírací nabídce pole **Číslo položky** vyberte položku, kterou jste nastavili pro provize. 
13. Zadejte číslo do pole **Množství**. Udělejte si poznámku o řádku Čistá částka. Ta představuje výnosy z prodeje, které v tomto příkladu jsou základem pro výpočet provize.  
14. Zvolte **Uložit**.
15. V podokně akcí vyberte možnost **Faktura**.
16. Vyberte možnost **Faktura**.
17. Rozbalte sekci **Parametry**.
18. V poli **Množství** vyberte možnost **Vše**.
19. Vyberte možnost **Ano** v poli **Účtování**.
20. Vyberte **OK** a poté vyberte **OK** v dalším podokně. Zaúčtování transakce může trvat kolem minuty. K dokončení povolte zpracování a nezavírejte stránku.  

## <a name="review-the-registered-sales-commissions"></a>Zobrazení registrovaných provizí z prodeje
1. V podokně akcí zvolte **Faktura** a poté opět vyberte **Faktura**.
2. V podokně akcí zvolte **Faktura** a poté vyberte **Transakce provizí**.

    - Na kartě **Přehled** jsou zobrazeny řádky představující částky provize vyplacené prodejním zástupcům, kteří jsou přiřazeni k vyfakturované prodejní objednávce. Zkontrolujme si podrobnosti.  
    - Pokud jste použili průvodce „Nastavení pravidel prodejní provize“ k nastavení skupiny **Prodejní provize**, existují dva prodejci, kteří obdrží provizi, a provize bude mezi nimi rozdělena stejnoměrně.  
    - V tomto příkladu se vypočítává celková částka provize jako procento výnosu z prodeje (čistá částka řádku objednávky).  
3. Zavřete stránku.
4. Vyberte **Doklad**. Transakce dokladu můžete zkontrolovat pro částky provize, které byly zaúčtované do předdefinovaných výdajů a účtů vyplacené provize.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]