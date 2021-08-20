---
title: Jak pracovníci používají rozhraní pro provádění výrobního provozu
description: Tohle téma popisuje, jak používat rozhraní pro provádění výrobního provozu z pohledu pracovníka.
author: johanhoffmann
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: c2215ae4162616fec892a8bce6cff5d5f68e5aa1457b41d86bb540bdcff87197
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747858"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Jak pracovníci používají rozhraní pro provádění výrobního provozu

[!include [banner](../includes/banner.md)]

Rozhraní pro provádění výrobního provozu je optimalizováno pro dotykovou interakci. Jeho provedení poskytuje vizuální kontrast, který splňuje požadavky na přístupnost pro prostředí dílny. Nabízí všechny funkce jako zařízení úkolového lístku. Umožňuje však také paralelní spuštění více úloh ze seznamu úloh. (Tato funkce je také známá jako *sdružování úloh*.) Navíc ze seznamu úloh mohou pracovníci otevřít průvodce, který byl vytvořen v Microsoft Dynamics 365 Guide. Tímto způsobem mohou získat vizuální pokyny na HoloLens.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Přihlášení k rozhraní pro provádění výrobního provozu jako pracovník

Než mohou pracovníci začít zařízení používat, musí jej připravit supervizor nebo technický personál a otevřít správnou stránku v Dynamics 365 Supply Chain Management. Další informace o nastavení zařízení najdete v části [Nastavení zařízení pro spuštění rozhraní pro provádění výrobního provozu](production-floor-execution-setup.md).

Po přípravě zařízení se na něm zobrazí přihlašovací stránka. Tato stránka zobrazuje informace o stavu úloh pro místní pracovní buňku. Tyto informace jsou pravidelně aktualizovány. Na tuto stránku se pracovníci přihlásí pomocí ID znaku. Ačkoli pracovníci nemusí mít uživatelský účet pro Supply Chain Management, musí mít účet *časově registrovaný pracovník*, který mohou použít při přihlášení.

![Přihlašovací stránka k rozhraní pro provádění výrobního provozu.](media/pfei-sign-in-page.png "Přihlašovací stránka k rozhraní pro provádění výrobního provozu")

Zbývající části tohoto tématu popisují, jak pracovníci pracují s rozhraním.

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

## <a name="reporting-scrap"></a>Hlášení odpadu

Když pracovník dokončí nebo částečně dokončí úlohu, může vykázat odpadvýběrem úlohy na kartě **Aktivní úlohy** a poté volbou **Hlásit odpad**. Pak v dialogovém okně **Hlášení odpadu** pracovník zadá množství odpadu pomocí numerické klávesnice. Pracovník také vybere důvod (*Žádný*, *Stroj*, *Operátor* nebo *Materiál*).

![Dialogové okno Hlášení odpadu.](media/pfei-report-scrap-dialog.png "Dialogové okno Hlášení odpadu")

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