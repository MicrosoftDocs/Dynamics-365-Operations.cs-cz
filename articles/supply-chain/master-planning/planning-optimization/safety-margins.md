---
title: Pojistné doby
description: Toto téma popisuje, jak lze použít pojistné doby s doplňkem optimalizace plánování pro Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 52740246f745272f238ec3dcf8e53f7310e4b24271da4a5d6388a1b9c4706521
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6774842"
---
# <a name="safety-margins"></a>Pojistné doby

[!include [banner](../../includes/banner.md)]

Toto téma popisuje, jak lze použít pojistné doby s doplňkem optimalizace plánování pro Microsoft Dynamics 365 Supply Chain Management.

## <a name="safety-margins-overview"></a>Přehled pojistných dob

Účelem pojistných dob je povolit nastavení, které poskytuje určitou časovou rezervu nad rámec běžné doby realizace. Například když materiál musí být vybalen nebo zkontrolován poté, co dorazí od dodavatele, nemůžete jen tak přidat čas navíc k době realizace nákupu, protože tento přístup poskytne dodavateli další časovou rezervu. V tomto příkladu použijeme rezervu příjmu k zajištění, že dodavatel provede dodávku dříve. Tento přístup poskytuje časovou rezervu, aby bylo možné se zbožím manipulovat interně.

Existují tři typy pojistných dob:

- **Rezerva** – Časová rezerva pro zadání objednávky dodávky
- **Rezerva příjmu** – Časová rezerva pro zpracování příchozí dodávky
- **Rezerva výdeje** – Časová rezerva pro manipulaci se zásilkami

Následující obrázek ukazuje, jak tyto pojistné doby platí v průběhu času.

![Pojistné doby.](media/safety-margins-1.png)

Všechny pojistné doby jsou definovány ve dnech. Výchozí hodnota *0* (nula) označuje, že není použita žádná pojistná doba. Pokud nastavíte více pojistných dob, přidají se všechny k celkovému času od *data objednávky* dodávky po *datum požadavku* poptávky. Například nastavení nemá žádnou dobu realizace a všechny tři typy pojistných dob jsou nastaveny na jeden den. V takovém případě budou mezi datem objednávky dodávky a datem požadavku poptávky tři dny, takže pokud je datum objednávky 1. července, datem požadavku bude 4. července.

### <a name="receipt-margin"></a>Rezerva příjmu

Rezerva příjmu je pravděpodobně nejpoužívanější ze tří pojistných dob. Používá se na *datum doručení* a zpět z *data požadavku*. Jinými slovy, produkty by měly být obdrženy stanovený počet dnů rezervy příjmu před tím, než jsou požadovány.

Následující obrázek znázorňuje rezervu příjmu.

![Rezerva příjmu.](media/safety-margins-2.png)

Rezerva příjmu se obvykle používá jako časová rezerva, aby se zajistil čas pro registraci skladu nebo jiné časově náročné procesy, které nejsou zachyceny jako součást obecné doby realizace v systému. Jednou z výhod pro nákupy je, že *datum doručení* nákupní objednávky se odpovídajícím způsobem posune dopředu. Pokud místo použití rezervy příjmu zvýšíte dobu realizace, bude dodavatel i nadále vyzván k dodání na poslední chvíli.

Všimněte si, že rezerva příjmu nemění *datum požadavku* dodávky. Proto není rezerva příjmu přímo viditelná, když se porovnávají data požadavků na poptávku a nabídku (například na stránce **Čisté požadavky**). Pokud je například rezerva příjmu nastavena na čtyři dny a řádek nákupní objednávky je naplánován pro příjem k patnáctému v měsíci, vypočítá hlavní plánování upravené datum příjmu na devatenáctého v měsíci.

Všimněte si, že rezerva příjmu se nepoužije, když se jako dodávka použijí zásoby na skladě. Předpokládá se, že veškeré zásoby na skladě jsou k dispozici okamžitě bez ohledu na to, kdy byly skutečně přijaty.

### <a name="reorder-margin"></a>Rezerva

> [!NOTE]
> **Již brzy:** Tato funkce zatím není optimalizací plánování podporována. Dokud není podporována, všechny hodnoty, které jsou zadány v poli **Rezerva přidaná k době realizace položky** budou považovány za *0* (nula).

Následující obrázek znázorňuje rezervu.

![Rezerva.](media/safety-margins-3.png)

