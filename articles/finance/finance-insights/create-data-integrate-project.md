---
title: Vytvořte projekt integrace dat
description: Toto téma vysvětluje, jak vytvořit projekt integrace dat.
author: ShivamPandey-msft
ms.date: 05/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4d69ffcb6ccfcc7bae2891f2539941f7b6bbf86e
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722876"
---
# <a name="create-a-data-integration-project"></a>Vytvořte projekt integrace dat

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit projekt integrace dat.

1. Přihlaste se do Microsoft Dynamics 365 Finance.
2. Přejděte na **Pracovní prostory \> Správa dat** a vyberte dlaždici **Datové entity**. Než přejdete k dalšímu kroku, počkejte, dokud se neobnoví všechny datové entity.
3. Otevřete [portál Power Apps](https://make.powerapps.com/) a postupujte takto:

    1. Vyberte příslušné prostředí.
    2. V levém navigačním podokně nalevo vyberte **Dataverse \> Připojení**.
    3. Připojte se k příslušným instancím následujících položek:

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

4. Otevřete [prostředí Power Apps](https://admin.powerapps.com/environments) a postupujte takto:

    1. Vyberte **Integraci dat**.
    2. Vyberte **Sady připojení**.
    3. Vyberte **Nová sada připojení**.
    4. Zadejte název připojení.
    5. Vyberte odpovídající připojení pro následující položky:

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

    6. Vyberte příslušné mapování organizace.
    7. Vyberte **Vytvořit**.

5. Otevřete [prostředí Power Apps](https://admin.powerapps.com/environments) a postupujte takto:  

    1. Vytvořte jeden projekt integrace dat pro každou z následujících šablon pomocí sady připojení, kterou jste právě vytvořili:

        - Výsledek přehledu plateb zákazníka (CDS do Fin and Ops 10.0.17+)
        - Výsledky časové řady cashflow (CDS do Fin and Ops)
        - Výsledky časové řady rozpočtu (CDS do Fin and Ops)

      > [!NOTE]
      > Vytvoření více projektů integrace dat pro každou šablonu může způsobit chyby, které zablokují aktualizace.

    2. Nastavte vhodné plánování pro každý projekt.

> [!NOTE]
> Pokud nevidíte požadované entity v Dataverse, přejděte na **Kredit a inkasa** > **Nastavení** > **Finance Insights** > **Parametry Finance Insights**, povolte funkci **Předpovědi plateb zákazníka** a klikněte na tlačítko **Vytvořit predikční model**. Po dokončení nasazení modelu AI budou nasazeny entity Dataverse potřebné k vytvoření integrace.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
