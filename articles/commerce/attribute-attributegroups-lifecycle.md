---
title: Správa atributů a skupin atributů
description: Tento článek popisuje správu atributů a skupin atributů, které popisují produkty a jejich charakteristiky v aplikaci Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.openlocfilehash: aad448ea733aabdff3dc4438dcb682d49e0665c0
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/31/2022
ms.locfileid: "9386965"
---
# <a name="manage-attributes-and-attribute-groups"></a>Správa atributů a skupin atributů

[!include [banner](includes/banner.md)]

Tento článek popisuje správu atributů a skupin atributů, které popisují produkty a jejich charakteristiky v aplikaci Microsoft Dynamics 365 Commerce.

*Atributy* umožňují popis produktů a jejich charakteristik prostřednictvím uživatelem definovaných polí. Mezi příklady patří velikost paměti, kapacita pevného disku a shoda s normami Energy Star.

Atributy lze přidružit k různým entitám Commerce, jako jsou kategorie produktů a sítě, a lze jim nastavit výchozí hodnoty. Když jsou atributy přidruženy ke kategoriím produktů nebo kanálům, produkty zdědí tyto atributy a jejich výchozí hodnoty. Výchozí hodnoty atributů lze přepsat na úrovni jednotlivých produktů, na úrovni sítě nebo v katalogu.

Například typický televizní produkt může mít následující atributy.

| Kategorie   | Atribut           | Přípustné hodnoty                        | Výchozí hodnota |
|------------|---------------------|-------------------------------------------|---------------|
| Televize a video | Značka               | Libovolná platná hodnota značky                     | Není          |
| TV         | Velikost obrazovky         | 20 – 85 palců                              | 55 palců     |
|            | Svislé rozlišení | 4K (2160p), Full HD (1080p) nebo HD (720p) | 4K (2160p)    |
|            | Obnovovací frekvence obrazovky | 60 Hz, 120 Hz nebo 240 Hz                     | 60 Hz          |
|            | Vstupy HDMI         | 0–10                                      | 3             |

## <a name="attributes-and-attribute-types"></a>Atributy a typy atributů.

Atributy jsou založeny na *typech atributů*. Typ atributu určuje typ dat, které lze zadat pro určitý atribut. V Commerce jsou podporovány následující typy atributů:

- **Měna** – Tento typ podporuje hodnotu měny. Může být vázaná (může tedy podporovat rozsah hodnot), nebo může zůstat otevřená.
- **Datum a čas** – Tento typ podporuje hodnotu data a času. Může být vázaná nebo zůstat otevřená.
- **Desetinné číslo** – Tento typ podporuje číselnou hodnotu, která obsahuje desetinná místa. Podporuje také měrnou jednotku. Může být vázaná nebo zůstat otevřená.
- **Celé číslo** – Tento typ podporuje číselnou hodnotu. Podporuje také měrnou jednotku. Může být vázaná nebo zůstat otevřená.
- **Text** – Tento typ podporuje textovou hodnotu. Podporuje také předdefinovanou sadu možných hodnot, když je zapnuto nastavení **Pevný seznam**.
- **Logická hodnota** – Tento typ podporuje binární hodnotu (**pravda** nebo **nepravda**).
- **Odkaz** – Tento typ odkazuje na další atributy.

> [!NOTE]
> Kvůli [omezení indexu vyhledávání Azure](/rest/api/searchservice/data-type-map-for-indexers-in-azure-search) není **Desetinný** typ atributu podporován u vyhledávání v prostředí cloudu. Azure Cognitive Search nepodporuje převod typů atributu **Desetinný** na typy polí **Edm.Double** cílového indexu, protože tato konverze by snížila přesnost.

### <a name="set-up-attribute-types"></a>Nastavit typy atributů

Chcete-li nastavit typy atributů, postupujte podle kroků v tomto ukázkovém postupu.

