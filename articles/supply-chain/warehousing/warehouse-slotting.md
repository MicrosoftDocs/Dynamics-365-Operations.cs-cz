---
title: Skladový slotting
description: Toto téma uvádí informace o skladovém slottingu. Skladový slotting umožňuje konsolidovat poptávku podle položek a měrných jednotek z objednávek, jež jsou ve stavu Objednáno, Rezervováno nebo Uvolněno. Pomáhá skladovým manažerům inteligentně plánovat výdejová skladová místa, než uvolní objednávky do skladu a vytvoří výdejní práce.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: ed9e6eae2ecc8de8d5eeef4699678e93dd74f193
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017407"
---
# <a name="warehouse-slotting"></a>Skladový slotting

[!include [banner](../includes/banner.md)]

Skladový slotting umožňuje konsolidovat poptávku podle položek a měrných jednotek z objednávek, jež jsou ve stavu *Objednáno* , *Rezervováno* nebo *Uvolněno*. Vygenerovanou poptávku je pak možné aplikovat na skladová místa, jež budou použita k výdeji, na základě množství, měrných jednotek, fyzických rozměrů, pevných skladových míst a dalších parametrů. Poté, co byl vytvořen slottingový plán, je možné vytvořit práce doplňování, aby bylo do každého skladového místa dodáno vhodné množství zásob.

Tato funkce pomáhá skladovým manažerům inteligentně plánovat výdejová skladová místa, než uvolní objednávky do skladu a vytvoří výdejní práce.

## <a name="turn-on-the-warehouse-slotting-feature"></a>Zapnutí funkce skladového slottingu

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Funkce skladového slottingu*

## <a name="set-up-warehouse-slotting"></a>Nastavení skladového slottingu

Chcete-li používat skladový slottingu, musíte v systému nastavit následující prvky.

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a>Vytvoření úrovní měrných jednotek pro slotting

Úrovně měrných jednotek umožňují pro účely slottingu seskupovat více měrných jednotek. Pokud se například ve stejné výdejové oblasti vydávají různé velikosti krabic, lze vytvořit jednu úroveň pro všechny velikosti. **Pro každou měrnou jednotku, která by měla být součástí úrovně, je třeba vytvořit řádek.**

1. Přejděte do **Řízení skladu \> Nastavení \> Doplnění \> Úrovně měrných jednotek pro slotting**.
1. Zvolte **Nové**.
1. V záhlaví nastavte následující hodnoty:

    - **Úroveň měrné jednotky:** *EaBoxPl*
    - **Popis:** *Každá krabice na paletě*

1. Zvolte **Uložit**.
1. Na záložce s náhledem **Měrné jednotky** přidejte řádek do mřížky výběrem možnosti **Nový**.
1. Na novém řádku nastavte následující hodnoty:

    - **Jednotka:** *Krabice*
    - **Popis:** Toto pole ponechte prázdné. Vyplní se automaticky při uložení změn.
    - **Třída jednotek:** *Množství*

1. Chcete-li přidat druhý řádek do mřížky, klikněte na tlačítko **Nový**.
1. Na novém řádku nastavte následující hodnoty:

    - **Jednotka:** *EA*
    - **Popis:** Toto pole ponechte prázdné. Vyplní se automaticky při uložení změn.
    - **Třída jednotek:** *Množství*

1. Chcete-li přidat třetí řádek do mřížky, klikněte na tlačítko **Nový**.
1. Na novém řádku nastavte následující hodnoty:

    - **Jednotka:** *PL*
    - **Popis:** Toto pole ponechte prázdné. Vyplní se automaticky při uložení změn.
    - **Třída jednotek:** *Množství*

1. Kliknutím na tlačítko **Uložit** uložte úroveň.

### <a name="create-a-directive-code-for-slotting"></a>Vytvoření kódu kód předpisu pro slotting

Musíte vybrat kód předpisu, který má být přiřazen k šabloně.

