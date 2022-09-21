---
title: Commerce chat s modulem Omnikanál pro Customer Service
description: Tento článek popisuje Commerce Chat s modulem Omnikanál pro Customer Service v Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-07-20
ms.openlocfilehash: b8eaed3eb015e96b1db6fa2297c341ea9d3ff8ad
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473802"
---
# <a name="commerce-chat-with-omnichannel-for-customer-service-module"></a>Commerce chat s modulem Omnikanál pro Customer Service

[!include [banner](includes/banner.md)]

Tento článek popisuje *Commerce Chat s modulem Omnikanál pro Customer Service* v Microsoft Dynamics 365 Commerce.

Ve verzi Commerce 10.0.29 byl do knihovny modulů Commerce přidán nový Commerce Chat s modulem Omnikanál pro Customer Service. Funkce Commerce chat poskytuje zákazníkům elektronického obchodu možnosti chatu Dynamics 365 Omnikanál pro Customer Service, což zahrnuje podporu živého agenta, která pomáhá řešit dotazy zákazníků, poskytovat zákaznický servis a usnadňovat prodej zákazníkům Commerce.

Funkce Commerce chat umožňuje maloobchodníkům dosáhnout těchto cílů:

- Zvyšte personalizovanou interakci se zákazníky, abyste zlepšili udržení zákazníků.
- Zlepšete služby zákazníkům prostřednictvím integrace lidských agentů a samoobslužných chatbotů.
- Pomozte agentům získat zkušenosti prostřednictvím údajů o zákaznických profilech, objednávkách a nákupech v reálném čase, což vede k provozním zlepšením a zapojení.
- Zlepšete celkovou spokojenost zákazníků a pomozte zvýšit prodej.

V rámci funkce Commerce chat jsou k dispozici následující možnosti:

- Commerce chat s Omnikanálem pro Customer Service
- Přidání **Commerce call centrum** jako kartu aplikace v prostředí agenta v Dynamics 365 Omnikanál pro Customer Service

## <a name="prerequisites-for-omnichannel-for-customer-service"></a>Předpoklady pro Omnikanál pro Customer Service

Nezbytným předpokladem je konfigurovat chat ve widgetu pro správu Omnikanálu pro Customer Service a získat některé parametry pro konfiguraci prostředí Commerce chat. Pokyny naleznete v tématu [Konfigurovat kanál chatu](/dynamics365/customer-service/set-up-chat-widget).

Po konfiguraci chatu ve widgetu pro správu Omnikanálu pro Customer Service získáte skript, který se podobá následujícímu příkladu.

`<script id="Microsoft_Omnichannel_LCWidget" src="https://oc-cdn-ocprod.azureedge.net/livechatwidget/scripts/LiveChatBootstrapper.js" data-app-id="xxxx-xxx-4be7-bcd5-1d118ecffe1f" data-org-id="5a0e73c0-xxxx-xxxxx-xxx- 76df135f375d" data-org-url="https://xxsxxxxssdb348f-crm.omnichannelengagementhub.com"></script>`

Zkopírujte tento skript, protože hodnoty v něm budete potřebovat ke konfiguraci modulu chatu.

### <a name="commerce-chat-with-omnichannel-for-customer-service-mandatory-fields"></a>Povinná pole Commerce chat s Omnikanálem pro Customer Service

Následující tabulka ukazuje hodnoty skriptu z widgetu pro správu Omnikanálu pro Customer Service, které jsou nutné ke konfiguraci modulu Commerce Chat s Omnikanálem pro Customer Service.

| Vlastnost widgetu | Popis |
| ------------- |--------------|
| Zdroj skriptu | Hodnota **src** ve skriptu widgetu chatu. |
| ID aplikace dat | Hodnota **data-app-id** ve skriptu widgetu chatu. |
| ID organizace dat | Hodnota **data-org-id** ve skriptu widgetu chatu. |
| URL organizace dat | Hodnota **data-org-url** ve skriptu widgetu chatu. |

## <a name="configure-the-commerce-chat-experience-for-your-e-commerce-site"></a>Nakonfigurujte prostředí Commerce chat pro svůj web elektronického obchodu

Jedním z doporučených způsobů, jak implementovat chat pro váš web elektronického obchodu, je přidat modul Commerce Chat s Omnikanálem pro Customer Service do fragmentu sdíleného záhlaví, který se používá na stránkách vašeho webu elektronického obchodu.

Chcete-li přidat modul chatu do fragmentu záhlaví vašeho webu v nástroji Commerce Site Builder, postupujte takto.

1. V tvůrci webů pro váš web přejděte na **Fragmenty**.
1. Zvolte **Nové**.
1. V dialogovém okně **Vyberte fragment** vyberte modul **Commerce chat s Omnikanálem pro Customer Service**, zadejte název fragmentu a poté vyberte **OK**.
1. V zobrazení osnovy vyberte slot **Konektor chatu Msdyn365 cs**.
1. V podokně **Vlastnosti chatu** napravo postupujte takto:

    1. V poli **Zdroj skriptu** zadejte hodnotu **src**, kterou jste získali ze skriptu Omnikanál pro Customer Service.
    1. V poli **ID aplikace dat** zadejte hodnotu **data-app-id**, kterou jste získali ze skriptu Omnikanál pro Customer Service.
    1. V poli **ID organizace dat** zadejte hodnotu **data-org-id**, kterou jste získali ze skriptu Omnikanál pro Customer Service.
    1. V poli **URL organizace dat** zadejte hodnotu **data-org-url**, kterou jste získali ze skriptu Omnikanál pro Customer Service.

    ![Vytvoření fragmentu modulu Commerce Chat v Commerce Site Builder.](media/Commerce-chat-creating-new-fragment.png)

1. Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.
1. Přejděte na **Fragmenty** a otevřete fragment záhlaví pro váš web.
1. Ve slotu **Výchozí kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat fragment**.
1. V dialogovém okně **Vybrat moduly** vyberte fragment chatu, který jste vytvořili předtím, a pak vyberte tlačítko **OK**.
1. Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.

## <a name="add-commerce-headquarters-as-an-application-tab-for-omnichannel-for-customer-service"></a>Přidejte Commerce headquarters jako kartu aplikace pro Omnikanál pro Customer Service

Můžete přidat kartu aplikace pro Commerce headquarters v Omnikanálu pro Customer Service. Živí agenti pak mohou používat uživatelské rozhraní pro prostředí agenta Omnikanálu pro Customer Service, aby měli snadný přístup k modulu Dynamics 365 Commerce Customer Service, který obsahuje kontextové informace o zákazníkovi spolu s informacemi o jeho prodejních objednávkách. Kromě toho mohou zástupci zákaznických služeb zadávat nové objednávky, iniciovat vracení zboží a ověřovat informace o stavu objednávky.

### <a name="create-a-new-application-tab-that-loads-commerce-headquarters-in-an-iframe-module"></a>Vytvořte novou kartu aplikace, která načte Commerce headquarters v modulu iFrame 

Chcete-li vytvořit novou kartu aplikace, která načte Commerce headquarters v modulu iFrame, postupujte následovně.

1. Otevřete [Power Apps Maker Portal](https://make.powerapps.com).
1. V navigačním podokně nalevo vyberte položku **Aplikace**.
1. Vyberte **Centrum pro správu zákaznických služeb**.
1. Přejděte do **Prostředí agenta**.
1. Pro **Šablony karet aplikace** vyberte **Spravovat**.
1. Vytvořte novou kartu aplikace typu **Web třetí strany**. Pokyny naleznete v [Spravovat šablony karty aplikace](/dynamics365/app-profile-manager/application-tab-templates?tabs=customerserviceadmincenter).
1. V **Parametrech**, v poli **Hodnota** parametru **url** zadejte následující URL, kde `<YourOrganizationHeadquartersURL>` a `<LegalEntityname>` jsou nahrazeny příslušnými hodnotami. Omnikanál pro Customer Service načte **{AccountNumber}** z kontextu chatu. Proto nechte **{AccountNumber}**, jak je.

    `https://<YourOrganizationHeadquartersURL>/?mi=MCRCustomerService&cmp=<LegalEntityName>&embedded=true&customerId={AccountNumber}`

1. Ponechte pole **Hodnota** parametru **data** prázdný.

![Vytvoření karty aplikace v Dynamics 365 Omnichannel Customer Service.](media/OC-CS-Admin-Application-Tab-Parameters.png)

## <a name="enable-a-new-application-tab-for-customer-agents-in-dynamics-365-omnichannel-for-customer-service"></a>Povolte novou kartu aplikace pro zákaznické agenty v Dynamics 365 Omnikanál pro Customer Service

Chcete-li povolit novou kartu aplikace pro zákaznické agenty v Dynamics 365 Omnikanál pro Customer Service, postupujte takto.
    
1. Otevřete [Power Apps Maker Portal](https://make.powerapps.com).
1. V navigačním podokně nalevo vyberte položku **Aplikace**.
1. Vyberte **Centrum pro správu zákaznických služeb**.
1. Přejděte na **Zákaznická podpora \> proudy práce**.
1. Otevřete pracovní proud, který jste vytvořili pro své agenty, a poté v **Pokročilém nastavení** vyberte **Výchozí nastavení relací**.
1. V **Kartách aplikací** vyberte **Přidat existující kartu aplikace** a poté přidejte novou kartu aplikace, kterou jste vytvořili dříve. Tento krok zajistí, že karta aplikace, která načte Commerce headquarters v modulu iFrame se objeví, když agent přijme příchozí chatovací hovor z vašeho webu elektronického obchodu.

## <a name="add-context-variables-in-dynamics-365-omnichannel-for-customer-service"></a>Přidejte kontextové proměnné v Dynamics 365 Omnikanál pro Customer Service

Chcete-li přidat kontextové proměnné v Dynamics 365 Omnikanál pro Customer Service, postupujte takto.

1. Otevřete [Power Apps Maker Portal](https://make.powerapps.com).
1. V navigačním podokně nalevo vyberte položku **Aplikace**.
1. Vyberte **Centrum pro správu zákaznických služeb**.
1. Přejděte na **Zákaznická podpora \> proudy práce**.
1. Otevřete pracovní proud, který jste vytvořili pro své agenty, a poté v **Rozšířeném nastavení** přejděte do sekce **Kontextové proměnné**.
1. Vyberte **Upravit** a poté přidejte **AccountNumber** jako kontextovou proměnnou typu **text**. Tato proměnná pomůže Commerce headquarters načíst informace o zákaznících s odpovídajícími čísly účtů.

> [!NOTE]
> Pokud si chcete přečíst e-mailové adresy a jména přihlášených uživatelů z kanálu elektronického obchodu, můžete přidat **E-mail** a **Jméno** jako kontextové proměnné typu **text** navíc ke kontextové proměnné **AccountNumber**.