1. Přihlaste se do Commerce headquarters jako manažer prodeje.
1. Přejděte do nabídky **Řízení informací o produktech \> Nastavení \> Kategorie a atributy \> Typy atributů**.
1. V podokně akcí zvolte **Nový**.
1. Do pole **Název typu atributu** zadejte **Typ Taška**.
1. V poli **Typ** vyberte **Text**.
1. Nastavte možnost **Pevný seznam** na **Ano**.
1. Na záložce **Hodnoty** vyberte **Přidat**.
1. V novém řádku zadejte do pole **Hodnota** text **Aktovka**.
1. Přidejte dalších pět řádků. V poli **Hodnota** každého řádku zadejte jinou hodnotu: **Psaníčko**, **Kabelka**, **Batoh**, **Přes rameno** nebo **Peněženka**.
1. V podokně akcí vyberte **Uložit**.
1. V podokně akcí zvolte **Nový**.
1. Do pole **Název typu atributu** zadejte **Typ Sluneční brýle**.
1. V poli **Typ** vyberte **Text**.
1. Nastavte možnost **Pevný seznam** na **Ano**.
1. Na záložce **Hodnoty** vyberte **Přidat**.
1. V novém řádku zadejte do pole **Hodnota** text **Ray ban**.
1. Přidejte další dva řádky. V poli **Hodnota** každého řádku zadejte jinou hodnotu: **Aviator** nebo **Oakley**.
1. V podokně akcí vyberte **Uložit**.

![Stránka typů atributů.](media/AttributeType_2022Series.png)

### <a name="set-up-an-attribute"></a>Nastavit atribut

Chcete-li nastavit atribut, postupujte podle kroků v tomto ukázkovém postupu.

1. Přihlaste se do Commerce headquarters jako manažer prodeje.
1. Přejděte do nabídky **Řízení informací o produktech \> Nastavení \> Kategorie a atributy \> Atributy**.
1. V podokně akcí zvolte **Nový**.
1. Do pole **Název** zadejte **Typ Taška**.
1. V poli **Název typu atributu** vyberte **Typ Taška**.
1. V podokně akcí vyberte **Uložit**.

![Stránka Atributy.](media/Attribute_2022Series.png)

## <a name="attribute-metadata"></a>Metadata atributu

*Metadata atributů* vám umožní vybrat možnosti k určení chování atributů pro každý produkt. Můžete například určit, zda atributy jsou požadovány, zda je lze použít pro vyhledávání a zda slouží jako filtr.

Pro produkty lze nastavení metadat atributů přepsat na úrovni kanálu.

Stránka **Atributy** obsahuje několik možností, které souvisejí s metadaty atributů. Pokud například v části **Metadata atributů pro kanály Commerce** nastavíte možnost **Lze upřesnit** na **Ano**, atribut se zobrazí pro upřesnění nebo filtrování produktů ve výsledcích vyhledávání a na stránkách procházení kategorií. Chcete-li atribut nakonfigurovat jako upravitelný, musíte nejprve vybrat **Nastavení filtru** v podokně akcí a potvrdit nastavení filtru pro atribut.

## <a name="filter-settings-for-attributes"></a>Nastavení filtrů pro atributy

Nastavení filtrů pro atributy vám umožní určit, jak jsou filtry atributů zobrazeny v pokladním místě. Chcete-li přistoupit k nastavení filtru pro atribut, zvolte na stránce **Atributy** v podokně akcí vyberte **Nastavení filtru**.

Stránka **Nastavení filtru** obsahuje následující pole:

- **Název** – Ve výchozím nastavení je toto pole nastaveno na název atributu. Hodnotu však lze upravit.
- **Možnost zobrazení** - K dispozici jsou následující možnosti:

    - **Jedna hodnota** – Tato možnost je k dispozici pro následující typy atributů: **Logická**, **Měna**, **Desetinné číslo**, **Celé číslo** a **Text**. Umožňuje vybrat pouze jednu hodnotu pro zpřesnění ve stránkách seznamu produktů, mezi něž patří například stránky procházení kategorií a stránky s výsledky vyhledávání produktů.
    - **Více hodnot value** – Tato možnost je k dispozici pro následující typy atributů: **Měna**, **Desetinné číslo**, **Celé číslo** a **Text**. Umožňuje vybrat více hodnot pro atribut v klientovi pro upřesnění.

