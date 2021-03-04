---
title: Nastavení uznání výnosů
description: Toto téma popisuje možnosti nastavení pro uznání výnosů a jejich dopady.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: b90c98628fef2006addb64a6b880ab4020edb8cd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995559"
---
# <a name="revenue-recognition-setup"></a>Nastavení uznání výnosů
[!include [banner](../includes/banner.md)]

Byl přidán nový modul **Uznání výnosů**, který obsahuje položky nabídky pro veškerá požadovaná nastavení. Toto téma popisuje možnosti nastavení a jejich dopady.

> [!NOTE]
> Funkci uznání výnosů nelze zapnout prostřednictvím správy funkcí. V současné době ji aktivujete pomocí konfiguračních klíčů.

> Uznání výnosů (včetně funkce sady) nelze použít v kanálech Commerce (elektronické obchodování, POS, kontaktní středisko). Položky konfigurované s uznáním výnosů nesmí být přidány na objednávky nebo do transakcí vytvořených v kanálech Commerce.

Modul **Uznání výnosů** má následující možnosti nastavení:

- Deníky uznání výnosů
- Parametry pro uznání výnosů
- Plány výnosů 
- Nastavení zásob

    - Skupiny položek a uvolněné produkty
    - Definování plánu výnosů
    - Definování výnosové ceny

        - Účetní profily
        - Sady

    - Komponenty sady
    - Položka sady

- Nastavení projektu

## <a name="revenue-recognition-journals"></a>Deníky uznání výnosů

Pro uznání výnosů byl zaveden nový typ deníku. Deník je povinný a používá se ve dvou scénářích.

První scénář nastane poté, co jsou splněny všechny smluvní závazky, když je odložený výnos uznán vytvořením deníku uznání výnosů, který je založen na podrobnostech plánu výnosů. Deník obsahuje účetní položku, která přesouvá zůstatek z účtu hlavní knihy odložených výnosů na účet hlavní knihy výnosů.

Druhý scénář nastane, když je deník vytvořen poté, co dojde k opakovanému přidělení. K opětovnému přidělení dochází, když je řádek prodejní objednávky přidán k dříve fakturované prodejní objednávce, nebo když je vytvořena nová prodejní objednávka obsahující řádek, který je součástí původní smlouvy. Pokud byla faktura zaúčtována před přidáním nového řádku prodejní objednávky, musí být pro zaúčtovanou fakturu zákazníka vytvořena účetní opravná položka.

Deník se nastavuje na stránce **Názvy deníku** (**Uznání výnosů \> Nastavení \> Názvy deníku**). Typ deníku musí být nastaven na **Uznání výnosů**. Deník uznání výnosů vám umožňuje vybrat účtovací vrstvu, do které se má provést zaúčtování.

## <a name="parameters-for-revenue-recognition"></a>Parametry pro uznání výnosů

Nastavení uznání výnosů se konfigurují na kartě **Uznání výnosů** stránky **Parametry hlavní knihy** (**Uznání výnosů \> Nastavení \> Parametry hlavní knihy**). K dispozici jsou následující nastavení:

- **Název deníku uznání výnosů** – Zvolte deník, který byl vytvořen pro uznání výnosů. Deník je povinný, když jsou výnosy uznány z plánu výnosů, nebo když provedete opětovné přidělení pro prodejní objednávku, která již byla fakturována.
- **Povolit metodu přidělení slevy** – Tuto možnost nastavte na **Ano**, abyste určili výnosovou cenu přidělením reálné tržní hodnoty, která je definována ve výnosové ceně každého uvolněného produktu. Toto přidělení zahrnuje přidělení jakýchkoliv řádkových slev napříč položkami. Pokud je tato možnost nastavena na **Ne**, systém použije střední cenu, která je definována ve výnosové ceně každého uvolněného produktu. Pokud je tato možnost nastavena na **Ne**, ale pro uvolněné produkty není nastavena žádná střední cena, k přidělení výnosové ceny nedojde.
- **Zahrnout slevy záhlaví** – Nastavte tuto možnost na **Ano** a určete výnosovou cenu přidělením slev záhlaví napříč produkty. Pokud je tato možnost nastavena na **Ne**, sleva záhlaví není zahrnuta v přidělení výnosové ceny.
- **Zakázat smluvní podmínky** - Tuto možnost nastavte na **Ano**, pokud produkty, které mají typ výnosu **Podpora po uzavření smlouvy**, lze uvolnit, i když pro ně nejsou definována data zahájení a ukončení smlouvy. Obvykle jsou pro položky typu výnosu **Podpora po uzavření smlouvy** požadována data zahájení a ukončení smlouvy. Pokud není definováno datum zahájení a ukončení smlouvy, vypočítají se podrobnosti plánu výnosů v účtování pomocí počtu událostí a data faktury.
- **Zaúčtovat opravy faktur do pohledávek při opětovném přidělení** - Když provedete opětovné přidělení faktur, které již byly zaúčtovány, musí být opravena účetní položka pro zaúčtovanou fakturu. Pomocí této možnosti můžete určit, jak se má oprava provést.

    - Tuto možnost nastavte na **Ne**, abyste omezili účtování opravné transakce do hlavní knihu. Pokud je tato možnost nastavena na **Ne**, nevytvářejí se v pohledávkách žádné další doklady k opravě interního účetnictví. Při uhrazení faktury se v procesu vyrovnání použije stará účetní položka k zaúčtování jakýchkoli platebních slev nebo realizovaných zisků nebo ztrát.
    - Tuto možnost nastavte na **Ano**, aby se automaticky vytvořil stornovací doklad a nová faktura za opravnou transakci v pohledávkách. Protože tato oprava je opravou interního účetnictví, nové dokumenty se zákazníkovi neposílají ani nesdělují. Stornovací doklad je vyrovnán na původní fakturu a nová opravená faktura je zaplacena zákazníkem. Všimněte si, že všechny tři dokumenty jsou zobrazeny v sestavách, například ve výkazu zákazníka.

[![Informace o nastavení](./media/revenue-recognition-setup-info.png)](./media/revenue-recognition-setup-info.png)

## <a name="revenue-schedules"></a>Plány výnosů

Pro každou událost, pro kterou lze výnosy odložit, musí být vytvořen plán výnosů. Pokud vaše organizace například poskytuje podporu po dobu šesti měsíců, 12 měsíců, 18 měsíců a 24 měsíců, musíte pro každé období vytvořit plán výnosů. Nastavení plánu výnosů určuje, jak bude výnosová cena přidělena mezi počet vybraných období. Určuje také výchozí data zadaná pro plán výnosů, který je vytvořen při zaúčtování faktury.

Pokud výnosy uznáte podle milníku, doporučujeme vám vytvořit plán uznání výnosů pro počet milníků, bez ohledu na data uznání. Po vytvoření plánů je můžete upravit tak, aby odrážely očekávaná data milníků. Tyto záznamy lze zablokovat, dokud nebudete upozorněni, že byl dosažen milník a výnosy lze uznat.

Plány výnosů se vytváří na stránce **Plány výnosů** (**Plány výnosů \> Nastavení \> Plány výnosů**).

[![Plány výnosů](./media/revenue-recognition-revenue-schedules.png)](./media/revenue-recognition-revenue-schedules.png)

Zadejte popisné hodnoty do polí **Plán výnosů** a **Popis**. Následující dodatečná nastavení se používají k vytvoření plánu výnosů po zaúčtování faktury.

- **Výskyty** – Zadejte počet měsíců nebo výskytů pro odložení výnosů.
- **Automatické blokování** – Zaškrtněte toto políčko, pokud by se všechny řádky plánu výnosů měly při zaúčtování faktury automaticky zablokovat. Blokování musí být ručně odstraněno z každého řádku plánu, než bude možné uznat odložený výnos řádku.
- **Automatické smluvní podmínky** – Toto políčko zaškrtněte, pokud mají být automaticky nastavena data zahájení a ukončení smlouvy. Tato data jsou automaticky nastavena pouze pro uvolněné produkty typu výnosů **Podpora po uzavření smlouvy**. Datum zahájení smlouvy je automaticky nastaveno na požadované datum expedice řádku prodejní objednávky a datum ukončení smlouvy je automaticky nastaveno na datum zahájení plus počet měsíců nebo výskytů, který je definován v nastavení plánu výnosů. Například produkt na řádku prodejní objednávky je pro jednoletou záruku. Pro tento plán výnosů je zaškrtnuto pole výchozího plánu výnosů **12M** (12 měsíců) a **Automatické smluvní podmínky**. Pokud řádek prodejní objednávky má požadované datum expedice 16. prosince 2019, výchozí datum zahájení smlouvy je 16. prosince 2019 a výchozí datum ukončení smlouvy je 15. prosince 2020.
- **Základ pro uznání** – Základ pro uznání určuje, jak je výnosová cena přidělena mezi výskyty.

    - **Měsíčně podle dat** – Částka je přidělena na základě skutečných dnů v každém měsíci.
    - **Měsíčně** – Částka je přidělena rovnoměrně mezi počet měsíců, který je definován ve výskytech.
    - **Výskyty** – Částka je přidělena rovnoměrně mezi výskyty, ale může zahrnovat období navíc, pokud jako způsob uznání vyberete **Skutečné počáteční datum**.

