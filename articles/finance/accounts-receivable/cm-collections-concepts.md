---
title: Klíčové pojmy správy inkasa
description: Tato témata definují klíčové pojmy správy inkasa.
author: mikefalkner
manager: AnnBe
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7d6f49939807102cc6c29bd50674a5e58e2b1b66
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015142"
---
# <a name="collections-management-key-concepts"></a>Klíčové pojmy správy inkasa

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dříve než začnete s nastavením nebo práci s inkasem, měli byste se seznámit s následujícími koncepty:

- Snímky pro sledování splatnosti odběratele obsahují informace o splatném zůstatku v určitém okamžiku.
- Fondy zákazníků kolekce pomáhají v uspořádání vaší práce.
- Inkasní agenti mohou mít své vlastní fondy zákazníků.
- Stránky seznamů umožňují uspořádat odběratele inkasa, aktivity a případy.
- Všechny informace o inkasu odběratele jsou na jedné stránku, která umožňuje provádět další akce.
- Odpuštění, obnovení nebo stornování úroků a poplatků je možné provést v jednom kroku.
- Vytvoření transakcí odpisů je možné provést v jednom kroku.
- Zpracování plateb s nedostatečnými finančními prostředky je možné provést v jednom kroku.

Toto téma popisuje jednotlivé pojmy.

## <a name="customer-aging-snapshots"></a>Snímky sledování splatnosti odběratele 

Snímek sledování splatnosti obsahuje vypočtené splatné zůstatky pro odběratele v konkrétním bodě v čase. Tyto informace se zobrazí na stránce se seznamem **Splatné zůstatky** a **Inkasa**. Před zobrazením informací na stránkách se seznamem inkas (**Splatné zůstatky**, **Inkasní aktivity**a **Inkasní případy**) je nutné vytvořit snímek sledování splatnosti.

Pro každého odběratele má snímek sledování splatnosti záhlaví snímku sledování splatnosti a záznamy podrobností, které odpovídají každému období pro sledování splatnosti v definici období pro sledování splatnosti.

Záhlaví snímku sledování splatnosti obsahuje celkovou splatnou částku, limit úvěru, dodací list, částku, částku prodejní objednávky, počet sporných transakcí a celkovou částku sporných transakcí pro účet odběratele. Všechny transakce odběratele jsou zahrnuty do výpočtu těchto množství. Celková splatná částka, limit úvěru, částka dodacího listu a částka prodejní objednávky jsou zobrazeny v okně s fakty **Informace o úvěru** na stránce **Inkasa**.

Pro každé období sledování splatnosti v definici období pro sledování splatnosti je vytvořen záznam podrobností ve snímku sledování splatnosti. Každý záznam podrobností obsahuje ID období sledování splatnosti a celkovou částku transakcí s daty, která jsou v období pro sledování splatnosti. Transakce jsou přidružené k období pro sledování splatnosti, jako je například 30 dnů po splatnosti. Datum se vztahuje ke **sledování splatnosti**k hodnotě data, které jste zadali při vytváření snímku sledování splatnosti. Tyto informace se zobrazí na stránce se seznamem **Splatné zůstatky** a v okně s fakty **Splatné zůstatky** na stránce **Inkasa**.

## <a name="collections-customer-pools"></a> Fond odběratelů inkasa 

Fondy odběratelů jsou dotazy, které definují skupinu záznamů odběratelů. Tyto seskupené záznamy slouží k zobrazení informací o účtech odběratelů, které jsou zahrnuty, a ke správě inkas nebo procesů sledování splatnosti pro tato inkasa. Fondy odběratelů lze použít k filtrování informací na stránkách se seznamem inkas. Slouží také k filtrování účtů odběratele, které budou zahrnuty při vytváření snímků pro sledování splatnosti.

## <a name="collections-agents"></a>Inkasní agenti