- **Ovládání zobrazení** - K dispozici jsou následující možnosti:

    - **Seznam** – Tato možnost je k dispozici u všech typů atributů.
    - **Rozsah** – Tato možnost je k dispozici pro následující typy atributů: **Měna**, **Desetinné číslo** a **Celé číslo**.
    - **Posuvník** – Tato možnost je k dispozici pro následující typy atributů: **Měna**, **Desetinné číslo** a **Celé číslo**.
    - **Posuvník s panely** – Tato možnost je k dispozici pro následující typy atributů: **Měna**, **Desetinné číslo** a **Celé číslo**.

- **Prahová hodnota** – Toto nastavení je povinné, pokud jste vybrali **Rozsah** jako typ ovládání zobrazení. Hodnoty lze definovat pomocí středníku (;) jako oddělovače.

    Například u atributu **Objem tašky**, který má typ atributu **Celé číslo**, může být prahová hodnota **10; 20; 50; 100; 200; 500; 1000; 5000**. V takovém případě zobrazí pokladní místo následující rozsahy. Rozsahy, které nemají žádné produkty v sadě výsledků, se zobrazí šedě.

    - Je menší než 10
    - 10 – 20
    - 20 – 50
    - 50 – 100
    - 100 – 200
    - 200 – 500
    - 500 a více

Nastavení filtru pro atributy platí pouze pro atributy produktů a lze je použít k upřesnění výsledků vyhledávání produktů a procházení kategorií. Nevztahují se na vyhledávání zákazníků nebo vyhledávání objednávek, ačkoli stejné atributy lze použít k obohacení informací o zákaznících nebo objednávkách.

Ve výchozích modulech Commerce není k dispozici žádná podpora nastavení filtrů **Ovládání zobrazení**, například **Rozsah**, **Posuvník** a **Posuvník s panely**. Nastavení **Rozsah** a **Posuvník** jsou nadále podporována u řešení pokladních míst, zatímco nastavení **Posuvník s panely** platí pro starší verzi online obchodu SharePoint a je nadále k dispozici pro integraci třetích stran a vlastní scénáře.

Doporučujeme, aby upřesnitelné atributy měly atribut typu **Text**, u kterého je zapnuta možnost **Pevný seznam**, a ponechat seznam spravovatelný (max. 100–200 jedinečných hodnot). Pokud bude mít upřesnění 1 000 nebo více jedinečných hodnot, je vhodnější použít atribut typu **Text**, u kterého je možnost **Pevný seznam** zakázána.

Překlady jsou důležité u názvů atributů a jejich hodnot. U atributů typu **Text** se zapnutou možností **Pevný seznam** můžete definovat překlady pro hodnoty atributů v části **Typ atributu**. U všech ostatních typů atributu můžete definovat překlady na stránce, kde definujete hodnoty atributů. Například pro atribut typu **Text** můžete definovat překlady pro výchozí hodnotu atributu na stránce **Atributy**. Pokud však přepíšete výchozí hodnotu na úrovni produktu, můžete definovat překlady pro atribut na stránce **Atributy produktu**.

Poté, co byl atribut označen jako upřesnitelný pro kanál, neměli byste aktualizovat typ atributu. V opačném případě ovlivníte zveřejnění produktových dat do indexu vyhledávání. Místo toho doporučujeme vytvořit nový atribut pro nový typ upřesnění a odstranit předchozí atribut jeho odebráním z jiných skupin atributů.

