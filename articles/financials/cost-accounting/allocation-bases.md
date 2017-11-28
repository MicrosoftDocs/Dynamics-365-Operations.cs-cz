---
title: "Základy přidělení"
description: "Toto téma poskytuje informace o základech přidělení. Základy přidělení jsou klíčové komponenty v nákladovém účetnictví a používají se většinou pro přidělení režijních nákladů."
author: AndersGirke
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 63f39a6c06a0c6b5df901f7aa4235aab3c4ac06e
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="allocation-bases"></a>Základy přidělení 

[!include[banner](../includes/banner.md)]

Základ přidělení je základem, na kterém nákladové účetnictví přiděluje režijní náklady. Základem přidělení může být množství, jako například použité strojohodiny, spotřebované kilowatthodiny (kWh) nebo obsazená plocha. Základy přidělení se většinou používají k přiřazení režijních nákladů do produkovaných zásob. Například IT oddělení přiděluje své výdaje podle počtu počítačů používaných každým oddělením.

Existují tři typy základů přidělení v nákladovém účetnictví:

- Základy přidělení členů předdefinovaných dimenzí
- Základy přidělení hierarchie
- Základy přidělení vzorce

## <a name="predefined-dimension-member-allocation-bases"></a>Základy přidělení členů předdefinovaných dimenzí

Předdefinované základy přidělení člena dimenze jsou vytvářeny automaticky při vytvoření člena dimenze jednoho z následujících typů:

- Členy statistické dimenze
- Členy dimenze prvku nákladů

> [!NOTE]
> Předdefinované základy přidělení člena dimenze založené na členovi dimenze prvku nákladů zvažují pouze hodnoty od poskytovatele zdroje dat, jako je například hlavní kniha nebo rozpočet.

### <a name="example-1-use-a-cost-element-dimension-member-as-the-allocation-base"></a>Příklad 1: Použijte člena dimenze prvku nákladů jako základ přidělení
Tento příklad ukazuje, jak vytvořit pravidlo přidělení nákladů pro přidělení prvku nákladů 10002 (pojištění zaměstnance) k zůstatku zaznamenanému na prvku nákladů 10001 (mzdy). Pravidlo přidělení je definováno na základě poměru platů každého oddělení k celkovým platům. (Je třeba revidovat!).

V hlavní knize je definována účtová osnova následujícím způsobem.

| Účtová osnova | Hlavní účet | popis        | Typ hlavního účtu |
|------------------|--------------|--------------------|-------------------|
| Sdílený           | 10001        | Platy           | Výdaj           |
| Sdílený           | 10002        | Pojištění zaměstnance | Výdaj           |

Definujte dimenzi prvků nákladů a nakonfigurujte datový konektor. Po dokončení importu dat jsou v nákladovém účetnictví vytvořeny následující položky.

**Členy dimenze prvku nákladů**

| Název dimenze prvku nákladů | Prvek nákladů |  popis       | Typ    |
|-----------------------------|--------------|--------------------|---------|
| Prvky nákladů               | 10001        | Platy           | Primární |
| Prvky nákladů               | 10002        | Pojištění zaměstnance | Primární |

**Základy přidělení členů předdefinovaných dimenzí** 

| Jméno  | popis        | Dimenze prvku nákladů |
|-------|--------------------|------------------------|
| 10001 | Platy           | Prvky nákladů          |
| 10002 | Pojištění zaměstnance | Prvky nákladů          |

Do hlavní knihy byly zaúčtovány následující položky:

- Položky, které zobrazují hlavní účet platů, pochází z mzdového systému a jsou zaúčtovány do nákladových středisek.
- Výdaj za pojištění zaměstnance je ručně zaúčtován do výchozího nákladového střediska.

| Datum účtování | Nákladové středisko |  popis        | Hlavní účet |  popis       | Částka v zúčtovací měně |
|-----------------|-------------|---------------------|--------------|--------------------|-------------------------------|
| 01. 03. 2017      | CC001       | HR                  | 10001        | Platy           | 2 000,00                      |
| 01. 03. 2017      | CC002       | FI                  | 10001        | Platy           | 5 000,00                      |
| 01. 03. 2017      | CC003       | IT                  | 10001        | Platy           | 3 000,00                      |
| 01. 03. 2017      | CC099       | Výchozí nákladové středisko | 10002        | Pojištění zaměstnance | 1 000,00                      |

