---
title: Použití pracovního postupu ke správě informací o zaměstnanci
description: Tento článek vysvětluje, jak můžete použít funkci workflow ke správě informací o zaměstnancích.
author: twheeloc
ms.date: 11/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: dbbbb0ee807cb65fa4f4f9a29cc4a2b6b045b08c
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750727"
---
# <a name="use-workflows-to-manage-employee-information"></a>Použití pracovního postupu ke správě informací o zaměstnanci

[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek vysvětluje, jak můžete použít funkci workflowu pro lidské zdroje ke správě informací o zaměstnancích. Například můžete přidružit workflow k pozici a konfigurovat workflow pro schválení, který se zahájí, když zaměstnanec změní svůj záznam.

Funkce workflowu pro lidské zdroje obsahuje velký počet workflowů pro správu aktivit lidských zdrojů. Navíc jsou k dispozici četné možnosti, abyste mohli upravit konkrétní workflowy a přidružit je k hierarchii vykazování. Workflowy pomáhají při správě změn ve více typech informací o zaměstnancích. Workflow je možné přidružit k pozici. Pokud poté zaměstnanci změní svůj záznam zaměstnance, zahájí se workflow, který vyžaduje schválení před uložením nových informací. Workflowy jsou předem definované pro následující typy informací, které vám pomohou efektivně spravovat změny a zachovat přesnost dat zaměstnanců:

-   Identifikační čísla
-   Kurzy
-   Vzdělání
-   Obrázek
-   Zapůjčené položky
-   Odborné zkušenosti
-   Zkušenost z projektu
-   Dovednosti
-   Pozice důvěry
-   Akce lidských zdrojů
-   Registrace do kurzu

Když jsou zaměstnanci přijati, převedeni nebo ukončeni, workflow může zahrnovat proces přezkoumání. Tímto způsobem může být přezkoumán dokument nebo lze definovat podmínky akce jako součást workflowu. Po dokončení procesu přezkoumání se dokončí dokument nebo akce a workflow přejde ke kroku pro konečné schválení.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Přidružení workflowu k hierarchii pozic

Workflow lze přidružit k jakékoli hierarchii pozic, kterou konfigurujete. Pro směrování pracovního postupu se používají dva typy hierarchií: **Manažerská** a **Konfigurovatelná**.

- **Manažerská** hierarchie představuje strukturu výkaznictví společnosti nebo organizace. Další informace o tomto typu hierarchie viz [Podřízený pozice](hr-personnel-positions.md#reports-to-position).
- **Konfigurovatelná** hierarchie představuje matici nebo vlastní hierarchii. Další informace o tomto typu hierarchie viz [Vztahy](hr-personnel-positions.md#relationships).

### <a name="managerial-hierarchy-example"></a>Příklad manažerské hierarchii

Pracovní postup můžete nakonfigurovat tak, aby když zaměstnanec odešle požadavek na nákup nového počítače, byl požadavek směrován k manažerovi zaměstnance a manažerovi na úrovni přeskakování. Když konfigurujete krok pracovního postupu, nastavte pole **Typ přiřazení** na **Hierarchie**. Karta **Typ hierarchie** se poté zpřístupní. V tomto příkladu vyberte **Manažerskou** hierarchii.

### <a name="configurable-hierarchy-example"></a>Příklad konfigurovatelné hierarchie

Pokud je pozice přidružena k hierarchii vykazování matice, můžete nakonfigurovat workflow, který směruje výdaje pro konkrétní projekt na vedoucího projektu místo vedoucího zaměstnance. V tomto případě nastavte **Typ přířazení** na **Hierarchie**. Pak na kartě **Typ hierarchie** vyberte **Konfigurovatelnou** hierarchii. Po nastavení pracovního postupu vyberte **Přidružit** hierarchii na stránce **Nastavení pracovního postupu** pro výběr hierarchie, která by měla být použita pro směrování pracovního postupu.

> [!IMPORTANT]
> Když je dokument, transakce nebo kmenový záznam odeslán ke schválení pracovního postupu, použije se primární pozice předkladatele k určení, komu by měl být dokument směrován jako další.

### <a name="hierarchy-setting-in-workflow-parameters"></a>Nastavení hierarchie v parametrech Workflow

1. Na stránce **Parametry pracovního postupu** přejděte na **Hierarchické směrování**.
2. Ve výchozím nastavení je volba **Použit hierarchii pozic** nastavena na **Ne**. V tomto případě bude pracovní postup při navigaci v hierarchii používat primární pozici pracovníka. Nastavte možnost na **Ano**, aby pracovní postup při navigaci v hierarchii používal nadřazený prvek pozice.

### <a name="additional-example"></a>Další příklad 

Zaměstnanec Grace Sturman má dvě pozice: konzultant a trenér. Primární pozice Grace je trenér. Když nezaškoluje nové zaměstnance, je k dispozici pro poradenskou činnost. Prostřednictvím své primární pozice je Grace podřízena Claire, ředitelce lidských zdrojů. Claire je podřízená Charliemu. Pro svou pozici konzultanta má Grace několik vztahů s tečkovanou čárou v závislosti na projektu.

Společnost Grace vytváří pravidla směrování pracovních postupů, která jsou založena na **Konfigurovatelné** hierarchii (maticové/projektové hierarchie). Tato hierarchie využívá pozici poradce Grace. Pokud je možnost **Použijte hierarchii pozic** nastavena na **Ne**, když je dokument směrován ke schválení Grace, pracovní postup se podívá na její primární pozici (školitele), aby určil, kam by měl být dokument směrován jako další. V tomto případě bude směrována nejprve ke Claire a poté k Charliemu. Pokud je možnost nastavena na **Ano** a pracovní postup používá **Konfigurovatelnou** hierarchii, bude pracovní postup zkoumat pozici konzultanta Grace a vztah podřízenosti, aby určil, kam by měl být dokument dále směrován.

### <a name="configure-a-human-resources-workflow"></a>Konfigurace workflowu lidských zdrojů
Chcete-li konfigurovat základní workflow, který je spuštěn, když zaměstnanci požadují změny v jejich osobní identifikaci, postupujte takto.

1.  Na stránce **Workflowy lidských zdrojů** vyberte **Nové**.
2.  V seznamu dostupných workflowů vyberte **Identifikační čísla**.
3.  Vyberte **Spustit** a otevřete Návrháře workflowů. Potom zadejte uživatelské jméno a heslo.
4.  Přesuňte prvek **Schválit identifikační číslo** ze seznamu prvků workflowu na plátno návrháře.
5.  Připojte prvek schválení k položkám **Začátek** a **Konec**.
6.  Dvakrát klepněte (nebo dvakrát klikněte) na **Schválit prvek**, vyberte a podržte (nebo klikněte pravým tlačítkem) a poté vyberte **Vlastnosti**.
7.  Postupujte podle těchto kroků a přidejte pokyny pro pracovní položku:

    1.  Vyberte **Přiřazení** a potom vyberte **Hierarchie** pro typ přiřazení.
    2.  Pod výběrem **Hierarchie** vyberte **Konfigurovatelná hierarchie**.
    3.  Přidejte podmínku ukončení a zavřete stránku.

8.  Proveďte další pokyny.
9.  Zvolte **Uložit a zavřít**. Aktivujte nový workflow, když se otevře dialogové okno, a vyberte **Aktivovat**.
10. Přejděte to nabídky **Lidské zdroje** &gt; **Pozice** &gt; **Typy hierarchií pozic**.
11. Vyberte **Matice**.
12. Přidejte na seznam položku **Identifikační číslo pracovníka**.

## <a name="additional-resources"></a>Další prostředky

[Zobrazení a správa změn adres](hr-personnel-view-address-changes.md) 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