Vyhledávání podle atributů je podporováno, ale načítá výsledky pouze pro přesné shody hledaných slov. Dejme tomu, že atribut **Tkanina** má hodnotu **Kašmírová bavlna**. Pokud zákazník hledá „Kašmír“, žádné produkty s látkou **Kašmírová bavlna** se nenajdou. Pokud však zákazník hledá „Kašmírová“, „bavlna“ nebo „Kašmírová bavlna“, budou produkty s látkou **Kašmírová bavlna** načteny.

### <a name="additional-attribute-metadata-options"></a>Další možnosti metadat atributů

> [!NOTE]
> Tyto možnosti metadat atributů jsou použitelné pouze u starších online obchodů SharePoint a externích integrací. Další informace o těchto možnostech metadat atributů naleznete v tématu [Přehled schématu vyhledávání ve službě SharePoint Server 2013](/SharePoint/search/search-schema-overview).

Následující další možnosti metadat atributů jsou také dostupné na stránce **Atributy**:

- Lze prohledávat
- Lze získat
- Lze se dotázat.
- Lze řadit
- Ignorovat velikost písmen a formát
- Úplná shoda

Tyto možnosti byly původně určené k vylepšení funkce vyhledávání ve starších online obchodech založených na službě SharePoint. Nemusí platit na webech elektronického obchodu Commerce nebo pokladních místech. Protože je i nadále podporována integrace bezobslužných míst, jsou tyto možnosti dostupné při exportu metadat atributů s využitím sady Commerce Software Development Kit (SDK). Pomocí sady Commerce SDK můžete produkty umístit do vlastního, optimalizovaného externího vyhledávacího indexu. Tímto způsobem můžete zajistit, že budou indexovány pouze atributy, které by měly být indexovány.

## <a name="attribute-groups"></a>Skupiny atributů

*Skupina atributů* slouží k seskupení jednotlivých atributů součásti nebo podsoučásti v modelu konfigurace výrobku. Atribut můžete zahrnout do více než jedné skupiny atributů. Skupiny atributů pomáhají uživatelům nakonfigurovat produkty, protože různé voby jsou uspořádány ve specifickém kontextu. Můžete přiřadit skupiny atributů k kategoriím nebo kanálům. Můžete také nastavit výchozí hodnoty atributů ve skupině atributů.

![Stránka skupin atributů.](media/AttributeGroup_2022Series.png)

### <a name="create-an-attribute-group"></a>Tvorba skupiny atributů

Chcete-li vytvořit skupinu atributů, postupujte podle kroků v tomto ukázkovém postupu.

1. Přihlaste se do Commerce headquarters jako manažer prodeje.
1. Přejděte do nabídky **Řízení informací o produktech \> Nastavení \> Kategorie a atributy \> Skupiny atributů**.
1. Vytvořte skupinu atributů s názvem **Košile**.
1. Přidejte následující atributy: **Metoda čištění**, **Typ límečku**, **Kolekce** a **Design**.

> [!NOTE]
> Hodnoty pořadí zobrazení atributů ve skupině atributů neovlivňují pořadí zpřesnění ve výsledcích vyhledávání a procházení kategorií, a ani se na něj nevztahují. Jsou použitelné pouze u scénáře „atributy objednávky“.

### <a name="assign-attribute-groups-to-categories"></a>Přiřazení skupin atributů ke kategoriím

Jedna nebo více skupin atributů může být spojena s uzly kategorií v následujících typech hierarchií kategorií:

- Hierarchie obchodních produktů
- Hierarchie kategorií navigace v kanálu
- Hierarchie kategorií doplňkových produktů

Když jsou produkty kategorizovány do kategorií, které jsou přidruženy ke skupinám atributů, zdědí atributy, které jsou zahrnuty v těchto skupinách atributů.

![Záložka s náhledem Skupiny atributů produktu na stránce Hierarchie produktů Commerce.](media/AGRetailProdHierarchy_2022Series.png)

