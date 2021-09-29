---
title: Zapečetěné nabídky pro požadavky na nabídku
description: Toto téma popisuje, jak nastavit zapečetěné nabídky tak, aby byly odpovědi dodavatelů na nabídky utajeny, dokud nebudou odpečetěny pracovníky nákupu.
author: yanansong
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 02cbe9d6a6d157208d73ed756efae24df2a082de
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500627"
---
# <a name="sealed-bidding-for-rfqs"></a>Zapečetěné nabídky pro požadavky na nabídku

[!include [banner](../includes/banner.md)]

Zapečetěné nabídky uchovávají odpovědi dodavatelů na nabídky utajeny, dokud nebudou odpečetěny pracovníky nákupu. Všechny nabídky související s požadavkem na nabídku (RFQ) jsou nejprve k dispozici k odpečetění po skončení platnosti nabídky. Před odpečetěním nabídky k ní mají přístup pouze uživatelé, kteří mají vyhrazené uživatelské role a kteří zastupují dodavatele.

> [!IMPORTANT]
> Úpravy nebo rozšiřování formulářů nebo vytváření nových formulářů či obchodní logiky může narušit ochranu, kterou společnost Microsoft poskytuje pro zapečetěné nabídky. Nesete riziko vyplývající z použití jakýchkoli úprav, rozšíření, nových formulářů nebo obchodní logiky nebo nemožnosti používat funkci zapečetěného nabízení kvůli těmto úpravám, rozšířením, novým formulářům nebo obchodní logice.  Společnost Microsoft neodpovídá za žádné škody vyplývající z jakýchkoli úprav nebo rozšíření formulářů nebo jakýchkoli nových formulářů či obchodní logiky, které vytvoříte nebo jakákoli třetí strana vytvoří pro vás. Společnost Microsoft neposkytuje technickou ani jinou podporu pro jakékoli úpravy, rozšíření, nové formuláře nebo obchodní logiku vytvořené vámi nebo jakoukoli třetí stranou. Nesete výhradní odpovědnost za dodržování všech příslušných zákonů nebo předpisů týkajících se zapečetěných nabídek.

## <a name="how-bids-are-kept-secure"></a>Jak jsou nabídky bezpečně uchovávány

Zapečetěné nabídky používají asymetrické šifrování k zašifrování šifrovacího klíče nabídky (KEK) a symetrické šifrování k šifrování skutečné nabídky. Systém se integruje s trezorem Microsoft Azure Key Vault pro generování a správu šifrovacích klíčů, které se používají k šifrování zapečetěných nabídek. Každá nabídka má svůj vlastní šifrovací klíč. Toto šifrování je bezpečně uloženo v trezoru klíčů, který vlastní organizace provozující aplikaci Dynamics 365 Supply Chain Management. Systém přistupuje k trezoru klíčů na vyžádání, kdykoli je vyžadováno šifrování a dešifrování.

## <a name="setup-and-configuration"></a>Instalace a konfigurace

Tato část popisuje předpoklady, které musejí být splněny, než budete moci rozesílat požadavky na nabídky vyžadující zapečetěné nabídky.

### <a name="step-1-set-up-user-access-to-sealed-bidding"></a>Krok 1: Nastavte přístup uživatele k zapečetěným nabídkám

Když používáte zapečetěné nabídky, mohou zobrazovat, upravovat a odesílat nabídky pro tohoto dodavatele pouze uživatelé, kteří jsou nastaveni jako kontaktní osoba dodavatele, a to dokud neuplyne lhůta pro podávání nabídek. Tito uživatelé musejí mít roli **Dodavatel (externí)** a musejí být nastaveni jako kontaktní osoba pro účet dodavatele. Kontaktní osoba musí mít také povolení ke spolupráci dodavatele, jak je popsáno v tématu [Nastavení a správa dodavatelské spolupráce](set-up-maintain-vendor-collaboration.md).

Protože uživatelé, kteří mají příslušná oprávnění a jsou nastaveni jako kontaktní osoby dodavatele, mají přístup k uzavřeným nabídkám dodavatele, je důležité sledovat, kdo tito uživatelé jsou. Správce systému, který nastavuje uživatele a role zabezpečení, je zodpovědný za omezení přístupu k zapečetěným nabídkám na ty uživatele, kterým je skutečně povoleno je zobrazit.

