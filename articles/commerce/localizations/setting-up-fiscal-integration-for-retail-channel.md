---
title: Nastavení fiskální integrace pro obchodní kanály
description: Toto téma obsahuje pokyny pro nastavení funkce fiskální integrace pro velkoobchodní kanály.
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
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 475459e20bb53a726524311fb66ddd82dee454ef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231711"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Nastavení fiskální integrace pro obchodní kanály

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Úvod

Toto téma obsahuje pokyny pro nastavení funkce fiskální integrace pro velkoobchodní kanály. Další informace o fiskální integraci naleznete v tématu [Přehled fiskální integrace pro velkoobchodní kanály](fiscal-integration-for-retail-channel.md).

Proces nastavení fiskální integrace zahrnuje následující obecné úlohy:

1. Konfigurace fiskálních konektorů, které reprezentují fiskální zařízení nebo služby používané pro účely fiskální registrace, jako jsou fiskální tiskárny.
2. Nakonfigurujte poskytovatele dokumentů, kteří generují fiskální dokumenty k registraci ve fiskálních zařízeních nebo službách podle fiskálních konektorů.
3. Nakonfigurujte proces fiskální registrace, který definuje pořadí kroků fiskální registrace a fiskálních konektorů a poskytovatelů fiskálních dokumentů používaných v jednotlivých krocích.
4. Přiřaďte procesy fiskální registrace do funkčních profilů POS.
5. Přiřadíte technické profily konektoru hardwarovým profilům.

## <a name="set-up-a-fiscal-registration-process"></a>Nastavení procesu fiskální registrace

Před použitím funkce fiskální integrace byste měli konfigurovat následující nastavení.

1. Aktualizujte parametry velkoobchodu.

    1. Na stránce **Sdílené parametry velkoobchodu** na kartě **Obecné** nastavte možnost **Povolit fiskální integraci** na **Ano**. Na kartě **Číselné řady** definujte číselné řady pro následující reference:

        - Číslo fiskálního technického profilu
        - Číslo skupiny fiskálních konektorů
        - Číslo procesu registrace

    2. Na stránce **Parametry velkoobchodu** definujte číselné řady pro číslo fiskálního funkčního profilu.

    > [!NOTE]
    > Číselné řady jsou volitelné. Čísla pro všechny entity fiskální integrace lze generovat z číselných řad nebo ručně.

2. Nahrajte konfigurace fiskálních konektorů a poskytovatelů fiskálních dokumentů.

    Zprostředkovatel fiskálního dokumentu je zodpovědný za generování fiskálních dokumentů, které představují velkoobchodní transakce a události, které jsou zaregistrovány na POS ve formátu, který se používá pro interakci s fiskálním zařízením nebo službou. Poskytovatel fiskálního dokumentu například může generovat vyjádření fiskálního příjmu ve formátu XML.

    Fiskální konektor zodpovídá za komunikace s fiskálním zařízením nebo službu. Fiskální konektor může například odeslat fiskální příjem, který poskytovatel fiskálních dokumentů vytvořil ve formátu XML pro fiskální tiskárnu. Podrobnější informace o kompoenntách fiskální integrace získáte v části [Ukázky procesu fiskální registrace pro fiskální zařízení](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).

    1. Na stránce **Fiskální konektory** (**Retail and Commerce \> Nastavení kanálu \> Fiskální integrace \> Fiskální konektory**), nahrajte konfiguraci XML pro každé zařízení nebo službu, které plánujete použít pro účely fislální integrace.

        > [!TIP]
        > Výběrem možnosti **Zobrazit** můžete zobrazit funkční a technické profily, které se vztahují k aktuálnímu fiskálnímu konektoru.

    2. Na stránce **Poskytovatelé fiskálního dokumentu** (**Retail and Commerce \> Nastavení kanálu \> Fiskální integrace \> Poskytovatelé fiskálního dokumentu**), nahrajte konfiguraci XML pro každé zařízení nebo službu, které plánujete použít pro účely fiskální integrace.

        > [!TIP]
        > Výběrem možnosti **Zobrazit** můžete zobrazit funkční a technické profily, které se vztahují k aktuálnímu poskytovateli fiskálního dokumentu.

    Příklady konfigurací fiskálních konektorů a poskytovatelů fiskálního dokumentu naleznete v tématu [Ukázky fiskální integrace v sadě Retail SDK](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-retail-sdk).

    > [!NOTE]
    > Mapování dat je považováno za součást poskytovatele fiskálního dokumentu. Chcete-li nastavit různá mapování dat pro stejný konektor (například pravidla pro konkrétní stav), měli byste vytvořit různé poskytovatele fiskálních dokumentů.

