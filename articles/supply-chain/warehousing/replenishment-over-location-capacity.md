---
title: Doplnění nad kapacitu místa
description: Toto téma obsahuje informace o funkci Doplňování přes kapacitu místa. Tato funkce umožňuje veškerou doplňovací práci, která bude vyžadována na den, který má být vytvořen, a řídí dostupnost této doplňovací práce, aby bylo zajištěno, že místu vyskladnění nedojdou zásoby, ani nepřekročí kapacitu.
author: Mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 0c3dedc47558e98f63fb5883e4731bf021b9602b
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677919"
---
# <a name="replenishment-over-location-capacity"></a>Doplnění nad kapacitu místa

[!include [banner](../includes/banner.md)]

Některé velkoobjemové sklady nebo sklady s omezeným prostorem musí přepravit více kusů zboží za den, než kolik se vejde na místo vyskladnění. Funkce *Doplnění nad kapacitu místa* umožňuje veškerou doplňovací práci, která bude vyžadována na den, který má být vytvořen, a řídí dostupnost této doplňovací práce, aby bylo zajištěno, že místu vyskladnění nedojdou zásoby, ani nepřekročí kapacitu.

Tato funkce umožňuje vytvořit více prací doplnění, než kolik se vejde na místo, a blokuje dokončení doplňovacích prací, když je místo plné. Jak zásoby ve vychystávacím místě klesnou pod nastavitelný práh, je k dispozici více doplňovacích prací.

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a>Zapnutí funkce Doplnění nad kapacitu místa

Chcete-li tuto funkci zpřístupnit, zapněte následující funkce ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (v tomto pořadí):

1. Blokování práce pro celou organizaci (od Supply Chain Management verze 10.0.21 je tato funkce povinná, takže je ve výchozím nastavení zapnutá a nelze ji znovu vypnout).
1. Doplnění nad kapacitu místa

## <a name="set-up-the-feature-for-the-example-scenario"></a>Nastavení funkce pro tento vzorový scénář

Tato část obsahuje pokyny a příklad, který ukazuje, jak nastavit tuto funkci a připravit ukázková data pro příkladový scénář, který je uveden dále v tomto tématu.

### <a name="enable-sample-data"></a>Povolit ukázková data

