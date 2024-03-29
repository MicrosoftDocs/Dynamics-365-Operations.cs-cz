---
title: Export akreditivu
description: Tato procedura vás provede procesem exportního akreditivu.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf06a73bf7665059658c7884a0b9f973929d647c
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779547"
---
# <a name="export-letter-of-credit"></a>Export akreditivu

[!include [banner](../../includes/banner.md)]

Tato procedura vás provede procesem exportního akreditivu.

Pojem akreditiv označuje bankovní smlouvu, ve které banka souhlasí se zajištěním platby jménem kupujícího za předpokladu, že jsou splněny podmínky mezi kupujícím a prodávajícím.



Před provedením této procedury spusťte procedury **Nastavení zařízení banky a zaúčtování profilů** a **Akreditiv_Vytvoření smlouvy o bankovních zařízeních**. Abyste mohli úspěšně spustit tuto proceduru, musí být vybrána ukázková společnost USMF.


## <a name="create-sales-order-for-export-letter-of-credit"></a>Vytvoření prodejní objednávky pro exportní akreditiv
1. Přejděte na **Pohledávky > Objednávky > Všechny prodejní objednávky**.
2. Klepněte na možnost **Nový**.
3. V poli **Účet odběratele** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Rozbalte nebo sbalte oddíl **Obecné**.
7. V poli **Lokalita** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Umožňuje vybrat nebo zobrazit **lokalitu**, ve které je uloženo zboží k vydání.  
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. V poli **Sklad** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Umožňuje vybrat nebo zobrazit **sklad**, ve kterém je uloženo zboží k vydání.  
10. Klikněte na odkaz na vybraném řádku v seznamu.
    * Poznámka: V poli **Typ bankovního dokumentu** musí být vybrána hodnota **Akreditiv**.  
11. Vyberte v poli **Typ bankovního dokumentu** možnost **Akreditiv**.
12. Rozbalte nebo sbalte oddíl **Dodání**.
    * Vyberte **Řízení data dodání** = **Žádné**.  
13. Zadejte datum do pole **Požadované datum příjmu**.
14. Klikněte na tlačítko **OK**.
15. V poli **Číslo položky** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Vyberte požadované zboží k výdeji nebo prodeji.  
16. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
17. Klikněte na odkaz na vybraném řádku v seznamu.
18. Zadejte číslo do pole **Jednotková cena**.
19. Rozbalte nebo sbalte oddíl **Podrobnosti řádku**.
20. Klikněte na záložku **Dodání**.
21. Zadejte datum do pole **Požadované datum expedice**.
22. Zadejte datum do pole **Potvrzené datum expedice**.
23. V podokně akcí klikněte na **Spravovat**.
24. Klikněte na možnost **Akreditiv**.
25. Zadejte hodnotu do pole **Číslo bankovního dokumentu**.
26. Do pole **Datum vypršení** platnosti zadejte datum a čas.
27. Rozbalte nebo sbalte oddíl **Bankovní údaje**.
28. V poli **Vydávající banka** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
29. Klikněte na odkaz na vybraném řádku v seznamu.
30. V poli **Avizující banka** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
31. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
32. Klikněte na odkaz na vybraném řádku v seznamu.
33. Klikněte na možnost **Načíst dodávky prodejní objednávky**.
34. Klikněte na možnost **Vydat bankovní dokument**.
35. Zavřete stránku.

## <a name="post-packing-slip"></a>Zaúčtovat dodací list
1. V podokně akcí klikněte na tlačítko **Vyskladnit a zabalit**.
2. Klikněte na **Zaúčtovat dodací list**.
3. Rozbalte nebo sbalte oddíl **Parametry**.
4. V poli **Množství** vyberte možnost **Vše**.
5. Rozbalte nebo sbalte oddíl **Nastavení**.
6. Do pole **Datum dodacího listu** zadejte datum.
7. Vyberte číslo dodávky.
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. Klikněte na tlačítko **OK**.
10. Klikněte na tlačítko **OK**.

## <a name="post-sales-invoice"></a>Zaúčtovat prodejní fakturu
1. V podokně akcí klikněte na možnost **Faktura**.
2. Klikněte na **Faktura**.
3. Rozbalte nebo sbalte oddíl **Přehled**.
4. Vyberte **číslo dodávky**.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Rozbalte nebo sbalte oddíl **Nastavení**.
7. Zadejte datum do pole **Datum faktury**.
8. Klikněte na tlačítko **OK**.
9. Klikněte na tlačítko **OK**.

## <a name="shipment-document-submitted-status"></a>Stav odeslaného dodacího dokladu
1. V podokně akcí klikněte na **Spravovat**.
2. Klikněte na možnost **Akreditiv**.
3. Rozbalte nebo sbalte oddíl **Řádky**.
    * Poznámka: Pole **Dokument odeslán** je nastaveno na hodnotu **Ano**.  

## <a name="verify-export-letter-of-credit"></a>Ověřit exportní akreditiv
1. Přejděte na **Pokladna a banka > Akreditivy > Exportovat akreditiv a kolekci importu**.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
    * Ověřte, že **Exportovat akreditiv** má **stav dodávky** **Fakturováno**.  

## <a name="customer-payment"></a>Platba odběratele
1. Přejděte na **Pohledávky > Platby > Deník plateb**.
2. Klepněte na možnost **Nový**.
3. Označte v seznamu vybraný řádek.
4. V poli **Název** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Klikněte na možnost **Řádky**.
7. Do pole **Datum** zadejte datum.
8. Zadejte požadované hodnoty do pole **Účet**.
9. Klikněte na **vyrovnání**.
10. Zaškrtněte políčko záhlaví součtů.
    * Poznámka: Nastavte pole **Zobrazit** na hodnotu **Akreditiv**.  
11. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
12. Zaškrtněte políčko **Označit** nebo jeho zaškrtnutí zrušte.
13. Klikněte na tlačítko **OK**.
14. Klikněte na kartu **Platba**.
    * Ověření čísla bankovního dokumentu čísla dokladu a podrobností o čísle dodávky  
15. Klikněte na možnost **Zaúčtovat**.

## <a name="verify-export-letter-of-credit-after-payment"></a>Ověřit exportní akreditiv po platbě
1. Přejděte na **Pokladna a banka > Akreditivy > Exportovat akreditiv a kolekci importu**.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
    * Ověřte, že **stav dodávky** = **přijaté platby** a **částka zůstatku** = **0,00**.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
