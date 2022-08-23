---
title: Zpřístupnění hotového zboží fyzicky před odesláním do deníků
description: Když je vyrobená položka hlášena jako dokončená, je registrována jako dostupná pro další fyzické zpracování a je zaúčtován jeden nebo více deníků. Tento článek popisuje, jak odložit zaúčtování deníku povolením jejich zpracování dávkovou úlohou ve frontě zpráv.
author: johanhoffmann
ms.date: 08/02/2022
ms.topic: article
ms.search.form: ProdParameters, JmgProdParameters, InventLocation, JmgMES3PMessageProcessorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-08-02
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 7a8327552d9e6c38721fdac9ee1795e61f90f329
ms.sourcegitcommit: 8d072505f66f507aafbaae65bedf3b530eb6cb7b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9266479"
---
# <a name="make-finished-goods-physically-available-before-posting-to-journals"></a>Zpřístupnění hotového zboží fyzicky před odesláním do deníků

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Když pracovník nahlásí vyrobenou položku jako hotovou, systém ji zaregistruje jako dostupnou pro další fyzické zpracování (například odeslání nebo uložení). Během tohoto procesu je také zaúčtován jeden nebo více deníků (jako je například zpráva jako hotový deník, deník výběrového seznamu a deník karet cest). Pokud chcete své položky fyzicky zpřístupnit před zpracováním všech účtování, můžete systém nastavit tak, aby odložil účtování do deníku. Odložená účtování jsou pak spravována dávkovou úlohou, která zpracuje účtování tak, jak to systémové prostředky dovolí.

Následující obrázek ukazuje, jak jsou procesy pro zaúčtování deníků vyvolány jak s odloženým zaúčtováním, tak bez něj.

![Proces sestavy jako dokončený s odloženým zaúčtováním do deníku a bez něj.](media/deferred-posting-flowchart.png "Proces sestavy jako dokončený s odloženým zaúčtováním do deníku a bez něj")

## <a name="turn-on-deferred-journal-posting-for-your-system"></a>Zapnutí pro systém odloženého účtování do deníku

Než můžete použít odložené zaúčtování do deníku, musíte ho ve svém systému zapnout. Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení výroby*
- **Název funkce:** *(Preview) Před zaúčtováním do deníků zpřístupnit hotové zboží fyzicky*

## <a name="set-up-journal-posting-options-for-reporting-as-finished"></a>Nastavení možností účtování do deníku pro vykazování jako dokončené

Pracovníci mohou hlásit položky jako dokončené pomocí kteréhokoli z následujících klientů:

- Webový klient
- Mobilní aplikace Warehouse Management
- Rozhraní pro provádění výrobního provozu

Webový klient používá stejnou konfiguraci způsobu účtování jako mobilní aplikace Warehouse Management. Metoda účtování, kterou používá rozhraní pro provádění výrobního provozu, však musí být nakonfigurována samostatně.

### <a name="set-journal-posting-options-for-the-web-client-and-the-warehouse-management-mobile-app"></a>Nastavení možností účtování deníku pro webového klienta a mobilní aplikaci Warehouse Management

V mobilní aplikaci pracovníci hlásí položky jako dokončené otevřením položky nabídky mobilního zařízení, kde je hodnota **Proces tvorby práce** *Nahlásit jako hotové* nebo *Nahlásit jako hotové a odložit*. Ve webovém klientovi pracovníci hlásí položky jako hotové ze stránky seznamu **Všechny výrobní zakázky** nebo stránky **Výrobní zakázka (podrobnosti)**. Můžete nakonfigurovat výchozí metodu pro celou společnost a podle potřeby můžete také nastavit přepsání specifická pro sklad.

Pomocí následujícího postupu nakonfigurujte výchozí metodu účtování pro celou společnost pro vykazování hotových položek z webového klienta nebo mobilní aplikace Warehouse Management.

1. Přejděte na **Řízení výroby \> Nastavení \> Parametry řízení výroby**.
1. Na kartě **Deníky** v části **Vykázat jako hotové** nastavte pole **Metoda účtování** na některou z následujících hodnot:

    - *Bezprostřední* – Když je položka vykázána jako dokončená, systém plně zpracuje všechna související účetní účtování, než označí hotovou položku jako fyzicky dostupnou.
    - *Odložení* – Když je položka vykázána jako dokončená, systém označí hotovou položku jako fyzicky dostupnou a přidá zaúčtování do deníku do fronty zpráv. Systém nečeká na úplné zpracování účtování, než označí hotovou položku jako fyzicky dostupnou.

