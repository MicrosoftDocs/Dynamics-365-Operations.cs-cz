---
title: Import akreditivu
description: Tato procedura vás provede procesem importu akreditivu.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1768494182a79d7a33044498c1e768e61d937d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "313559"
---
# <a name="import-letter-of-credit"></a>Import akreditivu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura vás provede procesem importu akreditivu. Před provedením této procedury je nutné nastavit následující: bankovní zařízení, účetní profily, smlouvu zařízení banky a bankovní údaje dodavatele.

Tato procedura používá ukázkovou společnost USMF.


## <a name="create-a-purchase-order-with-letter-of-credit"></a>Vytvoření nákupní objednávky s akreditivem
1. Přejděte na Závazky > Nákupní objednávky > Všechny nákupní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet dodavatele zadejte nebo vyberte hodnotu.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Rozbalte sekci Obecné.
7. V poli Lokalita zadejte nebo vyberte hodnotu.
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. V poli Sklad zadejte nebo vyberte hodnotu.
10. Klikněte na odkaz na vybraném řádku v seznamu.
11. Zadejte datum do pole Datum účtování.
12. Zadejte datum do pole Datum dodání.
    * Poznámka: V poli „Typ bankovního dokumentu“ musí být vybrána hodnota „Akreditiv“.  
13. Klikněte na tlačítko OK.
14. V poli Číslo zboží zadejte nebo vyberte hodnotu.
15. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
16. Klikněte na odkaz na vybraném řádku v seznamu.
17. Rozbalte sekci Podrobnosti řádku.
18. Klepněte na kartu Doručení.
19. Zadejte datum do pole Datum dodání.
20. Zadejte datum do pole Potvrzené datum dodání.
21. Zadejte číslo do pole Jednotková cena.
    * Definujte podrobnosti akreditivu.  
22. V podokně akcí klepněte na možnost Spravovat.
23. Klikněte na Akreditiv nebo kolekci importu.
24. Do pole Datum použití zadejte datum a čas.
    * Ověřte, že pole „Bankovní účet“ má výchozí aktivní bankovní účet, který je založen na datu aplikace.  
25. Zadejte hodnotu do pole Číslo bankovního dokumentu.
26. Do pole Datum příjmu zadejte datum a čas.
27. Rozbalte oddíl Bankovní dokument.
28. Do pole Datum vypršení platnosti zadejte datum a čas.
29. Rozbalte část Bankovní údaje.
30. V poli Avizující banka zadejte nebo vyberte hodnotu.
31. Klikněte na odkaz na vybraném řádku v seznamu.
32. Klikněte na položku Uložit.
33. Klikněte na možnost Načíst dodávky nákupní objednávky.
34. Zavřete stránku.
35. V podokně akcí klikněte na položku Nákup.
36. Klikněte na tlačítko Potvrdit.
37. V podokně akcí klepněte na možnost Spravovat.
38. Klikněte na Akreditiv nebo kolekci importu.
39. Klikněte na možnost Zpracovat.
40. Klikněte na tlačítko Potvrdit.
    * Ověřte, zda Zůstatek zařízení snižuje částku nákupní objednávky.  V tomto příkladu Nákupní částka = 500,00,  Limit zařízení = 10 000,00,  tedy Zůstatek zařízení = 9 500,00.  
41. Zavřete stránku.
42. Zadejte číslo do pole Jednotková cena.
43. Klikněte na položku Uložit.
44. V podokně akcí klikněte na položku Nákup.
45. Klikněte na tlačítko Potvrdit.
    * Upravte akreditiv z důvodu změny v jednotkové ceně.  
46. V podokně akcí klepněte na možnost Spravovat.
47. Klikněte na Akreditiv nebo kolekci importu.
    * Upravte akreditiv z důvodu změny v jednotkové nákupní jednotkové ceně.  
48. Klikněte na možnost Zpracovat.
49. Klikněte na možnost Připojit.
50. Klepněte na tlačítko Odebrat.
51. Klepněte na tlačítko Ano.
52. Klikněte na možnost Načíst dodávky nákupní objednávky.
53. Klikněte na možnost Zpracovat.
54. Klikněte na tlačítko Potvrdit.
    * Ověřte, zda Zůstatek zařízení snižuje částku nákupní objednávky.  V tomto příkladu upravená Nákupní částka = 600,00,  Limit zařízení = 10 000,00,  tedy Zůstatek zařízení = 9 400,00.  
