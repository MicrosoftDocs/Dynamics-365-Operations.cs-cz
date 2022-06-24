---
title: Přehled fiskální integrace pro kanály Commerce
description: Tento článek obsahuje přehled funkcí fiskální integrace dostupných v Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: ea1de0791a0eaffa2a8b1ac57143bdfd753f855b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884837"
---
# <a name="fiscal-integration-overview-for-commerce-channels"></a>Přehled fiskální integrace pro kanály Commerce

[!include [banner](../includes/banner.md)]

Tento článek obsahuje přehled funkcí fiskální integrace dostupných v Dynamics 365 Commerce. 

Fiskální integrace zahrnuje integraci s různými fiskálními zařízeními a službami, které umožňují fiskální registraci prodeje v souladu s místními fiskálními zákony, které mají za cíl zabránit daňovým podvodům v maloobchodním průmyslu. Zde je několik typických scénářů, které lze pokrýt pomocí fiskální integrace:

- Zaregistrujte prodej na fiskálním zařízení, které je připojeno k pokladnímu místu (POS), jako je například fiskální tiskárna, a vytiskněte pro zákazníka příjmový doklad.
- Bezpečně odešlete informace, které souvisejí s prodejem a vráceními, které jsou dokončeny v Retail POS do externí webové službě, kterou provozuje daňový úřad.
- Pomozte zaručit nezaměnitelnost dat prodejních transakcí prostřednictvím digitálních podpisů.

