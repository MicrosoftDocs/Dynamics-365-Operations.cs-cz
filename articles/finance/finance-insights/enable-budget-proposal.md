---
title: Povolení návrhů rozpočtu (Preview)
description: Toto téma vysvětluje, jak zapnout funkci návrhu rozpočtu ve finančních přehledech.
author: ShivamPandey-msft
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7e90a1a2f2a8e7808f03ce9a6ee58c027bd48d8d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818697"
---
# <a name="enable-budget-proposals-preview"></a>Povolení návrhů rozpočtu (Preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Toto téma vysvětluje, jak zapnout funkci návrhu rozpočtu ve finančních přehledech.

1. Použijte informace ze stránky prostředí v Microsoft Dynamics Lifecycle Services (LCS) pro připojení k primární instanci Azure SQL pro dané prostředí. Spuštěním následujícího příkazu Transact-SQL (T-SQL) zapněte testování pro prostředí sandboxu. (Možná budete muset zapnout přístup ke své IP adrese v LCS, než se budete moci vzdáleně připojit k aplikačnímu objektovému serveru \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Pokud vaše nasazení Microsoft Dynamics 365 Finance je nasazení Service Fabric, můžete tento krok přeskočit. Tým finančních přehledů už měl testování zapnout za vás. Pokud nevidíte funkci v pracovním prostoru **Správa funkcí** nebo pokud se při pokusu o zapnutí setkáte s problémy, pošlete e-mail na adresu [Tým pro aplikaci Finanční přehledy (Preview)](mailto:fiap@microsoft.com).

2. Otevřete pracovní prostor **Správa funkcí** a postupujte takto:

    1. Vyberte možnost **Zkontrolovat aktualizace**.
    2. Vyhledejte **Návrh rozpočtu** a zapněte tuto funkci.

3. Jděte na **Rozpočtování \> Nastavení \> Základní rozpočtování \> Návrh rozpočtu (Preview)** a vyberte **Povolit funkci**.

#### <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů
Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb (SLA) pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]