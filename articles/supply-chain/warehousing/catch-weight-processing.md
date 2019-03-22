---
title: Zpracování produktu se skutečnou hmotností pomocí řízení skladu
description: Toto téma popisuje způsob použití šablon práce a směrnic skladového místa k určení, jak a kde se práce ve skladu provádí.
author: perlynne
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCatchWeightTag, WHSCatchWeightItemHandlingPolicy
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-1-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: ced22a144e57b624ceacb8bb5c3032218db3a0eb
ms.sourcegitcommit: bacec397ee48ac583596be156c87ead474ee07df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2019
ms.locfileid: "777265"
---
# <a name="catch-weight-product-processing-with-warehouse-management"></a>Zpracování produktu se skutečnou hmotností pomocí řízení skladu

[!include [banner](../includes/banner.md)]

## <a name="feature-exposure"></a>Expozice funkce

Chcete-li použít řízení skladu pro zpracování produktů se skutečnou hmotností, musíte pro zapnutí této funkce použít licenční konfigurační klíč. (Přejděte do nabídky **Správa systému \> Nastavení \> Konfigurace licence**. Poté na kartě **Konfigurační klíče** kartu rozbalte **Obchod \> Řízení skladu a správy přepravy** a zaškrtněte políčko u možnosti **Skutečná hmotnost pro sklad**).

> [!NOTE]
> Musí být zapnuty licenční konfigurační klíče pro možnosti **Řízení skladu a správy přepravy** i **Zpracování distribuce \> Skutečná hmotnost**.

Po zapnutí licenčního konfiguračního klíče můžete při vytvoření uvolněného produktu zvolit **Skutečná hmotnost**. Můžete také přidružit uvolněný produkt ke skupině dimenze úložiště, pro kterou je zvolen parametr **Použít procesy řízení skladu**.

Než budete moci produkt použít v řízení skladu, musíte provést několik základních nastavení pro konkrétní produkt týkajících se skutečné hmotnosti.

- Definujte převod nominální hmotnosti mezi jednotkou skutečné hmotnosti (pole) a jednotkou zásob (kilogram \[kg\]) jako součást definice převodu jednotek.
- Definujte tolerance minimální a maximální hmotnosti v rámci nastavení jednotky skutečné hmotnosti.
- Nastavte skupinu klasifikace jednotek, kde je jednotka skutečné hmotnosti definována jako nejnižší skladová jednotka zásob (SKU).
- Nastavte zásadu zpracování položky se skutečnou hmotností.

Další informace naleznete v tématu [Nastavení a správa položek se skutečnou hmotností](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-catch-weight-items).

## <a name="transaction-adjustments"></a>Úpravy transakce

Vzhledem k tomu, že hmotnost zásob, když se dostanou do skladu, se může lišit od hmotnosti, když jsou zásoby vydány ze skladu, musí zpracování produktu se skutečnou hmotností upravit zásoby.

**Příklad 1**

Během výrobního procesu **Ohlásit jako dokončené** je zaznamenaná vstupní hmotnost registrační značky obsahující osm krabic produktu se skutečnou hmotností jako 80,1 kg. Registrační značka pak odložení uložena v oblasti hotových výrobků a během doby skladování některé hmotnost dojde ke ztrátě do ovzduší.

Později, jako součást procesu výdeje prodejní objednávky, je váha stejné poznávací značky zaznamenána jako 79,8 kg. Proto v systému nyní máte hmotnostní rozdíl jako součást sady fyzické dimenze.

V takovém případě systém automaticky upraví rozdíl zaúčtováním transakce pro chybějící 0,3 kg.

**Příklad 2**

Ve své definici je produkt nastaven tak, aby toleroval minimální hmotnost 8 kg a maximální hmotnost 12 kg pro jednotku skutečné hmotnosti **Krabice**.

Máte dvě krabice produktu a jejich registrovaná hmotnost je 16 kg. Pokud pracovník skladu vybere a zváží jednu z krabic a váha je zaznamenána jako 9 kg, zbývající krabice bude vážit 7 kg. Protože 7 kg je však nižší než minimální hmotnost, systém provede automatickou úpravu k navýšení hmotnosti na skladě o 1 kg.

Chcete-li nastavit účty, do kterých jsou zaúčtovány tyto úpravy, přejděte na **Správa nákladů \> Nastavení zásad integrace hlavní knihy \> Zaúčtování**. Poté na kartě **Zásoby** definujte následující účty:

- Účet ztrát – skutečná hmotnost
- Účet zisků – skutečná hmotnost

## <a name="catch-weight-item-handling-policy"></a>Zásada zpracování položky se skutečnou hmotností

Zásada zpracování položky se skutečnou hmotností definuje dva primární toky správy skladu pro položky: kdy je hmotnost zboží zaznamenána a jakým způsobem je zaznamenána.

Můžete určit, kdy je hmotnost zaznamenána pro zpracování prodejní objednávky a převodního příkazu. Hmotnost lze zaznamenat během jednoho ze dvou následujících procesů:

- **Výdej** – Hmotnost je zaznamenaná během řádků práce počátečního vyskladnění práce objednávky.
- **Balení** – Hmotnost je zaznamenaná během ručního balení. (Je nutné odeslat položky do stanice balení.)

Pokud je během procesů balení kontejneru zaznamenána skutečná hmotnost na balicí stanici, pracovníci skladu nebudou vyzváni k záznamu hmotnost během práce výdeje. Namísto toho bude průměrná hmotnost fyzických zásob použita jako hmotnost vyskladněných zásob, které jdou do oblasti balení.

Pro interní procesy správy skladu, jako je inventura a opravy, je možné určit, zda by měla být zaznamenána hmotnost či nikoli. Pokud není zaznamenána, bude použita nominální hmotnost.

Můžete také definovat, jakým způsobem je hmotnost zaznamenána. V jednom ze dvou hlavní toků jsou štítky skutečné hmotnosti sledovány a používány k záznamu hmotnosti. V druhém toku nejsou štítky skutečné hmotnosti sledovány.

- **Ano** – Položka používá štítky skutečné hmotnosti. Číslo každého štítku představuje jednu jednotku skutečné hmotnosti (krabice) a ke štítku je přidružena hmotnost a jiné informace Pro odchozí procesy se použije hmotnost přidružená ke štítku.
- **Ne** – Položka nepoužívá štítky skutečné hmotnosti. Příchozí a odchozí procesy vážení jsou založeny na skutečné hmotnosti zaznamenané během každého procesu.

Proces sledování štítků skutečné hmotnosti lze použít pro položky, které nezmění hmotnost během doby skladování. Hmotnost bude zaznamenána pouze v průběhu vstupního procesu skladu. V průběhu odchozího procesu budou štítky skutečné hmotnosti pouze naskenovány, a hmotnosti, které jsou přidruženy ke štítkům se použijí pro zpracování odchozí transakce.

### <a name="how-to-capture-catch-weight"></a>Jak zaznamenat skutečnou hmotnost

Když se používá sledování štítku skutečné hmotnosti, musí být štítek vždy vytvořen pro každou jednotku skutečné hmotnosti, která je přijata, a každý štítek musí být vždy přiřazen k hmotnosti.

Například **Krabice** je jednotka skutečné hmotnosti a přijmete jednu paletu s osmi krabicemi. V takovém případě se musí vytvořit osm jedinečných štítků skutečné hmotnosti a hmotnost musí být přiřazena ke každému štítku. V závislosti na štítku příchozí skutečné hmotnosti lze zaznamenat buď hmotnost všech osmi krabic a průměrná hmotnosti pak může být rozdělena na každou krabici, nebo lze zaznamenat jedinečnou hmotnost pro každou krabici.

Když se nepoužívá sledování štítků skutečné hmotnosti, lze zaznamenat hmotnost pro každou sadu dimenzí, (například pro každou poznávací značku a sledovací dimenzi). Případně lze zaznamenat hmotnost podle agregované úrovně, například pět poznávacích značek (palet).

Pro metody zaznamenání výstupní hmotnosti lze definovat, zda se vážení provádí pro každou jednotku skutečné hmotnosti (to znamená pro krabici), nebo zda je zachycena hmotnost na základě množství, které bude vyskladněno (například tři krabice). Všimněte si, že pro proces výdeje řádku výroby se použije průměrná hmotnost, pokud není použita možnost **Nezaznamenáno**.

## <a name="supported-scenarios"></a>Podporované scénáře

Ne všechna workflow podporují zpracování produktu se skutečnou hmotností pomocí řízení skladu. Aktuálně platí následující omezení.
 
### <a name="configuring-catch-weight-products-for-warehouse-management-processes"></a>Konfigurace produktů se skutečnou hmotností pro procesy řízení skladu

