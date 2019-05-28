---
title: Finanční dimenze a zaúčtování
description: Při plánování a nastavení svých účtových osnov musíte zvážit, jak jednotlivé části budou spolupracovat při zaúčtování deníku nebo dokladu. Tyto komponenty zahrnují účetní struktury, rozšířená pravidla a vyrovnávací a pevné dimenze. Toto téma vysvětluje, co jednotlivé komponenty představují a jak pracují dohromady.
author: aprilolson
manager: AnnBe
ms.date: 08/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerChartofAccounts,DimensionDetails
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 89bc6f1f01f77dac4c24419705737783b07e4ac7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554752"
---
# <a name="financial-dimensions-and-posting"></a>Finanční dimenze a zaúčtování 

[!include [banner](../includes/banner.md)]

Při plánování a nastavení svých účtových osnov musíte zvážit, jak jednotlivé části budou spolupracovat při zaúčtování deníku nebo dokladu. Tyto komponenty zahrnují účetní struktury, rozšířená pravidla a vyrovnávací a pevné dimenze. Toto téma vysvětluje, co jednotlivé komponenty představují a jak pracují dohromady.

## <a name="chart-of-accounts-and-financial-dimension-components"></a>Komponenty účetních osnov a finančních dimenzí

Microsoft Dynamics 365 for Finance and Operations má bohatý systém na základě pravidel pro určení platných kombinací hlavních účtů hodnot finančních dimenzí. Tento oddíl poskytuje stručný přehled funkcí jednotlivých komponent a vysvětluje, kde komponenty naleznete.

### <a name="account-structures"></a>Účetní struktury

Když nastavujete svou hlavní knihu, je vyžadována účetní struktura. Je nutné definovat a aktivovat alespoň jednu účetní strukturu a přiřadit ji k hlavní knize. Účetní struktura musí v sobě obsahovat hlavní účet. Můžete definovat pořadí segmentů, které nejlépe vyhovuje vašemu podnikání. Po definování hlavního účtu může systém určit používanou účetní strukturu. Vložením hlavního účtu na začátek nebo do popředí struktury můžete pomoci omezit hodnoty a také systém použije poslední známou platnou hodnotu jako výchozí hodnotu. Můžete mít až 10 dalších finančních dimenzí v účetní struktuře. Účetní struktura definuje, které hodnoty finančních dimenzí jsou platné v kombinaci s jinými hodnotami. Také definuje, zda musí být hodnoty dimenzí zadány.

### <a name="advanced-rules"></a>Rozšířená pravidla

Rozšířená pravidla jsou volitelná součást při nastavení účtových osnov. Do účetní struktury můžete přidat tolik rozšířených pravidel, kolik chcete. Rozšířená pravidla se často používají ke zpracování scénářů, kde je třeba sledovat další finanční dimenze při splnění konkrétních kritérií. Například pokud používáte účet cestovních výdajů, může pro vás být potřebné sledovat další informace, jako je například událost, kvůli které je zaměstnanec na služební cestě. Pokud existuje více rozšířených pravidel, použijí se abecedně podle názvů pravidla. Segmenty, které pravidlo přidává, lze použít až po segmentech účetní struktury.

### <a name="balancing-dimension"></a>Vyrovnávací dimenze

Volitelně můžete definovat vyrovnávací finanční dimenzi. Na stránce **Hlavní kniha** lze definovat finanční dimenzi, která má být vyrovnána. Potom při zaúčtování transakcí do takové finanční dimenze systém automaticky vytvoří a zaúčtuje položky, aby vyrovnal finanční dimenzi.

### <a name="defaultfixed-financial-dimensions-on-the-main-account"></a>Výchozí/pevné finanční dimenze na hlavním účtu

