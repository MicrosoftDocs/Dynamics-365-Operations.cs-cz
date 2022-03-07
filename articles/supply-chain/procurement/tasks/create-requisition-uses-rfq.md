---
title: Vytvoření žádanky používající požadavek na nabídku
description: Toto téma popisuje postup přidání informací o ceně a dodavateli do nákupní žádanky z procesu požadavku na nabídku.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6083afe0e2bfafd337d572863a198330e8cb6cc8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812126"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Vytvoření žádanky používající požadavek na nabídku

[!include [banner](../../includes/banner.md)]

Toto téma popisuje postup přidání informací o ceně a dodavateli do nákupní žádanky z procesu požadavku na nabídku. Příklad uvedený v tomto průvodci lze použít u ukázkových dat společnosti USMF, a vy musíte být k dokončení všech kroků přihlášeni jako správce. Úkoly v této příručce obvykle provádí odborníci v oblasti zásobování.


## <a name="create-a-requisition"></a>Vytvoření žádanky
1. V navigačním podokně přejděte na **Moduly > Zásobování a zdroje > Nákupní žádanky > Mnou připravené nákupní žádanky**.
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Název**.
4. Zadejte datum do pole **Požadované datum**.
5. Zadejte datum do pole **Datum účtování**.
6. Vyberte **OK**.
7. V poli **Důvod** zadejte nebo vyberte hodnotu.
8. Vyberte **Přidat řádek**.
9. V poli **Kategorie zásobování** vyberte ve stromové struktuře kategorii a zvolte **OK**.
10. Do pole **Název produktu** zadejte hodnotu.
11. Zadejte číslo do pole **Množství**.
12. V poli **Jednotka** zadejte nebo vyberte hodnotu.
13. Zvolte **Uložit**.
14. Kliknutím na možnost **Workflow** otevřete dialogové okno.
15. Vyberte **Odeslat**.
16. Zavřete stránku.
17. Vyberte **Odeslat**.

## <a name="reassign-a-workflow-task"></a>Znovu přiřadit úlohu do workflowu
Další úkol je vytvořit požadavek na nabídku pro získání nabídek na váš produkt od dodavatelů. V ukázkových datech společnosti USMF je workflow žádanky nastaven s pravidlem. Díky tomu pokud dodavatel není vybrán, nebo je jednotková cena na řádku 0, úloha se přiřadí ke konkrétnímu pracovníkovi s cílem vytvořit požadavek na nabídku. Chcete-li pokračovat v této příručce, je nutné změnit přiřazení daného úkolu jinému uživateli (vám). To můžete provést jen po přihlášení jako správce.  

1. Kliknutím na možnost **Workflow** otevřete dialogové okno.
2. Zvolte **Zobrazit historii**.
3. Aktualizujte stránku.
4. Rozbalte část **Sledování podrobností**.
5. Ve stromovém zobrazení vyberte řádek začínající na „Workflow řádku bylo aktivováno v“.
6. Zvolte **Zobrazit podrobnosti workflowu**.
7. Rozbalte sekci **Pracovní položky**.
8. Vyberte **Opětovně přiřadit**.
9. V poli **Uživatel** vyberte možnost **Správce**.
10. Vyberte **Opětovně přiřadit**.
11. Zavřete dvě stránky.

## <a name="create-an-rfq"></a>Vytvoření požadavku na nabídku

1. Aktualizujte stránku.
2. Zvolte **Požadavek na nabídku**.
3. V poli **Kupující právnická osoba** vyberte možnost **USMF**. Je nutné vybrat stejnou právnickou osobu, která je uvedena na řádku požadavku.  
4. Označte na seznamu vybraný řádek. Pokud máte více řádků v nákupní žádance, vyberte všechny řádky, které chcete přidat do požadavku na nabídku.  
5. Vyberte **OK**.
6. Aktualizujte stránku.
7. Zajistěte, že je otevřené okno s fakty, a rozbalte oddíl **Související dokumenty**.
8. Zvolte odkaz v poli **Požadavek na nabídku** a otevřete tak požadavek na nabídku, který jste právě vytvořili.
9. Vyberte **Záhlaví**.
10. Vyberte **přidat**.
11. V poli **Účet dodavatele** zadejte nebo vyberte hodnotu.
12. Vyberte **přidat**.
13. V poli **Účet dodavatele** zadejte nebo vyberte hodnotu.
14. Zvolte **Odeslat**.
15. Vyberte **OK**.
16. Vyberte **Zadat odpověď**.
17. V podokně akcí zvolte **Odpovědět**.
18. Zvolte **Kopírovat data do odpovědi**. Dojde tak ke zkopírování dat, jako je množství a data, z požadavku na nabídku do odpovědi.  
19. Zadejte číslo do pole **Jednotková cena**. Jedná se o cenu, kterou jste obdrželi od dodavatele. Můžete také zadat doplňující informace od dodavatele.  
20. Zvolte **Přijmout**.
21. Vyberte **OK**.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Ověřte, že dodavatel a cena byly převedeny do požadavku
1. Zavřete stránku.
2. Vybrat **řádky**.
3. Vyberte **Související informace**.
4. Zvolte **Nákupní žádanka**.
5. Vyberte řádek, který byl převeden na požadavek na nabídku. Ověřte, že cena i dodavatel byly zkopírováni do žádanky.  
6. Kliknutím na možnost **Workflow** otevřete dialogové okno.
7. Zvolte Dokončeno.
8. Vyberte stránku.
9. Zvolte Dokončeno.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]