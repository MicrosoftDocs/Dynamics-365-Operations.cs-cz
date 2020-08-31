---
title: Vytvoření směrnic skladového místa
description: Toto téma vysvětluje, jak vytvořit směrnice skladového místa. Směrnice skladového místa jsou pravidla definovaná uživatelem, která pomáhají identifikovat místa vyskladnění a umístění pro pohyb zásob.
author: Mirzaab
manager: tfehr
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-28
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: bdd99b5faefd7054023b45a91fad070aac055a26
ms.sourcegitcommit: ecad92c9cb7e9e57688e678f79f747673c921df5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2020
ms.locfileid: "3692131"
---
# <a name="create-location-directives"></a>Vytvoření směrnic skladového místa

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit směrnice skladového místa. Směrnice skladového místa jsou pravidla definovaná uživatelem, která pomáhají identifikovat místa vyskladnění a umístění pro pohyb zásob. V transakce prodejní objednávky například směrnice skladového místa určuje, které zboží bude vydáno a kam bude umístěno.

> [!NOTE]
> V tomto tématu se týká funkcí v modulu **Správa skladu**. Nevztahuje se na funkce v modulu [Řízení zásob](../inventory/inventory-home-page.md).

Směrnice skladového místa lze použít k následujícím úkolům:

- Odložení příchozích položek.
- Vyskladnění a umístění zboží pro výstupní transakce.
- Vyskladnění a vložení surovin do výroby.
- Doplnění skladových míst.

## <a name="prerequisites"></a>Předpoklady

Než budete moci vytvořit směrnici o umístění, musíte se ujistit, že jsou splněny všechny požadované podmínky.

