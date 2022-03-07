---
title: Správa zákazníků v obchodech
description: Toto téma vysvětluje, jak mohou maloobchodníci povolit funkce správy zákazníků v místě prodeje (POS) v Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 46a18d36a389e8a52253c2c3a153e0eae95c0e57
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799414"
---
# <a name="customer-management-in-stores"></a>Správa zákazníků v obchodech

[!include [banner](includes/banner.md)]

Toto téma vysvětluje, jak mohou maloobchodníci povolit funkce správy zákazníků v místě prodeje (POS) v Microsoft Dynamics 365 Commerce.

Je důležité, aby spolupracovníci obchodu mohli vytvářet a upravovat záznamy zákazníků na POS. Tímto způsobem mohou zaznamenávat jakékoli aktualizace informací o zákaznících, jako je e-mailová adresa, telefonní číslo a adresa. Tyto informace jsou užitečné v následných systémech, jako je marketing, protože účinnost těchto systémů závisí na přesnosti jejich údajů o zákaznících.

Pracovníci prodeje mohou spustit pracovní postup vytváření zákazníků ze dvou vstupních bodů POS. Mohou vybrat tlačítko, které je namapováno na operaci **Přidat zákazníka** nebo mohou vybrat **Vytvořit zákazníka** na panelu aplikací na stránce s výsledky vyhledávání. V obou případech se zobrazí dialogové okno **Nový zákazník**, kde prodejní spolupracovníci mohou zadat požadované údaje o zákazníkovi, například jméno zákazníka, e-mailovou adresu, telefonní číslo, adresu a jakékoli další informace, které jsou relevantní pro danou firmu. Tyto další informace lze zachytit pomocí atributů zákazníka, které jsou spojeny se zákazníkem. Další informace o atributech zákazníka najdete v části [Atributy zákazníka](dev-itpro/customer-attributes.md).

Obchodní spolupracovníci mohou také zaznamenávat sekundární e-mailové adresy a telefonní čísla. Kromě toho mohou zachytit preference zákazníka ohledně přijímání marketingových informací prostřednictvím kterékoli z těchto sekundárních e-mailových adres nebo telefonních čísel. K aktivaci této funkce musí maloobchodníci zapnout funkci **Zaznamenat více e-mailů a telefonních čísel a souhlas s marketingem těchto kontaktů** v pracovním prostoru **Správa funkcí** v centrále Commerce (**Správa systémů \> Pracovní prostory \> Správa funkcí**).

## <a name="default-customer-properties"></a>Výchozí vlastnosti zákazníka

Maloobchodníci mohou použít stránku **Všechny obchody** v ústředí Commerce (**Retail a Commerce \> Kanály \> Obchody**) a přidružit výchozího zákazníka ke každému obchodu. Commerce poté zkopíruje vlastnosti definované pro výchozího zákazníka do všech nových záznamů o zákazníkovi, které jsou vytvořeny. Například dialogové okno **Vytvořit zákazníka** zobrazuje vlastnosti, které jsou zděděny od výchozího zákazníka, který je přidružen k obchodu. Mezi tyto vlastnosti patří typ zákazníka, skupina zákazníků, předvolba účtenky, měna a jazyk. Jakékoli přidružení (seskupení zákazníků) se dědí také od výchozího zákazníka. Finanční dimenze se však dědí ze skupiny zákazníků, která je přidružena k výchozímu zákazníkovi, nikoli od samotného výchozího zákazníka.

Prodejní spolupracovníci mohou pro zákazníka zachytit více adres. Jméno a telefonní číslo zákazníka se dědí z kontaktních informací, které jsou spojeny s každou adresou. Karta s náhledem **Adresy** záznamu zákazníka obsahuje pole **Účel**, které mohou prodejní spolupracovníci upravit. Pokud je typ zákazníka **Osoba**, výchozí hodnota je **Domov**. Pokud je typ zákazníka **Organizace**, výchozí hodnota je **Sídlo**. Mezi další hodnoty, které toto pole podporuje, patří **Domov**, **Kancelář** a **Poštovní schránka**. Hodnota pole **Země** pro adresu je zděděna z primární adresy, která je uvedena na stránce **Provozní jednotka** stránka v centrále Commerce v nabídce **Správa organizace \> Organizace \> Provozní jednotky**.

## <a name="sync-customers-and-async-customers"></a>Synchronní zákazníci a asynchronní zákazníci