Chcete-li s [příkladovým scénářem](#example-scenario) pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.

### <a name="location-profile"></a>Profil umístění

Povolte funkci doplňování přes kapacitu v profilu místa.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Profily míst**.
1. V levém podokně vyberte možnost **PICK-06**.
1. V podokně akcí vyberte **Upravit**.
1. Na pevné záložce **Doplnění** nastavte následující hodnoty:

    - **Překročit lokální kapacitu:** *Ano*

        Když je tato možnost povolena, bude povoleno překročení maximální kapacity místa o práci doplnění. To také umožňuje další pole na pevné záložce **Doplnění**.

    - **Typ prahu dostupnosti práce:** *Množství*

        Toto pole definuje metodu, která se používá k určení, kdy by mělo být uvolněno více práce. Můžete uvolnit podle množství nebo procent.

        - *Procento* - Tuto možnost vyberte, chcete-li použít procentuální kapacitu, která je založena na limitech skladování nebo objemu. Výběr této možnosti povolí pole **Procento přetečení** a zakáže dvě pole související s množstvím, **Množství přetečení** a **Jednotka přetečení**.

            Tuto možnost můžete použít, pokud místa výběru používají objemové jednotky.

            Pokud je vybrána tato možnost, nastavte pole **Procento přetečení** na, ve kterém bude k dispozici více prací doplnění.

        - *Množství* - Tuto možnost vyberte, chcete-li použít konkrétní hodnotu množství. Výběr této možnosti zakáže pole **Procento přetečení** a povolí pole **Množství přetečení** a **Jednotka přetečení**.

            Tuto možnost použijte, pokud nepoužíváte objem pro místa, která se doplňují, nebo pokud máte konzistentní množství, ve kterých chcete do místa přivést další inventář.

           Pokud je vybrána tato možnost, nastavte pole **Množství přetečení** a **Jednotka přetečení** na množství a jednotku, ve které bude k dispozici více doplňovacích prací.

    - **Množství přetečení:** *0.65*

        Toto pole definuje množství, při kterém místo přetéká.

        Práce bude k dispozici pokaždé, když je součet množství na skladě v místě a množství práce pod touto hodnotou. Jakákoli práce doplnění nad touto hodnotou bude blokována a bude nutné ji odblokovat ručně.

        Při výpočtu pracovního množství se berou v úvahu limity místního skladování.

    - **Jednotka přetečení:** *PL*

        Toto pole definuje jednotku, která je spojena s množstvím přetečení.

        V tomto případě bude k dispozici více doplňovacích prací, jakmile se umístění dostane na 0,65 palety (PL).

    - **Procento přetečení**

        Toto pole definuje procento, při kterém místo přetéká.

        Práce bude k dispozici pokaždé, když je součet množství na skladě v místě a množství práce pod tímto procentem. Jakékoli procento množství práce doplnění nad touto hodnotou bude blokováno a bude nutné je odblokovat ručně.

        Při výpočtu procenta pracovního množství se berou v úvahu limity místního skladování. Pokud nejsou definovány žádné limity pro místo uskladnění, procento množství práce bude vypočteno podle objemu, pokud jsou v profilu místa definována omezení objemu.

> [!IMPORTANT]
> Pokud používáte ukázková data pro právnickou osobu **USMF** právnická osoba a dříve jste zapnuli funkci *Umístění poznávací značky*, musíte vypnout nastavení **Povolit umístění poznávací značky** pro profil místa **BULK-06** k dokončení mobilních kroků v příkladu scénáře.

### <a name="wave-step-code"></a>Kód kroku vlny

> [!NOTE]
> Chcete-li nastavit kód kroku vlny, jak je zde popsáno, možná budete muset nejprve použít [řízení funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) k zapnutí funkce, která je pojmenována *Kód kroků vlny napříč organizací*.

1. Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Kódy kroku vlny**.
1. Klikněte na **Nový** a poté nastavte následující hodnoty:

    - **Kód kroku vlny:** *Replen*
    - **Popis kroku vlny:** *Doplnění*
    - **Typ kroku vlny:** *Doplnění*

1. Zvolte **Uložit**.

### <a name="replenishment-template"></a>Šablona doplnění

Šablony doplnění jsou sada pravidel, která určují, kdy a jak je skladové místo doplňováno.

1. Přejděte na **Řízení skladu \> Nastavení \> Doplnění \> Šablony doplnění**.
1. V podokně akcí vyberte **Upravit**.
1. V části **Přehled** vyberte řádek, na kterém je pole **Doplňte šablonu** nastaveno na *Doplnění poptávky*.
1. Nastavte následující hodnoty:

    - **Kód kroku vlny:** *Replen*
    - **Povolit použití nerezervovaných množství ve vlnové poptávce:** *Ano*

1. Zvolte **Uložit**.

### <a name="wave-template"></a>Šablona vlny

1. Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.
1. V levém podokně nastavte v poli **Typ šablony vlny** na hodnotu *Doplnění*.
1. Vyberte šablonu **61 Shipping** v seznamu.
1. V podokně akcí vyberte **Upravit**.
1. Na pevné záložce **Obecné** nastavte volbu **Uvolnění práce automatického doplnění** na *Ano*.

    Nastavením této možnosti na *ano* můžete vytvořit doplnění podle poptávky a automaticky je vydat. Musíte přidat metodu doplnění vlny do šablony vlny a vytvořit šablonu doplnění typu **Poptávka vlny**. Nastavte šablonu doplnění na stránce **Šablony doplnění**. Chcete-li nastavit šablonu doplňování, musíte do šablony vlny přidat metodu doplňování.

1. Na pevné záložce **Metody** ve sloupci **Vybrané metody** najděte následující řádek:

    - **Název metody:** *replenish*
    - **Název:** *Doplnění*

1. Nastavte pole **Kód kroku vlny** pro tento řádek na *Replen*.
1. Zvolte **Uložit**.

## <a name="example-scenario"></a>Příklad

Po zpřístupnění a nastavení všech výše popsaných vzorových dat můžete v rámci tohoto scénáře vyzkoušet funkci *Doplnění nad kapacitu místa*. Hodnoty zobrazené v tomto scénáři předpokládají, že pracujete se standardními ukázkovými daty, která jste vybrali v právnické osobě **USMF** a připravili jste vzorové záznamy, které jsou popsány dříve v tomto tématu. Tento scénář také slouží jako příklad, který ukazuje, jak lze funkci použít v produkčním nastavení.

### <a name="create-replenishment-work"></a>Vytvořit práci doplnění

#### <a name="create-sales-order-1"></a>Vytvoření prodejní objednávky 1

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. V podokně Akce zvolte možnost **Nová** a otevře se dialogové okno pro vytvoření nové prodejní objednávky.
1. V dialogovém okně nastavte následující hodnoty:

    - **Účet zákazníka:** *US-007*
    - **Sklad:** *61*

1. Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.
1. Otevře se nová prodejní objednávka. Zahrnuje nový prázdný řádek na pevné záložce **Řádky prodejní objednávky**. Na tomto řádku nastavte následující hodnoty:

    - **Číslo položky:** *T0100*
    - **Množství:** *40*

1. Na pevné záložce **Řádky prodejních objednávek** vyberte **Zásoby \> Rezervace**.
1. Na stránce **Rezervace** vyberte možnost **Rezervovat šarži**.
1. Zavřete stránku.
1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.

    Zobrazí se informační zprávy, které uvádí ID vlny a ID dodávky, které byly vytvořeny. Vytvoří se také vlna doplnění.

    Obdržíte také varovnou zprávu, která uvádí: „ID práce XXXX nelze odblokovat, protože má nedokončené doplňování.“

#### <a name="create-sales-order-2"></a>Vytvoření prodejní objednávky 2

1. Na stránce **Všechny prodejní objednávky** v podokně akcí zvolte možnost **Nová** a otevře se dialogové okno pro vytvoření nové prodejní objednávky.
1. V dialogovém okně nastavte následující hodnota:

    - **Účet zákazníka:** *US-001*
    - **Sklad:** *61*

1. Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.
1. Otevře se nová prodejní objednávka. Zahrnuje nový prázdný řádek na pevné záložce **Řádky prodejní objednávky**. Na tomto řádku nastavte následující hodnoty:

    - **Číslo položky:** *T0100*
    - **Množství:** *60*

1. Na pevné záložce **Řádky prodejních objednávek** vyberte **Zásoby \> Rezervace**.
1. Na stránce **Rezervace** vyberte možnost **Rezervovat šarži**.
1. Zavřete stránku.
1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.

    Zobrazí se informační zprávy, které uvádí ID vlny a ID dodávky, které byly vytvořeny. Vytvoří se také vlna doplnění.

    Obdržíte také varovnou zprávu, která uvádí: „ID práce XXXX nelze odblokovat, protože má nedokončené doplňování.“

#### <a name="create-sales-order-3"></a>Vytvoření prodejní objednávky 3

1. Na stránce **Všechny prodejní objednávky** v podokně akcí zvolte možnost **Nová** a otevře se dialogové okno pro vytvoření nové prodejní objednávky.
1. V dialogovém okně nastavte následující hodnoty:

    - **Účet zákazníka:** *US-004*
    - **Sklad:** *61*

1. Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.
1. Otevře se nová prodejní objednávka. Zahrnuje nový prázdný řádek na pevné záložce **Řádky prodejní objednávky**. Na tomto řádku nastavte následující hodnoty:

    - **Číslo položky:** *T0100*
    - **Množství:** *30*

1. Na pevné záložce **Řádky prodejních objednávek** vyberte **Zásoby \> Rezervace**.
1. Na stránce **Rezervace** vyberte možnost **Rezervovat šarži**.
1. Zavřete stránku.
1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.

    Zobrazí se informační zprávy, které uvádí ID vlny a ID dodávky, které byly vytvořeny. Vytvoří se také vlna doplnění.

    Obdržíte také varovnou zprávu, která uvádí: „ID práce XXXX nelze odblokovat, protože má nedokončené doplňování.“

#### <a name="view-work-details"></a>Zobrazit podrobnosti práce

1. Přejděte do **Řízení skladu \> Práce \> Podrobnosti práce**.
1. V části **Přehled** vyfiltrujte sloupec **Sklad** pro sklad *61*.
1. Měli byste vidět, že pro tři prodejní objednávky bylo vytvořeno sedm ID práce.

    - Tři ze sedmi ID práce mají hodnotu **Typ pracovního příkazu** *Doplnění* a čtyři mají hodnotu **Typ pracovního příkazu** *Prodejní objednávky*.
    - Všechna tři ID práce, která mají hodnotu **Typ pracovního příkazu** *Doplnění*, mají stejná místa *Výběr* a *Vložení* v sekci **Řádky**:

        - **Výběr:** *02A01R5S1B*
        - **Vložení:** *06A01R2S1B*

    - Pro prodejní objednávku 1 byla vytvořena dvě ID práce.

1. Pro každou prodejní objednávku si poznamenejte ID práce.

V závislosti na množství, které máte k dispozici, se mohou vytvořená množství práce mírně lišit. Celkově by se však vytvořená záhlaví práce měla shodovat s tímto příkladem scénáře.

#### <a name="on-hand-inventory-license-plate-id"></a>ID registrační značky na skladě

Později v tomto scénáři budete používat mobilní aplikaci (nebo emulátor) Řízení skladu, kde musíte identifikovat registrační značku pro dokončení scénářů vychystávání a doplňování.

Chcete-li najít ID registrační značky, které budete později potřebovat, postupujte takto.

1. Přejděte na **Řízení zásob \> Dotazy a sestavy \> Zásoby na skladě**.
1. Vyberte **Zobrazit filtry** pro otevření podokna filtru.
1. Chcete-li získat poznávací značky pro scénář, zadejte následující kritéria filtrování. Použijte filtr *začíná na*.

    - **Číslo položky:** *T0100*
    - **Sklad:** *61*

1. Zvolte **Použít**.
1. V podokně akcí zvolte **Rozměry**.
1. V dialogovém okně **Zobrazení dimenzí** v části **Dimenze úložiště** vyberte všechny hodnoty.
1. V části **Transakce** vyberte **Číslo položky** a **Množství \<\> 0**.
1. Po dokončení vyberte **OK** a zavřete dialogové okno.
1. Mřížka **Na skladě** zobrazuje čísla registračních značek pro položku *T0100* na každém místě. Poznamenejte si poznávací značku, která je na každém místě, protože tyto informace budete potřebovat později.
1. Zavřete stránku.

### <a name="process-steps"></a>Kroky procesu

Provedete doplnění umístění skladu pro první dvě ID práce. Práce na třetím doplňování budou blokovány, dokud úroveň zásob v místě vyskladnění neklesne pod prahovou hodnotu.

#### <a name="replenishment"></a>Doplnění

1. Přihlaste se do mobilní aplikace Řízení skladu jako uživatel skladu *61*. (Zadejte *61* jako ID uživatele a *1* jako heslo.)
1. Přejděte na **Zásoby \> Doplnění**.

    Jste vyzváni, abyste dokončili první práci na doplnění. Zobrazí se číslo položky, množství a umístění pro vyskladnění.

1. V poli **LP** zadejte číslo registrační značky položky v zobrazeném umístění.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).

    Systém vygeneruje cílové číslo registrační značky pro novou registrační značku pro vybranou položku.

