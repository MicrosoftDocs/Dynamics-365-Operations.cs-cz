---
title: Odeslání konfigurace do služby Lifecycle Services
description: Toto téma popisuje, jak vytvořit novou konfiguraci elektronického výkaznictví (ER) a nahrát ji do Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41a8fcf2592bde4901aba703e0cd124b1155dac6
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270552"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a>Odeslání konfigurace do služby Lifecycle Services

[!include [banner](../../includes/banner.md)]

Tohle téma popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou [konfiguraci elektronického výkaznictví](../general-electronic-reporting.md#Configuration) a odeslat ji do [knihovny majetku na úrovni projektu](../../lifecycle-services/asset-library.md) ve službě Microsoft Dynamics Lifecycle Services (LCS).

> [!IMPORTANT]
> Používání služby LCS jako úložiště pro konfigurace elektronického výkaznictví (ER) je označeno jako [zastaralé](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Další informace viz [Regulatory Configuration Service (RCS) – ukončení podpory úložiště Lifecycle Services (LCS)](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).

V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost s názvem Litware, Inc a odešlete ji do služby LCS. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace elektronického výkaznictví se sdílí mezi společnostmi. K provedení těchto kroků musíte v RCS nejprve dokončit jednotlivé kroky v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md). Je rovněž vyžadován přístup k LCS.

1. Přihlaste se k aplikaci použitím některé z následující role:

    - Návrhář elektronického výkaznictví
    - Správce systému

2. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
3. Vyberte **Litware, Inc.** a označte ji jako **Aktivní**.
4. Vyberte **Konfigurace**.

<a name="accessconditions"></a>
> [!NOTE]
> Ujistěte se, že aktuální uživatel Dynamics 365 Finance je členem projektu LCS, který obsahuje [knihovnu majetku](../../lifecycle-services/asset-library.md#asset-library-support), která slouží k importu konfigurací elektronického výkaznictví.
>
> K projektu LCS nemůžete přistupovat z úložiště elektronického výkaznictví, které představuje jinou doménu, než je doména použitá v aplikaci Finance. Pokud to zkusíte, zobrazí se prázdný seznam projektů LCS a nebudete moci importovat konfigurace elektronického výkaznictví z knihovny majetku na úrovni projektu v LCS. Chcete-li získat přístup ke knihovnám majektu na úrovni projektu z úložiště elektronického výkaznictví, které slouží k importu konfigurací elektronického výkaznictví, přihlaste se do aplikace Finance pomocí přihlašovacích údajů uživatele, který patří ke klientovi (doméně), pro který byla zřízena aktuální instance Finance.

## <a name="create-a-new-data-model-configuration"></a>Vytvoření nové konfigurace datového modelu

1. Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.
2. Na stránce **Konfigurace** výběrem možnosti **Vytvořit konfiguraci** otevřete rozevírací dialogové okno.

    V tomto příkladu vytvoříte konfiguraci, která obsahuje vzorový model dat pro elektronické doklady. Tato konfigurace modelu dat bude odeslána do LCS později.

3. V poli **Název** zadejte **Vzorová konfigurace modelu**.
4. V poli **Popis** zadejte **Vzorová konfigurace modelu**.
5. Vyberte **Vytvořit konfiguraci**.
6. Vyberte **Návrhář modelů**.
7. Zvolte **Nové**.
8. Do pole **Název** zadejte **Vstupní bod**.
9. Vyberte **přidat**.
10. Zvolte **Uložit**.
11. Zavřete stránku.
12. Vyberte **Změnit stav**.
13. Zvolte **Dokončit**.
14. Vyberte **OK**.
15. Zavřete stránku.

## <a name="register-a-new-repository"></a>Registrace nového úložiště

1. Přejděte do části **Správa organizace \> Pracovní prostory \> Elektronické výkaznictví**.

2. V části **Zprostředkovatelé konfigurace** vyberte dlaždici **Litware Inc.**

3. Na dlaždici **Litware, Inc.** vyberte **Úložiště**.

    Nyní můžete otevřít seznam úložišť pro poskytovatele konfigurace Litware, Inc.

4. Výběrem možnosti **Přidat** otevřete rozevírací dialogové okno.

    Nyní můžete přidat nové úložiště.

5. V poli **Typ úložiště konfigurace** vyberte **LCS**.
6. Zvolte **Vytvořit úložiště**.
7. V poli **Projekt** zadejte nebo vyberte hodnotu.

    V tomto příkladu vyberte požadovaný projekt LCS. Musíte mít [přístup](#accessconditions) k tomuto projektu.

8. Vyberte **OK**.

    Vytvořte nový záznam v úložišti.

9. Označte na seznamu vybraný řádek.

    V tomto příkladu vyberte záznam úložiště **LCS**.

    Všimněte si, že registrované úložiště je označeno aktuálním poskytovatelem. Jinými slovy, do tohoto úložiště lze umístit pouze konfigurace, které vlastní tento poskytovatel, a proto je možné je odeslat do vybraného projektu LCS.

10. Zvolte **Otevřít**.

    Tím otevřete úložiště se seznamem konfigurací elektronického výkaznictví. Pokud vybraný projekt zatím nebyl použit pro sdílení konfigurací elektronického výkaznictví, seznam bude prázdný.

11. Zavřete stránku.
12. Zavřete stránku.

## <a name="upload-a-configuration-into-lcs"></a>Odeslání konfigurace do LCS

1. Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.
2. Na stránce **Konfigurace** ve stromové struktuře konfigurací vyberte položku **Vzorová konfigurace modelu**.

    Muíte vybrat vytvořenou konfiguraci, která již byla dokončena.

3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.

    Pro tento příklad vyberte verzi vybrané konfigurace ve stavu **Dokončeno**.

4. Vyberte **Změnit stav**.
5. Vyberte **Sdílet**.

    Stav konfigurace se změní z **Dokončeno** na **Sdíleno**, když je konfigurace publikována v LCS.

6. Vyberte **OK**.
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho.

    Pro tento příklad vyberte verzi této konfigurace ve stavu **Sdíleno**.

    Všimněte si, že stav vybrané verze se změnil z **Dokončeno** na **Sdíleno**.

8. Zavřete stránku.
9. Vyberte **Úložiště**.

    Nyní můžete otevřít seznam úložišť pro poskytovatele konfigurace Litware, Inc.

10. Zvolte **Otevřít**.

    V tomto příkladu vyberte úložiště **LCS** a otevřete jej.

    Všimněte si, že vybraná konfigurace je zobrazena jako majetek vybraného projektu LCS.

11. Otevřete LCS přechodem na <https://lcs.dynamics.com>.
12. Otevřete projekt, který byl dříve použit pro registraci úložiště.
13. Otevřete knihovnu majetku projektu.
14. Vyberte typ majetku **Konfigurace GER**.

    V seznamu by měla být uvedena konfigurace elektronického výkaznictví, kterou jste nahráli.

    Všimněte si, že odeslané konfigurace LCS je možné importovat do jiné instance, pokud poskytovatelé mají přístupová práva k tomuto projektu LCS.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
