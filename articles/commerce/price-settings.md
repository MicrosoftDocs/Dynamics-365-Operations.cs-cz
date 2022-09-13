---
title: Nastavení cen
description: Tento článek popisuje různá nastavení pro správu cen a slev v Microsoft Dynamics 365 Commerce headquarters.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-11
ms.openlocfilehash: 4bc8cb16e7960d26adbb9590b4ad83cf46b02838
ms.sourcegitcommit: 6fd44fc6e9a7bad197cab58c36ec25a555724cf1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410762"
---
# <a name="pricing-settings"></a>Nastavení cen

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Tento článek popisuje různá nastavení pro správu cen a slev v Microsoft Dynamics 365 Commerce headquarters. Tato nastavení umožňují organizacím definovat cenové chování v jejich řešení Commerce tak, aby vyhovovalo specifickým obchodním potřebám.

## <a name="company-level-pricing-settings"></a>Nastavení cen na úrovni společnosti

Většina nastavení cen je na úrovni společnosti a lze je nalézt v části **Parametry Commerce \> Ceny a slevy** v Commerce headquarters.

### <a name="best-price-and-compound-concurrency-control-model"></a>Model řízení souběžnosti nejlepší ceny a složené slevy

Nastavení **Model řízení souběžnosti Nejlepší cena a složené** určuje, jak cenový modul zpracovává více slev v režimu souběžnosti **nejlepší cena** nebo **složené**. 

Pokud je parametr nastaven na **Nejlepší cena a složené v rámci priority, nikdy složená napříč prioritami**, všechny **složené** slevy, které mají stejnou cenovou prioritu, se sčítají. Složený výsledek pak soutěží s libovolnými slevami **nejlepší ceny**, které mají stejnou cenovou prioritu, je použita nejlepší cena a všechny slevy, které mají nižší prioritu, jsou ignorovány.

Pokud je parametr nastaven na **Nejlepší cena pouze v rámci priority, vždy složená napříč prioritami**, se všemi **složenými** slevami se zachází jako se slevou **nejlepší ceny**. V rámci cenové priority vyhrává pouze jedna sleva. Pokud je tato jediná sleva **nejlepší cena** nebo **složená** sleva, je složena se všemi dalšími slevami **nejlepší cena** nebo **složenými** slevami, které mají nižší cenovou prioritu.

### <a name="discount-compound-behavior"></a>Chování složené slevy

Nastavení **Chování skládání slev** určuje, jak cenový modul vypočítá více složených slev.

Pokud je parametr nastaven na **Složený**, jedna sleva se uplatňuje na druhou kumulativně. Pokud je nastaveno na **Složená z původní ceny**, jsou všechny slevy řešeny nezávisle na sobě a uplatňovány na stejnou původní cenu.

Chcete například sloučit 10procentní a 20procentní slevu na produkt, který má původní cenu $100. Pokud nastavíte parametr **Chování skládání cen** na **Složená**, konečná cena bude 72 $ (100 $ &times; 90 % &times; 80 %). Pokud nastavíte **Skládání na původní cenu**, konečná cena bude 70 $ (100 $ − 10 % − 20 %).

### <a name="enable-competition-between-exclusive-threshold-and-other-periodic-discounts"></a>Povolit konkurenci mezi exkluzivními mezními a jinými pravidelnými slevami

Pokud je parametr **Povolit konkurenci mezi exkluzivními mezními a jinými pravidelnými slevami** nastaven na **Ano**, cenový modul umožňuje exkluzivní mezní slevy konkurovat exkluzivním nemezním slevám. Stále platí priorita cen. Chování mezních slev **nejlepší cena** a **složená** sleva zůstává zachováno. Jinými slovy, nesoutěží s nemezními slevami.

### <a name="manual-line-discount-and-system-discount"></a>Ruční řádková sleva a systémová sleva

Nastavení **Manuální řádková sleva a systémová sleva** určuje, jak cenový modul aplikuje ruční slevu na řádku a systémovou slevu na stejný řádek. Manuální řádková sleva může být připočtena k systémové slevě nebo může nahradit systémovou slevu. Když se složí ruční řádková sleva a systémová sleva, logika výpočtu respektuje nastavení **Chování skládání cen**. Ruční celková sleva, která se vztahuje na celou objednávku, toto nastavení nerespektuje.