1. Hodnotu potvrďte výběrem tlačítka **OK**.

    Je ukázána práce vyskladnění, která dává uživateli pokyn k umístění cílové registrační značky do místa doplnění. Umístění *Vložení* by mělo být **06A01R2S1B**.

1. Potvrďte zadané údaje a vyberte **OK**.

    Zobrazí se zpráva „Práce dokončena“ a jsou zobrazeny podrobnosti o další úloze výběru doplňku: číslo položky, množství a umístění, ze kterého lze vybrat. Místo výběru bude stejné jako první místo doplnění. Proto bude registrační značka mít stejné ID registrační značky, jaké bylo použito pro první úkol doplnění.

1. Opakováním předchozích kroků dokončete doplňování pro druhý pracovní úkol. Množství a cílová registrační značka se budou lišit od množství a cílové registrační značky pro první pracovní úkol.

Po dokončení druhého doplňování práce se zobrazí zpráva „Práce dokončena“. Mobilní zařízení vás také informuje, že není k dispozici žádná práce, přestože některé práce na doplňování zbývají. K tomuto chování dochází, protože práce doplňování má stav dostupnosti *Zadržení* a je proto označen jako **Blokováno**.

Stav *Zadržení* byl spuštěn, protože profil umístění pro místo výběru, ke kterému je práce přiřazena, má hodnotu **Množství přetečení** *0,65 PL*. Dva předchozí pracovní úkoly doplňování naplnily umístění téměř na hranici přetečení pro položku *T0100*. (Převod jednotek pro položku je *1 PL = 100 ea* .) Proto by zbývající doplňovací práce způsobily, že umístění překročí limit přetečení.

