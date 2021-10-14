---
title: Stáří vyskladnění zásob směrnice skladového místa
description: Toto téma vysvětluje, jak během vyskladňování používat strategie direktivy umisťování první do skladu, první ze skladu (FIFO) a poslední do skladu, první ze skladu (LIFO).
author: mirzaab
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSWorkTable,WHSWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 83f73052d1d9d8a29a80ce3cf1035a259cd92c17
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578577"
---
# <a name="location-directive-inventory-picking-aging"></a>Stáří vyskladnění zásob směrnice skladového místa

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak během vyskladňování používat strategie direktivy umisťování první do skladu, první ze skladu (FIFO) a poslední do skladu, první ze skladu (LIFO). Tyto strategie pracují ve spojení s daty sledování splatnosti, která jsou zaznamenávána pro místa, která mají být sledována při prvním vstupu zásob do skladu. Funkce *Stáří vyskladnění zásob směrnice skladového místa* používá k určení stárnutí datum na místě. Funkce *Stav skladového místa* aktualizuje datum na místě podle data z registrační značky.

Pomocí strategií FIFO a LIFO můžete dodávat jak dávkově sledované položky, tak položky bez dávkového sledování, na základě data, kdy byl inventář zadán do skladu. Tato schopnost může být užitečná zejména u zásob bez dávkového sledování, kde není k dispozici datum vypršení platnosti pro třídění.

Při prvním přijetí nebo vytvoření inventáře ve skladu systém aktualizuje příslušnou poznávací značku tak, aby se aktuální datum zobrazilo jako datum stárnutí. Toto datum je pak používáno strategiemi lokalizační směrnice k identifikaci nejstaršího nebo nejnovějšího inventáře ve skladu. Pokud je inventář přesunut na místo, které není sledováno poznávací značkou, samotné umístění je aktualizováno informacemi o stárnutí a tyto informace pak budou použity strategiemi.

## <a name="turn-on-the-feature"></a>Zapnutí funkce

Chcete-li tuto funkci zpřístupnit, zapněte následující funkce ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) v tomto pořadí:

1. Stav umístění ve skladu
1. Stáří vyskladnění zásob směrnice skladového místa

## <a name="feature-requirements"></a>Požadavky funkcí

Chcete-li použít tuto funkci, musíte nastavit možnost **Povolit stav místa** na *Ano* pro každý [profil místa](tasks/create-location-profile.md), který se používá k ukládání zásob. Chcete-li nastavit tuto možnost pro profil místa, přejděte na **Správa skladu \> Nastavení \> Sklad \> Profily míst** a vyberte profil místa. Tuto možnost najdete na pevné záložce **Všeobecné**.

## <a name="feature-scenarios"></a>Scénáře funkcí

Tato část obsahuje příklady, které ukazují, jak nastavit a používat strategie FIFO a LIFO.

> [!TIP]
> Tato část obsahuje dva scénáře, jeden pro FIFO a jeden pro LIFO. Postupy, které jsou k dispozici, předpokládají, že provedete oba scénáře, v pořadí. Doporučujeme provést oba scénáře, abyste mohli zažít rozdíly mezi těmito dvěma strategiemi.

### <a name="make-sample-data-available"></a>Příprava ukázkových dat

Chcete-li s těmito scénáři pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.

Tyto scénáře můžete také použít jako vodítko pro použití této funkce v produkčním systému. V takovém případě však musíte každé vlastní nastavení, které je zde popsáno, nahradit vlastními hodnotami.

### <a name="set-up-the-scenarios"></a><a name="demo-set-up"></a>Nastavení scénářů

Ukázková data vyžadují nastavení a inventarizaci, aby podpořila scénáře. Podle těchto kroků vytvořte data zásob, která jsou požadována pro práci ve scénářích FIFO a LIFO.

