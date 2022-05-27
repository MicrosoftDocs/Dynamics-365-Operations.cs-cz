---
title: Funkce plánu fakturace
description: Toto téma vysvětluje funkce plánů fakturace, jako jsou metody stanovení cen, eskalace a slevy, data vyrovnání, poměrná část, zpětné účtování a rozdělení skupin položek.
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
ms.openlocfilehash: 0ce323565a94e8e70d90a65b7a3143e984a1c159
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8700717"
---
# <a name="billing-schedule-features"></a>Funkce plánu fakturace

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje funkce plánů fakturace a řádků plánů fakturace. Popisuje různé metody, které se používají pro stanovení cen, jak používat eskalace a slevy a jak stornovat fakturační období. Obsahuje také příklady proporčních výpočtů a rozdělených skupin položek.

## <a name="pricing-methods"></a>Metody stanovení cen

K výpočtu jednotkové ceny položky můžete použít jednu z následujících metod stanovení ceny:

* Plochý
* Standardní
* Úroveň
* Jednotná vrstva

### <a name="flat-pricing"></a>Paušální ceny

Při použití metody paušálního stanovení ceny lze jednotkovou cenu řádkové položky plánu fakturace na stránce **Všechny fakturační plány** upravit na libovolnou hodnotu. Hodnota **Cenová jednotka** je vždy **1**. Proto jsou hodnoty **Jednotková cena** a **Čistá částka** pro položku jsou stejné.

### <a name="standard-pricing-without-a-trade-agreement"></a>Standardní cena (bez obchodní smlouvy)

Když se použije standardní metoda stanovení cen bez obchodní smlouvy, nastavíte jednotkovou cenu pro řádkovou položku plánu fakturace výběrem **Správa informací o produktech** na stránce **Podrobnosti o vydání produktu**. Jednotková cena je uvedena v sekci **Základní prodejní cena**. Počítá se jako *Cena* &divide; *Cenové množství*.

### <a name="standard-pricing-with-a-trade-agreement"></a>Standardní cena (s obchodní smlouvou)

Následující příklady ukazují standardní výpočty cen, pokud existuje obchodní smlouva. Můžete vytvářet obchodní smlouvy na stránce **Podrobnosti o vydání produktu**.

Oba příklady používají položku, která má následující cenové skupiny.

| Množství od | Množství do | U z M | Cena | Cenová jednotka |
|---|---|---|---|---|
| 0 | 100 | Každý | 1.50 | 1 |
| 100 | 200 | Každý | 1.25 | 1 |
| 200 | 999999 | Každý | 1,00 | 1 |

**Příklad 1**

Fakturované množství je 250 a je použit standardní způsob stanovení ceny. Protože je množství v rozmezí cenového množství 200–999 999, jednotková cena je 1,00. 

Čistá částka je vypočtena následujícím způsobem:

*Čistá částka* = (*Množství* &times; *Cena*) &divide; *Cenová jednotka* = (250 &times; 1,00) &divide; 1 = 250

**Příklad 2**

Fakturované množství je 100 a je použit standardní způsob stanovení ceny. Protože je fakturované množství v rozmezí cenového množství 0–100, jednotková cena je 1,50.

> [!NOTE]
> Fakturované množství je v rozsahu 0–100 místo v rozsahu 100–200, protože při standardním chování párování množství se množství shoduje, pokud je *více než nebo rovno* množství "od" a *méně než* množství "do".

Čistá částka je vypočtena následujícím způsobem:

*Čistá částka* = (100 &times; 1.50) &divide; 1 = 150

### <a name="tier-pricing"></a>Cenová hladina

V následujícím příkladu má položka následující cenové skupiny.

| Množství od | Množství do | U z M | Cena | Cenová jednotka |
|---|---|---|---|---|
| 0 | 100 | Každý | 1.50 | 10 |
| 100 | 200 | Každý | 1.25 | 10 |
| 200 | 999999 | Každý | 1,00 | 10 |

Pokud je fakturované množství 250 a je použita metoda cenové hladiny, ceny položek se vypočítají následujícím způsobem na základě cenových hladin:

- **Prvních 100 položek:** 100 &times; 1,50 = 150,00
- **Druhých 100 položek:** 100 &times; 1,25 = 125,00
- **Zbývající položky:** 50 &times; 1,00 = 50,00

