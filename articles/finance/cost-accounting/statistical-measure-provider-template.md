---
title: Členy statistické dimenze a šablony poskytovatelů statistických měření
description: Toto téma uvádí informace o členech statistické dimenze a šablonách poskytovatelů statistických měření. Členy statistické dimenze lze použít jako základ přidělení v zásadách, jako je distribuce nákladů a přidělení nákladů. Můžete je také používat k vykazování spotřeby nepeněžních nákladů.
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerSourceEntryProvider, CAMStatisticalDimension, CAMAXStatisticalMeasureProviderTemplate, CAMAXStatisticalMeasureProviderConfiguration, CAMStatisticalDimensionMember, CAMDataConnectorStatisticalMeasure, CAMImportedStatisticalMeasure, CAMImportedStatisticalMeasureProviderConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ec8ec7bc7785b1ddec58b78bd14ce164ad1ce032
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441266"
---
# <a name="statistical-dimension-members-and-statistical-measure-provider-templates"></a>Členy statistické dimenze a šablony poskytovatelů statistických měření

[!include [banner](../includes/banner.md)]

Statistické dimenzí a jejich členy se používají pro registraci a kontrole nefinančních položek v nákladovém účetnictví. Členy statistické dimenze lze použít pro dva účely:

- Jako základ pro přidělení v zásadách, jako je distribuce nebo přidělení nákladů
- Pro vykazování nefinanční spotřeby

## <a name="statistical-dimension"></a>Statistická dimenze

Statistická dimenze má jedinečný název a sadu jedinečných členů dimenze. Statistická dimenze je přiřazena ID hlavní knihy nákladového účetnictví. Tento vztah váže všechny odpovídající členy statistické dimenze do hlavní knihy nákladového účetnictví. Proto se všechny statistické položky vytvoří v rámci nákladového účetnictví hlavní knihy.

> [!NOTE]
> Statistická dimenze může být přiřazena více hlavním knihám nákladového účetnictví.

Následuje příklad statistické dimenze.

| Jméno                        | Datový konektor pro členy dimenzí |
|-----------------------------|--------------------------------------|
| Sdílené statistické prvky | Importované členy dimenze           |

Toto je příklad statistické dimenze, která byla přiřazena do hlavní knihy nákladového účetnictví.

| Jméno                  | Zúčtovací měna | Typ směnného kurzu | Fiskální kalendář | Dimenze prvku nákladů | Statistická dimenze       |
|-----------------------|---------------------|--------------------|-----------------|------------------------|-----------------------------|
| Účetnictví na úrovni manažerů | USD                 | Konstantní měna  | Fiskální období   | Sdílené prvky rozpočtových   | Sdílené statistické prvky |

## <a name="statistical-dimension-members"></a>Členy statistické dimenze

Člen statistické dimenze představuje entitu, pro kterou chcete zaregistrovat nefinanční měřítka. Tato měřítka lze použít jako základ přidělení nebo pouze k vykazování nefinančních hodnot.

Členy statistické dimenze lze vytvářet ručně. Případně je možné je importovat ze souboru pomocí nástroje importu a exportu řízení dat.

Člen statistické dimenze se automaticky stane předdefinovaným základem přidělení. Lze ho použít jako základ přidělení v zásadách nebo jako vstup v jiných typech základů přidělení.

Zde je několik příkladů typických členů statistické dimenze.

| Název statistické dimenze  | Statistické prvky | popis             | Jednotka |
|-----------------------------|----------------------|-------------------------|------|
| Sdílené statistické prvky | FTE                  | Zaměstnanci na plný úvazek     | Př.  |
| Sdílené statistické prvky | Elektrické energie          | Spotřeba elektřiny | kWh  |
| Sdílené statistické prvky | CC balení              | Nákladové středisko balení   | Hod |

## <a name="statistical-measure-provider-template"></a>Šablona poskytovatele statistického měření

Statistická měření mohou pocházet z mnoha zdrojů. Dynamics 365 Finance je skvělým zdrojem pro extrahování statistických měřítek. Šablonu poskytovatele statistických měření můžete použít ke snadné konfiguraci statistických měření, která budete extrahovat.

Definice šablony poskytovatele statistických měření je obecná a lze ji opakovaně používat ve více členech statistické dimenze.

> [!NOTE]
> Všechny tabulky, které obsahují finanční dimenze, lze použít jako zdroje pro statistická měření.

**Příklad: Počet zaměstnanců na nákladové středisko**

