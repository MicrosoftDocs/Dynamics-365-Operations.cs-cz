---
title: "Vytvořit workflow"
description: "Tato témata vysvětluje postup při vytváření workflowu."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: b4d4f14753f1755c251e1ae12dd9addec31d2fdd
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="create-a-workflow"></a>Vytvořit workflow

[!include[banner](../includes/banner.md)]


Tato témata vysvětluje postup při vytváření workflowu.

<a name="open-the-workflow-editor"></a>Otevřete editor workflowu
------------------------

Modul aplikace Microsoft Dynamics 365 for Operations, ve kterém pracujete, určuje typy workflowu, které můžete vytvořit. Podle následujících kroků vyberte typ workflowu k vytvoření a otevření editoru workflowu.

1.  Otevřete modul, pro který chcete vytvořit nový workflow. Když například chcete vytvořit workflow pro nákupní žádanky, klepněte na **Zásobování a zdroje**.
2.  Klikněte na **Nastavení** &gt; **\[Název modulu\] workflowy**.
3.  Na stránce seznamu, která se zobrazí, v podokně akcí klikněte na kartu klikněte na **Nový**.
4.  Na stránce **Vytvořit workflow** vyberte typ workflowu, který chcete vytvořit, a klepněte na tlačítko **Vytvořit workflow**. Otevře se editor workflowu. Při navrhování workflowu postupujte následujícím způsobem.

## <a name="drag-workflow-elements-onto-the-canvas"></a>Přetáhněte prvky workflowu na plátno
Oblast **Prvky workflowu** editoru workflowu obsahuje prvky, které můžete přiřadit k workflowu. Prvky do workflowu přidáte tak, že je přetáhnete na plátno.

## <a name="connect-the-elements"></a>Připojení prvků
Jeden prvek workflowu k jinému připojíte podržením ukazatele nad prvkem, dokud se neobjeví spojovací body. Klikněte na spojovací bod a přetáhněte jej na jiný prvek. Nezapomeňte spojit všechny prvky.

## <a name="configure-the-properties-of-the-workflow"></a>Konfigurace vlastností workflowu
Nakonfigurujte vlastnosti workflowu pomocí následujících kroků.

1.  Klepnutím na plátno se ujistěte, že není vybrán žádný prvek workflowu.
2.  Kliknutím na **Vlastnosti** otevřete formulář **Vlastnosti** pro workflow.
3.  Postupujte podle pokynů v tématu [Konfigurace vlastností workflowu](configure-workflow-properties.md).

## <a name="configure-the-elements-of-the-workflow"></a>Konfigurace prvků workflowu
Nakonfigurujte každý prvek, který jste přetáhli na plátno. Další informace o konfiguraci jednotlivých prvků workflowu naleznete v následujících tématech:

-   [Konfigurace ručního úkolu](configure-manual-task-workflow.md)
-   [Konfigurace automatizované úlohy](configure-automated-task-workflow.md)
-   [Konfigurace procesu schválení](configure-approval-process-workflow.md)
-   [Konfigurace kroku schválení](configure-approval-step-workflow.md)
-   [Konfigurace ručního rozhodnutí](configure-manual-decision-workflow.md)
-   [Konfigurace podmíněného rozhodnutí](configure-conditional-decision-workflow.md)
-   [Konfigurace paralelní aktivity](configure-parallel-activity-workflow.md)
-   [Konfigurace paralelní větve](configure-parallel-branch-workflow.md)
-   [Konfigurace workflow položky řádku](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Vyřešení chyb nebo varování
Podokno **Chyby a varování** v dolní části editoru workflowu zobrazuje zprávy, které byly vygenerovány pro workflow. Pokud chcete vyhledat prvek, kde došlo k chybě nebo upozornění, poklepejte na chybu nebo upozornění. Předtím, než je možné aktivovat workflow, musí být vyřešeny všechny chyby a upozornění.

## <a name="save-and-activate-the-workflow"></a>Uložení a aktivace workflowu
Až budete připraveni uložit a aktivovat workflow, postupujte následovně.

1.  Kliknutím na tlačítko **Uložit a zavřít** zavřete editor workflowu a otevřete formulář **Uložit workflow**.
2.  Zadejte komentáře ke změnám provedeným v daném workflowu a potom klikněte na **OK**.
3.  Pokud byly vyřešeny všechny chyby a upozornění, zobrazí se stránka **Aktivovat workflow**. Vyberte některou z následujících možností:
    -   Pokud chcete aktivovat tuto verzi workflowu, klepněte na tlačítko **Aktivovat novou verzi**. Když je workflow aktivní, uživatelé do něj mohou odesílat dokumenty ke zpracování a schválení.
    -   Pokud nechcete tuto verzi aktivovat, klepněte na tlačítko **Neaktivovat novou verzi**. Workflow můžete aktivovat později.






