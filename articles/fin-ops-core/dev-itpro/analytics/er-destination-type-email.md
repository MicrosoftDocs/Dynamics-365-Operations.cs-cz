---
title: Typ cílového umístění elektronického výkaznictví e-mailu
description: Toto téma vysvětluje, jak nakonfigurovat cíl e-mailu pro každou SLOŽKU nebo SOUBOR ve formátu elektronického výkaznictví (ER).
author: NickSelin
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2248b8a35b076eb778a50bbbc67d083380ceee62
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2022
ms.locfileid: "8324001"
---
# <a name="email-er-destination-type"></a>Typ cílového umístění elektronického výkaznictví e-mailu

[!include [banner](../includes/banner.md)]

Když je spuštěn formát elektronického výkaznictví (ER), lze vygenerovat jeden nebo více odchozích dokumentů. Komponenty formátu **Složka** nebo **Soubor** se ve formátech ER používají k určení struktury odchozích dokumentů. U těchto typů komponent můžete konfigurovat e-mailový cíl, kam budou odesílány odchozí dokumenty jako přílohy e-mailů.

Pro každou komponentu formátu ER **Složka** nebo **Soubor** můžete konfigurovat e-mailový cíl. V tomto případě **je každý odchozí dokument e-mailem odeslán zvlášť**. Vygenerovaný dokument je na základě tohoto nastavení cíle doručen jako příloha e-mailové zprávy. 

> [!NOTE]
> Pokud není generován žádný dokument, protože výraz **Povoleno** pro relevantní komponentu **Soubor** byl konfigurován tak, aby vrátila logickou hodnotu **Nepravda**, neposílá se žádný e-mail, i když je pro komponentu konfigurován a povolen e-mailový cíl.