1. Přihlaste se do systému, ve kterém jsou nainstalována ukázková data, a vyberte právnickou osobu **USMF**.
1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Profily skladových míst**.
1. V podokně akcí vyberte **Upravit**.
1. V seznamu profilů polohy vyberte možnost **FLOOR-05**.
1. Na pevné záložce **Obecné** nastavte možnost **Povolit stav místa** na *Ano*.
1. Zvolte **Uložit**.
1. Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.
1. V seznamu směrnic skladového místa vyberte možnost **63 SO výdejová kontejnerizace**.
1. Vyberte možnost **Upravit**, tím přepnete stránku do režimu úprav.
1. Na pevné záložce **Akce směrnice místa** najděte řádek, kde je pole **Pořadové číslo** nastaveno na *1* a postupujte jedním z těchto kroků:

    - Pokud nastavujete scénář FIFO, změňte hodnotu pole **Strategie** na *Stárnutí místa FIFO*.
    - Pokud nastavujete scénář LIFO, změňte hodnotu pole **Strategie** na *Stárnutí místa LIFO*.

1. Na záložce s náhledem **Akce směrnic skladového místa** vyberte možnost **Upravit dotaz**.
1. V dialogovém okně dotazu na kartě **Oblast** přidejte tlačítkem **Přidat** nový řádek a pak nastavrte následující hodnoty.

    - **Tabulka:** *umístění*
    - **Odvozená tabulka:** *Skladová místa*
    - **Pole:** *ID zóny*
    - **Kritéria:** *Podlaha*

1. Vyberte **OK**, pokud chcete použít své nastavení a zavřete dialogové okno dotazu.
1. Změny směrnice skladového místa uložíte výběrem možnosti **Uložit**.
1. Na mobilním zařízení nebo v aplikaci *Dynamics 365 for Finance and Operations - Warehousing* na vašem PC, proveďte následující kroky k odstranění existujícího inventáře z umístění skladu a podpořte scénáře:

    1. Přihlaste se ke skladu *63* pomocí příslušného ID uživatele a hesla.
    1. V hlavní nabídce vyberte **Kvalita**.
    1. V nabídce **Řízení kvality** vyberte **Odpad**.
    1. Na stránce **Odpad** vyberte pole **LOC/LP** a zadejte *63\_1*.
    1. Vyberte **Enter** nebo **OK**.
    1. Potvrďte podrobnosti **Odpad** pro **Úprava ven** výběrem **Enter** nebo **OK**.

    Když je inventář registrační značky upraven, zobrazí se zpráva „Práce dokončena“.

    Tyto kroky ponechají zásoby na dvou místech v demonstračních datech. Každé místo má jiné datum stárnutí. Umístění *FL-001* má datum stárnutí 15. dubna 2017 a místo *FL-002* má datum stárnutí 29. ledna 2017. Obě umístění obsahují položku *A0001*.

    Chcete-li zobrazit tato data, přejděte na **Řízení zásob \> Dotazy a sestavy \> Seznam na skladě** a poté filtrujte ve skladu *63* a položku *A0001*. V řádcích, kde je pole **Místo** nastaveno na *FL-001* nebo *FL-002*, vyberte řádek, který má kladnou hodnotu **Fyzické zásoby** a poté v podokně akcí vyberte **Transakce**. Pole **Fyzické datum** zobrazí datum, které odpovídá jednomu z výše uvedených dat stárnutí.

### <a name="scenario-1-set-up-and-use-fifo-location-aging"></a><a name="fifo-demo"></a>Scénář 1: Nastavení a použití stárnutí místa FIFO

Strategie FIFO najde místo, které obsahuje nejstarší datum stárnutí, a přidělí výdej podle tohoto data stárnutí.

