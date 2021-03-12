---
title: Duální měna
description: Toto téma obsahuje informace o duální měně, kdy je měna vykazování použita jako druhá zúčtovací měna pro aplikaci Microsoft Dynamics 365 Finance.
author: kweekley
manager: AnnBe
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, Ledger, AssetTransReportingCurrencyAmountsWizard,BankAccountTransReportingCurrencyAmountsWizard, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 04126c0cddd1242e9607274e35f4b7626ad573d2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990457"
---
# <a name="dual-currency"></a>Duální měna

[!include [banner](../includes/banner.md)]

Funkce, jež byla představena v aplikaci Microsoft Dynamics 365 for Finance and Operations verze 8.1 (říjen 2018) umožňuje změnu účelu zúčtovací měny a její použití jako druhé zúčtovací měny. Tato funkce je někdy označována jako *duální měna*. Změny pro duální měnu nelze vypnout pomocí konfiguračního klíče nebo parametru. Vzhledem k tomu, že se měna vykazování používá jako druhá zúčtovací měna, způsob výpočtu zúčtovací měny v logice zaúčtování byl změněn.

Byly navíc zdokonaleny různé moduly pro sledování, vykazování a používání měny vykazování v různých procesech. Mezi ovlivněné moduly patří:

- Hlavní kniha 
- Finanční výkaznictví 
- Závazky
- Pohledávky 
- Pokladna a banka 
- Dlouhodobý majetek 
- Konsolidace

Po upgradu je třeba provést konkrétní kroky pro správu hotovosti a banky a dlouhodobý majetek. Proto si nezapomeňte přečíst a porozumět příslušné části tohoto tématu.

## <a name="posting-process"></a>Proces zaúčtování

Byla změněna logika účtování pro všechny transakce, které generují účetní zápis do hlavní knihy. Zde je dřívější způsob výpočtu měny vykazování:

Částka v transakční měně \> částka v zúčtovací měně \> částka v měně vykazování

Příklad: transakce se zadává v měně Kanadský dolar (CAD). Částka v kanadských dolarech je převedena na zúčtovací měnu, což je americký dolar (USD). Částka v kanadských dolarech je pak převedena na měnu vykazování, což je euro (EUR). Proto musí existovat směnné kurzy mezi CAD a USD a mezi USD a EUR.

Nový výpočet vypadá takto:

Částka v měně transakce \> Částka v měně účetnictví

Částka v měně transakce \> Částka v měně pro vykazování

Proto musí nyní existovat směnné kurzy mezi CAD a USD a mezi CAD a EUR.

## <a name="reports-and-inquiries"></a>Dotazy a sestavy

Různé sestavy a dotazy nyní zobrazují částky v měně vykazování i částky v zúčtovací měně. Ne všechny sestavy a dotazy byly aktualizovány. Například nebyly změněny sestavy zobrazující částky pouze v měně transakce.

Změny jsou provedeny podle jednoho ze dvou vzorců:

- Pokud měla sestava nebo dotaz dostatek volného místa pro zobrazení částek v zúčtovací měně i měně vykazování, byly přidány částky v měně vykazování.
- Jestliže sestava nebo dotaz neměly k dispozici dostatek volného místa pro zobrazení částek v obou měnách, byla přidána možnost, aby si uživatelé mohli vybrat měnu, která se zobrazí.

Pro různé sestavy a dotazy byla také přidána logika pro potlačení částek měny vykazování, jestliže byla měna vykazování stejná jako zúčtovací měna nebo pokud v hlavní knize pro právnickou osobu nebyla definována zúčtovací měna.

## <a name="financial-journals"></a>Finanční deníky

Byly aktualizovány finanční deníky, jako je například deník hlavní knihy a deník faktury dodavatele tak, aby zahrnovaly další informace o sekundární měně. Součty pro doklad a deník jsou nyní zobrazeny v měně vykazování. Kromě toho se informace o směnném kurzu měny vykazování nyní zobrazují na kartě **Hlavní** řádek deníku. Proto je možné přepsat směnný kurz měny vykazování při zadávání transakcí.