Můžete také [seskupit](#grouping) několik komponent typu **Složka** nebo **Soubor** dohromady a poté konfigurovat e-mailový cíl pro všechny komponenty ve skupině. V tomto případě jsou všechny odchozí dokumenty, které jsou generovány komponentami patřícími do skupiny **, odesílány jako více příloh jednoho e-mailu**. Každý generovaný dokument je na základě tohoto nastavení cíle doručen jako příloha jedné e-mailové zprávy.

> [!NOTE]
> Pokud je alespoň jeden dokument generován komponentou **Soubor** ve skupině komponent, je odeslán e-mail. Pokud není seskupenými komponentami generován žádný dokument, protože výraz **Povoleno** pro každou komponentu **Soubor** byl konfigurován tak, aby vrátila logickou hodnotu **Nepravda**, neposílá se žádný e-mail, i když je pro tuto skupinu komponent konfigurován a povolen e-mailový cíl.
>
> **E-mail** je jediný cíl, který lze konfigurovat pro skupinu komponent. Chcete-li doručit dokument, který je odeslán e-mailem na základě nastavení e-mailového cíle pro skupinu, přidejte další cílový záznam, vyberte požadovanou komponentu a poté konfigurujte další cíl pro tento záznam.

Pro jednu konfiguraci formátu ER lze konfigurovat více skupin komponent. Tímto způsobem můžete konfigurovat e-mailový cíl pro každou skupinu komponent a e-mailový cíl pro každou komponentu.

## <a name="enable-an-email-destination"></a>Povolení cílového místa e-mailu

Chcete -li odeslat jeden nebo více výstupních souborů e -mailem, postupujte takto.

1. Na stránce **Místo určení elektronického výkaznictví** na pevné záložce **Cíl souboru** vyberte komponent nebo skupinu komponentů v mřížce.
2. Vyberte **Nastavení** a pak v dialogovém okně **Nastavení cíle** na kartě **E-mail** nastavte možnost **Povoleno** možnost na **Ano**.

[![Nastavení možnosti Povoleno na Ano pro e-mailový cíl.](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="configure-an-email-destination"></a>Konfigurace e-mailového cíle

### <a name="email-content"></a>Obsah e-mailu

Předmět a text e-mailové zprávy můžete upravit.

Do pole **Předmět** zadejte text předmětu e-mailu, který by se měl objevit v poli předmětu elektronické zprávy generované za běhu. Do pole **Text** zadejte text e-mailu, který by se měl objevit v poli text elektronické zprávy generované za běhu. Můžete nastavit konstantní text pro předmět a tělo e-mailu nebo můžete použít [vzorce](er-formula-language.md) elektronického výkaznictví k dynamickému vytvoření textů e-mailů za běhu. Konfigurovaný vzorec musí vrátit hodnotu typu [Řetězec](er-formula-supported-data-types-primitive.md#string).

Text vašeho e-mailu je složeno ve formátu TEXT nebo HTML v závislosti na e-mailovém klientovi. Můžete použít libovolné rozvržení, styl a značky, které HTML a vložené šablony stylů CSS umožňují.

> [!NOTE]
> E-mailoví klienti mají omezení rozložení a stylu, která mohou vyžadovat úpravy HTML a CSS stylů, které používáte pro tělo zprávy. Doporučujeme vám seznámit se s osvědčenými postupy vytváření HTML, které budou podporovat nejoblíbenější e-mailoví klienti.
>
> Použijte správné kódování k implementaci návratu na začátek řádku v závislosti na formátování těla. Další informace najdete v definici datového typu [Řetězec](er-formula-supported-data-types-primitive.md#string).

### <a name="email-addresses"></a>E-mailové adresy

Můžete zadat odesílatele e-mailu a příjemce e-mailu. Ve výchozím nastavení je e-mail odeslán jménem aktuálního uživatele. Chcete-li zadat jiného odesílatele e -mailu, musíte nakonfigurovat pole **Odesílatel**.

> [!NOTE]
> Když je nakonfigurován cíl e-mailu, pole **Odesílatel** je viditelné pouze uživatelům, kteří mají bezpečnostní oprávnění `ERFormatDestinationSenderEmailConfigure` **Nakonfigurujte e-mailovou adresu odesílatele pro cíle formátu ER**.
>
> Když je cíl e-mailu nabídnut k úpravám za [běhu](electronic-reporting-destinations.md#security-considerations), pole **Odesílatel** je viditelné pouze uživatelům, kteří mají bezpečnostní oprávnění  `ERFormatDestinationSenderEmailMaintain` **Nakonfigurujte e-mailovou adresu odesílatele pro cíl formátu ER**.
>
> Když je pole **Odesílatel** nakonfigurováno tak, aby používalo jinou e-mailovou adresu, než je adresa aktuálního uživatele, musí být oprávnění **Odeslat jako** nebo **Odeslat jménem** správně [nastaveno](/microsoft-365/solutions/allow-members-to-send-as-or-send-on-behalf-of-group) dopředu. Jinak je za běhu vyvolána následující výjimka: „Nelze odeslat e-mail jako \<from email account\> z účtu \<current user account\>, zkontrolujte prosím oprávnění „Odeslat jako“ na \<from email account\>."

Můžete nakonfigurovat pole **Odesílatel** pro vrácení více než jedné e-mailové adresy. V tomto případě se jako adresa odesílatele e-mailu použije první adresa v seznamu.

Chcete-li určit příjemce e-mailu, musíte nakonfigurovat pole **Příjemce** a **Kopie** (nepovinné).

E-mailové adresy pro ER lze konfigurovat dvěma způsoby. Konfiguraci lze dokončit stejným způsobem jako funkce správy tisku, nebo můžete e-mailovou adresu vyřešit přímým odkazem na konfiguraci elektronického výkaznictví pomocí vzorce.

## <a name="email-address-types"></a>Typy e-mailových adres

Pokud vyberete možnost **Upravit** vedle pole **Odesílatel**, **Příjemce** nebo **Kopie** v dialogovém okně **Nastavení cíle**, zobrazí se příslušné dialogové okno **Odesílatel e-mailu**, **Příjemce e-mailu** nebo **Kopie e-mailu**. Zde můžete nakonfigurovat odesílatele e-mailu a příjemce e-mailu. Vyberte možnost **Přidat** a poté zvolte typ e-mailové adresy, který použijete. Aktuálně jsou podporovány dva typy: **Správa tisku – e-mail** a **Konfigurační e-mail**.

[![Výběr typu e-mailové adresy.](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management-email"></a>Správa tisku – e-mail

Pokud vyberete jako typ e-mailové adresy možnost **Správa tisku – e-mail**, můžete zadat pevné e-mailové adresy v dialogovém okně **Odesílatel e-mailu**, **Příjemce e-mailu** nebo **Kopie e-mailu** nastavením následujících polí:

- V poli **Zdroj e-mailu** vyberte možnost **Žádný**.
- V poli **Další e-mailové adresy oddělené znakem „;“** zadejte pevné e-mailové adresy.

Alternativně můžete e-mailové adresy získat z kontaktních údajů strany, pro kterou generujete odchozí dokument. Pro použití jiných než pevných e-mailových adres je nutné vybrat v poli **Zdroj e-mailu** [roli](../../fin-ops/organization-administration/overview-global-address-book.md#party-roles) strany pro cíl souboru. Podporovány jsou následující role:

- Odběratel
- Dodavatel
- Potenciální zákazník
- Kontakt
- Konkurent
- Pracovní podproces
- Uchazeč
- Potenciální dodavatel
- Zakázaný dodavatel
- Právnická osoba

Chcete-li například konfigurovat e-mailový cíl pro formát ER, který se používá ke zpracování plateb dodavatele, vyberte roli **Dodavatel**.

Po výběru požadované role vyberte tlačítko **Vazba** (symbol řetězu) vedle pole **E-mailový zdrojový účet** a otevřete tak stránku [Návrhář vzorců](general-electronic-reporting-formula-designer.md). Na této stránce pak můžete konfigurovat vzorec, který za běhu vrátí číslo účtu strany, která je přiřazena konfigurované roli ze zpracovaného dokumentu do e-mailového cíle.

> [!NOTE]
> Vzorce jsou specifické pro konfiguraci elektronického výkaznictví.

Na stránce **Návrhář vzorců** zadejte v poli **Vzorec** odkaz na podporovanou roli pro konkrétní dokument. Namísto psaní odkazu v podokně **Zdroj dat** vyhledejte a vyberte uzel zdroje dat, který představuje účet nakonfigurované role, a poté výběrem položky **Přidat zdroj dat** aktualizujte vzorec. Například pokud konfigurujete e-mailový cíl pro konfiguraci **Platební převod ISO 20022**, která se používá ke zpracování plateb dodavatele, je uzlem představujícím účet dodavatele uzel `'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

![Konfigurace účtu zdroje e-mailu.](./media/er_destinations-emaildefineaddresssource.gif)

Pokud jsou čísla účtů konfigurované role jedinečná pro celou instanci Microsoftu Dynamics 365 Finance, může pole **Společnost zdroje e-mailu** v dialogovém okně **E-mail – komu** zůstat prázdné.

Případně může dojít k situaci, kdy různé strany v [Globálním adresáři](../../fin-ops/organization-administration/overview-global-address-book.md) byly registrovány v různých společnostech ([právnických osobách](../../fin-ops/organization-administration/organizations-organizational-hierarchies.md#legal-entities)) takovým způsobem, že všichni používají stejné číslo účtu k vyplnění konfigurované role. V tomto případě nejsou čísla účtů pro konfigurovanou roli jedinečná pro celou instanci Finance. Chcete-li tedy explicitně vybrat stranu, nemůžete zadat pouze číslo účtu. Musíte také zadat společnost, ve které byla strana zaregistrována, abyste mohli naplnit konfigurovanou roli. Vyberte tlačítko **Vazba** (symbol řetězu) vedle pole **Společnost zdroje e-mailu** v dialogovém okně **E-mail – komu** a otevřete tak stránku [Návrhář vzorců](general-electronic-reporting-formula-designer.md). Na této stránce pak můžete konfigurovat vzorec, který za běhu vrátí kód společnosti, jejíž požadovaný zdroj musí být nalezen v rozsahu.

> [!TIP]
> Pokud musíte ke spuštění formátu ER použít kód společnosti, ale formát ER neposkytuje žádný zdroj dat, ze kterého lze kód společnosti získat, konfigurujte vzorec `GetCurrentCompany()` pomocí integrované funkce ER s názvem [GETCURRENTCOMPANY](er-functions-other-getcurrentcompany.md).

> [!NOTE]
> Vzorce jsou specifické pro konfiguraci elektronického výkaznictví.

Chcete-li určit typ e-mailových adres, které musí být použity za běhu, vyberte v dialogovém okně **E-mail – komu** příkaz **Upravit** vedle pole **Komu** a otevřete tak rozevírací dialogové okno **Přiřadit e-mailovou adresu**. Poté nastavte následující pole:

- V poli **Účel** vyberte účely potřeby. Budou použity pouze e-mailové adresy vybraných účelů z kontaktů nalezené strany.
- Nastavte možnost **Primární kontakt** na **Ano**, když chcete použít jako primární e-mailovou adresu tu adresu, která je konfigurována pro zjištěnou stranu.

> [!NOTE]
> Pokud jsou v poli **Účel** vybrány účely a současně je možnost **Primární kontakt** nastavena na **Ano**, bude za běhu použit každá e-mailová adresa, která splňuje alespoň jedno konfigurované kritérium.

### <a name="configuration-email"></a>Konfigurační e-mail

Vyberte **Konfigurační e-mail** jako typ e-mailové adresy, pokud má vámi používaná konfigurace uzel ve zdrojích dat, který vrací buď jednu e-mailovou adresu, nebo více e-mailových adres oddělených středníkem (;). V návrháři vzorců můžete použít zdroje dat a [funkce](er-formula-language.md#Functions), abyste získali správně naformátovanou e-mailovou adresu nebo správně naformátované e-mailové adresy, které jsou odděleny středníky. Například pokud používáte konfiguraci **Platební převod ISO 20022**, měl by se uzel představující primární e-mailovou adresu dodavatele z kontaktních údajů dodavatele, na který by měl být zaslán průvodní dopis, jmenovat `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![Konfigurace zdroje e-mailové adresy.](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="group-format-components"></a><a id="grouping"></a>Seskupení komponent formátu

Chcete-li seskupit komponenty formátu, vyberte na stránce **Místo určení elektronického výkaznictví** v rychlé záložce **Cíl souboru** komponenty v mřížce a poté vyberte možnost **Skupina**.

**E-mail** je jediný dříve konfigurovaný cíl, který je pro vybrané komponenty stále k dispozici. Nejsou k dispozici žádné další dříve nakonfigurované cíle, protože u skupiny komponent jsou považovány za nepodporované. O těchto změnách budete podle potřeby informováni.

Záznam, který jste dříve přidali, se považuje za záhlaví vytvořené skupiny. Tento záznam záhlaví obsahuje nastavení e-mailového cíle pro skupinu. Dalšími záznamy jsou členové skupiny, kteří budou používat nastavení e-mailového cíle ze záznamu záhlaví skupiny.

Chcete-li zrušit seskupení komponent formátu, vyberte na rychlé záložce **Cíl souboru** záznam patřící do skupiny, a poté vyberte možnost **Zrušit seskupení**.

- Pokud vyberete záznam záhlaví, bude zrušeno seskupení celé skupiny.
- Pokud vyberete záznam člena a bude to záznam posledního člena ve skupině, bude zrušeno seskupení celé skupiny.
- Pokud vyberete záznam člena, který není záznamem posledního člena ve skupině, bude tento záznam vyloučen z aktuální skupiny.

Následující obrázek ukazuje strukturu formátu ER, který byl konfigurován tak, aby vytvářel odchozí komprimovaný soubor, který obsahuje upomínku a příslušné faktury odběratele ve formátu PDF.

[![Struktura formátu ER, který generuje odchozí dokumenty.](./media/ER_Destinations-Email-Grouping1.png)](./media/ER_Destinations-Email-Grouping1.png)

Následující obrázek ukazuje proces seskupování jednotlivých komponent, popsaný v tomto tématu, a povolení cíle typu **E-mail** pro novou skupinu, aby byl dopis s upomínkou odeslán společně s příslušnými fakturami odběratelem, které jsou ke zprávě přiloženy.

[![Seskupení jednotlivých komponent a povolení e-mailového cíle.](./media/ER_Destinations-Email-Grouping2.gif)](./media/ER_Destinations-Email-Grouping2.gif)

## <a name="additional-resources"></a>Další prostředky

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Místa určení elektronického výkaznictví](electronic-reporting-destinations.md)
- [Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
