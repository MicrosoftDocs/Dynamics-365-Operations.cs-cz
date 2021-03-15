---
title: Nastavení plnění objednávek pro obchody
description: Toto téma poskytuje přehled nastavení plnění obchodu.
author: rubencdelgado
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: rubendel
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8d6cfa0d1eba4ccb0b24839b7cc632835b17107e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965302"
---
# <a name="set-up-order-fulfillment-for-stores"></a>Nastavení plnění objednávek pro obchody

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Přehled

Mnoho maloobchodních prodejců by chtělo optimalizovat plnění objednávky tak, že povolí plnění objednávky obchodům. Plnění objednávek na úrovni obchodu může pomoci zmírnit scénáře přeplnění pro konkrétní obchod, nebo může být zapotřebí z logistického hlediska v případech, kdy má obchod dodatečnou kapacitu nebo je umístěn v těsnější vzdálenosti od zákazníka. Aby se vyhovělo této potřebě, je na pokladním místě k dispozici sjednocená operace plnění objednávky.

Objednávky pro plnění v konkrétním obchodě mají sklad obchodu označený v záhlaví nebo řádcích objednávky.

Operace plnění objednávky na pokladním místě poskytuje jediný pracovní prostor v pokladním místě, který lze použít pro zpracování objednávek. To obsahuje vše, od přijetí objednávky až po její označení jako vyexpedované nebo inicializování vyzvednutí v obchodě.

## <a name="set-up-the-order-fulfillment-operation"></a>Nastavení operace plnění objednávky

Plnění objednávky [ID operace 928](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-operations) lze použít pro přístup k pracovní oblasti plnění objednávky obchodu v pokladním místě.

Postupujte podle kroků v části [Přidat operaci do mřížky tlačítek](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) a určete, který parametr má být použit při vyvolání plnění objednávky na pokladním místě. Ve výchozím nastavení se zvolí **Všechny objednávky** po určení operací plnění objednávky. Když je nakonfigurována s tímto parametrem, operace uvede seznam všech řádků objednávky pro plnění v aktuálním obchodě. Je k dispozici také možnost **Objednávky k expedici**, kterou lze přiřadit k tlačítku a využít v případě, že uživatel pouze chce zobrazit objednávky, které budou expedovány z obchodu. Nakonec je tu možnost **Objednávky k výdeji**. Při vyvolání na pokladním místě se uvede pouze seznam objednávek, které mají být vyzvednuty v obchodě. Různé parametry lze přiřadit různým tlačítkům, aby měl uživatel k dispozici různé způsoby zobrazení plnění objednávek.

### <a name="enable-users-to-access-order-fulfillment-at-the-point-of-sale"></a>Povolte uživatelům přístup k plnění objednávek na pokladním místě.

Operace plnění objednávky nemá momentálně vlastní oprávnění, ale v budoucnosti mohou uživatelé vyžadovat oprávnění **Povolit načtení objednávky** k vyvolání operace z pokladního místa.

Na úrovni obchodu je k dispozici nastavení konfigurace k určení, zda řádek objednávky musí být přijat ručně z pokladního místa. Pokud tato možnost konfigurace není nastavena, řádky objednávky budou přijaty ve výchozím nastavení. Pokud je tato možnost konfigurace zapnuta, uživatelé budou muset na pokladním místě mít oprávnění **Povolit přijetí objednávky** pro příjem objednávek z pokladního místa.

### <a name="enable-manual-order-acceptance"></a>Povolení ručního přijetí objednávky

Ve výchozím nastavení jsou řádky objednávky přiřazené k obchodu označené jako **Přijato**. To znamená, že se předpokládá, že budou plněny z přiřazeného obchodu a nebudou podléhat dalšímu přiřazení. V určitých případech mohou maloobchodní prodejci chtít ručně přijmout objednávky předtím, než mohou být plněny. Například pokud má obchod nedostatek zaměstnanců a není schopen plnit objednávky, manažer obchodu přijme pouze tolik objednávek ke zpracování, které podle jeho soudu lze v daný den splnit. Dokud není objednávka přijata, může být opětovně přidělena účetním systémem do jiného obchodu. Tímto způsobem poskytuje přijetí objednávky způsob označení, že byla objednávka potvrzena obchodem a bude plněna.

Řádky objednávky pro vyzvednutí v obchodě jsou vždy označeny jako **Čekající** a nepodléhají přijetí.

