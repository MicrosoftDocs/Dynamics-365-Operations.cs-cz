---
title: Odebrané nebo zastaralé funkce platformy
description: Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z aktualizací platformy aplikací Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: d394f5ca84efc5beb943d349e45a3d2c9639d83c
ms.sourcegitcommit: 75974ae567bb0eacf0f65cac992b34ce5c680b93
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/03/2020
ms.locfileid: "3095767"
---
# <a name="removed-or-deprecated-platform-features"></a>Odebrané nebo zastaralé funkce platformy

[!include [banner](../includes/banner.md)]

Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z aktualizací platformy aplikací Finance and Operations.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Tento seznam je určen k tomu, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování. 

> [!NOTE]
> Podrobné informace o objektech v aplikacích Finance and Operations lze nalézt v části [Sestavy technických informací](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí aplikací Finance and Operations.

## <a name="platform-update-32"></a>Aktualizace platformy 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Dialogové okno pro změnu požadavku workflowu již neobsahuje rozevírací seznam pro výběr uživatele.
|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Jednalo se o bezpečnostní problém, protože požadavek na změnu mohl být odeslán nežádoucímu uživateli. Šlo také o problém s využitelností, protože aplikace nutila uživatele určit, kdo je původce workflowu, a ručně jej vybrat.  |
| **Nahrazeno jinou funkcí?**   | Ne |
| **Ovlivněné oblasti produktu**         | Workflow |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Rozevírací seznam pro výběr uživatelů byl odebrán z dialogového okna pro změnu požadavku v aktualizaci platformy 32. Požadavky na změnu požadavku budou automaticky odeslány původci, jak bylo zamýšleno. Další informace o této funkci naleznete v tématu [Akce v procesech schválení workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Vložené odkazy na procházení k podrobnostem již nejsou podporovány ve stránkovaných dokumentech vykreslených službou hostovanou v cloudu 
|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Adresy URL pro navigaci vložené do dokumentů vykreslených službou mohou obsahovat citlivé obchodní údaje. Odebíráme podporu vložených odkazů na procházení k podrobnostem coby bezpečnostní opatření pro další ochranu dat zákazníka. V důsledku této změny si uživatelé také užijí lepšího výkonu při interaktivním vytváření dokumentů.  |
| **Nahrazeno jinou funkcí?**   | Žádný |
| **Ovlivněné oblasti produktu**         | Vykazování |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Tato funkce je aktivně odebírána ze služby.<br><br>Moderní klient nabízí řadu možností pro vytváření zobrazení s automaticky generovanými odkazy, které pomáhají při navigaci v aplikaci. Stránkované dokumenty vykreslené službou jsou doporučeny pro externí sdělení, které jsou zasílány e-mailem, archivovány a vytištěny pro příjemce. Zlepšili jsme prostředí pro zobrazení náhledu dokumentů přímo v prohlížeči, které nabízí přímý přístup k místním tiskárnám. Další informace naleznete v tématu [Náhled dokumentů PDF pomocí integrovaného prohlížeče](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Předchozí oznámení o odebraných nebo zastaralých funkcích
Další informace o funkcích, které byly v předchozích verzích odebrány nebo zastaraly, naleznete v tématu [Odebrané nebo zastaralé funkce v předchozích verzích](../migration-upgrade/deprecated-features.md).