- **Způsob odpisu** – Způsob uznání určuje výchozí data, která jsou nastavena v plánu výnosů pro fakturu.

    - **Skutečné počáteční datum** – Plán je vytvořen buď pomocí data zahájení smlouvy (u položek podpory po uzavření smlouvy \[PCS\]), nebo podle data fakturace (u základních a nezákladních položek).
    - **Prvního v měsíci** – Datum v prvním řádku plánu je datum zahájení smlouvy (nebo datum fakturace). Všechny následující řádky plánů jsou však vytvořeny pro prvního v měsíci.
    - **Rozdělení v polovině měsíce** – Datum v prvním řádku plánu závisí na datu fakturace. Pokud je faktura zaúčtována mezi prvním až patnáctým dnem v měsíci, vytvoří se plán výnosů pomocí prvního dne v měsíci. Pokud je faktura zaúčtována šestnáctého a později, vytvoří se plán výnosů pomocí prvního dne v následujícím měsíci.
    - **Prvního v následujícím měsíci** – Datum v plánu je první den následujícího měsíce.

Volbou tlačítka **Podrobnosti plánu výnosů** zobrazíte obecná období a procenta, která jsou v každém období uznána. Ve výchozím nastavení je hodnota **Procento uznání** rovnoměrně rozdělena mezi počet období. Pokud je základ uznání nastaven buď na **Měsíčně** nebo **Výskyty**, procento uznání lze změnit. Když změníte procento uznání, varovná zpráva vás upozorní, že celková hodnota se nerovná 100 procentům. Pokud obdržíte zprávu, můžete pokračovat v úpravách řádků. Před zavřením stránky se však musí celkové procento rovnat 100.

[![Podrobnosti plánu výnosů](./media/revenue-recognition-revenue-schedule-details.png)](./media/revenue-recognition-revenue-schedule-details.png)

## <a name="inventory-setup"></a>Nastavení zásob

Výnosy za uvolněné produkty na prodejních objednávkách můžete uznat, nikoli však s prodejními kategoriemi na prodejních objednávkách nebo s volnými fakturami, pokud v dokumentu nejsou žádné položky. Výběr, který provedete při nastavování uvolněných produktů, určuje, jak budou uznány výnosy položky. Výběry například určují, zda je přidělena výnosová cena a zda je výnos odložen pomocí plánu výnosů.

Nastavení může začít na záložce s náhledem **Uznání výnosů** stránky **Skupina položek** (**Uznání výnosů \> Nastavení \> Nastavení zásob a produktů \> Skupina položek**). Tato stránka zahrnuje několik polí nastavení: Tato pole se používají k nastavení výchozích hodnot pouze pro nové uvolněné produkty vytvořené v systému. Při vytváření nových produktů se hodnoty, které zde nastavíte, zadávají ve výchozím nastavení pro skupinu položek. Výchozí hodnoty pro uvolněné produkty můžete přepsat na stránce **Uvolněné produkty** (**Uznání výnosů \> Nastavení \> Nastavení zásob a produktů \> Uvolněné produkty**). Výchozí hodnoty, které jsou nastaveny pro uvolněné produkty, se poté přenesou do prodejní objednávky.

## <a name="item-groups-and-released-products"></a>Skupiny položek a uvolněné produkty

### <a name="define-the-revenue-schedule"></a>Definování plánu výnosů