Počet zaměstnanců na nákladové středisko je statistické měření, který lze použít pro různé účely, které poskytují přehled pro vedoucí:

- Měřítko statistického vykazování podle nákladového střediska
- Základ přidělení pro různé typy výdajů
- Interní nákladové sazby podle nákladového střediska:

    - Náklady podle zaměstnance
    - Výnosy podle zaměstnance

Tabulka HcmEmployment obsahuje seznam všech zaměstnanců v instanci. Tato tabulka je globální. Proto záznamy nesouvisejí s konkrétním ID oblasti dat.

Následuje příklad zaměstnanců v tabulce HcmEmployment.

| Jméno       | Nákladové středisko | popis   | Typ pracovníka |
|------------|-------------|----|-------------|
| Zaměstnanec 1 | CC001       | HR | Zaměstnanec    |
| Zaměstnanec 2 | CC002       | FI | Zaměstnanec    |
| Zaměstnanec 3 | CC002       | FI | Zaměstnanec    |
| Zaměstnanec 4 | CC003       | IT | Zaměstnanec    |
| Zaměstnanec 5 | CC003       | IT | Zaměstnanec    |
| Zaměstnanec 6 | CC002       | FI | Dodavatel  |

Při vytváření záznamu **Šablona zprostředkovatele statistických měření** musíte rozhodnout, kterou funkci použít:

- **Počet** – je převeden počet záznamů na objekt nákladů.
- **Součet** – je převeden součet záznamů na objekt nákladů. (Pole **Součet** a **Datum** jsou povinná.)

## <a name="using-the-count-function"></a>Použití funkce Počet

Například šablonu zprostředkovatele statistických měření lze nastavit následujícím způsobem.

| Jméno  | Funkce | Zdrojová tabulka  | Pole součtu      | Datové pole     |
|-------|----------|---------------|----------------|----------------|
| FTE  | Počet    | HcmEmployment | Nelze použít | Nelze použít |

Můžete také přidat jeden nebo více rozsahů k omezení měření ze zdrojové tabulky.

V tomto příkladu, pokud chcete pouze přidat počet zaměstnanců na plný úvazek (FTE), stačí přidat rozsah do pole **Typ pracovníka**. V poli **Kritéria** vyberte **Zaměstnanec** k omezení výstupního rozsahu následujícím způsobem.

**Rozsahy**

| Zdrojová tabulka  | Pole       | Kritéria |
|---------------|-------------|----------|
| HcmEmployment | Typ pracovníka | Zaměstnanec |

Předtím, než do nákladového účetnictví zadáte statistické hodnoty, je nutné vytvořit vztah mezi šablonou poskytovatele statistických měření a členem statistické dimenze. Tento vztah je vytvořen pro hlavní knihu nákladového účetnictví a verzi. Vztah sestává z konektoru dat a poskytovatele dat. Můžete mít několik datových konektorů a zprostředkovatelů na pro člena statistické dimenze.

> [!NOTE]
> V tomto příkladu vytvoříme vztah pouze pro **skutečnou verzi**.

Při vytváření vztahu přejděte postupně na položky **Hlavní kniha nákladového účetnictví** \> **Skutečná verze** \> **Spravovat** \> **Statistická měření**. V tomto scénáři vyberte datový konektor **Dynamics 365 Finance – Statistická měření**, protože chceme extrahovat data z aplikace Finance.

**Zdroj dat**

| Název        | Datový konektor                                                                     | Člen statistické dimenze |
|-------------|------------------------------------------------------------------------------------|------------------------------|
| FTEs D365FO | Dynamics 365 Finance – Statistická měření | FTE                         |

**Konfigurace poskytovatele dat**

| Název statistické šablony |
|---------------------------|
| FTE                      |

Po zpracování zdrojových dat hlavní knihy pro statistické měření jsou v nákladovém účetnictví vytvořeny následující statistické položky.

**Deník**

| Deník | Typ deníku                       | Fiskální kalendářní období | Rok   |  Období  |  Verze | Datový konektor pro zdrojové položky|
|---------|------------------------------------|------------------------|--------|----------|----------|------------------------------|
| 00001   | Deník převodů statistických položek | Fiskální                 | 2017   | Období 1 | Hlavní kniha USMF | FTE                   |

**Položky deníku převodů statistických položek**

| Datum účtování | Hodnota | Statistický prvek |   popis       | Nákladové středisko |
|-----------------|-----------|---------------------|---------------------|-------------|
| 31. 01. 2017      | 1.00      | FTE                | Zaměstnanci na plný úvazek | CC001       |
| 31. 01. 2017      | 2,00      | FTE                | Zaměstnanci na plný úvazek | CC002       |
| 31. 01. 2017      | 2,00      | FTE                | Zaměstnanci na plný úvazek | CC003       |