Chcete-li přiřadit skupiny atributů ke kategoriím v hierarchii produktů Commerce, postupujte podle následujících kroků.

1. Přihlaste se do Commerce headquarters jako manažer prodeje.
1. Přejděte na **Retail and Commerce \> Produkty a kategorie \> Hierarchie produktů Commerce**.
1. Vyberte hierarchii navigace **Móda**.
1. V části **Pánské oděvy** zvolte kategorii **Kalhoty** a poté na záložce s náhledem **Skupiny atributů produktů** přidejte skupinu atributů s názvem **Pánské pásky**.
1. Vyberte kategorii **Módní sluneční brýle** a ověřte nové atributy ve skupině atributů **Módní sluneční brýle** výběrem **Zobrazit atributy**. Skupina atributů by měla zobrazovat atributy **Tvar čočky** a **Značka slunečních brýlí**.
1. Vyberte kategorii **Kalhoty** a ověřte atributy pro skupinu atributů **Pánské pásky** výběrem příkazu **Zobrazit atributy**. Skupina atributů by měla zobrazovat atributy **Značky pánských pásků**, **Materiál pásku** a **Velikost pásku**.

Stejný základní postup lze také použít k přiřazení skupin atributů ke kategoriím v hierarchii kategorií navigace kanálu a hierarchii kategorií doplňkových produktů. V kroku 2 však použijte jednu z následujících cest v závislosti na hierarchii, které chcete skupiny atributů přiřadit:

- **Hierarchie kategorií navigace kanálu**: Přejděte na **Maloobchodní a velkoobchodní prodej \> Správa produktů a kategorií \> Kategorie kanálu a atributy produktu**.
- **Hierarchie kategorií doplňkových produktů**: Přejděte na **Maloobchodní a velkoobchodní prodej \> Správa produktů a kategorií \> Kategorie doplňkových produktů**.

> [!NOTE]
> Ujistěte se, že skupiny atributů asociujete pouze v hierarchii kategorií na záložce s náhledem **Skupiny atributů produktu**, ne na záložce s náhledem **Hodnoty atributů kategorie**. Pokud se atributy objeví na záložce s náhledem **Hodnoty atributů kategorie**, vyberte příkaz **Upravit hierarchii kategorií** v podokně akcí. Poté na záložce s náhledem **Skupiny atributů kategorií** vyberte uzly kategorie a vyberte **Odstranit**. Neexistuje žádná podpora pro načítání atributů podle kategorie prostřednictvím Commerce Scale Unit.

## <a name="identify-viewable-and-refinable-attributes-for-commerce-channels-for-the-default-product-collection"></a>Identifikace viditelných a upřesnitelných atributů pro kanály Commerce pro výchozí kolekci produktů

Poté, co přiřadíte různé skupiny atributů ke kategoriím v různých hierarchiích (hierarchie produktů Commerce nebo kategorií navigace kanálem) a definujete hodnoty atributů pro každý produkt na základě přidružení kategorií, musíte zapnout příznak **Zobrazit atributy na kanálu**, aby byly tyto atributy viditelné v konkrétním kanálu.

1. Přejděte na **Retail and Commerce \> Nastavení kanálu \> Kategorie kanálu a atributy produktu**.
1. Vyberte **Nastavit metadata atributu** a poté vyberte atribut v levém navigačním podokně.
1. Na záložce s náhledem **Atributy produktu kanálu** (nikoli na záložce s náhledem **Atributy kategorie**) nastavte možnost **Zobrazit atribut na kanálu** na **Ano**, aby byl atribut viditelný.
1. Pokud chcete, aby byl atribut také upřesnitelný, nastavte možnost **Lze upřesnit** na **Ano**.

### <a name="control-visibility-of-dimension-based-refiners-such-as-size-style-and-color"></a>Řízení viditelnosti zpřesnění založených na dimenzi, jako je velikost, styl a barva

