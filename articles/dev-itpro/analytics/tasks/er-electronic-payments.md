--- 
title: "Generování elektronických dokumentů pro platby za použití konfigurace formátu pro elektronické výkaznictví (ER)"
description: "Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může použít novou konfiguraci formátu pro elektronické výkaznictví a vytvořit tak elektronické doklady pro zpracování plateb."
author: NickSelin
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a5d958d3b55bfa76f3cfbb3c1a289e4e89c49146
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="generate-electronic-documents-for-payments-using-a-format-configuration-for-electronic-reporting-er"></a>Generování elektronických dokumentů pro platby za použití konfigurace formátu pro elektronické výkaznictví (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může použít novou konfiguraci formátu pro elektronické výkaznictví a vytvořit tak elektronické doklady pro zpracování plateb. Tyto kroky lze provést v rámci vzorové společnosti GBSI.

K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření konfigurace s formátem platebního dokladu".


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

