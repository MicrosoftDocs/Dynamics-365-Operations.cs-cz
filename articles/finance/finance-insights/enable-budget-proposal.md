---
title: Povolení návrhů rozpočtu (Preview)
description: Toto téma vysvětluje, jak zapnout funkci návrhu rozpočtu ve finančních přehledech.
author: ShivamPandey-msft
ms.date: 07/16/2021
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
ms.openlocfilehash: cc7b06ee40553a254a939babc30e6f5c99f85507c1a3db4e916f480560cf8835
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768932"
---
# <a name="enable-budget-proposals-preview"></a>Povolení návrhů rozpočtu (Preview)

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak zapnout funkci návrhu rozpočtu ve finančních přehledech.

1. Použijte informace ze stránky prostředí v Microsoft Dynamics Lifecycle Services (LCS) pro připojení k primární instanci Azure SQL pro dané prostředí. Spuštěním následujícího příkazu Transact-SQL (T-SQL) zapněte testování pro prostředí sandboxu. (Možná budete muset zapnout přístup ke své IP adrese v LCS, než se budete moci vzdáleně připojit k aplikačnímu objektovému serveru \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Tento krok přeskočte, pokud používáte verzi 10.0.20 nebo novější nebo pokud používáte nasazení Service Fabric. Tým finančních přehledů už měl testování zapnout za vás. Pokud nevidíte funkci v pracovním prostoru **Správa funkcí** nebo pokud při pokusu o zapnutí dojde k potížím, kontaktujte <fiap@microsoft.com>.

2. Otevřete pracovní prostor **Správa funkcí** a postupujte takto:

    1. Vyberte možnost **Zkontrolovat aktualizace**.
    2. Vyhledejte **Návrh rozpočtu** a zapněte tuto funkci.

3. Jděte na **Rozpočtování \> Nastavení \> Základní rozpočtování \> Návrh rozpočtu (Preview)** a vyberte **Povolit funkci**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