Standardně uživatelé aplikace mohou zobrazit všechny informace o odběratelích na stránkách se seznamem inkas. Záznamy inkasního agenta vám umožňují určit fondy odběratelů, s jejichž pomocí lze filtrovat informace na stránkách se seznamem inkas a na stránce **Inkasa**.

Inkasní agenti pracují s odběrateli a zajišťují včasné inkasování plateb. Jedná se o pracovníky, kteří jsou přiřazeni k uživatelům na stránce **Nastavení uživatelů**.

## <a name="collections-list-pages"></a> Stránky se seznamem inkasa 

Následující stránky se seznamem umožňují uspořádání informací o inkasu:

- **Splatné zůstatky** – Sloupce na této stránce se seznamem zobrazují zůstatky odběratelů a splatné částky podle období pro sledování splatnosti. Tyto informace jsou uloženy na snímku sledování splatnosti. Období pro sledování splatnosti je určeno podle použité definice období pro sledování splatnosti. Definice období pro sledování splatnosti je převzata z fondu odběratelů, pokud byl zadán v dotazu fondu. Pokud fond nemá definici období pro sledování splatnosti, použije se výchozí definice období pro sledování splatnosti určená na stránce **Parametry pohledávek**. Pokud není určena žádná výchozí definice období pro sledování splatnosti, použije se první definice období pro sledování splatnosti na stránce **Definice období pro sledování splatnosti**.
- **Inkasní aktivity** – Sloupce na této stránce se seznamem zobrazují aktivity, které jsou označeny jako inkasní aktivity. Tyto aktivity se vytvoří na stránce **Inkasa**. Aktivity slouží ke sledování vámi prováděné práce související s inkasem.
- **Případy inkasa** – Sloupce na této stránce se seznamem zobrazují informace o případech, které náleží do kategorie s typem případu **Inkasa**.

### <a name="aging-snapshots"></a>Snímky sledování splatnosti

Snímek sledování splatnosti musí být vytvořen dříve, než je možné zobrazit informace na stránkách se seznamem inkas. Zobrazí se informace pouze pro odběratele, pro které byl vytvořen snímek sledování splatnosti. Záznamy, které se zobrazí na stránce se seznamem, lze dále filtrovat níže popsaným způsobem:

- Podle výchozího nastavení mají uživatelé přístup ke všem odběratelům, kteří mají snímek sledování splatnosti.
- Existují-li fondy odběratelů, uživatel musí být nastaven jako inkasní agent, aby mohl použít fondy pro filtrování informací na stránkách se seznamem inkasa. Informace jsou omezeny na odběratele, kteří jsou zahrnuti ve vybraném fondu odběratelů.
- Pokud je uživatel nastaven jako inkasní agent, na stránkách se seznamem inkas jsou dostupné pouze fondy, které jsou vybrány pro daného inkasního agenta. Pokud vyberete možnost **Povolit agentovi zobrazit všechny fondy odběratelů** na stránce **Inkasní agent** pro inkasního agenta, všechny fondy budou k dispozici pro tohoto agenta.

## <a name="collections-page"></a> Inkasní stránka

Na stránce **Inkasa** můžete sledovat, spravovat a reagovat na inkasní informace, aktivity a případy odběratele.

V horní části stránky jsou zobrazeny případy vybraného odběratele, prostřední část zobrazuje transakce odběratele a dolní část zobrazuje aktivity odběratele. Můžete vytvořit případy inkasa a sledovat tak inkasní informace pro jednu nebo více transakcí a aktivit. Informace v horní a dolní části mohou být filtrovány podle případu.

Okna s fakty zobrazují splatné zůstatky a limit úvěru pro vybraného odběratele. Tyto informace jsou uloženy na snímku sledování splatnosti. V případě potřeby můžete aktualizovat snímek sledování splatnosti aktualizovanými informacemi.

