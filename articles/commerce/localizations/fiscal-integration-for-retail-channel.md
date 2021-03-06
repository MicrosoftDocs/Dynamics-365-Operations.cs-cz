---
title: Přehled fiskální integrace pro kanály Commerce
description: Toto téma obsahuje přehled funkcí fiskální integrace dostupných v Dynamics 365 Commerce.
author: josaw
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2019-1-16
ms.dyn365.ops.version: 10
ms.openlocfilehash: 155056eb3a2acd0d66e0ace8d5558929678cb8e3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798774"
---
# <a name="overview-of-fiscal-integration-for-commerce-channels"></a>Přehled fiskální integrace pro kanály Commerce

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Úvod

Toto téma obsahuje přehled funkcí fiskální integrace dostupných v Dynamics 365 Commerce. Fiskální integrace zahrnuje integraci s různými fiskálními zařízeními a službami, které umožňují fiskální registraci prodeje v souladu s místními fiskálními zákony, které mají za cíl zabránit daňovým podvodům v maloobchodním průmyslu. Zde je několik typických scénářů, které lze pokrýt pomocí fiskální integrace:

- Zaregistrujte prodej na fiskálním zařízení, které je připojeno k pokladnímu místu (POS), jako je například fiskální tiskárna, a vytiskněte pro zákazníka příjmový doklad.
- Bezpečně odešlete informace, které souvisejí s prodejem a vráceními, které jsou dokončeny v Retail POS do externí webové službě, kterou provozuje daňový úřad.
- Pomozte zaručit nezaměnitelnost dat prodejních transakcí prostřednictvím digitálních podpisů.

