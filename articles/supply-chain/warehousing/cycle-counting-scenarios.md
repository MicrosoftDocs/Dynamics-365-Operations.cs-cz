---
title: Ukázkové scénáře cyklické inventury
description: Tento článek poskytuje kolekci scénářů, které zkoumají funkce cyklické inventury v Microsoft Dynamics 365 Supply Chain Management.
author: GalynaFedorova
ms.date: 06/08/2021
ms.topic: article
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 90a3f132a96081b56ab60f5b0ba5cc328b820879
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899317"
---
# <a name="cycle-counting-example-scenarios"></a>Ukázkové scénáře cyklické inventury

[!include [banner](../includes/banner.md)]

Tento článek poskytuje kolekci scénářů, které zkoumají funkce cyklické inventury v Microsoft Dynamics 365 Supply Chain Management. Nejprve popisuje požadavky na vaše stávající prostředí Supply Chain Management. Poté vysvětluje, jak konfigurovat cyklické inventury, a popisuje všechny fáze cyklické inventury. Po dokončení byste měli dobře rozumět cyklickým inventurám, včetně řízených cyklických inventur, cyklických inventur naslepo, místních cyklických inventur, prahových hodnot cyklické inventury a plánů cyklických inventur.

## <a name="prerequisites"></a>Předpoklady

### <a name="make-demo-data-available"></a>Zpřístupnění ukázkových dat

Každý scénář v tomto článku odkazuje na hodnoty a záznamy, které jsou součástí standardních ukázkových dat poskytovaných pro Supply Chain Management. Pokud chcete při procházení scénářů použít hodnoty, které jsou zde uvedeny, nezapomeňte pracovat v prostředí, ve kterém jsou nainstalovaná ukázková data, a nastavte právnickou osobu (společnost) na **USMF**, než začnete.

### <a name="turn-on-support-for-the-warehouse-management-mobile-app"></a>Zapněte podporu pro mobilní aplikaci Warehouse Management

Chcete-li používat mobilní aplikaci Warehouse Management, musí být ve vašem systému zapnutá funkce *Uživatelská nastavení, ikony a názvy kroků pro novou skladovou aplikaci*. Od verze Supply Chain Management 10.0.25 je tato funkce povinná a nelze ji vypnout. Pokud používáte verzi starší než 10.0.25, mohou správci tuto funkčnost zapnout nebo vypnout vyhledáním funkce *Uživatelská nastavení, ikony a názvy kroků pro novou skladovou aplikaci* v pracovním prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="prepare-demo-data-for-the-scenarios"></a><a name= "prepare-demo-data"></a>Připravte ukázková data pro scénáře

Pomocí těchto kroků potvrďte, že jsou ve vašem systému k dispozici všechna demo data požadovaná pro scénáře ve společnosti USMF. Vytvořte všechny záznamy nebo hodnoty, které chybí.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Pracovník**.
1. V podokně seznamu vyberte **Julia Funderburk**.
1. Na pevné záložce **Uživatelé** vyberte řádek, který má následující hodnoty. Pokud žádný z těchto řádků nemá tyto hodnoty, vytvořte je.

    - **ID uživatele:** *61*
    - **Uživatelské jméno:** *WH61*
    - **Výchozí sklad:** *61*
    - **Název nabídky:** *Hlavní*

1. Na pevné záložce **Práce** nastavte následující hodnoty pro uživatele *61*, pokud ještě nejsou nastaveny:

    - **Je supervizorem cyklické inventury:** *Ne*
    - **Maximální limit procent:** *0*
    - **Maximální limit množství:** *0*
    - **Maximální limit hodnoty:** *0*

