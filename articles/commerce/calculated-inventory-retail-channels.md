---
title: Vypočítat dostupnost zásob pro maloobchodní kanály
description: V tomto tématu jsou popsány možnosti, které jsou k dispozici pro zobrazení množství na skladě pro obchod a online kanály.
author: hhainesms
ms.date: 08/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-11
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 29efccab017d9dff98872871bfe953fba19d2c30
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799678"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Výpočet dostupnosti zásob pro maloobchodní kanály

[!include [banner](../includes/banner.md)]

V tomto tématu je popsán způsob, jakým společnost může pomocí Microsoft Dynamics 365 Commerce zobrazit odhadovanou dostupnost na skladě pro produkty v online a obchodních kanálech.

## <a name="accuracy-of-calculation"></a>Přesnost výpočtu

Služba Commerce používá více serverů a databází k zajištění škálovatelnosti a výkonu. Proto je důležité, abyste pochopili, že dostupné hodnoty zásob, které jsou poskytovány prostřednictvím aplikace v rámci prodeje (POS), prostřednictvím rozhraní (API) pro dostupnost zásob e-Commerce a na stránkách zásob na skladě v Commerce Headquarters nemusí být 100% přesné v reálném čase. Pokud nebyly transakce vytvořené pro produkty v kanálu online nebo obchodu dosud synchronizovány se serverem a databází služby Commerce Headquarters, nemusí být na stránkách zásob na skladě v Commerce Headquarters zobrazena přesná hodnota zásob v reálném čase pro tyto produkty. Naopak, pokud jste nakonfigurovali společnost tak, aby uživatelé v Commerce Headquarters nebo v jiných integrovaných aplikacích mohli prodávat, získávat, vracet nebo jinak upravovat zásoby z obchodu nebo online skladu, může POS nebo online kanál obsahovat všechny informace, které jsou nutné k zobrazení přesné hodnoty na skladě v reálném čase pro položky.

V tomto tématu jsou vysvětleny procesy synchronizace dat, které lze často spouštět, aby bylo možné omezit latenci dat mezi aplikacemi nebo kanály. Je však důležité, abyste porozuměli tomu, že veškerá data dostupnosti na skladě, která jsou poskytována v průběhu operačního dne, jsou považována za odhadovanou hodnotu. Pokud se tedy pokusíte porovnat informace o množství na skladě, které aplikace poskytuje se skutečnými fyzickými zásobami v regálech, nebo pokud se pokusíte porovnat hodnoty na skladě zobrazené v POS s údaji na skladě, které najdete pro stejný sklad v Commerce Headquarters, tyto hodnoty se mohou lišit. Tento rozdíl v provozním dnu je očekávaný a neměl by být považován za problém. Chcete-li auditovat data a ujistit se, že hodnoty, které jsou k dispozici v rozhraní API dostupnosti zásob a Commerce Headquarters, odpovídají skutečným fyzickým jednotkám, které jste našli v obchodě nebo ve skladu, nejlepším řešením je učinit tak po dokončení operací s kanálem pro daný den a po správné synchronizaci všech transakcí mezi Commerce Headquarters a kanálem.

## <a name="use-inventory-lookup-apis-for-e-commerce-inventory-availability-requests"></a>Použít API vyhledávání zásob pro požadavky na dostupnost zásob e-Commerce

Pomocí následujících rozhraní API můžete zobrazit dostupnost zásob pro produkt, když se odběratelé nakupují na webu e-Commerce.

- **GetEstimatedAvailability** – pomocí tohoto rozhraní API můžete získat dostupnost zásob pro položku ve skladu kanálu e-Commerce nebo všechny sklady, které jsou spojeny s konfigurací skupiny plnění pro kanál elektronického obchodu. Toto rozhraní API lze také použít pro sklady v určité oblasti nebo radiu vyhledávání na základě zeměpisných dat.
- **GetEstimatedProductWarehouseAvailability** – pomocí tohoto rozhraní API můžete požadovat zásoby pro položku z určitého skladu. Můžete jej například použít k zobrazení dostupnosti zásob ve scénářích, které zahrnují výdej objednávky.

