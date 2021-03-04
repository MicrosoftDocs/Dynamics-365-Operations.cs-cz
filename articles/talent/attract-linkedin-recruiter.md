---
title: Zdrojování kandidátů pomocí LinkedIn Recruiter v aplikaci Attract
description: Použijte integraci LinkedIn poskytovanou aplikací Microsoft Dynamics 365 Talent - Attract ke zdrojování uchazečů o zaměstnání pomocí LinkedIn Recruiter.
author: andreabichsel
manager: AnnBe
ms.date: 08/31/2020
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
ms.openlocfilehash: 96e4660c4958bf5f2a0910bfad770e1e713f800f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528262"
---
# <a name="source-candidates-with-linkedin-recruiter-in-attract"></a>Zdrojování kandidátů pomocí LinkedIn Recruiter v aplikaci Attract

[!include [banner](includes/banner.md)]

LinkedIn je nejvyšší světová síť profesionálů, která poskytuje přístup k nejlepším talentům. Microsoft Dynamics 365 Talent: Attract vám umožní zdrojovat kandidáty přímo z LinkedIn. Proto je snazší než kdykoli dříve najít talenty, které potřebujete k obsazení otevřených pozic. Po nastavení připojení k LinkedIn prostřednictvím Attract můžete zobrazit potenciální kandidáty na LinkedIn a exportovat je do aplikace jediným kliknutím.

Pokud tuto funkcinemáte, obraťte se na správce. Dříve než budete moci využít výhod LinkedIn Recruiter z Attract, je nutné, aby váš správce [nastavil integraci s LinkedIn](./attract-admin-linkedin.md). Poté můžete nastavit připojení LinkedIn Recruiter a začít vyhledávat kandidáty.

>[!IMPORTANT]
>Od 1. července 2020 již LinkedIn nepodporuje Internet Explorer 11. Uživatelé mohou stále používat LinkedIn s Internet Explorer 11, ale zobrazí se výzva k upgradu nebo použití jiného prohlížeče. Další informace viz [Podporované internetové prohlížeče pro LinkedIn](https://www.linkedin.com/help/linkedin/answer/4135/supported-internet-browsers-for-linkedin).

## <a name="set-up-your-connection-with-linkedin-recruiter"></a>Nastavit připojení pomocí LinkedIn Recruiter

Chcete-li začít pracovat s LinkedIn Recruiter prostřednictvím aplikace Attract, je nutné vytvořit připojení pomocí LinkedIn Recruiter. V tomto kroku budete potřebovat své přihlašovací údaje do LinkedIn Recruiter.

1. Zvolte tlačítko **Nastavení** (ikona ozubeného kola) v pravém horním rohu stránky.
2. Vyberte **Nastavení uživatele**.
3. Na kartě **Připojení** vyberte možnost **Připojit** vedle **LinkedIn**. Postupujte podle pokynů, které jsou k dispozici službou LinkedIn.

    ![[Nastavení připojení k LinkedIn Recruiter z aplikace Attract](./media/attract-set-up-linkedin-recruiter-connection.png)](./media/attract-set-up-linkedin-recruiter-connection.png)

## <a name="view-linkedin-candidates-in-attract"></a>Zobrazit kandidáty LinkedIn v aplikaci Attract

Po připojení LinkedIn Recruiter můžete zobrazit linkedinové profily kandidátů v aplikaci Attract.

>[!NOTE]
>Pokud vám byla přidělena licence Recruiter (Náborář), můžete zobrazit úplné informace o kandidátech.<br><br>
>Pokud máte licenci Hiring Manager (Náborový manažer) nebo žádnou licenci, nezapomeňte se odhlásit z LinkedIn nebo LinkedIn Recruiter před přechodem na kartu LinkedIn pro kandidáta v aplikaci Attract. Budete moci zobrazit základní údaje veřejného profilu kandidáta, například jeho křestní jméno a příjmení.

1. V aplikaci Attract vyberte **Pracovní pozice** nebo **Skupiny talentů** v levé části a poté vyberte uchazeče.

    ![[Zobrazit kandidáty LinkedIn v aplikaci Attract](./media/attract-view-linkedin-candidates.png)](./media/attract-view-linkedin-candidates.png)

2. V profilu kandidáta vyberte kartu **LinkedIn**. Můžete zobrazit profil kandidáta a historii InMail.

   ![Zobrazení informací o kandidátovi na LinkedIn](./media/attract-candidate-linkedin-tab.png)

Odtud můžete provést následující akce:

- Vyberte kartu **Náborové aktivity** k zobrazení následujících:
   
   - Poznámky o náboráři (veřejné i soukromé). Ve výchozím nastavení jsou poznámky soukromé a viditelné pouze pro vlastníka poznámek.
   - Aktivita InMail (mimo obsah InMail). Posunutím do dolní části stránky zobrazíte výměnu InMail s vaším potenciálním zákazníkem a další uživatele ve vaší organizaci, kteří s vaším potenciálním zákazníkem interagují.
   - Aktivita odmítnutí kandidátů

- Volbou **Odeslat InMail** pošlete InMail, aniž byste museli opustit aplikaci Attract.

- Volbou **Uložit do úlohy** uložíte úlohu, aniž byste opustili Attract.

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

    ![[Zobrazení informací o aplikaci Attract v LinkedIn Recruiter](./media/attract-view-information-from-linkedin-recruiter.png)](./media/attract-view-information-from-linkedin-recruiter.png)

> [!NOTE]
> Údaje o uchazeči a žádosti se nebudou synchronizovat s programem LinkedIn Recruiter, pokud se uchazeč nedostal za fázi potenciálního uchazeče.

## <a name="view-linkedin-talent-pools"></a>Zobrazit skupiny talentů LinkedIn

Pokud kandidáti souhlasí se sdílením svého LinkedIn profilu s libovolným uživatelem ve vaší organizaci, vytvoří se nový záznam uchazeče v aplikaci Attract. Tito kandidáti pak budou uvedeni v systémově vytvořené skupině talentů LinkedIn.

1. V systému Attract vyberte **Skupiny talentů** na levé straně.
2. Vyberte skupinu talentů LinkedIn. Zobrazí se seznam kandidátů a jejich profilů se zakázaným inzerováním z LinkedIn. Profily se zakázaným inzerováním obsahují křestní jména a příjmení kandidáta a e-mailovou adresu, pokud se ji uchazeč rozhodne sdílet.

## <a name="see-also"></a>Viz také

[Časté dotazy týkající se integrace Attract s řešením LinkedIn](./attract-linkedin-faq.md)

[Nastavení integrace s řešením LinkedIn pro aplikaci Microsoft Dynamics 365 Talent - Attract](./attract-admin-linkedin.md)

[Vytvoření, schválení a zveřejnění pracovních míst v aplikaci Attract](./creating-jobs-attract.md)

[Publikování pracovních míst na LinkedIn z aplikace Microsoft Dynamics 365 Talent - Attract](./attract-post-jobs-to-linkedin.md)

[Odstraňování problémů s integrací s LinkedIn a aplikací Microsoft Dynamics 365 Talent - Attract](./attract-troubleshoot-linkedin.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]