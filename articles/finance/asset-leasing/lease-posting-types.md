---
title: Typy zaúčtování leasingu
description: Toto téma popisuje typy účtování, které se používají pro transakce leasingu aktiv.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 721463000c05eb1774335ccce1af39468c2aed9f179e5e88d8725f4d265d6870
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718240"
---
# <a name="lease-posting-types"></a>Typy zaúčtování leasingu

[!include [banner](../includes/banner.md)]

Toto téma popisuje typy účtování, které se používají pro transakce leasingu aktiv.

## <a name="lease-asset"></a>Aktivum leasingu

Účet je přidružen k používanému majetku (ROU). Z tohoto účtu je odečtena částka, když je leasing původně uznán podle nových účetních standardů leasingu, tématu Kodifikace účetních standardů 842 (ASC 842) a Mezinárodního standardu účetního výkaznictví 16 (IFRS 16). U upraveného leasingu může být z tohoto účtu odečtena nebo připsána částka v závislosti na tom, zda úprava zvyšuje nebo snižuje závazek z leasingu.

**Příklad záznamů v deníku:** Počáteční uznání<br>
**Debet:** leasign majetku XXX<br>
**Kredit:** leasingový závazek XXX

## <a name="lease-liability"></a>Leasingový závazek

Účet je spojen s leasingovým závazkem, ke kterému dochází, když jsou platby diskontovány podle nových standardů IFRS 16 a ASC 842. Tento účet je kreditován, když je leasing od počátku uznán podle nových standardů. Je debetován leasingovými splátkami a kreditován úroky.

**Příklad záznamů v deníku:** Počáteční uznání<br>
**Debet:** leasign majetku XXX<br>
**Kredit:** leasingový závazek XXX

**Příklad záznamů v deníku:** Časové rozlišení úroků<br>
**Debet:** úrokové náklady XXX<br>
**Kredit:** leasingový závazek XXX

**Příklad záznamů v deníku:** Leasingová splátka<br>
**Debet:** leasingový závazek XXX<br>
**Kredit:** závazek dodavatele / leasingová splátka XXX

## <a name="short-term-lease-liability"></a>Krátkodobý leasingový závazek

Účet je spojen s krátkodobým závazkem z leasingu, když je zaúčtován zápis do deníku reklasifikace závazků z krátkodobého pronájmu. Na tento účet se připisuje krátkodobý závazek z amortizačního plánu poslední den v měsíci. Stejná částka je však odečtena první den následujícího měsíce.

**Příklad záznamů v deníku:** reklasifikace krátkodobých leasingových závazků<br>
**Debet:** leasingový závazek XXX<br>
**Kredit:** krátkodobý leasingový závazek XXX<br>
**Debit:** krátkodobý leasingový závazek XXX<br>
**Kredit:** leasingový závazek XXX

## <a name="depreciation-expense"></a>Odpisové výdaje

Účet je spojen s výdajem, který souvisí s odpisy aktiva ROU podle IFRS 16, ASC 842 a finančního leasingu podle IAS 17 a ASC 840. Tento účet je debetován, když je každý měsíc odepisován používaný majetek.

**Příklad záznamů v deníku:** Časové rozlišení odpisů<br>
**Debet:** výdej za odpis XXX<br>
**Kredit:** Akumulovaný odpis XXX

## <a name="gainloss-on-lease-modification"></a>Zisk/ztráta při upravení leasingu

Účet je spojen s jakýmikoli zisky nebo ztrátami, které vzniknou úpravami leasingu. Zisk může vzniknout během úpravy leasingu, pokud tato úprava sníží závazek z leasingu o částku, která přesahuje účetní hodnotu aktiva ROU.

Například leasing má aktuální účetní hodnotu závazku z leasingu ve výši $150 000 a účetní hodnotu aktiva ROU ve výši $100 000. Leasing je upraven a tato úprava vytváří novou současnou hodnotu budoucích minimálních leasingových plateb (PVFMLP) ve výši $ 40 000. Proto bude odpovědnost za leasing stržena společností $110 000 (150 000 $ - $40 000). Protože používaný majetek je pouze $100 000, snížení $110 000 sníží aktivum za 0 (nula). Účetní pokyny proto stanoví, že zbytek by měl být zaúčtován na účet zisků. V tomto případě bude konečným zápisem do deníku debit z leasingové odpovědnosti za $110 000, kredit z leasingového aktiva za $100 000 a kredit na účtu zisku $10 000.