Po zpracování zdrojových dat hlavní knihy jsou v nákladovém účetnictví vytvořeny následující položky.

**Položky nákladů**

| Objekt nákladů |  popis        | Prvek nákladů  |  popis       | Chování nákladů   |Částka|Datum účtování|
|-------------|---------------------|---------------|--------------------|-----------------|------|---------------|
| CC001       | HR                  | 10001         | Platy           | Neklasifikované    |2 000,00|  01. 03. 2017    |
| CC002       | FI                  | 10001         | Platy           | Neklasifikované    |5 000,00|     01. 03. 2017         |
| CC003       | IT                  | 10001         | Platy           | Neklasifikované    |3 000,00|      01. 03. 2017        |
| CC099       | Výchozí nákladové středisko | 10002         | Pojištění zaměstnance | Neklasifikované    |1 000,00|      01. 03. 2017       |

V tomto zjednodušeném příkladu je vytvořeno pravidlo přidělení nákladů pro přidělení prvku nákladů 10002 (pojištění zaměstnance) souvisejícího se zůstatkem zaznamenaným na prvku nákladů 10001 (mzdy).

**Pravidlo distribuce nákladů**

| Uzel hierarchie dimenze objektu nákladů | Uzel hierarchie dimenze prvku nákladů | Chování nákladů | Základ přidělení |
|--------------------------------------|---------------------------------------|---------------|-----------------|
| CC099                                | 10002                                 | Neklasifikované  | 10001           |

**Provést výpočet režijních nákladů**

Poté, co je prvek nákladů 10001 (platy) použit jako základ přidělení, je výsledek výpočtu režijních nákladů následující.

| Objekt nákladů | popis | Hodnota |   Koeficient přidělení         | Částka |
|-------------|-------------|-----------|-----------------------------|--------|
| CC001       | HR          | 2 000     | (2 000 ÷ 10 000) × 1 000 | 200,00 |
| CC002       | FI          | 5 000     | (5 000 ÷ 10 000) × 1 000 | 500.00 |
| CC003       | IT          | 3 000     | (3 000 ÷ 10 000) × 1 000 | 300,00 |

**Deník**

| Deník | Typ deníku                          | Fiskální kalendářní období | Rok | Období   | Verze                                                                 |
|---------|---------------------------------------|------------------------|------|----------|-------------------------------------------------------------------------|
| 00001   | Deník výpočtu distribuce nákladů | Fiskální                 | 2017 | Období 1 | Výpočet režijních nákladů / 01-02-2017 23:51:00: 00 / Hlavní kniha /2017 / Období 1 |

**Položky deníku pro zůstatek objektu nákladů**

| Datum účtování | Objekt nákladů | popis         | Prvek nákladů | popis        | Chování nákladů |  Částka  |
|-----------------|-------------|---------------------|--------------|--------------------|---------------|----------|
| 31. 01. 2017      | CC099       | Výchozí nákladové středisko | 10002        | Pojištění zaměstnance | Neklasifikované  | 1 000,00 |

**Položky nákladů**

| Objekt nákladů |  popis        | Prvek nákladů |    popis     | Chování nákladů | Částka    | Datum účtování |
|-------------|---------------------|--------------|--------------------|---------------|-----------|-----------------|
| CC099       | Výchozí nákladové středisko | 10002        | Pojištění zaměstnance | Neklasifikované  | -1 000,00 | 31. 01. 2017      |
| CC001       | HR                  | 10002        | Pojištění zaměstnance | Neklasifikované  | 200,00    | 31. 01. 2017      |
| CC002       | FI                  | 10002        | Pojištění zaměstnance | Neklasifikované  | 500.00    | 31. 01. 2017      |
| CC099       | IT                  | 10002        | Pojištění zaměstnance | Neklasifikované  | 300,00    | 31. 01. 2017      |

### <a name="example-2-use-a-statistical-dimension-member-as-the-allocation-base"></a>Příklad 2: Použijte člena statistické dimenze prvku nákladů jako základ přidělení

Členy statistické dimenze lze použít jako základ přidělení můžete k definování zásad nebo vykazování nefinanční spotřeby podle objektů nákladů. Můžete ručně vytvořit členy statistické dimenze nebo pomocí nástroje importu/exportu správy dat je importovat ze souboru.

**Členy statistické dimenze**

