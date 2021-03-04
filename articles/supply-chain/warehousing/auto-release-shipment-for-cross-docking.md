---
title: Automatická dodávka prodejní dodávky pro cross docking
description: Toto téma popisuje strategii cross dockingu, která umožňuje automaticky uvolnit objednávku do skladu v případě, že výrobní zakázka, která dodává množství poptávky, je vykázána jako dokončená, aby bylo množství přesunuto přímo z místa výstupu výroby do odchozího umístění.
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: b86fe2f3ea4321dbe598233018934187ba0d713a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423612"
---
# <a name="auto-release-shipment-for-cross-docking"></a>Automatická dodávka prodejní dodávky pro cross docking

[!include [banner](../includes/banner.md)]

Toto téma popisuje strategii cross dockingu, která umožňuje automaticky uvolnit objednávku do skladu, pokud je výrobní zakázka, která dodává množství poptávky, vykázána jako dokončená. Tímto způsobem je množství, které je požadováno pro splnění objednávky poptávky, přesunuto přímo z výstupního místa výroby do výstupního skladového místa.

Cross docking je tok zpracování skladu, v němž je množství potřebné ke splnění výstupní objednávky směrováno do výstupního překladiště objednávky nebo do pracovní oblasti v místě, kde byla přijata vstupní objednávka. (Vstupní objednávka může být nákupní objednávka, převodní příkaz nebo výrobní zakázka.) Vzhledem k tomu, že pokročilá funkce cross dockingu podporuje všechny objednávky dodávek a poptávky a vyžaduje, aby byla uvolněna výstupní poptávka před určením příležitosti pro přeložení, funkce dodávky s automatickou verzí má tyto charakteristiky:

- Podporuje pouze výrobní zakázky jako dodávku a jako požadavek pouze prodejní objednávky a převodní příkazy.
- Operaci cross dockingu lze spustit i v případě, že objednávka poptávky nebyla uvolněna do skladu před zaregistrováním příjemky dodávky (tj. předtím, než byla výroba hlášena jako dokončená).

Tato funkce cross dockingu má dvě výhody:

- Skladové operace mohou přeskočit krok odložení množství hotového zboží do běžného skladovacího prostoru, pokud tato množství budou pouze znovu vybrána ke splnění výstupní objednávky. Místo toho lze množství přesunout z místa výstupu do místa dodání/expedice. Tímto způsobem funkce pomáhají minimalizovat počet zpracování zásob a v důsledku toho pomáhá maximalizovat čas a ušetřit místo na dílně.
- Skladové operace mohou odložit uvolnění prodejních objednávek a převodních příkazů do skladu, dokud není výstup dokončeného zboží pro přidruženou výrobní zakázku hlášen jako dokončený. Tato výhoda může být obzvláště důležitá v prostředích výroby na zakázku, kde doba realizace výroby může být delší než doba realizace v prostředí výroby do skladu.

## <a name="prerequisites"></a>Předpoklady

| Předpoklad | Popis |
|---|---|
| Zboží | Položky musí být povoleny pro procesy správy skladu.<p>**Poznámka:** položky s povolenou skutečnou hmotností nelze zahrnout do procesů cross dockingu.</p> |
| Sklad | Sklad musí být povolen pro procesy správy skladu. |
| Šablony cross dockingu | Pro daný sklad musí být nastavena alespoň jedna šablona pro cross dockingu, která používá zásady **Při potvrzení dodávky**. |
| Pracovní třída | Pro typ pracovního příkazu **Cross docking** musí být vytvořeno ID pracovní třídy cross dockingu. |
| Šablony práce | K vytvoření práce vyzvednutí a vložení jsou vyžadovány šablony práce typu pracovního příkazu **Cross docking**. |
| Směrnice skladového místa | Směrnice skladových míst typu pracovního příkazu **Cross docking** jsou požadovány pro vedení práce vložení do skladů, kde budou zabalena a expedována množství prodejní objednávky. |
| Značení mezi objednávkou poptávky a výrobní zakázkou | Skladový systém může aktivovat automatické uvolnění dodávky odchozí objednávky a vytvořit práci cross dockingu z výstupního umístění na akci dokončené výroby, pouze pokud jsou prodejní objednávky a převodní příkazy rezervovány a označeny proti výrobní zakázce. |