**Příklad záznamů v deníku:** Leasingová úprava<br>
**Debet:** leasingový závazek XXX<br>
**Kredit** leasing majetku XXX<br>
**Kredit:** Zisk XXX

## <a name="accumulated-depreciation"></a>Akumulovaný odpis

Účet je přidružen k protiúčtu majetku používaného majetku. Účet je kreditován při zaúčtování výdaje odpisu.

**Příklad záznamů v deníku:** Časové rozlišení odpisů<br>
**Debet:** výdej za odpis XXX<br>
**Kredit:** Akumulovaný odpis XXX

## <a name="variable-payment"></a>Variabilní splátka

Účet je spojen s variabilními leasingovými splátkami, které vznikají přeceněním indexu podle leasingů dle ASC 842, ASC 840 a IAS 17. V harmonogramu splátek leasingu jsou variabilní splátky zahrnuty ve sloupci **Variabilní splátka**. Z tohoto účtu je odečtena částka, když je faktura vytvořena na řádku plánu splátek, který obsahuje variabilní splátku.

**Příklad záznamů v deníku:** Leasingová splátka<br>
**Debet:** leasingový závazek XXX<br>
**Debet:** Variabilní splátka XXX<br>
**Kredit:** závazek dodavatele / leasingová splátka XXX

## <a name="deferred-rent-asset-liability"></a>Aktivum (pasivum) odložené splátky

Účet je spojen s aktivem nebo pasivem odložené splátky, který je vytvořen odložením splátky leasingu. Z tohoto účtu je odečtena částka, když je faktura zaúčtována proti odložené splátce leasingu, pokud je částka leasingové splátky vyšší než lineární výdaje leasingu za dané období. Je kreditován, pokud je leasingová splátka nižší než lineární výdaje leasingu v daném období.

**Příklad záznamů v deníku:** Leasingová splátka (leasing s odloženými splátkami)<br>
**Debet:** leasingový výdaj XXX<br>
**Kredit:** pasivum odložené splátky XXX<br>
**Kredit:** závazek dodavatele / leasingová splátka XXX

## <a name="lease-expense"></a>Výdaje leasingu

Účet je spojen s náklady na leasing, pokud je leasing klasifikován jako leasing s opožděnými splátkami. Z tohoto účtu je odečtena částka, když je faktura zaúčtována na základě odložené splátky.

**Příklad záznamů v deníku:** Leasingová splátka (leasing s odloženými splátkami)<br>
**Debet:** leasingový výdaj XXX<br>
**Kredit:** pasivum odložené splátky XXX<br>
**Kredit:** závazek dodavatele / leasingová splátka XXX

## <a name="impairment-expense"></a>Výdaje snížení hodnoty

Proti účtu se účtuje, když je snížena hodnota leasingu. Tento účet je debetován, zatímco účet používaného majetku je přímo kreditován.

**Příklad záznamů v deníku:** Leasingová splátka<br>
**Debet:** Výdaj snížení hodnoty XXX<br>
**Kredit:** používaný majetek XXX

## <a name="lease-payment"></a>Leasingová splátka

Proti účtu se provede účetní zápis, pokud je vypnutý parametr **Platba dodavateli**. Tento účet je kreditován místo závazku dodavateli, pokud je parametr vypnutý.

**Příklad záznamů v deníku:** Leasingová splátka<br>
**Debet:** leasingový závazek XXX<br>
**Kredit:** Leasingová splátka XXX

## <a name="expense-type-postings"></a>Zaúčtování typu výdajů

Účet, který je vybrán pro každý typ výdajů, je debetován při generování platby pro daný typ výdajů. Například účet určený prontyp výdajů **Pojištění** je debetován, kdykoli je vytvořena položka faktury nebo deníku plateb z rozvrhu zachraňovacích nákladů pro výdaje na pojištění.

**Příklad záznamů v deníku:** platba za pojištění<br>
**Debet:** Účet typu výdajů na pojištění XXX<br>
**Kredit:** Ofsetový účet XXX

> [!NOTE]
> Ofsetový účet je vybrán na úrovni leasingu na řádcích pro plán plateb zachraňovacích nákladů. Tento offsetový účet lze přidružit k dodavateli nebo k účtu hlavní knihy.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
