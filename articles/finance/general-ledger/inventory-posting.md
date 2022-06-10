---
title: Zaúčtování zásob
description: Toto téma vysvětluje kartu Zaúčtování zásob na stránce Profil účtování zásob.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 464ffccd658003271b517038f430914fd5d8d50e
ms.sourcegitcommit: 6744cc2971047e3e568100eae338885104c38294
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/20/2022
ms.locfileid: "8783364"
---
# <a name="inventory-posting"></a>Zaúčtování zásob

Karta **Zásoby** na stránce **Profily zaúčtování zásob** se používá ke kontrole toho, jak se transakce zásob zaúčtují do hlavní knihy. Transakce zásob jsou transakce, které nejsou vytvořeny z prodejních objednávek, nákupních objednávek nebo výrobních zakázek. Automaticky současně zaúčtují fyzické a finanční aktualizace zásob. Jednou z výjimek jsou převodní příkazy, které oddělují fyzické a finanční aktualizace při odeslání a přijetí zásob.

V následující tabulce jsou uvedeny některé příklady transakcí zásob.

| Typ transakce | Příjem nebo výdej | Fyzické zaúčtování, finanční zaúčtování nebo obojí | Popis |
|---|---|---|---|
| Přesun | Oboje | Oboje | <p>Deník pohybů je deník zásob, který můžete použít k přidání nebo odebrání zásob. Funguje jako deník úprav zásob. Jedním z klíčových rozdílů je však to, že je zadán hlavní účet, který kompenzuje položku.</p><p>Do deníku pohybů se zapisují počáteční zůstatky a jednorázové úpravy, které musí být účtovány do výdajů. Používá se například při odebrání zásob pro prodejní vzorek.</p><p>Když je deník zaúčtován, fyzické a finanční aktualizace probíhají současně.</p><p>Kladná množství na řádcích deníku představují příjmy a záporná množství představují vydání.</p> |
| Úprava zásob | Oboje | Oboje | Deník úprav zásob se používá k přidávání nebo odebírání zásob. Nedovolí vám vybrat protiúčet. K aktualizaci položky hlavní knihy se používají pouze účty, které jsou uvedeny na stránce **Profil účtování zásob**. |
| Převod (deník) | Oboje | Oboje | <p>Deník převodů se používá k přesunu zásob z jednoho místa na druhé (pomocí dimenzí úložiště). Aktualizuje informace o produktu ve skladové transakci pomocí nových dimenzí produktu nebo sledování.</p><p>Deník převodu vytvoří jeden řádek pro pohyb položky. Tento řádek obsahuje pole „z“ a „do“ pro dimenze zásob. Každý řádek v deníku převodů vytváří dvě transakce zásob. Vytvoří se jedna transakce pro dimenze zásob „z“. Představuje výdej a má záporné množství. Druhá transakce je vytvořena pro dimenze zásob „do“. Představuje příjem a má kladné množství.</p><p>Deníky převodů nemusí vytvořit doklad, pokud je pohyb zásob považován za nefinanční převod. Dimenze zásob, které se liší pro hodnoty „z“ a „do“, nejsou označeny možností **Finanční zásoby** ve stránce **Skupina dimenzí úložiště** nebo **Skupina dimenzí sledování**. Například, pokud není zapnuta možnost **Finanční zásoby** u dimenze **Umístění** a přesunete zásoby z jednoho místa na jiné místo ve stejném pracovišti a skladu, nevytvoří se žádný doklad.</p><p>Deníky převodu se od převodních příkazů liší tím, že pro pohyb neexistují žádné doklady. Aktualizace se provádí v jedné transakci zaúčtováním deníku. Naproti tomu převodní příkaz může generovat doklady vyskladnění a odeslání a vyžaduje ke zpracování transakce dvě aktualizace.</p> |
| Dodávka převodního příkazu | Problém | Oboje | <p>Když vytvoříte nový převodní příkaz, každá kombinace řádku a dimenze zásob má dvě transakce zásob: jednu pro zásilku převodního příkazu a jednu pro příjem převodního příkazu. Když odešlete převodní příkaz, aktualizují se dvě transakce zásob a vytvoří se dvě další transakce zásob pro tranzit zboží, celkem tedy čtyři transakce zásob.</p><ol><li>První transakce zásob se používá k odebrání položky ze zdrojového skladu a umístění. Stav výdeje této transakce je **Prodáno** a vyjadřuje tak, že položka již není k dispozici ve skladu.</li><li>Druhá transakce zásob se používá k přidání položky do tranzitního skladu, který je vybrán pro sklad, ze kterého se zboží převádí. Stav příjmu této transakce je **Zakoupeno**.</li><li>Třetí transakce zásob slouží k přesunu z tranzitního skladu do cílového skladu. Stav výdeje této transakce je **Rezervované – fyzicky**. Tento stav zajišťuje, že položka nemůže být spotřebována jiným procesem, dokud je stále na cestě.</li><li>Čtvrtá transakce zásob slouží pro příjem zboží do cílového skladu. Stav příjmu této transakce je **Objednáno**.</li></ol> |
| Příjem převodního příkazu | Příjemka | Oboje | Když je převodní příkaz přijat v cílovém skladu, stav zásob transakce zásob, která je v tranzitním skladu (číslo 3 v předchozím příkladu), se aktualizuje na **Prodáno** a stav zásob transakce zásob pro cílový sklad se aktualizuje na **Zakoupeno**. |
| Kusovník | Oboje | Oboje | K vykazování produktu jako hotového a spotřebování surovin, které byly spotřebovány během procesu, můžete použít deník kusovníku, aniž byste použili výrobní zakázku. Deník kusovníku obvykle obsahuje alespoň jeden kladný řádek pro hotové zboží a jeden nebo více záporných řádků pro suroviny, které se spotřebovávají. Řádek hotového zboží je příjem do zásoby, zatímco záporné řádky jsou výdeje surovin ze zásob. Když vytvoříte deník kusovníku, první řádek je záhlaví kusovníku a další přidané řádky jsou řádky kusovníku. |
| Změna vlastnictví zásob | Oboje | Oboje | Deník změn vlastnictví zásob se používá ke změně vlastnictví zasílaných zásob z dodavatele na vaši organizaci. Deníky změn vlastnictví zásob se podobají deníkům převodu zásob v tom, že dvě transakce zásob souvisejí s každou kombinací řádku a dimenze zásob. Jedna transakce zásob odebere zásoby od dodavatele v dimenzi **Vlastnictví** a druhý přidá položku k právnické osobě v dimenzi **Vlastnictví**. |
| Doručení položky | Příjemka | Fyzické | Deník příjmu položek se používá k aktualizaci stavu příjmu zásob na **Registrováno**. Obvykle se používá pro příjem zboží nákupní objednávky a vratky prodejní objednávky. |
| Výrobní vstup | Příjemka | Fyzické | Deník výrobních vstupů se podobá deníku příchodů položek. Výrobní vstup slouží k příjmu hotového zboží z výrobní zakázky na sklad. Po zaúčtování deníku se stav transakce zásob aktualizuje na **Registrováno**. |
| Inventura | Oboje | Oboje | Deník inventur se používá k zaznamenání množství položek, které byly spočítány pro konkrétní kombinaci dimenzí zásob. Transakce zásob se vytvoří, když řádek deníku obsahuje rozdíl v inventuře. Řádek, který má vyšší spočítané množství, způsobí příjem do zásob. Řádek, který má nižší spočítané množství, způsobí výdej ze zásob. Řádky, kde se spočítané množství shoduje s očekávaným množstvím, nemají žádné transakce zásob. |
| Inventura podle štítků | Nelze použít | Nelze použít | Deník inventur podle štítků se používá ke sledování štítků zásob, které jsou přiřazeny a používány v úplném počtu zásob. Deník můžete použít k přiřazení čísla štítku ke konkrétní kombinaci položky a dimenze zásob a ke sledování stavu tohoto štítku během úplné inventury. Deníky inventur podle štítků nevytvářejí transakce zásob. |
| Objednávky kvality | Problém | Fyzické | <p>Objednávka kvality se používá k zaznamenání výsledků testů pro danou šarži v inventáři. Každá objednávka kvality souvisí s existující transakcí zásob nebo částí transakce zásob.</p><p>Objednávka kvality vygeneruje novou transakci zásob ve dvou situacích:</p><ul><li>Objednávka kvality je označena jako **Destruktivní test** na kartě **Všeobecné**.</li><li>Objednávka kvality je označena jako **Karanténa při nezdařeném ověření** na kartě **Všeobecné** a test neprojde ověřením. V tomto případě jsou vytvořeny dvě transakce zásob. Jedna transakce zásob odebere položku z původní kombinace dimenzí zásob a umístění a druhá přidá položku do karanténního skladu.</li></ul> |
| Karanténní příkazy | Oboje | Oboje | <p>Transakce zásob karanténních příkazů jsou jako převodní příkaz. Karanténní sklad se používá ke sledování zásob. Existují dvě transakce příjmu a dvě transakce výdeje.</p><p>Při prvním vytvoření objednávky se vytvoří dvě transakce. Transakce příjmu má stav **Objednáno** u karanténního skladu, který je propojen se skladem, kde se položka nachází. Transakce výdeje má stav **Na objednávce** u skladu, kde je položka uložena.</p><p>Když spustíte karanténní příkaz, vytvoří se dvě další transakce a existující transakce se aktualizují. Stav transakce příjmu pro karanténní sklad je aktualizován na **Přijato** a stav transakce výdeje pro sklad úložiště se aktualizuje na **Odečteno**.</p><p>Dvě nové transakce se použijí k označení případného přesunu zpět do skladu. Transakce příjmu má stav **Objednáno** pro úložný sklad a tato transakce výdeje má stav **Rezervované – fyzicky** pro karanténní sklad.</p><p>Když nahlásíte karanténní příkaz jako dokončený, tato operace představuje fyzickou aktualizaci karanténního příkazu. Stav příjmu ve skladu se aktualizuje na **Přijato**.</p><p>Když ukončíte karanténní příkaz, tato operace představuje finanční aktualizaci karanténního příkazu. Stav transakcí výdeje se aktualizuje na **Prodáno** a stav transakcí příjmu se aktualizuje na **Zakoupeno**.</p><p>Případně můžete zrušit karanténní příkaz. Tato operace odebere položku ze zásob. Když zrušíte karanténní příkaz, zůstanou pouze tři transakce. Transakce příjmu pro sklad úložiště je odstraněna a stav zbývající transakce příjmu je aktualizován na **Zakoupeno**. Stav dvou transakcí výdeje je aktualizován na **Prodáno**. Tato operace je fyzickou a finanční aktualizací objednávky.</p> |

