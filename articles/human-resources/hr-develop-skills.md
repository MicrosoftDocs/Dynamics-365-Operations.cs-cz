---
title: Nakonfigurujte dovednosti
description: Můžete sledovat dovednosti svého pracovníka v Dynamics 365 Human Resources. Můžete také určit dovednosti, které jsou požadovány pro určitou práci.
author: twheeloc
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 7c853ad71aecd7f5d214c02da97f7956ff2391df
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695949"
---
# <a name="configure-skills"></a>Nakonfigurujte dovednosti

> [!IMPORTANT]
> Funkce uvedené v tomto tématu jsou aktuálně dostupné pro zákazníky Human Resources v samostatné infrastruktuře Finance.  


Můžete sledovat dovednosti svého pracovníka v Dynamics 365 Human Resources. Můžete také určit dovednosti, které jsou požadovány pro určitou práci.

Zde jsou příklady dovedností, které lze sledovat:

- Dozorčí - schopnost dohlížet na práci ostatních.
- Vůdčí - schopnost vést zaměstnance a obchodní domény.
- Plánování - schopnost dívat se dopředu, formulovat vize a schopnost tyto vize definovat.
- HTML – schopnost psát v kódu HTML.

Pokud jste ještě nenastavili typy dovedností a modely hodnocení, budete je muset před vytvořením dovedností přidat.

Dovednosti pro pracovníka mohou zadat následující lidé:

- Pracovníci mohou sami zadat dovednosti do samoobsluhy zaměstnanců. Tyto dovednosti vyžadují souhlas manažera.
- Manažeři mohou zadat dovednosti pro své pracovníky. Můžete vytvořit pracovní postup, který tyto dovednosti automaticky schválí.

## <a name="create-a-skill-type"></a>Vytvoření typu dovednosti

Typy dovedností jsou kategorie, do kterých jednotlivé dovednosti spadají, například administrativa nebo prodej.

1. V pracovním prostoru **Rozvoj zaměstnanců** vyberte **Odkazy**.

2. V **Nastavení kompetence** vyberte **Typy dovedností**.

3. Zvolte **Nové**.

4. Vyplňte následující pole:

   - **Typ dovednosti**: Zadejte název typu dovednosti.
   - **Popis**: Zadejte popis typu dovednosti.

5. Zvolte možnost **Uložit**.

## <a name="create-a-rating-model"></a>Vytvoření nového modelu hodnocení

Modely hodnocení pomáhají ve vyhodnocení skutečné úrovně dovedností osoby, úrovně, které mají dosáhnout, nebo úrovně dovednosti, která je požadována pro úlohu. Každé úrovni v modelu hodnocení je přiřazen koeficient.

1. V pracovním prostoru **Rozvoj zaměstnanců** vyberte **Odkazy**.

2. V **Nastavení kompetence** vyberte **Modely hodnocení**.

3. Zvolte **Nové**.

4. Vyplňte následující pole:

   - **Hodnocení**: Zadejte název modelu hodnocení, například **Dovednosti**.
   - **Popis**: Zadejte popis modelu hodnocení, například **Hodnocení dovedností**.

5. V sekci **Úrovně** vyberte **Nový**. Pro každou úroveň, kterou chcete přidat, vyplňte následující pole:

   - **Ǔroveň**: Zadejte název úrovně.
   - **Popis**: Zadejte popis úrovně.
   - **Faktor**: Zadejte hodnotu faktoru od 0-9. Faktor pomáhá normalizovat výsledky dovedností, které používají různé modely hodnocení. Každá úroveň musí mít jedinečný faktor. Úrovně s vyšší hodnotou koeficientu nesou v modelu hodnocení větší váhu.

   Podle potřeby pokračujte v přidávání úrovní. Můžete zadat až 10 úrovní pro každý model hodnocení.

6. Zvolte možnost **Uložit**.

## <a name="create-a-skill"></a>Vytvoření dovednosti

Před přiřazením dovednosti nebo vytvořením vyhledávání s mapováním dovedností nebo vytvořením profilu dovedností je nutné zadat informace o dovednostech na stránce **Dovednosti**. Pro každou dovednost můžete vybrat typ dovednosti a model hodnocení.

1. V pracovním prostoru **Rozvoj zaměstnanců** vyberte **Odkazy**.

2. V **Nastavení kompetence** vyberte **Dovednosti**.

3. Zvolte **Nové**.

4. Vyplňte následující pole:

   - **Dovednost**: Zadejte název typu dovednosti.
   - **Popis**: Zadejte popis dovednosti.
   - **Hodnocení**: Vyberte model hodnocení, který chcete pro tuto dovednost použít.
   - **Typ dovednosti**: Vyberte ze seznamu typů dovedností.

5. Zvolte možnost **Uložit**.

## <a name="see-also"></a>Viz také

[Zadejte dovednosti](hr-develop-enter-skills.md)<br>
[Mapové dovednosti](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
