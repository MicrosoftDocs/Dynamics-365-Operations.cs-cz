---
title: EEU 00047 Záloha pro zaměstnance
description: Tato procedura ukazuje, jak lze nastavit a registrovat transakce pro držitele zálohy.
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: RCashTable, LedgerJournalSetup, HcmWorkerGroup_RU, EmplPosting_RU, VendParameters, RCashPosting, BankParameters, PaymTerm, HcmWorker, HcmWorkerNewWorker, HcmWorkerAdvHolderTableListPage_RU, HcmWorkerAdvHolderTable_RU, PurchTable, PurchCreateOrder, HcmAdvHolderLookup_RU, InventItemIdLookupPurchase, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, EmplTrans_RU, EmplBalance_RU
ms.openlocfilehash: 4406aea1b5c6d45c3768de63d694c13457afc04c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282391"
---
# <a name="eeu-00047-advance-payment-to-employee"></a>EEU 00047 Záloha pro zaměstnance

[!include [banner](../../includes/banner.md)]

Tato procedura ukazuje, jak lze nastavit a registrovat transakce pro držitele zálohy. Procedura byla vytvořena za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Litvě. Tento úkol lze použít pouze pro právnické osoby s primární adresu v Polsku, Litvě, Lotyšsku, Estonsku, České republice nebo Maďarsku. Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.


## <a name="create-a-new-cash-account"></a>Vytvoření nového bankovního účtu
1. Přejděte do nabídky Pokladna a banka > Bankovní účty > Pokladní účty.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Hotovost.
4. Zadejte hodnotu do pole Název.
5. V poli Skupina číselné řady zadejte nebo vyberte hodnotu.
6. Rozbalte sekci Ověření.
7. V poli Měna zadejte nebo vyberte hodnotu.
8. Vyberte možnost Ano v poli Záporná hotovost.
9. Klikněte na položku Uložit.

## <a name="create-a-new-journal"></a>Vytvoření nového deníku
1. Přejděte do hlavní knihy > Nastavení deníku > Názvy deníků.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název.
4. V poli Číselná řada dokladů zadejte nebo vyberte hodnotu.
5. Klikněte na položku Uložit.
6. Klepněte na možnost Nový.
7. Zadejte hodnotu do pole Název.
8. Vyberte volbu v poli Typ deníku.
9. V poli Číselná řada dokladů zadejte nebo vyberte hodnotu.
10. Klikněte na položku Uložit.

## <a name="create-an-advance-holder-group"></a>Vytvoření skupiny držitelů záloh
1. Přejděte na Závazky > Nastavení > Držitelé zálohy > Skupiny držitelů záloh.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Skupina.
4. Zadejte nějakou hodnotu do pole Popis.
5. Klikněte na položku Uložit.

## <a name="create-an-employee-posting-profile"></a>Vytvoření účetního profilu zaměstnance
1. Přejděte na Závazky > Nastavení > Držitelé zálohy > Účetní profily zaměstnanců.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Účetní profil.
4. Zadejte nějakou hodnotu do pole Popis.
5. Označte na seznamu vybraný řádek.
6. Vyberte volbu v poli Platné pro.
7. Zadejte požadované hodnoty do pole Součtový účet.
8. Klikněte na položku Uložit.

## <a name="set-up-advance-holder-parameters"></a>Nastavení parametrů držitele zálohy
1. Přejděte do nabídky Závazky > Nastavení > Parametry závazků.
2. Klepněte na kartu Držitelé zálohy.
3. V poli Účetní profil zadejte nebo vyberte hodnotu.
4. V poli Název zadejte nebo vyberte hodnotu.
5. V poli Hotovost zadejte nebo vyberte hodnotu.
6. V poli Název zadejte nebo vyberte hodnotu.
7. V poli Typ účtu vyberte možnost.
8. Zadejte požadované hodnoty do pole Hlavní účet.
9. Klikněte na kartu Číselné řady.
10. Klikněte na položku Uložit.

## <a name="set-up-a-cash-posting-profile"></a>Nastavení účetního profilu pro hotovost
1. Přejděte do nabídky Pokladna a banka > Nastavení > Účetní profily pro hotovost.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Účtování hotovosti.
4. Zadejte nějakou hodnotu do pole Popis.
5. Označte na seznamu vybraný řádek.
6. Vyberte volbu v poli Platné pro.
7. Zadejte požadované hodnoty do pole Hlavní účet.
8. Klikněte na položku Uložit.

