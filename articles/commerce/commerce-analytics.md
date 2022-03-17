---
title: Analytické nástroje Commerce (Preview)
description: Toto téma vysvětluje, jak nainstalovat a používat funkci analýzy v Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 02/24/2022
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 7e3721421e15bc3e5937691cdbaee51e4d3cdd17
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349736"
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
- SQL pohledy v Azure Synapse Analytics
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

Transakční data jdou do Commerce HQ buď přímo (v případě objednávek, které jsou zachyceny přímo v klientu Commerce HQ), nebo prostřednictvím Commerce Scale Unit (v případě objednávek, které jsou zachyceny na POS, v e-shopu nebo ve vlastních klientech, kteří používají Headless Commerce).

Funkce Export do Data Lake se pak používá ke zkopírování transakčních dat do vašeho datového jezera jako nezpracovaná data. V datovém jezeře jsou nezpracovaná data uložena ve složce Tabulky.

Data webové aktivity elektronického obchodu jsou odesílány přímo do datového jezera. Data, která jsou produkována jinými systémy, jako např Dynamics 365 Connected Spaces, jsou těmito systémy odeslána přímo do datového jezera.

#### <a name="step-3-transformation-and-aggregation"></a>Krok 3: Transformace a agregace

Poté, co jsou nezpracovaná data ve vašem datovém jezeře, služba analýzy Commerce je přečte, transformuje, agreguje a zapíše zpět do datového jezera ve formě logických entit (ve složce Entity) a agregovaných metrik (ve složce Ontologie).

#### <a name="step-4-querying"></a>Krok 4: Dotazování

Řešení Azure Synapse Analytics se používá k dotazování na data ve vašem datovém jezeře prostřednictvím rozhraní Transact-SQL (T-SQL). Toto rozhraní zahrnuje zobrazení SQL. Zobrazení SQL umožňují federované dotazování na data v datovém jezeře, a to buď přímo prostřednictvím klienta T-SQL (pro ad-hoc analýzu) nebo prostřednictvím vizualizačního nástroje, jako je např. Power BI.

#### <a name="step-5-modeling-and-serving"></a>Krok 5: Modelování a obsluhování

Data, která jsou dotazována řešením Azure Synapse Analytics, jdou do sémantického modelu Power BI. V závislosti na typu dat se buď pravidelně importují v paměti do Power BI nebo přímo v modulu runtime.

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

#### <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Filtry nejvyšší úrovně

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

#### <a name="products"></a><a name="ProductsPage"></a> Produkty

- Prodej
- Okraj
- Vrácení

