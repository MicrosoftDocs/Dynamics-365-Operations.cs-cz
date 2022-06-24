---
title: Nastavení parametrů nákladů za doručení
description: Tento článek popisuje, jak nastavit obecné informace a nastavení konfigurace, které se používají v modulu Náklady za doručení pro účtování, aktualizace stavu, číselné řady a chování.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 99dbe17d4e83c2c75d52ca3fd22a1772d8045355
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871971"
---
# <a name="landed-cost-parameters-setup"></a>Nastavení parametrů nákladů za doručení

[!include [banner](../../includes/banner.md)]

Stránka **Parametry nákladů za doručení** se používá k nastavení obecných informací a nastavení konfigurace, které se používají v modulu **Náklady za doručení** pro účtování, aktualizace stavu, číselné řady a chování. Nastavení parametrů je sdíleno mezi právnickými osobami a může být upraveno správcem.

## <a name="open-the-landed-cost-parameters-page"></a>Otevření stránka Parametry nákladů za doručení

Chcete-li pracovat s parametry, přejděte na **Náklady za doručení \> Nastavení \> Parametry nákladů za doručení** a poté nastavte pole podle popisu v následujících podsekcích.

![Stránka Parametry nákladů za doručení.](media/landed-cost-parameters.png "Stránka Parametry nákladů za doručení")

## <a name="general-tab"></a>Karta Obecné

### <a name="general-fasttab"></a>Záložka s náhledem Obecné

Následující tabulka popisuje pole, která jsou k dispozici na záložce **Obecné** karty **Obecné** na stránce **Parametry nákladů za doručení**.

| Nastavení | popis |
|---|---|
| Použijte přepravní sazbu | Sazba za přepravu je stanovena na definované období a používá se u odhadovaných nákladů na zboží, které používají více měn. Tuto možnost nastavte na *Ano*, chcete-li použít sazbu za přepravu. |
| Typ směnného kurzu | Výchozí kolekce směnných kurzů, která se používá pro výpočty s více měnami u cesty a nákladů na cestu. |
| Aktualizovat množství nákupní objednávky | Vyberte, co se stane, když uživatel změní množství na řádku nákupní objednávky:<ul><li>**Přijmout** – Množství cesty se automaticky upraví.</li><li>**Varování** – Pokud je řádek připojen k cestě, zobrazí se varování, ale množství cesty se aktualizuje.</li><li>**Chyba** – Pokud je řádek připojen k cestě, zobrazí se chybová zpráva a nákupní objednávku nelze aktualizovat. Řádek objednávky proto musí být z cesty nejprve odstraněn.</li></ul> |
| Automaticky aktualizovat počet kartonů | Když je tato možnost nastavena na *Ano*, jsou všechny kartony spojeny dohromady a zobrazeny na úrovních cesty a kontejneru. Když je nastaven na *Ne*, je počet kartonů zpočátku nastaven na 0 (nula) a lze ho podle potřeby ručně upravit. |

### <a name="costing-fasttab"></a>Záložka Ocenění

Následující tabulka popisuje pole, která jsou k dispozici na záložce **Ocenění** karty **Obecné** na stránce **Parametry nákladů za doručení**.

