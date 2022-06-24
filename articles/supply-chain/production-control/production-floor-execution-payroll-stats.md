---
title: Zobrazení zůstatku dovolené v rozhraní pro provádění výrobního provozu
description: Tento článek poskytuje příklad scénáře, který ukazuje, jak nastavit aplikaci Microsoft Dynamics 365 Supply Chain Management tak, aby na základě statistiky mezd poskytovala pracovníkům přehled o zůstatcích dovolené za aktuální rok.
author: johanhoffmann
ms.date: 04/22/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-04-22
ms.dyn365.ops.version: 10.0.XX
ms.openlocfilehash: 2a6b6f52bfa7539b7c9bb5841536b0d564d0274c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852266"
---
# <a name="show-vacation-balances-in-the-production-floor-execution-interface"></a>Zobrazení zůstatku dovolené v rozhraní pro provádění výrobního provozu

[!include [banner](../includes/banner.md)]

Tento článek poskytuje příklad scénáře, který ukazuje, jak nastavit aplikaci Microsoft Dynamics 365 Supply Chain Management tak, aby na základě statistiky mezd poskytovala všem pracovníkům přehled o zůstatcích dovolené za aktuální rok. Zaměstnanci budou moci vidět zůstatek své dovolené v dialogovém okně **Můj den** v rozhraní pro provádění výrobního provozu.

Tento scénář používá dánský zákon o prázdninách, kde rok dovolené trvá od 1. září do 31. srpna. V tomto scénáři vaše společnost najala nového pracovníka. kterému poskytne zůstatek 10 dnů dovolené po zbytek aktuálního roku dovolené.

## <a name="turn-on-the-required-features"></a>Zapnutí požadovaných funkcí