## <a name="example-cross-docking-flow"></a>Příklad toku cross dockingu

Typický tok cross dockingu se skládá z následujících hlavních kroků.

1. Příjemce prodejní objednávky vytvoří prodejní objednávku pro produkt vyráběný na zakázku. Požadované množství obvykle není na skladě a je nutné je nejprve vyrobit.
2. Příjemce prodejní objednávky vytvoří výrobní zakázku přímo z řádku prodejní objednávky. Příjemce prodejní objednávky tímto způsobem rezervuje a označí množství prodejní objednávky proti množství výrobní zakázky. 

    Výrobní plánovač případně určí, že označení musí být aktualizováno při potvrzení plánovaných objednávek.

3. Výrobní zakázka prochází následujícími kroky:

    1. Plánovač výroby odhadne a uvolní výrobní zakázku. (Odhad zahrnuje rezervaci surovin a tato verze zahrnuje uvolnění do skladu.)
    2. Pracovník skladu zahájí a dokončuje výdej surovin z místa uložení do skladového místa ve výrobním vstupu podle výrobní zakázky.
    3. Výrobní zakázka je spuštěna operátorem dílenského řízení.
    4. V poslední operaci používá operátor stroje mobilní zařízení k ohlášení výrobní zakázky jako dokončené.

4. Systém používá nastavení k identifikaci události cross dockingu pro dvě propojené objednávky a poté dokončí tyto úlohy:

    1. Automaticky vydá přidruženou prodejní objednávku do skladu za účelem vytvoření dodávky.
    2. Automaticky vytvoří práci cross dockingu, která obsahuje pokyny pro výdej dokončeného zboží z výstupního umístění a jeho přesunutí do výstupního umístění, do kterého jsou zablokované direktivy umístění pro cross docking přiřazeny k prodejní objednávce.
    3. Vyzve operátora stroje k dokončení práce cross dockingu ihned po ohlášení výrobní zakázky jako dokončené.

5. Po dokončení operace cross dockingu a naložení množství na vozidlo, bude při výstupním plánování skladu potvrzena prodejní dodávka.

## <a name="example-scenario"></a>Příklad

V tomto scénáři musíte mít nainstalována ukázková data a musíte použít ukázkovou společnosti **USMF**.

### <a name="set-up-cross-docking-that-uses-the-auto-release-shipment-feature"></a>Nastavení cross dockingu, který používá funkci dodávky s automatickou verzí

#### <a name="cross-docking-template"></a>Šablona cross dockingu

1. Přejděte na **Řízení skladu** \> **Nastavení** \> **Práce** \> **Šablony cross dockingu**.
2. Zvolte **Nové**.
3. Do pole **Pořadové číslo** zadejte **1**.
4. Do pole **ID šablony cross dockingu** zadejte název, například **XDock\_RAF**.
5. V poli **Zásady uvolnění poptávky** vyberte **Při přijetí dodávky**.
6. Do pole **Sklad** zadejte číslo skladu, do kterého chcete nastavit proces cross dockingu. V tomto příkladu vyberte **51**.

    > [!NOTE]
    > Jakmile vyberete jako zásadu vydání poptávky pro šablonu **Při přijetí dodávky**, nebudou všechna ostatní pole na stránce k dispozici. Podobně nelze definovat žádné zdroje dodávek. Toto chování je způsobeno tím, že cross docking, který používá funkci automatické dodávky, podporuje jako zdroje dodávek pouze výrobní zakázky a vyžaduje, aby mezi prodejními objednávkami a výrobními zakázkami existovalo označení. Pokud jako zásadu uvolnění poptávky vyberete **Před přijetím dodávky**, budou pole na kartách **Plánování** a **Zdroje dodávky** dostupná a editovatelná.

