---
title: Kontrola kvality
description: Toto téma obsahuje informace o funkci Kontrola kvality. Tato funkce umožňuje pracovníkům skladu provádět rychlé namátkové kontroly kvality, zatímco přijímají položky do oblasti příchozího doku.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0848eeb2ad073915ad90d2fd2a4a91f0f420c0ab
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103281"
---
# <a name="quality-check"></a>Kontrola kvality

[!include [banner](../includes/banner.md)]

Funkce *Kontrola kvality* umožňuje pracovníkům skladu provádět rychlé namátkové kontroly kvality, zatímco přijímají položky do oblasti příchozího doku. Tyto namátkové kontroly jsou výhodné, když pracovníci kontrolují obaly nebo jiné snadno rozpoznatelné části položky. Tato funkce vede pracovníky, aby se rychle podívali a zjistili, zda je něco zjevně vadné nebo poškozené před tím, než doplní zásoby ve skladovém místě po výdeji.

Tato funkce je alternativou ke standardnímu procesu kontroly kvality. Nabízí větší flexibilitu a rychlejší zpracování.

Při použití této funkce dojde ke kontrole příjezdu a kvality následujícím způsobem:

1. Když dorazí zásilka, pracovník skladu zaznamená příchod. Pracovník také naskenuje registrační značku a zaregistruje místo.
1. Pracovník provede rychlou kontrolu kvality a zaznamená výsledek (úspěšný nebo neúspěšný) dané registrační značky.
1. Nastane jedna z následujících akcí:

    - Pokud je kontrola kvality úspěšná, je registrační značka přijata a navedena obvyklým způsobem na přijímací místo.
    - Pokud se kontrola kvality nezdaří, je registrační značka odmítnuta a stávající práce výdeje pro ni je přesměrována na alternativní místo k další kontrole. Je vytvořena nová objednávka kvality. Chcete-li zobrazit objednávku kvality vytvořenou při kontrole kvality, která se nezdařila, přejděte na **Řízení zásob \> Periodické úkoly \> Řízení kvality \> Objednávky kvality**.

Tento proces lze také nastavit tak, aby všechny naskenované registrační značky byly okamžitě přesměrovány na místo kontroly kvality.

## <a name="turn-the-quality-check-feature-on-or-off"></a>Zapnutí nebo vypnutí funkce kontroly kvality

Chcete-li používat funkčnost popsanou v tomto tématu, musí být ve vašem systému zapnuta funkce *Kontrola kvality*. Od verze Supply Chain Management 10.0.25 je tato funkce povinná a nelze ji vypnout. Pokud používáte verzi starší než 10.0.25, mohou správci tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Kontrola kvality* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="set-up-the-feature-for-the-example-scenario"></a>Nastavení funkce pro tento vzorový scénář

Tato část obsahuje pokyny a příklad, který ukazuje, jak nastavit funkci *Kontrola kvality* a připravit ukázková data pro příkladový scénář, který je uveden dále v tomto tématu.

### <a name="make-sample-data-available"></a>Příprava ukázkových dat