### <a name="step-2-enable-the-sealed-bidding-feature"></a>Krok 2: Povolení funkce zapečetěného nabízení

Než začnete tuto funkci nastavovat nebo používat, musíte se ujistit, že je ve vašem systému k dispozici. Správci mohou použít pracovní prostor **[Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** ke kontrole stavu této funkce a jejímu zapnutí, je-li to potřeba. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Zásobování a zdroje*
- **Název funkce:** *Zapečetěné nabídky pro požadavky na nabídku*

### <a name="step-3-set-up-azure-key-vault"></a>Krok 3: Nastavení trezoru Azure Key Vault

Supply Chain Management používá šifrovací klíče k ochraně všech zapečetěných nabídek a jejich utajení až do příslušné doby. Využívá schopností trezoru klíčů generovat a udržovat požadované klíče. Chcete-li aktivovat tento systém, musíte proto nastavit připojení ze Supply Chain Management k trezoru klíčů.

> [!IMPORTANT]
> Trezor klíčů musí být vytvořen v předplatném Azure, které je ve vlastnictví vaší organizace (nikoli v předplatném, kde používáte Supply Chain Management).

Každá nabídka načte svůj vlastní tajný klíč. Tento klíč se používá pokaždé, když uživatel nabídku zobrazí, aktualizuje nebo ji odpečetí.

Trezor klíčů generuje klíč, který se používá k načtení tajného klíče, když dodavatel vybere položku **Nabídka** v rozhraní spolupráce dodavatele. Klíč poté vyprší po pevně stanovené době, kterou správce nákupu nastaví na stránce **Parametry modulu Zásobování a zdroje** v Supply Chain Management. Po vypršení platnosti klíče nebude nikdo moci nabídku zobrazit, upravit ani odpečetit. Proto je důležité konfigurovat vypršení platnosti klíče tak, aby byl dostatek času na dokončení nabídkového procesu.

V následujících třech krocích nastavíte připojení ke službě Key Vault. Nejprve nastavíte trezor klíčů, který budete používat pro zapečetěné nabídky. Dále nakonfigurujete v aplikaci Supply Chain Management komunikaci s trezorem klíčů. Nakonec nastavíte dobu vypršení platnosti klíče.

### <a name="step-4-set-up-a-key-vault-to-use-with-sealed-bidding"></a>Krok 4: Nastavení trezoru klíčů, který budete používat pro zapečetěné nabídky

Při nastavení trezoru klíčů postupujte následujícím způsobem. Pořadí kroků je velmi důležité.

1. Pokud jste ještě nenastavili předplatné Azure, které je oddělené od předplatného, kde používáte Supply Chain Management, nastavte jej.
1. Nastavte si trezor klíčů ve svém odděleném úložišti Azure. Další informace viz téma [Údržba úložiště Azure Key Vault](https://support.microsoft.com/help/4040294/maintaining-azure-key-vault-storage).
1. Nastavte si aplikaci Supply Chain Management tak, aby fungovala jako klient pro váš trezor klíčů. Další informace naleznete v tématu [Nastavení klienta Azure Key Vault](https://support.microsoft.com/help/4040305/setting-up-azure-key-vault-client).

### <a name="step-5-configure-key-vault-parameters-in-supply-chain-management"></a>Krok 5: Konfigurace parametrů služby Key Vault v Supply Chain Management

Chcete-li konfigurovat aplikaci Supply Chain Management tak, aby komunikovala s trezorem klíčů během zapečetěného nabízení cen, postupujte takto.

1. Přihlaste se do Supply Chain Management a přejděte do části **Správa systému \> Nastavení \> Parametry trezoru klíčů**.
1. Výběrem položky **Nový** vytvořte záznam a nastavte pro něj následující pole:

    - **Název** – Zadejte název.
    - **Popis** – Zadejte popis.
    - **Adresa URL trezoru klíčů** - Zadejte výchozí adresu URL pro trezor klíčů.
    - **Klient úložiště klíčů** – Zadejte ID interaktivního klienta aplikace Active Directory, která je přidružena k trezoru klíčů pro autentizaci.
    - **Tajný klíč trezoru klíčů** – Zadejte tajný klíč pro certifikát.
    - **Povoleno pro zapečetěné nabídky** – Tuto možnost nastavte na *Ano*.

![Stránka parametrů služby Key Vault](media/sealed-bidding-key-vault-param.png "Stránka parametrů služby Key Vault")

> [!NOTE]
> U zapečetěných nabídek můžete současně povolit pouze jednu konfiguraci trezoru klíčů. Než deaktivujete stávající konfiguraci trezoru klíčů, musíte se ujistit, že všechny zapečetěné nabídky, které ji používají, jsou odpečetěny. Zkontrolujte každý případ RFQ typu *Zapečetěno* a ujistěte se, že všechny jeho odpovědi jsou odpečetěny.

### <a name="step-6-set-the-key-expiration-time"></a>Krok 6: Nastavení doby vypršení platnosti klíče

Chcete-li nastavit čas vypršení platnosti, který se použije na klíč generovaný pro každou novou nabídku, postupujte takto.

1. Přejděte do nabídky **Parametry modulu Zásobování a zdroje \> Nastavení \> Parametry modulu Zásobování a zdroje**.
1. Na kartě **Požadavek na nabídku** v poli **Posun (dny)** zadejte počet dní, po které by mělo období požadavku trvat. Když se vytvoří požadavek na nabídku, počet dní, které zde zadáte, se přičte k systémovému datu, aby se definovalo výchozí datum vypršení platnosti požadavku.
1. V poli **Posun ve dnech vypršení platnosti šifrovacího klíče** zadejte počet dní, po které by měl být každý šifrovací klíč po vydání platný. Po vypršení platnosti klíče nebude nikdo moci zobrazit, upravit ani odpečetit zapečetěnou nabídku, která klíč používá.

> [!TIP]
> Hodnota **Posun ve dnech vypršení platnosti šifrovacího klíče** by neměla být menší než hodnota **Posun (dny)**.

### <a name="step-7-set-the-default-bid-type"></a><a name="set-default-bid-type"></a>Krok 7: Nastavení výchozího typu nabídky

Každý případ RFQ má typ nabídky. Typ nabídky definuje, zda daný případ RFQ poskytuje otevřené nebo uzavřené nabídky.

#### <a name="rfq-cases-that-dont-have-a-solicitation-type"></a>Případy RFQ, které nemají typ oslovení

Chcete-li nastavit výchozí typ nabídky, který je přiřazen novým případům RFQ, kterým není při vytváření přiřazen typ oslovení, postupujte takto.

1. Přejděte do nabídky **Parametry modulu Zásobování a zdroje \> Nastavení \> Parametry modulu Zásobování a zdroje**.
1. Na kartě **Požadavek na nabídku** nastavte pole **Typ nabídky** na *Zapečetěná*.

#### <a name="rfq-cases-that-have-a-solicitation-type"></a>Případy RFQ, které mají typ oslovení

Chcete-li nastavit výchozí typ nabídky, který je přiřazen novým případům RFQ, kterým je při vytváření přiřazen typ oslovení, postupujte takto.

1. Přejděte na **Zásobování a zdroje \> Nastavení \> Požadavek na nabídku \> Typ oslovení**.
1. Vytvořte nový typ oslovení nebo vyberte existující typ oslovení, u kterého chcete použít typ nabídky *Zapečetěná*.
1. Nastavte pole **Typ nabídky** na hodnotu *Zapečetěná*.
1. Opakujte tyto kroky pro každý další typ oslovení, u kterého chcete implementovat zapečetěné nabídky.

> [!TIP]
> Typ oslovení nemusí být přiřazen při vytváření nového požadavku na nabídku. Pokud je přiřazen typ oslovení, může jej výchozí typ nabídky RFQ načíst. V opačném případě lze použít výchozí typ oslovení, který je definován v parametrech modulu Zásobování a zdroje.

## <a name="the-sealed-bidding-process"></a>Proces zapečetěných nabídek

Zapečetěné nabídky jsou zpracovány téměř stejným způsobem, jaký je popsán v [Přehledu požadavků na nabídku (RFQ)](request-quotations.md). Hlavním rozdílem je to, že data nabídek a jejich přílohy jsou šifrovány, dokud není nabídka odpečetěna.

> [!IMPORTANT]
> [Dotazníky](/dynamicsax-2012/appuser-itpro/view-and-respond-to-questionnaires) nejsou šifrovány a neměly by být používány ke shromažďování citlivých informací

Shrnutí celého procesu vypadá takto:

1. Vytvoříte a odešlete požadavek na nabídku jednomu nebo více dodavatelům.
1. Prodejci reagují odesláním zapečetěné nabídky.
1. Po uplynutí doby platnosti zadávání nabídek odpečetíte nabídky.
1. Nabídky se stanou viditelnými a vy je můžete vyhodnotit a porovnat.
1. Po přijetí nabídky vygenerujete nákupní objednávku, vygenerujete kupní smlouvu nebo aktualizujete nákupní požadavek.

### <a name="create-an-rfq-case-that-uses-sealed-bidding"></a>Vytvoření případu RFQ, který používá zapečetěné nabídky

Proces vytváření případu RFQ se zapečetěnými nabídkami je téměř stejný jako proces pro nepečetěné nabídky. Informace o tom, jak vytvořit oba typy případů RFQ, najdete v tématu [Vytvoření požadavku na nabídku](tasks/create-request-quotation.md). Tato část zdůrazňuje několik důležitých aspektů při vytváření RFQ pro zapečetěné nabídky.

Případy RFQ pro zapečetěné nabídky musejí mít **Typ nabídky** nastaven na *Zapečetěná*. Existují tři způsoby, jak přiřadit tuto hodnotu případu RFQ:

- Poté, co vytvoříte případ RFQ, nastavte hodnotu přímo v něm.
- Definujte zapečetěné nabízení jako výchozí typ nabídky pro všechny případy RFQ v parametrech modulu Zásobování a zdroje. (Viz část [Nastavení výchozího typu nabídky](#set-default-bid-type) dříve v tomto tématu.)
- Když vytváříte nový případ RFQ, vyberte typ oslovení, který je nastaven pro zapečetěné nabídky. (Viz část [Nastavení výchozího typu nabídky](#set-default-bid-type).)

U zapečetěných nabídek určuje hodnota **Datum a čas vypršení platnosti** případu RFQ, kdy lze podané nabídky odpečetit. Hodnota **Datum a čas vypršení platnosti** na každém řádku bude odpovídat hodnotě v záhlaví.

Po odeslání případu RFQ nemůžete typ nabídky změnit.

### <a name="vendors-respond-to-an-rfq"></a>Reakce dodavatelů na požadavek

Dodavatelé, kteří odpovídají na zapečetěnou nabídku, používají stejný postup, jaký používají u otevřených nabídek, jak je uvedeno v tématu [Práce s požadavky na nabídku v pracovním prostoru Nabídky dodavatele](vendor-collaboration-work-customers-dynamics-365-operations.md#working-with-rfqs-in-the-vendor-bidding-workspace). Podrobné pokyny o tom, jak pracovat s otevřenými i zapečetěnými nabídkami, najdete v tématu [Zadání a porovnání nabídek pro požadavek na nabídku a přidělení smlouvy](tasks/enter-compare-rfq-bids-award-contracts.md). Jediným rozdílem mezi zpracováním zapečetěných nabídek a otevřených nabídek je to, že až do vypršení lhůty pro podávání nabídek odborníci na nákup nemohou otevřít zapečetěnou nabídku dodavatele. Zapečetěnou nabídku dodavatele může otevřít pouze jeho kontaktní osoba.

> [!IMPORTANT]
> U zapečetěných nabídek mohou dodavatelé nahrávat přílohy pouze ve formátu PDF. Jiné formáty nebudou akceptovány.

Poté, co registrovaný uživatel dodavatele vybere příkaz **Nabídka** na případu RFQ se zapečetěnou nabídkou, může zadat údaje o svých nabídkách a tato data budou uchována v bezpečí. Dodavatelé mohou svou práci během přípravy nabídky ukládat, vracet se k ní tak často, jak potřebují, a poté ji odeslat, až bude připravena. Dodavatelé si také mohou svou nabídku zobrazit poté, co ji odešlou. Pokud musí dodavatelé svou nabídku změnit poté, co ji odešlou, mohou ji odvolat, aktualizovat a znovu odeslat kdykoli až do uplynutí nabídkového období.

Během zapečetěného nabízení platí následující podmínky:

- Během zapečetěného nabízení systém vytvoří deník *Požadavek na nabídku*.
- Když dodavatel podá nabídku, vytvoří se deníky RFQ bez řádků, které mají zapečetěnou cenu.
- Po odpečetění případu se vytvoří deníky RFQ s cenou a částkou. Do tohoto deníku se dostanete výběrem příkazu **Deníky požadavků na nabídku** na stránce **Všechny požadavky na nabídku**.
- Systém ukládá protokol každé akce, kterou uživatelé provedou se zapečetěnou nabídkou. Mezi tyto akce patří zobrazení, úpravy a uložení nabídky. Tento protokol je viditelný jak pro dodavatele, tak pro odborníky na nákup, kteří mají k nabídce přístup.
- Jak nabídka postupuje, odborníci v oblasti nákupu si mohou zobrazit její stav. Stav se pak změní na *Odběratel aktualizuje* nebo *Odesláno odběratelem*.
- Stav řádků v zapečetěné nabídce zůstává *Odesláno* dokud není nabídka uzavřena.
- Pokud se dodavatel rozhodne nabídku odmítnout, bude mít **Průběh odpovědi** nabídky hodnotu *Zamítnuto odběratelem*. Tento stav bude viditelný pro zaměstnance nákupu.
- Odpovědi v dotaznících **ne** jsou uloženy v šifrované podobě v databázi. Proto nejsou zapečetěné. V uživatelském rozhraní RFQ však nebudou viditelné, dokud není případ odpečetěn.

### <a name="all-sealed-bid-activities-are-logged"></a>Všechny aktivity zapečetěných nabídek jsou zaznamenány

Podrobný protokol zaznamenává všechny uživatelské aktivity a akce pro nabídku. Protokol aktivit umožňuje organizacím určit, kdo aktualizoval nabídku během její životnosti a o jaké aktualizace šlo. Umožňuje také organizacím potvrdit, že k zapečetěné nabídce přistupovali pouze autorizovaní lidé. Protokol aktivit je k dispozici u každé nabídky na stránce **Aktivita**.

### <a name="review-rfq-activity"></a>Kontrola aktivity RFQ

Každá interakce s nabídkou je zaznamenána a lze ji zobrazit na stránce **Aktivita**. Následující obrázek znázorňuje příklad.

![Příklad stránky Aktivita](media/sealed-bidding-rfq-activity.png "Příklad stránky Aktivita")

Dodavatelé získají přístup ke stránce **Aktivita** výběrem položky **Aktivita** na stránce **Požadavek na nabídku – Zapečetěná nabídka**. Zaměstnanci nákupu k ní mají přístup výběrem položky **Aktivita** na stránce **Požadavek na nabídku**. Protokol aktivit poskytuje plnou viditelnost dodavatelům a zaměstnancům nákupu, kteří otevřeli nabídku. Proto může odhalit jakýkoli neoprávněný přístup.

### <a name="unseal-sealed-bids"></a>Odpečetění zapečetěných nabídek

Když uplyne hodnota **Datum a čas vypršení platnosti**, která byla konfigurována pro případ RFQ se zapečetěným nabízením, bude k dispozici tlačítko **Odpečetit** . Výběrem tlačítka **Odpečetit** odemknete všechny nabídky pro vybraný případ RFQ. Všechna data nabídek a přílohy se poté stanou viditelnými, aby bylo možné spravovat odpovědi na případ. Kromě toho se vytvoří deníky, které obsahují data odeslaných nabídek.

Událost odpečetění je zaznamenána a lze ji zobrazit na stránce **Aktivita**.

### <a name="process-accepted-bids"></a>Zpracování přijatých nabídek

Proces porovnávání a schvalování dříve zapečetěných nabídek je stejný jako u otevřených nabídek. Informace o tom, jak hodnotit, porovnávat, odmítat a přijímat nezapečetěné nabídky, najdete v tématu [Zadání a porovnání nabídek pro požadavek na nabídku a přidělení smlouvy](tasks/enter-compare-rfq-bids-award-contracts.md).

## <a name="the-rfq-activity-log-can-never-be-deleted"></a>Protokol aktivit RFQ nelze nikdy odstranit

Nikdo, dokonce ani správci a podpora společnosti Microsoft, nemůže upravovat nebo mazat protokol aktivit RFQ. Toto omezení pomáhá zajistit spravedlnost zapečetěného nabídkového řízení. Pomáhá také zajistit, aby byl udržován přesný záznam pro audit.
