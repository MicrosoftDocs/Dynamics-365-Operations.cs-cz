---
title: Čárové kódy GS1
description: Toto téma popisuje, jak nastavit čárové kódy GS1 a QR kódy, aby bylo možné ve skladu skenovat štítky.
author: Mirzaab
ms.date: 03/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 083748d4aecf551fd326b6c3cbf6d92cf3daf717
ms.sourcegitcommit: d475dea4cf13eae2f0ce517542c5173bb9d52c1c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/05/2022
ms.locfileid: "8547809"
---
# <a name="gs1-bar-codes"></a>Čárové kódy GS1

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- Preview until 10.0.25 GA -->

Pracovníci ve skladech musí často dokončit několik úkolů, když pomocí skeneru mobilního zařízení registrují pohyby položky, palety nebo kontejneru. Tyto úkoly mohou zahrnovat jak skenování čárových kódů, tak ruční zadávání informací na mobilním zařízení. Čárové kódy používají formát specifický pro určitou společnost, který definujete a spravujete ve službě Microsoft Dynamics 365 Supply Chain Management.

Čárové kódy GS1 pro přepravní štítky byly vyvinuty tak, aby poskytovaly globální standard pro výměnu dat mezi společnostmi. Jsou k dispozici jak v lineárních (1D) symbolikách (formátech čárových kódů), jako je GS1-128, tak v 2D symbolikách, jako jsou kódy GS1 DataMatrix a GS1 QR. Čárové kódy GS1 kódují data, ale také vám umožňují použít předdefinovaný seznam *identifikátorů aplikace* k definici významu těchto dat. Standard GS1 definuje formát dat a různé druhy dat, která lze použít ke kódování. Na rozdíl od starších standardů čárových kódů mohou mít čárové kódy GS1 více datových prvků. Naskenování jednoho čárového kódu proto může zachytit několik typů informací o produktu, jako je dávka a datum vypršení platnosti.

Podpora GS1 ve službě Supply Chain Management dramaticky zjednodušuje proces skenování ve skladech, kde jsou palety a kontejnery označeny pomocí čárových kódů ve formátu GS1. Pracovníci skladu mohou extrahovat všechny požadované informace pomocí jediného skenování čárového kódu GS1. Čárové kódy GS1 eliminují nutnost provádět vícenásobné skenování a/nebo ručně zadávat informace a pomáhají tak zkrátit čas spojený s úkoly. Současně také pomáhají zlepšit přesnost.

Správci logistiky musí nastavit požadovaný seznam identifikátorů aplikací a každý z nich přiřadit k příslušným položkám nabídky mobilního zařízení. Identifikátory aplikace pak lze použít napříč sklady jako globální nastavení pro účely stěhování a balení. Všechny přepravní štítky proto budou mít jednotnou formu.

Pokud není uvedeno jinak, toto téma používá výraz *čárový kód* jako odkaz na lineární čárové kódy (1D) i čárové kódy 2D.

## <a name="the-gs1-bar-code-format"></a>Formát čárového kódu GS1

