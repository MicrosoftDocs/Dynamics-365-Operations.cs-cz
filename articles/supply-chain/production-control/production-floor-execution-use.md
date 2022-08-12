---
title: Jak pracovníci používají rozhraní pro provádění výrobního provozu
description: Tento článek popisuje, jak používat rozhraní pro provádění výrobního provozu z pohledu pracovníka.
author: johanhoffmann
ms.date: 01/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0d857ef31e0fed2a0d7550197209fac9251d8812
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069779"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Jak pracovníci používají rozhraní pro provádění výrobního provozu

[!include [banner](../includes/banner.md)]

Rozhraní pro provádění výrobního provozu je optimalizováno pro dotykovou interakci. Jeho provedení poskytuje vizuální kontrast, který splňuje požadavky na přístupnost pro prostředí dílny. Nabízí všechny funkce jako zařízení úkolového lístku. Umožňuje však také paralelní spuštění více úloh ze seznamu úloh. (Tato funkce je také známá jako *sdružování úloh*.) Navíc ze seznamu úloh mohou pracovníci otevřít průvodce, který byl vytvořen v Microsoft Dynamics 365 Guide. Tímto způsobem mohou získat vizuální pokyny na HoloLens.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Přihlášení k rozhraní pro provádění výrobního provozu jako pracovník

Než mohou pracovníci začít zařízení používat, musí jej připravit supervizor nebo technický personál a otevřít správnou stránku v Dynamics 365 Supply Chain Management. Další informace o nastavení zařízení najdete v části [Nastavení zařízení pro spuštění rozhraní pro provádění výrobního provozu](production-floor-execution-setup.md).

Po přípravě zařízení se na něm zobrazí přihlašovací stránka. Tato stránka zobrazuje informace o stavu úloh pro místní pracovní buňku. Tyto informace jsou pravidelně aktualizovány. Na tuto stránku se pracovníci přihlásí pomocí ID znaku. Ačkoli pracovníci nemusí mít uživatelský účet pro Supply Chain Management, musí mít účet *časově registrovaný pracovník*, který mohou použít při přihlášení.

![Přihlašovací stránka k rozhraní pro provádění výrobního provozu.](media/pfei-sign-in-page.png "Přihlašovací stránka k rozhraní pro provádění výrobního provozu")

Zbývající části tohoto článku popisují, jak pracovníci pracují s rozhraním.

## <a name="all-jobs-tab"></a>Karta Všechny úlohy

Karta **Všechny úlohy** obsahuje seznam úloh se všemi výrobními úlohy, které mají stav *Nezahájeno*, *Zastaveno* nebo *Zahájeno*. (Tento název karty je přizpůsobitelný a může se u vašeho systému lišit.)

![Karta Všechny úlohy.](media/pfei-all-jobs-tab.png "Karta Všechny úlohy")

Seznam úloh má následující sloupce. Čísla odpovídají číslům na předchozím obrázku.

1. **Sloupec výběru** – Sloupec zcela vlevo používá zatržítko k označení úloh, které vybral pracovník. Pracovníci mohou v seznamu vybrat více úloh najednou. Chcete-li vybrat všechny úlohy v seznamu, zaškrtněte políčko v záhlaví sloupce. Když je vybrána jedna úloha, podrobnosti o této úloze se zobrazí ve spodní části stránky.
1. **Sloupec Stav úlohy** – Tento sloupec používá symboly k označení stavu každé úlohy. Úlohy, které nemají v tomto sloupci žádný symbol, mají stav *Nezahájeno*. Zelený trojúhelník označuje úlohy, které mají stav *Zahájeno*. Dvě žluté svislé čáry označují úlohy, které mají stav *Zastaveno*.
1. **Sloupec s vysokou prioritou** – Tento sloupec používá vykřičníky k označení úloh, které mají vysokou prioritu.
1. **Objednávka** – Tento sloupec zobrazuje číslo výrobní zakázky pro úlohu.
1. **Popis** – Tento sloupec zobrazuje popis operace, jejíž je úloha součástí.
1. **Požadováno** – Tento sloupec zobrazuje množství, které má úloha vyrobit.
1. **Zahájeno** – Tento sloupec zobrazuje množství, které již bylo pro úlohu zahájeno.
1. **Dokončeno** – Tento sloupec zobrazuje množství, které již bylo pro úlohu dokončeno.
1. **Zlikvidováno** – Tento sloupec zobrazuje množství, které již bylo pro úlohu zlikvidováno.
1. **Zbývající** – Tento sloupec zobrazuje množství, které zbývá do dokončení úlohy.

