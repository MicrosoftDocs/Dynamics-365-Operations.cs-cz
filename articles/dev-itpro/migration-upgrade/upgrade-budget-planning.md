---
title: Upgrade plánování rozpočtu
description: Existují významné rozdíly mezi plánování rozpočtu v aplikaci Microsoft DynamicsAX 2012 a Microsoft Dynamics 365 for Finance and Operations. Některé funkce nebyly upgradovány a proto vyžadují rekonfiguraci. Toto téma vysvětluje, co je nutné rekonfigurovat, a také popisuje nové funkce, které mají být brány v úvahu po dokončení upgradu.
author: ryansandness
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.custom: 272923
ms.assetid: 17cdfe74-bdfd-466a-9bdd-c12583f250c7
ms.search.region: Global
ms.author: ryansand
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 3d57419ca5c59be185c87b869302b41bef05a3c7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554489"
---
# <a name="upgrade-budget-planning"></a>Upgrade plánování rozpočtu

[!include [banner](../includes/banner.md)]

Existují významné rozdíly mezi plánování rozpočtu v aplikaci Microsoft DynamicsAX 2012 a Microsoft Dynamics 365 for Finance and Operations. Některé funkce nebyly upgradovány a proto vyžadují rekonfiguraci. Toto téma vysvětluje, co je nutné rekonfigurovat, a také popisuje nové funkce, které mají být brány v úvahu po dokončení upgradu.  

Plánování rozpočtu v aplikaci Microsoft Dynamics 365 for Finance and Operations obsahuje mnoho vylepšení, která nebyla k dispozici v aplikaci Microsoft Dynamics AX 2012. Toto téma vysvětluje změny, které musíte provést zákazníci, kteří upgradují. Rovněž zdůrazňuje nové funkce, které by měla být vzaty v úvahu při procesu upgradu. Z důvodu rozsahu změn nebude možné otevřít jakékoliv existující plány rozpočtu, dokud nebudou provedeny změny popsané v tomto tématu. Sestavy však budou fungovat a nebudou vyžadovat žádné změny.

## <a name="overview-of-changes"></a>Přehled změn
V modulu rozpočtování pro Finance and Operations bylo provedeno mnoho významných změn. Tyto změny mají za cíl usnadnit konfiguraci a opětovné použití plánování rozpočtu a snížit každoroční údržbu a nastavování. Následující oblasti z aplikace AX 2012 se již v aplikaci Finance and Operations nevyskytují:

-   Šablony plánu rozpočtu (konfigurace plánování rozpočtu)
-   Složky plánu rozpočtu (konfigurace plánování rozpočtu)
-   Omezení scénáře (konfigurace plánování rozpočtu)
-   Šablony pro pravidla fáze plánování rozpočtu a šablony (proces plánování rozpočtu)
-   Pole matice pro šablony listů
-   Průvodce šablonou plánu rozpočtu v aplikaci Microsoft Excel

Některé nové koncepty nelze upgradovat z předchozí funkce přímo. Proto je nutné dokončit některé rekonfigurace, aby bylo možné adresovat tyto nové koncepty. Následující části popisují koncepty, které nahradily položky v předcházejícím seznamu.

### <a name="columns"></a>Sloupce

Sloupce jsou nový koncept nahrazující části šablon aplikace Excel a také pole matic. Sloupce mohou představovat období, měsíc, čtvrtletí, nebo žádné časové omezení. Odkazy na čas jsou dynamické. Odkazují na relativní období nebo rok s odkazem na proces rozpočtu. Například sloupec **Předchozí rok leden** se vztahuje na fiskální období 1 pro rok -1. Sloupec je specifický pro scénář plánu rozpočtu, jako jsou například skutečné hodnoty nebo žádost o rozpočet.

### <a name="layouts"></a>Rozvržení