**Statistické položky**

| Objekt nákladů |    | Datum účtování | Člen statistické dimenze |  popis        | Hodnota |
|-------------|----|-----------------|------------------------------|---------------------|-----------|
| CC001       | HR | 31. 01. 2017      | FTE                         | Zaměstnanci na plný úvazek | 1.00      |
| CC002       | FI | 31. 01. 2017      | FTE                         | Zaměstnanci na plný úvazek | 2,00      |
| CC003       | IT | 31. 01. 2017      | FTE                         | Zaměstnanci na plný úvazek | 2,00      |

Pokud je předdefinovaný základ přidělení člena dimenze FTE přidružen jako základ přidělení v pravidle distribuce nákladů, náklady budou rozděleny pomocí následujícího faktoru přidělení.

| Objekt nákladů | popis    | Hodnota | Koeficient přidělení |
|-------------|----|-----------|-------------------|
| CC001       | HR | 1.00      | (1/5) × částka    |
| CC002       | FI | 2,00      | (2/5) × částka    |
| CC003       | IT | 2,00      | (2/5) × částka    |

## <a name="using-the-sum-function"></a>Použití funkce Součet

Výrobní nákladové středisko CC010 (balení) je odpovědné za zabalení produktů před jejich odeslání zákazníkům. Přímé mzdové náklady jsou přidány k produktům kusovníku (BOM) a postupu. Nepřímé náklady na spuštění nákladového střediska musí být přiřazeny také vyráběným produktům. Nejlepší statistické měření pro takové přidělení je často počet evidovaných hodin výroby na produkt v daném období.

Tabulka ProdRouteTrans obsahuje všechny transakce výrobní práce na právnickou osobu DataAreadID.

Následuje příklad zaměstnanců v tabulce ProdRouteTrans.

| Odkaz        | Počet | Operace | Typ | Čas  | Fyzické datum | Skupina produktů (finanční dimenze) | Právnická osoba |
|------------------|--------|-----------|------|-------|---------------|-------------------------------------|--------------|
| Výrobní zakázka | P0001  | Balení | Čas | 8,00  | 01. 01. 2017    | Pomerančový džus B2B                    | USMF         |
| Výrobní zakázka | P0001  | Balení | Čas | 8,00  | 01. 02. 2017    | Pomerančový džus B2B                    | USMF         |
| Výrobní zakázka | P0002  | Balení | Čas | 4,00  | 01. 03. 2017    | Spotřebitel pomerančového džusu               | USMF         |
| Výrobní zakázka | P0003  | Balení | Čas | 4,00  | 01. 03. 2017    | Spotřebitel pomerančového džusu               | USMF         |
| Výrobní zakázka | P0004  | Reconst.  | Čas | 10,00 | 01. 03. 2017    | Spotřebitel pomerančového džusu               | USMF         |

Při vytváření záznamu **Šablona zprostředkovatele statistických měření** musíte rozhodnout, kterou funkci použít:

- **Počet** – je převeden počet záznamů na objekt nákladů.
- **Součet** – je převeden součet záznamů na objekt nákladů. (Pole **Součet** a **Datum** jsou povinná.)

Šablonu zprostředkovatele statistických měření lze nastavit následujícím způsobem.

| Jméno    | Funkce | Zdrojová tabulka   | Pole součtu | Datové pole    |
|---------|----------|----------------|-----------|---------------|
| CC balení | Součet      | ProdRouteTrans | Pracovní doba     | Fyzické datum |

Můžete také přidat rozsahy k omezení měření ze zdrojové tabulky.

Pokud v tomto příkladu potřebujete pouze součet hodin, které se vztahují k nákladovému středisku balení CC010, je možné přidat rozsah do pole **Operace**. V poli **Kritéria** vyberte **Balení** k omezení výstupního rozsahu následujícím způsobem.

**Rozsahy**

| Zdrojová tabulka   | Pole     | Kritéria  |
|----------------|-----------|-----------|
| ProdRouteTrans | Operace | Balení |

Předtím, než do nákladového účetnictví zadáte statistické hodnoty, je nutné vytvořit vztah mezi šablonou poskytovatele statistických měření a členem statistické dimenze. Tento vztah je vytvořen pro hlavní knihu nákladového účetnictví a verzi. Vztah sestává z konektoru dat a poskytovatele dat. Můžete mít několik datových konektorů a zprostředkovatelů na pro člena statistické dimenze.

