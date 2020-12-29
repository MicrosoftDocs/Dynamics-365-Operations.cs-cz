---
title: Kalendáře a hlavní plánování
description: Toto téma obsahuje přehled kalendáře dodavatelsko-odběratelského řetězce dodávek a jejich vliv na hlavní plánování.
author: t-benebo
manager: tfehr
ms.date: 08/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2c32957b0bd234ed14e6333a36a46c6a83ec2e91
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423836"
---
# <a name="calendars-and-master-planning"></a>Kalendáře a hlavní plánování

[!include [banner](../includes/banner.md)]

Toto téma obsahuje přehled kalendáře dodavatelsko-odběratelského řetězce dodávek a jejich vliv na hlavní plánování.  Jsou popsány různé kalendáře použité v modulu hlavní plánování, včetně jejich vlivu data expedice a příjmu v plánované objednávce. Nakonec jsou uvedena doporučení týkající se přiřazení, použití a aktualizace kalendářů.

## <a name="definition-of-a-calendar"></a>Definice kalendáře

Kalendář, který bude vaše organizace používat, můžete definovat na stránce v okně **Správa organizace > Nastavení > Kalendáře > Kalendáře**. 

Každá položka data v kalendáři může být **otevřená** nebo **uzavřená** nebo **základní kalendář**. Tato hodnota je určena ve sloupci **Řízení** na stránce **Pracovní doby**. Pro každé datum platí: 
- **Otevřená** -znamená, že je provedena práce pro vybraný den. Kalendář se bude aktualizovat podle šablony pracovní doby.
- **Zavřená** -znamená, že práce není provedena během dne. 
- **Základní kalendář** – označuje, že konkrétní datum zdědí pracovní doby a hodnotu otevřená nebo zavřená ze základního kalendáře. Proto po aktualizaci základního kalendáře zdědí vybraný kalendář časy operací z tohoto kalendáře. 

Pro všechna uzavřená data bude automaticky přiděleno zaškrtávací políčko **Uzavřeno pro vyzvednutí**. Pro otevřená data můžete ručně vybrat možnost **Zavřeno pro vyzvednutí**. Ta označuje, že se práce provádí k danému datu, ale expedice nebude provedena. 

## <a name="calendars-that-affect-master-planning"></a>Kalendáře, které ovlivňují hlavní plánování

### <a name="calendar-for-a-coverage-group"></a>Kalendář pro skupinu disponibility
Skupina disponibility označuje běžnou sadu parametrů používanou pro doplnění položek, které náleží k dané skupině disponibility. 

Chcete-li přidat kalendář pro skupinu disponibility, přejděte na **Hlavní plánování > Nastavení > Disponibilita > Skupiny disponibility**  a vytvořte tak skupinu disponibility. Najděte skupinu disponibility, ke které chcete přiřadit kalendář, a vyberte ji v poli **Kalendář**.

Skupinu disponibility lze přiřadit na jiný stránkách: 
    - Na stránce **Podrobnosti uvolněného produktu** položky. Pokud chcete zobrazit skupinu disponibility položky, přejděte na **Správa informací o produktu > Produkty > Uvolněné produkty** a vyberte položku, která bude převedena na stránku **Podrobnosti o uvolněném produkut**. Skupinu disponibility položky můžete zobrazit na pevné záložce **Plán**.
    - Na stránce **Disponibilita položky**. Na stránce podrobností uvolněné položky kliknutím na **Disponibilita položky** přejděte na stránku disponibility položky. Na kartě Přehled se zobrazí různé parametry pro doplnění v závislosti na pracovišti, skladu a produktu. Skupina disponibility pro jednotlivé položky bude zděděna ze skupiny disponibility na stránce **podrobnosti o uvolněném produktu**. Lze ji přepsat pomocí možnosti **Použít specifické nastavení** nebo **Přepsat nastavení skupiny** na kartě **Obecné**.
    - Na stránce **Parametry hlavního plánování**. Pokud nemá položka skupinu disponibility nastavenou na předchozích stránkách, hlavní plánování vezme obecnou skupinu nastavenou v parametrech hlavního plánování. Toto nastavení se provádí v části **Hlavní plánování > Nastavení > Parametry hlavního plánování** v poli **Obecná skupina disponibility**. 

