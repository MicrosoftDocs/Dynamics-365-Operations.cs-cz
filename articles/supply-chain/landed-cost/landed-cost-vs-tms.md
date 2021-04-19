---
title: Náklady za doručení a Správa přepravy
description: 'Microsoft Dynamics 365 Supply Chain Management poskytuje dva různé moduly pro práci s přepravou: Správa přepravy (TMS) a Náklady za doručení. Toto téma shrnuje funkce, které mají tyto dva moduly společné, a zdůrazňuje rozdíly mezi nimi.'
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: bb5ecaa237eed2a1902c965fd42b31cc1708a4e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833850"
---
# <a name="landed-cost-vs-transportation-management"></a>Náklady za doručení a Správa přepravy

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management poskytuje dva různé moduly pro práci s přepravou: **Správa přepravy** (TMS) a **Náklady za doručení**. Toto téma shrnuje funkce, které mají tyto dva moduly společné, a zdůrazňuje rozdíly mezi nimi. Tyto informace můžete použít k rozhodnutí, který modul nejlépe vyhovuje vašim obchodním praktikám. Možná zjistíte, že některé obchodní praktiky fungují lépe v TMS, zatímco jiné fungují nejlépe v modulu Náklady za doručení. Poté, v závislosti na vašich obchodních požadavcích, se můžete rozhodnout použít výhradně jeden modul, nebo můžete oba moduly kombinovat.

Toto téma není komplexním přehledem všech funkcí obou modulů. Místo toho zdůrazňuje dostupné funkce, protože se týká přepravy zboží od dodavatele do skladu vašeho podniku, kde jej lze spotřebovat.

## <a name="terminology-reference-data-and-reporting-differences"></a>Terminologie, referenční údaje a rozdíly ve vykazování

### <a name="terminology-comparison"></a>Porovnání terminologie

TMS a Náklady za doručení používají různé pojmy pro podobné koncepty. Následující tabulka obsahuje přehled pojmů a jejich použití ve dvou modulech.

| Pojem TMS | Pojem nákladů za doručení | Poznámky |
|----------|------------------|-------|
| **Načíst**<p>*Vytížení* je kolekce zásilek, které jsou přepravovány současně na stejné přepravní jednotce (jako je nákladní automobil nebo loď). Vytížení mohou být příchozí nebo odchozí.</p> | **Cesta**<p>*Cesta* je obvykle jediné plavidlo, které cestuje po jedné trase *(cestě)*. Cesta může obsahovat více *přepravních kontejnerů* a může také zahrnovat příchozí objednávky od různých právnických osob vaší organizace. Cesty mohou být pouze příchozí.</p> | TMS také používá pojem *číslo cesty*, které odkazuje na informační pole, kde můžete zadat identifikátor. K poli TMS však není přidružena žádná funkce a nesouvisí s konceptem *cesty* v Nákladech za doručení. |
| **Trasa**<p>*Trasa* je fyzická cesta přepravy z místa původu do místa určení.</p> | **Cesta**<p>*Cesta* je fyzická trasa přepravy z místa původu do místa určení. Každá cesta (plavba) musí být přiřazena k cestě (trase).</p> | |
| **Segmenty trasy**<p>Trasa může mít více *segmentů trasy*, z nichž každý představuje krok cesty. Trasa může zahrnovat více dopravců nebo služeb, z nichž každý je považován za segment trasy.</p> | **Úseky**<p>Každá cesta může mít více *úseků*, z nichž každý představuje krok cesty. Úsek může být součástí přepravy, celní manipulace nebo jiné aktivity.</p> | |
| **Kontejnery**<p>*Kontejnerem* může být libovolný druh obalu nebo balení, který používá aplikace TMS.</p> | **Přepravní kontejnery**<p>*Přepravní kontejner* je fyzický přepravní kontejner, známý z kontejnerových lodí.</p> | |
| **Kódy komodit**<p>V TMS (a na jiných místech v Supply Chain Management) identifikují *kódy komodit* typy komodit. Mohou ovlivnit tarify, manipulaci s nebezpečnými materiály atd.</p> | **Kódy komodit**<p>V nákladech za doručení jsou *kódy komodit* založeny na úrovni právnické osoby. Používají se většinou pro účely vytváření sestav.</p> | Náklady za doručení mohou také použít kódy komodit, které se používají v TMS a dalších místech aplikace Supply Chain Management. Kódy komodit modulu Náklady za doručení se však používají pouze v tomto modulu. |

