---
title: Řazení práce řízené systémem
description: Toto téma uvádí informace o řazení práce řízeném systémem. Tato funkce umožňuje třídit a filtrovat pracovní příkazy, které systém předává uživatelům k provádění. Hodí se v situacích, kdy se k řízení procesu vydávání ze skladu využívají další kritéria.
author: Mirzaab
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: b433787f330de3634c59f7b1b2babfe07e3bdf09
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577809"
---
# <a name="system-directed-work-sequencing"></a>Řazení práce řízené systémem

[!include [banner](../includes/banner.md)]

Řazení práce řízené systémem umožňuje třídit a filtrovat pracovní příkazy, které systém předává uživatelům k provádění. Funkce je užitečná v situacích kdy se k řízení procesu výdeje ze skladu vyžadují další kritéria (např. čas dodávky, zóna výdeje, profil skladového místa nebo kombinace různých kritérií).

Tato funkce rozšiřuje současnou funkci výdeje řízeného systémem přidáním systémem řízeného pořadí dotazů, kde mohou uživatelé nastavovat pořadí a jeden nebo více dotazů, jež všechny vytvořené pracovní příkazy vyhodnocují. Pouze pracovní příkazy, jež splňují kritéria stanovená v nastavení položky nabídky mobilního zařízení, budou zachyceny a prezentovány.

Tato funkce proto umožňuje další optimalizaci procesů výdeje ze skladu. Identifikuje pracovní příkazy, které odpovídají zadaným kritériím, přiřadí je ke správné položce nabídky mobilního zařízení a poté je předloží pracovníkovi na základě konkrétní sady dovedností, zařízení pro výdej nebo jiného požadavku.

> [!NOTE]
> Pokud jsou nutná jiná kritéria, je třeba použít více položek nabídky mobilního zařízení.

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a>Zapnutí funkce Řazení práce řízené systémem v rámci celé organizace

Než můžete použít funkci Řazení práce řízené systémem, musíte ji v systému zapnout. Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba. Funkce je zde uvedena následujícím způsobem:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Řazení práce řízené systémem v rámci celé organizace*

## <a name="setup"></a>Nastavení

### <a name="make-demo-data-available"></a>Zpřístupnění ukázkových dat

Chcete-li s tímto scénářem pracovat pomocí hodnot prezentovaných v tomto tématu, musíte používat systém, ve kterém jsou nainstalována standardní ukázková data. Dále musíte vybrat právnickou osobu **USMF**. Scénář používá sklad *51* z ukázkových dat.

> [!IMPORTANT]
> Před vydáním objednávek do skladu zajistěte, aby skladová místa pro vyskladnění měla dostatečné množství zásob pro všechny položky objednávek.
>
> Výchozí data USMF by měla tento scénář podporovat. Pokud nepoužíváte ukázková data, zkontrolujte nastavení **Směrnice skladového místa** a zjistěte tak, která výdejní skladová místa se použijí pro výdej prodejní objednávky. Pokud musíte upravit zásoby, můžete vytvořit ruční pohyby, použít doplnění nebo využít jakýkoli jiný tok.

### <a name="set-up-a-mobile-device-menu-item"></a>Vytvoření nabídky mobilního zařízení

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V seznamu položek nabídky mobilních zařízení vyberte **Prodejní výdej – systém**. Požadovaná položka nabídky by již měla existovat. 
1. Potvrďte následující nastavení:

    - Na záložce s náhledem **Obecné** by měla být v poli **Řídí:** hodnota *Řízeno systémem*.
    - Na záložce s náhledem **Třídy práce** by se mělo zobrazit následující nastavení.

        | ID pracovní třídy | Typ pořadí pracovních činností |
        |---|---|
        | Prodej. | Prodejní objednávky |
        | Výdej PO | Prodejní objednávky |

1. V podokně Akce vyberte možnost **Dotazy na řazení práce řízené systémem**.
1. Vyberte možnost **Upravit**.
1. Smaže stávající řádek a akci potvrďte výběrem možnosti **Ano**.
1. V podokně Akce vyberte možnost **Nový** a vytvořte řádek.
1. Na novém řádku nastavte následující hodnoty:

    - **Pořadové číslo:** *1*
    - **Pole Popis:** *Množství práce menší než 20, sestupně*

