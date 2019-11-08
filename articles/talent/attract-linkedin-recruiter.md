---
title: Zdrojování kandidátů pomocí LinkedIn Recruiter v aplikaci Microsoft Dynamics 365 Talent - Attract
description: Použijte integraci LinkedIn poskytovanou aplikací Microsoft Dynamics 365 Talent - Attract ke zdrojování uchazečů o zaměstnání pomocí LinkedIn Recruiter.
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
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 8f2e95e74bbc8d78ed5d970f29b61150a45c6740
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551557"
---
# <a name="source-candidates-with-linkedin-recruiter-in-microsoft-dynamics-365-talent---attract"></a>Zdrojování kandidátů pomocí LinkedIn Recruiter v aplikaci Microsoft Dynamics 365 Talent - Attract
[!include[banner](../includes/banner.md)]

LinkedIn je nejvyšší světová síť profesionálů, která poskytuje přístup k nejlepším talentům. Microsoft Dynamics 365 Talent: Attract vám umožní zdrojovat kandidáty přímo z LinkedIn. Proto je snazší než kdykoli dříve najít talenty, které potřebujete k obsazení otevřených pozic. Po nastavení připojení k LinkedIn prostřednictvím Attract můžete zobrazit potenciální kandidáty na LinkedIn a exportovat je do aplikace jediným kliknutím.

Pokud tuto funkcinemáte, obraťte se na správce. Dříve než budete moci využít výhod LinkedIn Recruiter z Attract, je nutné, aby váš správce [nastavil integraci s LinkedIn](./attract-admin-linkedin.md). Poté můžete nastavit připojení LinkedIn Recruiter a začít vyhledávat kandidáty.

## <a name="set-up-your-connection-with-linkedin-recruiter"></a>Nastavit připojení pomocí LinkedIn Recruiter

Chcete-li začít pracovat s LinkedIn Recruiter prostřednictvím aplikace Attract, je nutné vytvořit připojení pomocí LinkedIn Recruiter. V tomto kroku budete potřebovat své přihlašovací údaje do LinkedIn Recruiter.

1. Zvolte tlačítko **Nastavení** (ikona ozubeného kola) v pravém horním rohu stránky.
2. Vyberte **Nastavení uživatele**.
3. Na kartě **Připojení** vyberte možnost **Připojit** vedle **LinkedIn**. Postupujte podle pokynů, které jsou k dispozici službou LinkedIn.

    ![[Nastavit připojení k LinkedIn Recruiter z Attract](./media/attract-setup-linkedin-recruiter-connection.png)](./media/attract-set-up-linkedin-recruiter-connection.png)

## <a name="view-linkedin-candidates-in-attract"></a>Zobrazit kandidáty LinkedIn v aplikaci Attract

Po připojení LinkedIn Recruiter můžete zobrazit linkedinové profily kandidátů v aplikaci Attract.

1. V aplikaci Attract vyberte **Pracovní pozice** nebo **Skupiny talentů** v levé části a poté vyberte uchazeče.

    ![[Zobrazit kandidáty LinkedIn v aplikaci Attract] (./media/attract-view-linkedin-candidates.png)](./media/attract-view-linkedin-candidates.png)

2. V profilu kandidáta vyberte kartu **LinkedIn**. Můžete zobrazit profil uchazeče spolu s historií InMail a s historií poznámek LinkedIn.

Odtud můžete uložit kandidáta do projektu LinkedIn Recruiter, odeslat inMail nebo použijte Update Me pro nastavení výstrahy v aplikaci LinkedIn Recruiter.

> [!NOTE]
> LinkedIn profil uchazeče se zobrazí v Attract, když se informace o uživateli kandidáta shodují s informacemi LinkedIn. Používají se následující pravidla párování:
> 
> 1. Pokud se e-mailová adresa a ID člena LinkedIn shoduje s v aplikaci Attract a LinkedIn, zobrazí se profil kandidáta. Kandidáti stále mají možnost propojit nebo zrušit propojení svého LinkedIn profilu s Attract.
> 2. Pokud neodpovídá e-mailová adresa nebo ID člena LinkedIn, zobrazí se seznam možných kandidátů. Poté můžete vybrat kandidáta v seznamu a propojit tento profil.
> 3. Pokud neexistují žádné vyhovující položky, budete upozorněni, že nebyla nalezena žádná shoda.

