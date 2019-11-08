---
title: Stažení konfigurace elektronického vykazování ze služby Lifecycle Services
description: Toto téma popisuje postup, jak stáhnout konfigurace elektronických sestav (ER) ze služby Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 561187343073a84b152151abe8770e89196eaa56
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174114"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Stažení konfigurací elektronického výkaznictví ze služby Lifecycle Services

[!include [banner](../includes/banner.md)]

Toto téma popisuje postup, jak stáhnout konfigurace elektronických sestav (ER) ze služby Microsoft Dynamics Lifecycle Services (LCS).

Tento kurz vás provede stahováním nejnovější verze konfigurací elektronických sestav (ER) v rámci Microsoft Dynamics Lifecycle Services (LCS).

1. Přihlaste se k aplikaci použitím některé z následující role:

    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

2. Přejděte do části **Správa organizace** &gt; **Elektronické výkaznictví**.
3. V části **Zprostředkovatelé konfigurace** vyberte dlaždici **Microsoft**.
4. Na dlaždici **Microsoft** klepněte na tlačítko **Úložiště**.

    [![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. Na stránce **Úložiště konfigurací** v mřížce vyberte existující úložiště typu **LCS**. Pokud se toto úložiště nezobrazí v mřížce, postupujte následovně:

    1. Kliknutím na **Přidat** přidejte nové úložiště.
    2. Vyberte možnost **LCS** jako typ úložiště.
    3. Klikněte na **Vytvořit úložiště**.
    4. Po výzvy postupujte podle pokynů k autorizaci.
    5. Zadejte název a popis úložiště.
    6. Kliknutím na **OK** potvrďte nový záznam úložiště.
    7. V mřížce vyberte nové úložiště typu **LCS**.

6. Klepněte na tlačítko **Otevřít** a zobrazte tak seznam konfigurací ER pro vybrané úložiště.

    [![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

7. Ve stromu konfigurací v levém podokně vyberte konfiguraci ER, kterou potřebujete.
8. Na pevné záložce **Verze** vyberte požadovanou verzi vybrané konfigurace ER.
9. Kliknutím na tlačítko **Importovat** stáhnete vybranou verzi ze LCS do aktuální instance.

    > [!NOTE]
    > Tlačítko **Import** nebude k dispozici u verzí konfigurace ER, které jsou již v aktuální instanci přítomny.

    [![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> V závislosti na nastavení ER jsou konfigurace ověřeny po jejich importu. Můžete být upozorněni na potíže se zjištěnou nekonzistencí. Tyto potíže je nutné před importováním verze konfigurace odstranit. Další informace naleznete v seznam souvisejících článků pro toto téma.

## <a name="additional-resources"></a>Další zdroje

[Přehled elektronického výkaznictví](general-electronic-reporting.md)