Rozvržení jsou nový koncept, který nahrazuje šablonu aplikace Excel. Rozvržení obsahují sloupce, které určují, jaký rozpočet nebo skutečné hodnoty a období se mají zobrazit. Rozvržení jsou též sdílena mezi klientem a doplňkem aplikace Excel. Díky tomu jsou možnosti uživatele při zadání nebo zobrazení dat v klientovi aplikace Finance and Operations lepší oproti aplikaci AX 2012. Pokud chcete zadat data do klienta aplikace Finance and Operations, nejste již omezeni na zobrazení a zadávání jediného scénáře do zobrazení transakcí. Místo toho vám zobrazení srovnání umožní snadno zobrazovat a zadávat částky pro vícero období a účtů současně. Rozvržení lze definovat také tak, že můžete zadat a zobrazit měny, komentáře a další volitelná data. Rozvržení vám rovněž umožní definovat, které dimenze hlavní knihy a popisy dimenze mají být zobrazeny. Rozvržení také zahrnuje omezení scénáře, která určují, jaké sloupce v šabloně lze upravovat a jaké sloupce by měly být k dispozici v aplikaci Excel. Po definování rozvržení se pro něj vytvoří šablona. Tato šablona pak vytvoří odpovídající šablonu aplikace Excel. Můžete potom upravovat šablonu aplikace Excel, abyste začlenili více vzorců a formátování, než ji znovu odešlete. Rozvržení poté budou přiřazena ke každému pravidlu fáze na stránce **Proces plánování rozpočtu**. Rozvržení tedy nahrazují šablony, které byly přiřazeny a použity podobným způsobem.

### <a name="budget-planning-processes"></a>Procesy plánování rozpočtu

Procesy plánování rozpočtu jsou převážně stejné jako v aplikaci AX 2012. Nejvýznamnější změnou je nahrazení šablon rozvrženími. Pokud byly v aplikaci AX 2012 dříve dokončeny jakékoliv procesy, budou tyto procesy aktualizovány na probíhající stav, aby bylo kožné provést změny. Je nutné přiřadit rozvržení potřebné pro každé pravidlo fáze k určení toho, jaké scénáře a časová období se zobrazí při otevření plán v klientovi. Rozvržení dále určují, jaké šablony aplikace Excel se otevřou mimo aplikaci Dynamic 365 for Finance and Operations, abyste mohli zobrazit rozpočet. **Výchozí účetní struktura** je nová povinné pole pro proces plánování rozpočtu. Pro každý proces plánování rozpočtu přiřaďte primární účetní strukturu, která má být použita pro rozpočtování.

### <a name="attachments"></a>Přílohy

V aplikaci AX 2012 byly ukládány dokumenty odůvodnění do složky přílohy. Žádný předchozí dokumenty odůvodnění nebudou upgradovány. Dokumenty odůvodnění se nyní ukládají do databáze. Pokud má být tato informace v upgradované verzi, můžete odeslat konečné dokumenty odůvodnění pro každý plán jako přílohu pomocí tlačítka **Odůvodnění** v podokně akcí. V aplikaci AX 2012 byly vytvořeny na základě šablony listy aplikace Excel pro každý plán rozpočtu. Všechny plány v aplikaci Finance and Operations otevřou kopii rozvržení. Žádné změny souboru aplikace Excel však nejsou uloženy. Jakékoliv vzorce nebo podpůrné informace, které byly použity na bázi podle plánu, musí být přidány prostřednictvím komentářů, dokumentu odůvodnění nebo nějakých jiných doplňkových procesů.

