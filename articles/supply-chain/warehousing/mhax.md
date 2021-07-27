---
title: Rozhraní vybavení manipulace s materiálem (MHAX)
description: Toto téma popisuje, jak nastavit rozhraní zařízení pro manipulaci s materiálem (MHAX), abyste se mohli připojit k externím systémům pro manipulaci s materiálem (MH).
author: Mirzaab
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMHEParameters, WMHESubscription, WMHEQueueManagerWorkspace, WMHEInboundQueue, WMHEOutboundQueue
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: db58e3d1a6665d15ad2f3ac25612ecbf448a9c17
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344189"
---
# <a name="material-handling-equipment-interface-mhax"></a>Rozhraní vybavení manipulace s materiálem (MHAX)

[!include [banner](../../includes/banner.md)]

Můžete použít *rozhraní zařízení pro práci s materiálem* (MHAX) pro připojení externích systémů pro práci s fyzickým materiálem (MH) do skladu, který je spravován pomocí pokročilé správy skladu (WMS) v Microsoft Dynamics 365 Supply Chain Management. Rozhraní mezi systémy WMS a MH se skládá ze dvou front: jedné pro odchozí události (WMS na MH) a jedné pro příchozí události (MH na WMS). Systém WMS generuje odchozí události na základě řádků práce, které jsou vytvořeny během různých procesů vytváření a provádění prací. Systém MH poté pravidelně dotazuje systém WMS na nové události a zpracovává odpovědi. Poté, co systém MH dokončí zpracování událostí v souladu s pracovními pokyny, odešle příchozí události, jako je dokončení řádků práce a krátké vyzvednutí.

Následující obrázek ukazuje různé prvky a pořadí, ve kterém dochází k procesům při použití integrace MHAX.

![Složky a interakce MHAX.](media/mhax-components.png "Složky a interakce MHAX")

Zde je vysvětlení interakcí, které jsou zobrazeny na předchozím obrázku:

1. Během vytváření nebo provádění práce se ve výstupní frontě vytvářejí odchozí události.
2. Zařízení MH se připojuje ke službě zařízení MH, dotazuje se na všechny nové události, které se ho týkají, a zpracovává tyto události.
3. Když je zařízení MH připraveno hlásit zpět, znovu se připojí ke službě a odešle příchozí události. Tyto události jsou okamžitě zpracovány procesorem fronty.
4. Na základě dat příchozí události může procesor fronty spouštět existující práci, upravovat ji nebo vytvářet novou práci.

## <a name="turn-on-the-mhax-feature"></a>Zapnutí funkce MHAX

Než budete moci používat funkci MHAX, musíte zapnout její funkci i její konfigurační klíč.

