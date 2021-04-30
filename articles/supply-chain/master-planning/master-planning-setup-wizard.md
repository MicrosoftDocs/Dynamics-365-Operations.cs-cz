---
title: Průvodce nastavením hlavního plánování
description: Toto téma popisuje různé důležité strategie a parametry, které se používají k nastavení hlavního plánování.
author: t-benebo
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: c55c36358b8acf93ab25a358d4d7cd6a4212c2b2
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909420"
---
# <a name="master-planning-setup-wizard"></a>Průvodce nastavením hlavního plánování

[!include [banner](../includes/banner.md)]

Toto téma obsahuje pokyny pro **Průvodce nastavením hlavního plánování**. Vysvětluje způsob výpočtu návrhů parametrů a také obsahuje příklady, které ukazují, jak různé společnosti nastavují hlavní plánování na základě svých obchodních potřeb.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3YnSB]

[Video Průvodce nastavením hlavního plánování v aplikaci Dynamics 365 Supply Chain Management](https://youtu.be/c-e6n-8rZb4) (zobrazené výše) je součástí playlistu [Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), který je k dispozici na YouTube.


## <a name="specific-requirements-of-your-company"></a>Specifické požadavky vaší společnosti

Na první stránce průvodce se zobrazí dotaz na konkrétní požadavky vaší společnosti. Vaše odpovědi na tyto otázky nemusíte být přesné, ale měli byste být schopni poskytnout hrubý odhad počtu položek a plánovaných objednávek, které budou pro právnickou entitu. Vaše odpovědi se používají ke konfiguraci parametrů, které platí pro vaši právnickou entitu, nikoli pouze pro hlavní plán, který jste vybrali. Následující části popisují vypočtené parametry a použité vzorce.

### <a name="number-of-threads"></a>Počet vláken

- **Pokud vyrábíte jakékoliv z položek:** Počet vláken = počet plánovaných objednávek ÷ 1 000
- **Pokud nevyrábíte žádné z položek:** Počet vláken = počet položek ÷ 1 000

Pokud počet vypočtených vláken přesahuje 75 % dostupného počtu vláken, je limitován na 75 % počtu vláken, která jsou k dispozici pro každého zákazníka. (Počet dostupných vláken bude určen pro každého zákazníka.)

Více informací naleznete v části [Počet vláken](/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-threads).

### <a name="bundle-size"></a>Velikost sady

Velikost svazku bude nastavena na **1**. Tato hodnota je často nejlepší hodnotou, protože pomáhá zlepšit výkon hlavního plánování.

Další informace naleznete v tématu [Počet úkolů v sadě úkolů pomocníka](/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-tasks-in-helper-task-bundle).

### <a name="firming-bundle-size"></a>Velikost potvrzujícího svazku

- **Pokud vyrábíte jakékoliv z položek:** Velikost potvrzujícího svazku bude nastavena na větší z těchto dvou hodnot: **10** a výpočet svazku
- **Pokud nevyrábíte žádné z položek:** Velikost potvrzujícího svazku bude nastavena na větší z těchto dvou hodnot: **50** a výpočet svazku

Výpočet svazku = (počet plánovaných objednávek × (ochranná doba potvrzení ÷ ochranná doba disponibility) ÷ počet vláken) ÷ 10

### <a name="cache-size"></a>Velikost mezipaměti

Velikost mezipaměti bude nastavena na **Maximum**. Tato hodnota je často nejlepší hodnotou, protože pomáhá zlepšit výkon hlavního plánování.

Další informace naleznete v tématu [Přidělení času úlohám v sadě úloh](/dynamics365/unified-operations/supply-chain/production-control/allocate-time-jobs-job-bundle).

### <a name="manufacturing-setup"></a>Nastavení výroby

Při výrobě položek se později v průvodci zobrazí stránka **Nastavení výroby**.

## <a name="scope-of-the-current-plan"></a>Rozsah aktuálního plánu

Na stránce **Rozsah aktuálního plánu** průvodce odpovězte na otázky, které souvisejí s tím, jak daleko v budoucnu budou různé požadavky zohledněny a vypočteny v hlavním plánování. Každá otázka se ptá, zda chcete použít funkci a jak ji chcete nakonfigurovat.

Například v případě funkce plánu prognózy se průvodce zeptá: „Chcete použít plán prognóz v hlavním plánování, aby plánované objednávky byly navrženy ke splnění přepokládané poptávky?“

Existují tyto možnosti:

- **Ne** – Hlavní plánování nebude navrhovat plánované objednávky pro splnění prognózy. Na kartě **Ochranné doby** stránky **Hlavní plány** (**Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**) průvodce nastaví možnost **Plán prognóz (ochranná doba)** na **Ano** a nastaví počet dnů na **0** (nula). Toto nastavení přepíše ochrannou dobu určenou ve skupině disponibility. Vzhledem k tomu, že počet dní je nastaven na **0** (nula), nebude funkce použita.
- **Ano, jak je definováno v tomto hlavním plánu** – Zpřístupní se pole, kde můžete zadat počet dní, po které bude hlavní plánování navrhovat plánované objednávky ke splnění předpokládané poptávky. Průvodce nastaví možnost **Plán prognóz (ochranná doba)** na **Ano** a nastaví počet dnů na počet zadaný v poli **Plán prognóz** na kartě **Ochranné doby** stránky **Hlavní plány**. Toto nastavení přepíše hodnoty nastavené ve skupinách disponibility.
- **Ano, jak je definováno v disponibilitě** – Průvodce nastaví možnost **Plán prognóz (ochranná doba)** na **Ne**. Ochranné doby, které jsou zadány ve skupině disponibility, budou použity k určení doby, po kterou budete plánovat prognózu.

Zbývající otázky na této stránce a jejich odpovědi se řídí stejným schématem:

- **Ne** – Možnost **Plán prognóz (ochranná doba)** bude nastavena na hodnotu **Ano** a počet dní bude nastaven na **0** (nula).
- **Ano, jak je definováno v toto hlavním plánu** – Možnost **Plán prognóz (ochranná doba)** bude nastavena na **Ano**. Počet dnů, které zadáte, bude použit a přepíše hodnoty nastavené ve skupinách disponibility.
- **Ano, jak je definováno ve skupině disponibility** – Možnost **Plán prognóz (ochranná doba)** bude nastavena na **Ne**.

Další informace naleznete v tématu [Plánování úlohy](/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="scheduling-options"></a>Možnosti plánování

Stránka **Možnosti plánování** se zobrazí pouze v případě, že jste odpověděli **Ano** na otázku „Vyrábíte některé z plánovaných položek?“ na první stránce průvodce.

Vaše odpověď na první otázku na této stránce („Potřebujete naplánovat operace rozdělené do jednotlivých úloh?“) určuje metodu plánování na kartě **Obecné** na stránce **Hlavní plány**.

- **Ano** – Bude použito plánování úlohy.
- **Ne** – Bude použito plánování operací.

Další informace naleznete v tématech [Plánování operací](/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling) a [Plánování úlohy](/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="updates-of-demand-and-supply"></a>Aktualizace poptávky a nabídky

Otázky na stránce **Aktualizace poptávky a nabídky** se vztahují k potvrzení, zprávám akce a zpožděním.

Nastavení hlavního plánování bude aktualizováno na základě vašich odpovědí podle stejného schématu, které je popsáno v předchozí části:

- **Ne** – Možnost **Ochranná doba** na stránce **Hlavní plány** bude nastavena na hodnotu **Ano** a počet dní bude nastaven na **0** (nula).
- **Ano, jak je definováno v toto hlavním plánu** – Možnost **Ochranná doba** bude nastavena na **Ano**. Počet dnů, které zadáte, bude použit a přepíše hodnoty nastavené ve skupinách disponibility.
- **Ano, jak je definováno ve skupině disponibility** – Možnost **Ochranná doba** bude nastavena na **Ne**.

Pro vypočtená zpoždění budou vaše odpovědi na otázky v průvodci aktualizovat odpovídající parametry na kartě **Vypočtená zpoždění** na stránce **Hlavní plány**.

## <a name="summary-of-your-changes"></a>Souhrn vašich změn

Poslední stránka průvodce zobrazuje změny doporučené na základě vašich odpovědí. Zobrazuje jak hodnotu v nastavení (**Aktuální nastavení**), tak hodnotu, kterou průvodce doporučuje (**Nová konfigurace**).

Můžete také změnit parametry v nové konfiguraci. Parametry jsou rozděleny do parametrů, které se vztahují k vaší právnické osobě, a parametrů, které se vztahují pouze k vybranému hlavnímu plánu. Chcete-li zobrazit všechny parametry nastavení, které lze změnit pomocí průvodce, vyberte možnost **Zobrazit všechny parametry** v dolní části stránky. Poté můžete změnit parametry.

Po vybrání položky **Dokončit** bude použita nová konfigurace. Pokud vyberete možnost **Zrušit**, nebude použita žádná ze změn.

## <a name="examples"></a>Příklad

Tato část popisuje nastavení dvou fiktivních společností a zobrazuje, jak se může nastavení změnit podle potřeb jednotlivých firem.

### <a name="example-1-contoso-manufacturer"></a>Příklad 1: Contoso Manufacturer

Contoso Manufacturer je výrobní společnost vyrábějící reproduktory. Nakupuje různé suroviny a komponenty od různých dodavatelů, které se používají pro konečné reproduktory. Zde jsou některé charakteristické rysy dodávky a výroby:

- Konečné zboží, které společnost vyrábí, má strukturu kusovníku.
- Všechny konečné položky a komponenty jsou plánovány hlavním plánováním. Ruční plánování není provedeno.
- Postup operací je definován pro výrobu každé výsledné položky.
- Výrobní závod produkuje finální položky. Má definovaný počet frézovacích a vrtacích strojů, které se používají ke zpracování komponent. Jednotlivé součásti musí být těmito stroji zpracovány.
- Existuje mnoho dodavatelů. Průměrná doba realizace položek je jeden týden. Skupina položek od stejného dodavatele bude mít dobu realizace 7 týdnů.

V průvodci jsou pro výrobce Contoso Manufacturer zadány následující hodnoty:

- **Disponibilita:**

    - **Otázka:** „Chcete zadat počet dnů horizontu plánování?“
    - **Odpověď:** „Ano, jak je definováno ve skupinách disponibility.“

    Vzhledem k tomu, že doba realizace položek je velmi odlišná, nemusí společnost Contoso plánovat všechny položky pro stejné období v budoucnosti. Jsou vytvářeny skupiny disponibility pro položky. Položky s podobnou dobou realizace jsou přiřazeny ke stejné skupině disponibility. Horizont plánování pro každou skupinu disponibility (to znamená ochrannou dobu disponibility) je přibližně doba realizace plus rezerva jednoho týdne. Hlavní plánování pak zajistí, že položky jsou plánovány předem na základě jejich doby realizace.

    Proto budou pro tento příklad vytvořeny dvě skupiny disponibility. Jedna skupina disponibility bude mít ochrannou dobu disponibility dva týdny a druhá bude mít ochrannou dobu disponibility osm týdnů.

    Pokud **Ano, jak je definováno v tomto hlavním plánu** je vybráno jako odpověď, počet zadaných dní by měl přesahovat nejdelší dobu realizace všech položek. Avšak protože mnoho položek není nutné plánovat s takovým předstihem, mnoho plánovaných objednávek bude vypočítáno, ale nikdy použito. Proto se zvýší runtime hlavního plánování.

- **Plánování:**

    - **Otázka:** „Potřebujete naplánovat operace rozdělené na jednotlivé úlohy?“
    - **Odpověď:** „Ano“.

    Společnost Contoso Manufacturing musí plánovat jednotlivé úlohy, které budou provedeny na dílně. Proto bude používat plánování úloh.

- **Kapacita:**

    - **Otázka:** „Chcete plánovat pomocí kapacity zdrojů?“
    - **Odpověď:** „Ano, jak je definováno v tomto hlavním plánu.“ Je zadáno **10 dní**.

    Počet frézovacích a vrtacích strojů je omezený. Plánování výroby musí brát toto omezení v úvahu a včas uspořádat úlohy podle kapacity zdrojů. Jinými slovy, naplánované úlohy budou přeplánovány na základě omezení zdrojů. Plánování použije kromě definovaného období také dobu realizace. (Plánované výrobní zakázky se mohou překrývat.) Vzhledem k tomu, že doba realizace pro položky je sedm dní, bude kapacita zdrojů pro hlavní plánování zvažována během 10 dnů.

- **Pořadí:**

    - **Otázka:** „Chcete provést posloupnost plánovaných objednávek pomocí hodnot sekvencí produktu?“
    - **Odpověď:** „Ano, jak je definováno ve skupinách disponibility.“

    Postup je definován pro výrobu každé výsledné položky. Proto hlavní plánování naplánuje objednávky včas podle definovaných postupů.

- **Rozpad:**

    - **Otázka:** „Chcete naplánovat objednávky pro všechny prvky v kusovníku (plán pro nadřazenou položku a všechny podřízené položky)?“
    - **Odpověď:** „Ano, jak je definováno ve skupinách disponibility.“

    Všechny položky použité pro výrobu musí být plánovány. Vzhledem k tomu, že položky mají velmi odlišné doby realizace, bude mít hlavní plánování vyšší výkonnost při použití skupin disponibility. Opět lze zadat rezervu jednoho týdne a rozpad lze provést pro stejnou dobu jako disponibilitu.

### <a name="example-2-contoso-retailer"></a>Příklad 2: Contoso Retailer

Contoso Retailer je distribuční společností v módním průmyslu. Používá hlavní plánování k výpočtu, kdy by měly být provedeny nákupní objednávky na základě předpokládaného prodeje. Zde jsou některé z jeho charakteristických rysů:

- Contoso Retailer používá prognózu poptávky k předpovědi prodeje. Nákupní objednávky budou plánovány podle prognózy.
- Obchody používají žádanky pro doplnění.
- Doba realizace z hlavního skladu do každého obchodu je přibližně dva týdny pro všechny položky.

V průvodci jsou pro výrobce Contoso Retailer zadány následující hodnoty:

- **Prognóza poptávky:**

    - **Otázka:** „Chcete použít plán prognóz v hlavním plánování, aby plánované objednávky byly navrženy ke splnění předpokládaného požadavku?“
    - **Odpověď:** „Ano, jak je definováno v tomto hlavním plánu.“

    Contoso zahrnula prognózu poptávky k předpovědi prodeje. Proto musí hlavní plánování doporučit plánované objednávky ke splnění prognózy.

- **Potvrzení:**

    - **Otázka:** „Chcete, aby hlavní plánování automaticky potvrdilo plánované objednávky do dokladů objednávek, například výrobních zakázek nebo nákupních objednávek?“
    - **Odpověď:** „Ano, jak je definováno v tomto hlavním plánu.“ Je zadán **1 den**.

    Vzhledem k tomu, že Contoso Retailer vytvoří nákupní objednávky přímo z plánovaných nákupních objednávek, je užitečné, pokud jsou plánované nákupní objednávky automaticky potvrzeny. Protože společnost spouští hlavní plánování každý den, ochranná doba potvrzení jednoho dne automaticky potvrdí všechny objednávky, které jsou požadovány pro následující den.

- **Schválené žádanky:**

    - **Otázka:** „Chcete zahrnout poptávku ze schválených žádanek k doplňování maloobchodních prodejen?“
    - **Odpověď:** „Ano, jak je definováno v tomto hlavním plánu.“ Je zadán **1 den**.

    Společnost Contoso používá schválené žádanky ze svých obchodů k vytvoření plánovaných nákupních objednávek pro doplnění těchto obchodů. Vzhledem k tomu, že hlavní plánování je spuštěno každý den, budou do plánování zahrnuty žádanky z posledního dne.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]