### <a name="calendar-for-a-vendor"></a>Kalendář pro dodavatele
Pokud chcete označit pracovní dny dodavatele, můžete dodavateli přiřadit nákupní kalendář na stránce **Výchozí hodnoty nákupní objednávky** pro dodavatele. 

Chcete-li nastavit kalendář pro dodavatele, je nutné vytvořit kalendář v části **Správa organizace > kalendáře > kalendáře**. Po vytvoření kalendáře je nutné ho přiřadit dodavateli. Přejděte na **Závazky dodavatelů > Dodavatelé > Všichni dodavatelé** a vyberte dodavatele, kterému chcete přiřadit kalendář. Pak na stránce dodavatele na pevné záložce **Výchozí hodnoty nákupní objednávky** přiřaďte nový nákupní kalendář pomocí rozevírací nabídky. 

Kalendář pro dodavatele označuje dny, kdy přijmou umístění nákupní objednávky, a data, kdy mohou objednávky doručovat do vaší společnosti. Následně budou data objednávky pro nákupní objednávky pro dodavatele s nákupním kalendářem data definovaná jako otevřená v kalendáři. Data dodání pro tyto objednávky budou také v otevřené dny budou mít tedy dopad na doby realizace zakoupené položky. 

#### <a name="define-the-lead-time-for-a-purchased-item"></a>Definování doby realizace pro zakoupenou položku

K určení doby realizace nákupu (pokud mají být zahrnuty pouze pracovní dny) pro určitou položku je nutné přejít na stránku výchozího nastavení objednávky produktu v části **řízení informací o produktech > produkty > uvolněné produkty** a Vyberte **výchozí nastavení objednávky**. 

> [!Note]
> Hodnota **Pracovních dnů** v době realizace nákupu označují pracovní dny dodavatele. Například kalendář pro dodávku pouze v úterý s dobou realizace 10 dní a dny zaškrtnutým políčkem pro pracovní dny označuje, že by trvalo deset týdnů (10 úterků), než by byla položka doručena.
Ve většině případů nedoporučujeme tedy vybrat pracovní dny pro dobu realizace nákupní objednávky.

#### <a name="define-lead-times-from-the-trade-agreements-page"></a>Definujte doby realizace ze stránky obchodních smluv

Hlavní plánování můžete nastavit tak, aby zahrnoval všechny obchodní smlouvy pro dodavatele. Obchodní smlouvy jsou dohody o pevných cenách nebo slevách, které jsou nastaveny pro jednoho nebo více zákazníků nebo dodavatelů pro prodej nebo nákup jednotlivých nebo více produktů. Přejděte na **Hlavní plánování >Nastavení > Parametry hlavního plánování** a na kartu **Plánované objednávky** a vyberte **Najít obchodní smlouvy** pro zahrnutí obchodní smlouvy při plánování. Hlavní plánování může vybrat dodavatele s **minimální dobou realizace** nebo **nejnižší jednotkovou cenou**.

### <a name="calendar-for-a-warehouse"></a>Kalendář pro sklad
Můžete přiřadit kalendář ke skladu a označit tak otevřená data příjmu a expedice. Pokud skladu není přiřazen žádný kalendář, předpokládá se, že je otevřený všechny dny. 

> [!Note]
> Přiřazení kalendáře tranzitnímu skladu nemá žádný vliv. Tranzitní sklady se používají na podporu příkazů k převodu. Příslušná data expedice nebo příjmu pro objednávky jsou definována podle otevřených dní v odchozím a přijímajícím skladu a režimu kalendáře dodávek.

#### <a name="closed-for-pickup-policy"></a>Zásada Uzavřeno pro výdej
Pokud chcete určit, že je sklad otevřený pro příjem, ale vyzvednutí není možné, můžete použít možnost **zásady Uzavřeno pro vyzvednutí** ve skladovém kalendáři. Toto nastavení platí i pro vyzvednutí zákazníkem. 

