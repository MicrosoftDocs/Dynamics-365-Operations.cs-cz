---
title: "Atributy, skupiny atributů a jejich přidružení k různým maloobchodním entitám v aplikaci Finance and Operations"
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application pdate 5, AX 8.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 53af4335146be6c163a6d84b60155e1a741c0be4
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---

# <a name="attributes-attribute-groups-and-their-associations-with-various-retail-entities-in-finance-and-operations"></a>Atributy, skupiny atributů a jejich přidružení k různým maloobchodním entitám v aplikaci Finance and Operations

[!include[banner](includes/banner.md)]

*Atributy* poskytují způsob k dalšímu popisu produktu a jeho vlastností prostřednictvím uživatelem definovaných polí (jako například **Velikost paměti**, **Kapacita pevného disku**, **Je kompatibilní se standardem Energy Star** atd). V aplikaci Microsoft Dynamics 365 for Finance and Operations lze atributy přidružit k různým maloobchodním entitám, jako jsou kategorie produktů a maloobchodní sítě, a lze jim nastavit výchozí hodnoty. Produkty pak dědí atributy a výchozí hodnoty při přidružení ke kategorii produktu nebo maloobchodní síti. Výchozí hodnoty lze přepsat na úrovni jednotlivých produktů, na úrovni maloobchodní sítě nebo v maloobchodním katalogu.
 
Například typický televizní produkt může mít následující atributy.

| Kategorie   | Atribut                | Přípustné hodnoty          | Výchozí hodnota |
|------------|--------------------------|-----------------------------|---------------|
| Televize a video | Značka                    | Libovolná platná hodnota značky       | None          |
| TV         | Velikost obrazovky              | 20 – 80 palců                | None          |
|            | Svislé rozlišení      | 480i, 720p, 1080i nebo 1080p | 1080p         |
|            | Obnovovací frekvence obrazovky      | 60 Hz, 120 Hz nebo 240 Hz       | 60 Hz          |
|            | Vstupy HDMI              | 0–10                        | 3             |
|            | Vstupy DVI               | 0–10                        | 1             |
|            | Kompozitní vstupy         | 0–10                        | 2             |
|            | Komponentní vstupy         | 0–10                        | 1             |
| LCD        | Připraveno na 3D                 | Ano nebo Ne                   | Ano           |
|            | 3D k dispozici               | Ano nebo Ne                   | Žádný            |
| Plazma     | Provozní teplota od      | 0–43 °C              | 32            |
|            | Provozní teplota do        | 0–43 °C              | 1597           |
| Projekční | Záruka | 6, 12 nebo 18 měsíců         | 12            |
|            | Počet trubic    | 1–5                         | 3             |

## <a name="attributes-and-attribute-types"></a>Atributy a typy atributů.

Atributy jsou založeny na *typech atributů*. Typ atributu určuje typ dat, které lze zadat pro určitý atribut. Aplikace Finance and Operations aktuálně podporují následující typy atributů:

- **Měna** – Tento typ podporuje hodnotu měny. Může být vázaná (může tedy podporovat rozsah hodnot), nebo může zůstat otevřená.
- **Datum a čas** – Tento typ podporuje hodnotu data a času. Může být vázaná nebo zůstat otevřená.
- **Desetinné číslo** – Tento typ podporuje číselnou hodnotu, která obsahuje desetinná místa. Podporuje také měrnou jednotku. Může být vázaná nebo zůstat otevřená.
- **Celé číslo** – Tento typ podporuje číselnou hodnotu. Podporuje také měrnou jednotku. Může být vázaná nebo zůstat otevřená.
- **Text** – Tento typ podporuje textovou hodnotu. Podporuje také předdefinovanou sadu možných hodnot (tedy *výčet*).
- **Logická hodnota** – Tento typ podporuje binární hodnotu (**pravda** nebo **nepravda**).
- **Odkaz** – Tento typ odkazuje na další atributy.

