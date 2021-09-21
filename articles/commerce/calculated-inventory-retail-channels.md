---
title: Výpočet dostupnosti zásob pro maloobchodní kanály
description: V tomto tématu je popsán způsob, jakým společnost může pomocí Microsoft Dynamics 365 Commerce zobrazit odhadovanou dostupnost na skladě pro produkty v online a obchodních kanálech.
author: hhainesms
ms.date: 09/01/2021
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
ms.openlocfilehash: d3cfd8c2f0b88a4e634cee0398283a51eddf60b2
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472164"
---
# <a name="calculate-inventory-availability-for-retail-channels"></a>Výpočet dostupnosti zásob pro maloobchodní kanály

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

V tomto tématu je popsán způsob, jakým společnost může pomocí Microsoft Dynamics 365 Commerce zobrazit odhadovanou dostupnost na skladě pro produkty v online a obchodních kanálech.

## <a name="accuracy-of-inventory-availability"></a>Přesnost dostupnosti zásob

Služba Commerce používá více serverů a databází k zajištění škálovatelnosti a výkonu. Proto je důležité, abyste pochopili, že dostupné hodnoty zásob, které jsou poskytovány prostřednictvím aplikace v rámci prodeje (POS), prostřednictvím rozhraní (API) pro dostupnost zásob e-Commerce a na stránkách zásob na skladě v Commerce Headquarters nemusí být 100% přesné v reálném čase. Pokud nebyly transakce vytvořené pro produkty v kanálu online nebo obchodu dosud synchronizovány s centrálou, nemusí být na stránkách zásob na skladě v centrále zobrazena přesná hodnota zásob v reálném čase pro tyto produkty. Naopak, pokud jste nakonfigurovali společnost tak, aby uživatelé v centrále nebo v jiných integrovaných aplikacích mohli prodávat, získávat, vracet nebo jinak upravovat zásoby z obchodu nebo online skladu, může POS nebo online kanál obsahovat všechny informace, které jsou nutné k zobrazení přesné hodnoty v reálném čase pro položky.

Je důležité, abyste porozuměli tomu, že veškerá data dostupnosti na skladě, která jsou poskytována v průběhu operačního dne, jsou považována za odhadovanou hodnotu. Pokud se tedy pokusíte porovnat informace o množství na skladě, které aplikace poskytuje se skutečnými fyzickými zásobami v regálech, nebo pokud se pokusíte porovnat hodnoty na skladě zobrazené v POS s údaji na skladě, které najdete pro stejný sklad v centrále, tyto hodnoty se mohou lišit. Tento rozdíl v provozním dnu je očekávaný a neměl by být považován za problém. Chcete-li auditovat data a ujistit se, že hodnoty, které jsou k dispozici v POS, rozhraní API a centrále, odpovídají skutečným fyzickým jednotkám, které jste našli v obchodě nebo ve skladu, nejlepším řešením je učinit tak po dokončení operací s kanálem pro daný den a po správné synchronizaci všech transakcí mezi centrálou a kanály.

## <a name="channel-side-inventory-calculation"></a>Výpočet zásob na straně kanálu

Výpočet zásob na straně kanálu je mechanismus, který bere jako základ poslední známá data zásob kanálu v ústředí Commerce, a poté zohlední další změny zásob, ke kterým došlo na straně kanálu, které nejsou zahrnuty do tohoto základu pro výpočet téměř reálného stavu – odhadované vlastní zásoby v reálném čase. 

V logice výpočtu zásob na straně kanálu jsou aktuálně zohledněny následující změny zásob:

- Zásoby prodávané prostřednictvím pokladních objednávek v obchodě
- Zásoby prodávané prostřednictvím objednávek zákazníků v obchodě nebo online kanálu
- Zásoby vrácené do skladu
- Zásoby vydané (výběr, zabalení, odeslání) ze skladu

Chcete-li použít výpočet zásob na straně kanálu, musíte povolit funkci **Optimalizovaný výpočet dostupnosti produktu**.

Pokud je vaše obchodní prostředí verze **10.0.8 až 10.0.11**, postupujte následovně.

1. V centrále obchodování jděte na možnost **Retail a Commerce** \> **Sdílené parametry obchodu**.
1. Na kartě **Zásoby** v poli **Úloha dostupnosti produktu** vyberte **Použít optimalizovaný proces pro úlohu dostupnosti produktu**.

