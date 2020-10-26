---
title: Aplikace Human Resources v Teams
description: V tomto tématu se seznámíte s aplikací Microsoft Dynamics 365 Human Resources v aplikaci Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51f04e553da822c4e09d31bcd72c71b674ad1f1b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930010"
---
# <a name="human-resources-app-in-teams"></a>Aplikace Human Resources v Teams

[!include [banner](includes/preview-feature.md)]

Aplikace Microsoft Dynamics 365 Human Resources v aplikaci Microsoft Teams umožňuje zaměstnancům rychle požádat o volno a zobrazit informace o jejich zůstatku volna v Microsoft Teams. Zaměstnanci mohou komunikovat s robotem a vyžádat si informace. Karta **Volno** poskytuje podrobnější informace. Kromě toho můžou lidem posílat informace o svém nadcházejícím volnu v týmech a chatech mimo aplikaci Human Resources.

![Robot aplikace pracovního volna Human Resources Teams](./media/hr-admin-teams-leave-app-bot.png)

![Karta volna aplikace pracovního volna Human Resources Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![Karta s žádostí o volno v Human Resources](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>Instalace a nastavení

Aplikaci Human Resources najdete v obchodě Teams. Informace o instalaci aplikace Teams najdete v části [Správa žádostí o dovolenou v aplikaci Teams](hr-teams-leave-app.md).

Informace o správě oprávnění k aplikaci v Teams naleznete v části [Správa zásad povolení k aplikaci v Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Povolení oznámení pro aplikaci Human Resources v Teams

Pokud chcete, aby uživatelé dostávali oznámení o žádostech o pracovní volno v aplikaci Teams, musíte povolit oznámení v aplikaci Human Resources.

>[!NOTE]
>Oznámení dostanou pouze uživatelé, kteří jsou přihlášeni k Teams a používají aplikaci Human Resources Teams.

1. V modulu Human Resources vyberte **Správa systému** .

2. Vybrerte **Odkazy** .

3. V části **Nastavení** vyberte **Systémové parametry** .

4. Na kartě **Obecné** nastavte možnost **Povolit oznámení pro aplikaci Teams** na **Ano** .

   ![Povolení oznámení aplikace Teams v systémových parametrech](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Chcete-li zapnout oznámení Teams pro všechny uživatele, při výzvě vyberte **Ano** .

   ![Povolení oznámení Teams pro všechny uživatele](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>Zapnutí nebo vypnutí oznámení aplikace Teams pro jednotlivé uživatele

Jakmile povolíte oznámení pro aplikaci Human Resources Teams, můžete oznámení zapnout nebo vypnout pro jednotlivé uživatele.

1. V modulu Human Resources vyberte **Správa systému** .

2. Vybrerte **Odkazy** .

3. V části **Uživatelé** vyberte **Možnosti uživatele** .

4. Vyberte kartu **Pracovní postup** .

5. Nastavte možnost **Povolit oznámení pro aplikaci Teams** na **Ano** , čímž povolíte oznámení pro uživatele nebo **Ne** , čímž deaktivujete oznámení pro uživatele.

   ![Povolte oznámení aplikace Teams na kartě Možnosti uživatele na kartě Pracovní postup.](./media/hr-admin-teams-leave-app-notifications.png)

6. Zvolte **Uložit** .

## <a name="known-issues"></a>Známé problémy

| Výdej | Stav |
| --- | --- |
| Horizontální posouvání nefunguje na Android telefonech | Horizontální posouvání není problém na zařízeních iOS nebo počítačích. Pracujeme na opravě pro Android. |
| Zůstatek je nesprávný při zadávání volna pro budoucí datum. | Prognózy ještě nejsou k dispozici. Zůstatek se zobrazuje pro aktuální datum. |
| Nelze zrušit požadavek ve stavu **Probíhá kontrola** . | Tato funkce není momentálně podporována a bude přidána v budoucím vydání. |
| Informace o zůstatku se počítají od dnešního dne. | Systém aktuálně nezobrazuje zůstatky od období časového rozlišení, i když je nakonfigurováno v parametrech pracovního volna a absence. |

## <a name="troubleshooting"></a>Řešení potíží

Pokud má uživatel potíže s přihlášením nebo používáním aplikace Human Resources Teams, zkuste problémy vyřešit podle těchto pokynů. Pokud problémy přetrvávají i po pokusu o vyřešení, obraťte se na podporu. Pro další informace si přečtěte [Získání podpory](hr-admin-troubleshooting-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Nelze se přihlásit do aplikace Human Resources v Teams

Pokud vás uživatel kontaktuje, protože se nemůže přihlásit do aplikace, ověřte, zda má přidružený záznam zaměstnance v Human Resources.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Chyba při schvalování žádostí o dovolenou v aplikaci Human Resources v Teams

Pokud se uživateli při pokusu o schválení žádostí o dovolenou v aplikaci Teams zobrazí chyba, proveďte v rámci řešení potíží následující kroky:

1. Ověřte, že jeho účet Teams je stejný, jaký používá pro přístup k Human Resources.

2. Ověřte, zda je platným schvalovatelem požadavku, a to kontrolou nastavení pracovního postupu pro schválení dovolené. Další informace o pracovních postupech žádostí o dovolenou najdete v tématu [Vytvoření pracovního postupu žádosti o dovolenou](hr-leave-and-absence-workflow.md).

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
[Správa žádostí o dovolenou v aplikaci Teams](hr-teams-leave-app.md)

