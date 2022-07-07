---
title: Nastavení prognózy poptávky
description: Tento článek popisuje úlohy nastavení, které je třeba provést, aby bylo možné používat prognózy poptávky.
author: t-benebo
ms.date: 11/23/2021
ms.topic: article
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fae2ac53dec8696075e7506d979c1cf9fb277af5
ms.sourcegitcommit: d98ecbd9457197ec8f8e281f9c2f24dcce7b8269
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/14/2022
ms.locfileid: "8960128"
---
# <a name="demand-forecasting-setup"></a>Nastavení prognózy poptávky

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak nastavit prognózu poptávky.  

## <a name="item-allocation-keys"></a>Alokační klíče pro položky

Alokační klíče položek vytvářejí skupiny položek. Prognóza poptávky se vypočítá pro položku a její dimenze pouze v případě, že položka je součástí alokačního klíče položky. Toto pravidlo je vynuceno pro seskupení velkého počtu položek tak, abyste prognózy poptávky mohli vytvářet rychleji. Prognózy se vytváří pouze podle historických dat.

Položka a její dimenze musí být součástí pouze jednoho alokačního klíče položky, pokud se alokační klíč položky používá při vytváření prognózy.

Chcete-li vytvořit alokační klíče položek a přidat k nim skladovou jednotku (SKU), postupujte takto.

1. Přejděte do uzlu **Hlavní plánování \> Nastavení \> Prognóza poptávky \> Alokační klíče pro položky**.
1. Buď vyberte alokační klíč polohy v podokně seznamu, nebo vyberte v podokně akcí možnost **Nový** a vytvořte nový. V záhlaví nový nebo vybraný klíč nastavte následující pole:

    - **Alokační klíč položky** – Zadejte jedinečný název klíče.
    - **Název** – Zadejte popisný název klíče.

1. Chcete-li přidat položky do vybraného alokačního klíče položek nebo položky odebrat, postupujte podle jednoho z těchto kroků:

    - Na rychlé kartě **Alokace položky** pomocí tlačítek **Nový** a **Odstranit** na panelu nástrojů přidejte nebo odeberte podle potřeby položky. Pro každý řádek vyberte číslo položky a podle potřeby přiřaďte hodnoty dimenzí v ostatních sloupcích. Vyberte **Zobrazit dimenze** na panelu nástrojů, chcete-li změnit sadu sloupců dimezne zobrazených v mřížce. (Hodnota ve sloupci **Procento** je při generování prognóz poptávky ignorována.)
    - Pokud chcete do klíče přidat velký počet položek, vyberte **Přiřadit položky** na podokně akcí a otevřete stránku, kde můžete najít a přiřadit více položek k vybranému klíči.

> [!IMPORTANT]
> Dejte pozor, abyste do každého alokačního klíče položky zahrnuli pouze relevantní položky. Zbytečné položek mohou způsobit zvýšení nákladů při použití služby strojového učení Microsoft Azure.

## <a name="intercompany-planning-groups"></a>Skupiny mezipodnikového plánování

Prognóza poptávky může vygenerovat prognózy mezi více společnostmi. V aplikaci Dynamics 365 Supply Chain Management jsou společnosti, které jsou plánovány společně, seskupeny do stejné skupiny pro mezipodnikové plánování. Chcete-li u každé společnosti určit, které alokační klíče položek by měly být brány v úvahu při prognózování poptávky, přiřaďte alokační klíč položek k členu mezipodnikové plánovací skupiny.

> [!IMPORTANT]
> Optimalizace plánování v současnosti nepodporuje mezipodnikové plánovací skupiny. Chcete-li provádět mezipodnikové plánování, které využívá optimalizaci plánování, nastavte dávkové úlohy hlavního plánování, které zahrnují hlavní plány pro všechny relevantní společnosti.

Chcete-li nastavit mezipodnikové plánovací skupiny, postupujte následujícím způsobem.

1. Přejděte na **Hlavní plánování \> Nastavení \> Skupiny mezipodnikového plánování**.
1. Buď vyberte plánovací skupinu v podokně seznamu, nebo vyberte v podokně akcí možnost **Nový** a vytvořte novou. V záhlaví nové nebo vybrané skupiny nastavte následující pole:

    - **Název** – Zadejte jedinečný název plánovací skupiny.
    - **Popis** – zadejte krátký popis plánovací skupiny.

1. Na rychlé kartě **Členové mezipodnikové plánovací skupiny** pomocí tlačítek na panelu nástrojů přidejte řádek pro každou společnost (právnickou osobu), která by měla být součástí skupiny. Pro každý řádek je třeba nastavit tato pole:

    - **Právnická osoba** – Vyberte název společnosti (právnické osoby), která je členem vybrané skupiny.
    - **Plánovací sekvence** – Přiřaďte objednávku, ve které má být společnost zpracována, vzhledem k ostatním společnostem. Nejprve se zpracují nízké hodnoty. Toto pořadí může být důležité, když poptávka po jedné společnosti ovlivňuje jiné společnosti. V těchto případech by společnost, která dodává poptávku, měla být zpracována jako poslední.
    - **Hlavní plán** – Vyberte hlavní plán ke spuštění pro aktuální společnost.
    - **Automatické kopírování do statického plánu** – Zaškrtněte toto políčko, chcete-li zkopírovat výsledek plánu do statického plánu.
    - **Automatické kopírování do dynamického plánu** – Zaškrtněte toto políčko, chcete-li zkopírovat výsledek plánu do dynamického plánu.

