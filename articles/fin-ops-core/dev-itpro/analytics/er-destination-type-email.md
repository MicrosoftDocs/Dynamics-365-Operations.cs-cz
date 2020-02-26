---
title: Typ cílového umístění elektronického výkaznictví e-mailu
description: Toto téma obsahuje informace o tom, jak konfigurovat cíl e-mailu pro každou komponentu SLOŽKA nebo SOUBOR formátu elektronického výkaznictví, který je nakonfigurován pro generování odchozích dokumentů.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019666"
---
# <a name="EmailDestinationType">E-mailový cíl</a>

[!include [banner](../includes/banner.md)]

Můžete konfigurovat cíl e-mailu pro každou komponentu SLOŽKA nebo SOUBOR formátu elektronického výkaznictví, který je nakonfigurován pro generování odchozích dokumentů. Vygenerovaný dokument je na základě nastavení cíle dodán jako příloha elektronické pošty.

Nastavením možnosti **Povoleno** na **Ano** odešlete výstupní soubor prostřednictvím e-mailu. Po povolení této možnosti můžete zadat příjemce e-mailů a upravit předmět a tělo e-mailové zprávy. Můžete nastavit konstantní texty pro předmět a tělo e-mailu nebo můžete použít [vzorce](er-formula-language.md) elektronického výkaznictví k dynamickému vytvoření textů e-mailů. 

E-mailové adresy pro ER lze konfigurovat dvěma způsoby. Konfiguraci lze dokončit stejným způsobem, jakým ji dokončí funkce správy tisku, nebo můžete e-mailovou adresu vyřešit přímým odkazem na konfiguraci elektronického výkaznictví pomocí vzorce.

[![Povolení cílového místa e-mailu](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>Typy e-mailových adres

Po zvolení **Upravit** v polích **Komu** nebo **Kopie** se zobrazí dialogové okno **E-mail – komu**. Můžete zvolit typ e-mailové adresy, který použijete. Typy e-mailů konfigurace **Konfigurační e-mail** a **Správa tisku** jsou aktuálně podporovány.

[![Volba typu e-mailu](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management"></a>Správa tisku

Vyberete-li typ e-mailu **Správa tisku**, můžete zadat pevné e-mailové adresy do pole **Komu**. 

[![Konfigurace pevných e-mailových adres](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)

Pro použití jiných než pevných e-mailových adres je nutné vybrat typ zdroje e-mailu pro cíl souboru. Podporovány jsou následující hodnoty: **Odběratel**, **Dodavatel**, **Potenciální zákazník**, **Kontakt**, **Konkurent**, **Pracovník**, **Uchazeč**, **Potenciální dodavatel** a **Zakázaný dodavatel**. Po výběru typu zdroje e-mailu použijte tlačítko vedle pole **E-mail – zdrojový účet** a otevřete formulář **Návrhář receptur**. Pomocí tohoto formuláře můžete připojit vzorec, který se vrací za běhu **účet strany** vybraného typu zdroje ze zpracovaného dokumentu do cíle e-mailu.

[![Konfigurace účtu zdroje e-mailu](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)

Vzorce jsou specifické pro konfiguraci elektronického výkaznictví. V poli **Vzorec** zadejte odkaz specifický pro dokument pro stranu typu Odběratel nebo Dodavatel. Namísto zadávání můžete najít uzel zdroje dat, který reprezentuje účet odběratele nebo dodavatele, a volbou možnosti **Přidat zdroj dat** aktualizovat vzorec. Příklad: Pokud používáte konfiguraci **platební převod ISO 20022**, uzel představující účet dodavatele má tvar `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

Zadáte-li hodnotu řetězce, například `"DE-001"`, a uložíte vzorec, bude kontaktní osobě dodavatele zaslán e-mail, **DE-001**.


[![Stránka návrháře vzorců elektronického výkaznictví](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)

[![Konfigurace účtu zdroje e-mailu](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)



### <a name="configuration-email"></a>Konfigurační e-mail

Použijte tento typ e-mailu, pokud má použitá konfigurace uzel ve zdrojích dat, které vrací **e-mailovou adresu**. Zdroje dat a funkce můžete použít v návrháři receptur, abyste získali správně naformátovanou e-mailovou adresu. Příklad: Pokud používáte konfiguraci **platební převod ISO 20022**, uzel představující e-mailovou adresu kontaktní osoby dodavatele má tvar `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![Konfigurace zdroje e-mailové adresy](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="additional-resources"></a>Další zdroje

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [Místa určení elektronického výkaznictví](electronic-reporting-destinations.md)
- [Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)