### <a name="some-reference-data-isnt-shared"></a>Některá referenční data nejsou sdílena

TMS a Náklady za doručení nesdílejí referenční data pro entity, jako je nastavení nákladů, cesty a úseky. Pokud používáte oba moduly, musíte nesdílená referenční data znovu vytvořit.

### <a name="intercompany-reports-dont-work-with-goods-in-transit"></a><a name="intercompany-reports"></a>Mezipodnikové sestavy nefungují u přepravovaného zboží

Následující sestavy nefungují ve spojení s funkcí přepravovaného zboží, kterou poskytuje modul Náklady za doručení:

- [Sestava Celkové mezipodnikové přepravované zboží](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)
- [Sestava Celkové mezipodnikové přepravované zboží](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)

Tyto sestavy předpokládají, že přeprava zboží je zahájena, jakmile vydáte prodejní dodací list, a že je po přijetí převzato do skladu. Přepravované zboží však není takto zpracováno. Pokud tedy používáte přepravované zboží a mezipodnikové funkce společně, výsledky obou těchto sestav budou nesprávné.

## <a name="using-the-two-modules-together"></a>Společné použití obou modulů

TMS můžete použít pro příchozí i odchozí operace. Ačkoli modul Náklady za doručení poskytuje většinu stejných základních funkcí jako TMS pro příchozí operace, některé funkce také přidává. Proto je možná vhodné zvážit použití TMS pro odchozí operace a Náklady za doručení pro příchozí operace.

Obecně nedoporučujeme používat oba moduly společně pro příchozí operace. Měli byste použít modul, který nejlépe vyhovuje vašim požadavkům. Pokud tyto dva moduly používáte společně, nesmíte mezi nimi sdílet zdrojové dokumenty. Například nepoužívejte stejnou nákupní objednávku současně pro vytížení v TMS a cestu v modulu Náklady za doručení. Zejména musíte zajistit, že nenastavíte systém tak, aby automaticky vytvářel příchozí vytížení. Pokud jsou položky z nákupních objednávek zahrnuty do cesty, nelze s nimi zacházet jako s vytížením.

## <a name="goods-in-transit"></a>Přepravované zboží

Jedním z hlavních rysů Nákladů za doručení je schopnost modulu zpracovávat přepravované zboží. Zpracování přepravovaného zboží vám umožní převzít finanční vlastnictví přepravovaných položek před jejich fyzickým přijetím v cílovém skladu. Zpracování přepravovaného zboží je často nutné v mezinárodním obchodu.

### <a name="tms-goods-in-transit-features"></a>Funkce TMS pro přepravované zboží

TMS v současné době nepodporuje zpracování přepravovaného zboží.

### <a name="landed-cost-goods-in-transit-features"></a>Funkce modulu Náklady za doručení pro přepravované zboží

Zpracování přepravovaného zboží je primární funkcí modulu Náklady za doručení a poskytuje následující funkčnost:

- **Sklady přepravovaného zboží** – Sklady pro přepravované zboží lze přidružit ke každému skladu v Supply Chain Management. Zboží je převedeno do skladů přepravovaného zboží po fakturaci původní nákupní objednávky. Položky, které jsou tam fyzicky rezervovány, nebudou k dispozici pro spotřebu, dokud nebudou přijaty v jejich fyzickém skladu. Proto můžete převzít finanční vlastnictví zboží fakturací nákupní objednávky.
- **Účet hlavní knihy přepravovaného zboží** – Modul Náklady za doručení přidá do profilu zaúčtování nákupní objednávky konkrétní účet zaúčtování hlavní knihy za účelem zpracování zboží při tranzitním zpracování. Tento účet hlavní knihy přepravovaného zboží funguje jako účet typu „přijaté zboží, které nebylo dosud fakturováno“. Když je fakturována původní nákupní objednávka a je vytvořena objednávka přepravovaného zboží, přímé náklady na nákupní objednávku se zaúčtují na účet hlavní knihy přepravovaného zboží, dokud nebude zboží přijato na konečném fyzickém místě.
- **Aktualizace řízení sledování** – Objednávky přepravovaného zboží podporují funkci řízení sledování v Nákladech za doručení. Řízení sledování vám umožňuje aktualizovat očekávané datum příjezdu zboží během jeho přepravy. Řízení sledování poté aktualizuje cestu a související řádky nákupní objednávky. Očekávané datum dodání je pak k dispozici pro hlavní plánování a logistiku.
- **Spouštění nadměrných a nedostatečných transakcí** – Pokud dojde k odchylce mezi řádkem očekávaného zboží na cestě a skutečným zbožím, které je přijato do skladu, Náklady za doručení to vyřeší vytvořením nadměrné anebo nedostatečné transakce. Tyto transakce pak můžete spravovat na základě způsobu, jakým je chcete zpracovat, a to prostřednictvím nákupní objednávky nebo deníku pohybu. Nadměrné a nedostatečné transakce poskytují odkaz zpět na cestu, původní nákupní objednávku a nový deník pohybu nebo nákupní objednávku pro odchylku.
- **Objednávky přepravovaného zboží** – Modul Náklady za doručení zavádí nový zdrojový doklad, který je známý jako *objednávka přepravovaného zboží*. Objednávky přepravovaného zboží umožňuje fakturovat původní nákupní objednávku a převzít finanční vlastnictví položek. Když je nákupní objednávka fakturována, vytvoří se nový zdrojový dokument pro každý řádek nákupní objednávky, který má kombinaci dimenzí zásob. Zboží je poté fyzicky přesunuto do skladu přepravovaného zboží, kde je fyzicky vyhrazeno proti objednávce přepravovaného zboží a nelze jej spotřebovat, dokud není objednávka přepravovaného zboží přijata.

## <a name="miscellaneous-charges-and-shipment-costs"></a>Různé poplatky a náklady na dopravu

Jedním z nejdůležitějších aspektů přepravy a správy zásilek u zboží je uznání režijních nákladů spojených se zásilkami. Tyto režijní náklady nejsou přímými náklady na zásoby, které jsou spojeny s nákupní objednávkou a zásilkou nebo cestou. Místo toho se jedná o dodatečné náklady, které jsou zavedeny povahou pohybu zboží od dodavatele do vaší organizace. Tyto náklady mohou zahrnovat náklady na přepravu, které jsou spojeny s přepravou zboží z jednoho fyzického místa do druhého, nebo náklady na clo spojené s dovozem zboží od zahraničního dodavatele.

Náklady za doručení zpracovávají tyto náklady vytvořením nového typu nákladové struktury, která je známá jako *automatické náklady*. TMS zpracovává tyto náklady pomocí funkce různých poplatků.

### <a name="tms-charge-and-cost-features"></a>Funkce poplatků a nákladů v TMS

TMS používá různé poplatky ke správě dodatečných nákladů na vytížení, která jsou přidělena příslušným řádkům zdrojového dokumentu. Tyto různé poplatky lze nastavit na úrovni řádku nákupní objednávky nebo záhlaví nákupní objednávky.

V TMS lze různé poplatky rozdělit podle hmotnosti, objemu nebo množství zásob. Poplatky lze rozdělit na poplatky za přepravu nebo příslušenství. Používání dalších metod rozdělování v TMS bude vyžadovat další změny v kódu aplikace.

### <a name="landed-cost-charge-and-cost-features"></a>Funkce poplatků a nákladů v modulu Náklady za doručení

Náklady za doručení poskytují sadu nákladových funkcí, které zpracovávají dodatečné náklady spojené s přepravou zboží. Tyto náklady jsou známé jako automatické náklady a jsou použity v době počáteční fakturace zásilky pomocí odhadované částky nákladů. Každý typ nákladů je spravován ve svém vlastním účtování. Po zaúčtování skutečných faktur za režijní náklady se odhadované náklady automaticky aktualizují, aby odrážely skutečné náklady.

Kromě toho mohou být režijní náklady spojené s přepravou zboží fakturovány během cesty z přístavu původu nebo kdykoli po přijetí zboží. Tato schopnost poskytuje větší flexibilitu ve spotřebě zboží.

Následující seznam uvádí některé koncepty funkcí poplatků a nákladů v modulu Náklady za doručení:

- **Nákladová oblast** – Náklady a poplatky lze přiřadit k různým úrovním neboli *nákladovým oblastem* na cestě. Náklad může být použit na úrovni cesty a rozdělena na každou položku na cestě. Náklady lze dále uplatnit na úrovni kontejneru, nákupní objednávky, položky nebo převodního příkazu. Každý nákladový poplatek lze spravovat samostatně v různých oblastech a rozdělit na náklady za položku.
- **Metody rozdělení** – V modulu Náklady za doručení je k dispozici několik způsobů rozdělení. Nákladové poplatky lze rozdělit podle množství, částky v dolarech, hodnoty, hmotnosti, objemu, měrného systému nebo uživatelem definovaného objemového měřítka.
- **Řízení účtování/odchylky** – Poplatky za náklady jsou v modulu Náklady za doručení nastaveny jako vlastní typ nákladového kódu. Každý typ kódu nákladů umožňuje definovat clearingový účet pro poplatky za odhadované náklady a také účty časového rozlišení a odchylky kupní ceny pro odchylky v odhadovaných nákladech oproti skutečným nákladům. Když se odhadované náklady zpočátku účtují, připíše se kredit na clearingový účet. Po zaúčtování skutečných faktur se zaúčtují poplatky za skutečné náklady a odhadované náklady se odečtou z clearingového účtu.

## <a name="matching-freight-bills-and-invoices"></a>Spárování nákladních listů a faktur

### <a name="tms-bill-and-invoice-matching-features"></a>Funkce párování nákladních listů a faktur v TMS

TMS může spárovat nákladní listy obsahující odhadované náklady a faktury se skutečnými náklady na přepravné. Faktury lze přijímat elektronicky nebo papírově. Spárování odchylek mezi odhadovanými a skutečnými náklady nemá vliv na ocenění zásob.

Další informace najdete v tématu [Odsouhlasení nákladu ve správě přepravy](../transportation/reconcile-freight-transportation-management.md).

### <a name="landed-cost-bill-and-invoice-matching-features"></a>Funkce párování nákladních listů a faktur v Nákladech za doručení

Náklady za doručení mohou spárovat nákladní listy a poplatky za odhadované náklady a mohou fakturovat poplatky za skutečné náklady na odhadované náklady. V době fakturace jsou poplatky za přepravu v deníku faktur a odhadované náklady jsou vymazány z clearingového účtu. Poplatky za skutečné náklady se navíc zaúčtují proti nákladům na zboží prodané za položku spolu s rozdíly mezi odhadovanými a skutečnými poplatky. Toto chování umožňuje flexibilitu v procesu fakturace.

## <a name="tracking"></a>Sledování

Důležitým rysem modulů TMS i Náklady za doručení je schopnost sledovat zboží a identifikovat, kde se na cestě z místa původu do konečného cílového skladu nachází. Sledování umožňuje sledovat a aktualizovat pohyb zboží a rozpoznat, kdy dorazí do skladu ke spotřebě. Kromě stavu zboží během jeho cesty poskytují Náklady za doručení očekávané a skutečné datum pro každý krok cesty.

### <a name="tms-tracking-features"></a>Funkce sledování v TMS

TMS poskytuje omezené funkce pro sledování příchozích vytížení. Zobrazuje datumy a umožňuje vytvoření integrace k nalezení přesné polohy (například na stránce **Stav přepravy**).

Pro každý segment trasy můžete zadat odhadované plány a časy příjezdu.

### <a name="landed-cost-tracking-features"></a>Funkce sledování v Nákladech za doručení

Náklady za doručení mohou poskytnout řízení sledování pro každou cestu, od přístavu původu až po konečné místo určení. Řízení sledování nastavuje stav cesty. Stav označuje, zda probíhá plavba,celní odbavení na celnici, nebo místní dodání do konečného skladu. Stav lze nastavit na úrovni řádku nákupní objednávky, kontejneru a záhlaví cesty. Máte tedy podrobnější kontrolu nad celým procesem.

S každým krokem cesty je navíc spojeno potvrzené očekávané datum, které je založeno na zadaných dobách realizace. Potvrzené a očekávané termíny dodání se přidají k řádku nákupní objednávky a objednávky přepravovaného zboží, a lze je použít pro hlavní plánování a logistiku. Kromě očekávaných datumů lze aktualizovat i skutečné datumy. Následné kroky na cestě budou poté odpovídajícím způsobem aktualizovány.