## <a name="active-jobs-tab"></a>Karta Aktivní úlohy

Karty **Aktivní úlohy** zobrazují seznam všech úloh, které již přihlášený pracovník zahájil. (Tento název karty je přizpůsobitelný a může se u vašeho systému lišit.)

![Karta Aktivní úlohy.](media/pfei-active-jobs-tab.png "Karta Aktivní úlohy")

Seznam aktivních úloh má následující sloupce:

- **Sloupec výběru** – Sloupec zcela vlevo používá zatržítko k označení úloh, které vybral pracovník. Pracovníci mohou v seznamu vybrat více úloh najednou. Chcete-li vybrat všechny úlohy v seznamu, zaškrtněte políčko v záhlaví sloupce. Když je vybrána jedna úloha, podrobnosti o této úloze se zobrazí ve spodní části stránky.
- **Objednávka** – Tento sloupec zobrazuje číslo výrobní zakázky pro úlohu.
- **Popis** – Tento sloupec zobrazuje popis operace, jejíž je úloha součástí.
- **Požadováno** – Tento sloupec zobrazuje množství, které má úloha vyrobit.
- **Zahájeno** – Tento sloupec zobrazuje množství, které již bylo pro úlohu zahájeno.
- **Dokončeno** – Tento sloupec zobrazuje množství, které již bylo pro úlohu dokončeno.
- **Zlikvidováno** – Tento sloupec zobrazuje množství, které již bylo pro úlohu zlikvidováno.
- **Zbývající** – Tento sloupec zobrazuje množství, které zbývá do dokončení úlohy.

## <a name="my-jobs-tab"></a>Karta Moje úlohy

Karta **Moje úlohy** umožňuje pracovníkům snadno zobrazit všechny nezahájené a nedokončené úlohy, které jsou jim specificky přiřazeny. Je to užitečné ve společnostech, kde jsou úkoly někdy nebo vždy přiděleny konkrétním pracovníkům (lidské zdroje) namísto jiných typů zdrojů (jako jsou stroje).

Plánovací systém automaticky přiřadí každou produkční úlohu ke konkrétnímu záznamu prostředku a každý záznam prostředku má svůj typ (například stroj nebo člověk). Když nastavíte zaměstnance jako výrobního pracovníka, můžete účet pracovníka přidružit k jedinečnému záznamu lidských zdrojů.

Karta **Moje úlohy** obsahuje všechny nezahájené a nedokončené úlohy, které byly přiřazeny k záznamu lidských zdrojů přihlášeného pracovníka, pokud je nějaký pracovník přihlášen. Nikdy neuvádí úlohy, které byly přiřazeny k počítači nebo jinému typu zdroje, i když přihlášený pracovník na těchto úlohách začal pracovat.

Chcete-li zobrazit všechny úlohy, které byly spuštěny přihlášeným pracovníkem, bez ohledu na typ zdroje, ke kterému je každá úloha přiřazena, použijte kartu **Aktivní úlohy**. Chcete-li zobrazit všechny nedokončené úlohy, které odpovídají konfiguraci místního filtru úloh, bez ohledu na pracovníka nebo stav zahájení, použijte kartu **Všechny úlohy**.

![Karta Moje úlohy.](media/pfei-my-jobs-tab.png "Karta Moje úlohy")

## <a name="my-machine-tab"></a>Karta Můj stroj

Karta **Můj stroj** pracovníkům umožňuje vybrat majetek, který je připojen ke zdroji stroje v sadě filtrů na kartě **Všechny úlohy**. Pracovník pak může zobrazit stav vybraného majetku čtením hodnot až čtyř vybraných čítačů a seznamů posledních požadavků na údržbu a registrovaných prostojů. Pracovník může také požádat o údržbu vybraného majetku a zaregistrovat a upravit prostoje stroje. (Tento název karty je přizpůsobitelný a může se u vašeho systému lišit.)

![Karta Můj stroj.](media/pfei-my-machine-tab.png "Karta Můj stroj")

Karta **Můj stroj** má následující sloupce. Čísla odpovídají číslům na předchozím obrázku.

1. **Majetek stroje** - Vyberte zařízení stroje, které chcete sledovat. Začněte psát název a vyberte jej ze seznamu odpovídajícího majetku, nebo vyberte ikonu lupy a vyberte ze seznamu všech aktiv spojených se zdroji, které jsou ve filtru seznamu úloh.

    > [!NOTE]
    > Uživatelé Supply Chain Management mohou podle potřeby přiřadit zdroj ke každé stránce **Všechny majetky** (na kartě **Fixní majetek** pomocí rozevíracího seznamu **Zdroj**). Další informace naleznete v tématu [Vytvoření majetku](../asset-management/objects/create-an-object.md).

