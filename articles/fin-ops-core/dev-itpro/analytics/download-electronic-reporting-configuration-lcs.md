---
title: Stažení konfigurace elektronického vykazování ze služby Lifecycle Services
description: Tento článek popisuje postup, jak stáhnout konfigurace elektronických sestav (ER) ze služby Microsoft Dynamics Lifecycle Services (LCS).
author: kfend
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.form: ERSolutionImport, ERWorkspace
ms.openlocfilehash: f48dd14bc3009550d78bd71db030c172d2ef6450
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277809"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Stažení konfigurace elektronického vykazování ze služby Lifecycle Services

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak stáhnout nejnovější verzi [konfigurací elektronického výkaznictví](general-electronic-reporting.md#Configuration) z [knihovny sdíleného majetku](../lifecycle-services/asset-library.md) v Microsoft Dynamics Lifecycle Services (LCS).

> [!IMPORTANT]
> Používání služby LCS jako úložiště pro konfigurace elektronického výkaznictví (ER) je označeno jako [zastaralé](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Další informace viz [Regulatory Configuration Service (RCS) – ukončení podpory úložiště Lifecycle Services (LCS)](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).

1. Přihlaste se k aplikaci použitím některé z následující role:

    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

2. Přejděte do části **Správa organizace** &gt; **Pracovní prostory** &gt; **Elektronické výkaznictví**.
3. V části **Zprostředkovatelé konfigurace** vyberte dlaždici **Microsoft**.
4. Na dlaždici **Microsoft** vyberte **Úložiště**.

    [![Dlaždice Microsoft na stránce Konfigurace lokalizace.](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. Na stránce **Úložiště konfigurací** v mřížce vyberte existující úložiště typu **LCS**. Pokud se toto úložiště nezobrazí v mřížce, postupujte následovně:

    1. Volbou **Přidat** přidejte úložiště.
    2. Vyberte možnost **LCS** jako typ úložiště.
    3. Zvolte **Vytvořit úložiště**.
    4. Pokud se zobrazí výzva k autorizaci, postupujte podle pokynů na obrazovce.
    5. Zadejte název a popis úložiště.
    6. Volbou **OK** potvrďte nový záznam úložiště.
    7. V mřížce vyberte nové úložiště typu **LCS**.

6. Vyberte **Otevřít** a zobrazte tak seznam konfigurací ER pro vybrané úložiště.

    [![Stránka úložišť konfigurace.](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

    > [!TIP]
    > Pokud máte potíže s přístupem do úložiště LCS ke stažení konfigurací ze sdílené knihovny majetku v LCS, můžete si konfigurace stánout také z [globálního úložiště](er-download-configurations-global-repo.md).

7. Ve stromu konfigurací v levém podokně vyberte požadovanou konfiguraci elektronického výkaznictví.
8. Na pevné záložce **Verze** vyberte požadovanou verzi vybrané konfigurace ER.
9. Volbou **Importovat** stáhnete vybranou verzi ze LCS do aktuální instance.

    > [!NOTE]
    > Tlačítko **Import** nebude k dispozici u verzí konfigurace ER, které jsou již v aktuální instanci přítomny.

    [![Stránka úložiště konfigurace.](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> V závislosti na nastavení ER jsou konfigurace ověřeny po jejich importu. Můžete být upozorněni na potíže se zjištěnou nekonzistencí. Tyto potíže je nutné před importováním verze konfigurace odstranit. Další informace naleznete v seznam souvisejících témat pro tento článek.

## <a name="additional-resources"></a>Další prostředky

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Stáhněte si konfigurace elektronického výkaznictví z Globálního úložiště konfigurační služby](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
