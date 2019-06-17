<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="omni-auto-charges.md" target-language="cs-CZ">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>omni-auto-charges.2f6e37.47829a6fcae37e03510929dc46b942455016df0b.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>47829a6fcae37e03510929dc46b942455016df0b</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>ffc37f7c2a63bada3055f37856a30424040bc9a3</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/16/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\omni-auto-charges.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Omni-channel advanced auto charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Omnikanálové rozšířené automatické náklady</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes capabilities for managing additional order charges for Retail channel orders using advanced auto charges features.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toto téma popisuje funkce pro správu dalších nákladů objednávky pro objednávky maloobchodní sítě pomocí funkcí rozšířených automatických nákladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Omni-channel advanced auto charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Omnikanálové rozšířené automatické náklady</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides information on configuration and deployment of the advanced auto-charges feature which are available in Dynamics 365 for Retail version 10.0.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Toto téma obsahuje informace o konfiguraci a nasazení funkce rozšířených automatických nákladů, která je k dispozici v aplikaci Dynamics 365 for Retail verze 10.0.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When the advanced auto-charges features are enabled, orders created in any supported Retail channel (point of sale (POS), call center, and online), can take advantage of the <bpt id="p1">[</bpt>auto-charges<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> configurations defined in the ERP application for both header and line-level related charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud jsou funkce rozšířených automatických nákladů povoleny, objednávky vytvořené v libovolném podporovaném kanálu Retail (pokladní místo (POS), kontaktní středisko a online) mohou využít konfigurací <bpt id="p1">[</bpt>automatických nákladů<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> definovaných v aplikaci ERP pro související náklady záhlaví a úrovně řádku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>In releases prior to Dynamics 365 for Retail version 10.0, <bpt id="p1">[</bpt>auto-charge<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> configurations are only accessible by orders created in e-Commerce and call center channels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ve vydáních před Dynamics 365 for Retail verze 10.0 jsou konfigurace <bpt id="p1">[</bpt>automatických nákladů<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)</ept> přístupné pouze pro objednávky vytvořené v kanálech e-Commerce a kontaktního střediska.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In versions 10.0 and later, POS-created orders can leverage the auto-charges configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ve verzi 10.0 a novějších mohou objednávky vytvořené v POS využít konfigurace automatických nákladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>That way, additional miscellaneous charges can systematically be added to sales transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tímto způsobem další vedlejší náklady mohou být systematicky přidány do prodejních transakcí.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>When using releases prior to version 10.0, a POS user is prompted to manually enter a shipping fee during the creation of a "ship all" or "ship selected" POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Používáte-li verze starší než je verze 10.0, uživatel POS je vyzván k ručnímu zadání dopravného během vytváření transakcí POS „expedovat vše“ nebo „expedovat vybrané“.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>While the miscellaneous charges capabilities of the application are utilized in respect to how the charges are written to the order, no systematic calculation is provided – the calculation relies on the user's input to determine the value of the charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">Zatímco funkce vedlejších nákladů v aplikaci se používají s ohledem na to, jak jsou náklady zapsány do objednávky, není poskytován systematický výpočet - výpočet se opírá o vstup uživatele, který určuje hodnotu nákladů.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The charges can only be added as a single "shipping" related charges code and cannot easily be edited or changed in the POS after they are created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Náklady lze přidat pouze jako jeden kód nákladů souvisejících s expedicí a nelze je snadno upravit ani změnit v POS po jejich vytvoření.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The use of manual prompts to add shipping charges is still available in versions 10.0 and later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Použití ruční výzvy k přidání nákladů na expedici je stále k dispozici ve verzi 10.0 a starších.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>If an organization does not enable the <bpt id="p1">**</bpt>Advanced Auto-charges<ept id="p1">**</ept> parameter, the POS prompts for manual entry of charges will remain the same.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud organizace nepovolí parametr <bpt id="p1">**</bpt>rozšířené automatické náklady<ept id="p1">**</ept>, výzvy POS k ručnímu zadání nákladů zůstanou stejné.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>With the advanced auto-charges feature, POS users can have systematic calculations for any defined miscellaneous charges based on auto-charges setup tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Díky funkci rozšířených automatických nákladů mohou mít uživatelé POS systematické výpočty pro všechny definované vedlejší náklady založené na tabulkách nastavení automatických nákladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In addition, users will have the ability to add or edit an unlimited amount of additional charges and fees to any POS sales transaction at the header or line-level (for a cash and carry or customer order).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Navíc uživatelé budou mít možnost přidávat nebo upravovat neomezené množství dodatečných nákladů a poplatků do jakékoli prodejní transakci POS na záhlaví nebo na úrovni řádku (pro „cash and carry“ nebo objednávku odběratele).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Enabling advanced auto-charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Povolení rozšířených automatických nákladů</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>On the <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Headquarters setup <ph id="ph2">\&gt;</ph> Parameters <ph id="ph3">\&gt;</ph> Retail parameters<ept id="p1">**</ept> page, go to the <bpt id="p2">**</bpt>Customer orders<ept id="p2">**</ept> tab. On the <bpt id="p3">**</bpt>Charges<ept id="p3">**</ept> FastTab, set <bpt id="p4">**</bpt>Use advanced auto-charges<ept id="p4">**</ept> to <bpt id="p5">**</bpt>Yes<ept id="p5">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">Na stránce <bpt id="p1">**</bpt>Maloobchod <ph id="ph1">\&gt;</ph> Nastavení centrály <ph id="ph2">\&gt;</ph> Parametry <ph id="ph3">\&gt;</ph> Parametry maloobchodu<ept id="p1">**</ept> přejděte na kartu <bpt id="p2">**</bpt>Objednávky odběratele<ept id="p2">**</ept>. Na záložce s náhledem <bpt id="p3">**</bpt>Náklady<ept id="p3">**</ept> nastavte možnost <bpt id="p4">**</bpt>Použít rozšířené automatické náklady<ept id="p4">**</ept> na <bpt id="p5">**</bpt>Ano<ept id="p5">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Advanced Auto-Charges Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Parametr rozšířených automatických nákladů</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>When advanced auto-charges are enabled, users are no longer prompted to manually enter a shipping charge at the POS terminal when creating a ship-all or ship-selected customer order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Když jsou povoleny rozšířené automatické náklady, uživatelé nejsou nadále vyzýváni k ručnímu zadání nákladů na terminálu POS při vytváření objednávky odběratele expedovat vše a expedovat vybrané.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>POS order charges are systematically calculated and added to the POS transaction (if a corresponding auto-charges table that matches the criterion of the order being created are found).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Náklady objednávky POS jsou systematicky vypočítávány a přidávány k transakci POS (pokud je nalezena odpovídající tabulka automatických nákladů, která odpovídá kritériu vytvářené objednávky).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Users can also add or maintain header or line-level charges manually through newly added POS operations that can be added to the POS screen layouts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Uživatelé mohou přidávat nebo udržovat náklady záhlaví nebo na úrovni řádku ručně prostřednictvím nově přidaných operací POS, které lze přidat do rozvržení obrazovky POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>When advanced auto-charges are enabled, the existing <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> for <bpt id="p2">**</bpt>Shipping charges code<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Refund shipping charges<ept id="p3">**</ept> are no longer utilized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud jsou povoleny rozšířené automatické náklady, existující <bpt id="p1">**</bpt>Parametry maloobchodu<ept id="p1">**</ept> pro <bpt id="p2">**</bpt>Kód dopravného<ept id="p2">**</ept> a <bpt id="p3">**</bpt>Refundovat dopravné<ept id="p3">**</ept> se již nepoužívají.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>These parameters are only applicable if the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is set to <bpt id="p2">**</bpt>No<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tyto parametry jsou použitelné pouze tehdy, když je parametr <bpt id="p1">**</bpt>Použít rozšířené automatické náklady<ept id="p1">**</ept> nastaven na <bpt id="p2">**</bpt>Ne<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Before you enable this feature, ensure that you have tested and trained your employees, as this will change the business process flow of how shipping or other charges are calculated and added to POS sales orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Než povolíte tuto funkci, ujistěte se, že jste vyzkoušeli a vyškolili své zaměstnance, protože to změní tok obchodních procesů výpočtu dopravného a jiných nákladů a přidání do prodejních objednávek POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Make sure that you understand the impact of the process flow to the creation of transactions from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ujistěte se, že rozumíte dopadu toku procesu na vytváření transakcí z POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>For call center and e-Commerce orders, the impact of enabling advanced auto-charges is minimal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro objednávky kontaktního střediska a e-Commerce je dopad povolení rozšířených automatických nákladů minimální.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Call center and e-Commerce applications will continue to have the same behavior they have had historically related to the auto-charges tables to calculate additional order fees.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aplikace kontaktního střediska a e-Commerce budou mít nadále stejné chování, které měly v minulosti, v souvislosti s tabulkami automatických nákladů pro výpočet dalších nákladů objednávky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Call center channel users will continue to have the ability to manually edit any system calculated auto-charges at the header or line level, or manually add additional miscellaneous charges at the header or line level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Uživatelé kanálu kontaktního střediska budou nadále mít možnost ručně upravit veškeré automatické náklady vypočítané systémem v záhlaví nebo na úrovni řádku, nebo ručně přidat další vedlejší náklady na záhlaví nebo úrovni řádku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Additional POS operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Další operace POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>For advanced auto-charges to work properly in your POS application environment, new POS operations have been added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Aby rozšířené automatické náklady fungovaly správně v prostředí vaší aplikace POS, byly přidány nové operace POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>These operations must be added to your <bpt id="p1">[</bpt>POS screen layouts<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> and deployed to the POS devices as you deploy advanced auto-charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tyto operace musí být přidány do vašeho <bpt id="p1">[</bpt>rozvržení obrazovky POS<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> a nasazeny na zařízení POS při nasazení rozšířených automatických nákladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>If these operations are not added, users will not be able to manage or maintain miscellaneous charges on the POS transactions and will have no way of adjusting or changing the charges values that are systematically calculated based on auto-charges configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud tyto operace nebudou přidány, uživatelé nebudou schopni spravovat nebo udržovat vedlejší náklady na transakcích POS a nebudou mít žádný způsob, jak upravit nebo změnit hodnoty nákladů, které jsou systematicky vypočítávány na základě konfigurace automatických nákladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>At minimum, it is suggested that you deploy the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation to your POS layout.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Minimálně navrhujeme nasadit operaci <bpt id="p1">**</bpt>Spravovat náklady<ept id="p1">**</ept> do vašeho rozvržení POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The new operations are as follows.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Nové operace jsou následující.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source><bpt id="p1">**</bpt>142 - Manage charges<ept id="p1">**</ept> – Use this operation to allow POS users to view and edit miscellaneous charges for the POS transaction that were either added manually or systematically through auto-charges calculations.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>142 – Spravovat náklady<ept id="p1">**</ept> – Tuto operaci použijte k tomu, aby uživatelé POS mohli zobrazit a upravovat vedlejší náklady pro transakci POS, které byly buď přidány ručně nebo systematicky pomocí výpočtů automatických nákladů.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>141 - Add header charges<ept id="p1">**</ept> – Use this operation to give the user the ability to manually add a header-level miscellaneous charge to any POS sales transaction (and select the charges code to be used).</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>141 - Přidat náklady záhlaví<ept id="p1">**</ept> – Tuto operaci použijte k tomu, abyste uživateli umožnili ručně přidat vedlejší náklady na úrovni záhlaví do jakékoliv prodejní transakce POS (a vybrat kód nákladů, který se má použít).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>140 - Add line charges<ept id="p1">**</ept> – Use this operation to give the user the ability to manually add a line level miscellaneous charge to any POS sales transaction line (and select the charges code to be used).</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>140 - Přidat náklady řádku<ept id="p1">**</ept> – Tuto operaci použijte k tomu, abyste uživateli umožnili ručně přidat vedlejší náklady na úrovni řádku do jakéhokoliv řádku prodejní transakce POS (a vybrat kód nákladů, který se má použít).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>143 - Recalculate charges<ept id="p1">**</ept> – Use this operation to perform a full re-calculation of the charges for the sales transaction.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>143 - Přepočítat náklady<ept id="p1">**</ept> – Použijte tuto operaci k provedení úplného přepočítání nákladů pro prodejní transakci.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Any previously user-overwritten auto-charges will be recalculated based on the current cart configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Veškeré dříve uživatelem přepsané automatické náklady budou přepočítány na základě aktuální konfigurace košíku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>As with all POS operations, security configurations can be made to require manager approval in order to execute the operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jako u všech operací POS lze provést konfigurace zabezpečení, aby bylo požadováno schválení manažerem za účelem provedení operace.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>It is important to note that the above listed POS operations can also be added to the POS layout even if the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Je důležité poznamenat, že výše uvedené operace POS lze také přidat k rozvržení POS, i v případě, když je parametr <bpt id="p1">**</bpt>Použít rozšířené automatické náklady<ept id="p1">**</ept> zakázán.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In this scenario, organizations will still get added benefits of being able to view manually added charges and edit them using the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V tomto scénáři budou organizace stále přidávat další výhody v tom, že budou moci zobrazit manuálně přidané náklady a upravovat je pomocí operace <bpt id="p1">**</bpt>Spravovat náklady<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Users may also use the <bpt id="p1">**</bpt>Add header charges<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Add line charges<ept id="p2">**</ept> operations for POS transactions even when <bpt id="p3">**</bpt>Use advanced auto-charges<ept id="p3">**</ept> parameter is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Uživatel může rovněž použít operace <bpt id="p1">**</bpt>Přidat náklady záhlaví<ept id="p1">**</ept> a <bpt id="p2">**</bpt>Přidat náklady řádku<ept id="p2">**</ept> pro POS transakce, i když je parametr <bpt id="p3">**</bpt>Použít rozšířené automatické náklady<ept id="p3">**</ept> zakázán.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>The <bpt id="p1">**</bpt>Recalculate charges<ept id="p1">**</ept> operation has less functionality if used when <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> is disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Operace <bpt id="p1">**</bpt>Přepočítat náklady<ept id="p1">**</ept> má nižší funkci, je-li použita při zákazu možnosti <bpt id="p2">**</bpt>Použít rozšířené automatické náklady<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In this sceanrio, nothing would be recalculated and any charges manually added to the transaction would just reset to $0.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V tomto scénáři by nebylo nic přepočítáno a veškeré náklady ručně přidané do transakce by se pouze resetovaly na 0,00 USD.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Use case examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Použití příkladů případu</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>In this section, sample use cases are presented to help you understand the configuration and usage of auto-charges and miscellaneous charges within the context of Retail channel orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V této části jsou uvedeny ukázkové příklady použití, které vám pomohou porozumět konfiguraci a použití automatických nákladů a vedlejších nákladů v rámci objednávek maloobchodní sítě.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>These examples illustrate the behavior of the application when the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter has been enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tyto příklady ilustrují chování aplikace při povolení parametru <bpt id="p1">**</bpt>Použít automatické rozšířené náklady<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Auto-charges header charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Příklad nákladů záhlaví automatických nákladů</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Příklad použití</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>A retailer wants to automatically add charges for freight when transactions are created in any Retail channel that require a shipment of products to the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Maloobchodní prodejce chce automaticky přidávat náklady za dopravné při vytváření transakcí v jakémkoli maloobchodním kanálu, který vyžaduje dodávku produktů zákazníkovi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The retailer offers 2 methods of delivery: Ground and Air.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prodejce nabízí 2 způsoby dodání: po zemi a letecky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>If a customer chooses Ground delivery and the order value is less than $100, the retailer wants to charge the customer a freight charge of $10.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud zákazník zvolí dodání po zemi a hodnota objednávky je menší než 100 USD, prodejce chce zpoplatnit odběratele za dopravné částkou 10 USD.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>If the order is over $100 in value and the customer chooses ground shipping, the customer will not be charged any additional freight fees.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud je objednávka vyšší než 100 USD a zákazník si zvolí pozemní dopravu, zákazníkovi nebudou účtovány žádné dodatečné poplatky za dopravu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If the customer chooses the Air method of delivery for all orders, regardless of their total value, will be charged a freight fee of $20.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud si zákazník zvolí způsob dodávky letecky pro všechny objednávky, bez ohledu na jejich celkovou hodnotu, bude účtován poplatek za dopravu ve výši 20 USD.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Instalace a konfigurace</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>This scenario requires the configuration of two auto-charges tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tento scénář vyžaduje konfiguraci dvou tabulek s automatickými náklady.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Go to <bpt id="p1">**</bpt>Accounts receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Auto charges<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Přejděte na <bpt id="p1">**</bpt>Pohledávky <ph id="ph1">\&gt;</ph> Nastavení nákladů <ph id="ph2">\&gt;</ph> Automatické náklady<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Configure two different header-level auto charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nakonfigurujte dva druhy různých automatických nákladů na úrovni záhlaví.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Configure one for the "Ground mode" of delivery and one for the "Air mode" of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nakonfigurujte jeden pro doručení po zemi a druhý pro doručení letecky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>For this scenario, configure them to be used for "All customers".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V tomto scénáři je nakonfigurujte tak, aby se používaly pro všechny odběratele.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>For the ground delivery charges, in the lines section of the <bpt id="p1">**</bpt>Auto-charges<ept id="p1">**</ept> page, define a charge that will be applied for orders between $.01 and $100 as $10.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">U nákladů za pozemní doručení definujte v části řádků stránky <bpt id="p1">**</bpt>Automatické náklady<ept id="p1">**</ept> náklad 10 USD, který bude použit pro objednávky mezi 0,01 a 100 USD.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Create another charges line to indicate orders over $100.01 will have no charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vytvořte jiný řádek nákladů pro označení, že objednávky nad 100,01 USD nebudou mít žádné náklady.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Auto charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Příklad automatických nákladů</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>For the air delivery charges, in the lines section of the auto-charges form, define a charge of $20.00 that will be applied to all orders (between a value of $.01 to $9,999,999).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">U nákladů za letecké doručení definujte v části řádků formuláře automatických nákladů náklad 20 USD, který bude použit na všechny objednávky (mezi 0,01 a 9 999 999 USD).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Send the changes to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Odešlete změny do databáze Retail Serveru / kanálu, aby je mohlo POS použít spuštěním úlohy <bpt id="p1">**</bpt>1040 plán distribuce<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Sales processing for this scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zpracování prodeje pro tento scénář</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>After the configuration steps above are complete and the changes have been applied to the channel database, any customer order or sales transaction created in the POS, call center, or e-Commerce channels that have the ground or air delivery methods set at the header level will utilize these charges and automatically apply them to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Po dokončení výše uvedených konfiguračních kroků a použití změn databáze kanálu použije každá objednávka odběratele nebo prodejní transakce vytvořená v kanálech POS, kontaktního střediska nebo e-Commerce se způsobem doručení po zemi nebo letecky nastaveným na úrovní řádku tyto náklady a automaticky je aplikuje na prodej.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>At this time the charges will apply to all sales transactions created within the legal entity that utilize these delivery modes, as there is no functionality to designate that an auto-charge configuration will only apply to a specific selling channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V tuto chvíli se náklady budou vztahovat na všechny prodejní transakce vytvořené v rámci právnické osoby, která používá tyto způsoby doručení, protože neexistuje žádná funkce, která by označovala, že konfigurace automatických nákladů bude platit pouze pro konkrétní prodejní kanál.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For POS and e-Commerce scenarios, because there is no clearly defined "header" on these orders, header-level charges will only apply if all sales lines on the transaction are set to ship with the exact same mode of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Protože není jasně definované záhlaví na těchto objednávkách, náklady na úrovni řádků se pro scénáře POS a e-Commerce použijí pouze tehdy, když všechny řádky prodeje na transakci jsou nastaveny na expedici se stejným způsobem dodání.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>If there are "mixed-modes" of fulfillment on the transactions created by POS or e-Commerce, only line-level auto-charges will be considered and applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jestliže existují smíšené způsoby plnění na transakcích vytvořených pomocí POS nebo e-Commerce, budou zvažovány a použity pouze automatické náklady na úrovni řádku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>In call center scenarios, the user has control over the setting of the delivery mode at the order header, therefore header-level charges will apply for these orders even if some of the sales lines have been configured to use a different mode of delivery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ve scénářích kontaktního střediska má uživatel kontrolu nad nastavením způsobu dodání na záhlaví objednávky. Proto se náklady na úrovni záhlaví použijí pro tyto objednávky i v případě, že některé řádky prodeje byly nakonfigurovány pro použití jiného způsobu dodání.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Header-level charges for call center orders will always be based on the mode of delivery that is defined at the order header level of the sales order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Náklady na úrovni záhlaví pro objednávky kontaktního střediska budou vždy založeny na způsobu dodání, který je definován na úrovni záhlaví prodejní objednávky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Auto-charges line charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Příklad nákladů řádku automatických nákladů</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Příklad použití</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>A retailer wants to add an additional charge to the customer for setup fees when the customer purchases a particular model of computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Maloobchodní prodejce chce přidat další náklady odběrateli za instalační poplatky v případě, kdy odběratel zakoupí určitý model počítače.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>This computer requires additional non-optional setup actions that the retailer will perform for the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tento počítač vyžaduje další nevolitelné instalační akce, které je prodejce provede pro odběratele.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The retailer has informed customers that there will be an additional fee for this setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prodejce informoval odběratele, že za tuto instalaci bude účtovat další poplatek.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The retailer prefers to manage the charges related to this fee separately from the product sales price for financial reporting purposes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Maloobchodní prodejce preferuje správu nákladů spojených s tímto poplatkem odděleně od prodejní ceny produktu pro účely finančního výkaznictví.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>A setup fee of $19.99 will be charged to the customer when this specific computer is purchased in any retail channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Instalační poplatek 19,99 USD bude odběrateli účtován při koupi tohoto konkrétní počítače v libovolné maloobchodní síti.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Instalace a konfigurace</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This scenario requires the configuration of one line-level auto charges table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tento scénář vyžaduje konfiguraci jedné tabulky s automatickými náklady na úrovni řádku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Go to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Auto charges<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Přejděte na <bpt id="p1">**</bpt>Pohledávky <ph id="ph1">\&gt;</ph> Nastavení nákladů <ph id="ph2">\&gt;</ph> Automatické náklady<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Set the <bpt id="p1">**</bpt>Level<ept id="p1">**</ept> drop-down menu to <bpt id="p2">**</bpt>Line<ept id="p2">**</ept>, and create a new auto-charges record for all customers and for the specific product or product group where the setup fees will be charged.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Nastavte rozevírací nabídku <bpt id="p1">**</bpt>Úroveň<ept id="p1">**</ept> na <bpt id="p2">**</bpt>Řádek<ept id="p2">**</ept> a vytvořte nový záznam automatických nákladů pro všechny odběratele a pro konkrétní produkt nebo skupinu produktů, u kterých bud účtován instalační poplatek.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Auto charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Příklad automatických nákladů</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Odešlete náklady do databáze Retail Serveru / kanálu, aby je mohlo POS použít spuštěním úlohy <bpt id="p1">**</bpt>1040 plán distribuce<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Sales processing for this scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zpracování prodeje pro tento scénář</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>After the configurations steps above are complete and the changes have been applied to the channel database, any customer order or sales transaction created in the POS, call center, or e-Commerce channels that have this item on the order will trigger a line-level charge to be systematically added to the order total.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Po dokončení výše uvedených konfiguračních kroků a použití změn databáze kanálu spustí každá objednávka odběratele nebo prodejní transakce vytvořená v kanálech POS, kontaktního střediska nebo e-Commerce s touto položkou na objednávce náklady na úrovni řádku, které budou systematicky přidány k celkové objednávce.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>At this time the charges will apply to any sales line that matches the configuration of the line-level auto charges within the legal entity, as there is no functionality to configure a line-level auto-charge to apply only to a specific selling channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">V tuto chvíli se náklady budou vztahovat na všechny řádky prodeje, které se shodují s konfigurací automatických nákladů na úrovni řádku v rámci právnické osoby, protože neexistuje žádná funkce pro konfiguraci automatických nákladů, která platí pouze pro konkrétní prodejní kanál.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Manual header charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Příklad ručních nákladů záhlaví</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Use case scenario description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Popis příkladu použití</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>A retailer is making an exception to typical processes by offering to provide a special home delivery of products to a customers who order products in the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Maloobchodní prodejce uděluje výjimku z typických procesů tím, že nabízí speciální dodávku produktů domů zákazníkům, kteří objednávají produkty v obchodě.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The retailer and the customer have agreed that the customer will pay an additional $25 handling fee for this service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prodejce a zákazník se dohodli, že zákazník za tuto službu zaplatí další manipulační poplatek ve výši 25 USD.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The order-taker needs to add this additional fee to the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Osoba přebírající objednávku musí přidat tento dodatečný poplatek k transakci.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Because the fee is a blanket fee and not related to any single product on the order, a header charge will be utilized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Vzhledem k tomu, že poplatek je paušální a nesouvisí s žádným konkrétním produktem na objednávce, bude použit náklad záhlaví.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Instalace a konfigurace</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Ensure the charges code that will be used in this scenario has been properly configured by going to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Charges<ept id="p1">**</ept> to define an appropriate charges code for the scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ujistěte se, že kód nákladů, který bude použit v tomto scénáři, byl správně nakonfigurovaný přechodem na <bpt id="p1">**</bpt>Pohledávky <ph id="ph1">\&gt;</ph> Nastavení nákladů <ph id="ph2">\&gt;</ph> Náklady<ept id="p1">**</ept> pro definování příslušného kódu nákladů pro tento scénář.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Příklad nákladů</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>If the charge should be considered a "shipping" related charge for the purpose of shipping related discounts or promotions, set <bpt id="p1">**</bpt>Shipping charge<ept id="p1">**</ept> on the charges code to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited">Pokud by poplatek měl být považován za náklad související s přepravou pro účel slevy nebo propagace související s přepravou, nastavte <bpt id="p1">**</bpt>Dopravné<ept id="p1">**</ept> na kódu nákladů na <bpt id="p2">**</bpt>Ano<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>If this charge is also allowed to be systematically refunded during the processing of a return transaction in the POS application, set <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud je rovněž možné tento poplatek systematicky refundovat během procesu transakce vrácení v aplikaci POS, nastavte <bpt id="p1">**</bpt>Vratný<ept id="p1">**</ept> na <bpt id="p2">**</bpt>Ano<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>The <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag is only applicable when the <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> parameter is set to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Příznak <bpt id="p1">**</bpt>Vratný<ept id="p1">**</ept> lze použít pouze tehdy, když je parametr <bpt id="p2">**</bpt>Použít rozšířené automatickyé náklady<ept id="p2">**</ept> nastaven na hodnotu <bpt id="p3">**</bpt>Ano<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Odešlete náklady do databáze Retail Serveru / kanálu, aby je mohlo POS použít spuštěním úlohy <bpt id="p1">**</bpt>1040 plán distribuce<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>The <bpt id="p1">**</bpt>Add header charge<ept id="p1">**</ept> operation must be configured in your <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a button that is accessible to the user from POS can call this operation (operation 141).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Operace <bpt id="p1">**</bpt>Přidat náklady záhlaví<ept id="p1">**</ept> musí být nakonfigurována ve vašem <bpt id="p2">[</bpt>rozvržení obrazovky POS<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> tak, aby tlačítko, které je dostupné pro uživatele z POS, mohlo volat tuto operaci (operaci 141).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The screen layout changes must be distributed to the retail channel as well through the distribution schedule function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Změny rozvržení obrazovky musí být distribuovány na maloobchodní síť, stejně jako prostřednictvím funkce plánu distribuce.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Sales processing of manual header charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zpracování prodeje ručních nákladů záhlaví</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>To execute the scenario in the POS application, the POS user will create the sales transaction as usual, adding the products and any other configurations to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro provedení scénáře v aplikaci POS uživatel POS vytvoří obvyklou prodejní transakci a do prodeje přidá produkty a další konfigurace.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Prior to collecting payment, the user should execute the <bpt id="p1">**</bpt>Add header charge<ept id="p1">**</ept> operation, which will prompt the user to select a charges code and enter the charges value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Před inkasováním platby by měl uživatel provést operaci platbu <bpt id="p1">**</bpt>Přidat náklady záhlaví<ept id="p1">**</ept>, která vyzve uživatele k výběru kódu nákladů a zadání hodnoty nákladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Once the user completes the process, the charge will be added to the sales order as a header-level charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jakmile uživatel dokončí proces, náklad bude přidán do prodejní objednávky jako náklad na úrovni záhlaví.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>This process can be applied in the call center by using the existing <bpt id="p1">**</bpt>Charges<ept id="p1">**</ept> feature found on the <bpt id="p2">**</bpt>Sell<ept id="p2">**</ept> tab on the toolbar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tento proces lze použít v kontaktním středisku pomocí stávající funkce <bpt id="p1">**</bpt>Náklady<ept id="p1">**</ept>, která se nalézá na kartě <bpt id="p2">**</bpt>Prodej<ept id="p2">**</ept> na panelu nástrojů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>On the <bpt id="p1">**</bpt>Maintain charges<ept id="p1">**</ept> page, the user can add a new charges line to the order header.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Na stránce <bpt id="p1">**</bpt>Spravovat náklady<ept id="p1">**</ept> může uživatel přidat nový řádek nákladů do záhlaví objednávky.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Manual line charges example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Příklad ručních řádků záhlaví</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Use case scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Příklad použití</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>A customer has requested that 2 of the 5 items on their sales order be gift-wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Odběratel požádal, aby 2 z 5 položek na jeho prodejní objednávce byly dárkově zabaleny.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>The retailer offers this optional service for a fee of $2.00 per item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Prodejce poskytuje tuto volitelnou službu za poplatek 2 USD za položku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The order-taker will need to add these fees to the specific items that need to be gift-wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Osoba přebírající objednávku bude muset přidat tyto poplatky ke konkrétním položkám, které mají být dárkově zabaleny.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Setup and configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Instalace a konfigurace</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Ensure the charges code that will be used in this scenario has been properly configured by going to <bpt id="p1">**</bpt>Accounts Receivable <ph id="ph1">\&gt;</ph> Charges setup <ph id="ph2">\&gt;</ph> Charges<ept id="p1">**</ept> to define an appropriate charges code for the scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ujistěte se, že kód nákladů, který bude použit v tomto scénáři, byl správně nakonfigurovaný přechodem na <bpt id="p1">**</bpt>Pohledávky <ph id="ph1">\&gt;</ph> Nastavení nákladů <ph id="ph2">\&gt;</ph> Náklady<ept id="p1">**</ept> pro definování příslušného kódu nákladů pro tento scénář.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>If the charge should be considered a "shipping" related charge for the purpose of shipping related discounts or promotions, set the <bpt id="p1">**</bpt>Shipping charge<ept id="p1">**</ept> on the charges code to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud by poplatek měl být považován za náklad související s přepravou pro účel slevy nebo propagace související s přepravou, nastavte <bpt id="p1">**</bpt>Dopravné<ept id="p1">**</ept> na kódu nákladů na <bpt id="p2">**</bpt>Ano<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>If the charge is also allowed to be systematically refunded during the processing of a return transaction in the POS application, set <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud je rovněž možné tento poplatek systematicky refundovat během procesu transakce vrácení v aplikaci POS, nastavte <bpt id="p1">**</bpt>Vratný<ept id="p1">**</ept> na <bpt id="p2">**</bpt>Ano<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>The <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag is only applicable when the <bpt id="p2">**</bpt>Use advanced auto-charges<ept id="p2">**</ept> parameter is set to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Příznak <bpt id="p1">**</bpt>Vratný<ept id="p1">**</ept> lze použít pouze tehdy, když je parametr <bpt id="p2">**</bpt>Použít rozšířené automatickyé náklady<ept id="p2">**</ept> nastaven na hodnotu <bpt id="p3">**</bpt>Ano<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Send the charges to the Retail Server/Channel DB so that the POS can utilize them by running the <bpt id="p1">**</bpt>1040 distribution schedule<ept id="p1">**</ept> job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Odešlete náklady do databáze Retail Serveru / kanálu, aby je mohlo POS použít spuštěním úlohy <bpt id="p1">**</bpt>1040 plán distribuce<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>The <bpt id="p1">**</bpt>Add line charge<ept id="p1">**</ept> operation must be configured in your <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a button that is accessible to the user from POS can call this operation (operation 140).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Operace <bpt id="p1">**</bpt>Přidat náklady řádku<ept id="p1">**</ept> musí být nakonfigurována ve vašem <bpt id="p2">[</bpt>rozvržení obrazovky POS<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> tak, aby tlačítko, které je dostupné pro uživatele z POS, mohlo volat tuto operaci (operaci 140).</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>The screen layout changes must be distributed to the retail channel as well through the distribution schedule function.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Změny rozvržení obrazovky musí být distribuovány na maloobchodní síť, stejně jako prostřednictvím funkce plánu distribuce.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Sales processing of the manual line charge</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zpracování prodeje ručních nákladů řádku</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>To execute the scenario in the POS application, the POS user will create the sales transaction as usual, adding the products and any other configurations to the sale.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pro provedení scénáře v aplikaci POS uživatel POS vytvoří obvyklou prodejní transakci a do prodeje přidá produkty a další konfigurace.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Prior to collecting payment, the user should select the specific line where the charge will apply from the POS item list display and execute the <bpt id="p1">**</bpt>Add line charge<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Před inkasováním platby by měl uživatel vybrat konkrétní řádek, kde se použijí náklady ze zobrazení seznamu položek POS, a provést operaci <bpt id="p1">**</bpt>Přidat náklady<ept id="p1">**</ept> řádku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>The user will be prompted to select a charges code and enter the charges value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Uživatel bude vyzván ke zvolení kódu nákladů a zadání hodnoty nákladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Once the user completes the process, the charge will be linked to the line and added to the order total as a line level charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jakmile uživatel dokončí proces, náklad bude propojen na řádek a přidán k součtu objednávky jako náklad na úrovni řádku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The user can repeat the process to add additional line charges to other items lines on the transaction if needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Uživatel může opakovat proces pro přidání dalších nákladů řádku k dalším řádkům položek na transakci v případě potřeby.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The same process can be applied in the call center by using the "maintain charges" feature found under the <bpt id="p1">**</bpt>Financials<ept id="p1">**</ept> drop-down menu in the <bpt id="p2">**</bpt>Sales order lines<ept id="p2">**</ept> section on the <bpt id="p3">**</bpt>Sales order<ept id="p3">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Stejný proces lze použít v kontaktním středisku pomocí funkce Udržovat náklady, která se nalézá pod rozevírací nabídkou <bpt id="p1">**</bpt>Finance<ept id="p1">**</ept> v části <bpt id="p2">**</bpt>Řádky prodejní objednávky<ept id="p2">**</ept> na stránce <bpt id="p3">**</bpt>Prodejní objednávka<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>This will open the <bpt id="p1">**</bpt>Maintain charges<ept id="p1">**</ept> page where the user can add a new line specific charge to the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Tím se otevře stránka <bpt id="p1">**</bpt>Udržovat náklady<ept id="p1">**</ept>, kde může uživatel přidat nový náklad specifický pro řádek k transakci.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Additional features</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Další funkce</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Editing charges on a POS sales transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Úprava nákladů na prodejní transakci POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>The <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> operation (142) should be added to the <bpt id="p2">[</bpt>POS screen layout<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> so that a user can view and edit or override any system-calculated or manually-created header or line-level charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Operace <bpt id="p1">**</bpt>Správa nákladů<ept id="p1">**</ept> (142) by měla být přidána do <bpt id="p2">[</bpt>rozvržení obrazovky POS<ept id="p2">](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts)</ept> tak, aby uživatel mohl zobrazit a upravit nebo přepsat jakékoli systémem vypočítané nebo ručně vytvořené náklady na úrovni řádku nebo záhlaví.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>If the operation is not added, users will not be able to adjust the value of the charges on the POS transaction, nor will they be able to view the details of the charges such as the type of charges code tied to the charge.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Není-li operace přidána, uživatelé nebudou moci upravit hodnotu nákladů na transakci POS, ani nebudou schopni zobrazit podrobnosti o nákladech, jako je typ kódu nákladů navázaný na náklad.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>On the <bpt id="p1">**</bpt>Manage charges<ept id="p1">**</ept> page in POS, the user can view both header and line-level charges details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Na stránce <bpt id="p1">**</bpt>Spravovat náklady<ept id="p1">**</ept> v POS může uživatel zobrazit podrobnosti nákladů na úrovni záhlaví a řádku.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The user can use the <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> function available on this page to make changes to the amount charged to a specific charges line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Uživatel může použít funkci <bpt id="p1">**</bpt>Upravit<ept id="p1">**</ept> dostupnou na této stránce pro provedení změn částky účtované na konkrétní řádek nákladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Once a charges line is overwritten manually, it will not be systematically recalculated unless the user initiates the <bpt id="p1">**</bpt>Recalculate charges<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Jakmile je řádek nákladů ručně přepisován, nebude systematicky přepočítáván, pokud uživatel neinicializuje operaci <bpt id="p1">**</bpt>Přepočítat náklady<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>If the <bpt id="p1">**</bpt>Charge override reason code<ept id="p1">**</ept> has been configured on the <bpt id="p2">**</bpt>Retail parameters<ept id="p2">**</ept> setup page, the user will be prompted to provide a reason code when charges have been modified in the POS application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud byl <bpt id="p1">**</bpt>Kód důvodu přepsání nákladů<ept id="p1">**</ept> nakonfigurován na stránce nastavení <bpt id="p2">**</bpt>Parametry maloobchodu<ept id="p2">**</ept>, uživatel bude vyzván k zadání kódu důvodu, když byly upraveny náklady v aplikaci POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>If reason codes have been captured for overwritten charges, a new report is also available to review and audit these overrides.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud byly kódy důvodů zaznamenány pro přepsané náklady, přepsán, bude k dispozic též nová sestava pro kontrolu a audit těchto přepsání.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>The report can be found in <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Inquiries and reports <ph id="ph2">\&gt;</ph> Charge override history<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sestava se nalézá v možnostech <bpt id="p1">**</bpt>Maloobchod <ph id="ph1">\&gt;</ph> Dotazy a sestavy <ph id="ph2">\&gt;</ph> Historie přepsání nákladů<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Refunding charges on a POS return transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Refundace nákladů na transakci vrácení POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>If the <bpt id="p1">**</bpt>Use advanced auto-charges<ept id="p1">**</ept> parameter is set to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>, the existing retail parameter for <bpt id="p3">**</bpt>Refund shipping charges<ept id="p3">**</ept> is no longer applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud je parametr <bpt id="p1">**</bpt>Použít rozšířené automatické náklady<ept id="p1">**</ept> nastaven na hodnotu <bpt id="p2">**</bpt>Ano<ept id="p2">**</ept>, existující parametr pro možnost <bpt id="p3">**</bpt>Refundovat dopravné<ept id="p3">**</ept> již není k dispozici.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>To indicate which charges should be systematically refunded to a customer when using advanced auto-charges, ensure the related charges code has been configured as <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> setup page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Chcete-li uvést, které poplatky by měly být zákazníkovi systematicky refundovány při použití rozšířených automatických nákladů, zkontrolujte, zda je příslušný kód nákladů nakonfigurován <bpt id="p1">**</bpt>Vratný<ept id="p1">**</ept> na stránce nastavení <bpt id="p2">**</bpt>Kód nákladů<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Make sure that the settings have been synchronized to your Retail channel databases through distribution schedule processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Ujistěte se, že nastavení byla synchronizována do databází maloobchodní sítě prostřednictvím zpracování plánu distribuce.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Refunding charges on a return order transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Refundace nákladů na transakci vratky</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Charges are not systematically refunded to <bpt id="p1">**</bpt>Return orders<ept id="p1">**</ept> created in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Náklady nejsou systematicky refundovány do <bpt id="p1">**</bpt>vratek<ept id="p1">**</ept> vytvořených v aplikaci Retail.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Users are required to select the <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> option when creating the <bpt id="p2">**</bpt>Return order<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Uživatelé musí vybrat možnost <bpt id="p1">**</bpt>kopírovat náklady<ept id="p1">**</ept> při vytvoření <bpt id="p2">**</bpt>vratky<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>If <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> is not selected, charges from the original sales transaction will not be automatically refunded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud není možnost <bpt id="p1">**</bpt>Kopírovat náklady<ept id="p1">**</ept> zvolena, náklady z původní prodejní transakce nebudou automaticky refundovány.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>If <bpt id="p1">**</bpt>Copy charges<ept id="p1">**</ept> is selected, all charges will be copied to the return order and the user can manually edit or remove any charges they do not want to have refunded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud je možnost <bpt id="p1">**</bpt>Kopírovat náklady<ept id="p1">**</ept> zvolena, všechny náklady se zkopírují do vratky a uživatel může ručně upravovat nebo odebrat veškeré náklady, které nechce mít refundované.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The call center return order process currently does not acknowledge the <bpt id="p1">**</bpt>Refundable<ept id="p1">**</ept> flag on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Proces vratky kontaktního střediska aktuálně nepřipouští příznak <bpt id="p1">**</bpt>Vratný<ept id="p1">**</ept> v nastavení <bpt id="p2">**</bpt>Kód nákladů<ept id="p2">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Configuring POS receipts to show charges</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Konfigurace příjemek POS pro zobrazení nákladů</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>The following receipt elements have been added to the receipt line and footer to support the advanced auto-charges functionality.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Následující prvky příjemky byly přidány na řádek a zápatí příjemky pro podporu funkce rozšířených automatických nákladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source><bpt id="p1">**</bpt>Line Shipping Charges<ept id="p1">**</ept> – This line-level element can be used to recap specific charges codes that have been applied to the sales line.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Náklady expedice řádku<ept id="p1">**</ept> - Tento prvek na úrovni řádku lze použít k souhrnu kódů konkrétních nákladů, které byly použity na řádek prodeje.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Only charges codes that have been flagged as <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> charges on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> page will be displayed here.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Pouze kódy nákladů, které byly označeny příznakem jako náklady <bpt id="p1">**</bpt>Expedice<ept id="p1">**</ept> na stránce <bpt id="p2">**</bpt>Kód nákladů<ept id="p2">**</ept> se zobrazí na tomto místě.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source><bpt id="p1">**</bpt>Line Other Charges<ept id="p1">**</ept> – This line-level element can be used to recap any non-shipping specific charge codes that have been applied to the sales line.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Jiné náklady řádku<ept id="p1">**</ept> - Tento prvek na úrovni řádku lze použít k souhrnu kódů konkrétních neexpedičních nákladů, které byly použity na řádek prodeje.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>These are charges codes where the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> flag on the <bpt id="p2">**</bpt>Charges code<ept id="p2">**</ept> page has not been enabled.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Jedná se o kódy nákladů, kde příznak <bpt id="p1">**</bpt>Expedice<ept id="p1">**</ept> na stránce <bpt id="p2">**</bpt>Kód nákladů<ept id="p2">**</ept> nebyl povolen.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source><bpt id="p1">**</bpt>Order Shipping Charges Details<ept id="p1">**</ept> – This footer-level element displays the descriptions of the charge codes applied to the order that have been flagged as <bpt id="p2">**</bpt>Shipping<ept id="p2">**</ept> charges on the <bpt id="p3">**</bpt>Charges code<ept id="p3">**</ept> setup page.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Podrobnosti dopravného objednávky<ept id="p1">**</ept> - Tento prvek na úrovni zápatí zobrazí popisy kódů nákladů, které jsou použity na objednávku s příznakem nákladů <bpt id="p2">**</bpt>Expedice<ept id="p2">**</ept> na stránce nastavení <bpt id="p3">**</bpt>Kód nákladů<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source><bpt id="p1">**</bpt>Order Shipping Charges<ept id="p1">**</ept> – This footer-level element shows the dollar value of the shipping-related charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Dopravné objednávky<ept id="p1">**</ept> - Tento prvek na úrovni zápatí zobrazuje peněžní hodnotu nákladů souvisejících s expedicí.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source><bpt id="p1">**</bpt>Order Other Charges Details<ept id="p1">**</ept> – This footer-level element displays the description of the charges codes applied to the order that have not been flagged as shipping-related charges.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Podrobnosti jiných nákladů objednávky<ept id="p1">**</ept> - Tento prvek na úrovni zápatí zobrazí popis kódů nákladů, které jsou použity na objednávku bez příznaku nákladů souvisejících s expedicí.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source><bpt id="p1">**</bpt>Order Other Charges<ept id="p1">**</ept> – This footer-level element displays the dollar value of the other charges that are not shipping-related.</source><target logoport:matchpercent="98" state="translated" state-qualifier="x-fuzzy-match-unedited"><bpt id="p1">**</bpt>Jiné náklady objednávky<ept id="p1">**</ept> - Tento prvek na úrovni zápatí zobrazuje peněžní hodnotu jiných nákladů nesouvisejících s expedicí.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>It is recommended that the organization also add free text fields to the receipt footer, in order to define the areas where charges will be recapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Doporučujeme, aby organizace rovněž přidala volná textová pole do zápatí příjemky za účelem definování oblastí, kde budou náklady shrnuty.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Preventing charges from being calculated until the POS order is completed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Zabránění výpočtu nákladů do dokončení objednávky POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Some organizations may prefer to wait until the user has finished adding all of the sales lines to the POS transaction before calculating charges.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Některé organizace mohou chtít počkat, než uživatel dokončí přidání všech prodejních řádků k transakci POS před výpočtem nákladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>To prevent calculation of charges as items are added to the POS transaction, turn on the <bpt id="p1">**</bpt>Manual charge calculation<ept id="p1">**</ept> parameter in the <bpt id="p2">**</bpt>Functionality profile<ept id="p2">**</ept> used by the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Chcete-li zabránit výpočtu nákladů, když se k transakci POS přidávají položky, zapněte parametr <bpt id="p1">**</bpt>Ruční výpočet nákladů<ept id="p1">**</ept> ve <bpt id="p2">**</bpt>funkčním profilu<ept id="p2">**</ept> používaném obchodem.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Enabling this parameter will require the POS user to use the <bpt id="p1">**</bpt>Calculate totals<ept id="p1">**</ept> operation when they have completed adding the products to the POS transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Povolení tohoto parametru vyžaduje, aby uživatel POS použil operaci <bpt id="p1">**</bpt>Vypočítat součty<ept id="p1">**</ept> po dokončení přidání produktů k transakci POS.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>The <bpt id="p1">**</bpt>Calculate totals<ept id="p1">**</ept> operation will then trigger the calculation of any auto charges for the order header or lines as applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Operace <bpt id="p1">**</bpt>Vypočítat součty<ept id="p1">**</ept> poté spustí výpočet jakýchkoliv automatických nákladů pro záhlaví nebo řádky objednávky podle potřeby.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Charges override reports</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sestavy přepsání nákladů</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>If users manually override the calculated charges or add a manual charge to the transaction, this data will available for auditing in the <bpt id="p1">**</bpt>Charge Override History<ept id="p1">**</ept> report.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pokud uživatelé ručně přepíší vypočtené náklady nebo přidají ruční náklady do transakce, budou tato data dostupná pro audit v sestavě <bpt id="p1">**</bpt>Historie přespání nákladů<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>The report can be accessed from <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Inquiries and reports <ph id="ph2">\&gt;</ph> Charge Override History<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Sestava se nalézá v možnostech <bpt id="p1">**</bpt>Maloobchod <ph id="ph1">\&gt;</ph> Dotazy a sestavy <ph id="ph2">\&gt;</ph> Historie přepsání nákladů<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>It is important to note that the data needed for this report is imported from the channel database into HQ through the "P" distribution schedule jobs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Je důležité poznamenat, že data potřebná pro tuto sestavu se importují z databáze maloobchodní sítě do HQ prostřednictvím úloh plánování distribuce "P".</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Therefore, information about overrides just performed in the POS may not be immediately available on this report until this job has uploaded the store transaction data into HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Informace o přepsáních právě provedených v POS proto nemusí být okamžitě k dispozici v této sestavě, dokud tato úloha nenahraje data transakce obchodu do HQ.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>