## <a name="multi-leg-journeys"></a>Cesty s více úseky

Koncept cesty identifikuje, kde se zboží v procesu nachází, a řídí stav zboží během jeho přepravy. Zboží může projít několika úseky cesty a ke konkrétnímu úseku můžete přiřadit různé náklady. Jako příklady lze uvést náklady na dopravu při plavbě na lodi a náklady na místní dopravu při přepravě zboží z přístavu do místa určení.

### <a name="tms-multi-leg-journey-features"></a>Funkce cesty s více úseky v TMS

V TMS mohou být trasy rozděleny na segmenty trasy, které představují cesty s několika úseky. TMS může přidělit místní sazby a poplatky za příslušenství k jednotlivým segmentům trasy.

Další informace najdete v tématu [Plánování tras nákladní dopravy s více zastávkami](../transportation/plan-freight-transportation-routes-multiple-stops.md).

### <a name="landed-cost-multi-leg-journey-features"></a>Funkce cesty s několika úseky v Nákladech za doručení

Náklady za doručení poskytují prostředí pro přesun zboží z místa původu do cíle prostřednictvím řady úseků, kterými jsou zastávky nebo kroky na cestě. Úseky jsou kombinovány a vytvářejí šablony cest, které definují, jak se zboží přesouvá od dodavatele k vaší organizaci.

V každém úseku cesty můžete dále definovat stav každého řádku nákupní objednávky a doby realizace, které jsou s ním spojeny. Kombinovaná doba realizace pro všechny úseky se používá k identifikaci odhadovaného data dodání. Pro použití cesty s několika úseky je však nutné zpracování přepravovaného zboží. Cesta zboží na cestě je spravována v tabulce, která je specifická pro modul Náklady za doručení.

## <a name="receiving-by-container"></a>Příjem podle kontejneru

Řízení způsobu, jakým je zboží rozdělováno a skladováno na lodi, může být velmi důležité. Na lodi může být zboží uloženo v jednom kontejneru nebo více kontejnerech. Když je zboží přijato, je přijato v kontejnerech, a různé kontejnery na cestě mohou být přijaty v různých časech nebo v různých datech.

TMS i Náklady za doručení poskytují funkce pro správu příjmu zboží v kontejneru. TMS používá koncept vytížení ke správě zboží, nákupních objednávek a převodních příkazů, které jsou přidruženy k přepravnímu kontejneru. TMS podporuje příjem na základě struktury balení, které je přijímáno prostřednictvím avíza expedice zboží (ASN). Náklady za doručení využívají koncept přepravních kontejnerů ke zpracování nákupních objednávek a řízení režijních nákladů, které jsou spojeny s kontejnerem na plavidle.

### <a name="tms-receiving-by-container-features"></a>Funkce příjmu podle kontejneru v TMS

TMS podporuje příchozí avíza expedice zboží, všechny varianty příjmu prostřednictvím mobilní aplikace Řízení skladu a všechny metody příjmu prostřednictvím klienta Supply Chain Management.

### <a name="landed-cost-receiving-by-container-features"></a>Funkce příjmu podle kontejneru v Nákladech za doručení

Aby podporovaly příjem podle kontejneru, vytvoří Náklady za doručení záznamy o přepravním kontejneru a přidruží nákupní objednávky ke konkrétnímu přepravnímu kontejneru pomocí jeho ID kontejneru. Poté lze na tento přepravní kontejner použít režijní náklady a rozdělit je tak, aby byly spojeny s příslušnými nákupními objednávkami.

Kontejnery v Nákladech za doručení lze přijímat prostřednictvím nového typu příjmu, který se nazývá *příjem přepravovaného zboží*, prostřednictvím deníků příjezdu nebo prostřednictvím příjmu z mobilního zařízení. Pokud jsou použity deníky příjezdu, množství lze inicializovat z objednávky přepravovaného zboží nebo z řádků původní nákupní objednávky v kontejneru. Náklady za doručení poskytují dva pracovní typy pro příjem prostřednictvím mobilní aplikace Řízení skladu.

Náklady za doručení neposkytují ASN pro elektronický příjem zboží. Kromě toho nepodporují toky mobilní aplikaci Řízení skladu, které zpracovávají příjem zatížení, příjem registrační značky nebo příjem smíšené registrační značky.

