---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Talent (11. června 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
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
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 20dc0768463d9a5d6762cb062deb0bdbe4d53fe3
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528662"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-11-2019"></a>Co je nového a co se změnilo v aplikaci Dynamics 365 Talent (11. června 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

### <a name="search-engine-optimization-for-job-posts"></a>Optimalizace webového vyhledávače pro nabídky volných míst

Po zapnutí **Optimalizace webového vyhledávače** v centru pro správu aplikace Dynamics 365 Talent: Attract informuje aplikace Attract rozhraní API indexování Google, aby zaindexovalo webovou stránku, kdykoliv aktivujete a uveřejníte novou nabídku práce nebo aktualizujete stávající práci. Tato úloha se pak zobrazí ve výsledcích hledání pro Google a další vyhledávače.

Podobně platí, že při zrušení nabídky práce aplikace Attract informuje API indexování, aby se zrušené práce neobjevovaly ve výsledcích hledání.

> [!NOTE]
> Webové nástroje pro indexaci dat nemají definovaný časový rámec pro indexaci webových stránek nebo aktualizaci výsledků hledání.

## <a name="coming-soon-in-attract"></a>Již brzy v aplikaci Attract

### <a name="job-approvals-appear-on-the-home-page"></a>Schválení práce se zobrazí na domovské stránce

Schválení se zobrazují v části **Schválení** na řídicím panelu. Schvalovatelé mohou zkontrolovat svá schválení v části **Přiřazeno vám**, která zobrazuje ID práce, pracovní pozici, ostatní schvalovatele a datum přiřazení práce. Uživatelé, kteří odesílají práci ke schválení, mohou revidovat své práce v části **Vyžádáno vámi**, která zobrazuje schvalovatele, kteří musí schválit odeslanou práci.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2337.

### <a name="platform-update-27-for-finance-and-operations"></a>Aktualizace Platform 27 pro Finance and Operations

Další podrobnosti o aktualizaci Platform Update 27 pro Finance and Operations naleznete v tématu [Funkce Preview v aktualizaci Platform Update 27 aplikace Dynamics 365 Finance and Operations (červen 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).

### <a name="feature-management-workspace-in-talent"></a>Pracovní prostor správy funkcí v aplikaci Talent

Pracovní prostor **Správa funkcí** ve **správě systému** umožňuje prohlížení, povolování, zakazování a plánování funkcí, které byly dodány v jednotlivých vydáních. Ve výchozím nastavení jsou nové funkce vypnuté. Pracovní prostor **Správa funkcí** slouží k jejich zapnutí a zobrazení odpovídající dokumentace.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Podpora entity Common Data Service pro vlastní pole

Entita vydávajícího úřadu nyní podporuje vlastní pole.

### <a name="new-common-data-service-entities"></a>Nové entity Common Data Service

Byla přidána entita skupiny úkolů.

## <a name="in-preview"></a>Náhled

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Funkce Preview budou povoleny pouze v prostředích sandbox.

Další informace o tom, jak jsou publikovány změny, naleznete v části [Zřízení aplikace Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

Když zřizujete novou instanci aplikace Talent, můžete určit, zda je typem instance Produkce nebo Sandbox. Instance typu Sandbox umožňuje dřívější testování nových funkcí. Všechny existující instance aplikace Talent budou aktualizovány na typ instance **Produkční**. Chcete-li, aby byla jedna z existujících instancí aktualizována na typ instance **Sandbox**, obraťte se na [podporu](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) a inicializujte požadavek na změnu.

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Omezení typů pracovního volna v žádostech o volno

Organizace mohou nabízet mnoho typů volna svým zaměstnancům. Pro zaměstnance však nemusí být vhodné odesílat požadavky na volno u některých typů pracovního volna. Tyto typy pracovního volna mohou být namísto toho spravovány oddělením HR. V této verzi můžete konfigurovat, pro které typy pracovního volna mohou zaměstnanci odesílat žádosti o volno. 

## <a name="coming-soon-in-core-hr"></a>Již brzy v Core HR

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a>Zobrazení rozšířených informací o výkonu v samoobsluze pro manažery

Nová možnost umožní, aby manažeři zobrazili výkon svých přímých podřízených i jejich rozšířených podřízených. V současné době mohou linioví manažeři přiřazovat a aktualizovat cíle výkonnosti a vydávat nové revize. Kromě toho mohou přímí manažeři a jejich zaměstnanci udržovat a aktualizovat deníky výkonnosti, aby byl zajištěn plynulý proces kontroly výkonu. Při implementaci této změny budou mít manažeři možnost zobrazit a udržovat informace související s výkonem pro své rozšířené podřízené spolu se svými přímými podřízenými.

### <a name="print-performance-reviews"></a>Tisk kontrol výkonnosti

Zaměstnanci, manažeři a HR budou moci vytisknout hodnocení výkonnosti zaměstnance.
