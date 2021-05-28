---
title: Automatické nastavení nákladů
description: Toto téma popisuje nastavení pravidel nákladů pro různé úrovně příchozí cesty. Na základě těchto pravidel systém vypočítá náklady a automaticky je přidá. Uživatelé proto nemusí náklady ručně přidávat.
author: sherry-zheng
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostAutoSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d057522afbf6a6d706c51f7c9e69b656483c7eb1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021653"
---
# <a name="auto-costs-setup"></a>Automatické nastavení nákladů

[!include [banner](../../includes/banner.md)]

Na stránce **Automatické náklady** můžete nastavit pravidla nákladů pro různé nákladové oblasti (například cesty, přepravní kontejnery, folia, nákupní objednávky, položky nebo řádky převodních objednávek). Na základě pravidel a polí, která uživatelé vyberou při vytváření záznamů pro jednu z nákladových oblastí, systém vypočítá náklady a automaticky je přidá. Uživatelé proto nemusí náklady ručně přidávat.

Chcete-li pracovat s automatickými náklady, přejděte na stránku **Náklady za doručení \> Nastavení kalkulace \> Automatické náklady**. Poté nastavte pravidla pro automatické náklady, jak je popsáno ve zbytku tohoto tématu.

## <a name="work-with-cost-areas"></a>Práce s nákladovými oblastmi

Automatické náklady fungují jako obchodní smlouvy nebo různé automatické poplatky. Každý záznam o automatických nákladech patří do určité úrovně nákladů. Pole **Nákladová oblast** v podokně seznamu **Automatické náklady** slouží k výběru nákladové oblasti, se kterou chcete pracovat. Podokno seznamu zobrazuje pouze automatické náklady, které patří do aktuálně vybrané nákladové oblasti. Všechny automatické náklady, které vytvoříte, budou patřit do aktuálně vybrané nákladové oblasti.

Oblasti nákladů umožňují systému rozdělit náklady mezi řádky nákupní objednávky v nákladové oblasti. Například náklady na jeden přepravní kontejner rozdělí hodnotu na všechny produkty v tomto přepravním kontejneru. Pokud existují dva nebo více přepravních kontejnerů, lze pro každý přepravní kontejner zadat stejný typ nákladů. Proto lze použít typ kontejneru k nalezení správných automatických nákladů.

## <a name="buttons-on-the-action-pane"></a>Tlačítka v podokně akcí

V následující tabulce jsou popsána tlačítka, která jsou k dispozici v podoknu Akce stránky **Automatické náklady**.

| Tlačítko | popis |
|---|---|
| Úpravy | Úprava stávajících automatických nákladů. |
| Nová | Vytváření automatických nákladů. |
| Odstranit | Odstranění automatických nákladů. |
| Kopírovat z | Vytvořte nový záznam automatických nákladů na základě stávajícího záznamu. Poté můžete nový záznam libovolně upravit. Toto tlačítko vám pomůže rychle vytvořit nové automatické náklady. |
| Zobrazit dimenze | Otevřete dialogové okno, kde můžete vybrat dimenze zásob, které se ukazují pro zobrazené nákladové transakce. Pokud zrušíte zaškrtnutí políček, u nákladových transakcí se zobrazí méně dimenzí zásob. Proto se u transakce zobrazí méně podrobností. Pokud je pro automatické náklady zadána dimenze zásob, použijí se automatické náklady pouze v případě, že se pro položku na cestě použije zadaná dimenze zásob. |

## <a name="settings-on-the-header"></a>Nastavení v záhlaví

Kombinace nastavení v části záhlaví určuje, kdy a jak se k cestě přidají konkrétní automatické náklady. Automatické náklady budou použity na cestu, přepravní kontejner nebo folio, pouze pokud se podrobnosti automatických nákladů shodují s podrobnostmi v záhlaví dané nákladové oblasti. Součet všech odpovídajících automatických nákladů určuje odhadované náklady na doručení za cestu. Tato cena je rozdělena mezi všechny položky na plavidle nebo cestě.

V následující tabulce jsou popsána všechna pole, která se objeví v části záhlaví. Konkrétní dostupná pole se však liší v závislosti na nákladové oblasti a aktuálně vybraných dimenzích zobrazení.