Podokno akcí obsahuje tlačítka, která umožňují zobrazení souvisejících informací pro vybraného odběratele, případ, transakci nebo aktivitu. Můžete provést také společné akce, jako například změnit inkasní stav transakce, odeslat e-mail skrze integraci se svým poskytovatelem e-mailu, provést refundaci odběratelů, zpracovat platby NFP nebo odepsat neinkasovatelné zůstatky.

## <a name="waiving-reinstating-or-reversing-interest-and-fees"></a>Odpuštění, obnovení nebo storno úroku a poplatků

Můžete odpustit, obnovit nebo stornovat poplatky a úroky z transakcí, které jsou součástí oznámení úroků. Na záložce **Inkasovat** v podokně Akce na stránce se seznamem **Všichni odběratelé** zvolte **Oznámení úroků**, **Úrok z transakce** nebo **Poplatek**.

Tyto úpravy mají vliv pouze na oznámeních úroků a úroky a poplatky, které tyto obsahují. Informace o tom, jak odepsat všechny poplatky, které dluží odběratel, naleznete v části [Vytváření transakcí odpisů](#creating-write-off-transactions) v tomto tématu.

Další informace lze najít v části Vytvoření kódu úroků s rozsahem a Zpracování úroků.

## <a name="creating-write-off-transactions"></a>Vytváření transakcí odpisů

Nedobytné pohledávky lze odepsat výběrem možnosti **Odepsat** na stránce **Inkasa** a na stránkách se seznamem inkas.

Při odepsání transakcí odběratele budou všechny transakce tohoto odběratele automaticky označeny k vyrovnání. Částka, která je odepsána, závisí na čisté částce označených transakcí. Transakce odpisu je vytvořena v obecném deníku a může obsahovat až tři typy řádků deníku:

- První typ řádku deníku obsahuje položku pro odpis odběratele. Pokud označené transakce obsahují více kombinací kódů měny, dimenzí a profilů zaúčtování, bude vytvořen samostatný řádek deníku pro každou kombinaci.
- Druhý typ řádku deníku obsahuje položku pro odpis hlavní knihy. Pokud označené transakce obsahují více kombinací kódů měny, dimenzí a profilů zaúčtování, bude vytvořen samostatný řádek deníku pro každou kombinaci.
- Třetí typ řádku deníku obsahuje informace o odpisu hlavní knihy pro DPH. Tento řádek deníku je vytvořen pouze, pokud je vybrána možnost **Samostatná DPH** na stránce **Parametry pohledávek**. Pokud označené transakce obsahují více kombinací účtů na vstupu DPH, dimenzí a kódů DPH, bude vytvořen samostatný řádek deníku pro každou kombinaci. Transakce odpisu je vytvořena v měně transakce. Další informace lze najít v části Vytvoření odpisového deníku pro odběratele.

## <a name="process-nsf-payments"></a>Zpracování plateb NSF

Můžete zpracovat platby NFP volbou možnosti **Platba NFP** na stránce **Inkasa**. Zvolením tohoto tlačítka dojde ke zrušení platby. Pokud pro odběratele platí nějaký poplatek NFP, v deníku plateb se vytvoří poplatek za transakci. Výše poplatku závisí na nastavení automatických poplatků. Automatické poplatky, které platí pro platby NFP, jsou určeny podle skupiny poplatků, která je vybrána na stránce **Bankovní účty** pro související bankovní účet.

## <a name="additional-resources"></a>Další zdroje

[Nastavení parametrů správy úvěru odběratelů](./cm-credit-mgmt-setup.md)

[Informace o nastavení správy kreditu odběratelů](./cm-setup-information.md)

[Přidání informací o správě kreditu pro zákazníka](./cm-add-credit-mgmt-information-customer.md)

[Úvěrové skupiny odběratele](./cm-customer-credit-groups.md)

[Úpravy úvěrového limitu odběratele](./cm-credit-limit-adjustments.md)

[Blokování úvěru pro prodejní objednávky](./cm-sales-order-credit-holds.md)

[Periodické úkoly správy úvěru odběratelů](./cm-periodic-tasks.md)
