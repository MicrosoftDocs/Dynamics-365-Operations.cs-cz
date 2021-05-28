---
title: Správa směn a zásuvky s hotovostí
description: Toto téma vysvětluje, jak nastavit a používat směny ve velkoobchodním pokladním místě (POS).
author: jblucher
ms.date: 05/10/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d9d36bcb05cf466d34d921d8cd5266b6c12a63d7
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6028244"
---
# <a name="shift-and-cash-drawer-management"></a>Správa směn a zásuvky s hotovostí

[!include [banner](includes/banner.md)]

Toto téma vysvětluje, jak nastavit a používat směny ve velkoobchodním pokladním místě (POS).

V aplikaci Dynamics 365 Commerce termín *směna* popisuje kolekci transakčních dat POS a aktivit mezi dvěma místy v čase. Pro každou směnu se porovnává očekáváná částka peněz oproti spočítané a deklarované částce.

Směny se obvykle otevírají na začátku pracovního dne. Uživatel v daném okamžiku deklaruje počáteční částku, kterou obsahuje zásuvka s hotovostí. Prodejní transakce jsou pak prováděny v průběhu dne. Na konci dne se spočítá zásuvka a jsou deklarovány uzávěrkové částky. Je uzavřena směna a bude vytvořena sestava Z. Sestava Z označuje, zda nějaká částka chybí nebo přebývá.

## <a name="typical-shift-scenarios"></a>Typické scénáře směny

Aplikace Commerce obsahuje několik možností konfigurace a operací POS, které podporují řadu obchodních procesů ukončení dne pro POS. Tato část popisuje některé typické scénáře směny.

### <a name="fixed-till"></a>Pevná pokladna

Tento scénář se tradičně používá nejčastěji. Stále se používá velmi často. Ve směně pevné pokladny jsou směna a pokladna přiduženy ke konkrétní registrační pokladně. Nejsou přesunuty z jedné registrační pokladny do jiné. Směnu pevné pokladny lze použít podle jednoho uživatele nebo ji sdílet mezi několik uživatelů. Směna pevné pokladny nevyžaduje žádnou zvláštní konfiguraci.

### <a name="floating-till"></a>Plovoucí pokladna

Ve směně plovoucí pokladny lze směnu a zásuvku s hotovostí přesunout z jedné registrační pokladny do jiné. Ačkoli registrační pokladna může mít pouze jednu aktivní směnu na zásuvku s hotovostí, směny lze pozastavit a pak je později obnovit, i na jiné registrační pokladně.

Například obchod má dvě registrační pokladny. Každá registrační pokladna se otevře na začátku dne, když pokladník otevře novou směnu a poskytne počáteční částku. Když je jeden pokladník připraven na přestávku, pozastaví svou směnu a odstraní pokladnu ze zásuvky s hotovostí. Tato registrační pokladna je poté k dispozici další pokladníkům. Může se přihlásit jiný pokladník a otevřít svou vlastní směnu na registrační pokladně. Po ukončení přestávky prvního pokladníka může tento pokladník obnovit svou směnu, když bude dostupná jedna z dalších registračních pokladen. Směna plovoucí pokladny nevyžaduje žádnou zvláštní konfiguraci nebo oprávnění.

### <a name="single-user"></a>Jediný uživatel

Mnoho maloobchodních prodejců upřednostňuje pouze jednoho uživatele na směnu k zajištění nejvyšší úrovně odpovědnosti za hotovost v zásuvce. Pokud pouze jeden uživatel může použít pokladnu přiřazenou ke směně, je tento uživatel výhradně odpovědný za jakékoli nesrovnalosti. Pokud více uživatelů používá směnu, je obtížné určit, kdo udělal chybu nebo kdo se mohl pokusit z pokladny krást.

### <a name="multiple-users"></a>Více uživatelů

Někteří maloobchodní prodejci jsou ochotni obětovat úroveň zodpovědnosti, která existuje při směnách s jedním uživatelem, a povolí více uživatelů na jednu směnu. Tento postup je typický, pokud existuje více uživatelů, než je dostupných registračních pokladen, a potřeba flexibility a rychlosti vyváží potenciální ztráty. Dále je typický tehdy, když manažeři obchodu nemají své lastní směny, ale mohou podle potřeby použít směny jakéhokoliv ze svých pokladníků. Aby se mohl uživatel přihlásit ke směně a použít směnu otevřenou jiným uživatelem, musí mít POS oprávnění **Povolit vícenásobné přihlášení směn**.

### <a name="shared-shift"></a>Sdílená směna