| Nastavení | popis |
|---|---|
| Účetní specifikace | Vyberte hodnotu úpravy v hlavní knize:<ul><li>**Celkem** - Celkový údaj se zaúčtuje do hlavní knihy.</li><li>**Skupina položek** – Úprava je určena za každou skupinu položek.</li><li>**Počet položek** – Úprava je určena za každou položku. Tato hodnota poskytuje nejvíce podrobností.</li></ul> |
| Povolit nulové náklady | Tuto možnost nastavte na *Ne*, aby se zobrazila chyba, pokud se uživatel pokusí zaúčtovat odhad nákladů u faktury za cestu nebo nákupní objednávky, která neobsahuje hodnotu očekávaných nákladů na cestu. Chybová zpráva uvádí, že náklady 0 (nula) nelze přidělit a zaúčtování faktury se nezdaří. V takovém případě může uživatel ručně aktualizovat odhad (nebo překonfigurovat automatické náklady) a poté buď načíst aktualizovanou hodnotu, nebo odstranit náklad, pokud se nepoužije.<p>Tuto možnost nastavte na *Ano*, aby cesta mohla mít prázdné náklady. V tomto případě bude cena 0 (nula) přidělena podle oblasti nákladů. Po přijetí cesty může být faktura s náklady dodavatele zpracována oproti nákladům s nulovou cenou.</p><p>Doporučujeme konfigurovat odhad v záznamu automatických nákladů, aby se zabránilo zobrazování nákladů s nulovou cenou. Ačkoli tento odhad není úplně přesný, měl by být stále přesnější než předpokládané nulové náklady.</p> |
| Datum zaúčtování úpravy | Když zaúčtujete závazkovou fakturu za náklady na cestu, aktualizuje se také tabulka vyrovnání (úpravy zásob). Vyberte datum, které je ve výchozím nastavení nastaveno na stránce **Vybrat náklady na cestu**, když jste v deníku faktur:<ul><li>**Datum transakce** – Použije se datum deníku (datum zaúčtování).</li><li>**Datum faktury nákupní objednávky** - Použije se datum finančního zaúčtování skladové faktury (nákupní objednávky).</li><li>**Vybrané datum** - Uživatel může určit datum zaúčtování. I když lze datum ponechat prázdné, pokud je při zaúčtování nákladové faktury stále prázdné, zobrazí se uživateli chyba.</li></ul> |
| Použít doklad nákupní faktury | Když je tato možnost nastavena na *Ano*, transakce časového rozlišení budou používat stejné číslo dokladu, které se používá pro nákupní fakturu. Když je nastavena na *Ne*, systém použije další dostupné číslo ze sekvence čísel **Doklad časového rozlišení nákladů**, která je nastavena na kartě **Číselné řady** stránky **Parametry nákladů za doručení**.<p>Tato možnost účinkuje, pouze když je možnost **Zaúčtovat na účet poplatků v hlavní knize** nastavena na *Ano* na kartě **Faktura** stránky **Parametry závazků**.</p> |
| Blokovat ruční zaúčtování na clearingový účet | Tuto možnost nastavte na *Ano*, když chcete zabránit zaúčtování na clearingové účty, kde transakce nebyla spojena s cestou výběrem možnosti **Funkce \> Vybrat náklady na cestu** v podokně akcí deníku faktur dodavatele. Doporučujeme nastavit tuto možnost na *Ano*, aby bylo možné správně vypořádat cestu a clearingový účet. |
| Použít účet časového rozlišení poplatků typu nákladů | Když je tato možnost nastavena na *Ano*, použije se účet časového rozlišení, který je konfigurován pro příslušný kód typu nákladů na stránce **Kódy typů nákladů** ke shromáždění nákladů jako výdajů.<p>Tato možnost účinkuje, pouze když je možnost **Zaúčtovat na účet poplatků v hlavní knize** nastavena na *Ano* na kartě **Faktura** stránky **Parametry závazků**. |
| Zaúčtovat úpravy jako odchylku | Když je tato možnost nastavena na *Ano*, přepíše standardní funkčnost a vynutí zaúčtování transakcí úprav zásob, které souvisejí s odchylkami mezi odhadovanými náklady a skutečnými náklady, na účet odchylky.<p>Když je tato možnost nastavena na *Ne*, transakce úprav zásob, které souvisejí s odchylkami, jsou zpracovány na základě konfigurace metody kalkulace nákladů a kódu typu nákladů. U standardních nákladů budou odchylky stále účtovány na účet odchylek. U klouzavého váženého průměru (WMA) se odchylky zaúčtují buď na účet odchylek, nebo do zásob.</p><p>Tato možnost účinkuje, pouze když je možnost **Zaúčtovat na účet poplatků v hlavní knize** nastavena na *Ano* na kartě **Faktura** stránky **Parametry závazků**.</p> |