Chcete-li zapnout ruční přijetí řádků objednávky, přejděte na **Maloobchod a velkoobchod** \> **Kanály** \> **Obchody** \> **Všechny obchody**. Vyberte obchod a klikněte na ID obchodu, chcete-li zobrazit podrobnosti obchodu. Klikněte na možnost **Upravit**. Na pevné záložce **Obecné** vyhledejte dílčí záhlaví **Plnění objednávky** a změňte **Ruční přijetí** z **Ne** na **Ano**.

### <a name="enable-reject-order-line-capability"></a>Povolit možnost odmítnutí řádku objednávky

Řádky objednávky mohou být také odmítnuty z pokladního místa. Zamítnutí řádku objednávky znamená, že nebude plněna v obchodě, a odešle řádek objednávky zpět pro opětovné přiřazení do jiného obchodu nebo skladu. Oprávnění pro odmítnutí řádku objednávky, je udělováno prostřednictvím oprávnění **Povolit odmítnout objednávky** ve skupině oprávnění POS přidružené k pracovníkovi. Při odmítnutí řádku mohou maloobchodní prodejci zmocnit své pracovníky k poskytnutí důvodu odmítnutí. Toho lze dosáhnout pomocí informačních kódů **Aktivita informačního kódu** typu **Plnění objednávky** a přiřazením informační kódu k položce **Zamítnout řádek objednávky** ve funkčním profilu přidruženém ke kanálu.

> [!NOTE]
> Pouze informační kódy **Aktivita informačního kódu** typu **Plnění objednávky** lze přiřadit k akci **Zamítnout řádek objednávky**.

### <a name="synchronize-changes-to-the-channel-database"></a>Synchronizace změn do databáze kanálu

Poté, co byla operace přiřazena k mřížce tlačítek, byla přiřazena správná oprávnění je nakonfigurován kanál, změny musí být synchronizovány s databází kanálu. Postupujte tak, že přejdete na **Maloobchod a velkoobchod** \> **IT pro maloobchod a velkoobchod** \> **Plán distribuce**. Vyberte plán „1090, Pokladny“ za účelem synchronizace změn mřížky tlačítek a poté klikněte na **Spustit**. Dále synchronizujte změny oprávnění volbou „1060, Zaměstnanci“ a klikněte na tlačítko **Spustit**. Dále synchronizujte změny kanálu volbou „1070, Konfigurace kanálu“ a klikněte na tlačítko **Spustit**. Nakonec synchronizujte nově vytvořený informační kód pro důvod odmítnutí výběrem „1110, Globální konfigurace“ a klikněte na tlačítko **Spustit**.

## <a name="use-order-fulfillment-at-the-point-of-sale"></a>Použití plnění objednávky na pokladním místě

Otevřete pokladní místo a zvolte operaci plnění objednávky. V závislosti na konfiguraci budou uvedeny všechny řádky, řádky objednávky pro výdej nebo řádky objednávky k expedici.

### <a name="order-fulfillment-view"></a>Zobrazení plnění objednávek

Zobrazení plnění objednávek zobrazuje seznam řádků objednávky pro plnění v obchodě a obsahuje následující sloupce:

- Číslo objednávky
- Číslo produktu
- popis
- Objednané množství
- Požadované datum dodání
- Jméno zákazníka
- Stav plnění

Další informace pro konkrétní řádek objednávky lze zobrazit výběrem řádku objednávky a potom otevřením plovoucího panelu umístěného pod přihlášeným uživatelem/informace o změně zobrazená na záhlaví pokladního místa. Tato nabídka obsahuje 2 karty: jednu pro podrobnosti řádku a druhou pro podrobnosti o objednávce. Karta podrobností řádku obsahuje následující informace:

- Objednané množství
- Zboží zbývající k expedici/vyzvednutí
- Vyskladněné množství
- Zabalené množství
- Fakturované množství (již vyskladněné nebo expedované)
- Způsob dodání
- Adresa dodání

Plovoucí panel podrobností má také kartu, která poskytuje další podrobnosti úrovně objednávky, včetně:

- Jméno zákazníka
- ID odběratele
- Číslo objednávky
- Celková hodnota objednávky
- Zůstatek objednávky

Ve spodní části zobrazení plnění objednávky je podokno akcí. To obsahuje všechny akce, které lze provést proti řádku objednávky. Pokud není akce k dispozici na základě stavu řádku, akce nebude k dispozici.

