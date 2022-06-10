---
title: Nastavte pokročilý import bankovního odsouhlasení pomocí elektronického výkaznictví
description: Toto téma vysvětluje, jak používat elektronické hlášení k nastavení pokročilého procesu importu bankovního odsouhlasení.
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 30530a9870ba2ff0546237d2698d1675afa78104
ms.sourcegitcommit: 2b4ee1fe05792332904396b5f495d74f2a217250
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2022
ms.locfileid: "8770187"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Nastavte pokročilý import bankovního odsouhlasení pomocí elektronického výkaznictví

[!include [banner](../includes/banner.md)]

Funkce Rozšířené odsouhlasení banky umožňuje importovat elektronické bankovní výpisy a automaticky je odsouhlasit z bankovních transakcí v aplikaci Microsoft Dynamics 365 Finance. Toto téma vysvětluje, jak nastavit funkci importu pro bankovní výpisy. Nastavení import bankovního výpisu závisí na formátu vašeho elektronického bankovního výpisu. Aplikace Microsoft Dynamics 365 Finance podporuje tři formáty bankovního výpisu: ISO20022, MT940 a BAI2. 

## <a name="set-up-the-electronic-reporting-configuration"></a>Nastavte konfiguraci elektronického výkaznictví

1. Přejděte na **Pracovní prostory \> Elektronické sestavy**.
2. Na dlaždici pro poskytovatele konfigurace **Microsoft** vyberte **Úložiště**.
3. Vyberte **Globální** a potom vyberte **Otevřít**.
4. Pokud je nutné vytvořit připojení k úložišti, vyberte v dialogovém okně modrý odkaz.
5. V seznamu konfigurace najděte **Model bankovního výpisu \> Model bankovního výpisu BAI2**.
6. Vyberte formát **BAI2**.
7. Na pevné záložce **Verze** zvolte nejnovější verzi a poté zvolte **Importovat**.

## <a name="set-up-the-bank-statement-format"></a>Nastavte formát bankovních výpisů

1. Přejděte do nabídky **Pokladna a banka \> Nastavení \> Nastavení rozšířeného odsouhlasení banky \> Formát bankovního výpisu**.
2. Zvolte **Nové**.
3. Nastavte pole **Formát výpisů** a **Název**.
4. Vyberte zaškrtávací políčko **Obecný formát elektronického importu**.
5. Nastavte pole **Konfigurace formátu importu** na formát **BAI2**.

## <a name="set-up-the-bank-account"></a>Nastavení bankovního účtu

1. Přejděte do části **Pokladna a banka \> Bankovní účty \> Bankovní účty**.
2. Otevřete bankovní účet.
3. Na pevné záložce **Odsouhlasení** nastavte možnost **Rozšířené odsouhlasení banky** na **Ano**.
4. Nastavte pole **Formát výpisu** na formát **BAI2**, který jste vytvořili dříve.

## <a name="import-the-bank-statement"></a>Import bankovního výpisu

1. Přejděte do části **Pokladna a banka \> Odsouhlasení bankovního výpisu \> Bankovní výpisy**.
2. V horní části stránky **Bankovní výpisy** vyberte **Výpis importu**.
3. Nastavte pole **Bankovní účet** na bankovní účet ve výpisu.
4. Nastavte pole **Formát výpisu** na formát **BAI2**, který jste vytvořili dříve.
5. Vyberte **Procházet** a vyberte soubor **BAI**.
6. Vyberte **Odeslat**.
7. Vyberte **OK** k importu vybraných souborů.


## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Příklady formátů bankovních výpisů a technické rozložení
Níže jsou uvedeny příklady technických definic rozložení pro komplexní importní soubory s bankovním odsouhlasením a tři související [vzorové soubory bankovních výpisů](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Technická definice rozložení                             | Vzorový soubor s bankovním výpisem          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)     |
| DynamicsAXISO20022Layout | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)     |

