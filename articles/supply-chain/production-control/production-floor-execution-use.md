---
title: Jak pracovníci používají rozhraní pro provádění výrobního provozu
description: Tohle téma popisuje, jak používat rozhraní pro provádění výrobního provozu z pohledu pracovníka.
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 40c6794fdf25da44a75aba4a502a89966c0ec4d0
ms.sourcegitcommit: 9dd2d38e76d4d93171315ec319e6ce7d51d4e6c7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/15/2020
ms.locfileid: "4012458"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>Jak pracovníci používají rozhraní pro provádění výrobního provozu

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Rozhraní pro provádění výrobního provozu je optimalizováno pro dotykovou interakci. Jeho provedení poskytuje vizuální kontrast, který splňuje požadavky na přístupnost pro prostředí dílny. Nabízí všechny funkce jako zařízení úkolového lístku. Umožňuje však také paralelní spuštění více úloh ze seznamu úloh. (Tato funkce je také známá jako *sdružování úloh*.) Navíc ze seznamu úloh mohou pracovníci otevřít průvodce, který byl vytvořen v Microsoft Dynamics 365 Guide. Tímto způsobem mohou získat vizuální pokyny na HoloLens.

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>Přihlášení k rozhraní pro provádění výrobního provozu jako pracovník

Než mohou pracovníci začít zařízení používat, musí jej připravit supervizor nebo technický personál a otevřít správnou stránku v Dynamics 365 Supply Chain Management. Další informace o nastavení zařízení najdete v části [Nastavení zařízení pro spuštění rozhraní pro provádění výrobního provozu](production-floor-execution-setup.md).

Po přípravě zařízení se na něm zobrazí přihlašovací stránka. Tato stránka zobrazuje informace o stavu úloh pro místní pracovní buňku. Tyto informace jsou pravidelně aktualizovány. Na tuto stránku se pracovníci přihlásí pomocí ID znaku. Ačkoli pracovníci nemusí mít uživatelský účet pro Supply Chain Management, musí mít účet *časově registrovaný pracovník* , který mohou použít při přihlášení.

![Přihlašovací stránka k rozhraní pro provádění výrobního provozu](media/pfei-sign-in-page.png "Přihlašovací stránka k rozhraní pro provádění výrobního provozu")

Zbývající části tohoto tématu popisují, jak pracovníci pracují s rozhraním.

## <a name="all-jobs-tab"></a>Karta Všechny úlohy

Karta **Všechny úlohy** obsahuje seznam úloh se všemi výrobními úlohy, které mají stav *Nezahájeno* , *Zastaveno* nebo *Zahájeno*.

![Karta Všechny úlohy](media/pfei-all-jobs-tab.png "Karta Všechny úlohy")

Seznam úloh má následující sloupce. (Čísla odpovídají číslům na předchozím obrázku.)

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

![Karta Aktivní úlohy](media/pfei-active-jobs-tab.png "Karta Aktivní úlohy")

Seznam úloh na kartě **Aktivní úlohy** má následující sloupce:

- **Sloupec výběru** – Sloupec zcela vlevo používá zatržítko k označení úloh, které vybral pracovník. Pracovníci mohou v seznamu vybrat více úloh najednou. Chcete-li vybrat všechny úlohy v seznamu, zaškrtněte políčko v záhlaví sloupce. Když je vybrána jedna úloha, podrobnosti o této úloze se zobrazí ve spodní části stránky.
- **Objednávka** – Tento sloupec zobrazuje číslo výrobní zakázky pro úlohu.
- **Popis** – Tento sloupec zobrazuje popis operace, jejíž je úloha součástí.
- **Požadováno** – Tento sloupec zobrazuje množství, které má úloha vyrobit.
- **Zahájeno** – Tento sloupec zobrazuje množství, které již bylo pro úlohu zahájeno.
- **Dokončeno** – Tento sloupec zobrazuje množství, které již bylo pro úlohu dokončeno.
- **Zlikvidováno** – Tento sloupec zobrazuje množství, které již bylo pro úlohu zlikvidováno.
- **Zbývající** – Tento sloupec zobrazuje množství, které zbývá do dokončení úlohy.