55. Zavřete stránku.

## <a name="post-packing-slip"></a>Zaúčtovat dodací list
1. V podokně akcí klikněte na položku Přijmout.
2. Klikněte na položku Příjemka produktu.
3. Zadejte hodnotu do pole PurchParmTable_Num.
    * Vyberte číslo dodávky vytvořené s odkazem na akreditiv.  
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Zadejte datum do pole Příjemka produktu.
6. Klikněte na tlačítko OK.
7. Zavřete stránku.
8. Zavřete stránku.

## <a name="verify-import-letter-of-credit-status"></a>Ověření stavu importního akreditivu
1. Přejděte na Pokladna a banka > Akreditivy > Importovat akreditiv a kolekci importu.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
    * Ověřte stav importního akreditivu.    
    *   
4. Zavřete stránku.
5. Zavřete stránku.

## <a name="post-purchase-invoice"></a>Zaúčtování nákupní faktury
1. Přejděte na Závazky > Nákupní objednávky > Všechny nákupní objednávky.
    * Vyberte nákupní objednávku, která byla vytvořena s akreditivem.  
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. V podokně akcí klikněte na položku Faktura.
5. Klepněte na Faktura.
6. Zadejte hodnotu do pole Číslo.
7. V poli Číslo dodávky zadejte nebo vyberte hodnotu.
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. Do pole Datum faktury zadejte datum.
10. Klikněte na položku Aktualizovat stav párování.
11. Klikněte na položku Zaúčtovat.
12. Zavřete stránku.
13. Zavřete stránku.

## <a name="verify-import-letter-of-credit-status"></a>Ověření stavu importního akreditivu
1. Přejděte na Pokladna a banka > Akreditivy > Importovat akreditiv a kolekci importu.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
    * Ověřte stav akreditivu2.  
    * Ověřit:  Stav dodávky =  Fakturováno Podronmosti bankovního zařízení  
4. Klikněte na možnost Zobrazit.
5. Klikněte na možnost Tisk přihlášky.
6. Klikněte na tlačítko OK.
    * Ověřte, že se přihláška akreditivu vytiskne.  
7. Zavřete stránku.
8. Zavřete stránku.
9. Zavřete stránku.

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a>Zaúčtovat deník plateb dodavatele pro vytvořené nákupní faktury s akreditivem
1. Přejděte na Závazky > Platby > Deník plateb.
2. Klikněte na položku Nová.
3. V poli Název zadejte nebo vyberte hodnotu.
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Klikněte na možnost Řádky.
6. Do pole Datum zadejte datum.
7. Zadejte požadované hodnoty do pole Účet.
8. Klikněte na možnost Vyrovnat transakce.
9. Rozbalte část Součty.
10. Vyberte možnost v poli Zobrazit.
    * Ověřte, aby byla aktualizovány pole Číslo bankovního dokumentu a Číslo dodávky.  
11. Vyberte Zaškrtnout políčko.
12. Klikněte na tlačítko OK.
13. Klikněte na kartu Platba.
    * Ověřte, aby byla aktualizovány pole Číslo bankovního dokumentu a Číslo dodávky.  
14. Klikněte na položku Zaúčtovat.
15. Zavřete stránku.
16. Zavřete stránku.

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a>Po zaplacení faktury ověřte stav importního akreditivu
1. Přejděte na Pokladna a banka > Akreditivy > Importovat akreditiv a kolekci importu.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
    * Ověřte stav importního akreditivu.   
4. Zavřete stránku.

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a>Ověření limitu bankovního zařízení a sestavu využití
1. Přejděte na Pokladna a banka > Dotazy a sestavy > Akreditivy a záruční listiny > Sestava zařízení banky a využití.
2. Rozbalte oddíl Záznamy k zahrnutí.
3. Klepněte na tlačítko Filtr.
    * Definujte pole Kritéria pomocí požadovaného bankovního účtu.  
4. V poli Kritéria zadejte nebo vyberte hodnotu.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Klikněte na tlačítko OK.
7. Klikněte na tlačítko OK.
    * Ověřte sestavu, která obsahuje seznam transakcí.  
    * Ověřte že sestava obsahuje seznam transakcí s číslem bankovního dokladu, limitem zařízení, využitou částkou a částkou zůstatku zařízení.  
8. Zavřete stránku.