1. **Nastavení** - Vyberte ikonu ozubeného kola a otevřete dialogové okno, kde si můžete vybrat, která počítadla se mají zobrazit pro vybraný majetek stroje. Hodnoty těchto čítačů jsou zobrazeny v horní části karty **Správa majetku**. Nabídka **Nastavení** (zobrazená na následujícím snímku obrazovky) umožňuje povolit až čtyři čítače. U každého počítadla, které chcete povolit, použijte vyhledávací pole v horní části dlaždice a vyberte počítadlo. Vyhledávací pole obsahuje seznam všech čítačů přidružených k aktivu vybranému v horní části stránky **Správa majetku** . Nastavte každé počítadlo tak, aby sledovalo hodnotu **Agregované** nebo nejnovější **Aktuální** hodnotu čítače. Například pokud nastavíte čítač, který sleduje, kolik hodin stroj běžel, měli byste jej nastavit na **Agregované**. Pokud nastavíte počitadlo pro měření nejnovější aktualizované teploty nebo tlaku, měli byste jej nastavit na **Aktuální**. Volbou **OK** uložte svá nastavení a zavřete dialogové okno.

    ![Nastavení karty Můj stroj.](media/pfei-my-machine-tab-settings.png "Nastavení karty Můj stroj")

1. **požadavek na údržbu** - Výběrem tohoto tlačítka otevřete dialogové okno, kde můžete vytvořit požadavek na údržbu. Budete moci poskytnout popis a poznámku. Na požadavek bude upozorněn uživatel Supply Chain Management, který poté bude moci převést požadavek na údržbu na objednávku údržby.
1. **Registrovat prostoje** - Výběrem tohoto tlačítka otevřete dialogové okno, kde můžete zaregistrovat prostoje stroje. Budete moci vybrat kód důvodu a zadat časové rozpětí data a času prostoje. Registrace výpadku stroje se používá pro výpočet efektivity majetku stroje.
1. **Zobrazit nebo upravit** - Toto tlačítko vyberte, chcete-li otevřít dialogové okno, kde můžete upravit nebo zobrazit stávající záznamy o prostojích.

## <a name="starting-and-completing-production-jobs"></a>Zahájení a dokončení výrobních úloh

Pracovníci zahájí výrobní úlohu výběrem úlohy na kartě **Všechny úlohy** a poté výběrem možnosti **Zahájit úlohu** otevřou dialogové okno **Zahájení úlohy**.

![Dialogové okno Zahájení úlohy.](media/pfei-start-job-dialog.png "Dialogové okno Zahájení úlohy")

Pracovníci v dialogovém okně **Zahájení úlohy** potvrdí množství výroby a poté zahájí úlohu. Pracovníci mohou upravit množství výběrem pole **Množství** a poté pomocí zobrazené numerické klávesnice. Pracovníci pak volbou **Zahájit** začnou práci na úloze. Dialogové okno **Zahájení úlohy** se zavře a úloha se přidá na kartu **Aktivní úlohy**.

Pracovníci mohou zahájit úlohu v jakémkoli stavu. Když pracovník zahájí úlohu ve stavu *Nezahájeno*, pole **Množství** v dialogovém okně **Zahájení úlohy** zpočátku zobrazuje celé množství. Když pracovník zahájí úlohu ve stavu *Zahájeno* nebo *Zastaveno*, pole **Množství** zpočátku zobrazuje zbývající množství.

## <a name="reporting-good-quantities"></a>Hlášení množství zboží

Když pracovník dokončí nebo částečně dokončí úlohu, může vykázat množství zboží, které bylo vyprodukováno, výběrem úlohy na kartě **Aktivní úlohy** a poté volbou **Hlásit průběh**. Pak v dialogovém okně **Hlášení průběhu** pracovník zadá množství zboží pomocí numerické klávesnice. Ve výchozím nastavení je množství prázdné. Po zadání množství může pracovník aktualizovat stav úlohy na *Probíhá*, *Zastaveno* nebo *Dokončeno*.

![Dialogové okno Hlášení průběhu.](media/pfei-report-progress-dialog.png "Dialogové okno Hlášení průběhu")

## <a name="reporting-good-quantities-on-batch-orders-that-have-co-products-and-by-products"></a>Hlášení dobrých množství u dávkových objednávek, které mají koprodukty a vedlejší produkty

Pracovníci mohou používat rozhraní provádění produkčního podlaží k hlášení průběhu dávkových objednávek. Toto hlášení zahrnuje hlášení o koproduktech a vedlejších produktech.

