---
title: Nastavení parametrů správy úvěru
description: V tomto článku jsou popsány možnosti, které lze použít ke konfiguraci správy úvěru, tak aby byly splněny požadavky vašeho podniku.
author: JodiChristiansen
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2ac5e0ba8c9279fc5f04a80d4444b11850e72d3c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876347"
---
# <a name="credit-management-parameters-setup"></a>Nastavení parametrů správy úvěru

[!include [banner](../includes/banner.md)]

V tomto článku jsou popsány možnosti, které lze použít ke konfiguraci správy úvěru, tak aby byly splněny požadavky vašeho podniku. Chcete-li používat funkce správy úvěru, nastavte parametry na stránce **Parametry úvěrů a inkas** (**Úvěry a inkasa \> Nastavení \> Parametry úvěrů a inkas**).

## <a name="credit-parameters"></a>Parametry úvěru

Existují čtyři pevné záložky v sekci **Úvěry**, na kterých můžete měnit parametry, jež řídí správu úvěru: **Blokování úvěru**, **Kontrolní bod správy úvěru**, **CStatistika správy úvěru** a **Limity úvěru**. Následující části popisují nastavení, která jsou k dispozici na jednotlivých pevných záložkách.

### <a name="credit-holds"></a>Blokování úvěru

- Chcete-li vyžadovat, aby byla pravidla zaúčtování znovu kontrolována, pokud došlo k navýšení hodnoty prodejní objednávky (rozšířená cena) od uvolnění prodejní objednávky ze seznamu blokování, nastavte možnost **Umožnit úpravu hodnoty prodejních objednávek po uvolnění blokování objednávky** na **Ne**.
- V poli **Důvody zrušených objednávek** vyberte důvod uvolnění, který bude standardně použit, dojde-li ke zrušení prodejní objednávky, která byla blokována správou úvěru.
- Chcete-li kontrolovat limit úvěru skupiny odběratelů podle limitu úvěru, když odběratel na prodejní objednávce náleží ke skupině odběratelů podle limitu úvěru, nastavte možnost **Kontrolovat limit úvěru skupin odběratelů podle limitu úvěru** na **Ano**. Bude zkontrolován limit úvěru pro danou skupinu a v případě, že je dostatečný, bude zkontrolován limit úvěru pro odběratele.
- Chcete-li kontrolovat pořadí platebních podmínek, abyste určili, zda se platební podmínky na prodejní objednávce liší od výchozích platebních podmínek daného odběratele, nastavte možnost **Zkontrolovat limit úvěru při zvýšení platebních podmínek** na **Ano**. Pokud mají nové platební podmínky vyšší pořadí než původní platební podmínky, objednávka se zablokuje ve správě úvěrů.
- Chcete-li kontrolovat pořadí slev při vyrovnání, abyste určili, zda se platební sleva na prodejní objednávce liší od výchozí platební slevy daného odběratele, nastavte možnost **Zkontrolovat limit úvěru při zvýšení slevy při vyrovnání** na **Ano**. Pokud má nová platební sleva vyšší pořadí než původní platební sleva, objednávka se zablokuje ve správě úvěrů.
- V poli **Důvod uvolnění upravených objednávek** vyberte důvod uvolnění, který bude použit jako výchozí, když budou upravené objednávky automaticky uvolněny z blokování správy úvěru.
- Chcete-li kontrolovat chování pravidla **Vypršela platnost limitu úvěru**, nastavte možnost **Ignorovat pravidlo blokování při vypršení platnosti limitu úvěru, je-li datum vypršení platnosti prázdné** na **Ano**. Chcete-li zablokovat objednávku v případě, že datum vypršení platnosti bude prázdné, nastavte možnost **Ne**.
- V Řízení skladu lze vytvořit vytížení při zadání prodejní objednávky. Chcete-li ponechat řádky prodejní objednávky na vytížení, je-li prodejní objednávka blokována pro úvěr, nastavte možnost **Odebrat blokované řádky vytížení** na **Ne**. Vytížení nelze zpracovat, pokud je blokována prodejní objednávka. Chcete-li odebrat řádky prodejní objednávky z vytížení, je-li prodejní objednávka blokována pro úvěr, nastavte možnost **Ano**. Poté lze vytížení zpracovat.
- Prodejní objednávky mohou být automaticky uvolněny z kontroly správy úvěru. V poli **Důvod automatického uvolnění** vyberte důvod uvolnění, který bude při automatickém uvolnění prodejních objednávek použit jako výchozí.
- Prodejní objednávky mohou být automaticky uvolněny z kontroly správy úvěru. V poli **Automaticky uvolnit** vyberte možnost **Bez zaúčtování**, chcete-li uvolnit blokování objednávky. Proces, který zablokoval objednávku, je nutné spustit ručně. Vyberte možnost **Se zaúčtováním**, chcete-li zaúčtovat objednávku pomocí stejného procesu zaúčtování, který byl spuštěn při zablokování prodejní objednávky.

### <a name="credit-management-checkpoint"></a>Kontrolní bod správy úvěru

Můžete nastavit časování, které slouží ke kontrole prodejních objednávek z hlediska možných problémů s úvěrem. Pevná záložka **Kontrolní bod správy úvěru** označuje procesy zaúčtování dokumentů, které zahrnují zpracování pravidel správy úvěrů. Rovněž je možné kontrolovat pravidla úvěru v případě, že provádíte buď pro forma zaúčtování nebo úplné zaúčtování prodejní objednávky. Označením těchto políček můžete definovat procesy zaúčtování, které mají zablokovat objednávku, pokud po zpracování pravidel blokování správy úvěru dojde k potížím.