1. Ve výchozím nastavení pokud nejsou přiřazeny žádné alokační klíče položek k členům skupiny mezipodnikového plánování, prognóza poptávky bude vypočtena pro všechny položky, které jsou přiřazeny ke všem alokačním klíčům položek ze všech společností. Další možnosti filtrování pro společnosti a alokační klíče položek jsou k dispozici v dialogovém okně **Generování statistické základní prognózy** (**Hlavní plánování \> Prognózování \> Prognóza poptávky \> Generování statistické základní prognózy**). Chcete-li přiřadit alokační klíče položek společnosti ve vybrané skupině mezipodnikového plánování, vyberte společnost a poté na rychlé kartě **Členové mezipodnikové plánovací skupiny** vyberte **Alokační klíče položek** na panelu nástrojů.

> [!IMPORTANT]
> Dejte pozor, abyste do každé mezipodnikové plánovací skupiny zahrnuli pouze relevantní klíče alokace položky. Zbytečné položek mohou způsobit zvýšení nákladů při použití služby Azure Machine Learning.

## <a name="set-up-demand-forecasting-parameters"></a><a name="parameters"></a>Nastavení parametrů prognózy poptávky

Použijte stránku **Parametry prognózování poptávky** k nastavení několika možností, které řídí, jak bude prognózování poptávky fungovat ve vašem systému.

### <a name="open-the-demand-forecasting-parameters-page"></a>Otevřete stránku parametrů prognózy poptávky

Pokud chcete nastavit parametry prognózy poptávky přejděte na **Hlavní plánování \> Nastavení \> Tvorba prognóz poptávky \> Parametry tvorby prognóz poptávky**. Vzhledem k tomu, že prognózy poptávky jsou spuštěny mezi více společnostmi, toto nastavení je globální. Jinak řečeno platí pro všechny právnické osoby (společnosti).

### <a name="general-settings"></a>Obecné nastavení

Použijte kartu **Všeobecné** stránky **Parametry prognózování poptávky** k definování obecných nastavení pro prognózování poptávky.

#### <a name="demand-forecast-unit"></a>Jednotka prognózy poptávky

Prognóza poptávky generuje prognózy ve větším množství. Je tedy nutné v poli **Jednotka prognózy poptávky** vyjádřit měrnou jednotku množství. Toto pole definuje jednotku, která bude použita pro všechny prognózy poptávky, bez ohledu na obvyklé jednotky zásob pro každý produkt. Použitím konzistentní jednotky prognózy zajistíte, že agregace a procentuální rozdělení bude dávat smysl. Další informace o agregaci a procentuálním rozdělení naleznete v tématu [Provedení ručních úprav u základní prognózy](manual-adjustments-baseline-forecast.md).

Pro každou měrnou jednotku používanou pro skladové jednotky, které jsou zahrnuty do prognózy poptávky, se ujistěte, že existuje pravidlo převodu pro měrnou jednotku a měrnou jednotku obecné prognózy, kterou vyberete zde. Při generování prognózy se zaznamená seznam položek, které nemají převod měrné jednotky. Proto můžete nastavení snadno opravit. Další informace o měrných jednotkách a jak mezi nimi převádět, viz [Správa měrných jednotek](../pim/tasks/manage-unit-measure.md).

#### <a name="transaction-types"></a>Typy transakcí

Použijte pole na rychlé kartě **Typy transakcí** a vyberte typy transakcí, které se použijí při generování prognózy základního statistiky.

Prognóza poptávky slouží k provedení prognózy u závislé i nezávislé poptávky. Například pouze pokud je možnost **Prodejní objednávka** nastavena na *Ano* a pokud všechny položky, které jsou považovány při tvorbě prognózy poptávky jsou položky, které jsou prodány, systém vypočítá nezávislou poptávku. Kritické dílčí komponenty však lze přidat k alokačním klíčům položek a zahrnout do prognózy poptávky. V takovém případě pokud je možnost **Řádek výroby** nastavena na *Ano*, vypočítá se závislá prognóza.

Typy transakcí pro jeden nebo více konkrétních alokačních klíčů položek můžete přepsat pomocí karty **Alokační klíče položek**. Tato karta poskytuje podobná pole.

#### <a name="choose-how-to-create-the-baseline-forecast"></a>Vyberte, jak vytvořit výchozí prognózu

Pole **Strategie generování předpovědi** umožňuje vybrat metodu, která se používá k vytvoření základní prognózy. K dispozici jsou tři metody:

- *Kopírovat historickou poptávku* – Vytvářejte prognózy pouhým zkopírováním historických dat.
- *Azure Machine Learning Service* – Použijte model prognózy, který používá Azure Machine Learning Service. Služba Azure Machine Learning Service je aktuální řešení strojového učení pro Azure. Proto jej doporučujeme používat, pokud chcete používat model prognózy.
- *Azure Machine Learning* – Použijte model prognózy, který používá Azure Machine Learning Service Studio (klasické). Azure Machine Learning Studio (klasické) je zastaralé a brzy bude odebráno z Azure. Proto vám doporučujeme vybrat *Azure Machine Learning Service*, pokud prognózování poptávky nastavujete poprvé. Pokud aktuálně používáte Azure Machine Learning Studio (klasické), měli byste si naplánovat přechod na Azure Machine Learning Service co nejdříve.