Chcete-li s [příkladovým scénářem](#example-scenario) pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.

### <a name="quality-check-template"></a><a name="quality-template"></a>Šablona kontroly kvality

Šablona kontroly kvality definuje pravidla pro provádění rychlých přímých kontrol kvality v době přijetí.

1. Přejděte do **Řízení skladu \> Nastavení \> Práce \> Šablona kontroly kvality**.
1. Chcete-li přidat šablonu do mřížky, klikněte na tlačítko **Nový**.
1. Definujte novou šablonu nastavením následujících hodnot:

    - **Název šablony kontroly kvality:** *Dock check*

        Zadejte název, který identifikuje zásady použité pro tuto šablonu.

    - **Zásady přijímání:** *Vyzvat uživatele*

        Určete, zda by uživatelé měli být při zpracování práce vyzváni k přijetí nebo odmítnutí kvality zásob, nebo zda by kvalita měla být automaticky odmítnuta. Dostupné možnosti jsou *Automatické odmítnutí* a *Vyzvat uživatele*.

    - **Zásady zpracování kvality:** *Vytvořte objednávku kvality*

        Vyberte zásady, které by měly být použity při odmítnutí kvality zásob. Existují tyto možnosti:

        - *Vytvořit pouze práci* - Jednoduše vytvořte práci, která usnadní pohyb zásob.
        - *Vytvořit objednávku kvality* - Vytvořte objednávku kvality, která usnadní zkoušky kvality.

    - **Testovací skupina:** *Příloha*

        Určete testovací skupinu, která by měla být použita ve vytvořené objednávce kvality. Testovací skupiny jsou nastaveny v rámci modulu **Řízení zásob**.

        Nechte možnost **Destruktivní text** pro testovací skupinu vypnutou. Tato možnost definuje, zda při testech v testovací skupině dojde ke zničení vzorku. Pokud je použit destruktivní test, systém generuje transakci, když je pro položku vytvořena objednávka kvality. Nová skladová transakce odhadne snížení zásob pro testované množství. Dokončení objednávky kvality v kroku ověření způsobí snížení zásob. Skladová transakce je označena jako objednávka kvality.

### <a name="work-class--quality-check"></a><a name="work-class"></a>Třída práce - kontrola kvality

Pracovní třídy se používají k nasměrování a/nebo omezení typu řádků pracovních příkazů, které pracovníci skladu může v mobilním zařízení zpracovat.

1. Přejděte na **Řízení skladu \> Nastavení \> Práce \> Pracovní třídy**.
1. Zvolte **Nová** pro vytvoření třídy práce.
1. V záhlaví nastavte následující hodnoty:

    - **ID pracovní třídy:** *Kontrola kvality*

        Zadejte název, který identifikuje pracovní třídu.

    - **Popis:** *Kontrola kvality*

        Zadejte krátký popis, který označuje, k čemu je pracovní třída používána.

    - **Typ pracovního příkazu:** *Kontrola kvality*

        Vyberte typ pracovního příkazu vytvořeného pracovní třídou. Při nastavování kontroly kvality vždy vyberte *Kontrola kvality*.

1. Na pevné záložce **Platné typy umístění** nechte pole **Typ místa** prázdné.

    Pokud vyberete typ umístění, omezíte umístění, kam lze položky po jejich výběru umístit. Toto pole se používá, když se směrnice umístění pokusí o překlad umístění nebo když pracovník skladu ručně zadá umístění pro položku nabídky mobilního zařízení.

Další informace o pracovních třídách a o tom, jak je vytvořit, viz [Vytvoření pracovní třídy](tasks/create-work-class.md).

### <a name="work-template"></a>Šablona práce

Šablony práce umožňují definovat pracovní operace, které musí být provedeny ve skladu. Obvykle pracovní operace ve skladu sestávají z páru akcí: skladoví pracovníci vyskladní zásoby na skladě na jednom místě a převedou vyskladněné zásoby v jiném skladovém místě. Pracovní šablona pro kontrolu kvality definuje pracovní operace pro provádění kontroly kvality.

#### <a name="purchase-orders"></a>Nákupní objednávky

1. Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.
1. V záhlaví nastavte pole **Typ pracovního příkazu** na *Nákupní objednávky*.
1. V podokně akcí vyberte **Upravit**.
1. Vyberte pracovní šablonu, která by měla zahrnovat krok kontroly kvality. V části **Přehled** v poli **Šablona práce** vyberte *Příjemka NO 51*.
1. V části **Podrobnosti pracovní šablony** si všimněte, že mřížka má dva existující řádky: jeden pro *Výběr* a jeden pro *Vložení*.
1. V části **Podrobnosti pracovní šablony** vyberte **Nový** pro přidání řádku pro kontrolu kvality do mřížky. Všimněte si, že pole **Číslo řádku** pro nový řádek je nastaveno na *3*.
1. Na novém řádku nastavte následující hodnoty. Potvrďte výchozí hodnoty ve všech zbývajících polích.

    - **Typ práce:** *Kontrola kvality*
    - **ID pracovní třídy:** *Nákup*
    - **Název šablony kontroly kvality:** *Dock check*

        Vyberte jedinečný identifikátor pracovní třídy. Tato hodnota umožňuje konfiguraci položek nabídky mobilního zařízení a typů práce, které tyto položky nabídky mohou zpracovat.

1. V podokně Akce vyberte **Uložit** pro uložení dosavadní práce.

    Obdržíte informační zprávu, která uvádí: „Neplatné - kontrola kvality musí přijít ihned po vyzvednutí.“ Proto musíte změnit hodnotu **Číslo řádku** pro řádek, který jste právě přidali.

1. Postupujte podle těchto kroků a změňte hodnotu **Číslo řádku** pro nový řádek:

    1. V části **Podrobnosti pracovní šablony** vyberte řádek, na kterém je pole **Typ práce** nastaveno na *Kontrola kvality*.
    2. Vyberte tlačítko **Posunout nahoru** nebo **Posunout dolů** pro přesunutí řádku *Kontrola kvality* za řádek *Vyzvednout*.

1. V podokně akcí vyberte **Uložit**.

#### <a name="quality-in-quality-check"></a>Kvalita v kontrole kvality

Dále vytvořte pracovní šablonu pro kontrolu kvality.

1. V záhlaví **Pracovní šablony** změňte hodnotu pole **Typ pracovního příkazu** na *Kontrola kvality*.
1. V podokně Akce vyberte možnost **Nový** pro přidání řádku do mřížky v části **Přehled**.
1. Na novém řádku nastavte následující hodnoty:

    - **Šablona práce:** *51 Kontrola kvality*

        Zadejte název šablony.

    - **Popis šablony práce:** *51 Kontrola kvality*

1. Chcete-li, aby byla dostupná část **Podrobnosti šablony práce**, klikněte na **Uložit**.
1. Zatímco nová šablona je stále vybrána v části **Přehled**, vyberte **Nový** v části **Podrobnosti pracovní šablony** pro přidání řádku do mřížky.
1. Na novém řádku nastavte následující hodnoty:

    - **Typ práce:** *Výdej*
    - **ID pracovní třídy:** *Kontrola kvality*

        Vyberte název [pracovní třídy](#work-class), který jste dříve vytvořili pro práci s kontrolou kvality.

1. V části **Podrobnosti pracovní šablony** vyberte znovu **Nový** pro přidání jiného řádku.
1. Na novém řádku nastavte následující hodnoty:

    - **Typ práce:** *Vložit*
    - **ID pracovní třídy:** *Kontrola kvality*

        Vyberte název [pracovní třídy](#work-class), který jste dříve vytvořili pro práci s kontrolou kvality.

1. V podokně akcí vyberte **Uložit**.

Další informace týkající se šablon práce naleznete v tématu [Řízení práce ve skladu pomocí šablon práce a směrnic umístění](control-warehouse-location-directives.md).

### <a name="location-directive--quality-failures"></a>Směrnice o umístění - selhání kvality

Směrnice skladového místa jsou pravidla, která pomáhají identifikovat místa vyskladnění a umístění pro pohyb zásob. V transakce prodejní objednávky například směrnice skladového místa určuje, které zboží bude vydáno a kam bude umístěno. Musíte definovat pravidlo směrnice o umístění, abyste určili, jak budou prováděny kontroly kvality, které selhaly.

1. Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.
1. V levém podokně nastavte pole **Typ pracovního příkazu** na *Nákupní objednávky* na práci se směrnicemi místa tohoto typu.
1. V podokně Akce vyberte možnost **Nová** k vytvoření direktivy místa pro kontroly kvality.
1. V záhlaví nastavte následující hodnoty:

    - **Pořadové číslo:** Přijměte výchozí hodnotu.
    - **Název:** *51 do kvality*

1. Na záložce s náhledem **Směrnice skladového místa** natavte následující hodnoty. Potvrďte výchozí hodnoty ve všech zbývajících polích.

    - **Typ práce:** *Vložit*
    - **Lokalita:** *5*
    - **Sklad:** *51*

1. V podokně akcí kliknutím na **Uložit** uložte direktivu a zpřístupněte pevnou záložku **Řádky**.
1. Na záložce s náhledem **Řádky** přidejte řádek do mřížky výběrem možnosti **Nový**.
1. Na novém řádku nastavte následující hodnoty. Potvrďte výchozí hodnoty ve všech zbývajících polích.

    - **Od množství:** *1*
    - **Do množství:** *1000000*

1. V podokně akcí kliknutím na **Uložit** uložte nový řádek a zpřístupněte pevnou záložku **Akce direktivy místa**.
1. Když je na pevné záložce **Řádky** vybrán nový řádek, vyberte **Nový** na pevné záložce **Akce směrování polohy** pro přidání řádku do mřížky, abyste mohli nastavit akci pro linku.
1. V novém řádku nastavte pole **Název** na *Kvalita*. Potvrďte výchozí hodnoty ve všech zbývajících polích.
1. V podokně akcí vyberte možnost **Uložit**, chcete-li, aby bylo tlačítko **Upravit dotaz** dostupné na pevné záložce **Akce direktivy umístění**.
1. V době, kdy je řádek, který jste právě přidali, stále vybrán na pevné záložce **Akce směrování polohy**, vyberte **Upravit dotaz** pro otevření dialogového okna, ve kterém můžete upravit dotaz pro akci.
1. Na kartě **Oblast** přidejte řádek do dotazu výběrem možnosti **Přidat**.
1. Na novém řádku nastavte následující hodnoty:

    - **Tabulka:** *umístění*
    - **Odvozená tabulka:** *Skladová místa*
    - **Pole:** *Skladové místo*
    - **Kritéria:** *QMS*

    Umístění *QMS* je umístění skladu pro kvalitu.

1. Zvolte **OK** a zavřete dialogové okno.
1. Nyní je nutné změnit pořadí existujících direktiv umístění pro sklad *51*. Uložte novou direktivu umístění *51 do kvality*, aktualizujte stránku a v seznamu vyberte direktivu o umístění. Potom v podokně akcí pomocí tlačítka **posunout nahoru** a **Posunout dolů** umístěte direktivu umístění pro sklad *51* v následujícím pořadí. (Před výběrem **Posunout nahoru** nebo **Posunout dolů** musíte v seznamu vybrat direktivu o umístění.)

    1. 51 Do kvality
    2. 51 PO Direct
    3. 51 QMS

### <a name="mobile-device-menu-items"></a>Položky nabídky mobilního zařízení

Nakonfigurujte položku nabídky tak, aby mobilní zařízení mohla provádět funkci **Kontrola kvality**.

#### <a name="purchase-putaway"></a>Výdej nákupu

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V seznamu vyberte položku nabídky mobilního zařízení **Nákupní vyskladnění**.
1. V podokně akcí vyberte **Upravit**.
1. V části **Pracovní třídy** přidejte řádek do mřížky výběrem možnosti **Nová**.
1. Na novém řádku nastavte následující hodnoty:

    - **ID pracovní třídy:** *Kontrola kvality*

        Zadejte název [pracovní třídy](#work-class), který jste dříve vytvořili pro práci s kontrolou kvality.

    - **Typ pracovního příkazu:** *Kontrola kvality*

1. V podokně akcí vyberte **Uložit**.

#### <a name="purchase-order-line-receiving"></a>Přijetí řádku nákupní objednávky

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V podokně akcí zvolte **Nový**.
1. V záhlaví nastavte následující hodnoty:

    - **Název položky nabídky:** *Příjem řádku PO*
    - **Název:** *Příjem řádku PO*
    - **Režim:** *Práce*
    - **Použít existující práci:** *Ne*

1. Na záložce s náhledem **Obecné** nastavte následující hodnoty. Potvrďte výchozí hodnoty ve všech zbývajících polích.

    - **Proces tvorby práce:** *Příjem a vyskladnění řádku nákupní objednávky*
    - **Generovat registrační značky:** *Ano*
    - **Pracovní šablona:** *51 Příjemka NO*

1. V podokně akcí vyberte **Uložit**.

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a>Přidání položky nabídky do nabídky mobilního zařízení

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.
1. V levém podokně vyberte nabídku **Příchozí**.
1. V podokně akcí vyberte **Upravit**.
1. Ve sloupci **Dostupné nabídky a položky nabídky** najděte a vyberte novou položku nabídky **Příjem řádku PO**.
1. Stisknutím tlačítka se šipkou doprava přesuňte **Příjem řádku NO** do sloupce **Struktura nabídky**.
1. Ve sloupci **Struktura nabídky** vyberte **Příjem řádku PO** a poté pomocí tlačítka se šipkou nahoru nebo dolů přesuňte položku nabídky na požadovanou pozici v nabídce mobilního zařízení.
1. V podokně akcí vyberte **Uložit**.

## <a name="example-scenario"></a><a name="example-scenario"></a>Příklad

Po zpřístupnění a nastavení všech výše popsaných vzorových dat můžete v rámci tohoto scénáře vyzkoušet funkci *Kontrola kvality*. Hodnoty zobrazené v tomto scénáři předpokládají, že pracujete se standardními ukázkovými daty, která jste vybrali v právnické osobě **USMF** a připravili jste vzorové záznamy, které jsou popsány dříve v tomto tématu. Tento scénář také slouží jako příklad, který ukazuje, jak lze funkci použít v produkčním nastavení.

### <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky

1. Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. V podokně akcí zvolte **Nový**.
1. V dialogovém okně **Vytvoření nákupní objednávky** nastavte následující hodnoty:

    - **Účet dodavatele:** *104*
    - **Sklad:** *51*

1. Vyberte **OK** - nová prodejní objednávka se vytvoří a dialogové okno se zavře.
1. Na pevné záložce **Řádky prodejní objednávky** obsahuje mřížka nový prázdný řádek. Na tomto řádku nastavte následující hodnoty:

    - **Číslo položky:** *M9203*
    - **Množství:** *3*
    - **Jednotka:** *PL*

1. V podokně akcí vyberte **Uložit**.

### <a name="process-quality-check-receiving"></a>Zpracování příjmu kontroly kvality

Po vytvoření nákupní objednávky ji můžete obdržet pomocí položky nabídky **Příjem řádku PO** a funkčnosti funkce *Kontrola kvality*.

#### <a name="receive-pallet-1"></a>Příjem palety 1

1. Přihlaste se do mobilní aplikace Řízení skladu jako uživatel skladu *51*. (Zadejte *51* jako ID uživatele a *1* jako heslo.)
1. Jděte na **Příchozí \> Příjem řádku PO**.
1. V poli **PONUM** zadejte číslo nákupní objednávky.
1. Potvrďte znovu číslo nákupní objednávky.
1. Do pole **LINENUM** zadejte číslo řádku z nákupní objednávky, kterou přijímáte. Protože objednávka má v tomto scénáři pouze jeden řádek, zadáte *1* v poli **LINENUM** pro každý krok příjmu.
1. Potvrďte číslo řádku.
1. Do pole **QTY** zadejte množství pro přijetí. Protože objednávka platí pro tři palety (*PL*) v tomto scénáři a existují tři kroky příjmu, zadáte hodnotu *1* do pole **QTY** pro každý krok příjmu.
1. Potvrďte množství.

    Stránka **Kontrola kvality**, která se objeví, nemá žádná vstupní pole. Ve spodní části je pouze potvrzovací tlačítko (znak zaškrtnutí) a tlačítko Nabídka (**≡**) nahoře. (Tlačítko Nabídka se někdy označuje jako hamburger nebo hamburgerové tlačítko.) Pro urychlení procesu kontroly kvality, když paleta projde kontrolou kvality, uživatel pouze potvrdí stránku **Kontrola kvality**.

    ![Stránka Kontrola kvality.](media/quality-check.png "Stránka Kontrola kvality")

1. Vyberte potvrzovací tlačítko a předejte kontrolu kvality palety 1 z řádku 1.

    Stránka **Objednávky: Vložit**, která se objeví, zobrazuje podrobnosti o práci vložení:

    - **LOC:** Systém určil umístění

        Toto místo je určeným místem výdeje pro příjem nákupní objednávky.

    - **LP:** Systémem generované ID poznávací značky
    - **Položka:** *M9203*
    - **Množství:** *1 PL: 100 ea*

    Zobrazí se také popis položky.

1. Potvrďte práci zaskladnění.

    Na stránce **Úkol** pro přijetí řádku objednávky obdržíte zprávu „Dokončena práce“. Pole **LINENUM** je k dispozici, takže můžete začít přijímat další paletu.

#### <a name="receive-pallet-2"></a>Příjem palety 2

U tohoto scénáře bude paleta 2 odmítnuta.

1. V poli **LINENUM** zadejte *1* a potvrďte číslo řádku.
1. Pole **QTY** je nyní k dispozici. Zadejte *1* a potvrďte množství.

    Zobrazí se stránka **Kontrola kvality**. Pro tento příjem bude paleta odmítnuta z hlediska kvality a bude vložena do umístění kvality *QMS*.

1. Vyberte tlačítko Nabídka (**≡**) v horní části stránky a poté v nabídce vyberte možnost **Odmítnout**.
1. Na stránce **Úkol**, která se zobrazí, zadejte **QMS** jako místo *vložení* pro odeslání palety k další kontrole.

    Stránka **Kvalita v kontrole kvality: Vložit**, která se objeví, zobrazuje podrobnosti o práci vložení:

    - **LOC:** *QMS*

        Toto místo je určeným místem výdeje pro příjem odmítnuté kvality.

    - **LP:** Systémem generované ID poznávací značky
    - **Položka:** *M9203*
    - **Množství:** *1 PL: 100 ea*

    Zobrazí se také popis položky.

1. Potvrďte práci zaskladnění.

    Na stránce **Úkol** pro přijetí řádku objednávky obdržíte zprávu „Dokončena práce“. Pole **LINENUM** je k dispozici, takže můžete začít přijímat další paletu.

Nyní jste dokončili kontrolu kvality a vytvořili jste objednávku kvality pro odmítnutou paletu. Chcete-li zobrazit vytvořenou objednávku kvality, přejděte na **Řízení zásob \> Periodické úkoly \> Řízení kvality \> Objednávky kvality**.

Testování objednávky kvality je nyní možné zpracovat. V tomto tématu není zahrnuto testování kvality.

Další informace o řízení kvality naleznete v tématu [Přehled řízení kvality](../inventory/enable-quality-management.md).

#### <a name="receive-pallet-3"></a>Příjem palety 3

U tohoto scénáře bude paleta 3 přijata.

1. V poli **LINENUM** zadejte *1* a potvrďte číslo řádku.
1. Pole **QTY** je nyní k dispozici. Zadejte *1* a potvrďte množství.

    Zobrazí se stránka **Kontrola kvality**. Pro tento příjem bude paleta přijata z hlediska kvality a bude vložena do umístění hromadného výdeje.

1. Vyberte potvrzovací tlačítko pro předání kontroly kvality.

    Stránka **Objednávky: Vložit**, která se objeví, zobrazuje podrobnosti o práci vložení:

    - **LOC:** Systém určil umístění

        Toto místo je určeným místem výdeje pro příjem nákupní objednávky.

    - **LP:** Systémem generované ID poznávací značky
    - **Položka:** *M9203*
    - **Množství:** *1 PL: 100 ea*

    Zobrazí se také popis položky.

1. Potvrďte práci zaskladnění.

    Na stránce **Úkol** pro přijetí řádku objednávky obdržíte zprávu „Dokončena práce“. Pole **LINENUM** je k dispozici, takže můžete začít přijímat další paletu.

1. Vyberte tlačítko Nabídka (**≡**) v horní části stránky a poté v nabídce vyberte možnost **Zrušit** pro návrat do nabídky.

Nyní můžete mobilní aplikaci zavřít.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]