Můžete také definovat počet dnů odkladu před další kontrolou pravidel úvěru. Ačkoliv je možné určit, že pravidla správy úvěru jsou při zaúčtování kontrolována, pravidla nebudou kontrolována po zadaný počet dnů odkladu. Můžete například potvrdit prodejní objednávku v den č. 1 a určit pro krok potvrzení dva dny odkladu. V tomto případě se pravidla úvěru nezkontrolují v dalším kroku zaúčtování (například vytvoření dodacího listu nebo fakturace objednávky) do dne č. 4. V den č. 4 nebo po tomto dnu budou pravidla znovu zkontrolována při zaúčtování a počet dnů odkladu bude změněn na hodnotu, která je zadána pro následující kontrolní bod zaúčtování.

Nezadáte-li počet dnů odkladu, budou pravidla úvěru zkontrolována při každém kroku zaúčtování, který je nastaven ke spouštění pravidel správy úvěru. Pokud prodejní objednávku uvolníte bez zaúčtování a poté znovu spustíte stejný krok zpracování objednávky, budou pravidla úvěru znovu zkontrolována. Objednávka se například zablokuje po potvrzení a vy ji uvolníte buď s zaúčtováním, nebo bez něj. V takovém případě bude objednávka znovu blokována, pokud ji znovu potvrdíte. Použijte dny odkladu, má-li objednávka pokračovat na další krok zpracování bez opětného blokování.

> [!Note]
> Pokud má jeden kontrolní bod zaúčtování zadaný den odkladu, všechny kontrolní body označené k zaúčtování musejí mít dny odkladu.

- Označením políčka **Zaúčtování** můžete spustit pravidla správy úvěru, když je spuštěn kontrolní bod zaúčtování zobrazený na řádku. Pokud toto políčko neoznačíte, pravidla budou kontrolována pouze jednou během celého procesu zaúčtování.
- Pokud políčko **Zaúčtování** označíte, zadejte počet dnů odkladu, které mají uplynout předtím, než budou pravidla blokování zkontrolována. Není-li označeno políčko **Zaúčtování**, nelze přidat dny odkladu.
- Označením políčka **Pro forma** můžete spustit pravidla správy úvěru, když je spuštěn kontrolní bod pro forma zaúčtování zobrazený na řádku. Ve většině případů je pole **Zaúčtování** v dialogovém okně zobrazeném při zaúčtování prodejní objednávky nastaveno na **Ne**.
- Pokud políčko **Zaúčtování** označíte, zadejte počet dnů odkladu, které mají uplynout předtím, než budou pravidla blokování zkontrolována. Není-li označeno políčko **Zaúčtování**, nelze přidat dny odkladu.

### <a name="credit-management-statistics"></a>Statistiky správy úvěrů

V okně s fakty **Statistika správy úvěru odběratele** na stránce **Odběratel** je zahrnuto několik statistik správy úvěru. Je nutné zadat několik hodnot, které jsou nutné k výpočtu těchto statistik. Zadejte počet měsíců, který se použije pro výpočet následujících hodnot v okně s fakty **Statistika správy úvěru odběratele**:

1. Počet dnů neuhrazeného prodeje 1
2. Počet dnů neuhrazeného prodeje 2
3. Průměrný zůstatek 1
4. Průměrný zůstatek 2
5. Průměrný limit úvěru v %
6. Průměrná expozice v %

### <a name="credit-limits"></a>Limity úvěru

- Ve správě úvěru je limit úvěru odběratele zobrazen v měně odběratele. Je nutné definovat typ směnného kurzu pro limit úvěru v měně odběratele. V poli **Typ směnného kurzu limitu úvěru** vyberte typ směnného kurzu, který má být použit k převodu primárního limitu úvěru na limit úvěru odběratele.
- Chcete-li uživatelům zabránit v úpravách limitů úvěru na stránce **Odběratel**, nastavte možnost **Povolit ruční úpravy limitů úvěru** na **Ne**. Je-li tato možnost nastavena na **Ne**, změny limitu úvěru odběratele lze provést pouze zaúčtováním transakcí úprav limitu úvěru.
- Nastavte možnost **Obejít rezervace zásob** na **Ano**, aby byly ignorovány rezervace zásob při kontrole pravidel blokování správy kreditu. V tomto případě systém zkontroluje kompletní množství řádku a povolí období odkladu kontrolních bodů bez ohledu na rezervované množství zásob.
- Když je povolena správa kreditu, nastavení pole **Zpráva při překročení limitu úvěru** se použije pouze pro zpracování volných faktur. Přestože se zprávy nadále přidávají do prodejních objednávek, když zákazníci překročí svůj limit úvěru, přítomnost těchto zpráv neblokuje potvrzení, tisk výdejek a dodacích listů, ani zaúčtování faktur.

    Správa kreditu je ve výchozím nastavení povolena, ale můžete ji zakázat. Pokud je povolena, pomocí pravidel blokování správy kreditu a kontrolních bodů můžete zjistit, kdy zákazníci překročí svůj limit úvěru. Pokud je zakázána, zprávy přidávané do prodejních objednávek na základě nastavení pole **Zpráva při překročení limitu úvěru** vám pomohou zjistit, kdy zákazníci překročí svůj limit úvěru.

### <a name="number-sequences-and-shared-number-sequence-parameters"></a>Číselné řady a sdílené parametry číselných řad

Ke zpracování úprav limitu úvěru je nutné zadat ID deníku. Je nutné přidat číslo úpravy limitu úvěru, které by mělo být použito ke generování ID deníku.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
