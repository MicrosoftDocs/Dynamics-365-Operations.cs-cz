---
title: Správa žádostí o dovolenou v aplikaci Teams
description: Toto téma ukazuje, jak požádat o volno v aplikaci Dynamics 365 Human Resources v Microsoft Teams.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2ea495259ba29f302753991e260d5a8fa990322b
ms.sourcegitcommit: e3f11fc9a9dae416a490437678bb482a0094f9a9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2021
ms.locfileid: "5953405"
---
# <a name="manage-leave-requests-in-teams"></a>Správa žádostí o dovolenou v aplikaci Teams

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Aplikace Dynamics 365 Human Resources v aplikaci Microsoft Teams vám umožňuje rychle požádat o volno a zobrazit informace o svém zůstatku volna přímo v Microsoft Teams. Můžete komunikovat s robotem a požádat o informace a zahájit žádost o dovolenou. Karta **Volno** poskytuje podrobnější informace. Kromě toho můžete lidem posílat informace o svém nadcházejícím volnu v Teams a chatech mimo aplikaci Human Resources.

## <a name="install-the-app"></a>Instalace aplikace

Aplikaci Dynamics 365 Human Resources najdete v obchodě Teams.

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

> [!NOTE]
> Aplikace nyní podporuje roli zabezpečení správce systému.
 
## <a name="use-the-bot"></a>Použití robota

Po instalaci aplikace se zobrazí uvítací zpráva, která vás informuje o typech akcí, které může robot provést vaším jménem.

