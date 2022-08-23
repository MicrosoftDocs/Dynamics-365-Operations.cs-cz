---
title: Odstraňování problémů s rozšířením Store Commerce
description: Tento článek vysvětluje, jak řešit problémy s rozšířením v aplikaci Microsoft Dynamics 365 Commerce Store Commerce.
author: josaw1
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1a2d6a68b7556d8b4d05529efd90f9e66f0c5925
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269774"
---
# <a name="troubleshoot-store-commerce-extension-issues"></a>Odstraňování problémů s rozšířením Store Commerce

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak řešit problémy s rozšířením v aplikaci Microsoft Dynamics 365 Commerce Store Commerce.

## <a name="extensions-packages-arent-loaded"></a>Balíčky rozšíření se nenačtou

### <a name="extensions-packages-dont-appear-on-the-pos--settings-page"></a>Balíčky rozšíření se na nezobrazují na stránce POS \> Nastavení

Triggery Commerce Runtime (CRT) možná nebyly aktualizovány tak, aby zahrnovaly balíček rozšíření, nebo nejsou nasazeny. Více informací viz [Rozšířitelnost a triggery Commerce Runtime (CRT)](../dev-itpro/commerce-runtime-extensibility-trigger.md).

### <a name="extensions-packages-appear-on-the-pos--settings-page-but-the-manifest-isnt-loaded"></a>Balíčky rozšíření se objeví na stránce POS \> Nastavení, ale manifest se nenačte

Potvrďte, že balíčky rozšíření existují ve složce **C:\\Program Files\\Microsoft Dynamics 365\\10.0\\Store Commerce\\Extensions**. Pokud balíčky existují, měla by tam být složka **POS**, která obsahuje manifest.

Pokud složka **POS** neexistuje, potvrďte, že projekt Store Commerce správně odkazuje na projekt rozšíření místa prodeje (POS). Ověřte referenční cestu projektu a ujistěte se, že existuje. 

Na následujícím příkladu má projekt instalačního programu problémy s odkazovaným projektem rozšíření.

![Referenční projekt instalačního programu Store Commerce není platný.](media/ReferenceNotValid.png)

Pokud je reference na projekt rozšíření správně přidána, nedojde k žádnému varování nebo problému se závislostí v projektu instalačního programu, jak ukazuje následující příklad.

![Referenční projekt instalačního programu Store Commerce je platný.](media/ReferenceValid.png)