Všeobecné specifikace GS1 specifikují, které symboly lze použít pro čárové kódy GS1 a jak zakódovat data v čárovém kódu. Tato část poskytuje krátký úvod k tématu. Úplné informace viz [Obecné specifikace GS1](https://www.gs1.org/docs/barcodes/GS1_General_Specifications.pdf), které vydává GS1. Dokument specifikací GS1 je pravidelně aktualizován a informace, které poskytuje, jsou aktuální s vydáním GS1 General Specifications 22.0.

Čárové kódy GS1 používají následující symboly:

- **Lineární nebo 1D čárové kódy** – GS1-128 a GS1 DataBar
- **2D čárové kódy** – GS1 DataMatrix, GS1 QR Code a GS1 Dotcode

Všimněte si, že v GS1-128 jsou zvláštní zmínky o GS1, což je zvláštní případ běžného lineárního čárového kódu Code-128, GS1 DataMatrix a GS1 QR Code. Rozdíl mezi verzí GS1 a verzí bez GS1 je přítomnost speciálního znaku (FNC1) jako prvního znaku v datech čárového kódu. Přítomnost znaku FNC1 znamená, že data v čárovém kódu by měla být interpretována podle specifikace GS1.

Data v samotném čárovém kódu se skládají z více datových prvků, z nichž každý je identifikován identifikátorem aplikace na začátku pole. Obvykle jsou data také prezentována pod čárovým kódem ve formátu čitelném pro člověka, kde je v závorkách uveden identifikátor aplikace. Zde je příklad: `(01) 09521101530001 (17) 210119 (10) AB-123`. Tento čárový kód obsahuje tři prvky:

- **Identifikátor aplikace 01** – Globální číslo obchodní položky GS1 (GTIN) položky.
- **Identifikátor aplikace 17** – Datum expirace.
- **Identifikátor aplikace 10** – Číslo šarže.

Pro každý prvek mohou mít data buď předdefinovanou délku, nebo proměnnou délku. Existuje pevný seznam identifikátorů aplikací, které mají předdefinované délky. Všechny ostatní identifikátory aplikací mají proměnnou délku a seznam identifikátorů aplikací GS1 specifikuje maximální délku a formát dat. Například identifikátor aplikace 01 má předdefinovanou délku 16 znaků (dva pro samotný identifikátor aplikace a poté 14 pro GTIN) a identifikátor aplikace 17 má předdefinovanou délku osmi znaků (dva pro samotný identifikátor aplikace a poté šest pro datum). Avšak identifikátor 10 aplikace má dvě čísla pro samotný identifikátor aplikace a pak až 20 alfanumerických znaků.

Když jsou prvky složeny, pokud prvek následuje za prvkem s proměnnou délkou, musí být použit oddělovací znak. Tento oddělovač může být buď speciální znak FNC1, nebo znak oddělovače skupiny (netisknutelný znak, který má kód ASCII 29 a hexadecimální kód 1D). Oddělovač by se neměl používat za posledním prvkem. Ačkoli by se oddělovač také neměl používat po prvcích, které mají předdefinovanou délku, jeho přítomnost není kritickou chybou.

V datech čárového kódu z předchozího příkladu čárového kódu, který obsahuje identifikátory aplikace 01, 17 a 10, budou data v symbolu Code-128, QR Code nebo DataMatrix zakódována jako `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` (identifikátory aplikací jsou uvedeny tučně). Nejlepším postupem je umístit jakýkoli prvek, který má proměnnou délku, na konec, aby se eliminovala potřeba dalšího znaku oddělovače skupiny. Čárový kód však může mít i jiné pořadí prvků, kde je oddělovač povinný. Následuje příklad: `<FNC1>`**`01`**`09521101530001`**`10`**`AB-123<GS>`**`17`**`210119`.

### <a name="dates-and-decimal-numbers"></a>Data a desetinná čísla

Data jsou vždy uvedena ve formátu *RRMMDD*, kde je století roku určeno specifikacemi GS1. Mohou být uvedena pouze data od 49 let v minulosti do 50 let v budoucnosti (vzhledem k aktuálnímu roku).

Některé datové prvky obsahují desetinná čísla. Například identifikátory aplikace 3100, 3101, ... 3105 představují čistou hmotnost v kilogramech. Protože tyto identifikátory aplikace mají předdefinovanou délku 10, je pro množství k dispozici šest čísel. Pozice desetinné čárky je určena posledním číslem identifikátoru aplikace. Proto může být tato rodina aplikačních identifikátorů také reprezentována jako *310n*. Protože norma GS1 stanoví, že nalevo od desetinné čárky musí být vždy alespoň jedno číslo, je povoleno maximálně pět desetinných míst.

Zde je několik příkladů, které ukazují, jak číslo *123456* bude interpretováno různými identifikátory aplikace (zobrazeny tučně):

- **`3100`**`123456` &rarr; 123456 (celé číslo)
- **`3101`**`123456` &rarr; 12345,6 (jedno desetinné číslo)
- **`3102`**`123456` &rarr; 1234,56 (dvě desetinná čísla)
- **`3103`**`123456` &rarr; 123,456 (tři desetinná čísla)
- **`3104`**`123456` &rarr; 12,3456 (čtyři desetinná čísla)
- **`3105`**`123456` &rarr; 1,23456 (pět desetinných čísel)

## <a name="scanning-gs1-bar-codes-in-supply-chain-management"></a>Skenování čárových kódů GS1 v Supply Chain Management

Ke skenování čárových kódů GS1 používají skladníci skener, který je zabudovaný v mobilním zařízení nebo je k němu připojen. Skener poté přenese naskenovaný čárový kód do mobilní aplikace Warehouse Management jako sérii událostí klávesnice. Tento provozní režim je také známý jako a *převodník na signál klávesnice* nebo *převodník*. Mobilní aplikace pak odešle přijatý text tak, jak je, do Supply Chain Management. Když systém obdrží vstupní data, nejprve určí, zda data začínají jednou z nakonfigurovaných předpon, které označují, že data jsou ve skutečnosti čárovým kódem GS1 (viz sekce [Nastavte globální možnosti GS1](#set-gs1-options)). Pokud naskenovaná data začínají jednou z těchto předpon, systém použije analyzátor GS1 k analýze dat a extrahování jednotlivých datových prvků podle jejich aplikačních identifikátorů. Po analýze dat bude aktuální vstupní pole nebo více polí vyplněno naskenovanými daty.

### <a name="configuration-of-bar-code-scanner-hardware-and-software"></a>Konfigurace hardwaru a softwaru čtečky čárových kódů

Aby Supply Chain Management správně rozpoznal a dekódoval čárové kódy GS1, musí být hardwarový skener nebo podpůrný software nakonfigurován k provádění následujících akcí:

- Přidání k naskenovaným čárovým kódům předpony, aby systém mohl rozpoznat čárový kód GS1.
- Převod netisknutelného znaku oddělovače skupiny ASCII (kód ASCII 29 nebo hexadecimální kód 1D) na tisknutelný znak, jako je vlnovka (~).

Ačkoli můžete k naskenovanému čárovému kódu přidat libovolnou předponu, jednou z možností je přidat identifikátor symboliky ISO/IEC 15424, známý také jako *Identifikátor AIM*. Tento tříznakový identifikátor začíná na `]`, pak má jeden znak, který identifikuje použitou symboliku, a pak má číslo, které se používá jako další modifikátor. Například identifikátor AIM `]C1` určuje čárový kód Code 128 (kvůli znaku `C`) a modifikátor `1` určuje, že na první pozici dat je znak FNC1. Na druhou stranu, `]C0` je čárový kód Code 128, který má jako první znak dat jakýkoli jiný znak.

Následujících pět symbolických identifikátorů odpovídá čárovým kódům GS1, které mají prvky identifikátoru aplikace:

- `]C1` – kód 128 (`C`) se znakem FNC1 na první pozici (`1`), také známý jako GS1-128.
- `]e0`– GS1 DataBar.
- `]d2`– DataMatrix (`d`) s ECC 200 a FNC1 na první pozici (`2`), také známý jako GS1 DataMatrix.
- `]Q3`- QR kód (`Q`) Symbol modelu 2 s FNC1 na první pozici (`3`), také známý jako GS1 QR Code.
- `]J1`– GS1 DotCode.

Pokud používáte tyto identifikátory, kompatibilita s čárovými kódy jiných značek než GS1 vyžaduje, aby byly skenery nebo skenovací software nakonfigurovány tak, aby odstranily všechny identifikátory, které neodpovídají identifikátorům GS1. Pokud například naskenujete „normální“ čárový kód Code 39, přidá se předpona `]A0`. Protože systém tuto předponu nepochopí jako jednu z předpon GS1, bude ji interpretovat jako data a poskytne neočekávané výsledky.

> [!NOTE]
> Verze 2.0.17.0 a novější mobilní aplikace Warehouse Management pro usnadnění odstraní všechny předpony AIM, které nejsou zahrnuty v předchozím seznamu. Toto chování podporuje případy, kdy můžete nakonfigurovat skener tak, aby přidal předponu AIM, ale neodstranil nechtěné předpony.

### <a name="single-and-multiple-field-scanning"></a>Skenování jednoho a více polí

Poté, co byla data analyzována z čárového kódu, budou vložena do řízení toku mobilního zařízení. Postupně budou zpracovány dvě metody:

- **Skenování jednoho pole** – Tato metoda vyplní pouze pole, do kterého byl naskenován čárový kód. Pokud například naskenujete čárový kód `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123`, zatímco je kurzor v poli **Položka**, GTIN `09521101530001` z čárového kódu se do tohoto pole zadá. Pokud naskenujete stejný čárový kód, zatímco je kurzor v poli **ID dávky**, do tohoto pole se zadá číslo dávky `AB-123` z čárového kódu. Tento režim funguje pro všechna pole ve všech tocích a vyžaduje pouze konfiguraci obecného nastavení GS1. Pokud čárový kód obsahuje více prvků, musí být přesto naskenován vícekrát, protože do toku mobilního zařízení bude zadán vždy pouze jeden kus čárového kódu. Toto chování je řízeno obecným nastavením GS1, jak je popsáno v sekci [Vytvořte obecné nastavení GS1](#generic-gs1-setup).
- **Skenování více polí** – Tato metoda vyplní více polí při naskenování jednoho čárového kódu tím, že do stavu toku mobilního zařízení vloží další data. Zásada je například nakonfigurována tak, aby vložila identifikátor aplikace 01 do ovládacího prvku `ItemId` a aplikační identifikát 10 do pole `InventBatchId`. V tomto případě, pokud naskenujete čárový kód `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123`, budou data pro obě proměnné odeslána současně. Proto vás systém v toku nevyzve k zadání čísla položkly a/nebo dávky. Toto chování je řízeno zásadami GS1, které jsou propojeny s položkami nabídky, jak je popsáno v sekci [ Nastavte zásady GS1 tak, aby byly pro položky nabídky mobilního zařízení](#policies-for-menus).

> [!WARNING]
> Výchozí zásady GS1 byly testovány, aby fungovaly bez neočekávaného chování. Přizpůsobení zásad GS1, které jsou propojeny s položkami nabídky, však může způsobit neočekávané chování, protože tok nemusí očekávat, že některá data budou k dispozici v určitou dobu.

## <a name="turn-on-the-gs1-feature"></a>Zapnutí funkce GS1

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Skenování čárových kódů GS1*

### <a name="turn-on-the-enhanced-parser-for-gs1-barcodes-feature"></a>Zapněte funkci Vylepšený analyzátor pro čárové kódy GS1

Pokud používáte čárové kódy GS1, doporučujeme také povolit funkci *Vylepšený analyzátor pro čárové kódy GS1*. Tato funkce poskytuje vylepšenou implementaci analyzátoru čárových kódů GS1. Přidává následující vylepšení:

- Řídí se algoritmem GS1 General Specification pro analýzu dat symbolů a ověřuje, že data v symbolu jsou platná podle specifikace.
- Nevyžaduje, abyste nastavovali hodnotu **Maximální délka identifikátoru** a používá nejdelší shodu předpon z nakonfigurovaných identifikátorů aplikace.
- Umožňuje snadněji konfigurovat desítkové identifikátory aplikací pomocí písmene *n*, aby odpovídaly libovolnému číslu. Můžete například nakonfigurovat pouze jeden identifikátor aplikace (*310n*) namísto samostatných identifikátorů aplikace (*3101*, *3102*, *3103* a tak dále).
- Opravuje problém, kdy jsou nesprávně zakódovaná data interpretována jako data pole.
- Přichází jako samostatná třída, kterou lze znovu použít v jiných kontextech, a umožňuje použití bodu rozšiřitelnosti k manipulaci s naskenovanými daty před vyplněním polí toku.

## <a name="set-up-global-gs1-options"></a><a name="set-gs1-options"></a>Nastavení globálních možností GS1

Stránka **Parametry správy skladu** nabízí několik nastavení, která vytvářejí globální možnosti GS1.

Chcete-li nastavit globální možnosti GS1, postupujte následujícím způsobem.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.
1. Na záložce **Čárové kódy** vyplňte následující pole:

    - **Znak FNC1**, **Znak Datamatrix** a **Znak QR kódu** – Zadejte znaky, které mají být interpretovány jako předpona pro každý typ čárového kódu GS1.
    - **Oddělovač skupin** – Zadejte znak, který nahradí znak oddělovače skupiny ASCII.
    - **Maximální délka identifikátoru** – Zadejte maximální počet znaků, který je povolen v identifikátoru aplikace. Toto pole není povinné, pokud je funkce *Vylepšený analyzátor GS1* ve vašem systému zapnutá.

> [!NOTE]
> Předpony systému sdělují, že čárový kód je zakódován podle standardu GS1. Současně a pro různé účely lze použít až tři předpony (**Znak FNC1**, **Znak datové matice** a **Znak QR kódu**).

## <a name="gs1-application-identifiers"></a>Identifikátory aplikace GS1

Formáty GS1 kódují data, ale také vám umožňují použít předdefinovaný seznam identifikátorů aplikace k definici významu dat. Správci logistiky musí nastavit požadovaný seznam identifikátorů aplikací a každý z nich přiřadit k příslušným položkám nabídky mobilního zařízení. Identifikátory pak lze použít napříč sklady jako globální nastavení pro účely stěhování a balení. Všechny přepravní štítky proto budou mít jednotnou formu.

Systém používá data, zejména předdefinované identifikátory aplikací, ke stanovení pravidel, která by měla být použita na příslušnou naskenovanou informaci.

Každý identifikátor aplikace signalizuje systému, že následující znaky v naskenovaném čárovém kódu by měly být považovány za blok zašifrovaných informací. Nastavení identifikátorů aplikace definuje, jak má systém interpretovat čárový kód a uložit jej jako hodnotu v systému.

Manažeři logistiky mohou používat standardní mezinárodní identifikátory aplikací a/nebo si vytvářet vlastní.

### <a name="load-the-standard-application-identifiers"></a>Načtení standardních identifikátorů aplikace

Chcete-li rychle začít, můžete načíst seznam běžných mezinárodních identifikátorů aplikací. Seznam pak můžete podle potřeby později rozšířit nebo upravit.

Chcete-li načíst standardní identifikátory aplikace, postupujte takto.

1. Přejděte do nabídky **Správa skladu \> Nastavení \> GS1 \> Identifikátory aplikace GS1**.
1. V podokně akcí vyberte **Vytvořit výchozí nastavení**.

> [!WARNING]
> Příkaz **Vytvořit výchozí nastavení** odstraní všechny aktuálně definované identifikátory aplikace a nahradí je standardním seznamem. Po načtení výchozího nastavení však můžete seznam přizpůsobit podle potřeby.

### <a name="set-up-custom-application-identifiers"></a>Nastavení vlastních identifikátorů aplikací

Pokud se některé nebo všechny identifikátory aplikací, které vaše společnost používá, liší od standardní sady, můžete vytvořit vlastní kódy od nuly nebo upravit standardní sadu podle potřeby.

Chcete-li nastavit a přizpůsobit vlastní identifikátory aplikace GS1, postupujte takto.

1. Přejděte do nabídky **Správa skladu \> Nastavení \> GS1 \> Identifikátory aplikace GS1**.
1. Proveďte jeden z následujících kroků:

    - Chcete-li vytvořit nový identifikátor: v podokně Akce vyberte **Nový** .
    - Chcete-li upravit existující identifikátor: Vyberte identifikátor a poté v podokně akcí vyberte **Upravit**.

1. Nastavte následující pole pro nový nebo vybraný identifikátor:

    - **Identifikátor aplikace** – Zadejte identifikační kód pro identifikátor aplikace. Tento kód je obvykle dvouciferné celé číslo, ale může být i delší. U desetinných hodnot udává poslední číslice počet desetinných míst. Další informace najdete v popisu zaškrtávacího políčka **Desetinné** později v tomto seznamu. Pokud je povolená funkce *Vylepšený analyzátor pro čárové kódy GS1*, můžete pomocí písmene vytvořit jediný identifikátor aplikace pro všechny varianty desetinných míst *n* jako poslední znak v identifikátoru aplikace. Můžete například nakonfigurovat pouze jeden identifikátor aplikace (*310n*) namísto samostatného identifikátoru pro každý počet desetinných míst (*3101*, *3102*, *3103* a tak dále).
    - **Popis** – Zadejte krátký popis identifikátoru.
    - **Pevná délka** – Toto políčko zaškrtněte, pokud hodnoty, které jsou skenovány pomocí tohoto identifikátoru aplikace, mají pevný počet znaků. Pokud je délka hodnot proměnná, zrušte zaškrtnutí tohoto políčka. V tomto případě musíte zadat konec hodnoty pomocí znaku oddělovače skupin, který jste zadali na stránce **Parametry správy skladu**.
    - **Délka** – Zadejte maximální počet znaků, které se mohou objevit v hodnotách naskenovaných pomocí tohoto identifikátoru aplikace. Pokud je zaškrtnuto políčko **Pevná délka**, očekává se přesně tento počet znaků.
    - **Typ** – Vyberte typ hodnoty, která se má skenovat pomocí tohoto identifikátoru aplikace (*Číselný*, *Alfanumerický* nebo *Datum*). Další informace o tom, jak jsou data a čísla reprezentována v datech čárového kódu, viz sekci [Data a desetinná čísla](#dates-and-decimal-numbers).
    - **Desetinný** – Toto políčko zaškrtněte, pokud hodnota obsahuje implicitní desetinnou čárku. Pokud je toto pole zaškrtnuto, systém použije k určení počtu desetinných míst poslední číslici identifikátoru aplikace. Další informace o tom, jak jsou data a čísla reprezentována v datech čárového kódu, viz sekci [Data a desetinná čísla](#dates-and-decimal-numbers).

> [!WARNING]
> Přestože vám systém umožní nastavit zaškrtávací políčko **Pevná délka** pro jakýkoli identifikátor aplikace, mělo by být použito pouze pro podmnožinu identifikátorů aplikace, které mají předdefinovanou délku podle obecných specifikací GS1. Vylepšený analyzátor GS1 již obsahuje seznam všech identifikátorů aplikací, které mají předdefinované délky.

> [!NOTE]
> Hodnota **Oddělovač skupin**, která je uvedena na stránce **Parametry správy skladu**, je volitelná, pokud má hodnota, za kterou následuje identifikátor aplikace, pevnou délku.

## <a name="establish-the-generic-gs1-setup"></a><a name="generic-gs1-setup"></a>Vytvoření obecného nastavení GS1

Obecné nastavení GS1 vytváří kolekci běžných mapování. Tato mapování srovnají každé relevantní vstupní pole v mobilní aplikaci s identifikátorem aplikace, který řídí, jak by měly být hodnoty z naskenovaných čárových kódů interpretovány a ukládány do tohoto pole. Ve výchozím nastavení se tato nastavení vztahují na všechna skenování pro všechny položky nabídky mobilního zařízení. Lze je však přepsat pro jedno nebo více konkrétních polí zásadou GS1, která je přiřazena konkrétní položce nabídky.

Obecné nastavení GS1 umožňuje skenovat pouze jednu hodnotu najednou. Pokud tedy chcete načíst více hodnot polí z jednoho skenování, musíte pro příslušné položky nabídky nastavit zásadu GS1.

Další informace o zásadách GS1 naleznete v další části.

### <a name="load-the-standard-generic-gs1-setup"></a>Načtení standardního obecného nastavení GS1

Stránka **Obecné nastavení GS1** umožňuje načíst standardní sadu mapování mezi poli mobilního zařízení a standardními identifikátory aplikace, které jsou vytvořeny výchozím nastavením.

Chcete-li vytvořit obecné nastavení GS1, přejděte na nabídku **Správa skladu \> Nastavení \> GS1 \> Obecné nastavení GS1**. Poté vyberte příkaz **Vytvořit výchozí nastavení**, aby se automaticky přiřadil vhodný identifikátor aplikace ke každému poli, které obvykle používají položky nabídky mobilního zařízení.

> [!WARNING]
> Pokud již nějaké obecné nastavení GS1 existuje, příkaz **Vytvořit výchozí nastavení** jej zcela odstraní a načte standardní nastavení.

### <a name="customize-the-standard-generic-gs1-setup"></a>Přizpůsobení standardního obecného nastavení GS1

Chcete-li přizpůsobit obecné nastavení GS1, postupujte takto.

1. Přejděte do nabídky **Správa skladu \> Nastavení \> GS1 \> Obecné nastavení GS1**.
1. Proveďte jeden z následujících kroků:

    - Vytvoření nového mapování: V podokně Akce vyberte možnost **Nová**.
    - Chcete-li upravit existující mapování: Vyberte mapování a poté v podokně akcí vyberte **Upravit**.

1. Nastavte následující pole pro nové nebo vybrané mapování:

    - **Pole** – Vyberte nebo zadejte vstupní pole mobilní aplikace, ke kterému má být přiřazena příchozí hodnota. Hodnota není zobrazovaný název, který vidí pracovníci. Je to název klíče, který je přiřazen poli v podkladovém kódu. Výchozí nastavení poskytuje kolekci polí, která budou pravděpodobně užitečná, a obsahuje intuitivní názvy klíčů pro každé pole a odpovídající naprogramované funkce. Možná však budete muset promluvit se svými vývojovými partnery, abyste našli správný výběr pro vaši implementaci.
    - **Identifikátor aplikace** – Vyberte příslušný identifikátor aplikace, jak je definován na stránce **Identifikátory aplikace GS1**. Identifikátor určuje, jak bude čárový kód interpretován a uložen jako hodnota pojmenovaného pole. Poté, co vyberete identifikátor aplikace, zobrazí pole **Popis** jeho popis.

## <a name="set-up-gs1-policies-to-be-to-mobile-device-menu-items"></a><a name="policies-for-menus"></a>Nastavení zásad GS1, aby byly položkami nabídky mobilního zařízení

Účelem standardu GS1 je umožnit pracovníkům načíst najednou několik hodnot při skenování jednoho čárového kódu. K dosažení tohoto cíle musejí logističtí manažeři nastavit zásady GS1, které systému řeknou, jak interpretovat vícehodnotové čárové kódy. Později můžete k položkám nabídky mobilního zařízení přiřadit zásady a řídit tak, jak bude čárový kód interpretován, když jej pracovníci skenují prostřednictvím konkrétní položky nabídky.

Pokud k položce nabídky není přiřazena žádná zásada GS1, systém může zachytit pouze jednu hodnotu. Tato hodnota je použita na vstupu mobilní aplikace, který je vybrán, když pracovník provede skenování, jak je uvedeno v obecném nastavení GS1. Pokud je k položce nabídky přiřazena zásada GS1, systém stále používá obecné nastavení GS1 k mapování první hodnoty čárového kódu do vybraného pole. Může však poté zachytit další hodnoty polí, jak je uvedeno v příslušných zásadách.

### <a name="load-the-standard-specific-gs1-policies"></a>Načtení standardních specifických zásad GS1

Chcete-li začít rychle, můžete načíst sadu zásad GS1. Zásady pak můžete podle potřeby později rozšířit nebo upravit.

Chcete-li načíst standardní identifikátory aplikace, postupujte takto.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> GS1 \> Zásada GS1**.
1. V podokně akcí vyberte **Vytvořit výchozí nastavení**.

> [!WARNING]
> Příkaz **Vytvořit výchozí nastavení** odstraní všechny aktuálně definované zásady a nahradí je standardní sadou zásad. Po načtení výchozího nastavení však můžete zásady přizpůsobit podle potřeby.

### <a name="set-up-custom-specific-gs1-policies"></a>Nastavení vlastních specifických zásad GS1

> [!WARNING]
> Některé zásady GS1 nemusí fungovat se všemi mobilními toky, které používáte. Když konfigurujete vlastní zásady GS1, musíte otestovat tok mobilního zařízení pomocí různých informací, které jsou naskenovány v různých bodech toku. Tímto způsobem můžete určit, zda se tok chová, jak očekáváte.

Chcete-li nastavit a přizpůsobit své zásady GS1, postupujte takto.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> GS1 \> Zásada GS1**.
1. Proveďte jeden z následujících kroků:

    - Vytvoření nové zásady: V podokně Akce vyberte možnost **Nová**.
    - Chcete-li upravit existující zásadu, vyberte ji v podokně seznamu.

1. V záhlaví nové nebo vybrané zásady nastavte následující pole:

    - **Název zásady** – Zadejte název zásady.
    - **Popis** – Zadejte krátký popis zásady.

1. Na záložce pod záhlavím namapujte názvy polí na identifikátory aplikace podle toho, jak to vyžaduje aktuální zásada. Pomocí tlačítek na panelu nástrojů můžete podle potřeby přidávat a odebírat řádky. Pro každý řádek je třeba nastavit tato pole:

    - **Pole** – Vyberte nebo zadejte vstupní pole mobilní aplikace, ke kterému má být přiřazena příchozí hodnota. Hodnota není zobrazovaný název, který vidí pracovníci. Je to název klíče, který je přiřazen poli v podkladovém kódu. Výchozí nastavení poskytuje kolekci polí, která budou pravděpodobně užitečná, a obsahuje intuitivní názvy klíčů pro každé pole a odpovídající naprogramované funkce. Možná však budete muset promluvit se svými vývojovými partnery, abyste našli správný výběr pro vaši implementaci.
    - **Identifikátor aplikace** – Vyberte příslušný identifikátor aplikace, jak je definován na stránce **Identifikátory aplikace GS1**. Identifikátor určuje, jak bude čárový kód interpretován a uložen jako hodnota pojmenovaného pole. Poté, co vyberete identifikátor aplikace, zobrazí pole **Popis** jeho popis.
    - **Třídění** – Každý vícehodnotový čárový kód obsahuje řadu identifikátorů aplikace a za každým z nich následuje hodnota. Příslušná zásada GS1 určuje, jak jsou jednotlivé identifikátory aplikace namapovány na pole databáze. Pokud však čárový kód používá stejný identifikátor aplikace více než jednou, systém při jejich mapování na pole použije pořadí, ve kterém se identifikátory aplikací objeví v kódu. U řádků, které sdílejí identifikátor aplikace s jedním nebo více dalšími řádky, použijte toto pole k určení pořadí, ve kterém se zpracovávají odpovídající řádky. Nejprve bude zpracován řádek, který má nejnižší hodnotu řazení.

> [!NOTE]
> U čárových kódů, které obsahují více než jeden identický identifikátor aplikace, *musíte* použít pole **Třídění** pro stanovení pořadí polí.

## <a name="assign-gs1-policies-to-mobile-device-menu-items"></a>Přiřazení zásad GS1 k položkám nabídky mobilního zařízení

Ve výchozím nastavení všechny položky nabídky mobilního zařízení poskytují vstupní pole, kde mohou pracovníci skenovat jednu hodnotu podle obecného nastavení GS1. Pokud chcete, aby pracovníci mohli skenovat více než jednu hodnotu pole v jednom skenování pro libovolnou položku nabídky mobilního zařízení, musíte přiřadit zásady GS1 podle těchto kroků.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. Vytvořte nebo otevřete položku nabídky.
1. Na záložce **Všeobecné** nastavte pole **Zásada GS1** na zásadu, která se vztahuje na položku nabídky.

## <a name="gs1-setup-example"></a>Příklad nastavení GS1

Tento příklad platí pro systém, kde jsou možnosti GS1 nastaveny následujícím způsobem:

- Na stránce **Parametry správy skladu** se vytvoří následující globální nastavení:

    - **Znak FNC1:** *\]C1*
    - **Oddělovač skupin:** *\~*

- Na stránce **Identifikátory aplikace GS1** jsou pro tento příklad relevantní následující identifikátory aplikace.

    | Identifikátor aplikace | popis | Pevná délka | Délka | Typ | Desetinné |
    |---|---|---|---|---|---|
    | 01 | Číslo GTIN | Vybrané | 14 | Číselné | Proplaceno |
    | 10 | Číslo dávky | Proplaceno | 20 | Alfanumerické | Proplaceno |
    | 17 | Datum vypršení platnosti | Vybrané | 6 | Datum | Proplaceno |
    | 30 | Přijaté množství | Proplaceno | 8 | Číselné | Proplaceno |

- Na stránce **Obecné nastavení GS1** jsou pro tento příklad relevantní následující nastavení pro obecné zásady GS1.

    | Pole | Identifikátor aplikace | popis |
    |---|---|---|
    | ItemId | 01 | Číslo GTIN |

- Na stránce **Zásady GS1** najdete zásadu, jejíž pole **Název zásady** je nastaveno na *Příjem nákupu*. Tato zásada obsahuje následující řádky.

    | Pole | Identifikátor aplikace | popis | Třídění |
    |---|---|---|---|
    | ExpDate | 17 | Datum vypršení platnosti | 0 |
    | InventBatchId | 10 | Číslo dávky | 0 |
    | Množství | 30 | Přijaté množství | 0 |

- Na stránce **Položky nabídky mobilního zařízení** je položka nabídky s názvem *Příjem nákupu*. Její pole **Zásada GS1** je nastaveno na *Příjem nákupu*.

Poté, co zboží pro nákupní objednávku dorazí do skladu, pracovník postupuje podle těchto kroků.

1. V mobilním zařízení vybere položku nabídky **Příjem nákupu**.
1. Zadá číslo nákupní objednávky.
1. Vybere pole **Položka** a naskenuje následující čárový kód: `]C10100000012345678~3030~10b1~17220215`.

Na základě nastavení, která jsou pro tento příklad vytvořena, systém analyzuje naskenovaný čárový kód následujícím způsobem.

| ID pole | ID aplikace | Hodnota | Poznámka |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Protože pracovník skenoval údaj do pole **Položka**, je do tohoto pole namapována první hodnota v čárovém kódu. Mapování je převzato z obecného nastavení GS1. |
| Množství | 30 | 30 | Protože je v jednom skenování zachyceno několik hodnot polí, toto mapování a všechna zbývající mapování jsou převzata ze zásady GS1, která je přiřazena položce nabídky **Příjem nákupu**. Tato hodnota je množstvím, které bylo přijato. |
| InventBatchId | 10 | b1 | Tato hodnota je ID dávky. |
| ExpDate | 17 | 220215 | Formát data je RRMMDD. Proto je datum vypršení platnosti 15. února 2022. |

Účtenka se poté zaregistruje a po jednom skenování se zadají příslušné hodnoty do databáze.
