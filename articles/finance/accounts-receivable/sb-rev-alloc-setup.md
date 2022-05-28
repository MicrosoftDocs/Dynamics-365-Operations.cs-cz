---
title: Nastavit víceprvkové přidělení výnosů
description: Toto téma popisuje, jak nastavit parametry pro víceprvkové přidělování příjmů ve fakturaci předplatného.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: bb5b220dd941cbb9f1fda5d0eb821a86a9135309
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685792"
---
# <a name="set-up-multiple-element-revenue-allocation"></a>Nastavit víceprvkové přidělení výnosů

Alokace výnosů z více prvků vám umožňuje nastavit různé šablony, které se používají k výpočtu a alokaci výnosů napříč vícero položkami. Tato funkce vám může pomoci splnit požadavky Kodifikace účetních standardů Téma 606 (ASC 606) a/nebo Mezinárodní standard účetního výkaznictví 15 (IFRS 15).

## <a name="multiple-element-revenue-allocation-parameters"></a>Parametry víceprvkového přidělení výnosů

Použijte srtánku **Víceprvkové parametry alokace výnosů** stránku pro nastavení parametrů pro víceprvkové přidělování příjmů.

### <a name="standalone-selling-price-origin"></a>Původ samostatné prodejní ceny

Pole **Samostatný původ prodejní ceny** pole určuje, odkud pochází samostatná prodejní cena. Hodnotu můžete aktualizovat na stránce **Samostatná prodejní cena položky** a na transakci. K dispozici jsou tyto možnosti.

| Parametr | Popis |
|--------|-------------|
| Částka | Samostatná prodejní cena je částka, kterou určíte a která je větší než 0 (nula). Částka se podle potřeby převádí mezi funkční a původní měnou. |
| Základní prodejní cena | Samostatná prodejní cena odpovídá základní prodejní ceně položky. |
| Cena faktury | Samostatná prodejní cena odpovídá fakturační ceně položky. |
| Procento položky | Samostatná prodejní cena je uvedena jako procentuální hodnota a vypočítává se na základě ceny položky. Pokud vyberete tuto možnost, zadejte výchozí procento. |
| Přidělit zbytkovou částku | <p>Původ samostatné prodejní ceny se vypočítá jako *Celková smluvní hodnota nadřazené položky* – *Celková samostatná prodejní cena podřízených položek*:</p><ul><li>*Celková smluvní hodnota nadřazené položky* je čistá nebo fakturovaná částka.</li><li>*Celková samostatná prodejní cena podřízených položek* je součet rozšířené nebo smluvní samostatné prodejní ceny všech podřízených položek, kromě podřízené položky, která využívá tento původ samostatné prodejní ceny.</li></ul><p>Pokud je vypočtená částka záporná, částka je nastavena na 0 (nula).</p><p>**Poznámka:** Tuto možnost lze vybrat pouze pro jednu podřízenou položku v rozdělení příjmů.</p> |
| Žádná | Původ samostatné prodejní ceny je založen na podřízených položkách. Tato možnost se vztahuje na položky, které jsou definovány jako nadřazené položky v šabloně rozdělení příjmů. Pokud je zaškrtnuto políčko **Rozdělení příjmů**, tato možnost se vybere automaticky a nastavení nelze změnit. |
| Procento z ceny nadřazené faktury | Původ samostatné prodejní ceny je procento z fakturované ceny nadřazené položky. Výchozí hodnotu můžete změnit. Tato možnost je k dispozici pouze pro podřízené položky v šabloně rozdělení příjmů. |
| Procento z nadřazené standardní ceny | Původ samostatné prodejní ceny je procento ze standardní ceny nadřazené položky. Výchozí hodnotu můžete změnit. Tato možnost je k dispozici pouze pro podřízené položky v šabloně rozdělení příjmů. Je to výchozí možnost pro podřízené položky. Když se volba pro podřízenou položku změní z **Procento standardní ceny nadřazené položky** na **Procento z ceny nadřazené faktury** nebo z **Procento z ceny nadřazené faktury** na **Procento standardní ceny nadřazené položky**, jsou také aktualizovány vypočtené hodnoty. |

### <a name="account-for-revenue-allocation-rounding-differences"></a>Zohlednit rozdíly zaokrouhlování přidělení výnosů