| Pole | popis |
|---|---|
| **Kód účtu** | <p>Vyberte jednu z následujících hodnot:</p><ul><li>**Tabulka** – Pravidlo nákladů se uplatňuje pouze na určitého odběratele.</li><li>**Tabulka** – Pravidlo nákladů se uplatňuje pouze na určitou skupinu odběratelů. Systém bude hledat [skupinu typů nákladů dodavatele](costing-parameters-setup.md) která je přidružena k záznamu dodavatele.</li><li>**Vše** – Pravidlo nákladů platí pro všechny dodavatele. |
| **Dopravní společnost** | Vyberte dodavatele nebo skupinu dodavatelů, na kterou se vztahuje pravidlo nákladů. Toto pole je k dispozici pouze tehdy, pokud vyberete možnost *Tabulka* nebo *Skupina* v poli **Kód účtu**. |
| **Celní deklarant** | Vyberte dodavatele nebo skupinu dodavatelů, na kterou se vztahuje pravidlo nákladů. Toto pole je k dispozici pouze tehdy, pokud vyberete možnost *Tabulka* nebo *Skupina* v poli **Kód účtu**. |
| **Kód položky** | <p>Vyberte jednu z následujících hodnot:</p><ul><li>**Tabulka** – Pravidlo nákladů se uplatňuje pouze na určitou položku.</li><li>**Skupina** – Pravidlo nákladů se uplatňuje pouze na určitou skupinu položek. Systém bude hledat [skupinu typů nákladů položky](costing-parameters-setup.md) která je přidružena k záznamu položky.</li><li>**Vše** – Pravidlo nákladů platí pro všechny položky.|
| **Vztah položky** | Vyberte položku nebo skupinu položek, na kterou se vztahuje pravidlo nákladů. Toto pole je k dispozici pouze tehdy, pokud vyberete možnost *Tabulka* nebo *Skupina* v poli **Kód položky**. |
| **Způsob dodání** | Vyberte způsob doručení (například letecky nebo lodí), na který se pravidlo nákladů vztahuje. |
| **Typ kontejneru** | Typ přepravního kontejneru, ve kterém bude zboží odesláno. Automatické náklady lze na cestu použít, pouze pokud typ kontejneru odpovídá nastavení automatických nákladů typu kontejneru cesty. |
| **Z přístavu** a **Do přístavu** | Zdrojový („od“) přístav a cílový („do“) přístav cesty. (Některé přepravní kontejnery mohou mít různé přístavy „do“, protože cesta může procházet přes více přístavů.) Automatické náklady lze na cestu použít pouze v případě, že se přístavy „od“ a „do“ v nastavení automatických nákladů shodují s přístavy „od“ a „do“ cesty. |
| **Číslo automatických nákladů** | Jednoznačný identifikátor pravidla automatických nákladů. Hodnota tohoto pole je automaticky generována na základě číselné řady, která je nastavena na stránce **Parametry nákladů za doručení**. |
| **Dimenze zásob** | Některé nákladové oblasti umožňují zahrnout do záhlaví jednu nebo více dimenzí položky (například velikost, barvu, sklad a číslo šarže). Chcete-li vybrat zahrnuté dimenze, vyberte možnost **Zobrazit dimenze** v podokně akcí. |

## <a name="settings-on-the-lines-fasttab"></a>Nastavení na záložce Řádky

Na záložce **Řádky** přidejte řádek pro každou měnu, kterou lze použít, když jsou na řádek nákupní objednávky na cestě použity náklady. 

U položek a nákupních objednávek systém porovná měnu každého řádku nákupní objednávky s měnami, které jsou uvedeny na záložce **Řádky**. Použije pouze nákladovou hodnotu, která je nastavena pro odpovídající řádek nebo položku. Pokud pro měnu řádku nebo položky není nastaven žádný řádek, nebudou na tento řádek nebo položku automatické náklady použity.

U ostatních typů nákladových oblastí budou všechny řádky na záložce **Řádky** použity na každou cestu, přepravní kontejner, folio nebo řádek převodní objednávky, který odpovídá hodnotám stanoveným v záhlaví.

V následující tabulce jsou popsána všechna pole, která se objeví na každém řádku. Konkrétní dostupná pole se však liší v závislosti na aktuálně vybrané nákladové oblasti.

