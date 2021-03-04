---
title: Rozdělení práce
description: Toto téma obsahuje informace o funkci rozdělení práce. Tato funkce umožňuje rozdělit velké pracovní příkazy na několik menších pracovních příkazů, které pak můžete přiřadit několika pracovníkům skladu. Tímto způsobem může stejnou práci vydat současně několika pracovníky skladu.
author: mirzaab
manager: tfehr
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e74b630e72d70829938f0f34efd624509b1ba7c3
ms.sourcegitcommit: 531be324bf706ca727d777720df899d6ddd3c2d7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/05/2020
ms.locfileid: "4424287"
---
# <a name="work-split"></a>Rozdělení práce

Funkce rozdělení práce umožňuje rozdělit velké pracovní ID (tzn. pracovní příkazy obsahující několik řídků) na několik menších pracovních ID, které pak můžete přiřadit několika pracovníkům skladu. Tímto způsobem může stejné číslo vytvoření práce vydat současně několik pracovníků skladu.

> [!IMPORTANT]
> Můžete rozdělit pouze pracovní příkazy, které mají stav *Otevřeno* nebo *Probíhá*.

## <a name="turn-on-the-work-split-functionality"></a>Zapněte funkci rozdělení práce

Než budete moci použít funkci rozdělení práce, musíte zapnout funkci a její nezbytnou funkci ve vašem systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkcí a zapnout ji dle potřeby.

Nejprve zapnout požadovanou funkci *Blokování práce v celé organizaci*, pokud již není zapnutá. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Blokování práce napříč organizací*

> [!NOTE]
> Když je tato funkce aktivována, aktualizace dat se automaticky použije po zapnutí této funkce u všech právnických osob.

Dále zapněte funkci *Rozdělení práce*, která je uvedena následujícím způsobem:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Rozdělení práce*

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a>Vylepšení stránek Podrobnosti práce a Všechny práce

Funkce *Rozdělení práce* přidá následující dvě tlačítka na kartu **Práce** v podokně Akcí na stránkách **Podrobnosti práce** a **Všechny práce**:

- **Rozdělení práce** - Rozdělte ID aktuální práce do několika menších ID práce, která lze zpracovat samostatnými pracovníky.
- **Zrušte relaci rozdělení práce** - Zrušte relaci rozdělení práce a zpřístupněte práci ke zpracování.

![Tlačítka relace Rozdělit práci a Zrušit rozdělení práce](media/Work_split_buttons.png "Tlačítka relace Rozdělit práci a Zrušit rozdělení práce")

> [!IMPORTANT]
> Tlačítko **Rozdělit práci** nebude k dispozici, pokud bude splněna některá z následujících podmínek:
>
> - Stav práce je jiný než *Otevřeno* nebo *Probíhá*.
> - ID kontejneru je přidruženo k ID práce. (Kontejner nelze systematicky rozdělit, protože vyžaduje fyzické akce.)
> - Práce je spojena se seskupením.
> - Typ pracovního příkazu je jiný než jeden z následujících typů:
>
>    - Prodejní objednávky
>    - Výdej suroviny
>    - Vydání převodního příkazu
>
> - Práce je aktuálně rozdělena jiným uživatelem. Pokud se pokusíte otevřít rozdělovací stránku pro práci, která je již rozdělena jiným uživatelem, zobrazí se následující chybová zpráva: „Práce s ID \#\#\#\# je v současné době rozdělena. Zkuste to znovu za několik minut. Pokud budete nadále dostávat tuto zprávu, obraťte se na nadřízeného.“

Nový důvod blokování práce *Rozdělení práce* označuje, kdy je ID práce v procesu rozdělení. Je to zobrazeno jak na stránce **Rozdělit práci** a v aplikaci skladu, pokud se uživatel pokusí spustit práci. Pokud jsou použity důvody blokování, název pole **Blokovaná vlna** z ID práce se změní na **Blokováno**.

## <a name="initiate-a-work-split"></a>Zahajte rozdělení práce

Funkce přidává novou stránku **Rozdělení práce**, která umožňuje uživatelům rozdělit pracovní řádky z ID práce. Při prvním otevření stránky se zobrazí řádky, které mají pracovní stav *Otevřeno* a které jsou k dispozici k rozdělení. V podokně akcí vyberte **Rozdělit práci** pro zpracování vybrané práce.

Chcete-li rozdělit práci, postupujte takto.

1. Otevřete jednu z následujících stránek práce:

    - **Podrobnosti práce** (**Řízení skladu \> Práce \> Podrobnosti práce**)
    - **Všechna práce** (**Řízení skladu \> Práce \> Všechna práce**)

1. V mřížce vyberte ID práce k rozdělení. Pole **Typ pracovního příkazu** musí být nastaveno na jednu z následujících hodnot:

    - Prodejní objednávky
    - Výdej suroviny
    - Vydání převodního příkazu

1. V podokně Akce na kartě **Práce** ve skupině **Práce** vyberte **Rozdělit práci**.

    Stránka **Rozdělit práci** se zobrazí s pracovními řádky, které jsou otevřené a dostupné k rozdělení. Ve výchozím nastavení jsou zobrazeny pouze dostupné pracovní řádky. Chcete-li zobrazit všechny řádky pro pracovní ID (například řádky, které mají pracovní typ *Vložit*), vyberte zaškrtávací políčko **Zobrazit všechny řádky** nad mřížkou.

    Zobrazí se následující zpráva: „Uživatelé nemohou zpracovat řádky práce, dokud nedokončíte rozdělení a nezavřete tuto stránku.“

    Pole **Důvod blokování práce** pro aktuální práci bude nastaveno na *Rozdělit práci* a práce bude zablokována.

    ![Důvod blokování](media/Blocking_reason.png "Důvod blokování")