## <a name="starting-and-completing-production-jobs"></a>Zahájení a dokončení výrobních úloh

Pracovníci zahájí výrobní úlohu výběrem úlohy na kartě **Všechny úlohy** a poté výběrem možnosti **Zahájit úlohu** otevřou dialogové okno **Zahájení úlohy**.

![Dialogové okno Zahájení úlohy](media/pfei-start-job-dialog.png "Dialogové okno Zahájení úlohy")

Pracovníci v dialogovém okně **Zahájení úlohy** potvrdí množství výroby a poté zahájí úlohu. Pracovníci mohou upravit množství výběrem pole **Množství** a poté pomocí zobrazené numerické klávesnice. Pracovníci pak volbou **Zahájit** začnou práci na úloze. Dialogové okno **Zahájení úlohy** se zavře a úloha se přidá na kartu **Aktivní úlohy**.

Pracovníci mohou zahájit úlohu v jakémkoli stavu. Když pracovník zahájí úlohu ve stavu *Nezahájeno* , pole **Množství** v dialogovém okně **Zahájení úlohy** zpočátku zobrazuje celé množství. Když pracovník zahájí úlohu ve stavu *Zahájeno* nebo *Zastaveno* , pole **Množství** zpočátku zobrazuje zbývající množství.

## <a name="reporting-good-quantities"></a>Hlášení množství zboží

Když pracovník dokončí nebo částečně dokončí úlohu, může vykázat množství zboží, které bylo vyprodukováno, výběrem úlohy na kartě **Aktivní úlohy** a poté volbou **Hlásit průběh**. Pak v dialogovém okně **Hlášení průběhu** pracovník zadá množství zboží pomocí numerické klávesnice. Ve výchozím nastavení je množství prázdné. Po zadání množství může pracovník aktualizovat stav úlohy na *Probíhá* , *Zastaveno* nebo *Dokončeno*.

![Dialogové okno Hlášení průběhu](media/pfei-report-progress-dialog.png "Dialogové okno Hlášení průběhu")

## <a name="reporting-scrap"></a>Hlášení odpadu

Když pracovník dokončí nebo částečně dokončí úlohu, může vykázat odpadvýběrem úlohy na kartě **Aktivní úlohy** a poté volbou **Hlásit odpad**. Pak v dialogovém okně **Hlášení odpadu** pracovník zadá množství odpadu pomocí numerické klávesnice. Pracovník také vybere důvod ( *Žádný* , *Stroj* , *Operátor* nebo *Materiál* ).

![Dialogové okno Hlášení odpadu](media/pfei-report-scrap-dialog.png "Dialogové okno Hlášení odpadu")

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

Nepřímé aktivity přímo nesouvisejí s výrobní zakázkou. Nepřímé aktivity lze flexibilně definovat, jak je popsáno v části [Nastavení nepřímých aktivit pro čas a docházku](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance).

Například Shannon, pracovnice ve společnosti Contoso, se chce zúčastnit schůzky společnosti a schůzky jsou považovány za nepřímou aktivitu. Platí jeden z následujících dvou scénářů:

- **Shannon pracuje na jedné nebo více aktivních úlohách.** Shannon vybere možnost **Aktivita** , vyhledá aktivitu (schůzku) a potvrdí její výběr. Zpráva, která se zobrazí, ji informuje, že má probíhající úlohy. Ve zprávě si Shannon může vybrat, zda dokončí nebo zastaví úlohy, na kterých pracuje, než půjde na schůzku.
- **Shannon nemá žádné aktivní úlohy.** Shannon vybere možnost **Aktivita** , vyhledá aktivitu (schůzku) a potvrdí její výběr. Nyní je registrována jako účastnice schůzky.

V obou scénářích poté, co Shannon potvrdí svůj výběr, přejde na přihlašovací stránku nebo na stránku, která na ni počká, aby potvrdila, že se vrátila ze své nepřímé aktivity. Stránka, která se zobrazí, závisí na konfiguraci rozhraní pro provádění výrobního provozu. (Další informace viz [Konfigurace rozhraní pro provádění výrobního provozu](production-floor-execution-configure.md).)

## <a name="working-on-breaks"></a>Práce na přestávkách

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