1. Pokud jste tak ještě neučinili, [připravte vzorová data](#demo-set-up), která se vyžadují pro tento scénář.
1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Zvolte **Nové**.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - Na záložce s náhledem **Odběratel** zadejte do pole **Účet odběratele** hodnotu *US-001*.
    - Na záložce s náhledem **Obecné** zadejte do pole **Sklad** hodnotu *63*.

1. Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.
1. Otevře se nová prodejní objednávka. Obsahují nový prázdný řádek v mřížce na záložce s náhledem **Řádky prodejní objednávky**. Na tomto řádku objednávky nastavte v poli **Číslo položky** hodnotu *A0001* a v poli **Množství** hodnotu *1*.
1. V nabídce **Zásoby** nad mřížkou vyberte možnost **Rezervace**.
1. Na stránce **Rezervace** v podokně Akce klikněte na **Rezervovat šarži**. Ve vybraném skladu se provede rezervace objednaného množství této položky v zásobách.
1. Zavřete stránku **Rezervace**.
1. Na stránce **Prodejní objednávka** v pododokně akcí na kartě **Sklad** ve skupině **Akce** vyberte **Uvolnit do skladu**. Zobrazí se informační zprávy. Systém vytvoří dodávku, přidá ji k novému nákladu a vytvoří požadovanou práci.
1. Na pevné záložce **Řádky prodejní objednávky** v nabídce **Sklad** vyberte **Podrobnosti o práci**, chcete-li otevřít práci, která byla vytvořena pro tuto prodejní objednávku. Všimněte si, že řádek, kde je hodnota **Typ práce** *Výdej*, ukazuje hodnotu **Skadové místo** *FL-002*. Toto místo obsahuje registrační značku, která má nejstarší datum stárnutí (FIFO).
1. Vyberte **Sklad \> Podrobnosti o zásilce**.
1. Na záložce **Obecné** si poznamenejte si ID vlny, abyste jej mohli použít ve scénáři 2.

### <a name="scenario-2-set-up-and-use-lifo-location-aging"></a>Scénář 2: Nastavení a použití stárnutí místa LIFO

Strategie LIFO najde místo, které obsahuje nejnovéjší datum stárnutí, a přidělí výdej podle tohoto data stárnutí. Ve scénáři 2 upravíte nastavení scénáře 1 (FIFO) a znovu použijete prodejní objednávku a vlnu, které byly vytvořeny během tohoto scénáře.

1. Před zahájením tohoto scénáře nastavte a dokončete celý scénář FIFO, jak je popsáno v [předchozí sekci](#fifo-demo). V tomto scénáři znovu použijete vlnu a většinu nastavení, které byly pro tento scénář vytvořeny.
1. Upravte směrnici místa **63 Výdej - kontejnerizace** tak, aby používala strategii *Místo stárnutí LIFO*, jak je popsáno v první části postupu [Nastavte scénáře](#demo-set-up).

    Dále upravíte vlnu, která byla vytvořena pro prodejní objednávku ve scénáři 1, aby používala strategii *Místo stárnutí LIFO*.

1. Přejděte na **Řízení skladu \> Výstupní vlny \> Vlny dodávek \> Všechny vlny**.
1. Vyberte a otevřete vlnu obsahující objednávku, kterou jste vytvořili pro scénář FIFO.
1. V podokně akcí na kartě **Práce** vyberte **Storno**, cchete-li zrušit práci, kterou jste vytvořili pro scénář FIFO.
1. V podokně akcí na kartě **Vlna** ve skupině **Vlna** zvolte **Zpracovat**.
1. Po dokončení zpracování v podokně akcí na kartě **Vlna** ve skupině **Související informace** vyberte **Práce** a otevřete práci, která byla vytvořena pro tuto vlnu.
1. Na stránce **Práce**, na kartě **Přehled**, by měly být dva řádky. Vyberte řádek, kde je pole **Stav práce** nastaveno hodnotu *Otevřená*.
1. Všimněte si, že řádek, kde je hodnota **Typ práce** *Výdej*, ukazuje hodnotu **Skadové místo** *FL-001*. Toto místo obsahuje registrační značku, která má nejnovější datum stárnutí (LIFO).

V těchto scénářích jste viděli, jak strategie stárnutí místa směřuje práci k místu zísob, které má nejstarší nebo nejnovější zásoby, v závislosti na vybrané strategii.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]