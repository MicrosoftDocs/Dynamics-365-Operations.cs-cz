---
title: Komprimujte velké dokumenty generované v elektronickém výkaznictví
description: Toto téma vysvětluje, jak komprimovat velké dokumenty generované formátem Electronic reporting (ER).
author: NickSelin
manager: kfend
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERFormatDestinationTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 30de55f9e55911290750c148621fd3d4531686c2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680847"
---
# <a name="compress-large-documents-that-are-generated-in-electronic-reporting"></a>Komprimujte velké dokumenty generované v elektronickém výkaznictví 

[!include [banner](../includes/banner.md)]

Můžete použít [Rámec elektronického výkaznictví (ER)](general-electronic-reporting.md) a nakonfigurovat řešení, které načte transakční data, aby vygeneroval odchozí dokument. Tento vygenerovaný dokument může být docela velký. Při generování tohoto typu dokumentu se používá paměť [Server aplikačních objektů (AOS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/access-instances#location-of-packages-source-code-and-other-aos-configurations) k jeho uložení. V určitém okamžiku musí být dokument poté stažen z vaší aplikace Microsoft Dynamics 365 Finance. V současné době je maximální velikost jednoho dokumentu generovaného v ER omezena na 2 gigabajty (GB). Navíc v současné době Finance [omezuje](https://fix.lcs.dynamics.com/Issue/Details?bugId=489291) velikost staženého souboru na 1 GB. Proto musíte nakonfigurovat řešení ER, které snižuje pravděpodobnost překročení těchto omezení a obdržíte výjimku **Stream byl příliš dlouhý** nebo **Přetečení nebo podtečení v aritmetické operaci**.

Při konfiguraci řešení můžete upravit formát ER v návrháři operací přidáním kořenového prvku **Složka** pro kompresi obsahu, který je generován některým z vnořených prvků. Komprese funguje „včas“, takže lze snížit maximální využití paměti a velikost staženého souboru.

> [!NOTE]
> Komprese souborů vyžaduje další procento využití procesoru.

Chcete-li získat další informace o tomto přístupu, proveďte příklad v tomto tématu.

## <a name="example-compress-an-outbound-document"></a>Příklad: Komprimovat odchozí dokument

Tento příklad ukazuje, jak uživatel, který je přiřazen k roli **Správce systému** nebo **Funkční konzultant elektronického výkaznictví**, může nakonfigurovat formát ER pro kompresi vygenerovaného dokumentu.

### <a name="prerequisites"></a>Předpoklady

Před provedením procedur v tomto tématu je nutné provést následující kroky.

1. [Aktivace poskytovatele konfigurace](er-defer-xml-element.md#activate-a-configuration-provider).
2. [Import ukázkových konfigurací elektronického výkaznictví](er-defer-xml-element.md#import-the-sample-er-configurations).
3. [Kontrola importovaného formátu](er-defer-xml-element.md#review-the-imported-format).

> [!NOTE]
> V současné době formátová struktura začíná od prvku **Sestava** typu **Soubor** a obsahuje prvky XML. Proto bude odchozí dokument vygenerován ve formátu XML a nebude použita žádná komprese.

### <a name="generate-an-er-format-to-get-an-uncompressed-document"></a>Vygenerujte formát ER a získejte nekomprimovaný dokument

1. [Spuštění importovaného formátu](er-defer-xml-element.md#run-the-imported-format).
2. Všimněte si, že velikost vygenerovaného dokumentu ve formátu XML je 3 kilobajty (KB).

    ![Náhled nekomprimovaného odchozího dokumentu](./media/er-compress-outbound-files1.png)

### <a name="modify-the-format-to-compress-the-generated-output"></a>Upravte formát pro kompresi generovaného výstupu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací rozbalte **Model to learn deferred elements**.
3. Vyberte konfiguraci **Format to learn deferred XML elements**.
4. Chcete-li uptavit strukturu formátu, vyberte možnost **Návrhář**.
5. Na stránce **Návrhář formátu** na kartě **Formát** vyberte **Přidat kořen** a kořenový prvek formátu.
6. V dialogovém okně **Přidat** vyberte **Společný\\ Složka**.
7. Vyberte **OK** pro potvrzení přidání nového kořenového prvku.
8. Zvolte **Uložit**.

> [!NOTE]
> Struktura formátu začíná od prvku typu **Složka**. Tento prvek vygeneruje výstup jako komprimovaný soubor (zip). Když je dokument, který je generován prvkem **Sestava** je vložen do odchozího souboru zip, jeho obsah bude komprimován, aby se zmenšila velikost odchozího souboru.

### <a name="generate-an-er-format-to-get-a-compressed-document"></a>Vygenerujte formát ER a získejte komprimovaný dokument

1. Na stránce **Návrhář formátu** zvolte **Spustit**.
2. Stáhněte soubor zip, který webový prohlížeč nabízí, a otevřete jej k revizi.
3. Všimněte si, že velikost vygenerovaného dokumentu ve formátu ZIP je 1 KB.

    > [!NOTE] 
    > Kompresní poměr souboru XML, který tento soubor zip obsahuje, je 87 procent. Kompresní poměr závisí na komprimovaných datech.

    ![Náhled komprimovaného odchozího dokumentu](./media/er-compress-outbound-files2.png)

> [!NOTE]
> Pokud je [destinace](electronic-reporting-destinations.md) ER nakonfigurována pro prvek formátu, který generuje výstup (prvek **Sestava** v tomto příkladu), obejde se komprese výstupu.

## <a name="additional-resources"></a>Další prostředky

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Místa určení elektronického výkaznictví](electronic-reporting-destinations.md)

[Odložení provádění prvků XML ve formátech elektronického výkaznictví](er-defer-xml-element.md)