Pokud je vaše obchodní prostředí verze **10.0.12 nebo pozdější**, postupujte následovně.

1. V centrále obchodu jděte na **Pracovní prostory \> Správa funkcí** a povolte funkci **Výpočet optimalizované dostupnosti produktu**.
1. Pokud vaše online a prodejní kanály používají stejné sklady plnění, musíte také povolit funkci **Vylepšená logika výpočtu inventáře na straně kanálu**. Tímto způsobem logika výpočtu na straně kanálu vezme v úvahu neodeslané transakce, které jsou vytvořeny v kanálu úložiště. (Těmito transakcemi mohou být transakce cash-and-carry, objednávky zákazníků a vrácení.)
1. Spusťte úlohu **1070** (**konfigurace kanálu**).

Pokud bylo vaše prostředí Commerce upgradováno z verze, která je starší než verze Commerce 10.0.8, po povolení funkce **Optimalizovaný výpočet dostupnosti produktu**, musíte také spustit **inicializaci plánovače obchodu**, aby se funkce projevila. Pokud chcete spustit inicializaci, jděte na **Retail a Commerce** \> **Nastavení centrály** \> **Plánovač obchodu**.

Chcete-li použít výpočet zásob na straně kanálu, je nezbytným předpokladem odeslání pravidelného snímku údajů o zásobách z centrály vytvořeného úlohou **Dostupnost produktu** do databází kanálu. Snímek představuje informace, které má ústředí k dispozici o zásobách pro určitou kombinaci produktu nebo varianty produktu a skladu. Zahrnuje pouze transakce zásob, které byly zpracovány a zaúčtovány v centrále v době, kdy byl snímek pořízen, a nemusí být 100% přesný v reálném čase kvůli neustálému zpracování prodeje, ke kterému dochází na distribuovaných serverech.

- Pokud byly zásoby prodávány pro produkt ve skladu prostřednictvím hotovostního a mezipodnikového prodeje odběratele v aplikaci POS, nebude centrála okamžitě obsahovat informace o související transakci výdeje zásob pro daný prodej. Centrála bude obsahovat informace o zásobách, které jsou prodány pro tyto typy prodeje obchodu pouze poté, co úloha P nahraje související transakci z databáze kanálů obchodu do centrály a související prodejní objednávky jsou vytvořeny prostřednictvím výpisu zaúčtování nebo dávkové zpracování postupného informačního kanálu. Proces vytvoření objednávky v centrále vytvoří související skladové transakce. 
- U kanálů s kanály elektronického obchodování obsahuje centrála informace o skladových transakcích pouze po odeslání transakcí do centrály prostřednictvím úlohy P a dokončení procesu synchronizace objednávky.

Chcete-li vytvořit snímek zásob v rámci centrály, postupujte podle následujících kroků.

1. Přejděte na **Retail and Commerce \> Retail and Commerce IT \> Produkty a zásoby \> Dostupnost produktu**.
1. Klepnutím na tlačítko **OK** spustíte úlohu **Dostupnost produktu**. Tuto úlohu lze rovněž naplánovat tak, aby byla spuštěna v dávce.

Po dokončení úlohy **Dostupnost produktu** musí být zachycená data přesunuta do databází kanálů tak, aby poslední snímek zásob služby centrály mohl být zvážen při výpočtu odhadovaných zásob na skladě.

Chcete-li synchronizovat data snímků z centrály do databází vašeho kanálu, postupujte takto.

1. Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**.
1. Spusťte úlohu **1130** (**Dostupnost produktu**), která synchronizuje data úlohy **Dostupnost produktu** vytvořená z centrály do databází vašeho kanálu.

## <a name="inventory-availability-apis-for-e-commerce"></a>Rozhraní API pro dostupnost zásob pro elektronický obchod

Commerce poskytuje následující rozhraní API pro scénáře elektronického obchodu pro dotazování dostupnosti zásob produktu:

- **GetEstimatedAvailability** – Pomocí tohoto rozhraní API můžete dotazovat zásoby produktu nebo varianty produktu ve skladu online kanálu nebo ve skladech, které jsou propojeny se skupinou plnění online kanálu.
- **GetEstimatedProductWarehouseAvailability** – pomocí tohoto rozhraní API můžete dotazovat zásoby pro produkt nebo variantu produktu z určitého skladu.

> [!NOTE]
> Tato rozhraní API nahrazují API **GetProductAvailabilities** a **GetAvailableInventoryNearby** v Commerce verze 10.0.7 a starší.

