---
title: Správa životního cyklu konfigurace elektronického vykazování
description: Toto téma popisuje způsob správy životního cyklu konfigurací elektronického výkaznictví pro řešení Microsoft Dynamics 365 for Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5724ba62bfb2c6e75ae895dc9285966c25f387a2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "344793"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Správa životního cyklu konfigurace elektronického vykazování

[!include [banner](../includes/banner.md)]

Toto téma popisuje způsob správy životního cyklu konfigurací elektronického výkaznictví pro řešení Microsoft Dynamics 365 for Finance and Operations.

## <a name="overview"></a>Přehled

Elektronické výkaznictví je modul pro podporu elektronických dokumentů specifických pro danou zemi a požadovaných zákonem v aplikaci Microsoft Dynamics 365 for Finance and Operations. Obecně platí, že Elektronické výkaznictví předpokládá schopnost provádět následující činnosti pro jeden elektronický dokument. Další podrobnosti získáte v tématu [Přehled elektronického vykazování](general-electronic-reporting.md)

- Návrh šablony pro elektronický dokument:

    - Identifikace požadovaných zdrojů dat, které lze zpřístupnit v tomto dokumentu:

        - Základní data aplikace Finance and Operations, například datové tabulky, datové entity a třídy.
        - Vlastnosti určité pro proces jako datum provedení a čas a časové pásmo.
        - Vstupní parametry uživatele definované koncovým uživatelem při spuštění.

    - Definování prvků nezbytných pro dokument a také jejich topologie pro určení konečného formátu dokumentu.
    - Konfigurace požadovaného toku dat z vybraného zdroje dat pro definování prvků dokumentu prostřednictvím součástí formátu vazeb datového zdroje dokumentu a určení logiky procesu řízení.

- Zpřístupněte šablonu, aby ji možné použít v jiných instancích aplikace Finance and Operations:

    - Převeďte šablonu dokumentu, která byla vytvořena v aplikaci Finance and Operations, na konfiguraci elektronického výkaznictví, a exportujte konfiguraci z aktuální instance aplikace Finance and Operations jako balíček XML, který může být uložen lokálně nebo v rámci LCS.
    - Převeďte konfiguraci elektronického výkaznictví na šablonu dokumentu aplikace Finance and Operations.
    - Importujte balíček XML, který je uložen lokálně nebo v rámci LCS, do aktuální instance aplikace Finance and Operations.

- Upravte šablonu elektronického dokumentu:

    - Přeneste šablonu z LCS do aktuální instance aplikace Finance and Operations jako konfiguraci elektronického výkaznictví.
    - Návrh vlastní verze konfigurace elektronického výkaznictví a uchování odkazu na základní verzi.

- Integrujte šablonu do konkrétního obchodního procesu, aby byla k dispozici v aplikaci Finance and Operations:

    - Konfigurujte nastavení aplikace Finance and Operations tak, aby aplikace začala používat konfiguraci elektronického výkaznictví (vytvořte odkaz na tuto konfiguraci v parametru souvisejícím s procesem). Například odkazujte na konfiguraci elektronického výkaznictví v konkrétní metodě platby závazků s cílem vygenerovat zprávu pro elektronickou platbu pro zpracování faktur.

- Použití šablony v určitém obchodním procesu:

    - Spusťte konfiguraci služby ER do určitého obchodního procesu. Například odkazujte na konfiguraci elektronického výkaznictví ke zpracování fakturu, když je vybraná metoda platby, která odkazuje na konfiguraci ER.

## <a name="concepts"></a>Koncepty
Následující role a související aktivity jsou přidruženy k životním cyklu konfigurace elektronického výkaznictví.

| Role                                       | Aktivity                                                      | popis |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| Funkční konzultant elektronického výkaznictví | Vytvořte a spravujte součásti elektronického výkaznictví (modelů a formáty).           | Obchodní pracovník, který navrhuje modely specifické pro doménu elektronického výkaznictví, navrhuje také požadované šablony pro elektronické dokumenty a vhodně je prováže. |
| Návrhář elektronického výkaznictví             | Vytvořte a spravujte mapování datového modelu.                          | Specialista aplikace Finance and Operations, který vybírá požadované zdroje dat aplikace Finance and Operations a navazuje je na datové modely elektronického výkaznictví v konkrétní doméně. |
| Účetní supervizor                      | Nakonfigurujte nastavení týkajícího se procesu, které odkazuje na artefakty elektronického výkaznictví. | Například role **Účetní supervizor**, která umožňuje použít nastavení konfigurace elektronického výkaznictví pro konkrétní účty metodu plateb závazků s cílem vygenerovat zprávu elektronické platby pro zpracování faktur. |
| Úředník plateb závazků            | Použijte artefakty elektronického výkaznictví v určitém obchodním procesu.                | Například role **Úředník pro platby závazků**, která umožňuje vygenerovat zprávy elektronických plateb pro zpracování faktur na základě formátu elektronického výkaznictví nastaveného pro konkrétní způsob platby. |

## <a name="er-configuration-development-lifecycle"></a>Životní cyklus vývoje konfigurace elektronického výkaznictví
Z následujících důvodů doporučujeme navrhovat konfigurace elektronického výkaznictví ve vývojovém prostředí v oddělené instanci aplikace Finance and Operations:

- Uživatelé mají buď role **Vývojáře elektronického vykazování** nebo **Funkčního konzultanta elektronického výkaznictví**, kteří mohou upravovat konfigurace a spouštět je pro účely testování. To může způsobit volání metod tříd a tabulek, které mohou potenciálně poškodit obchodní data a výkon aplikace Finance and Operations.
- Volání metod tříd a tabulek jako zdrojů dat elektronického výkaznictví není omezeno vstupními body aplikace Finance and Operations a zaznamenaným obsahem společnosti. Proto citlivá obchodná data mohou zobrazovat uživatelé mající buď roli **Vývojáře elektronického vykazování** nebo **Funkčního konzultanta elektronického výkaznictví**.

Konfigurace elektronického výkaznictví navržené ve vývojovém prostředí je možné odeslat do testovacího prostředí pro hodnocení konfigurace (správný proces integrace, správnost výsledků, výkonnost) a kontrola kvality (správnost role řídící přístupová práva, dělení zodpovědnosti atd.). Pro tento účel lze použít funkce, které umožňují výměnu konfigurace elektronického výkaznictví. Ověřené konfigurace elektronického výkaznictví je možné uložit buď do LCS pro sdílení se službami odběratelů nebo do výrobního prostředí pro interní použití, jak ukazuje následující ilustrace.

![Životní cyklus elektronického výkaznictví](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a>Další zdroje

[Přehled elektronického výkaznictví](general-electronic-reporting.md)