Funkce fiskální integrace je rámcem, který poskytuje společné řešení pro další vývoj a přizpůsobení integrace mezi Retail POS a fiskálními zařízeními a službami. Funkčnost zahrnuje také ukázky fiskální integrace, které podporují základní scénáře pro konkrétní země nebo oblasti a které pracují se specifickými fiskálními zařízeními nebo službami. Ukázka fiskální integrace se skládá z několika rozšíření komponent aplikace Commerce a je zahrnuta v sadě software development kit (SDK). Další informace o ukázkách fiskální integrace naleznete v tématu [Ukázky fiskální integrace v Retail SDK](#fiscal-integration-samples-in-the-retail-sdk). Informace o instalaci a použití sady Retail SDK naleznete v tématu [Architektura sady Retail software development kit (SDK)](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Chcete-li podporovat jiné scénáře, které nejsou podporovány ukázkou fiskální integrace, integrovat Retail POS s jinými fiskálními zařízeními nebo službami, nebo pokrýt požadavky jiných zemí nebo oblastí, musíte buď rozšířit existující ukázku fiskální integrace, nebo vytvořit novou ukázku pomocí příkladu existujícího ukázky jako příkladu.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices"></a>Proces fiskální registrace a ukázky fiskální integrace pro fiskální zařízení

Proces fiskální registrace v Retail POS se může skládat z jednoho nebo více kroků. Každý krok zahrnuje fiskální registraci konkrétních transakcí nebo události v jednom fiskálním zařízení nebo službě. Následující součásti řešení se účastní fiskální registrace ve fiskálním zařízení, které je napojeno na hardwarovou stanici:

- **Rozšíření Commerce Runtime (CRT)** – Tato součást serializuje data o transakcích/událostech ve formátu, který se také používá pro interakci s fiskálním zařízením, analyzuje odpovědi z fiskálního zařízení a ukládá odpovědi v databázi kanálů. Rozšíření také definuje specifické transakce a události, které musí být registrovány. Tato součást se často označuje jako *poskytovatel fiskálního dokumentu*.
- **Rozšíření hardwarové stanice** – Tato součást inicializuje komunikaci s fiskálním zařízením, odesílá požadavky a přímé příkazy do fiskálního zařízení na základě dat transakcí/událostí, které jsou extrahovány z fiskálního dokumentu, a přijímá odpovědi z fiskálního zařízení. Tato součást se často označuje jako *fiskální konektor*.

Ukázka fiskální integrace pro fiskální zařízení obsahuje rozšíření CRT a hardwarové stanice pro poskytovatele fiskálních dokumentů a fiskální konektor. Zahrnuje také následující konfigurace součástí:

- **Konfigurace poskytovatele fiskálního dokumentu** – Tato konfigurace definuje výstupní metodu a formát pro fiskální dokumenty. Obsahuje také mapování dat pro daně a způsoby platby, aby byla data z Retail POS kompatibilní s hodnotami, které jsou předem definovány ve firmwaru fiskálního zařízení.
- **Konfigurace fiskálního konektoru** – Tato konfigurace definuje fyzickou komunikaci s konkrétním fiskálním zařízením.

Proces fiskální registrace pro specifickou registrační pokladnu POS je definován příslušným nastavením ve funkčním profilu POS. Další podrobnosti o tom, jak konfigurovat proces fiskální registrace, odeslat konfigurace poskytovatele fiskálních dokumentů a fiskálních konektorů a změnit jejich parametry naleznete v tématu [Nastavení procesu fiskální registrace](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

Následující příklad ukazuje typický tok provedení fiskální registrace pro fiskální zařízení. Tok začíná událostí v POS (například dokončením prodejní transakce) a implementuje následující pořadí kroků:

1. POS požaduje fiskální dokument z CRT.
2. CRT určuje, zda aktuální událost požaduje fiskální registraci.
3. Na základě nastavení procesu fiskální registrace identifikuje CRT fiskální konektor a příslušného poskytovatele fiskálních dokumentů, které se použijí pro fiskální registraci.
4. CRT spustí poskytovatele fiskálních dokumentů, který vygeneruje fiskální dokument (například dokument XML), který představuje transakci nebo událost.
5. POS odešle fiskální dokument, který připravuje CRT, do hardwarové stanice.
6. Hardwarová stanice spustí fiskální konektor, který zpracuje fiskální dokument a komunikuje ho do fiskálního zařízení nebo služby.
7. POS analyzuje odpověď z fiskálního zařízení nebo služby a určí, zda byla fiskální registrace úspěšná.
8. CRT uloží odpověď do databáze kanálů.

![Schéma řešení](media/emea-fiscal-integration-solution.png "Schéma řešení")

## <a name="error-handling"></a>Zpracování chyb

Architektura fiskální integrace poskytuje následující možnosti k řešení problémů během fiskální registrace:

- **Opakovat** – Operátoři mohou tuto možnost využít, pokud lze selhání vyřešit rychle, a fiskální registraci lze znovu spustit. Tuto možnost lze například použít, pokud není fiskální zařízení připojeno, ve fiskální tiskárna došel papír nebo je ve fiskální tiskárně zaseknutý papír.
- **Zrušit** – Tato možnost umožňuje operátorům odložit fiskální registraci aktuální transakce nebo události, pokud selže. Po odložení registrace může operátor pokračovat v práci na POS a může dokončit jakoukoli operaci, pro kterou není požadována fiskální registrace. Když nastane událost vyžadující fiskální registraci v POS (například otevření nové transakce), automaticky se zobrazí dialogové okno pro zpracování chyb, které oznamuje operátorovi, že předchozí transakce nebyla správně zaregistrována, a poskytuje možnosti zpracování chyb.
- **Přeskočit** – Operátoři mohou tuto možnost využít, pokud lze fiskální registraci vynechat za určitých podmínek a lze pokračovat v pravidelných operacích na POS. Tuto možnost lze například použít, pokud lze obchodní transakci, u níž fiskální registrace selhala, zaregistrovat ve zvláštním papírovém deníku.
- **Označit jako registrované** – Operátoři mohou tuto možnost použít, když byla transakce skutečně zaregistrována ve fiskálním zařízení (například byla vytištěna fiskální příjemka), ale došlo k chybě, když byla fiskální odpověď uložena do databáze kanálů.

> [!NOTE]
> Možnosti **Přeskočit** a **Označit jako registrované** je třeba aktivovat v procesu fiskální registrace před jejich použití. Kromě toho musí být udělena odpovídající oprávnění operátorům.

Možnosti **Přeskočit** a **Označit jako registrované** umožňují informačním kódům zaznamenat některé konkrétní informace o selhání, jako je důvod selhání nebo odůvodnění pro přeskočení fiskální registrace nebo označení transakce jako registrované. Další informace o způsobu nastavení parametrů zpracování chyb naleznete v tématu [Nastavení zpracování chyb](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>Volitelná fiskální registraci

Fiskální registrace může být povinná pro některé operace, ale volitelná pro jiné. Fiskální registrace pravidelných prodejů a vrácení může být například povinná, ale fiskální registrace operací, které se týkají vkladů zákazníků, může být volitelná. V tomto případě by nedokončení fiskální registrace prodeje mělo blokovat další prodej, ale nedokončení fiskální registrace vkladu zákazníka by nemělo blokovat další prodej. Chcete-li rozlišit povinné a volitelné operace, doporučujeme, abyste je zpracovali prostřednictvím různých poskytovatelů dokumentů a abyste nastavili samostatné kroky v procesu fiskální registrace pro tyto poskytovatele. Parametr **Pokračovat při chybě** by měl být povolen pro všechny kroky, které souvisí s volitelnou fiskální registrací. Další informace o způsobu nastavení parametrů zpracování chyb naleznete v tématu [Nastavení zpracování chyb](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-running-fiscal-registration"></a>Ruční spuštění fiskální registrace

Pokud byla fiskální registrace transakce nebo události odložena po selhání (například pokud operátor zvolil **Zrušit** v dialogovém okně zpracování chyb), můžete ručně spustit fiskální registraci vyvoláním příslušné operace. Více informací naleznete v části [Povolit ruční provedení odložené daňové registrace](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

### <a name="fiscal-registration-health-check"></a>Kontrola stavu fiskální registrace

Postup kontroly stavu pro fiskální registrace ověří dostupnost fiskálního zařízení nebo služby, když dojde ke konkrétní události. Pokud nelze momentálně provést fiskální registraci, je operátor informován předem.

POS spustí kontrolu stavu, jakmile dojde k následujícím událostem:

- Otevře se nová transakce.
- Pozastavená transakce je odvolána.
- Prodejní transakce nebo transakce vrácení je dokončena.

Pokud se kontrola stavu nezdaří, POS zobrazí dialogové okno kontroly stavu. Toto dialogové okno nabízí následující tlačítka:

- **OK** – Toto tlačítko umožňuje operátorovi ignorovat chybu kontroly stavu a pokračovat ve zpracování operace. Operátorři mohou vybrat toto tlačítko pouze tehdy, pokud mají oprávnění **Povolení přeskočení chyby kontroly stavu**.
- **Zrušit** – Pokud operátor vybere toto tlačítko, POS zruší poslední akci (například položka není přidána do nové transakce).

> [!NOTE]
> Kontrola stavu je spuštěna pouze v případě, když aktuální operace vyžaduje fiskální registraci a když je parametr **Pokračovat při chybě** zakázán pro aktuální krok procesu fiskální registrace. Další informace naleznete v tématu [Nastavení zpracování chyb](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Ukládání fiskální odezvy ve fiskální transakci

Když je fiskální registrace transakce nebo události úspěšná, v databázi kanálů se vytvoří fiskální transakce a bude propojena s původní transakcí nebo událostí. Obdobě pokud zvolíte **Přeskočit** nebo **Označit jako registrované** pro nezdařenou fiskální registrací, tyto informace se uloží ve fiskální transakci. Fiskální transakce drží fiskální odezvu fiskálního zařízení nebo služby. Pokud proces fiskální registrace sestává z několika kroků, vytvoří se fiskální transakce pro každý krok procesu, který měl za následek úspěšnou nebo neúspěšnou registraci.

Fiskální transakce jsou přeneseny do Headquarters podle *úlohy P*, společně s maloobchodními transakcemi. Na záložce s náhledem **Fiskální transakce** stránky **Transakce obchodu** uvidíte fiskální transakce, které jsou napojeny na transakce.

Fiskální transakce ukládá následující podrobnosti:

- Podrobnosti procesu fiskální registrace (proces, skupina konektorů, konektor atd.). Též ukládá sériové číslo fiskálního zařízení do pole **Číslo pokladny**, pokud jsou tyto informace zahrnuty do fiskální odezvy.
- Stav fiskální registrace: **Dokončeno** pro úspěšnou registraci, **Přeskočeno**, pokud operátor zvolil možnost **Přeskočit** pro nezdařenou registraci, nebo **Označeno jako registrované**, pokud operátor zvolil možnost **Označit jako registrované**.
- Transakce informačních kódů, které souvisí s vybranou fiskální transakcí. Chcete-li zobrazit transakce informačních kódů, na záložce s náhledem **Fiskální transakce** zvolte fiskální transakci, která má stav **Přeskočeno** nebo **Označen jako registrované**, a poté vyberte **Transakce informačních kódů**.

## <a name="fiscal-texts-for-discounts"></a>Fiskální texty pro slevy

Některé země nebo oblasti mají zvláštní požadavky na dodatečné texty, které musí být vytištěny na fiskálních příjemkách při použití různých druhů slev. Funkce fiskální integrace umožňuje nastavit speciální text pro slevu, který je vytištěn na fiskální příjemce za řádkem slevy. Pro ruční slevy můžete nastavit fiskální text pro informační kód, který je určena jako informační kód **Sleva na produkt** ve funkčním profilu POS. Další informace o způsobu nastavení fiskálních textů pro slevy naleznete v tématu [Nastavení fiskálních textů pro slevy](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>Tisk fiskálních sestav X a Z

Funkce fiskální integrace podporuje generování výkazů na konci dne, které jsou specifické pro integrované fiskální zařízení nebo službu:

- Nová tlačítka, která spouštějí odpovídající operace, by měla být přidána do rozložení obrazovky POS. Další podrobnosti naleznete v tématu [Nastavení fiskálních sestav X/ Z z POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- V ukázce fiskální integrace by tyto operace měly odpovídat příslušným operacím fiskálního zařízení.

## <a name="fiscal-integration-samples-in-the-retail-sdk"></a>Ukázky fiskální integrace v Retail SDK

Následující ukázky fiskální integrace jsou v současné době k dispozici v sadě Retail SDK:

- [Vzor integrace fiskální tiskárny pro Itálii](emea-ita-fpi-sample.md)
- [Vzor integrace fiskální tiskárny pro Polsko](emea-pol-fpi-sample.md)
- [Ukázka integrace fiskální služby pro Rakousko](emea-aut-fi-sample.md)
- [Ukázka integrace fiskální služby pro Českou republiku](emea-cze-fi-sample.md)
- [Ukázka integrace kontrolní jednotky pro Švédsko](./emea-swe-fi-sample.md)
- [Ukázka integrace fiskální služby pro Německo](./emea-deu-fi-sample.md)

Následující funkce fiskální integrace je k dispozici také v sadě Retail SDK, ale v současné době nevyužívá architekturu fiskální integrace. Migrace této funkce do architektury fiskální integrace je plánována po pozdější aktualizace.


- [Digitální podpis pro Francii](emea-fra-cash-registers.md)
- [Digitální podpis pro Norsko](emea-nor-cash-registers.md)

Následující starší funkce fiskální integrace, která je k dispozici v aplikaci Retail SDK, nepoužívá architekturu fiskální integrace a bude v pozdějších aktualizacích zastaralá:

- [Ukázka integrace kontrolní jednotky pro Švédsko (starší)](./retail-sdk-control-unit-sample.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]