### <a name="set-up-attribute-types-in-finance-and-operations"></a>Nastavení typů atributů v aplikaci Finance and Operations

1. Přihlaste se ke klientovi účetního systému Finance and Operations jako manažer maloobchodního prodeje.
2. Přejděte do nabídky **Řízení informací o produktech** &gt; **Nastavení** &gt; **Kategorie a atributy** &gt; **Typy atributů**.
3. Vytvořte dva typy atributů typu **Text** typu, nastavte možnost **Pevný seznam** na **Yes**a poté přidejte seznam hodnot:

    - Pojmenujte typ atributu **Tvar čočky**a přidejte následující hodnoty: **Ovál**, **Čtverec** a **Obdélník**.
    - Pojmenujte druhý typ atributu **Značka slunečních brýlí**a přidejte následující hodnoty: **Ray ban**, **Aviator** a **Oakley**.

![Typy atributů](media/AttributeType.png)

### <a name="set-up-an-attribute-in-finance-and-operations"></a>Nastavení atributu v aplikaci Finance and Operations

1. Přihlaste se ke klientovi účetního systému jako manažer maloobchodního prodeje.
2. Přejděte do nabídky **Řízení informací o produktech** &gt; **Nastavení** &gt; **Kategorie a atributy** &gt; **Atributy**.
3. Vytvořte atribut s názvem **Čočky**.
4. Nastavte pole **Typ atributu** na **Tvar čočky**.

![Atributy](media/Attribute.png)

## <a name="attribute-metadata"></a>Metadata atributu

*Metadata atributů* vám umožní vybrat možnosti k určení chování atributů pro každý produkt. Můžete například určit, zda atributy jsou požadovány, zda je lze použít pro vyhledávání a zda slouží jako filtr.

Pro maloobchodní produkty lze nastavení metadat atributů přepsat na úrovni kanálu. Tuto funkci probereme později v tomto tématu.

Jak si můžete povšimnout, stránka **Atributy** obsahuje možnosti, které souvisejí s metadaty atributů. Pod možností **Metadata atributů pro POS** jedna z možností s názvem **"Lze upřesnit"** ovlivňuje chování hodnot atributů v maloobchodním pokladním místě, nebo způsob, kterým systém zpracovává tyto hodnoty atributů. Pouze atributy, pro které můžete nastavit možnost **"Lze upřesnit"** na **"Ano"**, se ukáží pro upřesnění nebo filtrování produktů v maloobchodním pokladním místě.

Zde jsou uvedeny zbývající možnosti metadat atributů na stárnce **Atributy**:

- Lze prohledávat
- Lze získat
- Lze se dotázat.
- Lze řadit
- Povolit více hodnot
- Ignorovat velikost písmen a formát
- Úplná shoda

Tyto možnosti byly původně určené k vylepšení funkce vyhledávání pro online poutače. Ačkoli aplikace Finance and Operations neobsahuje online poutače, obsahuje eCommerce Publishing Software Development Kit (SDK). Odběratele mohou použít tuto sadu SDK pro vložení produktů do libovolných vyhledávacích indexů. I když jsou data produktu importována, odběratelé by stále měli mít možnost rozlišit prohledávatelná dat, data, na která se lze dotazovat atd. Tímto způsobem mohou vytvářet optimální index, aby zajistili, že na indexu budou pouze atributy, které by tam měly *podle jejich názoru* být.

