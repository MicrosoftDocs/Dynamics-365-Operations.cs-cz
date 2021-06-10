---
title: Tisk štítků vlny
description: Toto téma popisuje tisk popisků vlny a vysvětluje, jak je nastavit.
author: perlynne
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 14a32f7fc4608ef8910646f80786a188c46dc89d
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102607"
---
# <a name="wave-label-printing"></a>Tisk štítků vlny

[!include [banner](../includes/banner.md)]

Tisk popisků vlny nabízí alternativní přístup k tisku štítků zavedením nové metody vlnových kroků, která umožňuje vytvářet a tisknout štítky přímo ze šablony vln během provádění vln. Proto budou štítky již k dispozici dříve, než pracovníci spustí pracovní příkaz na mobilním zařízení. Pracovníci pak mohou při sběru namísto po sběru připojit požadované štítky.

Tisk popisků vlny používá k vytvoření rozložení štítků programovací jazyk Zebra (ZPL). Rozložení štítků je rozděleno do tří částí (záhlaví, tělo a zápatí), aby bylo možné vytvořit štítky, které mají opakující se strukturu. Šablony vlnových štítků říkají systému, které rozvržení štítků se má použít. Uživatelé mohou určit, která tiskárna bude použita. Mohou také tisknout štítky na více tiskáren současně, jak vyžadují. Stránka **Historie popisků vlny** zobrazuje záznam všech štítků, které byly vytvořeny pomocí tohoto nastavení.

Štítky můžete tisknout a třídit na základě záhlaví práce, můžete tisknout štítky přestávky na pracovní hlavičku a můžete tisknout štítky obsahu kontejneru, štítky velkých písmen a další podobné štítky.

> [!NOTE]
> Tato funkce nenahrazuje stávající funkce tisku štítků, která je založena na směrování dokumentů.

Tisk popisků vlny nabízí následující vylepšení:

- Štítky tiskněte podle počtu kartonů na jednu pracovní linku bez použití kontejnerizace. („Karton“ je jednotka, která je určena na řádcích skupin sekvencí jednotek.)
- Vytiskněte několik různých štítků (například štítky kartonů a palet).
- Zahrňte výčet štítků (například 1/124, 2/124, ... 124/124) a definujte rozsah výčtu (například pracovní linie, nákladová linie nebo zásilka).
- Před vygenerováním přepravního dokladu vytvořte a vytiskněte ID přepravního dokladu na štítky.
- Pro každý karton vytvořte jedinečný kód sériového přepravního kontejneru (SSCC) a vložte jej do každého štítku.
- Vytvořte číselné sekvence kompatibilní s GS1 pro ID přepravních dokladů a SSCC.
- Opakovaně tiskněte štítky z mobilních zařízení i z bohatého klienta.
- Anulujte štítky (například ve scénářích krátkého výběru) a znovu je vytiskněte.
- Vyčistěte historii vlnového štítku.
- Vylepšení rozvržení rozvržení dokumentu jsou sdílena mezi rozvrženími směrování dokumentů a rozvržením popisků vlny. (Více informací viz [Rozvržení směrování dokumentů pro poznávací značky](../warehousing/document-routing-layout-for-license-plates.md).)

Tato vylepšení zefektivňují označování kartonů před paletizací. Výhodou jsou zejména pro společnosti, které dodávají velkým maloobchodníkům, kteří automaticky potvrzují příjmy z objednávek skenováním každého kartonu samostatně.

> [!NOTE]
> Konfigurační scénáře popsané v tomto tématu můžete implementovat samostatně nebo v kombinaci, v závislosti na vašich obchodních požadavcích. Můžete navrhnout několik šablon popisků vlny, které fungují v sekvenci (jak je znázorněno ve scénáři 3). Například můžete použít scénář 1 pro tisk štítků na kartonech a scénář 2 pro tisk štítků na paletách (pokud se palety na skladě liší ve velikosti a složení).

## <a name="turn-on-the-wave-label-printing-feature"></a>Zapnutí funkce tisku popisků vlny

Než můžete použít funkci *Tisk popisků vlny*, musíte ji v systému zapnout. Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba. Funkce je zde uvedena následujícím způsobem:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Tisk popisků vlny*

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a>Scénář 1: Tisk popisků vlny, kde je generován jeden popisek vlny

Tento scénář ukazuje, jak může společnost tisknout přepravní štítky pro velkého maloobchodníka, který automaticky potvrzuje potvrzení o objednávce skenováním každého kartonu samostatně.

Tento scénář ukazuje průběh toku.

### <a name="make-demo-data-available"></a>Zpřístupnění ukázkových dat

Pokud chcete provést tento scénář, musíte mít nainstalována ukázková data a musíte vybrat právnickou osobu **USMF**.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Ujistěte se, že je k dispozici metoda popisku vlny

Možná bude třeba obnovit metody zpracování vln, abyste měli dostupnou metodu tisku popisků vlny.

1. Přejděte do **Řízení skladu \> Nastavení \> Vlny \> Metody zpracování vlny**.
1. Potvrďte, že **waveLabelPrinting** je v seznamu. Pokud není, vyberte **Obnovit metody** v podokně Akce, abyste ji přidali.

### <a name="configure-a-wave-template"></a>Konfigurujte šablonu vlny

Šablony vln vám umožní propojit konkrétní příklady vlnových metod s odpovídající šablonou vlnových štítků.

1. Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.
1. Vyberte šablonu, např. **Vychozí dodávka 62**.
1. Na pevné záložce **Metody** přesuňte metodu **Tisk popisků vlny** do sloupce **Vybrané metody**.
1. V sloupci **Vybrané metody** vyberte metodu **Tisk popisků vlny** a nastavte její pole **Kód kroku vlny** na *PrintLabel*. Další informace o kódech kroku vlny viz [Kódy kroku vlny](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Vytvořte rozvržení vlnového štítku

Rozvržení štítku řídí, jaké informace jsou na štítku vytištěny a jak jsou rozloženy. Zde zadáte kód ZPL, který je odeslán do tiskárny.

1. Přejděte na **Správa skladu \> Nastavení \> Směrování dokumentu \> Rozložení popisku vlny**.
1. Vytvořte záznam, který má následující nastavení:

    - **ID rozložení štítku:** *Kartón*
    - **Popis:** *Karton (SSCC)*

1. V podokně akcí vyberte **Uložit**.
1. V podokně Akce vyberte **Nastavení řádku popisku vlny**.

    Zobrazí se stránka **Nastavení řádku popisku vlny**. Zde můžete nakonfigurovat dynamickou část štítku.

1. Přidejte řádek, který má následující nastavení:

    - **ID řádku:** *WaveLabel*
    - **Název tabulky řádků:** *WHSWaveLabel*
    - **Pozice počátku řádku:** *0*

        Toto pole definuje vertikální polohu, kde bude řádek začínat na štítku.

    - **Výška řádku:** *0*

        Toto pole definuje výšku každého řádku (v bodech) podle standardu ZPL. Výška řádku je kladná pro vodorovné štítky a záporná pro vertikální štítky. Protože v tomto příkladu je pouze jeden řádek, můžete nastavit hodnotu na *0* (nula).

    - **Řádky na stránku:** *1*

        Toto pole definuje počet řádků, které lze vytisknout na každý štítek.

        > [!NOTE]
        > Toto nastavení způsobí, že se pro každý záznam v tabulce vlnových štítků vytiskne samostatný štítek ZPL.

1. Zavřete stránku.
1. V podokně akcí vyberte **Upravit dotaz**.
1. V dialogovém okně Editor dotazů na kartě **Oblast** přidejte řádek, který má nasledující nastavení:

    - **Tabulka:** *Řádky práce*
    - **Odvozená tabulka:** *Řádky práce*
    - **Pole:** *Typ práce*
    - **Kritéria:** *Výdej*

    Tento dotaz zajišťuje, že na štítek budou vytištěny pouze pracovní řádky typu pick, nikoli pracovní řádky typu put.

1. Pokud chcete mít možnost vytisknout nákladní list, na kartě **Připojí se** vyberte záložku **Pracovní řádky** a připojte k nim tabulku **Zásilky**.
1. Zavřete dialogové okno editoru dotazů.
1. Pevná záložka **Rozložení textu tiskárny** má tři oddíly, kde můžete psát kód tiskárny: **Sekce záhlaví**, **Sekce text** a **Sekce zápatí**. V **Sekci záhlaví** v poli **Hlavička štítku** zadejte kód pro požadovanou hlavičku. Pokud například používáte tiskárny Zebra, můžete použít následující kód.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. V **Sekci text** v poli **Text štítku** zadejte kód ZPL pro požadovaný text. Následuje příklad.

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. V **Sekci text** v poli **Zápatí štítku** zadejte kód ZPL pro požadované zápatí. Následuje příklad.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Toto nastavení vytiskne jednu kopii každého štítku. Pokud potřebujete více kopií (například jednu kopii pro každou stranu palety), nastavte hodnotu **n** pro sekci **\^PQn** v zápatí na požadovaný počet kopií. Chcete-li například vytisknout čtyři kopie každého štítku, zadejte **\^PQ4**.

Váš štítek je nyní připraven k použití.

### <a name="create-a-wave-label-type"></a>Vytvořte typ vlnového štítku

Typy vlnových štítků se používají k propojení šablon vlnových štítků s jednotkou na řádcích skupin sekvencí jednotek.

1. Přejděte na **Správa skladu \> Nastavení \> Směrování dokumentu \> Typy popisků vlny**.
1. Přidejte typ popisku vlny, který má následující nastavení:

    - **Typ štítku:** *Kartón*
    - **Popis:** *Kartón*

### <a name="set-up-unit-sequence-groups"></a>Nastavit skupiny klasifikace jednotek

Dále nastavte skupinu sekvencí jednotek pro typ vlnového štítku.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Skupiny sekvenci jednotek**.
1. Vyberte skupinu **Ea Box PL**.
1. Pro řádek **Krabice** nastavte **Typ úrovně vlny** na *Kartón*.

### <a name="create-a-wave-label-template"></a>Vytvoření šablony vlnového štítku

Dále vytvořte šablonu vlnového štítku pro typ vlnového štítku.

1. Přejděte na **Správa skladu \> Nastavení \> Směrování dokumentu \> Šablony popisku vlny**.
1. Přidejte šsblonu úrovně vlnx a nastavte následující hodnoty v záhlaví:

    - **Název šablony štítku:** *Štítky kartonu*
    - **Popis:** *Štítky kartonů*
    - **Kód kroku vlny:** *PrintLabel*
    - **Sklad:** *62*

1. Na pevné záložce **Všeobecné** nastavte pole **Typ vlnového štítku** na *Karton*.
1. Na pevné záložce **Podrobnosti o šabloně vlnového štítku** přidejte nový řádek, který má následující nastavení:

    - **ID rozložení štítku:** *Kartón*
    - **Název tiskárny:** Vyberte vhodnou tiskárnu ZPL.
    - **Spustit dotaz:** *Ano* (Toto nastavení je volitelné, ale pro optimální výkon se doporučuje.)

1. V podokně akcí vyberte **Uložit**.
1. Volitelné: Pokud nastavujete design štítků specifických pro zákazníka, musíte vytvořit dotaz, abyste našli účet zákazníka. Na pevné záložce **Podrobnosti o šabloně vlnového štítku** vyberte **Upravit dotaz**. Pak v dialogovém okně Editor dotazů na kartě **Oblast** přidejte řádek, který má nasledující nastavení:

    - **Tabulka:** *Dodávky*
    - **Odvozená tabulka:** *Dodávky*
    - **Pole:** *Číslo účtu*
    - **Kritéria:** Zadejte příslušné číslo zákaznického účtu.

    Po dokončení vyberte **OK** a zavřete dialogové okno editoru dotazů.

1. V podokně Akce zvolte **Upravit dotaz** a otevřete dialogové okno editor dotazů pro celou šablonu štítku.
1. V dialogovém okně Editor dotazů na kartě **Třídění** přidejte řádek, který má nasledující nastavení:

    - **Tabulka:** *Řádky práce*
    - **Odvozená tabulka:** *Řádky práce*
    - **Pole:** *ID referenčního nákladového řádku (ID záznamu)*
    - **Směr hledání:** *Vzestupně*

1. Vyberte **OK** a dialogové okno editor dotazu zavřete.
1. Okno se zprávou vás vyzve k potvrzení operace resetování seskupení. Pokračujte výběrem tlačítka **Ano**.
1. V podokně Akce vyberte možnost **Skupina šablon úrovně vlny**.
1. V dialogovém okně **Skupina šablon úrovně vlny** vyberte řádek, ve kterém je pole **Název referenčního pole** nastaveno na *ID referenčního nákladového řádku* a poté zaškrtněte **ID sestavení štítku** pro tento řádek.

    > [!NOTE]
    > Toto nastavení vytvoří jednu sekvenci štítků („Karton 1 z X“) na řádek zatížení po celé vlně, bez ohledu na nastavení pracovní skupiny. Tuto sekvenci štítků lze vytisknout na rozvržení štítků.

### <a name="configure-number-sequence-extensions"></a>Konfigurace rozšíření posloupnosti čísel

Rozšíření číselných sekvencí řídí dodržování specifických číselných sekvencí GS1. Tato konfigurace je pro aktuální scénář volitelná. Další informace a pokyny k konfiguraci najdete v části [Konfigurovat rozšíření posloupnosti čísel](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Vytvořte prodejní objednávku a uvolněte ji do skladu

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Vytvořte prodejní objednávku, která má následující nastavení:

    - **Účet zákazníka:** *US-001*
    - **Sklad:** *62*

1. Přidejte dva řádky prodejní objednávky s následujícím nastavením:

    - Řádek prodejní objednávky 1:

        - **Číslo položky:** *A0001*
        - **Množství:** *9024*
        - **Jednotka:** *ea* (9024 ea = 376 Box = 47 PL)

    - Řádek prodejní objednávky 2:

        - **Číslo položky:** *A0002*
        - **Množství:** *9016*
        - **Jednotka:** *ea* (9016 ea = 322 Box = 46 PL)

    > [!NOTE]
    > Položky a množství, které jsou zde uvedeny, jsou pouze příklady. Musí používat skupinu sekvencí jednotek, kterou jste definovali dříve, vhodné převody jednotek *ea* na *Box* na *PL* musí být pro ně definovány a musí mít zásoby ve skladu *62*. Další informace viz [Měrná jednotka a politika skladování](unit-measure-stocking-policies.md).

1. Vyberte řádek prodejní objednávky 1. Pak v sekci **Řádek prodejní objednávky** v nabídce **Zásoby** vyberte možnost **Rezervace**.
1. Na stránce **Rezervace** vyberte v podokně Akce možnost **Rezervovat šarži** a zavřete stránku.
1. Opakujte kroky 4 a 5 pro řádek 2 prodejní objednávky.
1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.

    Dojde k následujícím událostem:

    - Systém zpracovává vytvořenou zásilku pomocí šablony, která zahrnuje krok tisku štítků. Rozvržení štítků se použije k definování formátu štítků a výsledkem bude štítek, který se vytiskne na tiskárně vybrané v šabloně štítků.
    - Štítky vlny se generují a tisknou. Počet štítků se bude rovnat počtu kartonů (v tomto příkladu 376 štítků pro řádek 1 a 322 štítků pro řádek 2).
    - Pro zásilky je vygenerován nový přepravní doklad. Pokud jste nakonfigurovali rozšíření číselných sekvencí, budou ID popisků vlny sledovat formát čísla **SSCC-18**. 

vlnové štítky můžete zobrazit a znovu vytisknout z následujících stránek. V podokně akcí každé ze stránek **Dodávky** ve skupině **Související informace** vyberte **vlnové štítky**.

- Všechny zásilky \> Podrobnosti o zásilce
- Všechny náklady \> Načíst podrobnosti
- Všechny vlny
- Štítky vlny
- Historie popisků vlny

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a>Scénář 2: Tisk vlnových štítků pro kontejnerizaci (bez záznamů vlnových štítků)

Tento scénář umožňuje tisknout štítky vln, když pomocí kontejnerizace automaticky rozdělujete položky do kartonů, a proto nevyžadují záznam vlnových štítků. V tomto případě ID kontejneru funguje jako zástupný symbol pro SSCC.

Zde jsou hlavní rozdíly mezi tímto scénářem a scénářem 1:

- **Šablony vlnových štítků:** Nevyberete typ vlnového štítku v šabloně vlnového štítku a nebudete vyžadovat seskupení sestavení štítků. V opačném případě nakonfigurujete šablonu popisku vlny a odkaz na šablonu vlny stejným způsobem, jaký je popsán ve scénáři 1. Chcete-li zabránit generování štítků vlny, musíte ponechat typ vlnového štítku prázdný.
- **Rozvržení vlnových štítků:** Nakonfigurujete nastavení řádků rozvržení vlnových štítků pro pracovní řádky namísto záznamů vlnových štítků. Nastavení řádků pro rozvržení štítků musíte nakonfigurovat pomocí tabulky **WHSWorkLine** místo tabulky **WHSWaveLabel**. Nastavení **Řádky na stránce** řídí počet řádků, které bude mít sekce text. 

Tato konfigurace je také vhodná pro obchodní scénáře, kde je více různých položek zabaleno do jednoho označeného pole nebo do palety, a tento proces balení lze definovat vytvořením práce (například práce, která je seskupena podle zásilky).

Tento scénář ukazuje průběh toku.

### <a name="make-demo-data-available"></a>Zpřístupnění ukázkových dat

Pokud chcete provést tento scénář, musíte mít nainstalována ukázková data a musíte vybrat právnickou osobu **USMF**.

### <a name="make-sure-that-the-wave-label-method-is-available"></a>Ujistěte se, že je k dispozici metoda popisku vlny

Možná bude třeba obnovit metody zpracování vln, abyste měli dostupnou metodu tisku popisků vlny.

1. Přejděte do **Řízení skladu \> Nastavení \> Vlny \> Metody zpracování vlny**.
1. Potvrďte, že **waveLabelPrinting** je v seznamu. Pokud není, vyberte **Obnovit metody** v podokně Akce, abyste ji přidali.

### <a name="set-up-a-wave-template"></a>Nastavení šablony vlny

Šablony vln vám umožní propojit konkrétní příklady vlnových metod s odpovídající šablonou vlnových štítků.

1. Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.
1. Vyberte šablonu, např. **Kontejnerizace 63**.
1. Na pevné záložce **Metody** přesuňte metodu **Tisk popisků vlny** do sloupce **Vybrané metody**.
1. V sloupci **Vybrané metody** vyberte metodu **Tisk popisků vlny** a nastavte její pole **Kód kroku vlny** na *PrintLabel*. Další informace o kódech kroku vlny viz [Kódy kroku vlny](wave-step-codes.md).

### <a name="create-a-wave-label-layout"></a>Vytvořte rozvržení vlnového štítku

1. Přejděte na **Správa skladu \> Nastavení \> Směrování dokumentu \> Rozložení popisku vlny**.
1. Vytvořte záznam, který má následující nastavení:

    - **ID rozložení štítku:** *Kartón*
    - **Popis:** *Karton (SSCC)*

1. V podokně akcí vyberte **Uložit**.
1. V podokně Akce vyberte **Nastavení řádku popisku vlny**.

    Zobrazí se stránka **Nastavení řádku popisku vlny**. Zde můžete nakonfigurovat dynamickou část štítku.

1. Přidejte řádek, který má následující nastavení:

    - **ID řádku:** *WorkLine*
    - **Název tabulky řádků:** *WHSWorkLine*
    - **Pozice počátku řádku:** *500*

        Toto pole definuje vertikální polohu, kde bude řádek začínat na štítku.

    - **Výška řádku** *-50*

        Toto pole definuje výšku každého řádku. Výška řádku je kladná pro vodorovné štítky a záporná pro vertikální štítky.

    - **Řádky na stránku:** *5*

        Toto pole definuje počet řádků, které lze vytisknout na každý štítek.

        > [!NOTE]
        > Toto nastavení vytiskne několik štítků ZPL na dílo, kde každá stránka pojme až pět pracovních řádků. Pokud je například štítek vytištěn pro kontejner, který má 12 řádků, vytisknou se tři štítky. Pokud chcete vytisknout samostatný štítek pro každý řádek výběru, nastavte tuto hodnotu na *1*.

1. Zavřete stránku.
1. V podokně akcí vyberte **Upravit dotaz**.
1. V dialogovém okně Editor dotazů na kartě **Oblast** přidejte řádek, který má nasledující nastavení:

    - **Tabulka:** *Řádky práce*
    - **Odvozená tabulka:** *Řádky práce*
    - **Pole:** *Typ práce*
    - **Kritéria:** *Výdej*

1. Pokud chcete mít možnost vytisknout nákladní list, na kartě **Připojí se** vyberte záložku **Pracovní řádky** a připojte k nim tabulku **Zásilky**.
1. Zavřete dialogové okno editoru dotazů.
1. Pevná záložka **Rozložení textu tiskárny** má tři oddíly, kde můžete psát kód tiskárny: **Sekce záhlaví**, **Sekce text** a **Sekce zápatí**. V **Sekci záhlaví** v poli **Hlavička štítku** zadejte kód pro požadovanou hlavičku. Pokud například používáte tiskárny Zebra, můžete použít následující kód.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. V **Sekci text** v poli **Text štítku** zadejte kód ZPL pro požadovaný text. Následuje příklad.

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. V **Sekci text** v poli **Zápatí štítku** zadejte kód ZPL pro požadované zápatí. Následuje příklad.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Toto nastavení vytiskne jednu kopii každého štítku. Pokud potřebujete více kopií (například jednu kopii pro každou stranu palety), nastavte hodnotu **n** pro sekci **\^PQn** v zápatí na požadovaný počet kopií. Chcete-li například vytisknout čtyři kopie každého štítku, zadejte **\^PQ4**.

Váš štítek je nyní připraven k použití.

### <a name="create-a-wave-label-template"></a>Vytvoření šablony vlnového štítku

1. Přejděte na **Správa skladu \> Nastavení \> Směrování dokumentu \> Šablony popisku vlny**.
1. Přidejte šsblonu úrovně vlnx a nastavte následující hodnoty v záhlaví:

    - **Název šablony štítku:** *Štítky kontejneru*
    - **Popis:** *Štítky kontejnerů*
    - **Kód kroku vlny:** *PrintLabel*
    - **Sklad:** *63*

1. Na pevné záložce **Podrobnosti o šabloně vlnového štítku** přidejte řádek, který má následující nastavení:

    - **ID rozložení štítku:** *Kontejner*
    - **Název tiskárny:** Vyberte vhodnou tiskárnu ZPL.
    - **Spustit dotaz:** *Ano* (Toto nastavení je volitelné, ale pro optimální výkon se doporučuje.)

1. V podokně akcí vyberte **Uložit**.
1. Volitelné: Pokud nastavujete design štítků specifických pro zákazníka, musíte vytvořit dotaz, abyste našli účet zákazníka. Na pevné záložce **Podrobnosti o šabloně vlnového štítku** vyberte **Upravit dotaz**. Pak v dialogovém okně Editor dotazů na kartě **Oblast** přidejte řádek, který má nasledující nastavení:

    - **Tabulka:** *Dodávky*
    - **Odvozená tabulka:** *Dodávky*
    - **Pole:** *Číslo účtu*
    - **Kritéria:** Zadejte příslušné číslo zákaznického účtu.

    Po dokončení vyberte **OK** a zavřete dialogové okno editoru dotazů.

### <a name="configure-number-sequence-extensions"></a>Konfigurace rozšíření posloupnosti čísel

Rozšíření číselných sekvencí řídí dodržování specifických číselných sekvencí GS1. Tato konfigurace je pro aktuální scénář volitelná. Další informace a pokyny k konfiguraci najdete v části [Konfigurovat rozšíření posloupnosti čísel](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Vytvořte prodejní objednávku a uvolněte ji do skladu

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Vytvořte prodejní objednávku, která má následující nastavení:

    - **Účet zákazníka:** *US-001*
    - **Sklad:** *63*

1. Přidejte pět řádků prodejní objednávky:

    - Řádek prodejní objednávky 1:

        - **Číslo položky:** *A0001*
        - **Množství:** *10*

    - Řádek prodejní objednávky 2:

        - **Číslo položky:** *A0002*
        - **Množství:** *20*

    - Řádek prodejní objednávky 3:

        - **Číslo položky:** *L0006*
        - **Množství:** *20*

    - Řádek prodejní objednávky 4:

        - **Číslo položky:** *L0100*
        - **Množství:** *40*

    - Řádek prodejní objednávky 5:

        - **Číslo položky:** *L0101*
        - **Množství:** *50*

    > [!NOTE]
    > Položky a množství, které jsou zde uvedeny, jsou pouze příklady. Musí mít zásoby v určeném skladu.

1. Vyberte řádek prodejní objednávky 1. Pak v sekci **Řádek prodejní objednávky** v nabídce **Zásoby** vyberte možnost **Rezervace**.
1. Na stránce **Rezervace** vyberte v podokně Akce možnost **Rezervovat šarži** a zavřete stránku.
1. Opakujte kroky 4 a 5 pro každý další řádek prodejní objednávky.
1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.

    Dojde k následujícím událostem:

    - Systém zpracovává vytvořenou zásilku pomocí šablony, která zahrnuje krok tisku štítků. Rozvržení štítků se použije k definování formátu štítků a konečným výsledkem bude štítek, který má pět řádků a vytiskne se na tiskárně vybrané v šabloně štítků.
    - Pro zásilky je vygenerován nový přepravní doklad. Pokud jste nakonfigurovali rozšíření číselných sekvencí, budou ID popisků vlny sledovat formát čísla **SSCC-18**. 

Tyto štítky vln můžete znovu vytisknout tak, že přejdete na **Správa skladu \> Dotazy a sestavy \> Historie vlnových štítků**.

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a>Scénář 3: Tisk vlnových štítků pro vícevrstvé štítky

Tento scénář ukazuje, jak používat funkci tisku vlnových štítků, když procesy skladování vyžadují několik úrovní přepravních štítků. Například samostatné štítky mohou být vytištěny na kartony a palety a štítek zalomení musí být vytištěn na celou zásilku. Štítky zalomení jsou samostatný typ štítku, který lze použít jako oddělovač mezi rolemi a kontejnery, jako jsou například štítky pro ID zásilky a čárový kód, takže štítky lze po vytištění snadno třídit.

Hlavní rozdíl mezi konfigurací tohoto scénáře a konfigurací scénáře 1, kromě skutečnosti, že jsou povoleny štítky zalomení, spočívá v tom, že více šablon štítků musí být spojeno se šablonami štítků vln a řádky skupin sekvencí jednotek. Chcete-li provést tuto konfiguraci, nastavte pro tento scénář následující prvky:

- **Metody zpracování vln:** Metodu označování vln označíte jako „opakovatelnou“, přidáte ji dvakrát (nebo vícekrát) do šablony vln a nastavíte různé kódy vlnových kroků.
- **Šablony vlnových štítků:** Nakonfigurujete šablony vlnových štítků a propojíte je s vlnovou šablonou. Každá šablona štítků vln má svůj vlastní typ štítků vln.
- **Rozvržení vlnových štítků:** Vytvoříte více rozvržení vlnových štítků. Pro každou „vrstvu“ štítků bude existovat samostatné rozvržení štítků a také rozvržení přerušení štítků.

Tento scénář ukazuje průběh toku.

### <a name="make-demo-data-available"></a>Zpřístupnění ukázkových dat

Pokud chcete provést tento scénář, musíte mít nainstalována ukázková data a musíte vybrat právnickou osobu **USMF**.

### <a name="set-up-a-wave-process-method"></a>Nastavení metody vlnového procesu

1. Přejděte do **Řízení skladu \> Nastavení \> Vlny \> Metody zpracování vlny**.
1. Potvrďte, že **waveLabelPrinting** je v seznamu. Pokud není, vyberte **Obnovit metody** v podokně Akce, abyste ji přidali.
1. Pro metodu **waveLabelPrinting** zaškrtněte **Zajistit opakovatelnost metody**.

### <a name="set-up-a-wave-template"></a>Nastavení šablony vlny

1. Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.
2. Vyberte šablonu, např. **Vychozí dodávka 62**.
3. Na pevné záložce **Metody** přesuňte metodu **Tisk popisků vlny** do sloupce **Vybrané metody**.
4. V sloupci **Vybrané metody** přiřaďte hodnotu **Kód kroku vlny**, například *Karton*, k metodě **Tisk štítků vlny**. Další informace o kódech kroku vlny viz [Kódy kroku vlny](wave-step-codes.md).
5. Přesuňte metodu **Tisk popisků vlny** do sloupce **Vybrané metody** podruhé.
6. V sloupci **Vybrané metody** přiřaďte jinou hodnotu **Kód kroku vlny**, například *Paleta*, k druhé metodě **Tisk štítků vlny**. Další informace o kódech kroku vlny viz [Kódy kroku vlny](wave-step-codes.md).

### <a name="create-three-wave-label-layouts"></a>Vytvořte tři rozvržení vlnového štítku

1. Přejděte na **Správa skladu \> Nastavení \> Směrování dokumentu \> Rozložení popisku vlny**.
1. Vytvořte záznam, který má následující nastavení:

    - **ID rozložení štítku:** *Kartón*
    - **Popis:** *Karton (SSCC)*

1. V podokně akcí vyberte **Uložit**.
1. V podokně Akce vyberte **Nastavení řádku popisku vlny**.

    Zobrazí se stránka **Nastavení řádku popisku vlny**. Zde můžete nakonfigurovat dynamickou část štítku.

1. Přidejte řádek, který má následující nastavení:

    - **ID řádku:** *WaveLabel*
    - **Název tabulky řádků:** *WHSWaveLabel*
    - **Pozice počátku řádku:** *0*

        Toto pole definuje vertikální polohu, kde bude řádek začínat na štítku.

    - **Výška řádku:** *0*

        Toto pole definuje výšku každého řádku (v bodech) podle standardu ZPL. Výška řádku je kladná pro vodorovné štítky a záporná pro vertikální štítky. Protože v tomto příkladu je pouze jeden řádek, můžete nastavit hodnotu na *0* (nula).

    - **Řádky na stránku:** *1*

        Toto pole definuje počet řádků, které lze vytisknout na každý štítek.

        > [!NOTE]
        > Toto nastavení způsobí, že se pro každý záznam v tabulce vlnových štítků vytiskne samostatný štítek ZPL.

1. Zavřete stránku.
1. V podokně akcí vyberte **Upravit dotaz**.
1. V dialogovém okně Editor dotazů na kartě **Oblast** přidejte řádek, který má nasledující nastavení:

    - **Tabulka:** *Řádky práce*
    - **Odvozená tabulka:** *Řádky práce*
    - **Pole:** *Typ práce*
    - **Kritéria:** *Výdej*

    Tento dotaz zajišťuje, že na štítek budou vytištěny pouze pracovní řádky typu pick, nikoli pracovní řádky typu put.

1. Pokud chcete mít možnost vytisknout nákladní list, na kartě **Připojí se** vyberte záložku **Pracovní řádky** a připojte k nim tabulku **Zásilky**. 
1. Zavřete dialogové okno editoru dotazů.
1. Pevná záložka **Rozložení textu tiskárny** má tři oddíly, kde můžete psát kód tiskárny: **Sekce záhlaví**, **Sekce text** a **Sekce zápatí**. V **Sekci záhlaví** v poli **Hlavička štítku** zadejte kód pro požadovanou hlavičku. Pokud například používáte tiskárny Zebra, můžete použít následující kód.


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. V **Sekci text** v poli **Text štítku** zadejte kód ZPL pro požadovaný text. Následuje příklad.

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. V **Sekci text** v poli **Zápatí štítku** zadejte kód ZPL pro požadované zápatí. Následuje příklad.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Toto nastavení vytiskne jednu kopii každého štítku. Pokud potřebujete více kopií (například jednu kopii pro každou stranu palety), nastavte hodnotu **n** pro sekci **\^PQn** v zápatí na požadovaný počet kopií. Chcete-li například vytisknout čtyři kopie každého štítku, zadejte **\^PQ4**.

1. První štítek je nyní připraven k použití.
1. Vytvořte druhý záznam rozvržení, který má následující nastavení:

    - **ID rozložení štítku:** *Paleta*
    - **Popis:** *Paleta*

1. V podokně akcí vyberte **Uložit**.
1. V podokně Akce vyberte **Nastavení řádku popisku vlny**.

    Zobrazí se stránka **Nastavení řádku popisku vlny**. Zde můžete nakonfigurovat dynamickou část štítku.

1. Přidejte řádek, který má následující nastavení:

    - **ID řádku:** *WaveLabel*
    - **Název tabulky řádků:** *WHSWaveLabel*
    - **Pozice počátku řádku:** *0*

        Toto pole definuje vertikální polohu, kde bude řádek začínat na štítku.

    - **Výška řádku:** *0*

        Toto pole definuje výšku každého řádku (v bodech) podle standardu ZPL. Výška řádku je kladná pro vodorovné štítky a záporná pro vertikální štítky. Protože v tomto příkladu je pouze jeden řádek, můžete nastavit hodnotu na *0* (nula).

    - **Řádky na stránku:** *1*

        Toto pole definuje počet řádků, které lze vytisknout na každý štítek.

        > [!NOTE]
        > Toto nastavení způsobí, že se pro každý záznam v tabulce vlnových štítků vytiskne samostatný štítek ZPL.

1. Zavřete stránku.
1. V podokně akcí vyberte **Upravit dotaz**.
1. V dialogovém okně Editor dotazů na kartě **Oblast** přidejte řádek, který má nasledující nastavení:

    - **Tabulka:** *Řádky práce*
    - **Odvozená tabulka:** *Řádky práce*
    - **Pole:** *Typ práce*
    - **Kritéria:** *Výdej*

    Tento dotaz zajišťuje, že na štítek budou vytištěny pouze pracovní řádky typu pick, nikoli pracovní řádky typu put.

1. Pokud chcete mít možnost vytisknout nákladní list, na kartě **Připojí se** vyberte záložku **Pracovní řádky** a připojte k nim tabulku **Zásilky**.
1. Zavřete dialogové okno editoru dotazů.
1. Pevná záložka **Rozložení textu tiskárny** má tři oddíly, kde můžete psát kód tiskárny: **Sekce záhlaví**, **Sekce text** a **Sekce zápatí**. V **Sekci záhlaví** v poli **Hlavička štítku** zadejte kód pro požadovanou hlavičku. Pokud například používáte tiskárny Zebra, můžete použít následující kód.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. V **Sekci text** v poli **Text štítku** zadejte kód ZPL pro požadovaný text. Následuje příklad.

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. V **Sekci text** v poli **Zápatí štítku** zadejte kód ZPL pro požadované zápatí. Následuje příklad.

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > Toto nastavení vytiskne jednu kopii každého štítku. Pokud potřebujete více kopií (například jednu kopii pro každou stranu palety), nastavte hodnotu **n** pro sekci **\^PQn** v zápatí na požadovaný počet kopií. Chcete-li například vytisknout čtyři kopie každého štítku, zadejte **\^PQ4**.

1. Druhý štítek je nyní připraven k použití.
1. Vytvořte třetí záznam rozvržení, který má následující nastavení:

    - **ID rozložení štítku:** *Přerušení*
    - **Popis:** *Štítek přerušení*

1. V podokně akcí vyberte **Uložit**.
1. Pevná záložka **Rozložení textu tiskárny** má tři oddíly, kde můžete psát kód tiskárny: **Sekce záhlaví**, **Sekce text** a **Sekce zápatí**. V **Sekci záhlaví** v poli **Hlavička štítku** zadejte kód ZPL pro požadovanou hlavičku. Následuje příklad.

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. Tentokrát není nutný nžádný text. Proto jednoduše zadejte požadovaný text do **Sekce zápatí**. Následuje příklad.

    ```plaintext
    ^XZ
    ```

    Třetí štítek je nyní připraven k použití.

    > [!NOTE]
    > Tento třetí štítek je štítek přerušení, který bude použit jako oddělovač mezi svitky štítků.

### <a name="create-two-wave-label-types"></a>Vytvořte dva typy vlnového štítku

1. Přejděte na **Správa skladu \> Nastavení \> Směrování dokumentu \> Typy popisků vlny**.
1. Vytvořte záznam, který má následující nastavení:

    - **Typ štítku:** *Karton*
    - **Popis:** *Kartón*

1. Vytvořte druhý záznam, který má následující nastavení:

    - **Typ štítku:** *Paleta*
    - **Popis:** *Paleta*

### <a name="set-up-unit-sequence-groups"></a>Nastavit skupiny klasifikace jednotek

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Skupiny sekvenci jednotek**.
1. Vyberte nebo vytvořte skupinu **Ea Box PL**.
1. Pro řádek **Krabice** nastavte **Typ úrovně vlny** na *Kartón*.
1. Pro řádek **PL** nastavte **Typ úrovně vlny** na *Paletu*.

### <a name="create-wave-label-templates"></a>Vytvoření šablon vlnového štítku

1. Přejděte na **Správa skladu \> Nastavení \> Směrování dokumentu \> Šablony popisku vlny**.
1. Vytvořte šablonu popisku, která má následující nastavení:

    - **Název šablony štítku:** *Štítky kartonu*
    - **Popis:** *Štítky kartonů*
    - **Kód kroku vlny:** *Karton*
    - **Sklad:** *62*

1. Na záložce s náhledem **Obecné** v poli **Typ popisků vlny** vyberte hodnotu, např. *Karton*.
1. Na pevné záložce **Podrobnosti o šabloně vlnového štítku** přidejte řádek, který má následující nastavení:

    - **ID rozložení štítku:** *Kartón*
    - **Název tiskárny:** Vyberte vhodnou tiskárnu ZPL.
    - **Spustit dotaz:** *Ano* (Toto nastavení je volitelné, ale pro optimální výkon se doporučuje.)

1. V podokně akcí vyberte **Uložit**.
1. Volitelné: Pokud nastavujete design štítků specifických pro zákazníka, musíte vytvořit dotaz, abyste našli účet zákazníka. Na pevné záložce **Podrobnosti o šabloně vlnového štítku** vyberte **Upravit dotaz**. Pak v dialogovém okně Editor dotazů na kartě **Oblast** přidejte řádek, který má nasledující nastavení:

    - **Tabulka:** *Dodávky*
    - **Odvozená tabulka:** *Dodávky*
    - **Pole:** *Číslo účtu*
    - **Kritéria:** Zadejte příslušné číslo zákaznického účtu.

    Po dokončení vyberte **OK** a zavřete dialogové okno editoru dotazů.

1. V podokně Akce zvolte **Upravit dotaz** a otevřete dialogové okno editor dotazů pro celou šablonu štítku.
1. V dialogovém okně Editor dotazů na kartě **Třídění** přidejte řádek, který má nasledující nastavení:

    - **Tabulka:** *Řádky práce*
    - **Odvozená tabulka:** *Řádky práce*
    - **Pole:** *ID referenčního nákladového řádku (ID záznamu)*
    - **Směr hledání:** *Vzestupně*

1. Přidejte druhý řádek, který má následující nastavení:

    - **Tabulka:** *Řádky práce*
    - **Odvozená tabulka:** *Řádky práce*
    - **Pole:** *ID dodávky*
    - **Směr hledání:** *Vzestupně*

1. Vyberte **OK** a dialogové okno editor dotazu zavřete.
1. Okno se zprávou vás vyzve k potvrzení operace resetování seskupení. Pokračujte výběrem tlačítka **Ano**.
1. V podokně Akce vyberte možnost **Skupina šablon úrovně vlny**.
1. V dialogovém okně **Skupina šablon popisků vlny** pro řádek, kde je pole **Název referenčního pole** nastaveno na *ID zásilky*, nastavte následující hodnoty:

    - **Tisk štítku přerušení:** Zaškrtněte toto políčko.
    - **ID rozložení štítku:** Vyberte štítek přerušení. (Například vyberte štítek *Přerušení*, který jste vytvořili dříve v tomto scénáři.)
    - **Název tiskárny:** Vyberte tiskárnu pro štítek přerušení. (Obvykle byste za účelem rozdělení rolí štítků měli vybrat stejnou tiskárnu, která je vybrána na pevné záložce **Podrobnosti o šabloně vlnového štítku**. Jsou však možné i jiné scénáře.)

1. Pro řádek, kde je pole **Název referenčního pole** nastaveno na *ID referenčního zatížení*, zaškrtněte **ID sestavení štítku**.

    > [!NOTE]
    > Toto nastavení vytvoří jednu sekvenci štítků („Karton 1 z X“) na řádek zatížení po celé vlně, bez ohledu na nastavení pracovní skupiny. Tuto sekvenci štítků lze vytisknout na rozvržení štítků. Štítky pro různé zásilky budou navíc odděleny vybraným štítkem přerušení.

1. Vyberte **OK**, chcete-li zavřít dialogové okno **Skupina šablon popisku vlny**.
1. Vytvořte druhou šablonu popisku, která má následující nastavení:

    - **Název šablony štítku:** *Štítky palet*
    - **Popis:** *Štítky palet*
    - **Kód kroku vlny:** *Paleta*
    - **Sklad:** *62*

1. Na záložce s náhledem **Obecné** v poli **Typ popisků vlny** vyberte hodnotu, např. *Paleta*.
1. Na pevné záložce **Podrobnosti o šabloně vlnového štítku** přidejte řádek, který má následující nastavení:

    - **ID rozložení štítku:** *Paleta*
    - **Název tiskárny:** Vyberte vhodnou tiskárnu ZPL.
    - **Spustit dotaz:** *Ano* (Toto nastavení je volitelné, ale pro optimální výkon se doporučuje.)

1. V podokně akcí vyberte **Uložit**.
1. Volitelné: Pokud nastavujete design štítků specifických pro zákazníka, musíte vytvořit dotaz, abyste našli účet zákazníka. Na pevné záložce **Podrobnosti o šabloně vlnového štítku** vyberte **Upravit dotaz**. Pak v dialogovém okně Editor dotazů na kartě **Oblast** přidejte řádek, který má nasledující nastavení:

    - **Tabulka:** *Dodávky*
    - **Odvozená tabulka:** *Dodávky*
    - **Pole:** *Číslo účtu*
    - **Kritéria:** Zadejte příslušné číslo zákaznického účtu.

    Po dokončení vyberte **OK** a zavřete dialogové okno editoru dotazů. 

1. V podokně Akce zvolte **Upravit dotaz** a otevřete dialogové okno editor dotazů pro celou šablonu štítku.
1. V dialogovém okně Editor dotazů na kartě **Třídění** přidejte řádek, který má nasledující nastavení:

    - **Tabulka:** *Řádky práce*
    - **Odvozená tabulka:** *Řádky práce*
    - **Pole:** *ID referenčního nákladového řádku (ID záznamu)*
    - **Směr hledání:** *Vzestupně*

1. Přidejte druhý řádek, který má následující nastavení:

    - **Tabulka:** *Řádky práce*
    - **Odvozená tabulka:** *Řádky práce*
    - **Pole:** *ID dodávky*
    - **Směr hledání:** *Vzestupně*

1. Vyberte **OK** a dialogové okno editor dotazu zavřete.
1. Okno se zprávou vás vyzve k potvrzení operace resetování seskupení. Pokračujte výběrem tlačítka **Ano**.
1. V podokně Akce vyberte možnost **Skupina šablon úrovně vlny**.
1. V dialogovém okně **Skupina šablon popisků vlny** pro řádek, kde je pole **Název referenčního pole** nastaveno na *ID zásilky*, nastavte následující hodnoty:

    - **Tisk štítku přerušení:** Zaškrtněte toto políčko.
    - **ID rozložení štítku:** Vyberte štítek přerušení. (Například vyberte štítek *Přerušení*, který jste vytvořili dříve v tomto scénáři.)
    - **Název tiskárny:** Vyberte tiskárnu pro štítek přerušení. (Obvykle byste za účelem rozdělení rolí štítků měli vybrat stejnou tiskárnu, která je vybrána na pevné záložce **Podrobnosti o šabloně vlnového štítku**. Jsou však možné i jiné scénáře.)

1. Pro řádek, kde je pole **Název referenčního pole** nastaveno na *ID referenčního zatížení*, zaškrtněte **ID sestavení štítku**.

    > [!NOTE]
    > Toto nastavení vytvoří jednu sekvenci štítků („Karton 1 z X“) na řádek zatížení po celé vlně, bez ohledu na nastavení pracovní skupiny. Tuto sekvenci štítků lze vytisknout na rozvržení štítků. Štítky pro různé zásilky budou navíc odděleny vybraným štítkem přerušení.

### <a name="configure-number-sequence-extensions"></a>Konfigurace rozšíření posloupnosti čísel

Rozšíření číselných sekvencí řídí dodržování specifických číselných sekvencí GS1. Tato konfigurace je pro aktuální scénář volitelná. Další informace a pokyny k konfiguraci najdete v části [Konfigurovat rozšíření posloupnosti čísel](../warehousing/configure-number-sequence-extensions.md).

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Vytvořte prodejní objednávku a uvolněte ji do skladu

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Vytvořte prodejní objednávku, která má následující nastavení:

    - **Účet zákazníka:** *US-001*
    - **Sklad:** *62*

1. Přidejte dva řádky prodejní objednávky:

    - Řádek prodejní objednávky 1:

        - **Číslo položky:** *A0001*
        - **Množství:** *9024*
        - **Jednotka:** *ea* (9024 ea = 376 Box = 47 PL)

    - Řádek prodejní objednávky 2:

        - **Číslo položky:** *A0002*
        - **Množství:** *9016*
        - **Jednotka:** *ea* (9016 ea = 322 Box = 46 PL)

    > [!NOTE]
    > Položky a množství, které jsou zde uvedeny, jsou pouze příklady. Musí používat skupinu sekvencí jednotek, kterou jste definovali dříve, vhodné převody jednotek *ea* na *Box* na *PL* musí být pro ně definovány a musí mít zásoby ve skladu *62*. Další informace viz [Měrná jednotka a politika skladování](unit-measure-stocking-policies.md).

1. Vyberte řádek prodejní objednávky 1. Pak v sekci **Řádek prodejní objednávky** v nabídce **Zásoby** vyberte možnost **Rezervace**.
1. Na stránce **Rezervace** vyberte v podokně Akce možnost **Rezervovat šarži** a zavřete stránku.
1. Opakujte kroky 4 a 5 pro řádek 2 prodejní objednávky.
1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.

    Dojde k následujícím událostem: 

    - Systém zpracovává vytvořenou zásilku pomocí šablony, která zahrnuje krok tisku štítků. Rozvržení štítků se použije k definování formátu štítků a výsledkem bude štítek, který se vytiskne na tiskárně vybrané v šabloně štítků.
    - Štítky vlny se generují a tisknou. Počet štítků se bude rovnat počtu kartonů (v tomto příkladu 376 štítků pro řádek 1, 322 štítků krabic pro řádek 2, 47 štítků palet pro řádek 1, 47 štítků PL pro řádek 2 a dva štítky přerušení, které mají ID zásilky).
    - Pro zásilky je vygenerován nový přepravní doklad. Pokud jste nakonfigurovali rozšíření číselných sekvencí, budou ID popisků vlny sledovat formát čísla **SSCC-18**. 

Štítky vln můžete zobrazit a znovu vytisknout z následujících stránek:

- Všechny zásilky \> Podrobnosti o zásilce
- Všechny náklady \> Načíst podrobnosti
- Všechny vlny
- Štítky vlny
- Historie popisků vlny

U většiny těchto stránek najdete příslušnou funkci výběrem **Vlnové štítky** ve skupině **Související informace** na kartě **Zásilky** v podokně akcí.

## <a name="additional-resources"></a>Další prostředky

- [Opakovaný tisk a anulování štítků vlny](reprint-and-void-wave-labels.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]