---
title: Vytvoření plánu volna a absence
description: Vytvářejte plány volna v Dynamics 365 Human Resources pro různé typy volna.
author: andreabichsel
manager: AnnBe
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cb42860292c5e3e654917cf2f62b525993aa795a
ms.sourcegitcommit: 1edd3d4642f8fdc801b43b981b7c1a1c36ae0645
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/11/2020
ms.locfileid: "3796490"
---
# <a name="create-a-leave-and-absence-plan"></a>Vytvoření plánu volna a absence

Definujte plány volna a absence v aplikaci Dynamics 365 Human Resources pro každý typ nabízeného volna. Plány volna a absence lze časově rozlišit v různých intervalech, například ročně, měsíčně nebo jednou za čtrnáct dní. Plán lze také definovat jako grant, kde dochází k jednomu časovému rozlišení v konkrétní datum. Můžete například vytvořit plán, který bude každoročně přidělovat pohyblivé svátky.

Plány dovolené v rámci úrovně umožňují zaměstnancům získávat zaměstnanecké výhody na základě množství času stráveného u organizace. Vrstvené plány umožňují automatickou registraci u dalších hodinam zaměstnaneckých výhod.

Můžete určit maximální přenesené částky nebo minimální zůstatky, aby zaměstnanci mohli používat pouze přesčasové hodiny.

Například u vrstveného plánu můžete zaměstnancům poskytnout výhodu 80 hodin od placeného času (PTO) pro nové zaměstnance. Poté můžete udělit 120 hodin za 60 měsíců.

Můžete také vytvářet zaměstnanecké výhody na základě pozice, například pracovní doby zaměstnaneckých výhod.

## <a name="create-a-leave-plan"></a>Vytvoření plánu volna

1. Na stránce **Pracovní volno a absence** klikněte na **Vytvořit nový plán**.

2. V části **Detaily** zadejte **název**, **počáteční datum**, **popis** a **typ pracovního volna** pro váš plán.

Pokud funkce **Konfiguruje více typů pracovního volna pro jedno pracovní volno a plán absencí** povolena, jsou typy pracovního volna konfigurovány v **Plánu časového rozlišení** místo **Podrobností**. Pro každý záznam v tabulce rozvrhu časového rozlišení můžete definovat typ pracovního volna. Kromě toho, když je tato funkce povolená, budete muset použít nové datové entity pro integraci nebo jiné scénáře, kde potřebujete použít entity. 

Nové entity jsou:

- Transakce fondu pracovního volna a absence V2
- Registrace k pracovnímu volnu a absenci V2
- Úroveň plánu pracovního volna a absence V2
- Plán pracovního volna a absence V2
- Žádost o pracovní volno V2

 > [!IMPORTANT]
   > Povolíte-li tuto funkci, nebude ji možné vypnout.