3. Vytvořte funkční profily konektoru a technické profily konektoru.

    1. Na stránce **Funkční profily konektoru** (**Retail and Commerce \> Nastavení kanálu \> Fiskální integrace \> Funkční profily konektoru**) vytvořte funkční profil konektoru pro každou kombinaci fiskálního konektoru a poskytovatele fiskálního dokumentu, který souvisí s fiskálním konektorem.

        1. Zvolte název konektoru.
        2. Vyberte poskytovatele dokumentu.

        Parametry mapování dat konektoru můžete změnit ve funkčním profilu konektoru. Chcete-li obnovit výchozí parametry, které jsou definovány v konfiguraci poskytovatele fiskálního dokumentu, vyberte **Aktualizovat**.

        **Příklady**

        |   | Formát | Příklad |
        |---|--------|---------|
        | **Nastavení sazeb DPH** | hodnota : VATrate | 1 : 2000, 2 : 1800 |
        | **Mapování kódů DPH** | VATcode : hodnota | vat20 : 1, vat18 : 2 |
        | **Mapování typů úhrad** | TenderType : hodnota | Hotovost : 1, Karta : 2 |

        > [!NOTE]
        > Funkční profily konektoru jsou specifické pro společnost. Pokud chcete používat stejnou kombinaci fiskálního konektoru a poskytovatele fiskálních dokumentů v různých společnostech, měli byste vytvořit funkční profil konektoru pro každou společnost.

    2. Na stránce **Technické profily konektoru** (**Retail and Commerce \> Nastavení kanálu \> Fiskální integrace \> Technické profily konektoru**) vytvořte technický profil konektoru pro každý fiskální konektor.

        1. Zvolte název konektoru.
        2. Zvolte typ konektoru. Pro zařízení, která jsou připojena k hardwarové stanici, vyberte **místní**.

            > [!NOTE]
            > Pouze místní konektory jsou aktuálně podporovány.

        Parametry na kartách **zařízení** a **nastavení** v technickém profilu konektoru lze změnit. Chcete-li obnovit výchozí parametry, které jsou definovány v konfiguraci fiskálního konektoru, vyberte **Aktualizovat**. V době, kdy se načítá nová verze konfigurace XML, obdržíte zprávu, která uvádí, že se současný poskytovatel fiskálního konektoru nebo dokumentu již používá. Tento postup nepřepíše ruční změny, dříve provedené ve funkčních a technických profilech konektoru. Chcete-li použít výchozí sadu parametrů z nové konfigurace, klikněte na tlačítko **Aktualizovat** na stránce **Funkční profily konektoru** a na stránce **Technické profily konektoru**.

4. Vytvořte skupiny fiskálních konektorů.

    Skupina fiskálních konektorů kombinuje fiskální konektory funkčních profilů, které provádí identické funkce a používají se ve stejné fázi v rámci procesu fiskální registrace. Například pokud lze v obchodě použít několik modelů fiskální tiskárny, lze fiskální konektory pro tyto tiskárny zkombinovat do skupiny fiskálního konektoru.

    1. Na stránce **Skupina fiskálních konektorů** (**Retail and Commerce \> Nastavení kanálu \> Fiskální integrace \> Skupiny fiskálních konektorů**) vytvořte novou skupinu fiskálních konektorů.
    2. Přidání funkčních profilů do skupiny konektoru. Klikněte na **Přidat** na stránce **Funkční profily** a vyberte číslo profilu. Ve skupině konektoru může mít každý fiskální konektor pouze jeden funkční profil.
    3. Pokud chcete pozastavit použití funkčního profilu, nastavte možnost **Zakázat** na **Ano**. Tato změna ovlivní pouze aktuální skupinu konektoru. Můžete pokračovat s použitím stejného funkčního profilu v jiných skupinách konektoru.

