---
title: Organizační hierarchie v Dataverse
description: Toto téma popisuje integraci dat organizace mezi aplikacemi Finance and Operations a Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: c7ef3a11817d60343503c80d89493262711524b1
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782301"
---
# <a name="organization-hierarchy-in-dataverse"></a>Organizační hierarchie v Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Vzhledem k tomu, že Dynamics 365 Finance, je finanční systém, *organizace* je hlavním konceptem a nastavení systému začíná konfigurací hierarchie organizací. Obchodní finance lze poté sledovat na úrovni organizace a také na libovolné úrovni v hierarchii organizací.

Přestože Dataverse nemá koncept organizační hierarchie, má několik volných konceptů, například celkový výnos z prodeje. Jako součást integrace Dataverse je do Dataverse přidána datová struktura hierarchie organizací.

## <a name="data-flow"></a>Tok dat

Podnikatelský ekosystém, který se skládá z aplikací Finance and Operations a Dataverse, bude nadále mít hierarchii organizací. Tato hierarchie organizací je postavena na aplikacích Finance and Operations, ale je zpřístupněna v Dataverse pro informační účely a účely rozšiřitelnosti. Následující ilustrace znázorňuje informace o hierarchii organizace, které jsou vystaveny v Dataverse jako jednosměrný tok dat z aplikací Finance and Operations do Dataverse.

![Obrázek architektury.](media/dual-write-data-flow.png)

Mapování tabulky organizační hierarchie je k dispozici pro jednosměrnou synchronizaci dat z aplikací Finance and Operations do Dataverse.

## <a name="templates"></a>Šablony

Informace o produktu obsahují všechny informace související s produktem a jeho definici, jako jsou například dimenze produktů nebo dimenze sledování a úložiště. Jak je ukázáno v následující tabulce, je vytvořena kolekce map tabulek pro synchronizaci produktů a souvisejících informací.

Aplikace Finance and Operations | Aplikace Customer Engagement     | popis
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
