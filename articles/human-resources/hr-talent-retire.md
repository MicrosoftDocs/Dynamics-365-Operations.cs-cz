---
title: Vyřazení aplikací Dynamics 365 Talent - Attract a Onboard
description: Toto téma popisuje vyřazení aplikací Dynamics 365 Talent - Attract a Onboard.
author: twheeloc
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e17b92621f05ad8483a7c578bfaece58a530df2d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691995"
---
# <a name="dynamics-365-talent-attract-and-onboard-apps-retirement"></a>Vyřazení aplikací Dynamics 365 Talent: Attract - Attract a Onboard


V prosinci 2019 jsme oznámili vyřazení aplikací Dynamics 365 Talent - Attract a Onboard k 1. únoru 2022, což našim zákazníkům dalo dva roky na přípravu.

Další informace o vyřazení těchto aplikací naleznete v části:
 - [Vyřazení aplikací Dynamics 365 Talent - Attract a Dynamics 365 Talent: Onboard](https://community.dynamics.com/365/humanresources/b/dynamics365forhumanresources/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
 - [Budování úspěšnější pracovní síly v aplikaci Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources)

Budeme i nadále podporovat aplikaci Dynamics 365 Human Resources, která našim zákazníkům pomáhá získat informace o pracovní síle potřebné k vytváření pracovního prostředí zaměstnanců založeného na datech v různých oblastech, jako jsou:

- Kompenzace
- Zam. výhody
- Pracovní volno a absence
- Dodržování předpisů
- Payroll
- Zpětná vazba o výkonnosti
- Školení a certifikace
- Samoobslužné programy

## <a name="dynamics-365-talent-apps-retirement-faq"></a>Časté dotazy k vyřazení aplikací Dynamics 365 Talent

### <a name="what-is-the-user-experience-for-both-dynamics-365-talent---attract-and-onboard-apps-starting-february-1-2022"></a>Co mohou uživatelé obou aplikací Dynamics 365 Talent – Attract a Onboard od 1. února 2022 očekávat?

Uživatelé nebudou moci používat aplikace a budou přesměrováni na stránku vyřazení.

### <a name="can-customers-continue-to-export-data-for-both-dynamics-365-talent---attract-and-onboard-apps-after-february-1-2022"></a>Mohou zákazníci po 1. únoru 2022 nadále exportovat data pro obě aplikace Dynamics 365 Talent – Attract a Onboard?
  
Ne, vyřazení bylo oznámeno v prosinci 2019 a požadované exportní kapacity byly poskytnuty do 1. února 2022. 

### <a name="will-the-customers-data-related-to-both-dynamics-365-talent---attract-and-onboard-apps-in-dataverse-be-deleted-after-february-1-2022"></a>Budou se údaje zákazníka související s aplikacemi Dynamics 365 Talent - Attract a Onboard uložené v Dataverse po 1. únoru 2022 odstraněny?

Ne, entity Dataverse zůstanou v prostředí Microsoft Dataverse zákazníka i povyřazení, pokud není řešení Human Capital Management Talent odstraněno nebo odinstalováno.

### <a name="i-know-the-name-of-the-talent-environment-how-can-i-see-the-attract-and-onboard-data-in-dataverse"></a>Znám název prostředí Talent. Jak zobrazím data Attract a Onboard v Dataverse?

1.  Přihlaste se do Power Apps: https://make.powerapps.com
2.  Vyberte prostředí, ve kterém chcete vidět data Attract a Onboard.
3.  Přejděte do nabídky **Dataverse > Tabulky**. 
4.  Zadejte "msdyn_" v poli **Hledat**. Pokud vidíte seznam tabulek začínajících na „msdyn_“ + názvy tabulek (příklad: msdyn_candidate), pak jste našli prostředí s daty Attract a Onboard.

[![Power Apps](./media/Powerapps.png)](./media/Powerapps.png)

### <a name="i-dont-know-the-name-of-the-talent-environment-how-can-i-find-the-environment-that-has-the-data-for-the-dynamics-365-talent-attract-and-dynamics-365-talent-onboard-applications"></a>Neznám název prostředí Talent. Jak mohu najít prostředí, které má data pro aplikace Dynamics 365 Talent: Attract a Dynamics 365 Talent: Onboard?

1)  Přihlaste se do centra pro správu Power Platform: https://admin.powerplatform.microsoft.com/
2)  Vyberte **Prostředí**.
3)  Vyberte určité prostředí, které bude vyhodnoceno.
4)  Vyberte položku **Zdroje > Aplikace Dynamics 365**.
5)  Pokud vidíte nainstalované řešení **Talent HCM**, toto prostředí by mělo obsahovat data Attract a Onboard. 

[![Power Platform](./media/HCMTalent.png)](./media/HCMTalent.png)

> [!NOTE] 
> Řešení **Talent HCM** se také používá v Dynamics 365 Human Resources.