Někteří výrobci, zejména ve zpracovatelském průmyslu, používají k řízení svých výrobních procesů dávkové objednávky. Dávkové příkazy se vytvářejí ze vzorců a tyto vzorce lze definovat tak, že mají jako výstup koprodukty a vedlejší produkty. Když je hlášena zpětná vazba o těchto dávkových objednávkách, musí být množství výstupu registrováno na položce receptury a také na koprodukty a vedlejší produkty.

Když pracovník dokončí nebo částečně dokončí úlohu na dávkové zakázce, může vykázat množství zboží nebo odpadu pro každý produkt, který je definován jako výstup pro objednávku. Produkty, které jsou definovány jako výstup pro dávkovou objednávku, mohou být typu *Vzorec*, *Koprodukt* nebo *Vedlejší produkt*.

Chce-li pracovník nahlásit dobré množství produktů, vybere úlohu na kartě **Aktivní úlohy** a poté vybere **Hlásit pokrok**.

Poté v dialogovém okně **Hlásit pokrok** si může pracovník vybrat mezi produkty, které jsou definovány jako výstup pro dávkovou objednávku, o kterých bude reportovat. Pracovník může vybrat jeden nebo více produktů v seznamu a poté vybrat **Hlásit pokrok**. U každého produktu je ve výchozím nastavení množství prázdné a pracovník může množství zadat pomocí numerické klávesnice. Pracovník může využít tlačítka **Předchozí** a **Další** pro pohyb mezi vybranými produkty. Po zadání množství pro každý produkt může pracovník aktualizovat stav úlohy na *Probíhá*, *Zastaveno* nebo *Dokončeno*.

![Hlášení koproduktů a vedlejších produktů.](media/report-co-by-products.png "Hlášení koproduktů a vedlejších produktů")

### <a name="reporting-on-batch-orders-for-planning-items"></a>Hlášení o dávkových objednávkách pro plánování položek

Když pracovník dokončí zakázku na dávkové zakázce pro položku plánování, vykáže množství pouze u koproduktů a vedlejších produktů, protože položky plánování neobsahují položku typ *Vzorec*.

### <a name="reporting-co-product-variation"></a>Hlášení variace koproduktu

Pokud je dávkový příkaz vytvořen z verze vzorce, kde je možnost **Variace koproduktů** je nastavena na *Ano*, pracovník může hlásit koprodukty, které nejsou součástí definice pro dávkové objednávky. Tato funkce se používá ve scénářích, kde může ve výrobním procesu dojít k neočekávanému výstupu produktu.

V tomto případě může pracovník specifikovat koprodukt a množství, které se má hlásit, výběrem **Variace koproduktů** v dialogovém okně hlášení pokroku. Pracovník si pak může vybrat ze všech uvolněných produktů, které jsou definovány jako koprodukty.

### <a name="reporting-catch-weight-items"></a>Vykazování položek se skutečnou hmotností

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Pracovníci mohou používat rozhraní provádění produkčního podlaží k hlášení průběhu dávkových objednávek, které jsou vytvořeny pro položky skutečné hmotnosti. Dávkové příkazy se vytvářejí ze vzorců, které lze definovat tak, aby měly položky skutečné hmotnosti jako položky vzorce, koprodukty a vedlejší produkty. Vzorec lze také definovat tak, aby obsahoval řádky vzorce pro přísady, které jsou definovány pro skutečnou hmotnost. Položky skutečné hmotnosti používají ke sledování inventáře dvě měrné jednotky: množství skutečné hmotnosti a množství inventáře. Například v potravinářském průmyslu lze maso v krabicích definovat jako položku skutečné hmotnosti, kde se množství skutečné hmotnosti používá ke sledování počtu krabic a množství v inventáři se používá ke sledování hmotnosti krabic.

## <a name="reporting-scrap"></a>Hlášení odpadu

Když pracovník dokončí nebo částečně dokončí úlohu, může vykázat odpadvýběrem úlohy na kartě **Aktivní úlohy** a poté volbou **Hlásit odpad**. Pak v dialogovém okně **Hlášení odpadu** pracovník zadá množství odpadu pomocí numerické klávesnice. Pracovník také vybere důvod (*Žádný*, *Stroj*, *Operátor* nebo *Materiál*).

![Dialogové okno Hlášení odpadu.](media/pfei-report-scrap-dialog.png "Dialogové okno Hlášení odpadu")