![Uvítací zpráva robota aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> Při první interakci s robotem se možná budete muset přihlásit. Pokud nevidíte přihlašovací dialogové okno, zkontrolujte nastavení prohlížeče a povolte automaticky otevíraná okna.

Můžete požádat robota a následující akce:

- Zahájit žádost o volno za vás.

  ![Zahájení žádosti o volno v chatu Teams](./media/hr-teams-leave-app-initiate.png)

- Chatovací robot za vás vyplní žádost o volno. Vyberte možnost **Požádat o volno** a upravte podrobnosti své žádosti.

  ![Úprava podrobností žádosti o volno](./media/hr-teams-leave-app-details.png)

- Po dokončení úprav podrobností žádosti o volno vyberte **Odeslat** a předejte žádost ke schválení.

  ![Odeslání žádosti o volno](./media/hr-teams-leave-app-submit.png)

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
   
### <a name="respond-to-teams-notifications"></a>Odpovídejte na oznámení týmů

Když vy nebo pracovník, jehož jste schvalovatelem, odešlete žádost o pracovní volno, obdržíte oznámení v aplikaci Human Resources v Teams. Chcete-li oznámení zobrazit, vyberte jej. Oznámení se také zobrazují v oblasti **Chat**.

Pokud jste schvalovatel, můžete v oznámení zvolit možnosti **Schválit** nebo **Odmítnout**. Můžete také zadat volitelnou zprávu.

![Oznámení o žádosti o pracovní volno v aplikaci Human Resources Teams](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a>Pošlete nadcházející informace o volném čase vašim spolupracovníkům

Po instalaci aplikace Human Resources pro Teams můžete snadno poslat informace o svém nadcházejícím volnu svým spolupracovníkům v týmech nebo chatech.

1. V týmu nebo chatu v Teams vyberte tlačítko Human Resources pod oknem chatu.

   ![Tlačítko Human Resources pod oknem chatu](./media/hr-teams-leave-app-chat-button.png)

2. Vyberte žádost o dovolenou, kterou chcete sdílet. Pokud chcete sdílet koncept žádosti o dovolenou, nejprve vyberte **Koncepty**.

   ![Vyberte nadcházející žádost o dovolenou ke sdílení](./media/hr-teams-leave-app-chat-search.png)

Vaše žádost o dovolenou se zobrazí v chatu.

![Karta s žádostí o volno v Human Resources](./media/hr-teams-leave-app-chat-card.png)

Pokud jste sdíleli koncept žádosti, zobrazí se jako koncept:

![Karta s konceptem žádosti o volno v Human Resources](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a>Zobrazení kalendáře pracovního volna týmu

Pokud jste manažer s přímými podřízenými, můžete si prohlédnout schválené a nevyřízené pracovní volno vašeho týmu.

1. V aplikaci Human Resources v Teams vyberte **Volno**.

2. Vyberte **Kalendář týmu**. Kalendář zobrazuje schválené a nevyřízené volno vašich přímých podřízených.

   ![Zobrazení kalendáře v aplikaci Human Resources Teams](./media/hr-teams-leave-app-view-calendar.png)

   > [!NOTE]
   > Pokud týmový kalendář nevidíte, požádejte správce o jeho aktivaci. Další informace naleznete v tématu [Instalace a nastavení](hr-admin-teams-leave-app.md#install-and-setup).

## <a name="supported-languages"></a>Podporované jazyky

Aplikace Dynamics 365 Human Resources v Teams podporuje následující jazyky:

| ID národního prostředí | Jazyk |
| --- | --- |
| de-DE | Němčina (Německo) |
| es-ES | Španělština (Španělsko) |
| es-MX | Španělština (Mexiko) |
| fr-CA | Francouzština (Kanada) |
| fr-FR | Francouzština (Francie) |
| it-IT | Italština (Itálie) |
| nl-NL | Holandština (Nizozemsko) |
| pt-BR | Portugalština (Brazílie) |
| tr-TR | Turečtina (Turecko) |
| zh-CN | Čínština (zjednodušená) |

## <a name="troubleshooting"></a>Řešení potíží

Pokud máte potíže s přihlášením nebo používáním aplikace Dynamics 365 Human Resources Teams, zkuste problémy vyřešit podle těchto pokynů. Pokud problémy přetrvávají i po pokusu o vyřešení, obraťte se na podporu. Pro další informace si přečtěte [Získání podpory](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Nelze se přihlásit do aplikace Human Resources v Teams

Pokud se nemůžete do aplikace přihlásit, je možné, že účet, pomocí kterého se přihlašujete do Microsoft Teams není spojen se záznamem zaměstnance v Dynamics 365 Human Resources. Požádejtea správce systému o ověření, jestli je váš záznam zaměstnance správně přidružen.

### <a name="translations-dont-display-correctly"></a>Překlady se nezobrazují správně

Pokud se překlady nezobrazují podle očekávání, ujistěte se, že jazyk, který vyberete v Teams, odpovídá jazyku vybranému v **Možnostech uživatele** Human Resources.

V Teams se podívejte na pole **Jazyk aplikace** v **Nastavení**.

![Nastavení Teams](./media/hr-teams-leave-app-settings.png)

V Human Resources vyberte **Nastavení** a poté vyberte **Možnosti uživatele**. Ověřte, že pole **Jazyk** odpovídá poli **Jazyk aplikace** v Teams.

![Možnosti uživatele v Human Resources](./media/hr-teams-leave-app-user-options.png)

Pokud problémy s překladem přetrvávají, dejte nám vědět. Informace najdete v tématu [Získání podpory pro aplikace Finance and Operations nebo Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Chyba při schvalování žádostí o dovolenou v aplikaci Human Resources v Teams

Pokud se vám při pokusu o schválení žádostí o dovolenou v aplikaci Teams zobrazí chyba, zkuste v rámci řešení potíží následující kroky:

1. Ověřte, že účet, který používáte k přihlášení k Microsoft Teams, je stejný, jaký používáte pro přístup k Dynamics 365 Human Resources.

2. Ověřte, jestli jste platným schvalovatelem požadavku, a to kontrolou nastavení pracovního postupu pro schválení dovolené. Další informace o pracovních postupech žádostí o dovolenou najdete v tématu [Vytvoření pracovního postupu žádosti o dovolenou](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Schvalovatelé dovolené nedostávají zprávy chatu Teams ke schválení žádostí o dovolenou

1. Zajistěte, aby byla povolena oznámení pro prostředí a uživatele. Další informace viz [Povolení oznámení pro aplikaci Human Resources v Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) a [Zapnutí nebo vypnutí oznámení aplikace Teams pro jednotlivé uživatele](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Ujistěte se, že jsou uživatelé přihlášeni ke kartě **Chaty** se stejnými přihlašovacími údaji, které používají pro schvalování žádostí o dovolenou. Pomocí zpráv „odhlásit se“ a poté „přihlásit“ se přihlaste se správnými přihlašovacími údaji.

3. Pokud problém přetrvává, zkontrolujte stav dávkové úlohy systému Business Events jako správce systému. Pokud je ve fázi čekání nebo provádění, zkuste to znovu za několik minut. Pokud se stav nezmění, přihlaste se na lístek podpory, aby náš tým mohl problém vyřešit.

## <a name="known-accessibility-issues"></a>Známé problémy s usnadněním

Aplikace Human Resources v Teams má následující problémy s usnadněním, na jejichž řešení pracujeme pro budoucí verze.

| Výdej | Řešení nebo vysvětlení |
| --- | --- |
| Zvětšení plochy o 400 % skryje některá tlačítka akcí. | Doporučujeme místo toho používat lupu, dokud nebudeme moci tuto úroveň zvětšení podporovat. |
| Na kartě **Volno** hlasový komentář oznamuje akci tlačítka při čtení záhlaví mřížky volna. | Záhlaví a prvky v mřížce jsou seskupeny podle roku a jsou sbalitelné. Komentář to interpretuje jako položku s akcemi, kterou ale není. |
| Na kartě **Volno** je při přechodu na **Kód důvodu** v nové žádosti potřeba potáhnutí prstem navíc. | Neexistuje žádný skrytý ovládací prvek, ke kterému se potáhnutí prstem pokouší dostat. |
| Na kartě **Volno**, pokud potáhnete prstem, když je kalendář otevřený, skončíte mimo ovládací prvek namísto horní části v nové žádosti nebo během úpravy požadavku. | Když dosáhnete položky **Přejít na dnešek**, považujte to za konec ovládacího prvku a potáhnutím prstem opačným směrem se dostanete zpět nahoru. |
| Na kartě **Chat**, když zadáte datum při používání asistenčního nástroje nebo navigace pomocí klávesnice, přeskočí fokus zpět na začátek. | Stiskněte klávesu Tab, dokud se znovu nedostanete do oblasti zadávání. |

## <a name="privacy-notice"></a>Oznámení o ochraně osobních údajů

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoft Language Understanding Intelligent Service (LUIS)

S robotem Dynamics 365 Human Resources v aplikaci Microsoft Teams jsou textové vstupy uživatele analyzovány pro porozumění základním dotazům/záměrům. Vstup uživatele, například „Vyhledat účet Contoso“, je přesměrován na jednu ze služeb Cognitive Services společnosti Microsoft nazvanou Language Understanding Intelligent Service (LUIS). Přečtěte si více o LUIS  [zde](https://www.luis.ai/). Služba LUIS ujasňuje nebo chápe záměr vstupu uživatele (v tomto případě je záměrem najít informace) a cílovou entitu (v tomto případě je zamýšlenou entitou účet s názvem Contoso). Tyto informace jsou poté předány do řešení  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/) společnosti Microsoft, které interaguje s daty z Dynamics 365 Human Resources a načte požadované informace pro uživatelský dotaz. 

Instalací a umožněním přístupu k používání robota souhlasíte s tím, že umožníte službě LUIS a rámci robota Azure zpracovat záměr za vstupem, což má za následek vylepšenou konverzační uživatelskou zkušenost. Služba LUIS a rámec robota Azure mohou mít ve srovnání s Dynamics 365 Human Resources různé úrovně shody. Zatímco služba LUIS má přístup pouze k uživatelským dotazům a není určena k připojení k datům nebo účtu uživatele Dynamics 365 Human Resources, uživatel robota Dynamics 365 Human Resources může dobrovolně zadat dotaz obsahující zákaznická data, osobní údaje nebo jiná data a takový obsah dotazu by mohl být zaslán do služby LUIS a do rámce robota Azure. 

Obsah dotazů a zpráv uživatele je v systému LUIS uchováván maximálně 30 dní, je šifrován a nepoužívá se pro školení ani zlepšení služeb. Přečtěte si více o Cognitive Services  [zde](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Chcete-li spravovat nastavení administrátora pro aplikace v Microsoft Teams, přejděte do [centra pro správu Microsoft Teams](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams  Azure Event Grid a Azure Cosmos DB

Při použití aplikace Dynamics 365 Human Resources v Microsoft Teams mohou některá data zákazníků téct mimo geografickou oblast, kde je nasazena služba Human Resources vašeho klienta.

Dynamics 365 Human Resources přenáší podrobnosti o žádosti o pracovní volno a úkolu pracovního postupu do Microsoft Azure Event Grid a Microsoft Teams. Tato data mohou být uložena v Event Grid Microsoft Azure až 24 hodin a budou zpracována ve Spojených státech, jsou šifrována během přenosu a v klidu a nejsou používána společností Microsoft nebo jejími subprocesory pro školení nebo vylepšení služeb. Chcete-li zjistit, kde jsou vaše data uložena v Teams, přečtěte si [Umístění dat v Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).

Při konverzaci s chatovacím robotem v aplikaci Human Resources může být obsah konverzace uložen v Azure Cosmos DB a přenesen do Microsoft Teams. Tato data mohou být uložena v Azure Cosmos DB po dobu až 24 hodin a mohou být zpracovávána mimo geografickou oblast, kde je nasazena služba Human Resources vašeho nájemce, je šifrována během přenosu a v klidu a není používána společností Microsoft nebo jejími subprocesory pro školení nebo vylepšení služeb. Chcete-li zjistit, kde jsou vaše data uložena v Teams, přečtěte si [Umístění dat v Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).
 
Chcete-li omezit přístup k aplikaci Human Resources v Microsoft Teams pro vaši organizaci nebo uživatele ve vaší organizaci, přečtěte si [Spravujte zásady oprávnění aplikace v Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Viz také

[Stažení a instalace aplikace Microsoft Teams](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Centrum nápovědy Microsoft Teams](https://support.office.com/teams)</br>
[Aplikace Human Resources v Teams](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]