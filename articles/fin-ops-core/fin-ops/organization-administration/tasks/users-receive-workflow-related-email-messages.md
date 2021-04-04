---
title: Umožňuje uživatelům dostávat e-mailové zprávy týkající se workflowu
description: Systém můžete konfigurovat na zaslání e-mailových zpráv uživatelům, když nastanou události týkající se workflowu.
author: jasongre
manager: AnnBe
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a81e01c36081ce7131ee65344f583755fa3bfd3
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564183"
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

> [!NOTE]
> Šablony e-mailů pracovního postupu budou získány buď ze systémových e-mailových šablon nebo e-mailových šablon organizace v závislosti na tom, zda je pracovní postup pracovním postupem na úrovni systému (nikoli společnosti) nebo na úrovni organizace (specifický pro společnost).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]