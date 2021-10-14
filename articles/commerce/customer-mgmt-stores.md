---
title: Správa zákazníků v obchodech
description: Toto téma vysvětluje, jak mohou maloobchodníci povolit funkce správy zákazníků v místě prodeje (POS) v Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4fd6039843be09ec706e45746d5724faa99a95e6
ms.sourcegitcommit: 3f59b15ba7b4c3050f95f2b32f5ae6d7b96e1392
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563054"
---
# <a name="customer-management-in-stores"></a>Správa zákazníků v obchodech

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Toto téma vysvětluje, jak mohou maloobchodníci povolit funkce správy zákazníků v místě prodeje (POS) v Microsoft Dynamics 365 Commerce.

Je důležité, aby spolupracovníci obchodu mohli vytvářet a upravovat záznamy zákazníků na POS. Tímto způsobem mohou zaznamenávat jakékoli aktualizace informací o zákaznících, jako je e-mailová adresa, telefonní číslo a adresa. Tyto informace jsou užitečné v následných systémech, jako je marketing, protože účinnost těchto systémů závisí na přesnosti jejich údajů o zákaznících.

Pracovníci prodeje mohou spustit pracovní postup vytváření zákazníků ze dvou vstupních bodů POS. Mohou vybrat tlačítko, které je namapováno na operaci **Přidat zákazníka** nebo mohou vybrat **Vytvořit zákazníka** na panelu aplikací na stránce s výsledky vyhledávání. V obou případech se zobrazí dialogové okno **Nový zákazník**, kde prodejní spolupracovníci mohou zadat požadované údaje o zákazníkovi, například jméno zákazníka, e-mailovou adresu, telefonní číslo, adresu a jakékoli další informace, které jsou relevantní pro danou firmu. Tyto další informace lze zachytit pomocí atributů zákazníka, které jsou spojeny se zákazníkem. Další informace o atributech zákazníka najdete v části [Atributy zákazníka](dev-itpro/customer-attributes.md).

Obchodní spolupracovníci mohou také zaznamenávat sekundární e-mailové adresy a telefonní čísla. Kromě toho mohou zachytit preference zákazníka ohledně přijímání marketingových informací prostřednictvím kterékoli z těchto sekundárních e-mailových adres nebo telefonních čísel. K aktivaci této funkce musí maloobchodníci zapnout funkci **Zaznamenat více e-mailů a telefonních čísel a souhlas s marketingem těchto kontaktů** v pracovním prostoru **Správa funkcí** v centrále Commerce (**Správa systémů \> Pracovní prostory \> Správa funkcí**).

## <a name="default-customer-properties"></a>Výchozí vlastnosti zákazníka

Maloobchodníci mohou použít stránku **Všechny obchody** v ústředí Commerce (**Retail a Commerce \> Kanály \> Obchody**) a přidružit výchozího zákazníka ke každému obchodu. Commerce poté zkopíruje vlastnosti definované pro výchozího zákazníka do všech nových záznamů o zákazníkovi, které jsou vytvořeny. Například dialogové okno **Vytvořit zákazníka** zobrazuje vlastnosti, které jsou zděděny od výchozího zákazníka, který je přidružen k obchodu. Mezi tyto vlastnosti patří **typ zákazníka**, **skupina zákazníků**, **možnost účtenky**, **e-mail příjemce**, **měna** a **jazyk**. Jakékoli **přidružení** (seskupení zákazníků) se dědí také od výchozího zákazníka. **Finanční dimenze** se však dědí ze skupiny zákazníků, která je přidružena k výchozímu zákazníkovi, nikoli od samotného výchozího zákazníka.

> [!NOTE]
> Hodnota **e-mailu s účtenkou** se zkopíruje z výchozího zákazníka pouze v případě, že pro nově vytvořené zákazníky není poskytnuto ID e-mailu s potvrzením. To znamená, že pokud je ID výchozího e-mailu k dispozici u výchozího zákazníka, pak všichni zákazníci vytvoření z webu elektronického obchodování obdrží stejné ID e-mailové účtenky, protože neexistuje žádné uživatelské rozhraní, které by od zákazníka zachytilo ID e-mailu s účtenkou. Doporučujeme vám ponechat pole **e-mail s účtenkou** prázdné pro výchozího zákazníka obchodu a použít jej pouze v případě, že máte obchodní proces, který závisí na přítomné e-mailové adrese s účtenkou. 

Prodejní spolupracovníci mohou pro zákazníka zachytit více adres. Jméno a telefonní číslo zákazníka se dědí z kontaktních informací, které jsou spojeny s každou adresou. Karta s náhledem **Adresy** záznamu zákazníka obsahuje pole **Účel**, které mohou prodejní spolupracovníci upravit. Pokud je typ zákazníka **Osoba**, výchozí hodnota je **Domov**. Pokud je typ zákazníka **Organizace**, výchozí hodnota je **Sídlo**. Mezi další hodnoty, které toto pole podporuje, patří **Domov**, **Kancelář** a **Poštovní schránka**. Hodnota pole **Země** pro adresu je zděděna z primární adresy, která je uvedena na stránce **Provozní jednotka** stránka v centrále Commerce v nabídce **Správa organizace \> Organizace \> Provozní jednotky**.

## <a name="sync-customers-and-async-customers"></a>Synchronní zákazníci a asynchronní zákazníci