Ve výchozím nastavení objednávky budou mít stav **Přijato**. Stav objednávky lze zobrazit jako sloupec v seznamu řádků objednávky. Pokud je položka **Ruční přijetí** konfigurována na úrovni kanálu, všechny řádky, které mají být expedovány, se zobrazí jako **Čekající** a musí být přijaty dříve, než mohou být plněny. Objednávky pro vyzvednutí v obchodě jsou ve výchozím nastavení **Čekající** a nemusí být přijaty.

### <a name="order-fulfillment-line-actions"></a>Akce řádku plnění objednávky

- **Upravit** - pokud je stav objednávky čekající, lze ho upravit na pokladním místě. Objednávky, které již byly částečně vyskladněné, zabalené nebo fakturované, nemohou být upraveny ze zobrazení plnění objednávky.
- **Přijmout** - pokud je položka **Ruční přijetí** nakonfigurována na úrovni kanálu, řádky musí být nejprve přijaty, dříve než mohou procházet proces plnění objednávky.
- **Vyskladnit** -možnost vyskladnění podporuje několik akcí. Nejprve **Výdej** aktualizuje stav řádku objednávky, aby se ostatní v obchodě nepokusili vyskladnit stejný řádek. Dále **Tisk výdejky** vytiskne výdejku pro vybraný řádek nebo řádky a aktualizuje jejich stav na **Výdej**. Formáty výdejek jsou ovládány jako součást formátů příjemek. Další informace o nastavení formátů příjemek naleznete v tématu [Šablony pro příjemky a tisk](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing). Nakonec možnost **Označit jako vyskladněno** označuje, že řádek byl vyskladněn. **Označit jako vyskladněno** zahájí odpovídající skladové transakce v účetním systému. Akce výdeje lze provést zároveň současně pro několik řádků objednávky napříč objednávkami a pro všechny způsoby dodání.
- **Zamítnout** - Řádky nebo částečné řádky lze odmítnout. To umožňuje jejich opětovné přiřazení z účetního systému do jiného obchodu nebo skladu. Řádky lze zamítnout pouze tehdy, pokud nebyly ještě vyskladněny či zabaleny. Chcete-li odmítnout řádek, který byl vyskladněn nebo zabalen, musí být u toho řádku zrušeno vydání nebo zabalení z účetního systému.
- **Balení** - možnost balení podporuje dvě akce: **Tisk dodacího listu** vytiskne dodací list pro vybrané řádky a položka **Označit jako zabaleno** označí řádky jako zabalené a označit řádky jako dodané v účetním systému. Současně lze zabalit pouze řádky objednávky, které patří ke stejné objednávce a se stejným způsobem dodání. Formáty dodacích listů jsou ovládány jako součást formátů příjemek. Další informace o nastavení formátů příjemek naleznete v tématu [Šablony pro příjemky a tisk](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing).
- **Expedovat** - akce expedice označí vybrané řádky jako **Dodáno** v účetním systému. Poté, co byl řádek plně expedován, se již nezobrazí v zobrazení plnění objednávky.
- **Výdej** - akce vyskladnění přidá řádky k zobrazení transakcí pro výdej. Pokud neexistují další řádky na objednávce, které nejsou aktuálně vydávány, budou přidány k zobrazení transakcí s nulovým množstvím. Poté, co byl řádek plně vydán, se již nezobrazí v zobrazení plnění objednávky.

### <a name="order-fulfillment-filtering"></a>Filtrování plnění objednávek

Plnění objednávky na pokladním místě obsahuje filtrování umožňující uživateli snadné vyhledávání podle potřeb. Filtry lze změnit na spodní části podokna akcí na obrazovce **Pokladní místo**. Ve výchozím nastavení je použit filtr **Typ dodání**, podle nastavení operace. Je-li operaci nastavena s parametrem **Všechny objednávky**, pak se daný filtr použije při přístupu k plnění objednávky. To platí i pro parametry **Vyzvednutí v obchodě** a **Expedovat z obchodu**. Jiné filtry, které lze použít k zobrazení plnění objednávky, zahrnují:

- Název zákazníka
- Jméno zákazníka
- E-mail odběratele
- Číslo objednávky
- Způsob dodání
- Číslo příjemky
- ID odkazu na kanál
- Původní číslo obchodu
- Stav řádku
- Vytvořeno
- Datum dodání
- Datum příjmu


[!INCLUDE[footer-include](../includes/footer-banner.md)]