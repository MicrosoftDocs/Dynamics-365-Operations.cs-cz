---
title: Delegování pracovních položek ve workflowu
description: Pokud plánujete být mimo kancelář nebo nemůžete reagovat na pracovní položku, můžete předat nebo znovu přiřadit své pracovní položky jinému uživateli.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f85a1318822ceaf829134bf2eb3581e350d5bea4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "346242"
---
# <a name="delegate-work-items-in-a-workflow"></a>Delegování pracovních položek ve workflowu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Pokud plánujete být mimo kancelář nebo nemůžete reagovat na pracovní položku, můžete předat nebo znovu přiřadit své pracovní položky jinému uživateli. Tento postup umožňuje konfiguraci systému pro automatické delegování vašich pracovních položek jinému uživateli.



K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="set-up-automatic-delegation"></a>Nastavení automatického předávání
1. Přejděte na Společné > Nastavení > Možnosti uživatelů.
2. Klikněte na kartu Workflow.
    * Ujistěte se, že je rozbalená část Delegování.    Chcete-li nakonfigurovat systém tak, aby automaticky delegoval vaše pracovní položky ostatním uživatelům, je nutné vytvořit pravidla delegování, která určí, kdy se budou delegovat určité typy pracovních položek. Při vytváření pravidla delegování postupujte takto:  
3. Klepněte na možnost Přidat.
4. Vyberte volbu v poli Rozsah.
    * Vše - Delegování všech pracovních položek, které máte přiřazeny.    Modul – Delegování pouze pracovních položek, které máte přiřazeny pro specifický typ workflowu. Pokud vyberete tuto možnost, je nutné vybrat typ workflowu v poli Název.    Workflow – Delegování pouze pracovních položek, které máte přiřazeny pro specifický workflow. Pokud vyberete tuto možnost, je nutné vybrat workflow v poli Název.  
5. V poli Delegovat vyberte uživatele, kterému chcete pracovní položku delegovat.
    * Použijte pole Počáteční datum a čas a Koncové datum a čas k určení, kdy mají být pracovní položky automaticky delegovány.  
6. Do pole Počáteční datum a čas zadejte datum a čas.
7. Do pole Koncové datum a čas zadejte datum a čas.
8. Zaškrtnutím políčka Povoleno můžete aktivovat pravidlo delegování.
    * Pokud jste vybrali Modul jako Rozsah, je nutné v poli Název vybrat modul.    Pokud jste vybrali Workflow jako Rozsah, je nutné v poli Název vybrat specifické workflow k delegování.  
9. Do pole Komentář zadejte komentář s vysvětlením, proč delegujete pracovní položky.

