---
title: Vyhledávání produktu a zákazníka v pokladním místě (POS)
description: Toto téma poskytuje přehled vylepšení, která byla provedena v aplikaci Dynamics 365 Commerce ohledně funkce vyhledávání produktu a vyhledávání zákazníka.
author: ShalabhjainMSFT
ms.date: 05/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 460c7d3b00421ba43414f7343887edf9b8adad9c
ms.sourcegitcommit: 9dd2d32fc303023a509d58ec7b5935f89d1e9c6d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/26/2022
ms.locfileid: "8806420"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Vyhledávání produktu a zákazníka v pokladním místě (POS)

[!include [banner](includes/banner.md)]

Moderní pokladní místo (MPOS) a cloudové pokladní místo (CPOS) poskytují snadno použitelnou funkci vyhledávání produktů a zákazníků. Panel vyhledávání je vždy k dispozici v horní části oken MPOS a CPOS, aby zaměstnanci mohli rychle vyhledat produkty a zákazníky.

Zaměstnanci mohou vyhledávat produkty v katalozích, které souvisejí s aktuálním obchodem. Mohou také vyhledávat produkty v katalozích, které souvisejí s jiným obchodem ve společnosti. Proto pokladníci mohou prodávat a vracet produkty mimo sortiment obchodu. Stejně tak mohou zaměstnanci vyhledávat zákazníky, kteří jsou ve společnosti spojeni s běžným obchodem nebo jiným obchodem. Kromě toho mohou zaměstnanci vyhledávat zákazníky, kteří jsou spojeni s jinou společností v nadřazené organizaci.

## <a name="product-search"></a>Hledání produktu

Ve výchozím nastavení se vyhledávání produktů provádí v sortimentu obchodu. Tento typ vyhledávání se nazývá *vyhledávání místních produktů*. Zaměstnanci však mohou snadno přepnout do libovolného katalogu, který je přidružen k aktuálnímu obchodu, nebo mohou vyhledávat v jiném obchodě. Tento typ vyhledávání se nazývá *vyhledávání vzdálených produktů*. Chcete-li změnit katalog, zvolte tlačítko **Kategorie** v levé části stránky. V horní části zobrazeného podokna vyberte tlačítko **Změnit katalog** a vyberte jeden z dostupných katalogů pro jeho prohlížení. Systém bude prohledávat vybraný katalog produktů.

Na stránce **Změnit katalog** mohou zaměstnanci snadno vybrat libovolný obchod, nebo mohou vyhledávat produkty ve všech obchodech.

![Změna katalogu.](./media/Changecatalog.png "Změna katalogu")

Vyhledávání místních produktů vyhledává v rámci následujících vlastností produktu:

- Číslo produktu
- Název produktu
- popis
- Dimenze
- Čárový kód
- Vyhledat název

### <a name="additional-local-product-search-capabilities-conventional-sql-full-text-search"></a>Další možnosti místního vyhledávání produktů (běžné fulltextové vyhledávání SQL) 

- U vyhledávání s více klíčovými slovy (to znamená u vyhledávání, které používají hledané termíny) mohou prodejci nakonfigurovat, zda výsledky vyhledávání mají obsahovat výsledky, které odpovídají *libovolnému* hledanému termínu, nebo pouze výsledky, které odpovídají *všem* hledaným termínům. Nastavení této funkce je k dispozici v profilu funkce POS pod novou skupinou s názvem **Vyhledávání produktu**. Ve výchozím nastavení je **Spárovat jakékoli hledané termíny**. Toto nastavení je rovněž doporučené nastavení. Pokud je použito nastavení **Spárovat jakýkoli zadaný termín**, jsou vráceny všechny produkty, které plně nebo částečně odpovídají jednomu nebo více hledaným termínům. Výsledky se automaticky seřadí vzestupně podle produktů, které mají nejvíce shod klíčových slov (úplných nebo částečných).

    Nastavení **Spárovat všechny hledané termíny** vrátí pouze produkty odpovídající všem hledaným termínům (úplné nebo částečné). Toto nastavení je užitečné, když jsou názvy produktu dlouhé a zaměstnanci potřebují zobrazit pouze omezené produkty ve výsledcích vyhledávání. Tento typ vyhledávání však má dvě omezení:

    - Hledání se provádí na základě jednotlivých vlastností produktu. Jsou například vráceny pouze produkty, které mají všechna vyhledaná klíčová slova v alespoň jedné vlastnosti produktu.
    - Neprohledávají se dimenze.