### <a name="transport-calendar"></a>Dopravní kalendář 
Pokud chcete označit data, která jsou dostupná pro expedici převodních příkazů z **odchozího skladu**, můžete přiřadit **přepravní kalendář**. Můžete nastavit kalendář přepravy podle způsobu dodání nebo podle režimu dodání a ze skladu. Kalendář přepravy je nastaven v cestě **Prodej a marketing > Nastavení > Distribuce > Režimy doručení**. Vyberte režim doručení a klikněte na tlačítko **Kalendář přepravy**.

Lze vytvořit řádek pro každý sklad a režim dodání, kde je kalendář přidán do sloupce **Kalendář přepravy**. Určí se tak kalendář přepravy, který se použije při odeslání zboží ze skladu pomocí daného způsobu dodávky. Chcete-li dopravní kalendář použít u všech dodávek pomocí daného způsobu dodání, lze vytvořit řádek bez určení skladu.  To bude mít vliv na všechny dodávky pomocí daného režimu dodávky, bez ohledu na sklad. 

Pokud není přiřazen žádný kalendář přepravy, předpokládá se, že jsou pro přepravu otevřeny všechny dny.

### <a name="calendar-for-a-customer"></a>Kalendář pro zákazníka
K označení dat, kdy může odběratel přijímat dodávky, můžete odběrateli přiřadit kalendář příjmu. Pokud odběrateli není přiřazen žádný kalendář, předpokládá se, že odběratel může přijmout objednávky ve všechny dny. Tato akce ovlivní datum příjmu na řádcích prodejní objednávky. Pokud vyberete datum v řádcích prodejní objednávky, které nejsou v kalendáři odběratele otevřené, systém označí, že datum příjmu není platné. 

Všimněte si, že je možné zahrnout pouze jeden kalendář na odběratele. Pokud potřebujete zahrnout kalendář pro každou jinou adresu pro odběratele, můžete vytvořit jednoho odběratele na adresu a přiřadit jeho odpovídající kalendář. 

Požadované datum příjmu v řádcích prodejní objednávky je ovlivněno kalendářem odběratele a způsobem kontroly data doručení. Více informací o výpočtu nejstaršího data doručení získáte v části [Příslib objednávky.](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/delivery-dates-available-promise-calculations).

### <a name="shipping-calendar-for-a-legal-entity"></a>Kalendář expedice pro právnickou osobu
Pokud chcete označit data, ve kterých může právnická osoba expedovat zboží, můžete nastavit kalendář expedice v části **Správa organizace > Organizace > Právnické osoby**. Vyberte právnickou osobu a přidejte kalendář na kartě **Zahraniční obchod a logistika** v poli **Expediční kalendář**. Expediční kalendář bude sloužit jako zdroj výchozích hodnot pro všechny kalendáře skladu v právnické osobě. 

## <a name="how-calendars-affect-dates-in-planning"></a>Jak kalendáře ovlivňují data v plánování

### <a name="order-date-of-a-planned-purchase-order"></a>Datum objednávky v plánované nákupní objednávce 
Datum objednávky na plánované nákupní objednávce určuje datum, kdy byla objednávka vystavena. Bude to otevřené datum v kalendáři dodavatele i v kalendáři skupiny disponibility. V některých případech dodavatele nutné několik dní marže mezi při jejich obdržení nákupní objednávky a při jejich může expedovat zboží. Tato data jsou uvedeny v rozpětí dnů dodavatele. Pokud je však zakoupená položka přiřazena ke skupině disponibility se dny marže tyto dny marže přepíšou dny marže dodavatele.

### <a name="delivery-date-of-a-planned-purchase-order"></a>Datum dodání plánované nákupní objednávky
Datum příjmu nákupu označuje datum, kdy obdržíte zboží. Bude to otevřené datum v kalendáři. Kalendář, který bude vzat do úvahy k označení, které dny lze nákupní objednávku přijmout, jsou následující, v pořadí od nejvyšší k nejnižší priority: 
1. Kalendář dodavatele
1. Kalendář pro skupinu disponibility
1. Skladový kalendář pro přijímající sklad

Kalendáři skupiny disponibility lze nastavit na různé stránky a bude mít prioritu v následujícím pořadí:
1. Skupiny disponibility položky na stránce **Disponibilita položky**
1. Skupina disponibility položky na stránce **Detaily uvolněného produktu**
1. Výchozí skupina disponibility položky v **parametrech hlavního plánování**

