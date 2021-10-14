---
title: Čisté požadavky a informace o doložení s Optimalizací plánování
description: Toto téma poskytuje informace o vypočítaných čistých požadavcích a informacích o doložení v Optimalizaci plánování.
author: ChristianRytt
ms.date: 7/28/2021
ms.topic: article
ms.search.form: ReqTransOverview
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5dbe4633ef061a054388e1b6aa6300e1c835c36a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569762"
---
# <a name="net-requirements-and-pegging-information-with-planning-optimization"></a>Čisté požadavky a informace o doložení s Optimalizací plánování

[!include [banner](../../includes/banner.md)]

Když spustíte hlavní plánování v Optimalizaci plánování, je důležité, abyste porozuměli jeho výstupu, jak stávající nabídka pokrývá poptávku a proč byla vytvořena konkrétní nabídka. Na stránce **Čisté požadavky** můžete lépe porozumět vypočítaným požadavkům, které vytváří hlavní plánování.

Stránka **Čisté požadavky** zobrazuje čisté požadavky, které pro produkt vypočítá Optimalizace plánování. Ukazuje také nastavení disponibility, která byla použita za běhu hlavního plánování, rozpis součtů požadavků podle typu transakce a informace o doložení.

## <a name="open-the-net-requirements-page"></a>Otevření stránky Čisté požadavky

Stránku **Čisté požadavky** můžete otevřít některým z následujících způsobů:

- Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**. Vyberte nebo otevřete produkt. Poté v podokně akcí na kartě **Plán** ve skupině **Požadavky** zvolte **Čisté požadavky**.
- Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**. Otevřete prodejní objednávku. Poté na záložce **Řádky prodejní objednávky** vyberte na panelu nástrojů položku **Produkt a dodávka \> Čisté požadavky**.
- Přejděte na **Hlavní plánování \> Hlavní plánování \> Plánované objednávky**. Vyberte nebo otevřete plánovanou objednávku. Poté v podokně akcí na kartě **Zobrazit** ve skupině **Požadavky** zvolte **Profil požadavku**.

## <a name="use-the-net-requirements-page"></a>Používání stránky Čisté požadavky

Stránka **Čisté požadavky** se skládá z horní a dolní části. Podokno akcí na této stránce obsahuje tlačítko **Aktualizovat**. Po výběru tohoto tlačítka se zobrazí nabídka příkazů.

### <a name="select-a-master-plan-to-view"></a>Výběr hlavního plánu, který chcete zobrazit

Než zkontrolujete čisté požadavky na produkt, nezapomeňte vybrat příslušný hlavní plán v poli **Plán** v horní části stránky.

### <a name="upper-section"></a>Horní část

Horní část stránky obsahuje následující karty:

- **Přehled** - Zobrazuje požadavky na položky dimenzí produktu.
- **Disponibilita položky** - Zobrazuje nastavení disponibility, které bylo použito při výpočtu požadavků.
- **Souhrn** - Zobrazuje rozpis součtů požadavků podle typu transakce.
- **Období** – Zobrazuje příjemky, problémy a předpokládané dostupné zásoby pro každé období, které je definováno šablonou období. Můžete také získat grafický pohled na předpokládané dostupné zásoby.

### <a name="lower-section"></a>Dolní část

Dolní část stránky obsahuje následující karty:

- **Přehled** - Zobrazuje seznam požadavků na produkty, které byly vypočteny během běhu hlavního plánování, spolu s transakcemi výdeje a příjmu, které odpovídají požadavkům. Ve výchozím nastavení je seznam seřazen podle data požadavku. Když vyberete požadavek, z obrazí se na záložce **Doložení** v dolní části buď zdroj požadavku, nebo transakce, které požadavek realizovaly.
- **Všeobecné** – Zobrazení podrobných informací o vybraném požadavku.
- **Akce** – Zobrazení zpráv akcí pro požadavky.

### <a name="the-action-pane"></a>Podokno Akce

V podokně akcí jsou k dispozici následující příkazy:

- **Aktualizovat \> Hlavní plánování** – Spustit hlavní plánování přímo ze stránky **Čisté požadavky**.
- **Aktualizovat \> Plánování prognóz** – Spustit plánování prognózy přímo ze stránky **Čisté požadavky**. Optimalizace plánování zatím tuto operaci nepodporuje.
- **Aktualizovat \> Plánování kontinuity** - Spustit plánování kontinuity přímo ze stránky **Čisté požadavky**. Optimalizace plánování zatím tuto operaci nepodporuje.

## <a name="example-scenario"></a>Příklad

Tento příklad ukazuje, jak jsou informace o doložení prezentovány na stránce **Čisté požadavky**.

