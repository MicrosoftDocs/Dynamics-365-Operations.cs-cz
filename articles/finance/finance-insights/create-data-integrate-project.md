---
title: Vytvořte projekt integrace dat
description: Toto téma vysvětluje, jak vytvořit projekt integrace dat.
author: ShivamPandey-msft
ms.date: 11/03/2021
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
ms.openlocfilehash: 7841f8b31e0ac1a40dce9acaac747f5f378236e0
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752657"
---
# <a name="create-a-data-integration-project"></a>Vytvořte projekt integrace dat

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

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
> Pokud nevidíte požadované entity v CDS, přejděte na **Kredit a inkasa > Nastavení > Finanční přehledy > Parametry finančních přehledů**, povolte funkci Předpovědi plateb zákazníka a klikněte na tlačítko **Vytvořit predikční model**. Po dokončení nasazení modelu AI (úspěšně nebo neúspěšně) budou entity CDS potřebné k vytvoření integrace nasazeny do CDS.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
