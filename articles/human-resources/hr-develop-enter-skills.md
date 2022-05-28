---
title: Zadejte dovednosti
description: Práce a manažeři mohou zadávat dovednosti v Dynamics 365 Human Resources.
author: twheeloc
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 32f08fa45c023c587d89623a12f101f50ef4a5fb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692996"
---
# <a name="enter-skills"></a>Zadejte dovednosti

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Můžete zadat cílové dovednosti, nebo skutečné dovedností zaměstnanců, uchazečů nebo kontaktů v Dynamics 365 Human Resources. Cílové dovednosti jsou dovednosti, kterých se osoba chystá dosáhnout. Skutečná dovednost je dovednost, kterou pracovník aktuálně disponuje.

## <a name="create-a-workflow-to-auto-approve-skills"></a>Vytvořte pracovní postup pro automatické schvalování dovedností

Chcete-li zadat dovednosti bez nutnosti schválení, musíte vytvořit pracovní tok, který dovednosti automaticky schválí.

> [!NOTE]
> Dovednosti zadávané pracovníky vždy vyžadují souhlas vedoucího. Tento pracovní postup pouze automaticky schvaluje dovednosti zadané manažery jménem jejich pracovníků.

1. V pracovním prostoru **Správa zaměstnanců** vyberte kartu **Odkazy**.

2. V části **Nastavení** vyberte **Workflowy lidských zdrojů**.

3. Zvolte **Nové**.

4. V podokně **Vytvořit pracovní postup** vyberte **Dovednosti pracovníků**.

   [![Vyberte pracovní postup Dovednosti pracovníků.](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)

5. V dialogovém okně **Otevřít tento soubor?** vyberte **Otevřít**. Po výzvě zadejte své přihlašovací údaje.

6. V editoru pracovního postupu vyberte prvek pracovního toku **Schvánit dovednosti** a přetáhněte jej na plátno.

   [![Vyberte prvek pracovního postupu Schválit dovednosti.](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)

7. Připojte prvek **Start** k prvku **Schválit dovednosti 1** a poté připojte prvek **Schválit dovednosti 1** k prvku **Konec**. Možná se budete muset posunout dolů, abyste viděli prvek **Konec**. Můžete jej přetáhnout blíže k ostatním prvkům.

   [![Prvky propojit pracovní postupy.](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)

8. Poklepejte na prvek pracovního postupu **Schválit dovednosti 1** a poté klepněte pravým tlačítkem na prvek **Krok 1**. Klepněte pravým tlačítkem na prvek **Krok 1** a poté vyberte **Vlastnosti**.

9. V okně **Vlastnosti** vyberte **Podmínka** na levé navigační liště.

10. Vyberte **Provést tento krok pouze v případě, že je splněna následující podmínka**.

11. Vyberte **Přidat podmínku**. Po **Kde** vyberte **Dovednosti v samoobsluze zaměstnanců** a potom vyberte **Dovednosti samoobsluhy zaměstnanců. Osoba**. Po **je** vyberte **pole** a potom vyberte **Vztah mezi uživatelem a osobou**.

    [![Uveďte podmínku.](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)

12. Vyberte **Úkol** na levé navigační liště.

13. Na kartě **Typ přiřazení** vyberte **Hierarchie**.

14. Na kartě **Výběr hierarchie** v poli **Typ hierarchie:** vyberte **Manažerská hierarchie**.

    [![Určete manažerskou hierarchii.](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)

15. Vyberte **Zavřít**, vyberte **Pracovní postup** v popisu cesty k plátnu a poté vyberte **Uložit a zavřít**.

Další informace o vytváření pracovních postupů naleznete v tématu [Přehled systému workflow](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json)

## <a name="enter-skills-for-a-worker"></a>Zadejte dovednosti pro pracovníka

1. Vyberte pracovníka.

2. Na panelu akcí na stránce **Pracovník** vyberte **Osoba** a potom vyberte **Dovednosti**.

3. Na stránce **Dovednosti** vyplňte následující pole pro každou dovednost:

   - **Dovednost**: Vyberte dovednost.
   - **Typ úrovně**: Vyberte **Aktuální** pro dovednost, kterou pracovník již má, nebo vyberte **Cílová** pro dovednost, na které pracovník pracuje.
   - **Úroveň**: Vyberte úroveň pro dovednosti pracovníka.
   - **Datum dovednosti**: vyberte datum v nástroji kalendář.
   - **Zkoušející**: Je-li to vhodné, vyberte zkoušejícího ze seznamu. Můžete filtrovat vyhledávání.
   - **Roky zkušeností**: Zadejte roky zkušeností.
   - **Ověřeno**: Pokud je dovednost ověřena, zaškrtněte políčko.
   - **Ověřil**: Zadejte název ověřovatele.

4. Až zadáte dovednosti, vyberte **Uložit**.

## <a name="see-also"></a>Viz také

[Nakonfigurujte dovednosti](hr-develop-skills.md)<br>
[Mapové dovednosti](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