1. Vyberte řádky, které chcete odebrat z aktuálního ID práce a přidat do nového ID práce. Dojde k následujícím událostem:

    - Když práci rozdělíte, vybraný řádek nebo řádky z původního ID práce se zruší a poté se zkopírují do nového ID práce.
    - Stávající struktura pracovní šablony a umístění vložení (a také budoucí páry vydat / vložit) jsou zachovány. Hodnoty pro následující pole ID práce se zkopírují z původní práce do nové práce:

        - ID nákladu
        - ID dodávky
        - Typ pracovního příkazu
        - Číslo objednávky
        - Lokalita
        - Sklad
        - Pracovní priorita
        - ID fondu práce
        - ID vlny
        - Číslo vytvoření práce

    - Následující pole nejsou zkopírována do nového ID práce:

        - **ID práce** - Z příslušné číselné řady je vygenerováno nové ID práce.
        - **Stav práce** - Toto pole je nastaveno na *Otevřeno*.
        - **Zamknul** - Toto pole je zpočátku nastaveno na prázdné.
        - **Cílová registrační značka** - Toto pole je prázdné.
        - **Datum a čas vytvoření** - Toto pole je nastaveno na aktuální datum a čas.
        - **Blokovaná vlna** - Toto pole je přepočítáno pro původní ID práce a nové ID práce.

1. V podokně akcí vyberte **Rozdělit práci**.

Během rozdělování práce se zobrazí následující zpráva: „Zpracování - dělení práce“. I když je tato zpráva viditelná, můžete operaci zrušit výběrem **Zrušit** v okně se zprávou.

Pokud není zaškrtnou políčko **Zobrazit všechny řádky**, řádek, který byla oddělena a zrušen, se již v mřížce nezobrazí. Pokud je zaškrtnuto políčko, měli byste vidět, že hodnota **Stav práce** pro tento řádek se změnilo na *Zrušeno*.

Zobrazí se následující oznámení, které označuje, že nové ID práce bylo vytvořeno: „Práce \#\#\#\# byla vytvořena oddělením od původní práce \#\#\#\#.“

Další pracovní řádky z původního ID práce (např řádky *Vložit*) budou podle potřeby upraveny tak, aby odrážely řádky prací, které byly zrušeny. Například, pokud původní ID práce mělo řádek *Vložit* pro množství 15 a řádky *Výdej*, kterých je celkem 10, byly zrušeny, nové množství *Vložit* na původním ID práce bude nyní 5.

Nová práce nebude okamžitě přiřazena žádnému uživateli. Můžete ji však nyní podle potřeby přiřadit uživateli pomocí standardní funkce na stránce **Podrobnosti o práci**.

> [!IMPORTANT]
> Můžete rozdělit pouze ID práce, která obsahuja dva nebo více dostupných pracovních řádků. Pokud vyberete **Rozdělit práci**, když existuje pouze jeden řádek práce, zobrazí se následující chybová zpráva: "V počáteční práci musí zůstat alespoň jeden řádek práce." V tomto případě nedojde k rozdělení.

## <a name="finish-a-work-split"></a>Dokončete rozdělení práce

Chcete-li dokončit rozdělení práce, důvod blokování *Rozdělit práci* musí být odstraněn. Toto lze provést dvěma způsoby:

- Uživatel, který rozděluje práci, zavře stránku **Rozdělit práci** výběrem tlačítka **Zavřít** (**X**) v pravém horním rohu. Když je stránka zavřená, důvod blokování *Rozdělení práce* bude odstraněn. Stav *Blokováno* této práce bude přepočítán, a pokud pro tuto práci nebudou žádné zbývající blokovací důvody, bude práce odblokována.
- Libovolný uživatel otevře ID práce a vybere tlačítko **Zrušit relaci rozdělení práce** v podokně akcí. Důvod blokování *Rozdělit práci* bude odstraněn a stav *Blokováno* této práce bude přepočítán, stejně jako když je zavřená stránka **Rozdělit práci**.

Po odstranění důvodu blokování *Rozdělit práci* lze práci spustit na mobilním zařízení, pokud je stav **Blokováno** nastaven na *Ne* na ID práce.

## <a name="user-blocking-on-the-warehouse-app"></a>Blokování uživatelů v aplikaci Sklad

Pokud se pokusíte použít apliaci skladu pro spuštění práce výdeje proti ID práce, která je rozdělována, zobrazí se následující chybová zpráva: „Práce s ID \#\#\#\# je v současné době rozdělována." Pokud se se vám zobrazí tato zpráva, vyberte **Storno**. Poté můžete pokračovat ve zpracování dalších prací.

## <a name="other-blocked-operations"></a>Další blokované operace

Veškeré operace, které upravují pracovní řádky, transakce zásob práce nebo odkazy doplňování, které souvisejí s prací, která je rozdělována, se nezdaří a zobrazí se následující chybová zpráva: „Práce s ID \#\#\#\# je právě rozdělována.“


[!INCLUDE[footer-include](../../includes/footer-banner.md)]