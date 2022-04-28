---
title: Nastavte a vygenerujte soubory kladných plateb pomocí elektronického výkaznictví
description: Toto téma vysvětluje postup při nastavení kladných plateb pomocí elektronického výkaznictví.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 43dd1a9cba1fe8df5cff26fe76af7e2957a0d6a4
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544468"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Nastavte soubory kladných plateb pomocí elektronického výkaznictví

Nastavte kladné platby pro generování elektronických seznamů šeků, které jsou dodávány bance. Poté při předložení šeku bance ho banka srovná se seznamem šeků. Pokud šek odpovídá tomu, co má banka má v záznamech v seznamu, banka jej zúčtuje. Pokud šek neodpovídá šeku v seznamu, banka předloží šek ke kontrole.

## <a name="set-up-the-electronic-reporting-configuration"></a>Nastavte konfiguraci elektronického výkaznictví

1. Přejděte na **Pracovní prostory \> Elektronické sestavy**.
2. Na dlaždici pro poskytovatele konfigurace **Microsoft** vyberte **Úložiště**.
3. Vyberte **Globální** a potom vyberte **Otevřít**.
4. Pokud je nutné vytvořit připojení k úložišti, vyberte v dialogovém okně modrý odkaz.
5. V seznamu konfigurace vyhledejte a vyberte **Model kladných plateb \> Formát kladných plateb**.
6. Na pevné záložce **Verze** zvolte nejnovější verzi a poté zvolte **Importovat**.

## <a name="set-up-a-positive-pay-format"></a>Nastavení formátu kladné platby

1. Přejděte do **Pokladna a banka \> Nastavení \> Formáty kladných plateb**.
2. Zvolte **Nové**.
3. Nastavte pole **Formát plateb** a **Popis**.
4. Vyberte zaškrtávací políčko **Obecný formát elektronického exportu**.
5. Nastavte pole **Konfigurace formátu exportu** na **Formát kladných plateb**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Přiřazení formátu kladné platby k bankovnímu účtu

1. Přejděte do části **Pokladna a banka \> Bankovní účty \> Bankovní účty**.
2. Otevřete bankovní účet.
3. Na pevné záložce **Všeobecné** nastavte pole **Formát kladných plateb** na formát, který byl vytvořen dříve.
4. Nastavte pole **Počáteční datum kladných plateb** na aktuální datum.

## <a name="generate-a-positive-pay-file"></a>Vygenerovat soubor kladných plateb

1. Přejděte na **Pokladna a banka \> Bankovní účty \> Bankovní účty**.
2. Otevřete bankovní účet, pro který je nastavena kladná platba.
3. Vyberte **Spravujte platby \> Kladná platba \> Soubor kladných plateb**.
4. Nastavte pole **Datum přerušení**. Kontroly generované před tímto datem budou zahrnuty.

Výsledný soubor XML bude stažen.
