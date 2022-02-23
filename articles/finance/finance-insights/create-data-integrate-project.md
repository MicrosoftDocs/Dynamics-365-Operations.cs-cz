---
title: Vytvoření projektu integrátoru dat (Preview)
description: Toto téma vysvětluje, jak vytvořit projekt integrátoru dat.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: fb17d5e82709a34ff088774d9e9034adb714b58c
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646246"
---
# <a name="create-a-data-integrator-project-preview"></a>Vytvoření projektu integrátoru dat (Preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Toto téma vysvětluje, jak vytvořit projekt integrátoru dat.

1. Přihlaste se do aplikace Microsoft Dynamics 365 Finance.
2. Přejděte na **Pracovní prostory \> Správa dat** a vyberte dlaždici **Datové entity**. Než přejdete k dalšímu kroku, počkejte, dokud se neobnoví všechny datové entity.
3. Otevřete [portál Power Apps](https://make.powerapps.com/) a postupujte takto:

    1. Vyberte příslušné prostředí.
    2. V levém navigačním podokně nalevo vyberte **Data \> Připojení**.
    3. Připojte se k příslušným instancím následujících položek:

        - Dynamics 365
        - Dynamics 365 for Fin & Ops

4. Otevřete [prostředí Power Apps](https://admin.powerapps.com/environments) a postupujte takto:

    1. Vyberte **Integrátor dat**.
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

        - Výsledky přehledu plateb zákazníka (CDS do Fin and Ops)
        - Výsledky časové řady cashflow (CDS do Fin and Ops)
        - Výsledky časové řady rozpočtu (CDS do Fin and Ops)

    2. Nastavte vhodné plánování pro každý projekt.

> [!NOTE]
> Pokud nevidíte požadované entity v CDS, přejděte na **Kredit a inkasa > Nastavení > Finanční přehledy > Parametry finančních přehledů**, povolte funkci Předpovědi plateb zákazníka a klikněte na tlačítko **Vytvořit predikční model**. Po dokončení nasazení modelu AI (úspěšně nebo neúspěšně) budou entity CDS potřebné k vytvoření integrace nasazeny do CDS.

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů

Verze Preview (1) mohou využívat méně ochrany soukromí a bezpečnostních opatření než služba Dynamics 365 Finance and Operations, (2) nejsou zahrnuty v dohodě o úrovni služeb (SLA) pro tuto službu, (3) neměly by být používány pro zpracování osobních údajů nebo jiných údajů, které podléhají právním nebo regulačním požadavkům, a (4) mají omezenou podporu.