Dokud nebude z místa vybrán dostatek zásob, aby byl pod položkou nabídky uvolnění práce v položce nabídky mobilního zařízení, zůstane toto doplňování blokováno.

#### <a name="sales-order-pick"></a>Výběr prodejní objednávky

Před dokončením zbývajícího úkolu doplňování musí být místo vyskladnění vyčerpáno ze zásoby na úroveň, na které lze zbývající část doplňování odblokovat. Jinými slovy, součet množství zásob na skladě v místě a množství doplňování nesmí překročit hodnota **Přetečené množství**. Pokud je tato částka menší než množství přetečení, zbývající doplňování bude odblokováno.

1. Přihlaste se do mobilní aplikace Řízení skladu jako uživatel skladu *61*. (Zadejte *61* jako ID uživatele a *1* jako heslo.)
1. Přejděte do **Výstupní \> Prodejní výdej**.
1. Zadejte první ID práce pro prodejní objednávku 1.

    Podívejte se na ID práce u prodejních objednávek, které jste si poznamenali dříve, na stránce **Podrobnosti o práci**. ID práce, které zde zadáte, vygeneruje výběrovou práci pro množství 10 ea ze dvou samostatných míst.

1. Vyberte **OK**.

    Stránka s úkolem **Prodejní objednávky: výběr** zobrazuje číslo položky, množství a umístění, ze kterého lze vybrat první umístění.

