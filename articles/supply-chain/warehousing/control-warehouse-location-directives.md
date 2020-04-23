---
title: Řízení práce ve skladu pomocí šablon práce a směrnic skladového místa
description: Toto téma popisuje způsob použití šablon práce a směrnic skladového místa k určení, jak a kde se práce ve skladu provádí.
author: perlynne
manager: tfehr
ms.date: 02/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aae57af04be8bcc6da2e5635b5ffa96d9fac147c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205729"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Řízení práce ve skladu pomocí šablon práce a směrnic skladového místa

[!include [banner](../includes/banner.md)]

Toto téma popisuje způsob použití šablon práce a směrnic skladového místa k určení, jak a kde se práce ve skladu provádí.

Pokyny, které pracovníci skladu obdrží v mobilním zařízení, jsou určeny podle šablon práce, které nastavíte v aplikaci Dynamics 365 Supply Chain Management k definování různých procesů a úloh ve skladu. Šablony práce určují způsob provedení práce pro každý skladový proces. Přiřazením směrnic skladového místa k šablonám práce můžete pomoci zajistit, že práce bude probíhat v určitých fyzických oblastech skladu.

## <a name="work-templates"></a>Šablony práce
Stránka **Šablony práce** umožňují definovat pracovní operace, které musí být provedeny ve skladu. Obvykle pracovní operace ve skladu sestávají z páru akcí: skladoví pracovníci vyskladní zásoby na skladě na jednom místě a převedou vyskladněné zásoby v jiném skladovém místě. 

Šablony práce obsahují záhlaví a související řádky. Každá šablona práce je pro určitý *typ pořadí pracovních činností*. Mnohé typy pracovních činností jsou přidruženy ke zdrojovým dokumentům, jako je nákupní nebo prodejní objednávka. Ostatní typy pořadí pracovních činností však představují samostatné procesy skladu, jako je například cyklická inventura. *ID fondů práce* umožňuje uspořádat práci do skupin. 

Nastavení v definici záhlaví práce dokáže určit, kdy mají být vytvořeny nové části práce. Můžete například nastavit maximální počet řádků vyskladnění a maximální očekávaný čas vyskladnění. Poté pokud práce pro výdej prodejní objednávky překročí některé z těchto hodnot, práce je rozdělena do dvou pracovních částí. 

Řádky práce představují fyzické úkoly, které jsou požadovány pro zpracování práce. Například pro proces výstupního skladu může existovat řádek práce pro vyzvednutí položek v rámci skladu, a jeden řádek pro uložení těchto položek do přípravné oblasti. Poté může existovat další řádek pro výdej položek z fázování a jiný řádek pro vkládání položek do nákladního automobilu v rámci procesu nakládání. Podle potřeby můžete nastavit *kód předpisu* na řádcích šablony práce. Kód předpisu je propojen s předpisem pro skladové místo a proto pomáhá zaručí, že je skladová práce zpracována na správném místě ve skladu. 

Můžete určit dotaz pro řízení toho, kdy dojde k použití určité šablony práce. Můžete například nastavit omezení, aby určitá šablona mohla být použita pouze pro určitý sklad. Alternativně můžete mít více šablon, které se používají k vytvoření práce pro zpracování odchozí prodejní objednávky v závislosti na původu prodeje. Systém používá pole **Pořadové číslo** k určení pořadí, ve kterém jsou posuzovány šablony práce. Proto pokud máte velmi konkrétní dotaz na určitou šablonu práce, měli byste jí zadat nízké pořadové číslo. Tento dotaz bude poté vyhodnocen před ostatními obecnějšími dotazy. 

Pokud chcete zastavit nebo pozastavit proces práce, můžete vybrat nastavení **Zastavit práci** na řádku práce. Pracovník, který provádí práci, v tomto případě nebude požádán o provedení dalšího kroku práce. Pokud se chcete přesunout na další krok, je třeba, aby tento nebo jiný pracovník práci znovu vybral. Můžete také oddělit úlohy v rámci práce pomocí jiného *ID třídy práce* na řádcích šablony práce.

## <a name="location-directives"></a>Směrnice skladového místa
Směrnice skladového místa jsou pravidla, která pomáhají identifikovat místa vyskladnění a umístění pro pohyb zásob. V transakce prodejní objednávky například směrnice skladového místa určuje, které zboží bude vydáno a kam bude umístěno. Směrnice skladového místa se skládají ze záhlaví a souvisejících řádků, a jejich vytvoření je možné na stránce **Směrnice skladového místa**. 

