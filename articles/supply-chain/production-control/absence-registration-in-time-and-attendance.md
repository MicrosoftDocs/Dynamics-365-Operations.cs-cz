---
title: Registrace absence v modulu Čas a docházka
description: Toto téma vysvětluje, jak pracovat s registracemi absence v modulu Čas a docházka.
author: johanhoffmann
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JMGParameters, JmgAbsenceCalendar
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a94df9dd706c2540779db70e794e4a0a3f2dd186
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/26/2021
ms.locfileid: "6103015"
---
# <a name="absence-registration-in-time-and-attendance"></a>Registrace absence v modulu Čas a docházka

[!include [banner](../includes/banner.md)]

Toto téma popisuje koncept absence a vysvětluje, jak pracovat s absencí v modulu Čas a docházka.

## <a name="absence-that-is-based-on-regular-work-hours"></a>Absence založená na běžné pracovní době

Pracovníci jsou považováni za nepřítomné za každou hodinu, kterou neodpracovali ve své standardní pracovní době. Běžná pracovní doba je definována ve standardním časovém profilu pracovníka.

Například pracovník pracuje v denním profilu, který má stanovený příchod v 7:00 a odchod v 15:00. Pokud pracovník označí čas příchodu v 9:00, je v tento den považován za nepřítomného od 7:00 do 9:00.

V takovém případě jsou pracovníci vyzváni, aby zadali důvod své absence. Důvod mohou určit zvolením kódu absence.

## <a name="absence-codes"></a>Kódy absencí

Kódy absence definují různé typy absence. Kódy absence určuje společnost.

Na kódy absence lze použít různá pravidla. Například kód absence lze nakonfigurovat tak, aby absenci odečítal ze mzdy nebo naopak neodečítal.

Společnost například definuje kód absence **Opoždění**, který pracovníci použijí, pokud přijdou pozdě a nemají k tomu dostatečný důvod. Společnost též definuje kód absence **Interní kurz**, který pracovníci použijí pro čas strávený docházkou na interní kurzy. Tyto kódy absence lze nastavit tak, že **Opoždění** se odečte od mzdy pracovníka, zatímco **Interní kurz** se z jeho mzdy neodečte.

Můžete nastavit automatické kódy absence. Tyto kódy absence lze použít pro výpočet času pracovníka, když není registrována žádná absence. Časový profil pracovníka určuje, zda se používá kód absence pro standardní pracovní dobu nebo pro pružnou pracovní dobu.

### <a name="set-up-standard-time-and-flex-time"></a>Nastavení standardní a pružné pracovní doby

- Nakonfigurujte parametry pro standardní a pružnou pracovní dobu pomocí možností **Automaticky vložit absenci** a **Automaticky vložit flex--** na stránce **Parametry času a docházky**.

## <a name="absence-groups"></a>Skupiny absencí

Kódy absencí jsou seskupeny do skupin absencí. Skupiny absencí použijete pro seskupení kódů absencí, které mají společné vlastnosti. Příklady zahrnují kódy absencí pro zákonnou absenci nebo absencí z důvodu návštěvy lékaře, účasti u soudu jako porotce nebo nemocného dítěte.

## <a name="planned-absence"></a>Plánovaná absence

Pokud víte, že pracovník bude nepřítomen určitou dobu, například nadcházející dovolená, můžete použít plánovanou absenci. Plánovanou absenci nastavíte pomocí konfigurace kódu absence tak, aby počítal s plánovanou absencí. Při nastavování plánované absence nebudete vyzváni k zadání kódu absence v době absence, když jsou počítány registrace pracovní doby uživatele. Plánovanou absenci lze určit pro jednoho zaměstnance, nebo můžete definovat dávkovou úlohu pro hromadnou aktualizaci plánovaných absencí pro pracovníky.

### <a name="set-up-planned-absence"></a>Nastavení plánované absence

1. Vyberte **Lidské zdroje** &gt; **Pracovníci** &gt; **Zaměstnanci** a vyberte zaměstnance.
2. Vyberte **Pracovní doba** &gt; **Přiřazení pracovní doby** &gt; **Registrace času absence** a nastavte plánovanou absenci.

