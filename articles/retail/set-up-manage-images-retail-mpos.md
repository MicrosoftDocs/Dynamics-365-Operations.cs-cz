<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="set-up-manage-images-retail-mpos.md" target-language="cs-CZ">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>set-up-manage-images-retail-mpos.3cc4ad.c256569135a00ea98a5c059b9dd12a07a000ee6a.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>c256569135a00ea98a5c059b9dd12a07a000ee6a</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\set-up-manage-images-retail-mpos.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Set up and manage images for Retail Modern POS (MPOS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nastavení a správa obrázků pro Retail Modern POS (MPOS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article explains the steps that are involved in setting up and managing images for the various entities that appear in Retail Modern POS (MPOS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tento článek vysvětluje postup, který je součástí nastavení a správy obrázků pro různé entity, které jsou obsaženy v modulu Retail Modern POS (MPOS).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Set up and manage images for Retail Modern POS (MPOS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nastavení a správa obrázků pro Retail Modern POS (MPOS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This article explains the steps that are involved in setting up and managing images for the various entities that appear in Retail Modern POS (MPOS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tento článek vysvětluje postup, který je součástí nastavení a správy obrázků pro různé entity, které jsou obsaženy v modulu Retail Modern POS (MPOS).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Setting up the media base URL and defining media templates to configure the format for image URLs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nastavení základní adresy URL média a definování šablon média ke konfiguraci formátu adresy URL pro obrázek</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The images that appear in Retail Modern POS (MPOS) must be hosted externally, outside Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Obrázky zobrazené v Retail Modern POS (MPOS) musí být hostovány externě mimo Microsoft Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Typically, they are hosted in a content management system, content delivery network (CDN), or media server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Standardně jsou umístěny v systému správy obsahu, sítě dodávky obsahu (CDN) nebo serveru médií.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>MPOS then fetches and displays the images for the appropriate entities, such as products and catalogs, by accessing the target URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS pak prostřednictvím přístupu k cílové adrese URL načte a zobrazí obrázky odpovídajících entit, jako jsou například výrobky a katalogy.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>To fetch these externally hosted images, MPOS requires the correct URL format for the images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">K načtení těchto externě hostovaných obrázků MPOS je zapotřebí správný formát adresy URL pro obrázky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You can configure the required URL format for the images by setting up the <bpt id="p1">**</bpt>Media base URL<ept id="p1">**</ept> value in the channel profile and using the <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept> functionality for each entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Požadovaný formát adresy URL pro obrázky lze konfigurovat pomocí nastavení hodnoty <bpt id="p1">**</bpt>základní adresy URL média<ept id="p1">**</ept> v kanálu profilu a používáním funkce <bpt id="p2">**</bpt>šablony definování médií<ept id="p2">**</ept> pro každou entitu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>You can also overwrite the standard URL format for a subset of entities by using the <bpt id="p1">**</bpt>Edit in Excel<ept id="p1">**</ept> functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Standardní formát adresy URL pro podmnožinu entit je rovněž možné přepsat pomocí funkce <bpt id="p1">**</bpt>úpravy v aplikaci Excel<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In the current version of Dynamics 365 for Retail, you can no longer set up the URL format by using the <bpt id="p1">**</bpt>Image<ept id="p1">**</ept> attribute XML for MPOS in the <bpt id="p2">**</bpt>Default<ept id="p2">**</ept> attribute group for entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V aktuální verzi aplikace Dynamics 365 for Retail již nelze nastavit formát adresy URL pomocí atributu <bpt id="p1">**</bpt>Obrázek<ept id="p1">**</ept> XML pro MPOS ve <bpt id="p2">**</bpt>výchozí<ept id="p2">**</ept> skupině atributů entit.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>If you're familiar with Microsoft Dynamics AX 2012 R3 and are now using the current version of Dynamics 365 for Retail, make sure that you always use the new <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> functionality to set up images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud jste obeznámeni s aplikací Microsoft Dynamics AX 2012 R3 a nyní používáte aktuální verzi aplikace Dynamics 365 for Retail, ujistěte se, že vždy používáte novou funkci <bpt id="p1">**</bpt>Definovat šablonu média<ept id="p1">**</ept> k nastavení obrázků.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Don't use or modify the <bpt id="p1">**</bpt>Image<ept id="p1">**</ept> attribute in the <bpt id="p2">**</bpt>Default<ept id="p2">**</ept> attribute group for any entities, including products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Není možné použít nebo upravit atribut <bpt id="p1">**</bpt>obrázku<ept id="p1">**</ept> ve <bpt id="p2">**</bpt>výchozím<ept id="p2">**</ept> skupině atributů pro všechny entity včetně produktů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Changes that you make directly in the <bpt id="p1">**</bpt>Default<ept id="p1">**</ept> attribute group for images won't be reflected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Změny prováděné přímo ve <bpt id="p1">**</bpt>výchozí<ept id="p1">**</ept> skupině atributů pro obrázky se neodrazí.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>This option will be disabled in a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tato možnost bude zakázána v budoucích verzích.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In the following procedures, images are set up for the Catalog entity as an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V následujících procedurách jsou obrázky nastaveny jako příklad pro entitu katalogu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>These procedures will help guarantee that the correct image destination path is set implicitly for all catalog images that use a common path.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tyto postupy vám pomůžou zajistit, že správná cílová cesta obrázků je implicitně nastavena pro všechny obrázky katalogu používající obecnou cestu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>For example, if you've set up a media server or CDN externally, and want the images to appear in MPOS for a given store, the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> functionality helps you the set the path where MPOS can look up and retrieve the images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Například jestliže jste externě nastavili server médií nebo CDN a chcete, aby se obrázky zobrazily v MPOS pro daný obchod, funkce <bpt id="p1">**</bpt>Definovat šablonu média<ept id="p1">**</ept> vám usnadní nastavení cesty umístění, kde MPOS může vyhledat a získávat obrázky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>For this demo data example, the media server is deployed on the Retail Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro tento příklad ukázkových dat je nasazen server médií na serveru maloobchodu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>However, you can have it anywhere outside Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Můžete jej však mít kdekoli mimo aplikaci Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Set up the media base URL for a channel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nastavení základní adresy URL médií pro kanál</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Open the Dynamics 365 for Retail HQ portal.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Otevřete portál Dynamics 365 for Retail HQ.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Click <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Channel setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Channel profiles<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Klikněte na <bpt id="p1">**</bpt>Maloobchodní prodej<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Nastavení kanálu<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Profily kanálu<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Navigation<ept id="p1">](./media/channel-profile1.png)](./media/channel-profile1.png)</ept></source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Navigace<ept id="p1">](./media/channel-profile1.png)](./media/channel-profile1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>In the channel profile that your store uses for MPOS, update the <bpt id="p1">**</bpt>Media base URL<ept id="p1">**</ept> field with the base URL of your media server or CDN.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">V profilu kanálu, který váš obchod používá pro MPOS aktualizujte pole <bpt id="p1">**</bpt>Základní adresu URL média<ept id="p1">**</ept> se základní adresou URL serveru média nebo CDN.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The base URL is the first part of the URL that is shared by all image folders of different entities.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Základní adresa URL je první část adresy URL, která je společná pro všechny složky obrázku různých entit.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Channel profiles page<ept id="p1">](./media/channel-profile2.png)](./media/channel-profile2.png)</ept></source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Stránka profilů kanálu<ept id="p1">](./media/channel-profile2.png)](./media/channel-profile2.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Define the media template for an entity</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Definování šablon médií pro entitu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Click <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Catalog management<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Catalog images<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Klikněte na <bpt id="p1">**</bpt>Maloobchodní prodej<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Správa katalogu<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Obrázky katalogu<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>On the <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> page, on the Action Pane, click <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Na stránce <bpt id="p1">**</bpt>Obrázky katalogu<ept id="p1">**</ept> v podokně akcí klepněte na příkaz <bpt id="p2">**</bpt>Definovat šablonu média<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Entity<ept id="p2">**</ept> field, <bpt id="p3">**</bpt>Catalog<ept id="p3">**</ept> should be selected by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V dialogovém okně <bpt id="p1">**</bpt>Definovat šablonu média<ept id="p1">**</ept> v poli <bpt id="p2">**</bpt>Entita<ept id="p2">**</ept>, má být výchozí nastavení na <bpt id="p3">**</bpt>Katalog<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>On the <bpt id="p1">**</bpt>Media path<ept id="p1">**</ept> FastTab, enter the remaining path of the image location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Na pevné záložce <bpt id="p1">**</bpt>Cesta média<ept id="p1">**</ept> zadejte zbývající cestu k místu obrázku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The media path supports <bpt id="p1">**</bpt>LanguageID<ept id="p1">**</ept> as a variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Cesta média podporuje <bpt id="p1">**</bpt>LanguageID<ept id="p1">**</ept> jako proměnnou.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>For example, for the demo data, you can create a <bpt id="p1">**</bpt>Catalogs<ept id="p1">**</ept> folder for all catalog images under the media base URL for your media server (<ph id="ph1">`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer`</ph>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Například pro ukázková data můžete vytvořit složku <bpt id="p1">**</bpt>Katalogy<ept id="p1">**</ept> pro všechny katalogové obrázky na základní adrese URL médií pro váš serveru médií (<ph id="ph1">`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer`</ph>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>You can then have a folder for each language, such as en-US or fr-FR, and copy the appropriate images under each folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Můžete pak mít složku pro každý jazyk, jako je například en-US nebo fr-FR a zkopírovat příslušné obrázky do každé složky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>If you don't have different images for the various languages, you can omit the <bpt id="p1">**</bpt>LanguageID<ept id="p1">**</ept> variable from your folder structure and point directly to the Catalogs folder that contains the catalog images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud nemáte různé obrázky pro různé jazyky, můžete vynechat proměnnou <bpt id="p1">**</bpt>LanguageID<ept id="p1">**</ept> ze své složkové struktury a poukázat přímo na složku katalogů, která bude obsahovat katalogové obrázky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The current version of Dynamics 365 for Retail supports the <bpt id="p1">**</bpt>{LanguageId}<ept id="p1">**</ept> token for Catalog, Product, and Category entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Poznámka: Aktuální verze aplikace Dynamics 365 for Retail podporuje token <bpt id="p1">**</bpt>{LanguageId}<ept id="p1">**</ept> pro entity katalog, produkt a kategorie.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>(The <bpt id="p1">**</bpt>{LanguageID}<ept id="p1">**</ept> token isn't supported for Customer and Worker entities, according to the existing standard that has been effective since Microsoft Dynamics AX 6.x.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(Token <bpt id="p1">**</bpt>{LanguageID}<ept id="p1">**</ept> není podporován pro odběratele a jednotky pracovníků, podle existujícího standardu, který byl platná od verze aplikace Microsoft Dynamics AX 6.x.)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>For images, the file name format is hard-coded to the catalog name and can't be changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro obrázky je formát názvu souboru pevně zakódován do názvu katalogu a nemůže být změněn.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Therefore, rename your images so that they have appropriate catalog names, to help guarantee that MPOS handles them correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Z tohoto důvodu přejmenujte své obrázky, aby měly odpovídající katalogové názvy, abyste si zajistili, že je MPOS zpracovávají správně.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In the <bpt id="p1">**</bpt>File Extension<ept id="p1">**</ept> field, select the expected file name extension, depending on the type of images that you have.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V poli <bpt id="p1">**</bpt>Přípona souboru<ept id="p1">**</ept> vyberte očekávané přípony názvu souboru, v závislosti na typu obrázku, které máte.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>For example, for the demo data, the catalog images are set to the .jpg extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Například pro ukázková data jsou katalogové obrázky nastaveny na příponu .jpg.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>(The image files are also renamed so that they have catalog names.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(Obrázkové soubory také přejmenujte tak, aby měly katalogové názvy.)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Klikněte na tlačítko <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>To validate that the media template for images has been saved correctly, on the <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept> again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">K ověření, zda šablony média pro obrázky byly uloženy správně, na stránce <bpt id="p1">**</bpt>Katalogové obrázky<ept id="p1">**</ept> klepněte znovu na <bpt id="p2">**</bpt>Definovat šablonu média<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>To validate the template without closing the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box, you can use the <bpt id="p2">**</bpt>Generate Image URLs for Excel<ept id="p2">**</ept> FastTab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">K ověření šablony, aniž byste zavřeli dialogového okno <bpt id="p1">**</bpt>Definovat šablonu média<ept id="p1">**</ept> můžete použít pevnou záložku <bpt id="p2">**</bpt>Generovat adresy URL obrázku pro Excel<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Check the appearance of the image URL, and verify that the URL complies with the template standard that was mentioned earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zkontrolujte vzhled adresy URL obrázku, ověřte, že adresa URL odpovídá standardu šablony, uvedenému výše.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>The <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box has now set the image path implicitly for all catalog images that use this common URL path.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dialogové okno <bpt id="p1">**</bpt>Definovat šablonu média<ept id="p1">**</ept> je nyní implicitně nastaven na cestu k obrázku pro všechny katalogové obrázky, které používají tuto běžnou cestu URL.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>This URL path applies to all catalog images unless they are overwritten.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tato cesta URL se vztahuje na všechny katalogové obrázky do doby, než budou přepsány.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The first part of the image path is taken from the media base URL that you defined in the channel profile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">První část cesty obrázku je převzata ze základní adresy URL média, které jste definovali v profilu kanálu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The remaining part of the path is taken from the path that you defined in the media template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zbývající část cesty je převzata z cesty, kterou jste definovali v šabloně média.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>The two parts are concatenated to provide the full URL of the image location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Obě části jsou spojeny, aby poskytly úplnou adresu URL obrázku skladového místa.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>For example, a catalog in the demo data is named Fabrikam Base Catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Například katalog v ukázkových datech je nazván Fabrikam Base Catalog.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Therefore, the image name must be Fabrikam Base Catalog.jpg so that it uses the catalog name and the .jpg file name extension that is configured in the template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Název proto musí být Fabrikam Base Catalog.jpg, aby byl používán název katalogu a přípona souboru .jpg, která je nastavena do šablony.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>In this case, after concatenation, the URL will be <ph id="ph1">`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg`</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V tomto případě bude po zřetězení URL adresa <ph id="ph1">`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg`</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Run the synchronization jobs to push the new template to the channel database, so that MPOS can use the template to access the images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Spusťte úlohy synchronizace pro zadání nové šablony do databáze kanálů, aby MPOS mohl šablonu použít pro přístup k obrázkům.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>To update the media template for catalog images on the channel side, be sure to run <bpt id="p1">**</bpt>Catalog Job 1150<ept id="p1">**</ept> from <bpt id="p2">**</bpt>Retail IT<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Distribution schedule<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Pokud chcete aktualizovat šablonu médií pro katalogové obrázky na straně kanálu média, je nutné spustit <bpt id="p1">**</bpt>Úlohu katalogu 1150<ept id="p1">**</ept> z <bpt id="p2">**</bpt>maloobchodního IT<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Plán distribuce<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Define media template dialog box<ept id="p1">](./media/catalog1.png)](./media/catalog1.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Dialogové okno Definovat šablonu média<ept id="p1">](./media/catalog1.png)](./media/catalog1.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Previewing an image from the entity level</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Náhled obrázku z úrovně entity</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>From the page for the entity item in HQ, you can preview the image that uses the image URL that is derived from the media template.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Ze stránky pro položky entit v centrále můžete zobrazit náhled obrázku, který používá adresa URL obrázku odvozenou ze šablony média.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>For this example, go to the appropriate catalog, and then, on the Action Pane, click <bpt id="p1">**</bpt>Media<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Images<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V tomto příkladu přejděte do odpovídajícího katalogu, a poté v podokně akcí klikněte na možnost <bpt id="p1">**</bpt>Média<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Obrázky<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Use the drop-down list to select different stores that might have different channel profiles.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Chcete-li vybrat jiné obchody, které mohou mít různé profily kanálů, použijte rozevírací seznam.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>To edit or remove the implicit media template, you must return to the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box for the <bpt id="p2">**</bpt>Catalog images<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">K úpravě nebo odstranění šablony implicitního média, se musíte vrátit do dialogového okna <bpt id="p1">**</bpt>Definovat šablonu média<ept id="p1">**</ept> pro stránku <bpt id="p2">**</bpt>Katalogové obrázky<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>You can use the <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Remove<ept id="p2">**</ept> buttons to manually change the path that is based on the implicit template and used for a specific image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lze použít tlačítka <bpt id="p1">**</bpt>Přidat<ept id="p1">**</ept> a <bpt id="p2">**</bpt>Odebrat<ept id="p2">**</ept> pro ruční změnu cesty, která je založena na implicitní šabloně a je využívána pro konkrétní obrázek.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>For more information, see the <bpt id="p1">[</bpt>Overwriting the media template for entity items<ept id="p1">](#overwriting-the-media-template-for-entity-items)</ept> section later in this article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Další informace naleznete v části <bpt id="p1">[</bpt>Přepsání šablony médií pro položky entit<ept id="p1">](#overwriting-the-media-template-for-entity-items)</ept> v další části tohoto článku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>After you've finished previewing an image and making any changes that you require, start the MPOS instance for the appropriate store, and see whether the catalog images are shown.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Poté, co jste dokončili náhled obrázku a provedli jakékoli změny, které jste požadovali, spusťte instanci MPOS odpovídajícího obchodu a podívejte se, zda se zobrazily katalogové obrázky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Images dialog box<ept id="p1">](./media/catalog4.png)](./media/catalog4.png)</ept></source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Dialogové okno Obrázky<ept id="p1">](./media/catalog4.png)](./media/catalog4.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>You can use the same procedure for all the five entities that are supported: Worker, Customer, Catalog, Category, and Products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Stejný postup lze použít pro všech pět entit, které jsou podporovány: pracovníka, odběratele, katalog, kategorie a produkty.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>"Catalog Products" (products that are set at the catalog level) and "Channel Products" (products that are set at the channel level) use the media template that is set for the Products entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">„Katalogové produkty“ (produkty, které jsou nastaveny na úrovni katalogu) a „Produkty kanálu“ (produkty, které jsou nastaveny na úroveň kanálu) používají šablonu média, která je nastavena pro entitu produktů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>For the Products media template, you can select the number of product images to show per product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro šablonu médií produktů můžete vybrat číslo obrázků produktů, které mají být zobrazeny po produktu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>You can also set the default image for a given product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Můžete také nastavit pro daný produkt výchozí obrázek.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>In this way, you can prevent blank images in MPOS and help to control which image is used as the default image for a product item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tímto způsobem lze zabránit prázdným obrázkům v MPOS a pomoci řídit, který obrázek se používá jako výchozí obrázek vyráběnou položku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>In the following example, each product has five images, and the first image is set as the default image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V následujícím příkladu má každý produkt pět obrázků a první obrázek je nastaven jako výchozí obrázek.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Variant products are treated the same way as master products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Varianty produktů jsou zpracovány stejným způsobem jako hlavní produkty.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The file name of the image file should be based on the product number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Název souboru obrazového souboru má být založen na čísle produktu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Some characters are also escaped while the file name is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Některé znaky také unikly, zatímco byl vytvářen název souboru.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Therefore, it's a good to verify the file name by using the <bpt id="p1">**</bpt>Generate Image URLs for Excel<ept id="p1">**</ept> section.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Je tedy dobré ověřit název souboru za použití oddílu <bpt id="p1">**</bpt>Generovat adresy URL obrázku pro Excel<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Define media template dialog box<ept id="p1">](./media/prods.png)](./media/prods.png)</ept></source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Dialogové okno Definovat šablonu média<ept id="p1">](./media/prods.png)](./media/prods.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Synchronization jobs to send a media template to the channel side</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Úlohy pro synchronizaci k odeslání šablony média na stránku kanálu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>For all the five supported entities (Worker, Customer, Catalog, Category, and Products), whenever you update the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog to set up an image, make sure that you run the Catalog job (1150) from <bpt id="p2">**</bpt>Retail IT<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Distribution schedule<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro všech pět podporovaných entit (pracovník, odběratel, katalog, kategorie a produkty), vždy při každé aktualizaci dialogového okna <bpt id="p1">**</bpt>Definovat šablonu média<ept id="p1">**</ept> k nastavení obrázku se ujistěte, že provedete úlohu katalogu (1150) z části <bpt id="p2">**</bpt>Maloobchodní IT<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Plán distribuce<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This job will enable the updated media template to be synced to the channel and used by MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tato úloha umožní synchronizaci aktualizované šablony médií ke kanálu a její používání MPOS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Run the Catalog job (1150) after you make any of the following changes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Spustíte úlohu katalogu (1150) po provedení následujících změn:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>You update the Catalog image media template from <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šablonu média katalogových obrázků aktualizujete možností <bpt id="p1">**</bpt>Katalogové obrázky<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Definovat šablonu média<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>You update the Employee image media template from <bpt id="p1">**</bpt>Employee images<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šablonu média obrázků zaměstnanců aktualizujete možností <bpt id="p1">**</bpt>Obrázky zaměstnance<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Definovat šablonu média<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>You update the Customer image media template from <bpt id="p1">**</bpt>Customer image<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šablonu média obrázků odběratelů aktualizujete možností <bpt id="p1">**</bpt>Obrázek odběratele<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Definovat šablonu média<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>You update the Product image media template from <bpt id="p1">**</bpt>Product images<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šablonu média obrázků produktů aktualizujete možností <bpt id="p1">**</bpt>Obrázky produktů<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Definovat šablonu média<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You update the Category image media template from <bpt id="p1">**</bpt>Category images<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Šablonu média obrázků kategorií aktualizujete možností <bpt id="p1">**</bpt>Obrázky kategorií<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Definovat šablonu média<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>You must also publish the channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Také musíte publikovat kanál.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Overwriting the media template for entity items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Přepsání šablon médií pro položky entity</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>As you learned in the previous section, the media template for a given entity supports only one common path.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jak jste se již dozvěděli v předchozím oddílu, šablona média dané entity podporuje pouze jednu společnou cestu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>This path is based on the media base URL that is configured and the media path that is defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tato cesta je založena na základní adrese URL média, která je nakonfigurovaná a cesty média, která je definována.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>However, in many cases, a retailer wants to be able to use images from different sources for a subset of items in an entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nicméně v mnoha případech maloobchodní prodejce chce používat obrázky z různých zdrojů pro podmnožinu položek v entitě.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>For example, a store uses the self-hosted media server for one set of catalog images but uses CDN URLs for another set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Například obchod používá vlastní hostovaný server médií pro jednu sadu obrázků katalogu, ale pro jinou sadu používá CDN adresy URL.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>To overwrite image URLs that are based on a media template for entity images at the entity level, you can use the Edit in Excel and Manual edit functionality from the <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro přepsání adresy URL obrázku, která je založena na šabloně médií pro obrázky entity na úrovni entity, můžete pro stránku <bpt id="p1">**</bpt>Náhled<ept id="p1">**</ept> použít funkce úprav a ručních úprav v aplikaci Excel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Overwrite by using Edit in Excel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Přepsání pomocí úprav v aplikaci Excel</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Click <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Catalog management<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Catalog images<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Klikněte na <bpt id="p1">**</bpt>Maloobchodní prodej<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Správa katalogu<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Obrázky katalogu<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>On the <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Na stránce <bpt id="p1">**</bpt>Obrázky katalogu<ept id="p1">**</ept> klepněte na příkaz <bpt id="p2">**</bpt>Definovat šablonu média<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>In the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Entity<ept id="p2">**</ept> field, <bpt id="p3">**</bpt>Catalog<ept id="p3">**</ept> should be selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V dialogovém okně <bpt id="p1">**</bpt>Definovat šablonu média<ept id="p1">**</ept> v poli <bpt id="p2">**</bpt>Entita<ept id="p2">**</ept>, má být nastavení na hodnotu <bpt id="p3">**</bpt>Katalog<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>On the <bpt id="p1">**</bpt>Media path<ept id="p1">**</ept> FastTab, notice the image location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Na pevné záložce <bpt id="p1">**</bpt>Cesta média<ept id="p1">**</ept> si povšimněte umístění obrázku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>On the <bpt id="p1">**</bpt>Generate Image URLs for Excel<ept id="p1">**</ept> FastTab, click <bpt id="p2">**</bpt>Generate<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Na pevné záložce <bpt id="p1">**</bpt>Generovat adresy URL obrázku pro Excel<ept id="p1">**</ept> klepněte na tlačítko <bpt id="p2">**</bpt>Generovat<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Whenever the media template is changed, you must click <bpt id="p1">**</bpt>Generate<ept id="p1">**</ept> before you can use the Edit in Excel functionality.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kdykoli při změně šablony média je před použitím funkcí úpravy v aplikaci Excel nutné klepnout na <bpt id="p1">**</bpt>Generovat<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Generate Image URLs for Excel FastTab<ept id="p1">](./media/excel1.jpg)](./media/excel1.jpg)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Generování URL adres obrázků pro záložku s náhledem Excel<ept id="p1">](./media/excel1.jpg)](./media/excel1.jpg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>You now see a preview of the image URLs that were generated based on the last saved media template.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Nyní můžete zobrazit náhled adres URL obrázků, které byly vygenerovány na základě naposledy uložené šablony média.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Generate Image URLs for Excel FastTab after Generate is selected<ept id="p1">](./media/excel2.png)](./media/excel2.png)</ept></source><target logoport:matchpercent="0" state="translated"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Generování URL adres obrázků pro záložku s náhledem Excel po volbě Generovat<ept id="p1">](./media/excel2.png)](./media/excel2.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>The URLs that are generated for Excel use the path and conventions of the media template that is defined.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Adresy URL generované pro aplikaci Excel používají cestu a konvence šablony média, která je definována.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>These conventions include the conventions for file names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tyto konvence zahrnují konvence pro názvy souborů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>The expectation is that you've set up the physical images outside Dynamics 365 for Retail, and the images can be retrieved from the URLs that are derived from the media template that you defined earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Předpokladem je, že jste nastavili fyzické obrázky mimo aplikaci Dynamics 365 for Retail a obrázky lze získat z adresy URL, která je odvozena z šablony média, kterou jste definovali dříve.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>You can overwrite these derived URLs by using the Edit in Excel functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Odvozené adresy URL lze přepisovat použitím funkcí úpravy v aplikaci Excel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Click <bpt id="p1">**</bpt>Edit in Excel<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Klepněte na <bpt id="p1">**</bpt>Upravit v aplikaci Excel<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>After the Microsoft Excel worksheet is opened, click <bpt id="p1">**</bpt>Enable edit<ept id="p1">**</ept> when you're prompted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Po otevření sešitu aplikace Microsoft Excel po zobrazení výzvy klepněte na tlačítko <bpt id="p1">**</bpt>povolit úpravu<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>When you're prompted, click <bpt id="p1">**</bpt>Trust this add-in<ept id="p1">**</ept> in the right pane, and wait for the add-in to complete the installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Po zobrazení výzvy klepněte v pravém podokně na možnost <bpt id="p1">**</bpt>Důvěřovat tomuto doplňku<ept id="p1">**</ept> a počkejte, až doplněk dokončí instalaci.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Trust this add-in<ept id="p1">](./media/excel4.jpg)](./media/excel4.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Důvěřovat tomuto doplňku<ept id="p1">](./media/excel4.jpg)](./media/excel4.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>If you're prompted to sign in, enter the credentials that you used to sign in to HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud budete vyzváni k přihlášení, zadejte pověření používané pro přístup k centrále.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Sign-in prompt<ept id="p1">](./media/excel5.png)](./media/excel5.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Výzva k přihlášení<ept id="p1">](./media/excel5.png)](./media/excel5.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>After you sign in, you should be able to see the list of image URLs for the various catalog entries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Poté, co se přihlásíte, je třeba zobrazit seznam adres URL obrázků pro různé položky katalogu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>You edit, add, and remove the image URLs for various entity items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Upravujte, přidávejte a odebírejte adresy URL obrázků pro různé položky entity.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>For all entities except Products, you can overwrite the image URLs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro všechny entity s výjimkou produktů je možné přepsat adresy URL obrázku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Modify the existing image URL, so that it uses the new destination URL of the image, and update the file name with the new file name for the image file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Upravte stávající adresu URL obrázku tak, aby používala novou cílovou adresu URL obrázku a aktualizujte název souboru novým názvem souboru pro soubor obrázku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>The file name must be unique to help guarantee that the record is unique.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Název souboru musí být jedinečný, aby pomohl zajistit, že daný záznam je jedinečný.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Overwrite the image URLs in Excel<ept id="p1">](./media/excel6.jpg)](./media/excel6.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Přepis adres URL obrázku v Excelu<ept id="p1">](./media/excel6.jpg)](./media/excel6.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>When you overwrite image URLs for Products entities by using the Edit in Excel functionality or the entity item page, MPOS always shows all the media template image URLs together with the overwritten image URLs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Při přepsání adres URL obrázku pro entity produktů pomocí funkce úprav aplikace Excel nebo stránky s položkami entity MPOS vždy zobrazí všechny adresy URL obrázku šablon médií spolu s přepsaným obrázkem adresy URL.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>After you've finished making your changes, click <bpt id="p1">**</bpt>Publish in Excel<ept id="p1">**</ept> to create a new explicit association entry.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jakmile jste ukončili provádění změn, klepněte na možnost <bpt id="p1">**</bpt>Publikovat v aplikaci Excel<ept id="p1">**</ept> a vytvoříte novou položku explicitního přidružení.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Return to HQ, and click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vraťte se do centrály a klepněte na tlačítko <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Run the appropriate synchronization jobs for the entity, and check the preview on the entity page or in MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Spusťte odpovídající úlohy synchronizace pro entitu a zkontrolujte náhled na stránce entit nebo v MPOS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Creating new records</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vytvoření nových záznamů</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>You can create new records in Excel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Můžete vytvořit nové záznamy v aplikaci Excel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>However, make sure that you provide the correct information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ověřte však, že poskytnete správné informace.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>For example, to create a new entry for a catalog, make sure that the catalog ID and catalog name are correct, and also provide a unique file name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Například k vytvoření nové položky pro katalog zkontrolujte, že jsou správné ID katalogu a název katalogu, a také zadejte jedinečný název souboru.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The unique file name is very important, because the uniqueness of records in Excel is validated during publishing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jedinečný název souboru je velmi důležitý, protože během publikování je v aplikaci Excel ověřována jedinečnost záznamů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>First copy the details from the catalog that you want to create a new record for, and copy the record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nejprve zkopírujte údaje z katalogu, pro který chcete vytvořit nový záznam, a záznam zkopírujte.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>You just have to update the file name and URL, because the rest of the information will be same.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Musíte aktualizovat název souboru a adresa URL, protože zbývající informace budou stejné.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>To create new records for Product entity items, you use the same basic procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">K vytvoření nových záznamů pro položky entit produktu můžete použít stejný základní postup.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>From the Excel worksheet, copy an existing record for the product that you to create a new record for, and then replace the image URL and filename.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ze sešitu aplikace Excel zkopírujte existující záznam pro produkt, pro který chcete vytvořit nový záznam a poté nahraďte adresu URL obrázku a název souboru.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Make sure that the file name is unique.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ujistěte se, že název souboru je jedinečný.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Deleting an existing record</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Odstranění existujícího záznamu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Only the overwritten image URL records can be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Odstranit lze pouze přepsané záznamy adresy URL obrázku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>After an image is deleted and synchronization is completed, the image will no longer appear on the <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page or in MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Po dokončení odstranění a synchronizace se již obrázek nebude zobrazovat na stránce <bpt id="p1">**</bpt>Náhled<ept id="p1">**</ept> nebo v MPOS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Image URL records that are derived from the media template can't be deleted, because these records are always derived from the media template every time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Záznamy URL obrázku, které jsou odvozeny ze šablony média, nelze odstranit, protože tyto záznamy jsou vždy odvozeny od šablony média.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Overwrite from the entity-level Preview page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Přepsání ze stránky náhledu úrovně entit</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>For all entities except Products, you can overwrite the image URL for a given entity item at the entity item level from the <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro všechny entity s výjimkou produktů, je možné přepsat adresu URL obrázku pro danou položku entity na úrovni položky entity ze stránky <bpt id="p1">**</bpt>Náhled<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>For Products, you can use the "Catalog Products" entity page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro produkty můžete použít stránku entit „Produkty v katalogu“.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>This example shows how to overwrite a catalog image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tento příklad ukazuje, jak přepsat obrázek v katalogu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Click <bpt id="p1">**</bpt>Catalogs<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Media<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Images<ept id="p3">**</ept>, and select the catalog image to update.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Klikněte na možnost <bpt id="p1">**</bpt>Katalogy<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Média<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Obrázky<ept id="p3">**</ept> a vyberte k aktualizaci obrázek v katalogu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>, and enter the image URL to overwrite the media template URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Klepněte na tlačítko <bpt id="p1">**</bpt>Přidat<ept id="p1">**</ept> a zadejte adresu URL obrázku k přepsání adresy URL šablony média.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>If you want this image to be shown in MPOS for the catalog, you can set it as the default image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Potřebujete-li, aby se tento obrázek zobrazil v MPOS pro katalog, můžete jej nastavit jako výchozí obrázek.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Klepněte na tlačítko <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>The image URL is updated for this catalog image, and a preview is shown.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Adresa URL obrázku je aktualizovaná pro tento obrázek v katalogu a zobrazuje se náhled.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>URL updated in the New image dialog box<ept id="p1">](./media/preview3.png)](./media/preview3.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Aktualizovaná adresa URL v dialogovém okně Nový obrázek<ept id="p1">](./media/preview3.png)](./media/preview3.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>You can also see the image preview for all overwritten image URLs on the <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> gallery page.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Můžete také zobrazit náhled obrázku pro všechny přepsané adresy URL obrázku na stránce s galerií <bpt id="p1">**</bpt>Obrázky v katalogu<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Catalog images gallery page<ept id="p1">](./media/preview-4.png)](./media/preview-4.png)</ept></source><target logoport:matchpercent="0" state="translated"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Stránka s galerií obrázků katalogu<ept id="p1">](./media/preview-4.png)](./media/preview-4.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Currently, the gallery doesn't show image previews for media template image URLs.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">V současné době galerie nezobrazuje náhledy obrázků pro šablony médií adres URL obrázků.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>For Catalog, Worker, Customer, and Category entities, if the user explicitly provides a URL through this page, we recommend that you indicate which image is the default image, because Retail Server clients show only one image per Catalog, Customer, Worker, and Category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro entity katalogu, pracovníka, odběratele a kategorie, pokud uživatel explicitně poskytne adresy URL prostřednictvím této stránky, doporučujeme naznačit, který obrázek bude výchozí obrázek, protože klienty serveru maloobchodu zobrazují pouze jeden obrázek pro katalog, odběratele, pracovníka a kategorii.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>If the user doesn't specify a default image, the system determines the default image and send it to the Retail service caller (MPOS or Ecommerce).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud uživatel nezadá výchozí obrázek, systém určí výchozí obrázek a odešlete jej volajícímu maloobchodních služeb (MPOS nebo obchodní stránky).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Overwrite the image URL for catalog product images from the Preview page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Přepsání adresy URL obrázku pro obrázky produktů v katalogu ze stránky náhledu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>To overwrite image URLs for catalog product images, you must use the <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro přepsání adresy URL obrázku pro obrázky produktů v katalogu musíte použít ze stránku <bpt id="p1">**</bpt>Náhled<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>You can't use the Edit in Excel functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nelze používat funkce úprav v aplikaci Excel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>To overwrite product images at a catalog level, select a catalog, and then select the product to overwrite the image for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud chcete přepsat obrázky produktů v úrovni katalogu, vyberte katalog, poté vyberte produkt, jehož obrázek bude přepsán.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Click <bpt id="p1">**</bpt>Attributes<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Klikněte na možnost <bpt id="p1">**</bpt>Atributy<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>On the next page, select <bpt id="p1">**</bpt>Image<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Edit<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Na další stránce vyberte <bpt id="p1">**</bpt>Obrázek<ept id="p1">**</ept>, a pak klikněte na tlačítko <bpt id="p2">**</bpt>Upravit<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>The <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page opens as a slider dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stránka <bpt id="p1">**</bpt>Náhled<ept id="p1">**</ept> se otevře jako posuvné dialogové okno.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>, and overwrite the image URL with a new URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Klepněte na tlačítko <bpt id="p1">**</bpt>přidat<ept id="p1">**</ept> a adresu URL obrázku přepište novou adresou URL.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Klepněte na tlačítko <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>You now see the preview of the new image and can set it as the default image.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Nyní vidíte náhled nového obrázku a můžete jej nastavit jako výchozí obrázek.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Image preview in the New image dialog box<ept id="p1">](./media/cat3.png)](./media/cat3.png)</ept></source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Náhled obrázku v dialogovém okně Nový obrázek<ept id="p1">](./media/cat3.png)](./media/cat3.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>After category image association, you must publish the channel and run the Channel job to help guarantee that the changes are published to the channel database.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Po přidružení obrázků kategorie musíte publikovat kanálu a spustit úlohu kanálu, abyste mohli zajistit, že změny jsou publikované do databáze kanálů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Setting up images to appear in Offline mode for MPOS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nastavení obrázků zobrazení v offline režimu pro MPOS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>MPOS can run in Online mode (when MPOS connected to Retail Server) or Offline mode (when there is no Retail Server or network connectivity, and transactions are stored in a local offline database).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS můžete spustit v online režimu (je-li MPOS připojeno k maloobchodnímu serveru) nebo v offline režimu (pokud neexistuje maloobchodní server nebo připojení k síti, a transakce jsou uloženy v místní offline databázi).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>When MPOS runs in Offline mode, it can't get images from the external image server to display from Retail Server, because Retail Server connectivity has been lost.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Při spuštění MPOS v offline režimu nelze získat obrázky z externího serveru obrázků pro zobrazení z maloobchodního serveru, protože se ztratilo připojení k maloobchodnímu serveru.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>However, you can still set up images so that they are shown when MPOS runs in Offline mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stále však můžete nastavit obrázky tak, aby se zobrazily při spuštění MPOS v offline režimu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Set up product images to appear in Offline mode for MPOS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nastavení obrázků produktů zobrazení v offline režimu pro MPOS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>The product images that must be used in Offline mode can be set up by uploading the required physical image into the base product image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Obrázky produktu, které je nutné použít v offline režimu lze nastavit odesláním požadovaného fyzického obrázku do obrázku základního produktu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Click <bpt id="p1">**</bpt>Product information management<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Products<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Products<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Klikněte na <bpt id="p1">**</bpt>Řízení informací o produktech<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Produkty<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Produkty<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Select the product to set the offline image for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vyberte produkt, pro který chcete nastavit offline obrázek.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Click <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>, and then click the arrow in the right corner to show the right pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Klepněte na tlačítko <bpt id="p1">**</bpt>Upravit<ept id="p1">**</ept> a poté klepněte na šipku v pravém horním rohu, abyste zobrazili pravé podokno.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>On the <bpt id="p1">**</bpt>Product image<ept id="p1">**</ept> FastTab, click <bpt id="p2">**</bpt>Change image<ept id="p2">**</ept>, and upload the physical image to use for the selected product in Offline mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Na pevné záložce <bpt id="p1">**</bpt>Obrázek produktu<ept id="p1">**</ept> klepněte na tlačítko <bpt id="p2">**</bpt>Změnit obrázek<ept id="p2">**</ept> a odešlete fyzický obrázek pro použitá vybraného produktu v offline režimu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Save and close the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Uložit a zavřít stránku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>While MPOS is in Online mode, run the Catalog job in HQ, to make sure that the data is sent at least one time to the offline database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Při online režimu MPOS spusťte úlohu katalogu v ústředí, abyste se ujistili, že data jsou odeslána alespoň jednou do offline databáze.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Put MPOS into Offline mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS přepněte do offline režimu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>You should see the image that you uploaded for the specific product in HQ.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Zobrazí se obrázek, který jste odeslali určitého výrobku v ústředí.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Product image in Offline mode<ept id="p1">](./media/offline1.png)](./media/offline1.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Obrázek produktu v offline režimu<ept id="p1">](./media/offline1.png)](./media/offline1.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Set up catalog, category, employee, and customer images to appear in Offline mode for MPOS</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Nastavení obrázků katalogu, kategorie, zaměstnance a odběratele pro zobrazení v offline režimu MPOS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>The catalog, category, employee, and customer images that must be used in Offline mode can be set up by adding the required image's destination link to the gallery and setting the image as the default image for the selected entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Obrázky katalogu, kategorie, zaměstnance a odběratelů, které musí být použity v offline režimu, lze nastavit přidáním požadovaného odkazu cíle obrázku do galerie a nastavením obrázku jako výchozího obrázku pro vybranou entitu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Go to the catalog, and then, on the Action Pane, click <bpt id="p1">**</bpt>Media<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Images<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Přejděte na katalog a poté v podokně akci klepněte na <bpt id="p1">**</bpt>Média<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Obrázky<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Follow the steps in the <bpt id="p1">[</bpt>Overwrite from the entity-level Preview page<ept id="p1">](#overwrite-from-the-entity-level-preview-page)</ept> section to add the external image URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Postupujte podle části <bpt id="p1">[</bpt>Přepsání ze stránky náhledu úrovně entit<ept id="p1">](#overwrite-from-the-entity-level-preview-page)</ept> pro přidání externí adresy URL obrázku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Mark this image as the default image for the catalog by selecting the check box against the Image listed in the grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Označte tento obrázek jako výchozí obrázek katalogu zaškrtnutím políčka proti obrázku uvedeného v mřížce.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Run the Catalog job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Spusťte úlohu katalogu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>This image will now be used as the Offline image for that catalog in MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tento obrázek bude nyní použit jako offline obrázek pro tento katalog v MPOS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Follow a similar process for other entities, such as Category, Employee, and Customer.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Postupujte podobně pro ostatní entity, jako je například kategorie, zaměstnanec a odběratel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Offline image<ept id="p1">](./media/offline2.png)](./media/offline2.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Offline obrázek<ept id="p1">](./media/offline2.png)](./media/offline2.png)</ept></target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>