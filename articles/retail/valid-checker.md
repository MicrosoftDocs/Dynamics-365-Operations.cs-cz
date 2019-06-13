<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="valid-checker.md" target-language="cs-CZ">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>valid-checker.125a66.1fc894206f9d90fce1e2eab292ac241e9d943e23.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>1fc894206f9d90fce1e2eab292ac241e9d943e23</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>aec1dcd44274e9b8d0770836598fde5533b7b569</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/03/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\valid-checker.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Retail transaction consistency checker</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kontrola konzistence maloobchodních transakcí</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the retail transaction consistency checker functionality in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toto téma popisuje funkci kontroly konzistence maloobchodních transakcí v aplikaci Microsoft Dynamics 365 for Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Retail transaction consistency checker</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kontrola konzistence maloobchodních transakcí</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toto téma popisuje funkci kontroly konzistence maloobchodních transakcí uvedenou v aplikaci Microsoft Dynamics 365 for Finance and Operations, verze 8.1.3.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Kontrola konzistence identifikuje a izoluje nekonzistentní transakce před tím, než se dostanou k procesu zaúčtování výkazů.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When a statement is posted in Microsoft Dynamics 365 for Retail, posting can fail due to inconsistent data in the retail transaction tables.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">Při zaúčtování výkazu v aplikaci Microsoft Dynamics 365 for Retail může zaúčtování selhat kvůli nekonzistentním datům v tabulkách maloobchodních transakcí.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The data issue may be caused by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">Problém s daty může být způsoben nepředvídanými potížemi v aplikaci Point of Sale (POS), nebo tím, že transakce byly nesprávně naimportovány z POS systémů třetích stran.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Examples of how these inconsistencies may appear include:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Příklady toho, jak mohou tyto nekonzistence vypadat, zahrnují:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The transaction total on the header table does not match the transaction total on the lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Celková částka transakce v tabulce záhlaví neodpovídá celkové částce transakce na řádcích.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The line count on the header table does not match with the number of lines in the transaction table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Počet řádků v tabulce záhlaví neodpovídá počtu řádků v tabulce transakcí.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Taxes on the header table do not match the tax amount on the lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Daně v tabulce záhlaví neodpovídají celkové částce daně na řádcích.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Když jsou nekonzistentní transakce přejaty procesem zaúčtování výkazů, vytvoří se nekonzistentní prodejní faktury a deníky plateb, následkem čehož celý proces zaúčtování výkazu selže.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Obnovení výkazů z takového stavu představuje složité opravy dat napříč mnoha tabulkami transakcí.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The retail transaction consistency checker prevents such issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Kontrola konzistence maloobchodních transakcí těmto problémům zabraňuje.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The following chart illustrates the posting process with the transaction consistency checker.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Následujíc tabulka znázorňuje proces zaúčtování s kontrolou konzistence transakcí.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">![</bpt>Statement posting process with retail transaction consistency checker<ept id="p1">]</ept><bpt id="p2">(./media/validchecker.png "</bpt>Statement posting process with retail transaction consistency checker<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>Proces zaúčtování výkazu s kontrolou konzistence transakcí<ept id="p1">]</ept><bpt id="p2">(./media/validchecker.png "</bpt>Proces zaúčtování výkazu s kontrolou konzistence transakcí<ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The <bpt id="p1">**</bpt>Validate store transactions<ept id="p1">**</ept> batch process checks the consistency of the retail transaction tables for the following scenarios.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Dávkové zpracování <bpt id="p1">**</bpt>Ověřit transakce obchodu<ept id="p1">**</ept> kontroluje konzistenci tabulek maloobchodních transakcí pro následující scénáře:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Customer account<ept id="p1">**</ept> – Validates that the customer account in the retail transaction tables exists in the HQ customer master.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Účet odběratele<ept id="p1">**</ept> - Ověřuje, že účet odběratele existuje v tabulce maloobchodních transakcí v HQ hlavních datech odběratele.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>Line count<ept id="p1">**</ept> – Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Počet řádků<ept id="p1">**</ept> - Ověřuje, že počet řádků, jak je zaznamenaný v tabulce záhlaví transakcí, odpovídá počtu řádků v tabulce prodejních transakcí.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Price includes tax<ept id="p1">**</ept> – Validates that the <bpt id="p2">**</bpt>Price includes tax<ept id="p2">**</ept> parameter is consistent across transaction lines.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Cena zahrnuje daň<ept id="p1">**</ept> – Ověřuje, zda je parametr <bpt id="p2">**</bpt>Cena zahrnuje daň<ept id="p2">**</ept> konzistentní napříč řádky transakce.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">**</bpt>Gross amount<ept id="p1">**</ept> – Validates that the gross amount on the header is the sum of the net amounts on the lines plus the tax amount.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Hrubá částka<ept id="p1">**</ept> – Ověřuje, že je hrubá částka v záhlaví součtem čistých částek na řádcích a částky daně.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>Net amount<ept id="p1">**</ept> – Validates that the net amount on the header is the sum of the net amounts on the lines.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Čistá částka<ept id="p1">**</ept> – Ověřuje, že je čistá částka v záhlaví součtem čistých částek na řádcích.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>Under / Over payment<ept id="p1">**</ept> – Validates that the difference between the gross amount on the header and the payment amount doesn't exceed the maximum underpayment/overpayment configuration.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Nedoplatek/přeplatek<ept id="p1">**</ept> – Ověřuje, že rozdíl mezi hrubou částkou v záhlaví a částkou platby nepřekračuje konfiguraci maximálního nedoplatku/přeplatku.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Discount amount<ept id="p1">**</ept> – Validates that the discount amount on the discount tables and the discount amount on the retail transaction line tables are consistent, and that the discount amount on the header is the sum of the discount amounts on the lines.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Částka slevy<ept id="p1">**</ept> – Ověřuje, že částka slevy v tabulkách slev a částka slevy v tabulkách řádků maloobchodních transakcí jsou konzistentní a že částka slevy v záhlaví je součtem částek slev na řádcích.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Line discount<ept id="p1">**</ept> – Validates that the line discount on the transaction line is the sum of all the lines in the discount table that corresponds to the transaction line.</source><target logoport:matchpercent="56" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Řádková sleva<ept id="p1">**</ept> - Ověřuje, že řádková sleva na řádku transakce je součtem všech řádků v tabulce slev, která odpovídá řádku transakce.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Gift card item<ept id="p1">**</ept> – Retail doesn't support the return of gift card items.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Položka dárkového poukazu<ept id="p1">**</ept> – Retail nepodporuje vrácení položek dárkového poukazu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>However, the balance on a gift card can be cashed out. Any gift card item that is processed as a return line instead of a cash-out line fails the statement posting process.</source><target logoport:matchpercent="0" state="translated">Nicméně zůstatek na dárkovém poukazu lze vyplatit v hotovosti. U jakékoliv položky dárkového poukazu, která je zpracována jako řádek vrácení namísto řádku vyplacení v hotovosti, se proces zaúčtování výkazů nezdaří.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The validation process for gift card items helps guarantee that the only return gift card line items on the retail transaction tables are gift card cash-out lines.</source><target logoport:matchpercent="0" state="translated">Proces ověřování pro položky dárkového poukazu pomáhá zaručit, že jediné položky řádku vrácení dárkového poukazu v tabulce maloobchodních transakcí jsou řádky vyplacení dárkového poukazu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>Negative price<ept id="p1">**</ept> – Validates that there are no negative price transaction lines.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Záporná cena<ept id="p1">**</ept> – Ověřuje, že neexistují žádné řádky transakce s negativní cenou.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Item &amp; Variant<ept id="p1">**</ept> – Validates that items and variants on the transaction lines exist in the item and variant master file.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Položka a varianta<ept id="p1">**</ept> – Ověřuje, že položky a varianty na řádcích transakce existují v hlavním souboru položek a variant.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Set up the consistency checker</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Nastavení kontroly konzistence</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Configure the "Validate store transactions" batch process, at <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Retail IT <ph id="ph2">\&gt;</ph> POS posting<ept id="p1">**</ept>, for periodic runs.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Nakonfigurujte dávkové zpracování „Ověřit transakce obchodu“ pro periodická spuštění pomocí možností <bpt id="p1">**</bpt>Maloobchod <ph id="ph1">\&gt;</ph> IT pro maloobchod <ph id="ph2">\&gt;</ph> Zaúčtování POS<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dávkovou úlohu lze naplánovat na základě hierarchie organizace obchodu, podobným způsobem, jakým se nastavují zpracování „Vypočítat příkazy v dávkách“ a „Zaúčtovat příkazy v dávkách“.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Doporučujeme, abyste nakonfigurovali toto dávkové zpracování tak, aby se spouštělo několikrát denně, a naplánovali jeho spuštění na konec každého provedení úlohy P.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Results of validation process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Výsledky procesu ověření</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The results of the validation check by the batch process are tagged on the appropriate retail transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Výsledky procesu ověření podle dávkového zpracování jsou označeny na příslušné maloobchodní transakci.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The <bpt id="p1">**</bpt>Validation status<ept id="p1">**</ept> field on the retail transaction record is either set to <bpt id="p2">**</bpt>Successful<ept id="p2">**</ept> or <bpt id="p3">**</bpt>Error<ept id="p3">**</ept>, and the date of the last validation run appears on the <bpt id="p4">**</bpt>Last validation time<ept id="p4">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pole <bpt id="p1">**</bpt>Stav ověření<ept id="p1">**</ept> na záznamu maloobchodní transakce je buď nastaveno na <bpt id="p2">**</bpt>Úspěšný<ept id="p2">**</ept> nebo <bpt id="p3">**</bpt>Chyba<ept id="p3">**</ept> a datum posledního spuštění ověření se zobrazí v poli <bpt id="p4">**</bpt>Poslední čas ověření<ept id="p4">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the <bpt id="p1">**</bpt>Validation errors<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Chcete-li zobrazit popisnější text chyby související se selháním ověření, zvolte příslušný záznam maloobchodní transakce a klikněte na tlačítko <bpt id="p1">**</bpt>Chyby ověřování<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Transakce, u kterých se nezdaří kontrola ověření, a transakce, které ještě nebyly ověřeny, nebudou publikovány do výkazů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Během procesu „Vypočítat výkaz“ budou uživatelé upozorněni, pokud existují transakce, které mohly být zahrnuty ve výkazu, ale nebyly.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>If a validation error is found, the only way to fix the error is to contact Microsoft Support.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud je nalezena chyba ověření, jediným způsobem její opravy je kontaktování podpory Microsoft Support.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In a future release, capability will be added so that users can fix the records that failed through the user interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V dalších verzích bude přidána funkce, aby mohli uživatelé opravit nepodařené záznamy prostřednictvím uživatelského rozhraní.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Logging and auditing capabilities will also be made available to trace the history of the modifications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Rovněž budou zpřístupněny funkce protokolování a auditu pro sledování historie úprav.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Additional validation rules to support more scenarios will be added in a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V budoucích verzích bude přidáno více pravidel ověření pro podporu více scénářů.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>