## <a name="vendor-invoices-sales-orders-and-sales-agreements"></a>Faktury dodavatele, prodejní objednávky a prodejní smlouvy
Faktury dodavatele, prodejní objednávky a prodejní smlouvy byly aktualizovány tak, aby zahrnovaly pevný směnný kurz pro měnu vykazování. Pevný směnný kurz lze definovat jak pro měnu účtování, tak pro měnu vykazování, pokud je měna transakce odlišná. Pokud jsou zúčtovací měna a měna vykazování stejné, bude pevný směnný kurz synchronizován s použitím pevné sazby zúčtovací měny jako pevné sazby měny vykazování. Pevný směnný kurz měny pro vykazování nelze pro tuto konfiguraci změnit. Pokud se zúčtovací měna a měna vykazování liší, pevný směnný kurz lze definovat jak pro měnu účtování, tak pro měnu vykazování během zadávání transakce. Pokud v hlavní knize není definována měna vykazování, nebude povoleno pole **Pevný směnný kurz měny vykazování** a nebude vypočtena žádná částka měny vykazování.

## <a name="module-changes"></a>Změny modulu

Následující moduly používají měnu vykazování jako druhou zúčtovací měnu:

- [Hlavní kniha](#general-ledger)
- [Finanční výkaznictví](#financial-reporting)
- [Závazky](#accounts-payable-and-accounts-receivable)
- [Pohledávky](#accounts-payable-and-accounts-receivable)
- [Pokladna a banka](#cash-and-bank-management)
- [Dlouhodobý majetek](#fixed-assets)
- [Konsolidace](#consolidations)

### <a name="general-ledger"></a>Hlavní kniha

Pokud měna vykazování byla definována v hlavní knize, hlavní kniha již sledovala částky v měně vykazování u každé účetní položky. Tyto částky jsou však nyní přeloženy z částek v měně transakce.

Byly provedeny následující dodatečné změny v modulu **Hlavní kniha**:

- V hlavní knize lze definovat samostatný typ směnného kurzu pro měnu vykazování. Pokud organizace nechce použít jiný typ směnného kurzu, můžete nechat pole pro typ směnného kurzu pro měnu vykazování prázdné. Případně můžete vybrat stejný typ směnného kurzu, jaký je použitý pro zúčtovací měnu. Pokud pole ponecháte prázdné, systém použije typ směnného kurzu pro zúčtovací měnu.
- Nový deník, Úprava měny vykazování, umožňuje zaúčtování úprav na účty hlavní knihy pouze v měně vykazování. Tento deník umožňuje zaúčtování pouze na účty hlavní knihy. Nepodporuje mezipodnikové zaúčtování a měna musí být měna vykazování právnické osoby, u níž byl deník zaúčtován. Při zaúčtování deníku jsou částky transakční měny a zúčtovací měny 0 (nula) a částky v měně vykazování jsou zaúčtovány s částkou, která je zadána v transakci. Vzhledem k tomu, že se změnil způsob, jakým je měna vykazování použita v modulech **závazky**, **pohledávky**, a **dlouhodobý majetek**, lze tento deník použít pro úpravy po dokončení upgradu. Příklady použití tohoto deníku naleznete v částech pro tyto moduly.
- Proces přidělení období byl aktualizován tak, aby se přidělovaly částky v měnách transakce, účtování a vykazování. V předchozích verzích bývaly přidělovány částky transakční a zúčtovací měny a potom byly částky v zúčtovací měně převedeny na měnu vykazování. Toto chování mohlo způsobit, že zůstatek byl na účtu hlavní knihy v měně vykazování. Nyní se po výpočtu a použití částek v účetní položce neuskuteční žádný převod.
- Proces přecenění cizí měny již přecenil částky v měně vykazování. Částka v měně vykazování je však nyní vypočítána pomocí částky v měně transakce, jak je popsáno v části [Proces zaúčtování](#posting-process) dříve v tomto tématu.
- Mnoho sestav a dotazů v hlavní knize již mělo zúčtovací měnu, ale pár jich ji nemělo. Jedním příkladem je stránka se seznamem **Předvaha**. Tato stránka se seznamem nyní zahrnuje sloupce pro zúčtovací měnu i měnu vykazování. Všimněte si, že sloupce pro měnu vykazování jsou skryté, pokud je zúčtovací měna a měna vykazování stejná nebo pokud v hlavní knize nebyla definována měna vykazování.

### <a name="financial-reporting"></a>Finanční výkaznictví

Vylepšení modulu **Finanční vykazování** umožňuje zahrnout částky v měně vykazování do finančního výkazu dvěma způsoby. V definici sloupce můžete vykazovat přímo v částkách měny vykazování, které jsou zaúčtovány do hlavní knihy (nová funkce). Případně můžete pokračovat k převodu částek v zúčtovací měně na měnu vykazování (existující funkce).

Tato změna je k dispozici prostřednictvím nastavení **zobrazení měny** v definici sloupce. Vyberete-li **Měna vykazování z hlavní knihy**, nejsou částky ve sloupci převedeny. Namísto toho jsou vykázány přímo z hlavní knihy. Pokud chcete, aby se ve sloupci zobrazovaly převedené částky, vyberte možnost **Převést na XXXX**, kde *XXXX* je měna vykazování, která by se ve sloupci měla zobrazovat. V takovém případě budou částky v zúčtovací měně převedeny na vybranou měnu pomocí existující funkce převodu.

### <a name="accounts-payable-and-accounts-receivable"></a>Pohledávky a závazky

Moduly **Závazky** a **Pohledávky** již sledovaly částky v měně vykazování. Částky však nebyly zobrazena nebo použitý pro různé procesy. Byly provedeny tyto změny:

- Částky v měně vykazování jsou nyní zobrazeny v transakcích odběratele a dodavatele. Částky v měně vykazování jsou také uvedeny pro otevřený zůstatek každé transakce.
- Časový proces byl aktualizován tak, aby organizace mohla zobrazit časové intervaly v zúčtovací měně nebo měně vykazování.
- Různé dotazy a sestavy byly aktualizovány tak, aby zobrazovaly částky v měně vykazování. Mezi příklady patří sestavy **Odsouhlasení zákazníka do hlavní knihy** a **Odsouhlasení dodavatele do hlavní knihy**.
- Proces přecenění cizí měny již přecenil částky v měně vykazování. Částka v měně vykazování je však nyní vypočítána pomocí částky v měně transakce, jak je popsáno v části [Proces zaúčtování](#posting-process).
- **Důležité aspekty upgradu:** Před provedením upgradu jsou částky měny vykazování dokumentů (faktury, platby atd.) vypočítány prostřednictvím zúčtovací měny. Faktura je například zaúčtována před provedením upgradů organizace, když není zaplacená faktura. Během upgradu nedojde ke změně účetního zápisu na faktuře. Po upgradu jsou však ovlivněny změny pro duální měnu. Proto se při provedení platby faktury částka platby v měně vykazování nyní počítá pomocí částky transakční měny. Při vyrovnání platby a faktury může být vypočten mírný rozdíl částky realizovaného zisku/ztráty, protože se částky měny vykazování nyní vypočítávají odlišně. Pokud je vypočtený rozdíl považován za značný, lze použít nový deník úpravy vykazované měny k úpravě zůstatku realizovaného zisku/ztráty a účtů hlavní knihy pohledávek/závazků pouze v měně vykazování.

### <a name="cash-and-bank-management"></a>Pokladna a banka

V předchozích verzích modul **Řízení hotovosti a banky** nesledoval žádné částky v měně vykazování pro transakce, které byly zaúčtovány pro každý bankovní účet. Po provedení upgradu jsou pro všechny nové transakce, které jsou zaúčtovány, automaticky sledovány částky v měně vykazování. Částky v měně vykazování však musí být přidány do dříve zaúčtovaných transakcí ve vedlejší knize.

- **Důležité aspekty upgradu:** Vzhledem k tomu, že transakce bankovního účtu dříve nesledovaly částky v měně v dílčí knize, byl přidán průvodce, abyste mohli přidat částky v měně vykazování k transakcím bankovního účtu. Tento průvodce **neprovádí** zaúčtování do hlavní knihy. Namísto toho vezme částky v měně vykazování z hlavní knihy a aktualizuje je v tabulkách vedlejší knihy.

    - Chcete-li spustit průvodce, vyberte **Řízení hotovosti a banky** \> **Nastavení** \> **Přidat částky v měně vykazování k transakcím bankovního účtu**.
    - Průvodce zobrazí transakce pro všechny bankovní účty v aktuální společnosti, které mají částku měny vykazování 0 (nula). Budou zahrnuty pouze transakce zaúčtované před upgradem.
    - Pro každou transakci bankovního účtu průvodce vyhledá odpovídající účetní položky v hlavní knize a zadá výchozí částku v měně vykazování. Ačkoli částky můžete upravit, doporučujeme, abyste je **neupravovali**. Jinak nemusí být možné odsouhlasit zůstatky bankovního účtu hlavní knihy. Jediná doba, kdy byste měli upravit částku, nastane, když nelze najít částku v měně vykazování v hlavní knize. Průvodce v takovém případě zobrazí částku 0 (nula) pro měnu vykazování.
    - Vyberete-li v průvodci možnost **Zrušit**, transakce bankovního účtu a jakékoli změny částek v měně vykazování částky budou uloženy až do dalšího spuštění průvodce. Částky v měně vykazování v transakcích bankovního účtu však nebudou aktualizovány. Tato aktualizace však proběhne pouze při výběru možnosti **Dokončit** v průvodci. Průvodce lze spustit více než jednou. Proto můžete opravit jakékoli nesprávné částky v měně vykazování, pokud došlo k chybě.

- Nebyly změněny žádné procesy v modulu řízení hotovosti a banky, ale různé sestavy a dotazy byly aktualizovány tak, aby zobrazovaly částky v měně vykazování. Výjimkou jsou sestavy prognózy cash flow. Nebyly aktualizovány tak, aby zahrnovaly částky v měně vykazování.

### <a name="fixed-assets"></a>Dlouhodobý majetek

V předchozích verzích modul **Dlouhodobý majetek** nesledoval žádné částky v měně vykazování pro transakce, které byly zaúčtovány pro každou knihu dlouhodobého majetku. Po provedení upgradu jsou pro všechny nové transakce, které jsou zaúčtovány, automaticky sledovány částky v měně vykazování. Částky v měně vykazování však musí být přidány do dříve zaúčtovaných transakcí ve vedlejší knize.

Kromě toho byly provedeny zásadní změny procesu odpisování. Tyto změny vyžadují akci uživatele po upgradu. Je důležité, abyste si přečetli a pochopili následující změny, i když ještě dlouhodobý majetek nepoužíváte.

- Způsob, jakým proces odpisu určuje částky v měně vykazování, se změnil. Následující scénář porovnává způsob, jakým odpis dříve určoval částku v měně vykazování a jak určuje částku v měně vykazování nyní.



    **Scénář odpisů**

    Majetek byl pořízen a zaúčtován s následujícími částkami. Všimněte si, že je částka v měně vykazování zaúčtována do hlavní knihy, ale není uložena v tabulkách dílčí knihy dlouhodobého majetku.

    | typ transakce | Částka transakce | Směnný kurz | Částka zúčtovací měny | Směnný kurz | Částka v měně vykazování |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Pořizovací cena      | 1 000 000 DKK      | 2.0           | 500 000 USD                | 2,5           | 200,000 EUR               |

    **Přechozí odpis pro měnu vykazování**

    Na konci roku se spustí návrh odpisu a vypočte následující částky.

    | typ transakce | Částka transakce | Směnný kurz | Částka zúčtovací měny | Směnný kurz | Částka v měně vykazování |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Odpis     | 50 000 USD         | 1.0           | 50 000 USD                 | 2.6           | 19,230.77 EUR             |

    Po spuštění návrhu odpisu se vypočítá částka v zúčtovací měně pomocí metody odpisu. Pak převede částku na měnu vykazování s použitím aktuálního směnného kurzu mezi USD a EUR. Tento převod způsobí problémy, vzhledem k tomu, že majetek nelze plně odepsat v měně vykazování při použití místní sazby.

    **Nový odpis pro měnu vykazování**

    Proces odpisu se změnil tak, aby byla také vypočtena částka v měně vykazování s použitím metody odpisu. Zde jsou výsledky při spuštění odpisu u majetku.

    | typ transakce | Částka transakce | Směnný kurz | Částka zúčtovací měny | Směnný kurz                                                       | Částka v měně vykazování |
    |------------------|--------------------|---------------|----------------------------|---------------------------------------------------------------------|---------------------------|
    | Odpis     | 50 000 USD         | 1.0           | 50 000 USD                 | 2,5<blockquote>[!NOTE] I když se zobrazuje tento směnný kurz, není použit k převodu na měnu vykazování.</blockquote> | 20,000 EUR                |

    Po spuštění návrhu odpisu se vypočítá částka v zúčtovací měně i částka v měně vykazování pomocí metody odpisu. Částky se následně používají v účetní položce v hlavní knize. K určení částky v měně vykazování se neprovede žádný převod.

- **Důležité aspekty upgradu:** Vzhledem k tomu, že transakce dlouhodobého majetku dříve nesledovaly měnu vykazování, byl přidán průvodce, abyste mohli přidat částky v měně vykazování k transakcím knihy dlouhodobého majetku. Tento průvodce **neprovádí** zaúčtování do hlavní knihy. Vzhledem k tomu, že se změnil způsob, jakým návrh odpisu vypočítává částky v měně vykazování, **musí** se spustit průvodce a musí být dokončen pro každou společnost předtím, než organizace může zadat nějaké transakce odpisů.

    - Chcete-li spustit průvodce, vyberte **Dlouhodobý majetek** \> **Nastavení** \> **Přidat částky v měně vykazování ke knihám dlouhodobého majetku**.
    - Průvodce zobrazí transakce pro všechny knihy dlouhodobého majetku v aktuální společnosti, které mají částku měny vykazování 0 (nula). Budou zahrnuty pouze transakce zaúčtované před upgradem.
    - Průvodce **nevyžaduje** částky měny vykazování v hlavní knize. Jak bylo uvedeno v předchozím scénáři, částky v měně vykazování, které byly původně zaúčtovány do hlavní knihy, nesprávně použily místní sazby. Tyto částky by se neměly zobrazit v dílčí knize dlouhodobého majetku, protože následující výpočet odpisů použije nesprávné množství. Místo toho průvodce vyhledá směnný kurz k datu prvního pořízení. Poté použije tento směnný kurz k doporučení částky v měně vykazování, která by měla být zaúčtována v dílčí knize. V tomto poli je například to, co mohl Průvodce zobrazovat pro předchozí scénáře.

        | Dlouhodobý majetek | Rezervovat      | typ transakce | Datum transakce | Měna | Částka v měně transakce | Množství  | Sm. kurz | Částka v měně vykazování |
        |-------------|-----------|------------------|------------------|----------|--------------------------------|---------|-----------|---------------------------|
        | BUIL-00001  | 200\_SLLT | Pořizovací cena      | 6/3/2016         | DKK      | 1 000 000                      | 500,000 | 2.5       | 250,000                   |
        | BUIL-00001  | 200\_SLLT | Odpisy     | 6/3/2016         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |
        | BUIL-00001  | 200\_SLLT | Odpisy     | 6/3/2016         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |
        | BUIL-00001  | 200\_SLLT | Odpisy     | 6/3/2016         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |

    - Mnozí zákazníci sledovali podrobnosti o svých majetkových transakcích v sešitech. Tyto informace zahrnují směnné kurzy a částky. Pokud máte tato data v sešitu, můžete vytvořit vlastní typ směnného kurzu a aktualizovat ho směnnými kurzy ze sešitu. Tento typ směnného kurzu se pak použije k zadání výchozího směnného kurzu k datu pořízení a vypočítá částku v měně vykazování. Pokud není vybrán typ směnného kurzu, průvodce použije typ směnného kurzu, který byl definován v hlavní knize.
    - Směnný kurz a částky v měně vykazování nelze měnit. Pokud změníte směnný kurz, částka v měně vykazování se přepočítá s použitím nového kurzu.
    - Vyberete-li v průvodci možnost **Zrušit**, transakce knihy dlouhodobého majetku a jakékoli změny směnného kurzu v měně vykazování budou uloženy až do dalšího spuštění průvodce. Částky v měně vykazování v transakcích knihy dlouhodobého majetku však nebudou aktualizovány. Tato aktualizace však proběhne pouze při výběru možnosti **Dokončit** v průvodci. Průvodce lze spustit více než jednou. Proto můžete opravit jakékoli nesprávné částky v měně vykazování, pokud došlo k chybě.
    - V případě kompletní aktualizace částek v měně vykazování v dílčí knize **musíte** nastavit možnost **Aktualizovali jste všechny částky v měně vykazování v transakcích knihy dlouhodobého majetku?** na **Ano** a pak vybrat možnost **Dokončit**. Výpočty odpisu nelze dokončit, dokud nenastavíte možnost **Aktualizovali jste všechny částky v měně vykazování v transakcích knihy dlouhodobého majetku?** na **Ano**. Po nastavení této možnosti na **Ano** již Průvodce není k dispozici.
    - Po aktualizaci transakcí dlouhodobého majetku v dílčí hlavní knize částkami v měně vykazování nebudou tyto částky odpovídat částkám, které byly původně zaúčtovány do hlavní knihy. Deník pro úpravy měny vykazování lze však použít k aktualizaci zůstatků na účtech knihy odpisů v hlavní knize tak, aby odpovídaly původně zaúčtovaným částkám.
    - Nová entita **Částky měny vykazování majetkových transakcí**, která byla přidána do pracovního prostoru **Správa dat**, umožňuje exportovat data z průvodce. Následně můžete data použít k určení zůstatku v dílčí knize dlouhodobého majetku pro odpisové transakce. Tento odhad lze použít k určení částky pro úpravu měny vykazování v hlavní knize.

- **Důležitý aspekt pro upgrade:** Do dlouhodobého majetku byla přidána nová pole pro nastavení a používají se při výpočtu odpisů. Je nutné aktualizovat tato pole před dalším výpočtem odpisů.

    - V knize dlouhodobého majetku (**dlouhodobý majetek** \> **knihy**) má pevná záložka **Obecné** nové pole **pořizovací cena v měně vykazování**.
    - V knize dlouhodobého majetku (**dlouhodobý majetek** \> **knihy**) má pevná záložka **Odpis** nové pole **Očekávaná hodnota vyřazení v měně vykazování**.
    - V parametrech dlouhodobého majetku (**dlouhodobý majetek** \> **nastavení** \> **Parametry dlouhodobého majetku**) má pevná záložka **Obecné** nové pole **Minimální částka odpisu v měně vykazování**.
    - V knihách (**dlouhodobý majetek** \> **nastavení** \> **knihy**) má pevná záložka **Obecné** dvě nová pole: **Zaokrouhlit odpis v měně vykazování** a **Ponechat zůstatkovou účetní hodnotu v měně vykazování**.

- Protože nyní návrh odpisu vypočítává částky v zúčtovací měně a měně vykazování, deník dlouhodobého majetku byl aktualizován tak, aby se zobrazovaly částky v měně vykazování. U odpisových transakcí je měna transakce vždy zúčtovací měna. Proto se tyto částky budou nadále zobrazovat ve sloupcích **MD** a **Dal**. Dva nové sloupce **má dáti v měně vykazování** a **Dal v měně vykazování**, byly přidány do mřížky.

    - Nová pole jsou k dispozici pouze v případě, že je typem transakce, jeden ze čtyř typů odpisů: **odpisování**, **Odpisová odchylka**, **mimořádný odpis**, nebo **procento pro výpočet speciálních odpisů**.
    - Je-li typ transakce odpisování je zadán v deníku dlouhodobého majetku, částky v měně vykazování se zobrazí v nových sloupcích. Tyto částky lze změnit.
    - Pokud je zúčtovací měna a měna vykazování v hlavní knize stejná, budou částky průběžně synchronizovány. Změníte-li částku **Dal**, částka **Dal v měně vykazování** se automaticky změní tak, aby jí odpovídala.
    - Pokud je do deníku dlouhodobého majetku zadán jakýkoli jiný typ transakce, částky **má dáti v měně vykazování** a **Dal v měně vykazování** se nikdy nezobrazí, ani před, ani po zaúčtování. Částky v zúčtovací měně a měně vykazování jsou stále k dispozici na dokladu, ve kterém se má zaúčtovat do hlavní knihy.
    
### <a name="consolidations"></a>Konsolidace
    
Funkce, které byly zavedeny v Dynamics 365 Finance verzi 10.0.5 (říjen 2019), umožňují funkcionalitu prostřednictvím správy funkcí pro zvýšenou flexibilitu pro konsolidaci a duální měnu. Chcete-li tuto funkci povolit, přejděte do pracovního prostoru **Správa funkcí** a vyberte možnost **Povolit funkci duální měny v konsolidaci hlavní knihy**.

V konsolidaci hlavní knihy byla přidána nová možnost pro konsolidaci částek ve zúčtovací měně nebo měně vykazování ze zdrojových společností. Pokud je zúčtovací měna nebo měna vykazování shodná se zúčtovací měnou nebo měnou vykazování v konsolidační společnosti, budou částky kopírovány přímo namísto převodu.

-  Nyní můžete zvolit, zda chcete použít zúčtovací měnu nebo měnu vykazování ze zdrojové společnosti jako transakční měnu v konsolidační společnosti.

- Částky zúčtovací měny nebo měny vykazování ze zdrojové společnosti budou zkopírovány přímo do částek zúčtovací měny nebo měny vykazování v konsolidační společnosti, pokud je některá z měn stejná. Pokud žádná z měn není stejná, jsou částky zúčtovací měny nebo měny vykazování v konsolidační společnosti vypočteny pomocí směnného kurzu.