## <a name="set-up-cash-and-bank-parameters"></a>Nastavení parametrů pokladny a banky
1. Přejděte do nabídky Pokladna a banka > Nastavení > Parametry pokladny a banky.
2. Klikněte na kartu Hotovost.
3. V poli Hotovost zadejte nebo vyberte hodnotu.
4. V poli Účtování hotovosti nebo vyberte hodnotu.
5. Klepněte na tlačítko Uložit.
6. Klikněte na kartu Číselné řady.
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
8. V poli Kód číselné řady zadejte nebo vyberte hodnotu.
9. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
10. V poli Kód číselné řady zadejte nebo vyberte hodnotu.
11. Klikněte na položku Uložit.

## <a name="set-up-terms-of-payment"></a>Nastavit podmínky platby
1. Přejděte do nabídky Závazky > Nastavení platby > Podmínky platby.
2. Klikněte na položku Upravit.
3. Vyberte možnost Ano v poli Od držitele zálohy.
4. Klikněte na položku Uložit.

## <a name="create-a-new-worker"></a>Vytvoření nového pracovníka
1. Přejděte k nabídce Lidské zdroje > Pracovníci > Pracovníci.
2. Klikněte na položku Nová.
3. Do pole Křestní jméno zadejte hodnotu.
4. Do pole příjmení zadejte hodnotu.
5. Zadejte hodnotu do pole ID pracovníka.
6. Klikněte na Přijmout nového pracovníka.
7. Klikněte na položku Uložit.

## <a name="set-up-a-worker-as-an-advance-holder"></a>Nastavení pracovníka jako držitele zálohy.
1. Přejděte na Závazky > Držitelé zálohy > Držitelé zálohy.
2. Klikněte na položku Upravit.
3. V poli Skupina zadejte nebo vyberte hodnotu.
4. Vyberte možnost Ano v poli Držitel zálohy.
5. Klikněte na položku Uložit.

## <a name="create-and-post-a-purchase-order-invoice"></a>Vytvoření a zaúčtování faktury nákupní objednávky.
1. Přejděte na Závazky > Nákupní objednávky > Všechny nákupní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet dodavatele zadejte nebo vyberte hodnotu.
4. Klepněte na tlačítko OK.
5. V poli Řádky nebo záhlaví vyberte možnost.
6. Rozbalte část Ceny a slevy.
7. V poli Platební podmínky zadejte nebo vyberte hodnotu.
8. V poli Držitel zálohy zadejte nebo vyberte hodnotu.
9. V poli Řádky nebo záhlaví vyberte možnost.
10. Označte na seznamu vybraný řádek.
11. V poli Číslo zboží zadejte nebo vyberte hodnotu.
12. Zadejte číslo do pole Množství.
13. Zadejte číslo do pole Jednotková cena.
14. Klikněte na položku Uložit.
15. V podokně akcí klikněte na položku Nákup.
16. Klikněte na tlačítko Potvrdit.
17. V podokně akcí klikněte na položku Faktura.
18. Klikněte na položku Faktura.
19. Kliknutím na Výchozí od: Množství v příjemce produktu otevřete dialogové okno.
20. Vyberte volbu v poli Výchozí množství pro řádky.
21. Klepněte na tlačítko OK.
22. Zadejte hodnotu do pole Číslo.
23. Do pole Popis faktury zadejte nějakou hodnotu.
24. Zadejte datum do pole Datum faktury.
25. Do pole Rejstřík DPH zadejte datum.
26. Zadejte datum do pole Datum přijetí dokumentu.
27. Klikněte na položku Zaúčtovat.

## <a name="balance-and-close-advance-holders-transactions"></a>Zůstatek a uzavření transakce držitelů záloh
1. Přejděte na Závazky > Držitelé zálohy > Držitelé zálohy.
2. Klikněte na Transakce.
3. Zavřete stránku.
4. Klikněte na Zůstatek.
5. Klikněte na Uzavřít v bance.
6. Vyberte možnost Ano v poli Automaticky.
7. V poli Převáděná částka zadejte číslo.
8. Klikněte na tlačítko OK.
9. Klikněte na Uzavřít v hotovosti.
10. Vyberte možnost Ano v poli Automaticky.
11. Klikněte na tlačítko OK.
12. Zavřete stránku.
13. Klikněte na Transakce.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