## <a name="rate-shopping-by-vendor"></a>Návrh přepravních sazeb podle dodavatele

Návrh přepravních sazeb umožňuje společnosti vybrat dodavatele dopravy na základě nejnižší ceny, nejrychlejší trasy nebo kombinace obou faktorů.

### <a name="tms-rate-shopping-features"></a>Funkce návrhu přepravních sazeb v TMS

TMS umožňuje identifikovat dodavatele a směrovací řešení pro příchozí a odchozí objednávky. Můžete například určit nejrychlejší trasu nebo nejlevnější sazbu pro dodávku.

TMS poskytuje úplný návrh přepravních sazeb a optimalizaci přepravy prostřednictvím pracovní plochy pro návrh trasy, flexibilních možností hodnocení prostřednictvím hodnotícího modulu, rozhraní API hodnotícího modulu pro integraci s externími stranami, a podporu objemové hmotnosti.

Další informace najdete v tématu [Moduly správy přepravy](../transportation/transportation-management-engines.md).

### <a name="landed-cost-rate-shopping-features"></a>Funkce návrhu přepravních sazeb v Nákladech za doručení

Náklady za doručení poskytují pouze omezenou podporu pro návrh přepravních sazeb podle dodavatele. I když můžete zadat hodnoty spedice, Náklady za doručení je neporovnává mezi více dodavateli.

## <a name="driver-check-incheck-out-with-appointment-scheduling"></a>Přihlášení / odhlášení řidiče s plánováním schůzek

Funkce přihlášení / odhlášení řidiče umožňuje systému sledovat příjezdy a zabránit zahlcení na nakládacích docích.

### <a name="tms-driver-check-incheck-out-features"></a>Funkce přihlášení / odhlášení řidiče v TMS

TMS umožňuje vytvářet *schůzky*. Schůzka představuje události, ke kterým dochází v doku u příjmu nákupní objednávky, odeslání prodejní objednávky nebo zpracování příchozího či odchozího vytížení ke konkrétnímu datu a času. Schůzky zajišťují, že jsou k dispozici doky pro nakládku a vykládku zboží, a pomáhají předcházet situacím, kdy na místo dorazí více dopravců najednou.

Systém umožňuje řidičům přihlásit se ke konkrétním dveřím doku.

### <a name="landed-cost-driver-check-incheck-out-features"></a>Funkce přihlášení / odhlášení řidiče v Nákladech za doručení

Náklady za doručení mohou ukládat odhady data a času, kdy bude kontejner doručen.

## <a name="transfer-orders-and-additional-costs"></a>Převodní příkazy a dodatečné náklady

Podniky často musí být schopny převádět zboží mezi sklady. Když k tomuto typu převodu dojde, jsou s ním spojeny náklady a možná budete chtít tyto náklady identifikovat. V modulu Náklady za doručení lze přidat převodní příkazy k cestě nebo plavidlu, aby bylo možné sledovat pohyb zboží z jednoho skladu nebo místa do druhého, odhadnout čas dodání a očekávané datum dodání a přidat režijní náklady k převodu zboží.

### <a name="tms-transfer-order-cost-features"></a>Funkce nákladů převodního příkazu v TMS

TMS podporuje vytváření poplatků za přepravu, které jsou spojeny s převody. Ačkoli tyto poplatky lze zobrazit z převodního příkazu, náklady za doručení se nepřičtou k ceně položky. Odsouhlasení nákladů je podporováno vytvořením nákladního listu, který je založen na těchto poplatcích. Tento nákladní list je poté spárován s fakturou za přepravu dodavatele.

### <a name="landed-cost-transfer-order-cost-features"></a>Funkce nákladů převodního příkazu v Nákladech za doručení

Náklady za doručení umožní přidat převodní příkazy k cestě nebo plavidlu. Tímto způsobem můžete přidat náklady na dopravu k cestě jako vyrovnání zásob v době přijetí převodního příkazu. Režijní náklady mohou být fakturovány za skutečné náklady a sledovány během cesty za účelem aktualizace nákladů na prodané zboží. Přestože převodní příkazy nepoužívají zpracování přepravovaného zboží ve standardním vydání, lze je přidat k cestě. Náklady za doručení se přičtou k celkové ceně každé položky.