V Commerce existují dva režimy vytváření zákazníků: Synchronní (nebo Sync) a Asynchronní (nebo Async). Ve výchozím nastavení jsou zákazníci vytvářeni synchronně. Jinými slovy jsou vytvářeni v ústředí Commerce v reálném čase. Režim vytváření zákazníků Sync je výhodný, protože noví zákazníci jsou okamžitě prohledatelní napříč kanály. Má to však také nevýhodu. Protože to generuje volání [Commerce Data Exchange: služba v reálném čase](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) volání do centrály Commerce, výkon může být ovlivněn, pokud se uskuteční mnoho souběžných volání vytváření zákazníků.

Pokud je možnost **Vytvořit zákazníka v asynchronním režimu** je nastavena na **Ano** v profilu funkce obchodu (**Retail a Commerce \> Nastavení kanálu \> Nastavení internetového obchodu \> Profily funkčnosti**), volání služby v reálném čase se nepoužívají k vytváření záznamů o zákaznících v databázi kanálů. Režim vytváření asynchronních zákazníků nemá vliv na výkon centrály Commerce. Každému novému záznamu zákazníka Async je přiřazen dočasný globálně jedinečný identifikátor (GUID), který se použije jako ID zákaznického účtu. Tento identifikátor GUID se uživatelům POS nezobrazuje. Místo toho se těmto uživatelům zobrazí **Čeká se na synchronizaci** jako ID zákaznického účtu. Ačkoli tato konfigurace nutí zákazníky, aby byli vytvářeni asynchronně, mějte na paměti, že úpravy záznamů zákazníků se vždy provádějí synchronně.

### <a name="convert-async-customers-to-sync-customers"></a>Převedení asynchronních zákazníků na synchronní zákazníky

Chcete-li převést zákazníky Async na zákazníky Sync, musíte nejprve spustit P-úlohu a odeslat zákazníky Async do centrály Commerce. Poté spusťte úlohu **Synchronizovat zákazníky a obchodní partnery z asynchronního režimu** k vytvoření ID zákaznického účtu. Nakonec spusťte úlohu **1010** k synchronizaci nových ID zákaznických účtů s kanály.

### <a name="async-customer-limitations"></a>Omezení asynchronních zákazníků

Funkce asynchronních zákazníků má v současné době následující omezení:

- Asynchronní záznamy o zákaznících nelze upravovat, pokud nebyl zákazník vytvořen v ústředí Commerce a nové ID zákaznického účtu nebylo synchronizováno zpět do kanálu.
- Přidružení nelze spojit se zákazníky Async. Proto noví zákazníci Async nezdědí přidružení od výchozího zákazníka.
- Věrnostní karty nelze vydat zákazníkům Async, pokud nebylo nové ID zákaznického účtu synchronizováno zpět do kanálu.
- Sekundární e-mailové adresy a telefonní čísla nelze pro zákazníky Async zachytit.

### <a name="customer-creation-in-pos-offline-mode"></a>Vytváření zákazníka v offline režimu POS

Pokud POS přejde do režimu offline, zatímco je povolen režim vytváření asynchronních zákazníků, nové záznamy zákazníků se vytvářejí asynchronně. Pokud POS přejde do režimu offline, když je deaktivován režim vytváření zákazníků Async, systém se automaticky přepne do režimu vytváření zákazníků Async. Jinými slovy záznamy zákazníka mohou být vytvořeny asynchronně, i když je režim vytváření asynchronních zákazníků deaktivován. Proto musí správci centrály Commerce vytvořit a naplánovat opakovanou dávkovou úlohu pro P-úlohu **Synchronizovat zákazníky a obchodní partnery z asynchronního režimu** a úlohu **1010**, aby byli všichni zákazníci Async převedeni na zákazníky Sync v centrále Commerce.

> [!NOTE]
> Pokud je možnost **Filtrovat sdílené tabulky údajů o zákaznících** nastavena na **Ano** na stránce **Schéma obchodního kanálu** (**Retail a Commerce \> Nastavení Commerce \> Plánovač Commerce \> Skupina databáze kanálů**), záznamy zákazníků se nevytvářejí v režimu offline POS. Další informace viz [Vyloučení dat offline](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Další prostředky

[Atributy odběratele](dev-itpro/customer-attributes.md)

[Vyloučení dat offline](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
