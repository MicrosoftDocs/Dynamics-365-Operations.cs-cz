---
title: Přehled
description: V Dynamics 365 Human Resources poskytuje pracovní prostor Pracovní volno a absence flexibilní prostředí pro vytváření nových plánů pracovního volna, workflowů pro správu požadavků a intuitivní samoobslužné stránky pro zaměstnance, kteří žádají o pracovní volno.
author: andreabichsel
manager: AnnBe
ms.date: 04/30/2020
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
ms.openlocfilehash: 2bb123b808615ff7d770c7c6b83338a32d922be3
ms.sourcegitcommit: de217452a85429675994e9cc0e06eb4821cab3e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/30/2020
ms.locfileid: "3325758"
---
# <a name="overview"></a>Přehled

Dynamics 365 Human Resources vám pomáhá poskytovat vašim pracovníkům skvělé benefity ve formě pracovního volna. Pracovní prostor **Pracovní volno a absence** poskytuje flexibilní prostředí pro vytváření nových plánů pracovního volna, workflowů pro správu požadavků a intuitivní samoobslužné stránky pro zaměstnance, kteří žádají o pracovní volno. Analýza pomáhá organizaci měřit a monitorovat zůstatky pracovního volna a využití plánů pracovního volna.

## <a name="set-up-leave-and-absence"></a>Nastavení pracovního volna a absence

Před vytvořením plánů pro zaměstnance, je nutné provést několik kroků nastavení:

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

- [Požádat o volno](hr-employee-self-service-request-time-off.md)
- [Správa žádostí o pracovní volno a absenci](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-known-issues"></a>Známé problémy s pracovním volnem a absencí

### <a name="rounding-precision"></a>Přesnost zaokrouhlování

Nelze nastavit **Přesnost zaokrouhlení** při nastavení **Typu zaokrouhlení**. **Přesnost zaokrouhlení** lze nastavit pouze pomocí entity **Typ pracovního volna a absence**. 

1. V **Typy pracovního volna a absence** vyberte **Otevřít v aplikaci Exce** pro otevření entity **Typ pracovního volna a absence**.

2. Po otevření a povolení souboru vyberte **Návrh**.

3. V tabulce **Typ pracovního volna a absence** vyberte možnost tužky pro úpravy.

4. Vyberte **RoundingPrecision** a **RoundingType** a poté vyberte položku **Přidat** pro přidání do seznamu polí.

5. Vyberte **Aktualizovat** a potom **Hotovo**.

6. Zadejte nebo vyberte **Typ zaokrouhlení** pro každý typ pracovního volna, pokud ještě nebyl nastaven. 

7. Zadejte **Přesnost zaokrouhlení** pro příslušné typy.

8. Výběrem **Publikovat** odešlete změny do Human Resources.

## <a name="leave-and-absence-preview-features"></a>Funkce náhledu pracovního volna a absence

V prostředí **izolovaného prostoru** můžete vyzkoušet nové funkce náhledu pracovního volna a absence. Informace o zapnutí funkcí náhledu naleznete v tématu [Správa funkcí](hr-admin-manage-features.md). 

[!include [banner](includes/preview-feature.md)]

Funkce náhledu zahrnují:

- **Přerušení pracovního volna** - můžete přerušit pracovní volno a absenci v Human Resources pro zaměstnance. Pozastavením volna se zastaví časové rozlišení volna pro vybrané typy pracovního volna. Pokud k přerušení dojde po zpracování časového rozlišení, pozastavením volna se vytvoří průběžná Úprava zůstatku zaměstnance. Při pozastavení dovolené zaměstnance můžete také uvést kódy důvodů. Uživatelské prostředí bylo aktualizováno, aby indikovalo pozastavení. 

- **Pravidla převodu do dalšího období** - můžete určit typ převodu pracovního volna do dalšího období pro převod zůstatků, kde byly převedeny úpravy převodu do dalšího období. Pokud například zaměstnanec přenese deset dní dopředu, můžete pro tyto 10 dny vybrat jiný typ pracovního volna. 

- **Uveďte kód důvodu a komentáře k úpravám** – Při úpravě zůstatku dovolené zaměstnance můžete uvést kód důvodu a komentář. 

- **Parametry přechodu na dovolenou a nepřítomnost** – Nyní můžete místo použití parametrů Lidské zdroje používat pouze parametry Dovolená a absence. 