Dimenze produktu, jako je velikost, styl a barva, jsou nejčastěji používanými zpřesněními. Chcete-li tyto dimenze produktu zpřístupnit jako zpřesnění, měli byste přidružit skupinu atributů na úrovni kanálu, která obsahuje odkaz na typ atributu, který automaticky dědí hodnoty z hodnot dimenzí produktu.

Aktualizací příznaků na stránce **Kategorie kanálu a atributy produktů** můžete určit, že dimenze produktu jsou viditelné a upravitelné. Vyberte kořenový uzel v navigačním podokně a poté na záložce s náhledem **Atributy produktu kanálu** nastavte možnost **Zobrazit atribut na kanálu** na **Ano** u atributů **Velikost**, **Styl** a **Barva**. Pokud chcete, aby tyto atributy byly také upřesnitelné, nastavte možnost **Lze upřesnit** u všech atributů na **Ano**.

![Nastavení metadat atributů pro zpřesnění dimenzí.](./media/ProductDimensionRefinersMetadataSetup_2022Series.png)

Chcete-li povolit atributy, aby byly dostupné v kanálu Houston založeném na ukázkových datech, postupujte podle kroků v tomto ukázkovém postupu.

1. Přejděte na **Retail and Commerce \> Nastavení kanálu \> Kategorie kanálu a atributy produktu**.
1. Vyberte kanál **Houston**.
1. V podokně akcí zvolte **Nastavit metadata atributu**.
1. Vyberte uzel kategorie **Móda** a poté na pevné záložce **Atributy produktu kanálu** vyberte **Zahrnout atribut** pro každý atribut.
1. Vyberte uzel kategorie **Módní doplňky**, zvolte **Módní sluneční brýle** a poté na pevné záložce **Atributy produktu kanálu** vyberte **Zahrnout atribut** pro každý atribut.
1. Vyberte uzel kategorie **Pánské oděvy**, zvolte **Kalhoty** a poté na pevné záložce **Atributy produktu kanálu** vyberte **Zahrnout atribut** pro každý atribut.
1. Po aktualizaci metadat atributů pro zamýšlené atributy a zpřesnění se ujistěte, že jste uložili změny a spustili úlohu **Publikovat aktualizace kanálu**. Poté, co budou aktualizace publikovány, musíte spustit následující úlohy: **1070** (**Konfigurace kanálu**), **1040** (**Produkty**) a **1150** (**Katalog**).

> [!NOTE]
> - Pokud vaše firma vyžaduje, abyste často přidávali nebo odebírali produkty v hierarchii navigace nebo prováděli změny, jako je aktualizace hodnot pořadí zobrazení, přidávání nových kategorií a přidávání nových skupin atributů do kategorií, doporučujeme konfigurovat úlohu **Publikovat aktualizace kanálu** tak, aby se často spouštěla v dávce. Případně spusťte ručně úlohu **Publikovat aktualizace kanálu** a pak následující úlohy Commerce Data Exchange (CDX): **1070** (**Konfigurace kanálu**), **1040** (**Produkty**) a **1150** (**Katalog**).
> - Možnost **Zdědit** slouží k určení, že kanál má zdědit skupiny atributů ze svého nadřazeného kanálu v hierarchii. Nastavíte-li možnost **Zdědit** na **Ano**, podřízený uzel kanálu zdědí všechny skupiny atributů a všechny atributy v těchto skupinách atributů.
> - Pokud není tlačítko **Nastavit metadata atributu** v podokně akcí dostupné, ujistěte se, že **Hierarchie navigace** je přidružena k vašemu kanálu na záložce s náhledem **Všeobecné**.
> - Na úrovni kanálu nesmíte přidružovat žádné skupiny atributů kromě skupin atributů založených na dimenzích (například ve **Skupinách atributů** na stránce **Kategorie kanálu a atributy produktů**).
> - Po zavedení podpory zákaznických katalogů business-to-business (B2B) v Commerce verze 10.0.27 se od vás očekává, že identifikujete zpřesnění a nastavení atributů u každého katalogu B2B tím způsobem, který je popsán v tomto článku.