1. Přejděte do nabídky **Správa systému \> Pracovní prostory \> Správa funkcí**.
2. V pracovním prostoru **[Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** zapněte funkci s názvem *Rozhraní zařízení pro práci s materiálem*.
3. Uveďte systém do režimu údržby, jak je popsáno v tématu [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
4. Přejděte do nabídky **Správa systému \> Nastavení \> Konfigurace licence**.
5. Rozbalte **Obchod \> Řízení skladu a dopravy** a potom zaškrtněte políčko **Rozhraní zařízení pro práci s materiálem**.
6. Vypněte režim údržby, jak je popsáno v tématu [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

## <a name="set-mhax-parameters"></a>Nastavení parametrů MHAX

Musíte nastavit několik obecných parametrů na stránce **Parametry rozhraní zařízení pro práci s materiálem** pro konfiguraci funkce.

1. Přejděte na **Rozhraní zařízení pro práci s materiálem \> Nastavení \> Parametry rozhraní zařízení pro práci s materiálem**.
2. Na kartě **Obecné** natavte následující pole:

    - **ID Uživatele** - Vyberte pracovníka. Tento pracovník bude použit ke spuštění všech pracovních operací (výběrů a vložení), které jsou zpracovány prostřednictvím příchozí fronty.
    - **Povolit ID příchozí zprávy** - Když je tato možnost nastavena na *Ano*, pokud je přijato duplicitní ID příchozí zprávy, bude zpráva odmítnuta a v chybové zprávě bude uvedeno, že zpráva již existuje. Když je tato možnost nastavena na *Ne*, budou povolena duplicitní ID příchozích zpráv.

3. Na kartě **Číselné řady** vyberte celočíselné řady, které by se měly použít ke generování jedinečných ID pro položky příchozí fronty, položky odchozí fronty a páry pracovních řádků.

## <a name="outbound-events"></a>Odchozí události

V určitých bodech během vytváření nebo provádění práce systém určuje, zda musí generovat odchozí události, které se mají odeslat do systému MH. Pokud je předplatné nakonfigurováno pro konkrétní bod během zpracování skladu, systém generuje událost podle nastavení předplatného.

### <a name="structure-of-outbound-events"></a>Struktura odchozích událostí

Každá odchozí událost je jednoznačně identifikována ID odchozí fronty. Typ odchozí transakce určuje typ události. Sklad a ID předplatného, které generovalo událost, se také zaznamenají na událost.

K přenosu dat do systému MH obsahuje odchozí událost 10 polí pro data (**data01** přes **data10**). Tato datová pole mají mapování 1: 1 (1: 1) na existující pole databáze. Konkrétně jsou extrahována z polí v tabulce pracovních řádků a pracovních záhlaví. Pole lze libovolně vybrat. Nastavíte je při vytváření předplatného.

Kromě 10 datových polí, která mají mapování 1: 1 na existující databázová pole, může událost obsahovat další datové pole, které je známé jako *datová část*. Obsah tohoto pole je generován vlastním kódem X ++, který je známý jako *generátor datové části*. V předplatném je nastaven jakýkoli generátor datové části, který by měl být použit.

Aby bylo zajištěno, že systém MH obdrží každé ID odchozí fronty pouze jednou, použije se stavové pole k určení, zda je událost připravena k odeslání do externího systému nebo zda již byla odeslána.

### <a name="outbound-queue-subscriptions"></a>Předplatné odchozí fronty

Před generováním událostí je třeba nastavit předplatné, které funkci MHAX řekne, zda a jak generovat události. Generované události jsou označeny identifikátorem předplatného. Proto se více systémů MH může připojit ke stejnému systému WMS, ale jejich události jsou oddělené. Když je služba MHAX dotazována na nové události, je předplatné jednou z dostupných možností pro načtení událostí.

Chcete-li vytvořit předplatné, přejděte na **Rozhraní zařízení pro manipulaci s materiálem \> Nastavení \> Předplatné**. U každého předplatného jsou k dispozici následující parametry:

- **ID předplatného** – Jedinečný název, který identifikuje předplatné.
- **Popis** – Volný textový popis předplatného.
- **Sklad** - Konkrétní sklady, podle kterých by měly být události filtrovány.
- **Typ odchozí transakce** - Typ událostí, které by předplatné mělo obsahovat.
- **Generátor užitečného zatížení** - Volitelné rozšíření kódu, které umožňuje zadat další informace do pole **Užitečné zatížení** odchozí události.

Ke každému předplatnému lze přiřadit dotaz. Tento dotaz filtruje pracovní řádky a záhlaví, aby dále omezil práci, která bude používat předplatné ke generování událostí. Chcete-li přidat dotaz k předplatnému, vyberte zaškrtávací políčko **Spustit dotaz** pro příslušné předplatné na stránce **Předplatné** a poté vyberte **Upravit dotaz** v podokně akcí. Zobrazí se standardní editor dotazů Supply Chain Management.

Předplatné navíc zahrnuje *mapu předplatného*, která mapuje pole z hlavičky práce nebo řádku práce na některá nebo všechna 10 volných datových polí odchozí události, jak je požadováno. Chcete-li vrátit informace službě MHAX, obvykle uvedete ID záznamu na řádku práce nebo *ID dvojice řádků práce*. (ID dvojice řádků práce je nová vlastnost, která umožňuje systému použít jediný návratový příkaz ke zpracování řádků výběru and vložení.) Zbývající pole závisí na případu použití. Některé příklady jsou uvedeny dále v tomto tématu.

Chcete-li nastavit mapu předplatného, vyberte příslušné předplatné na stránce **Předplatné** a poté vyberte **Mapa předplatného** v podokně akcí. V zobrazeném dialogovém okně **Mapa předplatného** můžete každému dostupnému datovému poli podle potřeby přiřadit tabulku a pole.

### <a name="outbound-event-types"></a>Typy odchozích událostí

Tato část popisuje různé typy událostí, které jsou k dispozici. (Typy událostí jsou také známé jako *typy transakcí*.) Rovněž vysvětluje, kdy je každý typ události vytvořen v systému WMS.

#### <a name="work-creation-events"></a>Události vytvoření práce

Události vytvoření práce se vytvářejí poté, co aplikace vygeneruje práci. Toto chování se vztahuje na většinu typů procesů vytváření prací, zejména na vytváření prací na vychystávání a doplňování. Obecně platí, že pokud je práce vytvořena ve stavu *Otevřeno*, který označuje, že práce je připravena ke spuštění pracovníkem, bude vygenerována událost vytvoření práce. Kromě toho budou generovány události vytváření prací pro základní práci pohybu (nikoli pohyb podle šablony), přestože tato práce není vytvořena jako otevřená práce.

Pozoruhodnou výjimkou z tohoto chování je práce s počítáním cyklů, která momentálně není podporována. Počty zásob v systému MH jsou mimo rozsah MHAX a výsledky počtů musí být importovány do deníku počítání zásob.

Po vytvoření práce služba MHAX zpracuje generované řádky práce a každému vygenerovanému řádku přiřadí každému vygenerovanému řádku práce ID dvojice řádků práce. Cílem je seskupit všechny vybrané řádky práce s postupným vložením pod jedno ID dvojice řádků práce. (Skupiny odpovídají párům výběru / vložení v šablonách práce.) Tímto způsobem lze použít jediné ID k hlášení dokončení práce pro všechny související řádky výběru a vložení. Proces seskupování začíná prvním řádkem a poté pokračuje se stejným ID, dokud nenarazí na postupnou dvojici pracovních / vložení / výběru řádků práce. Běžící ID je přiřazeno k řádce výběru této dvojice. Nové ID je poté použilo pro řádek výběru dvojice dále. Tento proces pokračuje, dokud nezpracuje všechny řádky, které patří do záhlaví práce.

Speciální funkcí událostí vytvoření práce je nastavení možnosti **Blokovaná vlna** na *Ano* v záhlaví práce, generované události budou mít stav *Blokováno* místo obvyklého stavu *Připraveno*, který se používá k jejich odeslání do systému MH. Příznak **Blokovaná vlna** v hlavičce práce označuje, že hlavička práce ještě není připravena ke spouštění pracovníků, pravděpodobně kvůli nedokončené práci doplňování. Když je příznak **Blokovaná vlna** zrušen, události, které již byly vygenerovány, jsou odblokovány a jsou k dispozici systému MH k načtení z fronty.

#### <a name="work-initiation-events"></a>Události zahájení práce

Události zahájení práce se aktivují, když se změní stav práce z *Otevřeno* na *Zpracovává se* během aktualizace práce.

#### <a name="work-completion-events"></a>Události dokončení práce

Události dokončení práce se aktivují, když se změní stav práce z *Zpracovává se* na *Uzavřeno* během aktualizace práce.

#### <a name="work-cancellation-events"></a>Události zrušení práce

Události zrušení práce se aktivují, když se změní stav práce z libovolného stavu mezi *Uzavřeno* na *Zrušeno* během aktualizace práce. Kromě toho jsou všechny ostatní události související s hlavičkou práce odstraněny z fronty všech předplatných. Tímto způsobem je zabráněno externím systémům ve zpracování událostí, které nejsou vyžadovány.

#### <a name="pickput-completion-events"></a>Události dokončení vyzvednutí/vložení

Události vyzvednutí/vložení se aktivují, když se změní stav práce ze *Zpracovává se* na *Uzavřeno* během aktualizace řádku práce.

### <a name="monitor-the-outbound-queue"></a>Monitorování odchozí fronty

Chcete-li zkontrolovat svou odchozí frontu, přejděte na **Rozhraní zařízení pro práci s materiálem \> Společné \> Odchozí fronta**. Stránka **Odchozí fronta** uvádí každou položku odchozí fronty a její stav. Výběrem položky fronty zobrazíte její podrobnosti. Mezi tyto podrobnosti patří typ transakce položky, předplatné, které se použilo, a hodnoty pro každé datové pole (**data01** přes **data10**) a užitečné zatížení.

### <a name="clean-up-the-outbound-queue"></a>Vyčištění odchozí fronty

Nakonec se vaše odchozí fronta začne zaplňovat položkami fronty, které již byly odeslány. Chcete-li tyto položky odstranit, přejděte na **Rozhraní zařízení pro práci s materiálem \> Pravidelné úkoly \> Vyčištění \> Vyčištění odchozí fronty**.

## <a name="inbound-events"></a>Příchozí události

Tato část popisuje různé typy příchozích událostí, které může systém MH hlásit zpět do systému WMS. Vysvětluje také, že data musí být dodána systémem MH a co každá příchozí událost dělá v systému WMS.

### <a name="structure-of-inbound-events"></a>Struktura příchozích událostí

Při odeslání příchozí události musí externí systém dodat typ příchozí transakce až s 10 parametry (**data01** přes **data10**). Volitelné ověření může zajistit, že služba MHAX neobdržela stejnou příchozí událost více než jednou. Chcete-li povolit toto ověření, musí mít každá příchozí událost jedinečné ID zprávy. Pokud obdržíte duplicitní ID zprávy a pokud je možnost **Povolit ID příchozí zprávy** nastavena na *Ano* na stránce **Parametry rozhraní zařízení pro práci s materiálem**, bude zpráva odmítnuta. Chybová zpráva bude uvádět, že zpráva již existuje.

Kromě příchozích datových polí systém přiřadí události jedinečné ID příchozí fronty.

### <a name="inbound-event-types"></a>Typy příchozích událostí

Tato část popisuje typy příchozích událostí (typy transakcí), které jsou podporovány, a data, která je nutné zadat pro zpracování událostí.

#### <a name="work-confirm-events"></a>Události potvrzení práce

Události potvrzení práce vyžadují, aby příchozí datová pole obsahovala následující informace:

- **data01** - ID dvojice řádků práce.
- **data02** - ID záznamu řádku práce (hodnota `RecId`).

    > [!NOTE]
    > *Musí být přítomno* pole **data01** *nebo* pole **data02**.

- **data03** - ID registrační značky, ze které si můžete vybrat.
- **data04** - ID cílové registrační značky hlavičky práce.

Pokud je zadáno ID dvojice hlavičky práce, všechny vybrané, vložené nebo vlastní pracovní řádky, které jsou označeny ID dvojice pracovních řádků a které mají stav *Otevřeno* nebo *Zpracovává se*, jsou spouštěny postupně. Pokud je poskytnuto ID záznamu v řádku práce (hodnota `RecId`), řádek práce musí být vyzvednutí, výdej nebo vlastní řádek práce, který má stav *Otevřeno* nebo *Zpracovává se*.

Řádky výdeje z pozic řízených registrační značkou vyžaduje, aby hodnota **data03** specifikovala registrační značku, ze které by se mělo vybírat, bez ohledu na to, zda jsou řádky označeny ID záznamu řádku práce nebo ID dvojice řádků práce. Pole **data04** musí specifikovat cílovou poznávací značku záhlaví práce pro výběr.

Řádky vyskladnění nepřijímají další informace. Jsou spouštěny pouze na základě umístění aktuálního řádku práce a registrační značky cíle práce. Pokud je nutné provést vyskladnění na jiné místo, změňte umístění řádku práce podle popisu v části [Přepis událostí](#override-events) dále v tomto tématu.

Vlastní řádky práce nevyžadují ani nepodporují žádné další informace v příchozí události.

#### <a name="short-pick-events"></a>Události rychlého výběru

Události rychlého výběru vyžadují, aby příchozí datová pole obsahovala následující informace:

- **data02** - ID záznamu práce (hodnota `RecId`).
- **data03** - ID registrační značky, ze které si můžete vybrat.
- **data04** – Množství k výběru.
- **data05** - Kód výjimky pro krátký výběr.
- **data06** - ID cílové registrační značky hlavičky práce.

> [!NOTE]
> Pole **data01** se nepoužívá pro události rychlého výběru.

Tato událost se podobá události potvrzení práce, ale vztahuje se pouze na řádky výběru.

#### <a name="override-events"></a><a id="override-events"></a>Události přepisu

Události přepisu vyžadují, aby příchozí datová pole obsahovala následující informace:

- **data01** - ID záznamu práce (hodnota `RecId`).
- **data02** - Nové ID místa.

Řádek práce musí mít stav buď *Otevřeno* nebo *Zpracovává se* a musí existovat nové umístění.

#### <a name="license-plate-receipt-events"></a>Události přijetí registrační značky

Události přijetí registrační značky vyžadují, aby příchozí datová pole obsahovala následující informace:

- **data01** - ID příchozí registrační značky pro přijetí.

Systém provádí operaci příjmu registrační značky na základě registrační značky, která je předána jako hodnota pole **data01**.

### <a name="monitor-the-inbound-queue"></a>Monitorování příchozí fronty

Chcete-li zkontrolovat svou příchozí frontu, přejděte na **Rozhraní zařízení pro práci s materiálem \> Společné \> příchozí fronta**. Stránka **příchozí fronta** uvádí každou položku příchozí fronty a její stav. Výběrem položky fronty zobrazíte její podrobnosti. Mezi tyto podrobnosti patří typ transakce položky, ID zprávy a hodnoty pro každé datové pole (**data01** přes **data10**).

Pokud během zpracování příchozích událostí došlo k chybě nebo jinému typu položky protokolu, můžete protokol zkontrolovat výběrem možnosti **Protokol chyb** v podokně akcí.

### <a name="inbound-event-processing"></a>Zpracování příchozí události

Příchozí události se nejprve zapíší do databáze a poté se okamžitě (synchronně) spustí. Pokud během zpracování dojde k chybě, událost je přesto zapsána do fronty, ale stav je nastaven na *Chyba*. Služba MHAX vrátí chybovou zprávu do systému MH a uloží protokol chyb do záznamu příchozí události pro pozdější zkoumání.

Události se stavem *Chyba* lze znovu zpracovat později, pokud je chybový stav opraven. Chcete-li je znovu zpracovat, proveďte některý z následujících kroků:

- Přejděte na **Rozhraní zařízení pro práci s materiálem \> Společné \> Příchozí fronta**. Vyberte příslušnou příchozí frontu a poté vyberte **Znovu zpracovat** v podokně akcí.
- Přejděte na **Rozhraní zařízení pro práci s materiálem \> Společné \> Znovu zpracovat chybnou příchozí frontu**. Zobrazí se standardní dialogové okno dávkové úlohy. Zde můžete nastavit filtr záznamů a naplánovat nebo spustit dávkovou úlohu pro opětovné zpracování fronty.

Všechny pracovní operace (výběry a vložení) jsou spouštěny s využitím pracovníka, který je vybrán v poli **ID uživatele** na stránce **Parametry rozhraní zařízení pro práci s materiálem**.

### <a name="clean-up-the-inbound-queue"></a>Vyčištění příchozí fronty

Nakonec se příchozí fronta začne zaplňovat položkami fronty, které již byly zpracovány. Chcete-li tyto položky odstranit, přejděte na **Rozhraní zařízení pro práci s materiálem \> Pravidelné úkoly \> Vyčištění \> Vyčištění příchozí fronty**.

## <a name="get-a-quick-overview-by-using-the-queue-manager"></a>Získání rychlého přehledu pomocí správce front

Chcete-li získat rychlý přehled o všech aktivitách, které souvisí s vašimi příchozími a odchozími frontami, přejděte na **Rozhraní zařízení pro práci s materiálem \> Pracovní prostory \> Správce front**. Stránka **Správce front** obsahuje sadu karet a dlaždic, které můžete použít k monitorování a prozkoumání vašich front. Poskytuje také užitečné odkazy na většinu dalších stránek zmíněných v tomto tématu.

## <a name="connect-to-the-mhax-service"></a>Připojení ke službě MHAX

MHAX je implementován jako vlastní služba. Proto je přístupný prostřednictvím volání SOAP a REST. Zde jsou adresy koncových bodů SOAP a REST:

- **SOAP:** `https://base_environment_URL/soap/services/WMHEServices`
- **REST:** `https://base_environment_URL/api/services/WMHEServices/WMHEService`

## <a name="retrieve-messages-from-the-outbound-queue"></a>Načíst zprávy z odchozí fronty

Chcete-li načíst zprávy z odchozí fronty, použijte jednu z následujících metod:

- Použijte `readOutboundSubscriptionQueue` k načtení událostí na základě ID předplatného.
- Použijte `readOutboundWarehouseQueue` k načtení událostí na základě typu události a ID skladu napříč více předplatnými.