## <a name="adjust-material-consumption-and-make-material-reservations"></a>Úprava spotřeby materiálu a rezervace materiálů

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Pracovníci mohou upravit spotřebu materiálu pro každou výrobní úlohu. Tato funkce se používá ve scénářích, kde skutečné množství materiálů, které bylo spotřebováno výrobní úlohou, bylo větší nebo menší než plánované množství. Proto musí být upraveno tak, aby vyjadřovalo aktuální stav zásob.

Pracovníci mohou také provádět rezervace podle šarže a sériového čísla materiálů. Tato funkce se používá ve scénářích, kdy pracovník musí ručně určit, které šarže materiálu nebo sériová čísla byly spotřebovány, aby byly splněny požadavky na sledovatelnost materiálu.

Pracovníci mohou určit množství, které se má upravit, výběrem možnosti **Upravit materiál**. Tato tlačítko je dostupné v následujících místech:

- V dialogovém okně **Hlášení odpadu**
- V dialogovém okně **Hlášení průběhu**
- Na pravém panelu nástrojů

### <a name="adjust-material-consumption-from-the-report-scrap-and-report-progress-dialog-boxes"></a>Úprava spotřeby materiálu v dialogových oknech Hlášení odpadu a Hlášení průběhu

Poté, co pracovník zadá nahlašované množství v dialogovém okně **Hlášení odpadu** nebo **Hlášení průběhu**, zpřístupní se tlačítko **Upravit materiál**. Když uživatel vybere toto tlačítko, objeví se dialogové okno **Upravit materiál**. V tomto dialogovém okně jsou uvedeny položky naplánované ke spotřebě, když je pro úlohu nahlášeno množství dobrého nebo vyřazeného zboží.

Seznam v dialogovém okně obsahuje následující informace:

- **Číslo produktu** – Základní produkt a varianta produktu.
- **Název produktu** – Název produktu.
- **Návrh** – Odhadované množství materiálu, které bude spotřebováno při vykazování postupu nebo odpadu pro zadané množství u úlohy.
- **Spotřeba** – Skutečné množství materiálu, které bude spotřebováno při vykazování postupu nebo odpadu pro zadané množství u úlohy.
- **Rezervováno** – Množství materiálu, které bylo fyzicky rezervováno ve skladu.
- **Jednotka** – Jednotka kusovníku.

Pravá strana dialogu obsahuje následující informace:

- **Číslo produktu** – Základní produkt a varianta produktu.
- **Odhadováno** – Odhadované množství, které má být spotřebováno.
- **Zahájeno** – Množství, které bylo zahájeno v rámci výrobní úlohy.
- **Zbývající množství** – Ta část odhadovaného množství, která zbývá ke spotřebě.
- **Uvolněné množství** – Množství, které bylo spiotřebováno.

Provádět můžete následující akce:

- Pracovník může určit množství materiálu k úpravě výběrem možnosti **Upravit spotřebu**. Po potvrzení množství se množství ve sloupci **Spotřeba** aktualizuje o upravené množství.
- Když pracovník vybere příkaz **Upravit materiál**, je vytvořen deník výrobních výdejek. Tento deník obsahuje stejné položky a množství jako seznam **Upravit materiál**.
- Když pracovník upraví množství v dialogovém okně **Upravit materiál**, pole **Návrh** na odpovídajícím řádku deníku se aktualizuje stejným množstvím. Pokud pracovník vybere tlačítko **Storno** v dialogovém okně **Upravit materiál**, seznam výdejek se odstraní.
- Když pracovník vybere **OK**, seznam výdejek odstraněn není. Bude zaúčtován při nahlášení úlohy v dialogovém okně **Hlášení odpadu** nebo **Hlášení průběhu**.
- Pokud pracovník vybere tlačítko **Storno** v dialogovém okně **Hlášení odpadu** nebo **Hlášení průběhu**, seznam výdejek se odstraní.

### <a name="adjust-material-from-the-primary-or-secondary-toolbar"></a>Úprava materiálu z primárního nebo sekundárního panelu nástrojů

Tlačítko **Upravit materiál** lze nakonfigurovat tak, aby se zobrazovalo na primárním nebo sekundárním panelu nástrojů. (Další informace viz téma [Návrh rozhraní pro provádění výrobního provozu](production-floor-execution-tabs.md).) Pracovník může vybrat příkaz **Upravit materiál** pro probíhající výrobní úlohu. V tomto případě se zobrazí dialogové okno **Upravit materiál**, kde pracovník může provést požadované úpravy. Po otevření dialogového okna se pro výrobní úlohu vytvoří výrobní výdejka, která obsahuje řádky pro upravená množství. Když pracovník vybere příkaz **Zaúčtovat**, úprava je potvrzena a seznam k odběru je zaúčtován. Když pracovník vybere **Storno**, výdejka je odstraněna a není provedena žádná změna.