1. Zvolte **Uložit**.
1. V podokně Akce vyberte možnost **Upravit dotaz**.
1. Na kartě **Spojení** rozbalte hierarchii spojení a zobrazte tabulku **Řádky práce**.
1. Vyberte spojení tabulky **Řádky práce**.
1. Zvolte **Přidat propojení tabulek**.
1. Zobrazí se seznam, v něm vyhledejte a vyberte řádek, který má následující nastavení:

    - **Režim spojení:** *n:1*
    - **Vztah:** *Skladová místa (skladové místo)*

1. Zvolte **Zvolit**.

    Skladová místa se přidávají do spojení tabulky.

1. Na kartě **Třídění** vyberte možnost **Přidat** a přidejte řádek.
1. Na novém řádku nastavte následující hodnoty:

    - **Tabulka:** *Řádky práce*
    - **Odvozená tabulka:** *Řádky práce*
    - **Pole:** *Množství práce* (V poli zprávy, které e zobrazí, klikněte na **Ano** a třídění se přidá do tohoto pole.)
    - **Směr hledání:** *Sestupně*

1. Vyberte kartu **Oblast**.

    Pokud by do řazení měla být zahrnuta pouze určitá pracovní kritéria, můžete je zadat na kartě **Oblast**. V tomto příkladu chcete zahrnout pouze práci, kde je množství menší než 20 ks (nejnižší měrná jednotka).

    Všimněte si, že některé řádky jsou již zahrnuty. Tyto řádky neodstraňujte.

1. Chcete-li přidat řádek, vyberte **Přidat řádek**.
1. Na novém řádku nastavte následující hodnoty:

    - **Tabulka:** *Řádky práce*
    - **Odvozená tabulka:** *Řádky práce*
    - **Pole:** *Zásoby – množství práce*
    - **Kritéria:** *\<20* (méně než 20)

1. Chcete-li přidat další řádek, vyberte **Přidat řádek**.
1. Na novém řádku nastavte následující hodnoty:

    - **Tabulka:** *Řádky práce*
    - **Odvozená tabulka:** *Řádky práce*
    - **Pole:** *Typ práce*
    - **Kritéria:** *Výdej*

1. Chcete-li přidat další řádek, vyberte **Přidat řádek**.
1. Na novém řádku nastavte následující hodnoty:

    - **Tabulka:** *umístění*
    - **Odvozená tabulka:** *Skladová místa*
    - **Pole:** *ID profilu skladového místa*
    - **Kritéria:** *!STAGE*

        > [!IMPORTANT]
        > Nezapomeňte zahrnout na vykřičník (*!*) před *STAGE*.

1. Klikněte **OK**. Dotaz se uloží a zavře.
1. Zvolte **Uložit**.
1. Zavřete stránku a vraťte se na stránku **Položky nabídky mobilního zařízení**.

> [!NOTE]
> Toto nastavení definuje kritéria, která se použijí k vložení způsobilé práce do položky nabídky mobilního zařízení. Pokud do dotazu přidáte další řádky kritérií, systém použije jako první ten řádek dotazu, který má nejnižší pořadové číslo. Jinými slovy, veškerá způsobilá práce s pořadovým číslem 1 bude uživateli prezentována jako první, následovat bude veškerá práce s pořadovým číslem 2. Pokud je tedy třeba používat společně konkrétní oblast a třídění, je třeba je zadat v témže dotazu na řazení práce řízené systémem.
>
> Toto nastavení zachytí jakoukoli práci, která má alespoň jeden řádek, kde je množství menší než 20 ks. Pokud tedy práce obsahuje řádek, kde je množství přesně 20 ks nebo více než 20 ks, bude platit pokud současně obsahuje také alespoň jeden řádek, kde je množství menší než 20 ks.

### <a name="location-directives"></a>Směrnice skladového místa

Pokud používáte výchozí data Contoso, nebude dotaz na akci směrnice skladového místa vyžadovat žádné změny. Chcete-li však mít jistotu, že směrnice skladového místa zachytí položky na prodejních objednávkách, když tuto funkci použijete v prostředí mimo Contoso, vytvořte novou směrnici skladového místa. Chcete-li ověřit nastavení v ukázkovém prostředí, postupujte takto.

1. Přejděte do nabídky **Řízení skladu** \> **Nastavení** \> **Směrnice skladového místa**.
1. V poli **Typ pracovního příkazu** vyberte možnost *Prodejní objednávky*.
1. Vyberte směrnici skladového místa s označením *51 Výdej*.
1. Na záložce s náhledem **Akce směrnice skladového místa** vyberte řádek pro akci **Výdej**.
1. Vyberte možnost **Upravit dotaz** nad mřížkou.
1. Zkontrolujte dotaz **Oblast**.

    1. Najděte řádek, kde má pole **Pole** nastavenou hodnotu *Skladové místo*.
    2. Ujistěte se, že je pole **Kritéria** prázdné (tj. neexistují žádná omezení).