5. Vytvořte proces fiskální registrace.

    Proces fiskální registrace je definován sledem registračních kroků a skupinou konektorů používaných v každém kroku.

    1. Na stránce **Proces fiskální registrace** (**Retail and Commerce \> Nastavení kanálu \> Fiskální integrace \> Procesy fiskální registrace**) vytvořte nový záznam pro každý jedinečný proces fiskálních integrace.
    2. Přidejte kroky registrace do procesu:

        1. Vyberte **přidat**.
        2. Zvolte typ fiskálního konektoru:
        3. V poli **číslo skupiny** vyberte vhodnou skupinu fiskálního konektoru.

6. Přiřaďte entity procesu fiskální registrace profilům POS.

    1. Na stránce **Profily funkce POS** (**Retail and Commerce \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Funkční profily**) přidělte proces fiskální registrace funkčnímu profilu POS. Vyberte **Upravit** a poté na kartě **Fiskální registrace** v poli **Číslo procesu** vyberte proces.
    2. Na stránce **Hardwarový profil POS** (**Retail and Commerce \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Hardwarové profily**) přiřaďte technické profily konektoru hardwarovému profilu. Vyberte **upravit**, přidejte řádek na kartu **Fiskální periferní zařízení** a potom v poli **číslo profilu** vyberte profil technického konektoru.

    > [!NOTE]
    > Můžete přidat několik technických profilů ke stejnému hardwarovému profilu. Profil hardwaru nebo profil funkce POS, by však měl mít pouze jeden průsečík s libovolnou skupinou fiskálního konektoru.

    Tok fiskální registrace je definován procesem fiskální registrace a také určitými parametry komponent fiskální registrace: rozšíření Doba běhu obchodu pro poskytovatele fiskálního dokumentu a rozšíření Hardwarová stanice pro fiskální konektor.

    - Přihlášení k odběru akcí a transakcí pro fiskální registraci je u poskytovatele fiskálního dokumentu předdefinované.
    - Poskytovatel fiskálního dokumentu nese odpovědnost také za identifikaci fiskálního konektoru, který se používá k fiskální registraci. Odpovídá funkčním profilům konektoru, které jsou zahrnuty ve skupině fiskálních konektorů, která je zadaná pro aktuální krok procesu daňové registrace s technickým profilem konektoru, který je přiřazen profilu hardwaru hardwarové stanice, se kteoru je POS spárován.
    - Poskytovatel fiskálního dokumentu používá nastavení mapování dat z konfigurace poskytovatele fiskálního dokumentu k transformaci dat transakce nebo události, například daně a plateb, zatímco je generován daňový doklad.
    - Pokud poskytovatel fiskálního dokumentu vygeneruje daňový doklad, fiskální konektor ho může zaslat do fiskálního zařízení tak, jak je, nebo ho analyzovat a převést do sekvence příkazů v programovacím rozhraní aplikace zařízení (API) v závislosti na tom, jak je komunikace zpracovávána.

7. Na stránce **Proces fiskální registrace** (**Retail and Commerce \> Nastavení kanálu \> Fiskální integrace \> Procesy fiskální registrace**) vyberte **Ověřit** k ověření procesu fiskální registrace.

    Doporučujeme spustit tento typ ověření v následujících případech:

    - Pro nový proces registrace po dokončení všech nastavení, včetně přiřazení procesů registrace funkčním a hardwarovým profilům POS.
    - Poté, co provedete změny v existujícím procesu daňové registrace a pokud tyto změny způsobí výběr jiného fiskálního konektoru v době běhu (například když změníte skupinu konektoru pro krok procesu fiskální registrace, povolte funkční profil konektoru ve skupině konektoru nebo přidejte nový funkční profil konektoru skupině konektoru).
    - Po provedení změn v přiřazení technických profilů konektoru hardwarovým profilům.