### <a name="keep-items-on-the-same-sales-line-for-discount-price-rounding"></a>Ponechat položky na stejném řádku prodeje pro zaokrouhlení zlevněné ceny

Částku množstevní slevy někdy nelze rovnoměrně vydělit kvalifikačním množstvím (například pokud je částka slevy $10 pro tři zakoupené jednotky). V těchto případech nastavení **Zachovávat položky na stejném prodejním řádku pro zaokrouhlení slevových cen** určuje, jak cenový modul použije a rozdělí částku slevy. Pokud je parametr nastaven na **Ano**, částka slevy se použije jako celek a nerozděluje se. Pokud je nastaveno na **Ne**, částka slevy se rozdělí mezi způsobilé množství a zaokrouhlí se. Například částka slevy $10 pro tři jednotky je rozdělena na $3,33 pro jednu jednotku, $3,33 pro druhou jednotku a $3,34 pro třetí jednotku.

### <a name="apply-discounts-to-key-in-price-products"></a>Uplatnit slevy pro produkty se zadáním ceny

Nastavení **Uplatnit slevy na produkty s ručně zadanou cenou** určuje, zda lze slevy uplatnit společně s „ručně zadanými cenami“, které jsou zadány v pokladním místě (POS). Nastavení **Ručně zadaná cena** v konfiguraci produktu určuje, zda a jak produkt podporuje zadanou cenu.

### <a name="apply-discounts-to-price-overrides"></a>Uplatnit slevy pro přepsání ceny

Nastavení **Použít slevy na přepisy cen** určuje, zda lze slevy uplatnit společně s přepsáním cen.

### <a name="distribute-discounts-for-least-expensive-discounts"></a>Distribuovat slevy pro nejlevnější slevy

U kombinovaných slev, které používají typ výpočtu „nejlevnější“, nastavení **Distribuovat slevy pro nejlevnější slevy** určuje, zda cenový modul rozděluje slevu mezi řádky.

Pokud je parametr nastaven na **Ne**, sleva se vztahuje pouze na nejlevnější řádky. Například při slevě na kombinaci „koupit 2 a získat 1 zdarma“ bude nejlevnější položka zdarma a další dvě položky zůstanou za plnou cenu. V tomto případě zákazník, který vrátí obě položky za plnou cenu, získá třetí položku stále zdarma. Tento scénář může maloobchodníkovi způsobit ztrátu.

Pokud je parametr nastaven na **Ano**, cenový nástroj rozdělí slevu na všechny příslušné řádky. Toto nastavení může pomoci snížit ztrátu při vrácení.

### <a name="manually-calculate-multi-line-prices-and-discounts"></a>Ručně vypočítat víceřádkové ceny a slevy

Nastavení **Ručně vypočítat víceřádkové ceny a slevy** řídí, zda cenový modul používá zpožděný výpočet ceny a slevy pro aplikaci POS a kanál call centra. Pokud je parametr nastaven na **Ano**, cenový modul okamžitě nevypočítá víceřádkové slevy (jako jsou množstevní slevy, prahové slevy a smíšené slevy), kdykoli se vytvoří nebo upraví prodejní objednávka v aplikaci POS nebo v kanálu call centra.

> [!NOTE]
> Ve verzi Commerce 10.0.30 a starší nastavení **Ručně vypočítat víceřádkové ceny a slevy** ovládá pouze kanál call centra. Oddělené nastavení **Ručně vypočítat slevy na více položek** v profilu funkčnosti řídí chování výpočtu ceny v aplikaci POS. Ve verzi Commerce 10.0.31 jsou tato dvě nastavení sloučena do jednoho nastavení na úrovni společnosti.

### <a name="retention-period-in-days"></a>Období zadržení ve dnech

Nastavení **Doba uchování ve dnech** nastavení udává, za kolik dní po datu vypršení platnosti (pokud je nastaveno datum vypršení platnosti) nebo po datu deaktivace (pokud datum vypršení platnosti není nastaveno), by měla být sleva systematicky mazána. Pokud je parametr nastaven na **0** (nula), nedojde k automatickému smazání.