Čistá částka je vypočtena následujícím způsobem:

*Čistá částka* = (150,00 &divide; 10) + (125,00 &divide; 10) + (50,00 &divide; 10) = 15,00 + 12,50 + 5,00 = 32,50

Po výpočtu čisté částky se jednotková cena vypočítá vydělením čisté částky množstvím:

*Jedn. cena* = 32,50 &divide; 250 = 0,13

### <a name="flat-tier-pricing"></a>Paušální cenová hladina

V následujícím příkladu má položka následující cenové skupiny.

| Množství od | Množství do | U z M | Částka jednotné vrstvy | Cenová jednotka |
|---|---|---|---|---|
| 0 | 50 | Každý | 100.00 | 50 |
| 50 | 200 | Každý | 150.00 | 200 |

V následující tabulce jsou uvedeny faktury a jednotkové ceny pro různá nakupovaná množství. Nejprve se vypočítá čistá částka a poté se vypočítá jednotková cena.

| Faktura | Množství nakoupené | Jednotková cena | Čistá částka |
|---|---|---|---|
| 1 | 25 | 2,00 &divide; 25 = 0,08 | 100 &divide; 50 = 2,00 |
| 2 | 20 | 2,00 &divide; 20 = 0,10 | 100 &divide; 50 = 2,00 |
| 3 | 50 | 2,00 &divide; 50 = 0,04 | 100 &divide; 50 = 2,00 |
| 4 | 60 | 0,75 &divide; 60 = 0,0125 = 0,01 | 150 &divide; 200 = 0,75 |

## <a name="escalations-and-discounts"></a>Eskalace a slevy

*Eskalace* je zvýšení ceny pro budoucí fakturační období, pro které ještě nebyla vytvořena faktura. *Sleva* je snížení ceny pro budoucí fakturační období, pro které ještě nebyla vytvořena faktura.

Ve fakturaci předplatného nelze eskalace a slevy aplikovat zpětně na plán fakturace. Nemůžete například použít eskalaci na plán fakturace tři měsíce do minulosti a zpracovat jej. Jinými slovy, nemůžete uplatnit zvýšení ceny, ke kterému došlo před třemi měsíci.

Můžete použít eskalaci nebo slevu na plán fakturace nebo řádek plánu fakturace na jednom z následujících míst:

- Stránka se seznamem **Všechny/aktivní plány fakturace**
- Konkrétní plán fakturace
- Řádek konkrétního plánu fakturace

### <a name="apply-an-escalation-or-discount"></a>Použijte eskalaci nebo slevu

Chcete-li použít eskalaci nebo slevu na plán fakturace, postupujte takto.

1. Vyberte plán fakturace nebo řádek plánu fakturace.
2. Vyberte **Eskalace a sleva** buď na kartě **Eskalace a sleva** nebo na řádku plánu fakturace.
3. Pokud se k výpočtu eskalace nebo slevy používá index spotřebitelských cen, vyberte hodnotu v poli **Výpočet indexu spotřebitelských cen**.
4. Vyberte **Nový**, chcete-li přidat eskalační nebo slevový řádek.
5. Pro slevu vyberte zaškrtávací políčko **Sleva**. Pro eskalaci nechte políčko **Sleva** nezaškrtnuté.
6. Nastavte pole **Počáteční datum** a **Frekvence**.
7. U položek odložených, které využívají funkci nevyfakturovaných výnosů, nastavte pole **Koncové datum**.
8. Nastavte pole **Procento**, **Množství** nebo **Harmonogram indexu spotřebitelských cen**.
9. Nastavte pole **Koncové datum**.
10. Vyberte **OK**.
11. Opakujte kroky 4 až 10 pro každou další eskalaci nebo slevu, kterou požadujete.

### <a name="fields-on-the-billing-schedule-lines-page"></a>Pole na stránce Řádky plánu fakturace

Stránka **Řádky plánu fakturace** obsahuje následující pole.

