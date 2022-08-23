---
title: Nastavení fiskální integrace pro obchodní kanály
description: Tento článek obsahuje pokyny pro nastavení funkce fiskální integrace pro velkoobchodní kanály.
author: EvgenyPopovMBS
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 9fd801395f2ba04c703734a1de7998d6a53b6462
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276122"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a>Nastavení fiskální integrace pro obchodní kanály

[!include [banner](../includes/banner.md)]

Tento článek obsahuje pokyny pro nastavení funkce fiskální integrace pro velkoobchodní kanály. Další informace o fiskální integraci naleznete v tématu [Přehled fiskální integrace pro velkoobchodní kanály](fiscal-integration-for-retail-channel.md).

## <a name="enable-features-in-commerce-headquarters"></a>Povolení funkcí v centrále Commerce

Chcete-li povolit funkce související s funkcí fiskální integrace pro obchodní kanály, postupujte takto.

1. V centru Commerce přejděte do nabídky **Správa systému \> Pracovní prostory \> Správa funkcí**.
1. Najděte a povolte následující funkce:

    - **Přímá fiskální integrace z registrů POS** – Tato funkce rozšiřuje rámec fiskální integrace přidáním schopnosti vytvářet fiskální konektory, které budou provozovány v místě prodeje (POS). Tento typ konektoru komunikuje s fiskálním zařízením nebo službou, která poskytuje aplikační programovací rozhraní HTTP (API) a nevyžaduje vyhrazený fyzický stroj v obchodě. Tato funkce například umožňuje fiskální integraci pro mobilní zařízení bez potřeby sdílené hardwarové stanice.
    - **Přepsání technického profilu fiskální integrace** – Tato funkce umožňuje rozšíření konfigurace fiskální integrace a přidává možnost kontroly parametrů připojení na stránce nastavení registru POS. Když je tato funkce povolena, můžete přepsat parametry technického profilu.
    - **Stav fiskální registrace registrů POS** – Když je tato funkce povolena, můžete zakázat proces fiskální registrace pro konkrétní registry POS. Pokud je pro registr POS zakázána fiskální registrace, nelze v tomto registru provádět prodejní transakce.
    - **Fiskální integrace zálohování místního úložiště** – Tato funkce rozšiřuje možnosti zpracování chyb rámce fiskální integrace. Umožňuje také automatické zálohování dat fiskální registrace v případě ztráty dat, takže data v místním úložišti jsou obnovena během aktivace zařízení.

## <a name="set-up-commerce-parameters"></a>Nastavení parametrů velkoobchodu

Chcete-li nastavit obecné parametry, postupujte následujícím způsobem.

1. Na stránce **Sdílené parametry velkoobchodu** na kartě **Obecné** nastavte možnost **Povolit fiskální integraci** na **Ano**.
1. Na kartě **Číselné řady** definujte číselné řady pro následující reference:

    - Číslo fiskálního technického profilu
    - Číslo skupiny fiskálních konektorů
    - Číslo procesu registrace

1. Na stránce **Parametry velkoobchodu** definujte číselné řady pro číslo fiskálního funkčního profilu.

> [!NOTE]
> Číselné řady jsou volitelné. Čísla pro všechny entity fiskální integrace lze generovat z číselných řad nebo ručně.

## <a name="set-up-a-fiscal-registration-process"></a>Nastavení procesu fiskální registrace

Proces nastavení fiskální integrace zahrnuje následující obecné úlohy:

- Konfigurace fiskálních konektorů, které reprezentují fiskální zařízení nebo služby používané pro účely fiskální registrace, jako jsou fiskální tiskárny.
- Nakonfigurujte poskytovatele dokumentů, kteří generují fiskální dokumenty k registraci ve fiskálních zařízeních nebo službách podle fiskálních konektorů.
- Nakonfigurujte proces fiskální registrace, který definuje pořadí kroků fiskální registrace a fiskálních konektorů a poskytovatelů fiskálních dokumentů používaných v jednotlivých krocích.
- Přiřaďte procesy fiskální registrace do funkčních profilů POS.
- Přiřadíte technické profily konektoru hardwarovým profilům.
- Přiřaďte technické profily hardwarovým profilům POS nebo funkce.

