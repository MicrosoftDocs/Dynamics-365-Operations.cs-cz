---
title: Asynchronní režim vytváření zákazníka
description: Tento článek popisuje režim asynchronního vytváření zákazníků v Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 95102936871e15f8e525abca736fa75927569b34
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473699"
---
# <a name="asynchronous-customer-creation-mode"></a>Asynchronní režim vytváření zákazníka

[!include [banner](includes/banner.md)]

Tento článek popisuje režim asynchronního vytváření zákazníků v Microsoft Dynamics 365 Commerce.

V Commerce existují dva režimy vytváření zákazníků: synchronní (nebo sync) a asynchronní (nebo async). Ve výchozím nastavení jsou zákazníci vytvářeni synchronně. Jinými slovy jsou vytvářeni v Commerce headquarters v reálném čase. Režim vytváření zákazníků sync je výhodný, protože noví zákazníci jsou okamžitě prohledatelní napříč kanály. Má to však také nevýhodu. Protože to generuje volání [Commerce Data Exchange: služba v reálném čase](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) volání do centrály Commerce, výkon může být ovlivněn, pokud se uskuteční mnoho souběžných volání vytváření zákazníků.

Pokud je možnost **Vytvořit zákazníka v asynchronním režimu** je nastavena na **Ano** v profilu funkce obchodu (**Retail a Commerce \> Nastavení kanálu \> Nastavení internetového obchodu \> Profily funkčnosti**), volání služby v reálném čase se nepoužívají k vytváření záznamů o zákaznících v databázi kanálů. Asynchronní režim vytváření zákazníků nemá vliv na výkon centrály Commerce. Každému novému záznamu zákazníka async je přiřazen dočasný globálně jedinečný identifikátor (GUID), který se použije jako ID zákaznického účtu. Tento identifikátor GUID se uživatelům pokladního místa (POS) nezobrazuje. Místo toho se těmto uživatelům zobrazí **Čeká se na synchronizaci** jako ID zákaznického účtu.

> [!IMPORTANT]
> Kdykoli POS přejde do režimu offline, systém automaticky asynchronně vytvoří zákazníky, a to i v případě, že je zakázán režim asynchronního vytváření zákazníků. Proto, bez ohledu na váš výběr synchronního a asynchronního vytváření zákazníků musí správci Commerce headquarters vytvořit a naplánovat opakovanou dávkovou úlohu pro **P-úlohu** **Synchronizovat zákazníky a obchodní partnery z asynchronního režimu** a úlohu **1010**, aby byli všichni zákazníci Async převedeni na zákazníky Sync v Commerce headquarters.

## <a name="async-customer-limitations"></a>Omezení asynchronních zákazníků

Funkce asynchronních zákazníků má v současné době následující omezení:

- Věrnostní karty nelze vydat zákazníkům async, pokud nebylo nové ID zákaznického účtu synchronizováno zpět do kanálu.

## <a name="async-customer-enhancements"></a>Vylepšení asynchronních zákazníků

Aby organizace pomohly používat asynchronní režim vytváření zákazníků ke správě zákazníků a aby se snížila komunikace s Commerce headquarters v reálném čase, byla zavedena následující vylepšení, která zajistí paritu mezi synchronizačními a asynchronními režimy v kanálech. 

| Vylepšení funkcí | Verze Commerce | Podrobnosti funkce |
|---|---|---|
| Zlepšení výkonu při načítání informací o zákaznících z databáze kanálů | 10.0.20 a novější | Aby se zlepšil výkon, je entita zákazníka rozdělena na menší entity. Systém pak získá pouze požadované informace z databáze kanálů. |
| Schopnost vytvořit adresu asynchronně během pokladny | 10.0.22 a novější | <p>Přepínač funkce: **Povolit asynchronní vytváření pro adresy zákazníků**</p><p>Podrobnosti funkce:</p><ul><li>Schopnost přidávat adresy bez volání služeb v reálném čase do Commerce headquarters</li><li>Schopnost jednoznačně identifikovat adresy v databázi kanálů bez použití ID záznamu (hodnota **RecId**)</li><li>Sledování časových razítek pro vytvoření adresy</li><li>Synchronizace adres v Commerce headquarters</li></ul><p>Tato funkce ovlivňuje synchronní i asynchronní zákazníky. Chcete-li kromě asynchronního vytváření adres upravovat adresy asynchronně, musíte aktivovat funkci **Úprava zákazníků v asynchronním režimu**.</p> |
| Aktivujte paritu mezi synchronním a asynchronním vytvářením zákazníků. | 10.0.24 a novější | <p>Přepínač funkce: **Aktivovat vylepšené vytváření asynchronního zákazníka**</p><p>Podrobnosti funkce: Schopnost zachytit další informace, jako je titul, přidružení od výchozího zákazníka a sekundární kontaktní informace (telefonní číslo a e-mailová adresa), zatímco vytváříte zákazníky asynchronně</p> |
| Uživatelsky přívětivé chybové zprávy | 10.0.28 a novější | Tato vylepšení pomáhají zlepšit uživatelsky přívětivé chybové zprávy, pokud uživatel nemůže okamžitě upravovat informace, když probíhá synchronizace. Tato vylepšení aktivujte pomocí nastavení **Aktivovat, aby některé prvky uživatelského rozhraní nemohly být modifikovány asynchronním zákazníkem** na **Nastavení webu \> Rozšíření** v konfigurátoru webů Commerce. |
| Schopnost asynchronně upravovat informace o zákaznících | 10.0.29 a novější | <p>Přepínač funkce: **Povolit úpravy zákazníků v asynchronním režimu**</p><p>Podrobnosti funkce: Schopnost asynchronně upravovat zákaznická data</p><p>Odpovědi na běžné otázky týkající se problémů souvisejících s asynchronní úpravou informací o zákaznících naleznete v části [Nejčastější dotazy k asynchronnímu režimu vytváření zákazníků](async-customer-mode-faq.md).</p> |

### <a name="feature-switch-hierarchy"></a>Hierarchie přepínání funkcí

Z důvodu hierarchie přepínačů funkcí, než aktivujete funkci **Povolit úpravy zákazníků v asynchronním režimu**, musíte aktivovat následující funkce: 

- **Zlepšení výkonu zákaznických objednávek a zákaznických transakcí** – Tato funkce je povinná od verze Commerce 10.0.28. 
- **Aktivovat vylepšené vytváření asynchronního zákazníka**
- **Povolit asynchronní vytváření pro adresy zákazníků**

Odpovědi na běžné otázky týkající se odstraňování problémů viz [Nejčastější dotazy k asynchronnímu režimu vytváření zákazníků](async-customer-mode-faq.md). 

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
