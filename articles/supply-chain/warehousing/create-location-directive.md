---
title: Práce se směrnicemi skladového místa
description: Toto téma popisuje, jak pracovat se směrnicemi skladového místa. Směrnice skladového místa jsou pravidla definovaná uživatelem, která pomáhají identifikovat místa vyskladnění a umístění pro pohyb zásob.
author: Mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-11-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b1b3bafb24ff6eb0c42d901fac3b6668cedf39ef
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963303"
---
# <a name="work-with-location-directives"></a>Práce se směrnicemi skladového místa

[!include [banner](../includes/banner.md)]

Směrnice skladového místa jsou pravidla, která pomáhají identifikovat místa vyskladnění a umístění pro pohyb zásob. V transakce prodejní objednávky například směrnice skladového místa určuje, které zboží bude vydáno a kam bude umístěno. Směrnice skladového místa se skládají z hlavičky a přidružených řádků. Jsou vytvořeny pro konkrétní *typy pracovních příkazů*.

> [!NOTE]
> V tomto tématu se týká funkcí v modulu **Správa skladu**. Nevztahuje se na funkce v modulu [Řízení zásob](../inventory/inventory-home-page.md).

Směrnice skladového místa lze použít k následujícím úkolům:

- Odložení příchozích položek.
- Vyskladnění a umístění zboží pro výstupní transakce.
- Vyskladnění a vložení surovin do výroby.
- Doplnění skladových míst.

## <a name="prerequisites"></a>Předpoklady

Než budete moci vytvořit směrnici o umístění, musíte se ujistit, že jsou splněny všechny požadované podmínky.

