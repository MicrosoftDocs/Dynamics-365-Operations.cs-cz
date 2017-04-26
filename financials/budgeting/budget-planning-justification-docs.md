---
title: "Doklady plánování rozpočtu"
description: "Doklady poskytují komentáře pro osoby požadující rozpočtu k vysvětlení, proč je nezbytná konkrétní rozpočet."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: c86d01fec3d8d7c210c7e73a034f4e9e384a0dcf
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-justification-documents"></a>Doklady plánování rozpočtu

[!include[banner](../includes/banner.md)]


Doklady poskytují komentáře pro osoby požadující rozpočtu k vysvětlení, proč je nezbytná konkrétní rozpočet. 

Šablony plánu rozpočtu je vytvořen správcem rozpočtu v aplikaci Microsoft Word a přiřazené k aktuální proces plánování rozpočtu. Vlastníci rozpočtu můžete potom otevřete šablonu a dat v aplikaci Word automaticky naplněna na jejich žádost rozpočtu základě. Poté se můžete přidat další text nebo data před uložením a upevnění dokument jejich individuální odůvodnění k jejich plánu rozpočtu.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Nastavit Microsoft Dynamics Office Add-in pro aplikaci Microsoft Word

1.  Otevřete nový dokument Microsoft Word.
2.  Klepněte na tlačítko **vložit** na pásu karet a klepněte na **obchodu**.
3.  Vyhledat Microsoft Dynamics Office Add-in a klepněte na tlačítko **přidat**.
4.  V aplikaci Word, klepněte v pravém podokně **přidat informace o serveru**.
5.  Zadejte nebo vložte adresu URL serveru a klepněte na tlačítko **OK**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Definovat šablony zdůvodnění v aplikaci Microsoft Word

1.  Klepněte na tlačítko **návrh** Microsoft Dynamics Office přidat-in po jste přihlášeni.
2.  Informace záhlaví použít **přidání polí** tlačítko.
3.  Vyberte zdroj dat entity BudgetPlanJustification a na **Další**. **Poznámka:** je vyžadována pro každý dokument odůvodnění této entity. Ostatní entity lze použít, ale odeslání 365 Microsoft Dynamics pro operace se nezdaří, pokud není součástí této entity.
4.  Přidáte BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter a DocumentNumber popisky a hodnoty v dokumentu aplikace Word. **Poznámka:** v případě potřeby můžete použít vlastní štítky, spíše než standardní popisky.
5.  Klepněte na **v** na dokončení části záhlaví.
6.  Úroveň podrobnosti řádku částek plánu rozpočtu, klepněte na tlačítko **tabulky přidat**.
7.  Znovu, vyberte zdroj dat entity BudgetPlanJustification a na **Další**.
8.  Přidejte pole pro EffectiveDate, ScenarioName, AccountDisplayValue a AccountingCurrencyExpenseAmount. **Poznámka:** jsou k dispozici přidat do řádků plánu rozpočtu jednotlivé komentáře, ty mohou být přidány do tabulky zde.
9.  Přidání doplňujících pokynů poskytnout koncovému uživateli a provádět jakékoli nezbytné formátování nebo styl v dokumentu.
10. Uložení dokumentu do místního počítače a zavřete soubor před pokračováním.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Použití šablony zdůvodnění nastavit proces plánování rozpočtu

1.  V Microsoft Dynamics 365 pro operace, přejděte na **rozpočtování**&gt;**nastavení**&gt;**plánování rozpočtu**&gt;**šablony zdůvodnění**.
2.  Klepněte na tlačítko **nové** a přejděte do nově vytvořeného dokumentu aplikace Microsoft Word.
3.  Zadejte zobrazovaný název šablony a popis. Click **OK**.
4.  Přejít na **rozpočtování**&gt;**nastavení**&gt;**rozpočtu****plánování**&gt;**procesu plánování rozpočtu**.
5.  Vyberte proces, kde by měla být použita šablona odůvodnění a klepněte na tlačítko **úprava**.
6.  V **šablonu dokumentu odůvodnění** pole, vyberte odpovídající šablonu a uložit.

##### <a name="edit-and-save-personalized-justification-documents"></a>Upravit a uložit dokumenty individuální odůvodnění.

1.  V 365 Dynamics pro operace vytvoření nového plánu rozpočtu nebo otevřete existující plán rozpočtu.
2.  V **zdůvodnění** rozevírací nabídky vyberte **vytvořit nové zdůvodnění**.
3.  Po vyplnění podrobností, vyberte Uložit individuální dokument z **zdůvodnění** rozevírací nabídky.





