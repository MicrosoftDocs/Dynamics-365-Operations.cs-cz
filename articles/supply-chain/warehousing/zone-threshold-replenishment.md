---
title: Doplnění prahu zóny
description: Doplňování na základě zón používá strategii minimálního/maximálního (min./max.) doplňování, ale místo pouze jednotlivých skladových míst vyhodnocuje celé skladové zóny. Skladoví manažeři mohou díky tomu rychleji zjistit, když je třeba do zóny vychystávání dodat další zásoby.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6f4ddd03ec16ac43b007b904eb688563735e0941
ms.sourcegitcommit: d9bffbeae2ba14f06294dd275383077d4d65c4fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/01/2020
ms.locfileid: "4654165"
---
# <a name="zone-threshold-replenishment"></a>Doplnění prahu zóny

[!include [banner](../includes/banner.md)]

Doplňování na základě zón používá strategii minimálního/maximálního (min./max.) [doplňování](replenishment.md), ale místo pouze jednotlivých skladových míst vyhodnocuje celé skladové zóny. Skladoví manažeři mohou díky tomu rychleji zjistit, když je třeba do zóny vychystávání dodat další zásoby.

Nastavení se u této funkce podobá nastavení pro doplňování podle skladového místa. Když však nastavíte šablonu pro min./max. doplňování, můžete také určit, zda má být příslušná mezní hodnota vyhodnocována podle skladového místa nebo zóny. Pokud nastavíte vyhodnocování podle zón, musíte do dotazu pro výběr zóny přidat konkrétní zóny.

Podobně jako u min./max. doplňování na základě skladového místa je min./max. doplňování na základě zón založeno na nastavení mezní hodnoty minimálních zásob, jež spouští vytvoření úlohy doplnění vybraných položek. Tato doplňovací úloha zvýší zásoby až do maximální mezní hodnoty stanovené pro zónu.

> [!NOTE]
> V aktuální vydané verzi nejsou podporovány procesy doplňování podle zón pro varianty produktů.


Na rozdíl od min./max. doplňování založeného na skladovém místě nevyžaduje min./max. doplňování založené na zónách, aby se u pevných skladových míst vyhodnocovalo, zda lze daná skladová místa využít k uskladnění konkrétní položky. Proto umožňuje doplňování podle zón použít min./max. doplňování, i když nemáte pevná skladová místa pro každou položku nebo variantu položky ve skladu. Když množství v zóně klesne pod stanovenou mezní hodnotu, vytvoří se doplňovací úloha. Směrnice skladových míst určují, na která konkrétní skladová místa mají být zásoby umístěny.

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a>Zapnutí funkce Zónové doplňování podle mezních hodnot

Než můžete použít funkci *Zónové doplňování podle mezních hodnot*, musíte ji v systému zapnout. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Zónové doplňování podle mezních hodnot*

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a>Nastavení zónového doplňování

Chcete-li nastavit doplňování podle zón, musíte v systému nakonfigurovat několik částí. Tato část představuje různá nastavení a uvádí ukázkové datové hodnoty, které můžete zadat, pokud chcete využít scénář na konci tohoto tématu.

### <a name="set-up-directive-codes"></a>Nastavení kódů předpisů

[Kódy předpisů](control-warehouse-location-directives.md) vám umožňují být konkrétnější při definování šablony skladového místa, jež se používá v šabloně práce. Každý kód vytváří společnou hodnotu, na kterou lze při konfiguraci šablony každého typu odkázat.

#### <a name="view-and-edit-directive-codes"></a>Zobrazení a úpravy kódů předpisů

Chcete-li zobrazit nebo upravit kódy předpisů, přejděte do **Řízení skladu \> Nastavení \> Kódy předpisů**.

#### <a name="prepare-demo-data-directive-codes"></a>Příprava ukázkových dat kódů předpisů

Tento příklad ukazuje, jak připravit kódy předpisů. Pokud plánujete využít scénář uvedený na konci tohoto tématu, použijte zde uvedené hodnoty ukázkových dat. Pokud ne, použijte vlastní hodnoty.