Pole **Zohledněte rozdíly zaokrouhlování přidělení výnosů** určuje účet, který se používá k zaznamenání jakýchkoli úprav zaokrouhlení částky výnosu ze smlouvy. Je k dispozici při použití opakované fakturace smlouvy.

## <a name="item-standalone-selling-price"></a>Samostatná prodejní cena položky

Použijte stránku **Samostatná prodejní cena položky**, chcete-li specifikovat původ a samostatnou prodejní cenu položky. Hodnoty zadané na této stránce se používají jako výchozí hodnoty na stránce **Alokace výnosů** v alokaci příjmů s více prvky a opakované smluvní fakturaci.

### <a name="specify-item-standalone-selling-price"></a>Zadejte samostatnou prodejní cenu položky

Chcete-li zadat samostatnou cenu položky, postupujte takto.

1. Na stránce **Samostatná prodejní cena položky** v poli **Samostatný původ prodejní ceny** vyberte původ samostatné prodejní ceny.
2. Proveďte některý z následujících kroků v závislosti na hodnotě, kterou jste vybrali v poli **Původ samostatné prodejní ceny**:

    * Pokud jste vybrali **Procenta položky**, zadejte procento v poli **Procenta**.
    * Pokud jste vybrali **Částka**, uveďte částku v poli **Samostatná prodejní cena**.

2. Pro každou položku, kterou chcete přidat do seznamu, vyberte **Přidat**.
3. V poli **Kód položky** vyberte kód položky. V poli **Vztah položky** vyberte vztah položky. U položek, kde není zaškrtnuté políčko **Rozdělení příjmů**, vybraná kombinace kódu položky a vztahu položky musí být jedinečná.
4. Změňte výchozí hodnotu pole **Původ samostatné prodejní ceny**, **Samostatná prodejní cena** nebo **Procenta** podle potřeby.
5. Pro každou nadřazenou položku, kterou chcete přidat do seznamu, vyberte **Přidat**.
6. V poli **Kód položky** vyberte kód položky. V poli **Vztah položky** vyberte vztah položky.
7. Zaškrtněte pole **Rozdělení výnosů**.
8. V poli **Vztah položky** vyberte vztah položky. Seznam se aktualizuje o nadřazenou položku a všechny podřízené položky.
9. U podřízené položky změňte výchozí hodnotu polí **Původ samostatné prodejní ceny**, **Procenta nadřazené standardní ceny**, **Procento z ceny nadřazené faktury** nebo **Přidělte zbytkovou částku** dle potřeby.
10. Chcete-li přidat několik položek najednou, vyberte **Přidat položky**.
11. Aktualizujte dotaz pro výběr rozsahu položek, které chcete přidat.
12. Vyberte **OK**, zkontrolujte seznam položek, které jste přidali, a vyberte **OK**.

### <a name="fields"></a>Pole

Stránka **Samostatná prodejní cena položky** obsahuje následující pole.

