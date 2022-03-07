---
title: Asynchronní režim vytváření zákazníka
description: Toto téma popisuje režim asynchronního vytváření zákazníků v Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 22bb4eaf3d4897904412120fa5580c42637b56e0
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913789"
---
# <a name="asynchronous-customer-creation-mode"></a>Asynchronní režim vytváření zákazníka

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Toto téma popisuje režim asynchronního vytváření zákazníků v Microsoft Dynamics 365 Commerce.

V Commerce existují dva režimy vytváření zákazníků: synchronní (nebo sync) a asynchronní (nebo async). Ve výchozím nastavení jsou zákazníci vytvářeni synchronně. Jinými slovy jsou vytvářeni v ústředí Commerce v reálném čase. Režim vytváření zákazníků sync je výhodný, protože noví zákazníci jsou okamžitě prohledatelní napříč kanály. Má to však také nevýhodu. Protože to generuje volání [Commerce Data Exchange: služba v reálném čase](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) volání do centrály Commerce, výkon může být ovlivněn, pokud se uskuteční mnoho souběžných volání vytváření zákazníků.

Pokud je možnost **Vytvořit zákazníka v asynchronním režimu** je nastavena na **Ano** v profilu funkce obchodu (**Retail a Commerce \> Nastavení kanálu \> Nastavení internetového obchodu \> Profily funkčnosti**), volání služby v reálném čase se nepoužívají k vytváření záznamů o zákaznících v databázi kanálů. Asynchronní režim vytváření zákazníků nemá vliv na výkon centrály Commerce. Každému novému záznamu zákazníka async je přiřazen dočasný globálně jedinečný identifikátor (GUID), který se použije jako ID zákaznického účtu. Tento identifikátor GUID se uživatelům pokladního místa (POS) nezobrazuje. Místo toho se těmto uživatelům zobrazí **Čeká se na synchronizaci** jako ID zákaznického účtu.

> [!IMPORTANT]
> Kdykoli POS přejde do režimu offline, systém automaticky asynchronně vytvoří zákazníky, a to i v případě, že je zakázán režim asynchronního vytváření zákazníků. Proto bez ohledu na váš výběr mezi synchronním a asynchronním vytvářením zákazníků musí správci centrály Commerce vytvořit a naplánovat opakující se dávkovou úlohu pro **P-práci**, úlohy **Synchronizovat zákazníky a obchodní partnery z asynchronního režimu** (dříve nazvanou **Synchronizovat zákazníky a obchodní partnery z asynchronního režimu**) a úlohu **1010**, aby byli všichni asynchronní zákazníci převedeni na synchronní zákazníky v centrále Commerce.

## <a name="async-customer-limitations"></a>Omezení asynchronních zákazníků

Funkce asynchronních zákazníků má v současné době následující omezení:

- Asynchronní záznamy o zákaznících nelze upravovat, pokud nebyl zákazník vytvořen v ústředí Commerce a nové ID zákaznického účtu nebylo synchronizováno zpět do kanálu.
- Věrnostní karty nelze vydat zákazníkům async, pokud nebylo nové ID zákaznického účtu synchronizováno zpět do kanálu.

## <a name="async-customer-enhancements"></a>Vylepšení asynchronních zákazníků

Od verze Commerce 10.0.24 můžete aktivovat funkci **Povolit vylepšené asynchronní vytváření zákazníků** v pracovním prostoru **Správa funkcí**. Tato funkce překlenuje propast mezi asynchronními a synchronizovanými režimy vytváření zákazníků v POS a elektronickém obchodování následujícími způsoby:

- Přidružení nelze spojit se zákazníky async.
- Tituly lze přidat k asynchronním zákazníkům.
- Sekundární e-mailové adresy a telefonní čísla nelze pro zákazníky async zachytit.

Od verze Commerce 10.0.22 můžete aktivovat funkci **Povolit asynchronní vytváření adres zákazníků** v pracovním prostoru **Správa funkcí**. Tato funkce umožňuje asynchronně ukládat nově vytvořené adresy zákazníků pro synchronizované i asynchronní zákazníky.

Pokud aktivujete výše uvedené funkce, musíte naplánovat opakovanou dávkovou úlohu pro **P-úlohu**, úlohu **Synchronizovat zákazníky a obchodní partnery z asynchronního režimu** a úlohu **1010**, aby byli všichni zákazníci async převedeni na zákazníky sync v centrále Commerce.

### <a name="customer-creation-in-pos-offline-mode"></a>Vytváření zákazníka v offline režimu POS

Jak bylo zmíněno výše, kdykoli POS přejde do režimu offline, systém automaticky asynchronně vytvoří zákazníky, a to i v případě, že je zakázán režim asynchronního vytváření zákazníků. Proto musí správci centrály Commerce vytvořit a naplánovat opakovanou dávkovou úlohu pro **P-úlohu**, úlohu **Synchronizovat zákazníky a obchodní partnery z asynchronního režimu** a úlohu **1010**, aby byli všichni zákazníci async převedeni na zákazníky sync v centrále Commerce.

> [!NOTE]
> Pokud je možnost **Filtrovat sdílené tabulky údajů o zákaznících** nastavena na **Ano** na stránce **Schéma obchodního kanálu** (**Retail a Commerce \> Nastavení Commerce \> Plánovač Commerce \> Skupina databáze kanálů**), záznamy zákazníků se nevytvářejí v režimu offline POS. Další informace viz [Vyloučení dat offline](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Další prostředky

[Správa zákazníků v obchodech](customer-mgmt-stores.md)

[Převedení asynchronních zákazníků na synchronní zákazníky](convert-async-to-sync.md)

[Atributy odběratele](dev-itpro/customer-attributes.md)

[Vyloučení dat offline](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