Následující postup použijte ke konfiguraci přepsání specifických pro sklad pro výchozí metodu účtování, která je nakonfigurována na stránce **Parametry řízení výroby**.

1. Přejděte do části **Řízení skladu \> Nastavení \> Rozdělení zásob \> Sklady**.
1. Vyberte sklad, který chcete nastavit.
1. V podokně akcí vyberte **Upravit**.
1. Na pevné záložce **Sklad** v části **Výrobní objednávky** nastavte pole **Metoda účtování** na některou z následujících hodnot:

    - *Zdědit* – Vybraný sklad zdědí nastavení ze stránky **Parametry řízení výroby**.
    - *Bezprostřední* – Když je položka vykázána jako dokončená, systém plně zpracuje všechna související účetní účtování, než označí hotovou položku jako fyzicky dostupnou.
    - *Odložení* – Když je položka vykázána jako dokončená, systém označí hotovou položku jako fyzicky dostupnou a přidá zaúčtování do deníku do fronty zpráv. Systém nečeká na úplné zpracování účtování, než označí hotovou položku jako fyzicky dostupnou.

### <a name="set-journal-posting-options-for-the-production-floor-execution-interface"></a>Nastavení možnosti účtování do deníku pro rozhraní provádění výrobního provozu

Pomocí následujícího postupu nakonfigurujte metodu účtování, která se používá, když jsou položky hlášeny jako hotové z rozhraní pro provádění výrobního provozu.

1. Klikněte na **Řízení výroby \> Nastavení \> Provádění výroby \> Výchozí hodnoty výrobní zakázky**.
1. Na kartě **Vykázat jako dokončené** v části **Vykázat jako hotový deník** nastavte pole **Metoda účtování** na některou z následujících hodnot:

    - *Bezprostřední* – Když je položka vykázána jako dokončená, systém plně zpracuje všechna související účetní účtování, než označí hotovou položku jako fyzicky dostupnou.
    - *Odložení* – Když je položka vykázána jako dokončená, systém označí hotovou položku jako fyzicky dostupnou a přidá zaúčtování do deníku do fronty zpráv. Systém nečeká na úplné zpracování účtování, než označí hotovou položku jako fyzicky dostupnou.

## <a name="schedule-the-message-processor-batch-job-to-process-deferred-postings"></a>Naplánování dávkové úlohy zpracovatele zpráv pro zpracování odložených účtování

Dávková úloha zpracovatele zpráv je zodpovědná za zpracování účtování deníku poté, co byla zařazena do fronty. Chcete-li zajistit, aby byly vaše účetní záznamy zpracovány, musíte tuto úlohu nakonfigurovat tak, aby se spouštěla v pravidelných intervalech. Následujícím postupem nastavte požadovanou dávkovou úlohu.

1. Přejděte do **Správa systému \> Zpracovatel zpráv \> Zpracovatel zpráv**.
1. Na pevné záložce **Parametry** nastavte pole **Fronta zpráv** na *Výroba*.
1. Na pevné záložce **Spustit na pozadí** nastavte možnost **Dávkové zpracování** na *Ano*. Poté nastavte plán opakování a podle potřeby nakonfigurujte další nastavení. Nastavení fungují stejně jako u jiných typů [úloh na pozadí](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) v Microsoft Dynamics 365 Supply Chain Management.

## <a name="track-the-progress-of-your-deferred-postings"></a>Sledování průběhu odloženého účtování

Odložená účtování v deníku jsou zařazena do fronty jako *zprávy zpracovatele zpráv*, které čekají, až je zpracuje *zpracovatel zpráv*. Zpracovatel zpráv je třeba nastavit tak, aby běžel jako plánovaná dávková úloha. Chcete-li zobrazit zprávy odloženého odesílání, které byly nebo budou zpracovány zpracovatelem zpráv, přejděte na **Kontrola výroby \> Výrobní zakázky \> Odložené zaúčtování výrobní zakázky**.

### <a name="message-grid-columns-and-filters"></a>Sloupce a filtry mřížky zpráv