- Pro produkty se skutečnou hmotností nelze u položek změnit skupinu dimenze úložiště (tak, aby pro ně bylo možné použít procesy správy skladu).
- Pouze zpracování receptury je podporováno pro produkty se skutečnou hmotností (nikoliv kusovníky).
- Produkty se skutečnou hmotností nelze přiřadit ke skupině sledovací dimenze pomocí dimenze vlastníka.
- Produkty se skutečnou hmotností nelze použít jako služby.
- Produkty se skutečnou hmotností lze použít jako produkty na skladě pouze jako součást skupiny modelu položky.
- Produkty se skutečnou hmotností nelze použít společně s funkcí ke sledování „Aktivní v prodejním procesu.“
- Produkty se skutečnou hmotností nelze použít společně s funkcí pro záznam sériových čísel. Proto produkty nemohou být převedeny z prázdných na sériové číslo jako součást procesu výdeje/balení.
- Produkty se skutečnou hmotností nelze použít společně s funkcí pro registraci sériových čísel před spotřebou
- Produkty se skutečnou hmotností, které mají povolenou variantu, nelze použít společně s funkcí pro převod měrných jednotek variant.
- Produkty se skutečnou hmotností nelze označit jako maloobchodní sadu produktů.
- Produkty se skutečnou hmotností lze použít pouze se skupinou klasifikace jednotky, která má manipulační jednotky skutečné hmotnosti a která má jednotku skutečné hmotnosti jako nejnižší sekvenci.
- U produktů se skutečnou hmotností lze převést skladovou jednotku na jednotku skutečné hmotnosti pouze tehdy, pokud převod vyprodukuje nominální množství větší než 1.
- Nastavení čárových kódů pro produkty se skutečnou hmotností nepodporuje nastavení proměnné hmotnosti.
 
### <a name="order-processing"></a>Zpracování objednávky

- Mezipodnikové zpracovávání objednávek není podporováno.
- Vytvoření avíza expedice zboží expedice (ASN/struktury balení) nepodporuje informace o hmotnosti.
- Objednané množství musí být spravované na základě jednotky skutečné hmotnosti.
 
### <a name="inbound-warehouse-processing"></a>Příchozí zpracování skladu

- Přijetí poznávacích značek vyžaduje, aby byly hmotnosti přiřazeny při registraci, vzhledem k tomu, že informace o hmotnosti není podporována jako součást avíza expedice zboží. Když se používají procesy štítku skutečné hmotnost, musí být číslo štítku ručně přiřazen o podle jednotky skutečné hmotnosti.
- Přijetí smíšených poznávacích značek není podporováno pro produkty se skutečnou hmotností.
 
### <a name="inventory-and-warehouse-operations"></a>Operace skladů a zásob

- Ruční vytváření karanténních příkazů není podporováno pro produkty se skutečnou hmotností.
- Ruční přesun zásob související s prací není podporováno pro produkty se skutečnou hmotností.
- Konsolidace poznávacích značek není podporováno pro produkty se skutečnou hmotností.
- Změny stavu skladu jako součást pravidelných úloh nejsou podporovány pro produkty se skutečnou hmotností.
- Změny stavu zásob, které jsou definovány podle dotazu, nejsou podporovány pro produkty se skutečnou hmotností. (Nejsou podporovány ani změny stav zásob objednávky kvality.)
- U produktů se skutečnou hmotností nelze změnit stav zásob ze stránky **Množství na skladě podle místa**.
- U produktů se skutečnou hmotností nelze změnit stav zásob jako součást práce přesunu aplikace skladu.
- Načtení poznávací značky pro inicializaci naskladnění skladu není podporováno pro produkty se skutečnou hmotností.
- Procesy vyvážení dávky nejsou podporovány pro produkty se skutečnou hmotností.
- Zpracování negativních fyzických zásob není podporováno pro produkty se skutečnou hmotností.
- Označení zásob nelze použít pro produkty se skutečnou hmotností.
 
### <a name="outbound-warehouse-processing"></a>Odchozí zpracování skladu

- Funkce pro výdej v seskupení není podporována pro produkty se skutečnou hmotností.
- Zpracování výdeje a balení skladu není podporováno pro produkty se skutečnou hmotností.
- Pro produkty se skutečnou hmotností nelze dokončit práci ze stránky **Práce**.
- U produktů se skutečnou hmotností lze práci definovanou v šabloně práce spustit automaticky.
- Funkce pro stornování práce není podporována pro produkty se skutečnou hmotností.
- U produktů se skutečnou hmotnosti není podporováno ruční zpracování stanice balení, kde je práce vytvořena po uzavření kontejnerů.
- Funkce pro skenování kus po kusu není podporována pro produkty se skutečnou hmotností.
 
