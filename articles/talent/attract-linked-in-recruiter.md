---
title: "Zajištění zdrojů pomocí LinkedIn Recruiter"
description: "Toto téma obsahuje informace o používání strojového učení pro získání doporučení práce a uchazeče o práci."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2fc6bf25d303d7d8de8002a923a080b90dcfbeab
ms.openlocfilehash: 106103e2c3d8f3d89aac5140174e5794da22536f
ms.contentlocale: cs-cz
ms.lasthandoff: 10/24/2018

---

# <a name="sourcing-with-linkedin-recruiter"></a>Zajištění zdrojů pomocí LinkedIn Recruiter
[!include[banner](../includes/banner.md)]

LinkedIn je největší databáze talentů na světě a často slouží jako primární systém, který náboráři používají k vyhledávání, komunikaci a zajišťování zdrojů uchazečů o pracovní pozice, které chtějí náboráři obsadit. Integrace programu LinkedIn Recruiter s aplikací Dynamics 365 for Talent: Attract uživatelům usnadňuje nábor a udržování synchronizace dat mezi dvěma systémy.

> [!NOTE]
> Aby bylo možné používat integraci programu LinkedIn Recruiter s aplikací Attract, je potřeba doplněk Comprehensive hiring a licence LinkedIn Recruiter.

## <a name="set-up-linkedin-recruiter-with-attract"></a>Nastavení webu LinkedIn Recruiter s aplikací Attract 

Než budete moci využívat program LinkedIn Recruiter, musíte nakonfigurovat přístup na úrovni smlouvy nebo společnosti s instancí aplikace Attract. Pro dokončení procesu konfigurace musíte spolupracovat s uživatelem, který je správce vaší smlouvy o programu LinkedIn Recruiter. Pomocí následujících kroků nakonfigurujte LinkedIn Recruiter s aplikací Attract.

1.  Přihlaste se k aplikaci Attract jako správce a přejděte na **nastavení pro správu**.

2.  V levém podokně klikněte na kartu **Integrace LinkedIn**.