1. Pro práci s ukázkovými daty vyberte právnickou osobu **USMF**.
1. Přejděte na **Řízení skladu \> Nastavení \> Kódy předpisů**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.
1. Na novém řádku nastavte následující hodnoty:

    - **Kód předpisu:** _Zone replen_
    - **Popis předpisu:**_Doplňování podle zóny_

1. Kliknutím na tlačítko **Uložit** uložte nový kód.

### <a name="set-up-replenishment-templates"></a>Nastavit šablony doplnění

[Šablony doplnění metodou min/max.](tasks/set-up-min-max-replenishment-process.md) jsou primární mechanismus pro udržování optimálních úrovní zásob na výdejních skladových místech. V těchto šablonách musíte nastavit pravidla, která budou použita k doplňování skladových zásob. Tyto šablony lze mimo jiné použít i pro doplňování podle zón.

#### <a name="view-and-edit-replenishment-templates"></a>Zobrazení a úprava šablon doplňování

Šablona doplnění je sada pravidel, která určuje, kdy a jak je skladové místo doplňováno. Vyberete šablonu, která určuje, kdy a jak má být doplňování prováděno. Chcete-li zobrazit nebo upravit šablony doplňování, přejděte na **Řízení skladu \> Nastavení \> Doplnění \> Šablony doplnění**.

#### <a name="prepare-a-demo-data-replenishment-template"></a>Příprava ukázkových dat pro šablonu doplnění

Tento příklad ukazuje, jak připravit šablonu doplnění. Pokud plánujete využít scénář uvedený na konci tohoto tématu, použijte zde uvedené hodnoty ukázkových dat. Pokud ne, použijte vlastní hodnoty.

1. Pro práci s ukázkovými daty vyberte právnickou osobu **USMF**.
1. Přejděte na **Řízení skladu \> Nastavení \> Doplnění \> Šablony doplnění**.
1. Vyberte možnost **Upravit**, tím přepnete stránku do režimu úprav.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky **Přehled**.
1. Na novém řádku nastavte následující hodnoty. Potvrďte výchozí hodnoty pro všechna ostatní pole.

    - **Šablona doplnění:** _Zone min/max replen_
    - **Popis:** _Doplňování metodou min./max. podle zón_
    - **Typ doplňování:** _Minimum nebo maximum_

1. Zvolte **Uložit**.
1. Zatímco je nový řádek stále vybrán v mřížce **Přehled**, stiskněte tlačítko **Nový** nad mřížkou **Podrobnosti šablony doplnění**. Tím přidáte řádek, který bude přiřazen k právě vytvořené šabloně doplnění *Zone Min/Max replen*.
1. Na novém řádku nastavte následující hodnoty:

    - **Pořadové číslo:** Zadejte _1_.
    - **Popis:** Zadejte _Doplnění ve výdejové zóně_.
    - **Jednotka doplnění:** Vyberte _ks_.
    - **Typ požadavku:** Toto pole ponechte prázdné.
    - **Kód předpisu:** toto pole spojuje šablonu doplnění se směrnicí skladového místa. Vyberte předtím vybraný kód předpisu z ukázkových dat (_Zone replen_).
    - **Šablona práce:** Toto pole ponechte prázdné.
    - **Minimální množství:** Toto pole určuje množství, při kterém bude aktivováno doplnění. Zadejte _50_.
    - **Maximální množství:** Toto pole nastavuje maximální množství položky, jež se může v zóně nacházet. Vygenerované práce doplnění zvýší zásoby na toto množství. Zadejte _150_.
    - **Jednotka:** Toto pole určuje jednotku pro hodnoty minimálního a maximálního množství. Vyberte _ks_.
    - **Přírůstek poptávky:** Vyberte možnost _Zaokrouhlit nahoru_.
    - **Doplnit prázdná pevná skladová místa:** Zaškrtněte toto políčko.
    - **Doplnit pouze pevná skladová místa** Zrušte zaškrtnutí tohoto políčka.
    - **Režim dotazu na produkt:** Vyberte _Dotaz na produkt_.
    - **Obor mezní hodnoty doplnění:** Toto pole určuje, zda má šablona provádět vyhodnocování podle zóny nebo podle konkrétního skladového místa. Vyberte _Zóna_.
    - **Sklad:** Vyberte _61_.