### <a name="production-processing"></a>Zpracování výroby

- U produktů se skutečnou hmotností jsou podporovány pouze dávkové objednávky pro produkty receptury.
- Funkce kanbanu není podporována pro produkty se skutečnou hmotností.
- U produktů se skutečnou hmotností nelze registrovat sériová čísla před spotřebou.
- Funkce pro stornování poznávacích značek není podporována pro produkty se skutečnou hmotností.
- U produktů se skutečnou hmotností lze vykazování jako dokončené registrovat podle sériového čísla.

### <a name="transportation-management-processing"></a>Zpracování správy přepravy

- Pracovní plocha sestavení vytížení není podporována pro produkty se skutečnou hmotností.
- Řádky požadavků na přepravu nejsou podporovány pro produkty se skutečnou hmotností.
 
### <a name="other-restrictions-and-behaviors-for-catch-weight-product-processing-with-warehouse-management"></a>Další omezení a chování pro zpracování produktů se skutečnou hmotností se správou skladu

- Když jsou štítky skutečné hmotnosti zaznamenány jako součást zpracování aplikace, uživatel nemůže provést zrušení z workflow.
- Během procesů výdeje, kde není uživatel vyzván k identifikaci sledovacích dimenzí, se provádí přiřazení hmotnosti na základě průměrné hmotnosti. K tomuto chování dochází například v případě, že je ve stejném umístění použita kombinace sledovacích dimenzí a poté, co uživatel zpracuje výdej, zůstane v umístění pouze jedna hodnota sledovací dimenze.
- Pokud jsou zásoby rezervovány pro produkt se skutečnou hmotností, který je konfigurován pro procesy správy skladu, rezervace se provádí na základě definované minimální hmotnosti, a to i v případě, že je toto množství naposledy zpracovávané množství zásob na skladě. Toto chování se liší od chování pro položky, které nejsou nakonfigurovány pro procesy správy skladu.
- Procesy, které používají hmotnost jako součást výpočtů kapacity (prahové hodnoty vln, maximální pracovní přestávky, maxima kontejnerů, kapacit vytížení místa atd.) nepoužívají skutečnou hmotnost zásob. Místo toho jsou procesy založeny na fyzické hmotnosti zpracování definované pro produkt.
- Obecně není funkce Retail podporována pro produkty se skutečnou hmotností.
 
### <a name="catch-weight-tags"></a>Štítky skutečné hmotnosti

V současné době je funkce štítků skutečné hmotnosti podporována pouze jako součást následujících scénářů:

- Při zpracování příjmu aplikace skladu nákupní objednávky.
- Při zpracování příjmu vytížení prostřednictvím aplikace skladu.
- Pro příjem poznávací značky, který se vztahuje k nákladu nákupní objednávky, se požaduje přiřazení hmotnosti během procesu příjmu. Naopak pro příjem převodního příkazu se používá pro převodní příkaz hmotnost z data expedice.
- Pro položku převodního příkazu a příjem řádku, který pochází z procesu správy skladu.
- Zpracování příjmu objednávky prodejní vratky může zaznamenávat štítky skutečné hmotnosti, ale zpracování nebude ověřeno, pokud jsou štítky stejné štítky, které byly původně dodány pro konkrétní řádek prodejní objednávky.
- Když se zpracování stavu zásob změnilo pomocí aplikace skladu.
- Když je převod skladu proveden pomocí aplikace skladu.
- Při zpracování příchozích a odchozích úprav prostřednictvím aplikace skladu.
- Když je práce výdeje zpracovávána pro prodejní objednávky a převodní příkazy. (Mějte na paměti, že štítky skutečné hmotnosti nelze zaznamenat pro výdej výrobních komponent.)
- Když je vyskladněné množství sníženo z řádků vytížení, bez ohledu na to, zda se používají kontejnery.
- Když jsou produkty zabaleny do kontejnerů ve stanici balení.
- Když jsou kontejnery znovu otevřeny.
- Když jsou produkty receptury vykazovány jako dokončené pomocí aplikace skladu.
- Při zpracování nákladů přepravy s použitím aplikace skladu.