| Název statistické dimenze | Statistický prvek | popis               | Jednotka |
|----------------------------|---------------------|---------------------------|------|
| Statistické prvky       | FTE                 | Zaměstnanci na plný úvazek       | Ea   |
| Statistické prvky       | Elektrické energie         | Spotřeba elektřiny   | kWh  |

Po uložení člena statistické dimenze se vytvoří odpovídající záznam v předdefinovaném základu přidělení člena dimenze.

**Základy přidělení členů předdefinovaných dimenzí**

| Jméno        | popis             | Statistická dimenze prvku |
|-------------|-------------------------|-------------------------------|
| FTE         | Zaměstnanci na plný úvazek     | Statistické prvky          |
| Elektrické energie | Spotřeba elektřiny | Statistické prvky          |

Statistická měření mohou pocházet z různých zdrojů:

- Spotřebu elektřiny lze měřit podle metrů, instalovaných na různých místech společnosti.
- Tabulky obsahují statistická měření. Například tabulka HcmEmployment obsahuje seznam všech zaměstnanců a nákladových středisek, pro která pracují.

| Jméno       | Nákladové středisko |  popis  | Typ pracovníka |
|------------|-------------|----|-------------|
| Zaměstnanec A | CC001       | HR | Zaměstnanec    |
| Zaměstnanec B | CC002       | FI | Zaměstnanec    |
| Zaměstnanec C | CC002       | FI | Zaměstnanec    |
| Zaměstnanec D | CC003       | IT | Zaměstnanec    |
| Zaměstnanec F | CC003       | IT | Zaměstnanec    |

> [!NOTE]
> Všechny tabulky, které obsahují finanční dimenze, lze použít jako zdroje pro statistická měření.

Nákladové účetnictví podporuje kolekci statistických měření pomocí následujících datových připojení:

- Nástroj importu a exportu správy dat
- Statistická měření

Načtení statistických měření ze systému vyžaduje šablonu poskytovatele statistických měření. Více informací naleznete v části o šabloně poskytovatele statistického měření. (Bude přidán odkaz, jakmile bude téma napsáno.)

**Šablony poskytovatelů statistického měření**

| Jméno  | Funkce | Zdrojová tabulka  | Pole součtu      | Datové pole     |
|-------|----------|---------------|----------------|----------------|
| FTE | Počet    | HcmEmployment | Nelze použít | Nelze použít |

Po zpracování zdrojových dat statistického měření budou v nákladovém účetnictví vytvořeny následující statistické položky.

**Statistické položky**

| Objekt nákladů | popis      | Datum účtování | Člen statistické dimenze | popis         | Hodnota |
|-------------|------------------|-----------------|------------------------------|---------------------|-----------|
| CC001       | HR               | 31. 01. 2017      | FTE                        | Zaměstnanci na plný úvazek | 1.00      |
| CC002       | FI               | 31. 01. 2017      | FTE                        | Zaměstnanci na plný úvazek | 2,00      |
| CC003       | IT               | 31. 01. 2017      | FTE                        | Zaměstnanci na plný úvazek | 2,00      |

Následuje příklad pravidla pro rozdělení nákladů, pokud je v něm jako základ přidělení přiřazen předdefinovaný základ přidělení člena dimenze FTE.

| Objekt nákladů | popis  | Hodnota | Koeficient přidělení |
|-------------|------|-----------|-------------------|
| CC001       | HR   | 1.00      | (1/5) × částka    |
| CC002       | FI   | 2,00      | (2/5) × částka    |
| CC003       | IT   | 2,00      | (2/5) × částka    |

Můžete použít importovanou datovou entitu statistických měření k importu statistických měření do nákladového účetnictví. Můžete také použít nástroj importu a exportu správy dat. V aplikaci Excel je zaznamenána spotřeba elektřiny následujícím způsobem.

| Datum účtování | Člen dimenze | Hodnota | Identifikátor zdroje |
|-----------------|------------------|-----------|-------------------|
| 31. 01. 2017      | CC001            | 2,450.00  | Elektrické energie       |
| 31. 01. 2017      | CC002            | 4,100.00  | Elektrické energie       |
| 31. 01. 2017      | CC003            | 15,000.00 | Elektrické energie       |

Po zpracování zdrojových dat statistického měření budou v nákladovém účetnictví vytvořeny následující statistické položky.

**Statistické položky**