Výnosy na řádku prodejní objednávky jsou odloženy, pokud je pro uvolněný produkt definován plán výnosů a ve výchozím nastavení je použit na řádku prodejní objednávky. Pokud by se toto nastavení mělo ve výchozím nastavení použít pro produkt, můžete definovat plán příjmů na záložce s náhledem **Uznání výnosů** stránky **Skupina položek** (**Uznání výnosů \> Nastavení \> Nastavení zásob a produktů \> Skupina položek**). Můžete také definovat nastavení pro uvolněný produkt na záložce s náhledem **Uznání výnosů** stránky **Uvolněné produkty** (**Uznání výnosů \> Nastavení \> Nastavení zásob \> Uvolněné produkty**).

V poli **Plán výnosů** vyberte plán výnosů, který představuje období, na které musí být výnosy odloženy. Plán výnosů je automaticky zadán na řádku prodejní objednávky a podrobnosti plánu jsou vytvořeny při zaúčtování faktury prodejní objednávky.

### <a name="define-the-revenue-price"></a>Definování výnosové ceny

Skupiny položek a uvolněné produkty lze nastavit buď pomocí metody střední ceny nebo metody přidělení slevy. Obě metody vyžadují odlišná nastavení na stránce **Uvolněné produkty**.

- **Je aktivní pro přidělení výnosů** – Tuto možnost nastavte na **Ano**, chcete-li zahrnout uvolněný produkt do výpočtu přidělení výnosů. Pokud je tato možnost nastavena na **Ne**, uvolněný produkt použije metodu střední ceny, pokud je střední cena definována. Pokud není definována střední cena, použije se k zaúčtování do výnosů nebo odložených výnosů jednotková cena na řádku prodejní objednávky.
- **Typ výnosů** – Zvolte typ výnosů, který definuje uvolněný produkt.

    - **Základní** – Položka je primárním zdrojem výnosů organizace. Tato hodnota je výchozím nastavením.
    - **Nezákladní** – Položka není primárním zdrojem výnosů organizace. Při použití nastavení střední ceny je cena „převzata“ do střední ceny a poté přidělena. Například základní položka má pevnou cenu, která musí být uznána jako výnos. Pokud existuje sleva, může být sleva převzata z výnosů základní položky, ale **pouze** do výše pevné ceny. Zbytek slevy je vyňat z výnosů pro nezákladní položky. Alternativně nemusí být sleva převzata z výnosu základní položky.
    - **Podpora po uzavření smlouvy** – Tato položka podporuje další prvky, které jsou zahrnuty v prodeji zákazníkovi. Výnosová cena je rozdělena mezi základní a nezákladní produkty, které jsou součástí prodeje. V závislosti na nastavení nemusí položky PCS vyžadovat, aby byla na řádku prodejní objednávky definována data zahájení a ukončení smlouvy.

- **Vyloučit z převzetí** – Tuto možnost nastavte na **Ano**, čímž označíte, že střední cenu položky nelze upravit pod minimální definované procento nebo nad maximální procento. Jakákoli výnosová cena bude odvozena z výnosové ceny jiného uvolněného produktu, který je zahrnut v prodejní objednávce. Pokud je tato možnost nastavena na **Ne**, lze střední cenu položky upravit nebo převzít. Pokud prodáváte více než jednu položku, která je nastavena jako střední cena, musí být nastaven alespoň jeden uvolněný produkt, kde je možnost **Vyloučit z vyjmutí** nastavena na **Ne**. Tímto způsobem existuje alespoň jedna položka, ke které lze přidělit jakékoli rozdíly ve výnosové ceně.
- **Střední cena** - Nastavením této možnosti na **Ano** označíte, že by se měla výnosová cena položky upravit tak, aby se rovnala střední ceně, pokud je pod minimální určenou tolerancí, nebo nad maximální tolerancí, a že částka převzetí by měla být přidělena na řádky, které mají produkty, u kterých je možnost **Vyloučit z převzetí** nastavena na **Ne**.

    - **Maximální tolerance** – Zadejte procento nad střední cenou, které je povoleno.
    - **Minimální tolerance** – Zadejte procento pod střední cenou, které je povoleno.