3. Definujte časové rozlišení na kartě **Časová rozlišení**. Časové rozlišení určuje, kdy a jak často je zaměstnanci přiděleno volno. V tomto kroku definujete zásady, podle kterých by měla být zadávána časová rozlišení, a zásady týkající se hodnocení výhod odchodu.

   1. Vyberte hodnotu z rozevíracího seznamu **frekvence časového rozlišení**:

      - Denně
      - Týdně
      - Dvoutýdenní
      - Každých 14 dní
      - Měsíčně
      - Kvartálně
      - Pololetně
      - Ročně
      - Žádní

   2. Výběrem možnosti v rozevíracím seznamu **základ období časového rozlišení** určete počáteční datum použité pro výpočet období časového rozlišení:

      | Základ období časového rozlišení | Popis |
      | --- | --- |
      | **Počáteční datum plánu** | Počáteční datum období časového rozlišení je datem, kdy je plán k dispozici. |
      | **Datum specifické pro zaměstnance** | Počáteční datum období časového rozlišení závisí na události zaměstnance:</br><ul><li>Vlastní (pro každou registraci je nutné zadat základ data časového rozlišení)</li><li>Datum výročí</li><li>Datum původního přijetí</li><li>Datum služebního věku</li><li>Upravené počáteční datum pracovníka</li><li>Počáteční datum pracovníka</li></ul> |

   3. Vyberte možnost z rozevíracího seznamu **Časově rozlišené datum přidělení**:

      - **Datum ukončení období časového rozlišení** – zaměstnanec má přidělen volno k poslednímu dni období odměny. Chcete-li časově rozlišovat správnou částku, musí proces časového rozlišení zahrnovat celé období. Je-li například období časového rozlišení 1. ledna 2020 do 31. ledna 2020, je nutné spustit časové rozlišení pro 1. února, 2020, aby zahrnovalo leden.

      - **Datum zahájení období časového rozlišení** – zaměstnanec bude mít přidělen volno k prvnímu dni období odměny.

   4. Vyberte možnost z rozevíracího seznamu **Zásady časového rozlišení při registraci**: Tato hodnota určuje, jak vypočítat časové rozlišení, když se zaměstnanec zaregistruje uprostřed období časového rozlišení.

      - **Poměrné rozložení** – Rozsah dat mezi datem registrace a datem zahájení slouží k určení rozdílu ve dnech. Tento rozdíl se použije při zpracování časového rozlišení.

      - **Úplné časové rozlišení** – úplná částka založená na vrstvě je udělena během zpracování prvního časového rozlišení.

      - **Žádné časové rozlišení** – není uděleno žádné časové rozlišení až do dalšího období časového rozlišení.

   5. Vyberte možnost z rozevíracího seznamu **Zásady časového rozlišení při zrušení registrace**: Tato hodnota určuje, jak vypočítat časové rozlišení, když zaměstnanec zruší registraci uprostřed období časového rozlišení.

      - **Poměrné rozložení** – Rozsah dat mezi datem registrace a datem zahájení slouží k určení rozdílu ve dnech. Tento rozdíl se použije při zpracování časového rozlišení.

      - **Úplné časové rozlišení** – úplná částka založená na vrstvě je udělena během zpracování prvního časového rozlišení.

      - **Žádné časové rozlišení** – není uděleno žádné časové rozlišení až do dalšího období časového rozlišení.

4. Definujte plán časového rozlišení na kartě **plán časového rozlišení**. Plán časového rozlišení určuje:

   - Jak zaměstnanec provede časové rozlišení
   - Jaké částky bude zaměstnanec časově rozlišovat
   - Jaké částky budou převedeny do dalšího období

   Úrovně lze vytvořit tak, aby bylo volno udělováno podle různých úrovní.

   Pokud máte zaměstnance s hodinovou mzdou mohou přidělit volno na základě odpracovaných hodin, namísto odpracovaných let v organizaci. Data odpracovaných hodin se obvykle ukládají v systému času a docházky. Je možné importovat pravidelné a přesčasové hodiny odpracované ze systému času a docházky a použít je jako základ odměny zaměstnance.
   
    1. Vyberte možnost z rozevíracího seznamu **Typ časového rozlišení**:

      - **Měsíce služby** – založení plánu časového rozlišení na měsících služby.

      - **Odpracované hodiny** – založte časový plán časového rozlišení na odpracovaných hodinách. Další informace o časovém rozlišení odpracovaných hodin naleznete v tématu [časové rozlišení časových údajů na základě odpracovaných hodin](hr-leave-and-absence-plans.md?accrue-time-off-based-on-hours-worked).

      Další informace o časovém rozlišení naleznete v tématu [časové rozlišení časových údajů na základě odpracovaných hodin](hr-leave-and-absence-plans.md?enrollments-and-balances).

    2. Zadejte hodnoty do tabulky plánu časového rozlišení:

      - **Měsíce služby** - minimální počet měsíců, které musí zaměstnanec odpracovat, aby měl nárok na časové rozlišení. Pokud nevyžadujete alespoň minimum, nastavte hodnotu na 0.

      - **Odpracované hodiny** definuje minimální počet hodin, které musí zaměstnanec odpracovat v období časového rozlišení, aby měl nárok na časové rozlišení. Pokud nevyžadujete alespoň minimum, nastavte hodnotu na 0.

      - **Časově rozlišená částka** - počet hodin nebo dnů, které budou zaměstnanci časově rozlišovat za dané období. Období vychází z četnosti časového rozlišení.

      - **Minimální zůstatek** -Zápornou hodnotu lze použít pro minimální zůstatek, pokud mohou zaměstnanci požadovat více dovolené, než mají k dispozici.

      - **Maximální převod do dalšího období** -Proces časového rozlišení upravuje zůstatky dovolené, které překročí maximální zůstatek převedený do dalšího období k výročí počátečního data.

      - **Udělené množství** - Počáteční počet hodin nebo dní, udělených zaměstnancům při jejich prvním přihlášení do plánu dovolených. Částka není časové rozlišení pro každé období časového rozlišení.
      
