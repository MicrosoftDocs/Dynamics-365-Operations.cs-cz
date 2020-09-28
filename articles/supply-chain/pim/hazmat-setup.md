---
title: Příprava nebezpečných materiálů
description: Toto téma vysvětluje, jak nastavit data potřebná ke klasifikaci položek jako nebezpečných materiálů. Když vytvoříte prodejní objednávku, která obsahuje položku klasifikovanou jako nebezpečný materiál, systém vygeneruje dokumentaci nebezpečného materiálu pro tuto prodejní objednávku při jeho expedici.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: b049559b64045e80a40afd99bac30a9cfe1d0580
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/14/2020
ms.locfileid: "3803206"
---
# <a name="set-up-hazardous-materials"></a>Příprava nebezpečných materiálů

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Chcete-li používat funkce nebezpečných materiálů, musíte nejprve nastavit data, která jsou požadována ke klasifikaci položek jako nebezpečných materiálů. Poté, dyž vytvoříte prodejní objednávku, která obsahuje položku klasifikovanou jako nebezpečný materiál, systém vygeneruje dokumentaci nebezpečného materiálu pro tuto prodejní objednávku při jeho expedici.

## <a name="turn-on-the-hazardous-materials-feature-for-your-system"></a>Zapnutí funkce nebezpečných materiálů v systému

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul**: *Řízení informací o produktech*
- **Název funkce** *Informace o produktu s nebezpečnými materiály a dokumentace expedice*

## <a name="hazardous-material-regulations"></a>Předpisy o nebezpečných materiálech

Abyste mohli používat procesy s nebezpečnými materiály, musíte nejprve vytvořit předpis. Předpisy definují, jak se pro položku vytvoří tištěný text k dodávce. Rovněž definují přidružené způsoby doručení.

Zde je několik společných předpisů:

- **ADR** – Nařízení vztahující se k mezinárodní přepravě nebezpečného zboží po silnici
- **CFR 49** - Nařízení v USA pro přepravu nebezpečného zboží
- **IMDG** – Kód mezinárodní námořní přepravy nebezpečného zboží
- **IATA** – Nařízení mezinárodního sdružení letecké dopravy (IATA) o nebezpečném zboží

Tyto předpisy pomáhají určit, jaké informace by se měly zobrazit, když pro položku vytisknete text k dodávce. Můžete definovat tolik předpisů, kolik musíte dodržovat.

> [!IMPORTANT]
> Funkce pro nastavení informačních kódů, které se vztahují k nebezpečným materiálům, nezaručuje, že vaše společnost dodržuje předpisy. Je to pouze nástroj, který vám pomáhá vytvářet procesy pro vaši společnost.

Předpis je obvykle k dispozici pro konkrétní způsob dopravy, jako je námořní, silniční nebo letecká doprava. Proto můžete každý předpis přidružit ke způsobu doručení. Způsob doručení se použije při tisku konkrétních dokumentů v Řízení skladu. V Řízení skladu je každá zásilka propojena s dopravcem a přepravní službou, které jsou nastaveny v modulu **Přeprava**. Způsob dodání je přidružen k dopravci a dopravní službě. Když spustíte sestavu, způsob doručení se použije k vyhledání tištěného textu dodávky, který je přidružen k uvolněné položce.

Tato nastavení nejsou specifická pro každou právnickou osobu (společnost). Proto můžete mít společnou sadu informací o nebezpečných materiálech, kterou sdílejí všechny vaše právní subjekty.

Pro každý předpis můžete definovat seznam materiálů a použít jej jako seznam šablon, který je přidružen k vydaným položkám. Pro každý předpis můžete také definovat nastavení tisku. Nastavení tisku umožňuje definovat, jak je sestaven text dodávky pro danou položku. Nastavení tisku se používá k sestavení tištěného textu dodávky pro uvolněnou položku.