Informace o účelu těchto zbývajících možností naleznete v tématu [Přehled schématu vyhledávání ve službě SharePoint Server 2013](https://technet.microsoft.com/en-us/library/jj219669.aspx).

## <a name="filter-settings-for-attributes"></a>Nastavení filtrů pro atributy

Nastavení filtrů pro atributy vám umožňí určit, jak jsou zobrazeny filtry pro atributy v maloobchodním pokladním místě. Chcete-li přistoupit k nastavení filtru pro atribut, zvolte na stránce **Atributy** v aplikaci Finance and Operations atribut a poté vyberte v podokně akcí **Nastavení filtru**.

Stránka **Předvolby zobrazení filtru** obsahuje následující pole:

- **Název** – Ve výchozím nastavení je toto pole nastaveno na název atributu. Hodnotu však lze upravit.
- **Možnost zobrazení** - K dispozici jsou následující možnosti:

    - **Jedna hodnota** – Tato možnost je k dispozici pro následující typy atributů: **Logická**, **Měna**, **Desetinné číslo**, **Celé číslo** a **Text**. Tato možnost umožňuje v klientovi výběr jedné hodnoty pro tyto atributy k upřesnění.
    - **Více hodnot value** – Tato možnost je k dispozici pro následující typy atributů: **Měna**, **Desetinné číslo**, **Celé číslo** a **Text**. Tato možnost umožňuje v klientovi výběr více hodnot pro tento atribut k upřesnění.

- **Ovládání zobrazení** - K dispozici jsou následující možnosti:

    - **Seznam** – Tato možnost je k dispozici pro všechny typy atributů.
    - **Rozsah** – Tato možnost je k dispozici pro následující typy atributů: **Měna**, **Desetinné číslo** a **Celé číslo**. 
    - **Posuvník** – Tato možnost je k dispozici pro následující typy atributů: **Měna**, **Desetinné číslo** a **Celé číslo**.
    - **Posuvník s panely** – Tato možnost je k dispozici pro následující typy atributů: **Měna**, **Desetinné číslo** a **Celé číslo**.

- **Prahová hodnota** – Toto nastavení je povinné, pokud jste vybrali **Rozsah** jako typ ovládání zobrazení. Hodnoty lze definovat pomocí středníku (;) jako oddělovače.

    Například pro filtr **Objem tašky** může být prahová hodnota **10; 20; 50; 100; 200; 500; 1 000; 5000**. V takovém případě zobrazí maloobchodní pokladní místo následující rozsahy. Všechny rozsahy, které nemají žádné produkty v sadě výsledků, se zobrazí šedě.

    - Je menší než 10
    - 10 – 20
    - 20 – 50
    - 50 – 100
    - 100 – 200
    - 200 – 500
    - 500 a více

![Nastavení filtru atributů](media/AttributeFilterSettings.PNG)

## <a name="attribute-groups"></a>Skupiny atributů

Po definování atributů je lze přiřadit do skupin atributů. *Skupina atributů* slouží k seskupení jednotlivých atributů pro součást nebo podsoučást v modelu konfigurace výrobku. Atribut můžete zahrnout do více než jedné skupiny atributů. Skupiny atributů pomáhají uživatelům nakonfigurovat produkty, protože různé voby jsou uspořádány ve specifickém kontextu. Můžete přiřadit skupiny atributů k maloobchodním kategoriím nebo maloobchodním kanálům.

Můžete také nastavit výchozí hodnoty atributů, které jsou součástí skupiny atributů. Například přidáte atribut barvy do skupiny atributů a zvolíte výchozí hodnotu atributu **Modrá**. V takovém případě po přidání skupiny atributů k maloobchodnímu produktu, který zahrnuje barvu jako jeden z jeho atributů, zobrazí se pro tento produkt výchozí barva **Modrá**.

![Skupiny atributů](media/AttributeGroup.png)

### <a name="create-an-attribute-group"></a>Tvorba skupiny atributů

1. Přihlaste se ke klientovi účetního systému jako manažer maloobchodního prodeje.
2. Přejděte do nabídky **Řízení informací o produktech** &gt; **Nastavení** &gt; **Kategorie a atributy** &gt; **Skupiny atributů**.
3. Vytvoření skupiny atributů s názvem **Módní sluneční brýle**.
4. Přidejte následující atributy: **Tvar čočky** a **Značka slunečních brýlí**.

### <a name="assign-attribute-groups-to-retail-categories"></a>Přiřazení skupin atributů ke kategoriím maloobchodu

Jednu nebo více skupin atributů lze přiřadit k uzlům kategorií v následujících typech hierarchií kategorií maloobchodu: Hierarchie maloobchodních produktů, hierarchie kategorie navigace kanálu a Doplňková hierarchie kategorií produktu. Poté po zařazení produktů do kategorií zdědí produkty atributy, které jsou zahrnuty ve skupinách atributů.

![Hierarchie maloobchodních produktů – Skupiny atributů produktů](media/AGRetailProdHierarchy.PNG)

Chcete-li přiřadit skupiny atributů ke kategoriím v hierarchii maloobchodních produktů, postupujte podle následujících kroků.

1. Přihlaste se ke klientovi účetního systému jako manažer maloobchodního prodeje.
2. Přejděte na **Maloobchod** &gt; **Správa kategorií a produktů** &gt; **Hierarchie maloobchodních produktů**.
3. Vyberte **Hierarchie navigace módou**.
4. Pod položkou **Pánské oděvy** zvolte kategorii **Kalhoty** a poté na rychlé záložce **Skupiny atributů produktů** přidejte skupinu atributů s názvem **Pánské pásky**.
5. Vyberte kategorii **Módní sluneční brýle** a ověřte nové atributy ve skupině atributů **Módní sluneční brýle** výběrem **Zobrazit atributy**.

    Skupina atributů by měla zobrazovat atributy **Tvar čočky** a **Značka slunečních brýlí**.

6. Pod možností **Pánské oděvy** vyberte kategorii **Kalhoty** a ověřte atributy pro skupinu atributů **Pánské pásky** výběrem **Zobrazit atributy**.

    Skupina atributů by měla zobrazovat atributy **Značky pánských pásků**, **Materiál pásku** a **Velikost pásku**.

> [!NOTE]
> Tento postup lze také použít k přiřazení skupin atributů ke kategoriím v hierarchii kategorie navigace kanálu a doplňkové hierarchii kategorií produktu. V kroku 2 použijte následující navigační cesty:
>
> - **Maloobchod** &gt; **Správa kategorií a produktů** &gt; **Navigační kategorie kanálu**
> - **Maloobchod** &gt; **Správa kategorií a produktů** &gt; **Doplňkové kategorie produktů**

### <a name="assign-attribute-groups-to-retail-stores"></a>Přiřazení skupin atributů k maloobchodním prodejnám

Jednu nebo více skupin atributů lze přiřadit k jedné nebo více maloobchodním prodejnám v hierarchii maloobchodních prodejen. Po upravení produktů pro konkrétní maloobchodní prodejny, zdědí produkty atributy, které jsou zahrnuty ve skupinách atributů.

1. Přihlaste se ke klientovi účetního systému jako manažer maloobchodního prodeje.
2. Přejděte na **Maloobchod** &gt; **Nastavení kanálu** &gt; **Kategorie kanálu a atributy produktu**.
3. Přiřazení skupin atributů ke kanálu Houston:

    1. Vyberte kanál **Houston**.
    2. Na pevné záložce **Skupina atributů** vyberte **Přidat**a pak v poli **Název** vyberte **SharePointProvisionedProductAttributeGroup**.
    3. Vyberte znovu **Přidat** a poté v poli **Název** vyberte **Pánské pásky**.
    4. Vyberte znovu **Přidat** a poté v poli **Název** vyberte **Módní sluneční brýle**.

        > [!NOTE]
        > Možnost slouží k určení, že tento kanál má zdědit skupiny atributů ze svého nadřazeného kanálu v hierarchii. Nastavíte-li možnost **Zdědit** na **Ano**, podřízený uzel kanálu zdědí všechny skupiny atributů a všechny atributy v těchto skupinách atributů.

4. Povolte atributy, aby byly k dispozici v kanálu Houston:

    1. V podokně akcí zvolte **Nastavit metadata atributu**.
    2. Vyberte uzel kategorie **Móda** a poté na pevné záložce **Atributy produktu kanálu** vyberte **Zahrnout atribut** pro každý atribut.
    3. Vyberte uzel kategorie **Módní doplňky**, zvolte **Módní sluneční brýle** a poté na pevné záložce **Atributy produktu kanálu** vyberte **Zahrnout atribut** pro každý atribut.
    4. Vyberte uzel kategorie **Pánské oděvy**, zvolte **Kalhoty** a poté na pevné záložce **Atributy produktu kanálu** vyberte **Zahrnout atribut** pro každý atribut.

![Kategorie kanálu a atributy produktu - Skupiny atributů](media/CCPAttrGrp.png)

## <a name="overriding-attribute-values"></a>Přepsání hodnot atributů

Výchozí hodnoty atributů lze přepsat na úrovni produktu pro jednotlivé výrobky. Výchozí hodnoty lze přepsat pro jednotlivé produkty v určitých katalozích, které jsou určeny v konkrétní maloobchodní síti.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Přepsání hodnot atributu jednotlivého produktu

1. Přihlaste se ke klientovi účetního systému jako manažer maloobchodního prodeje.
2. Přejděte na **Maloobchod** &gt; **Správa kategorií a produktů** &gt; **Uvolněné produkty podle kategorie**.
3. Vyberte uzel kategorie **Móda** &gt; **Módní doplňky** &gt; **Módní sluneční brýle**.
4. Vyberte požadovaný produkt v mřížce. Poté v podokně akcí na kartě **Produkt** ve skupině **Nastavení** zvolte **Atributy produktu**.
5. V levém podokně vyberte atribut a aktualizujte jeho hodnotu v pravém podokně.

![Stránka podrobností produktu – Skupiny atributů produktů](media/ProdDetailsProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-catalog"></a>Přepsání hodnot atributu produktů v katalogu

1. Přihlaste se ke klientovi účetního systému jako manažer maloobchodního prodeje.
2. Přejděte na **Maloobchod** &gt; **Správa katalogu** &gt; **Všechny katalogy**.
3. Vyberte katalog **Základní katalog Fabrikam**.
4. Vyberte uzel kategorie **Móda** &gt; **Módní doplňky** &gt; **Módní sluneční brýle**.
5. Na pevné záložce **Produkty** vyberte požadovaný produkt a poté vyberte **Atributy** nad mřížkou produktu.
6. Na následujících pevných záložkách aktualizujte hodnoty požadovaných atributů:

    - Médium sdíleného produktu
    - Sdílené atributy produktu
    - Médium kanálu
    - Atributy produktu kanálu

    > [!NOTE]
    > Pokud jsou vytvořeny sdílené atributy produktu a sdílená média produktu v aplikaci Finance and Operations, vztahují se na všechny maloobchodní produkty.

![Skupiny atributu produktu katalogu](media/CatalogProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-channel"></a>Přepsání hodnot atributu produktů v kanálu

1. Přihlaste se ke klientovi účetního systému jako manažer maloobchodního prodeje.
2. Přejděte na **Maloobchod** &gt; **Nastavení kanálu** &gt; **Kategorie kanálu a atributy produktu**.
3. Vyberte kanál **Houston**.
4. Na pevné záložce **Produkty** vyberte požadovaný produkt a poté vyberte **Atributy** nad mřížkou produktu.

    > [!NOTE]
    > Pokud nejsou k dispozici žádné produkty, přidejte produkty volbou možnosti **Přidat** na pevné záložce **Produkty** a následným výběrem požadovaných produktů v dialogovém okně **Přidat produkty**.

5. Na následujících pevných záložkách aktualizujte hodnoty požadovaných atributů:

    - Médium sdíleného produktu
    - Sdílené atributy produktu
    - Médium kanálu
    - Atributy produktu kanálu

    > [!NOTE]
    > Pokud jsou vytvořeny sdílené atributy produktu a sdílená média produktu v aplikaci Finance and Operations, vztahují se na všechny maloobchodní produkty.