Metodu generování prognózy pro jeden nebo více konkrétních alokačních klíčů položek můžete přepsat pomocí karty **Alokační klíče položek**. Tato karta poskytuje podobná pole.

#### <a name="override-default-forecast-algorithm-parameters-globally"></a>Globální přepsání výchozích parametrů algoritmu prognózy

Parametry a hodnoty výchozího algoritmu prognózy jsou přiřazeny na stránce **Parametry prognózování poptávky** (**Hlavní plánování \> Nastavení \> Prognóza poptávky \> Parametry prognózování poptávky**). Můžete je však globálně přepsat pomocí rychlé karty **Parametry algoritmu prognózy** na kartě **Všeobecné** stránky **Parametry prognózování poptávky**. (Můžete je také přepsat pro konkrétní alokační klíče pomocí karty **Alokační klíče položek** na stránce **Parametry prognózování poptávky**.)

Použijte tlačítka **Přidat** a **Odebrat** na panelu nástrojů pro vytvoření požadované kolekce přepsání parametrů. Pro každý parametr v seznamu vyberte hodnotu v poli **Název** a pak zadejte příslušnou hodnotu do pole **Hodnota**. Všechny parametry, které zde nejsou uvedeny, převezmou své hodnoty z nastavení na stránce **Parametry prognózování poptávky**. Další informace o použití standardní sady parametrů a výběru hodnot pro ně naleznete v části [Výchozí parametry a hodnoty pro modely prognózování poptávky](#model-parameters).

### <a name="set-forecast-dimensions"></a>Nastavení dimenzí prognózy

Dimenze prognózy označují úroveň podrobností, pro které je prognóza definována. Společnost, pracoviště a klíč alokace položek jsou povinné dimenze prognózy. Lze rovněž vygenerovat prognózy pro sklad, stav zásob, skupinu odběratelů, účet odběratele, zemi/oblast, stát nebo položku a společně se všemi úrovněmi dimenze položky. Pomocí karty **Dimenze prognózy** na stránce **Parametry vytváření prognózy poptávky** vyberte sadu dimenzí prognózy, která se používá při generování prognózy poptávky.

Kdykoli je možné přidat dimenze prognózy na seznam dimenzí, které se používají pro tvorbu prognózy poptávky. Můžete také dimenze prognózy ze seznamu odebrat. Ruční úpravy jsou však ztraceny, pokud přidáte nebo odeberete dimenze prognózy.

### <a name="set-up-overrides-for-specific-item-allocation-keys"></a>Nastavte přepsání pro konkrétní alokační klíče položek

Ne všechny položky fungují stejným způsobem z perspektivy prognózy poptávky. Proto můžete vytvořit specifická přepsání alokačního klíče pro většinu nastavení, která jsou definována na kartě **Všeobecné**. Výjimkou je jednotka prognózy poptávky. Chcete-li nastavit přepsání pro konkrétní alokační klíč položky, postupujte takto.

1. Na stránce **Parametry prognózování poptávky** na kartě **Alokační klíče položek** pomocí tlačítek na panelu nástrojů přidejte alokační klíče položek do mřížky nalevo nebo je podle potřeby odeberte. Potom vyberte alokační klíč, pro který chcete nastavit přepsání.
1. Na rychlé kartě **Typy transakcí** povolte typy transakcí, které chcete použít ke generování statistické základní prognózy pro produkty, které patří do vybraného alokačního klíče. Nastavení fungují stejně jako na kartě **Všeobecné**, ale vztahují se pouze na vybraný alokační klíč položky. Všechna nastavení zde (hodnoty *Ano* i *Ne*) přepíší všechna nastavení **Typy transakcí** na kartě **Všeobecné**.
1. Na rychlé kartě **Parametry algoritmu prognózy** vyberte strategii generování prognózy a přepsání parametru algoritmu prognózy pro produkty, které patří do vybraného alokačního klíče. Tato nastavení fungují stejně jako na kartě **Všeobecné**, ale vztahují se pouze na vybraný alokační klíč položky. Použijte tlačítka **Přidat** a **Odebrat** na panelu nástrojů pro definování požadované kolekce přepsání parametrů. Pro každý parametr v seznamu vyberte hodnotu v poli **Název** a pak zadejte příslušnou hodnotu do pole **Hodnota**. Další informace o použití standardní sady parametrů a výběru hodnot pro ně naleznete v části [Výchozí parametry a hodnoty pro modely prognózování poptávky](#model-parameters).

### <a name="set-up-the-connection-to-the-azure-machine-learning-service"></a>Nastavte připojení ke službě Azure Machine Learning Service

Použijte kartu **Azure Machine Learning Service** a nastavte připojení ke službě Azure Machine Learning Service. Toto řešení je jednou z možností pro vytvoření základní prognózy. Tato nastavení na této kartě se projeví pouze tehdy, když je pole **Strategie generování prognózy** nastavena na *Azure Machine Learning Service*.

Další informace o tom, jak nastavit Azure Machine Learning Service a jak se k ní připojit pomocí nastavení, najdete v tématu [Nastavení Azure Machine Learning Service](#setup-amls).

### <a name="set-up-the-connection-to-azure-machine-learning-studio-classic"></a>Nastavte připojení ke službě Azure Machine Learning Studio (klasické)

> [!IMPORTANT]
> Azure Machine Learning Studio (klasické) je zastaralé. Proto už pro něj v Azure nemůžete vytvářet nové pracovní prostory. Bylo nahrazeno službou Azure Machine Learning Service, která poskytuje podobné funkce a další. Pokud ještě nepoužíváte Azure Machine Learning, měli byste začít používat Azure Machine Learning Service. Pokud už máte pracovní prostor, který byl vytvořen pro Azure Machine Learning Studio (klasické), můžete ho používat, dokud nebude funkce z Azure úplně odebrána. Doporučujeme však co nejdříve aktualizovat na Azure Machine Learning Service. Přestože vás aplikace bude i nadále upozorňovat, že Azure Machine Learning Studio (klasické) je zastaralé, výsledek prognózy to neovlivní. Další informace o nové službě Azure Machine Learning Service a jak ji nastavit, najdete v tématu [Nastavení Azure Machine Learning Service](#setup-amls).
>
> Můžete libovolně přepínat mezi používáním nových a starých řešení strojového učení pomocí Supply Chain Management, dokud bude váš starý pracovní prostor Azure Machine Learning Studio (klasický) k dispozici.

Pokud již máte dostupný pracovní prostor Azure Machine Learning Studio (klasický), můžete jej použít ke generování prognóz tím, že jej připojíte k Supply Chain Management. Toto připojení můžete vytvořit pomocí karty **Azure Machine Learning** na stránce **Parametry prognózování poptávky**. (Nastavení na této kartě se projeví pouze tehdy, když je pole **Strategie generování prognózy** nastaveno na *Azure Machine Learning* .) Zadejte následující údaje o pracovním prostoru Azure Machine Learning Studio (klasické):

- Klíč rozhraní API webové služby
- Koncový bod URL webové služby
- Název účtu úložiště Azure
- Klíč účtu úložiště Azure

> [!NOTE]
> Název účtu úložiště Azure a klíč jsou nutné pouze při použití vlastního účtu pro úložiště. Při nasazování místní verze musíte mít vlastní účet úložiště ve službě Azure, aby služba Machine Learning měla přístup k historickým datům.

## <a name="default-parameters-and-values-for-demand-forecasting-models"></a><a name="model-parameters"></a>Výchozí parametry a hodnoty pro modely prognózování poptávky

Když ke generování modelů plánování prognóz používáte strojové učení, můžete možnosti strojového učení ovládat nastavením hodnot pro *parametry algoritmu prognózy*. Tyto hodnoty se odesílají ze Supply Chain Management do Azure Machine Learning. Použijte stránku **Parametry algoritmu prognózy** k řízení, které typy hodnot by měly být poskytovány a které hodnoty by měly mít.

Chcete-li nastavit výchozí parametry a hodnoty používané pro modely vytváření prognózy poptávky, přejděte na **Hlavní plánování \> Nastavení \> Prognóza poptávky \> Parametry algoritmu prognózy**. K dispozici je standardní sada parametrů. Každý parametr má následující pole:

- **Název** – Název parametru, který používá Azure. Obvykle byste tento název neměli měnit, pokud jste experiment nepřizpůsobili v Azure Machine Learning.
- **Popis** – Běžný název parametru. Tento název se používá k identifikaci parametru na jiných místech v systému (například na stránce **Parametry prognózování poptávky**).
- **Hodnota** – Výchozí hodnota pro parametr. Hodnota, kterou byste měli zadat, závisí na parametru, který upravujete. 
- **Vysvětlení** – Krátký popis parametru a jeho použití. Tento popis obvykle obsahuje rady o platných hodnotách pro pole **Value**.

Ve výchozím nastavení jsou poskytovány následující parametry. (Pokud se budete muset někdy vrátit k tomuto standardnímu seznamu, vyberte **Obnovit** na podokně akcí.)

- **Procento úrovně jistoty** - Interval jistoty obsahuje určitý úsek hodnot, které fungují jako vhodné odhady pro prognózu poptávky. 95% úroveň jistoty například označuje existenci 5% riziko, že budoucí poptávka se bude nacházet mimo rozsah intervalu jistoty.
- **Vynutit sezónnost** - Určuje, zda vynutit, aby model použil konkrétní typ sezónnosti. Tento parametr platí pouze pro ARIMA a ETS. Možnosti: *AUTO (výchozí)*, *ŽÁDNÁ*, *DOPLŇKOVÁ*, *MULTIPLIKATIVNÍ*.
- **Model prognózování** – Určuje, který model prognózy se má použít. Možnosti: *ARIMA*, *ETS*, *STL*, *ETS+ARIMA*, *ETS+STL*, *VŠE*. Chcete-li vybrat nejlépe odpovídající model, použijte možnost *VŠE*.
- **Maximální předpokládaná hodnota** - Určuje maximální hodnotu, která má být použita pro prognózy. Formát: + 1E [n] nebo číselná konstanta.
- **Minimální předpokládaná hodnota** - Určuje minimální hodnotu, která má být použita pro prognózy. Formát: -1E [n] nebo číselná konstanta.
- **Chybějící nahrazení hodnoty** – Určuje, jak jsou vyplněny mezery v historických datech. Možnosti: *(číselná hodnota)*, *STŘEDNÍ*, *PŘEDCHOZÍ*, *INTERPOLOVANÁ LINEÁRNÍ*, *INTERPOLOVANÁ POLYNOMIÁLNÍ*.
- **Chybí rozsah nahrazení hodnoty** – Určuje, zda se nahrazení hodnoty vztahuje pouze na rozsah dat každého jednotlivého atributu rozlišení nebo na celou sadu dat. K určení období, které systém používá při vyplňování mezer v historických datech, jsou k dispozici následující možnosti:

    - *GLOBÁLNÍ* – Systém používá celou škálu dat všech atributů granularity.
    - *HISTORY_DATE_RANGE* – Systém používá konkrétní časové období definované poli **Od data** a **Do data** v části **Historický horizont** v dialogovém okně **Generovat statistickou základní prognózu**.
    - *GRANULARITY_ATTRIBUTE* – Systém používá časové období aktuálně zpracovaného atributu granularity.

    > [!NOTE]
    > Atribut granularity je kombinací dimenzí prognózy, na základě kterých se prognóza provádí. Dimenze prognózy můžete definovat na stránce **Parametry vytváření prognózy poptávky**.

- **Nápověda k sezónnosti** – pro sezónní data uveďte nápovědu pro model prognózy, která zlepší přesnost prognózy. Formát: celé číslo, které představuje počet intervalů pro opakování vzoru poptávky. Zadejte například *6* pro data, která se opakují jednou za šest měsíců.
- **Procento velikosti testovací sady** – Procentní míra historických dat, která se má použít jako testovací sada pro výpočet přesnosti prognózy.

Hodnoty pro tyto parametry můžete přepsat tak, že přejdete na **Hlavní plánování \> Nastavení \> Prognóza poptávky \> Parametry prognózy poptávky**. Na stránce **Parametry vytváření prognózy poptávky** mžete přepsat parametry následujícími způsoby:

- Pokud chcete parametry přepsat globálně, použijte kartu **Obecné**.
- Pokud chcete přepsat parametry pro konkrétní alokační klíče položky, použijte kartu **Alokační klíče položky**. Parametry, které budou přepsány pro konkrétní alokační klíč položky, ovlivní pouze prognózu položek, které jsou přidruženy k danému alokačnímu klíči položky.

> [!NOTE]
> Na stránce **Parametry algoritmu prognózy** můžete pomocí tlačítek na podokně akcí přidat parametry do seznamu nebo odebrat parametry ze seznamu. Obvykle byste však tento přístup neměli používat, pokud jste experiment nepřizpůsobili v Azure Machine Learning.

## <a name="set-up-the-azure-machine-learning-service"></a><a name="setup-amls"></a>Nastavení služby Azure Machine Learning Service

Supply Chain Management vypočítává prognózy poptávky pomocí Azure Machine Learning Service, kterou musíte nastavit a spustit ve svém vlastním předplatném Azure. Tato část popisuje, jak nastavit Azure Machine Learning Service v Azure a pak ji připojit k prostředí Supply Chain Management.

### <a name="enable-the-azure-machine-learning-service-in-feature-management"></a>Povolte službu Azure Machine Learning Service ve správě funkcí

Než budete moci používat Azure Machine Learning Service pro prognózování poptávky, musíte zapnout funkci v Supply Chain Management, abyste povolili integraci. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Hlavní plánování*
- **Název funkce:** *Azure Machine Learning Service pro prognózy poptávky*

### <a name="set-up-machine-learning-in-azure"></a><a name="ml-workspace"></a>Nastavení strojového učení v Azure

Chcete-li povolit Azure používat strojové učení ke zpracování vašich prognóz, musíte pro tento účel nastavit pracovní prostor Azure Machine Learning. Máte dvě možnosti:

- Chcete-li nastavit pracovní prostor spuštěním skriptu poskytnutého společností Microsoft, postupujte podle pokynů v [možnosti 1: Spusťte skript, který automaticky nastaví váš pracovní prostor strojového učení](#ml-workspace-script) a poté přeskočte na část [Nastavení parametrů připojení Azure Machine Learning Service v Supply Chain Management](#demand-forecast-parameters).
- Chcete-li ručně nastavit pracovní prostor, postupujte podle pokynů v [možnosti 2: Ručně nastavit pracovní prostor strojového učení](#ml-workspace-manual) a poté přeskočte na část [Nastavení parametrů připojení Azure Machine Learning Service v Supply Chain Management](#demand-forecast-parameters). Tato možnost zabere více času, ale poskytuje vám větší kontrolu.

#### <a name="option-1-run-a-script-to-automatically-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-script"></a>Možnost 1: Spusťte skript, který automaticky nastaví váš pracovní prostor strojového učení

Tato část popisuje, jak nastavit pracovní prostor strojového učení pomocí automatického skriptu poskytovaného společností Microsoft. Pokud chcete, můžete ručně nastavit všechny prostředky podle pokynů v části [Možnost 2: Ručně nastavit pracovní prostor strojového učení](#ml-workspace-manual). Nemusíte absolvovat obě možnosti.

1. Na GitHubu otevřete úložiště [Šablony pro prognózování poptávky Dynamics 365 Supply Chain Management pomocí Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) a stáhněte si následující soubory:

    - quick_setup.ps1
    - sampleInput.csv
    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. Otevřete okno PowerShellu a spusťte skript **quick_setup.ps1**, který jste stáhli v předchozím kroku. Postupujte podle pokynů na obrazovce. Skript nastaví požadovaný pracovní prostor, úložiště, výchozí úložiště dat a výpočetní prostředky. Stále však musíte vytvořit požadované kanály podle zbývajících kroků tohoto postupu. (Kanály poskytují způsob, jak spustit předpovědní skripty ze Supply Chain Management.)
1. V Azure Machine Learning Studio nahrajte soubor **sampleInput.csv**, který jste stáhli v kroku 1, do kontejneru s názvem *demplan-azureml*. (Tento kontejner vytvořil skript quick_setup.ps1.) Tento soubor je vyžadován k publikování kanálu a generování testovací prognózy. Pokyny viz [Nahrání objektu blob bloku](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob).
1. V Azure Machine Learning Studio vyberte v navigátoru **Notebooks**.
1. Najděte následující umístění ve struktuře **Soubory**: **Users/\[aktuální uživatel\]/src**.
1. Nahrajte zbývající čtyři soubory, které jste stáhli v kroku 1, do umístění, které jste našli v předchozím kroku.
1. Vyberte soubor **api_trigger.py**, který jste právě nahráli, a spusťte ho. Vytvoří kanál, který lze spustit prostřednictvím rozhraní API.
1. Váš pracovní prostor je nyní nastaven. Přeskočte dopředu na část [Nastavení parametrů připojení Azure Machine Learning Service v Supply Chain Management](#demand-forecast-parameters).

#### <a name="option-2-manually-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-manual"></a>Možnost 2: Ručně nastavit pracovní prostor strojového učení

Tato část popisuje, jak ručně nastavit pracovní prostor strojového učení. Postupy v této části musíte provádět pouze v případě, že jste se rozhodli nespouštět skript automatického nastavení, jak je popsáno v části [Možnost 1: Spuštění skriptu pro nastavení pracovního prostoru strojového učení](#ml-workspace-script).

##### <a name="step-1-create-a-new-workspace"></a><a name="create-workspace"></a>Krok 1: Vytvořte nový pracovní prostor

Pomocí následující procedury vytvořte nový pracovní prostor strojového učení.

1. Přihlaste se do portálu Azure.
1. Otevřete službu **Strojové učení**.
1. Vyberte **Vytvořit** na panelu nástrojů pro otevření průvodce **Vytvořit**.
1. Projděte průvodce podle pokynů na obrazovce. Při práci mějte na paměti následující body:

    - Použijte výchozí nastavení, pokud jiné body v tomto seznamu nedoporučují jiná nastavení.
    - Ujistěte se, že jste vybrali geografickou oblast, která odpovídá oblasti, kde je nasazena vaše instance Supply Chain Management. V opačném případě by některá z vašich dat mohla procházet hranicemi regionu. Více informací naleznete v části [oznámení o ochraně osobních údajů](#privacy) dále v tomto článku.
    - Používejte vyhrazené prostředky, jako jsou skupiny prostředků, účty úložiště, registry kontejnerů, trezory klíčů Azure a síťové prostředky.
    - Na stránce průvodce **Nastavte parametry připojení Azure Machine Learning Service** musíte zadat název účtu úložiště. Použijte účet, který je vyhrazený prognózování poptávky. Vstupní a výstupní data prognózy poptávky budou uložena na tomto účtu úložiště.

Další informace naleznete v tématu [Vytvoření pracovního prostoru](/azure/machine-learning/quickstart-create-resources#create-the-workspace).

##### <a name="step-2-configure-storage"></a><a name="config-storage"></a>Krok 2: Nakonfigurujte úložiště

Pomocí následujícího postupu nastavte úložiště.

1. Na GitHubu otevřete úložiště [Šablony pro prognózování poptávky Dynamics 365 Supply Chain Management pomocí Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) a stáhněte si soubor **sampleInput.csv**.
1. Otevřete účet úložiště, který jste vytvořili v části [Krok 1: Vytvořte nový pracovní prostor](#create-workspace).
1. Postupujte podle pokynů v části [Vytvořte kontejner](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container) k vytvoření kontejneru s názvem *demplan-azureml*.
1. Nahrajte soubor **sampleInput.csv**, který jste stáhli v kroku 1, do kontejneru, který jste právě vytvořili. Tento soubor je nutný k publikování kanálu a generování testovací prognózy. Pokyny viz [Nahrání objektu blob bloku](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob).

##### <a name="step-3-configure-a-default-datastore"></a>Krok 3: Nakonfigurujte výchozí datové úložiště

Pomocí následujícího postupu nastavte výchozí úložiště dat.

1. V Azure Machine Learning Studio vyberte v navigátoru **Úložiště dat**.
1. Vytvořte nové datové úložiště typu *Azure Blob Storage*, které ukazuje na kontejner úložiště blob *demplan-azureml*, který jste vytvořili v části [Krok 2: Nakonfigurujte úložiště](#config-storage). (Pokud je typ ověřování nového datového úložiště *Klíč účtu*, zadejte klíč účtu pro vytvořený účet úložiště. Pokyny viz [Správa přístupových klíčů k účtu úložiště](/azure/storage/common/storage-account-keys-manage?tabs=azure-portal).)
1. Udělejte ze svého nového úložiště dat výchozí datové úložiště otevřením jeho údajů a výběrem **Nastavit jako výchozí úložiště dat**.

##### <a name="step-4-configure-compute-resources"></a><a name="config-compute-resources"></a>Krok 4: Nakonfigurujte výpočetní prostředky

Pomocí následujícího postupu nastavte výpočetní prostředek v Azure Machine Learning Studio ke spouštění skriptů generování prognóz.

1. Otevřete stránku údajů pro pracovní prostor strojového učení, který jste vytvořili v části [Krok 1: Vytvořte nový pracovní prostor](#create-workspace). Vyhledejte hodnotu **Webová adresa URL aplikace Studio** a výběrem odkazu ji otevřete.
1. Vyberte **Výpočetní prostředky** v navigačním podokně.
1. Na kartě **Výpočetní instance** vyberte **Nový** a otevřete průvodce, který vám pomůže vytvořit novou výpočetní instanci. Postupujte podle pokynů na obrazovce. Výpočetní instance bude použita k vytvoření kanálu prognózování poptávky (po zveřejnění kanálu jej lze odstranit). Použijte výchozí nastavení.
1. Na kartě **Výpočetní clustery** vyberte **Nový** a otevřete průvodce, který vám pomůže vytvořit nový výpočetní cluster. Postupujte podle pokynů na obrazovce. Výpočetní cluster bude použit ke generování prognóz poptávky. Jeho nastavení ovlivňuje výkon a maximální úroveň paralelizace běhu. Nastavte následující pole, ale pro všechna ostatní použijte výchozí nastavení:

    - **Název** – Zadejte *e2ecpucluster*.
    - **Velikost virtuálního počítače** – Upravte toto nastavení podle objemu dat, které očekáváte použít jako vstup pro prognózu poptávky. Počet uzlů by neměl překročit 11, protože ke spuštění generování prognózy poptávky je nutný jeden uzel a maximální počet uzlů, které lze poté použít ke generování prognózy, je 10. (Počet uzlů také nastavíte v souboru parameters.py v [Kroku 5: Vytvořte kanály](#create-pipelines).) Na každém uzlu bude několik pracovních procesů, které paralelně spouštějí skripty prognózy. Celkový počet pracovních procesů ve vaší úloze bude *Počet jader, která má uzel* × *Počet uzlů*. Pokud má například váš výpočetní cluster typ *Standard\_D4* (osm jader) a maximálně 11 uzlů, a pokud je hodnota `nodes_count` nastavena na *10* v souboru parameters.py, je efektivní úroveň paralelismu 80.

##### <a name="step-5-create-pipelines"></a><a name="create-pipelines"></a>Krok 5: Vytvořte kanály

Kanály poskytují způsob, jak spustit předpovědní skripty ze Supply Chain Management. Následujícím postupem vytvořte požadované kanály.

1. Na GitHubu otevřete úložiště [Šablony pro prognózování poptávky Dynamics 365 Supply Chain Management pomocí Azure Machine Learning](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) a stáhněte si následující soubory:

    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. V Azure Machine Learning Studio vyberte v navigátoru **Notebooks**.
1. Najděte následující umístění ve struktuře **Soubory**: **Users/\[aktuální uživatel\]/src**.
1. Nahrajte čtyři soubory, které jste stáhli v kroku 1, do umístění, které jste našli v předchozím kroku.
1. V Azure otevřete a zkontrolujte soubor **parameters.py**, který jste právě nahráli. Ujistěte se, že hodnota `nodes_count` je o jednu menší než hodnota, kterou jste nakonfigurovali pro výpočetní cluster v části [Krok 4: Nakonfigurujte výpočetní prostředky](#config-compute-resources). Pokud je hodnota `nodes_count` větší nebo rovna počtu uzlů ve výpočetním clusteru, může být spuštění kanálu možné. Poté však přestane reagovat, když čeká na požadované prostředky. Další informace o počtu uzlů viz část [Krok 4: Nakonfigurujte výpočetní prostředky](#config-compute-resources).
1. Vyberte soubor **api_trigger.py**, který jste právě nahráli, a spusťte ho. Vytvoří kanál, který lze spustit prostřednictvím rozhraní API.

### <a name="set-up-a-new-active-directory-application"></a><a name="aad-app"></a>Nastavení nové aplikace Active Directory

Aplikace Active Directory se vyžaduje k ověření se zdroji, které jsou vyhrazeny pro prognózování poptávky, pomocí instančního objektu. Aplikace by proto měla mít nejnižší úroveň oprávnění, která je vyžadována pro generování prognózy.

1. Přihlaste se do portálu Azure.
1. Zaregistrujte novou aplikaci v Azure Active Directory (Azure AD) klienta. Pokyny naleznete v části [Použití portálu k vytvoření aplikace Azure AD a hlavní služby, které mají přístup ke zdrojům](/azure/active-directory/develop/howto-create-service-principal-portal).
1. V průvodci postupujte podle pokynů na obrazovce. Použijte výchozí nastavení.
1. Udělte své nové aplikaci Active Directory přístup k následujícím prostředkům, které jste vytvořili v části [Nastavení strojového učení v Azure](#ml-workspace). Pokyny viz [Přiřazení roli Azure pomocí Azure Portal](/azure/role-based-access-control/role-assignments-portal?tabs=current). Tento krok umožní systému importovat a exportovat data prognóz a spouštět procesy strojového učení ze Supply Chain Management.

    - Role přispěvatele do pracovního prostoru strojového učení
    - Role přispěvatele do vyhrazeného účtu úložiště
    - Role přispěvatele data objektu blob úložiště do vyhrazeného účtu úložiště

1. V části **Certifikáty a tajné kódy** aplikace, kterou jste vytvořili, vytvořte pro aplikaci tajný kód. Pokyny viz [Přidání tajného klíče klienta](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret).
1. Poznamenejte si ID aplikace a její tajný kód. Podrobnosti o této aplikaci budete potřebovat později, až budete nastavovat stránku **Parametry prognózování poptávky** na stránce Supply Chain Management.

### <a name="set-up-azure-machine-learning-service-connection-parameters-in-supply-chain-management"></a><a name="demand-forecast-parameters"></a>Nastavení parametrů připojení Azure Machine Learning Service v Supply Chain Management

Pomocí následujícího postupu připojte prostředí Supply Chain Management ke službě strojového učení, kterou jste právě nastavili v Azure.

1. Přihlaste se k aplikaci Supply Chain Management.
1. Přejděte na **Hlavní plánování \> Nastavení \> Prognóza poptávky \> Parametry tvorby prognóz poptávky**.
1. Na kartě **Všeobecné** zkontrolujte, že pole **Strategie generování prognóz** je nastaveno na *Azure Machine Learning Service*.
1. Na kartě **Alokační klíče položek** zkontrolujte, že pole **Strategie generování prognóz** je nastaveno na *Azure Machine Learning Service* pro každý alokační klíč, který by měl používat Azure Machine Learning Service pro prognózování poptávky.
1. Na kartě **Azure Machine Learning Service** nastavte následující pole:

    - **ID klienta** – Zadejte ID vašeho klienta Azure. Supply Chain Management použije toto ID k ověření pomocí Azure Machine Learning Service. Své ID klienta najdete na stránce **Přehled** pro Azure AD na Azure Portal.
    - **ID aplikace instančního objektu** – Zadejte ID aplikace pro aplikaci, kterou jste vytvořili v části [Aplikace Active Directory](#aad-app). Tato hodnota se používá k autorizaci požadavků API pro Azure Machine Learning Service.
    - **Tajný klíč instančního objektu** – Zadejte tajný klíč aplikace instančního objektu, který jste vytvořili v části [Aplikace Active Directory](#aad-app). Tato hodnota se používá k získání přístupového tokenu pro objekt zabezpečení, který jste vytvořili k provádění autorizovaných operací proti Azure Storage a pracovnímu prostoru Azure Machine Language.
    - **Název účtu úložiště** – Zadejte název účtu úložiště Azure, který jste zadali při spuštění průvodce nastavením v pracovním prostoru Azure. (Další informace naleznete v části [Nastavení strojového učení v Azure](#ml-workspace).)
    - **Adresa koncového bodu kanálu** – Zadejte adresu URL koncového bodu REST kanálu pro vaši službu Azure Machine Learning Service. Tento kanál jste vytvořili jako poslední krok, když jste [nastavovali strojové učení v Azure](#ml-workspace). Chcete-li získat adresu URL kanálu, přihlaste se k Azure Portal a vyberte **Kanál** v navigaci. Na kartě **Kanál** vyberte koncový bod kanálu, který je pojmenován **TriggerDemandForecastGeneration**. Poté zkopírujte zobrazený koncový bod REST.

    ![Parametry na kartě Azure Machine Learning Service stránky parametrů prognózy poptávky.](media/azure-ml-service-parameters.png "Parametry na kartě Azure Machine Learning Service stránky parametrů prognózy poptávky")

## <a name="privacy-notice"></a><a name="privacy"></a>Oznámení o ochraně osobních údajů

Když vyberete *Azure Machine Learning Service* jako strategii generování prognóz, Supply Chain Management automaticky odesílá vaše zákaznická data pro historickou poptávku, jako jsou agregovaná množství, názvy produktů a dimenze produktů, místa dodání a příjmu, identifikátory zákazníků a také parametry prognózy, do geografické oblasti, kde jsou váš pracovní prostor strojového učení a jeho propojený účet úložiště umístěny, za účelem předpovídání budoucích požadavků. Služba Azure Machine Learning Service může být v jiné geografické oblasti, než je geografická oblast, kde je nasazena Supply Chain Management. Někteří uživatelé mohou řídit, zda je tato funkce povolena, výběrem strategie generování prognóz na stránce **Parametry prognózování poptávky**.

## <a name="additional-resources"></a>Další prostředky

- [Přehled prognózy poptávky](introduction-demand-forecasting.md)
- [Generování statistické základní prognózy](generate-statistical-baseline-forecast.md)
- [Ruční úpravy základní prognózy](manual-adjustments-baseline-forecast.md)
- [Webinář: seriál Prognóza poptávky s Azure Machine Learning](https://aka.ms/DemandForecastingwithAzureMachineLearningSeries)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
