---
title: Organizační hierarchie v Dataverse
description: Tento článek popisuje integraci dat organizace mezi finančními a provozními aplikacemi a Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 48533dd104f62080d0ebd47389a4a829c772db13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289039"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organizační hierarchie v Dataverse

[!include [banner](../../includes/banner.md)]



Vzhledem k tomu, že Dynamics 365 Finance je finanční systém, *organizace* je hlavním konceptem a nastavení systému začíná konfigurací hierarchie organizací. Obchodní finance lze poté sledovat na úrovni organizace a také na libovolné úrovni v hierarchii organizací.

Přestože Dataverse nemá koncept organizační hierarchie, má několik volných konceptů, například celkový výnos z prodeje. Jako součást integrace Dataverse je do Dataverse přidána datová struktura hierarchie organizací.

## <a name="data-flow"></a>Tok dat

Podnikatelský ekosystém, který se skládá z finančních a provozních aplikací a Dataverse bude nadále mít hierarchii organizací. Tato hierarchie organizací je postavena na finančních a provozních aplikacích, ale je zpřístupněna v Dataverse pro informační účely a účely rozšiřitelnosti. Následující ilustrace znázorňuje informace o hierarchii organizace, které jsou vystaveny v Dataverse jako jednosměrný tok dat z finančních a provozních aplikací do Dataverse.

![Obrázek architektury.](media/dual-write-data-flow.png)

Mapování tabulky organizační hierarchie jsou k dispozici pro jednosměrnou synchronizaci dat z finančních a provozních aplikací do Dataverse.

## <a name="templates"></a>Šablony

Organizace představuje skupinu lidí, kteří spolupracují na provádění obchodního procesu nebo dosažení cíle. Organizační hierarchie představuje vztahy mezi organizacemi, které tvoří váš podnik. Můžete definovat následující typy interních organizací: právnické osoby, provozní jednotky a týmy. Jak ukazuje následující tabulka, je vytvořena kolekce tabulkových map pro synchronizaci informací o právnických osobách, provozních jednotkách a souvisejících organizačních hierarchiích.

Finanční a provozní aplikace | Aplikace Customer Engagement     | Popis
-----------------------|--------------------------------|---
[Právnické osoby](mapping-reference.md#102) | cdm_companies | 
[Právnické osoby](mapping-reference.md#142) | msdyn_internalorganizations |
[Provozní jednotka](mapping-reference.md#143) | msdyn_internalorganizations |
[Organizační hierarchie - publikovaná](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | Tato šablona poskytuje jednosměrnou synchronizaci tabulky publikované hierarchie organizace.
[Účely organizační hierarchie](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | Tato šablona poskytuje jednosměrnou synchronizaci tabulky účelu hierarchie organizace.
[Typ organizační hierarchie](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | Tato šablona poskytuje jednosměrnou synchronizaci tabulky typu hierarchie organizace.

## <a name="internal-organization"></a>Interní organizace

Informace o interní organizaci v Dataverse pocházejí ze dvou tabulek, **Provozní jednotka** a **Právnická osoba**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