Chcete-li stanovit předpisy pro nebezpečný materiál, přejděte na **Řízení informací o produktech \> Nastavení \> Dokumentace expedice nebezpečného materiálu \> Předpis o nebezpečných materiálech**. Na stránce **Předpis o nebezpečných materiálech** můžete vytvořit libovolný počet předpisů a nakonfigurovat každý z nich pomocí polí, která jsou popsána v následujících podsekcích.

### <a name="hazardous-material-regulation-header"></a>Záhlaví předpisu o nebezpečných materiálech

Každý předpis má kód a popis. V následující tabulce jsou popsána pole, která jsou k dispozici v záhlaví.

| Pole | popis |
|---|---|
| Kód regulace | Zadejte kód k identifikaci záznamu předpisu nebezpečného materiálu. |
| popis | Zadejte popis předpisu nebezpečného materiálu. |

### <a name="print-setup-fasttab"></a>Záložka s náhledem Nastavení tisku

Každý předpis může mít libovolný počet nastavení tisku. Nastavení tisku definujete na záložce s náhledem **Nastavení tisku**. V následující tabulce jsou popsána pole, která jsou k dispozici pro každé nastavení tisku.

| Pole | popis |
|---|---|
| Pořadí | Definujte pořadí, ve kterém budou pole odkazována v textu dodávky. |
| Pole tisku | Vyberte pole, které chcete zahrnout do textu k dodávce. Ne všechna pole pro nebezpečný materiál budou k dispozici pro tisk. K dispozici budou pouze společná pole, která jsou použita k definování textu k dodávce v různých předpisech. První pole pro tisk byste měli definovat jako oddělovač polí, jehož hodnota **Sekvence** je *0* (nula), takže jej lze použít jako oddělovač mezi ostatními poli. Je vyžadován pouze jeden odkaz na oddělovač polí.<p>K dispozici jsou následující hodnoty:</p><ul></li><li>**Oddělovač polí** – Toto pole pro tisk slouží jako oddělovač polí pro text. V sekvenci je vyžadován pouze jeden oddělovač polí. Obvykle byste měli nastavit hodnotu **Sekvence** pro tohle pole pro tisk na *0* (nula). Systém vyhledá oddělovač polí a použije první, který najde v seznamu. Textová hodnota použitá v řetězci bude pocházet z pole **Vytisknout po**.</li><li>**Identifikace** – Toto pole pro tisk vloží do tištěného textu [identifikační kód a/nebo popis](#identification).</li><li>**Třída** – Toto pole pro tisk vloží do tištěného textu [kód a/nebo popis třídy](#classes).</li><li>**Divize** – Toto pole pro tisk vloží do tištěného textu [kód a/nebo popis divize](#divisions).</li><li>**Skupina balení** – Toto pole pro tisk vloží do tištěného textu [kód a/nebo popis skupiny balení](#packing-group).</li><li>**Kód a/nebo popis tunelu** – Toto pole pro tisk vloží do tištěného textu [kód a/nebo popis tunelu](#tunnel).</li><li>**Správný přepravní název** – Toto pole pro tisk vloží do tištěného textu [správný přepravní název](hazmat-items.md#hazmat-description).</li><li>**Technický název** – Toto pole pro tisk vloží do tištěného textu [technický název a/nebo kód](#technical-name).</li><li>**Kategorie přepravy** – Toto pole pro tisk vloží do tištěného textu [kód a/nebo popis kategorie přepravy](#transport-category).</li><li>**Uskladnění** – Toto pole pro tisk vloží do tištěného textu [kód a/nebo popis uskladnění](#stowage).</li><li>**Pevný text** – Toto pole pro tisk vloží, který je definován v poli **Pevný text** pro tento řádek.</li><li>**Kód a/nebo popis popisku** – Toto pole pro tisk vloží do tištěného textu [kód a/nebo popis popisku](#label).</li><li>**Balení do letadla** – Toto pole pro tisk vloží do tištěného textu [kód a/nebo popis pokynů pro balení do letadla](#packing-instruction).</li><li>**Omezené množství** – Toto tiskové pole kontroluje, zda je položka označena jako a [omezené množství zboží](hazmat-items.md#material-management) a pokud ano, zadá text, který je definován v poli **Pevný text** pro tento řádek.</li><li>**Popis balení** – Toto pole pro tisk vloží do tištěného textu [popis balení](#packing-description).</li></ul> |
| Vytisknout před | Zadejte text, který má být vytištěn před obsahem definovaným pomocí nastavení **Pole pro tisk**. |
| Vytisknout po | Zadejte text, který má být vytištěn po obsahu definovaném pomocí nastavení **Pole pro tisk**. |
| Tisk s předchozím | Toto políčko zaškrtněte, chcete-li zabránit tisku oddělovače polí mezi předchozím polem a tímto polem. Toto zaškrtávací políčko použijte pro pole pro tisk, která jsou volitelná nebo součástí jiného pole pro tisk. |
| Opravený text | Pokud nastavíte **Pole pro tisk** na pole **Pevný text** nebo **Omezené množství**, zadejte text, který se má vytisknout. |
| Zahrnout do tisku | Vyberte, která hodnota nebo hodnoty z vybraného pole pro tisk se mají pro tento řádek vytisknout. Můžete vytisknout kód, popis nebo kód i popis. |

### <a name="mode-of-delivery-fasttab"></a>Záložka s náhledem Způsob dodání

Předpis je sdílená tabulka a není specifická pro každý právní subjekt. Způsoby dodání jsou však specifické pro právnické osoby. Když tedy nastavujete způsob dodání, musíte vybrat vztah mezi předpisem, právnickou osobou a způsobem dodání.

V následující tabulce jsou popsána pole, která jsou k dispozici na záložce s náhledem **Způsob dodání**.

| Pole | popis |
|---|---|
| Společnost | Vyberte právnickou osobu, kterou chcete přidružit k tomuto předpisu. |
| Způsob dodání | Na základě právního subjektu, který jste vybrali, vyberte způsob dodání, který má být přidružen k předpisu. |

### <a name="country-fasttab"></a>Záložka s náhledem Země

Pro referenční účely můžete uvést země nebo regiony, pro které je nařízení relevantní. Když jsou však spuštěny sestavy dodávky, k určení předpisu se použije pouze způsob dodání. Při kontrole dodávky ze skladu neexistuje přímý odkaz na způsob dodání. Dodávku lze přidružit k dopravci a dopravní službě. Když definujete dopravní službu, musíte ji přidružit k režimu dodání. Tento vztah se použije v sestavách dodávek, jako je přepravní doklad, k vyhledání textu pro tisk k dané položce.

V následující tabulce je popsáno pole, které je k dispozici na záložce s náhledem **Země**.

| Pole | popis |
|---|---|
| Země nebo oblast | Vyberte zemi/oblast, kterou chcete přidružit k předpisu. |

## <a name="material-codes"></a><a name="hazmat-codes"></a>Kódy materiálu

Kódy materiálu stanovují nastavení, která se vztahují ke konkrétní nebezpečné součásti, která by mohla být součástí uvolněného produktu. Každý kód materiálu patří do konkrétního předpisu o nebezpečných materiálech a jeho definice musí být v souladu s tímto předpisem. Když použijete kód materiálu na uvolněný produkt pomocí pole **Kód materiálu**, veškerá nastavení nebezpečných materiálů kódu materiálu se automaticky použijí na tento produkt. Proces nastavení uvolněných produktů je proto rychlejší a méně náchylný k chybám.

Chcete-li spravovat definice nebezpečného materiálu, postupujte takto.

1. Přejděte na **Řízení informací o produktech \> Nastavení \> Dokumentace expedice nebezpečného materiálu \> Předpisy o nebezpečných materiálech**.
2. Vyberte předpis, pro který nastavíte definici nebezpečného materiálu.
3. V podokně akcí na kartě **Nastavení** zvolte **Nebezpečné materiály**.
4. Do pole **Kód materiálu** zadejte kód materiálu pro definici nebezpečného materiálu. Tuto hodnotu vyberete, když použijete kód materiálu na uvolněný produkt.

    Pole **Kód předpisu** je jen pro čtení a zobrazuje předpis, který jste vybrali v kroku 2.

5. Pomocí zbývajících polí na této stránce můžete vytvořit a nastavit každý nebezpečný materiál, který se vztahuje na vámi vybraný předpis. Pole, která jsou k dispozici, jsou podmnožinou polí nebezpečného materiálu, která jsou k dispozici pro jednotlivé uvolněné produkty. Další informace viz [Nebezpečné materiály ve výrobcích, objednávkách, dodávkách a nákladech](hazmat-items.md).

## <a name="hazardous-material-classification-groups"></a><a name="classification-groups"></a>Skupiny klasifikace nebezpečných materiálů

Každá skupina klasifikace nebezpečných materiálů definuje skupinu hodnot polí, které tvoří šablonu. Tuto šablonu můžete použít později, když nastavíte informace o nebezpečném materiálu pro uvolněnou položku.

Když přiřadíte kód skupiny klasifikace nebezpečných materiálů uvolněné položce, informace přidružené k této skupině klasifikace se zkopírují do příslušných polí položky. Proto můžete procesy nastavení zjednodušit vytvořením sady souvisejících hodnot polí, které často používáte společně.

Tato nastavení nejsou specifická pro každou právnickou osobu. Proto můžete mít společnou sadu informací o nebezpečných materiálech, kterou sdílejí všechny vaše právní subjekty.

Chcete-li stanovit skupiny klasifikace pro nebezpečný materiál, přejděte na **Řízení informací o produktech \> Nastavení \> Dokumentace expedice nebezpečného materiálu \> Skupina klasifikace nebezpečných materiálů**. Na stránce **Skupina klasifikace nebezpečných materiálů** můžete vytvořit libovolný počet skupin a nakonfigurovat každou z nich pomocí polí, která jsou popsána v následující tabulce.

| Pole | popis |
|---|---|
| Kód skupiny | Zadejte kód pro identifikaci skupiny. |
| popis | Zadejte popis skupiny. |
| Kód třídy | Přidružte [kód třídy](#classes) nebezpečného materiálu ke skupině. |
| Kód divize | Přidružte [kód divize](#divisions) nebezpečného materiálu ke skupině. |
| Kód skupiny balení | Přidružte [kód skupiny balení](#packing-group) ke skupině. |
| Kód kategorie přepravy | Přidružte [kód kategorie přepravy](#transport-category) ke skupině. |
| Multiplikátor | Zadejte násobitel nebezpečných materiálů, který platí pro vybranou třídu a diviz nebezpečných materiálů podle platných předpisů. Tento násobitel se používá jako součást vzorce, který počítá celkový počet *bodů nebezpečného materiálu*, které jsou součástí nákladu nebo dodávky. Další informace o bodech nebezpečného materiálu a tomto násobiteli viz [Záložka s náhledem Správa materiálu](hazmat-items.md#material-management). |

## <a name="hazardous-material-classes"></a><a name="classes"></a>Třídy nebezpečných materiálů

Třída nebezpečného materiálu je obvykle mapována na seznam tříd uvedený v předpisu, kterému chcete vyhovět. Například americká regulace CFR 49 uvádí „třídu 3“ jako vznětlivé hořlavé kapaliny. Můžete nastavit třídy, které jsou relevantní pro materiály, které musíte klasifikovat.

Každá třída bude přiřazena k nastavení materiálu v seznamu materiálů, který souvisí s předpisem. Každé uvolněné položce podle potřeby přiřadíte třídu, která popisuje nebezpečnou povahu produktu.

Tato nastavení nejsou specifická pro každou právnickou osobu. Proto můžete mít společnou sadu informací o nebezpečných materiálech, kterou sdílejí všechny vaše právní subjekty.

Třídy nebezpečných materiálů spolupracují s divizemi, skupinami a skupinami kompatibility následujícím způsobem:

- Když přiřadíte uvolněné položce třídu nebezpečného materiálu, musíte také přiřadit [divizi nebezpečného materiálu](#divisions).
- Můžete použít třídy nebezpečných materiálů společně se [skupinami klasifikace nebezpečných materiálů](#classification-groups) k vytvoření šablony kódů pro nastavení položek.
- Můžete použít [skupiny kompatibility nebezpečných materiálů](#compatibility-groups) ke zjištění, které třídy a divize nebezpečných materiálů lze přepravovat společně.

Chcete-li stanovit třídy pro nebezpečný materiál, přejděte na **Řízení informací o produktech \> Nastavení \> Dokumentace expedice nebezpečného materiálu \> Třída nebezpečného materiálu**. Na stránce **Třída nebezpečného materiálu** můžete vytvořit libovolný počet tříd a nakonfigurovat každou z nich pomocí polí, která jsou popsána v následující tabulce.

| Pole | popis |
|---|---|
| Kód třídy | Zadejte kód pro identifikaci této třídy. Tento kód definujete pro položku. Poté se použije ve vyhledávacích seznamech, když uvolněné položce přiřadíte třídu nebezpečného materiálu. |
| popis | Zadejte popis třídy. |

## <a name="hazardous-material-divisions"></a><a name="divisions"></a>Divize nebezpečných materiálů

Divize nebezpečných materiálů je podmnožinou třídy nebezpečných materiálů. Každému výrobku, který obsahuje nebezpečné materiály, musíte přiřadit jak divizi, tak třídu.

Pro třídy, které nemají žádné divize, vytvořte divizi s kódem *0*. Například v předpisu IATA nemají radioaktivní materiály třídy 7 žádné další poddivize. V tomto případě vytvoříte divizi *0*, kterou můžete přidružit k uvolněnému produktu, když přiřadíte třídu.

Tato nastavení nejsou specifická pro každou právnickou osobu. Proto můžete mít společnou sadu informací o nebezpečných materiálech, kterou sdílejí všechny vaše právní subjekty.

Divize nebezpečných materiálů spolupracují s třídami, skupinami a skupinami kompatibility následujícími způsoby:

- Když přiřadíte uvolněné položce divizi nebezpečného materiálu, musíte také přiřadit [třídu nebezpečného materiálu](#classes).
- Můžete použít divize nebezpečných materiálů společně se [skupinami klasifikace nebezpečných materiálů](#classification-groups) k vytvoření šablony kódů pro nastavení položek.
- Můžete použít [skupiny kompatibility nebezpečných materiálů](#compatibility-groups) ke zjištění, které třídy a divize nebezpečných materiálů lze přepravovat společně.

Chcete-li stanovit divize pro nebezpečný materiál, přejděte na **Řízení informací o produktech \> Nastavení \> Dokumentace expedice nebezpečného materiálu \> Divize nebezpečného materiálu**. Na stránce **Divize nebezpečného materiálu** můžete vytvořit libovolný počet divizí a nakonfigurovat každou z nich pomocí polí, která jsou popsána v následující tabulce.

| Pole | popis |
|---|---|
| Divize | Zadejte kód, který se použije jako referenční číslo divize. |
| popis | Zadejte popis divize. |
| Třída | Vyhledejte a přiřaďte třídu, do které divize patří. |

## <a name="hazardous-material-compatibility-groups"></a><a name="compatibility-groups"></a>Skupiny kompatibility nebezpečných materiálů

Skupiny kompatibility nebezpečných materiálů určují, které třídy a divize nebezpečných materiálů lze expedovat společně. Když operátoři vytvoří náklady nebo dodávky ze skladu, mohou spustit kontrolu kompatibility, která vydá varování, pokud náklad nebo dodávka obsahuje položky, které ne všechny patří do stejné skupiny kompatibility.

Tato nastavení nejsou specifická pro každou právnickou osobu. Proto můžete mít společnou sadu informací o nebezpečných materiálech, kterou sdílejí všechny vaše právní subjekty.

Chcete-li stanovit skupiny kompatibility pro nebezpečný materiál, přejděte na **Řízení informací o produktech \> Nastavení \> Dokumentace expedice nebezpečného materiálu \> Skupina kompatibility nebezpečných materiálů**. Na stránce **Skupina kompatibility nebezpečných materiálů** můžete vytvořit libovolný počet skupin kompatibility a nakonfigurovat každou z nich pomocí polí, která jsou popsána v následujících podsekcích.

### <a name="hazardous-material-compatibility-group-header"></a>Záhlaví skupiny kompatibility nebezpečných materiálů

Každá skupina kompatibility má kód a popis. V následující tabulce jsou popsána pole, která jsou k dispozici v záhlaví.

| Pole | popis |
|---|---|
| Skupina kompatibility | Zadání kódu pro identifikaci skupiny kompatibility |
| popis | Zadejte popis skupiny kompatibility. |

### <a name="compatibility-group-details"></a>Podrobnosti skupiny kompatibility

Každá skupina kompatibility má seznam tříd a divizí nebezpečných materiálů, které lze expedovat společně.

| Pole | popis |
|---|---|
| Třída | Vyberte třídu nebezpečného materiálu, která je kompatibilní se všemi ostatními třídami ve skupině. |
| Divize | Vyberte divizi nebezpečného materiálu, která patří do vybrané třídy. |

## <a name="hazardous-material-specification-values"></a>Hodnoty specifikace nebezpečného materiálu

Microsoft Dynamics 365 Supply Chain Management poskytuje několik typů specifikací nebezpečných materiálů. Pro každý typ musíte vytvořit centralizovanou sadu hodnot pro každé příslušné pole. Uživatelé pak mohou mezi těmito hodnotami vybírat, když konfigurují definice nebezpečného materiálu nebo uvolněné produkty. Supply Chain Management poskytuje kolekci stránek, kde můžete stanovit hodnoty. Každá stránka je věnována jednomu typu specifikace. Popis každé dostupné specifikace a informace o tom, jak stanovit hodnoty, které jsou pro ni k dispozici, viz následující podkapitoly.

Jedním příkladem specifikace nebezpečného materiálu je _kód uskladnění_, který určuje, jak lze daný materiál během přepravy skladovat. Použitím informací v této sekci vytvoříte centrální kolekci kódů uskladnění. Tato kolekce se poté uživatelům zobrazí v rozevíracím seznamu, když nastaví kód uskladnění uvolněného produktu.

Tyto hodnoty specifikace nebezpečného materiálu nejsou specifické pro každou právnickou osobu, proto můžete mít sadu společných hodnot, které jsou sdíleny mezi všemi vašimi právnickými osobami.

[Kódy materiálu](#hazmat-codes) použijete k vytvoření společných kolekcí nastavení pro každou specifikaci dle toho, jak se vztahuje na daný předpis. Podle potřeby pak můžete na každý uvolněný produkt použít příslušný kód. Informace, jak použít kód nebezpečného materiálu na konkrétní uvolněný produkt a jak konfigurovat jednotlivá nastavení tohoto produktu pro jakoukoli zde popsanou specifikaci, viz [Nebezpečné materiály ve výrobcích, objednávkách, dodávkách a nákladech](hazmat-items.md).

### <a name="hazardous-material-emergency-response"></a>Reakci na mimořádné situace nebezpečného materiálu

Specifikace *Nouzová opatření pro nebezpečný materiál* udává, co je třeba udělat, pokud se při přepravě produktu, který obsahuje daný nebezpečný materiál, něco pokazí.

Chcete-li stanovit hodnoty pro tuto specifikaci, přejděte na **Řízení informací o produktech \> Nastavení \> Dokumentace expedice nebezpečného materiálu \> Nouzová opatření pro nebezpečný materiál**. Na stránce **Nouzová reakce pro nebezpečný materiál** můžete vytvořit libovolný počet hodnot a každou nakonfigurovat s kódem klasifikace a krátkým popisem.

### <a name="hazardous-material-identification"></a><a name="identification"></a>Identifikace nebezpečného materiálu

Specifikace *Identifikace nebezpečného materiálu* určuje třídu nebo povahu nebezpečného materiálu. Tato hodnota je obyčejně kód, který je založen na standardu Spojených národů (UN). Každá třída je identifikována kódem a popisem a může stanovit omezení na způsoby dopravy. Například pro identifikaci hořlavého předmětu nebo materiálu vytvoříte třídu nebezpečných materiálů, která používá kód *FL* a popis *Hořlavé*. Rovněž uvedete, že třída nesmí být přepravována letecky.

Chcete-li stanovit hodnoty pro tuto specifikaci, přejděte na **Řízení informací o produktech \> Nastavení \> Dokumentace expedice nebezpečného materiálu \> Identifikace nebezpečného materiálu**. Na stránce **Identifikace nebezpečného materiálu** můžete vytvořit libovolný počet hodnot a nakonfigurovat každou z nich pomocí polí, která jsou popsána v následující tabulce.

| Pole | popis |
|---|---|
| Identifikace | Zadejte kód, který se použije jako referenční číslo, které identifikuje tuto třídu nebezpečného materiálu. |
| popis | Zadejte popis této třídy. |
| Omezit z letecké přepravy | Zaškrtnutím tohoto políčka označíte, že tato třída nebezpečného materiálu by neměla být přepravována letecky. |
| Omezit z námořní přepravy | Zaškrtnutím tohoto políčka označíte, že tato třída nebezpečného materiálu by neměla být přepravována po moři. |

### <a name="hazardous-material-label"></a><a name="label"></a>Štítek nebezpečného materiálu

Specifikace *Popisek nebezpečného materiálu* identifikuje štítek nebezpečného zboží, který musí být použit na příslušné uvolněné výrobky. Samotné popisky udávají, jak by se s produktem mělo zacházet. Například máte produkt, který obsahuje jedovatý plyn. V tomto případě vytvoříte kód popisku, který představuje popisek s jedovatým plynem. Rovněž vytvoříte svůj obchodní proces tak, aby tuto hodnotu vyhledával při expedici produktů.

Chcete-li stanovit hodnoty pro tuto specifikaci, přejděte na **Řízení informací o produktech \> Nastavení \> Dokumentace expedice nebezpečného materiálu \> Popisek nebezpečného materiálu**. Na stránce **Popisek nebezpečného materiálu** můžete vytvořit libovolný počet popisků a každý nakonfigurovat s identifikačním kódem a krátkým popisem.

### <a name="hazardous-material-packing-descriptions"></a><a name="packing-description"></a>Popisy balení nebezpečného materiálu

Specifikace *Popisy balení nebezpečného materiálu* udává, jak musí být nebezpečný předmět zabalen. Může být například nutné jej zabalit do konkrétního typu ocelového bubnu nebo jiného speciálního obalu.

Chcete-li stanovit hodnoty pro tuto specifikaci, přejděte na **Řízení informací o produktech \> Nastavení \> Dokumentace expedice nebezpečného materiálu \> Popisy balení nebezpečného materiálu**. Na stránce **Popisy balení nebezpečného materiálu** můžete vytvořit libovolný počet popisů balení a každý nakonfigurovat s identifikačním kódem a krátkým popisem.

### <a name="hazardous-material-packing-group"></a><a name="packing-group"></a>Skupina balení nebezpečného materiálu

Specifikace *Skupina balení nebezpečného materiálu* identifikuje skupinu balení pro nebezpečnou položku. Skupina balení umožňuje definovat kód a popis, který označuje, jak musí být položky nebezpečného materiálu zabaleny během přepravy nebo expedice. Skupina balení je k položce přiřazena prostřednictvím stránky **Nebezpečné materiály položky**.

Chcete-li stanovit hodnoty pro tuto specifikaci, přejděte na **Řízení informací o produktech \> Nastavení \> Dokumentace expedice nebezpečného materiálu \> Skupina balení nebezpečného materiálu**. Na stránce **Skupina balení nebezpečného materiálu** můžete vytvořit libovolný počet skupin balení a každý nakonfigurovat s identifikačním kódem a krátkým popisem.

### <a name="hazardous-material-packing-instruction"></a><a name="packing-instruction"></a>Pokyny pro balení nebezpečného materiálu

Specifikace *Pokyny pro balení nebezpečného materiálu* určuje pokyny k balení, které je třeba dodržovat, pokud je daná nebezpečná položka připravena k letecké přepravě.

Chcete-li stanovit hodnoty pro tuto specifikaci, přejděte na **Řízení informací o produktech \> Nastavení \> Dokumentace expedice nebezpečného materiálu \> Pokyny pro balení nebezpečného materiálu**. Na stránce **Pokyny pro balení nebezpečného materiálu** můžete vytvořit libovolný počet identifikátorů pokynů pro balení a každý nakonfigurovat s identifikačním kódem a krátkým popisem.

### <a name="hazardous-material-stowage"></a><a name="stowage"></a>Uskladnění nebezpečného materiálu

Specifikace *Uskladnění nebezpečného materiálu* udává, jak musí být produkt skladován na lodi, když je přepravován námořní dopravou.

Chcete-li stanovit hodnoty pro tuto specifikaci, přejděte na **Řízení informací o produktech \> Nastavení \> Dokumentace expedice nebezpečného materiálu \> Uskladnění nebezpečného materiálu**. Na stránce **Uskladnění nebezpečného materiálu** můžete vytvořit libovolný počet identifikátorů uskladnění a každý nakonfigurovat s identifikačním kódem a krátkým popisem.

### <a name="hazardous-material-transport-category"></a><a name="transport-category"></a>Kategorie přepravy nebezpečného materiálu

Specifikace *Kategorie přepravy nebezpečného materiálu* se obvykle používá k seskupení podobných nebezpečných produktů v sestavách. Například kategorie dopravy se používají v sestavě **Shrnutí dodávky**, kterou si můžete vytisknout ze záznamu dodávky ze skladu.

Chcete-li stanovit hodnoty pro tuto specifikaci, přejděte na **Řízení informací o produktech \> Nastavení \> Dokumentace expedice nebezpečného materiálu \> Kategorie přepravy nebezpečného materiálu**. Na stránce **Kategorie přepravy nebezpečného materiálu** můžete vytvořit libovolný počet kategorií přepravy a každý nakonfigurovat se zobrazovaným názvem a krátkým popisem.

### <a name="hazardous-material-technical-name"></a><a name="technical-name"></a>Technický název nebezpečného materiálu

Specifikace *Technický název nebezpečného materiálu* lze použít k poskytnutí běžně používaného nebo interního názvu společnosti, který popisuje každý materiál.

Chcete-li stanovit hodnoty pro tuto specifikaci, přejděte na **Řízení informací o produktech \> Nastavení \> Dokumentace expedice nebezpečného materiálu \> Technický název nebezpečného materiálu**. Na stránce **Technický název nebezpečného materiálu** můžete vytvořit libovolný počet technických názvů a každý nakonfigurovat se zobrazovaným názvem a krátkým popisem.

### <a name="hazardous-material-tunnel"></a><a name="tunnel"></a>Tunel s nebezpečným materiálem

Specifikace *Tunel pro nebezpečný materiál* omezuje typy tunelů, kterými lze přepravovat nebezpečný materiál, určením typů tunelů, které musí být použity. Kategorie tunelů jsou stanoveny příslušnými předpisy pro přepravu nebezpečných materiálů. Tato specifikace se obvykle vztahuje pouze na silniční dopravu.

Chcete-li stanovit hodnoty pro tuto specifikaci, přejděte na **Řízení informací o produktech \> Nastavení \> Dokumentace expedice nebezpečného materiálu \> Tunel pro nebezpečný materiál**. Na stránce **Tunel pro nebezpečný materiál** můžete vytvořit libovolný počet identifikátorů tunelů a každý nakonfigurovat s identifikačním kódem a krátkým popisem.