| Pole | Popis |
|---|---|
| Číslo položky | Číslo položky pro řádek plánu fakturace. Toto pole je dostupné pouze v případě, že je stránka otevtená z řádkové položky plánu fakturace. |
| Výpočet indexu spotřebitelských cen | <p>Vyberte metodu, která se používá k výpočtu eskalace indexu spotřebitelských cen:</p><ul><li>**Předchozí index spotřebitelských cen** – Pro výpočet eskalace použijte předchozí hodnotu indexu spotřebitelských cen.</li><li>**Základní index spotřebitelských cen** – Pro výpočet eskalace použijte hodnotu základního indexu spotřebitelských cen.</li></ul> |
| Mřížka **Řádek** | |
| Sleva | <p>Zaškrtnutím políčka určete, zda je změna částky eskalací nebo slevou:</p><ul><li>**Vybraný** – Změna aplikuje slevu na plán fakturace nebo řádek plánu fakturace.</li><li>**Vymazáno** – Změna aplikuje eskalaci na plán fakturace nebo řádek plánu.</li></ul><p>Nastavení tohoto zaškrtávacího políčka nelze změnit u položek, které používají funkci nevyfakturovaných příjmů. Slevy navíc nelze uplatnit na položky, které využívají rozdělení příjmů.</p> |
| Počáteční datum | Vyberte datum zahájení eskalace nebo slevy. |
| Frekvence | Vyberte frekvenci eskalace nebo slevy: **Žádný**, **Měsíční**, **Čtvrtletní**, **Pololetně** nebo **Každoročně**. |
| Procento | Zadejte procento eskalace nebo slevy. |
| Částka | Zadejte částku eskalace nebo slevy. |
| Plán indexu spotřebitelských cen | Vyberte plán indexu spotřebitrelských cen, který se používá k výpočtům. |
| Datum ukončení | <p>Vyberte koncové datum eskalace nebo slevy.</p><p>**Poznámka:** Toto pole je povinné pro položky, které používají funkci nevyfakturovaných příjmů.</p> |
| Číslo plánu odkladu | <p>Číslo plánu odkladu.</p><p>Toto pole je dostupné pouze v případě, že je stránka otevtená z řádku plánu fakturace.</p> |
| Číslo dávky deníku | <p>Číslo dávky deníku.</p><p>Toto pole je dostupné pouze v případě, že je stránka otevtená z řádku plánu fakturace.</p> |
| Částka celkové slevy | <p>Součet částek slev pro všechny řádky v mřížce.</p><p>Toto pole je dostupné pouze v případě, že je stránka otevtená z řádku plánu fakturace.</p> |
| Aktuální částka krátkodobých nevyfakturovaných příjmů | <p>Aktuální částka krátkodobých nevyfakturovaných příjmů.</p><p>Tato částka se objeví, když je zvolena metoda krátkodobého odložení na stránce **Parametry opakované fakturace smlouvy** a účty pro řádkovou položku jsou nastaveny na stránce **Nastavení nevyfakturovaných příjmů**.</p> |
| Aktuální částka dlouhodobých nevyfakturovaných příjmů | <p>Aktuální částka dlouhodobých nevyfakturovaných příjmů.</p><p>Tato částka se objeví, když je zvolena metoda krátkodobého odložení na stránce **Parametry opakované fakturace smlouvy** a účty pro řádkovou položku jsou nastaveny na stránce **Nastavení nevyfakturovaných příjmů**.</p> |

## <a name="proration-examples"></a>Příklady poměrného rozdělenní

Výpočty pro poměrnou část mohou být založeny na počtu dnů nebo počtu měsíců. Metoda, která se používá pro výpočet poměrné části, je nastavena na stránce **Parametry opakované fakturace smlouvy**. Metoda poměrného rozdělení ovlivňuje způsob výpočtu částek pro plán fakturace v následujících situacích:

- Počáteční tvorba
- Použití eskalace nebo slevy
- Ukončení
- Umístění nebo odstranění blokování
- Přidání podpory nebo obnovení

Metoda poměrného rozdělení také ovlivňuje výpočty v přehledu měsíčních opakujících se příjmů (MRR).

### <a name="example-1"></a>Příklad 1

Roční částka fakturačního plánu je 5000 USD. Datum zahájení je 12. srpna 2019 a datum ukončení je 22. prosince 2019. Frekvence fakturace je roční. Poměrná částka se vypočítá následujícím způsobem v závislosti na tom, zda se použije denní nebo měsíční metoda výpočtu:

- **Denně**

    - *Počet dní* = *Datum ukončení* – *Datum zahájení* + 1 = 133 dní
    - *Počet dní v roce* = 11. srpna 2020 – 12. srpna 2019 + 1 = 366 dní
    - *Poměrná částka* = 5 000 &times; (133 &divide; 366) = 1816,94

