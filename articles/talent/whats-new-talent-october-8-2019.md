---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (8. října 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/08/2019
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
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 40898ca7f54089337180def964b8942e8653663b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529473"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-8-2019"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (8. října 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2542. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).

### <a name="removal-of-benefits-open-enrollment-from-public-preview"></a>Odebrání registrace otevřených výhod z veřejného náhledu

V souladu s naším oznámením v příspěvku v blogu Strategické investice v [Core HR řídí provozní dokonalost](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence/) odebírá společnost Microsoft 18. října 2019 funkci registrace otevření výhod z veřejného náhledu. Místo toho bude v budoucnu vydána nová funkce. Produkční použití funkce pro registrace výhod, která je aktuálně ve veřejném náhledu, není podporováno. 

### <a name="common-data-service-integration-is-now-turned-off-by-default-on-new-provisions-343675"></a>Integrace Common Data Service je nyní ve výchozím nastavení vypnutá pro nová zřizování (343675)
 
Pokud jsou zřízena nová prostředí, integrace s Common Data Service je nyní vypnutá. Další informace naleznete v tématu [Konfigurace integrace Common Data Service](hr-common-data-service-integration.md).

### <a name="streamlined-employee-entry-and-navigation"></a>Zjednodušené zadávání zaměstnance a navigace

Funkce pro položku a navigaci zaměstnanců jsou nyní k dispozici ve všech prostředích. Chcete-li tuto funkci zapnout, přejděte na **Správa systému \> Odkazy \> Nastavení \> Systémové parametry \> Funkce náhledu** a vyberte **Rozšířený formulář a navigace pracovníka**. Tato funkce je poté zapnutá pro všechny uživatele. Tuto možnost můžete kdykoli vypnout.

Další informace naleznete v tématu [zjednodušené zadávání údajů o zaměstnancích](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/streamlined-employee-data-entry) v plánu Dynamics 365:2019 Release Wave 2.

### <a name="attract-and-onboard-create-inactive-workers-in-core-hr-380517"></a>Aplikace Attract a Onboard vytvářejí neaktivní pracovníky v Core HR (380517)

Vydání tohoto týdne opravuje problém, kdy aplikace Attract a Onboard vytvářejí neaktivní pracovníky v Core HR.

### <a name="the-workflow-fails-when-the-manager-is-signed-in-to-another-company-while-terminating-an-employee-346852"></a>Workflow se nezdaří, pokud je manažer přihlášen k jiné společnosti při výpovědi zaměstnanci (346852)

Workflow již nefunguje na základě právnické osoby, ke které je přihlášený manažer.

### <a name="missing-information-on-hcmonboardingworkerchecklisttaskentity-349591"></a>Chybějící informace v HcmOnboardingWorkerChecklistTaskEntity (349591)

Tato verze obsahuje další informace o **HcmOnboardingWorkerChecklistTaskEntity**. Několik příkladů:

- **Název skupiny**, když je přiřazený typ **skupina**
- **Jméno zaměstnance**, když je přiřazený typ **zaměstnanec**
- **Jméno manažera**, když je přiřazený typ **manažer**

### <a name="entities-arent-listed-in-alphabetical-order-in-common-data-service-administration-377414"></a>Entity nejsou uvedeny v abecedním pořadí ve správě Common Data Service (377414)

Problém: Entity jsou nyní uvedeny v abecedním pořadí na stránce **Správa CDS**.

### <a name="changing-the-employment-type-with-a-future-date-doesnt-allow-a-position-assignment-339958"></a>Změna typu zaměstnání s budoucím datem neumožňuje přiřazení pozice (339958).

Tato změna umožňuje přiřazení pozice při změně typů pracovníků (například z zaměstnance na dodavatele).

### <a name="updating-the-common-data-service-leave-bank-transaction-entity-creates-a-new-record-in-talent-352938"></a>Aktualizace entity Opustit bankovní transakci Common Data Service vytvoří nový záznam v aplikaci Talent (352938).

Transakce opuštění je nyní aktualizována, když je provedena aktualizace Common Data Service pro zanechané bankovní transakce.

### <a name="the-title-of-attachments-for-feedback-items-shows-the-feedback-description-343765"></a>Název příloh pro položky zpětné vazby zobrazuje popis zpětné vazby (343765).

Popis zpětné vazby se již v názvu přílohy nezobrazuje.

### <a name="compensation-workflow-comments-field-shows-incorrect-content-339297"></a>Pole Komentáře workflowu kompenzace zobrazuje nesprávný obsah (339297).

Tato změna zobrazí obsah pole **%HcmActionState.HcmWorkerActionComment.Comments%**.

### <a name="workcalendarentity-and-workcalendardayentity-arent-exposed-through-odata-376329"></a>WorkCalendarEntity a WorkCalendarDayEntity nejsou zveřejněny prostřednictvím OData (376329)

V této verzi jsou **WorkCalendarEntity** a **WorkCalendarDayEntity** nyní k dispozici prostřednictvím Open Data Protocol (OData).

### <a name="hcmworkerentity-is-slow-when-odata-is-used-375221"></a>HCMWorkerEntity je pomalá při použití OData (375221).

Změny zlepšují výkon **HCMWorkerEntity** při použití návrháře sešitu Microsoft Excel.

### <a name="manager-performance-journal-entry-shows-an-error-after-deleting-a-performance-journal-and-creating-a-new-one-336061"></a>Položka deníku výkonnosti správce zobrazuje chybu po odstranění deníku výkonnosti a vytvoření nového (336061)

Tato verze opravuje problém, ke kterému dojde po odstranění jednoho deníku výkonnosti a následném okamžitém vytvoření nového. Tato oprava mění chování samoobslužné služby manažera.

## <a name="coming-soon"></a>Již brzy

### <a name="print-performance-reviews"></a>Tisk kontrol výkonnosti

Viz [Tisk shrnutí výkonu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) v plánu Dynamics 365: 2019 release wave 2.


[!INCLUDE[footer-include](../includes/footer-banner.md)]