Můžete použít pole v horní části stránky **Odložené účtování výrobní zakázky** k nalezení konkrétních zpráv, které hledáte.

K dispozici jsou následující filtry:

- **Typ zprávy** – Určete typ zpráv, které se zobrazí v mřížce.
- **Stav zprávy** – Určete stav zpráv, které se zobrazí v mřížce. Existují následující stavy:

    - *Ve frontě* – Zpráva je připravena ke zpracování procesorem zpráv.
    - *Zpracováno* – Zpráva byla úspěšně zpracována procesorem zpráv.
    - *Zrušeno* – Zprávu se nepodařilo zpracovat během posledního pokusu a poté byla uživatelem zrušena.
    - *Nepodařilo se* – Zprávu se nepodařilo zpracovat při posledním pokusu. Systém třikrát zopakuje neúspěšné zprávy. Poté to vzdá a nechá zprávu ve stavy *Nepodařilo se*. Upozorňujeme, že zprávu nelze ručně zrušit ani upravit, dokud neproběhne poslední z těchto tří pokusů.

- **Obsah zprávy** – Tento filtr provádí fulltextové vyhledávání obsahu zprávy. (Obsah zprávy se v mřížce nezobrazuje.) Filtr považuje většinu speciálních symbolů (například spojovníky) za mezery a všechny znaky mezery za logické operátory OR. Pokud například hledáte konkrétní hodnotu `journalid` rovnou *USMF-123456*, systém vyhledá všechny zprávy, které obsahují „USMF“ nebo „123456“. V tomto případě bude seznam výsledků pravděpodobně dlouhý. Proto je lepší zadat pouze *123456*, protože to vrátí konkrétnější výsledky.

Seznam můžete také seřadit a filtrovat výběrem libovolného záhlaví sloupce a zadáním kritérií v rozevíracím dialogovém okně.

### <a name="view-the-message-log-message-content-and-details"></a>Zobrazit protokol zpráv, obsah zprávy a podrobnosti

Podrobné informace o zprávě najdete tak, že ji vyberete v mřížce a poté vyberete kartu **Protokol** nebo **Nezpracovaný obsah** pod mřížkou zpráv, kde se zobrazuje každá událost zpracování.

Panel nástrojů na kartě **Protokol** obsahuje následující tlačítka:

- **Protokol** – Výběrem tohoto tlačítka zobrazíte výsledky zpracování. Toto tlačítko je zvláště užitečné, když zprávy mají hodnotu **Výsledek zpracování** *Nepodařilo se* a chcete zjistit důvody selhání zpracování.
- **Balíček** – Více operací zpracování zpráv lze spustit jako součást stejného dávkového procesu. Toto tlačítko vyberte, chcete-li zobrazit tato podrobná data. Například můžete zjistit, zda existují závislosti, které vyžadují konkrétní pořadí zpracování pro některé zprávy.

### <a name="manually-process-or-cancel-a-message"></a>Ruční zpracování nebo zrušení zprávy

V případě potřeby můžete zprávu ručně zpracovat nebo zrušit v závislosti na jejím aktuálním stavu. Vyberte zprávu v mřížce a poté vyberte **Proces** nebo **Zrušit** v podokně Akce.

### <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Nastavte obchodní události k doručování upozornění na neúspěšné výsledky zpracování

Můžete nastavit [obchodní události](../../fin-ops-core/dev-itpro/business-events/home-page.md) k doručování upozornění na neúspěšné výsledky zpracování. Aktivujte obchodní událost s názvem *Zpráva procesoru zprávy byla zpracována* na stránce **Správa systému \> Nastavení \> Obchodní události \> Katalog obchodních událostí**.

V rámci aktivačního procesu budete vyzváni, abyste uvedli, zda je událost specifická pro jednu právnickou osobu, nebo se vztahuje na všechny právnické osoby. Budete také vyzváni k zadání hodnoty **Název koncového bodu**. Tato hodnota musí být definována první.

> [!NOTE]
> Pokud je pole **Když dojde k obchodní události** nastaveno na *Microsoft Power Automate* (a ne například *HTTPS*), hodnota **Název koncového bodu** bude automaticky vytvořena v Supply Chain Management na základě nastavení *Microsoft Power Automate*.
