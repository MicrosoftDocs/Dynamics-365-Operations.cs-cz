---
title: Přehled fiskální integrace pro maloobchodní sítě
description: Toto téma obsahuje přehled funkcí fiskální integrace dostupných v Microsoft Dynamics 365 for Retail.
author: josaw
manager: annbe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2019-1-16
ms.dyn365.ops.version: 10
ms.openlocfilehash: 2dc977e3c53b1f15b41b095f586861b67c973a6d
ms.sourcegitcommit: 68df883200b5c477ea1799cc28d3ef467cd29202
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/07/2019
ms.locfileid: "377128"
---
# <a name="overview-of-fiscal-integration-for-retail-channels"></a>Přehled fiskální integrace pro maloobchodní sítě

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Úvod

Toto téma obsahuje přehled funkcí fiskální integrace dostupných v Microsoft Dynamics 365 for Retail. Fiskální integrace zahrnuje integraci s různými fiskálními zařízeními a službami, které umožňují fiskální registraci maloobchodního prodeje v souladu s místními fiskálními zákony, které mají za cíl zabránit daňovým podvodům v maloobchodním průmyslu. Zde je několik typických scénářů, které lze pokrýt pomocí fiskální integrace: 

- Zaregistrujte maloobchodní prodej na fiskálním zařízení, které je připojeno k pokladnímu místu Retail (POS), jako je například fiskální tiskárna, a vytiskněte pro zákazníka příjmový doklad.
- Bezpečně odešlete informace, které souvisejí s prodejem a vráceními, které jsou dokončeny v Retail POS do externí webové službě, kterou provozuje daňový úřad.
- Pomozte zaručit nezaměnitelnost dat prodejních transakcí prostřednictvím digitálních podpisů.