| Objekt nákladů |    | Datum účtování | Člen statistické dimenze |    popis          | Hodnota |
|-------------|----|-----------------|------------------------------|-------------------------|-----------|
| CC001       | HR | 31. 01. 2017      | Elektrické energie                  | Spotřeba elektřiny | 2,450.00  |
| CC002       | FI | 31. 01. 2017      | Elektrické energie                  | Spotřeba elektřiny | 4,100.00  |
| CC003       | IT | 31. 01. 2017      | Elektrické energie                  | Spotřeba elektřiny | 15,000.00 |

Následuje příklad pravidla pro rozdělení nákladů, pokud je v něm jako základ přidělení přiřazen předdefinovaný základ přidělení člena dimenze elektřiny.

| Objekt nákladů | popis  | Hodnota | Koeficient přidělení          |
|-------------|------|-----------|----------------------------|
| CC001       | HR   | 2,450.00  | (2 450 ÷ 21 550) × částka  |
| CC002       | FI   | 4,100.00  | (4 100 ÷ 21 550) × částka  |
| CC003       | IT   | 15,000.00 | (15 000 ÷ 21 550) × částka |

## <a name="hierarchy-allocation-bases"></a>Základy přidělení hierarchie

Nákladoví účetní mohou ručně vytvořit základy přidělení hierarchie použitím uzel hierarchie dimenzí objektů nákladů do existujícího základu přidělení. Tímto způsobem lze omezit rozsah původních předefinovaných základů přidělení členů dimenze. Jeden předefinovaný základ přidělení člena dimenze lze použít k vytvoření několika základů přidělení hierarchie. Rozsahy lze udržovat v hierarchii dimenze objektů nákladů, která je přidružená k základům přidělení hierarchie.

### <a name="example-hierarchy-allocation-bases-that-are-based-on-full-time-employees-in-the-organization"></a>Příklad: Základy přidělení hierarchie, založené na zaměstnancích na plný úvazek v organizaci
Následuje příklad hierarchie dimenzí objektů nákladů, které lze použít k popisu zjednodušené organizace.

| Název hierarchie | Úroveň uzlu 0 | Úroveň uzlu 1 | Úroveň uzlu 2 | Členy dimenze |
|----------------|--------------|--------------|--------------|-------------------|
| Organizace   | Generální ředitelka          | CFO          | FICO         | CC001             |
| Organizace   | Generální ředitelka          | CFO          | HR           | CC002             |
| Organizace   | Generální ředitelka          | CIO          | IT           | CC003             |

Předdefinovaný základ přidělení člena dimenze FTE, vytvořený v předchozím oddílu, obsahuje následující položky.

**Statistické položky**

| Objekt nákladů | popis  | Datum účtování | Člen statistické dimenze | popis | Hodnota |
|-------------|------|-----------------|------------------------------|---------------------|-----------|
| CC001       | HR   | 31. 01. 2017      | FTE                        | Zaměstnanci na plný úvazek | 1.00      |
| CC002       | FI   | 31. 01. 2017      | FTE                        | Zaměstnanci na plný úvazek | 2,00      |
| CC003       | IT   | 31. 01. 2017      | FTE                        | Zaměstnanci na plný úvazek | 2,00      |

Náklady musí být rozděleny mezi nákladová střediska, které jsou podřízena vedoucímu finančního oddělení organizace. Je potvrzeno, že správný poměr přidělení je počet zaměstnanců pracujících na plný úvazek podle nákladového střediska.

**Základy přidělení hierarchie**

| Jméno                  | Základ přidělení | Hierarchie dimenze objektu nákladů | Uzel hierarchie dimenze objektu nákladů |
|-----------------------|-----------------|---------------------------------|--------------------------------------|
| Počet FTE v CFO | FTE           | Organizace                    | CFO                                  |

Funkce náhledu vám umožňuje ověřit základ přidělení hierarchie, který je vytvořen, na základě statistických položek v systému.

**Podrobnosti základu přidělení**

| Objekt nákladů | popis  |  Hodnota |
|-------------|------|------------|
| CC001       | HR   | 1.00       |
| CC002       | FI   | 2,00       |

Následuje příklad pravidla pro rozdělení nákladů, pokud je v něm jako základ přidělení přiřazen předdefinovaný základ přidělení hierarchie počtu FTE v CFO.

| Objekt nákladů | popis  | Hodnota | Koeficient přidělení |
|-------------|------|-----------|-------------------|
| CC001       | HR   | 1.00      | (1/3) × částka    |
| CC002       | FI   | 2,00      | (2/3) × částka    |

