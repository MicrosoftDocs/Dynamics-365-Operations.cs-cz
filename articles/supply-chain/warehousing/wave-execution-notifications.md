---
title: Oznámení o provedení vlny
description: Toto téma popisuje oznámení o provedení vlny a vysvětluje, jak je nastavit.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2022-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: fee112d3211f619b2146dd21c4f8a52ad33667d6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019147"
---
# <a name="wave-execution-notifications"></a>Oznámení o provedení vlny

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Funkce *Oznámení o provedení vlny* používá obchodní události a centrum akcí k doručování oznámení, která souvisejí s prováděním vln. Umožňuje určit typy událostí, které generují oznámení, sklady, které je generují, a uživatele, kteří je dostávají.

Tlačítko **Zobrazit zprávy** (symbol zvonku) na pravé straně navigační lišty označuje, kdy je pro aktuálního uživatele k dispozici zpráva z centra akcí. Uživatel může tlačítkem **Zobrazit zprávy** otevřít centrum akcí a zkontrolovat zprávy.

K podnikovým událostem dochází při spuštění obchodních procesů. Obchodní procesy jsou tvořeny úkoly. Během obchodního procesu provádějí uživatelé, kteří se na něm podílejí, obchodní akce, kterými plní tyto úkoly. Obchodní události poskytují mechanismus, který umožňuje externím systémům přijímat oznámení z aplikací Finance and Operations. Tímto způsobem mohou systémy provádět obchodní akce v reakci na obchodní události. Další informace naleznete v tématu [Přehled obchodních událostí](../../fin-ops-core/dev-itpro/business-events/home-page.md).

## <a name="turn-on-the-wave-execution-notifications-feature"></a>Zapnutí funkce Oznámení o provedení vlny

Než můžete použít funkci *Oznámení o provedení vlny*, musíte ji v systému zapnout. Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba. Funkce je zde uvedena následujícím způsobem:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Zapnutí funkce Oznámení o provedení vlny*

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a>Scénář: Odeslání oznámení o provedení dávky vlny do centra akcí

Tento scénář ukazuje kompletní tok pro odesílání oznámení o chybách při provádění dávky vlny zadané roli prostřednictvím centra akcí.

### <a name="make-demo-data-available"></a>Zpřístupnění ukázkových dat

Pokud chcete provést tento scénář, musíte mít nainstalována ukázková data a musíte vybrat právnickou osobu **USMF**.

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a>Ujistěte se, že vlny běží v dávkovém režimu

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Parametry řízení skladu**.
1. Na pevné záložce **Zpracování vlny** nastavte možnost **Zpracovat vlny v dávce** na *Ano*.

> [!NOTE]
> Pokud chcete zakázat oznámení o provádění dávkových vln, nastavte možnost **Zakázat oznámení o dávkách zpracování vlny** na *Ano*.

### <a name="configure-a-wave-notification-policy"></a>Konfigurace zásad oznámení o vlně

Zásady oznámení o vlně definují typy oznámení, která se odesílají, a uživatele, kteří jsou upozorněni.

1. Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Zásady oznámení o vlně**.
1. Vytvořte záznam, který má následující nastavení:

    - **Zásady oznámení o vlně** *24BatchError*
    - **Popis:** *Chyba dávky vlny skladu 24*
    - **Odeslat oznámení při:** *Pouze chyba*
    - **Roli:** *Správce systému*

        > [!NOTE]
        > Protože tento scénář používá ukázková data, role *Správce systému* je vybrána pro zjednodušení. Protože jste přihlášeni jako správce systému, obdržíte oznámení. V praxi byste však měli vybrat konkrétnější roli, které budou chodit oznámení o chybách při provádění dávek vln, například *Manažer skladu*.

1. V podokně akcí vyberte **Uložit**.

### <a name="configure-a-wave-template"></a>Konfigurujte šablonu vlny

Šablony vln vám umožní propojit konkrétní příklady vlnových metod s odpovídajícími šablonami popisků vln.

1. Přejděte na **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.
1. V podokně seznamu nastavte pole **Typ šablony vlny** na *Expedice* a potom vyberte šablonu vlny *Výchozí expedice 24* pro sklad 24.
1. Na pevné záložce **Obecné** nastavte pole **Zásady oznámení o vlně** na *24BatchError*.

### <a name="configure-a-work-template"></a>Konfigurace šablony práce

Šablony práce se používají při provádění vln pro generování práce. V tomto scénáři by provedení vlny mělo vyvolat chybu. Nastavením dotazu šablony práce na použití neexistujícího skladu zajistíte, že se provedení vlny nezdaří, a proto dojde k odeslání oznámení.

1. Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.
1. V podokně seznamu nastavte pole **Typ šablony práce** na *Prodejní objednávky* a potom vyberte šablonu práce *24 SO Stage* pro sklad 24.
1. V podokně akcí vyberte **Upravit dotaz**.
1. V dialogovém okně editoru dotazů na kartě **Rozsah** upravte následující řádek (nebo jej přidejte, pokud neexistuje):

    - **Tabulka:** *Dočasné pracovní transakce*
    - **Odvozená tabulka:** *Dočasné pracovní transakce*
    - **Pole:** *Sklad*
    - **Kritéria:** Změňte hodnotu z *24* na *Chyba*.

1. Vyberte **OK** a potvrďte změnu.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Vytvořte prodejní objednávku a uvolněte ji do skladu

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Vytvořte prodejní objednávku, která má následující nastavení:

    - **Účet zákazníka:** *US-001*
    - **Sklad:** *24*

1. Na záložce s náhledem **Řádky prodejní objednávky** přidejte prodejní objednávku s následujícím nastavením:

    - **Číslo položky:** *A0001*
    - **Množství:** *10*

    > [!NOTE]
    > Tyto položky a množství jsou pouze příklady. Zadaný sklad musí obsahovat dostatečný sklad.

1. V době, kdy je vybrán nový řádek na záložce s náhledem **Řádky prodejní objednávky**, vyberte na panelu nástrojů **Zásoby \> Rezervace**.
1. Na stránce **Rezervace** vyberte v podokně Akce možnost **Rezervovat šarži**. Poté stránku zavřete.
1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.

### <a name="notifications-from-wave-batch-job-execution"></a>Oznámení o provedení dávkové úlohy vlny

V závislosti na nastavení vašich obchodních událostí nakonec obdržíte oznámení o selhání provedení vlny. Zpráva centra akcí bude vypadat jako v následujícím příkladu a bude obsahovat odkaz na vlnu, která selhala.

> **Chyba během provedení vlny**  
> Při provádění vlny USMF-000000001 došlo k chybě.  
> Poslední zprávy: Pro vlnu USMF-000000001 nebyla vytvořena žádná práce.
>
> **STAV**  
> Aktivní
>
> Otevřít podrobnosti vlny

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
