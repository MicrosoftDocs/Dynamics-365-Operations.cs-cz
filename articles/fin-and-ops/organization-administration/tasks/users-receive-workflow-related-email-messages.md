--- 
title: "Konfigurace systému pro odeslání e-mailů souvisejících s workflow uživatelům"
description: "Systém můžete konfigurovat na zaslání e-mailových zpráv uživatelům, když nastanou události týkající se workflowu."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 04d90c9ded1ba7fb1ceac4ff1d54f54f6c43f9e9
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="configure-the-system-to-send-workflow-related-email-to-users"></a>Konfigurace systému pro odeslání e-mailů souvisejících s workflow uživatelům

[!include [task guide banner](../../includes/task-guide-banner.md)]

Systém můžete konfigurovat na zaslání e-mailových zpráv uživatelům, když nastanou události týkající se workflowu. Například je možné zaslat e-mailové zprávy uživatelům, když jim jsou přiřazeny dokumenty ke schválení. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.

1. Přejděte do nabídky Správa systému > Uživatelé > Uživatelé.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na Možnosti uživatelů.
4. Klikněte na kartu Workflow.
    * Ujistěte se, že je rozbalená část Oznámení.     V části Oznámení můžete určit, jakým způsobem má uživatel dostávat oznámení o události týkající se workflowu.  
5. V poli Typ oznámení workflowu položky řádku zvolte možnost.
    * Seskupená – Oznámení pro položky řádku jsou seskupena do jedné e-mailové zprávy.    Individuální – E-mailová zpráva je odeslána pro každou položku řádku.  
    * Pokud chcete, aby uživatelé dostávali upozornění v klientovi, zaškrtněte políčko Odesílat oznámení e-mailem.  
6. Klikněte na položku Uložit.
7. Zavřete stránku.