Obě API interně používají logiku výpočtu na straně kanálu a vrací odhadované **fyzicky dostupné** množství, množství **celkem k dispozici**, **měrná jednotka (UoM)** a **úroveň zásob** pro požadovaný produkt a sklad. Vrácené hodnoty lze v případě potřeby zobrazit na webu elektronického obchodu nebo je lze použít k aktivaci jiné obchodní logiky na vašem webu elektronického obchodu. Můžete například zabránit nákupu produktů s úrovní zásob „není skladem“.

Přestože jiná rozhraní API, která jsou k dispozici v Commerce, mohou přejít přímo do centrály a načíst množství na skladě pro produkty, nedoporučujeme, aby se používaly v prostředí elektronického obchodování z důvodu potenciálních problémů s výkonem a souvisejícího dopadu, který mohou tyto časté požadavky mít na serverech centrály. Navíc s výpočtem na straně kanálu mohou dvě výše uvedená rozhraní API poskytnout přesnější odhad dostupnosti produktu zohledněním transakcí vytvořených v kanálech, které ústředí dosud nejsou známy.

Chcete-li definovat, jak má být ve výstupu API vráceno množství produktu, postupujte takto.

1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry obchodu**.
1. Vyberte kartu **Zásoby** a poté na rychlé kartě **Rozhraní API dostupnosti zásob pro elektronický obchod** nakonfigurujte hodnotu nastavení **Množství ve výstupu API**.
1. Spusťte úlohu **1070** (**Konfigurace kanálu**), aby se synchronizovala poslední nastavení do kanálů.

Nastavení **Množství ve výstupu API** poskytuje tři možnosti:

- **Vrátit množství zásob** – Ve výstupu API se vrací fyzické dostupné a celkové dostupné množství požadovaného produktu.
- **Vrátit množství zásob odečtením vyrovnávací paměti zásob** – Množství vrácené ve výstupu API se upraví odečtením hodnoty vyrovnávací paměti zásob. Další informace o vyrovnávací paměti zásob viz [Konfigurace vyrovnávací paměti zásob a úrovní zásob](inventory-buffers-levels.md).
- **Nevrátit množství zásob** – Ve výstupu rozhraní API se vrátí pouze úroveň zásob. Další informace o úrovních zásob viz [Konfigurace vyrovnávací paměti zásob a úrovní zásob](inventory-buffers-levels.md).

Můžete použít parametr API `QuantityUnitTypeValue` k určení typu jednotky, ve které chcete, aby rozhraní API vrátila množství. Tento parametr podporuje možnosti **jednotka zásob** (výchozí), **nákupní jednotka** a **prodejní jednotka**. Vrácené množství je zaokrouhleno na definovanou přesnost odpovídající měrné jednotce (UOM) v centrále.

Rozhraní API **GetEstimatedAvailability** nabízí následující vstupní parametry pro podporu různých scénářů dotazů:

- `DefaultWarehouseOnly` – Tento parametr použijte k dotazování na zásoby produktu ve výchozím skladu online kanálu. 
- `FilterByChannelFulfillmentGroup` a `SearchArea` – Pomocí těchto dvou parametrů můžete dotazovat zásoby produktu ze všech míst vyzvednutí v konkrétní oblasti vyhledávání na základě parametrů `longitude`, `latitude` a `radius`. 
- `FilterByChannelFulfillmentGroup` a `DeliveryModeTypeFilterValue` – Tyto dva parametry použijte k dotazování na zásoby produktu ze specifických skladů, které jsou propojeny se skupinou plnění online kanálu a jsou nakonfigurovány tak, aby podporovaly určité způsoby doručení. Parametr `DeliveryModeTypeFilterValue` podporuje možnosti **vše** (výchozí), **doprava** a **vyzvednutí**. Například ve scénáři, kde lze online objednávku splnit z více přepravních skladů, můžete tyto dva parametry použít k dotazu na dostupnost zásob produktu ve všech těchto přepravních skladech. Rozhraní API v tomto případě vrací množství produktu a úroveň zásob v každém z přepravních skladů, plus agregované množství a agregovanou úroveň zásob ze všech přepravních skladů v rozsahu dotazu.
 
