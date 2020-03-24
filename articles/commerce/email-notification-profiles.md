---
title: Nastavení profilu oznámení e-mailem
description: Toto téma popisuje, jak vytvořit profil oznámení e-mailem v aplikaci Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9e5d90eaf1815bbe54b0bea40d92a0a993a23b75
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113798"
---
# <a name="set-up-an-email-notification-profile"></a>Nastavení profilu oznámení e-mailem


[!include [banner](includes/banner.md)]

Toto téma popisuje, jak vytvořit profil oznámení e-mailem v aplikaci Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Před vytvořením kanálů budete mít možnost nastavit profil, který zajistí, že e-mailová oznámení mohou být odeslána pro různé události, jako je například vytvoření objednávky, stav expedice objednávky a chyba platby.

Další informace o konfiguraci e-mailu naleznete v tématu [Konfigurace a odesílání e-mailu](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="create-an-email-notification-profile"></a>Vytvoření profilu oznámení e-mailem

Chcete-li vytvořit profil oznámení e-mailem, postupujte následujícím způsobem.

1. V navigačním podokně přejděte na **Moduly \> Maloobchodní a velkoobchodní prodej \> Nastavení centrály \> Profil oznámení e-mailem aplikace Commerce**.
1. V podokně akcí klikněte na možnost **Nový**.
1. Do pole **Profil oznámení e-mailem** zadejte název pro identifikaci profilu.
1. Zadejte příslušný popis do pole **Popis**.
1. Nastavení přepínač **Aktivní** na **Ano**.

### <a name="create-an-email-template"></a>Vytvoření šablonu e-mailu

Před vytvořením oznámení e-mailem je nutné vytvořit šablonu e-mailu organizace, která obsahuje e-mailové informace odesílatele a šablonu e-mailu.

Šablonu e-mailu vytvoříte takto:

1. V navigačním podokně přejděte na **Moduly \> Maloobchodní a velkoobchodní prodej \> Nastavení centrály \> Parametry \> E-mailové šablony organizace**.
1. V podokně akcí zvolte **Nový**.
1. V poli **ID e-mailu** zadejte ID, které pomůže identifikovat tuto šablonu.
1. Do pole **Jméno odesílatele** zadejte jméno odesílatele.
1. Zadejte smysluplný popis do pole **Popis e-mailu**.
1. Do pole **E-mail odesílatele** zadejte e-mailovou adresu odesílatele.
1. V části **Obecné** vyplňte veškeré potřebné volitelné informace (jako je například priorita e-mailu).
1. Rozbalte část **Obsah e-mailové zprávy**, zvolte **Nový** a vytvořte obsah šablony. Pro každou položku obsahu vyberte jazyk a zadejte předmět e-mailu. Pokud e-mail bude mít text, zkontrolujte zda je zaškrtnuto políčko **má tělo**.
1. V podokně akcí vyberte **E-mailová zpráva** a zadejte šablonu e-mailového textu.

Následující obrázek ukazuje několik příkladů nastavení šablony e-mailu.

![Nastavení šablony e-mailu](media/email-template.png)

### <a name="create-an-email-event"></a>Vytvoření e-mailové události

E-mailovou událost vytvoříte takto.

1. V navigačním podokně přejděte na **Moduly \> Maloobchodní a velkoobchodní prodej \> Nastavení centrály \> Profil oznámení e-mailem aplikace Commerce**.
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho. 
1. Z rozevíracího seznamu **ID e-mailu** vyberte e-mailovou šablonu.
1. Z rozevíracího seznamu vyberte **Typ oznámení e-mailem**.
1. Zaškrtněte políčko **Aktivní**.
1. V podokně akcí vyberte **Uložit**.

Následující obrázek ukazuje několik příkladů nastavení oznámení události.

![Nastavení oznámení události](media/email-notification-profile.png)

## <a name="additional-resources"></a>Další zdroje

[Konfigurace a odeslání e-mailu](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Přehled kanálů](channels-overview.md)

[Předpoklady nastavení kanálu](channels-prerequisites.md)

[Přehled organizací a organizačních hierarchií](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)