## <a name="formula-allocation-bases"></a>Základy přidělení vzorce

Základy přidělení vzorce umožňují definovat rozšířené vzorce k dosažení správného základu přidělení. Základy přidělení vzorce lze vytvořit ručně.

Při vytváření základu přidělení vzorce vyberete, jaká statistická dimenze a dimenze prvků nákladů má být základem pro vzorec. Všechny základy přidělení, které pocházejí z dříve zvolených dimenzí, lze použít v základu přidělení vzorce.

> [!NOTE]
> Dříve definované základy přidělení vzorce lze použít k definování nového základu přidělení vzorce.

V koeficientech základů přidělení vzorce vytvoříte alias, který přidružíte buď k základu přidělení nebo konstantě. Aliasy se poté použijí k definování vzorce.

Chcete-li definovat svůj vzorec, můžete použít následující operátory.

| Symboly | Text           |
|---------|----------------|
| ( )     | Závorky    |
| \<      | Menší než   |
| \>      | Větší než    |
| +       | Dodatek       |
| –       | Odčítání    |
| \*      | Násobení |

Tradiční výkazy **IF** nejsou podporovány. Můžete však vytvořit výkazy a ověřit, zda jsou pravdivé.

| Výkaz | Ověření | Výsledek |
|-----------|------------|--------|
| a \> b    | TRUE       | 1      |
| a \> b    | FALSE      | 0      |

### <a name="example-1-a-simple-formula"></a>Příklad 1: Jednoduchý vzorec

Účet za elektřinu se často skládá ze dvou částí:

- Fixní poplatek za připojení k síti
- Náklady, které jsou spojeny se spotřebou v kWh

Předdefinovaný základ přidělení člena dimenze elektřiny byl již definován a uchovává tyto hodnoty.

**Statistické položky**

| Objekt nákladů | Jméno | Datum účtování | Člen statistické dimenze | popis             | Hodnota |
|-------------|------|-----------------|------------------------------|-------------------------|-----------|
| CC001       | HR   | 31. 01. 2017      | Elektrické energie                  | Spotřeba elektřiny | 2,450.00  |
| CC002       | FI   | 31. 01. 2017      | Elektrické energie                  | Spotřeba elektřiny | 4,100.00  |
| CC003       | IT   | 31. 01. 2017      | Elektrické energie                  | Spotřeba elektřiny | 15,000.00 |

Pokud musí být nyní fixní poplatek rovnoměrně rozložen na objekty nákladů, které spotřebovávají elektřinu, máte k dispozici dvě možnosti pro přidělení nákladů:

- Vytvořte nový předdefinovaný základ přidělení, fixní poplatek za elektřinu, a poté použijte statistické měření 1,00 pro každý objekt nákladů, který spotřebovává elektřinu.
- Vytvořte základ přidělení vzorce, pevný poplatek za elektřinu, který využije výhody předdefinovaného základu přidělení elektřiny, jenž je již v systému definován. Výhodou této možnosti je, že data musí být načtena do nákladového účetnictví pouze pro jednoho člena statistické dimenze elektřiny.

**Základ přidělení vzorce** 

| Jméno              | Dimenze prvku nákladů | Statistická dimenze | Vzorec |
|-------------------|------------------------|-----------------------|---------|
| Fixní poplatek za elektřinu |                        | Statistické prvky  |         |

Než vyplníte pole **Vzorec**, je nutné určit alias, který má být použit ve vzorci.

**Koeficienty základu přidělení vzorce**

| Alias | Konstanta | Základ přidělení |
|-------|----------|-----------------|
| a     |          | Elektrické energie     |
| b     | 0,01     |                 |

Všimněte si, že 0 (nula) není podporována jako konstanta.

**Základ přidělení vzorce**

| Jméno              | Dimenze prvku nákladů | Statistická dimenze | Vzorec |
|-------------------|------------------------|-----------------------|---------|
| Fixní poplatek za elektřinu |                        | Statistické prvky  | a \> b  |

Funkce náhledu vám umožňuje ověřit základ přidělení vzorce, který je vytvořen, na základě statistických položek v systému.

**Podrobnosti základu přidělení**