> [!NOTE]
> Tato rozhraní API nahradí **GetProductAvailabilities** a **GetAvailableInventoryNearby** v Dynamics 365 Retail verze 10.0.7 a starší.

Obě rozhraní API načítají data ze serveru Commerce a poskytují odhad množství na skladě pro specifickou kombinaci produktu nebo varianty produktu a skladu. Přestože jiná rozhraní API, která jsou k dispozici naserveru Commerce, mohou přejít přímo do služby Commerce Headquarters a načíst množství na skladě pro produkty, nedoporučujeme, aby se používaly v prostředí elektronického obchodování z důvodu potenciálních problémů s výkonem a souvisejícího dopadu, který mohou tyto časté požadavky mít na serverech služby Commerce Headquarters. Pokud se navíc množství na skladě počítá prostřednictvím serveru Commerce, výpočet bude pravděpodobně zahrnovat zásoby, které byly prodány v posledních transakcích elektronického obchodu, které dosud nebyly synchronizovány s produktem Commerce Headquarters. Ačkoli Commerce Headquarters nemusí mít informace o těchto transakcích, databáze serveru Commerce a kanálu mají tato data. Proto budou data odvozena v aplikaci a mohou vám pomoci poskytnout přesnější odhad dostupných zásob produktu.

### <a name="get-started-with-e-commerce-calculated-inventory-availability"></a>Začínáme s vypočítanou dostupností zásob e-Commerce

Než použijete dvě rozhraní API, která byla zmíněna výše, musíte povolit funkci **Výpočet optimalizované dostupnosti produktu** prostřednictvím pracovního prostoru **Správa funkcí** v Commerce Headquarters.

Předtím, než může rozhraní API vypočítat nejlepší odhad dostupnosti zásob pro určitou položku, musí být zpracován pravidelný snímek dostupnosti zásob ze služby Commerce Headquarters a odeslán do databáze kanálů, kterou používá jednotka elektronického obchodu Commerce Scale Unit. Snímek představuje informace, které má program Commerce Headquarters k dispozici na skladě pro určitou kombinaci produktu nebo varianty produktu a skladu. Může zahrnovat úpravy zásob nebo pohyby, které jsou způsobeny skladovými příjmy, nebo dodávkami či jinými procesy prováděnými v rámci služby Commerce Headquarters a že kanál elektronického obchodu obsahuje informace pouze kvůli synchronizaci.

Ve snímku databáze, který vytvořila úloha **Dostupnost produktu**, budou v době pořízení snímku vypočteny pouze skladové transakce, které byly zpracovány a zaúčtovány do služby Commerce Headquarters. Pokud byly zásoby prodávány pro produkt ve skladovém skladu prostřednictvím hotovostního a mezipodnikového prodeje odběratele v aplikaci POS, nebude služba Commerce Headquarters okamžitě obsahovat informace o související transakci výdeje zásob pro daný prodej. Bude obsahovat informace o zásobách, které jsou prodány pro tyto typy prodeje obchodu pouze poté, co úloha P nahraje související transakci z databáze kanálů obchodu do služby Commerce Headquarters a související prodejní objednávka je vytvořena prostřednictvím výpisu. zaúčtování nebo dávkové zpracování trickleho informačního kanálu. Proces vytvoření objednávky v modulu Commerce Headquarters vytvoří související skladové transakce. U kanálů s kanály elektronického obchodování obsahuje Commerce Headquarters informace o skladových transakcích pouze po odeslání transakcí do služby Commerce Headquarters prostřednictvím úlohy P a dokončení procesu synchronizace objednávky. Proto je důležité, abyste si vědomi, že hodnota snímku zásob, která je k dispozici v úloze **Dostupnost produktu**, nemusí být 100% přesná v reálném čase, protože se jedná o stálé zpracování prodeje, ke kterému dochází v rámci distribuovaných serverů.

Chcete-li vytvořit snímek zásob v rámci služby Commerce Headquarters, postupujte podle následujících kroků.