Konfigurace sdílené směny umožňuje maloobchodním prodejcům mít jednu směnu pro více registračních pokladen, zásuvek s hotovostí a uživatelů. Sdílené směna má jedinou počáteční částku a jednu konečnou částku, které jsou shrnuty v rámci všech zásuvek s hotovostí. Sdílené směny jsou nejběžnější při použití mobilních zařízení. V tomto scénáři není samostatná zásuvka s hotovostí rezervována pro každou registrační pokladnu. Místo toho všechny registrační pokladny mohou sdílet jednu zásuvku s hotovostí.

Aby mohly být v obchodě použity sdílené směny, musí být zásuvka s hotovostí nakonfigurována jako zásuvka sdílené směny přes **Maloobchod a velkoobchod \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Profily hardwaru \> Zásuvky**. Kromě toho musí mít uživatelé jedno nebo obě oprávnění sdílené směny (Povolit správu sdílené směny a Povolit použití sdílené směny).

> [!NOTE]
> V každém obchodě je možné v každém okamžiku otevřít pouze jednu sdílenou směnu. Sdílené a samostatné směny lze použít ve stejném obchodě.

## <a name="shift-and-drawer-operations"></a>Operace směny a zásuvky

Chcete-li změnit stav směny nebo zvýšit či snížit množství peněz v zásuvce, lze provést různé operace. Tato část popisuje tyto operace směny pro Modern POS a Cloud POS.

### <a name="open-shift"></a>Otevřená směna

POS vyžaduje, aby uživatelé měli aktivní, otevřenou směnu, aby mohli provádět všechny operace, které vyprodukují finanční transakci, například prodej, vrácení nebo objednávku odběratele.

Pokud se uživatel přihlásí do POS, systém nejprve ověří, zda je k dispozici pro uživatele na aktuální registrační pokladně dostupná aktivní směna. Pokud neí aktivní směna k dispozici, může uživatel otevřít novou směnu, obnovit existující směnu nebo se přihlásit do režimu bez zásuvky, v závislosti na konfiguraci systému a oprávněních uživatele.

### <a name="declare-start-amount"></a>Počáteční částka výkazu

Tato operace je často první operací, kterou provede nově otevřená směna. Pro tuto operaci uživatelé určují počáteční množství hotovosti v zásuvce pro směnu. Tato operace je důležitá, protože výpočet přebývající částky/chybějící částky, ke kterému dochází při uzavření směny, bere v úvahu počáteční částku.

### <a name="float-entry"></a>Zadání plovoucího zůstatku

*Plovoucí položky* jsou neprodejní transakce, které se provádějí v aktivní směně ke zvýšení částky v zásuvce s hotovostí. Typickým příkladem plovoucí položky je transakce pro přidání další změny do zásuvky, když se vyčerpává zásuvka.

### <a name="tender-removal"></a>Odstranění úhrady

*Odebrání úhrady* jsou neprodejní transakce, které se provádějí v aktivní směně ke snížení částky v zásuvce s hotovostí. Tato operace se nejčastěji používá ve spojení s operací plovoucích položek na odlišné směně. Například protože v registrační pokladně 1 dochází hotovost, uživatel na registrační pokladně 2 provede odebrání úhrady ke snížení částky ve své zásuvce. Uživatel na registrační pokladně 1 poté zadá plovoucí položku ke zvýšení částky ve své zásuvce s hotovostí.

### <a name="suspend-shift"></a>Pozastavit směnu

Uživatelé mohou pozastavit své aktivní směny k uvolnění aktuální registrační pokladny pro jiného uživatele, nebo pro přesun své směny na jinou registrační pokladnu (to se v tomto případě často označuje jako směna plovoucí pokladny).

Pozastavení směny zabraňuje všem novým transakcím a změnám směn až do obnovení.

### <a name="resume-shift"></a>Obnovit směnu

Tato operace umožňuje uživatelům obnovit dříve pozastavenou směnu na jakékoliv registrační pokladně, která již nemá aktivní směnu.

### <a name="tender-declaration"></a>Výkaz úhrad

Tato operace se provede k určení celkové částky peněz, která je aktuálně v zásuvce s hotovostí. Uživatelé nejčastěji provádí tuto operaci před uzavřením směny. Určená částka se porovnává proti očekávané částce směny k výpočtu částky přebytku/nedostatku.

### <a name="safe-drop"></a>Odvod do trezoru

Odvody do trezoru lze provést kdykoli během aktivní směny. Tato operace odstraní peníze ze zásuvky s hotovostí, aby mohly být přeneseny na bezpečnější místo, jako je například trezor v zadní místnosti. Celková částka zaznamenaná pro odvody do trezoru je zahrnuta v součtech směny, ale není nutné ji počítat jako součást výkaz úhrad.

### <a name="bank-drop"></a>Odvod do banky

Odvody do banky jsou stejně jako odvody do trezoru prováděny na aktivních směnách. Tato operace odstraní peníze ze směny a připraví je na bankovní vklad.

