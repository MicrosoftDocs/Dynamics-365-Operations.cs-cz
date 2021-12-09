---
title: Analytické nástroje Commerce (Preview)
description: Toto téma vysvětluje, jak nainstalovat a používat funkci analýzy v Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 11/23/2021
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 8cfe2af756315b5be3eb22d99376a96166fffc52
ms.sourcegitcommit: f9fca3d55b47e615e5ef64669dab184e057ec234
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/23/2021
ms.locfileid: "7862766"
---
# <a name="commerce-analytics-preview"></a>Analytické nástroje Commerce (Preview)

[!include [banner](includes/banner.md)]

Toto téma vysvětluje, jak nainstalovat analýzu Commerce (Preview), funkci funkční analýzy, která je součástí Microsoft Dynamics 365 Commerce.

## <a name="commerce-analytics-preview-live-demo"></a>Živá ukázka Analytických nástrojů Commerce (Preview)

Můžete vyzkoušet [živou ukázku Analytických nástrojů Commerce (Preview)](https://aka.ms/CommerceAnalyticsDemo).

![Shrnutí Analytických nástrojů Commerce (Preview)](media/CommerceAnalytics_Summary.png)
![Platby Analytických nástrojů Commerce (Preview)](media/CommerceAnalytics_Payments.png)
![Webová aktivita Analytických nástrojů Commerce (Preview)](media/CommerceAnalytics_WebActivity.png)


## <a name="commerce-analytics-preview-system-architecture"></a>Architektura systému pro Analytické nástroje Commerce (Preview)

### <a name="key-components"></a>Klíčové komponenty

Analytické nástroje Commerce (Preview) se skládá z následujících klíčových komponent:

- Interaktivní sestavy Power BI připravené k použití
- Zobrazení SQL v analýze Azure Synapse
- Data entit a ontologie v Azure Data Lake
- Nezpracovaná data v Azure Data Lake

![Klíčové komponenty architektury systému analýzy Commerce](media/CommerceAnalyticsArchitecture_v2.png)

### <a name="data-flow"></a>Tok dat

#### <a name="step-1-data-generation"></a>Krok 1: Generování dat

Data pocházejí buď jako transakční data, nebo data o chování z jednoho z následujících zdrojů:

- Pracovník call centra používá klienta Commerce HQ ke zpracování prodejních objednávek.
- Pokladník v místě prodeje (POS) zpracovává prodejní transakce.
- Prodeje jsou vytvářeny ve vlastních aplikacích pomocí Headless Commerce (Commerce Scale Unit).
- Nakupující v elektronickém obchodování prohlíží váš web elektronického obchodování.
- Nakupující v elektronickém obchodování zadá objednávku na vašem webu elektronického obchodování.
- Data jsou produkována jinými systémy, jako např. Dynamics 365 Connected Spaces.

#### <a name="step-2-ingestion-and-pre-processing"></a>Krok 2: Přijetí a předběžné zpracování

Transakční data jdou do Commerce HQ buď přímo (v případě objednávek, které jsou zachyceny přímo v klientovi Commerce HQ), nebo prostřednictvím Commerce Scale Unit (v případě objednávek, které jsou zachyceny na POS, v e-shopu nebo ve vlastních klientech, kteří používají Headless Commerce).

Funkce Export do Data Lake se pak používá ke zkopírování transakčních dat do vašeho datového jezera jako nezpracovaná data. V datovém jezeře jsou nezpracovaná data uložena ve složce Tabulky.

Data webové aktivity elektronického obchodu jsou odesílány přímo do datového jezera. Data, která jsou produkována jinými systémy, jako např Dynamics 365 Connected Spaces, jsou těmito systémy odeslána přímo do datového jezera.

#### <a name="step-3-transformation-and-aggregation"></a>Krok 3: Transformace a agregace

Poté, co jsou nezpracovaná data ve vašem datovém jezeře, služba analýzy Commerce je přečte, transformuje, agreguje a zapíše zpět do datového jezera ve formě logických entit (ve složce Entity) a agregovaných metrik (ve složce Ontologie).

#### <a name="step-4-querying"></a>Krok 4: Dotazování

Analýza Azure Synapse se používá k dotazování na data ve vašem datovém jezeře prostřednictvím rozhraní Transact-SQL (T-SQL). Toto rozhraní zahrnuje zobrazení SQL. Zobrazení SQL umožňují federované dotazování na data v datovém jezeře, a to buď přímo prostřednictvím klienta T-SQL (pro ad-hoc analýzu) nebo prostřednictvím vizualizačního nástroje, jako je např. Power BI.

#### <a name="step-5-modeling-and-serving"></a>Krok 5: Modelování a obsluhování

Data, která jsou dotazována Analýzou Azure Synapse jdou do sémantického modelu Power BI. V závislosti na typu dat se buď pravidelně importují v paměti do Power BI nebo přímo v modulu runtime.

Nakonec jsou data vykreslena ve vizuálech Power BI, aby je uživatelé mohli prohlížet a pracovat s nimi.

## <a name="commerce-analytics-preview-functional-overview"></a>Přehled funkcí analýzy Commerce (Preview)

### <a name="summary"></a>Souhrn

Aplikace šablony analýzy Commerce obsahuje následující hlavní stránky sestav:

1. [Filtry nejvyšší úrovně](#TopLevelFilters)
2. [Produkty](#ProductsPage)
3. [Odběratelé](#CustomersPage)
4. [Kanály](#ChannelsPage)
5. [Prodej.](#SalesPage)
6. [Okraje](#MarginsPage)
7. [Vrácení](#ReturnsPage)
8. [Slevy](#DiscountsPage)
9. [Platby](#PaymentsPage)
10. [Odběratelé](#CustomersPage)
11. [Porovnání](#ComparisonPage)
12. [Webová aktivita](#WebActivityPage)
13. [Aktivita na webu – Filtr nejvyšší úrovně](#WebActivityTopLevelFilters)

####  <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Filtry nejvyšší úrovně

- Nastavení data

    - Rok
    - Čtvrtletí
    - Měsíc
    - Týden
    - Den

- Nastavení kanálu

    - Právnická osoba
    - Typ kanálu
    - Typ zákazníka
    - Typ prodeje
    - Kanál
    - Organizační hierarchie

- Nastavení produktů

    - Hierarchie kategorií
    - Kategorie

####  <a name="products"></a><a name="ProductsPage"></a> Produkty

- Prodej
- Okraj
- Vrácení

####  <a name="customers"></a><a name="CustomersPage"></a> Odběratelé

- Prodej
- Okraj
- Vrácení

#### <a name="channels"></a><a name="ChannelsPage"></a> Kanály

- Prodej
- Okraj
- Vrácení

### <a name="sales"></a>Prodej <a name="SalesPage"></a>

- Podle místa doručení
- Podle kanálu/obchodu/terminálu
- Podle zaměstnance
- Podle data
- Podle hodiny
- Podle kategorie produktů

### <a name="margins"></a><a name="MarginsPage"></a> Marže

- Podle místa doručení
- Vedlejší produkt
- Podle data

### <a name="returns"></a><a name="ReturnsPage"></a> Vratky

- Vratka dle částky

    - Podle obchodu
    - Vedlejší produkt
    - Podle data

- Vratja podle transakce

    - Podle obchodu
    - Vedlejší produkt
    - Podle data

### <a name="discounts"></a><a name="DiscountsPage"></a> Slevy

- Podle obchodu
- Vedlejší produkt
- Podle data
- Dekompozice

    - Právnická osoba
    - Obchod
    - Typ slevy
    - Název slevy
    - Produkt

### <a name="payments"></a><a name="PaymentsPage"></a> Platby

- Podle kanálu/terminálu
- Podle způsobu platby/typu
- Podle data
- Dekompozice

    - Právnická osoba
    - Typ kanálu
    - Obchod
    - Terminál
    - Způsob platby

### <a name="customers"></a><a name="CustomersPage"></a> Odběratelé

- Celoživotní hodnota zákazníků (LTV)

    LTV se počítá na základě celkové částky, kterou zákazník utratí napříč všemi prodejními kanály Dynamics 365 Commerce (včetně POS, elektronického obchodování a call centra).

- Recency

    Recency se počítá na základě počtu dní od poslední transakce zákazníka s organizací. Recency v současnosti nebere v úvahu signály netransakčního zapojení, jako je například procházení elektronického obchodu.

- Frekvence

    Frekvence se počítá na základě transakcí zákazníka s organizací. Frekvence v současnosti nebere v úvahu signály netransakčního zapojení, jako je například procházení elektronického obchodu.

- Délka vztahů

    Délka vztahu se počítá na základě počtu dní od vytvoření záznamu zákazníka v systému.

- Počet transakcí

### <a name="comparison"></a><a name="ComparisonPage"></a> Porovnání

- Srovnání produktů podle časového období

    - Prodeje a rozdíly v prodeji
    - Marže a rozdíly v marží

- Zákazník podle období

    - Prodeje a rozdíly v prodeji
    - Marže a rozdíly v marží

### <a name="web-activity"></a><a name="WebActivityPage"></a> Webová aktivita

#### <a name="top-level-filters"></a><a name="WebActivityTopLevelFilters"></a> Filtry nejvyšší úrovně

- Rozsah dat
- Typ kanálu
- Kanál
- Hierarchie kategorií

#### <a name="acquisitions"></a>Pořízení

- Zobrazení stránek

    - Podle země nebo oblasti
    - Vedlejší produkt
    - Podle stavu přihlášeného uživatele
    - Podle data

- Objednávky elektronického obchodu
- Míra konverze

    - Podle data

- Převodní trychtýř

    - Zobrazení stránky podle typu stránky (domovská stránka, stránka kategorie nebo stránka s podrobnostmi o produktu)
    - Přidat do vozíku
    - Přejít k pokladně
    - Nákup

#### <a name="sessions"></a>Relace

Relace je epizoda návštěvy uživatele na vašem webu elektronického obchodu. Relace se považuje za ukončenou po 30 minutách nečinnosti nebo 24 hodinách aktivního používání.

- Podle země nebo oblasti
- Podle původu (externí odkazující)
- Podle stavu přihlášeného uživatele
- Počet relací

    - Podle data
    - Podle vstupní stránky

- Objednávka dle relace

    - Podle data

- Míra odrazů relace

    Odraz relace je relace, kdy uživatel odejde ihned poté, co navštíví váš web elektronického obchodu. Další informace naleznete v tématu [Míra odrazů](https://en.wikipedia.org/wiki/Bounce_rate).

- Kliknutí dle relace

#### <a name="visitors"></a>Návštěvníci

Anonymní návštěvník na vašem webu elektronického obchodu je jednoznačně identifikován na základě konkrétního prohlížeče a konkrétního zařízení, které uživatel používá. Analýza Commerce nesleduje anonymní návštěvníky napříč různými prohlížeči nebo zařízeními. Anonymní návštěvník, který používá stejný prohlížeč na stejném zařízení, je jedinečně identifikován napříč více uživatelskými relacemi, dokud nebudou vymazána data v mezipaměti prohlížeče nebo neuplyne období (obvykle 12 měsíců), podle toho, co nastane dříve.

Pokud návštěvníci procházejí váš web elektronického obchodu, když jsou přihlášeni, analýza Commerce o nich může poskytnout další informace. Tyto informace jsou založeny na stávajícím vztahu, který má vaše organizace s návštěvníky v důsledku jejich předchozích nákupů napříč všemi prodejními kanály Dynamics 365 Commerce (včetně POS, elektronického obchodování a call centra). Mezi další informace patří aktuálnost, délka vztahu, celoživotní hodnota zákazníků a údaje o frekvenci.

- Návštěvnická marže
- Průměrné objednávky návštěvníků
- Průměrné prodeje návštěvníků
- Počet návštěvníků elektronického obchodu

    - Podle data
    - Podle umístění

        V současné době může analýza Commerce poskytovat návštěvníkům elektronického obchodu podrobnosti o poloze pouze na úrovni země/oblasti.

    - Podle aktuálnosti

        Recency se počítá na základě počtu dní od poslední transakce zákazníka s organizací. Recency v současnosti nebere v úvahu signály netransakčního zapojení, jako je například procházení elektronického obchodu.

    - Podle délky vztahů

        Délka vztahu se počítá na základě počtu dní od vytvoření záznamu zákazníka v systému.

    - Podle celoživotní hodnoty zákazníků (LTV)

        LTV se počítá na základě celkové částky, kterou zákazník utratí napříč všemi prodejními kanály Dynamics 365 Commerce (včetně POS, elektronického obchodování a call centra).

    - Podle frekvence

        Frekvence se počítá na základě transakcí zákazníka s organizací. Frekvence v současnosti nebere v úvahu signály netransakčního zapojení, jako je například procházení elektronického obchodu.

#### <a name="impressions"></a>Zobrazení

Jedná se o jediné zobrazení vizuálu produktu návštěvníkem elektronického obchodu. Návštěvník elektronického obchodu například přejde na domovskou stránku vašeho webu elektronického obchodování a prohlédne si produkt podložky na jógu v modulu seznamu **Nejprodávanější**. Návštěvník si poté prohlédne stejný produkt podložky na jógu v modulu seznamu **Výběr pro vás**. V tomto případě se jedná o dvě zorbazení produktu. 

V současné době jsou zobrazení sledována na následujících platformách:

- Seznamy (např. **Doporučeno**, **Nejprodávanější**, **Výběr pro vás** a **Trendy**)
- Modul košíku
- Kontejner výsledků hledání
- Kontejner výsledků hledání kategorií

V současné době se produkty, které jsou vykresleny v karuselovém modulu nebo ve vlastních vizuálech, nezapočítávají do metrik souvisejících se zobrazením.

Stránka **Sestava zobrazení** obsahuje následující metriky:

- Počet zobrazení

    - Podle typu stránky a modulu

        Typ stránky je obecný typ stránky, který je definován pro každou stránku na vašem webu elektronického obchodu. Typ modulu je typ vizuálního modulu elektronického obchodu, ve kterém je produkt zobrazen.

        Chcete-li vidět zobrazení podle modulu, možná budete muset přejít na stránku a vizuály modulu.

    - Vedlejší produkt
    - Podle stavu přihlášeného uživatele
    - Podle data

- Počet kliknutí zobrazení

    Ke kliknutí zobrazení dochází, když si návštěvník elektronického obchodu vybere vizuál produktu. Návštěvník se poté obvykle dostane na stránku s podrobnostmi o produktu.

- Míra prokliku zobrazení (CTR)

    CTR se vypočítá jako celkový počet kliknutí na zobrazení dělený celkovým počtem zobrazení.

## <a name="commerce-analytics-preview-installation"></a>Instalace Analýzy Commerce (Preview)

> [!NOTE]
> Analýza Commerce (Preview) je ve verzi Preview v USA, Kanadě, Spojeném království, Evropě, jihovýchodní Asii, východní Asii, Austrálii a Japonsku. Pokud je vaše prostředí Finance and Operations v kterékoli z těchto oblastí, můžete tuto funkci ve svém prostředí povolit pomocí Microsoft Dynamics Lifecycle Services (LCS). Před použitím této funkce si přečtěte [Nakonfigurujte export do Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>Povolit a nakonfigurovat analýzu Commerce (Preview)

Chcete-li nainstalovat analýzu Commerce (Preview), musíte mít oprávnění k vytváření prostředků v předplatném Azure. Musíte mít také oprávnění k instalaci doplňků v LCS. Zde je přehled kroků:

1. [Odešlete formulář pro příjem Preview pro analýzu Commerce (Preview)](#joinPreview).
2. [Povolení a konfigurace doplňku Export do Data Lake](#enableExportToDataLake).
3. [Povolit a nakonfigurovat doplněk analýzy Commerce (Preview)](#enableCommerceAnalyticsAddin).
4. [Vygenerujte si token sdíleného přístupového podpisu (SAS) pro svůj účet úložiště](#getSASToken).
5. [Stáhněte si skripty nasazení pro zobrazení Azure Synapse](#downloadSynapseDeploymentScripts).
6. [Nainstalujte a nakonfigurujte Azure Synapse workspace](#configureAzureSynapse).
7. [Instalace aplikace šablony Power BI](#powerbi).

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a>Odešlete formulář pro příjem Preview pro analýzu Commerce (Preview)

Odešlete [formulář pro příjem Preview pro analýzu Commerce (Preview)](https://forms.office.com/r/vW5VLJGXZ2). Zpracování formuláře může trvat až tři pracovní dny. Po jeho zpracování bude na e-mailovou adresu, kterou jste uvedli ve formuláři, zaslán potvrzovací e-mail.

### <a name="enable-and-configure-export-to-data-lake"></a><a name="enableExportToDataLake"></a>Povolení a konfigurace doplňku Export do Data Lake.

Analýza Commerce (Preview) spoléhá na funkci Export do Data Lake, která exportuje data Commerce HQ do Data Lake a udržuje data aktuální. Než nakonfigurujete analýzu Commerce (Preview), povolte a nakonfigurujte Export do Data Lake podle kroků v [Konfiguraci exportu do Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

Při konfiguraci exportu do Data Lake si poznamenejte následující informace, protože je budete muset zadat později:

- <a name="keyVault"></a>Název systému DNS (Domain Name System) trezoru klíčů a názvy tajných kódů, kam ukládáte ID aplikace a tajný klíč aplikace. Další informace viz [Přidat tajné kódy do trezoru klíčů](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).
- <a name="storageAccount"></a>Název účtu úložiště pro instanci Data Lake. Více informací viz [Ve vašem předplatném si vytvořte účet Data Lake Storage (Gen2)](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription).

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a>Povolit a nakonfigurovat doplněk analýzy Commerce (Preview).

Chcete-li nainstalovat doplněk analýzy Commerce (Preview) v LCS, musíte být správcem prostředí v LCS pro prostředí, které plánujete používat.

K instalaci a konfiguraci doplňku analýzy Commerce (Preview), postupujte následovně.

1. Přihlaste se do [LCS](https://lcs.dynamics.com/) a přejděte do svého prostředí.
2. Na stránce **Prostředí** na kartě **Doplňky prostředí** vyberte **Nainstalujte nový doplněk**.
3. V dialogovém okně vyberte **Analýza Commerce (Preview)**.

    Pokud není **Analýza Commerce (Preview)** uvedena v seznamu, ujistěte se, že jste se připojili k programu Insider.

4. V dialogovém okně **Doplněk nastavení** zadejte následující údaje.

    | Informace | Zdroj | Ukázková hodnota |
    |---|---|---|
    | ID klienta Azure AD pro vaše prostředí | Přihlaste se do [Portálu Azure](https://portal.azure.com/) a otevřete službu **Azure Active Directory**. Poté otevřete stránku **Vlastnosti** a zkopírujte hodnotu do pole **ID adresáře**. | 72f988bf-0000-0000-00000-2d7cd011db47 |
    | Název DNS vašeho trezoru klíčů | Zadejte [název DNS](#keyVault) vašeho trezoru klíčů. Tuto hodnotu jste si měli poznamenat v předchozí části. | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Tajný kód, který obsahuje ID aplikace | Zadejte [tajný kód, který ukládá ID aplikace](#keyVault). Tuto hodnotu jste si měli poznamenat v předchozí části. | app-id |
    | Tajný kód, který obsahuje tajný klíč aplikace | Zadejte [tajný kód, který ukládá tajný kód aplikace](#keyVault). Tuto hodnotu jste si měli poznamenat v předchozí části. | app-secret |

5. Přijměte podmínky nabídky zaškrtnutím políčka a poté vyberte **Instalovat**.

    Systém nainstaluje a nakonfiguruje doplněk analýzy Commerce (Preview) pro dané prostředí. Tento proces může trvat několik minut. Po jeho dokončení **Analýzy (Preview)** by měly být uvedeny na stránce **Prostředí** a stav by měl být **Instalováno**.

### <a name="generate-a-sas-token-for-your-storage-account"></a><a name="getSASToken"></a>Vygenerujte si token SAS pro svůj účet úložiště

Token SAS umožňuje externím subjektům přistupovat k vašemu účtu úložiště a mít určitou sadu oprávnění po omezenou dobu. Azure Synapse použije token SAS pro přístup k podkladovým datům v Data Lake.

> [!NOTE]
> Kvůli známému omezení analýzy Commerce (Preview) instance Azure Synapse ztratí přístup k datovému jezeru, když vyprší platnost tokenu SAS. Proto byste při generování tokenu SAS měli nastavit maximální datum vypršení platnosti, které povolují zásady zabezpečení vaší organizace.

Ke generování tokenu SAS postupujte následovně.

1. V portálu Azure přejděte na [účet úložiště](#storageAccount), které jste vytvořili při konfiguraci Export do Data Lake.
2. V levém podokně pod účtem úložiště vyberte **Sdílený přístupový podpis**.
3. Na stránce **Možnosti SAS** zadejte následující pole.

    | Pole | Hodnota |
    |---|---|
    | Povolené služby | Vyberte **Blob**. |
    | Povolené typy prostředků | Vyberte **Servis**, **Kontejner** a **Objekt**. |
    | Povolená oprávnění | Vyberte **Číst**, **Psát**, **Odstranit**, **Seznam**, **Přidat** a **Vytvořit**. |
    | Oprávnění ke správě verzí objektů Blob | Vyberte **Umožňuje mazání verzí**. |
    | Datum/čas začátku a ukončení platnosti | Podle potřeby nastavte počáteční a koncové datum a čas pro token SAS. |
    | Povolené IP adresy | Pole ponechejte prázdné. |
    | Povolené protokoly | Vyberte **pouze HTTPS**. |
    | Preferovaná úroveň směrování | Vyberte **Základní (výchozí)**. |
    | Podpisový klíč | Vyberte **key1** nebo **key2** podle potřeby. |

4. Vyberte **Vygenerovat SAS a připojovací řetězec**.
5. Zkopírujte hodnotu v poli **Token SAS** a vložte jej do textového editoru, jako je Poznámkový blok.

### <a name="download-the-deployment-scripts-for-azure-synapse-views"></a><a name="downloadSynapseDeploymentScripts"></a>Stáhněte si skripty nasazení pro zobrazení Azure Synapse.

Chcete-li vytvořit a publikovat požadovaná zobrazení v Azure Synapse workspace, musíte spustit sadu skriptů. Podle těchto pokynů stáhněte skripty.

1. Na GitHubu přejděte do úložiště [Microsoft/Dynamics365Commerce.Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions).
2. Stáhněte si skripty do místního počítače naklonováním úložiště nebo jej stáhněte jako soubor zip.

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a>Nainstalujte a nakonfigurujte Azure Synapse workspace.

Chcete-li nainstalovat a konfigurovat Azure Synapse workspace, postupujte dle těchto kroků.

1. Nainstalujte Azure Synapse workspace ve vašem předplatném Azure. Další informace naleznete v tématu [Rychlý start: Vytvoření Synapse workspace](/azure/synapse-analytics/quickstart-create-workspace).
2. V programu Poznámkový blok nebo jiném textovém editoru otevřete soubor skriptu **SetupSynapse.sql** ze složky v místním počítači, do které jste naklonovali nebo stáhli úložiště Dynamics365Commerce.Solutions v předchozí části. Soubor skriptu bude ve složce /Pipeline/CommerceAnalyticsSynapse/. Ve skriptu nahraďte zástupný text hodnotami, jak je uvedeno v následující tabulce.

    | Zástupný text | Hodnota náhrady |
    |---|---|
    | placeholder_storageaccount | Název [účtu úložiště](#storageAccount), který jste vytvořili při konfiguraci Export do Data Lake. |
    | <a name="phContainer"></a>zástupný kontejner | Název kontejneru úložiště, který byl vytvořen ve vaší instanci Data Lake poté, co jste úspěšně nainstalovali doplněk Export do Data Lake v LCS. Chcete-li získat název kontejneru, musíte k procházení účtu úložiště použít Průzkumníka úložiště v Azure Portal. |
    | placeholder_sastoken | [Token SAS](#getSASToken), který jste vytvořili. Nezapomeňte odstranit otazník (**?**) ze začátku hodnoty tokenu SAS. |
    | <a name="phUserPwd"></a>placeholder_password | Silné heslo dle vašeho výběru. Poznamenejte si toto heslo. Bude nastaveno jako heslo pro nový účet **reportreadonlyuser**, který skript vytvoří. **Nezadávejte** heslo k účtu **sqladminuser**. |

3. Zkopírujte aktualizovaný obsah souboru skriptu.
4. Na portálu Azure přejděte do nového Azure Synapse workspace. Na stránce **Přehled** vyberte **Otevřete Synapse Studio**.
5. V Synapse Studio vyberte **Nový \> SQL skript** a vložte obsah souboru skriptu do editoru skriptů SQL.
6. Ujistěte se, že pole **Použít databáze** je nastaveno na **master**.
7. Vyberte **Spustit** a počkejte, až skript skončí. Úspěšné spuštění skriptu vytvoří databázi pro analýzu Commerce, přihlašovací údaje pro přístup k datovému jezeru a uživatelský účet pouze pro čtení, který Power BI použije k připojení k instanci Azure Synapse.
8. Na místním počítači otevřete Windows PowerShell v režimu správce a přejděte do složky /Pipeline/CommerceAnalyticsSynapse/ ve složce, do které jste naklonovali nebo stáhli úložiště Dynamics365Commerce.Solutions.
9. Spuštěním následujícího příkazu nastavte zásady spouštění prostředí Windows PowerShell.

    ```powershell
    Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
    ```

10. Pokud modul SQL Server PowerShell ještě není nainstalován, nainstalujte jej spuštěním následujícího příkazu.

    ```powershell
    Install-Module sqlserver
    ```

    > [!NOTE]
    > Během instalace modulu můžete být vyzváni k instalaci poskytovatele NuGet. V tomto případě vyberte **Y** k inastalaci poskytovatele NuGet. Můžete být také vyzváni, abyste potvrdili, že instalujete moduly z nedůvěryhodného úložiště. V tomto případě vyberte **Y** a pokračujte v instalaci. Volitelně můžete spustit rutinu **Set-PSRepository**, aby důvěřovala úložišti **PSGallery**.

11. Publikujte zobrazení Azure Synapse spuštěním následujícího příkazu.

    ```powershell
    .\PublishSynapseViews.ps1 -serverName SERVER_NAME -password PASSWORD -storageAccount STORAGE_ACCOUNT -containerName CONTAINER_NAME -datarootpath DATA_ROOT_PATH
    ```

    Když spustíte tento příkaz, nahraďte zástupné hodnoty, jak je uvedeno v následující tabulce.

    | Hodnota zástupného textu | Hodnota náhrady |
    |---|---|
    | SERVER_NAME | Název koncového bodu bezserverové SQL Azure Synapse. Tuto hodnotu můžete získat ze stránky **Přehled** pro Azure Synapse workspace na Azure Portal. |
    | PASSWORD | Heslo pro účet **sqladminuser**. |
    | STORAGE_ACCOUNT | Název účtu úložiště pro Data Lake. |
    | CONTAINER_NAME | Název kontejneru, který byl vytvořen funkcí Export do Data Lake. Tento kontejner je stejný kontejner, který jste zadali jako hodnotu [placeholder_container](#phContainer) v kroku 2. |
    | DATA_ROOT_PATH | Název složky pod kontejnerem, který obsahuje všechna data. |

    > [!NOTE]
    > Název účtu úložiště, název kontejneru a cestu ke kořenu dat můžete najít pomocí prohlížeče Azure Storage a účtu úložiště Data Lake na Azure Portal.

12. Počkejte, až skript skončí. Úspěšné spuštění skriptu vytvoří zobrazení SQL v bezserverové SQL instanci Azure Synapse.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a>Instalace aplikace šablony Power BI

K instalaci aplikace šablony Power BI analýzy Commerce (Preview) postupujte následovně.

1. Přihlaste se do [portálu Power BI](https://powerbi.microsoft.com/) pomocí ID vaší organizace.
2. Instalujte aplikaci šablony Power BI analýzy Commerce (Preview) přechodem na [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Může se zobrazit upozornění, že aplikace není uvedena v seznamu v AppSource. Vyberte **Instalovat**.
3. Pokud aplikaci instalujete poprvé, přejděte ke kroku 5. Pokud jste tuto aplikaci již dříve nainstalovali, zobrazí se následující možnosti aktualizace aplikace:

    - **Aktualizujte pracovní prostor a aplikaci** – Aktualizujte stávající aplikaci šablony a přepište stávající nastavení aplikace, jako je název instance aplikace a konfigurace oprávnění.
    - **Aktualizujte pouze obsah pracovního prostoru bez aktualizace aplikace** – Aktualizujte stávající aplikaci šablony, ale ponechte stávající nastavení aplikace. *Tato možnost je doporučenou možností pro aktualizace aplikací.*
    - **Nainstalujte další kopii aplikace do nového pracovního prostoru** – Vytvořte nový pracovní prostor a poté v něm vytvořte kopii stávající aplikace šablony. Stávající pracovní prostor zůstane nedotčen.

4. Vyberte jednu z možností aktualizace a poté vyberte **Instalovat**.
5. Otevřete nainstalovanou aplikaci výběrem **Aplikace** v levém podokně a poté vyberte aplikaci.
6. Připojte aplikaci ke zdroji dat výběrem **Připojit**. Pokud jste aplikaci již nainstalovali, vyberte odkaz **Připojte svá data** ve žluté liště zpráv.
7. Nastavte následující pole.

    | Pole | Hodnota |
    |---|---|
    | Server | Zadejte název koncového bodu bezserverové SQL Azure Synapse, který jste vytvořili v předchozí části. Tuto hodnotu můžete získat ze stránky **Přehled** pro Azure Synapse workspace na Azure Portal. |
    | Databáze | Zadejte **CommerceAnalytics**. |
    | Jazyk | Vyberte hodnotu ze seznamu. Toto pole se používá pro lokalizované názvy produktů a kategorií. U hodnoty je rozlišována velikost písmen. |
    | Rozsah dat | Vyberte hodnotu ze seznamu. Data za vybraný počet měsíců budou importována do datové sady Power BI. Hodnota, kterou vyberete, ovlivňuje velikost datové sady a čas potřebný pro synchronizaci. |

8. Zvolte **Další**. Budete vyzváni k zadání přihlašovacích údajů pro připojení k SQL databáze Azure Synapse. Nastavte pole, jak je popsáno v následující tabulce.

    | Pole | Hodnota |
    |---|---|
    | Metoda ověřování | Vyberte **Základní**. |
    | Uživatelské jméno | Vstupte **reportreadonlyuser**. |
    | Heslo | Zadejte hodnotu, kterou jste nahradili zástupný symbol [placeholder_password](#phUserPwd) ve skriptu SetupSynapse.sql. Toto heslo platí pro účet **reportreadonlyuser**. |

9. Vyberte **Přihlaste se a připojte se**.
10. Počkejte, dokud nebude datová sada úspěšně aktualizována. Poté vyberte tlačítko **Upravit aplikaci** a otevřete pracovní plochu aplikace, kde můžete zobrazit stav aktualizace datové sady. V pracovním prostoru aplikace můžete také volitelně nastavit automatické plány aktualizací pro svou datovou sadu, spravovat oprávnění a přejmenovat instanci aplikace.

### <a name="privacy"></a><a name="privacy"></a>Důvěrnost

Ochrana vašich osobních údajů je pro nás důležitá. Chcete-li se dozvědět více, přečtěte si naše [Prohlášení o ochraně osobních údajů](https://go.microsoft.com/fwlink/?LinkId=521839).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