Pokud je funkce **Konfiguruje více typů pracovního volna pro jedno pracovní volno a plán absencí** povolena, vyberte volbu z **Typu pracovního volna**. 

   > [!IMPORTANT]
   > Povolíte-li tuto funkci, nebude ji možné vypnout.

Pokud povolíte funkci **Použití ekvivalentu plného úvazku**, aplikace Human Resources použije ekvivalent plného úvazku (FTE) definovaný pro pozici k časovému rozlišení zaměstnance. Je-li například FTE ,5 a částka časového rozlišení 10, zaměstnanec provede časové rozlišení 5. Tuto funkci lze použít pouze v případě, že povolíte více typů pracovního volna.  

5. Zvolte **Uložit**.

## <a name="accrue-time-off-based-on-hours-worked"></a>Časové rozlišení volna na základě odpracovaných hodin

Pokud máte zaměstnance s hodinovou mzdou mohou přidělit volno na základě odpracovaných hodin, namísto odpracovaných let v organizaci. Data odpracovaných hodin se obvykle ukládají v systému času a docházky. Je možné importovat pravidelné a přesčasové hodiny odpracované ze systému času a docházky a použít je jako základ odměny zaměstnance.

Při výběru odpracovaných hodin jako typu časového rozlišení můžete použít dva typy hodin, které lze použít pro časové rozlišení: pravidelné a přesčasové. Zpracování časového rozlišení pro plány odpracovaných hodin používají frekvenci časového rozlišení, spolu se základem období časového rozlišení, pro určení hodin, které mají být časově rozlišeny.

### <a name="annual-accrual-frequency"></a>Roční frekvence časového rozlišení

| Datum udělení časového rozlišení    | Úroveň odpracovaných hodin    | Částka časového rozlišení        | Data odpracovaných hodin   | Skutečné hodnoty odpracovaných hodin| Odměna               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31. 12. 2018            | 2080                 | 144                   | 1 1. 2018 - 31. 12. 2018  | 2085                | 144                 |        
| 31. 12. 2018            | 2080                 | 144                   | 1 1. 2018 - 31. 12. 2018  | 2000                | 0                 |


### <a name="monthly-accrual-frequency"></a>Měsíční frekvence časového rozlišení

| Datum udělení časového rozlišení    | Úroveň odpracovaných hodin    | Částka časového rozlišení        | Data odpracovaných hodin   | Skutečné hodnoty odpracovaných hodin| Odměna               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31. 8. 2018             | 160                  | 12                    | 1. 8. 2018 - 31. 8. 2018   | 184                 | 12                  |        
| 31. 8. 2018             | 160                  | 3                     | 1. 8. 2018 - 31. 8. 2018   | 184                 | 3                   |

### <a name="semi-monthly-accrual-frequency"></a>Čtrnáctidenní frekvence časového rozlišení