1. Přejděte na **Řízení skladu \> Nastavení \> Práce \> Fondy práce**.
1. Fondy práce se používají k oddělení skladové práce podle typu práce (v tomto případě na práci cyklické inventury). Ujistěte se, že existuje záznam, který má následující nastavení:

    - **ID fondu práce:** *CycleCount*
    - **Popis:** *Cyklická inventura*

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V podokně seznamu vyberte záznam s názvem *Cyklická inventura*. Pokud žádná položka nemá tento název, vytvořte ji. Potvrďte nebo nastavte pro záznam následující hodnoty:

    - **Název položky nabídky:** *Cyklická inventura*
    - **Titul:** *Řízená cyklická inventura*
    - **Režim:** *Práce*
    - **Použít existující práci:** - *Ano*
    - **Řídí:** *Řízeno systémem* (Tato hodnota označuje, že Supply Chain Management přiřadí ID práce cyklické inventury.)
    - **Zobrazit stav zásob:** *Ano*

1. V podokně Akce klikněte na možnost **Cyklická inventura**.
1. V dialogovém okně **Cyklická inventura na mobilním zařízení** potvrďte nebo nastavte následující hodnoty:

    - **Zobrazit číslo položky:** *Ano*
    - **Zobrazit registrační značky:** *Ano*
    - **Počet pokusů:** *1*

1. Zvolte **OK** a zavřete dialogové okno.
1. V podokně seznamu vyberte záznam s názvem *Cyklická inventura naslepo*. Pokud žádná položka nemá tento název, vytvořte ji. Potvrďte nebo nastavte pro záznam následující hodnoty:

    - **Název položky nabídky:** *Cyklická inventura naslepo*
    - **Titul:** *Cyklická inventura naslepo*
    - **Režim:** *Práce*
    - **Použít existující práci:** - *Ano*
    - **Řídí:** *Seskupení cyklické inventury* (Tato hodnota ukazuje, že pracovník může seskupit ID cyklické inventury specifické pro určité místo, zónu nebo fond práce.)

1. V podokně Akce klikněte na možnost **Cyklická inventura**.
1. V dialogovém okně **Cyklická inventura na mobilním zařízení** potvrďte nebo nastavte následující hodnoty:

    - **Zobrazit číslo položky:** *Ne*
    - **Zobrazit registrační značky:** *Ne*
    - **Počet pokusů:** *0*

1. Zvolte **OK** a zavřete dialogové okno.
1. V podokně seznamu vyberte záznam s názvem *Inventura na místě*. Pokud žádná položka nemá tento název, vytvořte ji. Potvrďte nebo nastavte pro záznam následující hodnoty:

    - **Název položky nabídky:** *Inventura na místě*
    - **Název:** *Místní inventura*
    - **Režim:** *Práce*
    - **Použít existující práci:** *Ne*
    - **Proces tvorby práce:** *Místní cyklická inventura* (Hodnota označuje, že pracovník může provádět cyklickou inventuru v umístění ve skladu kdykoliv, aniž by vytvořil cyklickou inventuru. Pokud chcete provádět cyklickou inventuru v daném místě, pracovník musí zadat ID tohoto místa.)

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.
1. V podokně seznamu vyberte záznam s názvem *Zásoby*. Pokud žádná položka nemá tento název, vytvořte ji. Potvrďte, že se v nabídce zobrazí následující položky nabídky cyklické inventury ve sloupci **Struktura nabídky**:

    - Cyklická inventura
    - Cyklická inventura naslepo
    - Místní inventura

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.
1. Na kartě **Cyklická inventura** natavte následující hodnoty:

    - **Výchozí typ úpravy cyklické inventury:** *Cyklická inventura* (Toto pole určuje typ deníku, který se zaúčtuje, když se provede cyklická inventura.)
    - **Výchozí ID pracovní třídy pro cyklickou inventuru:** *CCount* (Toto pole určuje pracovní třídu, která se používá pro cyklickou inventuru.)
    - **Výchozí pracovní priorita cyklické inventury:** *50* (Toto pole nastavuje prioritu, kterou má práce cyklické inventury ve srovnání s jinými typy prací ve skladu. Zadáním čísla, které je nižší, než je číslo zadané pro jiné typy prací, můžete zvýšit prioritu práce cyklické inventury.)

1. Přejděte na **Řízení skladu \> Nastavení \> Zásoby \> Typy vyrovnání**.
1. Stránka **Typy vyrovnání** umožňuje vytvářet kódy pro různé příchozí a odchozí vyrovnání, které mohou nastat. Potvrďte, že existuje záznam, který má následující nastavení:

    - **Typ vyrovnání zásob:** *Cyklická inventura*
    - **Popis:** *Cyklická inventura*
    - **Název:** *ICnt*