Chcete-li spustit tento scénář, musíte povolit funkci *Zobrazení Můj den pro rozhraní pro provádění výrobního provozu* v sekci [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Informace, jak povolit tuto a další funkce pro rozhraní pro provádění výrobního provozu, naleznete v části [Konfigurace rozhraní pro provádění výrobního provozu](production-floor-execution-configure.md).

## <a name="make-sample-data-available"></a>Příprava ukázkových dat

Chcete-li s tímto scénářem pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.

## <a name="create-a-new-pay-type"></a>Vytvoření nového typu mzdy

Začněte vytvořením nového *typu mzdy*, který bude sledovat získané dny dovolené pracovníků (také označované jako *zůstatek dovolené*). Typy mzdy se obvykle používají k výpočtu platů pracovníků. Typ mzdy, který zde vytvoříte, se však použije k výpočtu zůstatku.

1. Jděte na **Čas a docházka \> Nastavení \> Mzda \> Typy mezd**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.
1. Na novém řádku nastavte následující hodnoty:

    - **Typ mzdy:** *5151-1*
    - **Popis:** *Počítadlo dnů dovolené pracovníka*
    - **Zahrnout do exportu:** *Ne*

## <a name="update-the-pay-agreement"></a>Aktualizace platební smlouvy

V této sekci upravíte existující *platební smlouvu* přidáním nového typu mzdy a nastavením pravidel, která definují, jak se upraví zůstatek dovolené každého pracovníka při registraci dnů dovolené.

1. Jděte na **Čas a docházka \> Nastavení \> Mzda \> Platební smlouvy**.
1. Vyberte platební smlouvu, ve které chcete nastavit zásady dovolené. (Pokud pracujete se standardními vzorovými daty USMF, existuje pouze jedna platební smlouva *Man*.)
1. Ujistěte se, že vybraná platební smlouva je platná pro aktuální datum. Pokud pracujete se standardními vzorovými daty USMF, pole **Do data** platební smlouvy *Man* může být nastaveno na datum, které je v minulosti. Podle potřeby změňte hodnotu tak, aby to bylo za rok nebo dva v budoucnu.
1. V podokně akcí klikněte na možnost **Řádky smlouvy**.
1. Na stránce **Řádky platební smlouvy** na záložce s náhledem **Přehled** nastavte následující hodnoty na panelu nástrojů:

    - V prvním rozevíracím seznamu vyberte **Pondělí**.
    - V druhém rozevíracím seznamu vyberte **Absence**.

1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.
1. Na novém řádku nastavte pole **Typ mzdy** na typ mzdy, který jste pro tento scénář vytvořili (*5151-1*). Nastavení všech ostatních polí nechte na výchozích hodnotách.
1. Zatímco je stále vybrán nový řádek, na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Kód absencí:** *Dovolená*
    - **Použít pevné množství:** *Ano*
    - **Konstanta:** *-1*

1. V podokně akcí zvolte **Kopírovat den**.
1. V dialogovém okně **Kopírovat den** nastavte následující hodnoty:

    - **Úterý**, **Středa**, **Čtvrtek** a **Pátek:** *Ano*
    - **Přepsat:** *Ano*
    - **Absence:** *Ano*

1. Vyberte **OK**.

## <a name="create-a-payroll-statistic-group"></a>Vytvoření skupiny statistiky mezd

*Skupiny statistiky mezd* se používají k nastavení statistik registrací pracovníků za určité období. V tomto scénáři použijete skupinu statistik mezd k výpočtu počtu dnů dovolené, které pracovníci získají na období dovolené. V Dánsku trvá období dovolené od 1. září do 31. srpna.

1. Jděte na **Čas a docházka \> Nastavení \> Mzda \> Skupiny statistiky mezd**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.
1. Na novém řádku nastavte následující hodnoty:

    - **Skupina statistiky mezd:** *VAC*
    - **Popis:** *Zůstatek dovolené*
    - **Převod:** *Ne*

1. Zatímco je stále vybrán nový řádek, v podokně akcí vyberte možnost **Nastavení**.
1. Na stránce **Nastavení** v podokně Akce přidejte výběrem položky **Nový** řádek do mřížky.
1. V novém řádku nastavte pole **Typ mzdy** na *5151-1*.
1. Vyberte a podržte (nebo klikněte pravým tlačítkem) v poli **Kód období** a poté vyberte **Zobrazit podrobnosti**. Nyní můžete nastavit kód období, který později přiřadíte tomuto poli.
1. Na stránce **Typy období** v podokně akcí vyberte **Nový**, čímž přidáte řádek do mřížky.
1. Na novém řádku nastavte následující hodnoty:

    - **Typy období:** *VacYear*
    - **Popis:** *Rok dovolené*
    - **Frekvence:** *Let*

1. Zatímco je stále vybrán nový řádek, v podokně akcí vyberte možnost **Generovat období**.
1. V dialogovém okně **Generovat období** nastavte následující hodnoty:

    - **Zadejte počáteční datum období:** *1. září 2021*
    - **Délka období:** *5*

1. Vyberte **OK**.
1. Zavřete stránku **Typy období** pro návrat na stránku **Skupiny statistiky mezd**.
1. Nastav pole **Kód období** na typ období, který jste právě vytvořili (*VacYear*).

## <a name="create-a-statistical-balance-setup"></a>Vytvoření nastavení statistického zůstatku

V této sekci vytvoříte *nastavení statistického zůstatku*, které je propojeno se skupinou statistiky mezd, kterou jste vytvořili v předchozí části. Později toto nastavení statistického zůstatku propojíte se zobrazením **Můj den** v rozhraní pro provádění výrobního provozu. Zobrazení **Můj den** pak bude moci zobrazit zůstatky dovolené pro typ mzdy, který je přiřazen k přidružené skupině statistiky mezd.

1. Jděte na **Čas a docházka \> Nastavení \> Mzda \> Nastavení statistického zůstatku**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.
1. Na novém řádku nastavte následující hodnoty:

    - **Skupina statistiky mezd:** *VAC*
    - **Externí název:** *Zůstatek dovolené*
    - **Flexibilita:** *Ne*

## <a name="create-a-manual-premium"></a>Vytvoření ručních prémií

*Ruční prémie* se obvykle používají k poskytování příplatků za práci navíc. V tomto scénáři vytvoříte ruční prémii, kterou můžete použít k nastavení počátečního zůstatku dovolené pro každého pracovníka.

1. Jděte na **Čas a docházka \> Nastavení \> Mzda \> Ruční prémie**.
1. V podokně Akce vyberte možnost **Nový** a přidejte záznam.
1. V novém záznamu nastavte následující hodnoty:

    - **Prémie:** *VAC*
    - **Popis:** *Úpravy zůstatku dovolené pracovníků*
    - **Typ mzdy:** *5151-1*

## <a name="set-a-workers-initial-vacation-balance-and-adjust-it-by-one-day"></a>Nastavení počátečního zůstatku dovolené pracovníka a jeho úprava o jeden den

Správci mezd používají stránku **Schválení** pro kontrolu a schválení denních registrací pracovníků. V tomto scénáři převezmete roli správce, abyste mohli nastavit počáteční zůstatek dovolené pracovníka a zaregistrovat dny dovolené, které si pracovník vezme.

1. Jděte na **Čas a docházka \> Zkontrolovat a schválit \> Schválit**.
1. V dialogovém okně **Schválení** nastavte následující pole:

    - **Skupina schválení** – Vyberte skupinu schválení, do které patříte. (Pokud pracujete se standardními vzorovými daty USMF, existuje pouze jedna skupina schválení *AdmMan*.)
    - **Zobrazit celou skupinu, 1 den** – Vyberte tuto možnost a poté nastavte pole na aktuální datum.

1. Vyberte **OK**.
1. Stránka **Schválení** zobrazuje seznam záznamů, které odpovídají vašim kritériím. Vyberte pracovníka, kterého chcete schválit. Pokud pracujete se standardními vzorovými daty USMF, vyberte pracovníka *000496* (*Christina Portra*).
1. Udělte vybranému pracovníkovi 10 dní dovolené:

    1. Zatímco je pracovník stále vybrán, v podokně akcí vyberte možnost **Řádky prémií**.
    1. Na stránce **Řádky prémií** v podokně akcí vyberte možnost **Nový**, čímž přidáte řádek do mřížky.
    1. Na novém řádku nastavte následující hodnoty:

        - **Prémie:** *VAC*
        - **Množství:** *10*

    1. Zavřete stránku **Řádky prémií**.

1. Na stránce **Schválení** si všimněte, že pracovník využil jeden ze svých dnů dovolené k aktuálním datu:

    1. Zatímco je pracovník stále vybrán, ve spodní části stránky na panelu nástrojů na kartě **Přehled** vyberte možnost **Nový**, čímž přidáte řádek do mřížky.
    1. Na novém řádku nastavte následující hodnoty:

        - **Typ registrace deníku:** *Absence*
        - **Reference:** *Dovolená*

    1. V horní části stránky na panelu nástrojů vyberte **Převést**, čímž použijete zůstatek dovolené a vypočítáte odpočet.

## <a name="configure-the-production-floor-execution-interface-so-that-it-includes-the-my-day-dialog-box"></a>Konfigurace rozhraní pro provádění výrobního provozu, aby obsahovalo dialogové okno Můj den

V této sekci přidáte tlačítko **Můj den** do rozhraní pro provádění výrobního provozu. Pracovníci pak mohou toto tlačítko použít k otevření dialogového okna **Můj den**.

1. Přejděte do nabídky **Řízení výroby \> Nastavení \> Provádění výroby \> Konfigurace provádění výrobního provozu**.
1. Výběr konfigurace, například *Výchozí*.
1. V podokně akcí zvolte **Návrh karet**.
1. Na stránce **Návrh karet** v podokně seznamu vyberte *Všechny úlohy* pro zobrazení nastavení dané karty. Pole **Hlavní zobrazení** by nyní mělo obsahovat hodnotu *Všechny úlohy*.
1. V podokně akcí vyberte **Upravit**.
1. Na záložce s náhledem **Sekundární panel nástrojů** ve sloupci **Dostupné akce** vyberte **Můj den**. Poté jej výběrem pravé šipky přesuňte do sloupce **Vybrané akce**.

## <a name="check-your-balance-in-the-production-floor-execution-interface"></a>V rozhraní pro provádění výrobního provozu zkontrolujte zůstatek

V této sekci se přihlásíte do rozhraní pro provádění výrobního provozu jako pracovník, jehož dovolenou jste nastavili dříve. Poté otevřete dialogové okno **Můj den**, ve kterém uvidíte zůstatek dovolené.

1. Přejděte do nabídky **Řízení výroby \> Nastavení \> Provádění výroby \> Provádění výrobního provozu**.
1. Pokud budete vyzváni k výběru konfigurace, vyberte konfiguraci, kterou jste nastavili dříve v tomto scénáři (*Výchozí*).
1. Přihlaste se jako uživatel, kterého jste v tomto scénáři dříve nastavili. Pokud pracujete se standardními vzorovými daty USMF, měli byste být schopni se přihlásit zadáním *123* v poli **ID odznaku**. Toto ID odznaku odpovídá Christině Portra.
1. V levém panelu nástrojů vyberte **Můj den**.
1. V dialogovém okně se zaměřte na sekci **Zůstatky**. Tato sekce by nyní měla ukazovat, že máte zůstatek devíti dnů dovolené.