#### <a name="work-classes"></a>Pracovní třídy

1. Přejděte na **Řízení skladu** \> **Nastavení** \> **Práce** \> **Pracovní třídy**.
2. Zvolte **Nové**.
3. Do pole **ID pracovní třídy** zadejte název, například **CrossDock**.
4. V poli **Typ pořadí pracovních činností** vyberte možnost **Cross docking**.

Chcete-li omezit typy míst, kam lze vložit dokončené zboží pro cross docking, můžete zadat jeden nebo více platných typů skladového místa.

#### <a name="work-templates"></a>Šablony práce

1. Přejděte do nabídky **Řízení skladu** \> **Nastavení** \> **Práce** \> **Pracovní šablony**.
2. V poli **Typ pořadí pracovních činností** vyberte možnost **Cross docking**.
3. Zvolte **Nové**.
4. Do pole **Pořadové číslo** zadejte **1**.
5. Do pole **Šablona práce** zadejte název, například **CrossDock\_51**.
6. Zvolte **Uložit**.
7. V části **Podrobnosti pracovní šablony** vyberte **Nová**.
8. Pro nový řádek vyberte v poli **Typ práce** možnost **Vybrat**. V poli **ID pracovní třídy** vyberte **CrossDock**.
9. Zvolte **Nové**.
10. Pro nový řádek vyberte v poli **Typ práce** možnost **Vložit**. V poli **ID pracovní třídy** vyberte **CrossDock**.

#### <a name="location-directives"></a>Směrnice skladového místa

Standardní proces zaskladnění hotového zboží vyžaduje, aby směrnice skladového místa **Vložit** provedla pohyb vyskladněných výrobních množství do obvyklého prostoru úložiště. Obdobně je nutné nastavit směrnici **Vložit** skladového místa pro cross docking, která určuje, že práce bude mít dokončené množství ve stanoveném výstupním umístění, které služby doplní přidruženou prodejní objednávku.

Pro cross docking, jako u pravidelného zaskladnění hotového zboží, nemusíte pro akci výdejky vytvořit směrnici skladového místa, protože je zadáno výstupní umístění. Kromě toho se očekává, že toto výstupní místo bude nastaveno jako výchozí výstupní místo na jednom ze záznamů souvisejících s prostředky (tj. zdroj, vztah skupiny prostředků nebo skupina prostředků) nebo jako výchozí místo dokončeného zboží pro stavil.

1. Přejděte do nabídky **Řízení skladu** \> **Nastavení** \> **Směrnice skladového místa**.
2. V poli **Typ pořadí pracovních činností** vyberte možnost **Cross docking**.
3. Zvolte **Nové**.
4. Do pole **Pořadové číslo** zadejte **1**.
5. Do pole **Název** zadejte název, například **Portál**.
6. V poli **Typ práce** vyberte **Vložit**.
7. V poli **Pracoviště** zvolte **5**.
8. V poli **Sklad** zvolte **51**.
9. Na pevné záložce **Řádky** vyberte **Nový**.
10. Do pole **Do množství** zadejte maximální množství rozsahu, například **1000000.**
11. Zvolte **Uložit**.
12. Na pevné záložce **akce směrnic skladového místa** vyberte možnost **nový**.
13. Do pole **Název** zadejte název, například **Portál**.
14. Zvolte **Uložit**.
15. Pomocí standardního dotazovacího zařízení můžete omezit místo vložení na jedno nebo více konkrétních skladových míst. Vyberte **Upravit dotaz** a vyberte **51** jako kritérium pro pole **Sklad** v tabulce **Místa**.

### <a name="cross-dock-finished-goods-to-the-outbound-location"></a>Cross dock dokončeného zboží do výstupního umístění

Chcete-li cross dock množství dokončeného zboží do výstupního místa související prodejní objednávky, postupujte podle následujících kroků.