1. Přejděte na **Řízení skladu \> Nastavení \> Nastavení skladu \> Sklady**.
1. V podokně seznamu vyberte sklad *61*. Pokud žádná položka nemá tento název, vytvořte ji.
1. Na pevní záložce **Sklad** natavte následující hodnoty:

    - **Použít proces řízení skladu:** *Ano* (Tato hodnota umožňuje skladu pro procesy správy skladu.)
    - **Povolit pohyby registrační značky během cyklické inventury:** *Ano* (Tato hodnota umožňuje pracovníkům přesouvat poznávací značky během počtu cyklů.)

## <a name="scenario-1-guided-cycle-counting"></a>Scénář 1: řízená cyklická inventura

Než může dojít k řízené cyklické inventury, musíte vytvořit nějakou práci. Tato práce provede přiřazenou osobu skladem, od místa k místu, k dokončení inventur, které jsou v práci nastaveny.

### <a name="create-cycle-counting-work-for-scenario-1"></a>Vytvořit práci cyklické inventury pro scénář 1

Pomocí těchto kroků vytvořte práci cyklické inventury pro umístění položky *01A02R2S2B* (BULK-06) ve skladu *61*.

1. Přejděte do **Řízení skladu \> Cyklická inventura \> Práce cyklické inventury dle umístění**.
1. V dialogovém ikně **Vytvořit práci cyklické inventury podle umístění** nastavte pole **ID fondu práce** na *CycleCount*.
1. Na pevné záložce **záznamy, které mají být zahrnuty** vyberte možnost **Filtr**.
1. V dialogovém okně editoru dotazů na kartě **Rozsah** postupujte takto:

    - Pro řádek, kde je pole **Pole** nastaveno na *Sklad*, nastavte pole **Kritéria** na *61*.
    - Pro řádek, kde je pole **Pole** nastaveno na *Umístění*, nastavte pole **Kritéria** na *01A02R2S2B*.

1. Vyberte **OK** a dialogové okno editor dotazu zavřete.
1. Vyberte **OK** a zavřete dialogové okno **Vytvořit práci cyklické inventury podle umístění**.

    Po dokončení procesu vytváření práce se v centru akcí zobrazí zpráva.

1. Přejděte do **Řízení skladu \> Práce \> Podrobnosti práce**.
1. Najděte nově vytvořenou práci nastavením filtru na sloupec **ID fondu práce** k vyhledání záznamů, které mají hodnotu *CycleCount*.

### <a name="do-cycle-counting-work-for-scenario-1"></a>Proveďte práci cyklické inventury pro scénář 1

Po vytvoření práce cyklické inventury provedete práci prostřednictvím inventury položek v umístění skladu a zadáním do Supply Chain Management pomocí mobilního zařízení. Podle těchto kroků proveďte práci cyklické inventury v mobilní aplikaci Warehouse Management.