1. Přejděte na **Retail and Commerce \> Retail and Commerce IT \> Produkty a zásoby \> Dostupnost produktu**.
1. Klepnutím na tlačítko **OK** spustíte úlohu **Dostupnost produktu**. Tuto úlohu lze rovněž naplánovat tak, aby byla spuštěna v dávce.

Po dokončení úlohy **Dostupnost produktu** musí být zachycená data přesunuta do databází kanálů elektronického obchodu tak, aby poslední snímek zásob služby Commerce Headquarters mohl být zvážen při výpočtu odhadovaných zásob na skladě.

1. Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**.
1. Spusťte úlohu **1130** (**Dostupnost produktu**), která synchronizuje data úlohy **Dostupnost produktu** vytvořená z Commerce Headquarters do databází vašeho kanálu.

Je-li vyžadována dostupnost zásob z API **GetEstimatedAvailability** nebo **GetEstimatedProductWarehouseAvailability**, je proveden výpočet, který se pokusí získat nejlepší možný odhad zásob produktu. Výpočet odkazuje na všechny objednávky odběratele e-Commerce, které jsou v databázi kanálů, ale nebyly zahrnuty do dat snímku, které poskytla úloha 1130. Tato logika se provádí sledováním poslední zpracované skladové transakce z služby Commerce Headquarters a jejím porovnáním s transakcemi v databázi kanálů. Poskytuje základ pro výpočetní logiku na straně kanálu, takže další pohyby zásob, které se vyskytly pro prodejní transakce objednávky odběratele v databázi kanálů elektronického obchodu, lze rozdělit na odhadovanou hodnotu zásob, kterou rozhraní API jišťují.

Logika výpočtu na straně kanálu vrací odhadovanou fyzicky dostupnou hodnotu a celkovou dostupnou hodnotu pro požadovaný produkt a sklad. Hodnoty lze v případě potřeby zobrazit na webu e-Commerce nebo je lze použít k aktivaci jiné obchodní logiky na vašem webu e-Commerce. Můžete například zobrazit zprávu "nedostatek zásob" namísto skutečného množství na skladě, které rozhraní API předalo.

Logika výpočtu, kterou rozhraní API e-Commerce na straně kanálu používá pro odhadovanou hodnotu zásob, může vyhodnotit zásoby na základě objednávek odběratelů, které byly vytvořeny v databázi kanálů, ale ještě nebyly synchronizovány a zaúčtovány do Commerce Headquarters. Pokud databáze kanálů obsahuje také transakční data pro hotovostní prodejní transakce skladů pro konkrétní obchod, hotovostní prodejní transakce se nezohldní ve výpočtu e-Commerce na straně kanálu pro tyto sklady.

## <a name="configure-the-inventory-lookup-operation-in-the-pos-channel"></a>Konfigurace operace vyhledávání zásob v kanálu POS

V modulu Retail verze 10.0.9 a starší se operace **Vyhledávání zásob** z POS použila při volání služby Commerce Headquarters k získání informací o zásobách pro vybraný produkt, pro aktuální obchod uživatele i pro všechny ostatní obchody, které jsou nakonfigurovány pro skupinu plnění, jako součást konfigurace kanálu pro daný obchod. V Commerce verze 10.0.10 a novější můžete volání služby v reálném čase vypnout v Commerce Headquarters. Namísto toho můžete na serveru Commerce Server použít výpočet na straně kanálu k určení množství na skladě, které je fyzicky k dispozici pro obchod a všechna ostatní místa, která jsou definována ve skupině plnění. Tato konfigurace vypočtených zásob kanálů je rovněž užitečná pro místa, kde je připojení k Internetu nespolehlivé, protože nemusíte být online pro získání vyhledávání zásob z programu Commerce Headquarters.

