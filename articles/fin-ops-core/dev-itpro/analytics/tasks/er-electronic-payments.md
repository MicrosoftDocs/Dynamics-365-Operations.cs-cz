---
title: Generování elektronických dokumentů ER pro platby za použití konfigurace formátu
description: Toto téma popisuje, jak použít novou konfiguraci elektronického výkaznictví (ER) ke generování elektronických dokumentů ke zpracování plateb.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f62d7cd690406647886f9d6d1cb1491b691d4159
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752477"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a>Generování elektronických dokumentů ER pro platby za použití konfigurace formátu

[!include [banner](../../includes/banner.md)]

Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může použít novou konfiguraci formátu pro elektronické výkaznictví a vytvořit tak elektronické doklady pro zpracování plateb. Tyto kroky lze provést v rámci vzorové společnosti GBSI.

K provedení těchto kroků musíte nejprve dokončit kroky v postupu „Vytvoření konfigurace s formátem platebního dokladu“.


## <a name="change-the-configuration-of-the-electronic-payment-method"></a>Úprava konfigurace metody elektronické platby
1. Přejděte do nabídky Závazky > Nastavení platby > Metody platby.
2. V případě potřeby klepnutím rozbalte oddíl Formát souboru.
3. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli Metody platby pomocí hodnoty „Elektronicky“.
4. Klikněte na položku Upravit.
5. Vyberte možnost Ano v poli Obecné elektronické výkaznictví.
    * Vyberte možnost Ano, chcete-li použít pro generování souborů plateb obecný vzor elektronického vykazování.  
6. V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. Vyberte konfiguraci formátu BACS (Velká Británie – fiktivní).
8. Klikněte na položku Uložit.
9. Zavřete stránku.

## <a name="test-the-format-of-generated-payment-files"></a>Test formátu generovaných souborů platby
1. Přejděte na Závazky > Platby > Deník plateb.
2. Klikněte na položku Nová.
3. Označte v seznamu vybraný řádek.
4. V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte VendPay.  
6. Klikněte na položku Uložit.
7. Klikněte na položku Řádky.
8. Zadejte hodnotu DEMF do pole Společnost.
    * DEMF  
9. Zadejte hodnotu DE-01001 do pole Účet.
    * DE – 01001  
10. V poli Popis uveďte text Platba.
    * Platba  
11. Do pole Má dáti zadejte čísl.
    * 1 000  
12. Klikněte na kartu Platba.
13. V poli Způsob platby kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
14. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte elektronickou hodnotu.  
15. Klikněte na odkaz na vybraném řádku v seznamu.
16. Klikněte na položku Uložit.
17. Klepněte na Generovat platby.
18. V poli Způsob platby kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
19. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Vyberte elektronickou hodnotu.  
20. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte elektronickou hodnotu.  
21. Zadejte hodnotu do pole Název souboru.
    * Zadejte například Platby.  
22. V poli Bankovní účet kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
23. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte hodnotu GBSI OPER.  
24. Klikněte na tlačítko OK.
25. Klikněte na tlačítko OK.
    * Analyzujte vytvořený soubor platby ve formátu XML. Srovnejte jej s navrženým rozvržením dokumentu a definovanými atributy platební transakce.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]