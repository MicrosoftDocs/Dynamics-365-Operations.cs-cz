---
title: Umožňuje uživatelům dostávat e-mailové zprávy týkající se workflowu
description: Systém můžete konfigurovat na zaslání e-mailových zpráv uživatelům, když nastanou události týkající se workflowu.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4c9f2f22bc4b5ca5b4351f7956ad2eb6d3b903d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140414"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>Umožňuje uživatelům dostávat e-mailové zprávy týkající se workflowu

[!include [banner](../../includes/banner.md)]

Systém můžete konfigurovat na zaslání e-mailových zpráv uživatelům, když nastanou události týkající se workflowu. Například je možné zaslat e-mailové zprávy uživatelům, když jim jsou přiřazeny dokumenty ke schválení. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.

1. Přejděte na **Navigační podokno > Moduly > Správa systému > Uživatelé > Uživatelé**.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. V **Podokně akcí** klikněte na možnost **Možnosti uživatele**.
4. Klikněte na kartu **Workflow**. Zkontrolujte, zda je rozbalen oddíl **Oznámení**. V části **Oznámení** můžete určit, jakým způsobem má uživatel dostávat oznámení o události týkající se workflowu.  
5. V poli **Typ oznámení workflowu položky řádku** zvolte možnost.
    - Seskupená – Oznámení pro položky řádku jsou seskupena do jedné e-mailové zprávy.
    - Individuální – E-mailová zpráva je odeslána pro každou položku řádku.  
    - Pokud chcete, aby uživatelé dostávali upozornění v klientovi, zaškrtněte políčko **Odesílat oznámení e-mailem**.  
6. Klikněte na možnost **Uložit**.
7. Zavřete stránku.