## <a name="fixed-receipt-price-posting"></a>Zaúčtování pevné ceny příjmu

Pevná cena příjmu vám umožňuje použít standardní cenu produktu. Je to alternativa k výběru možnosti **Standardní cena** na stránce **Skupina modelů položek** pro položku. Hlavním rozdílem při použití pevné ceny příjmu je to, že při zaúčtování příjmu do zásoby se pro položku použije nákladová cena, která je aktuálně nakonfigurována. Neexistuje žádný proces přecenění nákladů pro pevnou cenu příjmu. Při zaúčtování finanční aktualizace se použije aktuální nákladová cena v době zaúčtování. Pokud se nákladová cena použitá při příjmu a na faktuře liší, bude odchylka zaúčtována na účty zisků a ztrát s pevnou cenou příjmu.

Chcete-li volitelně použít u produktu pevnou cenu příjmu, musíte provést následující konfiguraci:

- Na stránce **Skupina modelů položek** pro položku vybranou na řádku transakce zásob musí být zaškrtnuto políčko **Zaúčtovat fyzické zásoby**.
- Zaškrtněte políčko **Pevná cena příjmu** na stránce **Skupina modelů položek**.
- Na stránce **Profil účtování zásob** zadejte hlavní účty pro následující typy účtování:

    - Zisk pevné ceny příjmu
    - Ztráta pevné ceny příjmu

