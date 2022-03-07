---
title: Použití pracovního postupu ke správě informací o zaměstnanci
description: Toto téma vysvětluje, jak můžete použít funkci workflow ke správě informací o zaměstnancích.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d80ed49a4f423179997ac35562284a4e28af803f
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068078"
---
# <a name="use-workflows-to-manage-employee-information"></a>Použití pracovního postupu ke správě informací o zaměstnanci


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma vysvětluje, jak můžete použít funkci workflowu pro lidské zdroje ke správě informací o zaměstnancích. Například můžete přidružit workflow k pozici a konfigurovat workflow pro schválení, který se zahájí, když zaměstnanec změní svůj záznam.

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
Workflow lze přidružit k jakékoli hierarchii, kterou konfigurujete. Pokud je například pozice přidružena k hierarchii vykazování matice, můžete nakonfigurovat workflow, který směruje výdaje pro konkrétní projekt na vedoucího projektu místo vedoucího zaměstnance, který je přidružen k této pozici. Chcete-li vytvořit nový workflow nebo změnit existující workflow, na stránce **Workflowy lidských zdrojů** vyberte **Nový**. Vyberte workflow v seznamu, čímž otevřete Návrháře workflowů. Návrháře můžete použít k vytvoření nového workflowu nebo změně kroků existujícího workflowu. Když změníte existující workflow, změny jsou uloženy do nové verze. Proto se můžete vždy vrátit zpět k předchozí verzi, pokud bude třeba.

## <a name="configure-a-human-resources-workflow"></a>Konfigurace workflowu lidských zdrojů
Chcete-li konfigurovat základní workflow, který je spuštěn, když zaměstnanci požadují změny v jejich osobní identifikaci, postupujte takto.

1.  Na stránce **Workflowy lidských zdrojů** vyberte **Nové**.
2.  V seznamu dostupných workflowů vyberte **Identifikační čísla**.
3.  Vyberte **Spustit** a otevřete Návrháře workflowů. Potom na výzvu zadejte uživatelské jméno a heslo.
4.  Přetáhněte prvek **Schválit identifikační číslo** ze seznamu prvků workflowu na plátno návrháře.
5.  Připojte prvek schválení k položkám **Začátek** a **Konec**.
6.  Dvakrát klepněte (nebo dvakrát klikněte) na **Schválit prvek**, vyberte a podržte (nebo klikněte pravým tlačítkem) a poté vyberte **Vlastnosti**.
7.  Postupujte podle těchto kroků a přidejte pokyny pro pracovní položku:

    1.  Vyberte **Přiřazení** a potom vyberte **Hierarchie** pro typ přiřazení.
    2.  Pod výběrem **Hierarchie** vyberte **Konfigurovatelná hierarchie**.
    3.  Přidejte podmínku ukončení a zavřete stránku.

8.  Dokončete všechny další pokyny (neměly by existovat žádná další upozornění).
9.  Zvolte **Uložit a zavřít**. Aktivujte nový workflow, když se otevře dialogové okno, a vyberte **Aktivovat**.
10. Přejděte to nabídky **Lidské zdroje** &gt; **Pozice** &gt; **Typy hierarchií pozic**.
11. Vyberte **Matice**.
12. Přidejte na seznam položku **Identifikační číslo pracovníka**.

## <a name="additional-resources"></a>Další prostředky

[Zobrazení a správa změn adres](hr-personnel-view-address-changes.md) 





[!INCLUDE[footer-include](../includes/footer-banner.md)]
