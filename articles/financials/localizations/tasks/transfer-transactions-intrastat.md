--- 
title: "Převod transakcí do systému Intrastat"
description: "Tento postup vás provede nastavením parametrů systému Intrastat a převodem transakcí do systému Intrastat."
author: Anasyash
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategory, UnitOfMeasureLookup, ProcCategoryAddCommodityCode, EcoResProductDetailsExtended, IntrastatCommodityLookup, IntrastatTransactionCode, IntrastatParameters, DeliveryMode, MarkupTable, SalesTableListPage, SalesCreateOrder, SalesTable, MarkupTrans, SalesEditLines,  Intrastat, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cc21497a6905cdb57bd687b7bff0d9dc810ba9eb
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="transfer-transactions-to-the-intrastat"></a>Převod transakcí do systému Intrastat

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup vás provede nastavením parametrů systému Intrastat a převodem transakcí do systému Intrastat. Tato procedura byla vytvořena pomocí ukázkových dat společnosti DEMF.


## <a name="create-new-and-update-existing-commodity-code"></a>Vytvoření nového a aktualizace existujícího kódu komodity
1. Přejděte do nabídky Řízení informací o produktech > Nastavení > Kategorie a atributy > Hierarchie kategorií.
2. V seznamu vyhledejte nebo vyberte záznam, "Kódy komodit systému Intrastat".
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Ve stromovém zobrazení vyberte „záznam“.
    * Vyberte například „Intrastat\Reproduktor“.  
5. Klikněte na položku Upravit.
6. Rozbalte oddíl Zahraniční obchod.
7. V poli Dodatečné jednotky zadejte nebo vyberte hodnotu.
    * Vyberte například „ks“.  
8. V poli Hmotnost nelze použít vyberte možnost Ano.
9. Ve stromovém zobrazení vyberte Intrastat.
10. Klikněte na možnost Nový uzel kategorie.
11. Do pole Název zadejte název komodity.
    * Například zadejte „Jiné zboží“.  
12. V poli Kód zadejte kód komodity.
    * Zadejte například 995 00 00.  
13. Do pole Popisný název zadejte hodnotu.
    * Zadejte například Jiné.  
14. Klikněte na položku Uložit.
15. Zavřete stránku.

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a>Přiřazení kódu komodity k hierarchii produktů a uvolněným produktům
1. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli Jméno pomocí hodnoty „prodeje“.
2. Klikněte na odkaz na vybraném řádku v seznamu.
3. Ve stromovém zobrazení rozbalte uzel kategorie.
    * Například rozbalte "Prodejní hierarchie\Domácí audio".  
4. Ve stromovém zobrazení vyberte kategorii, ke které chcete přiřadit kód komodity.
    * Například vyberte "Prodejní hierarchie\Domácí audio\Reproduktory".  
5. Rozbalte oddíl Kódy komodit.
6. Klepněte na možnost Přidat.
7. V poli Vybrat hierarchii vyberte Intrastat.
8. Vyhledejte ze seznamu kód komodity a vyberte ho.
    * Vyberte například „Reproduktor 920 20 34“.  
9. Klepněte na SelectCodes.
10. Klikněte na tlačítko OK.
11. Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.
12. V seznamu vyberte uvolněný produkt, který přiřadíte ke kódu komodity.
    * Vyberte například „D0001“.  
13. Klikněte na položku Upravit.
14. Rozbalte oddíl Zahraniční obchod.
15. V poli Komodita zadejte kód komodity.
    * Vyberte například hodnotu „Reproduktor 920 20 34“.    
16. V poli Procento nákladů zadejte požadované číslo.
    * Například zadejte 3.  
17. V poli Země/oblast zadejte nebo vyberte zemi nebo oblast původu
    * Vyberte například AUT.  
18. Rozbalte oblast Spravovat sklad.
19. V poli Čistá hmotnost zadejte hmotnost v kg.
    * Například zadejte 2.5.  
20. Klikněte na položku Uložit.

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a>Nastavení kódy transakcí systému Intrastat a parametrů zahraničního obchodu
1. Přejděte na Daň > Nastavení > Zahraniční obchod > Kódy transakcí
2. Klikněte na položku Nová.
3. V poli Kód transakce zadejte hodnotu.
    * Jako kód transakce použitý pro vrácení zadejte například hodnotu 21.  
4. Zadejte název kódu transakce do pole Název.
    * Například zadejte Vrácení.  
5. Vyberte volbu v poli Statistická částka.
    * Vyberte například možnost „Prázdné“, která značí, že Statistická hodnota uváděná pro transakce s kódem transakce „21“ bude vždy nula.  
6. Přejděte na Daň > Nastavení > Zahraniční obchod > Parametry zahraničního obchodu.
7. V poli Kód transakce zadejte nebo vyberte hodnotu.
    * Vyberte například 11.  
8. V poli Dobropis zadejte nebo vyberte hodnotu.
    * Tato hodnota určuje fyzické vrácení. Dobropis pro fyzické vrácení bude převeden do deníku Intrastat v opačném směru. Například vrácení pro „doručení“ je převedeno na expedici.   V opačném případě je dobropis považován za opravu a je převeden ve stejném směru s opačným znaménkem. Například korekce doručení je převedena jako přijetí se zápornou částkou, kde je aktivní příznak nastaven na "Oprava".  
