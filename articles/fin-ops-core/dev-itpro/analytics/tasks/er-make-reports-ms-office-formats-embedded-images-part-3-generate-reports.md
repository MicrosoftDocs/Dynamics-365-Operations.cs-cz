---
title: Generování sestav ve formátech Office s integrovanými obrázky
description: Toto téma popisuje proces navrhování konfigurací elektronického výkaznictví (ER) ke generování elektronických dokumentů ve formátu Excel a Word obsahujících vložené obrázky.
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e15162251e5d6fa91c5a938fd846ef5b5c8cd7f
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093816"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a>Generování sestav ve formátech Office s integrovanými obrázky

[!include [banner](../../includes/banner.md)]

Následující postup popisuje, jak uživatel s rolí 'Správce systému' nebo 'Návrhář elektronického výkaznictví' může navrhnout konfigurace pro elektronické výkaznictví (ER) a vygenerovat tak elektronické dokumenty ve formátu MS Office (Excel nebo Word) s vloženými obrázky.

V tomto příkladu použijete vytvořené konfigurace ER pro vzorovou společnost 'Litware, Inc'.  K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky průvodce záznamem úloh "Vytváření sestav ER ve formátu MS Office s vloženými obrázky (část 2: konfigurace přehledu)". Tyto kroky lze provést v rámci společnosti 'USMF'.


## <a name="run-format-with-initial-model-mapping"></a>Spuštění formátu s počátečním mapováním modelu
1. Přejděte do části Pokladna a banka > Bankovní účty > Bankovní účty.
2. Použijte rychlý filtr k filtrování v poli Bankovní účet s hodnotou 'USMF OPER.
3. V podokně akcí klikněte na možnost Nastavit.
4. Klepněte na možnost Kontrola.
5. Klikněte na možnost Tisk testu.
    * Spusťte formát pro účely testování.  
6. V poli Obchodovatelný formát šeku vyberte Ano.
7. Klepněte na tlačítko OK.
    * Prohlédněte si vytvořený výstup. Logo společnosti se zobrazí v sestavě společně s podpisem oprávněné osoby. Obrázek podpisu je převzat z pole typu dat 'Kontejner' ze záznamu rozvržení šeku, který je přidružen k vybranému bankovnímu účtu.  
8. Rozbalte sekci Kopie.
9. Klikněte na položku Upravit.
10. V poli Vodoznak zadejte Tisknout vodoznak jako anulovaný.
    * Změňte nastavení rozložení vodoznaku tak, aby byl zobrazen text vodoznaku při generování dokumentu v elementu tvaru Excel.  
11. Klikněte na možnost Tisk testu.
12. Klepněte na tlačítko OK.
    * Prohlédněte si vytvořený výstup. Vodoznak je uveden v sestavě v souladu s možností výběru.  
13. Zavřete stránku.
14. V podokně akcí klikněte na možnost Spravovat platby.
15. Klikněte na možnost Kontroly.
16. Klepněte na tlačítko Zobrazit filtry.
17. Použijte následující filtry: zadejte hodnotu filtru "381","385","389" v poli Číslo kontroly za pomocí operátoru filtru „je jeden z“.
18. V seznamu označte všechny řádky.
19. Klikněte na Tisknout kopii šeku.
    * Spusťte formát a znovu vytiskněte vybrané šeky.  
    * Prohlédněte si vytvořený výstup. Vybrané šeky byly znovu vytištěny. Logo společnosti a popisky nejsou vytištěny, protože jsou uvedeny na předtištěném formuláři.  

## <a name="modify-the-mapping-of-the-imported-data-model"></a>Úprava mapování importovaného modelu dat
1. Zavřete stránku.
2. Zavřete stránku.
3. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
4. Ve stromové struktuře zvolte Model pro šeky.
5. Klikněte na možnost Návrhář.
6. Klikněte na možnost Mapovat model na datový zdroj.
7. Klikněte na možnost Návrhář.
    * Upravíme vazbu položky podpisu datového modelu a získáme tak obrázek podpisu ze souboru připojeného k záznamu rozvržení šeku, který je přidružen k vybranému bankovnímu účtu.  
8. Vypněte možnost Zobrazit podrobnosti.
9. Ve stromové struktuře rozbalte Rozvržení.
10. Ve stromovém zobrazení rozbalte layout\signature.
11. Ve stromovém zobrazení vyberte layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp.
12. Ve stromovém zobrazení rozbalte Chequesaccount.
13. Ve stromovém zobrazení rozbalte chequesaccount\<Relations.
14. Ve stromovém zobrazení rozbalte chequesaccount\<Relations\BankChequeLayout.
15. Ve stromovém zobrazení rozbalte chequesaccount\<Relations\BankChequeLayout\<Relations.
16. Ve stromovém zobrazení rozbalte chequesaccount\<Relations\BankChequeLayout\<Relations\<Document.
17. Ve stromovém zobrazení vyberte chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer().
18. Klikněte na možnost Vazba.
19. Klikněte na položku Uložit.
20. Zavřete stránku.
21. Zavřete stránku.
22. Zavřete stránku.
23. Zavřete stránku.

## <a name="run-format-using-the-adjusted-model-mapping"></a>Spuštění formátu pomocí upraveného mapování modelu
1. Přejděte do části Pokladna a banka > Bankovní účty > Bankovní účty.
2. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli Bankovní účet pomocí hodnoty „USMF OPER“.
3. V podokně akcí klikněte na možnost Nastavit.
4. Klepněte na možnost Kontrola.
5. Klikněte na možnost Tisk testu.
6. Klepněte na tlačítko OK.
    * Prohlédněte si vytvořený výstup. Obrázek z přílohy správy dokumentů je zobrazen jako podpis oprávněné osoby.  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a>Použití dokumentu MS Word jako šablony v importovaném formátu
1. Zavřete stránku.
2. Zavřete stránku.
3. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
4. Ve stromové struktuře rozbalte Model pro šeky.
5. Ve stromovém zobrazení vyberte Model for cheques\Cheques printing format.
6. Klikněte na možnost Návrhář.
7. Klikněte na Přílohy.
8. Klepněte na tlačítko Odstranit.
9. Klepněte na tlačítko Ano.
10. Klikněte na položku Nová.
11. Klepněte na volby Soubor.
    * Klepněte na tlačítko Procházet a vyberte předem stažený soubor 'Cheque template Word.docx'.  
12. Zavřete stránku.
13. V poli Šablona zadejte nebo vyberte hodnotu.
14. Klikněte na položku Uložit.
15. Zavřete stránku.
16. Klikněte na položku Upravit.
17. Vyberte možnost Ano v poli Koncept běhu.
18. Zavřete stránku.
19. Přejděte do části Pokladna a banka > Bankovní účty > Bankovní účty.
20. Použijte rychlý filtr k filtrování v poli Bankovní účet s hodnotou 'USMF OPER.
21. Klepněte na možnost Kontrola.
22. Klikněte na možnost Tisk testu.
23. Klepněte na tlačítko OK.
    * Prohlédněte si vytvořený výstup. Výstup byl vygenerován jako dokument aplikace Word s vloženými obrázky loga společnosti, podpisem oprávněné osoby a vybraným textem vodoznaku.  

