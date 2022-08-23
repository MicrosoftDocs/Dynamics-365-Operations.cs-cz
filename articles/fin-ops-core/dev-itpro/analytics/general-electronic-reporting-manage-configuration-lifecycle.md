---
title: Správa životního cyklu konfigurace elektronického vykazování
description: Tento článek popisuje způsob správy životního cyklu konfigurací elektronického výkaznictví pro Dynamics 365 Finance.
author: kfend
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: fe23d4cb2b293af466df2236b153974f95f636f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271576"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Správa životního cyklu konfigurace elektronického vykazování

[!include [banner](../includes/banner.md)]

Tento článek popisuje způsob správy životního cyklu [konfigurací](general-electronic-reporting.md#Configuration) [elektronického výkaznictví](general-electronic-reporting.md) (ER) pro Dynamics 365 Finance.

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
Z následujících důvodů doporučujeme navrhovat konfigurace elektronického výkaznictví ve vývojovém prostředí v oddělené instanci finanční a provozní aplikace:

- Uživatelé mají buď role **Vývojáře elektronického vykazování** nebo **Funkčního konzultanta elektronického výkaznictví**, kteří mohou upravovat konfigurace a spouštět je pro účely testování. To může způsobit volání metod tříd a tabulek, které mohou být potenciálně škodlivé pro obchodní data a výkon použití instance.
- Volání metod tříd a tabulek jako zdroje dat elektronického výkaznictví nejsou omezeny vstupními body a jsou zaznamenány do obsahu společnosti. Proto citlivá obchodná data mohou zobrazovat uživatelé mající buď roli **Vývojáře elektronického vykazování** nebo **Funkčního konzultanta elektronického výkaznictví**.

Konfigurace elektronického výkaznictví navržené ve vývojovém prostředí je možné [odeslat](#data-persistence-consideration) do testovacího prostředí pro hodnocení konfigurace (správný proces integrace, správnost výsledků, výkonnost) a kontrola kvality (správnost role řídící přístupová práva, dělení zodpovědnosti atd.). Pro tento účel lze použít funkce, které umožňují výměnu konfigurace elektronického výkaznictví. Ověřené konfigurace elektronického výkaznictví je možné uložit buď do LCS pro sdílení se službami odběratelů, nebo je možné je [importovat](#data-persistence-consideration) do provozního prostředí pro interní použití.

![Životní cyklus elektronického výkaznictví.](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a>Záležitosti perzistence dat

Můžete individuálně [importovat](tasks/er-import-configuration-lifecycle-services.md) různé [verze](general-electronic-reporting.md#component-versioning) [konfigurace](general-electronic-reporting.md#Configuration) ER do vaší finanční instance. Když je importována nová verze konfigurace ER, systém řídí obsah konceptové verze této konfigurace:

- Když je importovaná verze nižší než nejvyšší verze této konfigurace v aktuální instanci Finance, obsah konceptové verze této konfigurace zůstane nezměněn.
- Když je importovaná verze vyšší než jakákoli jiná verze této konfigurace v aktuální instanci aplikace Finance, obsah importované verze se zkopíruje do pracovní verze této konfigurace, abyste mohli pokračovat v úpravách poslední dokončené verze.

Pokud je tato konfigurace vlastněna [poskytovatelem](general-electronic-reporting.md#Provider) konfigurace, který je aktuálně aktivován, pracovní verze této konfigurace je pro vás viditelná na rychlé kartě **Verze** na stránce **Konfigurace** (**Správa organizace** > **Elektronické hlášení** > **Konfigurace**). Můžete vybrat pracovní verzi konfigurace a [upravit](er-quick-start2-customize-report.md#ConfigureDerivedFormat) její obsah pomocí příslušného návrháře ER. Když jste upravili pracovní verzi konfigurace ER, její obsah již neodpovídá obsahu nejvyšší verze této konfigurace v aktuální instanci Finance. Aby se zabránilo ztrátě vašich změn, systém zobrazí chybu, že import nemůže pokračovat, protože verze této konfigurace je vyšší než nejvyšší verze této konfigurace v aktuální instanci Finance. Když k tomu dojde, například s konfigurací formátu **X**, zobrazí se chyba **Verze formátu „X“ není dokončena**.

Chcete-li vrátit zpět změny, které jste provedli v pracovní verzi, vyberte nejvyšší dokončenou nebo sdílenou verzi vaší konfigurace ER v aplikaci Finance na rychlé kartě **Verze** a poté vyberte možnost **Získat tuto verzi**. Obsah vybrané verze se zkopíruje do pracovní verze.

## <a name="applicability-consideration"></a>Posouzení použitelnosti

Když navrhujete novou verzi konfigurace elektronického výkaznictví, můžete definovat její [závislost](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md) na dalších softwarových komponentách. Tento krok je považován za předpoklad pro řízení stažení této verze konfigurace z úložiště elektronického výkaznictví nebo externího souboru XML a pro další používání této verze. Když se pokusíte importovat novou verzi konfigurace elektronického výkaznictví, systém pomocí nakonfigurovaných předpokladů kontroluje, zda lze verzi importovat.

V některých případech můžete vyžadovat, aby systém při importu nových verzí konfigurací elektronického výkaznictví ignoroval nakonfigurované předpoklady. Chcete -li, aby systém během importu ignoroval předpoklady, postupujte takto.

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
3. Nastavte možnost **Přeskočit kontrolu předpokladů aktualizace a verze produktu při importuí** na **Ano**.

    > [!NOTE]
    > Tento parametr je specifický pro uživatele a konkrétní společnost.

## <a name="dependencies-on-other-components"></a>Závislosti na jiných komponentách

Konfigurace ER lze konfigurovat jako [závislé](er-download-configurations-global-repo.md#import-filtered-configurations) na jiných konfiguracích. Například můžete [importovat](er-download-configurations-global-repo.md) konfiguraci [datového modelu](er-overview-components.md#data-model-component) ER z globálního úložiště do instance [Microsoft Regulatory Configuration Services (RCS)](../../../finance/localizations/rcs-overview.md) nebo Dynamics 365 Finance a poté vytvořit novou konfiguraci [formátu](er-overview-components.md#format-component) ER, která je [odvozená](er-quick-start2-customize-report.md#DeriveProvidedFormat) z importované konfigurace datového modelu ER. Odvozená konfigurace formátu ER bude záviset na konfiguraci základního datového modelu ER.

![Odvozená konfigurace formátu ER na stránce Konfigurace.](./media/ger-configuration-lifecycle-img1.png)

Po dokončení návrhu formátu můžete změnit stav úvodní [verze](general-electronic-reporting.md#component-versioning) konfigurace formátu ER z **Koncept** na **Dokončeno**. Poté můžete sdílet dokončenou verzi konfigurace formátu ER jejím [publikováním](../../../finance/localizations/rcs-global-repo-upload.md) do globálního úložiště. Dále můžete přistupovat ke globálnímu úložišti z libovolné cloudové instance RCS nebo Finance. Poté můžete importovat jakoukoli verzi konfigurace ER, která je použitelná pro aplikaci, z globálního úložiště do této aplikace.

![Publikovaná konfigurace formátu ER na stránce úložiště konfigurace.](./media/ger-configuration-lifecycle-img2.png)

Na základě závislosti na konfiguraci, když vyberete konfiguraci formátu ER v globálním úložišti pro import do nově nasazené instance RCS nebo Finance, bude základní konfigurace datového modelu ER automaticky nalezena v globálním úložišti a importována spolu s vybranou konfigurací formátu ER jako základní konfigurace.

Verzi konfigurace formátu ER můžete také exportovat ze své aktuální instance RCS nebo Finance a uložit ji lokálně jako soubor XML.

![Export verze konfigurace formátu ER jako XML na stránce Konfigurace.](./media/ger-configuration-lifecycle-img3.png)

Ve verzích Finance **před verzí 10.0.29**, když se pokusíte importovat verzi konfigurace formátu ER z tohoto souboru XML nebo z jakéhokoli úložiště jiného než globálního úložiště do nově nasazené instance RCS nebo Finance, která ještě neobsahuje žádné konfigurace ER, bude vyvolána následující výjimka, která informuje, že nelze získat základní konfiguraci:

> Zbývají nevyřešené odkazy<br>
Odkaz objektu „\<imported configuration name\>“ na objekt „Base“ (\<globally unique identifier of the missed base configuration\>, \<version of the missed base configuration\>) nelze navázat

![Import verze konfigurace formátu ER na stránce úložiště konfigurace.](./media/ger-configuration-lifecycle-img4.gif)

Ve verzi **10.0.29 a novější**, když se pokusíte provést stejný import konfigurace a nelze-li základní konfiguraci nalézt v aktuální instanci aplikace nebo ve zdrojovém úložišti, které aktuálně používáte (pokud existuje), rámec ER se automaticky pokusí najít název chybějící základní konfigurace v globální mezipaměti úložiště. Poté v textu vyvolané výjimky představí název a globálně jedinečný identifikátor (GUID) chybějící základní konfigurace.

> Zbývají nevyřešené odkazy<br>
Odkaz objektu „\<imported configuration name\>“ na objekt „Base“ (\<name of the missed base configuration\> \<globally unique identifier of the missed base configuration\>, \<version of the missed base configuration\>) nelze navázat

![Výjimka na stránce úložiště konfigurace, když nelze nalézt základní konfiguraci.](./media/ger-configuration-lifecycle-img5.png)

Zadaný název můžete použít k nalezení základní konfigurace a poté ji ručně importovat.

> [!NOTE]
> Tato nová možnost funguje pouze v případě, že se alespoň jeden uživatel již přihlásil do globálního úložiště pomocí stránky [Úložiště konfigurace](er-download-configurations-global-repo.md#open-configurations-repository) nebo jednoho z polí [vyhledávání](er-extended-format-lookup.md) globálního úložiště v aktuální instanci Finance, a když byl obsah globálního úložiště uložen do mezipaměti.

## <a name="additional-resources"></a>Další prostředky

[Přehled elektronického výkaznictví](general-electronic-reporting.md)

[Definování závislosti konfigurací elektronického výkaznictví na jiných komponentách](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