> [!NOTE]
> Ve verzi Commerce 10.0.30 a dřívější je toto nastavení pojmenováno **Počet dní, po kterých mají být smazány slevy, jejichž platnost vypršela**.

### <a name="coupon-bar-code"></a>Čárový kód kupónu

Nastavení **Čárový kód kupónu** určuje, který konkrétní čárový kód se použije ke generování čárových kódů kupónů. Uživatelé si mohou vybrat jeden z předdefinovaných čárových kódů, které jsou nakonfigurovány na stránce **Nastavení čárového kódu**. Další informace o čárových kódech a maskách čárových kódů viz [Nastavení čárových kódů](set-up-bar-codes.md) a [Nastavení masky čárových kódů](set-up-bar-code-masks.md).

### <a name="coupon-code-must-be-manually-applied-to-return-transactions"></a>Kód kupónu musí být použit na transakce vrácení ručně

Nastavení **Pro vrácení transakcí je nutné použít kód kupónu ručně** se vztahuje pouze na transakce vrácení, pro které není poskytnuta účtenka. Nastavte parametr na **Ne**, pokud mají být na transakci automaticky použity kódy kuponů. Nastavte na **Ano**, pokud je nutné k transakci ručně přidat kódy kuponů.

### <a name="use-sales-agreements-set-up-for-the-organization"></a>Použít prodejní smlouvy nastavené pro organizaci

U objednávek business-to-business (B2B), pokud parametr **Použít prodejní smlouvy nastavené pro organizaci** je nastaven na **Ano**, cenový nástroj používá prodejní smlouvy, které jsou pro organizaci definovány v hierarchii zákazníků uživatele, aby určil cenu na základě smlouvy. Pokud je parametr nastaven na **Ne** nebo pokud není hierarchie zákazníků definována, cenový modul hledá prodejní smlouvy, které jsou definovány pro uživatele, aby určil cenu na základě smlouvy. Další informace o zákaznických hierarchiích pro elektronické obchodování B2B viz [Správa obchodních partnerů B2B pomocí zákaznických hierarchií](b2b/partners-customer-hierarchies.md).

## <a name="channel-level-pricing-settings"></a>Nastavení cen na úrovni kanálu

Následující nastavení umožňují organizacím řídit cenové chování v konkrétních prodejních kanálech.

### <a name="enable-order-price-control"></a>Povolit kontrolu ceny objednávky

Parametr **Povolit kontrolu ceny objednávky** se nachází na pevné záložce **Všeobecné** na stránce **Konfigurace call centra**. Nastavení určuje, zda cenový modul vynucuje omezení operace přepsání ceny v kanálu call centra. Funguje ve spojení s nastavením **Povolit úpravu ceny** na úrovni produktu.

Pokud je řízení ceny objednávek vypnuto, může kterýkoli uživatel call centra provádět změny cen na prodejních řádcích v kanálu call centra, bez ohledu na to, zda odpovídající produkty umožňují úpravu ceny.

Pokud je zapnutá kontrola ceny objednávky, pouze produkty, kde je parametr **Povolit úpravu ceny** nastaven na **Ano**, umožňují přepsání cen v prodejních objednávkách kanálu call centra a na odpovídajících prodejních řádcích musí být uveden kód důvodu. Uživatel call centra může změnit prodejní cenu pouze do výše hodnoty **Procento přirážky nákladů**, která je definována na v **Retail a Commerce \> Nastavení kanálu \> Nastavení call centra \> Přepsat oprávnění**. Pokud přepsání ceny překročí toto procento, musí uživatel odeslat požadavek, který je následně zpracován prostřednictvím předdefinovaného pracovního postupu Commerce ke kontrole a schválení. Další informace o pracovních postupech Commerce naleznete v tématu [Přehled systému workflow](/dynamics365/fin-ops-core/fin-ops/organization-administration/overview-workflow-system)

## <a name="product-level-pricing-settings"></a>Nastavení cen na úrovni produktu

Následující nastavení prosazují pravidla pro stanovování cen na úrovni produktu a lze je nalézt na stránce **Konfigurace produktu** organizace.

