---
title: Nastavení integrace LinkedIn a aplikací Attract
description: V tomto tématu je vysvětleno, jak konfigurovat integraci řešení LinkedIn v aplikaci Microsoft Dynamics 365 Talent - Attract, aby bylo možné snadno publikovat práce na LinkedIn z aplikace Attract a aby vaši pracovníci náboru mohli synchronizovat své informace o náboru s profilem kandidáta na LinkedIn.
author: andreabichsel
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
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 4c518fb7036d44aa52c8db859ee3616fc4e58a06
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833177"
---
# <a name="set-up-linkedin-integration-with-attract"></a>Nastavení integrace LinkedIn a aplikací Attract

[!include [banner](includes/banner.md)]

Pomozte pracovníkům náboru a vedoucím týmů přilákat nejlepší talenty konfigurací integrace LinkedIn s Microsoft Dynamics 365 Talent: Attract. Attract umožňuje publikovat nabídky práce přímo na LinkedIn, největší online síti profesionálů.

Úlohy, které publikujete na LinkedIn prostřednictvím Attract, jsou omezenýmy zápisy a nezpůsobí vaší společnosti žádné dodatečné náklady. Tyto výpisy jsou k dispozici pouze prostřednictvím softwarových partnerů LinkedIn, jako je například systém Attract. Nezobrazí se na panelu **Kariéra** na LinkedIn stránce vaší společnosti, protože zde jsou zobrazeny pouze placené výpisy. Zobrazí se však v případě, že potenciální kandidáti zobrazí všechna dostupná pracovní místa. Omezený výpisy jsou také zobrazeny ve vyhledávání práce na LinkedIn.

Attract nabízí dva způsoby integrace s LinkedIn, které vám pomohou získat kandidáty z této oblíbené webové stránky:

- Publikování pracovních míst z aplikace Attract na LinkedIn
- Zazdrojování kandidátů z LinkedIn do aplikace Attract.

Obě možnosti lze konfigurovat na kartě **Integrace LinkedIn** v centru pro správu. Chcete-li otevřít centrum pro správu, přejděte na <https://attract.talent.dynamics.com/adminsettings>.

> [!NOTE]
> Aby bylo možné používat integraci programu LinkedIn Recruiter s aplikací Attract, je potřeba doplněk [Komplexní nábor](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) a [licence LinkedIn Recruiter](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18). Další informace naleznete v tématu [Která verze aplikace Microsoft Dynamics 365 Talent - Attract](./attract-comprehensive-hiring.md).

Pokud máte potíže s publikováním prací na LinkedIn, nahlédněte do části [Odstraňování problémů s integrací s LinkedIn a aplikací Microsoft Dynamics 365 Talent - Attract](./attract-troubleshoot-linkedin.md).

Informace o dalších způsobech publikování prací na LinkedIn naleznete v tématu [Nejčastější dotazy týkající se integrace aplikace Attract s LinkedIn](./attract-linkedin-faq.md).

## <a name="configure-job-posting-to-linkedin"></a>Konfigurovat publikování práce na LinkedIn