1. Klikněte na **Vybrat produkty** nad mřížkou **Podrobnosti šablony doplnění**.
1. V dialogovém okně **Dotaz na produkt** klikněte na kartu **Oblast** a tlačítkem **Přidat** přidejte řádek mřížky.
1. Na novém řádku nastavte následující hodnoty:

    - **Tabulka:** _Položky_
    - **Odvozená tabulka:** _Položky_
    - **Pole:** _Číslo položky_
    - **Kritéria:** _A0001_

1. Vyberte **OK**, uložte svůj dotaz a zavřete dialogové okno.
1. Klikněte na **Vybrat zóny pro doplnění** nad mřížkou **Podrobnosti šablony doplnění**.
1. V dialogovém okně **Dotaz na zónu** na kartě **Oblast** přidejte řádek mřížky.
1. Na novém řádku nastavte následující hodnoty:

    - **Tabulka:** _Skladová zóna_
    - **Odvozená tabulka:** _Skladová zóna_
    - **Pole:** _ID zóny_
    - **Kritéria:** _PODLAHA_

1. Vyberte **OK**, uložte svůj dotaz a zavřete dialogové okno.

### <a name="set-up-location-directives"></a>Nastavit směrnice skladových míst

Na rozdíl od doplňování na základě minimálního/maximálního množství platí, že doplňování na bázi zón vyžaduje nastavení směrnice výdejového skladového místa i směrnice zaskladňovacího skladového místa, protože systém vyhodnocuje celou zónu a nikoli pouze výdejové skladové místo pro výstupní práci.

#### <a name="view-and-edit-location-directives"></a>Zobrazení a úpravy směrnic skladových míst

Chcete-li zobrazit nebo upravit směrnice skladových míst, přejděte do **Řízení skladu \> Nastavení \> Směrnice skladových míst**.

Příklady zobrazující, jak použít nastavení k vytvoření požadovaných směrnic výdejových a zaskladňovacích skladových míst, naleznete v další části.

#### <a name="prepare-demo-data-location-directives"></a>Příprava ukázkových dat směrnic skladových míst

Chcete-li připravit ukázková data, aby se dala použít ve scénáři uvedeném na konci tohoto tématu, musíte vytvořit dvě směrnice skladových míst: jednu pro výdej a druhou pro zaskladňování.

##### <a name="create-a-replenishment-pick-directive"></a>Vytvoření směrnice skladového místa pro výdej

1. Pro práci s ukázkovými daty vyberte právnickou osobu **USMF**.
1. Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.
1. V levém podokně nastavte v poli **Typ pracovního příkazu** hodnotu _Doplnění_.
1. V podokně Akce vyberte možnost **Nová**, vytvoří se nová směrnice.
1. Nastavte následující hodnoty:

    - **Pořadové číslo:** Přijměte výchozí hodnotu.
    - **Název:** Zadejte _Zone pick_.
    - **Typ práce:** Vyberte _Výdej_.
    - **Lokalita:** Vyberte _6_.
    - **Sklad:** Vyberte _61_.
    - **Kód směrnice:** Toto pole nechte prázdné.
    - **Více SKU:** U této možnosti nastavte hodnotu _Ne_.