### <a name="adjust-material-consumption-for-catch-weight-items"></a>Úprava spotřebu materiálu pro položky skutečné hmotnosti

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

Pracovníci mohou upravit spotřebu materiálu pro položky skutečné hmotnosti. Tato funkce se používá ve scénářích, kde skutečné množství materiálu skutečné hmotnosti, které bylo spotřebováno výrobní úlohou, bylo větší nebo menší než plánované množství. Proto musí být upraveno tak, aby vyjadřovalo aktuální stav zásob. Když pracovník upraví spotřebu položky skutečné hmotnosti, může upravit množství skutečné hmotnosti i množství inventáře. Pokud je například plánována výrobní zakázka na spotřebu pěti krabic, které mají odhadovanou hmotnost 2 kilogramy na krabici, pracovník může upravit jak počet krabic ke spotřebě, tak hmotnost krabic. Systém ověří, že zadaná hmotnost krabic je v rámci definované minimální a maximální prahové hodnoty, která je definována na uvolněném produktu.

### <a name="reserve-materials"></a>Rezervace materiálů

V dialogu **Upravit materiál** může pracovník provádět a upravovat rezervace materiálů výběrem příkazu **Rezervovat materiál**. Dialogové okno **Rezervovat materiál**, které se objeví, ukazuje fyzicky dostupné zásoby položky pro každou skladovací a sledovací dimenzi.

Pokud je materiál možné používat v procesech řízení skladu (WMS), seznam zobrazuje pouze fyzicky dostupné zásoby pro umístění výrobního vstupu pro materiál. Umístění výrobního vstupu je definováno u zdroje, kde je plánována výrobní úloha. Pokud je číslo položky řízeno šarží nebo sériovým číslem, zobrazí se úplný seznam fyzicky dostupných čísel šarží a sériových čísel. Chce-li pracovník zadat množství k rezervaci, vybere příkaz **Rezervovat materiál**. Chce-li pracovník odstranit existující rezervaci, vybere příkaz **Odebrat rezervaci**.

Další informace o tom, jak nastavit umístění výrobního vstupu, najdete v následujícím příspěvku na blogu: [Nastavení umístění výrobního vstupu](/archive/blogs/axmfg/deliver-picked-materials-to-the-locations-where-the-materials-are-consumed-by-operations-in-production).

> [!NOTE]
> Rezervace, které pracovník provádí v dialogovém okně **Rezervovat materiál**, zůstanou zachovány, když pracovník vybere **Storno** v dialogu **Hlášení průběhu** nebo **Hlášení odpadu**.
>
> U položek se skutečnou hmotností není možné upravovat rezervace.

## <a name="completing-a-job-and-starting-a-new-job"></a>Dokončení a zahájení nové úlohy

Pracovníci obvykle dokončí úlohu výběrem jedné nebo více aktuálních úloh na kartě **Aktivní úlohy** a poté volbou **Hlásit průběh**. Poté zadají vyrobené množství (množství zboží) a nastaví stav na *Dokončeno*. Pokud byla vybrána více než jedna úloha, pracovník se mezi nimi pohybuje tlačítky **Předchozí** a **Další**. Chcete-li zahájit novou úlohu, pracovník ji vybere na kartě **Všechny úlohy** a poté vybere **Zahájit úlohu**.

Pracovník může také zahájit novou úlohu, zatímco jeho předchozí úloha je stále otevřená. Pracovník opět vybere novou úlohu na kartě **Všechny úlohy** a poté vybere **Zahájit úlohu**. V tomto případě však dialogové okno **Zahájení úlohy** informuje pracovníka, že aktuálně pracuje na úloze, a proto musí tuto úlohu před zahájením nové úlohy buď zastavit, nebo dokončit.

## <a name="working-on-multiple-jobs-in-parallel"></a>Práce na více úlohách současně

Jeden pracovník může pracovat na více úlohách současně (tj. paralelně). V tomto případě se kolekce úloh, na kterých pracovník pracuje, nazývá a *sada úloh*. Pracovník může do sady přidat nové úlohy nebo dokončit jednu nebo více úloh v sadě. Následující dva scénáře ukazují, jak může pracovník paralelně pracovat na úlohách.

### <a name="scenario-1-a-worker-who-has-no-active-jobs-wants-to-start-two-jobs-and-work-on-them-in-parallel"></a>Scénář 1: Pracovník, který nemá žádné aktivní úlohy, chce spustit dvě úlohy a pracovat na nich paralelně