Záhlaví každé směrnice skladového místa musí být přidruženo k *typu pořadí pracovních činností*, který určuje typ skladové transakce, pro kterou bude použita směrnice, jako například prodejní objednávky, doplnění nebo výdej surovin. *Typ práce* určuje, zda se směrnice skladového místa použije pro výdej nebo vložení práce, nebo pro některé další skladové procesy, jako například inventuru nebo změny stavu zásob. Je třeba zadat *pracoviště* a *sklad*. *Kód předpisu*, který určíte v záhlaví, slouží k propojení směrnice skladového místa k jedné nebo více šablonám práce. 

Pro šablony práce lze nastavit dotaz, který určuje, kdy je použita konkrétní směrnice skladového místa. Můžete například určit, že pokud má elektronická objednávka původ v prodejní objednávce, zásoby musí být vyskladněny z vyhrazené místo ve skladu. Systém používá pole **Pořadové číslo** k určení pořadí, ve kterém jsou posuzovány směrnice pro dostupné místo. 

Řádky směrnice umístění stanoví další omezení aplikace pravidel hledání místa. Můžete zadat minimální a maximální množství, na které má být směrnice použita, a můžete určit, zda bude směrnice použita pouze pro specifickou skladovou jednotku. Například pokud je měrná jednotka palety, zboží v paletách může být vložit na určité skladové místo. Můžete také určit, zda lze množství rozdělit na více umístění. Stejně jako záhlaví směrnic skladového místa má každý řádek směrnice místa pořadové číslo určující pořadí, ve kterém jsou řádky posuzovány. 

Směrnice skladového místa mají další úroveň podrobností: *akce směrnice skladového místa*. Můžete určit více akcí směrnice skladového místa pro každý řádek. Pořadové číslo se znovu použije k určení pořadí, ve kterém jsou akce posuzovány. Na této úrovni můžete nastavit dotaz a definovat tak způsob vyhledání nejlepšího skladového místa ve skladu. Také můžete použít předdefinované nastavení **Strategie** a najít tak optimální skladové místo.

## <a name="location-directives-configuration-details"></a>Podrobnosti konfigurace směrnic skladového místa 

 ### <a name="sequence-number"></a>Pořadové číslo
 
Toto číslo označuje pořadí, ve kterém je zpracována směrnice skladového místa pro vybraný typ objednávky. Je možné ho změnit pomocí možností **Přesunout nahoru** a **Přesunout dolů** v nabídce.
 
 ### <a name="work-type"></a>Typ práce
 
Jedná se o typ práce, která má být vykonávána. Typ práce, který je k dispozici, závisí na typu skladové transakce, který jste vybrali v poli **Typ pracovního příkazu**.
-   **Vložit** - Typ práce **Vložit** znamená, že směrnice skladového místa najde nejvhodnější skladové místo pro umístění zásob přicházejících do systému, buď z přijetí, výroby nebo úprav zásob. Lze ho také použít k definování umístění do místa fáze nebo konečného místa expedice nákladové brány.
-   **Vyskladnit** - Typ práce **Vyskladnit** znamená, že sklad nalezne nejvhodnější skladové místo, odkud fyzicky rezervovat zásoby (vytvoření práce). Vyskladnění lze dokončit (řádek práce vyskladnění lze uzavřít), i když práce není dokončena. Uživatele může dokončit fyzické vyskladnění, což je krok vyskladnění. Uživatel poté může provést zrušení z mobilního zařízení a dokončit práci později. Záhlaví práce je však uzavřeno, když je dokončeno koncové vložení. 
-   **Inventura, Úpravy, Vlastní, Změna stavu zásob, Sestavení registrační značky vozidla, Tisk, Změna stavu, Zabalit do vnořených registračních značek** - Tyto možnosti se nepoužívají v žádném nastavení směrnic skladového místa. Jedná se o výčet, takže neexistuje žádné filtrování připojené k typu pracovního příkazu. 

### <a name="directive-code"></a>Kód předpisu

Vyberte kód předpisu, který se má přidružit k šabloně práce nebo šabloně doplnění. Ve formuláři **Kód směrnice** můžete vytvořit nové kódy, které lze použít pro propojení mezi šablonou práce, šablonou doplnění a směrnicí skladového místa. Tuto možnost můžete také použít pro vytvoření spojení mezi jakýmkoliv řádkem šablony práce a směrnicí skladového místa (jako je například nákladová brána nebo skladové místo fáze).

Všimněte si, že pokud je nastaven kód při generování práce, systém nebude hledat směrnici skladového místa podle posloupnosti, nýbrž podle kódu směrnice. To znamená, že můžete být konkrétnější v použití typu šablony skladového místa pro určitý krok v šabloně práce, jako je například fázování materiálů. 

### <a name="site"></a>Pracoviště

Pracoviště je povinné pole, protože směrnice skladového místa vyžaduje pracoviště a sklad, pro které je platná. 

### <a name="warehouse"></a>Sklad

Sklad je povinné pole, protože směrnice skladového místa vyžaduje pracoviště a sklad, pro které je platná.