### <a name="allow-price-adjust"></a>Povolit úpravu ceny

Pokud je parametr **Povolit úpravu ceny** nastaven na **Ano**, lze u produktu v prodejních objednávkách kanálu call centra použít přepsání ceny.

### <a name="key-in-price"></a>Zadat cenu

Nastavení **Ručně zadaná cena** určuje, zda je zadaná cena povinná, když je produkt přidán do prodejní transakce v POS. Definuje také odpovídající omezení cenové hodnoty.

### <a name="zero-price-valid"></a>Nulová cena je platná

Nastavení **Nulová cena platí** určuje, zda předdefinované, systémem vypočítané nebo ručně upravené prodejní ceny pro produkt mohou být 0 (nula). Nastavte parametr na **Ano**, pokud je povolena cena nula. Toto nastavení lze také určit na úrovni kategorie z hierarchie produktu Commerce.

### <a name="prevent-all-discounts"></a>Nepovolit žádnou slevu

Nastavením parametru **Zabránit všem slevám** na **Ano** zabráníte uplatnění všech typů slev (včetně manuálních slev) na produkt. Toto nastavení lze také určit na úrovni kategorie z hierarchie produktu Commerce.

> [!NOTE]
> Toto nastavení neomezuje operaci přepisu ceny, protože se nastaví cena, se kterou se nenakládá jako se slevou.

### <a name="prevent-manual-discounts"></a>Nepovolit manuální slevy

Nastavením parametru **Zabránit ručním slevám** na **Ano** zabráníte uplatnění všech manuálních slev na řádku nebo transakci na produkt. Všechny ostatní slevy lze stále uplatnit. Toto nastavení lze také určit na úrovni kategorie z hierarchie produktu Commerce.

> [!NOTE]
> Toto nastavení neomezuje operaci přepisu ceny, protože se nastaví cena, se kterou se nenakládá jako se slevou.

### <a name="prevent-retail-discounts"></a>Nepovolit maloobchodní slevy

Pokud je parametr **Zabránit maloobchodním slevám** nastaven na **Ano**, **jednoduchá** sleva, **množstevní** sleva, **mezní** sleva, **kombinovaná** sleva a sleva **na dopravu** nelze uplatnit na produkt. Všechny ostatní slevy (včetně ručních slev) lze stále uplatnit.

### <a name="prevent-tender-based-discounts"></a>Nepovolit slevy založené na způsobu úhrady

Pokud je parametr **Zabránit slevám na základě způsobu úhrady** nastaven na **Ano**, slevu **na základě způsobu úhrady** na produkt nelze uplatnit. Všechny ostatní slevy (včetně ručních slev) lze stále uplatnit.

Maloobchodní prodejci často vylučují některé produkty, jako jsou nové položky nebo položky na vyžádání, ze slev na položku (jako jsou jednoduché slevy nebo množstevní slevy). Pokud však zákazník zaplatí používanou upřednostňovanou nabídkou, mohou stále chtít uplatnit slevu založenou na způsobu úhrady. Pro dosažení tohoto výsledku musí prodejci nastavit parametry **Zabránit všem slevám** a **Zabránit slevám založeným na způsobu úhrady** na **Ne** a parametry **Zabránit ručním slevám** a **Zabránit maloobchodním slevám** na **Ano**.

## <a name="deprecated-or-removed-settings"></a>Odstraněná nebo zastaralá nastavení

Následující nastavení cen byla odstraněna nebo se plánuje odstranění z Dynamics 365 Commerce.