## <a name="export-linkedin-candidates-to-attract-with-one-click"></a>Exportovat kandidáty z LinkedIn do Attract jedním kliknutím

Při revizi kandidátů v LinkedIn Recruiter je můžete exportovat do pracovních pozic, které jsou aktuálně otevřeny v aplikaci Attract. Pro tento krok potřebujete oprávnění náborového manažera nebo náborového pracovníka v aplikaci Attract. Další informace o rolích v Attract naleznete v tématu [Zabezpečení a správa rolí v aplikaci Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/security-attract).

Je také nutné zajistit, aby úloha měla fázi potenciálního uchazeče. Další informace naleznete v tématu [Aktivita potenciálního uchazeče](./activities-attract.md#prospect-activity).

1. V aplikai Attract vytvořte pozici, přiřaďte příslušné role a aktivujte pracovní pozici.
2. V LinkedIn Recruiter vyhledejte vhodného kandidáta na práci a přejděte k profilu uchazeče.
3. Ve vyhledávacím poli na kartě kontaktu vyhledejte pracovní místo pomocí názvu nebo ID pracovního místa, které bylo aktivováno v systému Attract. Pokud pracovní místo nenajdete, vyberte **Změnit ATS** k vyhledání správné instance Attract.
4. Vyberte práci a pak vyberte **Export**.
5. V aplikaci Attract otevřete úlohu. Exportovaný kandidát se zobrazí na kartě **Potenciální uchazeč** pro danou úlohu.

## <a name="view-attract-information-in-linkedin-recruiter"></a>Zobrazit informace o aplikaci Attract v LinkedIn Recruiter

Pomocí LinkedIn Recruiter můžete sledovat, zda uchazeč žádal o jiná pracovní místa ve vaší organizaci, podívat se, kde se kandidát nachází v různých fází žádostí o pracovní pozici, a zobrazit zpětnou vazbu a komentáře z aplikace Attract.

1. Otevřete LinkedIn Recruiter a vyberte požadovaný profil kandidáta.
2. Přesuňte ukazatel myši na **V ATS**.
3. Chcete-li zobrazit informace o uchazečích, které jsou uloženy v Attract, vyberte některou z následujících možností:

    - **Úlohy & stavy** – zobrazení úloh, jejichž součástí je uchazeč, nejnovější stav a způsob, jakým uchazeč postupuje pro každou práci.
    - **Zpětná vazba z pohovoru** – zobrazení zpětné vazby, kterou vedoucí pohovorů zaslali do systému Attract.
    - **Poznámky** – zobrazí se poznámky, které byly pro tohoto kandidáta zadány v Attract.

    ![[Zobrazit informace Attract z LinkedIn Recruiter](./media/attract-view-information-from-linkedin-recruiter.png)](./media/attract-view-information-from-linkedin-recruiter.png)

> [!NOTE]
> Údaje o uchazeči a žádosti se nebudou synchronizovat s programem LinkedIn Recruiter, pokud se uchazeč nedostal za fázi potenciálního uchazeče.

## <a name="view-linkedin-talent-pools"></a>Zobrazit skupiny talentů LinkedIn

Pokud kandidáti souhlasí se sdílením svého LinkedIn profilu s libovolným uživatelem ve vaší organizaci, vytvoří se nový záznam uchazeče v aplikaci Attract. Tito kandidáti pak budou uvedeni v systémově vytvořené skupině talentů LinkedIn.

1. V systému Attract vyberte **Skupiny talentů** na levé straně.
2. Vyberte skupinu talentů LinkedIn. Zobrazí se seznam kandidátů a jejich profilů se zakázaným inzerováním z LinkedIn. Profily se zakázaným inzerováním obsahují křestní jména a příjmení kandidáta a e-mailovou adresu, pokud se ji uchazeč rozhodne sdílet.

## <a name="see-also"></a>Viz také

[Často kladené otázky k řešení LinkedIn](./attract-linkedin-faq.md)

[Nastavení integrace s řešením LinkedIn](./attract-admin-linkedin.md)

[Vytvoření prací](./creating-jobs-attract.md)

[Publikování pracovních míst na LinkedIn z aplikace Attract](./attract-post-jobs-to-linkedin.md)

[Odstraňování potíží s integrací s řešením LinkedIn](./attract-troubleshoot-linkedin.md)
