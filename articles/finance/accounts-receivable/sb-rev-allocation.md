---
title: Přidělení výnosu
description: Toto téma vysvětluje, jak použít přidělení výnosů ve fakturaci předplatného.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 2a1bdff364039c6bf0cdfbc11f0979398934c52c
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629395"
---
# <a name="revenue-allocation"></a>Přidělení výnosu

Toto téma vysvětluje, jak nastavit parametry přidělení výnosů pro plán fakturace. Při vytváření plánu fakturace můžete nastavit nebo upravit přidělení výnosů. Když otevřete stránku **Přidělení příjmů** pro aktivní nebo ukončený plán fakturace, pole jsou pouze pro čtení.

## <a name="specify-the-revenue-allocation-for-a-billing-schedule"></a>Zadání přidělení výnosů pro plán fakturace

Chcete-li zadat přidělení výnosů pro plán fakturace, postupujte takto.

1. Na stránce se seznamem **Všechny/aktivní plány fakturace** vyberte plán fakturace nebo řádek plánu fakturace.
2. Na kartě **Přidělení výnosů** v horní části stránky vyberte **Přidělení výnosů**.
3. V poli **Typ víceprvkového uspořádání** vyberte typ uspořádání více prvků (MEA).
4. V poli **Číslo víceprvkového uspořádání** zadejte číslo MEA. Poté v poli **Účet odložených výnosů smlouvy** zadejte účet odložených výnosů smlouvy.

    Pokud nastavíte pole **Typ víceprvkového uspořádání** na **Jednotlivě**, stejné hodnoty **Číslo víceprvkového uspořádání** a **Účet odložených výnosů smlouvy** se použijí pro každý řádek. Pokud nastavíte pole **Typ víceprvkového uspořádání** na **Více**, můžete zadat různé hodnoty **Číslo víceprvkového uspořádání** a **Účet odložených výnosů smlouvy** pro každý řádek.
    
    Číslo MEA lze přiřadit pouze dvěma nebo více položkám. Jediný řádek nesmí mít vlastní číslo MEA.

5. Zvolte možnost **Uložit**.

### <a name="fields"></a>Pole

Stránka **Typ víceprvkového uspořádání** obsahuje následující pole.

