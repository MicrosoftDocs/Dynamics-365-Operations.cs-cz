---
title: Sledování zdrojů pro profily a žádosti kandidátů
description: Toto téma obsahuje informace o sledování zdroje pro profily kandidáta a žádosti.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ebc82ada31d2803800358cd9aecfe389ada8f0dc
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/25/2019
ms.locfileid: "897450"
---
# <a name="track-sources-for-candidate-profiles-and-applications"></a>Sledování zdrojů pro profily a žádosti kandidátů 

[!include[banner](../includes/banner.md)]

> [!NOTE] 
> Funkce pojednávaná v tomto tématu je k dispozici jako součást verze Preview. Obsah a funkce se mohou změnit. Chcete-li použít tuto funkci, požádejte správce o její povolení pomocí **Nastavení pro správu** v aplikaci Attract. Budoucí verze nabídne sestavy sledování zdrojů. Další informace naleznete v tématu [Přístup k funkcím Preview v aplikaci Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature).

Když kandidáti požádají o práci, Attract automaticky sleduje zdroj jejich žádostí a poskytne vám cenné informace, které vám pomohou zaměřit náborové úsilí. Náboroví pracovníci a manažeři mohou také vybrat zdroj žádosti při ručním přidávání kandidáta k práci nebo skupině talentů.

Zdroj žádosti můžete zobrazit v podrobnostech aktivity žádosti na kartě **Aktivita**, stejně jako v historii žádosti dostupné pod možností **Profil** ve skupině talentů. Zdroj profilu kandidáta naleznete v podrobnostech kandidáta pod kartou **Profil** v žádostech i skupinách talentů.

> [!NOTE] 
> Šablony procesu naleznete v [doplňku komplexního náboru](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-comprehensive-hiring).

## <a name="pre-configured-sources"></a>Předkonfigurované zdroje

Výchozí seznam zdrojů obsahuje běžné zdroje žádostí. Některé typy zdrojů, například **Pracovní vývěska** a **Sociální sítě** mají další podrobnosti zdroje. Například **sociální sítě** zahrnují Facebook a Twitter. Typ zdroje **Reference** vám umožní určit interního zaměstnance jako poskytovatele reference. Výchozí seznam zdrojů obsahuje následující předem nakonfigurované zdroje:

-   Kariérní web Attract

-   Agentura

-   Kariérní veletrh

-   Marketing společnosti

-   Konference a obchodní veletrhy

-   Profesní asociace

-   Pracovní vývěska

    -   Indeed

    -   Seek

    -   CareerBuilder

    -   Google Jobs

    -   Xing

    -   Glassdoor

    -   Monster Jobs

-   Časopisy a publikace

-   Sociální sítě

    -   Facebook

    -   Twitter

-   Univerzitní nábor

-   LinkedIn

-   Classifieds

-   Reference

-   Přidáno náborářem

-   Jiný

## <a name="customize-the-source-list"></a>Přizpůsobení seznamu zdroje 

Můžete rozšířit seznam zdrojů a zahrnout další zdroje žádostí. Chcete-li přizpůsobit tento seznam, postupujte podle pokynů v části [Rozšíření sad možností v aplikaci Attract](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract). Upravte entitu **TalentSource** pro zahrnutí dalších zdrojů. 

Chcete-li se vyhnout negativním dopadům na uživatelské rozhraní, neupravujte nebo neodstraňujte hodnoty výčtů **TalentCategory** (nikoli názvy) pro následující položky:

- **Reference**
- **LinkedIn**
- **Jiný**

Místo toho můžete rozšířit výčet **TalentSource** pro přidání dalších typů zdrojů.