1. Vyberte **Uložit**. Vytvoří se směrnice obsahující vámi dosud nakonfigurované nastavení.
1. Na záložce s náhledem **Řádky** přidejte řádek do mřížky výběrem možnosti **Nový**.
1. Na novém řádku nastavte následující hodnoty:

    - **Pořadové číslo:** Zadejte _1_.
    - **Od množství:** Zadejte _0_.
    - **Do množství:** Zadejte _10000000_.
    - **Jednotka:** Pole ponechejte prázdné.
    - **Vyhledat množství:** Vyberte _Žádné_.
    - **Omezit podle jednotky:** Zrušte zaškrtnutí tohoto políčka.
    - **Zaokrouhlení na jednotku:** Zrušte zaškrtnutí tohoto políčka.
    - **Vyhledat množství balení:** Zrušte zaškrtnutí tohoto políčka.
    - **Povolit rozdělení:** Zaškrtněte toto políčko.

1. Kliknutím na tlačítko **Uložit** uložte nový řádek.
1. Zatímco je nový řádek stále ještě vybrán v mřížce **Řádky**, vyberte možnost **Nový** na záložce s náhledem **Akce směrnice skladového místa**. Přidáte tak nový řádek do mřížky.
1. Na novém řádku nastavte následující hodnoty:

    - **Pořadové číslo:** Zadejte _1_.
    - **Název:** Zadejte _Pick from bulk_.
    - **Využití pevného skladového místa:** Vyberte _Pevná a nepevná skladová místa_.
    - **Povolit záporný stav zásob:** Zrušte zaškrtnutí tohoto políčka.
    - **Dávka povolena:** Zrušte zaškrtnutí tohoto políčka.
    - **Strategie:** Vyberte _Žádná_.

1. Kliknutím na tlačítko **Uložit** uložte novou akci.
1. Dokud je nová akce stále ještě vybrána, klikněte na **Upravit dotaz** nad mřížkou **Akce směrnice skladového místa**.
1. Zobrazí se dialogové okno dotazu. Zde můžete vybrat skladová místa, z nichž se má provést doplnění. Na kartě **Oblast** přidejte řádek do mřížky výběrem možnosti **Přidat**.
1. Na novém řádku nastavte následující hodnoty:

    - **Tabulka:** _umístění_
    - **Odvozená tabulka:** _Skladová místa_
    - **Pole:** _ID zóny_
    - **Kritéria:** _BULK_

1. Vyberte **OK**, uložte svůj dotaz a zavřete dialogové okno.
1. Směrnici skladového místa uložíte výběrem možnosti **Uložit**.

##### <a name="create-a-replenishment-put-directive"></a>Vytvoření směrnice skladového místa pro zaskladnění

1. Na stránce **Směrnice skladového místa** zkontrolujte v levém podokně, že je v poli **Typ pracovního příkazu** sále ještě zadána hodnota _Doplnění_.
1. V podokně Akce vyberte možnost **Nová**, vytvoří se další nová směrnice.
1. Nastavte následující hodnoty:

    - **Pořadové číslo:** Přijměte výchozí hodnotu.
    - **Název:** Zadejte _Zone put_.
    - **Typ pracovního příkazu:** Vyberte _Zaskladnění_.
    - **Lokalita:** Vyberte _6_.
    - **Sklad:** Vyberte _61_.
    - **Kód předpis:** Vyberte _Zone replen_. Tím směrnici skladového místa propojíte se šablonou doplnění, kterou jste vytvořili dříve pomocí předtím vytvořeného kódu.
    - **Více SKU:** U této možnosti nastavte hodnotu _Ne_.

1. Vyberte **Uložit**. Vytvoří se směrnice obsahující vámi dosud nakonfigurované nastavení.
1. Na záložce s náhledem **Řádky** přidejte řádek do mřížky výběrem možnosti **Nový**.
1. Na novém řádku nastavte následující hodnoty:

    - **Pořadové číslo:** Zadejte _1_.
    - **Od množství:** Zadejte _0_.
    - **Do množství:** Zadejte _10000000_.
    - **Jednotka:** Pole ponechejte prázdné.
    - **Vyhledat množství:** Vyberte _Žádné_.
    - **Omezit podle jednotky:** Zrušte zaškrtnutí tohoto políčka.
    - **Zaokrouhlení na jednotku:** Zrušte zaškrtnutí tohoto políčka.
    - **Vyhledat množství balení:** Zrušte zaškrtnutí tohoto políčka.
    - **Povolit rozdělení:** Zaškrtněte toto políčko.

