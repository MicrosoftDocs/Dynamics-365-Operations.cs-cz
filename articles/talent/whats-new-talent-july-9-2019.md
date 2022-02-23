---
title: Co je nového nebo co se změnilo v aplikaci Dynamics 365 Talent (9. července 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/09/2019
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
ms.search.validFrom: 2019-07-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: feb39966d98fa7bde9a6bfad26b07fbd224da59b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528022"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-9-2019"></a>Co je nového nebo co se změnilo v aplikaci Dynamics 365 Talent (9. července 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.

### <a name="coming-soon-in-attract"></a>Již brzy v aplikaci Attract

#### <a name="job-approvals-appear-on-the-home-page"></a>Schválení práce se zobrazí na domovské stránce

Schválení se zobrazují v části **Schválení** na řídicím panelu. Schvalovatelé mohou zkontrolovat svá schválení v části **Přiřazeno vám**, která zobrazuje ID práce, pracovní pozici, ostatní schvalovatele a datum přiřazení práce. Uživatelé, kteří odesílají práci ke schválení, mohou revidovat své práce v části **Vyžádáno vámi**, která zobrazuje schvalovatele, kteří musí schválit odeslanou práci.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2374.

### <a name="platform-update-28-for-finance-and-operations"></a>Aktualizace Platform 28 pro Finance and Operations

Další podrobnosti o aktualizaci Platform Update 28 pro Finance and Operations naleznete v tématu [Funkce Preview v aktualizaci Platform Update 28 aplikace Dynamics 365 Finance and Operations (červenec 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-28).

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Podpora vlastních polí entity v Common Data Service 

Následující entity podporují vlastní pole: 

- **Plán fixní kompenzace**
- **Nastavení referenčního bodu kompenzace**
- **Linie nastavení referenčního bodu kompenzace**
- **Kód příjmů mzdy**
- **Mzdové období**
- **Událost fixní kompenzace**
- **Kompenzační mřížka**

Chcete-li zobrazit všechny aktualizované entity v aplikaci Talent:

1. Vyberte **Správa systému**, vyberte **Odkazy**, a pak vyberte **Konfigurace Common data service**.
2. Vyberte rozevírací nabídku **Název entity CDS**. Všechny uvedené entity mají nejnovější verzi. 

###  <a name="full-name-added-to-worker-entity-in-common-data-service"></a>Jméno a příjmení přidané do entity pracovníka v Common Data Service

Pole **Celé jméno** bylo přidáno do entity **Pracovník**.

### <a name="full-time-equivalent-higher-than-10"></a>Ekvivalent plného úvazku vyšší než 1,0

Nyní se zobrazí upozornění v případě, že je pro zaměstnance na plný úvazek na dané pozici zadána hodnota vyšší než 1,0. 

### <a name="a-warning-no-longer-displays-on-the-worker-page-when-there-is-no-future-dated-employment"></a>Na stránce pracovníka se již nezobrazuje upozornění, pokud neexistuje žádné zaměstnání v budoucnu.

Pokud po přechodu na stránku **Pracovník** ze seznamu **Existující zaměstnanci** přejdete z pracovního prostoru **Správa pracovníků**, přestanete dostávat zprávy označující, že existuje budoucí zaměstnání. 

### <a name="unable-to-delete-a-business-process-in-talent"></a>Nelze odstranit obchodní proces v aplikaci Talent

Obchodní procesy nyní můžete odstraňovat v pracovním prostoru **Obchodní procesy**.

### <a name="leave-balance-no-longer-displays-zero-for-plans-with-no-accruals-when-using-balance-as-of-accrual-period"></a>Zůstatek dovolené již v plánech bez časového rozlišení není zobrazen v případě, že je použit zůstatek k období časového rozlišení.

Plány, které jsou nastaveny bez časového rozlišení, mohou nyní zobrazovat zůstatek.

## <a name="in-preview"></a>Náhled

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Funkce Preview jsou povoleny pouze v instancích sandbox.

Když zřizujete novou instanci aplikace Talent, můžete určit, zda je typem instance **Produkce** nebo **Sandbox**. Instance typu **Sandbox** umožňují dřívější testování nových funkcí. Všechny existující instance aplikace Talent budou aktualizovány na typ instance **Produkční**. Chcete-li, aby byla jedna z existujících instancí aktualizována na typ instance **Sandbox**, obraťte se na [podporu](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) a inicializujte požadavek na změnu.

Další informace o tom, jak jsou publikovány změny, naleznete v části [Zřízení aplikace Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="restrict-leave-types-in-time-off-requests"></a>Omezení typů pracovního volna v žádostech o volno

Organizace mohou nabízet mnoho různých typů volna svým zaměstnancům. Pro zaměstnance však nemusí být vhodné odesílat požadavky na volno u některých typů pracovního volna. Tyto typy pracovního volna mohou být namísto toho spravovány oddělením HR. V této verzi můžete konfigurovat, pro které typy pracovního volna mohou zaměstnanci odesílat žádosti o volno. 

## <a name="coming-soon-in-core-hr"></a>Již brzy v Core HR

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Zobrazení rozšířených informací o výkonu v samoobsluze pro manažery

Nová možnost umožní, aby manažeři zobrazili výkon svých přímých podřízených i jejich rozšířených podřízených. V současné době mohou linioví manažeři přiřazovat a aktualizovat cíle výkonnosti a vydávat nové revize, na kterých jejich zaměstnanci spolupracují. Kromě toho mohou přímí manažeři a jejich zaměstnanci udržovat a aktualizovat deníky výkonnosti, aby byl zajištěn plynulý proces kontroly výkonu. Při implementaci této změny budou mít manažeři možnost zobrazit a udržovat informace související s výkonem pro své rozšířené podřízené spolu se svými přímými podřízenými. 

### <a name="entities-supporting-custom-fields"></a>Entity podporující vlastní pole

Pro vlastní pole v aplikaci Common Data Service budou povoleny následující entity: 

- **Typ odchodu**
- **Bankovní účet pracovníka**
- **Pracovní kalendář**
