---
title: Nemůžete najít rozevírací dialogové okno „Workflow“ pro deníky zásob
description: Nemůžete najít rozevírací dialogové okno Workflow na stránce deníku nebo související operace pracovního postupu nejsou k dispozici.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b2772a75c2388f4d78a459f9dfb72ad7c1be4ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475778"
---
# <a name="you-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Nemůžete najít rozevírací dialogové okno „Workflow“ pro deníky zásob

## <a name="symptoms"></a>Příznaky

Nemůžete najít rozevírací dialogové okno **Workflow** na stránce deníku nebo související operace pracovního postupu nejsou k dispozici.

K tomuto problému může dojít ze tří důvodů, jak je popsáno v následujících sekcích.

## <a name="resolution-1"></a>Řešení 1

Pokud se problém týká všech uživatelů, může docházet k tomu, že pracovnímu postupu schválení nebyl přiřazen název deníku. Chcete-li opravit problém, postupujte následovně.

1. Přejděte na **Řízení zásob &gt; Nastavení &gt; Názvy deníků &gt; Zásoby**.
1. V podokně seznamu vyberte ze sloupce seznamu název deníku.
1. Na pevné záložce **Obecné** nastavte možnost **workflow schválení** na *Ano*. Vyberte **Ano** po zobrazení výzvy k potvrzení změny.
1. V poli **Workflow** vyberte workflow, který chcete použít pro vybraný název deníku.

## <a name="resolution-2"></a>Řešení 2

Pokud váš pracovní postup používá přizpůsobený kód, po upgradu systému mohou nastat problémy. Například ve workflowu deníku může být tlačítko **Odeslat** šedé, takže jej nemůžete vybrat, chcete-li schválit odeslání.

Pokud je tlačítko **Odeslat** šedé, váš pracovní postup mohl být přizpůsoben, což znamená, že metoda workflowu `canSubmitToWorkflow()` v `FormDataUtil` byla rozšířena. Chcete-li tento problém vyřešit, změňte způsob, jakým rozšiřujete metodu `canSubmitToWorkflow()` k použití struktury v následujícím příkladu.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

## <a name="resolution-3"></a>Řešení 3

Pokud se problém týká pouze několika konkrétních uživatelů, nemusí mít tito uživatelé oprávnění zabezpečení, která jsou vyžadována ke spuštění operací pracovního postupu v denících zásob. Ověřte, že každý ovlivněný uživatel má bezpečnostní oprávnění *Udržovat pracovní postup deníku zásob*. Ve výchozím nastavení je toto oprávnění přiřazeno k povinnosti, která má stejný název, a tato povinnost je aplikována na roli *Skladník* a *Manažer skladu*.
