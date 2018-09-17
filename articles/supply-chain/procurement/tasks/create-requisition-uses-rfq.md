--- 
title: "Vytvoření žádanky používající požadavek na nabídku"
description: "Tato příručka popisuje postup přidání informací o ceně a dodavateli do nákupní žádanky z procesu požadavku na nabídku."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d97ccd15031b2f7398486eee4a716ecef5e9dafd
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Vytvoření žádanky používající požadavek na nabídku

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato příručka popisuje postup přidání informací o ceně a dodavateli do nákupní žádanky z procesu požadavku na nabídku. Příklad uvedený v tomto průvodci lze použít u ukázkových dat společnosti USMF, a vy musíte být k dokončení všech kroků přihlášeni jako správce. Úkoly v této příručce obvykle provádí odborníci v oblasti zásobování.


## <a name="create-a-requisition"></a>Vytvoření žádanky
1. Přejděte do nabídky Zásobování a zdroje > Nákupní žádanky > Nákupní žádanky připravené mnou.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Název.
4. Zadejte datum do pole Požadované datum.
5. Zadejte datum do pole Datum účtování.
6. Klepněte na tlačítko OK.
7. V poli Důvod zadejte nebo vyberte hodnotu.
8. Klikněte na položku Přidat řádek.
9. V poli Kategorie zásobování vyberte ve stromové struktuře kategorii a klepněte na tlačítko OK.
10. Do pole Název produktu zadejte hodnotu.
11. Zadejte číslo do pole Množství.
12. V poli Jednotka zadejte nebo vyberte hodnotu.
13. Klikněte na položku Uložit.
14. Kliknutím na možnost Workflow otevřete dialogové okno.
15. Klepněte na tlačítko Odeslat.
16. Zavřete stránku.
17. Klepněte na tlačítko Odeslat.

## <a name="reassign-a-workflow-task"></a>Znovu přiřadit úlohu do workflowu
    * Další úkol je vytvořit požadavek na nabídku pro získání nabídek na váš produkt od dodavatelů. V ukázkových datech společnosti USMF je workflow žádanky nastaven s pravidlem. Díky tomu pokud dodavatel není vybrán, nebo je jednotková cena na řádku 0, úloha se přiřadí ke konkrétnímu pracovníkovi s cílem vytvořit požadavek na nabídku. Chcete-li pokračovat v této příručce, je nutné změnit přiřazení daného úkolu jinému uživateli (vám). To můžete provést jen po přihlášení jako správce.  
1. Kliknutím na možnost Workflow otevřete dialogové okno.
2. Klikněte na Zobrazit historii.
3. Aktualizujte stránku.
4. Rozbalte část Sledování podrobností.
5. Ve stromovém zobrazení vyberte „řádek začínající na Workflow řádku byl aktivován v“.
6. Klikněte na Zobrazit podrobnosti workflowu.
7. Rozbalte sekci Pracovní položky.
8. Klepněte na tlačítko Změnit přiřazení.
9. V poli Uživatel vyberte možnost Správce.
10. Klepněte na tlačítko Změnit přiřazení.
11. Zavřete stránku.
12. Zavřete stránku.

## <a name="create-an-rfq"></a>Vytvoření požadavku na nabídku
1. Aktualizujte stránku.
2. Klikněte na Požadavek na nabídku.
3. V poli Kupující právnická osoba vyberte možnost USMF.
    * Je nutné vybrat stejnou právnickou osobu, která je uvedena na řádku požadavku.  
4. Označte v seznamu vybraný řádek.
    * Pokud máte více řádků v nákupní žádance, vyberte všechny řádky, které chcete přidat do požadavku na nabídku.  
5. Klikněte na tlačítko OK.
6. Aktualizujte stránku.
7. Otevřete okno s fakty a rozbalte oddíl Související dokumenty.
    * Okno s fakty je již pravděpodobně otevřené. Vyhledejte ikonu se šipkou napravo od tlačítka Přepnout řádky a záhlaví. Pokud šipka ukazuje vpravo, okno s fakty je již otevřeno. Pokud šipka ukazuje doleva, kliknutím na ni okno s fakty otevřete.  
8. Klepněte na odkaz v poli Požadavek na nabídku a otevřete tak požadavek na nabídku, který jste právě vytvořili.
9. Klikněte na Záhlaví.
10. Klepněte na možnost Přidat.
11. V poli Účet dodavatele zadejte nebo vyberte hodnotu.
12. Klepněte na možnost Přidat.
13. V poli Účet dodavatele zadejte nebo vyberte hodnotu.
14. Klepněte na tlačítko Odeslat.
15. Klikněte na tlačítko OK.
16. Klikněte na Zadat odpověď.
17. V podokně akcí klikněte na možnost Odpovědět.
18. Klikněte na Kopírovat data do odpovědi.
    * Dojde tak ke zkopírování dat, jako je množství a data, z požadavku na nabídku do odpovědi.  
19. Zadejte číslo do pole Jednotková cena.
    * Jedná se o cenu, kterou jste obdrželi od dodavatele. Můžete také zadat doplňující informace od dodavatele.  
20. Klepněte na možnost Akceptovat.
21. Klikněte na tlačítko OK.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Ověřte, že dodavatel a cena byly převedeny do požadavku
1. Zavřete stránku.
2. Klikněte na položku Řádky.
3. Klepněte na položku Související informace.
4. Klikněte na Nákupní žádanka.
5. Vyberte řádek, který byl převeden na požadavek na nabídku.
    * Ověřte, že cena i dodavatel byly zkopírováni do žádanky.  
6. Kliknutím na možnost Workflow otevřete dialogové okno.
7. Klikněte na tlačítko Dokončit.
8. Zavřete stránku.
9. Klikněte na tlačítko Dokončit.


