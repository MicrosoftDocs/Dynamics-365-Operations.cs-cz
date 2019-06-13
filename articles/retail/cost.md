<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="cost.md" target-language="cs-CZ">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>cost.4e88df.80e7a033467c3d94d55f06daa05f99bd27e19a29.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>80e7a033467c3d94d55f06daa05f99bd27e19a29</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\cost.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Cost configuration for distributed order management (DOM)</source><target logoport:matchpercent="53" state="translated" state-qualifier="fuzzy-match">Konfigurace nákladů pro distribuovanou správu objednávek</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes cost configuration for the distributed order management (DOM) functionality in Microsoft Dynamics 365 for Retail.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Toto téma popisuje konfiguraci nákladů pro funkcionalitu distribuované správy objednávek v aplikaci Microsoft Dynamics 365 for Retail.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Cost configuration for distributed order management (DOM)</source>
        <target logoport:matchpercent="53" state="translated" state-qualifier="leveraged-inherited">Konfigurace nákladů pro distribuovanou správu objednávek</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</source><target logoport:matchpercent="0" state="translated">Organizace zvažují více komponent nákladů, aby určily optimální umístění, odkud se bude plnit objednávka.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Some of these cost components are shipping cost, handling cost, and packaging cost.</source><target logoport:matchpercent="0" state="translated">Některými z těchto komponent nákladů jsou náklady na přepravu, náklady na zpracování a náklady balení.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>A combination of these costs is calculated to determine the fulfillment location.</source><target logoport:matchpercent="0" state="translated">Pro určení místa plnění se vypočítává kombinace těchto nákladů.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>When the first iteration of distributed order management (DOM) in Microsoft Dynamics 365 for Retail optimized the assignment of orders to fulfillment locations, it factored in distance only.</source><target logoport:matchpercent="0" state="translated">Když první iterace správy distribuovaných objednávek v aplikaci Microsoft Dynamics 365 for Retail optimalizovala přiřazení objednávek do míst plnění, byla tato skutečnost zohledněna pouze ve vzdálenosti.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Although distance can be correlated with cost, it isn't the same as cost.</source><target logoport:matchpercent="0" state="translated">Ačkoli vzdálenost může vzájemně souviset s náklady, není totéž jako náklady.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</source><target logoport:matchpercent="0" state="translated">Například náklady metody doručení na druhý den stojí více, než doručení na tutéž vzdálenost do tří nebo do sedmi dnů.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</source><target logoport:matchpercent="0" state="translated">Funkce konfigurace nákladů umožňuje maloobchodníkům definovat a konfigurovat další komponenty nákladů, které budou vypočítány a zohledněny při určování optimálního umístění, odkud se budou plnit řádky objednávky.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="52" state="translated" state-qualifier="fuzzy-match">Když jsou komponenty nákladů nakonfigurovány, řešitel DOM používá k určení optimálního umístění pro plnění objednávky pouze tyto definice nákladů.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>It doesn't consider the distance component as a cost.</source><target logoport:matchpercent="0" state="translated">Nepovažuje komponentu vzdálenosti jako náklady.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Když však nejsou nakonfigurovány žádné komponenty nákladů, řešitel DOM používá komponentu vzdálenosti jako náklad pro určení optimálního umístění pro plnění objednávky.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Set up cost components</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Nastavení komponent nákladů</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Two major cost component types can be defined in the system: <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Other<ept id="p2">**</ept>.</source><target logoport:matchpercent="0" state="translated">V systému lze definovat dva hlavní typy komponent nákladů: <bpt id="p1">**</bpt>Expedice<ept id="p1">**</ept> a <bpt id="p2">**</bpt>Jiné<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Both cost component types support multiple calculation bases, as shown in the following table.</source><target logoport:matchpercent="48" state="translated" state-qualifier="fuzzy-match">Oba typy komponent nákladů podporují více základů výpočtu, jak je znázorněno v následující tabulce.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Cost component type</source><target logoport:matchpercent="76" state="translated" state-qualifier="fuzzy-match">Typ komponenty nákladu</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Calculation basis</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Základ výpočtu</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Shipping</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Expedice</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Simple</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Jednoduchý</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Tiered</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Vrstvený</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Other</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Jiný</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Sales order</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">Prodejní objednávka</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Sales line</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Řádek prodeje</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Location</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">Umístění</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Shipping cost component type</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Typ komponenty nákladu Expedice</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and a calculation basis for shipping costs.</source><target logoport:matchpercent="0" state="translated">Tato část vysvětluje, jak nastavit každou kombinaci typu komponenty nákladu <bpt id="p1">**</bpt>Expedice<ept id="p1">**</ept> a základ výpočtu pro přepravní náklady.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>It also explains how the DOM solver uses each combination.</source><target logoport:matchpercent="30" state="translated" state-qualifier="fuzzy-match">Také vysvětluje, jak jsou řešitel DOM používá každou kombinaci.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Cost component type = Shipping and Calculation basis = Simple</source><target logoport:matchpercent="0" state="translated">Typ komponenty nákladů = Expedice a základ výpočtu = Jednoduchý</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Simple<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="0" state="translated">Pokud se použije kombinace typu komponenty nákladů <bpt id="p1">**</bpt>Expedice<ept id="p1">**</ept> a základ výpočtu <bpt id="p2">**</bpt>Jednoduchý<ept id="p2">**</ept>, přepravní náklady pro režim doručení jsou založeny buď na paušálních nákladech nebo na vzdálenosti.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You must set up the following fields for this combination:</source><target logoport:matchpercent="62" state="translated" state-qualifier="fuzzy-match">Pro tuto kombinaci musíte nastavit následující pole:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Koeficient nákladů<ept id="p1">**</ept> - Zadejte jedinečný identifikátor pro koeficient nákladů.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source><target logoport:matchpercent="78" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Popis<ept id="p1">**</ept> – Zadejte název a popis koeficientu nákladů.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source><target logoport:matchpercent="52" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Počáteční datum<ept id="p1">**</ept> a <bpt id="p2">**</bpt>Koncové datum<ept id="p2">**</ept> – Tato pole můžete použít k omezení koeficientu nákladů na konkrétní časový rozsah.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source><target logoport:matchpercent="54" state="translated" state-qualifier="fuzzy-match">Pokud tato pole ponecháte nevyplněná, koeficient nákladů bude platný pro neomezené období.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source><target logoport:matchpercent="59" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Aktivní<ept id="p1">**</ept> - Označuje, zda je koeficient nákladů aktivní.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source><target logoport:matchpercent="52" state="translated" state-qualifier="fuzzy-match">Distribuovaná správa objednávek zvažuje pouze aktivní faktory nákladů, které jsou přidružené k profilu plnění.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source><target logoport:matchpercent="32" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Společnost<ept id="p1">**</ept> - Určuje právnickou osobu, pro kterou je koeficient nákladů nakonfigurován.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>All lines of the calculation criteria must be for the same legal entity.</source><target logoport:matchpercent="32" state="translated" state-qualifier="fuzzy-match">Všechny řádky kritérií výpočtu musí být pro stejnou právnickou osobu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source><target logoport:matchpercent="59" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Způsoby dodání<ept id="p1">**</ept> - Určují způsoby dodání, pro které jsou nakonfigurovány náklady.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Typ výpočtu<ept id="p1">**</ept> – Určuje, jak mají být vypočítány náklady pro konkrétní způsob dodání.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Two calculation types are supported:</source><target logoport:matchpercent="62" state="translated" state-qualifier="fuzzy-match">Jsou podporovány dva typy výpočtu:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Pevný<ept id="p1">**</ept> – Pro způsob dodání se používá jednotný paušální náklad.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source><target logoport:matchpercent="33" state="translated" state-qualifier="fuzzy-match">Pokud vyberete tento typ výpočtu, pole <bpt id="p1">**</bpt>Náklady<ept id="p1">**</ept> definuje jednotný paušální náklad.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>Per-distance unit<ept id="p1">**</ept> – The cost for the mode of delivery is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Podle jednotky vzdálenosti<ept id="p1">**</ept> – Náklad pro způsob dodání se vypočítá jako hodnota nákladů specifikovaná v poli <bpt id="p2">**</bpt>Náklady<ept id="p2">**</ept> krát vzdálenost mezi adresou doručení a místy.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Náklady<ept id="p1">**</ept> – Určuje hodnotu nákladů používanou ve spojení s polem <bpt id="p2">**</bpt>Typ výpočtu<ept id="p2">**</ept> pro výpočet nákladů pro způsob dodání.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Cost component type = Shipping and Calculation basis = Tiered</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Typ komponenty nákladů = Expedice a základ výpočtu = Vrstvený</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>If a combination of the <bpt id="p1">**</bpt>Shipping<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Tiered<ept id="p2">**</ept> calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</source><target logoport:matchpercent="95" state="translated" state-qualifier="fuzzy-match">Pokud se použije kombinace typu komponenty nákladů <bpt id="p1">**</bpt>Expedice<ept id="p1">**</ept> a základ výpočtu <bpt id="p2">**</bpt>Vrstvený<ept id="p2">**</ept>, přepravní náklady pro režim doručení jsou založeny buď na paušálních nákladech nebo na vzdálenosti.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>However, in this combination, the distance is based on a tiered range of distances.</source><target logoport:matchpercent="0" state="translated">V této kombinaci je však vzdálenost založena na vrstveném rozsahu vzdáleností.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="62" state="translated" state-qualifier="leveraged-inherited">Pro tuto kombinaci musíte nastavit následující pole:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="68" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Koeficient nákladů<ept id="p1">**</ept> - Zadejte jedinečný identifikátor pro koeficient nákladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Popis<ept id="p1">**</ept> – Zadejte název a popis koeficientu nákladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>Default cost<ept id="p1">**</ept> – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Výchozí náklady<ept id="p1">**</ept> – Určují náklady, které by měly být použity pro způsob dodání, pokud vzdálenost mezi adresou doručení a místem nespadá do žádné z vrstvených vzdáleností pro způsob dodání.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="52" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Počáteční datum<ept id="p1">**</ept> a <bpt id="p2">**</bpt>Koncové datum<ept id="p2">**</ept> – Tato pole můžete použít k omezení koeficientu nákladů na konkrétní časový rozsah.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="54" state="translated" state-qualifier="leveraged-inherited">Pokud tato pole ponecháte nevyplněná, koeficient nákladů bude platný pro neomezené období.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="59" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktivní<ept id="p1">**</ept> - Označuje, zda je koeficient nákladů aktivní.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="52" state="translated" state-qualifier="leveraged-inherited">Distribuovaná správa objednávek zvažuje pouze aktivní faktory nákladů, které jsou přidružené k profilu plnění.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">**</bpt>Company<ept id="p1">**</ept> – Specify the legal entity that the cost factor is configured for.</source>
        <target logoport:matchpercent="32" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Společnost<ept id="p1">**</ept> - Určuje právnickou osobu, pro kterou je koeficient nákladů nakonfigurován.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>All lines of the calculation criteria must be for the same legal entity.</source>
        <target logoport:matchpercent="32" state="translated" state-qualifier="leveraged-inherited">Všechny řádky kritérií výpočtu musí být pro stejnou právnickou osobu.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>Modes of delivery<ept id="p1">**</ept> – Specify the modes of delivery that the cost is configured for.</source>
        <target logoport:matchpercent="59" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Způsoby dodání<ept id="p1">**</ept> - Určují způsoby dodání, pro které jsou nakonfigurovány náklady.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">**</bpt>Distance type<ept id="p1">**</ept> – Specify whether the tiered distance definition is an aerial distance or a road distance.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Typ vzdálenosti<ept id="p1">**</ept> – Určuje, zda definice vrstvené vzdálenosti je vzdušná vzdálenost nebo vzdálenost po silnici.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>Distance units<ept id="p1">**</ept> – Specify the unit that the tiered distance is measured in.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Jednotky vzdálenosti<ept id="p1">**</ept> – Určuje jednotku, ve které se měří vrstvená vzdálenost.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>Distance from<ept id="p1">**</ept> – Specify the start range for the tiered distance.</source><target logoport:matchpercent="56" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Vzdálenost od<ept id="p1">**</ept> – Určuje počátek rozsahu pro vrstvenou vzdálenost.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source><bpt id="p1">**</bpt>Distance to<ept id="p1">**</ept> – Specify the end range for the tiered distance.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Vzdálenost do<ept id="p1">**</ept> – Určuje konec rozsahu pro vrstvenou vzdálenost.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">**</bpt>Calculation type<ept id="p1">**</ept> – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Typ výpočtu<ept id="p1">**</ept> – Určuje, jak mají být vypočítány náklady pro konkrétní způsob dodání a vrstvenou vzdálenost.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Two calculation types are supported:</source>
        <target logoport:matchpercent="62" state="translated" state-qualifier="leveraged-inherited">Jsou podporovány dva typy výpočtu:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>Fixed<ept id="p1">**</ept> – A flat cost is used for the mode of delivery.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Pevný<ept id="p1">**</ept> – Pro způsob dodání se používá jednotný paušální náklad.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>If you select this calculation type, the <bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> field defines the flat cost.</source>
        <target logoport:matchpercent="33" state="translated" state-qualifier="leveraged-inherited">Pokud vyberete tento typ výpočtu, pole <bpt id="p1">**</bpt>Náklady<ept id="p1">**</ept> definuje jednotný paušální náklad.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>Per distance unit<ept id="p1">**</ept> – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the <bpt id="p2">**</bpt>Cost<ept id="p2">**</ept> field times the distance between the delivery address and the locations.</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Podle jednotky vzdálenosti<ept id="p1">**</ept> – Náklad pro způsob dodání a vrstvenou vzdálenost se vypočítá jako hodnota nákladů specifikovaná v poli <bpt id="p2">**</bpt>Náklady<ept id="p2">**</ept> krát vzdálenost mezi adresou doručení a místy.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value that is used in conjunction with the <bpt id="p2">**</bpt>Calculation type<ept id="p2">**</ept> field to compute the cost for a mode of delivery.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Náklady<ept id="p1">**</ept> – Určuje hodnotu nákladů používanou ve spojení s polem <bpt id="p2">**</bpt>Typ výpočtu<ept id="p2">**</ept> pro výpočet nákladů pro způsob dodání.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>When you define tiered distances, the system validates that there are no missing or overlapping distances.</source><target logoport:matchpercent="0" state="translated">Když definujete vrstvené vzdálenosti, systém ověří, zda se vzdálenosti nepřekrývají nebo nechybí.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The distance type that is used for a mode of delivery must be the same across all the tiered distances.</source><target logoport:matchpercent="55" state="translated" state-qualifier="fuzzy-match">Typ vzdálenosti používaný pro způsob dodání musí být shodný napříč všemi vrstvenými vzdálenostmi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Other cost component type</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">Jiný typ komponenty nákladu</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section explains how to set up each combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and an other cost type for non-shipping costs.</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match">Tato část vysvětluje, jak nastavit každou kombinaci typu komponenty nákladu <bpt id="p1">**</bpt>Jiný<ept id="p1">**</ept> a jiný typ nákladů pro jiné než přepravní náklady.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>It also explains how the DOM solver uses each combination.</source>
        <target logoport:matchpercent="30" state="translated" state-qualifier="leveraged-inherited">Také vysvětluje, jak jsou řešitel DOM používá každou kombinaci.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Cost component type = Other and Other cost type = Sales order</source><target logoport:matchpercent="0" state="translated">Typ komponenty nákladů = Jiný a jiný typ nákladů = Prodejní objednávka</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales order<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order level.</source><target logoport:matchpercent="0" state="translated">Kombinace typu nákladů <bpt id="p1">**</bpt>Jiný<ept id="p1">**</ept> a jiného typu nákladů <bpt id="p2">**</bpt>Prodejní objednávka<ept id="p2">**</ept> se používá pro definování nepřepravních nákladů na úrovni prodejní objednávky.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="62" state="translated" state-qualifier="leveraged-inherited">Pro tuto kombinaci musíte nastavit následující pole:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="68" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Koeficient nákladů<ept id="p1">**</ept> - Zadejte jedinečný identifikátor pro koeficient nákladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Popis<ept id="p1">**</ept> – Zadejte název a popis koeficientu nákladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="52" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Počáteční datum<ept id="p1">**</ept> a <bpt id="p2">**</bpt>Koncové datum<ept id="p2">**</ept> – Tato pole můžete použít k omezení koeficientu nákladů na konkrétní časový rozsah.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="54" state="translated" state-qualifier="leveraged-inherited">Pokud tato pole ponecháte nevyplněná, koeficient nákladů bude platný pro neomezené období.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="59" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktivní<ept id="p1">**</ept> - Označuje, zda je koeficient nákladů aktivní.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="52" state="translated" state-qualifier="leveraged-inherited">Distribuovaná správa objednávek zvažuje pouze aktivní faktory nákladů, které jsou přidružené k profilu plnění.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order level.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Náklady<ept id="p1">**</ept> – Určuje hodnotu nákladů pro nepřepravní náklady na úrovni prodejní objednávky.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Cost component type = Other and Other cost type = Sales line</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Typ komponenty nákladů = Jiný a jiný typ nákladů = Prodejní řádek</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Sales line<ept id="p2">**</ept> other cost type is used to define non-shipping costs at the sales order line level.</source><target logoport:matchpercent="93" state="translated" state-qualifier="fuzzy-match">Kombinace typu nákladů <bpt id="p1">**</bpt>Jiný<ept id="p1">**</ept> a jiného typu nákladů <bpt id="p2">**</bpt>Prodejní řádek<ept id="p2">**</ept> se používá pro definování nepřepravních nákladů na úrovni řádku prodejní objednávky.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="62" state="translated" state-qualifier="leveraged-inherited">Pro tuto kombinaci musíte nastavit následující pole:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="68" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Koeficient nákladů<ept id="p1">**</ept> - Zadejte jedinečný identifikátor pro koeficient nákladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Popis<ept id="p1">**</ept> – Zadejte název a popis koeficientu nákladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="52" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Počáteční datum<ept id="p1">**</ept> a <bpt id="p2">**</bpt>Koncové datum<ept id="p2">**</ept> – Tato pole můžete použít k omezení koeficientu nákladů na konkrétní časový rozsah.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="54" state="translated" state-qualifier="leveraged-inherited">Pokud tato pole ponecháte nevyplněná, koeficient nákladů bude platný pro neomezené období.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="59" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktivní<ept id="p1">**</ept> - Označuje, zda je koeficient nákladů aktivní.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="52" state="translated" state-qualifier="leveraged-inherited">Distribuovaná správa objednávek zvažuje pouze aktivní faktory nákladů, které jsou přidružené k profilu plnění.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the sales order line level.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Náklady<ept id="p1">**</ept> – Určuje hodnotu nákladů pro nepřepravní náklady na úrovni řádku prodejní objednávky.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Cost component type = Other and Other cost type = Location</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Typ komponenty nákladů = Jiný a jiný typ nákladů = Místo</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>A combination of the <bpt id="p1">**</bpt>Other<ept id="p1">**</ept> cost component type and the <bpt id="p2">**</bpt>Location<ept id="p2">**</ept> other cost type is used to define non-shipping costs for a group of locations or an individual location.</source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match">Kombinace typu nákladů <bpt id="p1">**</bpt>Jiný<ept id="p1">**</ept> a jiného typu nákladů <bpt id="p2">**</bpt>Místo<ept id="p2">**</ept> se používá pro definování nepřepravních nákladů pro skupinu míst nebo jednotlivé místo.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>You must set up the following fields for this combination:</source>
        <target logoport:matchpercent="62" state="translated" state-qualifier="leveraged-inherited">Pro tuto kombinaci musíte nastavit následující pole:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source><bpt id="p1">**</bpt>Cost factor<ept id="p1">**</ept> – Enter a unique identifier for the cost factor.</source>
        <target logoport:matchpercent="68" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Koeficient nákladů<ept id="p1">**</ept> - Zadejte jedinečný identifikátor pro koeficient nákladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">**</bpt>Description<ept id="p1">**</ept> – Enter the name and description of the cost factor.</source>
        <target logoport:matchpercent="78" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Popis<ept id="p1">**</ept> – Zadejte název a popis koeficientu nákladů.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source><bpt id="p1">**</bpt>Start date<ept id="p1">**</ept> and <bpt id="p2">**</bpt>End date<ept id="p2">**</ept> – You can use these fields to limit the cost factor for a specific date range.</source>
        <target logoport:matchpercent="52" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Počáteční datum<ept id="p1">**</ept> a <bpt id="p2">**</bpt>Koncové datum<ept id="p2">**</ept> – Tato pole můžete použít k omezení koeficientu nákladů na konkrétní časový rozsah.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>If you leave these fields blank, the cost factor is valid for an indefinite period.</source>
        <target logoport:matchpercent="54" state="translated" state-qualifier="leveraged-inherited">Pokud tato pole ponecháte nevyplněná, koeficient nákladů bude platný pro neomezené období.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">**</bpt>Active<ept id="p1">**</ept> – Indicate whether the cost factor is active.</source>
        <target logoport:matchpercent="59" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>Aktivní<ept id="p1">**</ept> - Označuje, zda je koeficient nákladů aktivní.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The DOM considers only active cost factors that are associated with the fulfillment profile.</source>
        <target logoport:matchpercent="52" state="translated" state-qualifier="leveraged-inherited">Distribuovaná správa objednávek zvažuje pouze aktivní faktory nákladů, které jsou přidružené k profilu plnění.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">**</bpt>Fulfillment group<ept id="p1">**</ept> – Specify the group of locations that the non-shipping cost is defined for.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>Skupina plnění<ept id="p1">**</ept> – Určuje skupinu míst, pro která jsou definovány nepřepravní náklady.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><bpt id="p1">**</bpt>Fulfillment location<ept id="p1">**</ept> – Specify the location that the non-shipping cost is defined for.</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Místo plnění<ept id="p1">**</ept> – Určuje místo, pro které jsou definovány nepřepravní náklady.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</source><target logoport:matchpercent="0" state="translated">Pro kritéria výpočtu na základě místa nelze určit skupinu plnění a místo plnění na stejném řádku.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">**</bpt>Cost<ept id="p1">**</ept> – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</source><target logoport:matchpercent="70" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Náklady<ept id="p1">**</ept> – Určuje hodnotu nákladů pro nepřepravní náklady na úrovni skupiny plnění nebo na úrovni místa plnění.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</source><target logoport:matchpercent="0" state="translated">Aby distribuovaná správa objednávek zvažovala při svém spuštění tyto náklady, musíte přidat koeficient nákladů do příslušného profilu plnění.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>