1. Přejděte na **Řízení skladu \> Nastavení \> Kódy předpisů**.
1. V podokně akcí zvolte **Nový**.
1. V poli **Kód předpisu** zadejte hodnotu *Slotting*.
1. V poli **Popis předpisu** zadejte hodnotu *Slotting*.

### <a name="set-up-slotting-templates"></a>Nastavení šablon slottingu

Každá šablona slottingu určuje, jak se přiřazují zásoby do skladových míst v konkrétním skladu. Každá šablona musí obsahovat řádek pro každou specifikaci slottingu. Postupy v této části využijte k nastavení šablon slottingu.

1. Přejděte na **Řízení skladu \> Nastavení \> Doplnění \> Šablony slottingu**.
1. Chcete-li vytvořit šablonu, klikněte na **Nová**.

Dále musíte nastavit záhlaví šablony, specifikaci slottingu a směrnice skladového místa, jak se vysvětluje v následujících částech.

#### <a name="set-up-a-slotting-template-header"></a>Nastavení záhlaví šablony slottingu

1. V záhlaví šablony nastavte následující hodnoty:

    - **Šablona slottingu:** _61_
    - **Popis:** _61_
    - **Typ poptávky:** *Prodejní objednávka*

        V současné době je jediný podporovaný typ poptávky *Prodejní objednávka*.

    - **Strategie poptávky:** _Objednáno_

        K dispozici pro toto pole jsou následující hodnoty:

        - **Objednáno** – za poptávku je třeba považovat kompletní objednané množství na prodejní objednávce.
        - **Rezervováno** – pouze rezervovaná (fyzická a objednávaná) množství z řádků objednávek lze považovat za poptávku.

    - **Sklad:** _61_
    - **Povolit použití nerezervovaných množství ve vlnové poptávce:** _Ano_

Můžete také určit dotaz ke zúžení oboru vyhodnocené poptávky.

#### <a name="set-up-slotting-specifications-for-each-template"></a>Nastavení specifikací slottingu pro jednotlivé šablony

Pro každou vytvořenou šablonu přidejte pro každou specifikaci slottingu řádek. Postupujte podle následujících kroků.

