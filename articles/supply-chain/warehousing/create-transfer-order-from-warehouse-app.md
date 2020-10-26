---
title: Vytvoření převodních příkazů z aplikace skladu
description: Toto téma popisuje, jak vytvářet a zpracovávat převodní příkazy z funkce aplikace skladu.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c30b0e74053480a08f84f4d7579021084ded5799
ms.sourcegitcommit: 286786445f72db20e993d37a63df0b886f8f5e99
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/12/2020
ms.locfileid: "3988367"
---
# <a name="create-transfer-orders-from-the-warehouse-app"></a>Vytvoření převodních příkazů z aplikace skladu

[!include [banner](../includes/banner.md)]

Tato funkce umožnuje pracovníkům skladu vytvářet a zpracovávat převodní příkazy přímo z aplikace skladu. Pracovníci skladu začnou výběrem cílového skladu a pak můžou pomocí aplikace naskenovat jednu nebo více registračních značek a přidat registrační značky do převodního příkazu. Když pracovník skladu vybere **Dokončit objednávku** , vytvoří dávková úloha požadovaný převodní příkaz a řádky příkazu na základě zásob na skladě registrovaných pro tyto registrační značky.

## <a name="enable-the-create-transfer-orders-from-warehouse-app-feature"></a><a name="enable-create-transfer-order-from-warehouse-app"></a>Povolení funkce vytváření převodních příkazů z aplikace skladu

