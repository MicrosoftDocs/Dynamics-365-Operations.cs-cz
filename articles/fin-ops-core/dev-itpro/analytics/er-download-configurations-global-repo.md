---
title: Stáhněte si konfigurace elektronického výkaznictví z Globálního úložiště konfigurační služby
description: Tento článek vysvětluje, jak stahovat konfigurace elektronického vykazování (ER) z globálního úložiště konfigurační služby.
author: kfend
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
ms.openlocfilehash: 3bbc341d1668e54fcb4034263a7e142166a94b05
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273301"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a>Stáhněte si konfigurace elektronického výkaznictví z Globálního úložiště konfigurační služby

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak stahovat [konfigurace elektronického vykazování (ER)](general-electronic-reporting.md#Configuration) z globálního úložiště konfigurační služby. Další informace viz [Microsoft Dynamics 365 Finance – Regulatory Services, konfigurační služba](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="open-configurations-repository"></a>Otevřete úložiště konfigurací

1. Přihlaste se k aplikaci Dynamics 365 Finance použitím některé z následující rolí:

    - Návrhář elektronického výkaznictví
    - Funkční konzultant elektronického výkaznictví
    - Správce systému

2. Přejděte do části **Správa organizace > Pracovní prostory > Elektronické výkaznictví**.
3. V části **Zprostředkovatelé konfigurace** vyberte dlaždici **Microsoft**.
3. Na dlaždici **Microsoft** vyberte **Úložiště**.

    ![Pracovní prostor elektronického vykazování.](./media/er-download-configurations-global-repo-er-workspace.png)

4. Na stránce **Úložiště konfigurací** v mřížce vyberte existující úložiště typu **Globální**. Pokud se toto úložiště nezobrazí v mřížce, postupujte následovně:

    1. Vyberte **Přidat** a přidejte nové úložiště.
    2. Vyberte **Globální** jako typ úložiště a poté vyberte **Vytvořit úložiště**.
    3. Po výzvy postupujte podle pokynů k autorizaci.
    4. Zadejte název a popis úložiště a poté vyberte **OK** k potvrzení nové položky úložiště.
    5. V mřížce vyberte nové úložiště typu **Globální**.

5. Vyberte **Otevřít** a zobrazte tak seznam konfigurací ER pro vybrané úložiště.

    ![Stránka úložišť konfigurace.](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a>Import jediné konfigurace

1. Na stránce **Úložiště konfigurace**, ve stromu konfigurací, vyberte požadovanou konfiguraci ER.
2. Na pevné záložce **Verze** vyberte požadovanou verzi vybrané konfigurace ER.
3. Vyberte **Importovat**, chcete-li stáhnout vybranou verzi z globálního úložiště do aktuální instance aplikace Finance and Operations.

    > [!NOTE]
    > Tlačítko **Import** nebude k dispozici u verzí konfigurace ER, které jsou již v aktuální instanci Finance přítomny.

    ![Stránka úložiště konfigurace, záložka Konfigurace.](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a>Import filtrovaných konfigurací

1. Na stránce **Úložiště konfigurace**, ve stromu konfigurací, rozbalte pevnou záložku **Filtr**.
2. V mřížce **Značky** přidejte všechny potřebné značky.
3. V poli **Použitelnost země / regionu** vyberte příslušné kódy zemí / regionů a poté vyberte **Použít filtr**.

    > [!NOTE]
    > Pevná záložka **Konfigurace** zobrazuje všechny konfigurace, které splňují zadané podmínky výběru.

4. Na pevné záložce **Konfigurace** vyberte **Import**, chcete-li stáhnout filtrované konfigurace z globálního úložiště do aktuální instance.
5. Na pevné záložce **Konfigurace** vyberte **Reset filtru** k vyčištění stanovených podmínek výběru.

    ![Stránka úložiště konfigurace, záložka Verze, tlačítko Importovat.](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> V závislosti na nastavení ER jsou konfigurace ověřeny po jejich importu. Můžete být upozorněni na potíže se zjištěnou nekonzistencí. Tyto potíže je nutné před importováním verze konfigurace odstranit. Další informace naleznete v seznam souvisejících zdrojů pro tento článek.

> [!NOTE]
> Konfigurace ER lze konfigurovat jako závislé na jiných konfiguracích. Proto spolu s vybranou konfigurací mohou být automaticky importovány i další konfigurace. Další informace o závislostech konfigurací najdete v článku [Definujte závislost ER konfigurací na jiných komponentách](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).

## <a name="additional-resources"></a>Další prostředky

[Přehled elektronického výkaznictví](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

