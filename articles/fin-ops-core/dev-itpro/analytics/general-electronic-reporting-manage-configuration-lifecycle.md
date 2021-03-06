---
title: Správa životního cyklu konfigurace elektronického vykazování
description: Toto téma popisuje způsob správy životního cyklu konfigurací elektronického výkaznictví pro řešení Dynamics 365 Finance.
author: NickSelin
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52aba53b5323a9c6c4331cd8de7e932bb9c3547e
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893194"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Správa životního cyklu konfigurace elektronického vykazování

[!include [banner](../includes/banner.md)]

Toto téma popisuje způsob správy životního cyklu konfigurací elektronického výkaznictví pro řešení Dynamics 365 Finance.

## <a name="overview"></a>Přehled

Elektronické výkaznictví je modul pro podporu elektronických dokumentů specifických pro danou zemi a požadovaných zákonem. Obecně platí, že Elektronické výkaznictví předpokládá schopnost provádět následující činnosti pro jeden elektronický dokument. Další podrobnosti získáte v tématu [Přehled elektronického výkaznictví (ER)](general-electronic-reporting.md)

- Návrh šablony pro elektronický dokument:

    - Identifikace požadovaných zdrojů dat, které lze zpřístupnit v tomto dokumentu:

        - Základní data, například datové tabulky, datové entity a třídy.
        - Vlastnosti určité pro proces jako datum provedení a čas a časové pásmo.
        - Vstupní parametry uživatele definované koncovým uživatelem při spuštění.

    - Definování prvků nezbytných pro dokument a také jejich topologie pro určení konečného formátu dokumentu.
    - Konfigurace požadovaného toku dat z vybraného zdroje dat pro definování prvků dokumentu prostřednictvím součástí formátu vazeb datového zdroje dokumentu a určení logiky procesu řízení.

- Zpřístupněte šablonu tak, aby ji možné použít v jiných instancích:

    - Převeďte šablonu dokumentu, která byla vytvořena v aplikaci Dynamics AX, na konfiguraci elektronického výkaznictví, a exportujte konfiguraci z aktuální instance aplikace jako balíček XML, který může být uložen lokálně nebo v rámci Lifecycle Services (LCS).
    - Převeďte konfiguraci elektronického výkaznictví jako šablonu dokumentu aplikace.
    - Importujte balíček XML, který je uložen místně nebo v rámci LCS do aktuální instance.

- Upravte šablonu elektronického dokumentu:

    - Přeneste šablonu z LCS do aktuální instance jako konfiguraci elektronického výkaznictví.
    - Návrh vlastní verze konfigurace elektronického výkaznictví a uchování odkazu na základní verzi.

- Integrujte šablonu v konkrétním obchodním procesu tak, aby byly k dispozici v aplikaci:

    - Konfigurujte nastavení aplikace tak, aby aplikace začala používat konfiguraci elektronického výkaznictví (vytvořte odkaz na tuto konfiguraci v parametru souvisejícím s procesem). Například odkazujte na konfiguraci elektronického výkaznictví v konkrétní metodě platby závazků s cílem vygenerovat zprávu pro elektronickou platbu pro zpracování faktur.

- Použití šablony v určitém obchodním procesu:

    - Spusťte konfiguraci služby ER do určitého obchodního procesu. Například odkazujte na konfiguraci elektronického výkaznictví ke zpracování fakturu, když je vybraná metoda platby, která odkazuje na konfiguraci ER.

## <a name="concepts"></a>Koncepty
Následující role a související aktivity jsou přidruženy k životním cyklu konfigurace elektronického výkaznictví.

| Role                                       | Aktivity                                                      | popis |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| Funkční konzultant elektronického výkaznictví | Vytvořte a spravujte součásti elektronického výkaznictví (modelů a formáty).           | Obchodní pracovník, který navrhuje modely specifické pro doménu elektronického výkaznictví, navrhuje také požadované šablony pro elektronické dokumenty a vhodně je prováže. |
| Návrhář elektronického výkaznictví             | Vytvořte a spravujte mapování datového modelu.                          | Specialista, který vybere požadované zdroje dat Finance a naváže je modely dat specifických pro doménu elektronického výkaznictví. |
| Účetní supervizor                      | Nakonfigurujte nastavení týkajícího se procesu, které odkazuje na artefakty elektronického výkaznictví. | Například role **Účetní supervizor**, která umožňuje použít nastavení konfigurace elektronického výkaznictví pro konkrétní účty metodu plateb závazků s cílem vygenerovat zprávu elektronické platby pro zpracování faktur. |
| Úředník plateb závazků            | Použijte artefakty elektronického výkaznictví v určitém obchodním procesu.                | Například role **Úředník pro platby závazků**, která umožňuje vygenerovat zprávy elektronických plateb pro zpracování faktur na základě formátu elektronického výkaznictví nastaveného pro konkrétní způsob platby. |

