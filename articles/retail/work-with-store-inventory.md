<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="work-with-store-inventory.md" target-language="cs-CZ">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>work-with-store-inventory.418f90.551a8408aa730bc1916f1c57b7cfd773966ce8bf.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>551a8408aa730bc1916f1c57b7cfd773966ce8bf</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\work-with-store-inventory.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Store inventory management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Správa skladových zásob</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the types of documents that you can use to manage inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toto téma popisuje typy dokumentů, které můžete použít ke správě zásob.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Store inventory management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Správa skladových zásob</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>When working with inventory in Dynamics 365 for Retail and using the POS application, it is important to note that POS provides limited support for inventory dimensions and certain inventory item types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Při práci se zásobami v aplikaci Dynamics 365 for Retail a používání aplikace Retail POS je důležité poznamenat, že POS poskytuje omezenou podporu pro dimenze zásob a určité typy skladových položek.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The POS solution does not support the following item configurations:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Řešení POS nepodporuje následující konfigurace položek:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>BOM items (except kit products, which utilize some components of the BOM framework)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Položky kusovníku (s výjimkou sady produktů, které používají některé součásti sady systému kusovníků)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Catch weight items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Položka se skutečnou hmotností</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Batch-controlled items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Položky řízené dávkou</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The POS application currently does not support the following tracking dimensions in the POS:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aplikace Retail POS v současné době nepodporuje následující sledovací dimenze v POS:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Batch tracking dimension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dimenze dávkového sledování</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Owner dimension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dimenze vlastníka</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The POS solution provides limited support for the following dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Řešení POS poskytuje omezenou podporu následujících dimenzí.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Limited support indicates that the POS may default some of these dimensions into inventory transactions automatically based on warehouse/store setup configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Omezená podpora označuje, že POS může nastavit některé z těchto dimenzí jako výchozí do skladových transakcí automaticky založených na konfiguraci nastavení skladu/úložiště.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>POS will not fully support the dimensions in the way they are supported if a sales transaction is manually entered into the ERP.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">POS nebude plně podporovat dimenze způsobem, kterým jsou podporovány v případě ručního zadání prodejní transakce do ERP.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">**</bpt>Warehouse Location<ept id="p1">**</ept> – Users will not have the ability to manage the receiving warehouse location for items received into a store warehouse when the store has not been configured to use the warehouse management process.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Skladové místo<ept id="p1">**</ept> – Uživatelé nebudou mít možnost spravovat přijímací skladové místo pro položky přijaté do skladu obchodu, pokud nebylo pro obchod nakonfigurováno použití procesu řízení skladu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>A default receiving location defined on the store warehouse will be used for these items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro tyto položky bude použito výchozí přijímací skladové místo definované ve skladu obchodu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>If the warehouse management process has been enabled for the store, limited support that prompts the user to choose a receiving location for the entire receipt will be triggered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud byl pro obchod povolen proces řízení skladu, bude spuštěna omezená podpora, která vyzve uživatele k výběru přijímacího místa pro celou příjemku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Items sold from the store will always be sold out of the default retail location as defined on the store warehouse setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Položky prodávané z obchodu budou vždy vyprodány z výchozího maloobchodního umístění, jak je definováno v nastavení skladu obchodu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The location for managing return inventory can be controlled through default return location definition on the store warehouse or based on return reason codes as defined in the return location policy.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Místo pro správu zásob vrácení lze ovládat pomocí výchozí definice skladového místa pro vrácení ve skladu obchodu nebo na základě kódů důvodu vrácení, které jsou definovány v zásadě umístění pro vrácení.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>License plate<ept id="p1">**</ept> – License plates are only applicable when <bpt id="p2">**</bpt>Use warehouse management process<ept id="p2">**</ept> has been enabled on the item and the store warehouse.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Registrační značka<ept id="p1">**</ept> - Registrační značky platí pouze v případě, když byla povolena možnost <bpt id="p2">**</bpt>Použít procesy řízení skladu<ept id="p2">**</ept> pro danou položku a sklad obchodu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>In POS, if inventory is received into a store warehouse where the warehouse management process has been enabled, and the location chosen to receive the item into is tied to a location profile that requires license plate control, the POS application will systematically apply a license plate to the receiving line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud jsou v POS přijaty zásoby do skladu obchodu, kde byl povolen proces řízení skladu, a skladové místo vybrané pro přijetí položky je navázáno na profil umístění, který vyžaduje řízení registrační značky, aplikace POS systematicky použije registrační značku na řádek příjmu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Users in POS will not have the ability to change or manage this license plate data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Uživatelé v POS nebudou mít možnost měnit ani spravovat data této registrační značky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>If full management of license plates is required, it is suggested the store use the WMS mobile application or the back office ERP client to manage the receipt of these items.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Je-li vyžadována úplná správa registračních značek, navrhuje se, aby obchod použil mobilní aplikaci WMS nebo klienta ERP účetního systému ke správě příjmu těchto položek.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Serial number<ept id="p1">**</ept> – The POS application has limited support for single serial number to be registered on a transaction sales line for orders created in POS with serialized items.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Sériové číslo<ept id="p1">**</ept> – Aplikace POS má omezenou podporu pro jednotlivá sériová čísla, která mají být registrována na řádku prodejní transakce pro objednávky vytvořené v POS se serializovanými položkami.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>This serial number is not validated against registered serial numbers already in inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toto sériové číslo není ověřováno proti registrovaným sériovým číslům, která jsou již v zásobách.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>If a sales order is created in the call center channel or fulfilled through the ERP and multiple serial numbers are registered to a single sales line during the fulfillment process in the ERP, these serial numbers will not be able to be applied or validated if a return is processed in POS for these orders.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Je-li prodejní objednávka vytvořena v kanálu kontaktního střediska nebo splněna prostřednictvím ERP a více sériových čísel je registrováno k jednomu řádku prodeje v průběhu procesu plnění v ERP, tato sériová čísla nebude možné použít nebo ověřit, pokud je pro tyto objednávky vrácení zpracováváno v POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">**</bpt>Inventory status<ept id="p1">**</ept> – For items that use the warehouse management process and require an inventory status, this status field is not able to be set or modified through the POS application.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Stav zásob<ept id="p1">**</ept> - Pro položky, které používají proces řízení skladu a vyžadují stav zásob, nelze toto pole stavu v aplikaci POS nastavit nebo změnit.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The default inventory status as defined on the store warehouse configuration will be used when items are received into inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Výchozí stav zásob definovaný v konfiguraci skladu obchodu bude použit při příjmu položek do zásob.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>All organizations must test item configurations through POS in development or test environments before deploying them to production.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Všechny organizace musí otestovat konfigurace položky prostřednictvím POS při vývoji nebo v testovacím prostředí před nasazením do výroby.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Test your items by performing regular cash and carry sales transacting and creating customer orders (if applicable) through the POS with your items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Položky otestujte provedením pravidelných hotovostních prodejních transakcí a vytvořením zákaznických objednávek (v příslušných případech) pomocí POS s položkami.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Testing must include running a full statement posting processes in your test environment and verifying that there are no issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Testování musí zahrnovat spuštění úplných procesů zaúčtování výkazů v testovacím prostředí a ověření, že nedochází k potížím.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Configuring items in a way that is not supported by the POS application, without proper testing, can result in your statement posting process failing in production without an easy way to correct the issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konfigurace položek způsobem, který aplikace POS nepodporuje, bez řádného testování, může způsobit neúspěch procesu zaúčtování ve výrobě bez jednoduchého způsobu opravy problémů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Partner or customer customizations to the application may optionally be considered to allow these posting processes to successfully complete.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Přizpůsobení aplikace partnerem nebo zákazníkem může být volitelně považováno za umožnění úspěšného dokončení těchto procesů zaúčtování.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>If customizations are not needed, the organization must ensure that the product configuration of your products has been done in a way that is supported by the standard POS application/order creation/statement posting process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud nejsou potřeba přizpůsobení, musí organizace zajistit, že konfigurace produktu byla provedena způsobem, který podporují standardní procesy aplikace POS/vytvoření objednávky/zaúčtování výkazu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Purchase orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nákupní objednávky</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Purchase orders are created at the head office.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nákupní objednávky se vytvářejí v ústředí.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail through the <bpt id="p1">**</bpt>Picking/Receiving<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud je maloobchodní sklad zahrnut v záhlaví nákupní objednávky, objednávku lze přijmout v obchodě pomocí řešení Modern POS (MPOS) nebo Cloud POS v aplikaci Microsoft Dynamics 365 for Retail pomocí operace <bpt id="p1">**</bpt>Výdej/Příjem<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>After the quantities that are received at the store are entered in the <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> field in POS for the purchase order document, they can be saved locally or committed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Po zadání množství přijatých v obchodě do pole <bpt id="p1">**</bpt>Přijmout nyní<ept id="p1">**</ept> v POS pro dokument nákupní objednávky mohou být tyto údaje uloženy místně nebo potvrzeny.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Saving this data locally has no effect on in-stock inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Uložení těchto dat lokálně nemá žádný dopad na zásoby na skladě.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Saving should be done only if the user is not ready to post the receipt to HQ and just needs a way to temporarily store the previously entered <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ukládání by mělo být provedeno pouze v případě, že uživatel není připraven zaúčtovat příjemku do HQ a pouze potřebuje způsob, jak dočasně uložit dříve zadaná <bpt id="p1">**</bpt>Přijmout nyní<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>This saves the receive now data locally to the user's channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tím se uloží data z přijetí místně do databáze kanálů uživatele.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>After the document is processed using the <bpt id="p1">**</bpt>Commit<ept id="p1">**</ept> option, the <bpt id="p2">**</bpt>Receive Now<ept id="p2">**</ept> data is sent to HQ and the purchase order receipt will be posted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Po zpracování dokumentu s použitím možnosti <bpt id="p1">**</bpt>Potvrdit<ept id="p1">**</ept> budou data <bpt id="p2">**</bpt>Přijmout nyní<ept id="p2">**</ept> odeslána do HQ a bude zaúčtována příjemka nákupní objednávky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Transfer orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Převodní příkazy</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>A transfer order can specify that a particular store is the location that items can be shipped from or the location the inventory will be received into.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Převodní příkaz může specifikovat, že konkrétní obchod je umístěním, ze kterého lze expedovat položky nebo do kterého budou zásoby přijaty.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If the POS user is the shipping warehouse for a transfer order, they will be able to enter <bpt id="p1">**</bpt>Ship Now<ept id="p1">**</ept> quantities from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud je uživatel POS expedičním skladem pro převodní příkaz, bude moci zadat množství <bpt id="p1">**</bpt>Expedovat nyní<ept id="p1">**</ept> z POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The data entered by the shipping store can be saved locally or committed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Data zadaná expedičním obchodem lze uložit místně nebo je potvrdit.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>When saved locally, no updates are made to the transfer order document in HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Při místním uložení nejsou provedeny žádné aktualizace dokumentu převodního příkazu v HQ.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Saving should be done only if the user is not ready to post the shipment to HQ and needs a way to temporarily store the previously entered <bpt id="p1">**</bpt>Ship Now<ept id="p1">**</ept> data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ukládání by mělo být provedeno pouze v případě, že uživatel není připraven zaúčtovat dodávku do HQ a potřebuje způsob, jak dočasně uložit dříve zadaná <bpt id="p1">**</bpt>Expedovat nyní<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>After the store is ready to confirm shipment, the <bpt id="p1">**</bpt>Commit<ept id="p1">**</ept> option should be selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jakmile bude obchod připraven k potvrzení dodávky, je třeba vybrat možnost <bpt id="p1">**</bpt>Potvrdit<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>This posts the shipment of the transfer order in HQ so that the receiving warehouse will now be able to receive against it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tato možnost zaúčtuje dodávku převodního příkazu v HQ, takže přijímací sklad bude nyní schopen proti ní přijímat.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>If the POS user is the receiving warehouse for a transfer order, they will be able to enter the <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> quantities from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud je uživatel POS přijímacím skladem pro převodní příkaz, bude moci zadat množství <bpt id="p1">**</bpt>Přijmout nyní<ept id="p1">**</ept> z POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The data entered by the receiving store can be saved locally or committed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Data zadaná přijímajícím obchodem lze uložit místně nebo je potvrdit.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Saving should be done only if the user is not ready to post the receipt to HQ and needs a way to temporarily store the previously entered <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ukládání by mělo být provedeno pouze v případě, že uživatel není připraven zaúčtovat příjemku do HQ a potřebuje způsob, jak dočasně uložit dříve zadaná <bpt id="p1">**</bpt>Přijmout nyní<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>This saves the receive now data locally to the user's channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tím se uloží data z přijetí místně do databáze kanálů uživatele.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>After the document is processed using the <bpt id="p1">**</bpt>Commit<ept id="p1">**</ept> option, the <bpt id="p2">**</bpt>Receive Now<ept id="p2">**</ept> data is sent to HQ and the transfer order receipt will be posted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Po zpracování dokumentu s použitím možnosti <bpt id="p1">**</bpt>Potvrdit<ept id="p1">**</ept> budou data <bpt id="p2">**</bpt>Přijmout nyní<ept id="p2">**</ept> odeslána do HQ a bude zaúčtována příjemka převodního příkazu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>It's important to note that the receiving store will be restricted to only being able to commit receive quantities that are equal to or less than shipped quantities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Je důležité si uvědomit, že přijímající obchod bude omezen pouze na schopnost potvrdit množství příjmu, která jsou rovna nebo menší než dodaná množství.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>An attempt to receive quantities on a transfer order that have not previously shipped will result in errors and the receipt will not be confirmed in HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokus o přijetí množství na převodních příkazech, která nebyla dříve expedována, bude mít za následek chyby a příjemka nebude potvrzena v HQ.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Stock counts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Počty na skladě</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Stock counts can be either scheduled or unscheduled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Inventury mohou být plánované nebo neplánované.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Plánované inventury zahajuje ústředí, které také určuje, které položky musí být spočítány.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ústředí vytvoří dokument inventury skladu, který lze přijmout v obchodě, kde jsou množství skutečných zásob na skladě zadána v MPOS nebo Cloud POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Neplánované maloobchodní inventury jsou zahájeny v obchodě a množství skutečných zásob na skladě jsou aktualizována v MPOS nebo Cloud POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Na rozdíl od plánovaných maloobchodních inventur nemají neplánované maloobchodní inventury předdefinovaný seznam položek.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>When a stock count of either type is completed, it is committed and sent to the head office.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Po dokončení obou typů inventury budou potvrzeny a odeslány do ústředí.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>At the head office, the count is validated and posted as a separate step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V ústředí bude inventura ověřena a zaúčtována jako samostatný krok.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Inventory lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vyhledávání zásob</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The current product quantity on hand for multiple stores and warehouses can be viewed on the <bpt id="p1">**</bpt>Inventory lookup<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Na stránce <bpt id="p1">**</bpt>Vyhledávání zásob<ept id="p1">**</ept> lze zobrazit aktuální množství produktu na skladě pro více obchodů a skladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kromě aktuálního množství na skladě je možné zobrazit budoucí množství, které lze slíbit (ATP) pro každý jednotlivý obchod.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>To do so, select the store that you want to view the ATP for and then click <bpt id="p1">**</bpt>Show store availability<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Chcete-li tak učinit, vyberte obchod, pro který chcete zobrazit ATP, a klikněte na <bpt id="p1">**</bpt>Zobrazit dostupnost obchodu<ept id="p1">**</ept>.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>