Pracovník vybere dvě úlohy na kartě **Všechny úlohy** a poté vybere **Zahájit úlohu**. Dialogové okno **Zahájení úlohy** obsahuje obě vybrané úlohy a pracovník může pro spuštění každé úlohy upravit množství. Pracovník poté potvrdí dialogové okno a může spustit obě úlohy.

### <a name="scenario-2-a-worker-who-has-two-active-jobs-that-are-in-progress-wants-to-start-a-third-job-and-work-on-it-in-parallel-with-the-other-two"></a>Scénář 2: Pracovník se dvěma právě probíhajícími úlohami chce zahájit třetí úlohu a pracovat na ní paralelně s dalšími dvěma

Pracovník vybere třetí úlohu na kartě **Všechny úlohy** a poté vybere **Sada**. V dialogovém okně **Sada** může pracovník upravit množství, se kterým se má úloha zahájit. Pracovník poté potvrdí dialogové okno výběrem možnosti **Sada**.

## <a name="working-on-indirect-activities"></a>Práce na nepřímých aktivitách

Nepřímé aktivity přímo nesouvisejí s výrobní zakázkou. Nepřímé aktivity lze flexibilně definovat, jak je popsáno v části [Nastavení nepřímých aktivit pro čas a docházku](/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance).

Například Shannon, pracovnice ve společnosti Contoso, se chce zúčastnit schůzky společnosti a schůzky jsou považovány za nepřímou aktivitu. Platí jeden z následujících dvou scénářů:

- **Shannon pracuje na jedné nebo více aktivních úlohách.** Shannon vybere možnost **Aktivita**, vyhledá aktivitu (schůzku) a potvrdí její výběr. Zpráva, která se zobrazí, ji informuje, že má probíhající úlohy. Ve zprávě si Shannon může vybrat, zda dokončí nebo zastaví úlohy, na kterých pracuje, než půjde na schůzku.
- **Shannon nemá žádné aktivní úlohy.** Shannon vybere možnost **Aktivita**, vyhledá aktivitu (schůzku) a potvrdí její výběr. Nyní je registrována jako účastnice schůzky.

V obou scénářích poté, co Shannon potvrdí svůj výběr, přejde na přihlašovací stránku nebo na stránku, která na ni počká, aby potvrdila, že se vrátila ze své nepřímé aktivity. Stránka, která se zobrazí, závisí na konfiguraci rozhraní pro provádění výrobního provozu. (Další informace viz [Konfigurace rozhraní pro provádění výrobního provozu](production-floor-execution-configure.md).)

## <a name="registering-breaks"></a>Registrace přestávek

Pracovníci mohou registrovat přestávky. Přestávky lze flexibilně definovat, jak je popsáno v části [Plat na základě registrace](pay-based-on-registrations.md).

Pracovník zaregistruje přestávku výběrem **Přestávka** a poté vyberte kartu, která představuje typ přestávky (například oběd). Poté, co pracovník potvrdí výběr, zařízení zobrazí buď přihlašovací stránku, nebo stránku, která počká, až pracovník potvrdí, že se vrátil z přestávky. Stránka, která se zobrazí, závisí na konfiguraci rozhraní pro provádění výrobního provozu. (Další informace viz [Konfigurace rozhraní pro provádění výrobního provozu](production-floor-execution-configure.md).)

## <a name="view-the-my-day-dialog"></a>Zobrazení dialogového okna „Můj den“

Dialogové okno **Můj den** poskytuje pracovníkům přehled jejich registrací a zůstatků. Dialog je rozdělen do následujících tří částí:

- V hlavní části jsou uvedeny registrace, které aktuální pracovník provedl ke zvolenému datu. Otevře se s registracemi pro aktuální den a poskytuje výběr data, který umožňuje pracovníkovi zobrazit další dny.
- Sekce **Poslední vypočítaný denní zůstatek** zobrazuje aktuální zůstatky pracovníka za placený čas, placený přesčas, absenci a placenou absenci. Tyto hodnoty jsou založeny na registracích, které byly vypočteny během schvalovacího procesu.
- Sekce **Zůstatky** poskytuje přehled zůstatků za definované období u vybraných kategorií registrací (jako je dovolená, standardní čas a přesčas). Tyto zůstatky jsou založeny na způsobu, jakým jsou nastaveny statistické zůstatky v modulu **Čas a docházka**. Další informace o tomto nastavení najdete v části [Zobrazení zůstatků dovolené v rozhraní pro provádění výrobního provozu](production-floor-execution-payroll-stats.md).

