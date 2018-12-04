---
title: "Dokumenty odůvodnění plánování budgetu"
description: "Dokumenty odůvodnění poskytují komentáře pro osoby požadující rozpočet k vysvětlení, proč je konkrétní rozpočet nezbytný."
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: c4ac839e69440c8d3f1e86007a074999189e391d
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---

# <a name="budget-planning-justification-documents"></a>Dokumenty odůvodnění plánování budgetu

[!include [banner](../includes/banner.md)]

Dokumenty odůvodnění poskytují komentáře pro osoby požadující rozpočet k vysvětlení, proč je konkrétní rozpočet nezbytný. 

Šablona plánu rozpočtu se vytváří správcem rozpočtu v aplikaci Microsoft Word a přiřazuje se k aktuálnímu procesu plánování rozpočtu. Vlastníci rozpočtu mohou potom otevřít šablonu a data v aplikaci Word se automaticky vyplní na základě jejich žádosti o rozpočet. Mohou poté přidat další text nebo data před uložením a přiložením svého přizpůsobeného dokumentu odůvodnění k plánu rozpočtu.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Nastavení doplňku Microsoft Dynamics Office pro Microsoft Word

1.  Otevřete nový dokument aplikace Microsoft Word.
2.  Klikněte na tlačítko **Vložit** na pásu karet a klikněte na **Obchod**.
3.  Vyhledejte doplněk Microsoft Dynamics Office a klikněte na tlačítko **Přidat**.
4.  V aplikaci Word klikněte v pravém podokně na možnost **Přidat informace serveru**.
5.  Zadejte nebo vložte adresu URL serveru a klikněte na tlačítko **OK**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Definování šablony odůvodnění v aplikaci Microsoft Word

1.  Klikněte na tlačítko **Návrh** v doplňku Microsoft Dynamics Office poté, co se přihlásíte.
2.  Pro informace záhlaví použijte tlačítko **Přidat pole**.
3.  Vyberte zdroj dat entity BudgetPlanJustification a klikněte na **Další**. **Poznámka:** Tato entita je vyžadována pro každý dokument odůvodnění. Ostatní entity lze použít, ale odeslání zpět do aplikace Microsoft Dynamics 365 for Finance and Operations se nezdaří, pokud není tato entita zahrnuta.
4.  Přidejte popisky BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter a DocumentNumber do dokumentu aplikace Word. **Poznámka:** V případě potřeby můžete použít vlastní popisky, spíše než standardní popisky.
5.  Klikněte na **Hotovo** pro dokončení části záhlaví.
6.  Pro získání podrobností o částkách plánu rozpočtu na úrovni řádků klikněte na tlačítko **Přidat tabulku**.
7.  Znovu vyberte zdroj dat entity BudgetPlanJustification a klikněte na **Další**.
8.  Přidejte pole pro EffectiveDate, ScenarioName, AccountDisplayValue a AccountingCurrencyExpenseAmount. **Poznámka:** Jsou-li k dispozici komentáře k přidání do jednotlivých řádků plánu rozpočtu, můžete je přidat do tabulky zde.
9.  Přidejte jakékoliv doplňující pokyny pro koncového uživatele a proveďte jakékoli nezbytné formátování nebo úpravu stylů v dokumentu.
10. Než budete pokračovat, uložte dokument do místního počítače a zavřete soubor.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Nastavení procesu plánování rozpočtu pro použití šablony odůvodnění

1.  V aplikaci Finance and Operations přejděte na **Rozpočtování** &gt; **Nastavení** &gt; **Plánování rozpočtu** &gt; **Šablony dokumentů odůvodnění**.
2.  Klikněte na tlačítko **Nový** a přejděte do nově vytvořeného dokumentu aplikace Microsoft Word.
3.  Zadejte název a popis zobrazení šablony. Klikněte na tlačítko **OK**.
4.  Přejděte do **Rozpočtování** &gt; **Nastavení** &gt; **Plánování** **rozpočtu** &gt; **Proces plánování rozpočtu**.
5.  Vyberte proces, kde by měla být použita šablona odůvodnění, a klikněte na tlačítko **Upravit**.
6.  V poli **Šablona dokumentu odůvodnění** vyberte odpovídající šablonu a uložte ji.

##### <a name="edit-and-save-personalized-justification-documents"></a>Upravte a uložte přizpůsobené dokumenty odůvodnění.

1.  V aplikaci Finance and Operations vytvořte nový plán rozpočtu nebo otevřete existující plán rozpočtu.
2.  V rozevírací nabídce **Odůvodnění** vyberte **Vytvořit nové odůvodnění**.
3.  Po vyplnění podrobností vyberte z rozevírací nabídky **Odůvodnění** možnost odeslání přizpůsobeného dokumentu.