Rezerva je přidána před dobu realizace položky pro všechny plánované objednávky během hlavního plánování. Proto zajišťuje dodatečný čas pro vystavení objednávky dodávky. Tato pojistná doba se obvykle používá jako časová rezerva k zajištění času pro schvalovací procesy nebo jiné interní procesy, které jsou vyžadovány během vytváření objednávek dodávky. Rezerva se vloží mezi *datum objednávky* nabídky a *počáteční datum*.

### <a name="issue-margin"></a>Rezerva výdeje

> [!NOTE]
> **Již brzy:** Tato funkce zatím není optimalizací plánování podporována. Dokud není podporována, všechny hodnoty, které jsou zadány v poli **Rezerva výdeje odečtená od požadovaného data** budou považovány za *0* (nula).

Následující obrázek znázorňuje rezervu výdeje.

![Rezerva výdeje.](media/safety-margins-4.png)

Rezerva výdeje se odečte od data požadavku poptávky během hlavního plánování. Pomáhá zajistit, abyste měli čas reagovat a odeslat příchozí objednávky nabídky. Tato pojistná doba se obvykle používá jako časová rezerva k zajištění času pro expedici a související odchozí procesy skladu.

Všimněte si, že když se použije rezerva výdeje, neodpovídají související data požadavků nabídky a poptávky. Místo toho se liší o rezervu výdeje, protože rezerva výdeje je přidána mezi *datum požadavku* dodávky a *datum požadavku* poptávky.

## <a name="set-up-safety-margins"></a>Nastavení pojistných dob

### <a name="turn-on-safety-margins-in-feature-management"></a>Zapnutí pojistných dob ve správě funkcí

