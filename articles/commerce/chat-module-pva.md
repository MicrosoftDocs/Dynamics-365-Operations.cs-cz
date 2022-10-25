---
title: Modul Commerce Chat s Power Virtual Agents
description: Tento článek popisuje Commerce Chat s modulem Power Virtual Agents, který integruje Microsoft Power Virtual Agents s weby Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-07
ms.openlocfilehash: 838990cb638479c9c90ba0e38794ecedd55e95b3
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691049"
---
# <a name="commerce-chat-with-power-virtual-agents-module"></a>Modul Commerce Chat s Power Virtual Agents

[!include [banner](includes/banner.md)]

Tento článek popisuje Commerce Chat s modulem Power Virtual Agents, který integruje Microsoft Power Virtual Agents s weby Dynamics 365 Commerce.

Commerce Chat s Power Virtual Agents umožňuje zákazníkům elektronického obchodování Dynamics 365 používat možnosti chatbota Power Virtual Agents a zpracovávat jejich dotazy. Od Dynamics 365 Commerce verze 10.0.30 lze tuto funkci začlenit do webových stránek elektronického obchodu pomocí modulu Commerce Chat s Power Virtual Agents, který je součástí knihovny modulů Commerce.

Commerce Chat s Power Virtual Agents pomáhá podnikům dosáhnout následujících cílů:

- Zvyšte personalizovanou interakci se zákazníky a zlepšete udržení zákazníků.
- Zlepšete služby zákazníkům prostřednictvím integrace samoobslužných chatbotů.
- Zlepšete celkovou spokojenost zákazníků a pomozte tak zvýšit prodej.

> [!NOTE]
> Chcete-li se dozvědět o rozdílech mezi Omnikanálem pro Customer Service Dynamics 365 a aplikacemi Power Virtual Agents, viz [Přehled modulů pro Commerce Chat](/commerce-chat-modules-overview.md).

## <a name="prerequisites-for-using-power-virtual-agents"></a><a id="prereq"></a>Požadavky na používání Power Virtual Agents

Chcete-li používat Commerce Chat s Power Virtual Agents, musíte nejprve vytvořit chatbota Power Virtual Agents pro váš web elektronického obchodu. Pokyny viz [Vytvořte robota Power Virtual Agent](/power-virtual-agents/authoring-first-bot).

Po konfiguraci chatbota musíte zkopírovat hodnoty parametrů chatbota **ID robota** a **ID tenanta** pro konfiguraci prostředí Commerce chat. Informace o kopírování těchto hodnot naleznete v části [Získejte parametry botů Power Virtual Agents](/power-virtual-agents/publication-connect-bot-to-custom-application#retrieve-your-power-virtual-agents-bot-parameters).

## <a name="configure-your-e-commerce-site"></a>Konfigurace webu elektronického obchodu 

Jedním z doporučených způsobů, jak implementovat chat pro váš web elektronického obchodu, je přidat modul Commerce Chat s Power Virtual Agents do fragmentu sdíleného záhlaví, který se používá na stránkách vašeho webu.

Chcete-li přidat modul chatu do fragmentu záhlaví vašeho webu v nástroji Commerce Site Builder, postupujte takto.

1. V tvůrci webů Commerce pro váš web přejděte na **Fragmenty**.
1. Zvolte **Nové**.
1. V dialogovém okně **Vyberte fragment** vyberte modul **Commerce chat s Power Virtual Agents**, zadejte název fragmentu a poté vyberte **OK**.
1. V zobrazení osnovy vyberte slot **Konektor chatu Msdyn365 pva**.
1. V podokně vlastnosti napravo postupujte takto:

    1. V **Parametry robota** v poli **Bot Framework Webchat chat CDN URL** ponechte výchozí hodnotu (např. `https://cdn.botframework.com/botframework-webchat/latest/webchat.js`).
    1. V poli **Bot Framework Direct Line Autentizační URL** ponechte výchozí hodnotu (např. `https://powerva.microsoft.com/api/botmanagement/v1/directline/directlinetoken`).
    1. V poli **ID robota** zadejte hodnotu Power Virtual Agents **ID robota**, kterou jste zkopírovali v sekci [Požadavky na použití Power Virtual Agents](#prereq).
    1. V poli **ID tenanta** zadejte hodnotu **ID tenanta**, kterou jste zkopírovali.

1. Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.
1. Přejděte na **Fragmenty** a otevřete fragment záhlaví pro váš web.
1. Ve slotu **Výchozí kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat fragment**.
1. V dialogovém okně **Vybrat moduly** vyberte fragment chatu, který jste vytvořili předtím, a pak vyberte tlačítko **OK**.
1. Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.

## <a name="proactive-chat-parameters"></a>Proaktivní parametry chatu

Úplný seznam parametrů proaktivní konfigurace chatu viz [Proaktivní parametry chatu modulu Commerce Chat](chat-proactive-chat-parameters.md).

> [!NOTE]
> Aktuálně Power Virtual Agents nepodporují autentizaci Azure Active Directory B2C (Azure AD B2C). Podporuje pouze anonymní volání Retail Cloud Scale Unit (RCSU) pro získání dostupnosti produktu nebo interakce s jinými anonymními API. Volání na ověřená rozhraní API prostřednictvím chatbotů Power Virtual Agents vyžadují explicitní přihlášení zákazníka.

## <a name="additional-resources"></a>Další prostředky

[Přehled funkcí chatu Commerce](commerce-chat-overview.md)

[Commerce chat s modulem Omnikanál pro Customer Service](commerce-chat-module.md)

[Proaktivní parametry chatu modulu Commerce Chat](chat-proactive-chat-parameters.md)