### <a name="multiple-sku"></a>Více skladových jednotek

To umožňuje více skladových jednotek (SKU) ve skladovém místě, jako je například nákladová brána. Vyberete-li **Více skladových jednotek**, skladové místo pro vložení bude určeno v práci (což je očekávané), ale bude možné pracovat pouze s vložením vícero položek (pokud práce zahrnuje rozdílné skladové jednotky k vyskladnění a vložení, nikoliv jedno vložení skladové jednotky). Nevyberete-li **Více skladových jednotek**, skladové místo pro vložení bude určeno pouze tehdy, pokud má vložení pouze jeden druh skladové jednotky. Pokud chcete použít obě akce, je nutné zadat dva řádky - jeden s povolenou možností více skladových jednotek a jeden se zakázanou možností více skladových jednotek. Tyto řádky musí mít stejnou strukturu a nastavení. Pro operace vložení je nutné mít směrnice skladového místa, které jsou identické, i když nerozlišujete mezi jednou a vícero skladovými jednotkami u ID práce. Rovněž je třeba nastavit vyskladnění, pokud máte objednávky s více než jednou položkou.

### <a name="sequence-number"></a>Pořadové číslo

Zadejte pořadí, ve kterém jsou zpracovány řádky předpisu skladového místa pro vybraný typ práce. Můžete také změnit pořadí v případě potřeby pomocí položek **Přesunout nahoru** a **Přesunout dolů**.

### <a name="fromto-quantity"></a>Množství od/do

Umožňuje určit rozsah množství pro případ, kdy je třeba zvolit pořadí střední mřížky. Určit rozsah množství od/do můžete v možnosti Množství v příslušné jednotce.

### <a name="unit"></a>Jednotka

Můžete zadat minimální a maximální množství, na které má být směrnice použita, a můžete určit, zda bude směrnice použita pouze pro specifickou skladovou jednotku. Pole jednotky na řádku se používá pouze pro vyhodnocení množství.

Při kontrole, zda je použitelný řádek směrnice skladového místa, bude založeno na množství v příslušné jednotce zadané na řádku směrnice skladového místa. Vždy, když je dosaženo řádku směrnice skladového místa, systém se pokusí o převod jednotky poptávky na jednotku zadanou na řádku. Pokud měrná jednotka neexistuje, bude pokračovat na další řádek. 

### <a name="locate-quantity"></a>Vyhledat množství

Tato možnost slouží pouze pro vložení/vyhledání množství do skladu. Slouží pouze k typu práce vložení. Platné hodnoty jsou:

-   **Množství registrační značky** – Při vyhodnocení, zda je množství v rámci rozsahů množství Od a Do, použijte množství na přijímané registrační značce.
-   **Sjednocené množství** – Při vyhodnocení, zda je množství v rámci rozsahů množství Od a Do, použijte množství sjednocované během konkrétní transakce.
-   **Zbývající množství** – Při vyhodnocení, zda je množství v rámci rozsahů množství Od a Do, použijte množství, které zbývá přijmout na řádku nákupní objednávky aktuálně vráceném se změnami.
-   **Očekávané množství** – Při vyhodnocení, zda je množství v rámci rozsahů množství Od a Do, použijte celkové množství řádku nákupní objednávky bez ohledu na to, co již bylo přijato.

### <a name="restrict-by-unit"></a>Omezit podle jednotky

To umožňuje, aby byl řádek směrnice skladového místa konkrétně určen pro měrnou jednotku nebo více měrných jednotek. Při rezervaci množství, pokud chcete rezervovat palety pro určitou skupinu skladových míst, pak by pořadí střední mřížky omezilo tuto konkrétní posloupnost na PL tak, aby jakékoliv množství menší než jedna paleta nevybralo tuto číselnou řadu. Vyberte **Omezit podle jednotky** pro nastavení jednotek. Řádek můžete také omezit na více než jednu jednotku. Tato bude fungovat pouze pro směrnici skladového místa typu vyskladnění. 

### <a name="round-up-to-unit"></a>Zaokrouhlit nahoru na jednotku

Toto políčko souvisí s polem **Omezit podle jednotky**. Pokud je řádek směrnice skladového místa **Omezit podle jednotky** nastaven na pole, volba **Zaokrouhlit nahoru na jednotku** označuje, že práce vygenerovaná ze směrnice pro výdej suroviny musí být zaokrouhlena nahoru na násobek jedné manipulační jednotky (zadané v možnosti **Omezit podle jednotky**). Všimněte si, že to funguje pouze pro výdej suroviny a pouze se směrnicí skladového místa typu výdej.

### <a name="locate-packing-qty"></a>Vyhledat množství balení

Pokud je na prodejní objednávce , převodním příkazu nebo výrobní zakázce určeno množství balení, omezuje to systém pouze k výběru skladových míst s množstvím balení ve skladovém místě. Tato bude fungovat pouze pro směrnici skladového místa typu vyskladnění.