## <a name="override-attribute-values"></a>Přepsání hodnot atributů

Výchozí hodnoty atributů lze přepsat na úrovni produktu pro jednotlivé výrobky. Lze je přepsat také pro jednotlivé produkty v určitých katalozích, které jsou určeny v konkrétní síti.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Přepsání hodnot atributu jednotlivého produktu

Chcete-li přepsat hodnoty atributů jednotlivého produktu, postupujte podle kroků v tomto ukázkovém postupu.

1. Přihlaste se do Commerce headquarters jako manažer prodeje.
1. Přejděte na **Maloobchodní a velkoobchodní prodej \> Správa kategorií a produktů \> Uvolněné produkty podle kategorie**.
1. Vyberte uzel **Móda \> Módní doplňky \> Módní sluneční brýle**.
1. Vyberte požadovaný produkt v mřížce. Poté v podokně akcí na kartě **Produkt** ve skupině **Nastavení** zvolte **Atributy produktu**.
1. V levém podokně vyberte atribut a aktualizujte jeho hodnotu v pravém podokně.

![Stránka hodnot atributů produktu.](media/ProdDetailsProdAttrValues_2022Series.png)

### <a name="override-the-attribute-values-of-all-products-in-a-catalog"></a>Přepsání hodnot atributů všech produktů v katalogu

Chcete-li přepsat hodnoty atributů všech produktů v katalogu, postupujte podle kroků v tomto ukázkovém postupu.

1. Přihlaste se do Commerce headquarters jako manažer prodeje.
1. Přejděte na uzel **Maloobchodní a velkoobchodní prodej \> Správa katalogu \> Všechny katalogy**.
1. Vyberte katalog **Základní katalog Fabrikam**.
1. Vyberte uzel **Móda \> Módní doplňky \> Módní sluneční brýle**.
1. Na pevné záložce **Produkty** vyberte požadovaný produkt a poté vyberte **Atributy** nad mřížkou produktu.
1. Na následujících pevných záložkách aktualizujte hodnoty požadovaných atributů:

    - Médium sdíleného produktu
    - Sdílené atributy produktu
    - Médium kanálu
    - Atributy produktu kanálu

### <a name="override-the-attribute-values-of-all-products-in-a-channel"></a>Přepsání hodnot atributu všech produktů v kanálu

Chcete-li přepsat hodnoty atributů všech produktů v kanálu, postupujte podle kroků v tomto ukázkovém postupu.

1. Přihlaste se do Commerce headquarters jako manažer prodeje.
1. Přejděte na **Retail and Commerce \> Nastavení kanálu \> Kategorie kanálu a atributy produktu**.
1. Vyberte kanál **Houston**.
1. Na pevné záložce **Produkty** vyberte požadovaný produkt a poté vyberte **Atributy** nad mřížkou produktu.
1. Pokud nejsou k dispozici žádné produkty, vyberte **Přidat** na záložce s náhledem **Produkty** a poté vyberte požadované produkty v dialogovém okně **Přidat produkty**.
1. Na následujících pevných záložkách aktualizujte hodnoty požadovaných atributů:

    - Médium sdíleného produktu
    - Sdílené atributy produktu
    - Médium kanálu
    - Atributy produktu kanálu

### <a name="define-variant-specific-attribute-values-and-define-multiple-values-for-product-attributes"></a>Definování hodnot atributů specifických pro jednotlivé varianty a více hodnot pro atributy produktů

Chcete-li definovat hodnoty atributů specifické pro jednotlivé varianty a definovat více hodnot pro atributy produktu, postupujte podle kroků v tomto ukázkovém postupu.

