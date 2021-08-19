---
title: Nadměrné vyskladnění u prodejních objednávek a převodních příkazů
description: Toto téma vysvětluje, jak povolit nadměrné vyskladnění u prodejních objednávek a převodních příkazů.
author: GalynaFedorova
ms.date: 07/06/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-06
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3c6f9d386f79754edce38e4e2cf4c9bfefbce69bdb252e8754f39d909827fa02
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722144"
---
# <a name="over-picking-for-sales-orders-and-transfer-orders"></a>Nadměrné vyskladnění u prodejních objednávek a převodních příkazů

[!include [banner](../includes/banner.md)]

Toto téma představuje scénář ukazující, jak povolit výběr konkrétního pracovníka nebo všech pracovníků pro nadměrné vyskladnění. Proces nadměrného vyskladnění umožňuje řízené nadměrné vyskladnění během práce výdeje.

Nadměrné vyskladnění zboží ze skladů je jednoduchý koncept. Systém umožňuje pracovníkům vybrat více položek, než je uvedeno v objednávce. Stále však bere do úvahy limit nadměrného doručení, který je nastaven na úrovni řádku převodního příkazu nebo prodejní objednávky. Pokud je tento limit překročen, aplikace Warehouse Management upozorní pracovníky, že překračují limit nadměrného doručení.

Funkce nadměrného vyskladnění pomáhá minimalizovat údržbu a také pomáhá zachovat flexibilitu vašeho nastavení. Můžete definovat jednu nebo více položek nabídky mobilního zařízení a povolit nadměrné vyskladnění pouze u některých z nich. Vybraným pracovníkům můžete také zabránit v nadměrném vyskladnění prodejních objednávek a/nebo převodních příkazů, aniž byste museli měnit položky nabídky. Místo toho můžete v příslušných nastaveních pracovníků vypnout jednu nebo obě tyto funkce.

Funkce nadměrného vyskladnění může pracovníkům ušetřit čas a námahu při vyskladňování a odesílání položek. Tato funkce například umožňuje pracovníkům provádět tyto úkoly:

- Kompenzovat zmenšování během vyskladnění nebo přepravy.
- Během vyskladnění se vyhnout nutnosti rozbalit nějaký obalový materiál.
- Kompenzovat poškození položky během přepravy.
- Odeslat odchylku množství nebo měrné jednotky.
- Minimalizovat nedodržení uvedených množství na registračních značkách.
- Vyhnout se plýtvání materiálem a nedostatku drahých materiálů.
- Změřit po vyzvednutí celkové vyzvednuté množství (například vážením nákladního vozidla).

> [!IMPORTANT]
> Funkce nadměrného vyskladnění se vztahuje pouze na vyzvednutí a zpracování prodejní objednávky a převodního příkazu. U doplňování není nadměrný výběr možný. Když jsou spuštěny práce doplňování, systém nedovolí uživatelům nadměrný výběr.

Scénář v tomto tématu ukazuje, jak funkci nadměrného vyskladnění nastavit a používat.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Předpoklad scénáře: Zpřístupnit ukázková data

Scénář v tomto tématu odkazuje na hodnoty a záznamy, které jsou součástí standardních ukázkových dat poskytovaných pro aplikaci Microsoft Dynamics 365 Supply Chain Management. Pokud chcete při cvičení použít hodnoty, které jsou zde uvedeny, nezapomeňte pracovat v prostředí, ve kterém jsou nainstalovaná ukázková data, a nastavte právnickou osobu na *USMF*, než začnete.

## <a name="scenario-setup"></a>Nastavení scénáře

Před zpracováním ukázkového scénáře musíte povolit nadměrné vyskladnění pro příslušného pracovníka i příslušnou položku nabídky.

### <a name="set-up-a-worker-to-allow-for-over-picking"></a>Nastavení nadměrného vyskladnění pro pracovníka

Zde je obecný postup konfigurace pracovníka, aby mohl používat nadměrné vyskladňování odděleně u prodejních objednávek a převodních příkazů. Tato konfigurace určuje, který výdejní pracovník může provést nadměrné vyskladnění a zda tento pracovník může provádět nadměrné vyskladnění jak u prodejních objednávek, tak převodních příkazů.

1. Přejděte do nabídky **Řízení skladu \> Nastavení \> Pracovník**.
1. V podokně seznamu vyberte **Julia Funderburk**.
1. Na pevné záložce **Uživatelé** vyberte řádek, který má následující hodnoty. Pokud žádný z těchto řádků nemá tyto hodnoty, vytvořte je.

    - **ID uživatele:** *24*
    - **Uživatelské jméno:** *WH 24*
    - **Výchozí sklad:** *24*
    - **Název nabídky:** *Hlavní*

1. Na pevné záložce **Práce** nastavte následující hodnoty pro uživatele *24*, pokud ještě nejsou nastaveny:

    - **Povolit nadměrné vyskladnění prodeje:** *Ano*
    - **Povolit nadměrné vyskladnění převodního příkazu:** *Ano*

### <a name="set-up-a-mobile-device-menu-item-to-allow-for-over-picking"></a>Nastavení položky nabídky na mobilním zařízení pro povolení nadměrného vyskladnění

Zde je obecný postup pro konfiguraci položky nabídky mobilního zařízení, aby bylo povoleno nadměrné vyskladnění. V závislosti na vašich obchodních požadavcích pro úroveň oprávnění pracovníka, který bude používat nabídku mobilního zařízení, mohou být některé parametry zapnuty nebo vypnuty.

1. Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.
1. V podokně seznamu vyberte záznam s názvem *Prodejní výdej*. Pokud žádná položka nemá tento název, vytvořte ji. Potvrďte nebo nastavte pro záznam následující hodnoty:

    - **Název položky nabídky:** *Prodejní výdej*
    - **Nadpis:** *Prodejní výdej*
    - **Režim:** *Práce*
    - **Použít existující práci:** - *Ano*
    - **Řídí:** *Řízeno uživatelem*
    - **Přepsat cílovou registrační značku vozidla:** *Ano*
    - **Přepsat registrační značku během vložení:** *Ano*
    - **Ponechat práci uzamčenou uživatelem:** *Ano*
    - **Povolit nadměrné vyskladnění:** *Ano*

> [!IMPORTANT]
> Poté, co jsou povoleny relevantní parametry pro pracovníka i položku nabídky mobilního zařízení, lze nadměrné vyskladnění zpracovat pouze prostřednictvím mobilního zařízení.

## <a name="example-scenario"></a>Příklad

Jakmile jsou splněny předpoklady, dokončeno nastavení pracovníka a nastavení položky nabídky, jste připraveni s funkcí pracovat.

### <a name="create-a-sales-order-that-allows-for-overdelivery"></a>Vytvoření prodejní objednávky, která umožňuje nadměrné vyskladnění

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Výběrem položky **Nová** vytvořte novou prodejní objednávku.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - **Účet zákazníka:** *US-001*
    - **Sklad:** *24*

1. Vyberte **OK**.
1. Otevře se nová prodejní objednávka. Na pevné záložce **Řádky prodejní objednávky** přidejte řádek s následujícím nastavením:

    - **Číslo položky:** *A0001*
    - **Množství:** *10*

1. Na pevné záložce **Podrobnosti řádku** na kartě **Dodání** nastavte pole **Navýšení dodávky** na *10*.
1. Na pevné záložce **Řádky prodejních objednávek** vyberte **Zásoby \> Rezervace**.
1. Na stránce **Rezervace** v podokně Akce vyberte **Rezervovat šarži** pro rezervaci zásob.
1. Zavřete stránku **Rezervace**.
1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.

Když je dokončeno uvolnění, obdržíte informační zprávy znázorňující ID vlny a ID nákladu, jež byly vytvořeny.

### <a name="get-the-work-id-and-license-plate-number-for-the-new-order"></a>Načtěte ID práce a registrační značku pro novou objednávku

Když jste uvolnili prodejní objednávku do skladu, systém by měl vytvořit nové ID práce, které má jeden řádek výdeje. Podle těchto pokynů vyhledejte ID práce a přiřazení registrační značky.

1. Přejděte do **Řízení skladu \> Práce \> Podrobnosti práce**.
1. V mřížce **Přehled** vyhledejte ve sloupci **Číslo objednávky** právě vytvořenou prodejní objednávku. Pro tuto prodejní objednávku si poznamenejte odpovídající ID práce.
1. Výběrem řádku nové prodejní objednávky v něm zobrazíte související informace v mřížce **Řádky**. Poznamenejte si skladové místo, ze kterého bude položka vydána.
1. Přejděte na **Řízení zásob \> Dotazy a sestavy \> Zásoby na skladě**.
1. V podokně akcí zvolte **Rozměry**.
1. V dialogovém okně **Zobrazení dimenze** zkontrolujte, že jsou zaškrtnuta políčka **Registrační značka**, **Sklad** a **Číslo položky** a poté vyberte **OK**.
1. V podokně **Filtr** nastavte následující filtry:

    - **Číslo položky** – **je jedním z** – *A0001*
    - **Sklad** – **začíná na** – *24*

1. Zvolte **Použít**.
1. Poznamenejte si zobrazené hodnoty pro **registrační značku**.

### <a name="over-pick-the-order-by-using-the-warehouse-management-mobile-app"></a>Nadměrně vyskladnění objednávky pomocí mobilní aplikace Warehouse Management

1. Přihlaste se do mobilní aplikace Řízení skladu jako uživatel skladu *24*.
1. Přejděte do **Výstupní \> Prodejní výdej**.
1. V poli **Naskenujte ID práce nebo reg. značku** zadejte ID práce, které bylo vytvořeno pro prodejní objednávku.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).
1. Vyberte **Nadměrné vyskladnění**.
1. Nastavte pole **Vyskladněné množství** na hodnotu *14*.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).

    Na stránce **Nadměrné vyskladnění** se zobrazí následující zpráva: „Nadměrné doručení řádku je 40,00 procent, ale povolené nadměrné doručení je pouze 10,00 procent." Tato zpráva označuje, že vyskladněné množství, které jste zadali, překračuje limit nadměrného doručení. Limit nadměrného doručení u řádku prodejní objednávky je 10 procent. Proto při zadaném množství 10 můžete navíc vyskladnit pouze 1 jednotku, tedy celkové množství bude 11.

1. Nastavte pole **Vyskladněné množství** na hodnotu *11*.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).
1. V poli **Poznávací značka** zadejte registrační značku, kterou jste si poznamenali v předchozí části.
1. V poli **Cílová registrační značka** zadejte cílovou registrační značku. Všimněte si, že se zobrazí místo výběru (*FLOOR-001*), položka (*A0001*) a množství (*11 ks*).
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).
1. Zkontrolujte informace na stránce **prodejní objednávky: vložení**. V poli **Místo** by mělo být uvedeno, že vybrané položky jdou do umístění *BAYDOOR*.
1. Vyberte tlačítko **OK** (symbol zaškrtnutí).

Na stránce **Naskenujte ID práce / ID registrační značky** se zobrazí zpráva „Práce dokončena“. Tato zpráva indikuje, že ID práce prodejní objednávky bylo dokončeno a nadměrně vybrané množství nepřekračuje limit 10 procent.