| Datum udělení časového rozlišení    | Úroveň odpracovaných hodin    | Částka časového rozlišení        | Data odpracovaných hodin   | Skutečné hodnoty odpracovaných hodin| Odměna               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31. 8. 2018             | 80                   | 6                     | 16. 8. 2018 - 31. 8. 2018  | 81                  | 6                  |        
| 31. 8. 2018             | 80                   | 6                     | 16. 8. 2018 - 31. 8. 2018  | 75                  | 0                   |

### <a name="weekly-accrual-frequency"></a>Týdenní frekvence časového rozlišení

| Datum udělení časového rozlišení    | Úroveň odpracovaných hodin    | Částka časového rozlišení        | Data odpracovaných hodin   | Skutečné hodnoty odpracovaných hodin| Odměna               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31. 8. 2018             | 40                   | 3                     | 27. 8. 2018 - 31. 8. 2018  | 42                  | 3                  |        
| 31. 8. 2018             | 40                   | 3                     | 27. 8. 2018 - 31. 8. 2018  | 35                  | 0                   |

### <a name="employee-assigned-leave-plans"></a>Plány pracovního volna přiřazené zaměstnanci

U přiřazených plánů pracovního volna zaměstnance je základ úrovně a typ hodin zobrazený pro plány. U aktivních plánů se pro informaci zobrazí rovněž skutečné odpracované hodiny pro aktivní plány.

### <a name="loading-data"></a>Načítání dat

Skutečné hodiny lze importovat pomocí entity **odpracovaných hodin pracovního volna a absence** ve správě dat. Pokud používáte kalendáře pracovní doby, import ověří, že pravidelné odpracované hodiny nepřekročí naplánované hodiny v den definovaný kalendářem. Import také ověří, že odpracované hodiny pro daný den nepřekročí 24 hodin. 

Pro import skutečných hodin, které mají být použity v procesu časového rozlišení pracovního volna, potřebujete následující informace:

- Číslo pracovníka 
- Datum pracovního dne
- Typ
- Pracovní doba

Jedno datum může mít přidružený pouze jeden z každého typu.

| Číslo pracovníka       | Datum pracovního dne           | Typ                  | Pracovní doba                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 6. 8. 2018             | Pravidelné               | 8                    |       
| 000337                | 7. 8. 2018             | Pravidelné               | 8                    |
| 000337                | 7. 8. 2018             | Přesčas              | 3                    |
| 000337                | 8. 8. 2018             | Pravidelné               | 8                    |
| 000337                | 7. 8. 2018             | Pravidelné               | 8                    |
| 000337                | 9. 8. 2018             | Pravidelné               | 8                    |

## <a name="enrollments-and-balances"></a>Přihlášení a zůstatky

### <a name="enrollment-date"></a>Datum registrace

Datum přihlášení určuje, kdy zaměstnanec může začít s časovým rozlišením volna. Pokud má například zaměstnanec naplánovanou dovolenou od 15. června 2018, nemůže si časově rozdělit volno před 15. červnem 2018.

### <a name="current-balance"></a>Aktuální zůstatek

Aktuální zůstatek je množství dovolené, které je k dispozici pro požadavky na volno. Tato částka zahrnuje časová rozlišení, schválené požadavky a úpravy do aktuálního data.

### <a name="current-balance-examples"></a>Příklady aktuálního zůstatku

#### <a name="annual-plan"></a>Roční plán

**Nastavení plánu**

| Počáteční datum plánu | Datum registrace | Frekvence časového rozlišení | Základ období časového rozlišení | Datum odměny časového rozlišení    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1. 1. 2018        | 1. 1. 2018        | Roční            | Počáteční datum plánu      | Koncové datum období časového rozlišení |

Časové rozlišení jsou zpracována k 1. lednu 2019 (1. 1. 2019), tak, aby bylo zahrnuto celé období.

**Výsledky**