### <a name="allow-split"></a>Povolit rozdělení

To určuje, zda smí směrnice skladového místa rozdělit přijaté množství nebo množství, které je rezervováno napříč vícero místy skladu, nebo zda celé množství musí být umístěno na jedno místo nebo rezervováno z jediného místa za účelem vytvoření práce. 

### <a name="sequence-number"></a>Pořadové číslo

Toto číslo je pořadí, ve kterém je zpracována směrnice skladového místa pro vybraný typ práce. Pořadí můžete v případě potřeby změnit. Nicméně buďte opatrní při použití číselných řad, protože zpracování se vždy spustí podle pořadí. 

### <a name="name"></a>Jméno

Zadejte název akce směrnice skladového místa. Ujistěte se, že při určení názvu budete konkrétní.

### <a name="fixed-location-usage"></a>Využití pevného skladového místa 

-   **Pevná a ostatní skladová místa** - Tato směrnice skladového místa zváží všechna skladová místa.
-   **Pouze pevná skladová místa pro produkt** – Směrnice skladového míst zváží pouze pevná skladová místa pro produkt.
-   **Pouze pevná skladová místa pro variantu produktu** – Směrnice skladového míst zváží pouze pevná skladová místa pro variantu produktu.

### <a name="allow-negative-inventory"></a>Povolit záporné zásoby

Výběrem této možnosti můžete v zadaném skladovém umístění povolit záporné počty zásob ve směrnici skladového místa. 

### <a name="batch-enabled"></a>Dávka povolena 

Zvolte použití strategií dávek pro položky, které mají povolenou dávku. Pokud je dosaženo řádku, kde je možnost **Dávka povolena** nastavena bez položky dávky, zpracování bude pokračovat k dalšímu řádku akce. 

### <a name="strategy"></a>Strategie

-   **Konsolidovat** - Tato strategie se používá pro konsolidaci položek v konkrétním skladovém místě, když jsou podobné položky již k dispozici. Tato operace funguje pouze pro typ vložení směrnic skladového místa. Běžné nastavení pro vložení bude konsolidace na prvním řádku akce a poté na druhém řádku pokus o vložení bez konsolidace. Konsolidace zboží bude mít za následek efektivnější pozdější vyskladnění.
-   **Párování množství balení** – Tato strategie vyhledá skladové místo obsahující registrační značku, která má požadované množství. Nelze jej použít s umístěními, která nejsou řízena registrační značkou. Tato strategie funguje pouze pro směrnici skladového místa typu práce vyskladnění.
-   **Rezervace dávky FEFO** - Tato strategie se používá, když se zásoby vyhledávají pomocí data vypršení platnosti dávky a jsou přiděleny pro rezervaci dávek. Tato strategie se dá použít pouze pro položky s povolenou dávkou. Tato operace funguje pouze pro směrnici skladového místa typu práce vyskladnění. 
-   **Zaokrouhlit nahoru na úplnou registrační značku** - Tato strategie umožňuje zaokrouhlování skladového množství, aby odpovídalo množství registrační značky přiřazenému ke zboží k výdeji. Tuto strategii můžete použít pouze pro typ doplnění směrnice skladového místa typu Vyskladnění. 
-   **Prázdné místo bez příchozí práce** - Tato strategie slouží k vyhledání prázdných míst. Sklad je považován za prázdný, pokud nemá žádné fyzických zásoby a neočekává příchozí práci. Tato strategie slouží pouze pro typ směrnice skladového místa Vložení. 

### <a name="example-of-the-use-of-location-directives"></a>Příklad použití směrnic skladového místa

V tomto příkladu zvažte proces nákupní objednávky, kde směrnice skladového místa musí vyhledat volnou kapacitu ve skladu pro skladové položky, které byly právě zaregistrovány na přijímacím překladišti. Nejprve potřebujete vyhledat volnou kapacitu v rámci skladu konsolidací s existujícími zásobami na skladě. Není-li konsolidace možná, pak musíte najít prázdné skladové místo. 

Pro tento scénář musíte definovat dvě akce směrnice skladového místa. První akce v číselné řadě musí používat strategii **Konsolidovat** a druhá strategii **Prázdné umístění s žádnou příchozí prací**. Pokud definujete třetí akci pro zpracování scénáře přetečení, jsou možné dva výsledky v případě, že neexistuje žádná další kapacita ve skladu: práci lze vytvořit i v případě, že jsou definována žádná skladová místa, nebo může proces vytváření práce selhat. Výsledek je určen nastavením na stránce **Selhání směrnice skladového místa**, kde můžete rozhodnout, zda chcete vybrat možnost **Zastavit práci při selhání směrnice umístění** pro každý typ pořadí pracovních činností.