## <a name="configuring-an-upgraded-environment-from-ax-2012"></a>Konfigurace upgradovaného prostředí z aplikace AX 2012
Abychom vám pomohli určit, jak konfigurovat upgradovaný systém, použijeme v následujícím příkladu upgradovaný proces rozpočtu z ukázkových dat aplikace AX 2012. Pro pomoc s procesem upgradu byla vytvořena výchozí data konfigurace pro sloupce. Tato výchozí data můžete aktualizovat nebo odstranit, pokud nesplňují vaše požadavky na konfiguraci. **Poznámka:** Existují nová požadovaná pole, která nebudou v systému nastavena. Pokud uvíznete na stránce, jako je například stránka **Konfigurace plánování rozpočtu**, a nedaří se vám ji opustit, můžete zavřít svůj prohlížeč a znovu ho otevřít na jiné stránce pro zadání podrobností ve správném pořadí. Existují povinná pole, která nejsou dosud nastavena. Z toho vyplývá, že může dojít k problémům, dokud se vše nenakonfiguruje a nenastaví se všechna požadovaná pole. Toto téma vysvětluje postup nastavení těchto polích podle potřeby. Následuje několik požadovaných polí:

-   Stránka **Proces plánování rozpočtu**: Pole **Výchozí účetní struktura**
-   Stránka **Proces plánování rozpočtu**: Pole **Rozvržení** na pevné záložce **Pravidla a rozložení fáze plánování rozpočtu**

### <a name="define-columns-and-layouts"></a>Definování sloupců a rozvržení

1. Na stránce **Konfigurace plánování rozpočtu** klikněte na kartu **sloupce**. Jako součást upgradu se automaticky vytvoří nové sloupce na základě řádků plánu rozpočtu. Sloupce nyní používají dynamická data, kde čas a rok jsou vyrovnány od fiskálního roku, který je definován v procesu plánování rozpočtu. **Poznámka:** Z důvodů výkonnosti při upgradu se předpokládá, že všechny rozpočtové cykly představují kalendářní roky, nikoli fiskální roky. Používáte-li fiskální roky, je třeba provést úpravy pro správné namapování sloupců na jejich fiskální rok. Například v aplikaci AX 2012 existovaly následující prvky:
   -   Scénáře plánu rozpočtu: Skutečné hodnoty, Základ, Žádost o rozpočet, Rozpočet schválen
   -   Řádky plánu rozpočtu pro všechny scénáře v roce 2017 a skutečné hodnoty pro roky 2017 a 2016

   V aplikaci Finance and Operations budou vytvořeny následující sloupce:

   | Název sloupce    | Scénář plánu rozpočtu | Časové období sloupce | Posun roku |
   |----------------|----------------------|--------------------|-------------|
   | Led Scénář 1 | Skutečné hodnoty              | 1                  | 0           |
   | Led Scénář 2 | Základ             | 1                  | 0           |
   | Led Scénář 3 | Žádost o rozpočet       | 1                  | 0           |
   | Led Scénář 4 | Rozpočet schválen      | 1                  | 0           |
   | Led Scénář 5 | Skutečné hodnoty              | 1                  | -1          |
   | Únor Scénář 1 | Skutečné hodnoty              | 1                  | 0           |
   | ...            | ...                  | ...                | ...         |

   V tomto příkladu je vytvořen sloupec s názvem **Led Scénář 1** pro nejnovější data transakce plánu rozpočtu nalezená tam, kde existují transakce v lednu. Podobný sloupec je vytvořen pro každý scénář, který obsahuje data. Poté, co existují sloupce pro všechna období v tomto roce, vytvoří se sloupce za předchozí roky.
