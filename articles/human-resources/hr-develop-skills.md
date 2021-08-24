---
title: Nakonfigurujte dovednosti
description: Můžete sledovat dovednosti svého pracovníka v Dynamics 365 Human Resources. Můžete také určit dovednosti, které jsou požadovány pro určitou práci.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a8025dd4000a3678e7f7eb7faebfa45852f0054570a2948dadbc21913c63f578
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732146"
---
# <a name="configure-skills"></a>Nakonfigurujte dovednosti

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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