[![Zobrazení správce aplikace Attract ke spuštění integrace s programem LinkedIn Recruiter](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3.  Klikněte na tlačítko **připojit** pro spuštění nastavení. Budete provedeni procesem registrace LinkedIn.

4.  Pokud máte licence na více smluv LinkedIn, vyberte smlouvu, kterou chcete spojit se systémem Attract. Pokud máte licenci jenom v rámci jedné smlouvy LinkedIn, tento krok není potřeba.

5.  V nastavení pro správu se nyní načte miniaplikace LinkedIn se seznamem integrací. Ve skupinovém rámečku **připojení systému Recruiter** klikněte na tlačítko **Požadavek**.

[![Zobrazení správce aplikace Attract k vyžádání integrace s programem LinkedIn Recruiter](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6.  Po vyžádání integrace ze systému Attract se zobrazí jako **Připraveno pro partnera** a dá se zapnout z **nastavení správy systému Recruiter**. Pokud a této stránce vidíte také možnost **Upozornit partnera**, počkejte chvíli, klikněte na tlačítko **Upozornit partnera** a poté stránku aktualizujte. Nyní by se měla zobrazovat jako **připravená pro partnera**.

[![Zobrazení správce systému Attract k označení strany požadavků Attract, které byly dokončeny.](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

Pokud chcete dokončit další krok, musíte mít oprávnění správce smluv LinkedIn Recruiter.

7.  Přihaste se k webu LinkedIn pomocí účtu správce a přejděte na web LinkedIn Recruiter vpravo nahoře. 

8. V nabídce **Další** v horní části obrazovky klikněte na **nastavení pro správu** a potom klikněte na kartu **ATS**.

Systém Attract bude uveden s několika možnostmi, které lze zapnout.

9. Pokud chcete povolit export pouze 1-kliknutím pro **indikátor In-ATS** a **miniaplikaci In-ATS profil**, vyberte **přístup na úrovni společnosti**. Pokud chcete povolit všechny funkce přístupu na úrovni společnosti plus historii InMail a přístupu neúplného profilu InMail, vyberte **Přístup na úrovni smlouvy**.

10. Zapněte požadovanou úroveň přístupu z nastavení **Admin ATS** programu LinkedIn Recruiter.

[![Zapnutí integrace aplikace Attract ze zobrazení pro správu proramu LinkedIn Recruiter](./media/EnableRSC.png)](./media/EnableRSC.png)

12. Přejděte zpět na nastavení pro správu jako správce Attract a vyberte kartu **Integrace LinkedIn**. Měli byste vidět vytížení miniaplikace LinkedIn načíst zobrazující možnost **povoleno** se zapnutou vybranou úrovní přístupu.

[![Dokončená integrace programu LinkedIn Recruiter](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="using-linkedin-recruiter-capabilities"></a>Použití možností webu LinkedIn Recruiter

Poté, co správce systému Attract povolí možnosti programu LinkedIn Recruiter, je program k dispozici pro přístup manažerům náboru a náborářům. Pokud chcete tyto možnosti použít, připojte se k účtu LinkedIn v části **uživatelská nastavení**. Poté, co byla připojena nastavení správce a uživatele, bude k dispozici několik možností.

### <a name="in-ats-profile-widget"></a>Miniaplikace In-ATS profile

V systému Attract můžete zobrazit profil LinkedIn uchazeče. Miniaplikace LinkedIn zobrazí profil uchazeče, když informace ATS odpovídá informacím o webu LinkedIn uživatelů.

Pokud chcete zobrazit profil, přejděte na profil uchazeče z pracovní pozice nebo fondu talentů. V profilu uchazeče vyberte kartu **LinkedIn** a načte se miniaplikace profilu. Její pomocí určete zda se jedná o shodu. Pokud tomu tak není, najděte správnou osobu. Z této stránky lze také uložit uchazeče do projektů LinkedIn Recruiter.

### <a name="1-click-export"></a>1-Klikněte na Exportovat. 

Při vybírání uchazečů ve službě LinkedIn můžete 1 kliknutím exportovat uchazeče do pracovních míst, která máte v současné době otevřená. Proveďte následující kroky pro export 1 kliknutím. Před dokončením těchto kroků ověřte, zda je vám přiřazená role manažera náboru nebo náboráře pro danou pracovní pozici a zda je pozice ve fázi **Potenciální zákazník**.

1.  Vytvořte pozici, přiřaďte příslušné role a aktivujte pracovní pozici.

2.  Po aktivaci pracovního místa přejděte do programu LinkedIn Recruiter.

3.  Vyhledejte hledaného uchazeče a přejděte do jeho profilu.

4.  Pomocí vyhledávacího pole na kartě kontaktu vyhledejte pracovní místo pomocí názvu nebo ID pracovního místa, které bylo aktivováno v systému Attract. Pokud pracovní místo nenajdete, klikněte na tlačítko **Změnit ATS** k vyhledání správné instance Attract.

5. Po výběru pracovního místa klikněte na tlačítko **exportovat**. Aplikace Attract nyní vyhledá uchazeče.

6.  Přejděte do aplikace Attract a otevřete příslušné pracovní místo. Uchazeče, kterého jste právě exportovali, najdete ve fázi **Potenciální zákazník** v pracovní pozici.

### <a name="in-ats-indicator"></a>Indikátor In-ATS 

Pomocí systému LinkedIn Recruiter můžete sledovat, zda uchazeč žádal o jiná pracovní místa ve vaší organizaci, podívat se, kde se nachází v různých fází žádostí o pracovní pozici, a zobrazit zpětnou vazbu a komentáře z aplikace Attract v programu LinkedIn Recruiter.

1.  Otevřete LinkedIn Recruiter a vyhledejte profil uchazeče, který hledáte.

2.  Přejděte dolů k zobrazení oddílu **In-ATS** v profilu uchazeče.

3.  Tento miniaplikace slouží k zobrazení všech informací o uchazeči, které jsou k dispozici v aplikaci Attract ze zobrazení LinkedIn Recruiter.

4.  Vyberte kartu **Pracovní místa a stavy** k zobrazení pracovních míst, která jsou součástí nejnovějšího stavu, a způsb, jakým se pohybovala proti jednotlivým pracovním místům.

5.  Vyberte kartu **Zpětná vazba z pohovoru** k zobrazení zpětné vazby, kterou vedoucí pohovorů zaslali do systému Attract.

6.  Výběrem karty **Poznámky** zobrazte poznámky, které byly zachyceny pro tohoto uchazeče v aplikaci Attract.

### <a name="inmail-history"></a>Historie InMail

Historie webu LinkedIn InMail je v programu LinkedIn Recruiter dostupná s přístupem na úrovni smlouvy. Pokud tato možnost povolena, můžete zobrazit celou historii InMail s uchazečem. Můžete se také podívat, kdo další z vaší organizace si vyměňoval InMail s uchazečem, nemůžete však zobrazit zprávy, které si zasílali.

Pokud chcete zobrazit historii InMail, přejděte na kartu **LinkedIn** a přejděte do spodní části stránky a zobrazte historii. Můžete zobrazit historii InMail pouze v případě, že uchazeč odpověděl na vaši žádost a rozhodl se nasdílet s vámi svůj profil ve službě LinkedIn. Zprávy z InMail se každých několik hodin synchronizují s aplikací Attract.

### <a name="notes-history"></a>Historie poznámek 

Historie poznámek LinkedIn je v programu LinkedIn Recruiter dostupná s přístupem na úrovni smlouvy. Pokud je to povoleno, můžete zobrazit poznámky, které byly zachyceny o uchazeči podle různých náborářů z vaší organizace.

Pokud chcete zobrazit historii poznámek, přejděte na kartu **LinkedIn** a přejděte do spodní části stránky a zobrazte historii. Můžete zobrazit všechny poznámky o uchazeči z webu LinkedIn Recruiter.

### <a name="inmail-stub-profile"></a>Profil InMail se zakázaným inzerováním

Profil InMail se zakázaným inzerováním je v programu LinkedIn Recruiter dostupný s přístupem na úrovni smlouvy. Pokud uchazeči souhlasí se sdílením svých profilů LinkedIn s libovolným uživatelem ve vaší organizaci, můžete sledovat uchazeče v aplikaci Attract a pro každého uchazeče se vytvoří nový záznam uchazeče.

Chcete-li zobrazit seznam uchazečů, přejděte na **Fondy talentů**, aby se zobrazil fond talentů LinkedIn vytvořený systémem. Tento fond talentů obsahuje seznam uchazečů a jejich profily se zakázaným inzerováním z webu LinkedIn, zobrazující křestní jméno a příjmení uchazeče. ID e-mailu uchazeče se zobrazí, pokud uchazeč nastavil sdílení své e-mailové adresy.