1. Přihlaste se do mobilní aplikace Warehouse Management jako pracovní uživatel, kterého jste nastavili v sekci [Připravit ukázková data pro scénáře](#prepare-demo-data) dříve v tomto článku. V příkladu v tomto článku je uživatel pojmenován *Julia Funderburk* a je nastaven na sklad *61*. (Demo data USMF by vám měla umožnit přihlásit se jako tento pracovní uživatel zadáním *61* jako ID uživatele a *1* jako heslo.)
1. V hlavní nabídce vyberte **Zásoby**.
1. V nabídce **Zásoby** vyberte **Řízená cyklická inventura**.
1. Vyberte pole **Množství**, zadejte *9* pomocí číselné klávesnice a poté vyberte **OK** (tlačítko zaškrtnutí).
1. Systém očekával, že pro tuto položku, umístění a poznávací značku zadáte počet 10 kusů. Proto budete požádáni o přepočítání. Vyberte pole **Množství**, opět zadejte *9* pomocí číselné klávesnice a poté vyberte **OK** (tlačítko zaškrtnutí). Na druhý pokus bude vaše inventura přijata.

    > [!NOTE]
    > Když systém zjistil rozdíl mezi očekávaným množstvím na skladě a množstvím, které jste zadali, požádal vás, abyste inventuru opakovali, protože pole **Počet pokusů** je nastaveno na *1* pro položku nabídky mobilního zařízení **Řízená cyklická inventura**. Byli jste vedeni k určitému číslu položky a číslu registrační značky, protože možnosti **Zobrazit číslo položky** a **Zobrazit registrační značku** jsou nastaveny na *Ano* pro položku nabídky mobilního zařízení.

1. Vyberte tlačítko **OK** (tlačítko zaškrtnutí).

### <a name="review-the-cycle-counting-differences-for-scenario-1"></a>Zkontrolujte rozdíly cyklické inventury pro scénář 1

Podle těchto kroků zkontrolujte rozdíly cyklické inventury.

1. Vraťte se do aplikace Supply Chain Management.
1. Přejděte do **Řízení skladu \> Práce \> Podrobnosti práce**.
1. Najděte a vyberte práci cyklické inventury, na kterou jste se podívali dříve. (Například nastavte filtr na slouopec **ID fondu práce** k vyhledání záznamů, které mají hodnotu *CycleCount*.) Všimněte si, že pole **Stav práce** pro tuto práci je nyní nastaveno na *Čeká na kontrolu*.

    > [!NOTE]
    > Pro pracovní uživatelský účet, který jste použili k provádění inventury, je možnost **Vedoucí cyklické inventury** nastavena na *Ne* a pole **Maximální procentní limit**, **Limit maximálního množství** a **Limit maximální hodnoty** jsou nastavena na *0* (nula). Proto všechny rozdíly v inventuře, které tento uživatel hlásí, musí být schváleny ručně a pole **Stav práce** pro související práci je nastaveno na *Čeká na kontrolu*. Pokud byla spočítaná hodnota v mezích odchylek (jak je uvedeno v polích **Maximální procentní limit** nebo **Limit maximálního množství** na stránce **Pracovní uživatelé**), nebo pokud byla možnost **Vedoucí cyklické inventury** pro uživatele nastavena na *Ano*, práce by byla automaticky uzavřena.

1. V podokně akcí na kartě **Práce** zvolte **Cyklická inventura**.
1. V podokně Akce klikněte na možnost **Přijmout množství**.

    Rozdíl se zaúčtuje pomocí standardního deníku inventury a vytvoří se nový pracovní příkaz.

1. Na stránce **Transakce cyklické inventury**, v podokně akcí, vyberte **Odvozená práce** pro nalezení práce, která byla vytvořena pro schválený rozdíl.

## <a name="scenario-2-blind-cycle-counting"></a>Scénář 2: cyklická inventura naslepo

Tento scénář vyžaduje, aby scénář 1 již byl ve vašem systému dokončen.

### <a name="create-cycle-counting-work-for-scenario-2"></a>Vytvořit práci cyklické inventury pro scénář 2

Než může dojít k cyklické inventuře naslepo, musíte vytvořit nějakou práci. Pomocí těchto kroků vytvořte práci cyklické inventury pro umístění položky *01A02R2S2B* (BULK-06) ve skladu *61*.

1. -Přejděte do **Řízení skladu \> Cyklická inventura \> Práce cyklické inventury dle položky**.
1. V dialogovém ikně **Vytvořit práci cyklické inventury podle položky** nastavte pole **ID fondu práce** na *CycleCount*.
1. Na pevné záložce **záznamy, které mají být zahrnuty** vyberte možnost **Filtr**.
1. V dialogovém okně Editor dotazů na kartě **Oblast** přidejte tři řádky, který mají nasledující nastavení:

    - Řádek 1:

        - **Tabulka:** *Položky*
        - **Pole:** *Číslo položky*
        - **Kritéria:** *L0101*

    - Řádek 2:

        - **Tabulka** *Dimenze zásob*
        - **Pole:** *Sklad*
        - **Kritéria:** *61*

    - Řádek 3:

        - **Tabulka** *Dimenze zásob*
        - **Pole:** *Skladové místo*
        - **Kritéria:** *01A02R2S2B*

1. Vyberte **OK** a dialogové okno editor dotazu zavřete.
1. Vyberte **OK** a zavřete dialogové okno **Vytvořit práci cyklické inventury podle položky**.

    Po dokončení procesu vytváření práce obdržíte informační zprávu.

### <a name="do-cycle-counting-work-for-scenario-2"></a>Proveďte práci cyklické inventury pro scénář 2

Po vytvoření práce cyklické inventury podle těchto kroků proveďte práci v mobilní aplikaci Warehouse Management.

1. Přihlaste se do mobilní aplikace Warehouse Management jako pracovní uživatel, kterého jste nastavili v sekci [Připravit ukázková data pro scénáře](#prepare-demo-data) dříve v tomto článku. V příkladu v tomto článku je uživatel pojmenován *Julia Funderburk* a je nastaven na sklad *61*. (Demo data USMF by vám měla umožnit přihlásit se jako tento pracovní uživatel zadáním *61* jako ID uživatele a *1* jako heslo.)
1. V hlavní nabídce vyberte **Zásoby**.
1. V nabídce **Zásoby** vyberte **Cyklická inventura naslepo**.
1. Vyberte pole **ID zóny**, zadejte *BULK06* a potom vyberte **OK** (tlačítko zaškrtnutí).
1. Vyberte pole **Položka**, zadejte *L0101* a potom vyberte **OK** (tlačítko zaškrtnutí).
1. Vyberte pole **Registrační značka**, zadejte *LP\_BULK\_06\_01* a potom vyberte **OK** (tlačítko zaškrtnutí).
1. Vyberte pole **Množství**, zadejte *10* a potom vyberte **OK** (tlačítko zaškrtnutí).

    > [!NOTE]
    > Přestože systém zjistil rozdíl mezi očekávaným množstvím na skladě a množstvím, které jste naskenovali, nepožádal vás, abyste inventuru opakovali, protože pole **Počet pokusů** je nastaveno na *0* (nula) pro položku nabídky mobilního zařízení **Cyklická inventura naslepo**. Byli jste požádáni ke skenování čísla položky a čísla registrační značky, protože možnosti **Zobrazit číslo položky** a **Zobrazit registrační značku** jsou nastaveny na *Ne* pro položku nabídky mobilního zařízení.

1. Vyberte tlačítko **OK** (tlačítko zaškrtnutí).

### <a name="review-the-cycle-counting-differences-for-scenario-2"></a>Zkontrolujte rozdíly cyklické inventury pro scénář 2

Podle těchto kroků zkontrolujte rozdíly cyklické inventury.

1. Vraťte se do aplikace Supply Chain Management.
1. Přejděte na **Řízení skladu \> Společné \> Práce \> Cyklická inventura práce čeká na kontrolu**.
1. V podokně akcí na kartě **Práce** zvolte **Cyklická inventura**.
1. V podokně Akce klikněte na možnost **Odmítnout inventuru**.

    Protože rozdíl v inventuře byl odmítnut, práce je uzavřena.

## <a name="scenario-3-spot-cycle-counting"></a>Scénář 3: místní cyklická inventura

V záznamu množství na skladě se uvádí, že existuje množství položky *L0101* na skladě v umístění *01A02R2S2B*. Pracovník skladu je v umístění *01A02R2S1B*. I když by toto umístění mělo být prázdné, je plné. Pracovník skladu proto okamžitě provede počet míst v tomto umístění.

### <a name="do-cycle-counting-work-for-scenario-3"></a>Proveďte práci cyklické inventury pro scénář 3

Podle těchto kroků proveďte práci cyklické inventury v mobilní aplikaci Warehouse Management.

1. Přihlaste se do mobilní aplikace Warehouse Management jako pracovní uživatel, kterého jste nastavili v sekci [Připravit ukázková data pro scénáře](#prepare-demo-data) dříve v tomto článku. V příkladu v tomto článku je uživatel pojmenován *Julia Funderburk* a je nastaven na sklad *61*. (Demo data USMF by vám měla umožnit přihlásit se jako tento pracovní uživatel zadáním *61* jako ID uživatele a *1* jako heslo.)
1. V hlavní nabídce vyberte **Zásoby**.
1. V nabídce **Zásoby** vyberte **Místní inventura**.
1. Vyberte pole **Umístění**, zadejte *01A02R2S1B* a potom vyberte **OK** (tlačítko zaškrtnutí).

    Systém zjistí, že ve správě Supply Chain Management je místo prázdné.

1. Vyberte **Přidejte LP nebo položku**.
1. Vyberte pole **Položka**, zadejte *L0101* a potom vyberte **OK** (tlačítko zaškrtnutí).
1. Vyberte pole **Registrační značka**, zadejte *LP\_BULK\_06\_01* a potom vyberte **OK** (tlačítko zaškrtnutí).
1. Vyberte pole **Množství**, zadejte *9* a potom vyberte **OK** (tlačítko zaškrtnutí).

    Protože systém detekuje, že uvedená registrační značka je již k dispozici v jiném umístění v Supply Chain Management, bude tato poznávací značka přesunuta do aktuálního umístění. Systém vás proto požádá o potvrzení pohybu.

1. Vyberte tlačítko **OK** (tlačítko zaškrtnutí).

### <a name="review-the-cycle-counting-differences-for-scenario-3"></a>Zkontrolujte rozdíly cyklické inventury pro scénář 3

Podle těchto kroků zkontrolujte výsledky inventury.

1. Vraťte se do aplikace Supply Chain Management.
1. Přejděte do **Řízení skladu \> Společné \> Podrobnosti práce**.
1. Zaškrtněte tlačítko **Zobrazit zavřeno** v horní části mřížky.
1. Nastavte filtr pro funkce **Typ pracovního příkazu** na *Pohyb zásob*.

    Systém tento počet automaticky detekoval jako pohyb zásob. Tento pohyb je povolen, protože je možnost **Během cyklické inventury povolte pohyby registrační značky** nastavena na *Ano* pro sklad *61* na stránce **Sklady**.

## <a name="scenario-4-define-cycle-count-thresholds"></a>Scénář 4: Definujte prahové hodnoty cyklické inventury

Jedním ze způsobů, jak vytvořit práci cyklické inventury, je použití prahových hodnot. Prahová hodnota cyklické inventury označuje limit množství nebo procenta skladových položek. Při dosažení prahové hodnoty bude automaticky vytvořena práce cyklické inventury.

Například existuje 60 položek na skladovém místě, které má prahovou hodnotu cyklické inventury 40. Během transakce prodejní objednávky je 25 položek vyskladněno ze skladového místa a umístěno do přechodného skladového místa. Nový počet položek je o 35 menší, než jaká je prahová hodnota množství, a pro skladové místo je tak automaticky vytvořena cyklická inventura.

Chcete-li nastavit prahové hodnoty cyklické inventury, postupujte podle následujících pokynů:

1. Přejděte do **Řízení skladu \> Nastavení \> Cyklická inventura \> Prahové hodnoty cyklické inventury**.
1. V podokně akcí vyberte **Nový** k vytvoření prahové hodnoty a nastavte pro ni následující hodnoty:

    - **ID prahové hodnoty cyklické inventury:** *L0101*
    - **Popis:** *Prahová hodnota L0101*
    - **Prahové množství:** *2*
    - **Jednotka:** *EA*
    - **Prahová hodnota kapacity založená na procentech:** *0.00*
    - **Typ prahové hodnoty pro cyklickou inventuru:** *Množství*
    - **Zpracovart cyklickou inventuru okamžitě:** *Ano*
    - **Dny mezi cyklickými inventurami** *1*
    - **ID fondu práce:** *CycleCount*

1. V podokně akcí zvolte **Vybrat položky**.
1. V dialogovém okně editoru dotazů na kartě **Rozsah** vyhledejte řádek, kde je hodnota v poli **Pole** nastavena na *Číslo položky*. Nastavte pole **Kritéria** pro tento řádek na *L0101*.
1. Vyberte **OK** a dialogové okno editor dotazu zavřete.

    Nyní jste definovali prahovou hodnotu cyklické inventury pro položku *L0101*.

Pro položku *L0101* bude nyní vytvořena cyklická inventura na jakémkoli místě, pokud je množství na skladě menší než 2 a pokud datum poslední cyklické inventury pro místo není dnes.

## <a name="scenario-5-define-cycle-count-plans"></a>Scénář 5: Definujte plány cyklické inventury

Plány cyklické inventury vám umožňují automatizovat vytváření prací cyklické inventury. Každý plán cyklické inventury můžete nastavit pomocí konkrétních dotazů na položky a umístění. Po spuštění dávkové úlohy se vytvoří práce cyklické inventury pro všechna umístění, která odpovídají kritériím položky a umístění (až do maximálního počtu počtů, který je zadán pro plán). Když je vytvořena práce cyklické inventury, řádek inventurní práce obsahuje informace o skladovém místě, které je nutné zahrnout. Zásoby na skladě přidružené k tomuto místu nejsou blokovány. Proto je k dispozici pro rezervaci a odchozí zpracování, přestože existuje práce s otevřenou inventurou.

Chcete-li nastavit plán cyklické inventury, postupujte podle následujících pokynů:

1. Přejděte do **Řízení skladu \> Nastavení \> Cyklická inventura \> Plány cyklických inventur**.
1. V podokně Akce vyberte možnost **Nový** pro přidání řádku do mřížky a pak pro ni nastavte následující hodnoty:

    - **ID plánu cyklické inventury** *BULK06*
    - **Popis:** *Inventura umístění pro BULK06*
    - **ID fondu práce:** *CycleCount*
    - **Maximální počet cyklických inventur** *10*
    - **Dny mezi cyklickými inventurami** *10*
    - **Prázdná místa:** *Vyloučit prázdné*
    - **Šablona práce:** Toto pole ponechte prázdné.

1. V podokně akcí zvolte **Vybrat umístění**.
1. Zobrazí se standardní dialogové okno editoru dotazů. Na kartě **Oblast** přidejte řádek a nastavte pro ni následující hodnoty:

    - **Tabulka:** *umístění*
    - **Pole:** *ID zóny*
    - **Kritéria:** *BULK06*

1. Vyberte **OK** a dialogové okno editor dotazu zavřete.
1. V podokně Akce klikněte na možnost **Zpracovat plán cyklická inventura**.
1. V dialogovém okně **Plány cyklické inventury** na pevné záložce **Spustit na pozadí** nastavte u možnosti **Dávkové zpracování** hodnotu *Ano*.
1. Vyberte **Opakování**.
1. V dialogovém okně **Definujte opakování** nastavte dávkovou úlohu tak, aby začala okamžitě a byla spuštěna jednou za minutu, a aby neexistovalo žádné datum ukončení.
1. Zvolte **OK** a zavřete dialogové okno **Definovat opakování**.
1. Zvolte **OK** a zavřete dialogové okno **Plány cyklické inventury**.

    Zpráva vás informuje, že úloha byla přidána do dávkové fronty.

1. Přejděte na **Řízení skladu \> Společné \> Plánování cyklické inventury**. Plán začíná okamžitě a vytváří inventuru. Protože práce inventury nebyla dokončena, pole **Stav** je nastaveno na *Zpracovává se*. Po jedné minutě se hodnota sloupce **Celkový počet cyklických inventur** se změní na *1*.

    > [!NOTE]
    > Práce cyklické inventury nebude vytvořena, pokud je počet dní od poslední cyklické inventury menší než hodnota, kterou jste nastavili pro pole **Dny mezi cyklickými inventurami** pro plán cyklické inventury. Pokud je například hodnota zadaná v poli **Dny mezi cyklickými inventurami** nastavena na *5*, práce cyklické inventury bude vytvořena každých pět dní. Pokud je však práce cyklické inventury zpracovávána třetího dne, další práce cyklické inventury bude vytvořen pět dnů po zpracování poslední cyklické inventury, osmého dne.

1. V podokně akcí vyberte **Práce**, chcete-li zobrazit práci inventury, která byla vytvořena.