1. Zkontrolujte, zda je zapnutý požadovaný licenční klíč. Přejděte na **Správa systému \> Nastavení \> Konfigurace licence**, rozbalte licenční klíč **Obchod** a vyberte konfigurační klíč **Správa skladu a dopravy**. U tohoto kroku je vyžadován přístup správce.
1. Přejděte na **Řízení skladu \> Nastavení \> Sklad \> Sklady**.
1. Vytvoření skladu.
1. Na záložce **Sklady** nastavte možnost **Použít procesy správy skladu** na *Ano*.
1. Vytvoření skladových míst, typů skladových míst, profilů skladových míst a formátů skladového místa. Další informace viz [Konfigurace umístění ve skladu podporujícím WMS](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).
1. Vytvoření pracovišť, zón a skupin zón. Další informace viz [Nastavení skladu](https://docs.microsoft.com/dynamics365/commerce/channels-setup-warehouse) a [Konfigurace umístění ve skladu podporujícím WMS](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).

## <a name="work-order-types-for-location-directives"></a>Typy pracovních příkazů pro směrnice skladového místa

Mnoho polí, která lze nastavit pro směrnice skladového místa, je společných pro všechny typy pracovních příkazů. Ostatní pole jsou však specifická pro konkrétní typy pracovních příkazů.

![Typy pracovních příkazů pro směrnice skladového místa](media/Location_Directives_Work_Order_Types.png "Typy pracovních příkazů pro směrnice skladového místa")

> [!NOTE]
> Dva typy pracovních příkazů, *Zrušená práce* a *Počítání cyklů*, jsou používány pouze systémem. Pro tyto typy pracovních příkazů nelze vytvořit směrnice skladového místa.

V tabulkách v následujících podsekcích je uveden seznam polí specifických pro běžné a pracovní příkazy, které jsou k dispozici při nastavení směrnice skladového místa.

### <a name="fields-that-are-common-to-all-work-order-types"></a>Pole, která jsou společná pro všechny typy pracovních příkazů

V následující tabulce jsou uvedena pole, která jsou společná pro všechny typy pracovních příkazů.

| Pevná záložka | Pole |
|---|---|
| Směrnice skladového místa | Typ práce |
| Směrnice skladového místa | Lokalita |
| Směrnice skladového místa | Sklad |
| Směrnice skladového místa | Kód předpisu |
| Směrnice skladového místa | Více skladových jednotek |
| Řádky | Pořadové číslo |
| Řádky | Od množství |
| Řádky | Do množství |
| Řádky | Jednotka |
| Řádky | Vyhledat množství |
| Řádky | Omezit podle jednotky |
| Řádky | Zaokrouhlit nahoru na jednotku |
| Řádky | Vyhledat množství balení |
| Řádky | Povolit rozdělení |
| Akce směrnice skladového místa | Pořadové číslo |
| Akce směrnice skladového místa | Jméno |
| Akce směrnice skladového místa | Využití pevného skladového místa |
| Akce směrnice skladového místa | Povolit záporné zásoby |
| Akce směrnice skladového místa | Dávka povolena |
| Akce směrnice skladového místa | Strategie |

### <a name="fields-that-are-specific-to-work-order-types"></a><a name="fields-specific-types"></a>Pole, která jsou specifická pro určité typy pracovních příkazů

V následující tabulce jsou uvedena pole, která jsou specifická pro konkrétní typy pracovních příkazů.

| Pevná záložka | Pole | Typ pracovního příkazu |
|---|---|---|
| Směrnice skladového místa | Umísťovat podle | Nákupní objednávky |
| Směrnice skladového místa | Použitelný dispoziční kód | Nákupní objednávky |
| Směrnice skladového místa | Dispoziční kód | Nákupní objednávky |
| Směrnice skladového místa | Použitelný dispoziční kód | Výdej dokončeného zboží |
| Směrnice skladového místa | Dispoziční kód | Výdej dokončeného zboží |
| Směrnice skladového místa | Použitelný dispoziční kód | Vratky |
| Směrnice skladového místa | Dispoziční kód | Vratky |
| Směrnice skladového místa | Použitelný dispoziční kód | Kanban – odložení |
| Směrnice skladového místa | Použitelný dispoziční kód | Kanban – výdej |
| Řádky | Šablona okamžitého doplnění | Prodejní objednávky |
| Řádky | Šablona okamžitého doplnění | Výdej suroviny |
| Řádky | Šablona okamžitého doplnění | Vydání převodního příkazu |
| Řádky | Šablona okamžitého doplnění | Kanban – výdej |

## <a name="open-the-location-directives-page"></a>Otevřete stránku Směrnice skladového místa

Pokud chcete otevřít stránku **Směrnice skladového místa**, přejděte na **Řízení skladu \> Nastavení \> Směrnice skladových míst**.

Odtud můžete zobrazit, vytvořit a upravit směrnice skladového místa pomocí příkazů v podokně akcí. V ostatních částech tohoto tématu najdete informace o tom, jak používat všechna pole, která jsou na stránce k dispozici.

## <a name="action-pane"></a>Podokno akcí

Podokno akcí na stránce **Směrnice skladového místa** obsahuje tlačítka, která můžete použít k vytváření, úpravám a mazání směrnic (**Upravit**, **Nový** a **Odstranit**). Obsahuje také následující tlačítka, která umožňují upravit pořadí zpracování směrnice skladového místa a konfigurovat dotaz, který definuje kritéria pro použití směrnice skladového místa:

- **Posunout nahoru** - Přesune vybranou směrnici skladového místa nahoru v pořadí. Můžete jej například přesunout ze sekvence číslo 4 do sekvence číslo 3.
- **Posunout dolů** - Přesune vybranou směrnici skladového místa dolů v pořadí. Můžete jej například přesunout ze sekvence číslo 4 do sekvence číslo 5.
- **Upravit dotaz** - Otevře dialogové okno, kde můžete definovat podmínky, za kterých má být vybraná směrnice skladového místa zpracována. Můžete například chtít, aby platila pouze pro konkrétní sklad.

## <a name="location-directives-header"></a>Záhlaví směrnic skladového místa

Záhlaví směrnice skladového místa obsahuje následující pole pro pořadové číslo a popisný název směrnice skladového místa:

- **Pořadové číslo** - Toto pole označuje sekvenci, ve které se systém pokusí použít každou směrnice skladového místa pro vybraný typ pracovního příkazu. Nejprve se použijí nízká čísla. Pořadí můžete změnit pomocí tlačítek **Posunout nahoru** a **Posunout dolů** v podokně akcí.
- **Název** - zadejte popisný název směrnice skladového místa. Tento název by měl pomoci identifikovat obecný účel směrnice. Například zadejte *Vychystávání zakázky odběratele ve skladu 24*.

## <a name="location-directives-fasttab"></a>Pevná záložka Směrnice skladového místa

Pole na pevné záložce **Směrnice skladového místa** jsou specifické pro typ pracovního příkazu, který je vybrán v poli **Typ pracovního příkazu** v podokně seznamu.

- **Typ práce** – Vyberte typ práce, která musí být provedena. Dostupné hodnoty záleží závisí na typu skladové transakce, který jste vybrali v poli **Typ pracovního příkazu**. Vyberte jednu z následujících hodnot:

    - **Vložit** - Směrnice skladového místa se pokusí najít nejideálnější umístění pro vložení inventáře, který přichází do systému, prostřednictvím příjmu, výroby nebo úprav inventury. Lze ho také použít k definování umístění do místa fáze nebo konečného místa expedice nákladové brány.
    - **vybrat** - Směrnice skladového místa se pokusí najít nejideálnější umístění, ze kterých lze fyzicky rezervovat inventář (tj. vytvořit pracovní příkaz). Vyskladnění lze dokončit (řádek práce vyskladnění lze uzavřít), i když práce není dokončena. Uživatel může dokončit fyzické vyskladnění. V systému je tato akce krokem k vyzvednutí. Uživatel poté může provést zrušení z mobilního zařízení a dokončit práci později. Záhlaví práce je však napřed uzavřeno, když je dokončeno koncové vložení.

    > [!IMPORTANT]
    > Ostatní hodnoty v poli **Typ práce** nejsou relevantní pro směrnice skladového místa. Zobrazují se pouze proto, že pole není filtrováno tak, aby odpovídalo vybranému typu pracovního příkazu.

- **Pracoviště** - Toto pole je povinné, protože směrnice skladového místa musí být schopna určit pracoviště a sklad, pro které je platná.
- **Sklad** - Toto pole je povinné, protože směrnice skladového místa musí být schopna určit pracoviště a sklad, pro které je platná.
- **Kód směrnice** – Vyberte kód směrnice, který se má přidružit k šabloně práce nebo šabloně doplnění. Na stránce **Směrnice** můžete vytvořit nové kódy, které lze použít k připojení pracovních šablon nebo šablon doplnění ke směrnicím skladového místa. Kódy směrnice lze také použít k vytvoření spojení mezi jakýmkoliv řádkem šablony práce a směrnicí skladového místa (jako je například nákladová brána nebo skladové místo fáze).

    > [!TIP]
    > Pokud je nastaven kód směrnice, systém nebude hledat směrnice skladového místa podle pořadového čísla, když musí být generovaná práce. Místo toho bude vyhledávat podle kódu směrnice. To znamená, že můžete být konkrétnější v použití typu šablony skladového místa pro konkrétní krok v šabloně práce, jako je například krok pro fázování materiálů.

- **Více SKU** – Nastavte tuto možnost na *Ano*, chcete-li povolit použití více skladových jednotek (SKU) v jednom skladovém místě. Například pro umístění křídlových dveří musí být povoleno více SKU. Pokud povolíte více SKU, bude vaše skladové místo pro vložení uvedeno v práci dle očekávání. Skladové místo však bude schopno zpracovat pouze vložení více položek (pokud práce zahrnuje různé SKU, které je třeba vybrat a umístit). Nezvládne vložení jedné SKU. Pokud nastavíte tuto možnost na *Ne*, skladové místo bude specifikováno pouze v případě, že vložení má pouze jeden druh SKU.

    > [!IMPORTANT]
    > Abyste mohli provádět vícepolohové i jednopolohové vnoření, musíte zadat dva řádky, které mají stejnou strukturu a nastavení, ale musíte nastavit možnost **Vícenásobná SKU** na *Ano* pro jeden řádek a *Ne* pro druhý. Pro operace vložení je proto nutné mít dvě stejné směrnice skladového místa, i když nerozlišujete mezi jednou a vícero skladovými jednotkami u ID práce. Často platí, že pokud nenastavíte obě tyto směrnice skladového místa umístění, neočekávaná umístění obchodních procesů budou pocházet z použité směrnice skladového místa. Podobné nastavení musíte použít pro směrnice skladového místa, které mají **Typ práce** *výběr*, pokud potřebujete zpracovat objednávky, které obsahují více SKU.

    Použijte možnost **Vícenásobné SKU** pro řádky práce, které zpracovávají více než jedno číslo položky. (Číslo položky bude v detailech práce prázdné a bude zobrazeno jako **Násobek** na stránkách zpracování v aplikaci skladu.)

    V typickém příkladu scénáře je pracovní šablona nastavena tak, aby měla více než jeden pár vyskladnění/vložení. V takovém případě možná budete chtít vyhledat konkrétní pracovní místo, které se použije pro řádky s **Typem práce** *Vložení*.

    > [!NOTE]
    > Pokud je možnost **Vícenásobná SKU** nastavena na *Ano*, nemůžete vybrat **Upravit dotaz** v podokně akcí, protože dotaz nelze vyhodnotit na úrovni položky, pokud existuje více položek. Chcete-li zajistit, aby byla vybrána požadovaná směrnice skladového místa, použijte pole **Kód směrnice** pro nasměrování výběru směrnice, která souvisí s řádky vyskladnění, kde je tento kód směrnice přiřazen v pracovní šabloně.

    Pokud vždy nepracujete s operacemi s jednou nebo více položkami, je důležité definovat dvě směrnice skladového místa pro pracovní příkaz *Vložení*: jednu, kde je možnost **Vícenásobná SKU** nastavena na *Ano* a jedna, kde je nastaven na *Ne*.

- **Příslušný dispoziční kód** - Zadejte, zda dispoziční kód směrnice skladového místa musí odpovídat dispozičnímu kódu, který je použit při přijetí položky, nebo zda mohou být směrnice skladového místa vybrány na základě libovolného dispozičního kódu. Při výběru možnosti *Přesná shoda* a ponechání prázdného pole **Dispoziční kód** budou použity pouze prázdné dispoziční kódy pro tuto směrnici skladového místa.

    > [!NOTE]
    > Toto pole je k dispozici pouze pro vybrané typy pracovních příkazů, kde je povoleno doplňování. Úplný seznam najdete v části [Pole, která jsou specifická pro typy pracovních příkazů](#fields-specific-types) dříve v tomto tématu.

- **Vyhledat podle** - Určete, zda by odložené množství mělo být celé množství na registrační značce, nebo zda by mělo být po jednotlivých položkách. Toto pole vám pomůže zajistit, aby byl veškerý obsah registrační značky vložen na jedno místo a aby systém nenavrhoval, abyste obsah rozdělili na několik míst pro procesy příjmu **ASN** (příjem registrační značky), příjem **Smíšené registrační značky** a **Klastr**. (Proces příjmu **Klastr** vyžaduje, aby *funkce odložení klastru* byla zapnutá.) Chování dotazu na směrnici skladového místa řádků a akcí směrnice skladového místa se bude lišit v závislosti na hodnotě, kterou vyberete. Pevná záložka **Čáry** se používá, jen tehdy, když je **Vyhledat podle** nastavena na *Položka*.

    > [!NOTE]
    > Toto pole je k dispozici pouze pro vybrané typy pracovních příkazů, kde je povoleno doplňování. Úplný seznam najdete v části [Pole, která jsou specifická pro typy pracovních příkazů](#fields-specific-types).

- **Dispoziční kód** - Toto pole se používá pro směrnice skladového místa, které mají typ pracovního příkazu *Nákupní objednávky*, *Hotové zboží odloženo* nebo *Vrátit objednávky* a typ práce *Vložit*. Použijte jej k vedení toku k použití konkrétní směrnice skladového místa, v závislosti na kódu dispozice, který pracovník vybral v aplikaci skladu. Můžete například nasměrovat vrácené zboží na místo kontroly, než bude vráceno do skladu. Dispoziční kód lze propojit se stavem zásob. Tímto způsobem jej lze použít ke změně stavu zásob v rámci procesu přijímání. Máte například dispoziční kód *QA*, který nastavuje stav zásob na *QA*. Poté můžete mít samostatnou směrnici skladového místa, abyste toto zboží přesunuli do karantény.

    > [!NOTE]
    > Toto pole je k dispozici pouze pro vybrané typy pracovních příkazů, kde je povoleno doplňování. Úplný seznam najdete v části [Pole, která jsou specifická pro typy pracovních příkazů](#fields-specific-types).

## <a name="lines-fasttab"></a>Pevná záložka Řádky

Pevnou záložku **Řádky** použijte k vytvoření podmínek pro použití souvisejících akcí, které jsou uvedeny na pevné záložce **Akce směrnice skladového místa**. Pro každý řádek můžete určit minimální a maximální množství, na které by se akce měla vztahovat. Můžete také určit, že akce by měly platit pro konkrétní jednotku zásob.

- **Pořadové číslo** - zadejte pořadí, ve kterém bude směrnice pro umístění řádku zpracována pro vybraný typ práce. Pořadí můžete podle potřeby změnit pomocí tlačítek **Posunout nahoru** a **Posunout dolů** v podokně akcí.
- **Z množství** - Určete začátek rozsahu množství, kterých se řádek týká. V poli **Jednotka** určete množství pro vybranou měrnou jednotku.
- **Do množství** - Určete konec rozsahu množství, kterých se řádek týká. V poli **Jednotka** určete množství pro vybranou měrnou jednotku.
- **Jednotka** - Vyberte měrnou jednotku pro dané položky. Můžete zadat minimální a maximální množství, na které má být směrnice použita, a můžete určit, zda bude směrnice použita pouze pro specifickou skladovou jednotku. Pole **Jednotky** se používá *pouze* pro vyhodnocení množství. Aby bylo možné určit, zda se řádek směrnice o umístění použije, systém použije množství v jednotce zadané na tomto řádku. Vždy, když dosáhne řádku směrnice skladového místa, systém se pokusí o převod jednotky poptávky na jednotku zadanou na řádku. Pokud převod jednotek měření neexistuje, systém přejde na další řádek.
- **Vyhledat množství** - Toto pole se používá pouze při pokusech o vložení nebo vyhledání položek ve skladu. (Proto je platná, pouze pokud je pole **Typ práce** nastaveno na *Vložit*). Vyberte jednu z následujících hodnot a určete množství, které se použije k vyhodnocení, zda je množství v rozsahu **Z množství** do **Do množství**:

    - **Množství na registrační značce** - Použijte množství na registrační značce, které je přijímáno.
    - **Jednotkové množství** - Použijte množství, které se použije během transakce. Například přijmete do skladu 1 000 kusů a rozdělíte toto množství na 10 registračních značek, z nichž každá má 100. V tomto případě můžete použít množství 1 000 položek namísto množství registrační značky 100.
    - **Zbývající množství** - Použijte množství, které ještě musí být přijato na zpracovávaném řádku nákupní objednávky.
    - **Očekávané množství** - Použijte celkové množství řádku nákupní objednávky bez ohledu na to, co již bylo přijato.

- **Omezit podle jednotky** - Toto zaškrtávací políčko umožňuje specifikovat řádek směrnice skladového místa pro měrnou jednotku nebo více měrných jednotek. Zaškrtnutím tohoto políčka omezíte měrné jednotky, které jsou považovány za platná kritéria výběru pro řádky směrnice skladového místa. Tato funkce funguje pouze pro směrnice skladového místa, kde je pole **Typ práce** nastaveno na *Výběr*.

    Když například rezervujete množství, chcete si rezervovat palety pouze z konkrétní sady míst. V tomto případě řádky omezí tuto sekvenci na palety takovým způsobem, že pro směrnici skladového místa nebude vybráno žádné množství, které je menší než paleta.

    Všimněte si, že ,zaškrtávací políčko **Omezit podle jednotky** nekontroluje jednotku nebo jednotky, které se používají na řádcích práce. Omezení jednotek platí pouze pro jednotky, které jsou dostupné prostřednictvím skupiny sekvencí jednotek. Například je položka spojena se skupinou sekvencí jednotek, která zahrnuje jak jednotku *palety*, tak *ks*. Byla stanovena měrná jednotka, kde 1 paleta = 100 ks, a směrnice o umístění používá **Omezit podle jednotky** funkčnost pouze pro palety. Dále byla definována pracovní šablona, která omezuje vytváření záhlaví práce na 50 ks. V tomto případě budou vytvořeny řádky práce o 50 ks. Chcete-li určit měrnou jednotku pro omezení, postupujte takto:

    1. Na pevné záložce **Řádky** vyberte na panelu nástrojů **Omezit podle jednotky**. (Toto tlačítko bude k dispozici až poté, co vyberete **Omezit podle jednotky** zaškrtávací políčko na řádku a poté vyberte **Uložit**.)
    1. Na stránce **Omezit podle jednotek** v poli **Jednotka** vyberte měrnou jednotku, kterou chcete omezit pro procesy výběru a vložení.

- **Zaokrouhlit nahoru na jednotku** - Toto pole funguje společně se zaškrtávacím políčkem **Omezit podle jednotky**. Pokud je například na řádku směrnice skladového místa vybraná možnost **Omezit podle jednotky** a **Zaokrouhlit nahoru na jednotku**, práce vygenerovaná ze směrnice pro výdej suroviny musí být zaokrouhlena nahoru v jedné manipulační jednotce, která je zadaná na stránce **Omezit podle jednotky**.

    > [!NOTE]
    > Toto nastavení **Zaokrouhlit nahoru na jednotku** funguje pouze pro typ pracovního příkazu *Vychystávání surovin* a pouze pro směrnice skladového místa, kde je pole **Typ práce** nastaveno na *Výběr*.

- **Vyhledat množství balení** - Pokud na prodejní objednávce, objednávce přenosu nebo výrobní objednávce určíte množství balení, toto zaškrtávací políčko umožňuje omezit systém tak, aby mohl vybrat pouze umístění, která mají alespoň toto množství balení.

    > [!NOTE]
    > Tato funkce bude fungovat pouze pro směrnici skladového místa typu *Vyskladnění* .

- **Povolit rozdělení** - Určete, zda smí směrnice skladového místa rozdělit přijaté množství nebo množství, které je rezervováno napříč vícero místy skladu, nebo zda celé množství musí být umístěno na jedno místo nebo rezervováno z jediného místa za účelem vytvoření práce.
- **Šablona okamžitého doplnění** – toto pole použijte, pokud chcete vytvořit připojení k šabloně doplnění a začněte tak okamžitě proces doplnění, pokud nejsou položky přiděleny. Pokud pole zůstane prázdné, doplňování položek se nespustí, dokud nebudou zpracovány všechny řádky směrnice skladového místa.

    > [!NOTE]
    > Toto pole je k dispozici pouze pro vybrané typy pracovních příkazů, kde je povoleno doplňování. Úplný seznam najdete v části [Pole, která jsou specifická pro typy pracovních příkazů](#fields-specific-types).

## <a name="location-directive-actions-fasttab"></a>Pevná záložka Akce směrnice skladového místa

Můžete určit více akcí směrnice skladového místa pro každý řádek. Pořadové číslo se znovu použije k určení pořadí, ve kterém jsou akce posuzovány. Na této úrovni můžete nastavit dotaz a definovat tak způsob vyhledání nejlepšího skladového místa ve skladu. Také můžete použít předdefinované hodnoty **Strategie** a najít tak optimální skladové místo.

- Pole **Pořadové číslo** - zobrazuje posloupnost, ve které budou akce zpracovány pro vybraný typ práce. Pořadí můžete změnit pomocí tlačítek **Posunout nahoru** a **Posunout dolů** na panelu nástrojů.
- **Název** - zadejte název akce směrnice místa. Buďte konkrétní, aby provedená akce byla jasná z názvu.
- **Využití pevné polohy** - Určete, která umístění by měla směrnice skladového místa zohlednit. Vyberte jednu z následujících hodnot:

    - **Pevná a ostatní skladová místa** - Tato směrnice skladového místa zváží všechna skladová místa.
    - **Pouze pevná skladová místa pro produkt** – Směrnice skladového míst zváží pouze pevná skladová místa pro produkt.
    - **Pouze pevná skladová místa pro variantu produktu** – Směrnice skladového míst zváží pouze pevná skladová místa pro variantu produktu.

- **Povolit záporné zásoby** - zaškrtnutím tohoto políčka můžete v zadaném skladovém umístění povolit záporné počty zásob ve směrnici skladového místa.
- **Povolená dávka** –Zaškrtnutím tohoto políčka můžete použít dávkové strategie pro položky, mají povolenou dávku. Je důležité, abyste zaškrtli toto políčko u procesů, které používají směrnice skladového místa k vyhledání umístění, ze kterých budou vybrány položky sledované číslem dávky. Tímto způsobem je zahrnuto hledání míst, která obsahují položky sledované číslem dávky. Pokud je toto políčko zaškrtnuto a **Strategie** pole je nastaveno na *Žádná*, systém přejde na další řádek akce.
- **Strategie** - Chcete-li usnadnit a urychlit definování akcí, které jsou přidruženy k jednotlivým řádkům směrnice skladového místa, použijte jednu z předdefinovaných strategií.

    - **Žádná** - Žádná strategie nebude použita.
    - **Párovat množství balení** - Tato strategie ověřuje, zda má výdejní skladové místo zadané množství balení. Tato strategie je platná, pouze pokud **Typ práce** pole je nastaveno na *Výběr*.
    - **Konsolidovat** - Tato strategie se používá pro konsolidaci položek v konkrétním skladovém místě, když jsou podobné položky již k dispozici. Tato strategie je platná, pouze pokud **Typ práce** pole je nastaveno na *Vložit*. V typickém nastavení pro vložení se systém pokouší konsolidovat na prvním řádku akce a poté na druhém řádku akce se snaží vložit bez konsolidace. Konsolidace zboží bude mít za následek efektivnější pozdější vyskladnění.
    - **Dávková rezervace FEFO** - Tato strategie využívá dávkové rezervace FEFO. Použijte ji, když se zásoby nacházejí pomocí data vypršení platnosti dávky a zařazují pro rezervaci dávek. Tato strategie se dá použít pouze pro položky s povolenou dávkou. Je platná, pouze pokud **Typ práce** pole je nastaveno na *Výběr*.
    - **Zaokrouhlete nahoru na celou dávku LP a FEFO** - Tato strategie kombinuje prvky strategií *dávkové rezervace FEFO* a *Zaokrouhlete na celé LP*. Je platný pouze pro dávkové položky a směrnice skladového místa, které mají typ práce *Výběr*. Aby bylo možné použít řádek, musí být dávkově povolen na použití strategie *Dávková rezervace FEFO* a strategii *Zaokrouhlit na celé LP* lze použít pouze pro doplnění. Pokud je tato strategie nakonfigurována společně s limitem umístění skladu, může to způsobit přetížení vybraného umístění pracovního místa a ignorování limitů skladování.
    - **Zaokrouhlit nahoru na úplnou registrační značku** - Tato strategie slouží k zaokrouhlování skladového množství, aby odpovídalo množství registrační značky přiřazenému ke zboží k výdeji. Tuto strategii můžete použít pouze pro směrnice skladového místa doplnění typu *Výběr*. Pokud je tato strategie nakonfigurována společně s limitem umístění skladu, může to způsobit přetížení vybraného umístění pracovního místa a ignorování limitů skladování.
    - **Řízeno registrační značkou** – tuto strategii použijte, když provedete uvolnění objednávky do skladu pro vytvoření práce výdeje a vložení. Tento přístup lze provést pro více registračních značek. Tato strategie se pokusí rezervovat a vytvořit práci výdeje z míst, kde jsou požadované registrační značky, které byly přidruženy k řádkům převodního příkazu. Pokud však tyto akce nelze dokončit, ale přesto chcete vytvořit vychystávací práci, měli byste se vrátit k jiné strategii pro akce směrnice skladovacího místa. V závislosti na požadavcích vašeho obchodního procesu můžete také hledat zásoby v jiné oblasti skladu.
    - **Prázdné místo bez příchozí práce** - Tato strategie slouží k vyhledání prázdných míst. Sklad je považován za prázdný, pokud nemá žádné fyzických zásoby a neočekává příchozí práci. Tuto strategii můžete použít pouze pro směrnice skladového místa, které mají typ práce *Výběr*.
    - **FIFO zastarávání místa** – Pomocí strategie FIFO můžete dodávat jak dávkově sledované položky, tak položky bez dávkového sledování, na základě data, kdy byl inventář zadán do skladu. Tato schopnost může být užitečná zejména u zásob bez dávkového sledování, kde není k dispozici datum vypršení platnosti pro třídění. Strategie FIFO najde místo, které obsahuje nejstarší datum stárnutí, a přidělí výdej podle tohoto data stárnutí.
    - **LIFO zastarávání místa** – Pomocí strategie LIFO můžete dodávat jak dávkově sledované položky, tak položky bez dávkového sledování, na základě data, kdy byl inventář zadán do skladu. Tato schopnost může být užitečná zejména u zásob bez dávkového sledování, kde není k dispozici datum vypršení platnosti pro třídění. Strategie LIFO najde místo, které obsahuje nejnovější datum stárnutí, a přidělí výdej podle tohoto data stárnutí.

## <a name="example-using-location-directives"></a>Příklad: použití směrnic skladového místa

V tomto příkladu zvažte proces nákupní objednávky, kde směrnice skladového místa musí vyhledat volnou kapacitu ve skladu pro skladové položky, které byly právě zaregistrovány na přijímacím překladišti. Nejprve potřebujete vyhledat volnou kapacitu v rámci skladu konsolidací s existujícími zásobami na skladě. Není-li konsolidace možná, pak musíte najít prázdné skladové místo.

Pro tento scénář musíte definovat dvě akce směrnice skladového místa. První akce v číselné řadě musí používat strategii *Konsolidovat* a druhá strategii *Prázdné umístění s žádnou příchozí prací*. Pokud definujete třetí akci pro zpracování scénáře přetečení, jsou možné dva výsledky v případě, že neexistuje žádná další kapacita ve skladu: práci lze vytvořit i v případě, že jsou definována žádná skladová místa, nebo může proces vytváření práce selhat. Výsledek je určen nastavením na stránce **Selhání směrnice skladového místa**, kde můžete zvolit, zda chcete vybrat možnost **Zastavit práci při selhání směrnice umístění** pro každý typ pořadí pracovních činností.

## <a name="next-step"></a>Další krok

Po vytvoření směrnic skladového místa můžete přiřadit každý kód směrnice ke kódu šablony práce pro vytvoření práce. Další informace naleznete v tématu [Řízení práce ve skladu pomocí šablon práce a směrnic skladového místa](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/control-warehouse-location-directives).

## <a name="additional-resources"></a>Další prostředky

- Video: [Podrobné prozkoumání konfigurace správy skladu](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Téma nápovědy [Řízení práce ve skladu pomocí šablon práce a směrnic skladového místa](control-warehouse-location-directives.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]