### <a name="validation-fasttab"></a>Záložka Ověření

Následující tabulka popisuje pole, která jsou k dispozici na záložce **Ověření** karty **Obecné** na stránce **Parametry nákladů za doručení**.

| Nastavení | popis |
|---|---|
| Více nákladových faktur | Vyberte, co se stane, pokud je za cestu, folio nebo kontejner zpracována více než jedna faktura pro stejný vedlejší poplatek.<ul><li>**Přijmout** – Systém by měl povolit více nákladových faktur.</li><li>**Varování** – Zobrazí se varování.</li><li>**Chyba** – Zobrazí se chybová zpráva.</li></ul> |
| Více dodavatelů na folio | Vyberte, co se stane, pokud je do folia přidáno více než jedna nákupní objednávka dodavatele.<ul><li>**Přijmout** - Systém by měl akci umožnit.</li><li>**Varování** – Zobrazí se varování, ale akci lze přesto provést.</li><li>**Chyba** – Zobrazí se chybová zpráva a akce se neprovede.</li></ul><p>Konkrétní hodnotu pro toto pole může požadovat váš celní makléř nebo místní zákony.</p> |
| Tolerance více režimů doručení | Vyberte, co se stane, pokud se k této cestě přidá zboží z nákupní objednávky, které používá jiný způsob doručení než cesta.<ul><li>**Přijmout** - Systém by měl akci umožnit.</li><li>**Varování** – Zobrazí se varování, ale akci lze přesto provést.</li><li>**Chyba** – Zobrazí se chybová zpráva a akce se neprovede.</li></ul> |
| Tolerance více skladů | Vyberte, co se stane, pokud cesta obsahuje několik řádků objednávky, které je třeba doručit do různých skladů. Tyto řádky objednávek mohou být rozloženy do jedné nebo více nákupních objednávek.<ul><li>**Přijmout** - Systém by měl akci umožnit.</li><li>**Varování** – Zobrazí se varování.</li><li>**Chyba** – Zobrazí se chybová zpráva.</li></ul> |
| Chybějící objem | Vyberte, co se stane, když uživatel přidá do cesty položku bez objemu.<ul><li>**Přijmout** - Systém by měl položku přijmout.</li><li>**Varování** – Zobrazí se varování.</li><li>**Chyba** – Zobrazí se chybová zpráva.</li></ul><p>Pokud se k výpočtu a rozdělení nákladů používají objemy, doporučujeme vybrat buď *Varování* nebo *Chyba*.</p> |
| Poskytovatel služeb bez nákladů na cestu | Vyberte, co se stane, když se uživatel pokusí zpracovat fakturu pro poskytovatele služeb, který nebyl propojen s cestou. <ul><li>**Přijmout** - Systém by měl akci umožnit.</li><li>**Varování** – Zobrazí se varování.</li><li>**Chyba** – Zobrazí se chybová zpráva.</li></ul><p>Doporučujeme vybrat *Varování*.</p> |

### <a name="defaults-fasttab"></a>Záložka Výchozí

Následující tabulka popisuje pole, která jsou k dispozici na záložce **Výchozí** karty **Obecné** na stránce **Parametry nákladů za doručení**.

