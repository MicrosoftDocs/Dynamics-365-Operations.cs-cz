---
title: Import konfigurace ze služby Lifecycle Services
description: Tohle téma popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může importovat novou verzi konfigurace elektronického výkaznictví ze služby Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c43cdce8d073f04a3158c8beb13a5376e669a4c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684444"
---
# <a name="import-a-configuration-from-lifecycle-services"></a>Import konfigurace ze služby Lifecycle Services

[!include [banner](../../includes/banner.md)]

Tohle téma popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může importovat novou verzi [konfigurace elektronického výkaznictví](../general-electronic-reporting.md#Configuration) z [knihovny majetku na úrovni projektu](../../lifecycle-services/asset-library.md) ve službě Microsoft Dynamics Lifecycle Services (LCS).

V tomto příkladu zvolíte požadovanou verzi konfigurace elektronického výkaznictví a importujete ji pro vzorovou společnost s názvem Litware, Inc. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace elektronického výkaznictví se sdílí mezi společnostmi. K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu [Odeslání konfigurace elektronického výkaznictví do služby Lifecycle Services](er-upload-configuration-into-lifecycle-services.md). Je rovněž vyžadován přístup k LCS.

1. Přihlaste se k aplikaci použitím některé z následující role:

    - Návrhář elektronického výkaznictví
    - Správce systému

2. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
3. Vyberte **Konfigurace**.

<a name="accessconditions"></a>
> [!NOTE]
> Ujistěte se, že aktuální uživatel Dynamics 365 Finance je členem projektu LCS, který obsahuje knihovnu majetku, ke které chce uživatel [přístup](../../lifecycle-services/asset-library.md#asset-library-support) kvůli importu konfigurací elektronického výkaznictví.
>
> K projektu LCS nemůžete přistupovat z úložiště elektronického výkaznictví, které představuje jinou doménu, než je doména použitá v aplikaci Finance. Pokud to zkusíte, zobrazí se prázdný seznam projektů LCS a nebudete moci importovat konfigurace elektronického výkaznictví z knihovny majetku na úrovni projektu v LCS. Chcete-li získat přístup ke knihovnám majektu na úrovni projektu z úložiště elektronického výkaznictví, které slouží k importu konfigurací elektronického výkaznictví, přihlaste se do aplikace Finance pomocí přihlašovacích údajů uživatele, který patří ke klientovi (doméně), pro který byla zřízena aktuální instance Finance.

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a>Odstranění sdílené verze konfigurace modelu dat

1. Na stránce **Konfigurace** ve stromové struktuře konfigurací vyberte položku **Vzorová konfigurace modelu**.

    Vytvořili jste první verzi vzorové konfigurace modelu dat a publikovali ji v LCS po provedení kroků v části [Odeslání konfigurace do služby Lifecycle Services](er-upload-configuration-into-lifecycle-services.md). V tomto postupu tuto verzi konfigurace elektronického výkaznictví odstraníte. Danou verzi poté importujete z LCS dále v tomto tématu.

2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.

    Pro tento příklad vyberte verzi této konfigurace ve stavu **Sdíleno**. Tento stav označuje, že byla konfigurace publikována do LCS.

3. Vyberte **Změnit stav**.
4. Vyberte **Ukončit**.

    Změnou stavu vybrané verze ze **Sdíleno** na **Ukončeno** umožníte její odstranění.

5. Vyberte **OK**.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.

    Pro tento příklad vyberte verzi této konfigurace ve stavu **Ukončeno**.

7. Zvolte **Odstranit**.
8. Vyberte **Ano**.

    Všimněte si, že pouze 2. verze návrhu vybrané konfigurace modelu dat je k nyní dispozici.

9. Zavřete stránku.

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a>Import sdílené verze konfigurace modelu dat z LCS

1. Přejděte do části **Správa organizace \> Pracovní prostory \> Elektronické výkaznictví**.

2. V části **Zprostředkovatelé konfigurace** vyberte dlaždici **Litware Inc.**

3. Na dlaždici **Litware, Inc.** vyberte **Úložiště**.

    Nyní můžete otevřít seznam úložišť pro poskytovatele konfigurace Litware, Inc.

4. Zvolte **Otevřít**.

    V tomto příkladu vyberte úložiště **LCS** a otevřete jej. Musíš mít [přístup](#accessconditions) k projektu LCS a knihovně majetku, ke které má přístup vybrané úložiště elektronického výkaznictví.

5. Označte na seznamu vybraný řádek.

    V tomto případě vyberte první verzi **vzorové konfigurace modelu** v seznamu verzí.

6. Vyberte **Import**.
7. Volbou **Ano** potvrďte import vybrané verze z LCS.

    Informační zpráva potvrzuje, že vybraná verze byla úspěšně importována.

8. Zavřete stránku.
9. Zavřete stránku.
10. Vyberte **Konfigurace**.
11. Ve stromovém zobrazení vyberte možnost **Vzorová konfigurace modelu**.
12. Vyhledejte na seznamu požadovaný záznam a vyberte ho.

    Pro tento příklad vyberte verzi této konfigurace ve stavu **Sdíleno**.

    Všimněte si, že nyní je k dispozici také sdílená 1. verze vybrané konfigurace datového modelu.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]