> [!NOTE]
> Následující konfigurace **Spárovat jakýkoli zadaný termín**/**Spárovat všechny zadané termíny** ve funkčních profilech POS jsou použitelné pouze pro **místní** prostředí vyhledávání produktů (konvenční fulltextové vyhledávání SQL). Tato konfigurace nemá žádný vliv na cloudové vyhledávání. Nový vyhledávač má svůj vlastní pokročilý algoritmus, který zvyšuje relevanci vyhledávání pro výsledky vyhledávání produktů. 

- Maloobchodníci mohou nakonfigurovat vyhledávání produktů pro zobrazení návrhů vyhledávání, když uživatelé zadávají názvy produktů. Nové nastavení této funkce je k dispozici v profilu funkce POS pod skupinu s názvem **Vyhledávání produktu**. Toto nastavení se nazývá **Zobrazit návrhy vyhledávání při zadávání**. Tato funkce pomůže zaměstnancům rychle najít produkt, který hledají, protože nemusí ručně zadávat celé jméno.
- Algoritmus vyhledávání produktu nyní hledá vyhledávané termíny ve vlastnosti produktu **Vyhledávání jména**.

![Návrhy produktů.](./media/Productsuggestions.png "Návrhy produktů")

## <a name="customer-search"></a>Hledat zákazníka

Vyhledávání zákazníka slouží k vyhledání zákazníků pro různé účely. Pokladníci například mohou chtít zobrazit seznam přání zákazníka nebo historii nákupů, nebo přidat zákazníka do transakce. Vyhledávací algoritmus spáruje hledané termíny oproti hodnotám uvedeným v následujících vlastnostech odběratele:

- Název
- E-mailová adresa
- Telefonní číslo
- Číslo věrnostní karty
- Adresa
- Číslo účtu

V rámci těchto vlastností poskytuje název nejvyšší flexibilitu pro vyhledávání s více klíčovými slovy, protože algoritmus vrací všechny odběratele, kteří odpovídají jakémukoliv z hledaných klíčových slov. V horní části výsledků se objevují zákazníci, kteří odpovídají většině klíčových slov. Toto chování pomáhá pokladníkům v situacích, kdy hledají zadáním celého jména, ale příjmení a křestní jméno byly při původním zadání zaměněna. Z důvodu výkonu však všechny ostatní vlastnosti zachovávají pořadí klíčových slov pro vyhledávání. Pokud se tedy pořadí klíčových slov pro vyhledávání neshoduje s pořadím, ve kterém jsou data uložena, nebudou vráceny žádné výsledky.

Ve výchozím nastavení se vyhledávání zákazníků provádí na adresářích zákazníků, které jsou přiřazeny k obchodu. Tento typ vyhledávání se nazývá *vyhledávání místních zákazníků*. Zaměstnanci však mohou také vyhledávat zákazníky globálně. Jinými slovy, mohou vyhledávat ve všech obchodech společnosti a ve všech ostatních právnických osobách. Tento typ vyhledávání se nazývá *vyhledávání vzdálených zákazníků*.

Pokud chtějí vyhledávat globálně, mohou zaměstnanci vybrat tlačítko **Filtrovat výsledky** v dolní části stránky a potom vybrat možnost **Prohledat všechny obchody**, jak je znázorněno na následujícím obrázku. V takovém případě nejsou vráceni jen zákazníci. Všechny typy stran, které jsou součástí jakéhokoli adresáře v ústředí jsou vráceny též. Tyto strany zahrnují pracovníky, dodavatele, kontakty a konkurenty.

> [!NOTE]
> Aby bylo možné získat výsledky vyhledávání pro vzdáleného zákazníka, je třeba zadat minimálně čtyři znaky.

ID zákazníka se nezobrazuje pro zákazníky dotazované z jiných právnických osob, protože pro tyto strany v současné společnosti nebylo vytvořeno žádné ID zákazníka. Pokud však zaměstnanec otevře stránku s podrobnostmi o zákazníkovi, systém automaticky vygeneruje ID zákazníka pro danou stranu a zároveň propojí adresáře zákazníka obchodu se zákazníkem. Proto bude zákazník viditelný v prohledáváních místního obchodu, která budou provedena později.

![Globální vyhledávání zákazníků.](./media/Globalcustomersearch.png "Globální vyhledávání zákazníků")

### <a name="additional-local-customer-search-capabilities"></a>Další možnosti vyhledávání místních zákazníků

Když uživatel vyhledá telefonní číslo, systém ignoruje speciální znaky (například mezery, pomlčky nebo hranaté závorky), které mohly být přidané při vytvoření odběratele. Pokladníci si tak nemusí dělat starosti s formátem telefonního čísla při hledání. Pokud telefonní číslo zákazníka byl zadáno například jako **123-456-7890**, pokladník můžete hledat zákazníka zadáním **1234567890**, nebo zadáním několika počátečních čísel telefonního čísla.

> [!NOTE]
> Zákazník může mít více telefonních čísel a více e-mailů. Algoritmus vyhledávání zákazníků také prochází těmito sekundárními e-maily a telefonními čísly, ale stránka s výsledky vyhledávání zákazníků zobrazuje pouze primární e-mail a telefonní číslo. To může způsobit určitý zmatek, protože vrácené výsledky zákazníka nezobrazí hledaný e-mail nebo telefonní číslo. V příštím vydání plánujeme vylepšit obrazovku výsledků vyhledávání zákazníků tak, aby se tyto informace zobrazovaly.

Tradiční vyhledávání zákazníků může být časově náročné, protože vyhledává mezi více poli. Místo toho mohou pokladníci hledat v jedné vlastnosti zákazníka, jako je jméno, e-mailová adresa nebo telefonní číslo. Vlastnosti, které používá algoritmus hledání odběratele, jsou souhrnně označovány jako *kritéria hledání odběratele*. Správce systému může snadno konfigurovat jedno nebo více kritérií jako zástupce, který se zobrazí v POS. Vzhledem k tomu, že je hledání omezeno na jediné kritérium, jsou zobrazeny pouze relevantní výsledky hledání a výkon je mnohem lepší než výkon standardního hledání odběratele. Následující obrázek znázorňuje zkratky hledání odběratele v POS.

![Klávesové zkratky vyhledávání zákazníků.](./media/SearchShortcutsPOS.png "Klávesové zkratky vyhledávání zákazníků")

Aby bylo možné nastavit kritérium hledání jako zástupce, musí správce otevřít stránku **Parametry Commerce** v aplikaci Commerce a poté na kartě **Kritéria vyhledávání POS** vybrat všechna kritéria, která se mají zobrazit jako zástupci.

![Konfigurovat klávesové zkratky vyhledávání.](./media/ConfigureShortcutsAX.png "Konfigurovat zástupce vyhledávání")

> [!NOTE]
> Pokud přidáte příliš mnoho zástupců, rozevírací nabídka panelu vyhledávání v POS se přehltí a může to ovlivnit vyhledávání zaměstnance. Doporučujeme přidávat pouze tolik zástupců, kolik potřebujete.

Pole **Pořadí zobrazení** určuje pořadí, ve kterém jsou zobrazeny zkratky v POS. Kritéria, která jsou zobrazena ve vlastnostech ihned po vybalení, které používá algoritmus hledání odběratele pro hledání odběratele. Partneři však mohou přidat vlastní vlastnosti jako zástupce hledání. Pokud chcete přidat vlastní vlastnosti jako zkratky hledání, musí správce systému rozšířit rozšiřitelné vyčíslení (enum), které se používá pro kritéria vyhledávání odběratele, a následně označit vlastní vlastnosti partnera jako zástupce. Partneři zodpovídají za zápis kódu k vyhledání výsledků, když se používají k hledání jejich vlastní zástupci.

Překlady pro zkratky jsou vyžadovány, pokud chcete, aby se na POS zobrazovaly zkratky. Pokud se jazyk vašeho kanálu liší od výchozího jazyka systému, musíte definovat překlad pro každou zkratku v očekávaném jazyce. Překlady můžete definovat výběrem příkazu **Přeložit** pro každou zkratku. 

> [!NOTE]
> Vlastní vlastnost, která je přidána do výčtu, neovlivní standardní algoritmus hledání odběratele. Jinými slovy, algoritmus hledání zákazníků nevyhledává ve vlastní vlastnosti. Uživatelé mohou vlastní vlastnosti použít k vyhledávání pouze v případě, že je vlastní vlastnost přidána jako zástupce, případně je přepsán výchozí algoritmus hledání.

Maloobchodníci mohou také nastavit výchozí režim vyhledávání zákazníků v POS na **Prohledat všechny obchody**. Tato konfigurace může být užitečná ve scénářích, ve kterých je nutné, aby zákazníci, kteří byli vytvořeni mimo POS, byli vyhledání okamžitě (například před spuštěním úlohy distribuce). Za tímto účelem musí maloobchodník zapnout možnost **Výchozí režim vyhledávání zákazníků** v profilu funkčnosti POS. Po nastavení na **Ano**, Každý pokus o hledání odběratele poté provede volání do centrály v reálném čase.

Aby se zabránilo neočekávaným problémům s výkonem, je tato konfigurace skryta za testovacím příznakem s názvem **CUSTOMERSEARCH_ENABLE_DEFAULTSEARCH_FLIGHTING**. Chcete-li tedy zobrazit možnost **Výchozí režim vyhledávání odběratelů** nastavující uživatelské rozhraní (UI), měl by maloobchodní prodejce vytvořit lístek podpory pro akceptační testování uživatele a výrobní prostředí. Po obdržení lístku bude tým inženýrů spolupracovat s maloobchodním prodejcem, aby se ujistil, že prodejce provádí testování v nevýrobním prostředí, aby zhodnotil výkonnost a implementoval požadované optimalizace.

## <a name="cloud-powered-customer-search"></a>Vyhledávání zákazníka využívající cloud

Veřejný náhled možnosti vyhledávání zákazníků pomocí služby Azure Cognitive Search byl vydán jako součást vydání Commerce 10.0.18. Kromě vylepšení výkonu mají uživatelé služby také prospěch z bohatého zdokonalení a vylepšených funkcí relevance. Vylepšení výkonu jsou obzvláště evidentní, když se použije funkce globálního vyhledávání („Prohledat všechny obchody“) POS. Důvodem je, že výsledky vyhledávání jsou načteny z indexu vyhledávání Azure namísto dotazu z dat v centrále Commerce. 

### <a name="enable-the-cloud-powered-search-feature"></a>Povolit cloudovou funkci vyhledávání

> [!NOTE]
> Je vyžadováno, aby jak centrála Commerce, tak jednotka Commerce Scale Unit byly aktualizovány na verzi 10.0.18. Aktualizace POS není nutná.

Chcete-li aktivovat funkci vyhledávání využívajícího cloud v centrále Commerce, postupujte takto.

1. Přejděte do nabídky **Správa systému \> Pracovní prostory \> Správa funkcí**.
1. Najděte a vyberte funkci **(Preview) Cloudové vyhledávání zákazníků** a poté vyberte **Povolit**.
1. Přejděte na **Retail a Commerce > Nastavení centrály > Plánovač Commerce > Inicializovat plánovač Commerce** a vyberte **OK** pro zobrazení nové úlohy **1010_CustomerSearch** na formuláři **Harmonogram distribuce**.
1. Přejděte na **Retail a Commerce > IT pro Retail a Commerce > Plán distribuce**.
1. Spusťte úlohu **1010_CustomerSearch**. Tato úloha publikuje datum do indexu vyhledávání Azure. Po dokončení publikování indexu bude stav úlohy nastaven na **Použito**.
1. Po nastavení stavu úlohy **1010_CustomerSearch** na **Použito** spusťte úlohu **1110 – Globální konfigurace** k aktualizaci kanálů POS nově aktivované funkce ve **Správě funkcí**.
1. Následně spouštějte úlohu **1010_CustomerSearch** v pravidelných intervalech a zasílejte aktualizace zákazníků do indexu vyhledávání.

> [!NOTE]
> U počátečního zveřejnění indexu může úloha **1010_CustomerSearch** trvat několik hodin, protože odešle všechny záznamy zákazníků do indexu vyhledávání Azure. Následné aktualizace by měly trvat několik minut. V časovém období, kdy je povolena funkce vyhledávání na cloudu, ale publikování indexu ještě není dokončeno, bude vyhledávání zákazníků z POS mít výchozí hodnotu existujícího vyhledávání založeného na SQL. Tím je zajištěno, že operace ukládání nebudou přerušeny.

### <a name="functional-differences-from-the-existing-search"></a>Funkční rozdíly od stávajícího vyhledávání

Následující seznam ukazuje, jak se funkce cloudového vyhledávání zákazníků liší od stávající funkce vyhledávání. 

- Zákazníci vytvoření a upravení v centrále Commerce jsou odesíláni do indexu vyhledávání Azure, když je spuštěna úloha **1010_CustomerSearch**. Aktualizace indexu těmto aktualizacím trvá minimálně 15 až 20 minut. Uživatelé POS budou moci hledat nové zákazníky (nebo hledat na základě aktualizovaných informací) asi 15 až 20 minut po aktualizaci v centrále Commerce. Pokud váš obchodní proces vyžaduje, aby zákazníci vytvoření v centrále Commerce mohli být okamžitě vyhledatelní v POS, nemusí to být pro vás ta správná služba.
- Noví zákazníci vytvoření v POS se odesílají do indexu Azure Search z Commerce Scale Unit a lze je okamžitě prohledávat v jakémkoli obchodě. Pokud je však funkce vytváření zákazníků Async zapnutá, nové záznamy o zákaznících nebudou publikovány do indexu Azure Search z Commerce Scale Unit a nebude možné je prohledávat z POS, dokud nebudou synchronizovány informace o zákazníkovi s centrálou Commerce a nebudou vygenerována ID zákazníka pro zákazníky Async. Úloha **1010_CustomerSearch** pak bude moci odeslat záznamy asynchronních zákazníků do indexu vyhledávání Azure. V průměru to bude asi 30 minut, než bude možné nově vytvořené zákazníky Async hledat na POS. Tento odhad předpokládá, že úlohy **1010_CustomerSearch**, **P-úloha** a **Synchronizovat zákazníky a obchodní partnery z asynchronního režimu** jsou naplánovány na spuštění každých 15 minut.
- Cloudové vyhledávání také vyhledává sekundární e-maily a telefonní čísla zákazníků, ale v současné době se ve výsledcích vyhledávání zákazníků zobrazuje pouze primární telefonní číslo a primární e-mailová adresa zákazníků. Na první pohled se může zdát, že byly vráceny irelevantní výsledky vyhledávání, ale kontrola sekundárního e-mailu a telefonního čísla zákazníka ve výsledcích vyhledávání vám může pomoci ověřit, zda hledané klíčové slovo vedlo ke shodě zákazníků. Aby se předešlo takovým nejasnostem, existují plány na vylepšení stránky s výsledky vyhledávání, aby uživatelé snadno pochopili, proč byl výsledek vyhledávání vrácen.
- Požadavek vyhledávání pomocí alespoň 4 znaků v globálním vyhledávání („Hledat ve všech obchodech“) se na tuto službu nevztahuje.

> [!NOTE]
> Funkce vyhledávání zákazníků pomocí služby Azure Cognitive Search je k dispozici v omezených oblastech jako náhled. Možnost vyhledávání zákazníků *není* k dispozici v následujících oblastech:
> - Brazílie
> - Indie

[!INCLUDE[footer-include](../includes/footer-banner.md)]
