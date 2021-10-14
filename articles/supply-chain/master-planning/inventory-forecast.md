---
title: Prognózy zásob
description: Toto téma popisuje funkčnost prognózy nabídky a poptávky, kterou lze použít k vytvoření prognózy zásob v aplikaci Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 06/08/2021
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ForecastSales, ForecastPurch, ForecastInvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 5ce997a0bb3d6766b801f3f4dea8ab3f19085d02
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577545"
---
# <a name="inventory-forecasts"></a>Prognózy zásob

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak zobrazit a vytvořit prognózy zásob. Můžete vytvářet a zobrazovat řádky prognózy nabídky a poptávky pro položky, skupiny položek, alokační klíče položek, účty zákazníků, skupiny zákazníků, účty dodavatelů a skupiny dodavatelů.

Pro každý řádek prognózy můžete vybrat model prognózy, který se použije. Poté můžete určit položku nebo skupinu položek, a k tomu množství nebo částku transakce. Dále je možné nastavit časový plán přidělení předpokládaného množství.

Řádky prognózy nabídky a poptávky vytvářejí prognózu zásob pro stejnou kombinaci položky a modelu. Tato prognóza zásob představuje rovnováhu mezi nabídkou a poptávkou, které byly zadány pro stejnou položku. Tento údaj nelze upravit. Prognóza zásob pomáhá týmu správy zásob zkontrolovat očekávané změny množství položky na skladě během nadcházejícího období, které bylo předpovídáno.

Po zadání poptávky anebo nabídky můžete spuštěním plánování prognóz vypočítat celkové požadavky na materiály a kapacitu a vygenerovat plánované objednávky.

## <a name="view-and-manually-enter-forecast-lines"></a><a name="manual-entry"></a>Zobrazení a ruční zadání řádků prognózy

Tento postup slouží k ručnímu vytvoření řádků prognózy pro produkty.

Existují také další způsoby, jak vytvořit řádky prognózy:

- [Generování statistické základní prognózy](generate-statistical-baseline-forecast.md).
- [Import historických dat pro prognózy poptávky](import-historical-data.md).
- [Generování prognózy pomocí webové služby Microsoft Azure Machine Learning](demand-forecasting-setup.md).
- [Import řádků prognózy poptávky nebo nabídky pomocí architektury pro správu dat (datové entity ForecastDemandForecastEntryStaging a ForecastSupplyForecastEntryStaging)](../../dev-itpro/data-entities/data-entities-data-packages.md).

Jak ukazuje tabulka v kroku 1, existují různé způsoby přístupu k použitým stránkám.

1. V závislosti na typu entity, pro kterou chcete vytvořit prognózu, a typu prognózy, kterou chcete vytvořit, otevřete stránku prognózy nabídky, poptávky nebo zásob, jak je popsáno v následující tabulce.

    | Celek | Pokyny |
    |---|---|
    | Uvolněné produkty | <ol><li>Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</li><li>Vyberte produkt, pro který chcete vytvořit prognózu.</li><li>V podokně akcí na kartě **Plán** vyberte ve skupině **Prognóza** položku **Prognóza poptávky**, **Prognóza nabídky** nebo **Prognóza zásob**, v závislosti na typu prognózy, se kterou chcete pracovat.</li></ol> |
    | Uvolněné varianty produktu | <ol><li>Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné varianty produktu**.</li><li>Vyberte variantu, pro kterou chcete vytvořit prognózu.</li><li>V podokně akcí na kartě **Plán** vyberte ve skupině **Prognóza** položku **Prognóza poptávky**, **Prognóza nabídky** nebo **Prognóza zásob**, v závislosti na typu prognózy, se kterou chcete pracovat.</li></ol> |
    | Sk. položek | <ol><li>Jděte na **Řízení zásob \> Nastavení \> Sklady \> Skupiny položek**.</li><li>Vyberte skupinu položek, pro kterou chcete vytvořit prognózu.</li><li>V podokně akcí vyberte položku **Prognózování \> Poptávka**, **Prognózování \> Nabídka** nebo **Prognózování \> Prognóza zásob**, v závislosti na typu prognózy, se kterou chcete pracovat.</li></ol> |
    | Alokační klíče pro položky | <ol><li>Přejděte do části **Řízení zásob \> Nastavení \> Prognóza**.</li><li>Vyberte alokační klíč položky, pro kterou chcete vytvořit prognózu.</li><li>V podokně Akce klikněte na možnost **Prognóza poptávky**.</li></ol> |
    | Odběratelé | <ol><li>Přejděte na **Hlavní plánování \> Prognózování \> Ruční zadání prognózy \> Zákazníci**.</li><li>Vyberte zákazníka, pro kterého chcete vytvořit prognózu.</li><li>V podokně Akce klikněte na možnost **Definovat prognózu poptávky**.</li></ol> |
    | Skupiny odběratelů | <ol><li>Přejděte na **Hlavní plánování \> Prognózování \> Ruční zadání prognózy \> Skupiny zákazníků**.</li><li>Vyberte skupinu zákazníků, pro kterou chcete vytvořit prognózu.</li><li>V podokně Akce klikněte na možnost **Definovat prognózu poptávky**.</li></ol> |
    | Dodavatelé | <ol><li>Přejděte na **Hlavní plánování \> Prognózování \> Ruční zadání prognózy \> Dodavatelé**.</li><li>Vyberte dodavatele, pro kterého chcete vytvořit prognózu.</li><li>V podokně Akce výběrem možnosti **Zápis** otevřete stránku **Prognóza dodávky**.</li></ol> |
    | Skupiny dodavatelů | <ol><li>Přejděte na **Hlavní plánování \> Prognózování \> Ruční zadání prognózy \> Skupiny dodavatelů**.</li><li>Vyberte skupinu dodavatelů, pro kterou chcete vytvořit prognózu.</li><li>V podokně Akce výběrem možnosti **Zápis** otevřete stránku **Prognóza dodávky**.</li></ol> | 
    | Všechny řádky | <ul><li>Přejděte na **Hlavní plánování \> Prognózování \> Řádky prognózy poptávky** nebo **Hlavní plánování \> Prognózování \> Řádky prognózy dodávek**, v závislosti na typu prognózy, se kterou chcete pracovat.</li></ul> |

    V závislosti na vašem výběru se zobrazí stránka **Prognóza nabídky** nebo **Prognóza poptávky**. Zobrazuje všechny existující řádky prognózy pro záznam, který jste vybrali před otevřením stránky.