2. Změňte názvy sloupců a popisy a ostatní podrobnosti, buď ručně v klientovi nebo pomocí hromadné aktualizace prostřednictvím doplňku aplikace Excel odkazujícího na entitu dat sloupce plánu rozpočtu. Ve sloupcích jsou nyní nastaveny všechny filtry, které byly předtím nastaveny na pole matic.
3. Vytvořte nové rozvržení plánu rozpočtu. Rozvržení odkazuje na několik sloupců za účelem definice zobrazení, které s objeví v aplikaci Excel a klientovi. Rozvržení nejprve vyžaduje, abyste stanovili sadu dimenzi hlavní knihy a určili tak, které finanční dimenze lze zadat. Po zadání sady dimenzí klikněte na tlačítko **Popisy** a vyberte popisy dimenze, které chcete zahrnout do rozvržení.
4. Na pevné záložce **Elementy rozložení** klikněte na tlačítko **Přidat** a přidejte metadata pro každý řádek, jako je například měna, komentář nebo třída rozpočtu, která určuje řádky výnosů oproti výdajům. Dále přidejte sloupce pro časové období a scénáře, které se vztahují k tomuto rozpočtovému cyklu a fázi. Tyto změny můžete provést ručně v klientovi nebo prostřednictvím doplňku aplikace Excel, který odkazuje na entitu data prvků rozvržení plánu rozpočtu.
5. Pro každý prvek rozvržení vyberte, zda lze sloupec upravit a zda se má sloupec také zobrazit v sešitu aplikace Excel pro toto rozvržení. **Poznámka:** Pro naše historické plány můžete zvážit rozvržení zobrazující 12 měsíčních sloupců pro všechny scénáře plánu rozpočtu pro tento proces.

### <a name="update-budget-planning-processes-to-use-the-appropriate-layout-for-each-budget-stage"></a>Aktualizace procesů plánování rozpočtu za účelem použití odpovídajícího rozvržení pro každou fázi rozpočtu

1.  Na stránce **Proces plánování rozpočtu** vyberte proces, který chcete konfigurovat.
2.  V podokně akcí klikněte na tlačítko **Upravit**.
3.  Určete výchozí účetní strukturu pro tento proces rozpočtu. **Výchozí účetní struktura** je nové povinné pole, které je nutné nastavit.
4.  Na pevné záložce **Pravidla a rozložení fáze plánování rozpočtu** v poli **Rozvržení** vyberte rozvržení, které bylo dříve nakonfigurováno a které je příslušné pro tuto fázi.
5.  Pokračujte výběrem stejného nebo odlišného rozvržení pro různé fáze plánování rozpočtu a poté uložte provedené změny.

## <a name="additional-features-to-consider-in-your-budgeting-process"></a>Další funkce ke zvážení při procesu rozpočtu
### <a name="budget-planning-workspace"></a>Pracovní prostor plánování rozpočtu

Tento pracovní prostor je určen jak pro vlastníka rozpočtu, tak pro jednotlivé přispěvatele rozpočtu. Obsahuje odkazy na všechny dokumenty rozpočtu, které vyžadují vaši pozornost. Obsahuje také sestavy a klíčové indikátory výkonnosti (KPI) pro proces rozpočtu. Správce rozpočtu může definovat aktuální proces plánování rozpočtu pro všechny uživatele na stránce **Parametry rozpočtování**. Na kartě **Nastavení pracovního prostoru** obsahuje pevná záložka **Plánování rozpočtu** pole, kde si můžete vybrat proces plánování rozpočtu.

### <a name="alternate-layouts"></a>Alternativní rozvržení

Alternativní rozvržení jsou novou funkcí, které vám umožní zobrazit plány v různých rozvrženích. Lze vytvořit jedno či více rozvržení jako možnosti. Poté můžete zobrazit plán rozpočtu v měsíčním nebo čtvrtletním rozvržení. Alternativní rozložení určujete na rychlé záložce **Pravidla a rozložení fáze plánování rozpočtu** na stránce **Proces plánování rozpočtu**.

### <a name="budget-milestones"></a>Milníky rozpočtu

Jako součást procesu rozpočtu je důležité, abyste rozuměli klíčovým datům a termínům. Nyní můžete nakonfigurovat data tak, aby měla své popisy. Uživatelé pracující na rozpočtu uvidí tyto popisy, když otevřou rozpočet za účelem oprav nebo zobrazení čehokoliv, co je jim přiřazeno.

### <a name="copy-from-budget-plan-allocation"></a>Kopírování z přidělení plánu rozpočtu