1. Přejděte na **Prodej a marketing** \> **Prodejní objednávky** \> **Všechny prodejní objednávky**.
2. Zvolte **Nové**.
3. Pro záhlaví prodejní objednávky vyberte účet zákazníka **US-001** a sklad, který je nastaven pro cross docking, který používá funkci dodávky s automatickou verzí.
4. Přidejte řádek pro hotový produkt a jako množství zadejte **10**.
5. V části **Řádky prodejní objednávky** vyberte **Produkt a dodávka** \> **Výrobní zakázka**.
6. V dialogovém okně **vytvořit výrobní zakázku** zkontrolujte výchozí hodnoty a pak vyberte možnost **Vytvořit**. Vytvoří se nová výrobní zakázka a je propojena s prodejní objednávkou (tj. je rezervovaná a označená).
7. Volitelné: Změňte hodnotu pole **Množství** tak, aby byla větší než hodnota potřebná ke splnění prodejní objednávky. Pokud je výrobní množství ohlášeno jako dokončené, systém vytvoří práci cross dockingu pro označené množství a práci zaskladnění pro zbývající množství podle běžného postupu zpracování dokončeného zboží.

    Jak bylo zmíněno dříve, musí existovat označení mezi prodejní objednávkou a výrobní zakázkou. V opačném případě cross docking nebude fungovat. Označení lze vytvořit několika způsoby:

    - Systém může toto označení vytvořit automaticky v následujících situacích:

        - Výrobní zakázka je ručně vytvořena přímo z řádku prodejní objednávky (viz krok 6).
        - Plánované výrobní zakázky se potvrzují a pole **Aktualizovat označení** je nastaveno na hodnotu **Standardní**.

    - Uživatel může označení vytvořit ručně otevřením stránky **Označení** z řádku objednávky poptávky.

    > [!NOTE]
    > Označení nelze ručně vytvořit pro položky, které jsou nastaveny pro použití standardního a váženého průměru jako skladových modelů.

8. Na stránce **Výrobní zakázka** v podokně akcí na kartě **Výrobní zakázka** ve skupině **Zpracování** vyberte **Odhad** a pak vyberte **OK**. Objednávka je odhadnuta a množství suroviny je rezervováno pro výrobu.
9. V podokně akcí na kartě **Výrobní zakázka** ve skupině **Proces** vyberte **Uvolnit** a pak vyberte **OK**. Pro suroviny je vytvořena práce s vyskladněním.
10. Otevřete a zkontrolujte práci. V podokně akcí na kartě **Sklad** ve skupině **Obecné** vyberte **Podrobnosti práce**. Poznamenejte si ID práce.
11. Přihlaste se ke skladové aplikaci a spusťte práci ve skladu 51.
12. Přejděte na **Výroba** \> **Výběr výroby**.
13. Zadejte ID práce pro zahájení a dokončení výběru surovin. 

    Po ohlášení práce jako dokončené je množství surovin k dispozici ve vstupním místě výroby (**005** v ukázkových datech USMF) a spuštění výrobní zakázky může začít.

14. Na stránce **Výrobní zakázka** v podokně akcí na kartě **Výrobní zakázka** ve skupině **Zpracování** vyberte **Start** a pak vyberte **OK**.
15. V aplikaci přejděte na **Výroba** \> **RAF a odložení**.
16. Do pole **ID výroby** zadejte číslo výrobní zakázky a další povinné podrobnosti a vyberte **OK**.

Všimněte si, že dojde k následujícím událostem:

- Uvolnění do skladu je aktivováno pro propojenou prodejní objednávku.
- Na základě uvolnění, dodávky a cross dockingu je vytvořena práce. Tato práce instruuje operátora skladu a vybírá množství potřebná ke splnění řádku prodejní objednávky a umístí je do výstupního umístění, které je zadáno ve směrnici umístění pro cross docking.
- Pokud je množství výrobní zakázky vyšší než množství vyžadované prodejní objednávkou, bude vytvořena běžná práce při zaskladnění. Tato práce instruuje operátora skladu k vyskladnění množství dokončeného zboží, které zbývá po přeložení a jeho přesunutí do běžného skladu podle směrnice o skladovém místě.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]