Další informace naleznete v tématu [Pevná cena příjmu](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="catch-weight-posting"></a>Zaúčtování skutečné hmotnosti

Produkty se skutečnou hmotností se často používají v průmyslových odvětvích, jako je potravinářský průmysl, kde se výrobky mohou mírně lišit hmotností, velikostí nebo obojím. Produkty se skutečnou hmotností používají dvě měrné jednotky: skladovou jednotku a jednotku skutečné hmotnosti. Hmotnost zásob při příjmu do skladu se může lišit od hmotnosti při výdeji ze skladu. Zpracování produktu se skutečnou hmotností upraví zásoby.

Pokud dojde k odchylce skutečné hmotnosti, rozdíly se zaúčtují na účty, které jsou uvedeny v polích **Účet ztrát – skutečná hmotnost** a **Účet zisků – skutečná hmotnost** na stránce **Profil účtování zásob**. Obvykle je v obou polích uveden stejný hlavní účet.

Následující tabulka ukazuje příklady výchozích typů účtování spolu s ukázkovými hlavními účty a popisy.

- Sloupec „Debetní/kreditní?“ sloupec udává, zda je transakce obvykle debetní nebo kreditní. V určitém případě může transakce zaúčtovat buď debety, nebo kredity.
- Sloupec „Clearingový účet“ označuje, že typ účtování je clearingový účet. To znamená, že částka zaúčtovaná na tomto účtu je automaticky stornována při zaúčtování pozdější transakce.
- Sloupec "P/F" označuje typ účtování. „P“ představuje fyzické účtování a „F“ představuje finanční účtování.
- Sloupec „Sledovat“ udává, zda je hlavní účet pro typ účtování obvykle stejný jako hlavní účet pro jiný typ účtování. Konkrétně označuje typ účtování, který se obvykle používá k účtování.

> [!NOTE]
> Hlavní účty a názvy hlavních účtů v tabulce jsou pouze návrhy. Doporučujeme, abyste ve spolupráci se svým účetním určili nejlepší konfiguraci pro vaše obchodní potřeby.

| Typ zaúčtování | Příklad hlavního účtu | Příklad názvu hlavního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | P/F | Sledovat | Popis |
|---|---|---|---|---|---|---|---|---|
| Účet ztrát – skutečná hmotnost | 510520 | Úprava zásob | Výdaje | | Číslo | Oboje | Účet zisků – skutečná hmotnost | Tento účet se používá, když zaúčtujete transakci zásob, kde je částka skutečné hmotnosti nižší. |
| Účet zisků – skutečná hmotnost | 510520 | Úprava zásob | Výdaje | | Číslo | Oboje | Účet ztrát – skutečná hmotnost | Tento účet se používá, když zaúčtujete transakci zásob, kde je částka skutečné hmotnosti vyšší. |

Další informace o produktech se skutečnou hmotností najdete v tématech [O položkách skutečné hmotnosti](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.md) a [Zachycení zpracování produktů pomocí řízení skladu](/supply-chain/warehousing/catch-weight-processing.md).

## <a name="inventory-to-fixed-asset-transfer-posting"></a>Zaúčtování převodu zásob do dlouhodobého majetku

Deníku přesunu zásob do dlouhodobého majetku (**Dlouhodobý majetek** \> **Deníky** \> **Deník přesunu zásob do dlouhodobého majetku**) se používá k přesunu položek ze zásob a jejich přeměně na dlouhodobý majetek. Další informace naleznete v tématu [Integrace dlouhodobého majetku](/fixed-assets/fixed-asset-integration.md).

Následující tabulka ukazuje příklady výchozích typů účtování spolu s ukázkovými hlavními účty a popisy.

- Sloupec „Debetní/kreditní?“ sloupec udává, zda je transakce obvykle debetní nebo kreditní. V určitém případě může transakce zaúčtovat buď debety, nebo kredity.
- Sloupec „Clearingový účet“ označuje, že typ účtování je clearingový účet. To znamená, že částka zaúčtovaná na tomto účtu je automaticky stornována při zaúčtování pozdější transakce.
- Sloupec "P/F" označuje typ účtování. „P“ představuje fyzické účtování a „F“ představuje finanční účtování.
- Sloupec „Sledovat“ udává, zda je hlavní účet pro typ účtování obvykle stejný jako hlavní účet pro jiný typ účtování. Konkrétně označuje typ účtování, který se obvykle používá k účtování.

> [!NOTE]
> Hlavní účty a názvy hlavních účtů v tabulce jsou pouze návrhy. Doporučujeme, abyste ve spolupráci se svým účetním určili nejlepší konfiguraci pro vaše obchodní potřeby.

| Typ zaúčtování | Příklad hlavního účtu | Příklad názvu hlavního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | P/F | Sledovat | Popis |
|---|---|---|---|---|---|---|---|---|
| Výdej dlouhodobého majetku | 180100 | Hmotný dlouhodobý majetek | Materiál | Kredit | Číslo | Oboje | Nelze použít | Tento účet se používá, když účtujete zásoby do deníku dlouhodobého majetku, abyste odstranili položku ze zásob a převedli ji na dlouhodobý majetek. |

## <a name="moving-average-posting"></a>Zaúčtování klouzavého průměru

Klouzavý průměr je metoda stálého výpočtu nákladů, která je založena na principu průměru. Náklady u výdejů zásob se nemění, když se mění nákupní cena. Rozdíl je kapitalizován a je založen na proporcionálním výpočtu. Zbývající částka je zanesena do výdajů.

Následující tabulka ukazuje příklady výchozích typů účtování s ukázkovými hlavními účty a popisy.

- Sloupec „Debetní/kreditní?“ sloupec udává, zda je transakce obvykle debetní nebo kreditní. V určitém případě může transakce zaúčtovat buď debety, nebo kredity.
- Sloupec „Clearingový účet“ označuje, že typ účtování je clearingový účet. To znamená, že částka zaúčtovaná na tomto účtu je automaticky stornována při zaúčtování pozdější transakce.
- Sloupec "P/F" označuje typ účtování. „P“ představuje fyzické účtování a „F“ představuje finanční účtování.
- Sloupec „Sledovat“ udává, zda je hlavní účet pro typ účtování obvykle stejný jako hlavní účet pro jiný typ účtování. Konkrétně označuje typ účtování, který se obvykle používá k účtování.

> [!NOTE]
> Hlavní účty a názvy hlavních účtů v tabulce jsou pouze návrhy. Doporučujeme, abyste ve spolupráci se svým účetním určili nejlepší konfiguraci pro vaše obchodní potřeby.

| Typ zaúčtování | Příklad hlavního účtu | Příklad názvu hlavního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | P/F | Sledovat | Popis |
|---|---|---|---|---|---|---|---|---|
| Cenová odchylka pro klouzavý průměr | 510600 | Cenová odchylka pro klouzavý průměr | Výdaje | Oboje | Číslo | Oboje | Nelze použít | Tento účet se používá, když existuje rozdíl v nákladech mezi příjemkou a fakturou. |
| Přecenění pro klouzavý průměr | 510610 | Přecenění klouzavého průměru | Výdaje | Oboje | Číslo | Oboje | Nelze použít | Tento účet se používá, když upravujete klouzavý průměr nákladů na produkt |

## <a name="sample-posting-profile-configuration"></a>Ukázka konfigurace profilu zveřejňování

Následující tabulka ukazuje příklady výchozích typů účtování s ukázkovými hlavními účty a popisy.

| Typ zaúčtování | Příklad hlavního účtu | Příklad názvu hlavního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | P/F | Sledovat | Popis |
|---|---|---|---|---|---|---|---|---|
| Skladový výdej | 140100 | Zásoby materiálů | Materiál | Kredit | Číslo | Oboje | Příjem na sklad | Tento účet se používá, když je zaúčtovaná transakce zásob výdejem (záporné množství) a nesouvisí s prodejem, nákupem nebo výrobou. Protiúčtem tohoto účtu je účet Výdaje zásob, ztráta. Tento účet obvykle představuje zásoby ve vaší rozvaze. |
| Výdaje zásob, ztráta | 510100 | Zisky a ztráty zásob | Výdaje | Debet | Číslo | Oboje | Výdaje zásob, zisk | Tento účet se používá, když je zaúčtovaná transakce zásob výdejem (záporné množství) a nesouvisí s prodejem, nákupem nebo výrobou. Protiúčtem tohoto účtu je účet Výdeje zásob. |
| Příjem na sklad | 140100 | Zásoby materiálů | Materiál | Debet | Číslo | Oboje | Skladový výdej | Tento účet se používá, když je zaúčtovaná transakce zásob příjmem (kladné množství) a nesouvisí s prodejem, nákupem nebo výrobou. Protiúčtem tohoto účtu je účet Výdaje zásob, zisk. Tento účet obvykle představuje zásoby ve vaší rozvaze. |
| Výdaje zásob, zisk | 510100 | Zisky a ztráty zásob | Výdaje | Kredit | Číslo | Oboje | Výdaje zásob, ztráta | Tento účet se používá, když je zaúčtovaná transakce zásob příjmem (kladné množství) a nesouvisí s prodejem, nákupem nebo výrobou. Protiúčtem tohoto účtu je účet Příjem zásob. |
| Mezijednotkové závazky | 231500 | Mezijednotkové závazky | Pasiva | Debet | Číslo | Oboje | | Tento účet se používá, když se zásoby převádějí mezi dimenzemi zásob, jako jsou například místa, a náklady na položku se mezi místy liší. |
| Mezijednotkové pohledávky | 131500 | Mezijednotková pohledávka | Materiál | Kredit | Číslo | Oboje | | Tento účet se používá, když se zásoby převádějí mezi dimenzemi zásob, jako jsou například místa, a náklady na položku se mezi místy liší. |
