---
title: Typ cílového umístění elektronického výkaznictví e-mailu
description: Toto téma vysvětluje, jak nakonfigurovat cíl e-mailu pro každou SLOŽKU nebo SOUBOR ve formátu elektronického výkaznictví (ER).
author: NickSelin
ms.date: 12/03/2020
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
ms.openlocfilehash: f2d8d441ad742252f3be7dc207544387f5224c37
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347989"
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

## <a name="configure-an-email-destination"></a>Konfigurace e-mailového cíle

Chcete-li odeslat výstupní soubor nebo několik výstupních souborů e-mailem, vyberte na stránce **Místo určení elektronického výkaznictví** na rychlé záložce **Cíl souboru** komponentu nebo skupinu komponent v mřížce, a poté vyberte **Nastavení**. V zobrazeném dialogovém okně **Nastavení cíle** na kartě **E-mail** nastavte možnost **Povoleno** možnost na **Ano**. Poté můžete zadat příjemce e-mailů a upravit předmět a tělo e-mailové zprávy. Můžete nastavit buď konstantní text pro předmět a tělo e-mailu, nebo můžete použít [vzorce](er-formula-language.md) elektronického výkaznictví k dynamickému vytvoření textů e-mailů.

E-mailové adresy pro ER lze konfigurovat dvěma způsoby. Konfiguraci lze dokončit stejným způsobem, jakým ji dokončí funkce správy tisku, nebo můžete e-mailovou adresu vyřešit přímým odkazem na konfiguraci elektronického výkaznictví pomocí vzorce.

[![Nastavení možnosti Povoleno na Ano pro e-mailový cíl.](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>Typy e-mailových adres

Pokud vyberete možnost **Upravit** vedle pole **Komu** nebo **Kopie** v dialogovém okně **Nastavení cíle**, zobrazí se dialogové okno **E-mail – komu**. Vyberte možnost **Přidat** a poté zvolte typ e-mailové adresy, který použijete. Aktuálně jsou podporovány dva typy: **Správa tisku – e-mail** a **Konfigurační e-mail**.

[![Výběr typu e-mailové adresy.](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management-email"></a>Správa tisku – e-mail

Pokud vyberete jako typ e-mailové adresy možnost **Správa tisku – e-mail**, můžete zadat pevné e-mailové adresy v dialogovém okně **E-mail – komu** nastavením následujících polí:

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

Vyberte **Konfigurační e-mail** jako typ e-mailové adresy, pokud má vámi používaná konfigurace uzel ve zdrojích dat, který vrací buď jednu e-mailovou adresu, nebo více e-mailových adres oddělených středníkem (;). V návrháři vzorců můžete použít [zdroje dat](general-electronic-reporting.md#FormatComponentOutbound) a [funkce](er-formula-language.md#functions), abyste získali správně naformátovanou e-mailovou adresu nebo správně naformátované e-mailové adresy, které jsou odděleny středníky. Například pokud používáte konfiguraci **Platební převod ISO 20022**, měl by se uzel představující primární e-mailovou adresu dodavatele z kontaktních údajů dodavatele, na který by měl být zaslán průvodní dopis, jmenovat `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

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