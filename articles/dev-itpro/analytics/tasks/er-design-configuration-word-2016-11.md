--- 
title: "Návrh konfigurací elektronického výkaznictví pro generování sestav ve formátu Word"
description: "Následující kroky vysvětlují, jak uživatel v roli správce systému nebo vývojáře elektronického výkaznictví může nakonfigurovat formáty elektronického výkaznictví pro generování sestav v podobě souborů aplikace Microsoft Word."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: dc47d44285af4c720d2f450d11fb1004ef461d0f
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a>Návrh konfigurací elektronického výkaznictví pro generování sestav ve formátu Word

[!include [task guide banner](../../includes/task-guide-banner.md)]

Následující kroky vysvětlují, jak uživatel v roli správce systému nebo vývojáře elektronického výkaznictví může nakonfigurovat formáty elektronického výkaznictví (ER) pro generování sestav v podobě souborů aplikace Microsoft Word. Tyto kroky lze provést v rámci společnosti GBSI.

K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky průvodce záznamem úloh s názvem „Vytvoření konfigurace ER pro generování sestav ve formátu OPENXML“. Předem musíte také stáhnout a uložit následující šablony pro vzorovou sestavu:

- [Šablona sestavy platby](https://go.microsoft.com/fwlink/?linkid=862266)
- [Vázaná šablona sestavy platby](https://go.microsoft.com/fwlink/?linkid=862266)


Tato procedura je určena pro funkci, která byla přidána do aplikace Microsoft Dynamics 365 for Operations, verze 1611.


## <a name="select-the-existing-er-report-configuration"></a>Volba existující konfigurace sestavy ER
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
    * Ujistěte se, že je poskytovatel konfigurace ‘Litware, Inc.’ zvolen jako aktivní.  
2. Klikněte na Konfigurace výkaznictví.
    * Znovu použijeme existující konfiguraci ER, která byla původně vytvořena ke generování výstupu sestavy ve formátu OPENXML.  
3. Ve stromovém zobrazení rozbalte „Model platby“.
4. Ve stromovém zobrazení vyberte Model platby\Ukázková sestava listu.
5. Klikněte na možnost Návrhář.

## <a name="replace-the-excel-template-with-the-word-template"></a>Výměna šablony aplikace Excel za šablonu aplikace Word
    * V současné době se používá dokument Excel jako šablona pro generování výstupu ve formátu OPENXML. Budeme importovat šablonu sestavy ve formátu Word.  
1. Klikněte na Přílohy.
    * Nahraďte existující šablonu aplikace Excel za šablonu Word s názvem SampleVendPaymDocReport.docx, kterou jste předtím stáhli. Všimněte si, že tato šablona obsahuje pouze rozvržení dokumentu, který chceme generovat jako ER výstup.  
2. Klepněte na tlačítko Odstranit.
3. Klepněte na tlačítko Ano.
4. Klikněte na položku Nová.
5. Klepněte na volby Soubor.
6. Klikněte na tlačítko Procházet. Vyhledejte a zvolte soubor SampleVendPaymDocReport.docx, který jste předtím stáhli. Klikněte na tlačítko OK.
    * Vyberte šablonu, kterou jste stáhli v předchozím kroku.  
7. V poli Šablona zadejte nebo vyberte hodnotu.

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>Rozšíření šablony aplikace Word přidáním vlastní části XML
1. Klikněte na položku Uložit.
    * Kromě uložení změn v konfiguraci aktualizuje připojenou šablonu aplikace Word rovněž akce Uložit. Struktura navrženého formátu je přenesena do připojeného dokumentu aplikace Word jako nová vlastní část XML s názvem 'Sestava'. Všimněte si, že připojená šablona aplikace Word obsahuje nejen rozvržení dokumentu, který chceme generovat jako ER výstup, ale zároveň i strukturu dat, která budou ER předána do této šablony za běhu.  
2. Klikněte na Přílohy.
    * Nyní je třeba navázat prvky vlastní části XML Sestava na části dokumentu aplikace Word.  
    * Pokud jste obeznámeni s dokumenty Word, které lze navrhovat jako formuláře obsahující ovládací prvky obsahu provázané s prvky vlastních částí XML, projděte si všechny kroky dalšího dílčího úkolu pro vytvoření takového dokumentu. Další informace naleznete na odkazu https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US. V opačném případě přeskočte všechny kroky v dalším dílčím úkolu.  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>Získání aplikace Word s vlastní částí XML pro provedení vazby dat
    * Otevřete teno dokument v aplikaci Word a proveďte následující:  – Otevřete kartu Vývojář v aplikaci Word (přizpůsobte si pás karet, pokud není ještě povolena).  - Vyberte podokno mapování XML.  - Vyberte ve vyhledávacím poli vlastní část XML ‘Sestava’.  - Proveďte mapování prvků vybrané vlastní části XML a ovládacích prvků obsahu dokumentu aplikace Word.  - Uložte aktualizovaný dokument Word na místní disk.  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>Odeslání šablony Word s vlastní částí XML navázanou na ovládací prvky obsahu
1. Klepněte na tlačítko Odstranit.
2. Klepněte na tlačítko Ano.
    * Přidejte novou šablonu. Pokud jste dokončili kroky uvedené v předchozím dílčím úkolu, vyberte dokument aplikace Word, který jste připravili a uložili místně. V opačném případě vyberte dříve staženou šablonu MS Word SampleVendPaymDocReportBounded.docx.  
3. Klikněte na položku Nová.
4. Klepněte na volby Soubor.
5. Klikněte na tlačítko Procházet. Vyhledejte a zvolte soubor SampleVendPaymDocReportBounded.docx, který jste předtím stáhli. Klepněte na tlačítko OK.
6. V poli Šablona zvolte dokument, který jste stáhli v předchozím kroku.
7. Klikněte na položku Uložit.
8. Zavřete stránku.

## <a name="execute-the-format-to-create-word-output"></a>Spuštění formátu pro vytvoření výstupu ve Wordu
1. V podokně akcí klikněte na možnost Konfigurace.
2. Klikněte na Parametry uživatelů.
3. Vyberte možnost Ano v poli Nastavení běhu.
4. Klikněte na tlačítko OK.
5. Klikněte na položku Upravit.
6. Vyberte možnost Ano v poli Koncept běhu.
7. Klikněte na položku Uložit.
8. Zavřete stránku.
9. Zavřete stránku.
10. Přejděte na Závazky > Platby > Deník plateb.
11. Klikněte na položku Řádky.
12. V seznamu označte všechny řádky nebo jejich označení zrušte.
13. Klikněte na Stav platby.
14. Klikněte na možnost Žádný.
15. Klepněte na Generovat platby.
16. Klikněte na tlačítko OK.
17. Klikněte na tlačítko OK.
    * Analyzujte vygenerovaný výstup. Povšimnete si, že vytvořený výstup je ve formátu aplikace Word a obsahuje podrobnosti o zpracovaných platbách.  


