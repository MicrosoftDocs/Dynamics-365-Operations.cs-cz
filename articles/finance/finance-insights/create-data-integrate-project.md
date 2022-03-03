---
title: Vytvořte projekt integrace dat
description: Toto téma vysvětluje, jak vytvořit projekt integrace dat.
author: ShivamPandey-msft
ms.date: 02/09/2022
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
ms.openlocfilehash: 50f435f9d461667a1908baa529d73766085c183a
ms.sourcegitcommit: 6526acd0300d9c5800d3d7675d54e23090d031df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2022
ms.locfileid: "8107280"
---
# <a name="create-a-data-integration-project"></a>Vytvořte projekt integrace dat

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit projekt integrace dat.

1. Přihlaste se do aplikace Microsoft Dynamics 365 Finance.
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

    1. Vytvořte projekty integrace dat pro následující šablony pomocí sady připojení, kterou jste právě vytvořili:

        - Výsledek přehledu plateb zákazníka (CDS do Fin and Ops 10.0.17+)
        - Výsledky časové řady cashflow (CDS do Fin and Ops)
        - Výsledky časové řady rozpočtu (CDS do Fin and Ops)

    2. Nastavte vhodné plánování pro každý projekt.

> [!NOTE]
> Pokud nevidíte požadované entity v Dataverse, přejděte na **Kredit a inkasa** > **Nastavení** > **Finance Insights** > **Parametry Finance Insights**, povolte funkci **Předpovědi plateb zákazníka** a klikněte na tlačítko **Vytvořit predikční model**. Po dokončení nasazení modelu AI budou nasazeny entity Dataverse potřebné k vytvoření integrace.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