### <a name="blind-close-shift"></a>Zavřít směnu bez zadání částky

*Směny uzavřené bez zadání částky* již nejsou aktivní, ale nebyly zcela uzavřeny. Na rozdíl od pozastavené směny nelze již směny uzavřené bez zadání částky obnovit. Lze však na nich později provést operace, jako například Počáteční částka výkazu a Výkaz úhrad, stejně jako z jiné registrační pokladny.

Směny uzavřené bez zadání částky se často používají k uvolnění registru pro nového uživatele nebo směnu, aniž by bylo nutné tuto směnu nejprve plně spočítat, odsouhlasit a zavřít.

### <a name="close-shift"></a>Zavřít směnu

Tato operace vypočítá součty směny, částky přebytku/nedostatku a potom dokončí aktivní nebo bez zadání částky uzavřenou směnu. V závislosti na oprávnění uživatele je též vytisknuta sestava Z týkající se směny. Nelze obnovit nebo upravit uzavřené směny.

### <a name="print-x"></a>Tisknout X

Tato operace vytvoří a vytiskne sestavu X pro aktuální aktivní směnu.

### <a name="reprint-z"></a>Znovu vytisknout Z

Tato operace znovu vytikne systémem vygenerovanou poslední sestavu Z při uzavření směny.

### <a name="manage-shifts"></a>Spravovat směny

Tato operace umožňuje uživatelům zobrazit všechny aktivní, pozastavené a bez zadání částky uzavřené směny obchodu. V závislosti na svých oprávněních mohou uživatelé provádět závěrečné uzávěrkových postupy, jako je Výkaz úhrad a Zavírání směn pro neurčené směny uzavřené bez zadání částky. Tato operace také umožní uživatelům zobrazit a odstranit neplatné směny ve vzácných případech, kdy je směna zanechána ve špatném stavu po přepnutí mezi režimy offline a online. Tyto neplatné směny neobsahují žádné finančních informace nebo transakční data potřebná pro vyrovnání.

## <a name="shift-and-drawer-permissions"></a>Oprávnění směn a zásuvek

Následující oprávnění POS mají vliv na to, co uživatel může a nemůže provést v různých situacích:

- **Povolit uzavření bez zadání částky**
- **Povolit tisk sestavy X**
- **Povolit tisk sestavy Z**
- **Povolit výkaz úhrad**
- **Povolit výkaz plovoucího zůstatku**
- **Otevřít zásuvku bez prodeje**
- **Povolit vícenásobné přihlášení směn** - Toto oprávnění umožňuje uživateli přihlásit se ke směně a použít směnu otevřenou jiným uživatelem. Uživatelé, kteří nemají toto oprávnění, se mohou přihlásit a použít pouze směny, které mají otevřené.
- **Povolit správu sdílené směny** – uživatelé musí mít toto oprávnění k otevření nebo uzavření sdílené směny.
- **Povolit použití sdílené směny** – uživatelé musí mít toto oprávnění k přihlášení se ke sdílené směně a jejímu použití.

## <a name="back-office-end-of-day-considerations"></a>Zvážení administrativy na konci dne

Způsob, jakým se používají odsouhlasení směn a zásuvek s hotovostí, se v POS liší od způsobu, jakým jsou sumarizována data transakcí při výpočtu výkazu. Je důležité, abyste tento rozdíl pochopili. V závislosti na konfiguraci a vašich obchodních procesech vám mohou dát data směny v POS (sestava Z) a vypočítaný výkaz v administrativě odlišné výsledky. Rozdíl neznamená nutně, že jsou data směny nebo vypočítaný výkaz nesprávné nebo že došlo k potížím s daty. Pouze to znamená, že poskytnuté parametry mohou zahrnovat více nebo méně transakcí, nebo že transakce byly sečteny odlišně.

Ačkoli každý prodejce má jiné obchodní požadavky, doporučujeme nastavit váš systém následujícím způsobem, abyste se vyhnuli situacím, kdy může k tomuto rozdíku dojít:

Přejděte na **Maloobchod a velkoobchod \> Kanály \> Obchody \> Všechny obchody \> Výkaz/uzávěrka** a pro každý obchod nastavte obě pole **Metoda výkazu** a **Metoda uzávěrky** na **Směna**.

Toto nastavení pomáhá zajistit, aby výkazy administrativy zahrnovaly stejné transakce jako směny v POS a aby se data sčítala podle této směny.

Další informace o výkazu a metodách uzávěrky naleznete v tématu [Konfigurace obchodů pro výkazy Retail](/dynamics365/unified-operations/retail/tasks/store-configurations-retail-statements).


[!INCLUDE[footer-include](../includes/footer-banner.md)]