Před publikováním prací z aplikace Attract do LinkedIn budete potřebovat [ID společnosti pro LinkedIn](https://aka.ms/findID). Vaše ID společnosti ve službě LinkedIn je řetězec čísel, který jednoznačně identifikuje vaši společnost ve službě LinkedIn. Další informace naleznete v tématu [Spojení vašeho ID společnosti LinkedIn s pracovní vývěskou – často kladené dotazy](https://aka.ms/findID).

Attract odešle vaše pracovní nabídky na LinkedIn a LinkedIn vyhledává informační kanál přibližně jednou denně. Publikování práce na webu může zabrat až 48 hodin.

Publikované pracovní nabídky na službě LinkedIn se objeví na živém webu LinkedIn. LinkedIn nemá žádné testovací prostředí pro publikování pracovních pozic. Proto se ujistěte, že nepublikujete žádné testovací úlohy omylem. 

1. V nabídce **Nastavení** (symbol ozubeného kola) v pravém horním rohu vyberte **Centrum pro správu**. Můžete také přejít na <https://attract.talent.dynamics.com/adminsettings>.
2. Vyberte kartu **Integrace LinkedIn**.
3. V poli **Název společnosti** zadejte název společnosti a v **ID společnosti** zadejte vaše ID společnosti LinkedIn. Ujistěte se, že název společnosti odpovídá názvu, který se zobrazuje na LinkedIn stránce vaší společnosti. Další informace o ID společnosti LinkedIn naleznete v tématu [Spojení vašeho ID společnosti LinkedIn s pracovní vývěskou – často kladené dotazy](https://www.linkedin.com/help/linkedin/answer/98972).

    Potřebujete-li změnit libovolné informace vaší organizace, prostudujte si téma [Změna adresy vaší organizace, technického kontaktu atd.](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more). Pokud potíže přetrvávají, obraťte se na [Podporu LinkedIn](https://www.linkedin.com/help/linkedin).

4. Zvolte **Uložit**.

## <a name="set-up-linkedin-recruiter-with-attract"></a>Nastavení programu LinkedIn Recruiter s aplikací Attract 

Chcete-li povolit pracovníkům náboru zdrojovat práce prostřednictvím LinkedIn Recruiter, je nutné nakonfigurovat integraci LinkedIn Recruiter v aplikaci Attract. Pro dokončení procesu konfigurace musíte spolupracovat s uživatelem, který je správce vaší smlouvy o programu LinkedIn Recruiter.

1. V nabídce **Nastavení** (symbol ozubeného kola) v pravém horním rohu vyberte **Centrum pro správu**. Můžete také přejít na <https://attract.talent.dynamics.com/adminsettings>.
2. Vyberte kartu **Integrace LinkedIn**.

    [![Zobrazení správce aplikace Attract ke spuštění integrace s programem LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Klepnutím na tlačítko **Připojit** spusťte instalační program. Budete provedeni procesem přihlášení LinkedIn.
4. Pokud máte licence na více smluv LinkedIn, vyberte smlouvu, kterou chcete spojit se systémem Attract. Pokud máte licenci jenom v rámci jedné smlouvy LinkedIn, tento krok můžete přeskočit.
5. V **Připojení systému Recruiter (RSC)** vyberte **Požadavek**.

    [![Zobrazení správce aplikace Attract k vyžádání integrace s programem LinkedIn Recruiter](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6. Nastavení **Připojení systému Recruiter (RSC)** by se nyní mělo zobrazit jako **Partner připraven**. Pokud a této stránce vidíte také možnost **Upozornit partnera**, počkejte chvíli, vyberte tlačítko **Upozornit partnera** a poté stránku aktualizujte. Nastavení by se mělo zobrazit jako **Partner připraven**.

    [![Zobrazení správce systému Attract k označení strany požadavků Attract, které byly dokončeny.](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

7. Pokud chcete dokončit následující krok, musíte mít oprávnění správce smluv LinkedIn Recruiter.

    1. Přihlaste se k LinkedIn pomocí účtu správce a poté vyberte **LinkedIn Recruiter** v pravém horním rohu. 
    2. V nabídce **Další** v horní části stránky vyberte **Nastavení pro správu** a potom vyberte kartu **ATS**.
    3. Chcete-li povolit export jedním klepnutím pouze pro jednu smlouvu, zapněte **Přístup na úrovni smlouvy (pro každou licenci této smlouvy)**. Chcete-li ji povolit pro celou společnost, zapněte **Přístup na úrovni smlouvy (pro každou smlouvu ve vaší společnosti)**.

    [![Zapnutí integrace aplikace Attract ze zobrazení pro správu programu LinkedIn Recruiter](./media/EnableRSC.png)](./media/EnableRSC.png)

8. V centru pro správu Attract vyberte kartu **Integrace LinkedIn**. Nastavení **Recruiter System Connect (RSC)** by se nyní mělo zobrazit jako **Povoleno**.

    [![Dokončení integrace LinkedIn Recruiter](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="set-up-apply-with-linkedin-in-attract"></a>Nastavení Požádat přes LinkedIn v aplikaci Attract

Můžete povolit kandidátům požádat o vaše práce pomocí svých LinkedIn profilů. Další informace o funci Požádat přes LinkedIn naleznete v [Síla LinkedIn všude: Požádat přes LinkedIn](https://blog.linkedin.com/2011/07/24/apply-with-linkedin).

Tato funkce je aktuálně v náhledu Před provedením těchto kroků je nutné, aby byla povolena možnost Požádat přes LinkedIn. Další informace o povolení funkcí náhledu naleznete v části [Přístup k funkcím verze Preview v Microsoft Dynamics 365 Talent](./access-preview-feature.md).

1. V nabídce **Nastavení** (symbol ozubeného kola) v pravém horním rohu vyberte **Centrum pro správu**. Můžete také přejít na <https://attract.talent.dynamics.com/adminsettings>.
2. Vyberte kartu **Integrace LinkedIn**.

    [![Zobrazení správce aplikace Attract ke spuštění integrace s programem LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Vedle **Požádat přes LinkedIn** vyberte **Připojit** pro start nastavení. Budete provedeni zbytkem procesu s LinkedIn.

## <a name="see-also"></a>Viz také

[Časté dotazy týkající se integrace Attract s řešením LinkedIn](./attract-linkedin-faq.md)

[Publikování pracovních míst na externí kariérní weby z aplikace Attract](./posting-jobs-external.md)

[Zdrojování kandidátů pomocí LinkedIn Recruiter v aplikaci Microsoft Dynamics 365 Talent - Attract](./attract-linkedin-recruiter.md)

[Vytvoření, schválení a zveřejnění pracovních míst v aplikaci Attract](./creating-jobs-attract.md)

[Odstraňování problémů s integrací s LinkedIn a aplikací Microsoft Dynamics 365 Talent - Attract](./attract-troubleshoot-linkedin.md)