#### <a name="customers"></a><a name="CustomersPage"></a> Odběratelé

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
> Analýza Commerce (Preview) je ve verzi Preview v USA, Kanadě, Spojeném království, Evropě, jihovýchodní Asii, východní Asii, Austrálii a Japonsku. Pokud je vaše prostředí finančních a provozních aplikací v kterékoli z těchto oblastí, můžete tuto funkci ve svém prostředí povolit pomocí služeb Microsoft Dynamics Lifecycle Services (LCS). Před použitím této funkce si přečtěte [Nakonfigurujte export do Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>Povolit a nakonfigurovat analýzu Commerce (Preview)

Chcete-li nainstalovat analýzu Commerce (Preview), musíte mít oprávnění k vytváření prostředků v předplatném Azure. Musíte mít také oprávnění k instalaci doplňků v LCS. 

Při povolení a konfiguraci doplňku analýzy Commerce (preview), postupujte následovně.

1. [Povolte a konfigurujte doplněk Export do Data Lake](#enableExportToDataLake).
1. [Nainstalujte a nakonfigurujte Azure Synapse workspace](#configureAzureSynapse).
1. [Přidejte tajné kódy do trezoru klíčů](#addSecrets).
1. [Povolit a nakonfigurovat doplněk analýzy Commerce (Preview)](#enableCommerceAnalyticsAddin).
1. [Instalace aplikace šablony Power BI](#powerbi).

### <a name="enable-and-configure-the-export-to-data-lake-add-in"></a><a name="enableExportToDataLake"></a>Povolení a konfigurace doplňku Export do Data Lake

> [!IMPORTANT]
> Při konfiguraci doplňku Export to Data Lake zrušte zaškrtnutí políčka **Změny dat v reálném čase** na stránce nastavení doplňku Export to Data Lake, abyste zajistili, že nebudou povoleny změny dat v reálném čase. Funkce **Změny dat v reálném čase** je ve fázi preview a není aktuálně podporována službou Commerce Analytics. Pokud tuto funkci povolíte, Commerce Analytics nebude moci zpracovávat vaše data v datovém jezeře a většina vašich sestav Power BI nezobrazí žádná data.

Analýza Commerce (Preview) spoléhá na funkci Export do Data Lake, která exportuje data centrály Commerce do Data Lake a udržuje data aktuální. Než nakonfigurujete analýzu Commerce (Preview), povolte a nakonfigurujte Export do Data Lake podle kroků v [Konfiguraci exportu do Azure Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

Při konfiguraci doplňku Export do Data Lake si poznamenejte následující informace, protože je budete muset zadat později:

- <a name="keyVault"></a>Název DNS (Domain Name System) trezoru klíčů, který jste zadali.
- Názvy tajných kódů, které jste zadali a které obsahují ID aplikace a tajný kód aplikace. Další informace viz [Přidat tajné kódy do trezoru klíčů](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a>Nainstalujte a nakonfigurujte Azure Synapse workspace.

Commerce Analytics (preview) vyžaduje, aby byl ve vašem Azure Synapse workspace zřízen Synapse SQL na vyžádání. Chcete-li nainstalovat a konfigurovat Azure Synapse workspace, postupujte dle těchto kroků.

1. Nainstalujte Azure Synapse workspace ve vašem předplatném Azure. Další informace naleznete v tématu [Rychlý start: Vytvoření Synapse workspace](/azure/synapse-analytics/quickstart-create-workspace).
1. <a name="serverlessep"></a>Po zřízení workspace otevřete stránku s přehledem zdrojů a poznamenejte si hodnotu **Koncový bod bezserverového SQL**. Tuto hodnotu budete muset v další části uložit do trezoru klíčů.
1. Na stránce přehledu vyberte odkaz **Otevřít Synapse Studio** a otevřete Azure Synapse Studio pro váš workspace.
1. V levé nabídce vyberte **Spravovat**. Chcete-li zobrazit názvy nabídek, možná budete muset vybrat odkaz pro rozbalení v nabídce vlevo.
1. V části **Skupina zabezpečení** vyberte **Řízení přístupu**. 
1. Vyberte **přidat**.
1. V podokně **Přidat přiřazení role** nastavte možnosti, jak je popsáno v následující tabulce.

    | Parametr | Hodnota |
    |--------|-------|
    | Rozsah | Vyberte **Workspace**. |
    | Role | Vyberte **Správce Synapse SQL**.|
    | Vybrat uživatele | Vyhledejte název vaší aplikace, který jste [vytvořili během instalace doplňku Export to Data Lake](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createapplication). Až se aplikace objeví ve výsledcích vyhledávání, vyberte ji. Aplikace se nyní objeví v části **Vybraní uživatelé, skupiny nebo instanční objekty**. |

1. Výběrem příkazu **Použít** dokončíte zadání role. Aplikaci jsou udělena oprávnění správce Synapse SQL. Proto může vytvářet požadovaná zobrazení během konfigurace doplňku Commerce Analytics (preview) LCS.

### <a name="add-secrets-to-the-key-vault"></a><a name="addSecrets"></a>Přidání tajných kódů do trezoru klíčů

Ve stejném [trezoru klíčů](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createkeyvault), který jste použili při konfiguraci doplňku Export to Data Lake, musíte přidat tajné kódy, které jsou uvedeny v následující tabulce. U každého tajného kódu musíte zadat jeho název a zadanou hodnotu.

| Navrhovaný název tajného kódu | Hodnota tajného kódu | Ukázková hodnota tajného kódu |
|---------|---------|---------|
| synapse-sql-server | Hodnota koncového bodu bezserverového SQL, kterou jste si poznamenali při [konfiguraci Azure Synapse workspace](#serverlessep). | `test-ondemand.sql.azuresynapse.net` |
| <a name="roUser"></a>readonly-sql-pwd | Heslo nastavené pro uživatele SQL s oprávněním pouze číst. Sestava Power BI použije toto heslo pro připojení k bezserverovému SQL. Chcete-li nastavit heslo, postupujte podle zásad vaší organizace pro hesla. | |

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a>Povolit a nakonfigurovat doplněk analýzy Commerce (Preview).

Chcete-li nainstalovat doplněk analýzy Commerce (Preview) v LCS, musíte být správcem prostředí v LCS pro prostředí, které plánujete používat.

K instalaci a konfiguraci doplňku analýzy Commerce (Preview), postupujte následovně.

1. Přihlaste se do [LCS](https://lcs.dynamics.com/) a přejděte do svého prostředí.
2. Na stránce **Prostředí** na kartě **Doplňky prostředí** vyberte **Nainstalujte nový doplněk**.
3. V dialogovém okně vyberte **Analýza Commerce (Preview)**.
4. V dialogovém okně **Doplněk nastavení** zadejte následující údaje.

    | Informace | Zdroj | Ukázková hodnota |
    |---|---|---|
    | Azure Active Directory (Azure AD) ID klienta | Přihlaste se do [Portálu Azure](https://portal.azure.com/) a otevřete službu **Azure Active Directory**. Poté otevřete stránku **Vlastnosti** a zkopírujte hodnotu do pole **ID klienta**. | `72f988bf-0000-0000-00000-2d7cd011db47` |
    | Název DNS vašeho trezoru klíčů Azure | Zadejte název DNS vašeho trezoru klíčů. Tuto hodnotu jste si poznamenali během [konfigurace doplňku Export to Data Lake](#keyVault). | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Název tajného kódu, který obsahuje ID aplikace | Zadejte tajný kód, který ukládá ID aplikace. Tuto hodnotu jste si poznamenali během [konfigurace doplňku Export to Data Lake](#keyVault). | `app-id` |
    | Název tajného kódu, který obsahuje tajný kód aplikace | Zadejte tajný kód, který ukládá tajný kód aplikace. Tuto hodnotu jste si poznamenali během [konfigurace doplňku Export to Data Lake](#keyVault). | `app-secret` |
    | Název tajného kódu, který obsahuje koncový bod bezserverového SQL pro Azure Synapse | Zadejte název tajného kódu, který obsahuje koncový bod bezserverového SQL. Tajný kód jste vytvořili během [přidávání tajných kódů k hodnotě klíče](#addSecrets). | `synapse-sql-server` |
    | Název tajného kódu, který obsahuje heslo nastavené pro uživatele SQL s oprávněním pouze číst v Azure Synapse | Zadejte název tajného kódu, který ukládá heslo nastavené pro uživatele bezserverového SQL s oprávněním pouze číst. Tento uživatel bude vytvořen a měl by být používán v sestavě Power BI za účelem připojení k bezserverovému SQL. Tajný kód jste vytvořili během [přidávání tajných kódů k hodnotě klíče](#addSecrets). | `readonly-sql-pwd` |

1. Přijměte podmínky nabídky zaškrtnutím políčka a poté vyberte **Instalovat**.

    Systém nainstaluje a nakonfiguruje doplněk analýzy Commerce (Preview) pro dané prostředí. Tento proces může trvat několik minut. Po jeho dokončení **Analýzy (Preview)** by měly být uvedeny na stránce **Prostředí** a stav by měl být **Instalováno**.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a>Instalace aplikace šablony Power BI

K instalaci aplikace šablony Power BI analýzy Commerce (Preview) postupujte následovně.

1. Přihlaste se do [portálu Power BI](https://powerbi.microsoft.com/) pomocí ID vaší organizace.
1. Instalujte aplikaci šablony Power BI analýzy Commerce (Preview) přechodem na [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Případně navštivte [stránku AppSource pro Dynamics 365 Commerce Analytics](https://appsource.microsoft.com/product/power-bi/dynamics-365-commerce.dydnamics-365-commerce-analytics) a vyberte možnost **Získat**.
1. Pokud aplikaci instalujete poprvé, přejděte ke kroku 5. Pokud jste tuto aplikaci již dříve nainstalovali, zobrazí se následující možnosti pro použití aktualizace aplikace:

    - **Aktualizujte pracovní prostor a aplikaci** – Aktualizujte stávající aplikaci šablony a přepište stávající nastavení aplikace, jako je název instance aplikace a konfigurace oprávnění.
    - **Aktualizujte pouze obsah pracovního prostoru bez aktualizace aplikace** – Aktualizujte stávající aplikaci šablony, ale ponechte stávající nastavení aplikace. *Tato možnost je doporučenou možností pro aktualizace aplikací.*
    - **Nainstalujte další kopii aplikace do nového pracovního prostoru** – Vytvořte nový pracovní prostor a poté v něm vytvořte kopii stávající aplikace šablony. Stávající pracovní prostor zůstane nedotčen.

1. Vyberte jednu z možností aktualizace a poté vyberte **Instalovat**.
1. Otevřete nainstalovanou aplikaci výběrem **Aplikace** v levém podokně a poté vyberte aplikaci.
1. Připojte aplikaci ke zdroji dat výběrem **Připojit**. Pokud jste aplikaci již nainstalovali, vyberte odkaz **Připojte svá data** ve žluté liště zpráv.
1. Nastavte následující pole.

    | Pole | Hodnota |
    |---|---|
    | Server | Zadejte koncový bod bezserverového SQL, který jste si po vás poznamenali po [vytvoření Azure Synapse workspace](#serverlessep). |
    | Databáze | Zadejte **CommerceAnalytics**. |
    | Jazyk | Vyberte hodnotu ze seznamu. Toto pole se používá pro lokalizované názvy produktů a kategorií. U hodnoty je rozlišována velikost písmen. |
    | Rozsah dat | Vyberte hodnotu ze seznamu. Data za vybraný počet měsíců budou importována do datové sady Power BI. Hodnota, kterou vyberete, ovlivňuje velikost datové sady a čas potřebný pro synchronizaci. |

1. Zvolte **Další**. Když budete vyzváni k zadání přihlašovacích údajů pro připojení k SQL databázi Azure Synapse, nastavte hodnoty polí, jak je uvedeno v následující tabulce.

    | Pole | Hodnota |
    |---|---|
    | Metoda ověřování | Vyberte **Základní**. |
    | Uživatelské jméno | Vstupte **reportreadonlyuser**. |
    | Heslo | Zadejte heslo, které jste [uložili pro uživatele SQL s oprávněním pouze číst v trezoru klíčů](#roUser). |

1. Vyberte **Přihlaste se a připojte se**.
1. Počkejte, dokud nebude datová sada úspěšně aktualizována. Poté vyberte **Upravit aplikaci** a otevřete pracovní plochu aplikace, kde můžete zobrazit stav aktualizace datové sady. V pracovním prostoru aplikace můžete také volitelně nastavit automatické plány aktualizací pro svou datovou sadu, spravovat oprávnění a přejmenovat instanci aplikace.

### <a name="privacy"></a><a name="privacy"></a>Důvěrnost

Ochrana vašich osobních údajů je pro nás důležitá. Chcete-li se dozvědět více, přečtěte si naše [Prohlášení o ochraně osobních údajů](https://go.microsoft.com/fwlink/?LinkId=521839).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