Než budete moct tuto funkci používat, musíte funkci a její předpoklady povolit ve svém systému. Správci mohou pomocí stránky [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a povolit je v případě potřeby.

1. Nejprve povolte funkci [Zpracovat události aplikace skladu](warehouse-app-events.md), která je uvedená ve [správě funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) jako:
    - **Modul** - Řízení skladu
    - **Název funkce** – Zpracovat události aplikace skladu
1. Pak povolte funkci *Vytvářet převodní příkazy z aplikace skladu* , která je uvedena jako:
    - **Modul** - Řízení skladu
    - **Název funkce** – Vytvářet a zpracovávat převodní příkazy z aplikace skladu
1. Pokud chcete automatizovat zpracování odchozích dodávek, musíte také povolit funkci [Potvrdit odchozí dodávky z dávkových úloh](confirm-outbound-shipments-from-batch-jobs.md). Tato funkce je uvedena jako:
    - **Modul** - Řízení skladu
    - **Název funkce** – Potvrdit odchozí dodávky z dávkových úloh

## <a name="set-up-a-mobile-device-menu-item-to-create-transfer-orders"></a><a name="setup-warehouse-app-menu"></a>Nastavení položky nabídky mobilního zařízení pro vytváření převodních příkazů

Tady jsou obecné pokyny pro nastavení položky nabídky mobilního zařízení pro vytvoření převodního příkazu. V závislosti na vašich obchodních požadavcích na úroveň automatizace, která má být nastavena, když uživatelé vytváří převodní příkazy ve skladu, budou povoleny různé konfigurace. Scénář v tomto dokumentu bude popisovat jednu takovou konfiguraci.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení** .
1. Vyberte **Nová** pro přidání nové položky nabídky. Začněte určením následujících nastavení:

    - **Název položky nabídky** – Přiřaďte název tak, jak by se měl zobrazovat v aplikaci Supply Chain Management.
    - **Název** – Přiřaďte název nabídky tak, jak by se měl zobrazovat pracovníkům v aplikaci skladu.
    - **Režim** – Nastavte na *Nepřímý* (tato aplikace skladu nebude vytvářet práci).
    - **Kód aktivity** – Nastavte na *Vytvořit převodní příkaz z registračních značek* , aby pracovníci skladu mohli vytvořit převodní příkaz na základě jedné nebo více naskenovaných registračních značek.

1. Pomocí nastavení **Zásady vytváření řádků převodních příkazů** můžete řídit způsob, jakým bude tato položka nabídky vytvářet řádky převodního příkazu. Tyto řádky budou vytvářeny a aktualizovány na základě zásob na skladě, které jsou registrovány pro naskenované registrační značky. Zvolte jednu z následujících hodnot:

    - **Bez rezervace** – Řádky převodního příkazu nebudou rezervovány.
    - **Registrační značka řízena s rezervací řádků** – Řádky převodního příkazu budou rezervovány a bude použita možnost strategie Registrační značka řízena, která ukládá relevantní ID registračních značek přidružená k řádkům příkazu. Hodnoty Vyhledané ID registrační značky lze proto používat jako součást procesu vytváření práce pro řádky převodních příkazů.

1. Pomocí nastavení **Zásady odchozí dodávky** můžete podle potřeby přidat další automatizaci do procesu expedice odchozích převodních příkazů. Když pracovník vybere tlačítko **Dokončit objednávku** , aplikace vytvoří událost aplikace skladu *Dokončit objednávku* , která uloží hodnotu, kterou tu zvolíte v poli **Zásady odchozí dodávky** , pro všechny řádky v aktuálním převodním příkazu. Později, když je fronta událostí zpracována dávkovou úlohou a vytvoří se převodní příkaz, může být hodnota uložená v tomto poli přečtena dávkovou úlohou a může proto řídit, jak tato úloha zpracovává každý řádek. Vyberte jednu z následujících možností:

    - **Žádné** – Neprovádí se žádné automatické zpracování.
    - **Uvolnit do skladu** – Automatizuje proces uvolnění do skladu.
    - **Potvrzení expedice** – Automatizuje proces potvrzení expedice.
    - **Uvolnění a potvrzení expedice** – Automatizuje procesy uvolnění do skladu i potvrzení expedice.

## <a name="add-the-mobile-device-menu-item-to-a-menu"></a>Přidání položky nabídky mobilního zařízení do nabídky

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení** .
1. Vyberte možnost **Upravit** .
1. Po výběru nové položky nabídky v části **Dostupné nabídky a položky nabídek** vyberte existující nabídku. Přidejte položku nabídky výběrem tlačítka se šipkou doprava.

## <a name="create-a-transfer-order-based-on-license-plates"></a>Vytvoření převodního příkazu na základě registračních značek

Aplikace skladu používá jednoduchý proces vytváření převodních příkazů na základě registračních značek. Pracovník pomocí aplikace skladu provede následující:

1. Vytvoří převodní příkaz a identifikuje cílový sklad.
1. Identifikuje všechny registrační značky k expedici.
1. Vyberte **Dokončit objednávku** .

>[!NOTE]
> Je možné, aby více pracovníků přiřazovalo registrační značky určené pro stejný převodní příkaz tak, že pomocí tlačítka **Vybrat převodní příkaz** vyberou existující, nezpracované číslo převodního příkazu z fronty událostí aplikace skladu. Informace o tom, jak najít hodnoty převodních příkazů, viz [Prošetřování událostí aplikace skladu](#inquire-the-warehouse-app-events).

## <a name="example-scenario"></a>Příklad

Tento scénář poskytuje přehled procesu vytváření převodních příkazů a jejich automatického zpracování na základě zásob na skladě registrovaných na vybraných registračních značkách.

Pokud si chcete projít tento scénář s doporučenými hodnotami, musíte pracovat v systému s nainstalovanými ukázkovými daty a vybrat právnickou osobu *USMF* .

Tento scénář předpokládá, že jste už povolili funkci [Vytvářet a zpracovávat převodní příkazy z aplikace skladu](#enable-create-transfer-order-from-warehouse-app) i [zpracování událostí aplikace skladu](warehouse-app-events.md).

Kromě nastavení možnosti vytvoření převodního příkazu v položkách nabídky mobilního zařízení musí být také nastavené a povolené další šablony, směrnice skladového místa a dávkové úlohy.

### <a name="example-scenario-blueprint"></a>Příklad podrobného plánu scénáře

Provozujete maloobchod a máte více registračních značek, z nichž každá obsahuje kombinaci položek umístěných v konkrétním místě v jednom z vašich skladů ( *Sklad 51* ). Chcete povolit proces, který pracovníkům umožní vytvořit převodní příkaz do jiného skladu ( *Sklad 61* ) pro kolekci naskenovaných registračních značek. Převodní příkaz automaticky aktualizujete pro expedici, jakmile bude identifikována poslední registrační značka pro tento příkaz.

![Příklad automatizovaného procesu pro převodní příkazy](media/create-transfer-order-from-app-example.png "Příklad automatizovaného procesu převodního příkazu")

### <a name="create-a-mobile-device-menu-item-for-creating-transfer-orders"></a>Vytvoření položky nabídky mobilního zařízení pro vytváření převodních příkazů

Tato část vysvětluje, jak můžete vytvořit novou položku nabídky mobilního zařízení pro vytváření převodních příkazů. Nastavte **Režim** na *Nepřímý* a **Kód aktivity** na *Vytvořit převodní příkaz z registračních značek* .

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení** .
1. Zvolte **Nové** .
1. Do pole **Název položky nabídky** zadejte název *Vytvořit PP* .
1. Do pole **Název** zadejte popis *Vytvořit PP* .
1. V poli **Režim** vyberte *Nepřímý* .
1. V nastavení **Kód aktivity** vyberte *Vytvořit převodní příkaz z registračních značek* .
1. V nastavení **Zásady vytváření řádků příkazu** vyberte *Registrační značka řízena s rezervací řádků* .
1. V nastavení **Zásady odchozí dodávky** vyberte *Uvolnění a potvrzení expedice* .
1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení** .
1. Vyberte možnost **Upravit** .
1. Vyberte existující nabídku **Zásoby** a pak vyberte novou položku nabídky v části **Dostupné nabídky a položky nabídek** . Přidejte tuto položku nabídky do nabídky **Zásoby** výběrem tlačítka se šipkou doprava.

### <a name="set-up-work-templates-to-auto-process-and-break-work-by-located-license-plate"></a>Nastavení šablon práce tak, aby automaticky zpracovávaly a zalamovaly práci podle vyhledané registrační značky

Tato část vysvětluje, jak povolit, aby šablona práce automaticky zpracovávala práci vytvořenou šablonou, když je uvolněna vlna.

1. Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony** .
1. V poli **Typ pracovního příkazu** vyberte *Vydání převodního příkazu* .
1. Vyberte **Nová** , abyste mohli vytvořit novou šablonu práce.
1. Do pole **Šablona práce** zadejte *51 Automatické zpracování RZ* .
1. Do pole **Popis šablony práce** zadejte *51 Automatické zpracování RZ* .
1. Zaškrtněte políčko **Automaticky zpracovat** . To musí být zaškrtnuté, aby mohly být zpracovány jakékoli kroky automatizace.
1. Ukázková data už obsahují šablonu práce *51 Převod* . Upravte pole **Pořadové číslo** tak, aby nová šablona práce měla nižší pořadové číslo než stávající šablona práce *51 Převod* .
1. Na panelu nástrojů vyberte **Uložit** a povolte záložku s náhledem **Podrobnosti šablony práce** .
1. Na záložce s náhledem **Podrobnosti šablony práce** vyberte možnost **Nový** na panelu nástrojů. Přidáte dva řádky.
1. V poli **Typ práce** vyberte *Vybrat* .
1. V poli **ID pracovní třídy** vyberte *TransfOut* .
1. Vyberte **Nový** na panelu nástrojů **Podrobnosti šablony práce** .
1. V poli **Typ práce** vyberte *Vložit* .
1. V poli **ID pracovní třídy** vyberte *TransfOut* .
1. Výběrem možnosti **Uložit** povolte pole **Kód předpisu** .
1. Na řádku *Vložit* pro **Typ práce** vyberte **Kód předpisu** *Baydoor* (Nákladová brána). Ujistěte se, že má tato nová šablona práce nejnižší **Pořadové číslo** .
1. Na panelu nástrojů vyberte **Upravit dotaz** . Otevře se editor dotazů.
1. Na kartě **Rozsah** vyberte **Přidat** .
1. Na přidaném řádku vyberte v části **Pole** možnost *Sklad* .
1. V poli **Kritéria** vyberte *51* .
1. Vyberte kartu **Třídění** .
1. Vyberte **Přidat** a nastavte **Pole** na *Vyhledané ID registrační značky* . Výběrem tohoto pole povolíte tlačítko **Zalomení záhlaví práce** na panelu nástrojů.
1. Výběrem možnosti **OK** a pak **Ano** resetujte seskupení a vraťte se na stránku **Šablony práce** .
1. Vyberte **Zalomení záhlaví práce** , povolte **Seskupit podle tohoto pole** pro **Vyhledané ID registrační značky** a okno zavřete.

> [!NOTE]
> Ne všechna nastavení lze automaticky zpracovávat, například položky se skutečnou hmotností a používání sledovacích dimenzí.

### <a name="set-up-location-directives-for-the-license-plate-guided-strategy"></a>Nastavení směrnic skladového místa pro strategii řízení registračními značkami

Tato část vysvětluje, jak nastavit proces výběru směrnice skladového místa pro použití strategie **Řízeno registračními značkami** .

1. Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa** .
1. Vyberte možnost **Upravit** .
1. V záhlaví navigačního seznamu vyberte **Typ pořadí pracovních činností** *Vydání převodního příkazu* .
1. V navigačním seznamu vyberte existující směrnici skladového místa **51 PP výdej** .
1. Na záložce s náhledem **Řádky** zaškrtněte políčko **Povolit rozdělení** .
1. Na záložce s náhledem **Akce směrnice skladového místa** přidejte nový řádek akce výběrem možnosti **Nová** .
1. Do pole **Název** zadejte *RZ řízena* .
1. V poli **Strategie** vyberte *Registrační značka řízena* . Tato akce musí mít nejnižší pořadové číslo.
1. Na panelu nástrojů vyberte **Uložit** .
1. Na panelu nástrojů vyberte ikonu **Aktualizovat** stránku.
1. Na záložce s náhledem **Akce směrnice skladového místa** vyberte řádek *PP výdej* .
1. Na panelu nástrojů **Akce směrnice skladového místa** změňte pomocí možnosti **Přesunout dolů** pořadové číslo tak, aby bylo vyšší než pořadové číslo právě vytvořené akce *RZ řízena* .

> [!NOTE]
> Strategie Registrační značka řízena se pokusí rezervovat a vytvořit práci výdeje z míst, kde jsou požadované registrační značky, které byly přidruženy k řádkům převodního příkazu. Pokud to však není možné a přesto byste chtěli vytvořit práci výdeje, měli byste se vrátit k strategii akcí směrnic skladového místa a možná také vyhledat zásoby v jiné oblasti skladu v závislosti na potřebách vašeho obchodního procesu.

### <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Nastavit dávkovou úlohu pro zpracování událostí aplikace skladu

Tato část vysvětluje, jak nastavit naplánovanou dávkovou úlohu pro zpracování událostí aplikace skladu.

1. Přejděte na **Správa skladu \> Periodické úkoly \> Zpracovat události aplikace skladu** .
2. V dialogovém okně povolte **Dávkové zpracování** v části **Spustit na pozadí** .
3. Vyberte **Opakování** a nastavte dávkovou úlohu tak, aby prováděla zpracování v intervalu, jaký potřebujete pro svou obchodní činnost.
4. Výběrem **OK** se vraťte do hlavního dialogového okna.
5. Výběrem **OK** v hlavním dialogovém okně přidejte úlohu do fronty dávek.

### <a name="set-up-a-batch-job-to-release-transfer-orders-automatically"></a>Nastavení dávkové úlohy na automatické uvolnění převodních příkazů

Tato část vysvětluje, jak můžete nastavit naplánovanou dávkovou úlohu tak, aby uvolnila převodní příkazy, které byly označeny jako „připraveno k uvolnění“.

1. Přejděte na **Řízení skladu \> Uvolnit do skladu \> Automaticky uvolnit převodní příkazy** .
1. V dialogovém okně rozbalte část **Záznamy k zahrnutí** .
1. Vyberte **Filtr** v části **Záznamy k zahrnutí** .
1. Na stránce dotazu **WHSTransferAutoRTWQuery** vyberte na kartě **Rozsah** možnost **Přidat** a přidejte do dotazu nový řádek.
1. V poli **Tabulka** tohoto nového řádku vyberte rozevírací nabídku a pak vyberte tabulku **Uvolnění řádku převodu do skladu** .
1. V rozevírací nabídce **Pole** vyberte **Zásady odchozí dodávky** .
1. V poli **Kritéria** vyberte **Uvolnění a potvrzení expedice** .
1. Na řádku, na kterém je **Pole** nastaveno na *Ze skladu* , vyberte v poli **Kritéria** položku *51* .
1. Výběrem **OK** se vraťte do hlavního dialogového okna.
1. Rozbalte část **Spustit na pozadí** a nastavte dávkové zpracování.
1. Povolte **Dávkové zpracování** v části **Spustit na pozadí** .
1. Vyberte **Opakování** a nastavte dávkovou úlohu tak, aby prováděla zpracování v intervalu, jaký potřebujete pro svou obchodní činnost.
1. Výběrem **OK** se vraťte do hlavního dialogového okna.
1. Výběrem **OK** v hlavním dialogovém okně přidejte úlohu do fronty dávek.

### <a name="set-up-the-process-outbound-shipment-batch-job"></a>Nastavení dávkové úlohy „Zpracovat odchozí dodávku“

Tato část vysvětluje, jak nastavit naplánovanou dávkovou úlohu na spuštění potvrzení odchozí dodávky pro náklady připravené k expedici související s řádky převodního příkazu, které jsou „připraveny k expedici“.

1. Přejděte na **Správa skladu \> Periodické úkoly \> Zpracování odchozích zásilek** .
1. Rozbalte oddíl **Záznamy k zahrnutí** .
1. Vyberte **Filtr** .
1. V dotazu **WHSLoadShipConfirm** vyberte kartu **Spojení** .
1. Rozbalte hierarchii tabulek tak, aby byly rozbaleny části **Náklady** a **Podrobnosti o nákladu** .
1. Vyberte tabulku **Podrobnosti o nákladu** .
1. Vyberte tlačítko **Přidat spojení tabulky** .
1. V seznamu relací tabulky ve sloupci **Vztah** vyfiltrujte nebo vyhledejte *Řádky převodního příkazu (Odkaz)* .
1. Nastavte fokus na vztah tabulky v seznamu a pak stiskněte tlačítko **Vybrat** .
1. Vyberte tabulku **Řádky převodního příkazu** .
1. Vyberte tlačítko **Přidat spojení tabulky** .
1. V seznamu vztahů tabulky ve sloupci **Vztah** vyfiltrujte nebo vyhledejte *Další pole převodu zásob (ID záznamu)* .
1. Nastavte fokus na vztah tabulky v seznamu a pak stiskněte tlačítko **Vybrat** .
1. Vyberte kartu **Oblast** .
1. V tabulkách **Rozsah** v dotazu nastavíte tři rozsahy kritérií dotazu. Výběrem tlačítka **Přidat** přidejte řádek.
1. Přidejte rozsah pro tabulku **Náklady** . **Pole** nastavte na *Stav nákladu* a **Kritéria** nastavte na *Naloženo* .
1. Přidejte další rozsah pro tabulku **Další pole převodu zásob** . **Pole** nastavte na *Zásady odchozí dodávky* a **Kritéria** nastavte na *Uvolnění a potvrzení expedice* .
1. Přidejte další rozsah pro tabulku **Podrobnosti o nákladu** . **Pole** nastavte na *Odkaz* a **Kritéria** nastavte na *Dodávka převodního příkazu* .
1. Výběrem **OK** se vraťte do hlavního dialogového okna.
1. Rozbalte sekci **Spustit na pozadí** .
1. Povolte **Dávkové zpracování** .
1. Vyberte **Opakování** a nastavte dávkovou úlohu tak, aby prováděla zpracování v intervalu, jaký potřebujete pro svou obchodní činnost.
1. Výběrem **OK** se vraťte do hlavního dialogového okna.
1. Výběrem **OK** v hlavním dialogovém okně přidejte úlohu do fronty dávek.

> [!NOTE]
> Další informace viz [Potvrdit odchozí dodávky z dávkových úloh](confirm-outbound-shipments-from-batch-jobs.md).

## <a name="processing-the-example-for-create-transfer-order-from-the-warehouse-app"></a>Zpracování příkladu „Vytvoření převodních příkazů z aplikace skladu”

### <a name="add-on-hand-on-a-license-plate"></a>Přidání zásob na skladě na registrační značce

Jako výchozí bod pro tento scénář budete muset mít registrační značku obsahující dostupné fyzické zásoby na skladě.

| Zboží | Sklad | Stav skladu | Skladové místo | Registrační značka | Množství |
| --- | --- | --- | --- | --- | --- |
| A0001 | 51 | Dostupné | RZ-010 | RZ10 | 1 |
| A0002 | 51 | Dostupné | RZ-010 | RZ10 | 2 |

Přidejte množství fyzických zásob na skladě pomocí následujících hodnot:

> [!NOTE]
> Budete muset vytvořit registrační značku a používat místa, která vám umožní dopravovat kombinace položek, jako je RZ-010.

### <a name="create-and-process-transfer-orders-from-the-warehouse-app"></a>Vytvářet a zpracovat převodní příkazy z aplikace skladu

1. Otevřete aplikaci a přihlaste se jako uživatel *51* . Aktuální sklad uživatele bude 51.
1. Vyberte položku nabídky **Vytvořit PP** z místa nabídky, které jste přidali během nastavování.
1. Začněte vytvářet převodní příkaz zadáním cílového skladu (Do skladu) v poli **Sklad** – zadejte *61* . Nový převodní příkaz bude směřovat z aktuálního skladu 51 (Ze skladu) do cílového skladu *61* .
1. Vyberte **OK** .
1. Naskenujte ID registrační značky v poli **Registrační značka** . Zadejte registrační značku zásob, kterou jste přidali v předchozím kroku – *RZ10* .
1. Vyberte **OK** .
1. Vyberte tlačítko nabídky a pak výběrem možnosti **Dokončit objednávku** dokončete vytvoření převodního příkazu aplikace skladu.

Pro uvedený příklad se použijí dvě **události aplikace skladu** ( *Vytvoření převodního příkazu* a *Dokončení převodního příkazu* ).

### <a name="inquire-the-warehouse-app-events"></a><a name="#inquire-the-warehouse-app-events"></a>Prošetřování událostí aplikace skladu

Frontu událostí a zprávy o událostech generované aplikací skladu si můžete zobrazit přechodem na **Řízení skladu \> Dotazy a zprávy \> Protokoly mobilních zařízení \> Události aplikace skladu** .

Zprávy o událostech *Vytvoření převodního příkazu* budou mít stav *Čekání* , což znamená, že dávková úloha **Zpracovat události aplikace skladu** nebude tyto zprávy o událostech přebírat a zpracovávat. Jakmile se stav zpráv o událostech aktualizuje na *Ve frontě* , dávková úloha události zpracuje. K tomu dojde současně s vytvořením události *Dokončení převodního příkazu* (když pracovník vybere tlačítko **Dokončit objednávku** v aplikaci skladu). Po zpracování zpráv o událostech *Vytvoření převodního příkazu* se stav aktualizuje na *Dokončeno* nebo *Chyba* . Když je stav události *Dokončení převodního příkazu* aktualizován na *Dokončeno* , všechny související události jsou odstraněny z fronty.

Protože **události aplikace skladu** pro vytvoření dat převodního příkazu nejsou dávkovou úlohou zpracovány, dokud není stav zpráv aktualizován na *Ve frontě* , budete muset vyhledat požadovaná čísla převodních příkazů jako součást pole **Identifikátor** . Pole **Identifikátor** je v záhlaví stránky **Události aplikace skladu** .

V rámci zpracování událostí skladu může selhat vytvoření řádku převodního příkazu. V takovém případě je stav zprávy o události aktualizován na *Chyba* a můžete použít informace **dávkového protokolu** , abyste zjistili důvod a mohli provést příslušnou akci a opravit jakékoli problémy.

Typické problémy mohou souviset s chybějícím nastavením procesu, jako je chybějící tranzitní sklad pro událost *Vytvoření převodního příkazu* . V takovém příkladu byste přidali tranzitní sklad do expedičního skladu a pomocí možnosti **Resetovat** byste změnili stav všech zpráv o událostech aplikace skladu ze stavu *Chyba* na *Ve frontě* , což znamená, že dávková úloha po opravě dat nastavení znovu zpracuje zprávy o událostech.

V produkčním prostředí by výjimky více souvisely s procesem – například byste mohli mít požadovanou registrační značku, která by byla v době zpracování dávkové úlohy prázdná. Nevytvořily by se proto žádné řádky převodního příkazu. Tuto zprávu o události, která selhala, můžete odebrat pomocí možnosti **Odstranit** nebo můžete přidat potřebné fyzické zásoby na skladě v této registrační značce a použít možnost **Resetovat** pro všechny související zprávy o událostech.

Další informace viz [Zpracování událostí aplikace skladu](warehouse-app-events.md).

### <a name="follow-up-on-the-example-scenario-processing"></a>Shrnutí zpracování ukázkového scénáře

Během tohoto scénáře se stalo následující:

1. Pomocí aplikace skladu jste vybrali položku nabídky, která používá kód aktivity **Vytvořit převodní příkaz z registračních značek** .
1. Aplikace vás vyzvala k výběru cílového skladu pro převodní příkaz. Zdrojový sklad je vždy ten, do kterého jste aktuálně přihlášení jako pracovník.
1. Při výběru cílového skladu systém zarezervoval číslo ID pro nadcházející převodní příkaz (na základě číselné řady převodních příkazů definované v systému), ale ještě tento převodní příkaz nevytvořil.
1. Když jste naskenovali registrační značku *RZ10* obsahující zásoby na skladě, který by měly být přesunuty do nového skladu, byla do fronty událostí přidána **událost aplikace skladu** k pozdějšímu zpracování. Tato událost skladu obsahovala podrobnosti zprávy o naskenování včetně zamýšleného čísla převodního příkazu.
1. V aplikaci skladu se při výběru tlačítka **Dokončit objednávku** vytvořila nová událost aplikace skladu **Dokončení převodního příkazu** a stav související existující události **Vytvoření převodního příkazu** se změnil na **Ve frontě** .
1. V back-endovém systému převzala **dávková úloha Zpracovat události aplikace skladu** událost **Ve frontě** a shromáždila zásoby na skladě související s naskenovanou registrační značkou. Na základě těchto zásob na skladě se vytvořil vlastní záznam převodního příkazu a přidružené řádky. Úloha také naplnila pole **Zásady odchozí dodávky** pro tento převodní příkaz pomocí hodnoty založené na nakonfigurovaném nastavení *Uvolnění a potvrzení expedice* a propojila registrační značku s řádky strategie **Registrační značka řízena** .
1. Na základě hodnoty pole **Zásady odchozí dodávky** na řádku tohoto převodního příkazu nyní dotaz **dávkové úlohy Automaticky uvolnit převodní příkazy** vedl k uvolnění převodního příkazu do expedičního skladu. A na základě nastavení použití **šablony vlny** , **šablony práce** a **směrnic skladového místa** byla práce automaticky zpracována s výsledkem, že **Stav nákladu** byl aktualizován na *Naloženo* .
1. Pro daný náklad byla provedena **dávková úloha Zpracovat odchozí dodávku** . Výsledkem bylo expedování převodního příkazu a vygenerování avíza expedice zboží.
1. Načasování všech těchto událostí závisí na nastavení **Opakování** pro vytvořené dávkové úlohy.

## <a name="frequently-asked-questions"></a>Časté dotazy

### <a name="mobile-device-menu-item-setup"></a>Nastavení položky nabídky mobilního zařízení

#### <a name="why-cant-i-see-create-transfer-order-from-license-plate-in-the-menu-item-work-activity-drop-down-list"></a>Proč v rozevíracím seznamu pracovní aktivity položky nabídky nevidím možnost „Vytvořit převodní příkaz z registrační značky“?

Musí být povolená funkce *Vytvářet a zpracovávat převodní příkazy z aplikace skladu* . Další informace viz [Povolení vytváření převodních příkazů z aplikace skladu](#enable-create-transfer-order-from-warehouse-app).

### <a name="warehouse-app-processes"></a>Procesy aplikace skladu

#### <a name="why-cant-i-see-the-menu-button-complete-order"></a>Proč nevidím tlačítko nabídky „Dokončit objednávku“?

K převodnímu příkazu musíte mít přiřazenou alespoň jednu registrační značku.

#### <a name="can-several-warehouse-app-users-add-license-plates-to-the-same-transfer-order-at-the-same-time"></a>Může několik uživatelů aplikace skladu přidávat registrační značky do stejného převodního příkazu současně?

Ano, několik pracovníků skladu může skenovat registrační značky do stejného převodního příkazu.

#### <a name="can-the-same-license-plate-be-added-to-different-transfer-orders"></a>Je možné stejnou registrační značku přidat do různých převodních příkazů?

Ne, registrační značku je možné v dané chvíli přidat pouze do jednoho převodního příkazu.

#### <a name="after-having-selected-the-complete-order-button-can-i-then-add-more-license-plates-for-that-transfer-order"></a>Můžu po výběru tlačítka „Dokončit objednávku“ přidat další registrační značky pro stejný převodní příkaz?

Ne, do převodního příkazu s událostí **Dokončení převodního příkazu** nemůžete přidávat další registrační značky.

#### <a name="how-can-i-find-existing-transfer-orders-to-be-used-via-the-select-transfer-order-button-in-the-warehouse-app-if-the-order-has-not-yet-been-created-in-the-backend-system"></a>Jak najdu existující převodní příkazy k použití prostřednictvím tlačítka „Vybrat převodní příkaz“ v aplikaci skladu, pokud tento příkaz ještě nebyl vytvořen v back-endovém systému?

V současné době nemůžete v této aplikaci převodní příkazy vyhledávat, ale čísla převodních příkazů můžete najít na stránce **Události aplikace skladu** . Další informace viz [Prošetřování událostí aplikace skladu](#inquire-the-warehouse-app-events).

#### <a name="can-i-manually-select-the-transfer-order-number-to-be-used-from-the-warehouse-app"></a>Můžu z aplikace skladu ručně vybrat číslo převodního příkazu, které se má použít?

Podporována jsou pouze automaticky generovaná čísla převodních příkazů na základě číselných řad.

### <a name="background-processing"></a>Zpracování na pozadí

#### <a name="how-should-i-clean-up-records-in-my-warehouse-app-events-queue-message-tables"></a>Jak můžu vyčistit záznamy v tabulkách zpráv fronty událostí aplikace skladu?

Můžete je zobrazit a udržovat na stránce **Události aplikace skladu** . Další informace viz [Prošetřování událostí aplikace skladu](#inquire-the-warehouse-app-events).

#### <a name="why-is-the-transfer-order-receipt-date-not-updated-according-to-my-delivery-date-control-setup"></a>Proč se neaktualizuje „Datum příjmu“ převodního příkazu podle mého nastavení „Řízení data dodání“?

Převodní příkazy se vytváří bez použití funkce **Řízení data dodání** .

#### <a name="can-i-use-a-license-plate-having-physical-negative-inventory-on-hand"></a>Můžu použít registrační značku se zápornými fyzickými zásobami na skladě?

Tato funkce podporuje pouze kladná fyzická množství na skladě. Před přiřazením registračních značek k převodnímu příkazu se ujistěte, že máte kladná fyzická množství na skladě ve skladu a v úrovni stavu zásob.