### <a name="shipping-date-of-a-planned-transfer-order"></a>Datum dodání plánované objednávky převodu
Při vytváření objednávky převodu mezi dvěma sklady jsou datum expedice a datum příjmu zahrnuty v záhlaví objednávky přenosu spolu s hodnotou Ze skladu a Do skladu. Rozdíl mezi těmito dvěma daty je očekávaná doba přepravy (ve dnech) mezi sklady.

Plánovaný převodní příkaz označuje datum, kdy je zboží expedováno z odchozího skladu. Kalendáře používané k určení dostupného data expedice jsou seřazeny podle priority: 
1. Kalendář odchozího skladu
1. Kalendář skupiny disponibility (viz záložní objednávka pro tento kalendář výše) Pokud je nastavený skladový kalendář, bude datum expedice otevřené datum v kalendáři. Pokud není nastaven skladový kalendář, převezme kalendář skupiny disponibility. 

### <a name="receipt-date-of-a-planned-transfer-order"></a>Datum přijetí plánované objednávky převodu
Datum přijetí objednávky převodu označuje datum přijetí zboží v příchozím skladu.

Kalendáře používané k určení dostupného data příjmu jsou seřazeny podle priority: 
1. Kalendář pro skupinu disponibility 
1. Kalendář přijímajícího skladu Pokud je nastavený kalendář disponibility, bude datum příjmu otevřené datum v kalendáři. Jestliže není nastaven kalendář skupiny disponibility, použije se skladový kalendář. 

Při hledání data expedice a příjmu plánovaného převodu budou zohledněny také marže vystavené uživatelem pro expedici a příjem. 

## <a name="using-calendars-in-master-planning"></a>Používání kalendářů v hlavním plánování

### <a name="assignment-of-scm-calendars"></a>Přiřazení kalendářů SCM
Je nutné nastavit kalendáře k identifikaci pracovních dní společnosti. Nejlepší implementací je nastavit kalendář pro každý prvek s jinými pracovními dny. Jinak řečeno, všechny externí kalendáře (odběratel, dodavatel) a všechny interní kalendáře (sklad, skupina disponibility a způsob dodání) související se společností.

### <a name="recommendation-on-warehouse-calendars"></a>Doporučení ohledně kalendáře skladu
Je doporučeno použít jeden kalendář na sklad pro zahrnutí pouze konkrétních změn ovlivňujících sklad. Dva nebo více skladů může mít například stejné pracovní dny, ale jiné zásady výdeje. V takovém případě kalendář pro jednotlivé sklady s příslušnými zásadami vyskladnění představují nejlepší implementaci pro systém k zahrnutí nejlepších dat plánovaného nákupu, převodu a výrobních zakázek. Pokud nejsou nastaveny žádná kalendáře skladu, kalendář právnické osoby lze použít také jako zdroj výchozích hodnot kalendáře skladu. 

### <a name="recommendation-of-coverage-group-calendars"></a>Doporučení kalendářů pro skupiny disponibility
Pokud jde o kalendář skupiny disponibility, je třeba uvážit, že existuje chování přepisu týkající se příjmu dat do hlavního plánování. Proto doporučujeme používat ho opatrně. Zvláště to je užitečné v případě, že musí být doplnění v určité dny v týdnu. 

### <a name="updating-scm-related-calendars"></a>Aktualizace kalendářů souvisejících se SCM
I když je důležité, aby všechny relevantní kalendáře měly přiřazené odpovídajících místo (dodavatele, odběratele, sklad, způsob dodání nebo skupinu disponibility), jejich aktualizace je stejně důležitá, aby odrážely změnu. Systém definuje datum výroby, převodu, nákupu a prodejní objednávky podle kombinace přiřazené kalendáře. Osvědčilo se objasnit, kdo nese odpovědnost za přiřazování a aktualizaci kalendářů v příslušných oblastech. V případě rozdělení či jiných neobvyklých změn pracovních dnů je nutné aktualizovat kalendáře příslušným způsobem. Všechny úkoly, které závisí na kalendářích, jako je hlavní plánování a plánování výroby, je nutné při aktualizaci kalendářů provést znovu. 
