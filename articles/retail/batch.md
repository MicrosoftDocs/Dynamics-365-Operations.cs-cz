<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="batch.md" target-language="cs-CZ">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>batch.e70006.4456fc3d5bc4547fa8211642b11ca6df455fa187.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4456fc3d5bc4547fa8211642b11ca6df455fa187</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>aec1dcd44274e9b8d0770836598fde5533b7b569</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/03/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\batch.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Improved handling of batch-tracked items</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">Vylepšené zpracování položek sledovaných dávkou</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the improvements that have been made to the handling of batches for batch-tracked items during the Retail statement posting process.</source><target logoport:matchpercent="40" state="translated" state-qualifier="fuzzy-match">Toto téma popisuje vylepšení provedená u zpracování dávek pro položky sledované dávkou během procesu zaúčtování maloobchodního výkazu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Improved handling of batch-tracked items</source>
        <target logoport:matchpercent="98" state="translated" state-qualifier="leveraged-inherited">Vylepšené zpracování položek sledovaných dávkou</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In Microsoft Dynamics 365 for Retail Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</source><target logoport:matchpercent="0" state="translated">V Microsoft Dynamics 365 for Retail Point of Sale (POS) nelze zaznamenat čísla dávek pro položky sledované dávkou v okamžiku prodeje.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</source><target logoport:matchpercent="0" state="translated">Nicméně pro konkrétní konfigurace při zaúčtování prodejů v centrále prostřednictvím objednávek zákazníků nebo zaúčtování výkazů očekává systém Microsoft Dynamics, že platná čísla dávky pro položky sledované dávkou existují a že budou použity během procesu fakturace.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</source><target logoport:matchpercent="0" state="translated">Pokud jsou pro produkty k dispozici platná čísla dávek, použije je proces fakturace objednávky zákazníka a proces fakturace prodejní objednávky ze zaúčtování výkazu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</source><target logoport:matchpercent="30" state="translated" state-qualifier="fuzzy-match">V opačném případě proces fakturace objednávky zákazníka nemůže provést zaúčtování a uživatel POS obdrží chybovou zprávu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Statement posting then goes into an error state.</source><target logoport:matchpercent="0" state="translated">Zaúčtování výkazu se pak dostane do chybového stavu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This error state occurs even when negative inventory has been turned on for the products.</source><target logoport:matchpercent="0" state="translated">K tomuto chybovému stavu dojde tehdy, když byly pro produkty zapnuty záporné zásoby.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Improvements that have been made in Microsoft Dynamics for Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</source><target logoport:matchpercent="0" state="translated">Vylepšení, která byla provedena v aplikaci Microsoft Dynamics for Retail verze 10.0.4 a novějších, pomáhají zaručit, že při zapnutých záporných zásobách pro položky sledované dávkou nebudou pro tyto položky blokovány fakturace objednávek zákazníků a fakturace prodejních objednávek prostřednictvím zaúčtování výkazu, pokud jsou zásoby 0 (nula) nebo není k dispozici číslo dávky.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</source><target logoport:matchpercent="0" state="translated">Nová funkcionalita používá výchozí ID dávky pro prodejní řádky, když nejsou čísla dávek k dispozici.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>To define the default batch ID that is used for customer orders, on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Customer orders<ept id="p2">**</ept> tab, on the <bpt id="p3">**</bpt>Order<ept id="p3">**</ept> FastTab, set the <bpt id="p4">**</bpt>Default batch id<ept id="p4">**</ept> field.</source><target logoport:matchpercent="0" state="translated">Chcete-li definovat výchozí ID dávky, které se používá pro objednávky zákazníka, na stránce <bpt id="p1">**</bpt>Parametry maloobchodu<ept id="p1">**</ept> na kartě <bpt id="p2">**</bpt>Objednávky zákazníka<ept id="p2">**</ept> na záložce s náhledem <bpt id="p3">**</bpt>Objednávka<ept id="p3">**</ept> nastavte pole <bpt id="p4">**</bpt>Výchozí ID dávky<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>To define the default batch ID that is used for sales order invoicing through statement posting, on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Posting<ept id="p2">**</ept> tab, on the <bpt id="p3">**</bpt>Inventory update<ept id="p3">**</ept> FastTab, set the <bpt id="p4">**</bpt>Default batch id<ept id="p4">**</ept> field.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">Chcete-li definovat výchozí ID dávky, které se používá pro fakturaci prodejní objednávky prostřednictvím zaúčtování výkazu, na stránce <bpt id="p1">**</bpt>Parametry maloobchodu<ept id="p1">**</ept> na kartě <bpt id="p2">**</bpt>Zaúčtování<ept id="p2">**</ept> na záložce s náhledem <bpt id="p3">**</bpt>Aktualizace zásob<ept id="p3">**</ept> nastavte pole <bpt id="p4">**</bpt>Výchozí ID dávky<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</source><target logoport:matchpercent="31" state="translated" state-qualifier="fuzzy-match">Tato funkce je k dispozici pouze tehdy, když je zapnuta rozšířená správa skladu pro konkrétní sklad obchodu a položky.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</source><target logoport:matchpercent="0" state="translated">V novější verzi bude tato funkcionalita podporována též pro scénáře, kde se rozšířená správa skladu nepoužívá.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>