Buy box Commerce, výběr obchodu, seznam přání, košík a ikona košíku využívají výše uvedená rozhraní API a parametry k zobrazování zpráv na úrovni zásob na webu elektronického obchodu. Nástroj pro tvorbu webů Commerce poskytuje různá nastavení inventáře pro řízení chování zboží a nákupu. Další informace [Použít nastavení zásob](inventory-settings.md).

## <a name="pos-inventory-lookup-with-channel-side-calculation"></a>Vyhledávání zásob POS s výpočtem na straně kanálu

V Commerce verze 10.0.9 a starší se operace **Vyhledávání zásob** z POS použila při volání služby centrály k získání informací o zásobách pro vybraný produkt, pro aktuální obchod uživatele i pro všechny ostatní obchody, které jsou nakonfigurovány pro skupinu plnění, jako součást konfigurace kanálu pro daný obchod. Ve verzi Commerce 10.0.10 a novější můžete vypnout volání služby v reálném čase do centrály a místo toho použít výpočet na straně kanálu na serveru Commerce k určení okamžitých zásob, které jsou fyzicky k dispozici pro obchod a další umístění, která jsou definována ve skupině plnění. Tato konfigurace vypočtených zásob kanálů je rovněž užitečná pro místa, kde je připojení k Internetu nespolehlivé, protože nemusíte být online pro získání vyhledávání zásob z centrály.

Je-li výpočet na straně kanálu správně nakonfigurován a spravován, může poskytovat spolehlivější odhad aktuálních skladových zásob, protože používá transakční data, která jsou uložena v databázi kanálů Commerce, ale centrála ještě nemusí tyto informace obsahovat. Použijete-li například existující volání v reálném čase služby pro vyhledávání zásob v POS, nebude mít centrála k dispozici informace o prodeji a převodu, které se právě vyskytly u produktu. Hodnota množství na skladě, kterou centrála vrátí pro daný produkt, však pravděpodobně překročí skutečné množství na skladě pro obchod o jednu jednotku. Pokud však použijete výpočet na straně kanálu, bude prodej uskutečněný a přenesený do výpočtu určen a odečten od zobrazené hodnoty množství na skladě. Ačkoliv hodnoty, které jsou vyvolány výpočtem na straně kanálu a jsou v reálném čase, poskytují pouze odhady množství na skladě, hodnota, kterou výpočet na straně kanálu poskytuje, je pro aktuální obchod mnohem pravděpodobnější.

Chcete-li nakonfigurovat operaci POS **Vyhledání skladových zásob** v ústředí Commerc k použití logiky výpočtu na straně kanálu a vypnout volání služeb v reálném čase, musíte nejprve povolit funkci **Výpočet optimalizované dostupnosti produktu** prostřednictvím pracovního prostoru **Správa funkcí** v ústředí Commerce a postupovat následovně.

1. Přejděte na **Maloobchodní a velkoobchodní prodej \> Instalace kanálu \> Nastavení POS \> Profily POS \> Funkční profily**.
1. Vyberte funkční profil.
1. Na pevné záložce **Funkce** v části **Výpočet dostupnosti zásob** změňte hodnotu pole **Režim výpočtu dostupnosti zásob** ze **Služby v reálném čase** na **Kanál**. Všechny funkční profily standardně používají volání služby v reálném čase. Chcete-li použít výpočetní logiku na straně kanálu, je nutné změnit hodnotu tohoto pole. Tato změna ovlivní všechny maloobchodní obchody propojené s vybraným profilem funkčnosti.

Poté je nutné synchronizovat změny kanálů pomocí procesu plánu distribuce v centrále následujícím postupem.

1. Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**.
1. Spusťte úlohu **1070** (**konfigurace kanálu**).

Po dokončení konfigurace již informace o fyzicky dostupných zásobách nepoužívají volání služby v reálném čase, pokud uživatel v aplikaci POS používá operaci **Vyhledávání zásob** (standardní a maticová zobrazení). Místo toho jsou data o fyzicky dostupných zásobách pro aktuální obchod a všech obchodech ve skupině plnění vypočítána na základě posledního známého snímku, který byl dodán do databáze kanálů ze služby Commerce Headquarters. Hodnota snímku je dále upřesněna výpočtem na straně kanálu za účelem nastavení fyzicky dostupné hodnoty na základě dalších transakcí prodeje nebo vrácení, které existují pro vybraný produkt v databázi kanálů, které nebyly zahrnuty do posledního synchronizovaný snímek z úlohy 1130. Pokud databáze kanálu neobsahuje transakční data pro žádný ze skladů nebo obchodů ve skupině plnění, neobsahuje žádné další transakce, které lze rozlišit do přepočtu hodnoty. Nejlepším odhadem množství na skladě, které lze zobrazit pro tyto sklady nebo obchody, jsou data z posledního snímku služby Commerce Headquarters.

