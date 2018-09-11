--- 
title: "Transakce záruční listiny"
description: "Tato procedura vás provede procesem Záruční listina."
author: kweekley
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c2e215f1ae16f907c8b64ea1f05cf67bfb0a04b6
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="letter-of-guarantee-transaction"></a>Transakce záruční listiny

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura vás provede procesem Záruční listina.



Před provedením této procedury je nutné dokončit následující úlohy:

- Nastavení bankovních zařízení a účetních profilů pro záruční listinu.

- Vytvoření smlouvy bankovního zařízení pro záruční listinu.



Tato procedura používá ukázkovou společnost USMF.


## <a name="create-sales-order-with-letter-of-guarantee"></a>Tvorba prodejní objednávky se záruční listinou
1. Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet odběratele zadejte nebo vyberte hodnotu.
4. Rozbalte sekci Obecné.
5. V poli Lokalita zadejte nebo vyberte hodnotu.
6. Klikněte na odkaz na vybraném řádku v seznamu.
7. V poli Sklad zadejte nebo vyberte hodnotu.
8. Klikněte na odkaz na vybraném řádku v seznamu.
9. Vyberte v poli Typ bankovního dokumentu možnost „Záruční listina“.
10. Klepněte na tlačítko OK.
11. V poli Číslo zboží zadejte nebo vyberte hodnotu.
12. Zadejte číslo do pole Jednotková cena.
13. Rozbalte sekci Podrobnosti řádku.
14. Klikněte na záložku Dodání.
    * Poznámka: Vyberte Řízení data dodání = Žádné.  
15. Zadejte datum do pole Požadované datum expedice.
16. Zadejte datum do pole Potvrzené datum expedice.

## <a name="process-letter-of-guaranteerequest"></a>Zpracovat příkaz záruční listina_Požadavek
1. V podokně akcí klepněte na možnost Spravovat.
2. Klikněte na možnost Záruční listina.
3. V podokně akcí klikněte na možnost Záruční listina.
4. Kliknutím na možnost Požadavek otevřete dialogové okno.
5. V poli Typ zadejte nebo vyberte hodnotu.
6. Klikněte na odkaz na vybraném řádku v seznamu.
7. Zadejte číslo do pole Hodnota.
8. Do pole Datum vypršení platnosti zadejte datum a čas.
9. Klikněte na tlačítko OK.
10. Zavřete stránku.

## <a name="process-letter-of-guaranteesubmit-to-bank"></a>Zpracovat příkaz záruční listina_Odeslat do banky
1. Přejděte na možnost Pokladna a banka > Záruční listiny > Záruční listiny.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Kliknutím na Odeslat do banky otevřete dialogové okno.
4. V poli Bankovní účet zadejte nebo vyberte hodnotu.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Klikněte na tlačítko OK.

## <a name="process-letter-of-guaranteereceive-from-bank"></a>Zpracovat příkaz záruční listina_Přijmout z banky
1. Kliknutím na Přijmout z banky otevřete dialogové okno.
2. Zadejte hodnotu do pole Číslo banky.
    * Ověřte hodnoty ve vypočtených polích Marže a výdaje.  
3. Klikněte na tlačítko OK.
4. Rozbalte sekci Akce.
    * Ověřte záznam „Přijmout z banky“.  
5. Klepnutím přejdete na odkaz v poli Číslo dávky deníku.
6. Klikněte na položku Řádky.
    * Ověřte záznamy zaúčtování deníku.  
7. Zavřete stránku.

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a>Zpracovat příkaz záruční listina_Předat příjemci
1. Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.
2. Klikněte na odkaz na vybraném řádku v seznamu.
3. V podokně akcí klepněte na možnost Spravovat.
4. Klikněte na možnost Záruční listina.
5. V podokně akcí klikněte na možnost Záruční listina.
6. Kliknutím na Dát příjemci otevřete dialogové okno.
7. Klikněte na tlačítko OK.
8. Přejděte na možnost Pokladna a banka > Záruční listiny > Záruční listiny.
9. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
10. Kliknutím na Dát příjemci otevřete dialogové okno.
11. Klikněte na tlačítko OK.
12. Rozbalte sekci Akce.
    * Ověřte záznam „Dát příjemci“.  

## <a name="process-letter-of-guaranteeincrease-value"></a>Zpracovat příkaz záruční listina_Zvýšit hodnotu
1. Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.
2. Klikněte na odkaz na vybraném řádku v seznamu.
3. V podokně akcí klepněte na možnost Spravovat.
4. Klikněte na možnost Záruční listina.
5. V podokně akcí klikněte na možnost Záruční listina.
6. Kliknutím na možnost Zvýšit hodnotu otevřete dialogové okno.
7. Zadejte číslo do pole Hodnota k navýšení.
8. Klikněte na tlačítko OK.
9. Přejděte na možnost Pokladna a banka > Záruční listiny > Záruční listiny.
10. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
11. Kliknutím na možnost Zvýšit hodnotu otevřete dialogové okno.
12. Klikněte na tlačítko OK.
13. Rozbalte sekci Akce.
    * Ověřte záznam „Zvýšit hodnotu“.  
14. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
15. Klepnutím přejdete na odkaz v poli Číslo dávky deníku.
16. Klikněte na položku Řádky.
    * Ověřte zaúčtované záznamy deníku.  

## <a name="process-letter-of-guaranteeliquidate"></a>Zpracovat příkaz záruční listina_Likvidovat
1. Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.
2. Klikněte na odkaz na vybraném řádku v seznamu.
3. V podokně akcí klepněte na možnost Spravovat.
4. Klikněte na možnost Záruční listina.
5. V podokně akcí klikněte na možnost Záruční listina.
6. Otevřete dialogové okno kliknutím na možnost Likvidovat.
7. Klikněte na tlačítko OK.
8. Přejděte na možnost Pokladna a banka > Záruční listiny > Záruční listiny.
9. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
10. Otevřete dialogové okno kliknutím na možnost Likvidovat.
11. Klikněte na tlačítko OK.
12. Rozbalte sekci Akce.
    * Ověřte záznam „Likvidovat“.  
13. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
14. Klepnutím přejdete na odkaz v poli Číslo dávky deníku.
15. Klikněte na položku Řádky.
    * Ověřte zaúčtované záznamy deníku.  
16. Zavřete stránku.


