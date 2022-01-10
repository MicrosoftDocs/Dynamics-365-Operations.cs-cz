---
title: Ukázka integrace fiskální služby pro Německo
description: V tomto tématu je uveden přehled ukázkové fiskální integrace pro Německo v Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-5-29
ms.openlocfilehash: ca747215a8dfb85237365880ad5bdd49e57ec949
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944681"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>Ukázka integrace fiskální služby pro Německo

[!include[banner](../includes/banner.md)]

V tomto tématu je uveden přehled ukázkové fiskální integrace pro Německo v Microsoft Dynamics 365 Commerce.

Pro účely splnění fiskálních požadavků na registrační pokladny v Německu obsahuje funkce Microsoft Dynamics 365 Commerce pro Německo vzorovou integraci pokladního místa (POS) s externí fiskální registrační službou. Vzorek rozšiřuje [funkci fiskální integrace](fiscal-integration-for-retail-channel.md). Je založena na řešení [EFR (Electronic Fiscal Register)](https://www.efsta.eu/de/fiskalloesungen/deutschland) od [EFSTA](https://www.efsta.eu/de/) a umožňuje komunikaci se službou EFR přes protokol HTTPS. Služba EFR by měla být hostována buď na hardwarové stanici Retail nebo na samostatném počítači, se kterým se lze propojit z hardwarové stanice. Ukázka je poskytnuta ve formě zdrojového kódu a je součástí sady software development kit (SDK) pro maloobchod.

Společnost Microsoft nevydává žádný hardware, software nebo dokumentaci k EFSTA. Informace o tom, jak řešení EFR získat a provozovat, vám poskytne [EFSTA](https://www.efsta.eu/de/kontakt/kontakt).

## <a name="scenarios"></a>Scénáře

Následující scénáře uvádějí ukázku integrace služby fiskální registrace pro Německo.

### <a name="sales-operations"></a>Prodejní operace

- **Registrace prodeje a vrácení typu cash and carry ve službě fiskální registrace:**

    Registrace prodejních operací zahrnuje následující kroky:

    1. Registrace zahájení transakce

        Zahájení každé transakce je registrováno v technickém zabezpečovacím prvku (TSE), který je napojen na službu EFR. Výsledkem procesu registrace je přiřazení ID transakce (TID) prvkem TSE.

    2. Registrace ukončení transakce

        Když je transakce uzavřena v POS, je zaregistrována pomocí stejného TID, které bylo přiděleno při registraci zahájení transakce. V tuto chvíli jsou odeslána podrobná data transakce do služby fiskální registrace. Tyto údaje obsahují informace o řádku prodeje a informace o slevách, platbách a daních

    3. Zaznamenání odpovědi ze služby fiskální registrace

        Data zabezpečení jsou přijata z TSE jako součást odpovědi a uložena v transakci v databázi kanálů. Data zabezpečení tvoří následující informace:

        - TID
        - Datum a čas zahájení transakce
        - Datum a čas ukočnení transakce
        - Čítač podpisů
        - Hodnota šeku
        - Sériové číslo prvku TSE

- **Registrace zákaznických objednávek ve službě fiskální registrace:** Proces registrace je stejný jako proces prodeje a vrácení typu cash and carry.
- **Registrace operací zahrnujících dárkové poukazy a vklady:** Proces registrace je stejný jako proces prodeje a vrácení typu cash and carry.

#### <a name="notifying-users-about-fiscal-registration-failures"></a>Upozorňování uživatelů na selhání fiskální registrace

Existují dva způsoby, jak může služba fiskální registrace upozornit uživatele na selhání, ke kterým došlo během fiskální registrace:

- Vytištění dalších informací z odpovědi v poli **Informační zpráva** na příjemkách.
- Zobrazení oznámení z fiskální služby jako zprávu uživatele v POS.

    > [!NOTE]
    > Tento oznamovací mechanismus vyžaduje, aby byl zapnutý parametr **Zobrazit oznámení o fiskální registraci** na stránce **Technické profily konektoru**.

#### <a name="printing-receipts"></a>Tisk příjemek

Tisk příjemek je v Německu povinný. Všechny příjemky musí obsahovat alespoň tyto informace:

- Název a adresu společnosti
- Informace o zboží, včetně cen a množství
- Informace o přijatých platbách
- Informace o daních, včetně celkových částek podle daňové sazby
- Data zabezpečení:

    - TID
    - Datum a čas zahájení transakce
    - Datum a čas ukočnení transakce
    - Čítač podpisů
    - Hodnota šeku
    - Sériové číslo prvku TSE

- Informační zpráva

> [!NOTE]
> QR kód lze vytisknout i na příjemky. Přestože je QR kód volitelný, důrazně se doporučuje. Další informace, jak získat QR kód jako součást odpovědi ze služby fiskální registrace, naleznete v dokumentu „Příručka EFR \[DE\]“, který je veřejně dostupný na webu [Dokumentace EFSTA](https://public.efsta.net/efr/).
>
> Pole **Informační zpráva** na příjemkách obsahuje oznámení ze služby fiskální registrace. Pokud je například rozbité podpisové zařízení, lze na příjemku vytisknout speciální text.

#### <a name="voided-suspended-and-recalled-transactions"></a>Anulované, pozastavené a odvolané transakce

- Anulovaná transakce je registrována jako požadavek na ukončení transakce ve službě fiskální registrace.
- Pozastavená transakce je registrována jako požadavek na ukončení transakce ve službě fiskální registrace.
- Odvolání pozastavené transakce je registrováno jako zahájení nové transakce ve službě fiskální registrace.

### <a name="non-sales-transactions-and-shift-closing"></a>Neprodejní transakce a uzavírání směn

Následující neprodejní transakce jsou registrovány jako nefiskální operace ve službě fiskální registrace s použitím značky **NFS**:

- Počáteční částka výkazu
- Zadání plovoucího zůstatku
- Odstranění úhrady
- Odvod do trezoru
- Odvod do banky
- Účty příjmů
- Účty výdajů

Operace **Zavřít směnu** je také registrována jako nefiskální operace ve službě fiskální registrace s použitím značky **NFS**.

### <a name="data-export-and-audit"></a>Export dat a audit

Všechny transakce musí být podepsány prvkem TSE, aby byla zajištěna jejich integrita, pravost a úplnost a aby se zabránilo manipulaci se zaznamenanými daty.

> [!WARNING]
> Lze použít pouze certifikovaný prvek TSE. Informace o typech a modelech prvků TSE, které jsou podporovány v řešení EFR, naleznete v dokumentu „Příručka k EFR \[DE\]“, který je veřejně dostupný na webu [Dokumentace EFSTA](https://public.efsta.net/efr/). Pro informace, jak zvolit a získat prvek TSE, kontaktujte [EFSTA](https://www.efsta.eu/at/kontakt).

Předpisy v Německu vyžadují podporu pro export DSFinV-K. Export DSFinV-K lze aktivovat v řešení EFR. Další informace o exportu DSFinV-K naleznete v dokumentu „Příručka k EFR \[DE\]“, který je veřejně dostupný na webu [Dokumentace EFSTA](https://public.efsta.net/efr/).

### <a name="limitations-of-the-sample"></a>Omezení vzorku

Služba daňové registrace podporuje pouze scénáře, kde je součástí cen daň z prodeje. Proto musí být možnost **Ceny zahrnují DPH** nastavena na **Ano** pro obchody a odběratele.

Fiskální služba nepodporuje situace, kdy je na stejný řádek transakce použit více než jeden kód DPH.

Rámec fiskální integrace nepodporuje prodejní nabídky. Tyto operace tedy nejsou registrovány ve fiskální službě.

## <a name="set-up-commerce-for-germany"></a>Natavení aplikace Commerce pro Německo

Tato část popisuje nastavení Commerce, která jsou specifická a doporučená pro Německo. Další informace o nastavení naleznete v tématu [Domovská stránka Commerce](../index.md).

Chcete-li použít funkci specifickou pro Německo, je nutné zadat následující nastavení.

- V primární adrese právnické osoby nastavte pole **Země/oblast** na **DEU** (Německo).
- V profilu funkce POS každého obchodu, který se nachází v rámci Německa, nastavte pole **kód ISO** na **DE** (Německo).

Zadejte také následující nastavení pro Německo. Po dokončení instalace nezapomeňte spustit příslušné distribuční úlohy.

### <a name="set-up-vat-per-german-requirements"></a>Nastavení DPH podle německých požadavků

Musíte vytvořit kódy DPH, skupiny daní DPH a skupiny DPH za zboží. Musíte také nastavit informace o DPH pro produkty a služby. Další informace o způsobu nastavení a použití funkcí DPH získáte v části [Přehled DPH](../../finance/general-ledger/indirect-taxes-overview.md).

Na příjemky můžete vytisknout zkrácený kód daně z obratu (například „A“ nebo „B“). Chcete-li tuto funkci zpřístupnit, nastavte pole **Kód pro tisk** na stránce **Kódy DPH**.

### <a name="set-up-stores"></a>Nastavení obchodů

Na stránce **Všechny obchody** aktualizujte podrobnosti o obchodu. Je nutné konkrétně nastavit následující parametry:

- V poli **Skupina DPH** zadejte skupinu DPH, kterou chcete použít pro prodeje výchozímu odběrateli.
- Nastavte možnost **Ceny jsou včetně DPH** na **Ano**.
- V poli **název** zadejte název společnosti. Tato změna pomáhá zajistit, že se název společnosti zobrazí na dokladu o prodeji. Případně můžete přidat název společnosti na prodejní doklad jako volný text.
- Nastavte **daňové identifikační číslo (DIČ)** na identifikační číslo společnosti. Tato změna pomáhá zajistit, že se identifikační číslo společnosti zobrazí na dokladu o prodeji. Případně můžete přidat identifikační číslo společnosti na prodejní doklad jako volný text.

### <a name="set-up-functionality-profiles"></a>Nastavení funkčních profilů

Nastavte funkční profily POS. Na pevné záložce **Číslování dokladů** nastavte číslování dokladů vytvořením nebo aktualizací záznamů pro typy příjmových transakcí **Prodej**, **Prodejní objednávka** a **Vrácení**.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Nakonfigurujte vlastní pole tak, aby bylo možné použít je ve formátech příjemky pro prodejní příjemky

Můžete konfigurovat jazykový text a vlastní pole, která se používají ve formátech příjemky POS. Výchozí společnost uživatele, který vytvoří nastavení příjmu, musí být stejná právnická osoba, pro kterou se vytváří nastavení text jazyka. Alternativně lze vytvořit texty ve stejném jazyce, které mají být vytvořeny ve výchozí společnosti uživatele a právnické osobě prodejny, pro kterou se nastavení vytváří.

Na stránce **jazykový text** přidejte následující záznamy popisků vlastního pole rozvržení účtenky. Upozorňujeme, že hodnoty **ID jazyka**, **ID textu** a **Text**, které jsou zobrazeny v tabulce, jsou jenom příklady. Lze je změnit tak, aby splňovaly vaše požadavky. Hodnoty **ID textu**, které budete používat, však musí být jedinečné a musí být rovny nebo větší než 900001.

Přidejte následující štítky POS do oddílu **POS** na stránce **Text jazyka**.

| ID jazyka | ID textu | Text                                  |
|-------------|---------|---------------------------------------|
| cs       | 900001  | QR kód                               |
| cs       | 900002  | ID transakce                        |
| cs       | 900003  | Tiskový kód maloobchodní daně                 |
| cs       | 900004  | Částka daně (prodej)                    |
| cs       | 900005  | Daňový základ (prodej)                     |
| cs       | 900006  | Počáteční datum a čas transakce           |
| cs       | 900007  | Koncové datum a čas transakce             |
| cs       | 900008  | Sériové číslo prvku zabezpečení |
| cs       | 900009  | Čítač podpisů                     |
| cs       | 900010  | Hodnota šeku                           |
| cs       | 900011  | Informační zpráva                          |

Na stránce **Vlastní pole** přidejte následující záznamy popisků vlastního pole rozvržení účtenky. Upozorňujeme, že hodnoty **ID textu titulku** musí odpovídat hodnotám **ID textu**, které jste zadali na stránce **jazykový text**.

| Název                            | Typ    | ID textu titulku |
|---------------------------------|---------|-----------------|
| QRCODE\_DE                      | Příjemka | 900001          |
| TRANSACTIONID\_DE               | Příjemka | 900002          |
| RETAILPRINTCODE\_DE             | Příjemka | 900003          |
| SALESTAXAMOUNT\_DE              | Příjemka | 900004          |
| SALESTAXBASIS\_DE               | Příjemka | 900005          |
| TRANSACTIONSTARTDATETIME\_DE    | Příjemka | 900006          |
| TRANSACTIONENDDATETIME\_DE      | Příjemka | 900007          |
| SECURITYELEMENTSERIALNUMBER\_DE | Příjemka | 900008          |
| SIGNCOUNTER\_DE                 | Příjemka | 900009          |
| SIGN\_DE                        | Příjemka | 900010          |
| INFOMESSAGE\_DE                 | Příjemka | 900011          |

> [!NOTE]
> Je důležité, abyste zadali správné názvy vlastních polí, jak jsou uvedeny v předcházející tabulce. Nesprávný název vlastního pole způsobí chybějící data v příjemkách.

### <a name="configure-receipt-formats"></a>Konfigurace formátů příjemky

Pro každý poožadovaný formát příjemky změňte hodnotu pole **Chování tisku** na **Vždy tisknout**.

V Návrháři formátu příjemky přidejte následující vlastní pole do příslušných oddílů příjemky. Všimněte si, že názvy polí odpovídají jazykovým textům, které jste definovali v předchozím oddílu.

- **Záhlaví:** Přidejte následující pole:

    - **Název obchodu** a **Daňové identifikační číslo**: pole, která umožňují vytisknout na příjemky název a identifikační číslo společnosti. Případně můžete přidat název společnosti a identifikační číslo do rozložení jako volný text.
    - Pole **Adresa obchodu**, **Datum**, **Čas 24H**, **Číslo příjemky**, a **Číslo registrační pokladny**.

- **Řádky:** Přidejte následující pole:

    - Pole **Název položky**
    - Pole **Množství**
    - Pole **Celková cena s daní**
    - Pole **Tiskový kód maloobchodní daně**, které slouží k vytištění zkráceného kódu, který odpovídá kódu DPH, který se vztahuje k položce

- **Zápatí:** Přidejte následující pole:

    - Pole platby, aby se vytiskly částky platby pro každou metodu platby. Například přidejte pole **název úhrady** a **Částka úhrady** na jeden řádek rozvržení.
    - Pole ve skupině polí **Daňový rozpis**. Všechna pole v této skupině polí musí být vytištěna na jednom samostatném řádku.

        - Pole **DIČ**, což je standardní pole, které umožňuje vytisknout souhrn DPH pro každý kód DPH. Toto pole musí být přidáno na nový řádek.
        - Pole **Procento daně**, což je standardní pole, které se používá k tisku platné daňové sazby pro kód DPH.
        - Pole **Daňový základ (prodej)**, které slouží k vytisknutí celkové částky hotovostního prodeje pro kód DPH. Operace záloh a dárkových poukazů jsou vyloučeny.
        - Pole **Částka daně (prodej)**, které slouží k vytisknutí částky daně pro hotovostní prodeje pro kód DPH.
        - Pole **Tiskový kód maloobchodní daně**, které slouží k vytištění zkráceného kódu, který odpovídá kódu DPH.

    - Pole, která obsahují data zabezpečené transakce vrácená službou fiskální registrace:

        - Pole **ID transakce**, které identifikuje počet hotovostních transakcí služby fiskální registrace
        - Pole **Počáteční datum a čas transakce**
        - Pole **Koncové datum a čas transakce**
        - Pole **Sériové číslo prvku zabezpečení**
        - Pole **Čítač podpisů**
        - Pole **Hodnota šeku**
        - Pole **QR kód**, které slouží k vytištění odkazu na evidovanou hotovostní transakci ve formě QR kódu

        > [!NOTE]
        > Hodnota **QR kód** je načtena z odpovědi fiskálního registru. EFR vrací QR kód ve své odpovědi pouze v případě, že je hodnota pole **Atributy** v konfiguraci EFR popsána v dokumentaci EFSTA. Formát QR kódu v poli **Atributy** v konfiguraci EFR musí být nastaven na **BMP**.

    - Pole **Informační zpráva**, tkže zprávy oznámení ze služby fiskální registrace lze zobrazovat na příjemkách. Pokud je například rozbité podpisové zařízení, lze na příjemku vytisknout speciální text.

Další informace o tom, jak pracovat s formáty příjemek, naleznete v tématu [Nastavení a návrh formátů příjmu](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-germany"></a>Nastavení fiskální integrace pro Německo

Ukázka integrace služby fiskální registrace pro Německo je založena na [funkci fiskální integrace](fiscal-integration-for-retail-channel.md) a je součástí řešení Retail SDK. Ukázka se nachází ve složce **src\\FiscalIntegration\\Efr** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (například [ukázka ve verzi/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Ukázka [se skládá](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) ze zprostředkovatele fiskálního dokumentu, což je rozšíření řešení Commerce Runtime (CRT) a fiskálního konektoru, který je rozšířením hardwarové stanice Commerce. Další informace o použití sady Retail SDK naleznete v části [Architektura Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) a [Nastavení kanálu sestavení pro sadu SDK nezávislého balení](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači (VM) v Microsoft Dynamics Lifecycle Services (LCS). Další informace viz [Pokyny k nasazení ukázkové fiskální integrace pro Německo (starší verze)](emea-deu-fi-sample-sdk.md).
>
> Podpora nového modelu nezávislého balení a rozšíření pro vzorky fiskální integrace je plánována pro pozdější verze.

Postupujte podle kroků pro nastavení fiskální integrace popsané v části [Nastavení fiskální integrace pro kanály Commerce](setting-up-fiscal-integration-for-retail-channel.md):

1. [Nastavení procesu fiskální registrace](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Kromě toho si všimněte nastavení pro proces fiskální registrace, který je [specifický pro tuto ukázku služby fiskální registrace](#set-up-the-registration-process).
1. [Nastavení zpracování chyb](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

    > [!WARNING]
    > Možnosti zpracování chyb v rámci fiskální integrace nemusí být plně v souladu s místními fiskálními předpisy.
    >
    > - Doporučujeme, abyste ponechali vypnutou možnost **Pokračovat při chybě** na stánce **Proces fiskální registrace**, protože všechny transakce musí být správně registrovány, i když první pokus o fiskální registraci nebyl úspěšný.
    > - Než zapnete možnosti **Přeskočit** nebo **Označit jako registrované** na stránce **Proces fiskální registrace**, měli byste tyto změny v procesu fiskální registrace projednat se svým daňovým poradcem nebo místním finančním úřadem.

1. [Povolit ruční provedení zápisu odložené daňové registrace](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Konfigurace komponent kanálu](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Nastavení procesu registrace

Pokud chcete povolit registrační proces, postupujte pomocí následujících kroků pro nastavení centrály Commerce. Další informace viz [Nastavení fiskální integrace pro obchodní kanály](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Stáhněte si konfigurační soubory pro poskytovatele fiskálních dokumentů a fiskální konektor:

    1. Otevřete úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Vyberte správnou verzi větve vydání podle vaší verze SDK/aplikace (například **[vydání/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Otevřete **src \> FiscalIntegration \> Efr**.
    1. Stáhněte si konfigurační soubor poskytovatele fiskálních dokumentů v umístění **Configurations \> DocumentProviders \> DocumentProviderFiscalEFRSampleGermany.xml** (například [soubor k vydání/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleGermany.xml)).
    1. Stáhněte si konfigurační soubor fiskálního konektoru v umístění **Configurations \> Connectors \> ConnectorEFRSample.xml** (například [soubor k vydání/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači v LCS. Konfigurační soubory pro tuto ukázku fiskální integrace jsou umístěny v následujících složkách Retail SDK na vývojářském virtuálním počítači v LCS:
    >
    > - **Konfigurační soubor poskytovatele fiskálních dokumentů:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration\\DocumentProviderFiscalEFRSampleGermany.xml
    > - **Konfigurační soubor fiskálního konektoru:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration\\ConnectorEFRSample.xml
    > 
    > Podpora nového modelu nezávislého balení a rozšíření pro vzorky fiskální integrace je plánována pro pozdější verze.

1. Přejděte na možnost **Retail a Commerce \> Nastavení centrály \> Parametry \> Sdílené parametry obchodu**. Na kartě **Obecné** nastavte možnost **Povolit fiskální integraci** na **Ano**.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Poskytovatelé fiskálních dokumentů** a načtěte konfigurační soubor poskytovatele fiskálního dokumentu, který jste stáhli dříve.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Fiskální konektory** a načtěte konfigurační soubor fiskálního konektoru, který jste stáhli dříve.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Funkční profily Connector**. Vytvořte nový funkční profil konektoru. Vyberte poskytovatele dokumentu a dříve načtený konektor. Podle potřeby aktualizujte [nastavení mapování dat](#default-data-mapping).
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Technické profily Connector**. Vytvořte nový technický profil konektoru a vyberte fiskální konektor, který jste načetli předtím. Podle potřeby aktualizujte [nastavení konektoru](#fiscal-connector-settings).
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Skupiny fiskálního konektoru**. Vytvořte novou skupinu fiskálního konektoru pro funkční profil konektoru, který jste vytvořili předtím.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Fiskální integrace \> Proces fiskální registrace**. Vytvořte nový procesu daňové registrace a krok procesu fiskální registrace a vyberte skupinu fiskálního konektoru, kterou jste předtím vytvořili.
1. Přejděte na **Maloobchodní a velkoobchodní prodej \> Instalace kanálu \> Nastavení POS \> Profily POS \> Funkční profily**. Vyberte funkční profil, který je připojena k obchodu, kde by měl být aktivován proces registrace. Na pevné záložce **Proces fiskální registrace** vyberte proces fiskální registrace, který jste předtím vytvořili.
1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Hardwarové profily**. Vyberte hardwarový profil spojený s hardwarovou stanicí, ke které bude připojena fiskální tiskárna. Na pevné záložce **Fiskální příslušenství** vyberte technický profil konektoru, který jste vytvořili dříve.
1. Spusťte plán distribuce (**Retail a Commerce \> IT Retail a Commerce \> plán distribuce**) a vyberte úlohy **1070** a **1090** k přenosu dat do databáze kanálů.

#### <a name="default-data-mapping"></a>Výchozí mapování dat

Následující výchozí mapování dat je součástí konfigurace poskytovatele fiskálního dokumentu, který je poskytován jako ukázka fiskální integrace:

- **Mapování typu úhrad** – Mapování platebních metod na hodnoty atribut **PayG** (platební skupina) v požadavcích zasílaných fiskální službě. Zde je výchozí mapování:

    ```
    1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1
    ```

    První komponenta v každém páru představuje platební metodu, která je nastavena pro obchod. Druhá komponenta představuje odpovídající platební skupinu, která je podporována službou fiskální registrace EFR. Další informace o skupinách plateb, které EFR podporuje pro Německo, viz [Reference k EFR](https://public.efsta.net/efr/).

    Ukázkové mapování platebních metod odpovídá platebním metodám obchodu, které jsou konfigurovány ve standardních ukázkových datech.

    | Způsob platby | Název způsobu platby |
    |----------------|---------------------|
    | 1              | Hotovost                |
    | 2              | Zaškrtnutí               |
    | 3              | Karta                |
    | 4              | Účet zákazníka    |
    | 5              | Jiné               |
    | 6              | Měna            |
    | 7              | Doklad             |
    | 8              | Dárkový poukaz           |
    | 9              | Úhrada – odebrat/plovoucí |
    | 10             | Věrnostní karty       |
    | 11             | Nelokální šeky    |

    Proto musíte upravit vzorové mapování podle platebních metod, které jsou nakonfigurovány ve vaší aplikaci.

- **Zahrnout zákaznická data** – Pokud je tento parametr zapnutý, budou požadavky na fiskální službu obsahovat informace o zákaznících, jako jsou jména a adresy, v případech, kdy je zákazník přidán k transakci.
- **Mapování sazeb daně z přidané hodnoty (DPH).** – Mapování procentních hodnot daně, které jsou nastaveny pro kódy daně z prodeje, na atribut **TaxG** (daňová skupina) v požadavcích zasílaných fiskální službě. Zde je výchozí mapování:

    ```
    A: 19.00; B: 7.00; C: 10.70; D: 5.50; E: 0.00
    ```

    První složka v každém páru představuje daňovou skupinu DPH, která je podporována službou fiskální registrace EFR. Druhá složka představuje odpovídající sazbu DPH. Další informace o skupinách DPH, které EFR podporuje pro Německo, viz [Reference k EFR](https://public.efsta.net/efr/).

- **Daňová skupina pro dárkové poukazy a vklady** – Hodnota atributu **TaxG** v požadavcích zasílaných fiskální službě na základě operací, které zahrnují dárkové poukazy nebo vklady. Zde je výchozí mapování:

    ```
    G
    ```

- **Daňová skupina pro osvobození od DPH** – Hodnota atributu **TaxG** v žádostech zasílaných fiskální službě na základě operací osvobozených od daňových povinností. Zde je výchozí mapování:

    ```
    F
    ```

> [!NOTE]
> Nastavení daní ve výchozím mapování dat jsou zodpovědná za párování nastavení daní v systému a daňových skupin ve službě EFR. Daňové skupiny lze tisknout na příjemky pouze v případě, že pole **Kód pro tisk** je nastaveno na stránce **Kódy DPH**.

#### <a name="fiscal-connector-settings"></a>Nastavení fiskálního konektoru

Následující nastavení jsou součástí konfigurace fiskálního konektoru, který je poskytován jako ukázka fiskální integrace:

- **Adresa koncového bodu** – adresa URL služby daňové registrace.
- **Časový limit** – doba v milisekundách, po kterou bude fiskální konektor čekat na odpověď ze služby fiskální registrace.
- **Zobrazit oznámení o fiskální registraci** – Tento příznak určuje, zda se mají operátorovi zobrazovat oznámení vrácená službou fiskální registrace.

### <a name="configure-channel-components"></a>Konfigurace komponent kanálu

> [!WARNING]
> Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači v LCS. Další informace viz [Pokyny k nasazení ukázkové fiskální integrace pro Německo (starší verze)](emea-deu-fi-sample-sdk.md).
>
> Podpora nového modelu nezávislého balení a rozšíření pro vzorky fiskální integrace je plánována pro pozdější verze.

#### <a name="set-up-the-development-environment"></a>Nastavení vývojového prostředí

Tento postup slouží k nastavení vývojového prostředí, abyste mohli testovat a rozšířit ukázku.

1. Naklonujte nebo stáhněte úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions). Vyberte správnou verzi větve vydání podle vaší verze SDK/aplikace. Další informace viz [Stažení ukázek Retail SDK a referenčních balíčků z GitHub a NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Otevřete řešení EFR v umístění **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln** a sestavte jej.
1. Instalace rozšíření Commerce Runtime:

    1. Vyhledejte instalační program rozšíření CRT:

        - **Commerce Scale Unit:** Ve složce **Efr\\ScaleUnit\\ScaleUnit.EFR.Installer\\bin\\Debug\\net461** vyhledejte instalační program **ScaleUnit.EFR.Installer**.
        - **Místní CRT v Modern POS:** Ve složce **Efr\\ModernPOS\\ModernPOS.EFR.Installer\\bin\\Debug\\net461** vyhledejte instalační program **ModernPOS.EFR.Installer**.

    1. Spusťte instalační program rozšíření CRT z příkazového řádku:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Místní CRT v Modern POS:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Instalace rozšíření hardwarové stanice:

    - Ve složce **Efr\\HardwareStation\\HardwareStation.EFR.Installer\\bin\\Debug\\net461** vyhledejte instalační program **HardwareStation.EFR.Installer**.
    - Spusťte instalační program rozšíření z příkazového řádku:

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Produkční prostředí

Postupujte podle kroků v části [Nastavení kanálu buildu pro ukázku fiskální integrace](fiscal-integration-sample-build-pipeline.md), kterými vygenerujete a uvolníte nasaditelné balíčky Cloud Scale Unit a samoobslužné nasaditelné balíčky pro ukázku fiskální integrace. Soubor YAML šablony **EFR build-pipeline.yml** se nachází ve složce **Pipeline\\YAML_Files** úložiště [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-extensions"></a>Návrh rozšíření

Ukázka integrace služby fiskální registrace pro Německo je založena na [funkci fiskální integrace](fiscal-integration-for-retail-channel.md) a je součástí řešení Retail SDK. Ukázka se nachází ve složce **src\\FiscalIntegration\\Efr** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (například [ukázka ve verzi/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Ukázka [se skládá](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) ze zprostředkovatele fiskálního dokumentu, což je rozšíření řešení CRT a fiskálního konektoru, který je rozšířením hardwarové stanice Commerce. Další informace o použití sady Retail SDK naleznete v části [Architektura Retail SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md) a [Nastavení kanálu sestavení pro sadu SDK nezávislého balení](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Kvůli omezením [nového modelu nezávislého balíčku a rozšíření](../dev-itpro/build-pipeline.md) jej v současné době nelze pro tuto ukázku fiskální integrace použít. Musíte použít předchozí verzi Retail SDK na vývojářském virtuálním počítači v LCS. Další informace viz [Pokyny k nasazení ukázkové fiskální integrace pro Německo (starší verze)](emea-deu-fi-sample-sdk.md). Podpora nového modelu nezávislého balení a rozšíření pro vzorky fiskální integrace je plánována pro pozdější verze.

### <a name="crt-extension-design"></a>Návrh rozšíření CRT

Účelem rozšíření je, ab poskytovatel daňového dokumentu generoval dokumenty specifické pro službu a zpracovával odpovědi z daňové registrační služby.

#### <a name="request-handler"></a>Obslužná rutina požadavku

Pro poskytovatele dokumentů existuje jedna obslužná rutina požadavků **DocumentProviderEFRFiscalDEU**. Tato obslužná rutina se používá ke generování fiskálních dokumentů pro službu fiskální registrace. Je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu zprostředkovatele zadanému v centrále Commerce.

Konektor podporuje následující požadavky:

- **GetFiscalDocumentDocumentProviderRequest** – tento požadavek obsahuje informace o dokladu, o němž by měl být vygenerován dokument. Vrátí dokument specifický pro službu, který má být registrován ve službě daňové registrace.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – Tento požadavek vrací odpověď spolu s rozšířenými daty.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor pro poskytovatele fiskálních dokumentů se nachází v umístění **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders\\DocumentProviderFiscalEFRSampleGermany.xml** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Tento soubor slouží k povolení konfigurace nastavení zprostředkovatele fiskálního dokumentu z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace.

### <a name="hardware-station-extension-design"></a>Design rozšíření hardwarové stanice

Účelem rozšíření je fiskální konektor určený ke komunikaci se službou daňové registrace.

Rozšíření hardwarové stanice je **HardwareStation.Extension.EFRSample**. Používá protokol HTTP k odesílání dokumentů, které rozšíření  CRT generuje pro daňovou registrační službu. Také zpracovává odpovědi, které jsou přijaty ze služby daňové registrace.

#### <a name="request-handler"></a>Obslužná rutina požadavku

Obslužná rutina požadavku **EFRHandler** je vstupní bod pro práci s požadavky služby daňové registrace. Tato rutina je zděděna z rozhraní **INamedRequestHandler**. Metoda **HandlerName** je odpovědná za vrácení názvu obslužné rutiny. Název obslužné rutiny by měl odpovídat názvu poskytovatele dokumentu fiskálního konektoru zadanému v centrále Commerce.

Konektor podporuje následující požadavky:

- **SubmitDocumentFiscalDeviceRequest** – tento požadavek odesílá dokumenty službě daňové registrace a z ní vrátí odpověď.
- **IsReadyFiscalDeviceRequest** – tento požadavek se používá pro kontrolu stavu služby daňové registrace.
- **InitializeFiscalDeviceRequest** – tento požadavek se používá pro inicializaci stavu služby daňové registrace.

#### <a name="configuration"></a>Konfigurace

Konfigurační soubor pro fiskální konektor se nachází v umístění **src\\FiscalIntegration\\Efr\\Configurations\\Connectors\\ConnectorEFRSample.xml** v úložišti [Řešení Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) repository. Tento soubor slouží k povolení nastavení pro fiskální konektor ke konfiguraci z centrály Commerce. Formát souboru je v souladu s požadavky na konfiguraci fiskální integrace.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