8. Na stránce **Plán distribuce** spusťte úlohu **1070** a **1090** pro převod dat do databáze kanálů.

## <a name="set-up-fiscal-texts-for-discounts"></a>Nastavení fiskální textů pro slevy

V některých případech musí být vytištěn speciální text na fiskálním příjmu v případě, že je použita sleva. Na stránce **Skupina fiskálních konektorů** (**Retail and Commerce \> Nastavení kanálu \> Fiskální integrace \> Skupiny fiskálních konektorů**) můžete nastavit fiskální texty pro slevy.

- Pro ruční slevy, které jsou použity v POS, je třeba nastavit fiskální text pro informační kód nebo skupinu informačních kódů, která je určena jako informační kód **sleva na produkt** v profilu funkce POS.

    1. Na stránce **Skupina fiskálního konektoru** vyberte **Text pro fiskální příjem**.
    2. Na kartě **Informační kódy** vyberte **Přidat** a vyberte informační kód nebo skupinu informačních kódů.
    3. V poli **číslo informačního kódu** vyberte požadovanou hodnotu.
    4. V poli **Číslo podkódu** vyberte hodnotu, pokud je vyžadován pro vybraný informační kód.
    5. V poli **Text pro fiskální příjem** upřesněte fiskální text, který je vytisknut na fiskální příjemce.
    6. Nastavte možnost **Vytisknout vstup uživatele na fiskálním příjmu** na **ano**, aby se přepsal text na fiskálním příjmu informacemi, které uživatel ručně zadá v POS. Tato možnost se vztahuje pouze na informační kódy s typem vstupu **Text**.

    > [!NOTE]
    > Můžete zadat fiskální text pro několik informační kódy na podporu scénářů, kdy se používají skupiny informačních kódů, odkazované informační kódy a spuštěné informační kódy. V těchto situacích fiskální příjemka bude obsahovat fiskální texty ze všech informačních kódů, které jsou propojeny s řádkem transakce, kde byla aplikována sleva.

- Pro specifické slevy pro kanál byste měli definovat fiskální text pro ID slevy.

    1. Na stránce **Skupina fiskálního konektoru** vyberte **Text pro fiskální příjem**.
    2. Na kartě **Slevy** vyberte **Přidat** a vyberte ID slevy.
    3. V poli **Text pro fiskální příjem** upřesněte fiskální text, který je vytisknut na fiskální příjemce.

    > [!NOTE]
    > Pokud je na jednom řádku transakce použito několik slev, bude fiskální příjemka obsahovat fiskální texty ze všech slev spojených s tímto řádkem transakce.

## <a name="set-error-handling-settings"></a>Nastavení zpracování chyb

