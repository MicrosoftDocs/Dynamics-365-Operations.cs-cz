---
title: Stav umístění ve skladu
description: Toto téma uvádí přehled funkce stavu skladového místa.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 31216c24f54f22ec928eb143d4a913aabcd50cf8
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424194"
---
# <a name="warehouse-location-status"></a>Stav umístění ve skladu

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management obsahuje několik polí skladových míst, jež vám při práci se skladovými a při jejich údržbě nabízejí určitou pružnost. Chcete-li mít lepší kontrolu nad toky ve skladu, můžete do dotazu na směrnici skladového místa zahrnout i stavy skladových míst.

Následující čtyři pole na stránce **Skladová místa** sledují údaje o aktuálním stavu skladového místa. Tato pole umožňují manažerům skladu mít přehled o stavu skladových míst. Umožňují také pokročilé vykazování a filtrování.

- **Číslo položky** – položka, která je aktuálně na skladovém místě. Pokud skladové místo obsahuje více položek, je toto pole prázdné.
- **Datum a čas poslední aktivity** – časové razítko poslední skladové transakce provedené v daném skladovém místě.
- **Datum pro sledování stárnutí** – datum, kdy byly zásoby ve skladovém místě přivezeny do skladu. Tato hodnota se vypočítává na základě data stárnutí registrační značky. Je přesná pro skladová místa, pro něž se využívá měření podle registračních značek, ale nemusí být přesná v případě skladových míst, jež takto sledována nejsou.
- **Stav skladového místa** – stav skladového místa. Možné hodnoty jsou čtyři.

    - **Neurčeno** – profil skladového místa stav nesleduje. Aktuální stav proto není známý.
    - **Prázdné** – ve skladovém místě nejsou v současné době žádné zásoby.
    - **Výdej** – ve skladovém místě byly od doby, kdy bylo naposledy prázdné, provedeny odchozí transakce.
    - **Skladování** – ve skladovém místě byly od doby, kdy bylo naposledy prázdné, prováděny pouze příchozí transakce.

## <a name="turn-on-the-warehouse-location-status-feature"></a>Zapnutí funkce Stav skladového místa

Než můžete použít funkci *Stav skladového místa*, musíte ji v systému zapnout. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Stav skladového místa*

## <a name="set-up-warehouse-location-status"></a>Nastavení stavu skladového místa

### <a name="prepare-the-sample-data-that-is-required-for-the-example-scenario"></a>Připravte ukázková data, jež potřebujete pro příkladový scénář

Než začnete pracovat na scénáři, musíte ukázková data aktivovat a nastavit funkci tak, jak se popisuje v této části. K provedení příkladového scénáře musíte použít skladovou aplikaci nebo emulátor aplikace běžící v prohlížeči. Zde uvedené kroky počítají s použitím skladové aplikace. Kroky v případě emulátoru aplikace běžícího v prohlížeči jsou však podobné.

#### <a name="use-the-usmf-legal-entity"></a>Použijte právnickou osobu USMF

Chcete-li s příkladovým scénářem pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.

#### <a name="set-up-location-profiles"></a>Nastavit profily skladových míst

Příklad scénáře vyžaduje přípravu dvou profilů skladových míst.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Profily skladových míst**.
1. Vyberte možnost **Upravit**, tím přepnete stránku do režimu úprav.
1. Vyberte profil **HROMADNÝ-06**.
1. Na záložce s náhledem **Obecné** nastavte následující hodnoty:

    - **Povolit položku na skladovém místě:** Nastavte u této volby hodnotu _Ano_.
    - **Povolit datum a čas aktivity skladového místa:** Nastavte u této volby hodnotu _Ano_.
    - **Povolit stav skladového místa:** Nastavte u této volby hodnotu _Ano_.

    Tyto volby určují, zda jsou ve skladovém místě aktivní referenční pole.

1. Kroky 3 až 4 zopakujte i pro profil **VÝDEJ-06**.

> [!NOTE]
> Když jsou parametry profilu skladového místa (**Povolit položku na skladovém místě**, **Povolit aktivitu skladového místa**, **Povolit stav skladového místa**) nastaveny na *Ano*, systém okamžitě aktualizuje příslušná skladová místa spuštěním úlohy *Kontrola konzistence stavu umístění skladu*.

### <a name="scenario"></a>Scénář

1. Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. Zvolte **Nové**.
1. V dialogovém okně **Vytvoření nákupní objednávky** vyberte na záložce s náhledem **Dodavatel** v poli **Účet dodavatele** hodnotu *104*.
1. Na pevné záložce **Obecné** v poli **Sklad** vyberte *61*.
1. Vyberte **OK**.
1. Otevře se nová nákupní objednávka (PO). Zahrnuje prázdný řádek v mřížce **Řádky nákupní objednávky**. Na tomto řádku nastavte následující hodnoty:

    - **Číslo položky:** _A0002_
    - **Množství:** _5_

1. V podokně Akce na kartě **Nákup** ve skupině **Akce** klikněte na tlačítko **Potvrdit**. Nákupní objednávka se potvrdí.
1. Na mobilním zařízení přejděte na **Vstupní \> Příjem nákupu**.
1. Vyberte pole **ČÍSLOPO** a zadejte číslo PO a potvrďte.
1. Vyberte pole **POLOŽKA**, zadejte jako číslo položky hodnotu *A0002* a potvrďte.
1. Na stránce **MNOŽ.** zadejte jako množství hodnotu *5* a potvrďte.

    Množství můžete měřit některým z následujících způsobů:

    - Tlačítkem se znaménkem plus (**+**) nebo mínus (**–**) můžete číselnou hodnotu přičíst nebo odečíst.
    - Výběrem prázdného pole mezi znaménkem plus (**+**) a znaménkem mínus (**–**) otevřete numerickou klávesnici.

1. Potvrďte výběr čísla položky *A0002* a množství *5*. Ve spodní části stránky se zobrazí zpráva „Práce dokončena“.
1. V pravém horním rohu klikněte na tlačítko Nabídka (někdy se označuje jako „hamburgerové tlačítko“ nebo „hamburger“) a poté vyberte **Storno**, chcete-li stránku **Příjem nákupu** opustit a vrátit se do nabídky **Vstupní**.
1. Na stránce nákupní objednávky vyberte položku **Podrobnosti práce** nad mřížkou **Řádky nákupní objednávky**.
1. Na kartě **Všeobecné** si všimněte hodnot ve vytvořených polích **ID práce** a **ID cílové registrační značky**.
1. V sekci **Řádky** si všimněte hodnot **Skladové místo** pro typy práce *Výdej* a *Zaskladnění*.
1. Na mobilním zařízení přejděte na **Vstupní \> Vyskladnění nákupu**.
1. Vyberte pole **ID**, zadejte ID práce a potvrďte.
1. Potvrďte ještě jednou, dokončí se zadávání *Výdeje*.
1. Klikněte na tlačítko nabídky v pravém horním rohu a poté dokončete práci *Výdeje* kliknutím na tlačítko **Hotovo**.
1. Poznamenejte si vyskladňovací skladové místo a potvrďte. Ve spodní části stránky se zobrazí zpráva „Práce dokončena“.
1. Stiskněte v pravém horním rohu tlačítko nabídky, poté vyberte **Storno**, chcete-li opustit **Vyskladnění nákupu** a vrátit se do nabídky **Vstupní**.
1. Chcete-li se vrátit do hlavní nabídky, vyberte **Zpět**.
1. V systému Dynamics 365 Supply Chain Management přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Skladová místa**.
1. Filtrujte podle **Skladového místa**, zadejte místo vyskladnění z práce nákupní objednávky. Měly by se vám zobrazit následující výsledky:

    - Sloupec **Stav skladového místa** zobrazuje hodnotu *Skladování*, protože poslední transakce na tomto skladovém místě byla zaskladnění.
    - Sloupec **Číslo položky** zobrazuje hodnotu *A0002*, protože tato položka byla přijata a zaskladněna na dané skladové místo.
    - Sloupec **Datum a čas poslední aktivity** ukazuje časové razítko (datum a čas) dokončení poslední práce na skladovém místě.