## <a name="scenario"></a>Scénář

### <a name="create-sales-order-picking-work"></a>Vytvoření práce výdeje prodejní objednávky

Před spuštěním výdeje řízeného systémem je třeba vytvořit výstupní práci. Pro tento scénář vytvořte čtyři prodejní objednávky, které vycházejí ze zadaných dotazů na řazení práce řízené systémem.

Rezervujte si množství zásob pro každou prodejní objednávku. Rezervované zásoby nemohou tedy být ze skladu odebrány na jiné objednávky, dokud se nezruší rezervace zásob nebo její část.

Poté uvolníte každou prodejní objednávku do skladu a vytvoříte výstupní práci.

#### <a name="sales-order-1"></a>Prodejní objednávka 1

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. V podokně Akce vyberte možnost **Nová** a vytvořte prodejní objednávku 1.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - V sekci **Odběratel** zadejte do pole **Účet odběratele** hodnotu *US-004*.
    - V sekci **Všeobecné** zadejte do pole **Sklad** hodnotu *51*.

1. Zvolte **OK** a zavřete dialogové okno. Poznamenejte si číslo prodejní objednávky.
1. Přidejte řádek do nové prodejní objednávky a nastavte následující hodnoty:

    - **Číslo položky:** *M9200*
    - **Množství:** *20*

1. V nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.
1. Na stránce **Rezervace** vyberte **Rezervovat šarži** k rezervování zásob.
1. Zavřete stránku **Rezervace**.
1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**. Vytvoří se práce pro sklad.

    Zobrazí se informační zprávy určující ID vlny a ID dodávky, jež byly vytvořeny pro tuto prodejní objednávku.

#### <a name="sales-order-2"></a>Prodejní objednávka 2

1. V podokně Akce vyberte možnost **Nová** a vytvořte prodení objednávku 2.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - **Účet zákazníka:** *US-007*
    - **Sklad:** *51*

1. Zvolte **OK** a zavřete dialogové okno. Poznamenejte si číslo prodejní objednávky.
1. Přidejte řádek do nové prodejní objednávky a nastavte následující hodnoty:

    - **Číslo položky:** *M9200*
    - **Množství:** *5*

1. Chcete-li přidat druhý řádek, klikněte na **Přidat řádek** a zadejte následující hodnoty:

    - **Číslo položky:** *M9201*
    - **Množství:** *1*

1. Proveďte rezervaci zásob pro oba řádky.
1. Uvolněte objednávku do skladu.

#### <a name="sales-order-3"></a>Prodejní objednávka 3

1. V podokně Akce vyberte možnost **Nová** a vytvořte prodení objednávku 3.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - **Účet zákazníka:** *US-009*
    - **Sklad:** *51*

1. Zvolte **OK** a zavřete dialogové okno. Poznamenejte si číslo prodejní objednávky.
1. Přidejte řádek do nové prodejní objednávky a nastavte následující hodnoty:

    - **Číslo položky:** *M9200*
    - **Množství:** *7*

1. Chcete-li přidat druhý řádek, klikněte na **Přidat řádek** a zadejte následující hodnoty:

    - **Číslo položky:** *M9202*
    - **Množství:** *8*

1. Proveďte rezervaci zásob pro oba řádky.
1. Uvolněte objednávku do skladu.

#### <a name="sales-order-4"></a>Prodejní objednávka 4

1. V podokně Akce vyberte možnost **Nová** a vytvořte prodení objednávku 4.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - **Účet zákazníka:** *US-010*
    - **Sklad:** *51*

1. Zvolte **OK** a zavřete dialogové okno. Poznamenejte si číslo prodejní objednávky.
1. Přidejte řádek do nové prodejní objednávky a nastavte následující hodnoty:

    - **Číslo položky:** *M9200*
    - **Množství:** *25*

1. Chcete-li přidat druhý řádek, klikněte na **Přidat řádek** a zadejte následující hodnoty:

    - **Číslo položky:** *M9202*
    - **Množství:** *10*

1. Proveďte rezervaci zásob pro oba řádky.
1. Uvolněte objednávku do skladu.