Po dokončení konfigurace nastavení uvolněného produktu musíte ručně definovat výnosovou cenu zadáním reálné hodnoty nebo střední ceny (pokud používáte metodu střední ceny) na stránce **Výnosové ceny** (přejděte na **Uznání výnosů \> Nastavení \> Nastavení zásob \> Uvolněné produkty** a poté v podokně akcí na kartě **Prodej** ve skupině **Uznání výnosů** zvolte **Výnosové ceny**).

[![Výnosové ceny](./media/revenue-recognition-revenue-prices.png)](./media/revenue-recognition-revenue-prices.png)

Výnosová cena, která je ručně definována na této stránce, se používá k určení přidělení výnosové ceny na každé prodejní objednávce na základě definovaných kritérií. Každé kritérium je spárováno se řádkem prodejní objednávky, aby se určila výnosová cena, která by měla být použita v procesu přidělování.

- **Kód položky** a **Vztah položky** – Výnosová cena může být definována pro jednotlivý produkt nebo skupinu produktů. Pokud jste v poli **Kód položky** vybrali možnost **Tabulka**, vyberte uvolněný produkt v poli **Vztah položky**. Pokud jste v poli **Skupina** vybrali možnost **Tabulka**, vyberte skupinu položek v poli **Vztah položky**.
- **Kód účtu** a **Číslo skupiny/účtu** – Výnosová cena může být definována pro všechny zákazníky, jednotlivého zákazníka nebo skupinu zákazníků. Pokud jste v poli **Kód účtu** vybrali možnost **Vše**, cena se použije pro všechny zákazníky. Pokud jste v poli **Kód účtu** vybrali možnost **Tabulka**, vyberte zákazníka v poli **Číslo skupiny/účtu**. Pokud jste v poli **Kód účtu** vybrali možnost **Skupina**, vyberte skupinu zákazníků v poli **Číslo skupiny/účtu**.
- **Měna** – Pro každou měnu, ve které zadáte prodejní objednávku, musíte zadat samostatnou výnosovou cenu. Pokud například v současné době prodáváte v amerických dolarech, kanadských dolarech a eurech, musíte definovat výnosovou cenu ve všech třech měnách. Výnosová cena se nepřevádí z jedné měny, jako je zúčtovací měna, na jiné měny transakcí, které používáte.
- **Částka nebo procento ceníku** – Určete, zda je výnosová cena nastavena jako částka nebo jako procento z ceníkové ceny. Pokud zvolíte **Procento z ceníku**, uživatelé mohou zadat střední cenu jako procento z ceníkové ceny místo částky. Hodnota **Procento z ceníku** se používá pouze pro uvolněné produkty, které jsou nastaveny jako položky PCS.
- **Cena přidělení výnosů** – V závislosti na hodnotě, kterou jste vybrali v poli **Částka nebo procento ceníku**, zadejte částku nebo procento představující výnosovou cenu, která se používá k přidělení výnosů mezi prvky v prodejní objednávce.
- **Od data** a **Do data** – Zadejte časové období, pro které je výnosová cena aktivní. Tato pole jsou volitelná.

Pokud je možnost **Povolit metodu přidělení slevy** na stránce **Parametry hlavní knihy** nastavena na **Ano** pokud je pole **Typ výnosů** pro váš uvolněný produkt nataveno na **Podpora po uzavření smlouvy**, musíte také určit položky, které jsou podporovány uvolněným produktem. Toto nastavení se provádí na stránce **Základ nastavení** (přejděte na **Uznání výnosů \> Nastavení \> Nastavení zásob \> Uvolněné produkty** a poté v podokně akcí na kartě **Prodej** ve skupině **Uznání výnosů** zvolte **Základ nastavení**).

Na stránce **Základ nastavení** přidejte záznam pro každou skupinu položek, kterou položka podporuje. Pokud dojde k přidělení výnosů, bude výnosová cena rozdělena mezi základní a nezákladní části pro položku PCS.

### <a name="posting-profiles"></a>Účetní profily

Schopnost odložit výnosy jsou podporovány třemi dalšími typy účtování. Tyto typy účtování se nastavují na kartě **Prodejní objednávka** stránky **Zaúčtování** (**Uznání výnosů \> Nastavení \> Nastavení zásob a produktů \> Zaúčtování**).