> [!IMPORTANT]
> Kdykoli POS přejde do režimu offline, systém automaticky asynchronně vytvoří zákazníky, a to i v případě, že je zakázán režim asynchronního vytváření zákazníků. Proto bez ohledu na váš výběr mezi synchronním a asynchronním vytvářením zákazníků musí správci centrály Commerce vytvořit a naplánovat opakující se dávkovou úlohu pro **P-práci**, úlohy **Synchronizovat zákazníky a obchodní partnery z asynchronního režimu** (dříve nazvanou **Synchronizovat zákazníky a obchodní partnery z asynchronního režimu**) a úlohu **1010**, aby byli všichni asynchronní zákazníci převedeni na synchronní zákazníky v centrále Commerce.

V Commerce existují dva režimy vytváření zákazníků: Synchronní (nebo Sync) a Asynchronní (nebo Async). Ve výchozím nastavení jsou zákazníci vytvářeni synchronně. Jinými slovy jsou vytvářeni v ústředí Commerce v reálném čase. Režim vytváření zákazníků Sync je výhodný, protože noví zákazníci jsou okamžitě prohledatelní napříč kanály. Má to však také nevýhodu. Protože to generuje volání [Commerce Data Exchange: služba v reálném čase](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) volání do centrály Commerce, výkon může být ovlivněn, pokud se uskuteční mnoho souběžných volání vytváření zákazníků.

Pokud je možnost **Vytvořit zákazníka v asynchronním režimu** je nastavena na **Ano** v profilu funkce obchodu (**Retail a Commerce \> Nastavení kanálu \> Nastavení internetového obchodu \> Profily funkčnosti**), volání služby v reálném čase se nepoužívají k vytváření záznamů o zákaznících v databázi kanálů. Režim vytváření asynchronních zákazníků nemá vliv na výkon centrály Commerce. Každému novému záznamu zákazníka Async je přiřazen dočasný globálně jedinečný identifikátor (GUID), který se použije jako ID zákaznického účtu. Tento identifikátor GUID se uživatelům POS nezobrazuje. Místo toho se těmto uživatelům zobrazí **Čeká se na synchronizaci** jako ID zákaznického účtu. 

### <a name="convert-async-customers-to-sync-customers"></a>Převedení asynchronních zákazníků na synchronní zákazníky

Chcete-li převést zákazníky Async na zákazníky Sync, musíte nejprve spustit **P-úlohu** a odeslat zákazníky Async do centrály Commerce. Potom spusťte úlohu **Synchronizovat zákazníky a obchodní partnery z asynchronního režimu** (dříve nazvanou **Synchronizovat zákazníky a obchodní partnery z asynchronního režimu**) k vytvoření ID zákaznického účtu. Nakonec spusťte úlohu **1010** k synchronizaci nových ID zákaznických účtů s kanály.

### <a name="async-customer-limitations"></a>Omezení asynchronních zákazníků

Funkce asynchronních zákazníků má v současné době následující omezení:

- Asynchronní záznamy o zákaznících nelze upravovat, pokud nebyl zákazník vytvořen v ústředí Commerce a nové ID zákaznického účtu nebylo synchronizováno zpět do kanálu. Adresu proto nelze uložit pro asynchronního zákazníka, dokud nebude tento zákazník synchronizován s centrálou Commerce, protože přidání adresy zákazníka je interně implementováno jako operace úprav v profilu zákazníka. Pokud je však povolena funkce **Povolit asynchronní vytváření adres zákazníků**, adresy zákazníků lze také uložit pro asynchronní zákazníky.
- Přidružení nelze spojit se zákazníky Async. Proto noví zákazníci Async nezdědí přidružení od výchozího zákazníka.
- Věrnostní karty nelze vydat zákazníkům Async, pokud nebylo nové ID zákaznického účtu synchronizováno zpět do kanálu.
- Sekundární e-mailové adresy a telefonní čísla nelze pro zákazníky Async zachytit.

Ačkoli některá z výše uvedených omezení mohou vést k tomu, že byste se rozhodli pro volbu Synchronizace zákazníka pro vaši firmu, tým Commerce pracuje na tom, aby možnosti asynchronních zákazníků více odpovídaly možnostem synchronizace zákazníků. Například od vydání Commerce verze 10.0.22 nová funkce **Povolte asynchronní vytváření adres zákazníků**, kterou můžete povolit v pracovním prostoru **Správa funkcí**, asynchronně ukládá nově vytvořené adresy zákazníků pro synchronní i asynchronní zákazníky. Pokud chcete uložit tyto adresy v profilu zákazníka v centrále Commerce, musíte naplánovat opakovanou dávkovou úlohu pro **P-úlohu** **Synchronizovat zákazníky a obchodní partnery z asynchronního režimu** a úlohu **1010**, aby byli všichni zákazníci Async převedeni na zákazníky Sync v centrále Commerce.

### <a name="customer-creation-in-pos-offline-mode"></a>Vytváření zákazníka v offline režimu POS

Kdykoli POS přejde do režimu offline, systém automaticky asynchronně vytvoří zákazníky, a to i v případě, že je zakázán režim asynchronního vytváření zákazníků. Proto, jak bylo uvedeno dříve, musí správci centrály Commerce vytvořit a naplánovat opakovanou dávkovou úlohu pro **P-úlohu** **Synchronizovat zákazníky a obchodní partnery z asynchronního režimu** a úlohu **1010**, aby byli všichni zákazníci Async převedeni na zákazníky Sync v centrále Commerce.

> [!NOTE]
> Pokud je možnost **Filtrovat sdílené tabulky údajů o zákaznících** nastavena na **Ano** na stránce **Schéma obchodního kanálu** (**Retail a Commerce \> Nastavení Commerce \> Plánovač Commerce \> Skupina databáze kanálů**), záznamy zákazníků se nevytvářejí v režimu offline POS. Další informace viz [Vyloučení dat offline](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Další prostředky

[Atributy odběratele](dev-itpro/customer-attributes.md)

[Vyloučení dat offline](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