Možnosti zpracování chyb, které jsou dostupné ve fiskální integraci, jsou nastaveny v procesu fiskální registrace. Další informace o nakládání s chybami ve fiskální integraci uvádí téma [Zpracování chyb](fiscal-integration-for-retail-channel.md#error-handling).

1. Na stránce **Proces fiskální registrace** (**Retail and Commerce \> Nastavení kanálu \> Fiskální integrace \> Procesy fiskální registrace**) můžete nastavit následující parametry pro každý krok procesu fiskální integrace.

    - **Povolit přeskočení** – tento parametr aktivuje možnost **Přeskočit** v dialogovém okně Zpracování chyb.
    - **Povolit označení za registrované** – Tento parametr aktivuje možnost **Označit jako registrované** v dialogovém okně zpracování chyb.
    - **Pokračovat při chybě** – Pokud je tento parametr povolen, může proces fiskální registrace pokračovat v registru POS, pokud selže fiskální registrace transakce nebo události. V opačném případě musí provozovatel pro spuštění fiskální registrace další transakce nebo události zopakovat neúspěšnou fiskální registraci, přeskočit ji nebo označit transakci nebo událost za registrovanou. Další informace naleznete v tématu [Volitelná fiskální registrace](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Pokud je parametr **Pokračovat při chybě** povolen, parametry **Povolit přeskočení** a **Povolit označení za registrované** jsou automaticky zakázány.

2. Možnosti **Přeskočit** a **Označit jako registrované** v dialogovém okně zpracování chyb vyžadují oprávnění **Povolit přeskočení nebo označit jako registrované**. Proto na stránce **Skupiny oprávnění** (**Retail and Commerce \> Zaměstnanci \> Skupiny oprávnění**) povolte oprávnění **Povolit přeskočení registrace nebo označit jako registrované**.
3. Možnosti **Přeskočit** a **Označit jako registrované** umožňují operátorům zadat další informace v případě selhání fiskální registrace. Aby bylo možné tuto funkci zpřístupnit, měli byste určit informační kódy **přeskočit** a **označit jako registrované** ve fiskálním konektoru skupiny. Informace, které operátor zadá, jsou pak uloženy jako transakce informačního kódu spojené s fiskální transakcí. Další podrobnosti o informačních kódech naleznete v tématu [informační kódy a skupiny informačních kódů](../info-codes-retail.md).

    > [!NOTE]
    > Funkce spouštění **Produkt** není podporována pro informační kódy používané pro volby **Přeskočit** a **Označit jako registrované** ve skupinách fiskálního konektoru.

    - Na stránce **Skupiny fiskálního konektoru** na kartě **Informační kódy** vyberte informační kódy nebo skupiny informačních kódů v polích **přeskočit** a **Označit jako registrované**.

    > [!NOTE]
    > Jeden fiskální dokument a jeden nefiskální dokument lze generovat v jakémkoli kroku procesu daňové registrace. Rozšíření poskytovatele fiskálního dokumentu identifikuje všechny typy transakcí nebo událostí jako související s fiskálními nebo nefiskálními dokumenty. Funkce zpracování chyb platí pouze pro fiskální dokumenty.
    >
    > - **Daňový doklad** – povinný dokument, který by měl být úspěšně registrován (například jako fiskální příjemka).
    > - **Nefiskální dokument** – doplňkový doklad pro transakci nebo událost (například dárkový poukaz).

4. Pokud musí být provozovatel schopen pokračovat v zpracování aktuální operace (například vytvoření nebo dokončení transakce) po výskytu chyby při kontrole stavu, měli byste povolit oprávnění **Povolit přeskočení chyby při kontrole stavu** na stránce **Skupiny oprávnění** (**Retail and Commerce \> Zaměstnanci \> Skupiny oprávnění**). Další informace o postupu kontroly stavu naleznete v tématu [Kontrola stavu fiskální registrace](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Nastavení fiskálních sestav X/ Z z POS

Pokud chcete povolit spouštění fiskálních sestav z POS, měli byste do rozložení POS přidat nová tlačítka.

- Na stránce **Mřížky tlačítka** proveďte postup v části [Přidání operací POS do rozložení POS pomocí návrháře mřížky tlačítka](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) k instalaci mřížky tlačítka a aktualizaci rozložení POS.

    1. Výběr rozložení k aktualizaci 
    2. Přidejte nové tlačítko a nastavte vlastnost tlačítka **Tisknout fiskální X**.
    3. Přidejte nové tlačítko a nastavte vlastnost tlačítka **Tisknout fiskální Z**.
    4. Na stránce **Plán distribuce** spusťte úlohu **1090** pro převod změn do databáze kanálů.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Povolení ručního provedení odložené daňové registrace

Chcete-li povolit ruční provedení odložené fiskální registrace, měli byste přidat nové tlačítko do rozvržení POS.

- Na stránce **Mřížky tlačítka** proveďte postup v části [Přidání operací POS do rozložení POS pomocí návrháře mřížky tlačítka](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) k instalaci mřížky tlačítka a aktualizaci rozložení POS.

    1. Výběr rozložení k aktualizaci
    2. Přidejte nové tlačítko a nastavte vlastnost tlačítka **Dokončit proces fiskální registrace**.
    3. Na stránce **Plán distribuce** spusťte úlohu **1090** pro převod vašich změn do databáze kanálů.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]