| Nastavení | popis |
|---|---|
| Název deníku | Vyberte výchozí deník, který má používat funkce *Vytvořit deník doručení*. |
| Stav cesty | Vyberte stav, který musí cesta mít, než si pro ni uživatelé mohou v systému nastavit nájemní přepravní kontejner. K této akci obvykle dochází, když je zboží v tranzitu nebo v překladišti. |
| Šablona cesty | Vyberte výchozí šablonu cesty, kterou chcete použít pro nové nájemní přepravní kontejnery. Obvykle vyberete šablonu cesty, která zahrnuje náklady na pronájem. |
| Přesun | Pokud je nadměrné / nedostatečné množství pro dodávku v rámci definované tolerance, bude automaticky zpracován deník pohybu. Vyberte výchozí deník pohybu, který chcete použít. Pole **Protiúčet** pro vybraný název deníku pohybu musí mít hodnotu. |
| Převod | Když je zpracována nedostatečná dodávka, množství nedostačujícího příjmu bude převedeno do skladu pro nedostatečné dodávky. Vyberte výchozí deník převodu, který chcete použít. |
| Zakázat nákupní objednávky bez cesty | U nákupních objednávek, které nejsou spojeny s cestou, vypněte funkci nákladů za doručení pro nadměrné a nedostatečné dodávky. |
| Zakázat nákupní objednávky zboží, které není v tranzitu | U nákupních objednávek, které nepoužívají funkci přepravovaného zboží, vypněte funkci nákladů za doručení pro nadměrné a nedostatečné dodávky. |
| Období odkladu nadměrného příjmu přepravovaného zboží | Určete počet dní po prvním přijetí přepravního kontejneru, aby bylo možné u tohoto přepravního kontejneru ještě dokončit další nadměrné příjmy. |

## <a name="status-updates-tab"></a>Karta aktualizací stavu

Systém používá hodnoty stavu k označení stavu každé cesty. Hodnoty stavu cesty lze automaticky použít na cesty prostřednictvím sledování cesty nebo periodických dávkových úloh. Případně je můžete použít ručně otevřením cesty a následným výběrem stavu ve skupině **Aktualizace cesty** na kartě **Spravovat** v podokně akcí. 

Můžete vytvořit tolik hodnost stavu cesty, kolik chcete. Čtyři z nich však musí být definovány tak, jak jsou použity pro zvláštní účely na kartě **Aktualizace stavu** stránky **Parametry nákladů za doručení**. V následující tabulce jsou popsána pole, která jsou zde k dispozici.

| Nastavení | popis |
|---|---|
| Nacenění nákladů | Vyberte stav cesty, který označuje, že cesta byla dokončena. |
| Na cestě | Vyberte stav cesty, který označuje, že cesta probíhá. |
| Připraveno k výpočtu nákladů | Vyberte stav cesty, který označuje, že cesta je připravena ke kalkulaci nákladů. Tento stav se používá, když byly pro cestu zpracovány všechny faktury za nákup zboží a faktury za náklady na cestu, kde je pole **Kredit u nákladů na cestu** nastaveno na *Dodavatel*. Cesty, které selžou v procesu ocenění, budou mít stav *Připraveno ke kalkulaci nákladů*.|
| Předběžně vypočítané náklady | Vyberte stav cesty, který označuje, že cesta je připravena k předběžné kalkulaci nákladů. Tento stav se používá, když se do cesty přidá nová nákladová transakce poté, co již byla oceněna. Nové nákladové transakce mohou být přičteny k dříve oceněné cestě, když je přijata druhá faktura za dopravné nebo neočekávaný poplatek za zdržení. Tento stav se automaticky použije, když je k oceněné cestě přidán nový náklad cesty. |

## <a name="voyage-creator-tab"></a>Karta tvůrce cesty

Následující tabulka popisuje oddíly na kartě **Tvůrce cesty** ve stránce **Parametry nákladů za doručení**.

| Sekce | popis |
|---|---|
| Tolerance | Pole **Tolerance vnějšího objemu** a **Tolerance vnější hmotnosti** definují mezní hodnoty, nad kterými se zboží považuje za nadměrné a s nadváhou. Když uživatel přidá zboží na stránce **Editor cesty**, systém zobrazí varování, pokud objem nebo hmotnost přesáhne hodnotu, kterou zde nastavíte. Hodnota každého pole je vyjádřena jako procento maximálního objemu nebo hmotnosti, které jsou nastaveny pro příslušný typ přepravního kontejneru. Doporučujeme, aby hodnota byla mezi 5 a 10 procenty maximálního objemu nebo hmotnosti. |
| Nastavení vytváření folia | Systém může během procesu vytváření cesty vytvořit více folií. V této části můžete definovat, kdy má být vytvořeno nové folio. U každého řádku v této části systém zkontroluje zadanou tabulku a pole a vytvoří folio pro každou jedinečnou hodnotu pole. |

