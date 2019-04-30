---
title: Delegování pracovních položek ve workflowu
description: Pokud plánujete být mimo kancelář nebo nemůžete reagovat na pracovní položku, můžete předat nebo znovu přiřadit své pracovní položky jinému uživateli.
author: jasongre
manager: AnnBe
ms.date: 04/09/2019
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
ms.openlocfilehash: feace647d7acef6abf86b13fcb8019c622c55ff6
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/12/2019
ms.locfileid: "976774"
---
# <a name="delegate-work-items-in-a-workflow"></a>Delegování položek práce ve workflow

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a>Ručně delegování pracovní položky

Pokud chcete delegovat oprávnění pro jednotlivé pracovní položky, vyberte možnost **Delegovat** v nabídce **Workflow** a zadejte uživatele k delegování a komentář. Tím bude pracovní položka znovu přiřazena danému uživateli, aby ji mohl dokončit.

## <a name="automatically-delegate-work-items"></a>Automatické delegování pracovních položek

Pokud plánujete absenci v kanceláři nebo nejste jinak schopní u pracovních položek nějakou dobu jednat, můžete automaticky delegovat nové pracovní položky na ostatní uživatele pomocí stránky **Uživatelské možnosti**.

### <a name="set-up-automatic-delegation"></a>Nastavení automatického předávání
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

