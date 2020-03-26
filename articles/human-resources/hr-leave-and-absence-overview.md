---
title: Přehled
description: V Dynamics 365 Human Resources poskytuje pracovní prostor **Pracovní volno a absence** flexibilní prostředí pro vytváření nových plánů pracovního volna, workflowů pro správu požadavků a intuitivní samoobslužné stránky pro zaměstnance, kteří žádají o pracovní volno.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 493bc3abe82103541125914896252b2eae596b38
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091741"
---
# <a name="overview"></a>Přehled

Dynamics 365 Human Resources vám pomáhá poskytovat vašim pracovníkům skvělé benefity ve formě pracovního volna. Pracovní prostor **Pracovní volno a absence** poskytuje flexibilní prostředí pro vytváření nových plánů pracovního volna, workflowů pro správu požadavků a intuitivní samoobslužné stránky pro zaměstnance, kteří žádají o pracovní volno. Analýza pomáhá organizaci měřit a monitorovat zůstatky pracovního volna a využití plánů pracovního volna.

## <a name="set-up-leave-and-absence"></a>Nastavení pracovního volna a absence

Dříve než můžete vytvořit plány pro zaměstnance, je nutné provést několik kroků nastavení:

- [Konfigurace parametrů pracovního volna a absence](hr-leave-and-absence-parameters.md)
- [Vytvoření kalendáře pracovní doby](hr-leave-and-absence-working-time-calendar.md)
- [Vytvoření workflow žádosti o pracovní volno](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a>Vytvoření a správa plánů pracovního volna

Před vytvořením plánů pracovního volna pro pracovníky je nutné vytvořit typy volna a absence. Po vytvoření plánu pracovního volna můžete do plánu zapsat pracovníky. Můžete také spustit proces časového rozlišení, vytvořit výstrahy a zobrazit analýzu pro vaše plány.

- [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md)
- [Vytvoření plánu pracovního volna a absence](hr-leave-and-absence-plans.md)
- [Přiřazení pracovníků k plánu pracovního volna](hr-leave-and-absence-enroll.md)
- [Časové rozlišení plánů pracovního volna a absence](hr-leave-and-absence-accrue.md)
- [Zobrazení analýz pro pracovní volno a absenci](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a>Žádost o volný čas a správa žádostí

Zaměstnanci mohou odesílat žádosti o volno a spravovat je v pracovním prostoru **Samoobsluha zaměstnanců**.

- [Požádat o volno](hr-employee-self-service-request-time-off.md)
- [Správa žádostí o pracovní volno a absenci](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-preview-features"></a>Funkce náhledu pracovního volna a absence

V prostředí **izolovaného prostoru** můžete vyzkoušet nové funkce náhledu pracovního volna a absence. Informace o zapnutí funkcí náhledu naleznete v tématu [Správa funkcí](hr-admin-manage-features.md). Funkce náhledu zahrnují:

- **Kalendář pracovního volna a absence** – parametry pracovního volna a absence budou přesunuty z **Parametrů Human Resources** na novou obrazovku nazvanou **Parametry pracovního volna a absence**. Nová obrazovka obsahuje novou kartu **Kalendář**. Tato funkce Preview umožňuje pouze podmnožinu parametrů. K nové obrazovce můžete přistupovat z karty **Odkazy** pracovního prostoru **Pracovní volno a absence**. Kalendáře zahrnují:
  - **Kalendář společnosti** -zobrazí všechny žádosti zaměstnance o volno. Uživatelé s rolí **lidské zdroje** mají k tomuto kalendáři přístup z karty **Odkazy** v pracovním prostoru **Pracovní volno a absence**.
  - **Kalendář týmu manažera** – zobrazí všechny žádosti podřízených o volno. Manažeři mohou získat přístup k kalendáři z karty **Můj tým** ve samoobsluze pro zaměstnance v nabídce **Pracovní volno a absence**. 

- **Kalendáře svátků pracovního vola a absence** – typy volna zahrnují novou možnost **svátků**, která se používá ve spojení s kalendářem pracovní doby. Dny definované svátky a zavíracími dny jsou nyní určeny jako **svátek** při generování pracovních dnů. Při zpracování časového rozlišení jsou úpravy prováděny u zaměstnanců přiřazených ke kalendáři s ohledem na svátky spadající na pracovní den.

- **Audit časového rozlišení pracovního volna** – nová obrazovka umožňuje zkontrolovat, kdy byla časová rozlišení zpracována a odstraněna všemi zaměstnanci i jednotlivými zaměstnanci. K nové obrazovce můžete přistupovat z karty **Odkazy** pracovního prostoru **Pracovní volno a absence**.

- **Odstranění časového rozlišení pracovního volna** – nyní můžete odstranit záznamy časového rozlišení pro konkrétní plány pracovního volna. K nové možnosti můžete přistupovat z karty **Odkazy** pracovního prostoru **Pracovní volno a absence**. U jednotlivých zaměstnanců se tato možnost zobrazí v seskupení **Pracovní volno a absence** v profilu zaměstnance. 

- **Zaokrouhlování časového rozlišení pracovního volna** – nové možnosti pro **Typ pracovního volna** definují, jaký typ zaokrouhlení má časové rozlišení použít, a desetinnou přesnost zaokrouhlení v průběhu procesu časového rozlišení. Při zpracování časových rozlišení jsou zaokrouhlení a přesnost použity pro záznamy časového rozlišení. 

- **Konfigurovat více typů pracovního volna u jednoho plánu pracovního volna** – nový sloupec v plánu časového rozlišení pracovního volna pro typy pracovního volna umožňuje definovat více typů pracovního volna v plánu pracovního volna a absence s různými plány časového rozlišení. Předchozí pole **Typ pracovního volna** je odstraněno. Při registraci zaměstnance se zůstatky pro typy pracovního volna nyní zobrazují v tabulce namísto na horním okraji obrazovky.

  > [!IMPORTANT]
  > Když tuto funkci povolíte, můžete ji poté vypnout.

- **Použití ekvivalentu plného úvazku zaměstnance pro časové rozlišení** – nový sloupec v plánu časového rozlišení pracovního volna pomocí ekvivalentu plného úvazku pro časové rozlišení. Při zpracování časového rozlišení používá aplikace primární pozici zaměstnance a ekvivalent plného úvazku pro určení poměrné částky časového rozlišení.

  > [!NOTE]
  > Tato funkce je k dispozici pouze tehdy, když povolíte možnost **Konfigurovat více typů pracovního volna u jednoho plánu pracovního volna**. 