| Částka časového rozlišení | Minimální zůstatek | Maximální převedení do dalšího období | Požadovaná délka | Aktuální zůstatek (k 1. 1.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 200            | 0               | 120                   | 40             | 160                              |

Aktuální zůstatek (160) = časově rozlišená částka (200) – požadovaná délka (40)

#### <a name="semimonthly-plan"></a>Čtrnáctidenní plán

**Nastavení plánu**

| Počáteční datum plánu | Datum registrace | Frekvence časového rozlišení | Základ období časového rozlišení | Datum odměny časového rozlišení    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1. 1. 2018        | 1. 2. 2018        | Každých 14 dní       | Počáteční datum plánu      | Koncové datum období časového rozlišení |

Časové rozlišení jsou zpracována k 1. květnu 2018 (5. 1. 2018), tak, aby bylo zahrnuto celé období.

**Výsledky**

| Částka časového rozlišení | Minimální zůstatek | Maximální převedení do dalšího období | Požadovaná délka | Aktuální zůstatek (k 1. 1.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 22                               |

Aktuální zůstatek (22) = časově rozlišená částka (5 × 6) – požadovaná délka (8)

#### <a name="monthly-plan"></a>Měsíční plán

**Nastavení plánu**

| Počáteční datum plánu | Datum registrace | Frekvence časového rozlišení | Základ období časového rozlišení | Datum odměny časového rozlišení    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1. 1. 2018        | 1. 2. 2018        | Každých 14 dní       | Počáteční datum plánu      | Koncové datum období časového rozlišení |

Časové rozlišení jsou zpracována k 1. květnu 2018 (5. 1. 2018), tak, aby bylo zahrnuto celé období.

**Výsledky**

| Částka časového rozlišení | Minimální zůstatek | Maximální převedení do dalšího období | Požadovaná délka | Aktuální zůstatek (k 1. 1.2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Aktuální zůstatek (7) = časově rozlišená částka (5 × 3) – požadovaná délka (8)

### <a name="forecasted-balance"></a>Předpokládaný zůstatek

*Předpovídaný zůstatek* je délka dovolené dostupná k budoucímu datu. Časové rozlišení a úpravy pro převedení do dalšího období jsou předpovídány do tohoto data.

Aplikace Human Resources používá následující vzorec:

Předpovídaný zůstatek pro pondělí = aktuální zůstatek – Požadavky + časově rozlišené množství – Úprava pro převod do dalšího období

### <a name="forecasted-balance-examples"></a>Příklady předpokládané zůstatku

#### <a name="annual-plan"></a>Roční plán

**Nastavení plánu**

| Počáteční datum plánu | Datum registrace | Frekvence časového rozlišení | Základ období časového rozlišení | Datum odměny časového rozlišení    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1. 1. 2018        | 1. 1. 2018        | Roční            | Počáteční datum plánu      | Koncové datum období časového rozlišení |

Časové rozlišení jsou zpracována k 15. únoru 2019 (2. 15. 2019), tak, aby bylo zahrnuto celé období.

**Výsledky**

| Částka časového rozlišení | Minimální zůstatek | Maximální převedení do dalšího období | Aktuální zůstatek | Předpokládaný zůstatek (k. 15. 2. 2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 20             | 0               | 20                    | 40              | 40                                   |

Předpokládaný zůstatek (40) = časově rozlišené množství (20) + aktuální zůstatek (40) – Úprava pro převod do dalšího období (20)

#### <a name="semimonthly-plan"></a>Čtrnáctidenní plán

**Nastavení plánu**

| Počáteční datum plánu | Datum registrace | Frekvence časového rozlišení | Základ období časového rozlišení | Datum odměny časového rozlišení    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1. 1. 2018        | 1. 2. 2018        | Každých 14 dní       | Počáteční datum plánu      | Koncové datum období časového rozlišení |

Časové rozlišení jsou zpracována k 15. únoru 2019 (2. 15. 2019), tak, aby bylo zahrnuto celé období.

**Výsledky**

| Částka časového rozlišení | Minimální zůstatek | Maximální převedení do dalšího období | Aktuální zůstatek | Předpokládaný zůstatek (k. 15. 2. 2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 5              | 0               | 20                    | 40              | 35                                   |

Předpokládaný zůstatek (35) = časově rozlišené množství (5 × 3) + aktuální zůstatek (40) – Úprava pro převod do dalšího období (20)

#### <a name="monthly-plan"></a>Měsíční plán

**Nastavení plánu**

| Počáteční datum plánu | Datum registrace | Frekvence časového rozlišení | Základ období časového rozlišení | Datum odměny časového rozlišení    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1. 1. 2018        | 1. 2. 2018        | Každých 14 dní       | Počáteční datum plánu      | Koncové datum období časového rozlišení |

Časové rozlišení jsou zpracována k 15. únoru 2019 (2. 15. 2019), tak, aby bylo zahrnuto celé období.

**Výsledky**

| Částka časového rozlišení | Minimální zůstatek | Maximální převedení do dalšího období | Aktuální zůstatek | Předpokládaný zůstatek (k. 15. 2. 2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 10             | 0               | 20                    | 40              | 30                                   |

Předpokládaný zůstatek (30) = časově rozlišené množství (10 × 1) + aktuální zůstatek (40) – Úprava pro převod do dalšího období (20)

### <a name="proration-balance-examples"></a>Příklady poměrně rozděleného zůstatku

#### <a name="prorated-monthly-plan"></a>Poměrně rozdělený měsíční plán

**Nastavení plánu**

| Počáteční datum plánu | Frekvence časového rozlišení | Základ období časového rozlišení |
|-----------------|-------------------|----------------------|
| 1. 1. 2018        | Měsíčně           | Počáteční datum plánu      |

**Výsledky**

| Zaměstnanec            | Počet odpracovaných měsíců | Datum registrace | Datum zahájení | Částka časového rozlišení | Zpracovat časové rozlišení | Rozvaha |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 1. 6. 2018        | 1. 6. 2018   | 1.00           | 1. 9. 2018        | 3,00    |
| Jan Norman          | 0,00              | 15. 6. 2018       | 15. 6. 2018  | 1.00           | 1. 9. 2018        | 2.53    |

#### <a name="full-accrual-monthly-plan"></a>Plně časově rozlišený měsíční plán

**Nastavení plánu**

| Počáteční datum plánu | Frekvence časového rozlišení | Základ období časového rozlišení |
|-----------------|-------------------|----------------------|
| 1. 1. 2018        | Měsíčně           | Počáteční datum plánu      |

**Výsledky**

| Zaměstnanec            | Počet odpracovaných měsíců | Datum registrace | Datum zahájení | Částka časového rozlišení | Zpracovat časové rozlišení | Rozvaha |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 1. 6. 2018        | 1. 6. 2018   | 1.00           | 1. 9. 2018        | 3,00    |
| Jan Norman          | 0,00              | 15. 6. 2018       | 15. 6. 2018  | 1.00           | 1. 9. 2018        | 3,00    |

#### <a name="no-accrual-monthly-plan"></a>Žádný časově rozlišený měsíční plán

**Nastavení plánu**

| Počáteční datum plánu | Frekvence časového rozlišení | Základ období časového rozlišení |
|-----------------|-------------------|----------------------|
| 1. 1. 2018        | Měsíčně           | Počáteční datum plánu      |

**Výsledky**

| Zaměstnanec            | Počet odpracovaných měsíců | Datum registrace | Datum zahájení | Částka časového rozlišení | Zpracovat časové rozlišení | Rozvaha |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 1. 6. 2018        | 1. 6. 2018   | 1.00           | 1. 9. 2018        | 3.00    |
| Jan Norman          | 0,00              | 15. 6. 2018       | 15. 6. 2018  | 1.00           | 1. 9. 2018        | 2.00    |

## <a name="see-also"></a>Viz také

- [Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md)
- [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md)
- [Časové rozlišení plánů pracovního volna a absence](hr-leave-and-absence-accrue.md)