1. Přejděte na **Řízení skladu \> Nastavení \> Sklad \> Sklady**.
1. Vytvoření skladu.
1. Na záložce **Sklady** nastavte možnost **Použít procesy správy skladu** na *Ano*.
1. Vytvoření skladových míst, typů skladových míst, profilů skladových míst a formátů skladového místa. Další informace viz [Konfigurace umístění ve skladu podporujícím WMS](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).
1. Vytvoření pracovišť, zón a skupin zón. Další informace viz [Nastavení skladu](https://docs.microsoft.com/dynamics365/commerce/channels-setup-warehouse) a [Konfigurace umístění ve skladu podporujícím WMS](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).

## <a name="setup"></a>Nastavení

### <a name="create-location-directives"></a>Vytvoření směrnic skladového místa

Při vytváření směrnice skladového místa postupujte takto.

1. Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.
1. V podokně seznamu nastavte **Typ pracovní zakázky** na typ transakce inventáře, pro kterou vytváříte směrnici o umístění.
1. V podokně Akce vyberte možnost **Nová**, vytvoří se směrnice skladového místa.
1. Pro novou směrnici skladového místa nastavte pole podle popisu v následující tabulce.

    | Pole | popis |
    |---|---|
    | Pořadové číslo | Zadejte celé číslo, které označuje pozici sekvence směrnice skladového místa. Pozice sekvence určují, v jakém pořadí jsou směrnice skladového místa zpracovány pro vybraný typ prácovního příkazu. |
    | Jméno | Zadat název nové směrnice skladového místa. | 
    | Typ práce | Vybrat typ práce, která má být vykonávána. Seznam hodnot záleží závisí na typu skladové transakce, který jste vybrali v poli **Typ pracovního příkazu**. K dispozici mohou být následující hodnoty:<ul><li>**Vložit** - Směrnice skladového místa se pokusí najít nejlepší umístění pro umístění inventáře, který přichází do systému, prostřednictvím příjmu, výroby nebo úprav inventury. Směrnice skladového místamísto se také používá k definování umístění na místo určení nebo konečného místa expedice nákladové brány v odchozím toku.</li><li>**vybrat** - Směrnice skladového místa se pokusí najít nejlepší umístění, ze kterých lze fyzicky rezervovat inventář (vytvořit pracovní příkazy). Vyskladnění lze dokončit (řádek práce vyskladnění lze uzavřít), i když práce není dokončena. Uživatel může dokončit fyzické vyskladnění. V systému je tato akce krokem k vyzvednutí. Uživatel poté může provést zrušení z mobilního zařízení a dokončit pracovní příkaz (například vybrat) později. Záhlaví práce je však napřed uzavřeno, když je dokončeno koncové vložení.</li><li>**Inventura**, **Úpravy**, **Vlastní**, **Změna stavu zásob**, **Sestavení registrační značky vozidla**, **Tisk**, **Změna stavu** a **Zabalit do vnořených registračních značek** - Tyto hodnoty nemohou být použity v žádném nastavení směrnic skladového místa.</li></ul> |
    | Lokalita | Vyberte pracoviště, ve kterém má být práce provedena. |
    | Sklad | Vyberte skladové místo, ve kterém má být práce provedena. |
    | Kód předpisu | Vyberte kód předpisu, který určí výběr předpisů umístění souvisejících s řádky vložení šablony práce s tímto kódem. Na **Směrnice** stránce můžete vytvořit nové kódy, které lze použít k připojení pracovní šablony ke směrnici skladového místa. Tuto stránku můžete také použít pro vytvoření spojení mezi jakýmkoliv řádkem šablony práce a směrnicí skladového místa (jako je například nákladová brána nebo skladové místo fáze). Další informace o konfuguraci kódů předpisů se šablonami práce naleznete v tématu [Řízení práce ve skladu pomocí šablon práce a směrnic umístění](control-warehouse-location-directives.md).<p>Pokud je nastaven kód šablony při generování práce, systém nebude hledat směrnice skladového místa podle kódu místo posloupnosti. To znamená, že můžete být konkrétnější v použití typu šablony skladového místa pro určitý krok v šabloně práce, jako je například krok pro fázování materiálů.</p> |
    | Dispoziční kód | Vyberte dispoziční kód pro přesměrování odložení přijatých položek do skladového místa. (Více informací viz [Nastavte kódy dispozic](tasks/set-up-dispositions-codes.md).) Toto pole je k dispozici, pouze pokud **Typ pracovní zakázky** pole je nastaveno na *Nákup objednávek*, *Vracení objednávek*, nebo *Hotové zboží odloženo*. |
    | Více skladových jednotek | Nastavte tuto možnost na *Ano*, chcete-li na místě použít více skladových jednotek (SKU). Tato možnost musí být například nastavena na *Ano* pro nákladovou bránu.<p>Pokud **Více SKU** možnost je nastavena na *Ano* , skladové místo bude upřesněno v práci (podle očekávání). Skladové místo však bude schopno zpracovat vícenásobné vložení položky, pouze pokud práce zahrnuje různá SKU, které musí být vybrány a vloženy, nikoli pokud práce obsahuje pouze jednu SKU, která musí být vložena.</p><p>Je-li **Více skladových jednotek** nastaveno na *Ne*, skladové místo pro vložení bude určeno pouze tehdy, pokud má vložení pouze jeden druh skladové jednotky.</p><p>Chcete-li použít oba přístupy, musíte zadat dva řádky, které mají stejnou strukturu a nastavení, ale nastavte **Více SKU** možnost na *Ano* pro jeden z řádků a *Ne* pro druhý. Jinými slovy dvě identické směrnice skladového místa jsou třeba pro operaci vložit, i když nerozlišujete mezi jednou a vícero skladovými jednotkami v ID práce. Rovněž je třeba nastavit směrnici skladového místa, pokud máte objednávky s více než jednou položkou.</p><p>**Všimněte si:** Nastavíte-li možnost **Více SKU** na *Ano* pro směrnici skladového místa typu práce *Vložení*, systém vždy vybere první řádek směrnice skladového místa bez ohledu na jiné omezení vytvořené na řádcích.</p> |

1. Volitelné: V podokně akcí vyberze **Upravit dotaz** pro výběr umístění nebo zadejte libovolné omezení, které se použije při výběru směrnice určitého skladového místa.
1. Na pevné záložce **Řádky** vytvořte jeden nebo více řádků pro zadání jednotek a vyhledání nebo rezervaci množství ve skladu.
1. Na každém novém řádku skladového místa nastavte pole podle popisu v následující tabulce.

    | Pole | popis |
    |---|---|
    | Pořadové číslo | Zadejte celé číslo, které označuje pozici sekvence směrnice skladového místa. Pozice sekvence určují, v jakém pořadí jsou směrnice skladového místa zpracovány pro vybraný typ práce. |
    | Od množství | Určete počáteční rozsah množství pro případ, kdy je třeba zvolit pořadí střední mřížky. V poli **Jednotka** určete množství pro vybranou měrnou jednotku. |
    | Do množství | Určete konečný rozsah množství pro případ, kdy je třeba zvolit pořadí střední mřížky. V poli **Jednotka** určete množství pro vybranou měrnou jednotku. |
    | Jednotka | Vyberte měrnou jednotku pro dané položky.<p>Můžete určit minimální a maximální množství, na které by se směrnice měla vztahovat. Můžete také určit, že směrnice by měla být použita pro konkrétní jednotku inventáře. Pole **Jednotky** se používá pouze pro vyhodnocení množství.</p><p>Aby bylo možné určit, zda se použije směrnice o umístění, systém vyhodnotí množství pomocí **Jednotka** hodnoty uvedené na řádku. Vždy, když je přistoupeno do řádku směrnice skladového místa, systém se pokusí o převod jednotky poptávky na jednotku zadanou na řádku. Pokud převod jednotek neexistuje, systém přejde na další řádek.</p> |
    | Vyhledat množství | Toto pole je platné, pouze pokud se pokusíte umístit nebo vyhledat množství ve skladu. Jinými slovy, platí pouze pro *Vložit* práce. Vyberte metodu, která se používá ke kontrole, zda je množství v rozsahu, který je nastavený v polích **Od množství** a **Do množství**. Pokud směrnice skladového místa je pro vstupní transakci, vyberte jednu z následujících možností:<ul><li>**Množství registrační značky** – Pro vyhodnocení, zda je množství v rámci rozsahu, použijte množství na přijímané registrační značce.</li><li>**Sjednocené množství** – Pro vyhodnocení, zda je množství v rámci rozsahu, použijte množství které je používané při transakci. Například ve skladu, pokud můžete přijmout množství 1000 a rozdělit ho na 10 registračních značek po 100, můžete použít množství 1000 položek místo množství registrační značky 100.</li><li>**Zbývající množství** – Pro vyhodnocení, zda je množství v rámci rozsahů , použijte množství, které zbývá přijmout na řádku nákupní objednávky aktuálně vráceném se změnami.</li><li>**Očekávané množství** – Pro vyhodnocení, zda je množství v rámci rozsahů množství, použijte celkové množství řádku nákupní objednávky bez ohledu na to, co již bylo přijato.</li></ul> |

1. Volitelné: Můžete vybrat následující dodatečné nastavení na pevné záložce **Řádky**.

    | Pole | popis |
    |---|---|
    | Omezit podle jednotky | Zaškrtnutím tohoto políčka omezíte měrné jednotky, které jsou považovány za platná kritéria výběru pro řádky směrnice skladového místa. Pokud byly zadány měrné jednotky, budou pro výběr řádku považovány za platné pouze položky, kde jednotka odpovídá alespoň jedné jednotce definované pro skupinu sekvencí jednotek.<p>Například jednotka je omezena na palety a položka je spojena se skupinou sekvencí jednotek, která zahrnuje *palety* jednotku. V takovém případě budou položky považovány za platnou možnost pro směrnicis kladového místa.</p><p>Nicméně, **Omezit podle jednotky** zaškrtávací políčko nekontroluje jednotku nebo jednotky, které se používají na řádcích práce. Omezení jednotek platí pouze pro jednotky, které jsou dostupné prostřednictvím skupiny sekvencí jednotek.</p><p>Například je položka spojena se skupinou sekvencí jednotek, která zahrnuje jak *palety*, tak *ks* jednotku. Byla stanovena měrná jednotka, kde 1 paleta = 100 ks, a směrnice o umístění používá **Omezit podle jednotky** funkčnost pouze pro palety. Dále byla definována pracovní šablona, která omezuje vytváření záhlaví práce na 50 ks. V tomto případě budou vytvořeny řádky práce o 50 ks.</p><p>Chcete-li určit měrnou jednotku pro omezení, postupujte takto</p><ol><li>Na pevné záložce **Řádky**, vyberte **Omezit podle jednotky**. Toto tlačítko bude k dispozici až poté, co vyberete **Omezit podle jednotky** zaškrtávací políčko na řádku a poté vyberte **Uložit**.</li><li>V poli **Jednotka** vyberte měrnou jednotku k omezení pro proces výdeje a odložení.</li></ol> |
    | Zaokrouhlit nahoru na jednotku | Tuto možnost vyberte pro označení toho, zda má být výdej suroviny zaokrouhlen na násobek manipulační jednotky uvedené v poli **Omezit podle jednotky**. Pole platí pouze pro výdej suroviny a směrnice skladového místa typu *Výdej*. |
    | Vyhledat množství balení | Toto políčko zaškrtněte, pokud je množství dodací jednotky určeno na stránce **Prodejní objednávka**. Pokud zaškrtnete toto políčko, budou vybrána pouze skladová místa s tímto množstvím dodací jednotky. |
    | Povolit rozdělení | Zaškrtnutím tohoto políčka můžete rozdělit množství do více umístění. |
    | Šablona okamžitého doplnění | Vytvořte připojení k šabloně doplnění a začněte tak okamžitě proces doplnění, pokud nejsou položky přiděleny. Pokud pole zůstane prázdné, doplňování položek se nespustí, dokud nebudou zpracovány všechny řádky směrnice skladového místa.<p>Toto pole je k dispozici pouze na vybraných typech pracovních příkazů, kde je povoleno doplňování, např *Prodejní objednávky* a *Sběr surovin*.</p> |

1. Na pevné záložce **Akce směrnic skladového místa** klepněte na tlačítko **Nový** a vyberte umístění nebo rozsah umístění.
1. Pole **Pořadové číslo** zobrazuje posloupnost, ve které bude směrnice pro umístění zpracována pro vybraný typ práce. Pořadí můžete změnit. Buďte však opatrní ohledně čísel sekvencí pro akce směrnic skladového místa, protože akce směrnich skladového místa budou vždy spuštěny v této posloupnosti.
1. V poli **Název** zadejte název akce směrnice místa. Buďte konkrétní, aby bylo jasné, co akce je.
1. Volitelné: Klepněte na tlačítko **Upravit dotaz** pro úpravu skladových míst a dalších kritérií.
1. Volitelné: Můžete nastavit následující dodatečná pole pro směrnici místa.

    | Pole | popis |
    |---|---|
    | Využití pevného skladového místa | Vyberte, která umístění směrnice umístění bere v úvahu.<ul><li>**Pevná a ostatní skladová místa** - Tato směrnice skladového místa zváží všechna skladová místa.</li><li>**Pouze pevná skladová místa pro produkt** – Směrnice skladového míst zváží pouze pevná skladová místa pro produkt.</li><li>**Pouze pevná skladová místa pro variantu produktu** – Směrnice skladového míst zváží pouze pevná skladová místa pro variantu produktu.</li></ul> |
    | Povolit záporné zásoby | Zaškrtnutím tohoto políčka můžete v zadaném skladovém umístění povolit záporné počty zásob. |
    | Dávka povolena | Zaškrtnutím tohoto políčka můžete použít dávkové strategie pro položky, mají povolenou dávku. Pokud je toto políčko zaškrtnuto a **Strategie** pole je nastaveno na *Žádná*, systém přejde na další řádek akce. |
    | Strategie | Vyberte strategii, kterou by směrnice skladového místa měla používat:<ul><li>**Žádná** - Žádná strategie nebude použita.</li><li>**Párovat množství balení** - Tato strategie umožňuje ověřit, zda má výdejní skladové místo zadané množství balení. Tato strategie je platná, pouze pokud **Typ práce** pole je nastaveno na *Výběr*.</li><li>**Konsolidovat** - Tato strategie se používá pro konsolidaci položek v konkrétním skladovém místě, když jsou podobné položky již k dispozici. Tato strategie je platná, pouze pokud **Typ práce** pole je nastaveno na *Vložit*. V typickém nastavení pro vložení se systém pokouší konsolidovat na prvním řádku akce a poté na druhém řádku akce se snaží vložit bez konsolidace. Konsolidace zboží bude mít za následek efektivnější pozdější vyskladnění.</li><li>**Rezervace dávky FEFO** - Tato strategie se používá, když se zásoby vyhledávají pomocí data vypršení platnosti dávky a jsou přiděleny pro rezervaci dávek. Strategie rezervace dávky FEFO (First Expiry, First Out) se používá také když je sklad vyhledán v rámci dávky před datem doporučené spotřeby společně s datem vypršení platnosti. Tato strategie se dá použít pouze pro položky s povolenou dávkou. Tato strategie je platná, pouze pokud **Typ práce** pole je nastaveno na *Výběr*. Když vyberete tuto strategii, přepíšete jakékoli třídění dotazů podle čísel šarží, které se použijí.</li><li>**Zaokrouhlit nahoru na úplnou registrační značku** - Tato strategie umožňuje zaokrouhlování skladového množství, aby odpovídalo množství registrační značky přiřazenému ke zboží k výdeji. Tuto strategii lze použít pouze pro doplnění typu lokalizačních směrnic, a to pouze tehdy, když **Typ práce** pole je nastaveno na *Vybrat*.</li><li>**Prázdné místo bez příchozí práce** - Tato strategie slouží k vyhledání prázdných míst. Sklad je považován za prázdný, pokud nemá žádné fyzických zásoby a neočekává příchozí práci. Tato strategie je platná, pouze pokud **Typ práce** pole je nastaveno na *Vložit*.</li></ul> |

## <a name="example-of-the-use-of-location-directives"></a>Příklad použití směrnic skladového místa

V tomto příkladu zvažte proces nákupní objednávky, kde směrnice skladového místa musí vyhledat volnou kapacitu ve skladu pro skladové položky, které byly právě zaregistrovány na přijímacím překladišti. Nejprve potřebujete vyhledat volnou kapacitu v rámci skladu konsolidací s existujícími zásobami na skladě. Není-li konsolidace možná, pak musíte najít prázdné skladové místo.

Pro tento scénář musíte definovat dvě akce směrnice skladového místa. První akce v číselné řadě musí používat strategii **Konsolidovat** a druhá strategii **Prázdné umístění s žádnou příchozí prací**. Pokud definujete třetí akci pro zpracování scénáře přetečení, jsou možné dva výsledky v případě, že neexistuje žádná další kapacita ve skladu: práci lze vytvořit i v případě, že jsou definována žádná skladová místa, nebo může proces vytváření práce selhat. Výsledek je určen nastavením na stránce **Selhání směrnice skladového místa**, kde můžete rozhodnout, zda chcete vybrat možnost **Zastavit práci při selhání směrnice umístění** pro každý typ pořadí pracovních činností.

## <a name="next-step"></a>Další krok

Po vytvoření směrnic skladového místa můžete přiřadit každý kód směrnice ke kódu šablony práce pro vytvoření práce. Další informace naleznete v tématu [Řízení práce ve skladu pomocí šablon práce a směrnic skladového místa](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/control-warehouse-location-directives).

## <a name="technical-information-for-system-admins"></a>Technické informace pro správce systému

Pokud nemáte přístup ke stránkám, které se používají k dokončení tohoto úkolu, obraťte se na správce systému a poskytněte informace, které jsou uvedeny v následující tabulce.

| Kategorie | Předpoklad |
|---|---|
| Configuration Keys | Přejděte do nabídky **Správa systému \> Nastavení \> Konfigurace licence**. Rozbalte licenční klíč **Obchod** a vyberte konfigurační klíč **Řízení skladu a správa přepravy**. |