1. Na mobilním zařízení přejděte na **Kvalita \> Pohyb**.
1. Vyberte pole **LOC/LP** a zadejte skladové místo, jež jste si poznamenali v předchozích krocích.
1. Potvrďte informace, které se zobrazí. Poznamenejte si vygenerované číslo registrační značky.
1. Na obrazovce **K informacím** vyberte pole **LOC/LP** a zadejte jako skladové místo, do něhož chcete položku přesunout, *06A07R2S1B*.
1. Na obrazovce **K informacím** potvrďte hodnotu **LP** (ID cílové registrační značky), je se generuje automaticky. Ve spodní části stránky se zobrazí zpráva „Práce dokončena“.
1. Stiskněte v pravém horním rohu tlačítko nabídky, poté vyberte **Storno**, chcete-li opustit **Pohyb** a vrátit se do nabídky **Správa kvality**.
1. Chcete-li se vrátit do hlavní nabídky, vyberte **Zpět**.
1. V systému Dynamics 365 Supply Chain Management přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Skladová místa**.
1. Obnovte stránku **Skladová místa** a znovu si prohlédněte původní místo vyskladnění. Všimněte si, že pole **Stav skladového místa** má nyní hodnotu *Prázdné* a sloupec **Číslo položky** je prázdný.
1. Zobrazte záznam pro skladové místo *06A07R2S1B* a všimněte si, že jeho hodnota **Stav** se změnila na *Skladování* a byla aktualizována i pole **Číslo položky** a **Datum a čas poslední aktivity**.
1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Zvolte **Nové**.
1. V dialogovém okně **Vytvořit prodejní objednávku** vyberte v poli **Účet odběratele** hodnotu *US-002*.
1. V poli **Sklad** zvolte *61*.
1. Vyberte **OK**.
1. Otevře se nová prodejní objednávka. Zahrnuje prázdný řádek v mřížce **Řádky prodejní objednávky**. Na tomto řádku nastavte následující hodnoty:

    - **Číslo položky:** _A0002_
    - **Množství:** _1_

1. Na záložce s náhledem **Řádky prodejních objednávek** v nabídce **Zásoby** vyberte možnost **Rezervace**.
1. Na stránce **Rezervace** vyberte **Rezervovat šarži**, pokud chcete rezervovat řádek objednávky. Zavřete stránku kliknutím na tlačítko **Zavřít** (**X**) v pravém horním rohu.
1. V podokně akcí na kartě **Sklad** ve skupině **Akce** vyberte možnost **Uvolnit do skladu.**
1. V sekci **Řádky prodejní objednávky** zvolte nabídku **Sklad** a v ní vyberte **Podrobnosti práce**.
1. Zkopírujte vytvořenou hodnotu **ID práce**.
1. Na mobilním zařízení přejděte na **Výstupní \> Prodejní výdej**.
1. Vyberte pole **ID**, zadejte ID práce, jež jste předtím zkopírovali, a potvrďte.
1. Na stránce **Prodejní objednávky: výdej** najdete v poli **LOC** jako výdejní skladové místo předtím vytvořené místo vyskladnění. Poznamenejte si toto místo.
1. Vyberte pole **LOC**, zadejte skladové místo a potvrďte.
1. Vyberte pole **LP**, zadejte číslo registrační značky, jež jste si poznamenali během aktivity pohybu, a potvrďte.
1. Vyberte pole **Položka**, zadejte jako číslo položky hodnotu *A0002* a potvrďte.
1. Na stránce **MNOŽ.** zadejte jako množství hodnotu *1* a potvrďte.

    Množství můžete měřit některým z následujících způsobů:

    - Tlačítkem se znaménkem plus (**+**) nebo mínus (**–**) můžete číselnou hodnotu přičíst nebo odečíst.
    - Výběrem prázdného pole mezi znaménkem plus (**+**) a znaménkem mínus (**–**) otevřete numerickou klávesnici.

1. Vyberte pole **CÍLOVÁ LP**, zadejte uživatelsky definované ID cílové registrační značky a potvrďte.
1. Potvrďte ještě jednou, práce výdeje se dokončí. Ve spodní části stránky se zobrazí zpráva „Práce dokončena“.
1. Stiskněte v pravém horním rohu tlačítko nabídky, poté vyberte **Storno**, chcete-li dokončit aktivitu výdeje a vrátit se do nabídky **Výstupní**.
1. V systému Dynamics 365 Supply Chain Management přejděte do nabídky **Řízení skladu \> Nastavení \> Sklad \> Skladová místa**.
1. Filtrujte podle **Skladového místa**, zadejte místo výdeje z práce prodejní objednávky.
1. Všimněte si, že v poli **Stav skladového místa**, z něhož byl prováděn výdej prodejní objednávky, je nyní hodnota *Výdej* a že bylo též aktualizováno pole **Datum a čas poslední aktivity**.

> [!NOTE]
> Pole skladového místa se aktualizují pouze skladovými transakcemi. Pokud provedete přesun zásob pomocí deníku nebo procesů jiných než skladových, aktualizace těchto polí se neprovede.
