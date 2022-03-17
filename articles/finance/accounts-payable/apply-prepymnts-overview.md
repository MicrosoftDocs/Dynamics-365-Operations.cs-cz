---
title: Automatické použití záloh na faktury dodavatele
description: Toto téma popisuje možnost automatického použití záloh na faktury dodavatele.
author: sunfzam
ms.date: 10/19/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 8583962c41a7ac5e27463f325ddc2ccd367331cc
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358207"
---
# <a name="automatically-apply-to-vendor-invoices"></a>Automatické použití na faktury dodavatele

[!include [banner](../includes/banner.md)]

Toto téma popisuje možnost automatického použití záloh na faktury dodavatele. Pro objednávku lze v rámci kupní smlouvy vytvořit platbu předem. Po obdržení faktury dodavatele lze zálohu použít k vyrovnání závazků z faktury dodavatele. Nová funkce umožňuje systému automaticky používat čísla nákupních objednávek na faktuře dodavatele k vyhledání odpovídajících záloh při importu faktury dodavatele.

Pokud jsou zálohy nalezeny a lze je použít, přidají se k existujícím řádkům faktury řádky pro uplatnění záloh. Během procesu párování faktur nejsou nikdy brány v úvahu řádky záloh.

Následující body popisují, jak se uplatňují zálohy, když jsou dodržovány různé nákupní procesy:

- **Jedna faktura dodavatele na nákupní objednávku** – Záloha na nákupní objednávce bude použita na fakturu dodavatele.
- **Jedna faktura dodavatele na více nákupních objednávek** – Zálohy na všech nákupních objednávkách budou použity na fakturu dodavatele.
- **Více faktur dodavatele na nákupní objednávku** – Záloha na nákupní objednávce bude použita na první importovanou fakturu dodavatele. Pokud částka zálohy přesáhne částku faktury, použití zálohy se nezdaří a je nutné provést zálohu ručně.
- **Více faktur dodavatele pro více nákupních objednávek** – Zálohy na nákupních objednávkách budou použita na první relevantní fakturu. Pokud částka zálohy přesáhne částku faktury, použití zálohy se nezdaří a je nutné provést zálohy ručně. Pokud jsou nějaké zálohy, které zůstanou po zálohách, použity na první faktuře, lze je použít na faktury následující.

Jestliže pokus o použití zálohy selže, další kroky určí na nastavení možnosti **Zablokovat proces následné automatizace v případě selhání použití zálohy**:

- **Ano** – Do historie automatizace se přidá chybové hlášení „Automatické použití zálohy: Selhalo“ a faktura zůstane v seznamu nevyřízených faktur dodavatele. Faktura zůstane zablokována, dokud ručně nezaplatíte zálohu.

Chcete-li ručně použít zálohy, přejděte na nevyřízenou fakturu dodavatele. Na stránce **Detaily faktury** nastavte možnost **Zahrnout do automatizovaného zpracování** pro blokovanou fakturu na **Ne**. Nyní můžete ručně použít platbu předem. Po připsání platby předem nastavte možnost **Zahrnout do automatizovaného zpracování** zpět na **Ano**, aby mohla být faktura automaticky zpracována.

Automatickou aplikaci zálohy můžete také obejít nastavením možnosti **Zahrnout do automatizovaného zpracování** na **Ne** a poté jejím nastavením zpět na **Ano**. Obdržíte následující zprávu: „Pro objednávku již existuje platba předem. Chcete to ignorovat u faktury vybraného dodavatele?“ Vyberte **Ano**. Do historie automatizace je přidána zpráva „Použití platby předem bylo vynecháno ručně“ a faktura dodavatele nebude zablokována, když se automatizovaný proces znovu spustí.

- **Ne** – Následné automatizační procesy budou pokračovat. Zálohu můžete uplatnit i při vyúčtování.
