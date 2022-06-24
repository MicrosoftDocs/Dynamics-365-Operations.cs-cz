---
title: Poradce při potížích souvisejících s připraveností řešení
description: Tento článek obsahuje informace o řešení potíží, které vám pomohou vyřešit problémy s připraveností řešení.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c280eef995664c640e382817dda9d6e1cde154c6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871488"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Poradce při potížích souvisejících s připraveností řešení

[!include [banner](../../includes/banner.md)]





Tento článek obsahuje informace o odstraňování potíží pro integrací dvojitého zápisu mezi aplikacemi Finance a Operace a Dataverse. Konkrétně obsahuje informace, které vám pomohou vyřešit problémy s připraveností řešení.

> [!IMPORTANT]
> Některé problémy, které tento článek řeší, mohou vyžadovat buď roli správce systému, nebo pověření správce klienta Microsoft Azure Active Directory (Azure AD). Oddíl pro každý výdej vysvětluje, zda jsou vyžadovány určité role nebo pověření.

## <a name="error-on-the-dual-write-page"></a>Chyba na stránce dvojího zápisu

Na stránce **Dvojího zápisu** se může zobrazit chybová zpráva podobná následujícímu příkladu:

*Entita s názvem 'msdyn\_dualwriteentitymap' s namemapping = 'logický' nebyla nalezena v MetadataCache.*

Chcete-li tento problém vyřešit, zkontrolujte, zda je v aplikaci Dataverse nainstalováno základní řešení dvojího zápisu. Základní řešení duálního zapisování je předpokladem pro sledování řešení.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]