> [!NOTE]
> V tomto příkladu vytvoříme vztah pouze pro **skutečnou verzi**.

Při vytváření vztahu přejděte postupně na položky **Hlavní kniha nákladového účetnictví** \> **Skutečná verze** \> **Spravovat** \> **Statistická měření**. V tomto scénáři vyberte datový konektor **Dynamics 365 Finance – Statistická měření**, protože chceme extrahovat data z aplikace Finance.

**Zdroj dat**

| Název           | Datový konektor                                                                     | Člen statistické dimenze |
|----------------|------------------------------------------------------------------------------------|------------------------------|
| CC balení D365FO | Dynamics 365 Finance – Statistická měření | CC balení                      |

Systém zjistí, že ProdRouteTrans je tabulka, kde každý záznam patří samostatné právnické osobě. Z toho vyplývá, že se zobrazí výzva k výběru právnické osoby, od níž mají být importovány transakce.

**Konfigurace poskytovatele dat**

| Název statistické šablony | Právnická osoba |
|---------------------------|--------------|
| CC balení                   | USMF         |

Po zpracování zdrojových dat pro statistické měření jsou v nákladovém účetnictví vytvořeny následující statistické položky.

**Deník**

| Deník | Typ deníku                     | Fiskální kalendářní období | Rok   | Období | Verze   |   Datový konektor pro zdrojové položky  |
|---------|----------------------------------|------------------------|--------|---------|----------------|---------|
| 00002   | Deník převodů statistických položek | Fiskální               | 2017    | Období 1  | Hlavní kniha USMF | CC balení |

**Položky deníku převodů statistických položek**

| Datum účtování | Hodnota | Statistický prvek |  popis          | Skupina produktů         |
|-----------------|-----------|---------------------|-----------------------|-----------------------|
| 31. 01. 2017      | 16.00     | CC balení             | Nákladové středisko balení | Pomerančový džus B2B      |
| 31. 01. 2017      | 8,00      | CC balení             | Nákladové středisko balení | Spotřebitel pomerančového džusu |

**Statistické položky**

| Objekt nákladů           | Datum účtování | Člen statistické dimenze |    popis        | Hodnota |
|-----------------------|-----------------|------------------------------|-----------------------|-----------|
| Pomerančový džus B2B      | 31. 01. 2017      | CC balení                      | Nákladové středisko balení | 16.00     |
| Spotřebitel pomerančového džusu | 31. 01. 2017      | CC balení                      | Nákladové středisko balení | 8,00      |

Pokud je předdefinovaný základ přidělení člena dimenze CC balení přidružen jako základ přidělení v pravidle distribuce nákladů, náklady budou rozděleny pomocí následujícího faktoru přidělení.

| Objekt nákladů           | Hodnota | Koeficient přidělení  |
|-----------------------|-----------|--------------------|
| Pomerančový džus B2B      | 16.00     | (16 ÷ 24) × částka |
| Spotřebitel pomerančového džusu | 8,00      | (8 ÷ 24) × částka  |

## <a name="imported-statistical-measures"></a>Importovaná statistická měření

Pomocí nástroje pro import/export správy dat můžete importovat statistická měření do nákladového účetnictví.

Datová entita používaná pro import má název Importovaná statistická měření.

> [!NOTE]
> Tato datová entita umožňuje maximálně pět jedinečných hodnot dimenze na položku.

Spotřeba elektrické energie je zaznamenána v aplikaci Microsoft Excel pomocí předdefinovaného formátu datové entity. Následuje příklad.

| Datum účtování | Název 1 člena dimenze | Název 2 člena dimenze | Název 5 člena dimenze | Hodnota  | Identifikátor zdroje |
|-----------------|------------------------|------------------------|------------------------|------------|-------------------|
| 31. 01. 2017      | CC001                  |                        |                        | 2,450.00   | Elektrické energie       |
| 31. 01. 2017      | CC002                  |                        |                        | 4,100.00   | Elektrické energie       |
| 31. 01. 2017      | CC003                  |                        |                        | 15,000.00  | Elektrické energie       |

Po importu dat prostřednictvím správy dat budou data uložena v tabulce Fázování nákladového účetnictví. Z toho vyplývá, že importovaná data lze použít ve více hlavních knihách nákladového účetnictví. Nové načtení dat není požadováno.

Pokud chcete importovat data, přejděte na **Importovaná data** \> **Datová entita** \> **Importovaná statistická měření**.