## <a name="cost-estimates-tab"></a>Karta Odhady nákladů

Karta **Odhady nákladů** ve stránce **Parametry nákladů za doručení** obsahuje pouze jedno pole: **Výchozí verze kalkulace**. Toto pole se použije pouze v případě, kdy je použita metoda kalkulace *Standardní výpočet nákladů*. Vyberte výchozí verzi kalkulace, kterou chcete použít pro periodický úkol *Aktualizace nákladové ceny položky*. Možná budete muset toto nastavení změnit pokaždé, když začne nový finanční rok.

## <a name="inventory-dimensions-tab"></a>Karta Dimenze zásob

Kartu **Dimenze zásob** na stránce **Parametry nákladů za doručení** používejte k určení toho, které dostupné dimenze zásob by se měly ve výchozím nastavení zobrazovat na všech stránkách nákladů za doručení, kde se používají dimenze.

Vyberte dimenzi a poté nastavte možnost **Řádky cesty**, **Přepravované zboží** anebo **Odhady nákladů** na *Ano* pro každou stránku, kde by měla být tato dimenze ve výchozím nastavení zobrazena. Podle potřeby tento krok opakujte pro další dimenze.

Nastavení na této kartě stanoví výchozí dimenze pro každou určenou stránku napříč právnickými osobami. Uživatelé, kteří pracují na jedné z určených stránek, však mohou přepsat výchozí dimenze výběrem možnosti **Zásoby \> Zobrazit dimenze** v podokně akcí.

## <a name="number-sequences-tab"></a>Karta Číselné řady

Karta **Číselné řady** na stránce **Parametry nákladů za doručení** uvádí každý typ posloupnosti referenčních čísel, který modul Náklady za doručení vyžaduje, ale který není sdílen mezi právnickými osobami. U každé reference v seznamu vyberte kód číselné řady.

> [!NOTE]
> V konfiguraci s více společnostmi musí být pro každou společnost (právnickou osobu) vytvořeny různé číselné řady.

## <a name="shared-number-sequences-tab"></a>Karta Sdílené číselné řady

Karta **Sdílené číselné řady** na stránce **Parametry nákladů za doručení** uvádí každý typ posloupnosti referenčních čísel, který je sdílen mezi právnickými osobami v modulu Náklady za doručení. Aktuálně je v seznamu pouze jedna číselná sekvence. Tato číselná řada se používá pro ID cesty.

Na stránce **Všechny cesty** mohou uživatelé zobrazit všechny cesty napříč všemi právnickými osobami. Chcete-li však upravit a zpracovat cestu, musí být uživatelé v právnické osobě vybraného záznamu.

## <a name="feature-visibility-tab"></a>Karta viditelnosti prvku

Náklady za doručení přidávají prvky (pole a funkce) do několika často používaných stránek v Microsoftu Dynamics 365 Supply Chain Management. Tyto stránky obsahují stránky, které souvisejí s hlavními daty dodavatele, vydanými produkty, nákupními objednávkami, převodními příkazy a nastavením skladu. Pokud používáte modul Náklady za doručení, musíte tyto funkce zviditelnit všude, než je budete moci používat. Pokud nepoužíváte náklady za doručení, můžete funkce skrýt, abyste je nebylo možné používat.

Na kartě **Viditelnost prvku** na stránce **Parametry nákladů za doručení** nastavte možnost **Aktivovat** na *Ano*, aby funkce nákladů za doručení byly viditelné všude tam, kde jsou k dispozici. Nastavením této možnosti na *Ne* skryjete funkce na běžných stránkách mimo modul Náklady za doručení. I když je však tato možnost nastavena na *Ne*, samotný modul, včetně stránky **Parametry nákladů za doručení**, zůstane k dispozici uživatelům, kteří mají správná oprávnění k přístupu.