1. Kliknutím na tlačítko **Uložit** uložte nový řádek.
1. Zatímco je nový řádek stále ještě vybrán v mřížce **Řádky**, vyberte možnost **Nový** na záložce s náhledem **Akce směrnice skladového místa**. Přidáte tak nový řádek do mřížky.
1. Na novém řádku nastavte následující hodnoty:

    - **Pořadové číslo:** Zadejte _1_.
    - **Název:** Zadejte _Zone put_.
    - **Využití pevného skladového místa:** Vyberte _Pevná a nepevná skladová místa_.
    - **Povolit záporný stav zásob:** Zrušte zaškrtnutí tohoto políčka.
    - **Dávka povolena:** Zrušte zaškrtnutí tohoto políčka.
    - **Strategie:** Vyberte _Konsolidovat_.

1. Kliknutím na tlačítko **Uložit** uložte novou akci.
1. Dokud je nová akce stále ještě vybrána, klikněte na **Upravit dotaz** nad mřížkou **Akce směrnice skladového místa**.
1. Zobrazí se dialogové okno dotazu. Zde můžete vybrat zónu, z níž se má provést doplnění. Tato zóna by měla být stejná jako zóna uvedená v šabloně doplnění. Na kartě **Oblast** přidejte řádek do mřížky výběrem možnosti **Přidat**.
1. Na novém řádku nastavte následující hodnoty:

    - **Tabulka:** _umístění_
    - **Odvozená tabulka:** _Skladová místa_
    - **Pole:** _ID zóny_
    - **Kritéria:** _PODLAHA_

1. Vyberte **OK**, uložte svůj dotaz a zavřete dialogové okno.
1. Směrnici skladového místa uložíte výběrem možnosti **Uložit**.

## <a name="scenario"></a>Scénář

Tato část obsahuje ukázkový scénář, který ilustruje, jak s touto funkcí pracovat.

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a>Připravte ukázková data, jež potřebujete pro scénář

Než začnete pracovat na scénáři, musíte ukázková data aktivovat a nastavit funkci tak, jak se popisuje v této části a v předchozích částech tohoto tématu.

#### <a name="use-the-usmf-legal-entity"></a>Použijte právnickou osobu USMF

Chcete-li se scénářem pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.

#### <a name="prepare-additional-sample-data"></a>Příprava dalších ukázkových dat