| Identifikátor zdroje | Datum účtování | Hodnota  | Název 1 člena dimenze | Název 2 člena dimenze | Název 5 člena dimenze |
|-------------------|-----------------|------------|------------------------|------------------------|------------------------|
| Elektrické energie       | 31. 01. 2017      | 2,450.00   | CC001                  |                        |                        |
| Elektrické energie       | 31. 01. 2017      | 4,100.00   | CC002                  |                        |                        |
| Elektrické energie       | 31. 01. 2017      | 15,000.00  | CC003                  |                        |                        |

Předtím, než do nákladového účetnictví zadáte statistické hodnoty, je nutné vytvořit vztah mezi identifikátorem zdroje a členem statistické dimenze. Tento vztah je vytvořen pro hlavní knihu nákladového účetnictví a verzi. Vztah sestává z konektoru dat a poskytovatele dat. Můžete mít několik datových konektorů a zprostředkovatelů na pro člena statistické dimenze.

> [!NOTE]
> V tomto příkladu vytvoříme vztah pouze pro **skutečnou verzi**.

Při vytváření vztahu přejděte postupně na položky **Hlavní kniha nákladového účetnictví** \> **Skutečná verze** \> **Spravovat** \> **Statistická měření**. Pro tento scénář vyberte datový konektor **Importovaná statistická měření**, protože data byla importována ze systému třetí strany do nákladového účetnictví z aplikace Excel.

**Zdroj dat**

| Jméno        | Datový konektor                | Člen statistické dimenze |
|-------------|-------------------------------|------------------------------|
| Elektrické energie | Importovaná statistická měření | Elektrické energie                  |

**Konfigurace poskytovatele dat**

| Importovat identifikátor zdroje | Funkce | Dimenze 1   | Dimenze 2 | Dimenze 5 |
|--------------------------|----------|--------------|------------|------------|
| Elektrické energie              | Součet      | Nákladová střediska |            |            |

> [!NOTE]
> Při definování konfigurace poskytovatele dat je nutné určit, které dimenze objektu nákladů porovnat s importovanými transakcemi. Po zpracování zdrojových dat hlavní knihy pro statistické měření jsou v nákladovém účetnictví vytvořeny následující statistické položky.

**Deník**

| Deník | Typ deníku                       | Fiskální kalendářní období | Rok  | Období  |Verze      |Datový konektor pro zdrojové položky |
|---------|------------------------------------|------------------------|-------|--------|---------------|-------------|
| 00002   | Deník převodů statistických položek | Fiskální                 | 2017  | Období 1 | Hlavní kniha USMF | Elektrické energie |

**Položky deníku převodů statistických položek**

| Datum účtování | Hodnota  | Prvek nákladů |   popis           | Nákladové středisko |
|-----------------|------------|--------------|-------------------------|-------------|
| 31. 01. 2017      | 2,450.00   | Elektrické energie  | Spotřeba elektřiny | CC001       |
| 31. 01. 2017      | 4,100.00   | Elektrické energie  | Spotřeba elektřiny | CC002       |
| 31. 01. 2017      | 15,000.00  | Elektrické energie  | Spotřeba elektřiny | CC003       |

**Statistické položky**

| Objekt nákladů |    | Datum účtování | Člen statistické dimenze |      popis                   | Hodnota  |
|-------------|----|-----------------|------------------------------|-------------------------|------------|
| CC001       | HR | 31. 01. 2017      | Elektrické energie                  | Spotřeba elektřiny | 2,450.00   |
| CC002       | FI | 31. 01. 2017      | Elektrické energie                  | Spotřeba elektřiny | 4,100.00   |
| CC003       | IT | 31. 01. 2017      | Elektrické energie                  | Spotřeba elektřiny | 15,000.00  |

Pokud je předdefinovaný základ přidělení člena dimenze Elektřina přidružen jako základ přidělení v pravidle distribuce nákladů, náklady budou rozděleny pomocí následujícího faktoru přidělení.

| Objekt nákladů |    | Hodnota | Koeficient přidělení          |
|-------------|----|-----------|----------------------------|
| CC001       | HR | 2,450.00  | (2 450 ÷ 21 550) × částka  |
| CC002       | FI | 4,100.00  | (4 100 ÷ 21 550) × částka  |
| CC003       | IT | 15,000.00 | (15 000 ÷ 21 550) × částka |

## <a name="additional-resources"></a>Další zdroje

[Základy přidělení](allocation-bases.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]