1. V poli **LP** zadejte číslo registrační značky položky v zobrazeném umístění.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).

    Stránka s úkolem **Prodejní objednávky: výběr** zobrazuje číslo položky, množství a umístění, ze kterého lze vybrat další umístění.

1. V poli **LP** zadejte číslo registrační značky položky v zobrazeném umístění.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).

    Stránka **Prodejní objednávky: Vložení** vám dá pokyn k odložení obou dokončených prací výběru na odchozí skladové místo.

1. Vyberte **OK**.

    Zobrazí se zpráva „Práce dokončena“.

1. Zadejte druhé ID práce pro prodejní objednávku 1.

    Pro toto pracovní ID existuje pouze jeden výběrový úkol.

1. Vyberte **OK**.

    Stránka s úkolem **Prodejní objednávky: výběr** zobrazuje číslo položky, množství a umístění, ze kterého lze vybrat.

1. V poli **LP** zadejte číslo registrační značky položky v zobrazeném umístění.

    Zadaná registrační značka bude jednou z registračních značek generovaných systémem z pracovních úkolů doplňování. Chcete-li se ujistit, že jste zachytili správné ID registrační značky, zkontrolujte zásoby na stránce **Seznam po ruce** pro položku, umístění a množství.

1. Vyberte tlačítko **OK** (symbol zaškrtnutí).
1. Potvrďte pokyny pro úlohu umístění do odchozího skladového místa.
1. Vyberte **OK**.

    Zobrazí se zpráva „Práce dokončena“.

Prodejní objednávka 2 je zablokována, protože úkol doplňování, ke kterému je připojen, není dokončen. V současné době je v místě vychystávání stále množství 30 ks a množství doplňování pro prodejní objednávku 2 je 60 ks. Součet zásob na skladě a zásob doplňování (90 ks) překračuje množství přetečení o 0,65 PL (nebo 65 ks). Před dokončením doplňovacích prací musí být vybrána prodejní objednávka 3.