Správci mohou přidat tuto funkci do rozhraní umístěním tlačítka **Můj den** na panel nástrojů pro každou relevantní kartu, jak je popsáno v části [Návrh rozhraní pro provádění výrobního provozu](production-floor-execution-tabs.md).

## <a name="working-in-teams"></a>Práce v týmech

Když je ke stejné výrobní úloze přiděleno více pracovníků, mohou vytvořit tým. Tým může nominovat jednoho pracovníka jako pilota. Zbývající pracovníci se pak automaticky stanou asistenty tohoto pilota. Pro výsledný tým musí stav úlohy zaregistrovat pouze pilot. Časové záznamy platí pro všechny členy týmu.

### <a name="prerequisites"></a>Předpoklady

Chcete-li používat týmy, musí správce povolit akci **Pomocník** pro primární panel nástrojů na kartě **Všechny úlohy** v rozhraní pro provádění výrobního provozu. Návod najdete v tématu [Návrh rozhraní pro provádění výrobního provozu](production-floor-execution-tabs.md).

### <a name="form-a-new-team-that-has-a-pilot-and-an-assistant"></a>Vytvoření nového týmu, který má vedoucího a pomocníka

Pracovník se může zaregistrovat jako pomocník výběrem možnosti **Pomocník** na kartě **Všechny úlohy**. Poté ve zobrazeném dialogovém okně **Vyberte zaměstnance, který má pomoci** může pracovník vybrat vedoucího týmu ze seznamu pracovníků, kteří aktivně pracují na úloze. Poté, co pracovník potvrdí svůj výběr, stane se pomocníkem vybraného pracovníka, který se stane vedoucím nového týmu.

### <a name="assign-a-new-pilot-to-an-existing-team"></a>Přiřazení nového vedoucího týmu do existujícího týmu

Když chce tým vybrat nového vedoucího, musí stávající vedoucí týmu nominovat jiného pracovníka v týmu jako nového vedoucího týmu. Pro nominaci nového vedoucího týmu vybere aktuální vedoucí možnost **Pomocník** na kartě **Všechny úlohy**. Poté ve zobrazeném dialogovém okně **Změnit vedoucího týmu** může vedoucí týmu vybrat nového vedoucího týmu ze seznamu pracovníků, kteří jsou již v týmu. Poté, co současný vedoucí týmu potvrdí svůj výběr, je z týmu úplně vyřazen. Může se však podle potřeby znovu připojit k týmu.

### <a name="assistant-clocks-out"></a>Odchod pomocníka

Když pracovník, který pracuje jako pomocník, odejde z práce, opustí tým. Pokud jsou možnosti **Trvalé týmy** a **Restartovat při registraci příchodu** nastaveny na *Ano*, pracovník, který odejde, se automaticky připojí k týmu při příštím příchodu. Tyto možnosti najdete na kartě **Obecné** na stránce **Parametry času a docházky**.

## <a name="opening-instructions"></a>Otevření pokynů

Pracovníci mohou otevřít dokument připojený k úloze výběrem volby **Pokyny**. Tlačítko **Pokyny** je k dispozici, pouze pokud je k úloze v hlavních datech přidružen dokument. Například dokument připojený k produktu na stránce **Uvolněné produkty** v Supply Chain Management bude pro pracovníky k dispozici k otevření v rozhraní pro provádění dílenského provozu.

## <a name="opening-mixed-reality-guides-for-hololens"></a>Otevření průvodců hybridní realitou pro HoloLens

[Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) může pracovníkům poskytnout praktickou výuku využívající hybridní realitu. Můžete definovat standardizované procesy, kde podrobné pokyny navedou zaměstnance na potřebné nástroje a součásti a ukážou jim, jak tyto nástroje používat v reálných pracovních situacích. Zde je přehled procesu.

1. Pokaždé, když pracovník otevře v rozhraní pro provádění dílenského provozu seznam úloh, rozhraní vyhledá všechny příslušné příručky pro zobrazené úlohy.
1. Pracovník vybere **Průvodci** pro zobrazení seznamu průvodců.
1. Pracovník vybere v seznamu příslušného průvodce.
1. Rozhraní pro provádění dílenského provozu zobrazí QR kód pro vybraného průvodce.
1. Pracovník si nasadí HoloLens a podívá se na QR kód pro spuštění průvodce.
1. Pracovník se s pomocí průvodce naučí danou úlohu.

Další informace, jak vytvořit, přiřadit a použít průvodce pro HoloLens viz [Poskytnutí průvodce hybridní reality pro pracovníky ve výrobě](instruction-guides-in-production-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
