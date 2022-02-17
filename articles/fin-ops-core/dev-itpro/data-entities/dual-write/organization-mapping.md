---
title: Organizační hierarchie v Dataverse
description: Toto téma popisuje integraci dat organizace mezi finančními a provozními aplikacemi a Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: afc1b5996667835c460f467526493380aa2d6403
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062079"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organizační hierarchie v Dataverse

[!include [banner](../../includes/banner.md)]



Vzhledem k tomu, že Dynamics 365 Finance, je finanční systém, *organizace* je hlavním konceptem a nastavení systému začíná konfigurací hierarchie organizací. Obchodní finance lze poté sledovat na úrovni organizace a také na libovolné úrovni v hierarchii organizací.

Přestože Dataverse nemá koncept organizační hierarchie, má několik volných konceptů, například celkový výnos z prodeje. Jako součást integrace Dataverse je do Dataverse přidána datová struktura hierarchie organizací.

## <a name="data-flow"></a>Tok dat

Podnikatelský ekosystém, který se skládá z finančních a provozních aplikací a Dataverse bude nadále mít hierarchii organizací. Tato hierarchie organizací je postavena na finančních a provozních aplikacích, ale je zpřístupněna v Dataverse pro informační účely a účely rozšiřitelnosti. Následující ilustrace znázorňuje informace o hierarchii organizace, které jsou vystaveny v Dataverse jako jednosměrný tok dat z finančních a provozních aplikací do Dataverse.

![Obrázek architektury.](media/dual-write-data-flow.png)

Mapování tabulky organizační hierarchie jsou k dispozici pro jednosměrnou synchronizaci dat z finančních a provozních aplikací do Dataverse.

## <a name="templates"></a>Šablony

Informace o produktu obsahují všechny informace související s produktem a jeho definici, jako jsou například dimenze produktů nebo dimenze sledování a úložiště. Jak je ukázáno v následující tabulce, je vytvořena kolekce map tabulek pro synchronizaci produktů a souvisejících informací.

Finanční a provozní aplikace | Aplikace Customer Engagement     | popis
-----------------------|--------------------------------|---
[Právnické osoby](mapping-reference.md#102) | cdm_companies | Poskytuje obousměrnou synchronizaci informací o právnické osobě (společnosti).
[Právnické osoby](mapping-reference.md#142) | msdyn_internalorganizations |
[Provozní jednotka](mapping-reference.md#143) | msdyn_internalorganizations |
[Organizační hierarchie - publikovaná](mapping-reference.md#139) | msdyn_internalorganizationhierarchies | Tato šablona poskytuje jednosměrnou synchronizaci tabulky publikované hierarchie organizace.
[Účely organizační hierarchie](mapping-reference.md#140) | msdyn_internalorganizationhierarchypurposes | Tato šablona poskytuje jednosměrnou synchronizaci tabulky účelu hierarchie organizace.
[Typ organizační hierarchie](mapping-reference.md#141) | msdyn_internalorganizationhierarchytypes | Tato šablona poskytuje jednosměrnou synchronizaci tabulky typu hierarchie organizace.

## <a name="internal-organization"></a>Interní organizace

Informace o interní organizaci v Dataverse pocházejí ze dvou tabulek, **Provozní jednotka** a **Právnická osoba**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
