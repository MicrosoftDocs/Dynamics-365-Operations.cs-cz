---
title: Vyzkoušejte jednotky škálování v distribuované hybridní topologii
description: Toto téma poskytuje informace o tom, jak vyzkoušet cloudové a hraniční jednotky škálování u pracovních zatížení výroby a správy skladu.
author: perlynne
ms.date: 03/03/2022
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-03-03
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 04fd79f3c582ae9ac51882f73410477efaa35496
ms.sourcegitcommit: b52ff5dfd32580121f74a5f262e5c2495e39d578
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/03/2022
ms.locfileid: "8376239"
---
# <a name="try-out-scale-units-in-a-distributed-hybrid-topology"></a>Vyzkoušejte jednotky škálování v distribuované hybridní topologii

[!include [banner](../includes/banner.md)]

Proces vyzkoušení distribuované hybridní topologie je jednoduchý. Během první fáze byste měli ověřit přizpůsobení, abyste se ujistili, že fungují v distribuované topologii. Máte dvě možnosti.

## <a name="option-1-evaluate-customizations-in-development-environments"></a>Možnost 1: Vyhodnoťte přizpůsobení v samostatných vývojových prostředích

Než začnete zprovozňovat prostředí sandbox, doporučujeme vám prozkoumat jednotky škálování v nastavení vývoje, jako je samostatné prostředí (označované také jako prostředí úrovně 1), abyste mohli ověřovat procesy, přizpůsobení a řešení. Během této fáze budou data a přizpůsobení aplikována na samostatné prostředí. Můžete vše spouštět v jediném prostředí, které může převzít roli podnikového centra i škálovací jednotky. Alternativně můžete mít dvě vývojová prostředí, z nichž jedno přebírá roli centra a druhé roli škálovací jednotky. Toto nastavení poskytuje nejlepší způsob, jak identifikovat a opravit problémy. K dokončení této fáze lze také použít nejnovější [sestavení předčasného přístupu (PEAP)](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxURUFWTjQzTzg0UUk5RkJHMDFEMVlSSDFEQy4u).

Pro instalaci a správu prostředí byste měli použít [nástroje nasazení jednotek škálování pro samostatná vývojová prostředí](https://github.com/microsoft/SCMScaleUnitDevTools). Tyto nástroje umožňují konfigurovat centrum a jednotky škálování v jednom nebo dvou oddělených samostatných prostředích. Nástroje jsou poskytovány jako binární verze i jako zdrojový kód na GitHubu. Prostudujte si projekt wiki, který obsahuje [Průvodce používáním krok za krokem](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide), který popisuje, jak se nástroje používají. Pokud [nasazujete jednotky škálování hraniční sítě na vlastní hardware pomocí místních obchodních dat (LBD)](cloud-edge-edge-scale-units-lbd.md), musíte postupovat jiným způsobem.

## <a name="option-2-acquire-add-ins-and-deploy-in-your-sandbox-environments"></a>Možnost 2: Získejte doplňky a nasaďte je v prostředích sandbox

Chcete-li vyzkoušet distribuovanou hybridní topologii, musíte mít dvě prostředí sandbox (vrstva 2), z nichž jedno obsahuje vaše data (podnikové centrum) a druhé je určeno pro škálovací jednotku a obsahuje „prázdná data“.

Musíte získat doplňky pro alespoň jednu cloudovou nebo hraniční škálovací jednotku. Poté budou přiděleny odpovídající sloty pro projekt a prostředí ve službách [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), takže prostředí škálovací jednotky lze nasadit pomocí [portálu správce jednotky škálování](https://aka.ms/SCMSUM).

Obraťte se na podporu společnosti Microsoft a požádejte o povolení prostředí sandbox.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
