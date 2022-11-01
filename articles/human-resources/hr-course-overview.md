---
title: Přehled kurzů
description: Tento článek vysvětluje jak správci Human Resources a vedoucí pracovníci mohou funkce kurzů používat ke správě informací o kurzech, které jsou dostupné pracovníkům.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a1fd00fb9feea9ab426f67095770389696452215
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716331"
---
# <a name="courses-overview"></a>Přehled kurzů

Microsoft Dynamics 365 Human Resources poskytuje řešení vzdělávacích potřeb vaší organizace. Toto řešení nabízí dvě vzdělávací cesty: *virtuální* a *pod vedením instruktora*.

*Virtuální učení* je vzdělávací prostředí, které je vylepšeno prostřednictvím online zdrojů. Ve *školení vedené instruktorem* instruktor provází školením skupinu pracovníků nebo studentů.

V našem výukovém modulu mohou odborníci, administrátoři, školící manažeři a manažeři Human Resources vytvářet a přidělovat pracovníkům obě vzdělávací cesty.

> [!NOTE]
> Chcete-li používat virtuální kurzy, musíte zapnout funkci **Vylepšení kurzu** v části Správa funkcí.

## <a name="set-up-virtual-courses"></a>Nastavení virtuálních kurzů

Chcete-li konfigurovat virtuální kurzy, musíte zapnout funkci **Vylepšení kurzu** v části Správa funkcí. Přejděte na **Kurzy \> Nový** a nastavte možnost **Virtuální** na **Ano**. Po aktivaci funkce je vyžadován odkaz na kurz. Pole **Stav kurzu** bude nastaveno na **Otevřený**. Možnost **Umožnit zaměstnanci, aby se sám registroval** bude nastavena na **Ano**, ale dá se nastavit na **Ne**.

Po zapnutí funkce **Vylepšení kurzu** ve správě funkcí dojde k následujícím změnám:

- Pro zadání kurzu musí být stanoven termín odevzdání.
- Je vyžadován odkaz na kurz.
- **Zaměstnanecká samoobsluha** zobrazí přehled zaměstnanců v části **Kurzy**. Uživatel může zobrazit kurzy, které jsou po termínu, mají termín brzy a přidělené.
- Pracovníci mohou absolvovat virtuální kurzy a sami se jim osvědčovat.

## <a name="set-up-instructor-led-courses"></a>Nastavení kurzů vedených instruktorem

Kurzy vedené instruktorem není nutné před použitím konfigurovat.

Následující informace jsou volitelné a dají se pro kurzy zadat. Pokud budou tyto informace zadány pro kurzy, měly by být nastaveny před vytvořením záznamů o kurzu:

- Typ kurzu
- Skupiny učeben
- Skupiny kurzů
- Místo konání kurzu
- Učebny
- Instruktoři
- Typy kurzů

*Typy kurzů* slouží k rozdělení kurzů podle struktury nebo obsahu kurzu. Na stránce  **Typy kurzů**  můžete vytvořit typy kurzů.

Maximální a minimální počty účastníků, které lze do kurzu registrovat, jsou uvedeny na pevné záložce  **Obecné**  na stránce  **Kurzy** .

### <a name="course-setup-type"></a>Typ nastavení kurzu 

*Typy nastavení* určují strukturu kurzu. Kurzy mají tři typy nastavení.

| Typ nastavení | Popis |
|------|--------|
| Standardní | Kurzy tohoto typu nastavení nemají denní agendu. Toto je výchozí typ nastavení, když vytváříte nový kurz. |
| Agenda | Tento typ nastavení vyberte pro naplánování podrobností pro jednotlivé dny vícedenního kurzu. |
| Agenda + relace | <p>Vyberte tento typ nastavení pro složitější kurzy. Agendu kurzu lze například rozdělit do *běhů* a *relací*.</p><ul><li>*Běhy* jsou konkrétní témata kurzu.</li><li>*Relace* rozdělují běhy a mohou identifikovat specifické procesy nebo postupy, které se vztahují k jednotlivým běhům.</li></ul> |

### <a name="course-tasks"></a>Úkoly kurzu

U každého kurzu proveďte následující úlohy:

- Zaregistrujte účastníky.
- Nastavte uzávěrku registrace.
- Definujte minimální a maximální počet účastníků.
- Přiřaďte místo konání kurzu a učebnu.
- Doporučte hotely účastníkům kurzu.
- Vytvořte popis kurzu, který je poté možné zveřejnit na portálu  **Samoobsluha pro zaměstnance**.

> [!NOTE]
> Kurz lze odstranit pouze v případě, že do něj není nikdo zaregistrován.

### <a name="course-statuses"></a>Stavy kurzu

Následující tabulka uvádí stavy kurzů a akce, které se pro každý z nich provádějí.

| Stav | Akce |
|------|--------|
| Vytvořeno | <ul><li>Zadávání a úprava informací o kurzu.</li><li>Změňte stav kurzu na  **Otevřen**, aby se pracovníci mohli do kurzu registrovat.</li></ul> | 
| Otevřít | <ul><li>Zaregistrujte účastníky na kurz.</li><li>Odeberte účastníky z kurzu.</li><li>Potvrďte účastníky kurzu.</li><li>Změňte stav kurzu na  **Uzavřený**  nebo  **Zrušený** pro účastníky, jejichž stav je  **Potvrzeno**.</li></ul>|
| Zavřeno | Kurz můžete znovu otevřít. |
| Zrušeno | Kurz můžete znovu otevřít. |

### <a name="course-participants"></a>Účastníci kurzu

*Účastníci kurzu* jsou pracovníci, kteří se účastní školicího kurzu nebo události. Účastníky můžete registrovat pro otevřené kurzy.

### <a name="workflow"></a>Pracovní postup

Zaměstnancům, kteří se do kurzu zaregistrují na stránce  **Samoobsluha pro zaměstnance** , může být registrace nasměrována do workflowu pro schválení. Workflow lze přiřadit ke kurzu na pevné záložce  **Obecné**  na stránce  **Kurzy** .
