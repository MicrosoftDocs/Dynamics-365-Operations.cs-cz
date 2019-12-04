---
title: Integrace se službou LinkedIn - Často kladené dotazy
description: Toto téma obsahuje odpovědi na otázky, které můžete mít v souvislosti s integrací LinkedIn a Microsoft Dynamics 365 Talent - Attract.
author: hasrivas
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 35428da709f480e1d3842b7e92deacba200326ee
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833085"
---
# <a name="linkedin-integration-faq"></a>Integrace se službou LinkedIn - Často kladené dotazy

[!include [banner](includes/banner.md)]

LinkedIn je největší světová síť profesionálů. Microsoft Dynamics Talent: Attract se integruje s LinkedIn, aby vám umožnil přístup k nejlepším světovým talentům. Attract vám umožní publikovaat pracovní nabídky přímo na LinkedIn a zároveň vám umožňuje získávat informace o uchazečích z LinkedIn do aplikace Attract.

## <a name="for-recruiters-and-hiring-managers"></a>Pro pracovníky a manažery náboru

V tomto tématu naleznete odpovědi na nejčastější dotazy týkající se společného použití Attract a LinkedIn.

### <a name="what-linkedin-features-do-i-get-with-attract"></a>Jaké funkce LinkedIn mohu v aplikaci Attract získat?

Integrace aplikace Attract s LinkedIn umožňuje provádět následující úlohy:

- [Publikovat práce na LinkedIn](./attract-post-jobs-to-linkedin.md) (jako Omezené seznamy zdarma).
- [Zdrojování kandidátů pomocí LinkedIn Recruiter v aplikaci Microsoft Dynamics 365 Talent - Attract](./attract-linkedin-recruiter.md#export-linkedin-candidates-to-attract-with-one-click).
- [Nastavení integrace s řešením LinkedIn pro aplikaci Microsoft Dynamics 365 Talent - Attract](./attract-admin-linkedin.md#set-up-apply-with-linkedin-in-attract).

### <a name="what-do-i-need-before-i-can-post-jobs-to-linkedin"></a>Co potřebuji, než budu moci odeslat úlohy na LinkedIn?

Váš správce musí [konfigurovat integraci LinkedIn v Attract](./attract-admin-linkedin.md#configure-job-posting-to-linkedin). Potom můžete začít!

### <a name="how-do-i-post-jobs-to-linkedin-from-attract"></a>Jak publikovat pracovní místa na LinkedIn z aplikace Attract?

Po vytvoření práce v Attract je nutné vybrat tlačítko **Publikovat nyní**, které odesílá do LinkedIn. Další informace naleznete v tématu [Publikování pracovních míst na LinkedIn z Microsoft Dynamics 365 Talent - Attract](./attract-post-jobs-to-linkedin.md#post-jobs-to-linkedin).

### <a name="can-i-get-candidate-information-from-linkedin-into-attract"></a>Mohu získat informace o kandidátech z LinkedIn do Attract?

Ano. Pokud najdete na LinkedIn vhodného kandidáta, můžete snadno exportovat informace o tomto kandidátovi do aplikace Attract. Další informace naleznete v tématu [Zazdrojování kandidátů s LinkedIn Recruiter v aplikaci Microsoft Dynamics 365 Talent - Attract](attract-linkedin-recruiter.md).

### <a name="how-can-i-get-help-accessing-linkedin-from-attract"></a>Jak lze získat pomoc s přístupem do LinkedIn z aplikace Attract?

Pokud máte potíže s přihlášením nebo publikováním prací na LinkedIn z aplikace Attract, nahlédněte do části [Odstraňování problémů s integrací s LinkedIn a aplikací Microsoft Dynamics 365 Talent - Attract](./attract-troubleshoot-linkedin.md).

Další informace o potížích s Attract naleznete v tématu [Získání podpory pro Microsoft Dynamics 365 Talent](./talent-support.md). Nápovědu ke LinkedIn naleznete na [Stránce podpory LinkedIn](https://www.linkedin.com/help).

## <a name="for-admins-and-developers"></a>Pro správcce a vývojáře

V tomto tématu naleznete odpovědi na nejčastější dotazy týkající konfigurace integrace mezi Attract a LinkedIn.

### <a name="how-do-i-configure-attract-so-that-recruiters-and-hiring-managers-can-post-jobs-to-linkedin"></a>Jak lze konfigurovat Attract, aby náboroví pracovníci a manažeři mohli publikovat pracovní nabídky na LinkedIn?

Dostupné možnosti lze konfigurovat na kartě **Integrace LinkedIn** v centru pro správu. Další informace naleznete v tématu [Nastavení integrace s LinkedIn pro Microsoft Dynamics 365 Talent - Attract](./attract-admin-linkedin.md).

### <a name="can-i-export-candidate-information-from-linkedin"></a>Mohu exportovat informace o kandidátech z LinkedIn?

Ano, ale nejprve je nutné konfigurovat integraci s aplikací LinkedIn Recruiter. Další informace naleznete v tématu [Nastavení integrace s LinkedIn pro Microsoft Dynamics 365 Talent - Attract](./attract-admin-linkedin.md).

### <a name="how-can-i-post-jobs-to-premium-job-slots-on-linkedin"></a>Jak lze na LinkedIn publikovat nabídky práce do prémiových nabídek volných míst?

I když Attract poskytuje výkonné řešení pro publikování nabídek práce na LinkedIn, může se stát, že budete potřebovat další flexibilitu. Můžete například chtít, aby se nad rámec omezených seznamů zdarma publikovaly nabídky do prémiových nabídek volných míst, nebo můžete chtít, aby LinkedIn zpracovával vaše dávkové úlohy více než jednou denně.

#### <a name="types-of-linkedin-job-posts"></a>Typy zobrazení volných míst v LinkedIn

LinkedIn nabízí následující typy zobrazení volných míst:

- **Omezený výpis** – bezplatná zobrazení pracovních míst, která se zobrazí ve výsledcích hledání, když kandidáti hledají úlohy na LinkedIn a na LinkedInové stránce společnosti. Omezený výpis je určen aktivním žadatelům o zaměstnání. Tento typ výpisu představuje typ, který Attract poskytuje na LinkedIn. Omezený výpis nelze na LinkedIn nijak propagovat. Chcete-li propagovat omezené výpisy, je nutné pracovat s LinkedIn a povolit sbalení pracovní nabídky. Další informace o sbalení pracovní nabídky naleznete v tématu [Omezené výpisy vs prémiové nabídky práce pro sbalení pracovní nabídky](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping) a [Sbalení pracovní nabídky – často kladéné dotazy](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions).
- **Prémiové nabídky volných pozic** – zakoupená zobrazení pozic, které se zobrazí na různých místech v rámci LinkedIn, jako je například informační kanál LinkedIn, e-maily a **Nabídky práce, které mohou být pro vás zajímavé**. Prémiové nabídky volných pozic jsou určeny pasivním kandidátům, ale zobrazují se také ve vyhledáváních volných míst.

Attract publikuje práce na LinkedIn jako Omezené záznamy. Chcete-li použít prémiové nabídky volných míst, musíte použít sbalení pracovní nabídky pomocí LinkedIn Recruiter. Sbalení pracovní nabídky vyžaduje smlouvu o sbalení pracovní nabídky s LinkedIn. Další informace získáte v části [Sbalení pracovní nabídky prostřednictvím LinkedIn Recruiter – přehled](https://www.linkedin.com/help/recruiter/answer/79037).

#### <a name="frequency-of-batch-processing-on-linkedin"></a>Frekvence dávkového zpracování na LinkedIn

Aplikace LinkedIn zpracuje pracovní nabídky v dávce pomocí Attract jednou za den. Proto může až 48 hodin, aby se úlohy na LinkedIn objevily po jejich odeslání pomocí aplikace. Pokud potřebujete, aby se úlohy zobrazovaly na LinkedIn dříve, nebo pokud potřebujete další flexibilitu, můžete použít rozhraní API Recruiter System Connect z LinkedIn. Další informace naleznete v tématu [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect).

#### <a name="table-of-options-for-job-posting-to-linkedin"></a>Tabulka možností pro odeslání práce do LinkedIn

V následující tabulce jsou popsány různé možnosti pro publikování volných míst na LinkedIn. Obsahuje výhody jednotlivých možností a další informace.

|  | Attract | Sbalení pracovní nabídky prostřednictvím LinkedIn Recruiter | Recruiter System Connect API |
|---|---|---|---|
| **Popis** | Attract publikuje práce na LinkedIn jako kanál XML. | Společnost uzavře s LinkedIn smlouvu a odesílá kanál XML pro publikování prací. | Zákazník používá API k synchronizaci informací mezi Attract a LinkedIn Recruiter. |
| **Jaký typ práce lze publikovat?** | Omezený výpis | Prémiová nabídka práce nebo omezený výpis | Omezený výpis |
| **Mohu práci propagovat na LinkedIn?** | Ne | Prémiové nabídky práce: Ano<br>Omezené výpisy: Ne | Ne |
| **Jak často jsou úlohy na LinkedIn publikovány?** | Jednou za den | Jednou za den | Několikrát denně, jak je definováno rozhraním API. |
| **Doporučený LinkedIn?** | Ne | Ano | Ne |
| **Co je třeba udělat?** | Zakoupit Attract | Smlouva o sbalení pracovní nabídky s LinkedIn a nákup prémiových nabídek pracovních pozic | Dohoda o rozhraní API s LinkedIn | 
| **Kde najdu další informace?** | [Nastavení integrace s řešením LinkedIn pro aplikaci Microsoft Dynamics 365 Talent - Attract](./attract-admin-linkedin.md) | [Sbalení pracovní nabídky prostřednictvím LinkedIn Recruiter – přehled](https://www.linkedin.com/help/recruiter/answer/79037) | [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect) |

> [!NOTE]
> K odeslání úloh na LinkedIn s aplikací Attract nepotřebujete licenci LinkedIn Recruiter System Connect.

## <a name="see-also"></a>Viz také

[Nastavení integrace s řešením LinkedIn pro aplikaci Microsoft Dynamics 365 Talent - Attract](./attract-admin-linkedin.md)

[Publikování pracovních míst na LinkedIn z aplikace Microsoft Dynamics 365 Talent - Attract](./attract-post-jobs-to-linkedin.md)

[Zdrojování kandidátů pomocí LinkedIn Recruiter v aplikaci Microsoft Dynamics 365 Talent - Attract](./attract-linkedin-recruiter.md)

[Odstraňování problémů s integrací s LinkedIn a aplikací Microsoft Dynamics 365 Talent - Attract](./attract-troubleshoot-linkedin.md)
