---
title: Zpracování produktu se skutečnou hmotností pomocí řízení skladu
description: Toto téma popisuje způsob použití šablon práce a směrnic skladového místa k určení, jak a kde se práce ve skladu provádí.
author: perlynne
manager: tfehr
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: b1d106fa6fe5072eb74813495253731dd988c376
ms.sourcegitcommit: 9a0be1ceee90e80f4c75f241aba847547b5032e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2020
ms.locfileid: "3693272"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Zpracování produktu se skutečnou hmotností pomocí řízení skladu

[!include [banner](../includes/banner.md)]


## <a name="feature-exposure"></a>Expozice funkce

Chcete-li použít řízení skladu pro zpracování produktů se skutečnou hmotností, musíte pro zapnutí této funkce použít licenční konfigurační klíč. Přejděte do nabídky **Správa systému \> Nastavení \> Konfigurace licence**. Poté na kartě **Konfigurační klíče** kartu rozbalte **Obchod \> Řízení skladu a správy přepravy** a zaškrtněte políčko u možnosti **Skutečná hmotnost pro sklad**.

> [!NOTE]
> Musí být zapnuty licenční konfigurační klíče pro možnosti **Řízení skladu a správy přepravy** i **Zpracování distribuce \> Skutečná hmotnost**. Chcete-li nastavit konfigurační klíče pro skutečnou hmotnost, musíte také zapnout funkci pomocí pracovního prostoru Správa **Správa funkcí**. Hlavní funkcí, která musí být zapnuta, je **Zpracování produktu se skutečnou hmotností pomocí řízení skladu**. Dvě související, ale volitelné funkce, které byste mohli chtít zapnout, jsou **Změny stavu zásob pro produkty se skutečnou hmotností** a **Použít existující značky skutečné hmotnosti při vykazování výrobních zakázek jako dokončených**.

Po zapnutí licenčního konfiguračního klíče můžete při vytvoření uvolněného produktu zvolit **Skutečná hmotnost**. Můžete také přidružit uvolněný produkt ke skupině dimenze úložiště, pro kterou je zvolen parametr **Použít procesy řízení skladu**.

Než budete moci produkt použít v řízení skladu, musíte provést několik základních nastavení pro konkrétní produkt týkajících se skutečné hmotnosti.

- Definujte převod nominální hmotnosti mezi jednotkou skutečné hmotnosti (pole) a jednotkou zásob (kilogram \[kg\]) jako součást definice převodu jednotek.
- Definujte tolerance minimální a maximální hmotnosti v rámci nastavení jednotky skutečné hmotnosti.
- Nastavte skupinu klasifikace jednotek, kde je jednotka skutečné hmotnosti definována jako nejnižší skladová jednotka zásob (SKU).
- Nastavte zásadu zpracování položky se skutečnou hmotností.

