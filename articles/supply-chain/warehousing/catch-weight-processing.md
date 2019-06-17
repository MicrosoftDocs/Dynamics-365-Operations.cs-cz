<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="catch-weight-processing.md" target-language="cs-CZ">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>catch-weight-processing.d3ca7d.6e295456838ca0195a472518b5979dfdc7819f74.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>6e295456838ca0195a472518b5979dfdc7819f74</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>19859d8566a8c7840066b2c10c6b08b67f1b83f4</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/04/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\supply-chain\warehousing\catch-weight-processing.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Catch weight product processing with warehouse management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zpracování produktu se skutečnou hmotností pomocí řízení skladu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to use work templates and location directives to determine how and where work is done in the warehouse.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toto téma popisuje způsob použití šablon práce a směrnic skladového místa k určení, jak a kde se práce ve skladu provádí.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Catch weight product processing with warehouse management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zpracování produktu se skutečnou hmotností pomocí řízení skladu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Feature exposure</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Expozice funkce</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>To use warehouse management to process catch weight products, you must use a license configuration key to turn on the functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Chcete-li použít řízení skladu pro zpracování produktů se skutečnou hmotností, musíte pro zapnutí této funkce použít licenční konfigurační klíč.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>(Go to <bpt id="p1">**</bpt>System administration <ph id="ph1">\&gt;</ph> Setup <ph id="ph2">\&gt;</ph> License configuration<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(Přejděte do nabídky <bpt id="p1">**</bpt>Správa systému <ph id="ph1">\&gt;</ph> Nastavení <ph id="ph2">\&gt;</ph> Konfigurace licence<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Then, on the <bpt id="p1">**</bpt>Configuration keys<ept id="p1">**</ept> tab, expand <bpt id="p2">**</bpt>Trade <ph id="ph1">\&gt;</ph> Warehouse and Transportation management<ept id="p2">**</ept>, and select the check box for <bpt id="p3">**</bpt>Catch weight for warehouse<ept id="p3">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Poté na kartě <bpt id="p1">**</bpt>Konfigurační klíče<ept id="p1">**</ept> kartu rozbalte <bpt id="p2">**</bpt>Obchod <ph id="ph1">\&gt;</ph> Řízení skladu a správy přepravy<ept id="p2">**</ept> a zaškrtněte políčko u možnosti <bpt id="p3">**</bpt>Skutečná hmotnost pro sklad<ept id="p3">**</ept>).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Both the <bpt id="p1">**</bpt>Warehouse and Transportation management<ept id="p1">**</ept> license configuration key and the <bpt id="p2">**</bpt>Process distribution <ph id="ph1">\&gt;</ph> Catch weight<ept id="p2">**</ept> license configuration keys must also be turned on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Musí být zapnuty licenční konfigurační klíče pro možnosti <bpt id="p1">**</bpt>Řízení skladu a správy přepravy<ept id="p1">**</ept> i <bpt id="p2">**</bpt>Zpracování distribuce <ph id="ph1">\&gt;</ph> Skutečná hmotnost<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>After the license configuration key is turned on, when you create a released product, you can select <bpt id="p1">**</bpt>Catch weight<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Po zapnutí licenčního konfiguračního klíče můžete při vytvoření uvolněného produktu zvolit <bpt id="p1">**</bpt>Skutečná hmotnost<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You can also associate the released product with a storage dimension group that the <bpt id="p1">**</bpt>Use warehouse management processes<ept id="p1">**</ept> parameter is selected for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Můžete také přidružit uvolněný produkt ke skupině dimenze úložiště, pro kterou je zvolen parametr <bpt id="p1">**</bpt>Použít procesy řízení skladu<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Before you can use the product in Warehouse management, you must do some basic product-specific setup for catch weight:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Než budete moci produkt použít v řízení skladu, musíte provést několik základních nastavení pro konkrétní produkt týkajících se skutečné hmotnosti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Define the nominal weight conversion between the catch weight unit (box) and the inventory unit (kilogram <ph id="ph1">\[</ph>kg<ph id="ph2">\]</ph>) as part of a unit conversion definition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Definujte převod nominální hmotnosti mezi jednotkou skutečné hmotnosti (pole) a jednotkou zásob (kilogram <ph id="ph1">\[</ph>kg<ph id="ph2">\]</ph>) jako součást definice převodu jednotek.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Define the minimum and maximum weight tolerances as part of the catch weight unit setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Definujte tolerance minimální a maximální hmotnosti v rámci nastavení jednotky skutečné hmotnosti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Set up a unit sequence group where the catch weight unit is defined as the lowest stock keeping unit (SKU).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nastavte skupinu klasifikace jednotek, kde je jednotka skutečné hmotnosti definována jako nejnižší skladová jednotka zásob (SKU).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Set up a catch weight item handling policy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nastavte zásadu zpracování položky se skutečnou hmotností.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For more information, see <bpt id="p1">[</bpt>Setting up and maintaining catch weight items<ept id="p1">](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Další informace naleznete v tématu <bpt id="p1">[</bpt>Nastavení a správa položek se skutečnou hmotností<ept id="p1">](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Transaction adjustments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Úpravy transakce</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Because the weight of inventory when it comes into a warehouse can differ from the weight when the inventory is issued out of the warehouse, the catch weight product processing must adjust the inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vzhledem k tomu, že hmotnost zásob, když se dostanou do skladu, se může lišit od hmotnosti, když jsou zásoby vydány ze skladu, musí zpracování produktu se skutečnou hmotností upravit zásoby.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>Example 1<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Příklad 1<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>During a <bpt id="p1">**</bpt>Report as finished<ept id="p1">**</ept> production process, the inbound weight of a license plate that contains eight boxes of a catch weight product is captured as 80.1 kg.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Během výrobního procesu <bpt id="p1">**</bpt>Ohlásit jako dokončené<ept id="p1">**</ept> je zaznamenaná vstupní hmotnost registrační značky obsahující osm krabic produktu se skutečnou hmotností jako 80,1 kg.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The license plate is then stored away in the finished goods area, and during the storage period, some weight is lost into the air.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Registrační značka pak odložení uložena v oblasti hotových výrobků a během doby skladování některé hmotnost dojde ke ztrátě do ovzduší.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Later, as part of a sales order picking process, the weight of the same license plate is captured as 79.8 kg.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Později, jako součást procesu výdeje prodejní objednávky, je váha stejné poznávací značky zaznamenána jako 79,8 kg.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Therefore, in the system, you now have a weight difference as part of the physical dimension set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Proto v systému nyní máte hmotnostní rozdíl jako součást sady fyzické dimenze.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>In this case, the system automatically adjusts the difference by posting a transaction for the missing 0.3 kg.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V takovém případě systém automaticky upraví rozdíl zaúčtováním transakce pro chybějící 0,3 kg.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Example 2<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Příklad 2<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>In its definition, a product is set up to tolerate a minimum weight of 8 kg and a maximum weight of 12 kg for the <bpt id="p1">**</bpt>Box<ept id="p1">**</ept> catch weight unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ve své definici je produkt nastaven tak, aby toleroval minimální hmotnost 8 kg a maximální hmotnost 12 kg pro jednotku skutečné hmotnosti <bpt id="p1">**</bpt>Krabice<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>You have two boxes of the product, and they have a registered weight of 16 kg.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Máte dvě krabice produktu a jejich registrovaná hmotnost je 16 kg.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>If a warehouse worker picks and weighs one of the boxes, and the weight is captured as 9 kg, the remaining box will weigh 7 kg.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud pracovník skladu vybere a zváží jednu z krabic a váha je zaznamenána jako 9 kg, zbývající krabice bude vážit 7 kg.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>However, because 7 kg is below the minimum weight, the system does an automatic adjustment to increase the weight of the on-hand inventory by 1 kg.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Protože 7 kg je však nižší než minimální hmotnost, systém provede automatickou úpravu k navýšení hmotnosti na skladě o 1 kg.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>To set up the accounts that these adjustments are posted to, go to <bpt id="p1">**</bpt>Cost management <ph id="ph1">\&gt;</ph> Ledger integration policies setup <ph id="ph2">\&gt;</ph> Posting<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Chcete-li nastavit účty, do kterých jsou zaúčtovány tyto úpravy, přejděte na <bpt id="p1">**</bpt>Správa nákladů <ph id="ph1">\&gt;</ph> Nastavení zásad integrace hlavní knihy <ph id="ph2">\&gt;</ph> Zaúčtování<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Then, on the <bpt id="p1">**</bpt>Inventory<ept id="p1">**</ept> tab, define the following accounts:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Poté na kartě <bpt id="p1">**</bpt>Zásoby<ept id="p1">**</ept> definujte následující účty:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Catch weight loss account</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Účet ztrát – skutečná hmotnost</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Catch weight profit account</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Účet zisků – skutečná hmotnost</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Catch weight item handling policy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zásada zpracování položky se skutečnou hmotností</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The catch weight item handling policy defines two primary warehouse management flows for the items: when the weight of the items is captured, and how it's captured.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zásada zpracování položky se skutečnou hmotností definuje dva primární toky správy skladu pro položky: kdy je hmotnost zboží zaznamenána a jakým způsobem je zaznamenána.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>You can define when the weight is captured for sales and transfer order processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Můžete určit, kdy je hmotnost zaznamenána pro zpracování prodejní objednávky a převodního příkazu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The weight can be captured during either of the following processes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hmotnost lze zaznamenat během jednoho ze dvou následujících procesů:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Picking<ept id="p1">**</ept> – The weight is captured during the initial pick work lines of order work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Výdej<ept id="p1">**</ept> – Hmotnost je zaznamenaná během řádků práce počátečního vyskladnění práce objednávky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">**</bpt>Packing<ept id="p1">**</ept> – The weight is captured during manual packing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Balení<ept id="p1">**</ept> – Hmotnost je zaznamenaná během ručního balení.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>(You must send the items to a packing station.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(Je nutné odeslat položky do stanice balení.)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>If the actual weight is captured at the packing station during the container packing processes, warehouse workers won't be prompted to capture the weight during picking work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud je během procesů balení kontejneru zaznamenána skutečná hmotnost na balicí stanici, pracovníci skladu nebudou vyzváni k záznamu hmotnost během práce výdeje.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Instead, the average weight of the physical inventory will be used as the weight of the picked inventory that goes to the packing area.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Namísto toho bude průměrná hmotnost fyzických zásob použita jako hmotnost vyskladněných zásob, které jdou do oblasti balení.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>For internal warehouse management processes like counting and adjustment corrections it is possible to define if the weight should be captured or not.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro interní procesy správy skladu, jako je inventura a opravy, je možné určit, zda by měla být zaznamenána hmotnost či nikoli.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>If not captured the nominal weight will be used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud není zaznamenána, bude použita nominální hmotnost.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>You can also define how the weight is captured.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Můžete také definovat, jakým způsobem je hmotnost zaznamenána.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>In one of the two main flows, catch weight tags are tracked and used to capture the weight.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V jednom ze dvou hlavní toků jsou štítky skutečné hmotnosti sledovány a používány k záznamu hmotnosti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>In the other flow, catch weight tags aren't tracked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V druhém toku nejsou štítky skutečné hmotnosti sledovány.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> – The item uses catch weight tags.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ano<ept id="p1">**</ept> – Položka používá štítky skutečné hmotnosti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Each tag number represents one catch weight unit (box), and a weight and other information are associated with the tag.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Číslo každého štítku představuje jednu jednotku skutečné hmotnosti (krabice) a ke štítku je přidružena hmotnost a jiné informace</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>For outbound processes, the weight that is associated with the tag is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro odchozí procesy se použije hmotnost přidružená ke štítku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">**</bpt>No<ept id="p1">**</ept> – The item doesn't use catch weight tags.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ne<ept id="p1">**</ept> – Položka nepoužívá štítky skutečné hmotnosti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The inbound and outbound weighing processes are based on the actual weight that is captured during each process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Příchozí a odchozí procesy vážení jsou založeny na skutečné hmotnosti zaznamenané během každého procesu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>The process of tracking catch weight tags can be used for items that won't change weight during the storage period.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Proces sledování štítků skutečné hmotnosti lze použít pro položky, které nezmění hmotnost během doby skladování.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>The weight will be captured only during the inbound warehouse process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hmotnost bude zaznamenána pouze v průběhu vstupního procesu skladu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>During the outbound process, the catch weight tags will just be scanned, and the weights that are associated with the tags will be used for the outbound transactional processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V průběhu odchozího procesu budou štítky skutečné hmotnosti pouze naskenovány, a hmotnosti, které jsou přidruženy ke štítkům se použijí pro zpracování odchozí transakce.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>How to capture catch weight</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jak zaznamenat skutečnou hmotnost</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>When catch weight tag tracking is used, a tag must always be created for every catch weigh unit that is received, and every tag must always be associated with a weight.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Když se používá sledování štítku skutečné hmotnosti, musí být štítek vždy vytvořen pro každou jednotku skutečné hmotnosti, která je přijata, a každý štítek musí být vždy přiřazen k hmotnosti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>For example, <bpt id="p1">**</bpt>Box<ept id="p1">**</ept> is the catch weight unit, and you receive one pallet of eight boxes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Například <bpt id="p1">**</bpt>Krabice<ept id="p1">**</ept> je jednotka skutečné hmotnosti a přijmete jednu paletu s osmi krabicemi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>In this case, eight unique catch weight tags must be created, and a weight must be associated with each tag.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V takovém případě se musí vytvořit osm jedinečných štítků skutečné hmotnosti a hmotnost musí být přiřazena ke každému štítku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Depending on the inbound catch weight tag, either the weight of all eight boxes can be captured, and the average weight can then be distributed to each box, or a unique weight can be captured for each box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V závislosti na štítku příchozí skutečné hmotnosti lze zaznamenat buď hmotnost všech osmi krabic a průměrná hmotnosti pak může být rozdělena na každou krabici, nebo lze zaznamenat jedinečnou hmotnost pro každou krabici.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>When catch weight tag tracking isn't used, the weight can be captured for each dimension set (for example, for each license plate and tracking dimension).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Když se nepoužívá sledování štítků skutečné hmotnosti, lze zaznamenat hmotnost pro každou sadu dimenzí, (například pro každou poznávací značku a sledovací dimenzi).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Alternatively, the weight can be captured based on an aggregated level, such as five license plates (pallets).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Případně lze zaznamenat hmotnost podle agregované úrovně, například pět poznávacích značek (palet).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>For the methods for capturing outbound weight, you can define whether the weighing is done for each catch weight unit (that is, per box), or whether the weight is captured based on the quantity that will be picked (for example, three boxes).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro metody zaznamenání výstupní hmotnosti lze definovat, zda se vážení provádí pro každou jednotku skutečné hmotnosti (to znamená pro krabici), nebo zda je zachycena hmotnost na základě množství, které bude vyskladněno (například tři krabice).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Note that for the production line picking and internal movement processes, the average weight will be used if the <bpt id="p1">**</bpt>Not captured<ept id="p1">**</ept> option is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Všimněte si, že pro proces výdeje řádku výroby a interních procesů pohybu se použije průměrná hmotnost, pokud není použita možnost <bpt id="p1">**</bpt>Nezaznamenáno<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>To restrict the warehouse management picking processes from capturing weights resulting in catch weight profit/loss adjustments, the Outbound weight variance method can be used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud chcete omezit proces výběru procesů při zaznamenání hmotností, jehož výsledkem jsou úpravy skutečné hmotnosti/ztrát, lze použít metodu odchylky od původní hmotnosti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Supported scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Podporované scénáře</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Not all workflows support catch weight product processing with warehouse management.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ne všechna workflow podporují zpracování produktu se skutečnou hmotností pomocí řízení skladu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>The following restrictions currently apply.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aktuálně platí následující omezení.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Configuring catch weight products for warehouse management processes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konfigurace produktů se skutečnou hmotností pro procesy řízení skladu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For catch weight products, the storage dimension group for items can't be changed (so that warehouse management processes can be used for them).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro produkty se skutečnou hmotností nelze u položek změnit skupinu dimenze úložiště (tak, aby pro ně bylo možné použít procesy správy skladu).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Only formula processing is supported for catch weight products (not bill of materials).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pouze zpracování receptury je podporováno pro produkty se skutečnou hmotností (nikoliv kusovníky).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Catch weight products can't be associated with a tracking dimension group by using the Owner dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Produkty se skutečnou hmotností nelze přiřadit ke skupině sledovací dimenze pomocí dimenze vlastníka.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Catch weight products can't be used as services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Produkty se skutečnou hmotností nelze použít jako služby.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Catch weight products can be used as "stocked products" only as part the item model group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Produkty se skutečnou hmotností lze použít jako produkty na skladě pouze jako součást skupiny modelu položky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Catch weight products can't be used together with the functionality for tracking "Active in sales process."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Produkty se skutečnou hmotností nelze použít společně s funkcí ke sledování „Aktivní v prodejním procesu.“</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Catch weight products can't be used together with the functionality for capturing serial numbers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Produkty se skutečnou hmotností nelze použít společně s funkcí pro záznam sériových čísel.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Therefore, products can't be transferred from a "blank" to a serial number as part of the picking/packing process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Proto produkty nemohou být převedeny z prázdných na sériové číslo jako součást procesu výdeje/balení.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Catch weight products can't be used together with the functionality for registering serials before consumption.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Produkty se skutečnou hmotností nelze použít společně s funkcí pro registraci sériových čísel před spotřebou</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Catch weight products that are variant-enabled can't be used together with the functionality for converting variant units of measure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Produkty se skutečnou hmotností, které mají povolenou variantu, nelze použít společně s funkcí pro převod měrných jednotek variant.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Catch weight products can't be marked as a retail "product kit."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Produkty se skutečnou hmotností nelze označit jako maloobchodní sadu produktů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Catch weight products can be used only with a unit sequence group that has catch weight handling units, and that has the catch weight unit as the lowest sequence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Produkty se skutečnou hmotností lze použít pouze se skupinou klasifikace jednotky, která má manipulační jednotky skutečné hmotnosti a která má jednotku skutečné hmotnosti jako nejnižší sekvenci.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>For catch weight products, the inventory unit can be converted to the catch weight unit only if the conversion produces a nominal quantity that is more than 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">U produktů se skutečnou hmotností lze převést skladovou jednotku na jednotku skutečné hmotnosti pouze tehdy, pokud převod vyprodukuje nominální množství větší než 1.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>The setup of bar codes for catch weight products doesn't support a variable weight setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nastavení čárových kódů pro produkty se skutečnou hmotností nepodporuje nastavení proměnné hmotnosti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Order processing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zpracování objednávky</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>The creation of advance ship notice (ASN/packing structures) doesn't support weight information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vytvoření avíza expedice zboží expedice (ASN/struktury balení) nepodporuje informace o hmotnosti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>The order quantity must be maintained based on the catch weight unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Objednané množství musí být spravované na základě jednotky skutečné hmotnosti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Inbound warehouse processing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Příchozí zpracování skladu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Receiving license plates requires that weights be assigned during registration, because weight information isn't supported as part of the advance ship notice.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Přijetí poznávacích značek vyžaduje, aby byly hmotnosti přiřazeny při registraci, vzhledem k tomu, že informace o hmotnosti není podporována jako součást avíza expedice zboží.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>When catch weight tag processes are used, the tag number must be manually assigned per catch weight unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Když se používají procesy štítku skutečné hmotnost, musí být číslo štítku ručně přiřazen o podle jednotky skutečné hmotnosti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Inventory and warehouse operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Operace skladů a zásob</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Manual creation of quarantine orders isn't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ruční vytváření karanténních příkazů není podporováno pro produkty se skutečnou hmotností.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Manual movement of inventory that is related to work isn't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ruční přesun zásob související s prací není podporováno pro produkty se skutečnou hmotností.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Consolidation of license plates isn't supported for catch weight products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Konsolidace poznávacích značek není podporováno pro produkty se skutečnou hmotností.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>License plate loading to initialize warehouse stock isn't supported for catch weight products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Načtení poznávací značky pro inicializaci naskladnění skladu není podporováno pro produkty se skutečnou hmotností.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Batch balancing processes aren't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Procesy vyvážení dávky nejsou podporovány pro produkty se skutečnou hmotností.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Handling of negative physical inventory isn't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zpracování negativních fyzických zásob není podporováno pro produkty se skutečnou hmotností.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Inventory marking can't be used for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Označení zásob nelze použít pro produkty se skutečnou hmotností.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Outbound warehouse processing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Odchozí zpracování skladu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>The functionality for cluster picking isn't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Funkce pro výdej v seskupení není podporována pro produkty se skutečnou hmotností.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Pick and pack warehouse processing isn't supported for catch weight products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Zpracování výdeje a balení skladu není podporováno pro produkty se skutečnou hmotností.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>For catch weight products, work that is defined in a work template can be run automatically.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">U produktů se skutečnou hmotností lze práci definovanou v šabloně práce spustit automaticky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>The functionality for reversing work isn't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Funkce pro stornování práce není podporována pro produkty se skutečnou hmotností.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>For catch weight products, manual packing station processing where work is created after containers are closed isn't supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">U produktů se skutečnou hmotnosti není podporováno ruční zpracování stanice balení, kde je práce vytvořena po uzavření kontejnerů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The functionality for pcs-by-pcs scanning isn't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Funkce pro skenování kus po kusu není podporována pro produkty se skutečnou hmotností.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Production processing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zpracování výroby</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>For catch weight products, only batch orders for formula products are supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">U produktů se skutečnou hmotností jsou podporovány pouze dávkové objednávky pro produkty receptury.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Kanban functionality isn't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Funkce kanbanu není podporována pro produkty se skutečnou hmotností.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>For catch weight products, serial numbers can't be registered before consumption.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">U produktů se skutečnou hmotností nelze registrovat sériová čísla před spotřebou.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>The functionality for reversing license plates isn't supported for catch weight products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Funkce pro stornování poznávacích značek není podporována pro produkty se skutečnou hmotností.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>For catch weight products, reporting as finished cannot be registered by serial number.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match">U produktů se skutečnou hmotností nelze vykazování jako dokončené registrovat podle sériového čísla.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Transportation management processing</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Zpracování správy přepravy</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Load building workbench processing isn't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pracovní plocha sestavení vytížení není podporována pro produkty se skutečnou hmotností.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Transport request lines aren't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Řádky požadavků na přepravu nejsou podporovány pro produkty se skutečnou hmotností.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Other restrictions and behaviors for catch weight product processing with warehouse management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Další omezení a chování pro zpracování produktů se skutečnou hmotností se správou skladu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>During picking processes where the user isn't prompted to identify tracking dimensions, the weight assignment is done based on the average weight.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Během procesů výdeje, kde není uživatel vyzván k identifikaci sledovacích dimenzí, se provádí přiřazení hmotnosti na základě průměrné hmotnosti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>This behavior occurs when, for example, a combination of tracking dimensions is used in the same location and, after a user processes picking, only one tracking dimension value is left in the location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">K tomuto chování dochází například v případě, že je ve stejném umístění použita kombinace sledovacích dimenzí a poté, co uživatel zpracuje výdej, zůstane v umístění pouze jedna hodnota sledovací dimenze.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>When inventory is reserved for a catch weight product that is configured for warehouse management processes, the reservation is done based on the minimum weight that is defined, even if this quantity is the on-hand last handling quantity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud jsou zásoby rezervovány pro produkt se skutečnou hmotností, který je konfigurován pro procesy správy skladu, rezervace se provádí na základě definované minimální hmotnosti, a to i v případě, že je toto množství naposledy zpracovávané množství zásob na skladě.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>This behavior differs from the behavior for items that aren't configured for warehouse management processes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toto chování se liší od chování pro položky, které nejsou nakonfigurovány pro procesy správy skladu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Processes that use the weight as part of capacity calculations (wave thresholds, work maximum breaks, container maximums, location load capacities, and so on) don't use the actual weight of the inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Procesy, které používají hmotnost jako součást výpočtů kapacity (prahové hodnoty vln, maximální pracovní přestávky, maxima kontejnerů, kapacit vytížení místa atd.) nepoužívají skutečnou hmotnost zásob.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Instead, the processes are based on the physical handling weight that is defined for the product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Místo toho jsou procesy založeny na fyzické hmotnosti zpracování definované pro produkt.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>In general, Retail functionality isn't supported for catch weight products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Obecně není funkce Retail podporována pro produkty se skutečnou hmotností.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Catch weight tags</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Štítky skutečné hmotnosti</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Currently, the functionality for catch weight tags is supported only as part of the following scenarios:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V současné době je funkce štítků skutečné hmotnosti podporována pouze jako součást následujících scénářů:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>When processing purchase order warehouse app receiving.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Při zpracování příjmu aplikace skladu nákupní objednávky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>When processing load receiving via warehouse app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Při zpracování příjmu vytížení prostřednictvím aplikace skladu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>For license plate receiving that is related to a purchase order load, weight assignment is requested during the receiving process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro příjem poznávací značky, který se vztahuje k nákladu nákupní objednávky, se požaduje přiřazení hmotnosti během procesu příjmu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>By contrast, for transfer order receiving, the weight from the shipment data for the transfer order is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Naopak pro příjem převodního příkazu se používá pro převodní příkaz hmotnost z data expedice.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>For transfer order item and line receiving that comes from a non-warehouse management process warehouse.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro položku převodního příkazu a příjem řádku, který pochází z procesu správy skladu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The processing of sales return order receiving can record catch weight tags, but the processing won't be validated if the tags are the same tags that were originally shipped for a particular sales order line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zpracování příjmu objednávky prodejní vratky může zaznamenávat štítky skutečné hmotnosti, ale zpracování nebude ověřeno, pokud jsou štítky stejné štítky, které byly původně dodány pro konkrétní řádek prodejní objednávky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>When processing a inventory status changed by using the warehouse app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Když se zpracování stavu zásob změnilo pomocí aplikace skladu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>When a warehouse transfer is done by using the warehouse app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Když je převod skladu proveden pomocí aplikace skladu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>When processing adjustment in and out via the warehouse app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Při zpracování příchozích a odchozích úprav prostřednictvím aplikace skladu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>When picking work is processed for sales and transfer orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Když je práce výdeje zpracovávána pro prodejní objednávky a převodní příkazy.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>(Note that catch weight tags can't be recorded for production component picking.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(Mějte na paměti, že štítky skutečné hmotnosti nelze zaznamenat pro výdej výrobních komponent.)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>When picked quantities are reduced from load lines, regardless of whether containers are used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Když je vyskladněné množství sníženo z řádků vytížení, bez ohledu na to, zda se používají kontejnery.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>When products are packed into containers at a packing station.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Když jsou produkty zabaleny do kontejnerů ve stanici balení.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>When containers are reopened.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Když jsou kontejnery znovu otevřeny.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>When formula products are reported as finished by using the warehouse app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Když jsou produkty receptury vykazovány jako dokončené pomocí aplikace skladu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>When transport loads are processed by using the warehouse app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Při zpracování nákladů přepravy s použitím aplikace skladu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>A catch weight tag can either be created using a warehousing app process, manually created in the form, or creating using a data entity process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Značku skutečné hmotnosti lze vytvořit pomocí procesu skladové aplikace, ručně ve formuláři nebo pomocí procesu datové entity.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>If a catch weight tag gets associated with an inbound source document line, such as purchase order line, the tag will be registered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud se značka skutečné hmotnosti přidruží k příchozí řádce zdrojového dokumentu, jako je řádka nákupní objednávky, značka bude zaregistrována.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>If the line is used for outbound processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Je-li řádek použit pro odchozí zpracování.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>The tag will be updated as shipped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Značka bude aktualizována jako expedovaná.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>