## <a name="er-configuration-development-lifecycle"></a>Životní cyklus vývoje konfigurace elektronického výkaznictví
Je doporučeno navrhovat konfigurace pravidel ve vývojovém prostředí, jako v oddělené instanci Finance and Operations z těchto důvodů souvisejících s elektronickým výkaznictvím:

- Uživatelé mají buď role **Vývojáře elektronického vykazování** nebo **Funkčního konzultanta elektronického výkaznictví**, kteří mohou upravovat konfigurace a spouštět je pro účely testování. To může způsobit volání metod tříd a tabulek, které mohou být potenciálně škodlivé pro obchodní data a výkon použití instance.
- Volání metod tříd a tabulek jako zdroje dat elektronického výkaznictví nejsou omezeny vstupními body a jsou zaznamenány do obsahu společnosti. Proto citlivá obchodná data mohou zobrazovat uživatelé mající buď roli **Vývojáře elektronického vykazování** nebo **Funkčního konzultanta elektronického výkaznictví**.

Konfigurace elektronického výkaznictví navržené ve vývojovém prostředí je možné [odeslat](#data-persistence-consideration) do testovacího prostředí pro hodnocení konfigurace (správný proces integrace, správnost výsledků, výkonnost) a kontrola kvality (správnost role řídící přístupová práva, dělení zodpovědnosti atd.). Pro tento účel lze použít funkce, které umožňují výměnu konfigurace elektronického výkaznictví. Ověřené konfigurace elektronického výkaznictví je možné uložit buď do LCS pro sdílení se službami odběratelů, nebo je možné je [importovat](#data-persistence-consideration) do provozního prostředí pro interní použití.

![Životní cyklus elektronického výkaznictví](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a><a name="data-persistence-consideration" />Záležitosti perzistence dat

Můžete individuálně [importovat](tasks/er-import-configuration-lifecycle-services.md) různé [verze](general-electronic-reporting.md#component-versioning) [konfigurace](general-electronic-reporting.md#Configuration) ER do vaší finanční instance. Když je importována nová verze konfigurace ER, systém řídí obsah konceptové verze této konfigurace:

   - Když je importovaná verze nižší než nejvyšší verze této konfigurace v aktuální instanci Finance, obsah konceptové verze této konfigurace zůstane nezměněn.
   - Když je importovaná verze vyšší než jakákoli jiná verze této konfigurace v aktuální instanci aplikace Finance, obsah importované verze se zkopíruje do pracovní verze této konfigurace, abyste mohli pokračovat v úpravách poslední dokončené verze.

Pokud je tato konfigurace vlastněna [poskytovatelem](general-electronic-reporting.md#Provider) konfigurace, který je aktuálně aktivován, pracovní verze této konfigurace je pro vás viditelná na rychlé kartě **Verze** na stránce **Konfigurace** (**Správa organizace** > **Elektronické hlášení** > **Konfigurace**). Můžete vybrat pracovní verzi konfigurace a [upravit](er-quick-start2-customize-report.md#ConfigureDerivedFormat) její obsah pomocí příslušného návrháře ER. Když jste upravili pracovní verzi konfigurace ER, její obsah již neodpovídá obsahu nejvyšší verze této konfigurace v aktuální instanci Finance. Aby se zabránilo ztrátě vašich změn, systém zobrazí chybu, že import nemůže pokračovat, protože verze této konfigurace je vyšší než nejvyšší verze této konfigurace v aktuální instanci Finance. Když k tomu dojde, například s konfigurací formátu **X**, zobrazí se chyba **Verze formátu „X“ není dokončena**.

Chcete-li vrátit zpět změny, které jste provedli v pracovní verzi, vyberte nejvyšší dokončenou nebo sdílenou verzi vaší konfigurace ER v aplikaci Finance na rychlé kartě **Verze** a poté vyberte možnost **Získat tuto verzi**. Obsah vybrané verze se zkopíruje do pracovní verze.

## <a name="additional-resources"></a>Další prostředky

[Přehled elektronického výkaznictví](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