- **Odložené výnosy** – Zadejte hlavní účet pro výnosovou cenu, která účtuje do odložených výnosů (místo výnosů). Výnosová cena je odložena, pokud má řádek prodejní objednávky plán výnosů.
- **Odložené náklady za prodané zboží** – Zadejte hlavní účet pro částku nákladů za prodané zboží, která se zaúčtuje do odložených nákladů za prodané zboží, pokud je výnos také odložen.
- **Clearing výnosů částečné faktury** – Zadejte hlavní účet pro clearingový účet, který se používá buď v případě, že je prodejní objednávka částečně fakturována, nebo když dojde k opakovanému přidělení. Zůstatek na tomto účtu se vrátí na 0 (nula), když jsou prodejní objednávky plně vyfakturovány.

### <a name="bundles"></a>Sady

Položky sady jsou jedinečné uvolněné produkty, které jsou nastaveny tak, aby zahrnovaly komponenty. Toto nastavení se provádí pomocí funkce kusovníku. Když je na prodejní objednávce zadána položka sady, jednotlivé komponenty se použijí ke stanovení výnosových cen a plánů výnosů. Tištěné dokumenty pro zákazníka, například prodejní objednávka a faktura, však odrážejí položku balíčku.

#### <a name="bundle-components"></a>Komponenty sady

Komponenty, které jsou zahrnuty v sadě, musí být nastaveny na stránce **Uvolněné produkty** (**Uznání výnosů \> Nastavení \> Nastavení zásob a produktů \> Uvolněné produkty**). Tyto komponenty jsou uvolněné produkty a musí být nastaveny stejným způsobem jako produkty, které jsou součástí kusovníku. Uvolněný produkt může být například položka typu **Položka** nebo **Služba**, ale musí být přiřazena ke skupině modelů položek, kde je volba **Produkt na skladě** nastavena na **Ano**. Další informace naleznete v dokumentaci nastavení pro položky kusovníku.

Komponenty musí být také nastaveny pro uznání výnosů, jako by to byly produkty, které lze prodat jednotlivě na prodejní objednávce. Například se ujistěte, že je pro každou komponentu definována správná výnosová cena a že pro položky PCS je nastaven základ ceny.

#### <a name="bundle-items"></a>Položky sady

Když nastavíte položku sady, musíte nastavit dvě pole na stránce **Uvolněné produkty** (**Uznání výnosů \> Nastavení \> Nastavení zásob a produktů \> Uvolněné produkty**):

- Na pevné záložce **Analyzovat** v poli **Typ výroby** musí být položka nastavena jako položka kusovníku.
- Na pevné záložce **Obecné** v poli **Sada** musí být položka označena jako položka sady.

Poté musí být komponenty přiřazeny k nadřazené položce sady/kusovníku na stránce **Verze kusovníku** (přejděte na **Uznání výnosů \> Nastavení \> Nastavení produktu a zásob \> Uvolněné produkty** a poté v podokně akcí na kartě **Analyzovat** ve skupině **Kusovník** zvolte **Verze kusovníku**). Další informace naleznete v dokumentaci nastavení pro kusovníky.

[![Uvolněné produkty, plány kusovníku](./media/revenue-recognition-bom-scheduleds.jpg)](./media/revenue-recognition-bom-scheduleds.jpg)

Pokud jsou nadřazená položka sady a komponenty sady nastaveny k přidělení, výnosová cena sady bude rozdělena do komponent na základě jejich procentuálního podílu výnosů.

## <a name="project-setup"></a>Nastavení projektu

Uznání výnosů lze rovněž použít pro prodejní objednávky, které jsou vytvořeny prostřednictvím projektů určených materiálem a časem. U prodejních objednávek, které pocházejí z projektů, stačí definovat hlavní účty v účetních profilech projektů, které se používají k účtování faktur projektu. Hlavní účty se definují na stránce **Nastavení účtování hlavní knihy** (**Uznání výnosů \> Nastavení \> Nastavení projektu \> Nastavení účtování hlavní knihy**).

- **Odložené výnosy faktury** – (pod **Výnosové účty**) - Zadejte hlavní účet pro výnosovou cenu, která účtuje do odložených výnosů (místo výnosů). Výnosová cena je odložena, pokud má řádek prodejní objednávky plán výnosů.
- **Odložené náklady** (pod **Nákladové účty**) – Zadejte hlavní účet pro částku nákladů za prodané zboží, která se zaúčtuje do odložených nákladů za prodané zboží, pokud je výnos také odložen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]