Další informace naleznete v tématu [Nastavení a správa položek se skutečnou hmotností](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Úpravy transakce

Vzhledem k tomu, že hmotnost zásob, když se dostanou do skladu, se může lišit od hmotnosti, když jsou zásoby vydány ze skladu, musí zpracování produktu se skutečnou hmotností upravit zásoby.

> [!NOTE]
> Aktivita mobilního zařízení spustí úpravy transakcí pouze v případě, že metoda odchylky výstupní hmotnosti pro zásady zpracování zboží se skutečnou hmotností je **Povolit odchylku hmotnosti**.

**Příklad 1**

Během výrobního procesu **Ohlásit jako dokončené** je zaznamenaná vstupní hmotnost registrační značky obsahující osm krabic produktu se skutečnou hmotností jako 80,1 kg. Registrační značka pak odložení uložena v oblasti hotových výrobků a během doby skladování některé hmotnost dojde ke ztrátě do ovzduší.

Později, jako součást procesu výdeje prodejní objednávky, je váha stejné poznávací značky zaznamenána jako 79,8 kg. Proto v systému nyní máte hmotnostní rozdíl jako součást sady fyzické dimenze.

V takovém případě systém automaticky upraví rozdíl zaúčtováním transakce pro chybějící 0,3 kg.

**Příklad 2**

Ve své definici je produkt nastaven tak, aby toleroval minimální hmotnost 8 kg a maximální hmotnost 12 kg pro jednotku skutečné hmotnosti **Krabice**.

Máte dvě krabice produktu a jejich registrovaná hmotnost je 16 kg. Pokud pracovník skladu vybere a zváží jednu z krabic a váha je zaznamenána jako 9 kg, zbývající krabice bude vážit 7 kg. Protože 7 kg je však nižší než minimální hmotnost, systém provede automatickou úpravu k navýšení hmotnosti na skladě o 1 kg.

Chcete-li nastavit účty, do kterých jsou zaúčtovány tyto úpravy, přejděte na **Správa nákladů \> Nastavení zásad integrace hlavní knihy \> Zaúčtování**. Poté na kartě **Zásoby** definujte následující účty:

- Účet ztrát – skutečná hmotnost
- Účet zisků – skutečná hmotnost

## <a name="catch-weight-item-handling-policy"></a>Zásada zpracování položky se skutečnou hmotností

Zásada zpracování položky se skutečnou hmotností definuje dva primární toky správy skladu pro položky: kdy je hmotnost zboží zaznamenána a jakým způsobem je zaznamenána.

Můžete určit, kdy je hmotnost zaznamenána pro zpracování prodejní objednávky a převodního příkazu. Hmotnost lze zaznamenat během jednoho ze dvou následujících procesů:

- **Výdej** – Hmotnost je zaznamenaná během řádků práce počátečního vyskladnění práce objednávky.
- **Balení** – Hmotnost je zaznamenaná během ručního balení. (Je nutné odeslat položky do stanice balení.)

Pokud je během procesů balení kontejneru zaznamenána skutečná hmotnost na balicí stanici, pracovníci skladu nejsou vyzváni k záznamu hmotnost během práce výdeje. Namísto toho je průměrná hmotnost fyzických zásob použita jako hmotnost vyskladněných zásob, které jdou do oblasti balení. Tento koncept platí také pro položky se skutečnou hmotností, které jsou sledovány pomocí značek. U položek sledovaných štítkem tyto parametry určují, kdy je štítek zachycen. Štítek lze zachytit v době výdeje pomocí mobilního zařízení nebo při ručním balení.

> [!NOTE]
> Vzhledem k tomu, že možnost **Balení** způsobí aktualizaci zásob pomocí průměrné vydané hmotnosti, může dojít k nesrovnalosti, která by mohla vést k úpravě zisku/ztráty skutečné hmotnosti nebo k rozdílu mezi hmotností zásob na skladě a hmotností štítku skutečné hmotnosti.

Pro interní procesy správy skladu, jako je inventura a opravy, je možné určit, zda by měla být zaznamenána hmotnost či nikoli. Pokud není zaznamenána, bude použita nominální hmotnost. Další možnosti umožňují zachytit hmotnost za jednotku skutečné hmotnosti a podle množství inventury.

Můžete také definovat, jakým způsobem je hmotnost zaznamenána. V jednom ze dvou hlavní toků jsou štítky skutečné hmotnosti sledovány a používány k záznamu hmotnosti. V druhém toku nejsou štítky skutečné hmotnosti sledovány.

- **Ano** – Položka používá štítky skutečné hmotnosti. Číslo každého štítku představuje jednu jednotku skutečné hmotnosti (krabice) a ke štítku je přidružena hmotnost a jiné informace Pro odchozí procesy se použije hmotnost přidružená ke štítku.
- **Ne** – Položka nepoužívá štítky skutečné hmotnosti. Příchozí a odchozí procesy vážení jsou založeny na skutečné hmotnosti zaznamenané během každého procesu.

Proces sledování štítků skutečné hmotnosti lze použít pro položky, které nezmění hmotnost během doby skladování. Hmotnost bude zaznamenána pouze v průběhu vstupního procesu skladu. V průběhu odchozího procesu budou štítky skutečné hmotnosti pouze naskenovány, a hmotnosti, které jsou přidruženy ke štítkům se použijí pro zpracování odchozí transakce.

Dalším důležitým parametrem, který souvisí se zpracováním štítků skutečné hmotnosti, je **Metoda sledování dimenze značky skutečné hmotnosti**. Značky mohou být buď částečně sledovány, nebo plně sledovány. Je-li značka částečně sledována, sleduje dimenze produktu, sledovací dimenze a stav zásob. Je-li značka plně sledována, sleduje dimenze produktu, sledovací dimenze a **všechny** dimenze úložiště.

Navíc, je-li u položky sledována značka, existuje parametr **Metoda zaznamenání odchozí značky**. Tento parametr lze nastavit tak, aby se vždy zobrazoval dotaz na značku u odchozích transakcí z mobilního zařízení. Alternativně můžete nastavit parametr tak, aby se zobrazil dotaz na značky pouze v případě, že jsou požadovány. Existuje například pět značek skutečné hmotnosti na skladě na dané registrační značce, které jste uvedli, že chcete vydat všech pět značek z registrační značky. V tomto případě, pokud je parametr **Metoda zaznamenání odchozí značky** nastaven na **Vyžádat značku jen, když je potřeba**, pět značek bude automaticky vyskladněno. Není nutné skenovat každou značku. Je-li parametr nastaven na **Vždy vyžadovat značkuí**, je nutné skenovat každou značku, a to i v případě, že je vyskladněno všech pět značek.

> [!NOTE]
> Jako pravidlo jsou visačky zachyceny a aktualizovány pouze z položek nabídky mobilního zařízení. Existuje však několik scénářů, kde jsou značky zachyceny někde jinde (například z ručního stanoviště balení). Obecně platí, že položky nabídky mobilního zařízení by měly být použity pro všechny aktivity skladu v případě, že jsou použity značky.

### <a name="how-to-capture-catch-weight"></a>Jak zaznamenat skutečnou hmotnost

**Když se používá sledování značky skutečné hmotnosti**, musí být značka vždy vytvořena pro každou jednotku skutečné hmotnosti, která je přijata, a každá značka musí být vždy přiřazena k hmotnosti.

Například **Krabice** je jednotka skutečné hmotnosti a přijmete jednu paletu s osmi krabicemi. V takovém případě se musí vytvořit osm jedinečných štítků skutečné hmotnosti a hmotnost musí být přiřazena ke každému štítku. V závislosti na štítku příchozí skutečné hmotnosti lze zaznamenat buď hmotnost všech osmi krabic a průměrná hmotnosti pak může být rozdělena na každou krabici, nebo lze zaznamenat jedinečnou hmotnost pro každou krabici.
Při použití **Použít existující značky skutečné hmotnosti při vykazování výrobních zakázek jako dokončených** s procesem povoleným prostřednictvím položky nabídky mobilního zařízení se zásoby aktualizují na základě existující informace štítku skutečné hmotnosti. V důsledku toho aplikace skladu nezobrazí výzvu k zaznamenání dat štítku skutečné hmotnosti jako součásti výrobní sestavy jako dokončené operace.

**Když se nepoužívá sledování značek skutečné hmotnosti**, lze zaznamenat hmotnost pro každou sadu dimenzí, (například pro každou poznávací značku a sledovací dimenzi). Případně lze zaznamenat hmotnost podle agregované úrovně, například pět poznávacích značek (palet).

U metod pro zachytávání výstupní hmotnosti lze v možnosti **Podle jednotky skutečné hmotnosti** určit, že vážení má být provedeno pro každou jednotku skutečné hmotnosti (například dle krabice). Možnost **Podle jednotky vyskladnění** umožňuje určit, že hmotnost má být zachycena na základě množství, které bude vyskladněno (například tři krabice). Všimněte si, že pro proces výdeje řádku výroby a interních procesů pohybu se použije průměrná hmotnost, pokud není použita možnost **Nezaznamenáno**.

V zásadě zpracování položek se skutečnou hmotností je definována metoda zachycování více hmotností. Každý parametr metody zachycování hmotností se používá v různých transakcích. V následující tabulce je uvedeno shrnutí parametrů, které transakce používají.

| Metoda                                     | Transakce                                |
|--------------------------------------------|--------------------------------------------|
| Metoda zaznamenání odchozí hmotnosti           | Vyskladňování prodeje, vyskladňování pro převod            |
| Metoda zaznamenání hmotnosti výrobní výdejky | Vyskladňování pro výrobu, spotřeba pro výrobu |
| Metoda zaznamenání hmotnosti přesunu           | Přesun                                   |
| Kdy má být zaznamenána oprava hmotnosti       | Množství úpravy, počítání                      |
| Metoda výpočtu zaznamenání hmotnosti           | Inventura                                   |
| Metoda zaznamenání hmotnosti převodu skladu | Převod skladu                         |

Pokud chcete zamezit procesům vyskladnění správy skladu zaznamenat hmotnost, jejichž důsledkem jsou úpravy skutečné hmotnosti/ztrát, můžete použít metodu odchylky od původní hmotnosti. Metoda odchylky výstupní hmotnosti se používá při následujících procesech mobilního zařízení: výdej prodeje, převod výdeje, výdej výroby, pohyby, inventura a převody skladu. Možnost **Omezit odchylku hmotnosti** můžete použít v případě, že se hmotnost položky se skutečnou hmotností během skladového skladování nemění a pokud nejsou vyžadovány úpravy zisku/ztráty skutečné hmotnosti. Možnost **Povolit odchylku hmotnosti** lze použít v případě, že se hmotnost může kolísat, a pokud je při záznamu fluktuace hmotnosti vyžadována úprava zisku/ztráty skutečné hmotnosti.

## <a name="unsupported-scenarios"></a>Nepodporované scénáře

Ne všechna workflow podporují zpracování produktu se skutečnou hmotností pomocí řízení skladu. Aktuálně platí následující omezení. Vztahují se na všechny položky se skutečnou hmotností bez ohledu na to, zda jsou označeny.

### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Konfigurace produktů se skutečnou hmotností pro procesy řízení skladu

- Pouze zpracování receptury je podporováno pro produkty se skutečnou hmotností (nikoliv kusovníky).
- Produkty se skutečnou hmotností nelze přiřadit ke skupině sledovací dimenze pomocí dimenze vlastníka.
- Produkty se skutečnou hmotností nelze použít jako služby.
- Produkty se skutečnou hmotností lze použít jako produkty na skladě pouze jako součást skupiny modelu položky.
- Produkty se skutečnou hmotností nelze použít společně s funkcí ke sledování „Aktivní v prodejním procesu.“
- Produkty se skutečnou hmotností nelze použít společně s funkcí pro záznam sériových čísel. Proto produkty nemohou být převedeny z prázdných na sériové číslo jako součást procesu výdeje/balení.
- Produkty se skutečnou hmotností nelze použít společně s funkcí pro registraci sériových čísel před spotřebou
- Produkty se skutečnou hmotností, které mají povolenou variantu, nelze použít společně s funkcí pro převod měrných jednotek variant.
- Produkty se skutečnou hmotností nelze označit jako obchodní sadu produktů.
- Produkty se skutečnou hmotností lze použít pouze se skupinou klasifikace jednotky, která má manipulační jednotky skutečné hmotnosti a která má jednotku skutečné hmotnosti jako nejnižší sekvenci.
- U produktů se skutečnou hmotností lze převést skladovou jednotku na jednotku skutečné hmotnosti pouze tehdy, pokud převod vyprodukuje nominální množství větší než 1.
- Nastavení čárových kódů pro produkty se skutečnou hmotností nepodporuje nastavení proměnné hmotnosti.

### <a name="order-processing"></a>Zpracování objednávky

- Vytvoření avíza expedice zboží expedice (ASN/struktury balení) nepodporuje informace o hmotnosti.
- Objednané množství musí být spravované na základě jednotky skutečné hmotnosti.

### <a name="inbound-warehouse-processing"></a>Příchozí zpracování skladu

- Přijetí poznávacích značek vyžaduje, aby byly hmotnosti přiřazeny při registraci, vzhledem k tomu, že informace o hmotnosti není podporována jako součást avíza expedice zboží. Když se používají procesy štítku skutečné hmotnost, musí být číslo štítku ručně přiřazen o podle jednotky skutečné hmotnosti.
- Pro produkty se skutečnou hmotností není podporována kontrola příchozí kvality. Pokud je tato možnost nakonfigurována, bude práce kontroly kvality přeskočena.

### <a name="inventory-and-warehouse-operations"></a>Operace skladů a zásob

- Ruční vytváření karanténních příkazů není podporováno pro produkty se skutečnou hmotností.
- Ruční přesun zásob související s otevřenou prací není podporováno pro produkty se skutečnou hmotností.
- Načtení poznávací značky pro inicializaci naskladnění skladu není podporováno pro produkty se skutečnou hmotností.
- Procesy vyvážení dávky nejsou podporovány pro produkty se skutečnou hmotností.
- Zpracování negativních fyzických zásob není podporováno pro produkty se skutečnou hmotností.
- Označení zásob nelze použít pro produkty se skutečnou hmotností.

### <a name="outbound-warehouse-processing"></a>Odchozí zpracování skladu

- Funkce pro výdej v seskupení není podporována pro produkty se skutečnou hmotností.
- Zpracování výdeje a balení skladu není podporováno pro produkty se skutečnou hmotností.
- U produktů se skutečnou hmotností nelze práci definovanou v šabloně práce spustit automaticky.
- U produktů se skutečnou hmotnosti systém nepodporuje ruční zpracování stanice balení, kde je práce výdeje zabaleného kontejneru vytvořena po uzavření kontejnerů.
- Funkce pro skenování kus po kusu není podporována pro produkty se skutečnou hmotností.

### <a name="production-processing"></a>Zpracování výroby

- U produktů se skutečnou hmotností jsou podporovány pouze dávkové objednávky pro produkty receptury.
- Funkce kanbanu není podporována pro produkty se skutečnou hmotností.
- U produktů se skutečnou hmotností nelze registrovat sériová čísla před spotřebou.
- Funkce pro stornování poznávacích značek z výroby není podporována pro produkty se skutečnou hmotností.
- U produktů se skutečnou hmotností nelze vykazování jako dokončené registrovat podle sériového čísla.

### <a name="transportation-management-processing"></a>Zpracování správy přepravy

- Pracovní plocha sestavení vytížení není podporována pro produkty se skutečnou hmotností.
- Řádky požadavků na přepravu nejsou podporovány pro produkty se skutečnou hmotností.

### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Další omezení a chování pro zpracování produktů se skutečnou hmotností se správou skladu

- Během procesů výdeje, kde není uživatel vyzván k identifikaci sledovacích dimenzí, se provádí přiřazení hmotnosti na základě průměrné hmotnosti. K tomuto chování dochází například v případě, že je ve stejném umístění použita kombinace sledovacích dimenzí a poté, co uživatel zpracuje výdej, zůstane v umístění pouze jedna hodnota sledovací dimenze.
- Pokud jsou zásoby rezervovány pro produkt se skutečnou hmotností, který je konfigurován pro procesy správy skladu, rezervace se provádí na základě definované minimální hmotnosti, a to i v případě, že je toto množství naposledy zpracovávané množství zásob na skladě. Toto chování se liší od chování pro položky, které nejsou nakonfigurovány pro procesy správy skladu. V tomto omezení existuje jedna výjimka. U výrobního výdeje se při výběru posledního manipulačního množství produktu se skutečnou hmotností, které je řízeno sériovým číslem, použije skutečná hmotnost.
- Procesy, které používají hmotnost jako součást výpočtů kapacity (prahové hodnoty vln, maximální pracovní přestávky, maxima kontejnerů, kapacit vytížení místa atd.) nepoužívají skutečnou hmotnost zásob. Místo toho jsou procesy založeny na fyzické hmotnosti zpracování definované pro produkt.
- Obecně není funkce Commerce podporována pro produkty se skutečnou hmotností.
- U produktů se skutečnou hmotností nelze stav zásob aktualizovat ze **Změny stavu skladu**.

### <a name="catch-weight-tags"></a>Štítky skutečné hmotnosti

Značku skutečné hmotnosti lze vytvořit pomocí procesu aplikace skladu, ručně ve formuláři nebo pomocí procesu datové entity. Pokud je značka skutečné hmotnosti přidružena k příchozí řádce zdrojového dokumentu, jako je řádka nákupní objednávky, značka bude zaregistrována. Je-li řádek použit pro zpracování výstupu, bude značka aktualizována jako dodaná.

Kromě omezení, která aktuálně platí pro produkty se skutečnou hmotností, mají produkty se značkou skutečné hmotnostmi v současné době jiná omezení.

- Všechny ruční aktualizace zásob (tj. aktualizace, které nejsou prováděny pomocí mobilního zařízení), musí zahrnovat odpovídající ruční aktualizace do přidružených značek skutečné hmotnosti, protože tyto aktualizace nejsou prováděny automaticky. Například ruční deníky úprav budou aktualizovat zásoby, ale ne asociované značky skutečné hmotnosti.
- Značky skutečné hmotnosti je nutné ručně aktualizovat, aby odrážely pohyby doplnění práce. Důvodem je skutečnost, že systém nemůže zachytit hmotnost při zpracování práce doplnění, a proto zaznamená průměrnou hmotnost.
- Přijetí smíšené registrační značky není aktuálně podporováno pro položky se značkou skutečné hmotnosti.
- Zpracování objednávky prodejní vratky může zaznamenat značky skutečné hmotnosti. Proces však neověřuje, zda je vracená značka shodná s tagem, která byla původně expedována pro prodejní objednávku.
- Položka nabídky mobilního zařízení, která obsahuje kód aktivity **Zaregistrovat spotřebu materiálu**, aktuálně nepodporuje záznamy skutečné hmotnosti.
- Ačkoliv jsou pro položky se značkou skutečné hmotností podporovány procesy počítání, jsou omezeny. Můžete například použít možnosti mobilního zařízení pro inventarizaci položek se značkou skutečné hmotnosti a použít průměrnou hmotnost. Avšak značky se skutečnou hmotností nejsou automaticky aktualizovány transakcí inventury. Po dokončení inventury transakcí je nutné ručně aktualizovat značky skutečné hmotnosti, aby odrážely zásoby. Pokud se položky, které nebyly původně umístěny do skladového místa, započítávají do tohoto skladového místa, použije se nominální hmotnost.
- Konsolidace registračních značek aktuálně nepodporuje položky se značkou skutečné hmotnosti.
- Funkce stornovat práci není podporována u položek se značkou skutečné hmotnosti, které jsou sledovány dle čísla značky.

> [!NOTE]
> Předchozí informace o štítcích se skutečnou hmotností jsou platné pouze v případě, že produkt se skutečnou hmotností má metodu sledování dimenze skutečné hmotnosti, která je plně sledována (tj. pokud je parametr **Metoda sledování dimenze značky skutečné hmotnosti** u zásad zpracování položek skutečné hmotnosti nastaven na hodnotu **Dimenze produktu, sledovací dimenze a všechny dimenze uskladnění**). Je-li položka se skutečnou hmotností pouze částečně sledována (tj. pokud je parametr **Metoda sledování dimenze značky skutečné hmotnosti** nastaven na **Dimenze produktu, sledovací dimenze a stav zásob**), použijí se další omezení. Vzhledem k tomu, že značka a zásoby v tomto případě ztratí viditelnost, některé další scénáře nejsou podporovány.