Než můžete použít tuto funkci s optimalizací plánování, musíte ji zapnout ve svém systému. Správci mohou pomocí pracovního prostoru [Správa funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba. Funkce je zde uvedena následujícím způsobem:

- **Modul:** _Hlavní plánování_
- **Název funkce:** _Pojistné doby pro optimalizaci plánování_

### <a name="define-safety-margins"></a>Definování pojistných dob

Pojistné doby mají flexibilní nastavení. Lze je nastavit jak na *skupinu disponsibility*, tak na *hlavní plán*. Je důležité, abyste pochopili, že pojistné doby jsou přidávány přes sebe. Například rezerva příjmu dvou dnů ve skupině disponsibility a tří dnů v hlavním plánu vytvoří faktickou rezervu příjmu pět dní.

Možnost nastavit pojistnou dobu hlavního plánu může být užitečná, když chcete simulovat delší dobu realizace nebo nejistotu pro konkrétní plán, ale bez ovlivnění denního plánování.

#### <a name="coverage-group-safety-margins"></a>Pojistné doby skupiny disponibility

Chcete-li použít pojistnou dobu na skupinu disponisibility, postupujte takto.

1. Přejděte na **Hlavní plánování \> Nastavení \> Skupiny disponibility**.
1. V podokně seznamu vyberte požadovanou skupinu disponsibility.
1. Na záložce s náhledem **Ostatní** v sekci **Pojistné doby ve dnech** použijte následující pole k nastavení požadovaných pojistných dob (ve dnech):

    - Rezerva příjmu přičtená k požadovanému datu
    - Rezerva výdeje odečtená od požadovaného data
    - Rezerva přidaná k době realizace položky

#### <a name="master-plan-safety-margins"></a>Pojistné doby hlavního plánu

Chcete-li použít pojistnou dobu na hlavní plán, postupujte takto.

1. Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**.
1. V podokně seznamu vyberte požadovaný hlavní plán.
1. Na záložce s náhledem **Pojistné doby ve dnech** použijte následující pole k nastavení požadovaných pojistných dob (ve dnech):

    - Rezerva příjmu přičtená k požadovanému datu
    - Rezerva výdeje odečtená od požadovaného data
    - Rezerva přidaná k době realizace položky

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a>Definování, zda jsou výpočty založeny na kalendářních nebo pracovních dnech

Můžete nastavit všechny pojistné doby tak, aby se počítaly na základě kalendářních nebo pracovních dnů.

1. Přejděte na **Hlavní plánování \> Nastavení \> Parametry hlavního plánování**.
1. Na kartě **Obecné** v sekci **Pojistné doby ve dnech** nastavte možnost **Pracovní dny** na *Ano* pro vypočítání pojistných dob na základě pracovních dnů. Nastavte možnost na *Ne* pro výpočet pojistných dob na základě kalendářních dnů.

Například kalendář je otevřen od pondělí do pátku a uzavřen od soboty do neděle. Pokud existuje pojistná doba v délce jednoho dne, datum požadavku v pondělí vytvoří datum doručení na předchozí pátek, protože sobota a neděle nejsou pracovní dny.

Kalendář, který slouží k určení pracovních dnů, závisí na nastavení a typu dodávky. Lze jej určit pomocí kalendářů skupiny disponsibility, skladu a dodavatele.

> [!NOTE]
> Pokud *sklad* není součástí dimenze disponsibility (jinými slovy, plánování je založeno pouze na *pracovišti*), kalendář skladu se nepoužívá.

Systém dokáže zpracovat nastavení, kde je definován jeden nebo více kalendářů. Následující podsekce popisují možné kombinace, které lze použít k dosažení požadovaného výsledku.

#### <a name="calendar-that-is-used-for-the-duration"></a>Kalendář, který se používá po celou dobu trvání

Definované kalendáře určují skutečnou celkovou dobu realizace v kalendářních dnech, od data objednávky dodávky do data požadavku poptávky. Používá se následující stanovení priorit kalendáře:

- **Doba realizace nákupu** – Zohledňuje se pouze kalendář skupiny disponisibility.
- **Rezerva příjmu** – Používá se kalendář skupiny disponisibility, pokud je definován. V ostatních případech se používá kalendář skladu.
- **Rezerva výdeje** – Používá se kalendář skupiny disponisibility, pokud je definován. V ostatních případech se používá kalendář skladu.
- **Rezerva** – Zohledňuje se pouze kalendář skupiny disponisibility.

#### <a name="calendar-that-is-used-for-the-final-date"></a>Kalendář, který se používá pro konečné datum

Následující pravidla se používají k určení, zda plánovací modul může použít zadané datum pro zadaný typ data:

- **Datum příjmu nákupu** – Použije se kalendář dodavatele, pokud je definován. Jinak se použije kalendář skupiny disponisibility, pokud je definován. Pokud není definován žádný z těchto kalendářů, použije se kalendář skladu.
- **Datum příjmu převodu** – Používá se kalendář skupiny disponisibility, pokud je definován. V ostatních případech se používá kalendář skladu.
- **Datum příjmu výroby** – Používá se kalendář skupiny disponisibility, pokud je definován. V ostatních případech se používá kalendář skladu.
- **Otevřený den problému výdeje** – Používá se kalendář skladu, pokud je definován. Jinak se použije kalendář skupiny disponisibility.
- **Otevřený den objednávky** – Používá se kombinace (průsečík) kalendáře skupiny disponsibility a kalendáře dodavatele. Chcete-li použít dané datum, musí být oba kalendáře otevřené. Pokud je definován pouze jeden z těchto kalendářů, použije se pouze tento kalendář.

#### <a name="calendar-setup-overview-matrix"></a>Matice přehledu nastavení kalendáře

Následující obrázek představuje matici, která shrnuje, které kalendáře se použijí při výpočtu pojistných dob. (Vyberte obrázek a otevřete jeho verzi ve vysokém rozlišení.) Následující zkratky a barvy se používají k označení, kde je specifikován každý typ kalendáře:

- **Skupina disponsibility (CG):** Zelená
- **Sklad (WH):** Žlutá
- **Dodavatel (V):** Modrá

[![Matice přehledu nastavení kalendáře.](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)

## <a name="calculating-delays"></a>Výpočet zpoždění

Všechny tři typy pojistných dob jsou zahrnuty, když systém určuje, zda je objednávka zpožděna.

Například položka má dobu realizace jeden den a rezervu příjmu tři dny. Nákupní objednávka pro tuto položku je nastavena tak, že je dnes vyžadována. V tomto případě se zpoždění počítá jako *doba realizace* + *rezerva příjmu* = čtyři dny. Proto pokud je dnes 14. srpna, čtyři dny zpoždění způsobí doručení 18. srpna. Následující obrázek znázorňuje tento příklad.

![Příklad výpočtu zpoždění.](media/safety-margins-delays.png)

## <a name="additional-resources"></a>Další prostředky

[Začínáme s optimalizací plánování](get-started.md)

[Analýza přizpůsobení pro optimalizaci plánování](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]