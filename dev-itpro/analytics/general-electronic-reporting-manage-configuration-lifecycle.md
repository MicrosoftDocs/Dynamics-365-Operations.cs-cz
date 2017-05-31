---
title: "Správa životního cyklu konfigurace elektronického vykazování"
description: "Toto téma popisuje způsob správy životního cyklu konfigurací elektronického výkaznictví pro řešení Microsoft Dynamics 365 for Operations."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: cecbb5bd57aa24a942d10241bd83e4c1996a3805
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Správa životního cyklu konfigurace elektronického vykazování

[!include[banner](../includes/banner.md)]


Toto téma popisuje způsob správy životního cyklu konfigurací elektronického výkaznictví pro řešení Microsoft Dynamics 365 for Operations.

<a name="overview"></a>Přehled
--------

Elektronické výkaznictví je modul pro podporu elektronických dokumentů specifických pro danou zemi a požadovaných zákonem v aplikaci Microsoft Dynamics 365 for Operations. Obecně platí, že Elektronické výkaznictví předpokládá schopnost provádět následující činnosti pro jeden elektronický dokument. Další podrobnosti získáte v tématu [Přehled elektronického vykazování](general-electronic-reporting.md)

-   Návrh šablony pro elektronický dokument:
    -   Identifikace požadovaných zdrojů dat, které lze zpřístupnit v tomto dokumentu:
        -   Základní data aplikace Dynamics 365 for Operations jako datové tabulky, data entit a třídy.
        -   Vlastnosti určité pro proces jako datum provedení a čas a časové pásmo.
        -   Vstupní parametry uživatele definované koncovým uživatelem při spuštění.
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
    -   Konfigurujte nastavení aplikace Dynamics 365 for Operations tak, aby aplikace začala používat konfiguraci elektronického výkaznictví odkazem na tuto konfiguraci v parametru souvisejícím s procesem. Například odkazujte na konfiguraci elektronického výkaznictví v konkrétní metodě platby závazků s cílem vygenerovat zprávu pro elektronickou platbu pro zpracování faktur.
-   Použití šablony v určitém obchodním procesu:
    -   Spusťte konfiguraci služby ER do určitého obchodního procesu. Například odkazujte na konfiguraci elektronického výkaznictví ke zpracování fakturu, když je vybraná metoda platby, která odkazuje na konfiguraci ER.

## <a name="concepts"></a>Koncepty
Následující role a související aktivity jsou přidruženy k životním cyklu konfigurace elektronického výkaznictví.

| Role                                       | Aktivity                                                      | popis                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funkční konzultant elektronického výkaznictví | Vytvořte a spravujte součásti elektronického výkaznictví (modelů a formáty).           | Obchodních osoba, která navrhuje modely specifické pro doménu elektronického výkaznictví, navrhuje také požadované šablony pro elektronické dokumenty a vhodně je prováže.                                                                           |
| Návrhář elektronického výkaznictví             | Vytvořte a spravujte mapování datového modelu.                          | Specialista Dynamics 365 for Operations, který vybere požadované zdroje dat pro aplikaci Dynamics 365 for Operations a naváže je modely dat specifických pro doménu elektronického výkaznictví.                                                                 |
| Účetní supervizor                      | Nakonfigurujte nastavení týkajícího se procesu, které odkazuje na artefakty elektronického výkaznictví. | Například role **Účetní supervizor**, která umožňuje použít nastavení konfigurace elektronického výkaznictví pro konkrétní účty metodu plateb závazků s cílem vygenerovat zprávu elektronické platby pro zpracování faktur. |
| Úředník plateb závazků            | Použijte artefakty elektronického výkaznictví v určitém obchodním procesu.                | Například role **Úředník pro platby závazků**, která umožňuje vygenerovat zprávy elektronických plateb pro zpracování faktur na základě formátu elektronického výkaznictví nastaveného pro konkrétní způsob platby.           |

## <a name="er-configuration-development-lifecycle"></a>Životní cyklus vývoje konfigurace elektronického výkaznictví
Je doporučeno navrhovat konfigurace pravidel ve vývojovém prostředí, jako v oddělené instanci aplikace 365 for Operations z těchto důvodů souvisejících s elektronickým výkaznictvím:

-   Uživatelé mají buď role **Vývojáře elektronického vykazování** nebo **Funkčního konzultanta elektronického výkaznictví**, kteří mohou upravovat konfigurace a spouštět je pro účely testování. To může způsobit volání metod tříd a tabulek, které mohou být potenciálně škodlivé pro obchodní data a výkon použití instance Dynamics 365 for Operations.
-   Volání metod tříd a tabulek jako zdroje dat elektronického výkaznictví nejsou omezeny vstupními body Dynamics 365 for Operations a jsou zaznamenány do obsahu společnosti. Proto citlivá obchodná data mohou zobrazovat uživatelé mající buď roli **Vývojáře elektronického vykazování** nebo **Funkčního konzultanta elektronického výkaznictví**.

Konfigurace elektronického výkaznictví navržené ve vývojovém prostředí je možné odeslat do testovacího prostředí pro hodnocení konfigurace (správný proces integrace, správnost výsledků, výkonnost) a kontrola kvality (správnost role řídící přístupová práva, dělení zodpovědnosti atd.). Pro tento účel lze použít funkce, které umožňují výměnu konfigurace elektronického výkaznictví. Ověřené konfigurace elektronického výkaznictví je možné uložit buď do LCS pro sdílení se službami odběratelů nebo do výrobního prostředí pro interní použití, jak ukazuje následující ilustrace. ![Životní cyklus elektronického výkaznictví](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Viz také
--------

[Přehled elektronického výkaznictví](general-electronic-reporting.md)