Funkce fiskální integrace v aplikaci Retail je rámcem, který poskytuje společné řešení pro další vývoj a přizpůsobení integrace mezi Retail POS a fiskálními zařízeními a službami. Funkčnost zahrnuje také ukázky fiskální integrace, které podporují základní maloobchodní scénáře pro konkrétní země nebo oblasti a které pracují se specifickými fiskálními zařízeními nebo službami. Ukázka fiskální integrace se skládá z několika rozšíření komponent aplikace Retail a je zahrnuta v sadě SDK aplikace Retail. Další informace o ukázkách fiskální integrace, které jsou k dispozici v sadě SDK aplikace Retail, naleznete v tématu [Ukázky fiskální integrace v Retail SDK](#fiscal-integration-samples-in-the-retail-sdk). Informace o instalaci a použití sady Retail SDK naleznete v tématu [Přehled doplňku Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Chcete-li podporovat jiné scénáře, které nejsou podporovány ukázkou fiskální integrace, integrovat Retail POS s jinými fiskálními zařízeními nebo službami, nebo pokrýt požadavky jiných zemí nebo oblastí, musíte buď rozšířit existující ukázku fiskální integrace, nebo vytvořit novou ukázku pomocí příkladu existujícího ukázky jako příkladu.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices"></a>Proces fiskální registrace a ukázky fiskální integrace pro fiskální zařízení

Proces fiskální registrace v Retail POS se může skládat z jednoho nebo více kroků. Každý krok zahrnuje fiskální registraci konkrétních maloobchodních transakcí nebo události v jednom fiskálním zařízení nebo službě. Následující součásti řešení se účastní fiskální registrace ve fiskálním zařízení, které je napojeno na hardwarovou stanici:

- **Rozšíření Commerce Runtime (CRT)** – Tato součást serializuje data o maloobchodních transakcích/událostech ve formátu, který se také používá pro interakci s fiskálním zařízením, analyzuje odpovědi z fiskálního zařízení a ukládá odpovědi v databázi kanálů. Rozšíření také definuje specifické transakce a události, které musí být registrovány. Tato součást se často označuje jako *poskytovatel fiskálního dokumentu*.
- **Rozšíření hardwarové stanice** – Tato součást inicializuje komunikaci s fiskálním zařízením, odesílá požadavky a přímé příkazy do fiskálního zařízení na základě dat maloobchodních transakcí/událostí, které jsou extrahovány z fiskálního dokumentu, a přijímá odpovědi z fiskálního zařízení. Tato součást se často označuje jako *fiskální konektor*.

Ukázka fiskální integrace pro fiskální zařízení obsahuje rozšíření CRT a hardwarové stanice pro poskytovatele fiskálních dokumentů a fiskální konektor. Zahrnuje také následující konfigurace součástí:

- **Konfigurace poskytovatele fiskálního dokumentu** – Tato konfigurace definuje výstupní metodu a formát pro fiskální dokumenty. Obsahuje také mapování dat pro daně a způsoby platby, aby byla data z Retail POS kompatibilní s hodnotami, které jsou předem definovány ve firmwaru fiskálního zařízení.
- **Konfigurace fiskálního konektoru** – Tato konfigurace definuje fyzickou komunikaci s konkrétním fiskálním zařízením.

Proces fiskální registrace pro specifickou registrační pokladnu POS je definován příslušným nastavením ve funkčním profilu POS. Další podrobnosti o tom, jak konfigurovat proces fiskální registrace, odeslat konfigurace poskytovatele fiskálních dokumentů a fiskálních konektorů a změnit jejich parametry naleznete v tématu [Nastavení procesu fiskální registrace](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

Následující příklad ukazuje typický tok provedení fiskální registrace pro fiskální zařízení. Tok začíná událostí v POS (například dokončením prodejní transakce) a implementuje následující pořadí kroků:

1. POS požaduje fiskální dokument z CRT.
2. CRT určuje, zda aktuální událost požaduje fiskální registraci.
3. Na základě nastavení procesu fiskální registrace identifikuje CRT fiskální konektor a příslušného poskytovatele fiskálních dokumentů, které se použijí pro fiskální registraci.
4. CRT spustí poskytovatele fiskálních dokumentů, který vygeneruje fiskální dokument (například dokument XML), který představuje maloobchodní transakci nebo událost.
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

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Ukládání fiskální odezvy ve fiskální transakci

Když je fiskální registrace transakce nebo události úspěšná, v databázi kanálů se vytvoří fiskální transakce a bude propojena s původní transakcí nebo událostí. Obdobě pokud zvolíte **Přeskočit** nebo **Označit jako registrované** pro nezdařenou fiskální registrací, tyto informace se uloží ve fiskální transakci. Fiskální transakce drží fiskální odezvu fiskálního zařízení nebo služby. Pokud proces fiskální registrace sestává z několika kroků, vytvoří se fiskální transakce pro každý krok procesu, který měl za následek úspěšnou nebo neúspěšnou registraci.

Fiskální transakce jsou přeneseny do Retail Headquarters podle *úlohy P*, společně s maloobchodními transakcemi. Na záložce s náhledem **Fiskální transakce** stránky **Transakce maloobchodu** uvidíte fiskální transakce, které jsou napojeny na maloobchodní transakce.

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

Následující ukázky fiskální integrace jsou v současné době k dispozici v sadě Retail SDK, která je vydána s aplikací Retail:

- [Ukázka integrace fiskální tiskárny pro Itálii](emea-ita-fpi-sample.md)
- [Ukázka integrace fiskální tiskárny pro Polsko](emea-pol-fpi-sample.md)

Následující funkce fiskální integrace je k dispozici také v sadě Retail SDK, ale v současné době nevyužívá architekturu fiskální integrace. Migrace této funkce do architektury fiskální integrace je plánována po pozdější aktualizace.

- [Digitální podpis pro Francii](emea-fra-cash-registers.md)
- [Digitální podpis pro Norsko](emea-nor-cash-registers.md)
- [Ukázka integrace kontrolní jednotky pro Švédsko](../dev-itpro/retail-sdk/retail-sdk-control-unit-sample.md)
