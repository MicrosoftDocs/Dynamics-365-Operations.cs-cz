---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Talent (25. června 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2019
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
ms.search.validFrom: 2019-06-25
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 56fadba6dc085f849953aa88cf28a2c83e265f40
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009023"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-25-2019"></a>Co je nového a co se změnilo v aplikaci Dynamics 365 Talent (25. června 2019)

[!include [banner](includes/banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>Již brzy v aplikaci Attract

### <a name="job-approvals-appear-on-the-home-page"></a>Schválení práce se zobrazí na domovské stránce

Schválení se zobrazují v části **Schválení** na řídicím panelu. Schvalovatelé mohou zkontrolovat svá schválení v části **Přiřazeno vám**, která zobrazuje ID práce, pracovní pozici, ostatní schvalovatele a datum přiřazení práce. Uživatelé, kteří odesílají práci ke schválení, mohou revidovat své práce v části **Vyžádáno vámi**, která zobrazuje schvalovatele, kteří musí schválit odeslanou práci.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard
Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2357.

### <a name="incorrect-value-displayed-for-primary-position-314266"></a>Pro primární pozici je zobrazena nesprávná hodnota (314266)

Tyto změny budou konzistentně zobrazovat nastavení **Primární pozice** na všech stránkách.

### <a name="cant-edit-after-recalling-the-workflow-in-review-318180"></a>Nelze upravit po odvolání workflow v revizi (318180)

Revize, které byly odvolány prostřednictvím workflow, lze nyní upravit.

### <a name="final-comments-field-in-reviews-isnt-translated-325921"></a>Pole konečných komentářů v revizích není přeloženo (325921).

Popisek **konečných komentářů** bude v aplikaci Talent přeložen.

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a>Funkce Preview budou povoleny pouze v prostředích sandbox.

Když zřizujete novou instanci aplikace Talent, můžete určit, zda je typem instance **Produkce** nebo **Sandbox**. Instance typu **Sandbox** umožňuje dřívější testování nových funkcí. Všechny existující instance aplikace Talent budou aktualizovány na typ instance **Produkční**. Chcete-li, aby byla jedna z existujících instancí aktualizována na typ instance **Sandbox**, obraťte se na [podporu](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) a inicializujte požadavek na změnu.

Další informace o tom, jak jsou publikovány změny, naleznete v části [Zřízení aplikace Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

## <a name="in-preview"></a>Náhled

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Omezení typů pracovního volna v žádostech o volno

Organizace mohou nabízet mnoho typů volna svým zaměstnancům. Pro zaměstnance však nemusí být vhodné odesílat požadavky na volno u některých typů pracovního volna. Tyto typy pracovního volna mohou být namísto toho spravovány oddělením HR. V této verzi můžete konfigurovat, pro které typy pracovního volna mohou zaměstnanci odesílat žádosti o volno. 

## <a name="coming-soon-in-core-hr"></a>Již brzy v Core HR

### <a name="feature-management-area-in-talent"></a>Oblast správy funkcí v aplikaci Talent

**Správa funkcí** bude z **správy systému** odebrána z důvodu problémů s touto funkcí. **Správu funkcí** znovu zavedeme v budoucím vydání. 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Podpora entity Common Data Service pro vlastní pole

Následující entity budou podporovat vlastní pole: **Kód příjmů mzdy**, **Událost fixní kompenzace**, **Kompenzační mřížka**, **Mzdové období** a **Referenční bod kompenzace**. 

### <a name="new-common-data-service-entities"></a>Nové entity Common Data Service

Entita **Kódy důvodu** bude přidána do Common Data Service.

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>Zobrazení informací o výkonu pro přímé a rozšířené podřízené v samoobsluze pro manažery

Nová možnost umožní, aby manažeři zobrazili výkon svých přímých podřízených i jejich rozšířených podřízených. V současné době mohou linioví manažeři přiřazovat a aktualizovat cíle výkonnosti a vydávat nové revize. Kromě toho mohou přímí manažeři a jejich zaměstnanci udržovat a aktualizovat deníky výkonnosti, aby byl zajištěn plynulý proces kontroly výkonu. Při implementaci této změny budou mít manažeři možnost zobrazit a udržovat informace související s výkonem pro své rozšířené podřízené spolu se svými přímými podřízenými.

### <a name="print-performance-reviews"></a>Tisk kontrol výkonnosti

Zaměstnanci, manažeři a HR budou moci vytisknout hodnocení výkonnosti zaměstnance.
