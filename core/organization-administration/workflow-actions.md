---
title: Akce workflowu
description: "V tomto článku jsou vysvětleny akce, které může provést každý účastník v procesu schválení workflowu."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: adcb0443f5ad07ae7178e9fde963184951e6b8d9
ms.lasthandoff: 03/31/2017


---

# <a name="workflow-actions"></a>Akce workflowu

[!include[banner](../includes/banner.md)]


V tomto článku jsou vysvětleny akce, které může provést každý účastník v procesu schválení workflowu.

Workflow může zahrnovat několik skupin osob: původce, zmocněnci pro úkol, pracovníci s rozhodovací pravomocí a schvalovatelé. Například v následujícím workflowu k vyúčtování výdajů je Stanislav původcem, členové fronty jsou zmocněnci pro úkol, Jan je pracovníkem s rozhodovací pravomocí a František, Šárka a Anna jsou schvalovateli.   [![Pracovní postup\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif) v následujících částech akce pracovního postupu, které mohou provádět každé skupiny.

## <a name="actions-that-an-originator-can-perform"></a>Akce, které může provádět původce
Původce zahájí instanci workflowu odesláním dokumentu ke zpracování. Stanislav musí například odeslat vyúčtování výdajů kliknutím na tlačítko **Odeslat** na stránce **Vyúčtování výdajů**.

## <a name="actions-that-a-task-assignee-can-perform"></a>Akce, které může provádět zmocněnec
Úkol lze přiřadit více osobám nebo frontě pracovních položek, které jsou sledovány více osobami. Dokončit ji však může pouze jediná osoba. Stanislav například odeslal vyúčtování výdajů a nasměroval své příjemky do oddělení vyúčtování výdajů, aby je jeho pracovníci zkontrolovali. Členové oddělení vyúčtování výdajů společnosti Adventure Works sledují frontu. Júlie, která je členkou tohoto oddělení, přijala úkol kontroly Stanislavova vyúčtování výdajů a příjemek. Může nyní provést jednu z těchto akcí: dokončení, zamítnutí, delegování, žádost o změnu, změna přiřazení nebo uvolnění. **Poznámka:** Dostupné akce se budou lišit v závislosti na tom, jak vývojář softwaru úkol navrhnul.

### <a name="complete"></a>Dokončení

Když uživatel úkol dokončí, je dokument, který byl odeslán ke zpracování, přiřazen dalšímu uživateli ve workflowu (existuje-li takový uživatel). Není-li vyžadováno další zpracování, proces workflowu bude ukončen. V tomto příkladu Júlie, která je členkou tohoto oddělení, přijala úkol kontroly Stanislavova vyúčtování výdajů a příjemek. Jakmile Júlie dokončí kontrolu, je dokument přiřazen Janovi.

### <a name="reject"></a>Zamítnout

Když uživatel dokument zamítne, proces workflowu skončí. V tomto příkladu Júlie, která je členkou tohoto oddělení, přijala úkol kontroly Stanislavova vyúčtování výdajů a příjemek. Když Júlie vyúčtování výdajů odmítne, proces workflowu skončí. Stanislav může poté vyúčtování výdajů znovu odeslat. Nejprve může provést změny, anebo může znovu odeslat původní verzi. Jestliže Stanislav vyúčtování výdajů znovu odešle, začíná proces workflowu u úlohy ruční kontroly.

### <a name="delegate"></a>Delegovat

Když uživatel úkol deleguje, je úkole přiřazen jinému uživateli. V tomto příkladu Júlie, která je členkou tohoto oddělení, přijala úkol kontroly Stanislavova vyúčtování výdajů a příjemek. Júlie tento úkol deleguje na Teodora, který je jejím asistentem. Teodor poté jedná jménem Júlie. Jakmile tedy Teodor kontrolu dokončí, bude vyúčtování výdajů přiřazeno Janovi, jako kdyby úkol dokončila Júlie.

### <a name="request-change"></a>Požadavek na změnu

Když uživatel požaduje provedení změny v dokumentu, který byl odeslán, je dokument vrácen zpět původci. V tomto příkladu Júlie, která je členkou tohoto oddělení, přijala úkol kontroly Stanislavova vyúčtování výdajů a příjemek. Júlie si ve vyúčtování výdajů všimne několika chyb a požádá o změny. Vyúčtování výdajů se odešle zpět Stanislavovi. Stanislav může vyúčtování výdajů znovu odeslat. Nejprve může provést požadované změny, anebo může znovu odeslat původní verzi. Pokud Stanislav vyúčtování výdajů odešle znovu, je nutné, aby člen fronty pracovních položek znovu zkontroloval vyúčtování výdajů a příjemky.

### <a name="reassign"></a>Opětovné přiřazení

Členové fronty pracovních položek mohou dokumenty ve frontě přeřadit do jiné fronty. V tomto příkladu Júlie, která je členkou oddělení vyúčtování výdajů společnosti Adventure Works, sleduje frontu. Z důvodu vyrovnání pracovního vytížení může vyúčtování výdajů a příjemky, které jsou jeho součástí, přeřadit pro jiné fronty.

### <a name="release"></a>Uvolnit

V některých případech může člen fronty pracovních položek úkol přijmout, ale poté zjistit, že jej nemůže provést. V takovém případě může osoba, která úkol přijala, uvolnit dokument zpět do fronty pracovních položek. V tomto příkladu Júlie, která je členkou tohoto oddělení, přijala úkol kontroly Stanislavova vyúčtování výdajů a příjemek. Júlie se rozhodne, že nemůže úkol dokončit, a tak dokument uvolní. Vyúčtování výdajů je vráceno do fronty, takže ostatní členové oddělení vyúčtování nákladů společnosti Adventure Works mohou úkol provést.

## <a name="actions-that-a-decision-maker-can-perform"></a>Akce, které může provádět pracovník s rozhodovací pravomocí
Dokument bývá obvykle přiřazen pracovníkovi s rozhodovací pravomocí, protože vyvstala otázka, kterou musí rozhodnout pracovník s rozhodovací pravomocí. Na otázku se obvykle odpovídá možnostmi **Ano** nebo **Ne**, nebo **Pravda** nebo **Nepravda**. Pokud pracovník s rozhodovací pravomocí nevybere některou z těchto možností, může rozhodnutí delegovat.

### <a name="choice-1-or-choice-2"></a>\[Volba 1\] nebo \[volba 2\]

Pracovník s rozhodovací pravomocí musí odpovědět na otázku, která se vztahuje k dokumentu. Na otázku se obvykle odpovídá možnostmi **Ano** nebo **Ne**, nebo **Pravda** nebo **Nepravda**. Odpověď, kterou pracovník s rozhodovací pravomocí vybere, určuje větev workflowu, která bude použita ke zpracování dokumentu. Stanislavovo vyúčtování výdajů je například přiřazeno Janovi. Jan musí rozhodnout, zda informace v dokumentu vyžadují hovor se Stanislavovým nadřízeným. Když Jan rozhodne, že je hovor nutný, je vyúčtování výdajů přiřazeno Adéle, která pak musí zavolat nadřízenému Stanislava. Pokud Jan rozhodne, že hovor není třeba, vyúčtování výdajů je přiřazeno Františkovi ke schválení.

### <a name="delegate"></a>Delegovat

Když pracovník s rozhodovací pravomocí deleguje rozhodnutí, je dokument přiřazen jinému uživateli, který musí rozhodnutí učinit. Stanislavovo vyúčtování výdajů je například přiřazeno Janovi. Jan deleguje rozhodnutí Marii, která je jeho asistentkou. Marie poté jedná jménem Jana. Když Marie rozhodne, že je hovor se Stanislavovým nadřízeným nutný, je vyúčtování výdajů přiřazeno Adéle, která pak musí zavolat nadřízenému Stanislava. Pokud Marie rozhodne, že hovor není třeba, vyúčtování výdajů je přiřazeno Františkovi ke schválení.

## <a name="actions-that-an-approver-can-perform"></a>Akce, které může provádět schvalovatel
Jakmile je dokument přiřazen schvalovateli, může tento schvalovatel provést jednu z následujících akcí: schválení, zamítnutí, delegování nebo žádost o změnu.

### <a name="approve"></a>Schválení

Když schvalovatel dokument schválí, je dokument přiřazen dalšímu uživateli ve workflowu (existuje-li takový uživatel). Není-li vyžadováno další zpracování, proces workflowu bude ukončen. Stanislav například odeslal vyúčtování výdajů na 6 000 USD a tento dokument je přiřazen Františkovi. Když František dokument schválí, je přiřazen Šárce ke schválení. Když Šárka vyúčtování výdajů schválí, proces workflowu skončí.

### <a name="reject"></a>Zamítnout

Když schvalující dokument zamítne, proces workflowu končí. Stanislav například odeslal vyúčtování výdajů na 12 000 USD a tento dokument je přiřazen Šárce. Když Šárka vyúčtování výdajů zamítne, proces workflowu skončí. Stanislav může vyúčtování výdajů znovu odeslat. Nejprve může provést změny, anebo může znovu odeslat původní verzi vyúčtování výdajů. Pokud Stanislav vyúčtování výdajů znovu odešle, začíná proces workflowu od schvalovacího procesu.

### <a name="delegate"></a>Delegovat

Když schvalující dokument deleguje, je dokument postoupen ke schválení jinému uživateli. Stanislav například odeslal vyúčtování výdajů na 12 000 USD a tento dokument je přiřazen Františkovi. František deleguje vyúčtování výdajů na Annu. Anna bude potom jednat jménem Františka. To znamená, že když Anna dokument schválí, je dokument přiřazen Šárce ke schválení, jako kdyby ho schválil František. Jakmile Šárka dokument schválí, je odeslán Anně ke schválení.

### <a name="request-change"></a>Požadavek na změnu

Když schvalující požaduje provedení změny v dokumentu, je dokument odeslán zpět původci. Stanislav například odeslal vyúčtování výdajů na 12 000 USD a tento dokument je přiřazen Šárce. Pokud bude Šárka požadovat změnu, bude vyúčtování výdajů odesláno zpět Stanislavovi. Stanislav může vyúčtování výdajů znovu odeslat. Nejprve může provést požadované změny, anebo může znovu odeslat původní verzi vyúčtování výdajů. Jestliže Stanislav vyúčtování výdajů znovu odešle, je odesláno Františkovi ke schválení, protože František je prvním schvalovatelem v procesu schvalování.