### <a name="get-work-ids-for-the-work-that-was-created"></a>Získání ID práce pro vytvořenou práci

1. Přejděte do **Řízení skladu \> Práce \> Podrobnosti práce**.
1. Filtrujte pole **Sklad** tak, aby se zobrazila pouze práce pro sklad *51*.
1. Měla by se vytvořit čtyři ID práce. Pro každou prodejní objednávku si poznamenejte ID práce.

    | ID prodejní objednávky | ID práce | Množství práce |
    |---|---|---|
    | Prodejní objednávka 1 | ID práce 1 | 20 ks |
    | Prodejní objednávka 2 | ID práce 2 | 6 ks (součet obou řádků) |
    | Prodejní objednávka 3 | ID práce 3 | 15 ks (součet obou řádků) |
    | Prodejní objednávka 4 | ID práce 4 | 35 ks (součet obou řádků) |

Před spuštěním toku na mobilním zařízení se ujistěte, že pro sklad *51* je pouze práce, kterou jste právě vytvořili, ve stavu *Otevřená* a že typ pracovního příkazu je *Prodejní objednávka*. V opačném případě se výsledky testu mohou lišit, protože výdej řízený systémem bude zahrnovat veškerou způsobilou práci.

1. Přejděte do **Řízení skladu \> Práce \> Výstupní \> Otevřená prodejní práce**.
1. V mřížce **Otevřená prodejní práce** filtrujte pole **Sklad** tak, aby se zobrazila pouze práce pro sklad *51*.
1. Ověřte, že jsou zobrazeny pouze čtyři ID práce, jež jste předtím vytvořili.
1. Zavřete stránku **Práce**.

### <a name="mobile-device-flow-execution"></a>Realizace toku na mobilním zařízení

Na základě nastavení bude systém dodávat uživatelskou práci, jež bude tříděna od nejvyššího množství na řádku práce po nejnižší. Množství na každém řádku musí být menší než 20 ks.

Pamatujte, že toto nastavení zachytí jakoukoli práci, která má alespoň jeden řádek, kde je množství menší než 20 ks. Pokud tedy práce obsahuje další řádek, kde je množství přesně 20 ks nebo více než 20 ks, bude platit také.

#### <a name="mobile-app"></a>Aplikace pro mobilní zařízení

1. Přihlaste se do skladové aplikace jako uživatel skladu *51*.
1. Přejděte do **Výstupní \> Prodejní výdej – systém**.

    Je prezentován krok výdeje pro ID práce *4*. Toto ID práce je uvedeno jako první kvůli pořadí dotazů řízenému systémem, kde jste určili, že by pro práce mělo být určováno pořadí na základě sestupného množství na řádku práce.

1. Proveďte požadovaný výdej a zaskladnění a zavřete ID práce.

    Dále je prezentováno ID práce *3*. Jeden z řádku práce je další v pořadí na základě množství na řádku práce.

1. Proveďte výdej a zaskladnění a zavřete ID práce.

    Dále je prezentováno ID práce *2*. Tento řádek práce výdeje je další v pořadí.

1. Proveďte výdej a zaskladnění a zavřete ID práce.

    Žádná další práce by se objevit neměla. ID práce *1* není způsobilé pro tuto položku nabídky mobilního zařízení, protože dotaz určuje, že záhlaví práce jsou brána v úvahu pouze v případě, že množství na řádcích práce je menší než 20 ks.

## <a name="tips"></a>Tipy

Dotazy na řazení práce řízené systémem jsou *inkluzivní*. Na tuto skutečnost při nastavování nezapomínejte. Například chcete, aby konkrétní položka nabídky zpracovávala pouze práci, kde je jako jednotka práce *ks* a zadáte toto omezení na kartě **Oblast** dotazu. V tom případě všechny práce, kde má alespoň jeden řádek práce nastavenou jednotku *ks*, budou předloženy pracovníkovi. Tato práce proto může zahrnovat také práci, kde mají řádky práce jinou jednotku než *ks* (např. *krabice* nebo *paleta*). Dotaz vyloučí pouze práci, kde nemá žádný řádek práce nastavenou jednotku práce *ks*.

Proto bylo v příkladu v tomto scénáři ID práce *4* také zachyceno dotazem. Při vytvoření byly přidány dva řádky: jeden pro 25 ks druhý pro 10 ks. Práce je prezentována uživateli, protože alespoň jeden řádek práce má množství menší než 20 ks.

V závislosti na scénáři můžete tomuto chování bránit s využitím dělení práce.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]