Funkce fiskální integrace je rámcem, který poskytuje společné řešení pro další vývoj a přizpůsobení integrace mezi Retail POS a fiskálními zařízeními a službami. Funkčnost zahrnuje také ukázky fiskální integrace, které podporují základní scénáře pro konkrétní země nebo oblasti a které pracují se specifickými fiskálními zařízeními nebo službami. Ukázka fiskální integrace se skládá z několika rozšíření komponent aplikace Commerce a je zahrnuta v sadě software development kit (SDK). Další informace o ukázkách fiskální integrace naleznete v tématu [Ukázky fiskální integrace v Commerce SDK](#fiscal-integration-samples-in-the-commerce-sdk). Informace o instalaci a použití sady Commerce SDK naleznete v tématu [Architektura sady Retail software development kit (SDK)](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Chcete-li podporovat jiné scénáře, které nejsou podporovány ukázkou fiskální integrace, integrovat Retail POS s jinými fiskálními zařízeními nebo službami, nebo pokrýt požadavky jiných zemí nebo oblastí, musíte buď rozšířit existující ukázku fiskální integrace, nebo vytvořit novou ukázku pomocí příkladu existujícího ukázky jako příkladu.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services"></a>Proces fiskální registrace a ukázky fiskální integrace pro fiskální zařízení a služby

Proces fiskální registrace v Retail POS se může skládat z jednoho nebo více kroků. Každý krok zahrnuje fiskální registraci konkrétních transakcí nebo události v jednom fiskálním zařízení nebo službě. Následující součásti řešení se účastní fiskální registrace ve fiskálním zařízení nebo službě:

- **Poskytovatel fiskálního dokumentu** – Tato součást serializuje data o transakcích/událostech ve formátu, který se také používá pro interakci s fiskálním zařízením nebo službou, analyzuje odpovědi z fiskálního zařízení a ukládá odpovědi v databázi kanálů. Rozšíření také definuje specifické transakce a události, které musí být registrovány.
- **Fiskální konektor** – Tato součást inicializuje komunikaci s fiskálním zařízením nebo službou, odesílá požadavky a přímé příkazy do fiskálního zařízení nebo služby na základě dat transakcí/událostí, které jsou extrahovány z fiskálního dokumentu, a přijímá odpovědi z fiskálního zařízení nebo služby

Ukázka fiskální integrace může obsahovat rozšíření Commerce Runtime (CRT), hardwarové stanice pro POS pro poskytovatele fiskálních dokumentů a fiskální konektor. Zahrnuje také následující konfigurace součástí:

- **Konfigurace poskytovatele fiskálního dokumentu** – Tato konfigurace definuje výstupní metodu a formát pro fiskální dokumenty. Obsahuje také mapování dat pro daně a způsoby platby, aby byla data z Retail POS kompatibilní s hodnotami, které jsou předem definovány ve firmwaru fiskálního zařízení nebo služby.
- **Konfigurace fiskálního konektoru** – Tato konfigurace definuje fyzickou komunikaci s konkrétním fiskálním zařízením nebo službou.

Proces fiskální registrace pro specifickou registrační pokladnu POS je definován příslušným nastavením ve funkčním profilu POS. Další podrobnosti o tom, jak konfigurovat proces fiskální registrace, odeslat konfigurace poskytovatele fiskálních dokumentů a fiskálních konektorů a změnit parametry konfigurace naleznete v tématu [Nastavení procesu fiskální registrace](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

> [!NOTE]
> Pokud potřebujete na těchto zařízeních poskytovat pouze nefiskální operace, jako je vyhledávání v katalogu produktů, vyhledávání zákazníků nebo vytváření konceptů transakcí, můžete vybrat registry s omezeními fiskálního procesu. Další informace viz [Nastavení registrů s omezeními fiskální registrace](setting-up-fiscal-integration-for-retail-channel.md#set-up-registers-with-fiscal-registration-restrictions).

Následující typický fiskální registrační tok začíná událostí v POS (například dokončením prodejní transakce) a implementuje předem definovanou sekvenci kroků, které zahrnují další komponenty Commerce (např. CRT a Hardwarová stanice).

1. POS požaduje fiskální dokument z rámce fiskální integrace (FIF).
1. FIF určuje, zda aktuální událost požaduje fiskální registraci.
1. Na základě nastavení procesu fiskální registrace identifikuje FIF fiskální konektor a příslušného poskytovatele fiskálních dokumentů, které se použijí pro fiskální registraci.
1. FIF spustí poskytovatele fiskálních dokumentů, který vygeneruje fiskální dokument (například dokument XML), který představuje transakci nebo událost.
1. FIF vrátí vygenerovaný fiskální doklad do POS.
1. POS požaduje, aby FIF předložila fiskální dokument fiskálnímu zařízení nebo službě.
1. FIF spustí fiskální konektor, který zpracuje fiskální dokument a odesílá ho do fiskálního zařízení nebo služby.
1. FIF vrátí fiskální odpověď (tj. odpověď fiskálního zařízení nebo služby) do POS.
1. POS analyzuje fiskální odpověď a určí, zda byla fiskální registrace úspěšná. Podle potřeby POS požaduje, aby FIF zpracoval všechny chyby, ke kterým došlo. 
1. POS požaduje, aby FIF zpracoval a uložil fiskální odpověď.
1. Poskytovatel fiskálních dokumentů zpracovává fiskální odpověď. V rámci tohoto zpracování poskytovatel fiskálních dokumentů analyzuje odpověď a extrahuje z ní rozšířená data.
1. FIF uloží odpověď a rozšířená data do databáze kanálu.
1. Podle potřeby vytiskne POS účtenku prostřednictvím běžné tiskárny účtenek, která je připojena k hardwarové stanici. Účtenka může obsahovat požadované údaje z fiskální odpovědi.
 
Následující příklady ukazují toky provedení fiskální registrace pro typická fiskální zařízení nebo služby.
 
### <a name="fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station"></a>Fiskální registrace se provádí prostřednictvím zařízení připojeného ke hardwarové stanici

Tato konfigurace se používá, když je k hardwarové stanici připojeno fyzické fiskální zařízení, jako je fiskální tiskárna. Je také použitelná, když komunikace s fiskálním zařízením nebo službou probíhá prostřednictvím softwaru, který je nainstalován na hardwarové stanici. V tomto případě se poskytovatel fiskálních dokumentů nachází na CRT a fiskální konektor je umístěn na hardwarové stanici.

![Fiskální registrace se provádí prostřednictvím zařízení připojeného ke hardwarové stanici.](media/FIF-CRT-HWS.png)

### <a name="fiscal-registration-is-done-via-an-external-service"></a>Fiskální registrace se provádí prostřednictvím externí služby

Tato konfigurace se používá, když se fiskální registrace provádí prostřednictvím externí služby, jako je webová služba provozovaná daňovým úřadem. V tomto případě se poskytovatel fiskálních dokumentů i fiskální konektor nacházejí na CRT.

![Fiskální registrace se provádí prostřednictvím externí služby.](media/FIF-CRT-CRT.png)
 
### <a name="fiscal-registration-is-done-internally-in-the-crt"></a>Fiskální registrace se provádí interně v CRT

Tato konfigurace se používá, když pro fiskální registraci není vyžadováno žádné externí fiskální zařízení nebo služba. Používá se například, když se fiskální registrace provádí prostřednictvím digitálního podepisování prodejních transakcí. V tomto případě se poskytovatel fiskálních dokumentů i fiskální konektor nacházejí na CRT.

![Fiskální registrace se provádí interně v CRT.](media/FIF-CRT-CRT-SGN.png)

### <a name="fiscal-registration-is-done-via-a-device-or-service-in-the-local-network"></a>Fiskální registrace se provádí prostřednictvím zařízení nebo služby v místní síti

Tato konfigurace se používá, když je v místní síti obchodu přítomno fyzické fiskální zařízení nebo fiskální služba a poskytuje aplikační programovací rozhraní (API) HTTPS. V tomto případě se poskytovatel fiskálních dokumentů nachází na CRT a fiskální konektor je umístěn na POS.

![Fiskální registrace se provádí prostřednictvím zařízení nebo služby v místní síti.](media/FIF-CRT-POS.png)

## <a name="error-handling"></a>Zpracování chyb

Architektura fiskální integrace poskytuje následující možnosti k řešení problémů během fiskální registrace:

- **Opakovat** – Operátoři mohou tuto možnost využít, pokud lze selhání vyřešit rychle, a fiskální registraci lze znovu spustit. Tuto možnost lze například použít, pokud není fiskální zařízení připojeno, ve fiskální tiskárna došel papír nebo je ve fiskální tiskárně zaseknutý papír.
- **Zrušit** – Tato možnost umožňuje operátorům odložit fiskální registraci aktuální transakce nebo události, pokud selže. Po odložení registrace může operátor pokračovat v práci na POS a může dokončit jakoukoli operaci, pro kterou není požadována fiskální registrace. Když nastane událost vyžadující fiskální registraci v POS (například otevření nové transakce), automaticky se zobrazí dialogové okno pro zpracování chyb, které oznamuje operátorovi, že předchozí transakce nebyla správně zaregistrována, a poskytuje možnosti zpracování chyb.
- **Přeskočit** – Operátoři mohou tuto možnost využít, pokud lze fiskální registraci vynechat za určitých podmínek a lze pokračovat v pravidelných operacích na POS. Tuto možnost lze například použít, pokud lze obchodní transakci, u níž fiskální registrace selhala, zaregistrovat ve zvláštním papírovém deníku.
- **Označit jako registrované** – Operátoři mohou tuto možnost použít, když byla transakce skutečně zaregistrována ve fiskálním zařízení (například byla vytištěna fiskální příjemka), ale došlo k chybě, když byla fiskální odpověď uložena do databáze kanálů.
- **Odložit** – Operátoři mohou tuto možnost použít, když transakce nebyla zaregistrována, protože registrační služba nebyla k dispozici. 

> [!NOTE]
> Možnosti **Přeskočit**, **Označit jako registrované** a **Odložit** je třeba aktivovat v procesu fiskální registrace před jejich použití. Kromě toho musí být udělena odpovídající oprávnění operátorům.

Možnosti **Přeskočit**, **Označit jako registrované** a **Odložit** umožňují informačním kódům zaznamenat některé konkrétní informace o selhání, jako je důvod selhání nebo odůvodnění pro přeskočení fiskální registrace nebo označení transakce jako registrované. Další informace o způsobu nastavení parametrů zpracování chyb naleznete v tématu [Nastavení zpracování chyb](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>Volitelná fiskální registraci

Fiskální registrace může být povinná pro některé operace, ale volitelná pro jiné. Fiskální registrace pravidelných prodejů a vrácení může být například povinná, ale fiskální registrace operací, které se týkají vkladů zákazníků, může být volitelná. V tomto případě by nedokončení fiskální registrace prodeje mělo blokovat další prodej, ale nedokončení fiskální registrace vkladu zákazníka by nemělo blokovat další prodej. Chcete-li rozlišit povinné a volitelné operace, doporučujeme, abyste je zpracovali prostřednictvím různých poskytovatelů dokumentů a abyste nastavili samostatné kroky v procesu fiskální registrace pro tyto poskytovatele. Parametr **Pokračovat při chybě** by měl být povolen pro všechny kroky, které souvisí s volitelnou fiskální registrací. Další informace o způsobu nastavení parametrů zpracování chyb naleznete v tématu [Nastavení zpracování chyb](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-rerun-fiscal-registration"></a>Ruční opětovné spuštění fiskální registrace

Pokud byla fiskální registrace transakce nebo události odložena po selhání (například pokud operátor zvolil **Zrušit** v dialogovém okně zpracování chyb), můžete ručně spustit fiskální registraci vyvoláním příslušné operace. Více informací naleznete v části [Povolit ruční provedení odložené daňové registrace](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

### <a name="postpone-option"></a>Možnost odložit

Možnost **Odložit** umožňuje pokračovat v procesu fiskální registrace, pokud aktuální krok selže. Lze jej použít, pokud existuje možnost zálohy fiskální registrace.

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
- Stav fiskální registrace: **Dokončeno** pro úspěšnou registraci, **Přeskočeno**, pokud operátor zvolil možnost **Přeskočit** pro nezdařenou registraci, nebo **Označeno jako registrované**, pokud operátor zvolil možnost **Označit jako registrované**, nebo **Odložené**, pokud operátor vybral možnost **Odložit**.
- Transakce informačních kódů, které souvisí s vybranou fiskální transakcí. Chcete-li zobrazit transakce informačních kódů, na záložce s náhledem **Fiskální transakce** zvolte fiskální transakci, která má stav **Přeskočeno**, **Označeno jako registrované** nebo **Odloženo**, a poté vyberte **Transakce informačních kódů**.

Výběrem možnosti **Rozšířená data** můžete také zobrazit některé vlastnosti fiskální transakce. Seznam vlastností, které lze zobrazit, je specifický pro funkci fiskální registrace, která generovala fiskální transakci. Můžete například zobrazit digitální podpis, pořadové číslo, kryptografický otisk certifikátu, identifikaci algoritmu hash a další fiskální transakční vlastnosti pro funkci digitálního podepisování pro Francii.

## <a name="fiscal-texts-for-discounts"></a>Fiskální texty pro slevy

Některé země nebo oblasti mají zvláštní požadavky na dodatečné texty, které musí být vytištěny na fiskálních příjemkách při použití různých druhů slev. Funkce fiskální integrace umožňuje nastavit speciální text pro slevu, který je vytištěn na fiskální příjemce za řádkem slevy. Pro ruční slevy můžete nastavit fiskální text pro informační kód, který je určena jako informační kód **Sleva na produkt** ve funkčním profilu POS. Další informace o způsobu nastavení fiskálních textů pro slevy naleznete v tématu [Nastavení fiskálních textů pro slevy](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>Tisk fiskálních sestav X a Z

Funkce fiskální integrace podporuje generování výkazů na konci dne, které jsou specifické pro integrované fiskální zařízení nebo službu:

- Nová tlačítka, která spouštějí odpovídající operace, by měla být přidána do rozložení obrazovky POS. Další podrobnosti naleznete v tématu [Nastavení fiskálních sestav X/ Z z POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- V ukázce fiskální integrace by tyto operace měly odpovídat příslušným operacím fiskálního zařízení.

## <a name="fiscal-integration-samples-in-the-commerce-sdk"></a>Ukázky fiskální integrace v Commerce SDK

Následující ukázky fiskální integrace jsou v současné době k dispozici v sadě Commerce SDK:

- [Vzor integrace fiskální tiskárny pro Itálii](./emea-ita-fpi-sample.md)
- [Vzor integrace fiskální tiskárny pro Polsko](./emea-pol-fpi-sample.md)
- [Ukázka integrace fiskální služby pro Rakousko](./emea-aut-fi-sample.md)
- [Ukázka integrace fiskální služby pro Českou republiku](./emea-cze-fi-sample.md)
- [Ukázka integrace kontrolní jednotky pro Švédsko](./emea-swe-fi-sample.md)
- [Ukázka integrace fiskální služby pro Německo](./emea-deu-fi-sample.md)
- [Vzor integrace fiskální tiskárny pro Rusko](./rus-fpi-sample.md)

Následující funkce fiskální integrace je také implementována pomocí rámce fiskální integrace, ale je k dispozici ihned a není součástí Commerce SDK:

- [Fiskální registrace pro Brazílii](./latam-bra-commerce-localization.md#fiscal-registration-for-brazil)
- [Digitální podpis pro Francii](./emea-fra-cash-registers.md)

Následující funkce fiskální integrace je k dispozici také v sadě Commerce SDK, ale v současné době nevyužívá architekturu fiskální integrace. Migrace této funkce do architektury fiskální integrace je plánována po pozdější aktualizace.

- [Digitální podpis pro Norsko](./emea-nor-cash-registers.md)

Následující starší funkce fiskální integrace, která je k dispozici v aplikaci Commerce SDK, nepoužívá architekturu fiskální integrace a bude v pozdějších aktualizacích zastaralá:

- [Ukázka integrace kontrolní jednotky pro Švédsko (starší)](./retail-sdk-control-unit-sample.md)
- [Digitální podpis pro Francii (starší)](./emea-fra-deployment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