| Pole | Popis |
|---|---| 
| Typ víceprvkového uspořádání | <p>Vyberte typ MEA pro transakci:</p><ul><li>**Více** – Řádkové položky v transakci jsou součástí MEA nebo existuje více než jedno uspořádání.</li><li>**Žádné** – Transakce je standardní transakce, která nemá žádné přidělení výnosů.</li><li>**Jediné** – Všechny položky transakce jsou součástí jediného uspořádání MEA.</li></ul> |
| Číslo víceprvkového uspořádání | <p>Číslo MEA pro řádek. Toto pole je dostupné, když je pole **Typ víceprvkového uspořádání** nastaveno na **Více**.</p><p>Pokud je toto pole prázdné a vy přiřadíte číslo MEA, pole **Původ samostatné prodejní ceny** a **Samostatná prodejní cena** se automaticky aktualizují na základě hodnot ze stránky **Samostatná prodejní cena položky**. K dispozici jsou pouze čísla MEA, která jsou přiřazena k jiným řádkům na prodejní zakázce.</p> |
| Účet odložených výnosů smlouvy | Zadejte obchodní vztah, který se má použít pro položky deníku při vytvoření faktury smlouvy MEA. Toto pole je dostupné, pouze když je používána opakovaná fakturace smlouvy. |
| **Řádky** | |
| Číslo varianty | Číslo varianty z prodejní objednávky. |
| Číslo položky | Číslo položky z prodejní objednávky. |
| Frekvence fakturace | Frekvence přidělení výnosů: **Denně**, **Měsíčně**, **Čtvrtletně**, **Pololetně** nebo **Každoročně**. |
| Množství | Hodnota je z prodejní objednávky. |
| Hodnota smlouvy | Hodnota smlouvy. |
| Číslo víceprvkového uspořádání | <p>Číslo MEA pro řádek. Toto pole je dostupné, když je pole **Typ víceprvkového uspořádání** nastaveno na **Více**.</p><p>Pokud je toto pole prázdné a vy přiřadíte číslo MEA, pole **Původ samostatné prodejní ceny** a **Samostatná prodejní cena** se automaticky aktualizují na základě hodnot ze stránky **Samostatná prodejní cena položky**. K dispozici jsou pouze čísla MEA, která jsou přiřazena k jiným řádkům na prodejní zakázce. Pokud tyto hodnoty nejsou pro položku nastaveny, použijí se hodnoty ze stránky **Parametry víceprvkového přidělení výnosů**.</p> | 
| Původ samostatné prodejní ceny | <p>Původ samostatné prodejní ceny:</p><ul><li>**Částka** - Samostatná prodejní cena je částka, kterou určíte a která je větší než 0 (nula). Částka se podle potřeby převádí mezi funkční a původní měnou.</li><li>**Základní prodejní cena** - Samostatná prodejní cena odpovídá základní prodejní ceně položky.</li><li>**Fakturační cena** - Samostatná prodejní cena odpovídá fakturační ceně položky.</li><li>**Procento položky** - Samostatná prodejní cena je uvedena jako procentuální hodnota a vypočítává se na základě ceny položky. Pokud je vybrána tato možnost, zadejte výchozí procento.</li><li>**Přidělit zbytkovou částku** - Původ samostatné prodejní ceny se vypočítá jako *Celková smluvní hodnota nadřazené položky* – *Celková samostatná prodejní cena podřízených položek*:</p><ul><li>*Celková smluvní hodnota nadřazené položky* je čistá nebo fakturovaná částka.</li><li>*Celková samostatná prodejní cena podřízených položek* je součet rozšířené nebo smluvní samostatné prodejní ceny všech podřízených položek, kromě podřízené položky, která využívá tento původ samostatné prodejní ceny.</li></ul><p>Pokud je vypočtená částka záporná, částka je nastavena na 0 (nula).</p><p>**Poznámka:** Tuto možnost lze vybrat pouze pro jednu podřízenou položku v rozdělení příjmů.</p></li><li>**Žádný** - Původ samostatné prodejní ceny je založen na podřízených položkách. Tato možnost se vztahuje na položky, které jsou definovány jako nadřazené položky v šabloně rozdělení příjmů. Pokud je zaškrtnuto políčko **Rozdělení příjmů**, tato možnost se vybere automaticky a nastavení nelze změnit.</li><li>**Procento nadřazené fakturační ceny** - Původ samostatné prodejní ceny je procento z fakturované ceny nadřazené položky. Tato možnost je k dispozici pouze pro podřízené položky v šabloně rozdělení příjmů.</li><li>**Procento nadřazené standardní ceny** - Původ samostatné prodejní ceny je procento ze standardní ceny nadřazené položky. Tato možnost je k dispozici pouze pro podřízené položky v šabloně rozdělení příjmů. Když se volba pro podřízenou položku změní z **Procento standardní ceny nadřazené položky** na **Procento z ceny nadřazené faktury** nebo z **Procento z ceny nadřazené faktury** na **Procento standardní ceny nadřazené položky**, jsou také aktualizovány vypočtené hodnoty.</li></ul> |
| Samostatná prodejní cena | <p>Samostatná prodejní cena řádku v měně transakce.</p><p>Hodnota v poli **Částka** je buď zadána nebo vypočítána.</p> |
| Samostatná prodejní cena smlouvy | Samostatná prodejní cena smlouvy. |
| Zbývající výnos smlouvy | Zbývající částka výnosů pro smlouvu. Tato částka je součtem všech řádků, pro které ještě nebyly vytvořeny faktury. |
| Celkové výnosy smlouvy | Celková částka výnosů smlouvy pro řádek. Tato částka je součtem všech řádků bez ohledu na faktury, které pro ně byly vytvořeny. |
| Účet odložených výnosů smlouvy | <p>Zadejte obchodní vztah, který se má použít pro položky deníku při vytvoření faktury smlouvy MEA.</p><p>Toto pole je dostupné, pouze když je používána opakovaná fakturace smlouvy.</p> |
| Chyba | Jakékoli chyby, ke kterým došlo při přidělení výnosů. |

## <a name="use-revenue-allocation-on-a-sales-order"></a>Použití přidělení výnosů na prodejní objednávce

Chcete-li použít funkci přidělení výnosů na prodejní objednávce, postupujte takto.

1. Na stránce **Všechny prodejní objednávky** vytvořte prodejní objednávku obsahující položky.
2. Na kartě **Faktura** v sekci **Přidělení výnosů** vyberte **Přidělení výnosů**.
3. V poli **Typ víceprvkového uspořádání** vyberte typ MEA.
4. V poli **Číslo víceprvkového uspořádání** zadejte číslo MEA.
5. Pokud je pole **Typ víceprvkového uspořádání** nastaveno na **Více**, vyberte požadované řádky a poté vyberte **Použít na vybrané**.
6. Zvolte možnost **Uložit**.

Pokud použijete časové rozlišení výnosů a výdajů, automaticky se vytvoří plán časově rozlišených položek. Můžete si jej prohlédnout na stránce **Všechny plány časově rozlišených položek**.