Nová metoda přidělení vám umožňuje distribuovat z nadřazeného plánu do podřízeného plánu, aniž byste museli procházet přechodnými úrovněmi hierarchie. Tato metoda je užitečné zejména pro zákazníky, kteří dříve vytvořili finanční dimenze pouze pro rozdělení rozpočtu a schválení.

### <a name="generating-budget-plans-from-new-budget-sources"></a>Generování plánů rozpočtu z nových zdrojů rozpočtu

Jako periodické procesy byly přidány následující možnosti. Tyto možnosti umožňují generovat plán rozpočtu pomocí existujících dat z jiného modulu jako výchozího bodu:

-   Generování plánu rozpočtu z prognózy poptávky
-   Generování plánu rozpočtu z prognózy dodávek
-   Generování plánu rozpočtu z projektu
-   Generování plánu rozpočtu z registru rozpočtu

### <a name="more-complete-tracking-of-amounts"></a>Podrobnější sledování částek

V aplikaci AX 2012 mělo plánování rozpočtu jednu částku plánu, která byla uložena pro každou hodnotu. V aplikaci Finance and Operations byl datový model rozšířen. Nyní existují částky zúčtovací měny, měny transakce a měny vykazování pro každou hodnotu. Během upgradu se tyto nové sloupce automaticky vyplní pro existující data.

### <a name="do-not-convert-currency-in-aggregation"></a>Nepřevádět měnu v seskupení

Obvykle když je podřízený plán agregovaný k nadřazené úrovni, částky budou automaticky převedeny z měny transakce na zúčtovací měnu pro organizaci. Když nastavíte možnost **Nepřevádět měnu v seskupení** na **Ne**, zůstanou souhrnné částky v původní měně. Tato možnost umožňuje tedy přesnější úpravy, které jsou ovlivněny výkyvy směnného kursu.

### <a name="looking-back-from-a-budget-plan-to-other-modules-that-contributed-to-the-budget"></a>Zpětné hledání z plánu rozpočtu do jiných modulů, které tvoří část rozpočtu

Plány rozpočtu lze vygenerovat z prognóz poptávek nebo dodávek, projektu a dalších oblastí. Dotaz Plány rozpočtu podle sad dimenzí obsahuje několik možností, které umožňují spuštění dotazů pro určení dat, která byla zdrojem pro plán rozpočtu.

### <a name="overwrite-or-append-to-plan-for-allocation-schedules"></a>Přepsání nebo připojení k plánu pro plánování přidělení

Pokud existuje více zdrojů částek, které musí být distribuovány, můžete určit, že částky mají být přídavné. V takovém případě částky nepřepíšou stávající částky. Místo toho jsou připojeny k existujícím částkám.

### <a name="default-financial-dimension-set-for-budget-planning-configuration"></a>Výchozí sada finančních dimenzí pro konfiguraci plánování rozpočtu

Stránka **Konfigurace plánování rozpočtu** nyní obsahuje pole, kde můžete zadat výchozí sadu finančních dimenzí. Ačkoliv je toto pole volitelné, může být vyžadováno pro některé dotazy. Může být rovněž vyžadováno, pokud chcete seskupit nebo filtrovat seskupení sestav podle sady dimenzí.

### <a name="data-entities"></a>Datové entity

Bylo přidáno několik datových entit, aby bylo možné rychle implementovat plánování rozpočtu. Entity vám rovněž umožní provádět změny prostřednictvím aplikace Excel. Nemusíte tedy vytvářet prostřednictvím klienta po jedné. Zde je uveden seznam nových datových entit:

-   Název entity
-   Parametry rozpočtu
-   Parametr plánu rozpočtu
-   Scénáře plánu rozpočtu
-   Fáze plánu rozpočtu
-   Fáze workflowu plánu rozpočtu
-   Plánování přidělení plánu rozpočtu
-   Přidělení fází plánování rozpočtu
-   Priority plánu rozpočtu
-   Sloupce plánu rozpočtu
-   Prvky rozložení plánu rozpočtu