Výchozí dimenze pocházejí z různých míst, jako jsou například hlavní záznamy (například záznamy odběratele nebo dodavatele), záhlaví dokumentů a hlavní účet. Toto téma se zaměřuje na výchozí dimenze na hlavním účtu podle právnické osoby. Můžete definovat, zda má hlavní účet hodnotu **Nestanovena** nebo **Pevná** pro každou finanční dimenzi, která se používá napříč všemi účetními strukturami v hlavní knize. Pokud je finanční dimenze **Nestanovena**, použije se výchozí hodnota, ale tuto hodnotu je možné přepsat. Toto chování se vztahuje na všechny výchozí hodnoty v systému, včetně výchozích hodnot, které pocházejí z hlavních záznamů. Pokud je hodnota finanční dimenze nastavena na hodnotu **Pevná**, bude vždy použita tato hodnota, bez ohledu na to, jestli pochází odněkud jako výchozí hodnota nebo byla zadána uživatelem.

## <a name="order-in-which-default-dimensions-are-applied-during-posting"></a>Pořadí, ve kterém se během zaúčtování používají výchozí dimenze

Uživatelé mají často dotazy ohledně pořadí, ve kterém se různé komponenty spouští. Je velmi důležité, abyste chápali pořadí, ve kterém se výchozí dimenze používají, vzhledem k tomu, že toto chování má vliv na váš přístup k nastavení.

> [!NOTE]
> Tyto informace se vztahují pouze na použití výchozích dimenzí v aplikaci. Pokud importujete data pomocí aplikace Microsoft Excel nebo rozhraní Data Management Framework, chování se liší.

### <a name="example-1"></a>Příklad 1

**Účetní struktura**

| Hlavní účet            | Obchodní jednotka           | Oddělení              | Nákladové středisko             |
|-------------------------|-------------------------|-------------------------|-------------------------|
| Všechny hodnoty jsou povoleny. | Všechny hodnoty jsou povoleny. | Všechny hodnoty jsou povoleny. | Všechny hodnoty jsou povoleny. |

**Hlavní účet**

| Hlavní účet | Jméno          | Právnická osoba | Oddělení                                 |
|--------------|---------------|--------------|--------------------------------------------|
| 401100       | Prodej produktu | USMF         | Pevná – 022 Oddělení prodeje a marketingu |

Následující obrázek znázorňuje pevnou výchozí dimenzi, která je nastavena na hlavním účtu 401100.

[![Výchozí finanční dimenze](./media/default-dimensions.png)](./media/default-dimensions.png)

V tomto velmi základním příkladu zadáme hlavní deník, kde je dimenze oddělení nastavena na použití výchozí hodnoty **023** (Operace). Zadáme a zaúčtujeme účet hlavní knihy. Následující obrázek znázorňuje výchozí finanční dimenze v hlavičce hlavní knihy.

[![Hlavní deníky](./media/general-journal.png)](./media/general-journal.png)

Výchozí dimenze v hlavičce deníku způsobí, že oddělení 023 se použije ve výchozím nastavení na řádku účtu prodeje. Následující obrázek znázorňuje řádek hlavního deníku, kde se použije výchozí hodnota dimenze **023** ze záhlaví.

[![Doklad deníku](./media/journal-voucher.png)](./media/journal-voucher.png)

Nicméně při zaúčtování řádku se použije pevná dimenze a řádek se zaúčtuje do oddělení 022. Následující obrázek znázorňuje zaúčtovaný doklad, kde je použita pevná dimenze pro účet prodeje.

[![Transakce dokladu](./media/voucher-transactions.png)](./media/voucher-transactions.png)

### <a name="example-2"></a>Příklad 2

Tento příklad používá stejné nastavení jako první příklad. Přidáme však druhou komponentu a použijeme dimenzi oddělení jako vyrovnávací dimenzi. Na následujícím obrázku je nastaveno **Oddělení** jako vyrovnávací finanční dimenze pro hlavní knihu USMF.

[![Hlavní kniha](./media/ledger.png)](./media/ledger.png)