1. Přihlaste se do Commerce headquarters jako manažer prodeje.
1. Přejděte na **Retail and Commerce \> Nastavení kanálu \> Kategorie kanálu a atributy produktu**.
1. Vyberte kanál **Houston**.
1. Na záložce s náhledem **Produkty** vyberte požadovanou variantu produktu a poté vyberte **Atributy** nad mřížkou produktu.
1. Pokud nejsou k dispozici žádné produkty, vyberte **Přidat** na záložce s náhledem **Produkty** a poté vyberte požadované varianty produktu v dialogovém okně **Přidat produkty**.
1. Na následujících pevných záložkách aktualizujte hodnoty požadovaných atributů:

    - Médium sdíleného produktu
    - Sdílené atributy produktu
    - Médium kanálu
    - Atributy produktu kanálu

#### <a name="example-of-variant-specific-attribute-configuration"></a>Příklad konfigurace atributu specifického pro variantu
        
V tomto příkladu je produkt **P001-Master** víceúčelovou obuví, která má tři varianty: **Běh**, **Chůze** a **Treking**. U každé varianty chcete jednoznačně definovat hodnotu atributu **Aktivita**. Na záložce s náhledem **Produkty** ve stránce **Kategorie kanálu a atributy produktů** pro váš kanál definujte hodnotu atributu **Aktivita** pro varianty, jak je uvedeno v následující tabulce.

| Varianta     | Hodnota atributu Aktivita |
|-------------|--------------------------|
| P001-Master | Sporty                   |
| P001-1      | Běh                  |
| P001-2      | Chůze                  |
| P001-3      | Treking                 |

Pokud uživatel hledá slovo „bota“, produkt **P001-Master** se ve výsledcích vyhledávání zobrazí. Pokud jste konfigurovali atribut **Aktivita** jako upřesnitelný, zpřesnění **Aktivita** vypíše jako upřesnitelnou hodnotu pouze **Sporty**, protože tato hodnota byla definována pro atribut **Aktivita** atribut na úrovni produktu **P001-Master**.

Ve výchozím nastavení jsou atributy na úrovni variant určeny k použití pouze na stránkách s podrobnostmi o produktu (PDP). Když vyberete konkrétní variantu produktu na PDP, aktualizují se specifikace produktu na PDP pro tuto konkrétní variantu.

Aby zpřesnění vyzvedla hodnoty atributů, které jsou definovány na úrovni varianty produktu, musíte definovat atribut na hlavní úrovni produktu, zaškrtnout políčko **Povolit více hodnot** a nastavit typ atributu na **Text**.

Dále musíte určit všechny možné hodnoty pro varianty produktu. U atributu **Aktivita**, který je použit v tomto příkladu, mohou mezi možné hodnoty patřit **Běh**, **Chůze**, **Turistika**, **Treking**, **Kempování**, **Vodní sporty** a **Zimní sporty**.

Poté, co určíte, jaké by měly být hodnoty atributů variant, je můžete definovat na hlavní úrovni produktu pomocí hodnot oddělených svislou čarou. Pro atribut **Aktivita** můžete definovat hodnotu atributu u hlavního produktu jako **Běh|Chůze|Turistika|Treking|Kempování|Vodní sporty|Zimní sporty**.

Poté můžete u každé varianty definovat hodnoty atributů zadáním hodnot oddělených svislou čarou nebo jednotlivých hodnot. Pro atribut **Aktivita** můžete konfigurovat individuální variantu produktu jako **Běh|Chůze |Turistika**, **Běh**, **Běh|Turistika|Vodní sporty** a tak dále.

Poté, co jste definovali hodnoty atributů variant, vyberte na stránce **Kategorie kanálu a atributy produktů** v podokně akcí příkaz **Publikovat aktualizace kanálu** a poté spusťte úlohy **1150**, **1040** a **1070**.

Po dokončení úloh a aktualizaci indexu vyhledávání by se ve výsledcích vyhledávání a procházení kategorií měly objevit všechny očekávané hodnoty.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