Je-li výpočet na straně kanálu správně nakonfigurován a spravován, může poskytovat spolehlivější odhad aktuálních skladových zásob, protože používá transakční data, která jsou uložena v databázi kanálů Commerce, ale Služba Commerce Headquarters ještě nemusí tyto informace obsahovat. Použijete-li například existující volání v reálném čase služby pro vyhledávání zásob v POS, nebude mít Služba Commerce Headquarters k dispozici informace o prodeji a převodu, které se právě vyskytly u produktu. Hodnota množství na skladě, kterou služba Commerce Headquarters vrátí pro daný produkt, však pravděpodobně překročí skutečné množství na skladě pro obchod o jednu jednotku. Pokud však použijete výpočet na straně kanálu, bude prodej uskutečněný a přenesený do výpočtu určen a odečten od zobrazené hodnoty množství na skladě. Ačkoliv hodnoty, které jsou vyvolány výpočtem na straně kanálu a jsou v reálném čase, poskytují pouze odhady množství na skladě, hodnota, kterou výpočet na straně kanálu poskytuje, je pro aktuální obchod mnohem pravděpodobnější.

### <a name="get-started-with-pos-channel-side-calculated-inventory-availability"></a>Začínáme s vypočítanou dostupností zásob na straně kanálu POS

Chcete-li použít logiku výpočtu na straně kanálu a vypnout volání služeb v reálném čase pro vyhledávání zásob z aplikace POS, musíte nejprve povolit funkci **Výpočet optimalizované dostupnosti produktu** prostřednictvím pracovního prostoru **Správa funkcí** v Commerce Headquarters. Kromě povolení této funkce musíte provést změny **funkčního profilu**.

Chcete-li změnit **funkční profil**, postupujte takto.

1. Přejděte na **Maloobchodní a velkoobchodní prodej \> Instalace kanálu \> Nastavení POS \> Profily POS \> Funkční profily**.
1. Vyberte funkční profil.
1. Na pevné záložce **Funkce** v části **výpočet dostupnosti zásob** změňte hodnotu pole **Režim výpočtu dostupnosti zásob** ze **Služby v reálném čase** na **Kanál**. Všechny funkční profily standardně používají volání služby v reálném čase. Chcete-li tedy použít výpočetní logiku na straně kanálu, je nutné změnit hodnotu tohoto pole. Tato změna ovlivní všechny maloobchodní obchody propojené s vybraným profilem funkčnosti.

Poté je nutné synchronizovat změny kanálu pomocí procesu plánu distribuce provedením následujících kroků:

1. Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**.
1. Spusťte úlohu **1070** (**konfigurace kanálu**).

Po dokončení konfigurace již informace o fyzicky dostupných zásobách nepoužívají volání služby v reálném čase, pokud uživatel v aplikaci POS používá operaci **Vyhledávání zásob** (standardní a maticová zobrazení). Místo toho jsou data o fyzicky dostupných zásobách pro aktuální obchod a všech obchodech ve skupině plnění vypočítána na základě posledního známého snímku, který byl dodán do databáze kanálů ze služby Commerce Headquarters. Hodnota snímku je dále upřesněna výpočtem na straně kanálu za účelem nastavení fyzicky dostupné hodnoty na základě dalších transakcí prodeje nebo vrácení, které existují pro vybraný produkt v databázi kanálů, které nebyly zahrnuty do posledního synchronizovaný snímek z úlohy 1130. Pokud databáze kanálu neobsahuje transakční data pro žádný ze skladů nebo obchodů ve skupině plnění, neobsahuje žádné další transakce, které lze rozlišit do přepočtu hodnoty. Nejlepším odhadem množství na skladě, které lze zobrazit pro tyto sklady nebo obchody, jsou data z posledního snímku služby Commerce Headquarters.

Obrazovky **Splnění objednávky** v POS také využívají výpočet na straně kanálu a zobrazení množství na skladě pro položky v případě, že je vybrán řádek plnění objednávky a uživatel zobrazí panel **Podrobnosti** pro množství na skladě pro vybranou položku.

## <a name="optimize-your-inventory-data"></a>Optimalizace dat zásob

Chcete-li zajistit nejlepší možný odhad zásob, je důležité, abyste používali následující úlohy služby Commerce Batch a spouštěli je často:

- **Úloha P** – úlohu P lze najít na stránce **Plány distribuce** a měla by být spouštěna často. Tato úloha přináší objednávky e-Commerce, asynchronní objednávky odběratele, které vytvořil POS, a objednávky v hotovosti vytvořené z databází kanálů do služby Commerce Headquarters, aby mohly být dále zpracovány. Dokud nebudou tato data synchronizována z kanálu do služby Commerce Headquarters, nemá obchodní ústředí žádné informace o úpravách zásob pro produkty v skladech, které jsou výsledkem těchto transakcí.
- **Synchronizovat objednávky** – Tato úloha zpracuje neformátovaná transakční data ve službě Commerce Headquarters, která úloha P poskytuje a převádí transakce e-Commerce a asynchronní objednávky odběratele do prodejních objednávek v Commerce Headquarters. Dokud nebude tato úloha zpracována a nebudou vytvořeny prodejní objednávky, nebudou vytvořeny žádné skladové transakce. To znamená, že množství na skladě v Commerce Headquarters tyto transakce nebere v úvahu.
- **Výpočet transakčních výpisů v dávce** – pro transakce cash-and-carry, které jsou vytvořeny v obchodě, proces postupného zaúčtování informačního kanálu zajišťuje efektivní aktualizaci skladů, které souvisejí s prodejem. Chcete-li získat nejúčinnější zpracování skladových transakcí pro objednávky cash-and-carry, nezapomeňte nakonfigurovat systém tak, aby používal [postupné zaúčtování kanálu](https://docs.microsoft.com/dynamics365/commerce/trickle-feed).
- **Zaúčtovat transakční příkazy v dávce** – Tato úloha je také vyžadována pro postupné zaúčtování kanálu. Následuje po úloze **Vypočítat transakční výpisy v dávce**. Tato úloha systematicky zaúčtuje vypočtené výkazy, takže prodejní objednávky pro prodeje cash-and-carry jsou vytvořeny v Commerce Headquarters a Commerce Headquarters přesněji odráží zásoby vašeho obchodu.
- **Dostupnost produktu** – Tato úloha vytvoří snímek zásob z služby Commerce Headquarters.
- **1130 (dostupnost produktu)** – Tato úloha se nachází na stránce **Plány distribuce** a měla by být spuštěna bezprostředně po úloze **Dostupnosti produktu**. Tato úloha přepravuje data snímku zásob z Commerce Headquarters do databází kanálů.

Doporučuje se, abyste tyto dávkové úlohy nespouštěli příliš často (každých několik minut). Časté běhy přetěžují ředitelství Commerce (HQ) a mohou potenciálně ovlivnit výkon. Obecně je dobrou praxí spouštět dostupnost produktu a 1130 úloh každou hodinu a naplánovat P-úlohu, synchronizovat objednávky a úlohy související s postupným účtováním se stejnou nebo vyšší frekvencí.

> [!NOTE]
> Z důvodů výkonnosti je při výpočtu dostupnosti zásob na straně kanálu použit k vytvoření požadavku na dostupnost zásob pomocí rozhraní API e-Commerce nebo nové logiky zásob na straně POS v případě, že uplynul dostatečný čas pro opětovné spuštění výpočetní logiky. Výchozí mezipaměť je nastavena na 60 sekund. Zapnuli jste například výpočet na straně kanálu pro váš obchod a zobrazili jste množství na skladě pro produkt na stránce pro **Vyhledávání zásob**. Je-li poté prodána jedna jednotka produktu, nebude stránka **Vyhledávání zásob** ukazovat snížený stav zásob, dokud nebude mezipaměť vymazána. Jakmile uživatelé zaúčtují transakce v POS, měli by počkat 60 sekund, než se ověří, že množství na skladě bylo sníženo.

Pokud Váš obchodní scénář vyžaduje menší čas v mezipaměti, požádejte o pomoc pracovníka technické podpory.


[!INCLUDE[footer-include](../includes/footer-banner.md)]