9. Rozbalte sekci Převod.
10. Vyberte možnost Ano v poli Položky s kódem zboží.
    * Vyberte tuto možnost, pokud chcete převést pouze transakce s přiřazeným kódem zboží. Transakce bez kódu komodity nebudou převedeny do systému Intrastat.  
11. V poli „Převést při splnění kritéria pro“ vyberte požadovanou možnost.
    * Vyberte například "Jedno z vybraných".  
12. Rozbalte oddíl Hierarchie kódů komodit.
13. Klepněte na kartu vlastností Země/oblasti.
14. Klikněte na položku Nová.
15. V poli Země/oblast zadejte nebo vyberte hodnotu.
    * Například vyberte hodnotu „FRA“.  
16. V poli Kód Intrastat zadejte kód ISO pro danou zemi.
    * Zadejte například FR.  
17. Do zadávacího pole Země/oblast vyberte položku „EU“.
18. Klikněte na kartu Číselné řady.

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a>Nastavení způsobů dodání a pravidel pro zahrnutí nákladů v systému Intrastat
1. Přejděte na Prodej a marketing > Nastavení > Distribuce > Způsoby dodání
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte například 20 Air.  
3. Rozbalte oddíl Zahraniční obchod.
4. Klikněte na položku Upravit.
5. V poli Přeprava zadejte nebo vyberte hodnotu.
    * Vyberte například 02.  
6. Přejděte na Pohledávky > Nastavení poplatků > Kód nákladů.
7. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli Kód nákladů pomocí hodnoty „dopravné“.
8. Rozbalte oddíl Zahraniční obchod.
9. Klikněte na položku Upravit.
10. Vyberte možnost Ano v poli Hodnota faktury Intrastat.
    * Částka bude přenesena do pole s náklady faktury a bude shrnuta s ohledem na převedenou částkou v poli Částka faktury.    Vyberte možnost Ano v poli Statistická hodnota Intrastat, pokud je třeba soubor změn přenést do pole Statistické náklady a shrnout pomocí pole Statistická částka.  

## <a name="sell-products-for-eu-customers"></a>Prodej produktů odběratelům EU
1. Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet odběratele vyberte zákazníka EU.
    * Vyberte například "DE-012 Litware Retail".  
4. Rozbalte sekci Dodání.
5. V poli Způsob dodání vyberte nebo zadejte hodnotu.
    * Vyberte například 20 Air.  
6. Klikněte na tlačítko OK.
7. Umístěte kurzor na první řádek z řádků prodejní objednávky.
8. V poli Číslo zboží zadejte nebo vyberte hodnotu.
    * Vyberte například D001.  
9. Rozbalte sekci Podrobnosti řádku.
10. Klepněte na kartu zahraničního obchodu.
    * Přeprava je vyplněna automaticky z vybraného způsobu dodání.  
11. V poli Přístav zadejte nebo vyberte hodnotu.
12. Klepněte na tlačítko Finanční údaje.
    * Podle nastavení se tato částka zahrne v poli Hodnota faktury Intrastat.  
13. Klikněte na položku Spravovat náklady.
14. V poli Kód nákladů zadejte nebo vyberte hodnotu.
    * V tomto příkladu vyberte Dopravné.  
15. Zaškrtněte políčko Zachovat.
16. Zadejte číslo do pole Hodnota nákladů.
    * Například zadejte 10.  
17. Klikněte na položku Uložit.
18. Zavřete stránku.
19. V podokně akcí klikněte na položku Faktura.
20. Klikněte na položku Faktura.
21. Rozbalte sekci Parametry.
22. V poli Množství vyberte možnost Vše.
23. Rozbalte sekci Nastavení.
24. Do pole Datum faktury zadejte datum.
    * Například zadejte 2015-01-31.  
25. Klikněte na tlačítko OK.
26. Klikněte na tlačítko OK.
27. Zavřete stránku.
28. Klikněte na položku Nová.
29. V poli Účet odběratele vyberte zákazníka EU.
    * Vyberte například DE-013 Trey Wholesales  
30. Klikněte na tlačítko OK.
31. V poli Číslo zboží zadejte nebo vyberte hodnotu.
    * Vyberte například D0001.  
32. Klikněte na položku Uložit.
33. Klikněte na položku Faktura.
34. Do pole Datum faktury zadejte datum.
    * Například zadejte datum 2015-01-31.  
35. Klikněte na tlačítko OK.
36. Klikněte na tlačítko OK.

## <a name="transfer-transactions-to-the-intrastat"></a>Převod transakcí do systému Intrastat
1. Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.
2. Klepněte na položku Převod.
3. Vyberte možnost Ano v poli Faktura odběratele.
4. Klepněte na tlačítko Filtr.
5. Označte na seznamu řádek s datem.
6. Zadejte hodnotu do pole Kritéria.
    * Například zadejte filtr pro období Leden 2015 (přesná hodnota závisí na formátu data): 1/1/2015..1/31/2015  
7. Klikněte na tlačítko OK.
8. Klikněte na tlačítko OK.
9. Vyhledejte na seznamu převedený záznam a vyberte ho.
10. Klikněte na záložku Obecné.
    * Zkontrolujte převedená data včetně Cílová země/oblast expedice, země původu, hmotnosti, množství, množství v dalších jednotkách, zboží, kódu transakce, výše faktury a statistických částek.   Tato data lze v případě potřeby změnit.  