1. Na záložce s náhledem **Podrobnosti šablony slottingu** vytvoříte řádek šablony kliknutím na **Nový**.
1. Na novém řádku nastavte následující hodnoty:

    - **Posloupnost:** _1_
    - **Popis:** _Pevné skladové místo_
    - **Minimální množství:** _1_

        Toto pole definuje minimální množství z poptávky, jež řádek vyžaduje.

    - **Maximální množství:** _1000000_

        Toto pole definuje maximální množství z poptávky, jež je pro daný řádek platné.

    - **Jednotka:** Pole ponechejte prázdné.

        Toto pole definuje měrnou jednotku, jež se využívá v definici minimálního a maximálního množství.

    - **Úroveň měrné jednotky:** _EaBoxPl_

        Toto pole definuje měrné jednotky poptávky, jež jsou pro daný řádek platné. (Další informace naleznete v části [Nastavení úrovní měrných jednotek pro slotting](#unit-tiers) výše v tomto tématu.)

    - **Kritéria přiřazení slotu:** _Zvážit množství_

        K dispozici pro toto pole jsou následující hodnoty:

        - **Předpokládat prázdné** – tento systém by měl předpokládat, že všechna skladová místa ve výdejové oblasti jsou prázdná a nemělo by se kontrolovat, zda v nich nejsou zásoby.
        - **Zvážit množství** – tento systém by měl kontrolovat skladová míst ve výdejové oblasti, aby v nich nebyly zásoby; pokud narazí na skladová místa, jež nejsou prázdná, měl by je přeskočit.

    - **Kód předpisu:** _Slotting_

        Toto pole definuje směrnici skladového místa, jež se používá k vyhledání skladového místa práce doplňování.

    - **Skladové místo pro přeplnění:** Toto pole nechte prázdné.

        Toto pole definuje skladové místo, do něhož se naskladňují zásoby, pokud se při zpracování řádku nedaří najít skladové místo pro dané množství.

    - **Povolit přerušení:** _Ano_

        Je-li u této možnosti nastavena hodnota *Ano* , v případě, že u určité poptávky nelze provést slotting, se vytvoří pohyb, kterým budou zásoby odebrány ze skladových míst, kde se nacházejí zásoby, ale kde nic nebylo zpracováno pomocí slottingu. Šablona se poté spustí znovu. Tentokrát bude ignorovat zásoby v daných skladových místech. Tato funkce funguje nejlépe, když je v poli **Kritéria přiřazení slotu** zadána hodnota _Zvážit množství_.

    - **Použití pevného skladového místa:** _Pouze pevná skladová místa pro produkt_

        K dispozici pro toto pole jsou následující hodnoty:

        - **Pevná a nepevná skladová místa** – systém by se neměl omezovat na použití pouze pevných skladových míst.
        - **Pouze pevná skladová místa pro produkt** – systém by měl provádět slotting pouze na skladová místa, jež jsou pro produkt pevnými skladovými místy.
        - **Pouze pevná skladová místa pro variantu produktu** – systém by měl provádět slotting pouze na skladová místa, jež jsou pro variantu produktu pevnými skladovými místy.

1. Zvolte **Uložit**.
1. Chcete-li vytvořit druhý řádek šablony, klikněte na tlačítko **Nový**.
1. Na novém řádku nastavte následující hodnoty:

    - **Posloupnost:** _2_
    - **Popis:** _Jiný_
    - **Minimální množství:** _1_
    - **Maximální množství:** _1000000_
    - **Jednotka:** Pole ponechejte prázdné.
    - **Úroveň měrné jednotky:** _EaBoxPl_
    - **Kritéria přiřazení slotu:** _Zvážit množství_
    - **Kód předpisu:** _Slotting_
    - **Skladové místo pro přeplnění:** Toto pole nechte prázdné.
    - **Povolit přerušení:** _Ano_
    - **Použít pevná skladová místa:** _Pevná a nepevná skladová místa_

    V dotazu pro druhý řádek nyní určíte kritéria, jež se použijí k určení skladových míst, na něž může proběhnout slotting poptávky z příslušného řádku.

1. Vyberte řádek, kde má pole **Pořadí** nastavenou hodnotu *2*.
1. Vyberte **Upravit dotaz**.
1. Na kartě **Oblast** přidejte řádek do mřížky výběrem možnosti **Přidat**.
1. Na novém řádku nastavte následující hodnoty:

    - **Tabulka:** *umístění*
    - **Odvozená tabulka:** *Skladová místa*
    - **Pole:** *ID profilu skladového místa*
    - **Kritéria:** *Výdej-06* (Klikněte v poli na dvojité plus \[**++**\], rozbalí se seznam, poté vyberte *Výdej-06* - *Výdejová lokalita 6*.)

1. Vyberte **OK**.

#### <a name="set-up-location-directives"></a>Nastavit směrnice skladových míst

Musí se nastavit alespoň jedna směrnice skladového místa, jež bude podporovat výběr slottingu. Chcete-li nastavit novou *směrnici skladového místa doplnění* pro skladová místa podporující výběr slottingu, využijte procedury popsané v této části.

1. Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.
1. V levém podokně vyberte v poli **Typ pracovního příkazu** hodnotu *Doplnění*.
1. V podokně akcí zvolte **Nový**.
1. V záhlaví nové směrnice skladového místa zadejte v poli **Název** hodnotu *61 Výběr slotu*.

##### <a name="configure-the-location-directives-fasttab"></a>Konfigurace záložky s náhledem pro Směrnice skladového místa

1. Na záložce s náhledem **Směrnice skladového místa** natavte následující hodnoty. Potvrďte výchozí hodnoty pro všechna ostatní pole.

    - **Typ práce:** _Výdej_
    - **Lokalita:** _6_
    - **Sklad:** _61_
    - **Kód předpisu:** _Slotting_

1. Chcete-li, aby byla dostupná záložka s náhledem **Řádky** , klikněte na **Uložit**.

##### <a name="configure-the-lines-fasttab"></a>Konfigurace záložky s náhledem Řádky

1. Na záložce s náhledem **Řádky** vytvořte řádek výběrem tlačítka **Nový**.
1. Na novém řádku nastavte následující hodnoty. Potvrďte výchozí hodnoty pro všechna ostatní pole.

    - **Od množství:** _0_
    - **Do množství:** _1000000_

1. Chcete-li, aby byla dostupná záložka s náhledem **Akce směrnice skladového místa** , klikněte na **Uložit**.

##### <a name="configure-the-location-directive-actions-fasttab"></a>Konfigurace záložky s náhledem pro Akce směrnice skladového místa

1. Na záložce s náhledem **Akce směrnice skladového místa** vytvořte řádek výběrem tlačítka **Nový**.
1. Na novém řádku nastavte následující hodnoty. Potvrďte výchozí hodnoty pro všechna ostatní pole.

    - **Název:** _Hromadný_
    - **Strategie:** _Žádná_

1. Kliknutím na **Uložit** zpřístupníte tlačítko **Upravit dotaz**.

##### <a name="edit-the-query"></a>Upravit dotaz

1. Na záložce s náhledem **Akce směrnic skladového místa** vyberte možnost **Upravit dotaz**.
1. Na kartě **Oblast** přidejte řádek do mřížky výběrem možnosti **Přidat**.
1. Na novém řádku nastavte následující hodnoty:

    - **Tabulka:** *umístění*
    - **Odvozená tabulka:** *Skladová místa*
    - **Pole:** *ID zóny*
    - **Kritéria:** *Hromadné* (Klikněte v poli na dvojité plus \[**++**\], rozbalí se seznam, poté vyberte *Bulk*.)

1. Vyberte **OK**.

## <a name="scenario"></a>Scénář

### <a name="set-up-the-scenario"></a>Nastavení scénáře

Pro tento scénář použijte předdefinovaná ukázková data a vytvořte záznamy, jak se popisuje v této části.

#### <a name="use-the-usmf-sample-data"></a>Použití ukázkových dat USMF

Chcete-li s tímto scénářem pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.

#### <a name="create-demand"></a>Vytvoření poptávky

Postupujte podle těchto kroků a vytvořte poptávku, na kterou použijete slotting.

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Klepnutím na možnost **Nová** vytvořte novou prodejní objednávku.
1. V dialogovém okně **Vytvořit prodejní objednávku** vyberte v poli **Účet odběratele** hodnotu _US-007_.
1. V poli **Sklad** zvolte _61_.
1. Vyberte **OK**.
1. Otevře se nová prodejní objednávka. Zahrnuje prázdný řádek na záložce s náhledem **Řádky prodejní objednávky**. Na tomto řádku nastavte následující hodnoty:

    - **Položka:** _L0101_
    - **Množství:** _20_

1. Chcete-li přidat nový řádek, klikněte na **Přidat řádek** a zadejte následující hodnoty:

    - **Položka:** _T0100_
    - **Množství:** _8_

1. Zvolte **Uložit**.
1. Klepnutím na možnost **Nová** vytvořte druhou prodejní objednávku.
1. V dialogovém okně **Vytvořit prodejní objednávku** vyberte v poli **Účet odběratele** hodnotu _US-008_.
1. V poli **Sklad** zvolte _61_.
1. Otevře se nová prodejní objednávka. Zahrnuje prázdný řádek na záložce s náhledem **Řádky prodejní objednávky**. Na tomto řádku nastavte následující hodnoty:

    - **Položka:** _T0100_
    - **Množství:** _1_

1. Zvolte **Uložit**.

### <a name="walk-through-a-typical-slotting-scenario"></a>Vyzkoušení obvyklého scénáře slottingu

Když jsou splněny všechny nezbytné předpoklady, jak se popisuje v předchozí části, můžete vyzkoušet tuto funkci pomocí cvičení v této části.

#### <a name="generate-demand"></a>Generovat poptávku

1. Přejděte na **Řízení skladu \> Nastavení \> Doplnění \> Šablony slottingu** a vyberte šablonu slottingu, kterou jste předtím vytvořili.
1. V podokně Akce klikněte na možnost **Generovat poptávku**. Tento příkaz vyhodnocuje veškerou poptávku, jež se nachází v systému a shoduje se s dotazem dle šablony slottingu. Celková poptávka napříč všemi objednávkami je pak konsolidována do jednoho řádku na množství / měrnou jednotku. Po dokončení procesu se zobrazí informační zpráva.

#### <a name="slotting-demand"></a>Poptávka na slotting

*Poptávka na slotting* ukazuje výsledky generování poptávky na základě nastavení šablony slottingu.

- V podokně Akce vyberte **poptávka na slotting** , zobrazí se výsledky příkazu **Generovat poptávku**. Řádky poptávky na slotting lze upravovat. Můžete smazat řádek, přidat nový řádek nebo upravit podrobnosti řádku.

> [!NOTE]
> Poptávku lze upravit ručně nebo ji můžete importovat z externího systému pomocí správy dat. Ať už je v poptávce na slotting cokoli, bude to použito v dalším kroku, bez ohledu na to, odkud to bylo získáno.

#### <a name="locate-demand"></a>Vyhledat poptávku

Po vygenerování poptávky musíte použít příkaz **Vyhledat poptávku** k vygenerování *plánu slottingu*.

- V podokně Akce klikněte na možnost **Vyhledat poptávku**. Spustí se proces slottingu. Po dokončení procesu se zobrazí informační zpráva.

#### <a name="slotting-plan"></a>Plán slottingu

Plán slottingu ukazuje skladová místa, k nimž byly přiřazeny jednotlivé položky a jednotlivá množství, zda bylo použito přeplnění, zda byla vytvořena práce s přerušením a jaká šablona bylo pro daný řádek použita. **Jakákoli poptávka, která nemohla být zpracována formou slottingu, se zvýrazní červeně.**

- V podokně Akce vyberte **Plán slottingu** , zobrazí se výsledky.

#### <a name="create-replenishment"></a>Vytvoření doplnění

Po vytvoření plánu slottingu musíte na základě tohoto plánu vytvořit *práce doplnění*.

- V podokně Akce zvolte **Spustit doplnění**. Po dokončení procesu se zobrazí informační zpráva. Tato zpráva označuje počet záhlaví, jež byla vytvořena pro ID sestavení práce.

Směrnice skladového místa, jež budou použity, se identifikují na základě kódu předpisu, který je specifikován na každém řádku šablony.

## <a name="tips"></a>Tipy

### <a name="set-up-automatic-slotting"></a>Nastavení automatického slottingu

Po přípravě všech povinných prvků můžete nastavit automatizaci slottingu tak, aby se slotting prováděl automaticky. Postupujte takto.

1. Přejděte na **Řízení skladu \> Doplnění \> Provádění slottingu**.
1. Určete kroky slottingu, jež se mají provést. Vyberte jeden nebo více z následujících kroků slottingu:

    - Generovat poptávku
    - Vyhledat poptávku
    - Vytvořit práci doplnění

    > [!NOTE]
    > Kroky slottingu jsou progresivní. Pokud chcete vybrat krok *Vyhledat poptávku* , musíte nejprve vybrat *Generovat poptávku*.

1. Určete šablonu slottingu, kterou chcete použít.
1. Pokud chcete spouštět běh automaticky, nastavte opakování.

Pro cvičení ve scénáři **nenastavujte** automatické spouštění slottingu.