Po výběru právnické osoby **USMF** přidejte další ukázková data, jak jsou potřeba. Postupujte podle popisu v sekci [Nastavení zónového doplňování](#setup) tohoto tématu.

#### <a name="check-your-on-hand-inventory"></a>Zkontrolujte množství na skladě.

Postupujte podle těchto kroků a ujistěte se, že váš systém obsahuje dostatek zásob, aby bylo možné ukázkový scénář realizovat.

1. Ujistěte se, že máte k dispozici zásoby položky *A0001* ve dvou různých skladových místech v oblasti výdeje (*PODLAHA*), jež je uvedena v šabloně doplňování. Celkové zásoby by však měly být nižší než požadované minimální množství (*50*), jež je uvedeno v šabloně doplnění. Tímto způsobem můžete simulovat výpočet pro celou zónu, nikoli pouze pro jedno skladové místo. **Upravte zásoby pomocí některého ze skladových procesů dle potřeby.**
1. Ujistěte se, že máte dostatečné zásoby položky *A0001* na hromadném skladovém místě, které je určeno ve směrnici skladového místa, kde se při práci doplnění má provádět výdej položek ze zóny s ID *BULK*. Celkové zásoby však musí být vyšší než požadované maximální množství (*150*), jež je uvedeno v šabloně doplnění.
1. Volitelné, ale doporučené: Chcete-li vytvořit deník úprav zásob postupujte takto:

    1. Přejděte do **Řízení zásob \> Položky deníku \> Položky \> Úprava zásob**.
    1. Zvolte **Nové**.
    1. V dialogovém okně **Vytvořit deník zásob** vyberte v poli **Sklad** hodnotu *61*.
    1. Vyberte **OK**.
    1. Na záložce s náhledem **Řádky deníku** použijte tlačítko **Nový**. Do mřížky přidejte tři řádky a nastavte následující hodnoty. Po dokončení nastavení každého řádku klikněte na **Uložit**.

        - **Řádek 1:**

            - **Číslo položky:** *A0001*
            - **Lokalita:** *6*
            - **Sklad:** *61*
            - **Skladové místo:** *02A01R1S1B*
            - **Registrační značka:** Vyberte existující registrační značku ze seznamu nebo vytvořte novou registrační značku.
            - **Množství:** *1000*

        - **Řádek 2:**

            - **Číslo položky:** *A0001*
            - **Lokalita:** *6*
            - **Sklad:** *61*
            - **Skladové místo:** *07A01R2S1B*
            - **Registrační značka:** Vyberte existující registrační značku ze seznamu nebo vytvořte novou registrační značku.
            - **Množství:** *15*

        - **Řádek 3:**

            - **Číslo položky:** *A0001*
            - **Lokalita:** *6*
            - **Sklad:** *61*
            - **Skladové místo:** *07A01R1S1B*
            - **Registrační značka:** Vyberte existující registrační značku ze seznamu nebo vytvořte novou registrační značku.
            - **Množství:** *10*

    1. V podokně Akce klikněte na možnost **Ověřit**. Vyřešte všechny chyby, které se vyskytnou. Poté přejděte k dalšímu kroku.
    1. V podokně Akce vyberte možnost **Zaúčtovat**. Tím se provede zaúčtování zásob do skladu.

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a>Ukázkový scénář: Spuštění min./max. doplňování založeného na zónách

Po zajištění všech nezbytných ukázkových dat můžete spustit doplňování takto.

1. Přejděte na **Řízení skladu \> Doplnění \> Doplnění**.
1. V dialogovém okně **Doplnění** na záložce s náhledem **Záznamy k zahrnutí** vyberte **Filtr**.
1. V dialogovém okně **Dotaz** na kartě **Oblast** upravte výchozí řádek tabulky následujícím způsobem:

    - **Tabulka:** Vyberte _Šablony doplnění_.
    - **Odvozená tabulka:** Vyberte _Šablony doplnění_.
    - **Pole:** Vyberte _Šablona doplnění_.
    - **Kritéria:** Vyberte _Min./max. doplnění na bázi zón_. Tuto šablonu doplnění jste vytvořili během přípravy ukázkových dat pro tento scénář.

1. Klikněte na **OK**, uložte dotaz a vraťte se do dialogového okna **Doplnění**.
1. Kliknutím na **OK** spusťte šablonu doplnění.

Práce doplnění jsou nyní vytvořeny pro výdej zásob ze zóny *BULK* a doplnění se provede do zóny *PODLAHA*.

## <a name="notes-and-tips"></a>Poznámky a tipy

Zde je několik poznámek a tipů pro práci s touto funkcí:

- Chcete-li nastavit práci doplnění, jež přejde do požadované zóny, můžete propojit řádky šablony doplnění a směrnice skladového místa některým z následujících způsobů:

    - Upravte záhlaví směrnice skladového místa a filtrujte vybrané řádky šablony doplnění.
    - Použijte kód směrnice na řádku šablony doplnění a srovnávejte jej se zaskladňovací směrnicí skladového místa.

- Pokud používáte dynamická skladová místa, vytvoří se práce doplnění pro první dostupné skladové místo nebo pro skladové místo, které již obsahuje zásoby, je-li akce směrnice skladového místa nastavena k použití strategie **Konsolidovat**.
- Pokud místo zón používáte pevná skladová místa, měli byste použít [standardní min./max. doplnění](tasks/set-up-min-max-replenishment-process.md).