### <a name="upload-configurations-of-fiscal-document-providers"></a>Nahrání konfigurace poskytovatelů fiskálních dokumentů

Zprostředkovatel fiskálního dokumentu je zodpovědný za generování fiskálních dokumentů, které představují velkoobchodní transakce a události, které jsou zaregistrovány na POS ve formátu, který se používá pro interakci s fiskálním zařízením nebo službou. Poskytovatel fiskálního dokumentu například může generovat vyjádření fiskálního příjmu ve formátu XML.

Chcete-li nahrát konfigurace poskytovatelů fiskálních dokumentů,, postupujte takto.

1. V centrále Commerce přejděte na stránku **Poskytovatelé fiskálních dokumentů** (**Maloobchod a obchodování \> Nastavení kanálu \> Fiskální integrace \> Poskytovatelé fiskálních dokumentů**).
1. Nahrajte konfiguraci XML pro každé zařízení nebo službu, kterou plánujete používat.

> [!TIP]
> Výběrem možnosti **Zobrazit** můžete zobrazit funkční a technické profily, které se vztahují k aktuálnímu poskytovateli fiskálního dokumentu.

> [!NOTE]
> Mapování dat je považováno za součást poskytovatele fiskálního dokumentu. Chcete-li nastavit různá mapování dat pro stejný konektor (například pravidla pro konkrétní stav), měli byste vytvořit různé poskytovatele fiskálních dokumentů.

### <a name="upload-configurations-of-fiscal-connectors"></a>Nahrání konfigurace fiskálních konektorů

