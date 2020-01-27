---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (29. října 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e2d79ee9e182df4a4efe65beb685567b1e7446ce
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897435"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (29. října 2019)

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2586. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a>Odstranění stran bez rolí by mělo být ve výchozím nastavení zapnuté (371233)

Když zřizujete nové prostředí v aplikaci Talent, je volba **Odstranit strany, pokud neexistují role** ve výchozím nastavení zapnutá. Když odstraníte pracovníka, nebude strana přidružená k pracovníkovi odebrána, pokud není zapnuto toto nastavení. Tato změna omezuje duplicitní záznamy v globálním adresáři, pokud potřebujete importovat, změnit nebo znovu naimportovat pracovníky.

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a>Mělo by být povoleno odstranění rozpracovaných a zrušených žádostí o dovolenou v Common Data Service (376999)

S touto změnou můžete nyní odstranit žádosti o dovolenou ve stavu **Koncept** nebo **Zrušeno** v Common Data Service.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Další hodnoty seznamu ve vlastních polích se neodrazí v Common Data Service po kliknutí na tlačítko Použít ve formuláři vlastních polí (379599)

Přidáte-li nové hodnoty seznamu do existujícího vlastního pole, které již bylo synchronizováno s aplikací Common Data Service, budou nyní k dispozici ve aplikaci Common Data Service po použití změn ve formuláři **Vlastní pole**.

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a>Použít kontrolní seznamy při zprovoznění mezi právnickými osobami, když existuje více zaměstnání (371270)

Ve vydání z tohoto týdne můžete použít kontrolní seznamy pro zaměstnance s více než jedním zaměstnáním ve formuláři **Pracovník > kontrolní seznamy**.

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a>Byla odebrána funkce náhledu zahrnutí otevřených výhod

V souladu s naším oznámením v příspěvku v blogu Strategické investice v [Core HR řídí provozní dokonalost](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) odebrala společnost Microsoft funkci registrace otevření výhod z veřejného náhledu. Místo toho bude v budoucnu vydána nová funkce. Výrobní použití funkce zahrnutí otevřených výhod není podporována.

## <a name="coming-soon"></a>Již brzy

### <a name="print-performance-reviews"></a>Tisk kontrol výkonnosti

Viz [Tisk shrnutí výkonu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) v plánu Dynamics 365: 2019 release wave 2.

### <a name="feature-management-workspace"></a>Pracovní prostor Správa funkcí

Funkce se přidávají a aktualizují v každém vydání. Funkce Správa funkcí poskytuje pracovní prostor, ve kterém si můžete prohlédnout seznam funkcí, které byly dodány v jednotlivých vydáních. Ve výchozím nastavení jsou nové funkce vypnuté. Pracovní prostor slouží k jejich zapnutí a zobrazení odpovídající dokumentace.

Další informace o změnách přicházejících ve správě funkcí naleznete v tématu [Přehled správy funkcí](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