### <a name="prerequisites"></a>Předpoklady

Než začnete procházet scénář, musí být splněny následující předpoklady:

1. Musíte pracovat v systému, kde jsou k dispozici standardní ukázková data, a musíte nastavit právnickou osobu na *USMF*.
2. Tento příklad používá produkt *1000*, který je součástí ukázkových dat USMF. Zkontrolujte, zda je tento produkt k dispozici a zda je nastaven následujícím způsobem:

    - **Výchozí typ objednávky:** *Nákupní objednávka*
    - **Zásoby na skladě:** *10.00*

3. Vytvořte prodejní objednávku pro množství *25.00* a jednotkovou cenu ve výši *1000*. Použijte dimenze úložiště, kde se nachází množství skladem.
4. Spusťte hlavní plánování pro hlavní plán *DynPlan*.

### <a name="review-the-calculated-requirements"></a>Kontrola vypočtených požadavků

Dále otevřete stránku **Čisté požadavky** pro produkt *1000* a zkontrolujte, jak si vypočítané požadavky navzájem odpovídají.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Vyberte produkt s **Číslem položky** rovným *1000*.
1. V podokně akcí na kartě **Plán** ve skupině **Požadavky** zvolte **Čisté požadavky**.
1. Na stránce **Čisté požadavky** nastavte pole **Plán** na *DynPlan*.
1. Na kartě **Přehled** v dolní části stránky ověřte, že jsou následující požadavky uvedeny jako řádky v mřížce.

    | Odkaz | Požadavek na množství | Kumulovaný |
    |---|---|---|
    | Na skladě | 10.00 | 10.00 |
    | Plánované nákupní objednávky | 15.00 | 25.00 |
    | Prodejní objednávka | -25.00 | (Prázdné) |

    > [!NOTE]
    > Pole **Požadované množství** představuje celkové množství, které požadavek buď vyžaduje (je-li hodnota záporná), nebo dodá (je-li hodnota kladná). Pole **Akumulováno** představuje celkový příjem a výdej, které se nahromadily během zvoleného období.

1. Vyberte řádek požadavku *Na skladě* a poté na záložce **Doložení** zkontrolujte požadavky, které jsou pokryty touto dodávkou. Měl by se tam objevit následující řádek.

    | Odkaz | Požadavek na množství | Pokryté množství |
    |---|---|---|
    | Prodejní objednávka | -25.00 | -10,00 |

    Stávající inventář na skladě částečně pokrývá poptávku, která pochází z prodejní objednávky.

    ![Informace doložení pro množství na skladě](media/pegging-on-hand.png "Informace doložení pro množství na skladě")

1. Vyberte řádek požadavku *Plánované nákupní objednávky* a poté na záložce **Doložení** zkontrolujte požadavky, které jsou pokryty touto dodávkou. Měl by se tam objevit následující řádek.

    | Odkaz | Požadavek na množství | Pokryté množství |
    |---|---|---|
    | Prodejní objednávka | -25.00 | -15.00 |

    Protože je prodejní objednávka již částečně pokryta, systém vytvoří plánovanou nákupní objednávku pro zbývající nekryté množství.

    ![Informace doložení o plánované nákupní objednávce](media/pegging-planned-purchase-order.png "Informace doložení o plánované nákupní objednávce")

1. Vyberte řádek požadavku *Prodejní objednávka* a poté na záložce **Doložení** zkontrolujte požadavky, které jsou kryty touto poptávkou. Měly by se tam objevit následující řádky.

    | Odkaz | Požadavek na množství | Pokryté množství |
    |---|---|---|
    | Na skladě | 10.00 | 10.00 |
    | Plánované nákupní objednávky | 15.00 | 15.00 |

    ![Informace doložení o prodejní objednávce](media/pegging-planned-purchase-order.png "Informace doložení o prodejní objednávce")

> [!NOTE]
> Protože Optimalizace plánování zatím některé funkce nepodporuje, nejsou typy požadavků *Pojistná zásoba* a *Dávka s ukončenou životností* součástí stránky **Čisté požadavky**. Další informace naleznete v tématu [Analýza shody optimalizace plánování](planning-optimization-fit-analysis.md)
>
> Pokud používáte integrovaný hlavní plánovací modul, jsou podporovány dávkově řízené produkty. U dávkově řízených produktů je inventář, jehož platnost vypršela, zobrazen na stránce **Čisté požadavky**, ale není doložen o požadavky poptávky. Řádky zásob s vypršenou platností tohoto typu jsou zobrazeny jako řádky požadavků *Dávka s ukončenou životností* na stránce **Čisté požadavky**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