| Pole | popis |
|---|---|
| **Měna** | Vyberte měnu, na kterou se řádek vztahuje. Tato měna souvisí s nákupní objednávkou. Když se systém pokouší najít automatické náklady, které by měly být použity na cestu a její řádky, vybere řádek, která má stejnou měnu jako nákupní objednávka. Toto pole je k dispozici pouze v případě, že je pole **Nákladová oblast** nastaveno na hodnotu *Nákupní objednávka* nebo *Položka*. |
| **Kód typu nákladů** | Typ nákladů. |
| **Způsob rozdělení** | <p>Metoda, která se používá k rozdělení nákladů na řádky. Existují tyto možnosti:</p><ul><li><p>**Procento** – Hodnota pole **Hodnota nákladů** je procento, které se vztahuje na celkovou hodnotu zboží.</p><p>Například je-li pole **Hodnota nákladů** nastaveno na *10* a celková hodnota zboží je 800 USD, hodnota nákladů je 80 USD (= 800 USD × 10 procent).</p></li><li>**Množství** – Náklady budou rozděleny na základě množství zboží.</li><li>**Částka** – Náklady budou rozděleny na základě hodnoty zboží.</li><li>**Objem** – Náklady budou rozděleny na základě objemu zboží. Objem je uveden v hlavním záznamu položky.</li><li>**Hmotnost** – Náklady budou rozděleny na základě hmotnosti zboží. Hmotnost je uvedena v hlavním záznamu položky.</li><li>**Metrika objemu** – Náklady budou rozděleny na základě objemového měření zboží.</li><li><p>**Měření** – Tato možnost umožňuje specifikovat měření v modulu **Náklady za doručení**. Často ho používají organizace, které neznají individuální objem nebo hmotnost zboží, ale které vyžadují přesnější rozdělení, než jaké dovolují možnosti **Částka** a **Množství**. Spedice nebo agent zajistí pro organizaci měření hmotnosti nebo kubických rozměrů buď na úrovni položky, nebo na úrovni nákupní objednávky.</p><p>Například námořní doprava se rovná 900 USD. Položka A má hmotnost 800 kilogramů (kg) a objem 2 krychlové metry (m³). Položka B má hmotnost 100 kilogramů (kg) a objem 1 krychlový metr (m³). Takto vypadají výsledky, když jsou náklady rozděleny podle hmotnosti:</p><ul><li>Položka A = 800 USD</li><li>Položka B = 100 USD</li></ul><p>Takto vypadají výsledky, když jsou náklady rozděleny podle objemu:</p><ul><li>Položka A = 600 USD</li><li>Položka B = 300 USD</li></ul><p>**Poznámka:** Když je pole **Způsob rozdělení** nastaveno na *Měření*, systém používá měření, která jsou zadána jak pro oblast nákladů (přepravní kontejner), tak pro řádky. Tato měření nemusí nutně přičítat údaje k očekávanému součtu. Pokud však požadujete, aby přičítaly údaje k očekávanému celkovému součtu, můžete provést kontrolu pomocí statistiky a zkontrolovat celkové měření. Nastavení výzvy měření a automatická aktualizace měření na úrovni zásilky nebo kontejneru jsou nastaveny v záhlaví cesty.</p></li></ul> |
| **Od data** | Určete začátek rozsahu dat pro výpočet, pokud existuje rozsah dat. Toto datum je první datum, kdy budou použity automatické náklady. |
| **Do data** | Určete konec rozsahu dat pro výpočet, pokud existuje rozsah dat. Toto datum je poslední datum, kdy budou použity automatické náklady. |
| **Kategorie** | <p>Vyberte metodu, která má být použita k výpočtu nákladů. Existují tyto možnosti:</p><ul><li>**Pevné** – Náklady budou rozděleny na základě způsobu rozdělení.</li><li>**Kusy** – Náklady budou rozděleny podle kusů. Způsob rozdělení tedy nebude použit.</li><li>**Procento** – Bude přičteno procento hodnoty zboží. Způsob rozdělení tedy nebude použit.</li><li>**Sazba** – Tuto možnost vyberte, pokud existují rozpisy množství. Pole **Způsob rozdělení** pro řádek musí být nastaveno na *Měření*.</li><ul> |
| **Rozděleno podle množství** | <p>Zaškrtnutím tohoto políčka vytvoříte tlačítko **Množstevní kategorie**, které je dostupné na záložce **Řádky**. Množstevní kategorie umožňují rozčlenit náklady, různé náklady se mohou lišit v závislosti na množství na řádku nákupní objednávky cesty. Tato funkce se často používá, když je zboří dodáváno letecky. Pole **Kategorie** pro řádek musí být nastaveno na *Sazba*.</p><p>Množství se vztahuje k možnosti vybrané v poli **Způsob rozdělení**. Hodnota nákladů bude až do množství, které je zadáno v poli **Hodnota nákladů**.<p>Například množství 45–100 kg vytvoří poplatek 6,00 USD za měření (například kg / m³). Množství překračující 100 kg vytvoří poplatek 5,50 USD za měření (například kg / m³).</p> |
| **Hodnota nákladů** | Zadejte hodnotu nákladů. |
| **Kód měny nákladů** | Vyberte měnu nákladů. |
| **Skupina DPH zboží** | Vyberte kód daně pro náklady. |
| **Minimální náklady** | <p>Toto pole se použije, pouze když je zaškrtnuto políčko **Rozděleno podle množství**. Pokud měření nedosáhne této hodnoty, je vybrána minimální hodnota bez ohledu na náklady, které jsou uvedeny na stránce **Množstevní kategorie**.<p>Například množství 0–45 kg vytvoří poplatek 6 USD za měření (kg / m³). Množství 46–100 kg vytvoří poplatek 5,50 USD za měření (kg / m³). Pokud jsou dodány 2 kg, množstevní kategorie vytvoří hodnotu nákladů 12 USD. Pokud je však pole **Minimální náklady** nastaveno na *100 USD*, konečné náklady budou 100 USD.</p> |
| **Agregovat** | Zaškrtnutím tohoto políčka umožníte uživatelům přesunout tyto náklady z úrovně přepravního kontejneru na úroveň cesty. V tomto případě lze náklady automaticky vypočítat na úrovni přepravního kontejneru. Lze je však také kombinovat a rozdělit mezi všechny položky ve všech kontejnerech na cestě, namísto všech položek v jednotlivých přepravních kontejnerech. |
| **Propojený typ nákladů** | <p>Aktuální řádek s jiným řádkem ve stejném záznamu automatických nákladů propojíte zadáním hodnoty **Kód typu nákladů** řádku, na který chcete odkazovat. Tato funkce je k dispozici, pouze když je pole **Kategorie** pro aktuální řádek nastaveno na *Procento*. Když je aktuální řádek propojen s jiným řádkem, budou náklady aktuálního řádku vycházet z nákladů jiného řádku.</p><p>Například dopravné je 1 000 USD a chcete, aby palivový příplatek činil 10 procent nákladů na dopravu. V tomto případě musí mít řádek nastaveno pole **Kategorie** na *Procento*, pole **Hodnota nákladů** na *10%* a pole **Propojený typ nákladů** na *Dopravné*.</p> |
| **Úprava hodnoty** a **Částka úpravy** | <p>Tato pole slouží k úpravě hodnoty a množství pro různé procentní hodnoty. Jsou k dispozici pouze v případě, kdy je pole **Nákladová oblast** nastaveno na *Položka*.</p><p>Pro různé součásti položky lze nastavit různé náklady. Jedna součást položky může mít jiné procento nákladů než ostatní součásti této položky. Tento přístup je někdy vyžadován k ohodnocení konkrétní části zboží různými sazbami.</p><p>Například clo pro hodinky se počítá ve dvou sazbách: jedna součást hodinek má 10procentní celní sazbu a druhá součást má 2procentní celní sazbu. V tomto případě se náklady rozdělí mezi tyto dvě součásti.</p><p>Náklady se vypočítají pro položku, ale hodnota nákladů se upraví o hodnotu součástí, které mají jinou kategorii nákladů. Náklady na zbývající součásti lze poté vypočítat pomocí částky, o kterou byl upraven předchozí výpočet.</p><p>Například součást A hodinek má cenu 9,50 USD a clo 10 procent, a komponenta B má cenu 0,50 USD a clo 2 procenta. Celkové náklady jsou tedy 10,00 USD. První položka je pro 10procentní řádek. Používá následující hodnoty:</p><ul><li>**Kategorie:** *Procento*</li><li>**Hodnota nákladů:** *10*</li><li>**Upravená hodnota:** *Upravit podle*</li><li>**Upravená hodnota:** *-0,50*</li></ul><p>Toto nastavení určuje, že náklady položky (10 USD) musejí být sníženy o 0,50 USD (cena součásti B), než se vypočítá 10% clo. Proto se na částku 9,50 USD použije 10 procent.</p><p>Druhá položka je pro 2procentní řádek (0,50 USD, o které byla upravena předchozí položka). Používá následující hodnoty:</p><ul><li>**Kategorie:** *Procento*</li><li>**Hodnota nákladů:** *2*</li><li>**Upravená hodnota:** *Použít*</li><li>**Úprava:** *0,50*</li></ul><p>Toto nastavení vypočítá zbývající clo splatné u součásti B.</p> |