Když se použije stejné nastavení hlavičky deníku a zaúčtuje se stejná transakce, použije se nejdříve pevná dimenze. Poté se použije logika vyrovnání, aby se zajistilo, že má každé oddělení vyrovnanou položku. Následující obrázek znázorňuje transakce dokladu, které zahrnují položku vyrovnání po použití pevné dimenze.

[![Transakce dokladu](./media/voucher-transactions2.png)](./media/voucher-transactions2.png)

### <a name="example-3"></a>Příklad 3

V tomto příkladu přidáme rozšířené pravidlo. Rozšířené pravidlo určuje, že pokud se použijí účet prodeje 401100 a oddělení 022 (prodej a marketing), systém má sledovat další segment s názvem Odběratel.

Tento příklad je důležitý z důvodu pořadí. Účetní struktura je určena po zadání hlavního účtu. Pokud odkazujete na nastavení účetní struktury, systém může určit, že hlavní účet, obchodní jednotka, oddělení a nákladové středisko jsou relevantní. V tomto okamžiku nebylo rozšířené pravidlo spuštěno, protože pevné dimenze nejsou použity, dokud nebyly použity výchozí dimenze pro doklad deníku při zaúčtování. Na následujícím obrázku není segment Odběratel přítomen, protože nebyla splněna kritéria pro rozšířené pravidlo.

[![Účet hlavní knihy](./media/drop-down.png)](./media/drop-down.png)

Zaúčtování nebude úspěšné, protože pevná dimenze byla použita na konci procesu. Ověření dimenzí určuje, zda je segment Odběratel vyžadován, pokud je hlavní účet 401100 a oddělení 022. Zaúčtování nelze provést, protože došlo k chybě ověření. Následující obrázek znázorňuje zprávu, která se zobrazí poté, co ověření dimenze určí, že Odběratel je požadovaný segment.

[![Podrobnosti zprávy](./media/message.png)](./media/message.png)

V tomto příkladu musíte přepsat výchozí hodnotu, aby se spustilo rozšířené pravidlo, můžete zadat segment Odběratel. Toto řešení však není možné dispozici vždy a někteří uživatelé dokonce ani neznají pravidla účtování. Proto je důležité pochopit pořadí, ve kterém se výchozích dimenze používají při nastavení účtové osnovy.

Abyste dosáhli v tomto příkladu toho, co požadujete, můžete změnit konfiguraci různými způsoby. Můžete například vytvořit novou účetní strukturu pro účty prodeje a zahrnout segment Odběratel do struktury. Můžete rovněž přidat další řádky do stávající účetní struktury a zadat hlavní účet a hodnoty platného oddělení. Poté pro vás může být užitečné v další odběratelské struktuře mít oddělenou účetní strukturu účtů prodeje, kde je přítomen segment Odběratel.

## <a name="additional-resources"></a>Další zdroje 

Některé z následujících zdrojů se vztahují k předchozí verzi aplikace Finance and Operations. Většina informací o použití výchozích dimenzí a mnoho konceptů je však stejných v předchozí verzi a odkazy jsou stále platné.

[Vyrovnané deníky pro mezijednotkové účetnictví](example-balanced-journals-interunit-accounting.md)

[Plánování účetní osnovy](plan-chart-of-accounts.md) 

[Blog plánování účtové osnovy v aplikaci AX 2012](https://blogs.msdn.microsoft.com/axsa/2014/06/12/planning-your-chart-of-accounts-in-ax-2012-part-1-of-7/) – Tento odkaz se vztahuje na část 1 řady skládající se ze sedmi částí.

[Výchozí nastavení dimenze v rozúčtování](https://blogs.msdn.microsoft.com/ax_gfm_framework_team_blog/2013/12/16/dimension-defaulting-in-accounting-distributions-part-1-introduction/)

[Dimenze výchozí v architektuře dimenzí](https://blogs.msdn.microsoft.com/ax_gfm_framework_team_blog/2014/09/)
