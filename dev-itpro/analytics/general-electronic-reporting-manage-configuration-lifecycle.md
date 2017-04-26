---
title: "Správa životního cyklu konfigurace elektronického vykazování"
description: "Toto téma popisuje, jak spravovat životní cyklus elektronické vykazování konfigurace služeb Microsoft Dynamics 365 pro operace řešení (ER)."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: f4d8994f6548119789715a4879b6bc02d25598e9
ms.lasthandoff: 03/31/2017


---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Správa životního cyklu konfigurace elektronického vykazování

[!include[banner](../includes/banner.md)]


Toto téma popisuje, jak spravovat životní cyklus elektronické vykazování konfigurace služeb Microsoft Dynamics 365 pro operace řešení (ER).

<a name="overview"></a>Přehled
--------

Elektronické výkaznictví je modul pro podporu elektronických dokumentů specifických pro danou zemi a požadovaných zákonem v aplikaci Microsoft Dynamics 365 for Operations. Obecně platí, že Elektronické výkaznictví předpokládá schopnost provádět následující činnosti pro jeden elektronický dokument. Další informace naleznete v tématu [elektronické sestavy Přehled](general-electronic-reporting.md).

-   Návrh šablony pro elektronický dokument:
    -   Identifikace požadovaných zdrojů dat, které lze zpřístupnit v tomto dokumentu:
        -   Základní 365 Dynamics pro operace dat, například tabulky dat, datových entit a třídy.
        -   Vlastnosti specifické pro proces, například provádění datum a čas a časové pásmo.
        -   Uživatel zadány vstupní parametry, koncovým uživatelem v době běhu.
    -   Definování prvků nezbytných pro dokument a také jejich topologie pro určení konečného formátu dokumentu.
    -   Konfigurace požadovaného toku dat z vybraného zdroje dat pro definování prvků dokumentu prostřednictvím součástí formátu vazeb datového zdroje dokumentu a určení logiky procesu řízení.
-   Zpřístupněte šablonu tak, aby ji možné použít v jiných instancích aplikace Dynamics 365 for Operations:
    -   Převeďte šablonu dokumentu, která byla vytvořena v aplikaci Dynamics 365 for Operations, na konfiguraci elektronického výkaznictví, a exportujte konfiguraci z aktuální instance aplikace Dynamics 365 for Operations jako balíček XML, který může být uložen lokálně nebo v rámci LCS.
    -   Převeďte konfiguraci elektronického výkaznictví jako šablonu dokumentu aplikace Dynamics 365 for Operations.
    -   Importujte balíček XML, který je uložen místně nebo v rámci LCS do aktuální instance aplikace Dynamics 365 for Operations.
-   Upravte šablonu elektronického dokumentu:
    -   Přeneste šablonu z LCS do aktuální instance Dynamics 365 for Operations jako konfiguraci elektronického výkaznictví.
    -   Návrh vlastní verze konfigurace elektronického výkaznictví a uchování odkazu na základní verzi.
-   Integrujte šablonu v konkrétním obchodním procesu tak, aby byly k dispozici v aplikaci Dynamics 365 for Operations:
    -   Konfigurujte nastavení aplikace Dynamics 365 for Operations tak, aby aplikace začala používat konfiguraci elektronického výkaznictví odkazem na tuto konfiguraci v parametru souvisejícím s procesem. Například naleznete v konfigurace ER v konkrétní metoda platby splatné účty generovat zprávu elektronické platby pro zpracování faktur.
-   Použití šablony v určitém obchodním procesu:
    -   Spusťte konfigurace služby ER do určitého obchodního procesu. Například chcete-li generovat zprávu elektronické platby pro zpracování faktur při způsobu platby, který odkazuje konfigurace ER je vybrána.

## <a name="concepts"></a>Koncepty
Následující role a související činnosti jsou spojeny s konfigurace omezené ER.

| Role                                       | Aktivity                                                      | popis                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funkční konzultant elektronického výkaznictví | Vytvořte a spravujte součásti elektronického výkaznictví (modelů a formáty).           | Organizační osoba, která navrhuje ER domény specifické datové modely, vzory požadované šablony pro elektronické dokumenty a váže je odpovídajícím způsobem.                                                                           |
| Návrhář elektronického výkaznictví             | Vytvořte a spravujte mapování datového modelu.                          | 365 Dynamics pro operace odborníka, který vybere požadované 365 Dynamics pro zdroje dat, operace a sváže je ER modely dat specifické pro domény.                                                                 |
| Účetní supervizor                      | Nakonfigurujte nastavení týkajícího se procesu, které odkazuje na artefakty elektronického výkaznictví. | Například **Účetní supervizor** role, která umožňuje nastavení konfigurace ER pro určitý způsob platby splatné účty generovat zprávu elektronické platby pro zpracování faktur. |
| Úředník plateb závazků            | Použijte artefakty elektronického výkaznictví v určitém obchodním procesu.                | Například **Úředník plateb závazků** role, která umožňuje zprávy elektronické platby budou vygenerovány pro zpracování faktury založené na formátu ER, který je nakonfigurován pro konkrétní způsob platby.           |

## <a name="er-configuration-development-lifecycle"></a>Životní cyklus vývoje konfigurace elektronického výkaznictví
Je doporučeno navrhovat konfigurace pravidel ve vývojovém prostředí, jako v oddělené instanci aplikace 365 for Operations z těchto důvodů souvisejících s elektronickým výkaznictvím:

-   Uživatelé mají buď role **Vývojáře elektronického vykazování** nebo **Funkčního konzultanta elektronického výkaznictví**, kteří mohou upravovat konfigurace a spouštět je pro účely testování. To může způsobit volání metod tříd a tabulek, které mohou být potenciálně škodlivé pro obchodní data a výkon použití instance Dynamics 365 for Operations.
-   Volání metod tříd a tabulek jako zdroje dat elektronického výkaznictví nejsou omezeny vstupními body Dynamics 365 for Operations a jsou zaznamenány do obsahu společnosti. Proto citlivá obchodná data mohou zobrazovat uživatelé mající buď roli **Vývojáře elektronického vykazování** nebo **Funkčního konzultanta elektronického výkaznictví**.

ER konfigurace, které jsou určeny ve vývojovém prostředí lze odeslat do testovacího prostředí pro hodnocení konfigurace (řádného procesu integrace, správnost výsledků a výkonnosti) a zabezpečování jakosti, jako jsou jimi řízené role přístupových práv a zodpovědnosti. Pro tento účel lze použít funkce, které umožňují výměnu dat konfigurace ER. Ověřené konfigurace ER nakonec lze uložit, LCS, kde budou moci sdílet s účastníky služby, nebo v provozním prostředí pro vnitřní použití, jako je znázorněno na následujícím obrázku. ![Konfigurace omezené ER](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Viz také
--------

[Přehled elektronického výkaznictví](general-electronic-reporting.md)




