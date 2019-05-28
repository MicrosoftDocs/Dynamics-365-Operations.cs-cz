---
title: Export akreditivu
description: Tato procedura vás provede procesem exportního akreditivu.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 730a6cc6ed4872f8d0ad92b89665587f472f6791
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566149"
---
# <a name="export-letter-of-credit"></a>Export akreditivu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura vás provede procesem exportního akreditivu.

Pojem akreditiv označuje bankovní smlouvu, ve které banka souhlasí se zajištěním platby jménem kupujícího za předpokladu, že jsou splněny podmínky mezi kupujícím a prodávajícím.



Před provedením této procedury spusťte procedury „Nastavení zařízení banky a zaúčtování profilů“ a „Akreditiv_Vytvoření smlouvy o bankovních zařízeních“. Abyste mohli úspěšně spustit tuto proceduru, musí být vybrána ukázková společnost USMF.




## <a name="create-sales-order-for-export-letter-of-credit"></a>Vytvoření prodejní objednávky pro exportní akreditiv
1. Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet odběratele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Rozbalte nebo sbalte oddíl Obecné.
7. V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Umožňuje vybrat nebo zobrazit lokalitu, ve které je uloženo zboží k vydání.  
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Umožňuje vybrat nebo zobrazit sklad, ve kterém je uloženo zboží k vydání.  
10. Klikněte na odkaz na vybraném řádku v seznamu.
    * Poznámka: V poli Typ bankovního dokumentu musí být vybrána hodnota „Akreditiv“.  
11. Vyberte v poli Typ bankovního dokumentu možnost „Akreditiv“.
12. Rozbalte nebo sbalte oddíl Dodání.
    * Vyberte Řízení data dodání = Žádné.  
13. Zadejte datum do pole Požadované datum příjmu.
14. Klikněte na tlačítko OK.
15. V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Vyberte požadované zboží k výdeji nebo prodeji.  
16. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
17. Klikněte na odkaz na vybraném řádku v seznamu.
18. Zadejte číslo do pole Jednotková cena.
19. Rozbalte nebo sbalte oddíl Podrobnosti řádku.
20. Klepněte na kartu Doručení.
21. Zadejte datum do pole Požadované datum expedice.
22. Zadejte datum do pole Potvrzené datum expedice.
23. V podokně akcí klepněte na možnost Spravovat.
24. Klikněte na možnost Akreditiv.
25. Zadejte hodnotu do pole Číslo bankovního dokumentu.
26. Do pole Datum vypršení platnosti zadejte datum a čas.
27. Rozbalte nebo sbalte oddíl Bankovní údaje.
28. V poli Vydávající banka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
29. Klikněte na odkaz na vybraném řádku v seznamu.
30. V poli Avizující banka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
31. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
32. Klikněte na odkaz na vybraném řádku v seznamu.
33. Klikněte na možnost Načíst dodávky prodejní objednávky.
34. Klikněte na možnost Vydat bankovní dokument.
35. Zavřete stránku.

## <a name="post-packing-slip"></a>Zaúčtovat dodací list
1. V podokně akcí klikněte na položku Vyskladnit a zabalit.
2. Klikněte na položku Zaúčtovat dodací list.
3. Rozbalte nebo sbalte oddíl Parametry.
4. V poli Množství vyberte možnost „Vše“.
5. Rozbalte nebo sbalte oddíl Nastavení.
6. Do pole Datum dodacího listu zadejte datum.
7. Vyberte číslo dodávky.
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. Klikněte na tlačítko OK.
10. Klikněte na tlačítko OK.

## <a name="post-sales-invoice"></a>Zaúčtovat prodejní fakturu
1. V podokně akcí klikněte na položku Faktura.
2. Klikněte na položku Faktura.
3. Rozbalte nebo sbalte oddíl Přehled.
4. Vyberte číslo dodávky.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Rozbalte nebo sbalte oddíl Nastavení.
7. Do pole Datum faktury zadejte datum.
8. Klikněte na tlačítko OK.
9. Klikněte na tlačítko OK.

## <a name="shipment-document-submitted-status"></a>Stav odeslaného dodacího dokladu
1. V podokně akcí klepněte na možnost Spravovat.
2. Klikněte na možnost Akreditiv.
3. Rozbalte nebo sbalte oddíl Řádky.
    * Poznámka: Pole Dokument odeslán je nastaveno na hodnotu „Ano“.  

## <a name="verify-export-letter-of-credit"></a>Ověřit exportní akreditiv
1. Přejděte na Pokladna a banka > Akreditivy > Exportovat akreditiv a kolekci importu.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
    * Ověřte, že exportní akreditiv má stav dodávky „Fakturováno“.  

## <a name="customer-payment"></a>Platba odběratele
1. Přejděte na Pohledávky > Platby > Deník plateb.
2. Klikněte na položku Nová.
3. Označte v seznamu vybraný řádek.
4. V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Klikněte na možnost Řádky.
7. Do pole Datum zadejte datum.
8. Zadejte požadované hodnoty do pole Účet.
9. Klepněte na vyrovnání.
10. Zaškrtněte políčko záhlaví součtů.
    * Poznámka: Nastavte možnost Zobrazit pole na hodnotu „akreditiv“.  
11. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
12. Zaškrtněte políčko Označit nebo jeho zaškrtnutí zrušte.
13. Klikněte na tlačítko OK.
14. Klikněte na kartu Platba.
    * Ověření čísla bankovního dokumentu čísla dokladu a podrobností o čísle dodávky  
15. Klikněte na položku Zaúčtovat.

## <a name="verify-export-letter-of-credit-after-payment"></a>Ověřit exportní akreditiv po platbě
1. Přejděte na Pokladna a banka > Akreditivy > Exportovat akreditiv a kolekci importu.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
    * Ověřit stav dodávky = přijaté platby a částka zůstatku = 0,00.  