## <a name="interrupted-planned-absence"></a>Přerušená plánovaná absence

Použijete-li možnost **Přerušit** při nastavování plánované absence, plánovaná absence bude přerušena v případě, že se pracovník dostaví do práce v období plánované absence. Plánovaná absence bude označena jako **Přerušená** a nebude mít žádný vliv na budoucí výpočty.

### <a name="set-up-a-planned-absence-for-interruption"></a>Nastavení plánované absence pro přerušení

1. Otevřete stránku **Registrace času absence**, jak je popsáno v postupu pro nastavení plánované absence.
2. Vyberte **Přerušit**.

Možnost **Přerušit** se použije při registraci času prostřednictvím dílenského terminálu nebo dílenského zařízení. Možnost se nepoužije, když jsou zadány registrace na stránkách výpočtu a schválení, nebo na stránce **Elektronická časová karta**.

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a>Příklady použití absence v profilu pružné pracovní doby

Následující tři příklady ukazují, jak se vypočítávají absence v profilu s pružnou pracovní dobou.

Příklady používají následující profil.

| Označení příchodu | Standardní čas    | Přerušení             | Standardní čas | Flexibilita-        | Označení odchodu | Flexibilita+        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| 8:00     | 9:00 až 11:30 | 11:30 až 12:00 | 12:00 až 15:00 | 15:00 až 16:00 | 16:00      | 16:00 až 18:00 |

### <a name="example-1-signing-out-during-a-flex--period"></a>Příklad 1: Odhlášení během pružné pracovní doby (Flex-)

Pracovník označí čas příchodu v 8:00 a čas odchodu v 15:30. Protože pracovník v tomto případě označí odchod během pružné pracovní doby (Flex-), nevypočítá se žádná absence a od zůstatku pružné pracovní doby pracovníka se odečte půl hodiny.

### <a name="example-2-signing-out-in-during-standard-time-period"></a>Příklad 2: Odhlášení ve standardní pracovní době

Pracovník označí čas příchodu v 8:00 a čas odchodu v 14:30. Protože pracovník v tomto případě označí odchod během standardní pracovní doby, absence se vypočítá z času 14:30 až 16:00 a zaregistruje se doba absence 1,5 hodiny. Je požadován kód absence pro toto období.

### <a name="example-3-signing-out-during-a-flex-period"></a>Příklad 3: Odhlášení během pružné pracovní doby (Flex+)

Pracovník označí čas příchodu v 8:00 a čas odchodu v 16:30. Protože pracovník v tomto případě označí odchod během pružné pracovní doby (Flex+), nevypočítá se žádná absence a do zůstatku pružné pracovní doby se přidá půl hodiny.

## <a name="absence-in-the-calculation-and-approval-process"></a>Absence v procesu výpočtu a schválení

Registrace pracovní doby pracovníka musí být vypočteny a schváleny předtím, než je lze převést do výplatního systému jako položky mzdy.

Schvalovatel může změnit registrace pracovní doby pracovníka. Schvalovatel může dokonce změnit jakoukoliv absenci, kterou pracovník zaregistroval. Pokud schvalovatel ručně zadá časové období, které má kód absence, není pro toto období kód absence přepsán výchozím kódem absence z parametrů modulu Čas a docházka.

Například pracovník označí příchod v 10:00 a vybere kód absence, který označuje, že má zpoždění. Později pracovník informuje svého nadřízeného o tom, že byl u lékaře od 8:00 do 10:00. Návštěva lékaře nesmí způsobit srážku ze mzdy pracovníka. Proto v tomto případě může nadřízený upravit dvě hodiny absence od 8:00 do 10:00 tak, že ručně zadá kód absence, který označuje pro tyto dvě hodiny nemoc.

### <a name="calculate-and-approve-absence"></a>Výpočet a schválení absence

- Vyberte **Čas a docházka** &gt; **Zkontrolovat a schválit** &gt; **Schválit nebo vypočítat**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]