1. V podokně akcí vyberte možnost **Nový**, a přidejte tak řádek prognózy do mřížky v horní části stránky.
1. Na novém řádku vyberte v poli **Model** ten model prognózy, který chcete použít. Poté podle potřeby zadejte další podrobnosti, například položku, skupinu položek, účet nebo skupinu zákazníka nebo dodavatele, množství položky nebo celkovou částku transakce. Úplné podrobnosti o polích, která jsou k dispozici na stránkách **Prognóza nabídky** a **Prognóza poptávky** najdete v dalších částech tohoto tématu.
1. Chcete-li distribuovat prognózu na celé období, vyberte na kartě **Přehled** položku **Přidělit prognózu** na panelu nástrojů.
1. V mřížce **Přidělení** zkontrolujte časový horizont a časové intervaly pro distribuci různých množství pro prognózu.

## <a name="supply-forecast-lines"></a>Řádky prognózy dodávek

Prognóza nabídky vám umožní vytvořit plán pro položky, které je třeba zakoupit. Říká referentům v oblasti nákupu a získávání zdrojů, co mají objednat.

Prognózu nabídky můžete zadat podle položky, skupiny položek, alokačního klíče položek, dodavatele a skupiny dodavatelů. Informace o všech způsobech otevření stránky **Prognóza nabídky** pro různé entity a záznamy najdete v oddíle [Zobrazení a ruční zadání řádků prognózy](#manual-entry) dříve v tomto tématu.

Horní část stránky **Prognóza nabídky** obsahuje mřížku řádků prognózy nabídky a sadu karet, pomocí kterých můžete zobrazit a nastavit další informace pro vybraný řádek prognózy. Spodní část stránky obsahuje mřížku **Přidělení**.

Následující podsekce popisují všechna pole, která jsou k dispozici na každé kartě, a všechny příkazy, které jsou k dispozici v podokně akcí stránky a na panelu nástrojů na kartě **Přehled**.

### <a name="action-pane-commands-on-the-supply-forecast-page"></a>Příkazy podokna akcí na stránce Prognóza nabídky

V následující tabulce jsou popsány příkazy, které jsou k dispozici v podoknu Akce stránky **Prognóza nabídky**.

| Příkaz | popis |
|---|---|
| Uložit | Uložte aktuální nastavení. |
| Upravit | Povolte nastavení na stránce, kterou chcete upravit. |
| Nová | Přidejte řádek prognózy do horní mřížky. |
| Odstranit | Odeberte vybraný řádek prognózy z horní mřížky. |
| Zůstatky prognózy | Zobrazte zůstatky prognózy, které byly vypočítány pro ID modelu vybraného řádku pro aktuální fiskální rok. Zůstatky jsou rozděleny podle období (měsíce). |
| Prognózy cashflow | Zobrazte transakce prognózy, které byly přiděleny do hlavní knihy. Více informací získáte v části [Prognóza cashflow](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Zásoby \> Zobrazit dimenze | Vyberte dimenze inventáře, které by se měly zobrazit v mřížce na kartě **Přehled**. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-supply-forecast-page"></a>Příkazy panelu nástrojů na kartě Přehled ve stránce Prognóza nabídky

V následující tabulce jsou popsány příkazy, které jsou k dispozici v panelu nástrojů na kartě **Přehled** stránky **Prognóza nabídky**.

| Příkaz | popis |
|---|---|
| Přidělit prognózu | Pokud používáte metodu přidělování, vygenerujte jednotlivé řádky plánu pro transakci prognózy. Množství řádku je poté rozděleno podle data (na základě zvolených časových intervalů), množství a částky pro celý časový horizont. (Viz část [Prognóza přidělení](#allocate-forecast) dále v tomto tématu.) |
| Hromadná aktualizace | Otevřete stránku **Úprava transakcí prognóz**. (Viz část [Hromadná aktualizace transakcí prognózy](#bulk-update) dále v tomto tématu.) |
| Prognóza zásob | Otevřete zobrazení stránky **Prognóza zásob**, která je filtrována pro vybranou kombinaci položky / modelu. (Viz část [Prognóza zásob](#inventory-forecast) dále v tomto tématu.) |
| Vytvořit požadavek na položku | Otevřete dialogové okno, kde můžete vytvořit požadavky na položku a řádky prodejní objednávky nebo řádky deníku položky pro transakce prognózy související s projektem. I když je tento příkaz k dispozici jak pro řádky prognózy nabídky, tak pro řádky prognózy poptávky, není možné ho použít na stránce **Prognóza nabídky**. |

### <a name="the-overview-tab-on-the-supply-forecast-page"></a>Karta Přehled ve stránce Prognóza nabídky

Následující tabulka popisuje pole na kartě **Přehled** stránky **Prognóza nabídky**.

| Pole | popis |
|---|---|
| **Model** | Model prognózy, ke kterému je transakce přidružena. |
| **Datum** | Datum zahájení transakce. |
| **Účet dodavatele** | Účet dodavatele, ke kterému je transakce přidružena. |
| **Skupina dodavatelů** | Skupina dodavatele, k níž je transakce přidružena. |
| **Číslo položky** | Identifikátor položky. |
| **Sk. položek** | Skupina položek, k níž je transakce přidružena. |
| **Alokační klíč položky** | Alokační klíč položky, který je přidružen k prognóze. |
| **Množství v SH** | Prognózované množství ve stanovené jednotce skutečné hmotnosti. |
| **Jednotka SH** | Jednotka skutečné hmotnosti, v níž se položka nakupuje. Hodnota se automaticky načte z nastavení položky. |
| **Množství** | Prognózované množství ve stanovené nákupní jednotce. |
| **Jednotka** | Jednotka, v níž se položka nakupuje. Hodnota se automaticky načte z nastavení položky. Můžete ji však upravit, pokud jsou nastaveny převody jednotek. |
| **Částka** | Celková částka minus slevy, kterými transakce prognózy přispívá k prognóze. |
| **Měna** | Měna, která je použita pro transakci prognózy. Výchozí měna je zadána automaticky, ale můžete vybrat jinou měnu. |
| (Jiné dimenze) | Další dimenze lze zobrazit jako sloupce v mřížce. Chcete-li vybrat další zobrazené dimenze, vyberte **Zobrazit dimenze** v podokně akcí. |

### <a name="the-general-tab-on-the-supply-forecast-page"></a>Karta Obecné ve stránce Prognóza nabídky

Karta **Obecné** ukazuje další informace o řádku, který je aktuálně vybrán na kartě **Přehled**. Některé z těchto informací se opakují z karty **Přehled**. Následující tabulka popisuje pole, která se vyskytují pouze na kartě **Obecné**.

| Pole | popis |
|---|---|
| Sestava | Chcete-li transakci zahrnout do vykazování, nastavte tuto možnost na *Ano*. |
| Komentáře | Zde je možné zadat libovolný komentář k transakci prognózy. |
| Aktivní | Chcete-li transakci zahrnout do rozpočtového vykazování, zaškrtněte toto políčko. |
| Zahrnout do prognóz cashflow | Toto políčko vyberte, chcete-li transakci prognózy přidělit položce v hlavní knize. Nastavení tohoto zaškrtávacího políčka nelze u transakcí vykazování upravit. |
| Skupina prodejní daně | Daňová skupina použitá za účelem stanovení daně pro transakci prognózy. |
| Skupina DPH zboží | Skupina DPH položky použitá za účelem stanovení daně pro transakci prognózy. |
| Metoda | <p>Vyberte metodu, která se používá k alokaci transakce prognózy:</p><ul><li>**Žádná** – Nebude provedeno žádné přidělení.</li><li>**Období** – Pro každé období se prognózuje stejné množství . Pokud vyberete tuto hodnotu, zadejte množství v poli **Za** a jednotka času v poli **Jednotka**.</li><li>**Klíč** – Přidělí prognózované množství podle alokačního klíče období, který je stanoven v poli **Klíč období**. Tuto metodu lze použít, když chcete brát do úvahy sezónní výchylky.</li></ol>|
| Za | <p>Zadejte počet časových intervalů do budoucnosti, které prognóza rozšiřuje. Toto pole je k dispozici pouze tehdy, pokud jste v poli **Metoda** vybrali volbu *Období*.</p><p>Například v poli **Metoda** vyberete *Období*, zadáte číslo *1* do pole **Za** a vyberete *Měsíce* v poli **Jednotka**. V poli **Ukončení** zadejte koncové datum, které sahá jeden rok do budoucnosti. V tomto případě se vytvoří jeden řádek prognózy pro každý měsíc následujícího roku na základě položky a množství stanovených v řádku záhlaví.</p> |
| Jednotka | Vyberte jednotku časového intervalu: *Dny*, *Měsíce* nebo *Roky*. Přidělení poté odpovídá počtu dnů, měsíců nebo roků uvedených v poli **Za**.|
| Klíč období | Zadejte alokační klíč období. |
| Konec | Koncové datum určete, když použijete pole **Za** a **Jednotka**. |

### <a name="the-item-tab-on-the-supply-forecast-page"></a>Karta Položka ve stránce Prognóza nabídky

Na kartě **Položka** se zobrazují další informace položky o řádku, který je aktuálně vybrán na kartě **Přehled**.

Mřížka v horní části karty **Položka** opakuje informace o položce, které se také zobrazují na kartě **Přehled**. Kromě toho obsahuje pole **Jednotková cena**, které zobrazuje nákupní cenu za počet jednotek uvedený v poli **Jednotka**. Jednotková cena je automaticky načtena z nastavení položky, ale lze ji upravit.

Pole pod mřížkou poskytují více podrobností o položce. Některé z těchto informací se opakují z karty **Přehled**. Následující tabulka popisuje pole, která se vyskytují pouze na kartě **Položka**.

| Pole | popis |
|---|---|
| Cenová jednotka | Počet jednotek, na které se nákupní cena vztahuje. Tato hodnota se načte automaticky z tabulky Položky, lze ji však změnit. |
| Nákupní poplatky | Pevné náklady na nákupní cenu. Tyto náklady nezávisí na množství. |
| Procento slevy | Sleva jako procento. |
| Částka slevy | Sleva jako částka na prodejní jednotku. |
| Hrubá částka | Částka, při které nejsou uplatněny žádné slevy. |
| Množství | Množství transakce ve skladových jednotkách položky. |
| Dílčí kusovník | Číslo kusovníku pro specifický dílčí kusovník. |
| Dílčí postup | Číslo postupu dílčího postupu. |

### <a name="the-financial-dimensions-tab-on-the-supply-forecast-page"></a>Karta Finanční dimenze ve stránce Prognóza nabídky

Karta **Finanční dimenze** zobrazuje všechny hodnoty finanční dimenze pro řádek, který je aktuálně vybrán na kartě **Přehled**.

### <a name="the-inventory-dimensions-tab-on-the-supply-forecast-page"></a>Karta Dimenze zásob ve stránce Prognóza nabídky

Karta **Dimenze zásob** zobrazuje všechny hodnoty dimenze zásob pro řádek, který je aktuálně vybrán na kartě **Přehled**.

### <a name="the-allocation-grid-on-the-supply-forecast-page"></a>Mřížka Přidělení ve stránce Prognóza nabídky

Pokud používáte alokační klíč položky nebo jste zadali prognózu položky pro jedno či více budoucích období, můžete prognózu přidělit výběrem položky **Přidělit prognózu** na panelu nástrojů na kartě **Přehled**. Množství se poté rozdělí způsobem, který je vyznačen řádky v mřížce **Přidělení**.

## <a name="demand-forecast-lines"></a>Řádky prognózy poptávky

Prognóza poptávky vám umožňuje zadat nebo generovat poptávku pro zákazníka. Pomáhá prodejním a marketingovým referentům informovat hlavní plánovací referentům o očekávané poptávce během nadcházejícího prognózovaného období.

Prognózu poptávky můžete zadat podle položky, skupiny položek, alokačního klíče položek, zákazníka a skupiny zákazníků. Informace o všech způsobech otevření stránky **Prognóza poptávky** pro různé entity a záznamy najdete v oddíle [Zobrazení a ruční zadání řádků prognózy](#manual-entry) dříve v tomto tématu.

Horní část stránky **Prognóza poptávky** obsahuje mřížku řádků prognózy poptávky a sadu karet, pomocí kterých můžete zobrazit a nastavit další informace pro vybraný řádek prognózy. Spodní část stránky obsahuje mřížku **Přidělení**.

Následující podsekce popisují všechna pole, která jsou k dispozici na každé kartě, a všechny příkazy, které jsou k dispozici v podokně akcí stránky a na panelu nástrojů na kartě **Přehled**.

### <a name="action-pane-commands-on-the-demand-forecast-page"></a>Příkazy podokna akcí na stránce Prognóza poptávky

V následující tabulce jsou popsány příkazy, které jsou k dispozici v podoknu Akce stránky **Prognóza poptávky**.

| Příkaz | popis |
|---|---|
| Uložit | Uložte aktuální nastavení. |
| Upravit | Povolte nastavení na stránce, kterou chcete upravit. |
| Nová | Přidejte řádek prognózy do horní mřížky. |
| Odstranit | Odeberte vybraný řádek prognózy z horní mřížky. |
| Zůstatky prognózy | Zobrazte zůstatky prognózy, které byly vypočítány pro ID modelu vybraného řádku pro aktuální fiskální rok. Zůstatky jsou rozděleny podle období (měsíce). |
| Prognóza cashflow | Zobrazte transakce prognózy, které musí být přiděleny do hlavní knihy. Více informací získáte v části [Prognóza cashflow](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Zobrazit dimenze | Vyberte dimenze produktu, úložiště a sledování, které by se měly zobrazit v mřížce na kartě **Přehled**. |
| Náhled hlavní knihy | Zobrazte položky hlavní knihy pro vybranou transakci. |
| Převést řádky nabídky | Převede řádky nabídky do vybraného projektu. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-demand-forecast-page"></a>Příkazy panelu nástrojů na kartě Přehled ve stránce Prognóza poptávky

V následující tabulce jsou popsány příkazy, které jsou k dispozici v panelu nástrojů na kartě **Přehled** stránky **Prognóza poptávky**.

| Příkaz | popis |
|---|---|
| Přidělit prognózu | Pokud používáte metodu přidělování, vygenerujte jednotlivé řádky plánu pro transakci prognózy. Množství řádku je poté rozděleno podle data (na základě zvolených časových intervalů), množství a částky pro celý časový horizont. (Viz část [Prognóza přidělení](#allocate-forecast) dále v tomto tématu.)|
| Hromadná aktualizace | Otevřete stránku **Úprava transakcí prognóz**. (Viz část [Hromadná aktualizace transakcí prognózy](#bulk-update) dále v tomto tématu.) |
| Prognóza zásob | Otevřete zobrazení stránky **Prognóza zásob**, která je filtrována pro vybranou kombinaci položky / modelu. (Viz část [Prognóza zásob](#inventory-forecast) dále v tomto tématu.) |
| Vytvořit požadavek na položku | Otevřete dialogové okno, kde můžete vytvořit požadavky na položku a řádky prodejní objednávky nebo řádky deníku položky pro transakce prognózy související s projektem. |

### <a name="the-overview-tab-on-the-demand-forecast-page"></a>Karta Přehled ve stránce Prognóza poptávky

Následující tabulka popisuje pole na kartě **Přehled** stránky **Prognóza poptávky**.

| Pole | popis |
|---|---|
| **Název úkolu** | Název dávkové úlohy použité k vytvoření řádku prognózy. |
| **Model** | Model prognózy, ke kterému je transakce přidružena. |
| **Datum** | Datum zahájení transakce. |
| **Účet zákazníka** | Účet zákazníka, ke kterému je transakce přidružena. |
| **Skupina odběratelů** | Skupina zákazníka, ke kterému je transakce přidružena. |
| **Číslo položky** | Identifikátor položky. |
| **Název produktu** | Popis položky |
| **Alokační klíč položky** | Alokační klíč položky použitý během přidělení prognózy zásob. |
| **Prod. množství** | Množství transakce ve stanovené prodejní jednotce. |
| **Jednotka** | Jednotka, ve které se položka prodává. |
| **Částka** | Celková částka bez slev, kterými transakce prognózy přispívá k prognóze. |
| **Prodejní cena** | Prodejní cena za počet jednotek uvedený v poli **Cenová jednotka**. Hodnota je automaticky načtena z nastavení položky, ale lze ji upravit. |
| **Prodejní měna** | Měna, která je použita pro transakci prognózy. Výchozí měna je zadána automaticky, ale můžete vybrat jinou měnu. |
| **Množství v SH** | Prognózované množství ve stanovené jednotce skutečné hmotnosti. |
| **Jednotka SH** | Jednotka skutečné hmotnosti, v níž se položka prodává. Hodnota se automaticky načte z nastavení položky. |
| (Jiné dimenze) | Další dimenze produktu, úložiště a sledování lze zobrazit jako sloupce v mřížce. Chcete-li vybrat další zobrazené dimenze, vyberte **Zobrazit dimenze** v podokně akcí. |

### <a name="the-general-tab-on-the-demand-forecast-page"></a>Karta Obecné ve stránce Prognóza poptávky

Karta **Obecné** ukazuje další informace o řádku, který je aktuálně vybrán na kartě **Přehled**. Některé z těchto informací se opakují z karty **Přehled**. Následující tabulka popisuje pole, která se vyskytují pouze na kartě **Obecné**.

| Pole | popis |
|---|---|
| Pořadové číslo prognózy poptávky | Jedinečné číslo řádku prognózy poptávky. Toto číslo je generováno pomocí číselné řady vybrané pro prognózy poptávky na stránce **Parametry hlavního plánování**. |
| Sk. položek | Skupina položek, k níž je transakce přidružena. |
| Sestava | Chcete-li transakci zahrnout do vykazování, nastavte tuto možnost na *Ano*. |
| Komentáře | Zde je možné zadat libovolný komentář k transakci prognózy. |
| Aktivní | Chcete-li transakci zahrnout do rozpočtového vykazování, zaškrtněte toto políčko. Nastavení tohoto zaškrtávacího políčka nelze u transakcí vykazování upravit. |
| Zahrnout do prognóz cashflow | Toto políčko vyberte, chcete-li transakci prognózy přidělit položce v hlavní knize. Nastavení tohoto zaškrtávacího políčka nelze u transakcí vykazování upravit. Více informací získáte v části [Prognóza cashflow](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Skupina prodejní daně | Daňová skupina použitá za účelem stanovení daně pro transakci prognózy. |
| Skupina DPH zboží | Skupina DPH položky použitá za účelem stanovení daně pro transakci prognózy. |
| Metoda | <p>Vyberte metodu, která se používá k alokaci transakce prognózy:</p><ul><li>**Žádná** – Nebude provedeno žádné přidělení.</li><li>**Období** – Pro každé období se prognózuje stejné množství . Pokud vyberete tuto hodnotu, zadejte množství v poli **Za** a jednotka času v poli **Jednotka**.</li><li>**Klíč** – Přidělí prognózované množství podle alokačního klíče období, který je stanoven v poli **Klíč období**. Tuto metodu lze použít, když chcete brát do úvahy sezónní výchylky.</li><ul>|
| Za | <p>Zadejte počet časových intervalů do budoucnosti, které prognóza rozšiřuje. Toto pole je k dispozici pouze tehdy, pokud jste v poli **Metoda** vybrali volbu *Období*.</p><p>Například v poli **Metoda** vyberete *Období*, zadáte číslo *1* do pole **Za** a vyberete *Měsíce* v poli **Jednotka**. V poli **Ukončení** zadejte koncové datum, které sahá jeden rok do budoucnosti. V tomto případě se vytvoří jeden řádek prognózy pro každý měsíc následujícího roku na základě položky a množství stanovených v řádku záhlaví. |
| Jednotka | Vyberte jednotku časového intervalu: *Dny*, *Měsíce* nebo *Roky*. Přidělení poté odpovídá počtu dnů, měsíců nebo roků uvedených v poli **Za**.|
| Klíč období | Zadejte alokační klíč období, který se používá k alokaci prognózy. Další informace naleznete v tématu [Přidělení dat pro plánování rozpočtu](../../finance/budgeting/budget-planning-data-allocation.md). |
| Konec | Koncové datum určete, když použijete pole **Za** a **Jednotka**. |

### <a name="the-item-tab-on-the-demand-forecast-page"></a>Karta Položka ve stránce Prognóza poptávky

Karta **Položka** ukazuje další informace položky pro řádek, který je aktuálně vybrán na kartě **Přehled**. Některé z těchto informací se opakují z karty **Přehled**. Následující tabulka popisuje pole, která se vyskytují pouze na kartě **Položka**.

| Pole | popis |
|---|---|
| Cenová jednotka | Počet prodejních jednotek, k nimž se vztahuje prodejní cena. Tato hodnota se načte automaticky z tabulky Položky, lze ji však změnit. |
| Prodejní náklady | Pevné náklady na prodejní cenu. Tyto náklady nezávisí na množství. |
| Nákladová cena | Náklady na aktuální transakci prognózy za skladovou jednotku. Hodnota se načte z tabulky Položky, lze ji však změnit. |
| Procento slevy | Sleva jako procento. |
| Částka slevy | Sleva jako částka na prodejní jednotku. |
| Hrubá částka | Částka, při které nejsou uplatněny žádné slevy. |
| Množství zásob | Množství transakce ve skladových jednotkách položky. |
| Použít určitý kusovník | Číslo kusovníku určitého kusovníku. |
| Použít určitý postup | Číslo postupu dílčího postupu. |

### <a name="the-project-tab-on-the-demand-forecast-page"></a>Karta Projekt ve stránce Prognóza poptávky

Karta **Projekt** ukazuje další projektové informace o řádku, který je aktuálně vybrán na kartě **Přehled**. Některé z těchto informací se opakují z karty **Přehled**, **Obecné** nebo **Položka**. Následující tabulka popisuje pole, která se vyskytují pouze na kartě **Projekt**.

| Pole | popis |
|---|---|
| Datum projektu | Datum transakce prognózy poptávky. |
| ID projektu | Identifikátor projektu, na který odkazuje aktuální transakce. |
| Zdroj financování | Zdroj financování, ke kterému je prognóza poptávky přidružena. |
| Číslo aktivity | Aktivita, ke které je transakce prognózy poptávky přidružena. |
| Kategorie | Nákladová kategorie aktuální transakce. |
| Vlastnost řádku | Stav, k němuž je transakce připojena. |
| ID transakce | Identifikátor systému pro transakci prognózy poptávky. |
| Částka nákladů | Částka transakce prognózy poptávky. |
| Jedn. cena | Cena za jednotku. |
| Změnil/a | Identifikátor pracovníka, který naposledy upravil vybranou transakci. |
| Datum fakturace | Zadejte očekávané datum faktury. |
| Datum eliminace | Zobrazte nebo změňte datum eliminace. Po vytvoření prognózy je datum eliminace nastaveno na datum ukončení projektu. Pokud projekt nemá datum ukončení, použije se datum projektu. Toto pole platí pro projekty s fixní cenou a investiční projekty. |
| Datum platby nákladů | Zadejte předpokládané datum platby nákupu. |
| Datum platby prodeje | Zadejte předpokládané datum platby prodeje. |

### <a name="the-financial-dimensions-tab-on-the-demand-forecast-page"></a>Karta Finanční dimenze ve stránce Prognóza poptávky

Karta **Finanční dimenze** zobrazuje všechny hodnoty finanční dimenze pro řádek, který je aktuálně vybrán na kartě **Přehled**.

### <a name="the-inventory-dimensions-tab-on-the-demand-forecast-page"></a>Karta Dimenze zásob ve stránce Prognóza poptávky

Karta **Dimenze zásob** zobrazuje všechny hodnoty dimenze zásob pro řádek, který je aktuálně vybrán na kartě **Přehled**.

### <a name="the-allocation-grid-on-the-demand-forecast-page"></a>Mřížka Přidělení ve stránce Prognóza poptávky

Pokud používáte alokační klíč položky nebo jste zadali prognózu položky pro jedno či více budoucích období, můžete prognózu přidělit výběrem položky **Přidělit prognózu** na panelu nástrojů na kartě **Přehled**. Množství se poté rozdělí způsobem, který je vyznačen řádky v mřížce **Přidělení**. (Viz část [Prognóza přidělení](#allocate-forecast) dále v tomto tématu.)

## <a name="inventory-forecast"></a><a name="inventory-forecast"></a>Prognóza zásob

Stránky prognózy nabídky a poptávky mají tlačítko **Prognóza zásob**, které otevírá pohled na stránku **Prognóza zásob**, ve kterém je filtrována stejná kombinace položky / modelu. Prognóza zásob představuje rovnováhu mezi nabídkou a poptávkou, které byly zadány pro stejnou položku. Tento údaj nelze upravit. Prognóza zásob pomáhá týmu správy zásob zkontrolovat očekávané změny množství položky na skladě během nadcházejícího období, které bylo předpovídáno.

### <a name="the-action-pane-on-the-inventory-forecast-page"></a>Podokno akcí na stránce Prognóza zásob

V následující tabulce jsou popsány příkazy, které jsou k dispozici v podoknu Akce stránky **Prognóza zásob**.

| Akce | popis |
|---|---|
| Prognóza dodávek | Otevřete zobrazení stránky **Prognóza nabídky**, která je filtrována pro stejnou kombinaci položky / modelu / kalendářního data. |
| Prognóza poptávky | Otevřete zobrazení stránky **Prognóza poptávky**, která je filtrována pro stejnou kombinaci položky / modelu / kalendářního data. |
| Zásoby \> Zobrazit dimenze | Vyberte dimenze produktu, úložiště a sledování, které by se měly zobrazit v mřížce **Přehled**. |

### <a name="the-grid-on-the-inventory-forecast-page"></a>Mřížka na stránce Prognóza zásob

Následující tabulka popisuje pole v mřížce na stránce **Prognóza zásob**.

| Pole | popis |
|---|---|
| **Model** | Model prognózy, ke kterému je transakce přidružena. |
| **Číslo položky** | Identifikátor položky. |
| **Datum rozpočtu** | Datum transakce prognózy. |
| **Typ prognózy** | Zdroj transakce (*Prognóza poptávky* nebo *Prognóza nabídky*). |
| **Množství v SH** | Prognózované množství v jednotce skutečné hmotnosti. |
| **Množství** | Předpovídané množství ve skladových jednotkách. |
| **Kumulovaná SH** | Kumulované předpovídané množství v jednotce skutečné hmotnosti, když bylo pro stejnou položku nashromážděno více řádků prognózy. |
| **Dílčí kusovník** | Číslo kusovníku dílčího kusovníku. |
| **Dílčí postup** | Číslo postupu dílčího postupu. |
| (Jiné dimenze) | Další dimenze lze zobrazit jako sloupce v mřížce. Chcete-li vybrat další zobrazené dimenze, vyberte **Zásoby \> Zobrazit dimenze** v podokně akcí. |

## <a name="allocate-forecast"></a><a name="allocate-forecast"></a>Přidělit prognózu

Následující postup slouží ke zpracování vybraných transakčních řádků prognózy. Když přidělíte prognózu, množství se poté rozdělí podle řádků v mřížce **Přidělení**.

1. V závislosti na typu entity, pro kterou chcete vytvořit prognózu, a typu prognózy, kterou chcete vytvořit, otevřete stránku prognózy nabídky nebo poptávky, jak je popsáno v tématu [Zobrazení a ruční zadání řádek předpovědi](#manual-entry).
1. Na stránce řádků prognózy nabídky nebo poptávky vyberte řádek prognózy a poté na kartě **Přehled** vyberte kartu **Přidělit předpověď** na panelu nástrojů.
1. V dialogovém okně **Přidělit předpověď** nastavte pole, která jsou popsána v následující tabulce. (Hodnota, kterou vyberete v poli **Metoda** určuje, že ostatní pole jsou k dispozici.)

    | Pole | popis |
    |---|---|
    | Metoda | <p>Vyberte metodu, která se používá k alokaci transakce prognózy:</p><ul><li>**Žádná** – Nebude provedeno žádné přidělení.</li><li>**Období** – Pro každé období se prognózuje stejné množství . Pokud vyberete tuto hodnotu, zadejte množství v poli **Za** a jednotka času v poli **Jednotka**.</li><li>**Klíč** – Přidělí prognózované množství podle alokačního klíče období, který je stanoven v poli **Klíč období**. Tuto metodu lze použít, když chcete brát do úvahy sezónní výchylky.</li><ul>|
    | Za | <p>Zadejte počet časových intervalů do budoucnosti, které prognóza rozšiřuje. Toto pole je k dispozici pouze tehdy, pokud jste v poli **Metoda** vybrali volbu *Období*.</p><p>Například v poli **Metoda** vyberete *Období*, zadáte číslo *1* do pole **Za** a vyberete *Měsíce* v poli **Jednotka**. Pak v poli **Ukončení** zadejte koncové datum, které sahá jeden rok do budoucnosti. V tomto případě se vytvoří jeden řádek prognózy pro každý měsíc následujícího roku na základě položky a množství stanovených v řádku záhlaví. |
    | Jednotka | Vyberte jednotku časového intervalu: *Dny*, *Měsíce* nebo *Roky*. Přidělení poté odpovídá počtu dnů, měsíců nebo roků uvedených v poli **Za**.|
    | Klíč období | Zadejte alokační klíč období, který se používá k alokaci prognózy. Další informace naleznete v tématu [Přidělení dat pro plánování rozpočtu](../../finance/budgeting/budget-planning-data-allocation.md). |
    | Konec | Zadejte koncové datum, které platí pro vaše nastavení, do pole **Pro** a **Jednotka**. |

1. Výběrem **OK** své nastavení potvrďte.
1. Výsledky si můžete prohlédnout na kartě **Přidělení** pro stejný řádek.

## <a name="bulk-update-forecast-transactions"></a><a name="bulk-update"></a>Hromadná aktualizace transakcí prognózy

Tento postup slouží ke zpracování existujících transakčních řádků prognózy. Transakční řádky prognózy můžete kopírovat, upravovat a odstraňovat.

1. Na stránce řádků prognózy nabídky nebo poptávky vyberte možnost **Hromadná aktualizace**.
1. V dialogovém okně vyberte **Filtr**.
1. Na kartě **Rozsah** vyberte kritéria identifikující data zdrojové prognózy, která chcete kopírovat, upravit nebo odstranit. Tato data mohou zahrnovat model prognózy, číslo položky a účet odběratele.
1. Výběrem **OK** svůj výběr potvrďte.

    Po výběru dat můžete v dialogovém okně **Úprava transakcí prognóz** definovat, jak je chcete zkopírovat, upravit nebo odstranit.

    > [!NOTE]
    > Krok filtrování je předpokladem pro použití funkce **Hromadné úpravy**. Pokud ho přeskočíte, program vybere a aktualizuje **všechny** řádky prognózy. Proto byste mohli neúmyslně způsobit duplikaci nebo odebrání transakcí.

1. V části **Řízení** vyberte, zda chcete zkopírovat, aktualizovat nebo odstranit vybrané transakce prognózy.
1. Chcete-li změnit parametry prognózy, použijte oddíl **Úpravy v poli**. Zaškrtněte políčko parametru a poté vyberte některou z dostupných možností. Vyberte například políčko **Model** a poté vyberte číslo modelu předpovědi. Existující řádky prognózy se zkopírují do vybraného modelu prognózy.
1. V oddílu **Změna období** můžete posunout počáteční a koncové datum prognózy dopředu nebo dozadu. Zaškrtněte políčko a poté použijte pole množství a období k definování způsobu přesunutí kalendářních dat prognózy. Můžete zadat záporné množství, abyste posunuli počáteční datum dopředu (to znamená, že začne dříve).

    Chcete-li například odložit datum zahájení transakce prognózy o šest měsíců, zaškrtněte políčko a zadejte *6* jako množství a jako období vyberte *Měsíce*.

1. Oddíl **Opravit pole** použijte k aktualizaci skutečných dat prognózy. V poli **Pole** vyberte kritérium, které chcete změnit. Do pole **Koeficient** zadejte násobitel, který se u vybraného kritéria použije, nebo zadejte konstantu, která bude přičtena nebo odečtena. Například vyberte *Množství* jako kritérium a zadáním koeficientu *1,5* vynásobte množství položky 1,5krát. Popřípadě, chcete-li snížit počet položek o 25 kusů, zadejte konstantu *-25*.
1. Oddíl **Finanční dimenze** použijte k aktualizaci finančních dimenzí řádků prognózy. Vyberte finanční dimenze, které chcete změnit, a poté zadejte hodnotu, která se použije na vybrané dimenze.
1. Výběrem **OK** použijte změny.

## <a name="use-forecasts-with-master-planning"></a>Použít hlavní plánování s prognózou

Po zadání prognózy poptávky a/nebo prognózy nabídky můžete zahrnout prognózy během hlavního plánování, aby se zohlednila očekávaná poptávka a/nebo nabídka v běhu hlavního plánování. Když jsou prognózy zahrnuty do hlavního plánování, jsou vypočítány hrubé požadavky na materiál a kapacitu a jsou generovány plánované objednávky.

### <a name="set-up-a-master-plan-to-include-an-inventory-forecast"></a>Nastavení hlavního plánu tak, aby zahrnoval prognózu zásob

Chcete-li nastavit hlavní plán tak, aby obsahoval prognózu zásob, postupujte takto.

1. Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**.
1. Vyberte stávající plán nebo vytvořte nový plán.
1. Na pevné záložce **Obecné** zadejte následující pole:

    - **Model prognózy** - vyberte model prognózy, který se použije. Tento model se zohlední, když se vygeneruje návrh dodávky pro aktuální hlavní plán.
    - **Zahrnout prognózu dodávek** - Tuto možnost nastavte na *Ano*, aby byla prognóza dodávek zahrnuta do aktuálního hlavního plánu. Pokud ji nastavíte na *Ne*, transakce prognózy dodávek nebudou zahrnuty do hlavního plánu.
    - **Zahrnout prognózu poptávky** - Tuto možnost nastavte na *Ano*, aby byla prognóza poptávky zahrnuta do aktuálního hlavního plánu. Pokud ji nastavíte na *Ne*, transakce prognózy poptávky nebudou zahrnuty do hlavního plánu.
    - **Metoda použitá ke snížení požadavků na prognózu** - Vyberte metodu, která by měla být použita ke snížení požadavků na prognózu. Další informace viz [Redukční klíč prognózy](planning-optimization/demand-forecast.md#reduction-keys).

1. Na pevné záložce **Ochranné doby ve dnech** můžete nastavit následující pole a určit období, během kterého je prognóza zahrnuta během:

    - **Plán prognózy** - Nastavte tuto možnost na *Ano* pro přepis ochranné doby plánu prognózy, která pochází z jednotlivých skupin pokrytí. Pokud chcete použít hodnoty z jednotlivých skupin pokrytí pro aktuální hlavní plán, nastavte *Ne*.
    - **Časové období prognózy** - Pokud nastavíte možnost **Plán prognózy** na *Ano*, zadejte počet dní (od dnešního data), kdy má být použita prognóza poptávky.

    > [!IMPORTANT]
    > Možnost **Plán prognózy** ještě není v rámci optimalizace plánování podporováno.

### <a name="run-a-master-plan-that-includes-an-inventory-forecast"></a>Spustit hlavní plán tak, aby zahrnoval prognózu zásob

Chcete-li spustit hlavní plán tak, aby obsahoval prognózu zásob, postupujte takto.

1. Přejděte na **Hlavní plánování \> Pracovní prostory \> Hlavní plánování**
1. V poli **Hlavní plán** zadejte nebo vyberte hlavní plán, který jste nastavili v předchozím postupu.
1. Na dlaždici **Hlavní plánování** vyberte **Spustit**.
1. V dialogovém okně **Hlavní plánování** nastavte možnost **Sledujte čas zpracování** na *Ano*.
1. Do pole **Počet vláken** zadejte číslo.
1. Na pevné záložce **záznamy, které mají být zahrnuty** vyberte možnost **Filtr**.
1. Zobrazí se standardní dialogové okno editoru dotazů. Na kartě **Oblast** vyberte řádek, ve kterém je pole **Pole** nastaveno na *Číslo položky*.
1. V poli **Kritéria** vyberte číslo položky, kterou chcete zahrnout do plánu.
1. Vyberte **OK**.

Chcete-li zobrazit vypočítané požadavky, otevřete stránku **Celkové požadavky**. Například na stránce **Uvolněné produkty** v podokně akcí, na kartě **Plán**, vyberte ve skupině **Požadavky** možnost **Celkové požadavky**.

Chcete-li zobrazit generované plánované objednávky, přejděte na **Hlavní plánování \> Běžné \> Plánované objednávky** a vyberte příslušný plán prognózy.

## <a name="additional-resources"></a>Další prostředky

- [Přehled prognózy poptávky](introduction-demand-forecasting.md)
- [Nastavení prognózy poptávky](demand-forecasting-setup.md)
- [Generování statistické základní prognózy](generate-statistical-baseline-forecast.md)
- [Ruční úpravy základní prognózy](manual-adjustments-baseline-forecast.md)
- [Hlavní plánování s prognózami poptávky](planning-optimization/demand-forecast.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
