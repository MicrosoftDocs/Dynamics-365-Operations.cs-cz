---
title: Správa žádostí o dovolenou v aplikaci Teams
description: Toto téma ukazuje, jak požádat o volno v aplikaci Dynamics 365 Human Resources v Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
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
ms.openlocfilehash: 0fbf44fe35af3147fd5fb478b6cbfc5a5d0b109d
ms.sourcegitcommit: 5b620f670ac0f403a0fdcdeb9c3f970b163191ee
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766753"
---
# <a name="manage-leave-requests-in-teams"></a>Správa žádostí o dovolenou v aplikaci Teams

[!include [banner](includes/preview-feature.md)]

Aplikace Microsoft Dynamics 365 Human Resources v aplikaci Microsoft Teams vám umožňuje rychle požádat o volno a zobrazit informace o svém zůstatku volna přímo v Microsoft Teams. Můžete komunikovat s robotem a vyžádat si informace. Karta **Volno** poskytuje podrobnější informace.

## <a name="install-the-app"></a>Instalace aplikace

Aplikaci Human Resources najdete v obchodě Teams.

1. V aplikaci Microsoft Teams zvolte tři tečky.

   ![Tři tečky aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. Vyhledejte Dynamics 365 Human Resources a poté vyberte dlaždici **Human Resources**.

   ![Dlaždice HR aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. Vyberte tlačítko **Přidat** pro instalaci aplikace.

   ![Instalace aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-in-store.png)

Pokud vás aplikace nepřihlásí automaticky, vyberte kartu **Nastavení** pro přihlášení.

![Karta nastavení aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> Pokud nevidíte přihlašovací dialogové okno, zkontrolujte nastavení prohlížeče a povolte automaticky otevíraná okna. 

Pokud máte přístup k více než jedné instanci aplikace Human Resources, můžete vybrat prostředí, ke kterému se chcete připojit, na kartě **Nastavení**.

> [!WARNING]
> Aplikace aktuálně nepodporuje roli zabezpečení správce systému a zobrazí chybovou zprávu, pokud se přihlásíte pomocí účtu správce systému. Chcete-li se přihlásit pomocí jiného účtu, na kartě **Nastavení** vyberte tlačítko **Přepnout účty** a poté se přihlaste pomocí uživatelského účtu, který nemá oprávnění správce systému.
 
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

1. Chcete-li vytvořit novou žádost o volno, zvolte **Nová žádost**.

   ![Nová žádost aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. Zadejte den nebo dny, na které chcete volno, a poté vyberte **Přidat**.

   ![Přidání volna aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. V případě potřeby zadejte kód důvodu. Také zadejte případné komentáře a přidejte všechny přílohy.

4. Až zadáte informace, napište **Odeslat** pro odeslání žádosti ke schválení. Můžete také naspat **Uložit jako koncept** a vrátit se k žádosti později.

### <a name="manage-draft-requests"></a>Správa konceptů žádostí

1. Zvolte kartu **Koncepty**.

   ![Karta konceptů aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. Vyberte symbol tužky, chcete-li žádost upravit, nebo vyberte koš, chcete-li žádost odstranit.

3. Proveďte potřebné změny. Až zadáte informace, napište **Odeslat** pro odeslání žádosti ke schválení. Můžete také zvolit **Uložit jako koncept** a vrátit se k žádosti později.

   ![Úprava konceptu aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="teams-notifications"></a>Oznámení aplikace Teams

Když vy nebo pracovník, jehož jste schvalovatelem, odešlete žádost o pracovní volno, obdržíte oznámení v aplikaci Human Resources v Teams. Chcete-li oznámení zobrazit, vyberte jej. Oznámení se také zobrazují v oblasti **Chat**.

Pokud jste schvalovatel, můžete v oznámení zvolit možnosti **Schválit** nebo **Odmítnout**. Můžete také zadat volitelnou zprávu.

![Oznámení o žádosti o pracovní volno v aplikaci Human Resources Teams](./media/hr-teams-leave-app-notification.png)

## <a name="view-your-teams-leave-calendar"></a>Zobrazení kalendáře pracovního volna týmu

Pokud jste manažer s přímými podřízenými, můžete si prohlédnout schválené a nevyřízené pracovní volno vašeho týmu.

1. V aplikaci Human Resources v Teams vyberte **Volno**.

2. Vyberte **Kalendář týmu**.

   ![Zobrazení kalendáře v aplikaci Human Resources Teams](./media/hr-teams-leave-app-view-calendar.png)

Kalendář zobrazuje schválené a nevyřízené volno vašich přímých podřízených.

![Kalendář volna v aplikaci Human Resources Teams](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

S robotem Dynamics 365 Human Resources v aplikaci Microsoft Teams jsou textové vstupy uživatele analyzovány pro porozumění základním dotazům/záměrům. Vstup uživatele, například „Vyhledat účet Contoso“, je přesměrován na jednu ze služeb Cognitive Services společnosti Microsoft nazvanou Language Understanding Intelligent Service (LUIS). Přečtěte si více o LUIS  [zde](https://www.luis.ai/). Služba LUIS ujasňuje nebo chápe záměr vstupu uživatele (v tomto případě je záměrem najít informace) a cílovou entitu (v tomto případě je zamýšlenou entitou účet s názvem Contoso). Tyto informace jsou poté předány do řešení  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) společnosti Microsoft, které interaguje s daty z Dynamics 365 Human Resources a načte požadované informace pro uživatelský dotaz. 

Instalací a umožněním přístupu k používání robota souhlasíte s tím, že umožníte službě LUIS a rámci robota Azure zpracovat záměr za vstupem, což má za následek vylepšenou konverzační uživatelskou zkušenost. Služba LUIS a rámec robota Azure mohou mít ve srovnání s Dynamics 365 Human Resources různé úrovně shody. Zatímco služba LUIS má přístup pouze k uživatelským dotazům a není určena k připojení k datům nebo účtu uživatele Dynamics 365 Human Resources, uživatel robota Dynamics 365 Human Resources může dobrovolně zadat dotaz obsahující zákaznická data, osobní údaje nebo jiná data a takový obsah dotazu by mohl být zaslán do služby LUIS a do rámce robota Azure. 

Obsah dotazů a zpráv uživatele je v systému LUIS uchováván maximálně 30 dní, je šifrován a nepoužívá se pro školení ani zlepšení služeb. Přečtěte si více o Cognitive Services  [zde](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Chcete-li spravovat nastavení administrátora pro aplikace v Microsoft Teams, přejděte do [centra pro správu Microsoft Teams](https://admin.teams.microsoft.com/).

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a>Microsoft Azure Event Grid a Microsoft Teams

Při použití funkce oznámení pro aplikaci Dynamics 365 Human Resources v Teams budou některá data zákazníků téct mimo geografickou oblast, kde je nasazena služba Human Resources vašeho klienta. Dynamics 365 Human Resources přenáší podrobnosti o žádosti o pracovní volno a úkolu pracovního postupu do Microsoft Azure Event Grid a Microsoft Teams. Tato data mohou být uložena až 24 hodin a zpracována ve Spojených státech, jsou šifrována během přenosu a v klidu a nejsou používána společností Microsoft nebo jejími subprocesory pro školení nebo vylepšení služeb.

## <a name="see-also"></a>Viz také

[Stažení a instalace aplikace Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Centrum nápovědy Microsoft Teams](https://support.office.com/teams)</br>
[Aplikace Human Resources v Teams](hr-admin-teams-leave-app.md)