| Pole | Popis |
|-------|-------------|
| Původ samostatné prodejní ceny | <p>Vyberte původ samostatné prodejní ceny:</p><ul><li>**Částka** - Samostatná prodejní cena je částka, kterou určíte a která je větší než 0 (nula). Částka se podle potřeby převádí mezi funkční a původní měnou.</li><li>**Základní prodejní cena** - Samostatná prodejní cena odpovídá základní prodejní ceně položky.</li><li>**Fakturační cena** - Samostatná prodejní cena odpovídá fakturační ceně položky.</li><li>**Procento položky** - Samostatná prodejní cena je uvedena jako procentuální hodnota a vypočítává se na základě ceny položky. Pokud vyberete tuto možnost, zadejte výchozí procento.</li></ul>**Přidělit zbytkovou částku** - Původ samostatné prodejní ceny se vypočítá jako *Celková smluvní hodnota nadřazené položky* – *Celková samostatná prodejní cena podřízených položek*:</p><ul><li>*Celková smluvní hodnota nadřazené položky* je čistá nebo fakturovaná částka.</li><li>*Celková samostatná prodejní cena podřízených položek* je součet rozšířené nebo smluvní samostatné prodejní ceny všech podřízených položek, kromě podřízené položky, která využívá tento původ samostatné prodejní ceny.</li></ul><p>Pokud je vypočtená částka záporná, částka je nastavena na 0 (nula).</p><p>**Poznámka:** Tuto možnost lze vybrat pouze pro jednu podřízenou položku v rozdělení příjmů.</p></li><li>**Žádný** - Původ samostatné prodejní ceny je založen na podřízených položkách. Tato možnost se vztahuje na položky, které jsou definovány jako nadřazené položky v šabloně rozdělení příjmů. Pokud je zaškrtnuto políčko **Rozdělení příjmů**, tato možnost se vybere automaticky a nastavení nelze změnit.</li><li>**Procento nadřazené fakturační ceny** - Původ samostatné prodejní ceny je procento z fakturované ceny nadřazené položky. Výchozí hodnotu můžete změnit. Tato možnost je k dispozici pouze pro podřízené položky v šabloně rozdělení příjmů.</li><li>**Procento nadřazené standardní ceny** - Původ samostatné prodejní ceny je procento ze standardní ceny nadřazené položky. Výchozí hodnotu můžete změnit. Tato možnost je k dispozici pouze pro podřízené položky v šabloně rozdělení příjmů. Je to výchozí možnost pro podřízené položky. Když se volba pro podřízenou položku změní z **Procento standardní ceny nadřazené položky** na **Procento z ceny nadřazené faktury** nebo z **Procento z ceny nadřazené faktury** na **Procento standardní ceny nadřazené položky**, jsou také aktualizovány vypočtené hodnoty.</li></ul> |
| Samostatná prodejní cena | Zadejte samostatnou prodejní cenu položky. Toto pole je dostupné, když je pole **Původ samostatné prodejní ceny** nastaveno na **Částku**. |
| Procento | Zadejte procento samostatné prodejní ceny. Toto pole je dostupné, když je pole **Původ samostatné prodejní ceny** nastaveno na **Procento položky**, **Procento z ceny nadřazené faktury** nebo **Procento nadřazené standardní ceny**. |
| Rozdělení výnosů | <p>Určete, zda řádek používá rozdělení příjmů:</p><ul><li>**Vybraný** – Pouze položky, pro které je nastavena šablona rozdělení příjmů, lze vybrat v poli **Vztah položky**. Můžete zaškrtnou toto políčko pouze pro pro nadřazené položky šablony rozdělení výnosu.</li><li>**Vymazáno** – Položka je standardní položka, která nepoužívá rozdělení příjmů.</li></ul> |
| Vztah | Symbol označuje, zda je položka nadřazenou nebo podřízenou položkou v rozdělení příjmů. |
| Kód položky | <p>Vyberte kód položky: **Tabulka** nebo **Skupina**.</p><p>Pokud je zaškrtnuto políčko **Rozdělení příjmů**, toto pole je nastaveno na **Tabulka** a hodnotu nelze změnit.</p> |
| Vztah položky | <p>Vyberte číslo položky.</p><p>Pokud je zaškrtnuto políčko **Rozdělení příjmů**, budou k výběru dostupné pouze položky, které jsou nadřazenými položkami, pro které je nastavena šablona rozdělení příjmů. Pokud je vybrána nadřazená položka, seznam se automaticky aktualizuje podřízenými položkami této nadřazené položky.</p> |
| Nadřazená položka | U nadřazené položky toto pole zobrazuje číslo položky. U podřízených položek v rozdělení příjmů zobrazuje číslo položky nadřazené položky. |

## <a name="mea-templates"></a>Šablony MEA

Použijte stránku **MEA šablony** k vytvoření a úpravě ID šablon uspořádání více prvků (MEA). Tato ID se používají na stránce **Alokace příjmů** pro seskupení položek dohromady.

### <a name="create-a-template"></a>Vytvořit šablonu

Chcete-li nastavit šablonu MEA, postupujte následujícím způsobem.

1. Na stránce **Šablony MEA** zvolte **Nová**.
1. Do pole **ID šablony MEA** zadejte jedinečné ID.
1. Zadejte popis do pole **Popis**.
1. V poli **Účet odložených výnosů ze smlouvy** vyberte účet, který chcete použít pro zápisy do deníku při vytvoření faktury smlouvy MEA. Toto pole je dostupné, když je povoleno a používáno opakované účtování smlouvy.
1. Zvolte možnost **Uložit**.
