---
title: Nastavení kódů důvodů
description: Aplikace Dynamics 365 Human Resources používá kódy důvodu k vysvětlení důvodu změny zaměstnaneckých výhod.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5bcfa60349d6d362504184dd90cc97ea27e8ba43
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689515"
---
# <a name="set-up-reason-codes"></a>Nastavení kódů důvodů


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Aplikace Dynamics 365 Human Resources používá kódy důvodu k vysvětlení důvodu změny zaměstnaneckých výhod.

> [!NOTE]
> Od ledna 2021 byly kódy důvodu migrovány do pracovního prostoru **Správa zaměstnanců** místo pracovního prostoru **Správa zaměstnaneckých výhod**. Další informace viz [Ruční migrace kódů důvodů do Správy zaměstnanců](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).

## <a name="create-reason-codes"></a>Vytvoření kódů rozhodnutí

1. V pracovním prostoru **Správa zaměstnanců** (nebo pracovním prostoru **Správa zaměstnaneckých výhod**, pokud vaše kódy důvodu nebyly ještě migrovány) vyberte **Odkazy** a potom vyberte **Kódy důvodů**.

2. Zvolte **Nové**.

3. Zadejte hodnoty pro zbývající pole:

   | Pole | Popis |
   | --- | --- |
   | **Kód důvodu** | Jedinečný název pro identifikaci důvodu, kdy zaměstnanec změnil zápis plánu zaměstnaneckých výhod. |
   | **Popis** | Popis kódu důvodu. |

4. V **Použitelné scénáře** nastavte **Správa zaměstnaneckých výhod** na **Ano**. (Nepoužije se, pokud vaše kódy důvodu dosud nebyly migrovány do pracovního prostoru **Správa zaměstnanců**.)

5. Zvolte možnost **Uložit**.

## <a name="manually-migrate-reason-codes-to-personnel-management"></a>Ruční migrace kódů důvodů do Správy zaměstnanců

V lednu 2021 byly kódy důvodu migrovány do pracovního prostoru **Správa zaměstnanců** místo pracovního prostoru **Správa zaměstnaneckých výhod**. Data kódu většiny důvodů se automaticky přenesou do vašeho prostředí. Některá data kódů důvodu nemusí migrovat. Například kódy důvodu mají nyní maximálně 15 znaků, takže jakékoli kódy příčiny delší než 15 znaků nebudou migrovány automaticky.

Uvidíte banner na stránce **Odkazy** pracovního prostoru **Správa zaměstnaneckých výhod**, který vás informuje o migraci a o tom, zda kódy důvodu neprovedly migraci.

1. Vyberte **Kódy důvodů** pro podrobnosti o stavu migrace.

   [![Kódy důvodu.](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)

2. Vyberte kód důvodu, který se nepodařilo migrovat.

   [![Stav migrace kódu důvodu.](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)

3. Vyberte **Migrujte kód důvodu**.

   [![Migrovat kód důvodu.](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)

4. V podokně **Migrace kódu důvodu zaměstnaneckých výhod** máte dvě možnosti pro mapování na kód důvodu Správy zaměstnanců:

   - Chcete-li ve správě zaměstnanců použít existující kód důvodu, vyberte jeden důvod v rozbalovací nabídce **Použít stávající kód důvodu**.
     > [!NOTE]
     > Existující kód důvodu můžete použít ve správě zaměstnanců pouze v případě, že na něj již jiný kód důvodu správy výhod nebyl migrován.
   - Chcete-li ve správě zaměstnanců vytvořit nový kód důvodu, zadejte nový v **Nový kód důvodu** a poté zadejte popis do **Nový popis**.

   [![Namapujte na kód důvodu správy zaměstnanců.](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)

Po migraci kódů důvodu na správu zaměstnanců je možnost jejich použití ve správě zaměstnaneckých výhod automaticky nastavena na **Ano**.

[![Použít ód důvodu ve správě zaměstnaneckých výhod.](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