- **Měsíčně**

    - *Počáteční měsíční část* = (31 – 12 + 1) &divide; 31 = 20 &divide; 31
    - *Prostřední měsíce* = 3
    - *Část konce měsíce* = 22 &divide; 31
    - Poměrná částka = 5000 &divide; 12 &times; \[(20 &divide; 31) + 3 + (22 &divide; 31)\] = 1814,52

### <a name="example-2"></a>Příklad 2

Roční částka fakturačního plánu je 12 000 USD. Datum zahájení je 1. srpna 2019 a datum ukončení je 31. prosince 2019. Frekvence fakturace je roční. Poměrná částka se vypočítá následujícím způsobem v závislosti na metodě výpočtu:

- **Denně**

    - *Počet dní* = *Datum ukončení* – *Datum zahájení* + 1 = 153 dní
    - *Počet dní v roce* = 31. července 2020 – 1. srpna 2019 + 1 = 366 dní
    - *Poměrná částka* = 12 000 &times; (153 &divide; 366) = 5016,39

- **Měsíčně (celý měsíc)**

    - *Počet měsíců* = 5
    - *Celkem měsíců* = 12
    - *Poměrná částka* = (12 000 &times; 5) &divide; 12 = 5 000

## <a name="reversing-a-period-billing"></a>Stornování fakturace za období

V tomto příkladu má plán fakturace pouze jeden řádek:

- Fakturace se provádí měsíčně po dobu 12 měsíců od ledna do prosince.
- Faktury byly vytvořeny za všechna období až do dubna.

Chcete stornovat fakturu za dubnové zúčtovací období.

Pokud ještě nebyla vytvořena prodejní faktura pro dubnové fakturační období, můžete prodejní objednávku odstranit. V tomto případě bude stav **fakturováno** detailu odstraněn. Protože však byla za zúčtovací období vytvořena faktura, stav **Fakturováno** detailu nelze vymazat. Chcete-li tedy stornovat dubnové vyúčtování, musíte pro řádek vytvořit kompenzační dobropis.

1. Na stránce **Všechny plány fakturace** vytvořte řádek fakturace pro tu stejnou položku.
2. Změňte hodnotu **Množství** pro položku na zápornou hodnotu původního množství.
3. Nastavte pole **Frekvence fakturace** na **Jednou**.
4. Aktualizujte počáteční a koncové datum tak, aby odpovídalo datům řádku podrobností fakturace, pro který chcete vytvořit dobropis. V tomto příkladu nastavte datum zahájení na 1. dubna 2019 a datum ukončení na 30. dubna 2019.
5. Uložte změny.
6. Otevřete stránku **Vygenerovat fakturu** a vytvořte prodejní objednávku, která má dobropis pro zadané období.
7. Volitelné: zaúčtujte fakturu.

Když si prohlédnete řádky pro plán fakturace, všimnete si, že nový řádek obsahuje odkaz na dobropis. Původní řádek bude mít stále odkaz na původní dubnovou fakturu.

## <a name="split-item-group-examples"></a>Příklady skupin rozdělených položek

V tomto případě je na místě následující nastavení:

- Na stránce **Parametry opakované fakturace smlouvy** je vybráno **Rozdělit podle skupiny položek** a pole **Jedinečný typ plánu** je nastaveno na **Zákazník**.
- Byly vytvořeny tři skupiny položek: **PREFIX**, **DATAHUB** a **SPP**.
- Zákazník US-001 má několik plánů fakturace, kde je skupina položek PREFIX nebo DATAHUB.
- Zákazník US-002 má několik plánů fakturace, kde je skupina položek PREFIX nebo SPP.

| Číslo plánu fakturace | Zákazník | Sk. položek |
|---|---|---|
| SCH001 | US-001 | PREFIX |
| SCH002 | US-001 | DATAHUB |
| SCH003 | US-002 | PREFIX |
| SCH004 | US-002 | SPP |

Zákazník US-001 zakoupí položku pro obnovení, která patří do skupiny položek PREFIX. Tato transakce je nová prodejní objednávka.

| Číslo prodejní objednávky | Zákazník | Hlavní položka | Položka obnovení | Sk. položek obnovení | Číslo plánu fakturace |
|---|---|---|---|---|---|
| SO0001 | US-001 | D0001 | D0002 | PREFIX | SCH001 |

