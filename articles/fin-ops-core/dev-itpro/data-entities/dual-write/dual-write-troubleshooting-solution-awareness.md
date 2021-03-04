---
title: Poradce při potížích souvisejících s připraveností řešení
description: Toto téma obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s připraveností řešení.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 79b2920b80ce4a8b419c2a146e15babc061cf64d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683550"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Poradce při potížích souvisejících s připraveností řešení

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Toto téma obsahuje informace o odstraňování potíží pro integrací dvojího zápisu mezi aplikacemi Finance and Operations a Dataverse. Konkrétně obsahuje informace, které vám pomohou vyřešit problémy s připraveností řešení.

> [!IMPORTANT]
> Některé problémy, které toto téma řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD). Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.

## <a name="error-on-the-dual-write-page"></a>Chyba na stránce dvojího zápisu

Na stránce **Dvojího zápisu** se může zobrazit chybová zpráva podobná následujícímu příkladu:

*Entita s názvem 'msdyn\_dualwriteentitymap' s namemapping = 'logický' nebyla nalezena v MetadataCache.*

Chcete-li tento problém vyřešit, zkontrolujte, zda je v aplikaci Dataverse nainstalováno základní řešení dvojího zápisu. Základní řešení duálního zapisování je předpokladem pro sledování řešení.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]