Fiskální konektor zodpovídá za komunikace s fiskálním zařízením nebo službu. Fiskální konektor může například odeslat fiskální příjem, který poskytovatel fiskálních dokumentů vytvořil ve formátu XML pro fiskální tiskárnu. Podrobnější informace o součástech fiskální integrace najdete v části [Ukázky procesu fiskální registrace pro fiskální zařízení a služby](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

Chcete-li nahrát konfigurace fiskálních konektorů,, postupujte takto.

1. V centrále Commerce přejděte na stránku **Fiskální konektory** (**Maloobchod a obchodování \> Nastavení kanálu \> Fiskální integrace \> Fiskální konektory**).
1. Nahrajte konfiguraci XML pro každé zařízení nebo službu, kterou plánujete používat pro účely fiskální integrace.

> [!TIP]
> Výběrem možnosti **Zobrazit** můžete zobrazit funkční a technické profily, které se vztahují k aktuálnímu fiskálnímu konektoru.

Příklady konfigurací fiskálních konektorů a poskytovatelů fiskálního dokumentu naleznete v tématu [Ukázky fiskální integrace v sadě Commerce SDK](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-commerce-sdk).

### <a name="create-connector-functional-profiles"></a>Vytvoření funkčních profilů konektoru

Při vytváření funkčního profilu konektoru postupujte takto.

1. V centrále Commerce přejděte na stránku **Funkční profily konektoru** (**Maloobchod a obchodování \> Nastavení kanálu \> Fiskální integrace \> Funkční profily konektoru**).
1. Pro každou kombinaci fiskálního konektoru a poskytovatele fiskálních dokumentů, která souvisí s tímto fiskálním konektorem, vytvořte funkční profil konektoru následujícím postupem.

    1. Zvolte název konektoru.
    1. Vyberte poskytovatele dokumentu.

#### <a name="change-data-mapping-parameters-in-a-connector-functional-profile"></a>Změna parametrů mapování dat ve funkčním profilu konektoru

Parametry mapování dat konektoru můžete změnit ve funkčním profilu konektoru. Následující tabulka uvádí některé příklady parametrů mapování dat ve funkčním profilu konektoru.

| Parametr | Formát | Příklad |
|-----------|--------|---------|
| Nastavení sazeb DPH | hodnota : VATrate | 1 : 2000, 2 : 1800 |
| Mapování kódů DPH | VATcode : hodnota | vat20 : 1, vat18 : 2 |
| Mapování typů úhrad | TenderType : hodnota | Hotovost : 1, Karta : 2 |

Chcete-li obnovit výchozí parametry, které jsou definovány v konfiguraci poskytovatele fiskálního dokumentu, na vyberte stránce **Funkční profily konektoru** možnost **Aktualizovat**.

> [!NOTE]
> Funkční profily konektoru jsou specifické pro společnost. Pokud chcete používat stejnou kombinaci fiskálního konektoru a poskytovatele fiskálních dokumentů pro různé společnosti, měli byste vytvořit funkční profil konektoru pro každou společnost.

### <a name="create-connector-technical-profiles"></a>Vytvoření technických profilů konektoru

Při vytváření technického profilu konektoru postupujte takto.

1. V centrále Commerce přejděte na stránku **Technické profily konektoru** (**Maloobchod a obchodování \> Nastavení kanálu \> Fiskální integrace \> Technické profily konektoru**).
1. Vytvořte technický profil konektoru pro každý fiskální konektor podle následujících kroků:

    1. Zvolte název konektoru.
    1. Zvolte typ konektoru:

        - U zařízení nebo služeb, které jsou připojeny k hardwarové stanici nebo jsou přítomny v místní síti, vyberte **Místní**.
        - U externích služeb vyberte **Externí**.
        - U interních konektorů v Commerce Runtime (CRT) vyberte **Vnitřní**. 

    1. Vyberte umístění konektoru:

        - Pokud je konektor umístěn na hardwarové stanici, vyberte **Hardwarová stanice**.
        - Pokud je konektor umístěn v registru POS, vyberte **Registrovat**.

Parametry na kartách **zařízení** a **nastavení** v technickém profilu konektoru lze změnit. Chcete-li obnovit výchozí parametry, které jsou definovány v konfiguraci fiskálního konektoru, vyberte **Aktualizovat**. V době, kdy se načítá nová verze konfigurace XML, obdržíte zprávu, která uvádí, že se současný poskytovatel fiskálního konektoru nebo dokumentu již používá. Tento postup nepřepíše ruční změny, dříve provedené ve funkčních a technických profilech konektoru. Chcete-li použít výchozí sadu parametrů z nové konfigurace, vyberte **Aktualizovat** na stránce **Funkční profily konektoru** nebo na stránce **Technické profily konektoru**.

Pokud musíte nastavit specifické parametry pro jednotlivý registr POS nebo obchod, postupujte takto.

1. V nabídce vyberte položku **Přepsat**.
1. Na stránce **Přepsat** vytvořte nový záznam.
1. Vyberte obchod nebo POS registr. Parametry vybraného technického profilu můžete přepsat pro jednotlivý POS registr nebo všechny POS registry v jednotlivé prodejně.
1. Na stránce **Zařízení** zadejte parametry pro vybraný POS registr nebo obchod.

### <a name="create-fiscal-connector-groups"></a>Vytvoření skupin fiskálních konektorů

Skupina fiskálních konektorů kombinuje fiskální konektory funkčních profilů, které provádí identické funkce a používají se ve stejné fázi v rámci procesu fiskální registrace. Například pokud lze v obchodě použít několik modelů fiskální tiskárny, lze fiskální konektory pro tyto tiskárny zkombinovat do skupiny fiskálního konektoru.

Pokud chcete vytvořit skupinu fiskálního konektoru, postupujte takto.

1. Přejděte na stránku **Skupina fiskálních konektorů** (**Maloobchod a obchodování \> Nastavení kanálu \> Fiskální integrace \> Skupiny fiskálních konektorů**).
1. Vytvořte novou skupinu fiskálních konektorů.
1. Přidání funkčních profilů do skupiny konektoru. Klikněte na **Přidat** na stránce **Funkční profily** a vyberte číslo profilu. Ve skupině konektoru může mít každý fiskální konektor pouze jeden funkční profil.
1. Pokud chcete pozastavit použití funkčního profilu, nastavte možnost **Zakázat** na **Ano**. Tato změna ovlivní pouze aktuální skupinu konektoru. Můžete pokračovat s použitím stejného funkčního profilu v jiných skupinách konektoru.

### <a name="create-a-fiscal-registration-process"></a>Vytvoření procesu fiskální registrace

Proces fiskální registrace je definován sledem registračních kroků a skupinou konektorů používaných v každém kroku.

Při vytvoření procesu fiskální registrace postupujte takto:

1. V centrále Commerce přejděte na stránku **Proces fiskální registrace** (**Maloobchod a obchodování \> Nastavení kanálu \> Fiskální integrace \> Proces fiskální registrace**).
1. Vytvořte nový záznam pro každý jedinečný proces fiskální registrace.
1. Kroky registrace do procesu přidejte takto:

    1. Vyberte **přidat**.
    1. Zvolte typ fiskálního konektoru:
    1. V poli **číslo skupiny** vyberte vhodnou skupinu fiskálního konektoru.

### <a name="assign-entities-of-the-fiscal-registration-process-to-pos-profiles"></a>Přiřazení entit procesu fiskální registrace k profilům POS

Entity procesu fiskální registrace přiřaďte k profilům POS takto.

1. V centrále Commerce přejděte na stránku **Funkční profily POS** (**Maloobchod a obchodování \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Funkční profily**). 
1. Přiřaďte procesy fiskální registrace do funkčního profilu POS.
1. Vyberte **Upravit** a poté na kartě **Fiskální registrace** v poli **Číslo procesu** vyberte proces.
1. Na kartě **Fiskální služby** vyberte technické profily konektoru s umístěním konektoru **Registr**.
1. Přejděte na stránku **Hardwarový profil POS** (**Maloobchod a obchodování \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Hardwarové profily**).
1. Přiřaďte technické profily konektoru k hardwarovému profilu. 
1. Vyberte položku **Upravit** a poté na kartě **Fiskální periferie** přidejte řádek. 
1. Zvolte technický profil konektoru v poli **Číslo profilu**.
1. Na kartě **Fiskální periferie** vyberte technické profily konektoru s umístěním konektoru **Hardwarová stanice**.

> [!NOTE]
> Můžete přidat několik technických profilů ke stejnému hardwarovému profilu. Profil hardwaru nebo profil funkce POS, by však měl mít pouze jeden průsečík s libovolnou skupinou fiskálního konektoru.

Tok fiskální registrace je definován procesem fiskální registrace a také určitými parametry komponent fiskální registrace: rozšíření CRT pro poskytovatele fiskálního dokumentu a rozšíření Hardwarová stanice pro fiskální konektor.

- Přihlášení k odběru akcí a transakcí pro fiskální registraci je u poskytovatele fiskálního dokumentu předdefinované.
- Poskytovatel fiskálního dokumentu nese odpovědnost také za identifikaci fiskálního konektoru, který se používá k fiskální registraci. Odpovídá funkčním profilům konektoru, které jsou zahrnuty ve skupině fiskálních konektorů, která je zadaná pro aktuální krok procesu daňové registrace s technickým profilem konektoru, který je přiřazen profilu hardwaru hardwarové stanice, se kteoru je POS spárován.
- Poskytovatel fiskálního dokumentu používá nastavení mapování dat z konfigurace poskytovatele fiskálního dokumentu k transformaci dat transakce nebo události, například daně a plateb, zatímco je generován daňový doklad.
- Pokud poskytovatel fiskálního dokumentu vygeneruje daňový doklad, fiskální konektor ho může zaslat do fiskálního zařízení tak, jak je, nebo ho analyzovat a převést do sekvence příkazů v rozhraní API v závislosti na tom, jak je komunikace zpracovávána.

### <a name="set-up-registers-with-fiscal-registration-restrictions"></a>Nastavte registry s omezeními fiskální registrace

Můžete si vybrat registry, kde je fiskální registrace zakázána, například v případech, kdy potřebujete na těchto zařízeních poskytovat pouze nefiskální operace, jako je vyhledávání v katalogu produktů, vyhledávání zákazníků nebo vytváření konceptů transakcí.

K nastavení registry s omezeními fiskální registrace postupujte následovně.

1. V ústředí Commerce Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Proces fiskální registrace**.
1. Vyberte požadovaný proces.
1. Vyberte kartu **Registry POS s omezením fiskálních procesů**.
1. Podle potřeby přidejte registry POS s omezením fiskálních procesů.

### <a name="validate-the-fiscal-registration-process"></a>Ověření procesu fiskální registrace

Doporučujeme ověřit proces fiskální registrace v následujících případech:

- Dokončili jste všechna nastavení pro nový registrační proces. Tato nastavení zahrnují přiřazení registračních procesů k funkčním profilům POS a hardwarovým profilům.
- Provedli jste změny ve stávajícím procesu fiskální registrace a tyto změny mohou způsobit výběr jiného fiskálního konektoru za běhu aplikace. (Například jste změnili skupinu konektorů pro krok procesu fiskální registrace, povolili jste funkční profil konektoru ve skupině konektorů nebo jste do skupiny konektorů přidali nový funkční profil konektoru.)
- Provedli jste změny v přiřazení technických profilů konektoru k hardwarovým profilům.

Při ověření procesu fiskální registrace postupujte takto.

1. V centrále Commerce přejděte na stránku **Proces fiskální registrace** (**Maloobchod a obchodování \> Nastavení kanálu \> Fiskální integrace \> Proces fiskální registrace**).
1. Vyberte položku **Ověřit** a ověřte proces fiskální registrace.
1. Na stránce **Plán distribuce** spusťte úlohu **1070** a **1090** pro převod dat do databáze kanálů.

## <a name="set-up-fiscal-texts-for-discounts"></a>Nastavení fiskální textů pro slevy

V některých případech musí být vytištěn speciální text na fiskálním příjmu v případě, že je použita sleva. Na stránce **Skupina fiskálních konektorů** (**Maloobchod a obchodování \> Nastavení kanálu \> Fiskální integrace \> Skupiny fiskálních konektorů**) můžete nastavit fiskální texty pro slevy.

- Pro ruční slevy, které jsou použity v POS, je třeba nastavit fiskální text pro informační kód nebo skupinu informačních kódů, která je určena jako informační kód **sleva na produkt** v profilu funkce POS.

    1. Na stránce **Skupina fiskálního konektoru** vyberte **Text pro fiskální příjem**.
    1. Na kartě **Informační kódy** vyberte **Přidat** a vyberte informační kód nebo skupinu informačních kódů.
    1. V poli **číslo informačního kódu** vyberte požadovanou hodnotu.
    1. V poli **Číslo podkódu** vyberte hodnotu, pokud je vyžadován pro vybraný informační kód.
    1. V poli **Text pro fiskální příjem** upřesněte fiskální text, který je vytisknut na fiskální příjemce.
    1. Nastavte možnost **Vytisknout vstup uživatele na fiskálním příjmu** na **ano**, aby se přepsal text na fiskálním příjmu informacemi, které uživatel ručně zadá v POS. Tato možnost se vztahuje pouze na informační kódy s typem vstupu **Text**.

    > [!NOTE]
    > Můžete zadat fiskální text pro několik informační kódy na podporu scénářů, kdy se používají skupiny informačních kódů, odkazované informační kódy a spuštěné informační kódy. V těchto situacích fiskální příjemka bude obsahovat fiskální texty ze všech informačních kódů, které jsou propojeny s řádkem transakce, kde byla aplikována sleva.

- Pro specifické slevy pro kanál byste měli definovat fiskální text pro ID slevy.

    1. Na stránce **Skupina fiskálního konektoru** vyberte **Text pro fiskální příjem**.
    1. Na kartě **Slevy** vyberte **Přidat** a vyberte ID slevy.
    1. V poli **Text pro fiskální příjem** upřesněte fiskální text, který je vytisknut na fiskální příjemce.

    > [!NOTE]
    > Pokud je na jednom řádku transakce použito několik slev, bude fiskální příjemka obsahovat fiskální texty ze všech slev spojených s tímto řádkem transakce.

## <a name="set-error-handling-settings"></a>Nastavení zpracování chyb

Možnosti zpracování chyb, které jsou dostupné ve fiskální integraci, jsou nastaveny v procesu fiskální registrace. Další informace o nakládání s chybami ve fiskální integraci uvádí téma [Zpracování chyb](fiscal-integration-for-retail-channel.md#error-handling).

Chcete-li nastavit zpracování chyb, postupujte takto.

1. Na stránce **Proces fiskální registrace** (**Maloobchod a obchodování \> Nastavení kanálu \> Fiskální integrace \> Procesy fiskální registrace**) můžete nastavit následující parametry pro každý krok procesu fiskální integrace.

    - **Povolit přeskočení** – tento parametr aktivuje možnost **Přeskočit** v dialogovém okně Zpracování chyb.
    - **Povolit označení za registrované** – Tento parametr aktivuje možnost **Označit jako registrované** v dialogovém okně zpracování chyb.
    - **Povolit odložení** – Tento parametr aktivuje možnost **Odložit** v dialogovém okně Zpracování chyb.
    - **Pokračovat při chybě** – Pokud je tento parametr povolen, může proces fiskální registrace pokračovat v registru POS, pokud selže fiskální registrace transakce nebo události. V opačném případě musí provozovatel pro spuštění fiskální registrace další transakce nebo události zopakovat neúspěšnou fiskální registraci, přeskočit ji nebo označit transakci nebo událost za registrovanou. Další informace naleznete v tématu [Volitelná fiskální registrace](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).

    > [!NOTE]
    > Pokud je parametr **Pokračovat při chybě** povolen, parametry **Povolit přeskočení** a **Povolit označení za registrované** jsou automaticky zakázány.

1. Možnosti **Přeskočit** a **Označit jako registrované** v dialogovém okně zpracování chyb vyžadují aktivaci oprávnění **Povolit přeskočení nebo označit jako registrované**. Chcete-li aktivovat oprávnění, přejděte na stránku **Skupiny oprávnění** (**Maloobchod a obchodování \> Zaměstnanci \> Skupiny oprávnění**) a nastavte možnost **Povolit přeskočení registrace nebo označit jako registrované** na **Ano**.
1. Možnost **Odložení** v dialogovém okně Zpracování chyb vyžaduje, aby bylo aktivováno oprávnění **Povolit odložení**. Chcete-li aktivovat oprávnění, přejděte na stránku **Skupiny oprávnění** (**Maloobchod a obchodování \> Zaměstnanci \> Skupiny oprávnění**) a nastavte možnost **Povolit přeskočení registrace nebo označit jako registrované** na **Ano**.
1. Možnosti **Přeskočit**, **Označit jako registrované** a **Odložit** umožňují operátorům zadat další informace v případě selhání fiskální registrace. Aby bylo možné tuto funkci zpřístupnit, měli byste určit informační kódy **Přeskočit**, **Označit jako registrované** a **Odložit** ve fiskálním konektoru skupiny. Informace, které operátor zadá, jsou pak uloženy jako transakce informačního kódu spojené s fiskální transakcí. Další podrobnosti o informačních kódech naleznete v tématu [informační kódy a skupiny informačních kódů](../info-codes-retail.md).

    > [!NOTE]
    > Funkce spouštění **Produkt** není podporována pro informační kódy používané pro volby **Přeskočit** a **Označit jako registrované** ve skupinách fiskálního konektoru.

    - Na stránce **Skupina fiskálního konektoru** na kartě **Informační kódy** vyberte informační kódy nebo skupiny informačních kódů v polích **Přeskočit**, **Označit jako registrované** a **Odložit**.

    > [!NOTE]
    > Jeden fiskální dokument a jeden nefiskální dokument lze generovat v jakémkoli kroku procesu daňové registrace. Rozšíření poskytovatele fiskálního dokumentu identifikuje všechny typy transakcí nebo událostí jako související s fiskálními nebo nefiskálními dokumenty. Funkce zpracování chyb platí pouze pro fiskální dokumenty.
    >
    > - **Daňový doklad** – povinný dokument, který by měl být úspěšně registrován (například jako fiskální příjemka).
    > - **Nefiskální dokument** – doplňkový doklad pro transakci nebo událost (například dárkový poukaz).

1. Pokud musí být provozovatel schopen pokračovat v zpracování aktuální operace (například vytvoření nebo dokončení transakce) po výskytu chyby při kontrole stavu, měli byste povolit oprávnění **Povolit přeskočení chyby při kontrole stavu** na stránce **Skupiny oprávnění** (**Maloobchod a obchodování \> Zaměstnanci \> Skupiny oprávnění**). Další informace o postupu kontroly stavu naleznete v tématu [Kontrola stavu fiskální registrace](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a>Nastavení fiskálních sestav X/ Z z POS

Pokud chcete povolit spouštění fiskálních sestav z POS, měli byste do rozložení POS přidat nová tlačítka.

- Na stránce **Mřížky tlačítka** proveďte postup v části [Přidání operací POS do rozložení POS pomocí návrháře mřížky tlačítka](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) k instalaci mřížky tlačítka a aktualizaci rozložení POS.

    1. Výběr rozložení k aktualizaci 
    1. Přidejte nové tlačítko a nastavte vlastnost tlačítka **Tisknout fiskální X**.
    1. Přidejte nové tlačítko a nastavte vlastnost tlačítka **Tisknout fiskální Z**.
    1. Na stránce **Plán distribuce** spusťte úlohu **1090** pro převod změn do databáze kanálů.

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a>Povolení ručního provedení odložené daňové registrace

Chcete-li povolit ruční provedení odložené fiskální registrace, měli byste přidat nové tlačítko do rozvržení POS.

- Na stránce **Mřížky tlačítka** proveďte postup v části [Přidání operací POS do rozložení POS pomocí návrháře mřížky tlačítka](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) k instalaci mřížky tlačítka a aktualizaci rozložení POS.

    1. Výběr rozložení k aktualizaci
    1. Přidejte nové tlačítko a nastavte vlastnost tlačítka **Dokončit proces fiskální registrace**.
    1. Na stránce **Plán distribuce** spusťte úlohu **1090** pro převod vašich změn do databáze kanálů.


## <a name="view-connection-parameters-and-other-information-in-pos"></a>Zobrazení parametrů připojení a dalších informací v POS

Chcete-li zobrazit parametry připojení a další informace v systému POS, postupujte podle následujících kroků.

1. Otevřete Modern POS (MPOS) nebo Cloud POS (CPOS).
1. Vyberte **Nastavení**. Pokud je fiskální integrace povolena, zobrazí se v části **Fiskální integrace** vpravo následující informace:

    - Stav fiskální registrace
    - Stav poslední fiskální transakce
    - Počet čekajících událostí auditu

1. Vyberte **Detaily** k zobrazení následujících informací:

    - Kroky procesu registrace
    - Parametry připojení
    - Podrobnosti událostí auditu
 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