Když je faktura za prodejní objednávku zaúčtována, položka obnovení je přidána do existujícího plánu fakturace (SCH001) pro zákazníka. Tento plán fakturace používá skupinu položek PREFIX. Všechny položky obnovení, které patří do stejné skupiny položek, jsou zařazeny do stejného rozvrhu fakturace.

**Záhlaví**
 
| Číslo plánu fakturace | Zákazník | Sk. položek |
|---|---|---| 
| SCH001 | US-001 | PREFIX |

**Řádek**

| Číslo plánu fakturace | Zákazník | Sk. položek |
|---|---|---|
| SCH001 | US-001 | D0002 |

Zákazník US-001 nyní zakoupí položku pro obnovení, která patří do skupiny položek SPP. Tato transakce je nová prodejní objednávka.

| Číslo prodejní objednávky | Zákazník | Hlavní položka | Položka obnovení | Sk. položek obnovení | Číslo plánu fakturace |
|---|---|---|---|---|---|
| SO0002 | US-001 | D0003 | D0004 | SPP | |

V současné době zákazník US-001 nemá plán fakturace, který používá skupinu položek SPP. Proto se vytvoří nový rozvrh fakturace.

**Záhlaví**

| Číslo plánu fakturace| Zákazník | Sk. položek |
|---|---|---|
| SCH005 | US-001 | SPP |

**Řádek**

| Číslo plánu fakturace | Zákazník | Sk. položek |
|---|---|---|
| SCH005 | US-001 | D0004 |

### <a name="multiple-billing-schedules-for-the-same-end-user-and-customer"></a>Více rozvrhů fakturace pro stejného koncového uživatele a zákazníka

V tomto případě je na místě následující nastavení:

- Na stránce **Parametry opakované fakturace smlouvy** je vybráno **Rozdělit podle skupiny položek** a pole **Jedinečný typ plánu** je nastaveno na **Koncový uživatel**.
- Na stránce **Koncoví uživatelé** je nastaven následující vztah zákazníka a koncového uživatele.

    | Účet zákazníka | Účet koncového uživatele |
    |---|---|
    | US-001 | US-221 |

Více rozvrhů fakturace se vytvoří pro kombinaci zákazníka a koncového uživatele. Protože je **Rozdělit podle skupiny položek** vybráno na stránce **Parametry opakované fakturace smlouvy**, lze vytvořit více rozvrhů fakturace pro stejný vztah zákazníka a koncového uživatele.

| Číslo plánu fakturace | Zákazník | Účet koncového uživatele | Skupina položek hlavičky |
|---|---|---|---|
| SCH005 | US-001 | US-221 | IG1 |
| SCH006 | US-001 | US-221 | IG2 |
| SCH007 | US-001 | US-221 | IG3 |

Na stránce **Nastavení položky** vytvoříte vztahy mezi položkami podpory a obnovení.

| Kód položky | Vztah položky | Položka podpory | Položka obnovení | Sk. položek obnovení |
|---|---|---|---|---|
| Tabulka | D001 | ITEM27 | D007 | IG1 |
| Tabulka | D002 | ITEM28 | D005 | IG2 |
| Tabulka | D003 | ITEM29 | D006 | IG3 |

Nyní pro odběratele US-001 vytvoříte prodejní objednávku. Tato prodejní objednávka obsahuje položky ze stránky **Nastavení položky**. Když vytvoříte prodejní objednávku, otevřete stránku **Proces podpory a obnovy** a nastavte pole **Účet koncového uživatele** a jakékoli další požadované informace pro položku obnovení.

Když je vytvořena a zaúčtována faktura za transakci, vytvoří se různé fakturační plány pro kombinaci zákazníka/koncového uživatele a skupiny položek. Ke stejnému fakturačnímu plánu lze přiřadit více než jeden řádek stejné prodejní objednávky.

| Číslo prodejní objednávky | Zákazník | Účet koncového uživatele | Hlavní položka | Položka podpory | Položka obnovení | Číslo plánu fakturace |
|---|---|---|---|---|---|---|
| SO0001 | US-001 | US-221 | D001 | ITEM27 | D007 | SCH005 |
| SO0001 | US-001 | US-221 | D002 | ITEM28 | D005 | SCH006 |
| SO0001 | US-001 | US-221 | D003 | ITEM29 | D006 | SCH005 |
