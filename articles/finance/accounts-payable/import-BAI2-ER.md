---
title: Nastavte pokročilý import bankovního odsouhlasení pomocí elektronického výkaznictví
description: Toto téma vysvětluje, jak používat elektronické hlášení k nastavení pokročilého procesu importu bankovního odsouhlasení pro výpisy BAI2.
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
ms.openlocfilehash: 39f1d8ba561ab0e36346f1dfb4f70df318c92a37
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544476"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>Nastavte pokročilý import bankovního odsouhlasení pomocí elektronického výkaznictví

[!include [banner](../includes/banner.md)]

Funkce Rozšířené odsouhlasení banky umožňuje importovat elektronické bankovní výpisy a automaticky je odsouhlasit z bankovních transakcí v aplikaci Microsoft Dynamics 365 Finance. Toto téma vysvětluje, jak nastavit funkci importu pro bankovní výpisy BAI2.

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