Obrazovky **Splnění objednávky** v POS také využívají výpočet na straně kanálu a zobrazení množství na skladě pro položky v případě, že je vybrán řádek plnění objednávky a uživatel zobrazí panel **Podrobnosti** pro množství na skladě pro vybranou položku.

## <a name="optimize-your-inventory-data"></a>Optimalizace dat zásob

Chcete-li zajistit nejlepší možný odhad zásob, je důležité, abyste používali následující úlohy služby Commerce Batch a spouštěli je často:

- **Úloha P** – úlohu P lze najít na stránce **Plány distribuce** a měla by být spouštěna často. Tato úloha přináší objednávky e-Commerce, asynchronní objednávky odběratele, které vytvořil POS, a objednávky v hotovosti vytvořené z databází kanálů do služby Commerce Headquarters, aby mohly být dále zpracovány. Dokud nebudou tato data synchronizována z kanálu do služby Commerce Headquarters, nemá obchodní ústředí žádné informace o úpravách zásob pro produkty v skladech, které jsou výsledkem těchto transakcí.
- **Synchronizovat objednávky** – Tato úloha zpracuje neformátovaná transakční data ve službě Commerce Headquarters, která úloha P poskytuje a převádí transakce e-Commerce a asynchronní objednávky odběratele do prodejních objednávek v Commerce Headquarters. Dokud nebude tato úloha zpracována a nebudou vytvořeny prodejní objednávky, nebudou vytvořeny žádné skladové transakce. To znamená, že množství na skladě v Commerce Headquarters tyto transakce nebere v úvahu.
- **Výpočet transakčních výpisů v dávce** – pro transakce cash-and-carry, které jsou vytvořeny v obchodě, proces postupného zaúčtování informačního kanálu zajišťuje efektivní aktualizaci skladů, které souvisejí s prodejem. Chcete-li získat nejúčinnější zpracování skladových transakcí pro objednávky cash-and-carry, nezapomeňte nakonfigurovat systém tak, aby používal [postupné zaúčtování kanálu](./trickle-feed.md).
- **Zaúčtovat transakční příkazy v dávce** – Tato úloha je také vyžadována pro postupné zaúčtování kanálu. Následuje po úloze **Vypočítat transakční výpisy v dávce**. Tato úloha systematicky zaúčtuje vypočtené výkazy, takže prodejní objednávky pro prodeje cash-and-carry jsou vytvořeny v Commerce Headquarters a Commerce Headquarters přesněji odráží zásoby vašeho obchodu.
- **Dostupnost produktu** – Tato úloha vytvoří snímek zásob z služby Commerce Headquarters.
- **1130 (dostupnost produktu)** – Tato úloha se nachází na stránce **Plány distribuce** a měla by být spuštěna bezprostředně po úloze **Dostupnosti produktu**. Tato úloha přepravuje data snímku zásob z Commerce Headquarters do databází kanálů.

> [!NOTE]
> - Obecně je nejlepší spouštět úlohy **Dostupnost produktu** a **1130** každou hodinu a naplánovat P-úlohu, synchronizovat objednávky a úlohy související s postupným účtováním se stejnou nebo vyšší frekvencí.
> - Z důvodů výkonnosti je při výpočtu dostupnosti zásob na straně kanálu použit k vytvoření požadavku na dostupnost zásob pomocí rozhraní API e-Commerce nebo nové logiky zásob na straně POS v případě, že uplynul dostatečný čas pro opětovné spuštění výpočetní logiky. Výchozí mezipaměť je nastavena na 60 sekund. Zapnuli jste například výpočet na straně kanálu pro váš obchod a zobrazili jste množství na skladě pro produkt na stránce pro **Vyhledávání zásob**. Je-li poté prodána jedna jednotka produktu, nebude stránka **Vyhledávání zásob** ukazovat snížený stav zásob, dokud nebude mezipaměť vymazána. Jakmile uživatelé zaúčtují transakce v POS, měli by počkat 60 sekund, než se ověří, že množství na skladě bylo sníženo.

Pokud váš obchodní scénář vyžaduje menší čas v mezipaměti, požádejte o pomoc pracovníka technické podpory.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