| Nastavení | Důvod pro zastarání nebo odstranění | Stav zastarání nebo odstranění |
|---------|-----------------------------------|-------------------------------|
| Zpracování překrývajících se slev | Toto nastavení jsme poskytli v parametrech Commerce, abychom řídili, jak cenový nástroj vyhledává a určuje nejlepší kombinaci slev, která se má použít. Možnost **Nejlepší sleva** protlačí všechny možné kombinace slev během výpočtu ceny. Možnost **Nejlepší výkon** je optimalizovaná možnost, která používá heuristický algoritmus a metodu mezní hodnoty pořadí k včasnému určení priorit, vyhodnocení a stanovení nejlepší kombinace slev. Možnost **Vyvážený výpočet** v kódu možnost funguje stejně jako možnost **Nejlepší výkon**. Je to tedy v podstatě duplicitní možnost. Aby se zlepšil výkon, byl modul stanovení cen aktualizován tak, aby používal pouze možnost **Nejlepší výkon** jako standardní možnost. Proto toto nastavení již není použitelné. | Zastaralé ve verzi 10.0.21 a bude odstraněno v říjnu 2022. |
| Povolení úprav ceny pro zvýšení ceny produktu | Toto nastavení jsme poskytovali pro řízení, zda funkce úpravy ceny umožňuje zvýšit cenu produktu. Když je tento parametr vypnutý, mohou organizace při použití funkce úpravy ceny nastavit pouze jednotkovou cenu produktu nižší, než je jeho základní cena a prodejní cena podle obchodní smlouvy. Toto nastavení činíme zastaralým, protože funkce úpravy ceny byla aktualizována tak, aby podporovala obousměrné úpravy (zvýšení nebo snížení). | Zastaralé ve verzi 10.0.30 a bude odstraněno v říjnu 2023. |
| Povolit sestavu cen pro maloobchod | Toto nastavení jsme poskytovali, abychom mohli ovládat, zda je funkce **Hlášení cen** k dispozici pro použití na stránce konfigurace obchodu. Toto nastavení zastaráváme, protože stránce konfigurace obchodu byl aktualizována, aby vždy poskytovala funkci **Hlášení cen** jako standardní funkci. | Zastaralé ve verzi 10.0.31 a bude odstraněno v říjnu 2023. |
| Použijte dnešní datum pro vypočítání cen | Cenový modul Dynamics 365 Supply Chain Management podporuje výpočet ceny na základě požadovaného data expedice nebo požadovaného data příjmu spolu s dnešním datem. Cenový modul Commerce podporuje pouze výpočet cen na základě dnešního data. Pro zákazníky, kteří používají funkce Supply Chain Management i Commerce, jsme toto nastavení poskytli a zákazníkům doporučujeme, aby jej vždy nastavili na **Ano**, aby tyto dva cenové moduly mohly spolupracovat. Toto nastavení činíme zastaralým, protože zásadně nemění chování výpočtu, a je proto nadbytečné. | Zastaralé ve verzi 10.0.31 a bude odstraněno v říjnu 2023. |
| Maximální cena | Toto nastavení jsme poskytli v profilu funkčnosti, abychom mohli řídit, zda lze prostřednictvím POS v konkrétních obchodech prodávat pouze produkty, jejichž prodejní cena je nižší než stanovená maximální cena. Toto nastavení jsme ukončili z důvodu nízkého využití funkcí. | Zastaralé ve verzi 10.0.31 a bude odstraněno v říjnu 2023. |
| Uplatnit slevy pro jednotkovou cenu | Toto nastavení bylo určeno ke řízení, zda se ceny a slevy zaokrouhlují na úrovni jednotkové ceny nebo na úrovni prodejního řádku během výpočtu ceny. Zastarali jsme ji, protože se nepoužívá nikde v aktuálním kódu. | Zastaralé ve verzi 10.0.31 a bude odstraněno v říjnu 2023. |
| Ručně vypočítat slevy několika položek | Toto nastavení jsme poskytli za účelem řízení, zda cenový modul používá zpožděný výpočet ceny pro kanál maloobchodu. Pokud je parametr nastaven na **Ano**, cenový modul okamžitě nevypočítá víceřádkové slevy (jako jsou množstevní slevy, prahové slevy a smíšené slevy), kdykoli se vytvoří nebo upraví prodejní objednávka v aplikaci POS. Rozhodli jsme se toto nastavení sloučit s podobným nastavením v parametrech Commerce, abychom vytvořili omnikanálové řízení. | Zastaralé ve verzi 10.0.31 a bude odstraněno v říjnu 2023. |

Úplný seznam odstraněných nebo zastaralých funkcí v Dynamics 365 Commerce naleznete v článku [Odebrané nebo zastaralé funkce v Dynamics 365 Commerce](get-started/removed-deprecated-features-commerce.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
