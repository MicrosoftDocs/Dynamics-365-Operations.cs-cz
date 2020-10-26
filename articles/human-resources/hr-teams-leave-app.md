---
title: Správa žádostí o dovolenou v aplikaci Teams
description: Toto téma ukazuje, jak požádat o volno v aplikaci Dynamics 365 Human Resources v Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c6856e417ee47f8f582f797c5bcedcff23a1432f
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3929986"
---
# <a name="manage-leave-requests-in-teams"></a>Správa žádostí o dovolenou v aplikaci Teams

[!include [banner](includes/preview-feature.md)]

Aplikace Microsoft Dynamics 365 Human Resources v aplikaci Microsoft Teams vám umožňuje rychle požádat o volno a zobrazit informace o svém zůstatku volna přímo v Microsoft Teams. Můžete komunikovat s robotem a požádat o informace a zahájit žádost o dovolenou. Karta **Volno** poskytuje podrobnější informace. Kromě toho můžete lidem posílat informace o svém nadcházejícím volnu v týmech a chatech mimo aplikaci Human Resources.

## <a name="install-the-app"></a>Instalace aplikace

Aplikaci Human Resources najdete v obchodě Teams.

1. V aplikaci Microsoft Teams zvolte tři tečky.

   ![Tři tečky aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. Vyhledejte Dynamics 365 Human Resources a poté vyberte dlaždici **Human Resources** .

   ![Dlaždice HR aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. Vyberte tlačítko **Přidat** pro instalaci aplikace.

   ![Instalace aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

Pokud vás aplikace nepřihlásí automaticky, vyberte kartu **Nastavení** pro přihlášení.

![Karta nastavení aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> Pokud nevidíte přihlašovací dialogové okno, zkontrolujte nastavení prohlížeče a povolte automaticky otevíraná okna. 

Pokud máte přístup k více než jedné instanci aplikace Human Resources, můžete vybrat prostředí, ke kterému se chcete připojit, na kartě **Nastavení** .

> [!NOTE]
> Aplikace nyní podporuje roli zabezpečení správce systému.
 
## <a name="use-the-bot"></a>Použití robota

Po instalaci aplikace se zobrazí uvítací zpráva, která vás informuje o typech akcí, které může robot provést vaším jménem.

![Uvítací zpráva robota aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> Při první interakci s robotem se možná budete muset přihlásit. Pokud nevidíte přihlašovací dialogové okno, zkontrolujte nastavení prohlížeče a povolte automaticky otevíraná okna.

Můžete požádat robota a následující akce:

- Zobrazit informace o zůstatku volna pro každý typ volna, do kterého jste zaregistrováni.

   ![Zobrazení zůstatků aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- Zobrazit další podrobnosti o konkrétním typu volna.

   ![Zobrazení podrobností aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot-details.png)

- Zahájit žádost o volno za vás.

   ![Žádost o volno aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot-request.png)
 
Po zahájení žádosti o dovolenou můžete upravit dny přímo na kartě.

![Úprava žádosti aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot-edit.png)
 
Až zadáte informace, vyberte **Odeslat** pro odeslání žádosti ke schválení. Můžete také zvolit **Uložit jako koncept** a vrátit se k žádosti později.

![Odeslání žádosti aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a>Správa volna v aplikaci Teams

Karta **Volno** umožňuje zobrazit:

- Informace o zůstatku pro každý typ volna, ke kterému jste zaregistrováni

- Nadcházející žádosti o volno

- Žádosti o volno

- Koncept žádostí o volno

![Karta volna aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a>Vytvoření nové žádosti

1. Chcete-li vytvořit novou žádost o volno, zvolte **Nová žádost** .

   ![Nová žádost aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. Zadejte den nebo dny, na které chcete volno, a poté vyberte **Přidat** .

   ![Přidání volna aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. V případě potřeby zadejte kód důvodu. Také zadejte případné komentáře a přidejte všechny přílohy.

4. Až zadáte informace, napište **Odeslat** pro odeslání žádosti ke schválení. Můžete také naspat **Uložit jako koncept** a vrátit se k žádosti později.

### <a name="manage-draft-requests"></a>Správa konceptů žádostí

1. Zvolte kartu **Koncepty** .

   ![Karta konceptů aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. Vyberte symbol tužky, chcete-li žádost upravit, nebo vyberte koš, chcete-li žádost odstranit.

3. Proveďte potřebné změny. Až zadáte informace, napište **Odeslat** pro odeslání žádosti ke schválení. Můžete také zvolit **Uložit jako koncept** a vrátit se k žádosti později.

   ![Úprava konceptu aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a>Odpovídejte na oznámení týmů

Když vy nebo pracovník, jehož jste schvalovatelem, odešlete žádost o pracovní volno, obdržíte oznámení v aplikaci Human Resources v Teams. Chcete-li oznámení zobrazit, vyberte jej. Oznámení se také zobrazují v oblasti **Chat** .

Pokud jste schvalovatel, můžete v oznámení zvolit možnosti **Schválit** nebo **Odmítnout** . Můžete také zadat volitelnou zprávu.

![Oznámení o žádosti o pracovní volno v aplikaci Human Resources Teams](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a>Pošlete nadcházející informace o volném čase vašim spolupracovníkům

Po instalaci aplikace Human Resources pro Teams můžete snadno poslat informace o svém nadcházejícím volnu svým spolupracovníkům v týmech nebo chatech.

1. V týmu nebo chatu v Teams vyberte tlačítko Human Resources pod oknem chatu.

   ![Tlačítko Human Resources pod oknem chatu](./media/hr-teams-leave-app-chat-button.png)

2. Vyberte žádost o dovolenou, kterou chcete sdílet. Pokud chcete sdílet koncept žádosti o dovolenou, nejprve vyberte **Koncepty** .

   ![Vyberte nadcházející žádost o dovolenou ke sdílení](./media/hr-teams-leave-app-chat-search.png)

Vaše žádost o dovolenou se zobrazí v chatu.

![Karta s žádostí o volno v Human Resources](./media/hr-teams-leave-app-chat-card.png)

Pokud jste sdíleli koncept žádosti, zobrazí se jako koncept:

![Karta s konceptem žádosti o volno v Human Resources](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a>Zobrazení kalendáře pracovního volna týmu

Pokud jste manažer s přímými podřízenými, můžete si prohlédnout schválené a nevyřízené pracovní volno vašeho týmu.

1. V aplikaci Human Resources v Teams vyberte **Volno** .

2. Vyberte **Kalendář týmu** .

   ![Zobrazení kalendáře v aplikaci Human Resources Teams](./media/hr-teams-leave-app-view-calendar.png)

Kalendář zobrazuje schválené a nevyřízené volno vašich přímých podřízených.

![Kalendář volna v aplikaci Human Resources Teams](./media/hr-teams-leave-app-calendar.png)

## <a name="troubleshooting"></a>Řešení potíží

Pokud máte potíže s přihlášením nebo používáním aplikace Human Resources Teams, zkuste problémy vyřešit podle těchto pokynů. Pokud problémy přetrvávají i po pokusu o vyřešení, obraťte se na podporu. Pro další informace si přečtěte [Získání podpory](hr-admin-troubleshooting-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Nelze se přihlásit do aplikace Human Resources v Teams

Pokud se nemůžete do aplikace přihlásit, je možné, že účet, pomocí kterého se přihlašujete do Microsoft Teams není spojen se záznamem zaměstnance v Dynamics 365 Human Resources. Požádejtea správce systému o ověření, jestli je váš záznam zaměstnance správně přidružen.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Chyba při schvalování žádostí o dovolenou v aplikaci Human Resources v Teams

Pokud se vám při pokusu o schválení žádostí o dovolenou v aplikaci Teams zobrazí chyba, proveďte v rámci řešení potíží následující kroky:

1. Ověřte, že účet, který používáte k přihlášení k Microsoft Teams, je stejný, jaký používáte pro přístup k Dynamics 365 Human Resources.

2. Ověřte, jestli jste platným schvalovatelem požadavku, a to kontrolou nastavení pracovního postupu pro schválení dovolené. Další informace o pracovních postupech žádostí o dovolenou najdete v tématu [Vytvoření pracovního postupu žádosti o dovolenou](hr-leave-and-absence-workflow.md).

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

S robotem Dynamics 365 Human Resources v aplikaci Microsoft Teams jsou textové vstupy uživatele analyzovány pro porozumění základním dotazům/záměrům. Vstup uživatele, například „Vyhledat účet Contoso“, je přesměrován na jednu ze služeb Cognitive Services společnosti Microsoft nazvanou Language Understanding Intelligent Service (LUIS). Přečtěte si více o LUIS  [zde](https://www.luis.ai/). Služba LUIS ujasňuje nebo chápe záměr vstupu uživatele (v tomto případě je záměrem najít informace) a cílovou entitu (v tomto případě je zamýšlenou entitou účet s názvem Contoso). Tyto informace jsou poté předány do řešení  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) společnosti Microsoft, které interaguje s daty z Dynamics 365 Human Resources a načte požadované informace pro uživatelský dotaz. 

Instalací a umožněním přístupu k používání robota souhlasíte s tím, že umožníte službě LUIS a rámci robota Azure zpracovat záměr za vstupem, což má za následek vylepšenou konverzační uživatelskou zkušenost. Služba LUIS a rámec robota Azure mohou mít ve srovnání s Dynamics 365 Human Resources různé úrovně shody. Zatímco služba LUIS má přístup pouze k uživatelským dotazům a není určena k připojení k datům nebo účtu uživatele Dynamics 365 Human Resources, uživatel robota Dynamics 365 Human Resources může dobrovolně zadat dotaz obsahující zákaznická data, osobní údaje nebo jiná data a takový obsah dotazu by mohl být zaslán do služby LUIS a do rámce robota Azure. 

Obsah dotazů a zpráv uživatele je v systému LUIS uchováván maximálně 30 dní, je šifrován a nepoužívá se pro školení ani zlepšení služeb. Přečtěte si více o Cognitive Services  [zde](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Chcete-li spravovat nastavení administrátora pro aplikace v Microsoft Teams, přejděte do [centra pro správu Microsoft Teams](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams  Azure Event Grid a Azure Cosmos DB

Při použití aplikace Dynamics 365 Human Resources v Microsoft Teams mohou některá data zákazníků téct mimo geografickou oblast, kde je nasazena služba Human Resources vašeho klienta.

Dynamics 365 Human Resources přenáší podrobnosti o žádosti o pracovní volno a úkolu pracovního postupu do Microsoft Azure Event Grid a Microsoft Teams. Tato data mohou být uložena v Event Grid Microsoft Azure až 24 hodin a budou zpracována ve Spojených státech, jsou šifrována během přenosu a v klidu a nejsou používána společností Microsoft nebo jejími subprocesory pro školení nebo vylepšení služeb. Chcete-li zjistit, kde jsou vaše data uložena v Teams, přečtěte si [Umístění dat v Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).

Při konverzaci s chatovacím robotem v aplikaci Human Resources může být obsah konverzace uložen v Azure Cosmos DB a přenesen do Microsoft Teams. Tato data mohou být uložena v Azure Cosmos DB po dobu až 24 hodin a mohou být zpracovávána mimo geografickou oblast, kde je nasazena služba Human Resources vašeho nájemce, je šifrována během přenosu a v klidu a není používána společností Microsoft nebo jejími subprocesory pro školení nebo vylepšení služeb. Chcete-li zjistit, kde jsou vaše data uložena v Teams, přečtěte si [Umístění dat v Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).
 
Chcete-li omezit přístup k aplikaci Human Resources v Microsoft Teams pro vaši organizaci nebo uživatele ve vaší organizaci, přečtěte si [Spravujte zásady oprávnění aplikace v Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Viz také

[Stažení a instalace aplikace Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Centrum nápovědy Microsoft Teams](https://support.office.com/teams)</br>
[Aplikace Human Resources v Teams](hr-admin-teams-leave-app.md)
