---
title: Aplikace Human Resources v Teams
description: V tomto tématu se seznámíte s aplikací Microsoft Dynamics 365 Human Resources v aplikaci Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
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
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 423ec36a73e8af9d915c5cfe16bd4d552448e2b6
ms.sourcegitcommit: d1541831d556b722a71aed442043ffb4a4576d87
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/20/2020
ms.locfileid: "3388109"
---
# <a name="human-resources-app-in-teams"></a>Aplikace Human Resources v Teams

[!include [banner](includes/preview-feature.md)]

Aplikace Microsoft Dynamics 365 Human Resources v aplikaci Microsoft Teams umožňuje zaměstnancům rychle požádat o volno a zobrazit informace o jejich zůstatku volna v Microsoft Teams. Zaměstnanci mohou komunikovat s robotem a vyžádat si informace. Karta **Volno** poskytuje podrobnější informace.

![Robot aplikace pracovního volna Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![Karta volna aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a>Instalace a nastavení

Aplikaci Human Resources najdete v obchodě Teams. Informace o instalaci aplikace Teams najdete v části [Správa žádostí o dovolenou v aplikaci Teams](hr-teams-leave-app.md).

Informace o správě oprávnění k aplikaci v Teams naleznete v části [Správa zásad povolení k aplikaci v Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="known-issues"></a>Známé problémy

| Výdej | Stav |
| --- | --- |
| Zůstatek je nesprávný při zadávání volna pro budoucí datum. | Prognózy ještě nejsou k dispozici. Zůstatek se zobrazuje pro aktuální datum. |
| Při snižování počtu hodin obsažených ve stávající žádosti **Zůstatek účtu** klesá místo aby stoupal. | Budeme řešit tento známý problém v budoucnosti. Zobrazení je nesprávné, ale správná množství jsou upravena po odeslání. |
| Pro stejná data se zobrazují dvě karty **Nadcházející volno**. | Karty představují jednotlivá odeslání. Budeme i nadále brát v potaz zpětnou vazbu a provádět úpravy. |
| Nelze zrušit požadavek ve stavu **Probíhá kontrola**. | Tato funkce není momentálně podporována a bude přidána v budoucím vydání. |
| Informace o zůstatku se počítají od dnešního dne. | Systém aktuálně nezobrazuje zůstatky od období časového rozlišení, i když je nakonfigurováno v parametrech pracovního volna a absence. |

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů

S robotem Dynamics 365 Human Resources v aplikaci Microsoft Teams jsou textové vstupy uživatele analyzovány pro porozumění základním dotazům/záměrům. Vstup uživatele, například „Vyhledat účet Contoso“, je přesměrován na jednu ze služeb Cognitive Services společnosti Microsoft nazvanou Language Understanding Intelligent Service (LUIS). Přečtěte si více o LUIS  [zde](https://www.luis.ai/). Služba LUIS ujasňuje nebo chápe záměr vstupu uživatele (v tomto případě je záměrem najít informace) a cílovou entitu (v tomto případě je zamýšlenou entitou účet s názvem Contoso). Tyto informace jsou poté předány do  [rámce robota Azure](https://azure.microsoft.com/services/bot-service/)  společnosti Microsoft, který interaguje s daty z Dynamics 365 Human Resources a načte požadované informace pro uživatelský dotaz. 

Instalací a umožněním přístupu k používání robota souhlasíte s tím, že umožníte službě LUIS a rámci robota Azure zpracovat záměr za vstupem, což má za následek vylepšenou konverzační uživatelskou zkušenost. Služba LUIS a rámec robota Azure mohou mít ve srovnání s Dynamics 365 Human Resources různé úrovně shody. Zatímco služba LUIS má přístup pouze k uživatelským dotazům a není určena k připojení k datům nebo účtu uživatele Dynamics 365 Human Resources, uživatel robota Dynamics 365 Human Resources může dobrovolně zadat dotaz obsahující zákaznická data, osobní údaje nebo jiná data a takový obsah dotazu by mohl být zaslán do služby LUIS a do rámce robota Azure. 

Obsah dotazů a zpráv uživatele je v systému LUIS uchováván maximálně 30 dní, je šifrován a nepoužívá se pro školení ani zlepšení služeb. Přečtěte si více o Cognitive Services  [zde](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Chcete-li spravovat nastavení administrátora pro aplikace v Microsoft Teams, přejděte do [centra pro správu Microsoft Teams](https://admin.teams.microsoft.com/). 

## <a name="see-also"></a>Viz také 

[Stažení a instalace aplikace Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Centrum nápovědy Microsoft Teams](https://support.office.com/teams)</br>
[Správa žádostí o dovolenou v aplikaci Teams](hr-teams-leave-app.md)