| Objekt nákladů | popis  | Vzorec           | Hodnota |
|-------------|------|-------------------|-----------|
| CC001       | HR   | 2.450,00 \> 0,01  | 1.00      |
| CC002       | FI   | 4.100,00 \> 0,01  | 1.00      |
| CC003       | IT   | 15.000,00 \> 0,01 | 1.00      |

Následuje příklad pravidla pro rozdělení nákladů, pokud je v něm jako základ přidělení přiřazen základ přidělení vzorce elektřiny.

**Koeficient přidělení velikosti objektů nákladů**

| Objekt nákladů | Jméno | Hodnota |  Koeficient přidělení |
|-------------|------|-----------|--------------------|
| CC001       | HR   | 1.00      | (1/3) × částka     |
| CC002       | FI   | 1.00      | (1/3) × částka     |
| CC003       | IT   | 1.00      | (1/3) × částka     |

### <a name="example-2-an-advanced-formula"></a>Příklad 2: Rozšířený vzorec
V tomto příkladu náklady na elektřinu nemohou pouze odrážet skutečnou spotřebu elektřiny podle kWh. Vedení chce zahrnout motivaci ke snížení spotřeby elektřiny. 

| Pravidlo              | Kurz | 
|-------------------|------|
| a <= 10000 kWh | 0.75 |
| a > 10000 kWh  | 1.15 |

Je vytvořen nový základ přidělení vzorce, spotřeba elektřiny.

**Základ přidělení vzorce**

| Jméno              | Dimenze prvku nákladů | Statistická dimenze | Vzorec |
|-------------------|------------------------|-----------------------|---------|
| Spotřeba elektřiny |                        | Statistické prvky  |         |

Než vyplníte pole **Vzorec**, je nutné určit alias, který má být použit ve vzorci.

**Koeficienty základu přidělení vzorce**

| Alias | Konstanta  | Základ přidělení |
|-------|-----------|-----------------|
| a     |           | Elektrické energie     |
| b     | 10,000.00 |                 |
| K     | 0.75      |                 |
| d     | 1.15      |                 |

**Základ přidělení vzorce**

| Jméno              | Dimenze prvku nákladů | Statistická dimenze | Vzorec                                                    |
|-------------------|------------------------|-----------------------|------------------------------------------------------------|
| Fixní poplatek za elektřinu |                        | Statistické prvky  | ((a \> b) × ((b × c) + (a – b) × d)) + ((a \<= b] × a × c) |

Funkce náhledu vám umožňuje ověřit základ přidělení vzorce, který je vytvořen, na základě statistických položek v systému.

**Podrobnosti základu přidělení**

| Objekt nákladů |    | Vzorec                                                                                                                             | Hodnota |
|-------------|----|-------------------------------------------------------------------------------------------------------------------------------------|-----------|
| CC001       | HR | ((2 450 \> 10 000) × ((10 000 × 0,75) + (2 450 – 10 000) × 1,15)) + ((2 450 \<= 10 000) × 2 450 × 0,75)     | 1,837.50  |
| CC002       | FI | ((4 100 \> 10 000) × ((10 000 × 0,75) + (4 100 – 10 000) × 1,15)) + ((4 100 \<= 10 000) × 4 100 × 0,75)     | 3,075.00  |
| CC003       | IT | ((15 000 \> 10 000) × ((15 000 × 0,75) + (15 000 – 10 000) × 1,15)) + ((15 000 \<= 10 000) × 15 000 × 0,75) | 1,3250.00 |

Podívejme se podrobněji na vzorec pro CC003 (IT):

((15 000 \> 10 000) × ((10 000 × 0,75) + (15 000 – 10 000) × 1,15)) + ((15 000 \<= 10 000) × 15 000 × 0,75) = 13 250

(1 × (7 500 + 5 000 × 1,15)) + (0 × 15 000 × 0,75)            

1 × 7 500 + 5 750 + 0 

Následuje příklad pravidla pro rozdělení nákladů, pokud je v něm jako základ přidělení přiřazen základ přidělení vzorce fixního poplatku za elektřinu.

| Objekt nákladů |  popis  | Hodnota | Koeficient přidělení                |
|-------------|----|-----------|----------------------------------|
| CC001       | HR | 1,837.50  | (1 837,50 ÷ 18 162,50) × částka  |
| CC002       | FI | 3,075.00  | (3 075,00 ÷ 18 162,50) × částka  |
| CC003       | IT | 13,250.00 | (13 250 ÷ 18 162,50) × částka |