1. Zadejte ID práce pro prodejní objednávku 3.

    Pro toto pracovní ID existuje pouze jeden výběrový úkol.

1. Vyberte **OK**.

    Stránka s úkolem **Prodejní objednávky: výběr** zobrazuje číslo položky, množství a umístění, ze kterého lze vybrat.

1. V poli **LP** zadejte číslo registrační značky položky v zobrazeném umístění.

    Zadaná registrační značka bude jednou z registračních značek generovaných systémem z pracovních úkolů doplňování. Chcete-li se ujistit, že jste zachytili správné ID registrační značky, zkontrolujte zásoby na stránce **Seznam po ruce** pro položku, umístění a množství.

1. Vyberte tlačítko **OK** (symbol zaškrtnutí).
1. Potvrďte pokyny pro úlohu umístění do odchozího skladového místa.
1. Vyberte **OK**.

    Zobrazí se zpráva „Práce dokončena“.

Jakmile je součet množství na skladě v místě vychystávání a množství doplňování pod prahem, budete moci zpracovat zbývající práci doplňování.

Vraťte se na stránku **Podrobnosti o práci** a všimněte si, že je dostupnost práce doplnění pro poslední kus doplnění (pro prodejní objednávku 2) *Otevřeno*, protože nyní je v místě dostatek prostoru na přijetí doplnění.

Nyní můžete tuto práci na doplňování zpracovat prostřednictvím mobilního zařízení.

1. Přejděte na **Zásoby \> Doplnění**.

    Jste vyzváni, abyste dokončili zbývající práci na doplnění. Zobrazí se číslo položky, množství a umístění pro vyskladnění.

1. V poli **LP** zadejte číslo registrační značky položky v zobrazeném umístění.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).

    Systém vygeneruje cílové číslo registrační značky pro novou registrační značku pro vybranou položku.

1. Hodnotu potvrďte výběrem tlačítka **OK**.

    Je ukázána práce vyskladnění, která dává uživateli pokyn k umístění cílové registrační značky do místa doplnění. Umístění *Vložení* by mělo být **06A01R2S1B**.

1. Potvrďte zadané údaje a vyberte **OK**.

    Obdržíte zprávy „Práce dokončena“ a „Žádná práce není k dispozici“.

Nyní si můžete vybrat prodejní objednávku 2. Když bylo dokončeno doplňování, které je spojeno s prodejní objednávkou, došlo k jeho odblokování.

1. Zadejte ID práce pro prodejní objednávku 2.

    Pro toto pracovní ID existuje pouze jeden výběrový úkol.

1. Vyberte **OK**.

    Stránka s úkolem **Prodejní objednávky: výběr** zobrazuje číslo položky, množství a umístění, ze kterého lze vybrat.

1. V poli **LP** zadejte číslo registrační značky položky v zobrazeném umístění.

    Zadaná registrační značka bude jednou z registračních značek generovaných systémem z pracovního úkolu doplňování. Chcete-li se ujistit, že jste zachytili správné ID registrační značky, zkontrolujte zásoby na stránce **Seznam po ruce** pro položku, umístění a množství.

1. Vyberte tlačítko **OK** (symbol zaškrtnutí).
1. Potvrďte pokyny pro úlohu umístění do odchozího skladového místa.
1. Vyberte **OK**.

    Zobrazí se zpráva „Práce dokončena“.

## <a name="notes-and-tips"></a>Poznámky a tipy

- Tato funkce pracuje se všemi typy doplňování: požadavek na vlnu, min / max, požadavek na zatížení a slotting.
- Pokud chcete, můžete ručně přepsat dostupnost práce doplňování pro každou hlavičku práce ze stránky **Podrobnosti o práci**.
- Když systém nastaví dostupnost práce při doplňování, vezme v úvahu veškerý inventář, který je již v místě před dokončením jakékoli práce
- Každá část práce na prodejní objednávce je spojena s konkrétní prací na doplnění. Neexistuje žádná odpovídající funkce dostupnosti prodejní práce.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]